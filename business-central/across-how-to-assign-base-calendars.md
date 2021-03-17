---
title: Sådan opsættes basiskalendere | Microsoft Docs
description: Du kan tildele en basiskalender til din virksomhed eller til virksomhedens samarbejdspartnere, f.eks. kunder, leverandører eller lokationer. Leverings- og modtagelsesdatoer på fremtidige salgsordrer, købsordrer, overflytningsordrer og produktionsordrelinjer beregnes i overensstemmelse med de arbejdsdage, der er angivet i kalenderen.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: 5c2733bf660b5d17b0f2e7273c48d7c3dffbb5ef
ms.sourcegitcommit: ff2b55b7e790447e0c1fcd5c2ec7f7610338ebaa
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 02/15/2021
ms.locfileid: "5384545"
---
# <a name="set-up-base-calendars"></a>Konfigurere basiskalendere
Du kan tildele en basiskalender til din virksomhed eller til virksomhedens samarbejdspartnere, f.eks. kunder, leverandører eller lokationer. Leverings- og modtagelsesdatoer på fremtidige salgsordrer, købsordrer, overflytningsordrer og produktionsordrelinjer beregnes i overensstemmelse med de arbejdsdage, der er angivet i kalenderen. Den vigtigste opgave i forbindelse med oprettelse af en ny basiskalender, er at angive og definere de fridage, som du vil anvende.  

