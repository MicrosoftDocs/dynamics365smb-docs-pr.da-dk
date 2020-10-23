---
title: Sådan oprettes serviceordrer | Microsoft Docs
description: Du kan bruge siden **Serviceordre** til at oprette dokumenter, hvor du indtaster oplysninger om en serviceydelse, f.eks. reparation og vedligeholdelse, for serviceartikler efter kundeforespørgsel.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: 4f2f9602cb050639651a17ea6728eb40762f1ea6
ms.sourcegitcommit: ddbb5cede750df1baba4b3eab8fbed6744b5b9d6
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 10/01/2020
ms.locfileid: "3918684"
---
# <a name="create-service-orders"></a>Oprette serviceordrer
Du kan bruge siden **Serviceordre** til at oprette dokumenter, hvor du indtaster oplysninger om en serviceydelse, f.eks. reparation og vedligeholdelse, for serviceartikler efter kundeforespørgsel.  

Når du opretter en serviceordre, behøver du kun at udfylde nogle få felter. Nogle felter er valgfri, og mange udfyldes automatisk, når du udfylder relaterede felter.  

## <a name="to-create-a-service-order"></a>Sådan oprettes en serviceordre    
1. Vælg ikonet ![Elpære, der åbner funktionen Fortæl mig](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig"), angiv **Serviceordrer**, og vælg derefter det relaterede link.  
2. Opret en ny serviceordre.  
3. I feltet **Nummer** skal du indtaste nummeret på serviceordren.  

     Hvis du har oprettet en nummerserie til serviceordrer på siden **Serviceopsætning**, kan du også trykke på Enter for at vælge det næste ledige serviceordrenummer.  

4. I feltet **Debitornr.** skal du markere den relevante debitor på listen. De kunderelevante felter bliver automatisk udfyldt med oplysninger fra tabellen **Debitor**.  

5. Afhængig af indstillingerne i oversigtspanelet **Obligatoriske felter** på siden **Serviceopsætning** kan det være nødvendigt at udfylde feltet **Serviceordretype** og feltet **Sælgerkode**.  
6. Det er valgfrit, om du vil udfylde resten af felterne.  
7. Registrer serviceartikellinjerne.  

## <a name="to-create-a-service-order-from-a-contract"></a>Sådan oprettes serviceordrer fra kontrakter  
Du kan automatisk oprette serviceordrer til reparation af serviceartikler baseret på servicekontrakter.  

1. Vælg ikonet ![Elpære, der åbner funktionen Fortæl mig](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig"), angiv **Opret kontraktserviceordrer**, og vælg derefter det relaterede link.  
2. Angiv de ønskede filtre i oversigtspanelet **Servicekontrakthoved**.  
3. Gå til oversigtspanelet **Indstillinger**, og udfyld felterne **Startdato** og **Slutdato** med start- og slutdatoen for den periode, du vil oprette kontraktserviceordrer for. Ved kørslen oprettes serviceordrer, som omfatter serviceartikler i servicekontrakter, med de næste planlagte servicedatoer inden for denne periode.  

    > [!NOTE]  
    >  Der er en grænse for det antal dage, du kan bruge som datointerval, hver gang du bruger denne kørsel. Du angiver denne grænse i feltet **Maks. dage for ordreoprettelse** på siden **Serviceopsætning**.  

4. I feltet **Handling** skal du vælge **Opret serviceordre**.  
    > [!NOTE]  
    >  Du kan ikke oprette en ordre med flere serviceartikler, hvis du indstiller feltet  **Én serviceart.linje pr. ordre** på siden **Serviceopsætning**. 

## <a name="to-convert-a-service-quote-to-a-service-order"></a>Sådan konverteres servicetilbud til serviceordrer
Når en kunde har accepteret et servicekontrakttilbud, skal du konvertere det til en serviceordre. Tilbuddet slettes, og der oprettes en ny serviceordre med samme beskrivelse som servicetilbuddet. Serviceordrens svardato og -tidspunkt genberegnes, og status angives til **Igangsat**. Reparationsstatus for serviceartiklerne i ordren ændres til **Ingen tidl. serv**.  

[!INCLUDE[d365fin](includes/d365fin_md.md)] søger allokeringsposter for alle de serviceartikler i servicetilbuddet, der har status **Aktiv**. Hvis der bliver fundet sådanne allokeringsposter, opdateres deres allokeringsstatus til **Genallokering nødvendig**. Når du genallokerer artiklerne i serviceordren, opdateres status for de allokeringsposter, der er registreret for tilbuddet, til **Udført.**   

1. Vælg ikonet ![Elpære, der åbner funktionen Fortæl mig](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig"), angiv **Servicekontrakttilbud**, og vælg derefter det relaterede link.  
2. Vælg det servicetilbud, der skal konverteres til en serviceordre.  
3. Vælg handlingen **Lav ordre**.  

## <a name="to-check-item-availability-for-one-or-more-orders"></a>Sådan kontrolleres varetilgængelighed for en eller flere ordrer  
Du kan kontrollere og se, hvis en vare, som du skal udføre en ordre for, er på lager, og hvis ikke, når varen er på lager. Hvis en vare kan reserveres, kan du reservere den for at sikre, at den er tilgængelig til brug. Du kan kontrollere tilgængeligheden for en bestemt ordre eller for alle ordrer.  

1.  Vælg ikonet ![Elpære, der åbner funktionen Fortæl mig](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig"), angiv **Ordreoversigt**, og vælg derefter det relaterede link.  
2. Gør ét af følgende:  

    * Hvis det drejer sig om en bestemt ordre, skal du vælge ordren og derefter vælge handlingen **Behovsoversigt**.  
    * Drejer det sig om alle ordrer, skal du vælge **Vis bilag**. Siden **Serviceordre** åbnes.  

3. Udvid varegrupperingen og få vist oplysninger om tilgængeligheden af varen på siden **Behovsoversigt**. Du kan f.eks. se, hvor mange varer der er på lager. Du kan også se, hvis og når en vare bliver tilgængelig, hvis den er i restordre, dvs. er Kildetype = Køb, eller om den er reserveret.

## <a name="to-reserve-an-item-for-a-service-order"></a>Sådan reserverer du en vare til en serviceordre
Hvis du har brug at sikre, at en vare er disponibel for en serviceordre, kan du reservere varen.

1. I feltet **Søg** skal du indtaste **Serviceordrer** og derefter vælge det relaterede link.  
2. Vælg serviceordren, og vælg derefter **Rediger**.  
3. Vælg **Handlinger**, vælg **Ordre**, og vælg derefter **Servicelinjer**.  
4. På siden **Servicelinjer** skal du vælge den vare, som skal reserveres, og derefter vælge handlingen **Reserver**.  
5. På siden **Reservation** skal du vælge **Reserver fra aktuel linje**.

## <a name="to-insert-lines-based-on-standard-service-codes"></a>Sådan indsættes linjer baseret på standardservicekoder  
Hvis du har defineret standardservicekoder og tildelt dem til serviceartikelgrupper, kan du indsætte de standardlinjer, der er knyttet til standardservicekoderne i servicedokumenter. Du kan finde flere oplysninger i [Definere standardservicekoder](service-how-setup-service-coding.md).   

1. Vælg ikonet ![Elpære, der åbner funktionen Fortæl mig](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig"), angiv **Serviceordrer**, og vælg derefter det relaterede link.  
2. Opret en ny serviceordre.  
3. Udfyld felterne efter behov.  
4. Udfyld serviceartikellinjerne med de ønskede oplysninger.  
5. Vælg linjen med den serviceartikel, du vil oprette servicelinjer til, og vælg derefter **Hent std.servicekoder**. Siden **Koder til standardserv.varegrupper** vindue åbnes med standardkoderne for den serviceartikelgruppe, der er angivet på linjen.  
6. Vælg den relevante kode, og vælg knappen **OK** for at indsætte standardservicelinjer.  

> [!NOTE]  
>  Hvis feltet **Serviceartikelgruppekode** på serviceartikellinjen i dokumentet er tomt, betyder det, at serviceartiklen ikke hører til nogen serviceartikelgruppe. I dette tilfælde indeholder siden **Koder til standardserv.varegrupper** en liste over alle standardservicekoder. Du skal vælge på listen til at indsætte standardservicelinjer i dokumentet. Du kan også vælge på listen over standardservicekoder, der er tildelt til en bestemt serviceartikelgruppe. Du kan få vist listen ved at markere den relevante kode i feltet **Serviceartikelgruppekode** på siden **Koder til standardserv.varegrupper**.  

## <a name="to-register-internal-or-public-comments"></a>Sådan registreres interne eller offentlige bemærkninger
Du kan tilføje bemærkninger, der udskrives på serviceordrer og servicetilbud, for at angive yderligere oplysninger. Du kan tilføje op til 80 tegn inkl. mellemrum. Hvis du har brug for at indtaste mere tekst, skal du vælge en anden linje. Når du vil registrere en bemærkning, skal du vælge en linje og derefter vælge handlingen **Bemærkninger**.  

## <a name="to-delete-invoiced-service-orders"></a>Sådan slettes fakturerede serviceordrer  
Ordrer slettes som regel automatisk, når de er faktureret fuldt ud. Når en faktura bogføres, oprettes der en tilsvarende post på siden **Bogførte servicefakturaer**. Det bogførte dokument kan ses i på siden **Bogført servicefaktura**.  

Serviceordrer slettes ikke automatisk i programmet, men hvis det samlede antal i ordren er bogført, ikke fra selve serviceordren, men fra siden **Servicefaktura**. Det kan i så fald være nødvendigt at slette fakturerede ordrer, der ikke er slettet. Det kan du gøre ved at aktivere kørslen **Slet fakturerede serviceordrer**.  

1. Vælg ikonet ![Elpære, der åbner funktionen Fortæl mig](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig"), angiv **Slet bogførte kontraktserviceordrer**, og vælg derefter det relaterede link. Kørselsanmodningssiden **Slet fakturerede serviceordrer** åbner.  
2. Når du skal vælge de ordrer, der skal slettes, kan du angive filtre i felterne **Nummer**, **Debitornr.** og **Faktureres til kundenr.** .  
3. Vælg **OK**.  


## <a name="see-also"></a>Se også  
[Bogføring af tjenesten](service-service-posting.md)  
[Bogføre en serviceordre](service-how-to-post-service-orders.md)  
[Konfigurere Service](service-setup-service.md)  
[Arbejde med serviceopgaver](service-how-to-work-on-service-tasks.md)  
[Allokere ressourcer](service-how-to-allocate-resources.md)  
