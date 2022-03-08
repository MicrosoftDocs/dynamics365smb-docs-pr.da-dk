---
title: Designoplysninger – Bogføring af montageordre | Microsoft Docs
description: Montageordrebogføring er baseret på de samme principper, som når der bogføres lignende aktiviteter af salgsordrer og produktionsforbrug/afgang. Dog kombineres principperne, fordi montageordrer har egen brugergrænseflade til bogføring, ligesom den for salgsordrer, mens faktisk postbogføring sker i baggrunden som direkte vare- og ressourcekladdeposteringer, ligesom for produktionsforbrug, afgang og kapacitet.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 06/08/2021
ms.author: edupont
ms.openlocfilehash: e855a7c1392b84a45c588c8a7dbe01de389a3377
ms.sourcegitcommit: 0953171d39e1232a7c126142d68cac858234a20e
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 06/09/2021
ms.locfileid: "6215999"
---
# <a name="design-details-assembly-order-posting"></a>Designoplysninger: Bogføring af montageordre
Montageordrebogføring er baseret på de samme principper, som når der bogføres lignende aktiviteter af salgsordrer og produktionsforbrug/afgang. Dog kombineres principperne, fordi montageordrer har egen brugergrænseflade til bogføring, ligesom den for salgsordrer, mens faktisk postbogføring sker i baggrunden som direkte vare- og ressourcekladdeposteringer, ligesom for produktionsforbrug, afgang og kapacitet.  

I lighed med produktionsordrebogføring bliver de forbrugte komponenter og de anvendte ressourcer konverteret og udlæst som montagevare, når montageordren er bogført. Du kan finde flere oplysninger i [Designoplysninger: Bogføring af produktionsordre](design-details-production-order-posting.md). Men montageordrers kost-flow er mindre kompliceret, især fordi montageomkostninger kun bogføres én gang og derfor ikke opretter lageret for igangværende arbejde.  

Følgende kladdeposteringer, der opstår under montageordrebogføring:  

-   Varekladden bogfører positive vareposter, der repræsenterer afgang af montageelementet, fra montageordrehovedet.  
-   Varekladden bogfører negative vareposter, der repræsenterer forbrug af montagekomponenter fra montageordrelinjerne.  
-   Ressourcekladden bogfører forbruget af montageressourcer (tidsenheder) fra montageordrelinjerne.  
-   Kapacitetskladden bogfører værdiposter, der vedrører ressourceforbrug, fra montageordrelinjerne.  

I følgende diagram vises strukturen af vare- og ressourceposter, der stammer fra bogføring af montageordren.  

![Vare, ressource og kapacitetsposter som følge af montageordrebogføring](media/design_details_assembly_posting_1.png "Vare, ressource og kapacitetsposter som følge af montageordrebogføring")  

> [!NOTE]  
>  Produktionsressourcer og arbejdscentre er medtaget for at illustrere, at der oprettes kapacitetsposter fra både produktion og montage.  

I følgende diagram vises, hvordan montagedata flyder ind i vareposter ved bogføring:  

![Montagerelateret posteringsflow under bogføring](media/design_details_assembly_posting_2.png "Montagerelateret posteringsflow under bogføring")  

## <a name="posting-sequence"></a>Bogføringssekvens  
Bogføringen af en montageordre forekommer i følgende rækkefølge:  

1.  Montageordrelinjerne bogføres.  
2.  Montageordrehovedet bogføres.  

Følgende tabel beskriver sekvensen af handlinger.  

|Handling|Beskrivelse|  
|------------|-----------------|  
|Initialiser bogføring|1. Foretag forudgående kontrol.<br />2. Tilføj bogføringsnummer, og rediger montageordrehovedet.<br />3. Frigiv montageordrer.|  
|Post|<ol><li>Opret det bogførte montageordrehoved.</li><li>Kopier bemærkningslinjer</li><li>Bogfør montageordrelinjer (forbrug):<br /><br /> <ol><li>Opret en statusside til beregning af montageforbrug.</li><li>Få det resterende antal, som varekladdelinjen baseres på.</li><li>Nulstil forbrugte og resterende mængder.</li><li>For montageordrelinjer af typen Vare:<br /><br /> <ol><li>Udfyld felter på varekladdelinjen.</li><li>Overfør reservationer til varekladdelinjen.</li><li>Bogfør varekladdelinjen for at oprette poster for varen.</li><li>Opret lagerkladdelinjer, og bogfør dem.</li></ol></li><li>For montageordrelinjer af typen Ressource:<br /><br /> <ol><li>Udfyld felter på varekladdelinjen.</li><li>Bogfør varekladdelinjen. Dette opretter kapacitetsposter.</li><li>Opret og bogfør ressourcekladdelinje.</li></ol></li><li>Overfør feltværdier fra montageordrelinjen til en nyoprettet bogført montageordrelinje.</li></ol></li><li>Bogfør montageordrehoved (afgang):<br /><br /> <ol><li>Udfyld felter på varekladdelinjen.</li><li>Overfør reservationer til varekladdelinjen.</li><li>Bogfør varekladdelinjen for at oprette poster for varen.</li><li>Opret lagerkladdelinjer, og bogfør dem.</li><li>Nulstil montagemængder og resterende mængder.</li></ol></li></ol>|  

> [!IMPORTANT]  
>  I modsætning til produktionsafgang, der bogføres med forventede omkostninger, bogføres montageafgange med faktiske omkostninger.  

