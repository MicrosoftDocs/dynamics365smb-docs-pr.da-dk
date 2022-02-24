---
title: Brug Momssatsændringsværktøj | Microsoft Docs
description: Brug Momssatsændringsværktøj
author: andregu
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: VAT, posting, tax, value-added tax
ms.date: 04/01/2020
ms.author: andregu
ms.openlocfilehash: 76c6f8902e9661f4f4dbbbf70487a53bf286edb2
ms.sourcegitcommit: 88e4b30eaf6fa32af0c1452ce2f85ff1111c75e2
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 04/01/2020
ms.locfileid: "3183160"
---
# <a name="use-the-vat-rate-change-tool"></a>Brug Momssatsændringsværktøj

## <a name="understanding-the-vat-rate-conversion-process"></a>Forstå processen til konvertering af momssatsændring.  
Momssatsændringsværktøjet udfører momssatskonverteringer for stamdata, kladder og ordrer på forskellige måder. De valgte masterdata og kladder opdateres af den nye generelle produktbogføringsgruppe eller momsproduktbogføringsgruppe. Hvis en ordre er blevet helt eller delvist leveret, bevarer de leverede varer den aktuelle generelle produktbogføringsgruppe eller momsproduktbogføringsgruppe. En ny ordrelinje oprettes for de ikke-leverede varer og opdateres for at justere aktuelle og nye momsbogføringsgrupper eller generelle produktbogføringsgrupper. Desuden opdateres oplysninger om varegebyrtildeling, reservationer og varesporingsoplysninger tilsvarende.  

Der er et par ting, som værktøjet ikke konverterer:

* Salgs- eller købsordrer og fakturaer, hvor leverancer er blevet bogført. Disse dokumenter bogføres ved hjælp af den aktuelle momssats.  
* Dokumenter, der har bogførte forudbetalingsfakturaer. For eksempel har du foretaget eller modtaget forudbetalinger på fakturaer, der ikke er afsluttet, før du bruger momssatsændringsværktøjet. I dette tilfælde vil der være en difference mellem det momsbeløb, der er forfaldent, og den moms, der er betalt i forudbetalinger, når fakturaen er fuldført. Momssatsændringsværktøj springer disse dokumenter over, og du skal opdatere dem manuelt.  
* Direkte leveringer eller specialordrer.  
* Salgs- eller købsordrer med lagerintegration, hvis de er delvist leveret eller modtaget.  
* Servicekontrakter.  

### <a name="to-prepare-vat-rate-change-conversions"></a>Sådan forberedes momssatsændringskonverteringer  
Før du konfigurerer momssatsændringsværktøj, skal du foretage følgende forberedelser.

* Hvis du har transaktioner, der bruger forskellige satser, skal de adskilles i forskellige grupper ved enten at oprette nye finanskonti for hver sats eller ved hjælp af datafiltre til gruppering af transaktioner i henhold til sats.  
* Hvis du opretter nye finanskonti, skal du oprette nye generelle bogføringsgrupper.  
* For at reducere antallet af dokumenter, der konverteres, skal du postere så mange dokumenter som muligt og reducere antallet af dokumenter, der ikke posteres, til et minimum.  
* Sikkerhedskopiering af data.

### <a name="to-set-up-the-vat-rate-change-tool"></a>Sådan konfigureres momssatsændringsværktøjet  
1. Vælg ikonet ![Elpære, der åbner funktionen Fortæl mig](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig"), angiv **Konfiguration af ændring af momssats**, og vælg derefter det relaterede link.  
2. På oversigtspanelerne **Stamdata**, **Kladder** og **Dokumenter** skal du vælge en bogføringsgruppeværdi i indstillingslisten for nødvendige felter. For hver gruppe kan du vælge, om der skal konverteres momsproduktbogføringsgrupper eller generelle produktbogføringsgrupper, eller om begge værdier skal konverteres, hvis de er tilgængelige i stamdata. I nogle områder kan du også angive et filter for kun at konvertere et undersæt af værdier, f.eks. finanskonti. 

### <a name="to-set-up-product-posting-group-conversion"></a>Sådan konfigureres produktbogføringsgruppekonvertering  
1. Vælg ikonet ![Elpære, der åbner funktionen Fortæl mig](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig"), angiv **Konfiguration af ændring af momssats**, og vælg derefter det relaterede link.  
2. På siden **Konfiguration af ændring af momssats** skal du vælge enten **Momsproduktbogf.gruppekonv.** eller **Gen. produktbogf.gruppekonv.**.  
3. Angiv den aktuelle bogføringsgruppe i feltet **Fra kode**.  
4. Angiv den nye bogføringsgruppe i feltet **Til kode**.  

### <a name="to-perform-vat-rate-change-conversion"></a>Sådan udføres konvertering af momssatsændring  
Du bruger momssatsændringsværktøjet til at administrere ændringer i standardmomssatsen. Du udfører momsproduktbogføringsgruppekonverteringer og generelle produktbogføringsgruppekonverteringer for at ændre momssatser og opretholde nøjagtig momsafregning. Afhængigt af din opsætning foretages følgende ændringer:  

* Moms- og generelle bogføringsgrupper konverteres.  
* Ændringer implementeres i finanskonti, debitorer, kreditorer, åbne dokumenter, kladdelinjer osv.  

> [!IMPORTANT]  
>  Inden du foretager konvertering af momssatsændringen, kan du teste konverteringen. Det gør du ved at følge fremgangsmåde nedenfor, men sørg for at fjerne markeringen i afkrydsningsfelterne **Udfør konvertering** og **Momssatsændringsværktøjet afsluttet**. Under testkonverteringen ryddes feltet **Konverteret** i tabellen **Momssatsændringslogpost** og feltet **Konverteringsdato** i tabellen **Momssatsændringslogpost** er tomt. Når konverteringen er afsluttet, skal du vælge **Ændringslogposter for momssats** for at få vist resultaterne af prøvekonverteringen. Kontroller hver post, før du udfører konverteringen. Kontroller især transaktioner, som bruger en gammel momssats.     

1. Vælg ikonet ![Elpære, der åbner funktionen Fortæl mig](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig"), angiv **Momssatsændring**, og vælg derefter linket **Konfiguration af ændring af momssats**.  
2. Kontroller, at du allerede har oprettet momsproduktbogføringsgruppekonverteringen eller den generelle produktbogføringsgruppekonvertering.  
3. Markér afkrydsningsfeltet **Udfør konvertering**.  

    > [!IMPORTANT]  
    >  Fjern markeringen af afkrydsningsfeltet **Momssatsændringsværktøjet afsluttet**. Afkrydsningsfelt vælges automatisk, når konverteringen af momssatsændring er afsluttet.  

4. Vælg handlingen **Konverter**.  
5. Når konverteringen er afsluttet, skal du vælge handlingen **Ændringslogposter for momssats** for at få vist resultaterne af konverteringen.  

> [!IMPORTANT]  
>  Efter konverteringen er feltet **Konverteret** valgt i tabellen **Momssatsændringslogpost**, og feltet **Konverteringsdato** i tabellen **Momssatsændringslogpost** viser konverteringsdatoen.  
## <a name="see-also"></a>Se også  
[Konfigurere moms](finance-setup-vat.md)  
[Opsætning af ikke-realiseret moms](finance-setup-unrealized-vat.md)      
[Rapportere moms til skattemyndighederne](finance-how-report-vat.md)  
[Arbejde med moms af salg og køb](finance-work-with-vat.md)  
[Lokal funktionalitet i Business Central](about-localization.md)
