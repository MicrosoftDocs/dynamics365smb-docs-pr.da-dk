---
title: Oprette nummerserier | Microsoft Docs
description: Lær, hvordan du konfigurerer nummerserier, der tildeler entydige ID-koder til konti og dokumenter i Business Central.
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: numbers, numbering
ms.date: 04/01/2021
ms.author: edupont
ms.openlocfilehash: 3e2404a0ab9de8a761d5721da669004e393cf55c
ms.sourcegitcommit: a7cb0be8eae6ece95f5259d7de7a48b385c9cfeb
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 07/08/2021
ms.locfileid: "6445993"
---
# <a name="create-number-series"></a>Oprette nummerserie
For hver af de virksomheder, som du opretter, skal du knytte entydige id-koder til ting som finanskonti, debitor- og kreditorkonti, fakturaer og andre dokumenter. Nummereringen er ikke kun vigtig til identifikation. Et veludviklet nummereringssystem gør det også nemmere at administrere og foretage analyse i virksomheden og kan reducere antallet af dataindtastningsfejl.

> [!Important]
> Der er som standard ikke tilladt huller i nummerserier, fordi den nøjagtige historik over økonomiske transaktioner i henhold til lovgivningen skal være tilgængelig for revision og derfor skal følge en ubrudt rækkefølge uden slettede numre.<br /><br />
Hvis du vil tillade huller i visse nummerserier, skal du først rådføre dig med din revisor eller regnskabschef for at sikre, at du overholder de juridiske krav i dit land/område. Du kan finde flere oplysninger i [Huller i nummerserier](ui-create-number-series.md#gaps-in-number-series).

> [!NOTE]  
>   Det anbefales, at du bruger samme nummerseriekoder, som du kan se vist på siden **Nummerserieoversigt** i demoregnskabet CRONUS. Koder som *K-FAK+* giver muligvis ikke mening for dig, men [!INCLUDE[prod_short](includes/prod_short.md)] har en række standardindstillinger, som afhænger af disse nummerseriekoder.

Du kan oprette et nummereringssystem ved at oprette en eller flere koder for hver type stamdata eller dokument. Du kan f.eks. oprette en kode til nummerering af debitorer, en anden kode til nummerering af salgsfakturaer og en anden kode til nummerering af dokumenter i finanskladder. Når du har oprettet en kode, skal du konfigurere mindst én nummerserielinje. Nummerserielinjen indeholder oplysninger som f.eks. det første og sidste nummer i serien og startdatoen. Du kan oprette mere end en nummerserielinje pr. nummerseriekode med en anden startdato for hver linje. Serierne bruges efter hinanden, hvor hver serie starter på den pågældende startdato.

> [!NOTE]
> Et tals maksimale længde i en nummerserie er 20 tegn. Der kan være situationer, hvor [!INCLUDE[prod_short](includes/prod_short.md)] vil tilføje et nummer med et systemgenereret id. Når dokumenter som f.eks. fakturaer bruges til at udligne transaktioner, f.eks. betalinger, genererer [!INCLUDE[prod_short](includes/prod_short.md)] id'er for de udlignede transaktioner. Id'et består af et nummer fra en nummerserie og et systemtildelt id på seks tegn, f.eks. -12345. Hvis du forventer at skulle behandle mere end 9999 dokumenter i bank- eller GIRO-kladder eller indbetalingskladder, skal du oprette en nummerserie til disse typer dokumenter, hvor numrene indeholder mindre end 14 tegn.

Normalt vil du indstille dine nummerserier til automatisk at indsætte det næste fortløbende nummer på nye kort eller i dokumenter, du opretter. Men du kan også konfigurere en nummerserie til at tillade, at du manuelt angive det nye nummer. Du kan angive dette med afkrydsningsfeltet **Manuel nummerering**.

Hvis du vil bruge mere end én nummerseriekode til en type stamdata - hvis du f.eks. vil bruge forskellige nummerserier til forskellige varekategorier - kan du bruge nummerserierelationer.

## <a name="gaps-in-number-series"></a>Huller i nummerserier
Ikke alle de poster, du opretter i [!INCLUDE[prod_short](includes/prod_short.md)], er økonomiske transaktioner, der skal bruge fortløbende nummerering. Debitorkort, salgstilbud og lageraktiviteter er eksempler på poster, der tildeles et nummer fra en nummerserie, men som ikke er underlagt økonomisk revision og/eller kan slettes. For disse nummerserier kan du markere afkrydsningsfeltet **Tillad huller i numre** på siden **Nummerserielinjer**. Denne indstilling kan også ændres, når nummerserien er oprettet. Du kan finde flere oplysninger i [Sådan opretter du en ny nummerserie](ui-create-number-series.md#to-create-a-new-number-series).

## <a name="behavior-of-the-no-field-on-documents-and-cards"></a>Egenskaberne for feltet Nummer på dokumenter og kort
På salgs-, købs- og overførselsdokumenter og på alle kort kan **Nummer** udfyldes automatisk eller manuelt fra en nummerserie og kan konfigureres til at være usynligt.

Feltet **Nummer** kan udfyldes på tre måder:

1. Hvis der kun findes én nummerserie for typen af dokument eller kort, hvor afkrydsningsfeltet **Standardnumre** er markeret, og afkrydsningsfeltet **Manuel nummerering** ikke er markeret, udfyldes feltet automatisk med det næste nummer i serien, og feltet **Nummer** kan ikke ses.

    > [!NOTE]  
    > Hvis nummerserien ikke fungerer, f.eks. fordi der ikke er flere tal, er feltet **Nummer** synligt, og du kan manuelt angive et nummer eller løse problemerne på siden **Nummerserie**.

2. Hvis der findes mere end én nummerserie for typen af dokument eller kort, og afkrydsningsfeltet **Standardnumre** ikke er markeret for den nummerserie, der aktuelt er tildelt, er feltet **Nummer** synligt, og kan du slå siden **Nummerserie** op og vælge den nummerserie, du vil bruge. Det næste nummer i serien indsættes derefter i feltet **Nummer** .

3. Hvis du ikke har defineret en nummerserie for denne type dokument eller kort, eller hvis feltet **Manuel nummerering** er markeret for nummerserien, er feltet **Nummer** synligt, og du skal angive et nummer manuelt. Du kan bruge op til 20 tegn (både tal og bogstaver).

Når du åbner et nyt dokument eller kort, der findes en nummerserie for, åbnes den relevante side **Konfiguration af salgsnummerserie**, så du kan oprette en nummerserie for denne type dokument eller kort, før du fortsætter med andre indtastning af data.

> [!NOTE]  
> Hvis du har brug for at aktivere manuel nummerering på f.eks. nye varekort, der er oprettet med en dataoverførselsproces, hvor **Nummer** som standard er skjult, skal du gå til siden **Lageropsætning** og vælge feltet **Varenumre** for at åbne og indstille de relaterede nummerserier til **Manuel nummerering**.

## <a name="to-create-a-new-number-series"></a>Sådan opretter du en ny nummerserie
1. Vælg ![Lightbulb, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, angiv **Nummerserie**, og vælg derefter det relaterede link.
2. Vælg handlingen **Ny**.
3. Udfyld felterne på den nye linje efter behov. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
4. Vælg handlingen **Linjer**.
5. På siden **Nummerserielinjer** skal du udfylde felterne for at definere den faktiske brug og indholdet af den nummerserie, du oprettede i trin 2.
6. Gentag trin 5 for så mange forskellige anvendelser af nummerserien, du har brug for. Feltet **Startdato** angiver, hvilken nummerserielinje der er aktiv.

## <a name="to-set-up-where-a-number-series-is-used"></a>Sådan definerer du, hvor en nummerserie skal bruges
Følgende procedure viser, hvordan du konfigurerer nummerserieren for området Salg. Trinene er som for andre områder.
1. Vælg ![Lightbulb, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, angiv **Salg og tilgodehavender**, og vælg derefter det relaterede link.
2. På siden **Salg** i oversigtspanelet **Nummerserie** skal du vælge den ønskede nummerserie for hvert salgskort eller dokument.

Det valgte nummer bliver nu brugt til at udfylde feltet **Nummer** på det relevante kort eller dokument i overensstemmelse med de valgte indstillinger på nummerserielinjen.

## <a name="to-create-relationships-between-number-series"></a>Sådan oprettes relationer mellem nummerserier
Hvis du har oprettet mere end en nummerseriekode for samme slags grundlæggende oplysninger eller transaktioner, kan du oprette relationer mellem koderne. Denne funktion kan være en hjælp ved valg af koder, når du bruger et nummer.

1. Vælg ![Lightbulb, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, angiv **Nummerserie**, og vælg derefter det relaterede link.
2. Vælg linjen med den nummerserie, du vil oprette relationer for, og vælg derefter **Relationer**.
3. I feltet **Seriekode** skal du indtaste koden for de antal serier, du vil knytte til de serier, du valgte under trin to .
4. Tilføj en linje for hver kode, du vil knytte til den valgte nummerserie.
5. Luk siden.

Når du derefter opretter noget, der kræver et nummer, kan du bruge de relationer, du har oprettet, til at vælge mellem de relaterede nummerserier.

## <a name="see-related-training-at-microsoft-learn"></a>Se relateret oplæring på [Microsoft Learn](/learn/modules/number-series-trail-codes-dynamics-365-business-central/index)

## <a name="see-also"></a>Se også
[Opsætning af [!INCLUDE[prod_short](includes/prod_short.md)]](setup.md)  
[Arbejde med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]