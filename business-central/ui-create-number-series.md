---
title: Oprette nummerserier | Microsoft Docs
description: "Lær, hvordan du konfigurerer nummerserier, der tildeler entydige ID-koder til konti og dokumenter i Business Central."
documentationcenter: 
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: numbers, numbering
ms.date: 10/01/2018
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 33b900f1ac9e295921e7f3d6ea72cc93939d8a1b
ms.openlocfilehash: 46131d6ad5f77a02ffe33d24f1210a226c3041c1
ms.contentlocale: da-dk
ms.lasthandoff: 11/26/2018

---
# <a name="create-number-series"></a>Oprette nummerserie
For hver af de virksomheder, som du opretter, skal du knytte entydige id-koder til ting som finanskonti, debitor- og kreditorkonti, fakturaer og andre dokumenter. Nummereringen er ikke kun vigtig til identifikation. Et veludviklet nummereringssystem gør det også nemmere at administrere og foretage analyse i virksomheden og kan reducere antallet af dataindtastningsfejl.

> [!NOTE]  
>   Det anbefales, at du bruger samme nummerseriekoder, som du kan se vist på siden **Nummerserieoversigt** i demonstrationsvirksomheden CRONUS. Koder som *K-FAK+* giver muligvis ikke mening for dig, men [!INCLUDE[d365fin](includes/d365fin_md.md)] har en række standardindstillinger, som afhænger af disse nummerseriekoder.

Du kan oprette et nummereringssystem ved at oprette en eller flere koder for hver type stamdata eller dokument. Du kan f.eks. oprette en kode til nummerering af debitorer, en anden kode til nummerering af salgsfakturaer og en anden kode til nummerering af dokumenter i finanskladder. Når du har oprettet en kode, skal du oprette mindst en nummerserielinje. Nummerserielinjen indeholder oplysninger som f.eks. det første og sidste nummer i serien og startdatoen. Du kan oprette mere end en nummerserielinje pr. nummerseriekode med en anden startdato for hver linje. Serierne bruges efter hinanden, hvor hver serie starter på den pågældende startdato.

Normalt vil du indstille dine nummerserier til automatisk at indsætte det næste fortløbende nummer på nye kort eller i dokumenter, du opretter. Men du kan også konfigurere en nummerserie til at tillade, at du manuelt angive det nye nummer. Du kan angive dette med afkrydsningsfeltet **Manuel nummerering**.

Hvis du vil bruge mere end én nummerseriekode til en type stamdata - hvis du f.eks. vil bruge forskellige nummerserier til forskellige varekategorier - kan du bruge nummerserierelationer.

## <a name="behavior-of-the-no-field-on-documents-and-cards"></a>Egenskaberne for feltet Nummer på dokumenter og kort
På salgs-, købs- og overførselsdokumenter og på alle kort kan **Nummer** udfyldes automatisk eller manuelt fra en nummerserie og kan konfigureres til at være usynligt.

Feltet **Nummer** kan udfyldes på tre måder:

1. Hvis der kun findes én nummerserie for typen af dokument eller kort, hvor afkrydsningsfeltet **Standardnumre** er markeret, og afkrydsningsfeltet **Manuel nummerering** ikke er markeret, udfyldes feltet automatisk med det næste nummer i serien, og feltet **Nummer** kan ikke ses.

    > [!NOTE]  
    > Hvis nummerserien ikke fungerer, f.eks. fordi der ikke er flere tal, er feltet **Nummer** synligt, og du kan manuelt angive et nummer eller løse problemerne på siden **Nummerserieoversigt**.

2. Hvis der findes mere end én nummerserie for typen af dokument eller kort, og afkrydsningsfeltet **Standardnumre** ikke er markeret for den nummerserie, der aktuelt er tildelt, er feltet **Nummer** synligt, og kan du slå siden **Nummerserieoversigt** op og vælge den nummerserie, du vil bruge. Det næste nummer i serien indsættes derefter i feltet **Nummer** .

3. Hvis du ikke har defineret en nummerserie for denne type dokument eller kort, eller hvis feltet **Manuel nummerering** er markeret for nummerserien, er feltet **Nummer** synligt, og du skal angive et nummer manuelt. Du kan bruge op til 20 tegn (både tal og bogstaver).

Når du åbner et nyt dokument eller kort, der findes en nummerserie for, åbnes den relevante side **Konfiguration af salgsnummerserie**, så du kan oprette en nummerserie for denne type dokument eller kort, før du fortsætter med andre indtastning af data.

> [!NOTE]  
> Hvis du har brug for at aktivere manuel nummerering på f.eks. nye varekort, der er oprettet med en dataoverførselsproces, hvor **Nummer** som standard er skjult, skal du gå til siden **Lageropsætning** og vælge feltet **Varenumre** for at åbne og indstille de relaterede nummerserier til **Manuel nummerering**.

## <a name="to-create-a-new-number-series"></a>Sådan opretter du en ny nummerserie
1. Vælg ikonet ![Elpære, der åbner funktionen Fortæl mig](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig"), angiv **Nummerserie**, og vælg derefter det relaterede link.
2. Vælg handlingen **Ny**.
3. Udfyld felterne på den nye linje efter behov. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

## <a name="to-set-up-where-a-number-series-is-used"></a>Sådan definerer du, hvor en nummerserie skal bruges
Følgende procedure viser, hvordan du konfigurerer nummerserieren for området Salg. Trinene er som for andre områder.
1. Vælg ikonet ![Elpære, der åbner funktionen Fortæl mig](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig"), angiv **Salg**, og vælg derefter det relaterede link.
2. På siden **Salg** i oversigtspanelet **Nummerserie** skal du vælge den ønskede nummerserie for hvert salgskort eller dokument.

Det valgte nummer bliver nu brugt til at udfylde feltet **Nummer** på det relevante kort eller dokument i overensstemmelse med de valgte indstillinger på nummerserielinjen.

## <a name="to-create-relationships-between-number-series"></a>Sådan oprettes relationer mellem nummerserier
Hvis du har oprettet mere end en nummerseriekode for samme slags grundlæggende oplysninger eller transaktioner, kan du oprette relationer mellem koderne. Denne funktion kan være en hjælp ved valg af koder, når du bruger et nummer.

1. Vælg ikonet ![Elpære, der åbner funktionen Fortæl mig](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig"), angiv **Nummerserie**, og vælg derefter det relaterede link.
2. Vælg linjen med den nummerserie, du vil oprette relationer for, og vælg derefter **Relationer**.
3. I feltet **Seriekode** skal du indtaste koden for de antal serier, du vil knytte til de serier, du valgte under trin to .
4. Tilføj en linje for hver kode, du vil knytte til den valgte nummerserie.
5. Luk siden.

Når du derefter opretter noget, der kræver et nummer, kan du bruge de relationer, du har oprettet, til at vælge mellem de relaterede nummerserier.

## <a name="see-also"></a>Se også
[Opsætning af [!INCLUDE[d365fin](includes/d365fin_md.md)]](setup.md)  
[Arbejde med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)  

