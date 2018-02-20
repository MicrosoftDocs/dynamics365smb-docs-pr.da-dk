---
title: Oprette nummerserier | Microsoft Docs
description: "Få at vide, hvordan du konfigurerer nummerserier, der tildeler entydige ID-koder til konti og dokumenter i Finance and Operations, Business edition."
documentationcenter: 
author: SusanneWindfeldPedersen
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: numbers, numbering
ms.date: 06/02/2017
ms.author: solsen
ms.translationtype: HT
ms.sourcegitcommit: bec0619be0a65e3625759e13d2866ac615d7513c
ms.openlocfilehash: 3f50bc1153ccd6b58bc502974c042626ce696078
ms.contentlocale: da-dk
ms.lasthandoff: 01/30/2018

---
# <a name="create-number-series"></a>Oprette nummerserie
For hver af de virksomheder, som du opretter, skal du knytte entydige id-koder til ting som finanskonti, debitor- og kreditorkonti, fakturaer og andre dokumenter. Nummereringen er ikke kun vigtig til identifikation. Et veludviklet nummereringssystem gør det også nemmere at administrere og foretage analyse i virksomheden og kan reducere antallet af dataindtastningsfejl.

> [!NOTE]  
>   Det anbefales, at du bruger samme nummerseriekoder, som du kan se vist i vinduet **Nummerserieoversigt** i demonstrationsvirksomheden CRONUS. Koder som *K-FAK+* giver muligvis ikke mening for dig, men [!INCLUDE[d365fin](includes/d365fin_md.md)] har en række standardindstillinger, som afhænger af disse nummerseriekoder.

Du kan oprette et nummereringssystem ved at oprette en eller flere koder for hver type stamdata eller dokument. Du kan f.eks. oprette en kode til nummerering af debitorer, en anden kode til nummerering af salgsfakturaer og en anden kode til nummerering af dokumenter i finanskladder. Når du har oprettet en kode, skal du oprette mindst en nummerserielinje. Nummerserielinjen indeholder oplysninger som f.eks. det første og sidste nummer i serien og startdatoen. Du kan oprette mere end en nummerserielinje pr. nummerseriekode med en anden startdato for hver linje. Serierne bruges efter hinanden, hvor hver serie starter på den pågældende startdato.

Normalt vil du indstille dine nummerserier til automatisk at indsætte det næste fortløbende nummer på nye kort eller i dokumenter, du opretter. Men du kan også konfigurere en nummerserie til at tillade, at du manuelt angive det nye nummer. Du kan angive dette med afkrydsningsfeltet **Manuel nummerering**.

Hvis du vil bruge mere end én nummerseriekode til en type stamdata - hvis du f.eks. vil bruge forskellige nummerserier til forskellige varekategorier - kan du bruge nummerserierelationer.

## <a name="to-create-a-new-number-series"></a>Sådan opretter du en ny nummerserie
1. Vælg ikonet ![Søg efter side eller rapport](media/ui-search/search_small.png "Ikonet Søg efter side eller rapport"), angiv **Nummerserie**, og vælg derefter det relaterede link.
2. Vælg handlingen **Ny**.
3. Udfyld felterne på den nye linje efter behov. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

**TIP!** Hvis du vil tillade manuel indtastning af et nummer på nye kort eller dokumenter, skal du fjerne markeringen i afkrydsningsfeltet **Standardnumre** og markere afkrydsningsfeltet **Manuel nummerering**.

Når du nu opretter et nyt kort eller dokument, der er indstillet til at bruge den pågældende nummerserie, du kan manuelt udfylde feltet **Nummer** med den ønskede værdi.  

## <a name="to-set-up-where-a-number-series-is-used"></a>Sådan definerer du, hvor en nummerserie skal bruges
Følgende procedure viser, hvordan du konfigurerer nummerserieren for området Salg. Trinene er som for andre områder.
1. Vælg ikonet ![Søg efter side eller rapport](media/ui-search/search_small.png "Ikonet Søg efter side eller rapport"), angiv **Nummerserie**, og vælg derefter det relaterede link.
2. I vinduet **Salg** i oversigtspanelet **Nummerserie** skal du vælge den ønskede nummerserie for hvert salgskort eller dokument.

Det valgte nummer bliver nu brugt til at udfylde feltet **Nummer** på det relevante kort eller dokument i overensstemmelse med de valgte indstillinger på nummerserielinjen.

## <a name="to-create-relationships-between-number-series"></a>Sådan oprettes relationer mellem nummerserier
Hvis du har oprettet mere end en nummerseriekode for samme slags grundlæggende oplysninger eller transaktioner, kan du oprette relationer mellem koderne. Denne funktion kan være en hjælp ved valg af koder, når du bruger et nummer.

1. Vælg ikonet ![Søg efter side eller rapport](media/ui-search/search_small.png "Ikonet Søg efter side eller rapport"), angiv **Nummerserie**, og vælg derefter det relaterede link.
2. Vælg linjen med den nummerserie, du vil oprette relationer for, og vælg derefter **Relationer**.
3. I feltet **Seriekode** skal du indtaste koden for de antal serier, du vil knytte til de serier, du valgte under trin to .
4. Tilføj en linje for hver kode, du vil knytte til den valgte nummerserie.
5. Luk vinduet.

Når du derefter opretter noget, der kræver et nummer, kan du bruge de relationer, du har oprettet, til at vælge mellem de relaterede nummerserier.

## <a name="see-also"></a>Se også
[Opsætning af [!INCLUDE[d365fin](includes/d365fin_md.md)]](setup.md)  
[Arbejde med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)  