## <a name="cost-adjustment"></a>Omkostningsregulering  
 Når der bogføres en montageordre, hvilket betyder, at komponenter (materiale) og ressourcer samles i en ny vare, skal det være muligt at bestemme den faktiske kostpris af montageelementet og den faktiske lageromkostning for de involverede komponenter. Dette opnås ved overførsel af omkostninger fra de bogførte poster i kilden (komponenter og ressourcer) til de bogførte poster på destinationen (montageelementet). Videresendelse af omkostninger sker ved beregning og oprettelse af nye poster, der kaldes reguleringsposter, der bliver knyttet til destinationsposterne.  

 Montageomkostninger, der skal videresendes, registreres med registreringsmekanismen for ordreniveau. Du kan finde oplysninger om andre mekanismer til registrering af regulering i [Designoplysninger: Omkostningsregulering](design-details-cost-adjustment.md).  

### <a name="detecting-the-adjustment"></a>Reguleringsregistrering  
Funktionen til registrering af ordreniveau bruges i konverteringsscenarier, produktion og montage. Funktionen fungerer på følgende måde:  

-   Omkostningsregulering registreres ved at markere ordren, når et materiale eller en ressource bogføres som forbrugt.  
-   Omkostninger overføres ved at anvende omkostningerne fra materialet/komponenten på de afgangsposter, der er tilknyttet samme ordre.  

I følgende illustration vises reguleringspoststrukturen, og hvordan montagekostpriser reguleres.  

![Montagerelateret posteringsflow under omkostningstilpasning](media/design_details_assembly_posting_3.png "Montagerelateret posteringsflow under bogføring")  

### <a name="performing-the-adjustment"></a>Udførelse af regulering  
Spredningen af registrerede justeringer fra materiale- og ressourceomkostninger på montageafgangsposter er udført af kørslen **Reguler kostværdi – vareposter**. Den indeholder funktionen Foretag justering af flere niveauer, som består af følgende to elementer:  

-   Foretag justering af montageordre – der videresender omkostninger fra materiale- og ressourceforbrug til montagens afgangspost. Linje 5 og 6 i nedenstående algoritme er ansvarlige for dette.  
-   Foretag reguleringer af enkelt niveau – som videresender omkostninger for individuelle varer, der benytter deres kostmetode. Linje ni og 10 i nedenstående algoritme er ansvarlige for dette.  

![Oversigt over omkostningstilpasningsalgoritmen til montagebogføring](media/design_details_assembly_posting_4.jpg "Oversigt over omkostningstilpasningsalgoritmen til montagebogføring")  

> [!NOTE]  
>  Elementet til justeringer af igangværende arbejde på linje 7 og 8 er ansvarlig for videresendelse af materiale til produktion og udnyttelse af kapaciteten til output af ikke-færdige produktionsordrer. Dette kan ikke bruges ved regulering af montageordreomkostninger, da begrebet Igangværende arbejde ikke gælder for montage.  

Du kan finde flere oplysninger om, hvordan omkostninger fra produktion og montage bogføres i finansregnskabet, i [Designoplysninger: Varekladde](design-details-inventory-posting.md).  

## <a name="assembly-costs-are-always-actual"></a>Montageomkostninger er altid faktiske omkostninger  
 Begrebet igangværende arbejde (VIA) gælder ikke i montageordrebogføring. Montageomkostninger bogføres kun som faktiske omkostninger, aldrig som forventede omkostninger. Du kan finde flere oplysninger i [Designoplysninger: Bogføring af forventet kostpris](design-details-expected-cost-posting.md).  

Dette aktiveres ved følgende datastruktur.  

-   I feltet **Type** på varekladdelinjer i tabellerne **Kapacitetspost** og **Værdipost** bruges *Ressource* til at identificere ressourceposter for montage.  
-   I feltet **Vareposttype** på varekladdelinjer i tabellerne **Kapacitetspost** og **Værdipost** bruges, *Montageafgang* og *Montageforbrug* til henholdsvis at identificere vareposter for afgangsmontage og de brugte montagekomponenter.  

Desuden bogføres gruppefelter på montageordrehovedet og montageordrelinjerne som standard på følgende måde.  

|Enhed|Type|Bogføringsgruppe|Finans- Produktbogføringsgruppe|  
|------------|----------|-------------------|------------------------------|  
|Montageordrehoved|Vare|Varebogføringsgruppe|Finans- Produktbogføringsgruppe|  
|Montageordrelinje|Vare|Varebogføringsgruppe|Finans- Produktbogføringsgruppe|  
|Montageordrelinje|Ressource||Finans- Produktbogføringsgruppe|  

Derfor er det kun faktiske omkostninger, der bogføres i Finans, og der udfyldes ingen mellemregningskonto fra montageordrebogføring. Du kan finde flere oplysninger i [Designoplysninger: Konti i Finans](design-details-accounts-in-the-general-ledger.md).  

## <a name="assemble-to-order"></a>Montage til ordre  
Den varepost, der er resultatet af bogføring af et ordremontagesalg, bliver fast udlignet med den relaterede varepost for montageafgangen. På samme måde er kostprisen for et montage efter ordre-salg afledt fra den montageordre, den var knyttet til.  

Vareposter af typen Salg, der stammer fra bogføring af montage til ordre-mængder, der er markeret med **Ja** i feltet **Montage til ordre**.  

Bogføring af salgsordrelinjer, hvor en del er lagerbeholdningen, og en anden del er montage til ordre-antallet, resulterer i separate vareposter, én for lagerbeholdningen og én for montage til ordre-antallet.  

## <a name="see-also"></a>Se også  
 [Designoplysninger: Lagerkostmetode](design-details-inventory-costing.md)   
 [Designoplysninger: Bogføring af produktionsordre](design-details-production-order-posting.md)   
 [Designoplysninger: Kostmetoder](design-details-costing-methods.md)  
 [Administrere lageromkostninger](finance-manage-inventory-costs.md)  
 [Finans](finance.md)  
 [Arbejde med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]