## <a name="to-set-up-a-base-calendar"></a>Sådan oprettes en basiskalender  
1.  Vælg ikonet ![Elpære, der åbner funktionen Fortæl mig](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig"), angiv **Basiskalender**, og vælg derefter det relaterede link.  
2.  Vælg handlingen **Ny**.  
3.  Udfyld feltet **Kode**.  
4. Vælg handlingen **Vedligehold basiskalender**.
5. På siden **Ændringer i basiskalender** skal du bruge feltet **Tilbagevendende** til at markere en bestemt dato eller dag som tilbagevendende fridag. Du kan vælge mellem indstillingerne **Årligt** og **Ugentligt**.  

    Hvis du vælger **Årligt**, skal du også angive den relevante dato i feltet **Dato**.  

    Hvis du vælger **Ugentligt**, skal du også angive den relevante ugedag i feltet **Dag**. Hvis du lader feltet stå tomt, skal du udfylde feltet **Dato**. Feltet **Dag** udfyldes automatisk.  

Når du indtaster en linje, vil feltet **Fridag** være markeret. Du kan vælge at fjerne markeringen for at gøre den til en arbejdsdag.  
 Når du vender tilbage til basiskalenderkortet, kan du se, at de poster for fridage, som du har oprettet, er blevet opdateret. Disse poster bliver nu vist med rødt og feltet **Fridag** er markeret.  

> [!NOTE]  
>  Når du opretter en ny basiskalender, kan du markere og kopiere linjer fra en eksisterende kalender. Dette gøres på siden **Ændringer i basiskalender**.  

> [!IMPORTANT]  
>  Enhver basiskalender, der er defineret for kreditoren eller lokationen, påvirker, hvordan datoerne beregnes og afrundet til arbejdsdage.
Angiver en datoformel for det tidsrum, det tager at genbestille varen. Den bruges til at beregne feltet **Planlagt modtagelsesdato**, hvis du beregner fremad, og feltet **Ordredato**, hvis du beregner bagud. Se [Leveringstid](across-how-to-assign-base-calendars.md#lead-time-calculation).

## <a name="lead-time-calculation"></a>Leveringstid
Enhver basiskalender, der er defineret for kreditoren eller lokationen, påvirker, hvordan datoerne beregnes og afrundet til arbejdsdage. I henhold hertil beregnes de to vigtige datofelter på købsordrelinjer på følgende måde under forskellige betingelser.

|Beregningsretning|Kreditorkalender defineret|Kreditorkalender ikke defineret|
|---------------------|-----------------------|---------------------------|
|Fremad|planlagt modtagelsesdato = ordredato + kreditorleveringstid (pr. kreditorkalender og afrundet til næste arbejdsdag i den første kreditorkalender og derefter lokationskalenderen)|planlagt modtagelsesdato = ordredato + kreditorleveringstid (pr. lokationskalender)|
|Baglæns|ordredato = planlagt modtagelsesdato + kreditorleveringstid (pr. kreditorkalender og afrundet til forrige arbejdsdag i den første kreditorkalender og derefter lokationskalenderen)|ordredato = planlagt modtagelsesdato - kreditorleveringstid (pr. lokationskalender)|

> [!NOTE]
> Udover den beregning af leveringstid, der påvirker den planlagte modtagelsesdato og ordredatoen, som vist i ovenstående tabel, kan lagerekspeditionstiden og sikkerhedstiden føjes til formlerne for at udgøre værdien i feltet **Forventet modt.dato** på følgende måde: Planlagt modtagelsesdato + Sikkerhedstid + Indgående lagerekspeditionstid = Forventet modt.dato.

> [!Important]
> Hvis lokationen bruger en væsentligt anden kalender end dine kreditorer, er det vigtigt, at du har konfigureret bestemte kalendere for disse leverandører til at beregne optimal leverandør leveringstider. Du kan finde oplysninger om, hvordan du opretter kreditorkalendere i [Sådan tildeles en basiskalender](across-how-to-assign-base-calendars.md#to-assign-a-base-calendar).

Indeholder i feltet **Leveringstid** kopieres fra enten varekortet eller lagervarekortet, hvis leveringstiden er defineret for varen, eller på siden **Vare/Leverandør-katalog**, hvis leveringstiden er defineret for kreditoren.

## <a name="to-customize-a-calendar"></a>Sådan tilpasses en kalender
Den vigtigste opgave i forbindelse med tilpasning af en basiskalender for din virksomhed eller en samarbejdspartner, er at angive eventuelle ændringer i statussen for arbejdsdage eller fridage.

En basiskalender vil f.eks. typisk opgive alle lørdage som fridage. Den tilpassede kalender for en bestemt lokation kan f.eks. angive alle lørdage i november og december måned og op til ferieperioden, som arbejdsdage.

I følgende procedure bruges en lokation som eksempel. Bemærk, at du allerede nu skal have tildelt en basiskalender til lokationen.

1. Vælg ikonet ![Elpære, der åbner funktionen Fortæl mig](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig"), angiv **Lokationer**, og vælg dernæst det relaterede link.
2. Åbn den lokation, du vil opdatere, og vælg derefter feltet **Tilpasset kalender**. Bemærk, at der skal vælges en kalender i feltet **Basiskalenderkode**.
3. På siden **Tilpassede kalenderposter**, der åbnes, skal du vælge handlingen **Bevar tilpassede kalenderændringer**.
4. I feltet **Tilpassede kalenderændringer** skal du tilføje linjer for tilpassede kalenderposter.

    Når du indtaster en linje, markeres afkrydsningsfeltet **Fridag** være markeret. Du kan fjerne markeringen, hvis du vil ændre status til en arbejdsdag.

    Du kan bruge feltet **Tilbagevendende** til at indstille en bestemt dato eller dag som en tilbagevendende fridag. Du kan vælge mellem indstillingerne **Årligt** og **Ugentligt**.

    Hvis du vælger **Årligt**, skal du også angive den relevante dato i feltet **Dato**. Hvis du vælger **Ugentligt**, skal du også angive den relevante ugedag i feltet **Dag**. Hvis du lader feltet stå tomt, skal du udfylde feltet **Dato**. Feltet **Dag** udfyldes automatisk. Det kunne være nyttigt, hvis du vil markere en bestemt dato som en arbejdsdag eller en fridag.

5. Vælg knappen **OK**.

På siden **Tilpassede kalenderposter** kan du se, at datoposterne er blevet opdateret med de ændringer, som du har foretaget.

På kortet Lokation, kan du se, at feltet **Tilpasset kalender** indeholder ordet **Ja**. Det angiver, at en tilpasset kalender er oprettet.

> [!Important]
> Hvis du ikke udfylder feltet **Lokationskode** på en ordrelinje, bruger programmet din virksomheds kalender.


Hvis du ikke udfylder feltet **Speditørkode** på ordrelinjen, bruger programmet din virksomheds kalender.

> [!NOTE]  
> Hvis du foretager ændringer i en kalender, hvori der er foretaget tilpassede kalenderændringer, opdateres alle eksisterende tilpassede kalendere automatisk.

## <a name="to-assign-a-base-calendar"></a>Sådan tildeles en basiskalender  
I følgende procedure planlægges leveringsdatoer på salgsordrelinjer for en kunde som eksempel.

Basiskalendere er knyttet til din egen virksomhed, debitorer, kreditorer, placeringer og speditører som følger:  

-   Basiskalenderen er knyttet til oversigtspanelet **Levering** på kortene **Firmaoplysninger** og **Debitor**.  
-   Basiskalenderen er tildelt i oversigtpanelet **Modtagelse** på kortet **Kreditor**.  
-   Basiskalenderen er tildelt i oversigtpanelet **Lager** på kortet **Lokation**.  
-   Basiskalenderen er tildelt på oversigtssiden **Speditørservice** på siden **Speditører**.  

1.  Vælg ikonet ![Elpære, der åbner funktionen Fortæl mig](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig"), angiv **Kunder**, og vælg derefter det relaterede link.  
2.  Åbn det **Debitor**-kort, som du vil oprette en basiskalender til.  
3.  Vælg den basiskalender, du vil tildele i feltet **Basiskalenderkode** i oversigtspanelet **Levering**.  

> [!IMPORTANT]  
>  -   Hvis du ikke tildeler en basiskalender til en virksomhed, beregnes alle datoer automatisk som arbejdsdage.  
> -   Hvis du angiver en tom lokation på en ordrelinje, beregnes alle datoer automatisk som arbejdsdage.  
> -   Enhver basiskalender, der er defineret for kreditoren eller lokationen, påvirker, hvordan datoerne beregnes og afrundet til arbejdsdage.

> [!NOTE]  
>  Før du kan oprette poster i tilpassede kalendere, skal du tildele en basiskalender til virksomheden.  

## <a name="see-also"></a>Se også
[Køb](purchasing-manage-purchasing.md)  
[Produktion](production-manage-manufacturing.md)    
[Lagerbeholdning](inventory-manage-inventory.md)  
[Arbejde med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]