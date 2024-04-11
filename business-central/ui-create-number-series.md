---
title: Oprette nummerserie
description: 'Lær, hvordan du konfigurerer nummerserier, der tildeler entydige ID-koder til konti og dokumenter i Business Central.'
author: brentholtorf
ms.topic: conceptual
ms.devlang: al
ms.search.keywords: 'numbers, numbering'
ms.search.form: '456, 457, 458, 459, 460, 461, 21, 22, 26, 27, 31'
ms.date: 02/26/2024
ms.author: bholtorf
ms.service: dynamics-365-business-central
---
# Oprette nummerserie

For hver af de virksomheder, som du opretter, skal du knytte entydige id-koder til ting som finanskonti, debitor- og kreditorkonti, fakturaer og andre dokumenter. Nummerering er ikke kun vigtig til identifikation. Et veludviklet nummereringssystem gør det også nemmere at administrere og foretage analyse i virksomheden og kan reducere antallet af dataindtastningsfejl.

> [!Important]
> Det er som standard ikke tilladt at have huller i nummerserier, fordi den nøjagtige historik over økonomiske transaktioner i henhold til lovgivningen skal være tilgængelig for revision og derfor skal følge en ubrudt rækkefølge uden slettede numre.
>
> Hvis du vil tillade huller i visse nummerserier, skal du rådføre dig med din revisor eller regnskabschef for at sikre, at du overholder de juridiske krav i dit land/område. Du kan finde flere oplysninger i [Huller i nummerserier](#gaps-in-number-series).

> [!NOTE]  
> Det anbefales, at du bruger samme nummerseriekoder, som du kan se vist på siden **Nummerserieoversigt** i demoregnskabet CRONUS. Koder som *K-FAK+* giver muligvis ikke mening for dig, men [!INCLUDE[prod_short](includes/prod_short.md)] har en række standardindstillinger, som afhænger af disse nummerseriekoder.

Du kan oprette et nummereringssystem ved at oprette en eller flere koder for hver type stamdata eller dokument. Du kan f.eks. oprette en kode til nummerering af debitorer, en anden kode til nummerering af salgsfakturaer og en anden kode til nummerering af dokumenter i finanskladder. Når du har oprettet en kode, skal du konfigurere mindst én nummerserielinje. Nummerserielinjen indeholder oplysninger som f.eks. det første og sidste nummer i serien og startdatoen. Du kan oprette mere end en nummerserielinje pr. nummerseriekode med en anden startdato for hver linje. Serierne bruges efter hinanden, hvor hver serie starter på den pågældende startdato.

> [!NOTE]
> Et tals maksimale længde i en nummerserie er 20 tegn. Der kan være situationer, hvor [!INCLUDE[prod_short](includes/prod_short.md)] vil tilføje et nummer med et systemgenereret id. Når dokumenter som f.eks. fakturaer bruges til at udligne transaktioner, f.eks. betalinger, genererer [!INCLUDE[prod_short](includes/prod_short.md)] id'er for de udlignede transaktioner. Id'et består af et nummer fra en nummerserie og et systemtildelt id på seks tegn, f.eks. -12345. Hvis du forventer at skulle behandle mere end 9999 dokumenter i bank- eller GIRO-kladder eller indbetalingskladder, skal du oprette en nummerserie til disse typer dokumenter, hvor numrene indeholder mindre end 14 tegn.

Normalt vil du indstille dine nummerserier til automatisk at indsætte det næste fortløbende nummer på nye kort eller i dokumenter, du opretter. Men du kan også konfigurere en nummerserie til at tillade, at du manuelt angive det nye nummer. Du kan angive dette med afkrydsningsfeltet **Manuel nummerering**.

Hvis du vil bruge mere end én nummerseriekode til en type stamdata - hvis du f.eks. vil bruge forskellige nummerserier til forskellige varekategorier - kan du bruge nummerserierelationer.

## Huller i nummerserier

Ikke alle de poster, du opretter i [!INCLUDE[prod_short](includes/prod_short.md)], er økonomiske transaktioner, der skal bruge fortløbende nummerering. Debitorkort, salgstilbud og lageraktiviteter er eksempler på poster, der tildeles et nummer fra en nummerserie, men som ikke er underlagt økonomisk revision og/eller kan slettes. For disse nummerserier kan du markere afkrydsningsfeltet **Tillad huller i numre** på siden **Nummerserielinjer**. Denne indstilling kan også ændres, når nummerserien er oprettet. Du kan finde flere oplysninger i [Sådan opretter du en ny nummerserie](ui-create-number-series.md#to-create-a-new-number-series).

## Egenskaberne for feltet felt på dokumenter og kort

På salgs-, købs-, overførsels- og servicedokumenter og på alle kort kan **Nummer** felter kan udfyldes automatisk eller fra en foruddefineret nummerserie, eller du kan tilføje dem manuelt. Men i visse tilfælde er feltet **nr.** feltet er usynligt for at forhindre dig i at redigere det.  

Feltet **Nummer** kan udfyldes på tre måder:

1. Hvis der kun findes én nummerserie for typen af dokument eller kort, hvor afkrydsningsfeltet **Standardnumre** er markeret, og afkrydsningsfeltet **Manuel nummerering** ikke er markeret, udfyldes feltet automatisk med det næste nummer i serien, og feltet Nummer. Feltet **Nummer** kan ikke ses på kortet eller dokumentet.  

    Selvom du definerer skabeloner med forskellige nummerserier til debitorer, er den nummerserie, der er defineret på siden **Salgsopsætning** konfigureret på denne måde, og feltet **Nr.** er usynligt på debitorkortet, uanset hvilken type du bruger. Det samme gælder for andre kort og dokumenter.  

    > [!NOTE]  
    > Hvis nummerserien ikke fungerer, f.eks. fordi den har nået det sidst definerede nummer i intervallet, vises feltet **Nr.**, hvor du kan indtaste et nummer manuelt. Du kan løse problemer på siden **Nummerserie**.

2. Hvis du har mere end én nummerserie for en type dokument eller kort, og afkrydsningsfeltet **Standardnumre** ikke er markeret for den tildelte nummerserie, vises feltet **Nummer**, og du kan gå til siden **Nummerserie** og vælge den nummerserie, du vil bruge. Det næste nummer i serien indsættes derefter i feltet **Nummer** .

3. Hvis du ikke har defineret en nummerserie for en type dokument eller kort, eller hvis feltet **Manuel nummerering** er markeret for nummerserien, vises feltet **Nummer**, hvor du kan indtaste et nummer manuelt. Du kan bruge op til 20 tegn (både tal og bogstaver).

Når du åbner et nyt dokument eller kort, der findes en nummerserie for, åbnes siden **Konfiguration af nummerserie**, så du kan oprette en nummerserie for denne type dokument eller kort og fortsætte med arbejdet.

> [!NOTE]  
> Hvis du har brug for at aktivere manuel nummerering på f.eks. nye varekort, der er oprettet med en dataoverførselsproces, hvor **Nummer** som standard er skjult, skal du gå til siden **Lageropsætning** og vælge feltet **Varenumre** for at åbne og indstille de relaterede nummerserier til **Manuel nummerering**.
>
> Det samme gælder, hvis du bruger funktioner til servicestyring. Du kan løse problemet ved at gå til siden **Serviceopsætning** og vælge feltet **Serviceartikelnumre** for at indstille nummerserien til **Manuel nummerering**.

## Sådan opretter du en ny nummerserie

1. Vælg det ![lyspæreikon, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, angiv **Nummerserie**, og vælg derefter det relaterede link.
2. Vælg handlingen **Ny**.  
3. Udfyld felterne på den nye linje efter behov. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]  
4. Vælg handlingen **Linjer**.  
5. På siden **Nummerserielinjer** skal du udfylde felterne for at definere den faktiske brug og indholdet af den nummerserie, du oprettede i trin 2.  
6. Gentag trin 5 for så mange forskellige anvendelser af nummerserien, du har brug for. Feltet **Startdato** angiver, hvilken nummerserielinje der er aktiv.  

> [!TIP]
> Hvis du vil tillade, at brugere angiver numre manuelt, når de registrerer en ny kunde eller leverandør, skal du f. eks. vælge feltet **Manuel nummerering** på selve nummerserien. Ryd feltet, hvis du vil undgå manuel nummerering.

Du kan tildele nummerserier til de skabeloner, som du opretter til de forskellige typer debitorer og kreditorer, som dine sælgere og indkøbere oftest tilføjer. Hvis det er tilfældet, skal du oprette de relevante nummerserier, knytte dem gennem forhold og derefter tilføje den første nummerserie i den relevante relation til den relevante opsætningsside. Når en bruger opretter en kunde, vælger han derefter den relevante skabelon, og den nye debitor får et nummer, der er tildelt fra den nummerserie, der er defineret for den pågældende skabelon.  

## Sådan oprettes relationer mellem nummerserier

Hvis du har oprettet mere end en nummerseriekode for samme slags grundlæggende oplysninger eller transaktioner, kan du oprette relationer mellem koderne. Denne funktion kan være en hjælp ved valg af koder, når du bruger et nummer. Når du forbinder en gruppe af nummerserier, knytter du alle de relaterede serier til den samme nummerseriekode. Du kan derefter angive koden i et felt i oversigtspanelet **Nummerering** på en af den relevante opsætningsside, f. eks **Salgsopsætning**.  

1. Vælg ![Lightbulb, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, angiv **Nummerserie**, og vælg derefter det relaterede link.
2. Vælg linjen med den nummerserie, du vil oprette relationer for, og vælg derefter **Relationer**.
3. I feltet **Seriekode** skal du indtaste koden for de antal serier, du vil knytte til de serier, du valgte under trin to .
4. Tilføj en linje for hver kode, du vil knytte til den valgte nummerserie.
5. Luk siden.

Når du derefter opretter noget, der kræver et nummer, kan du bruge de relationer, du har oprettet, til at vælge mellem de relaterede nummerserier.

## Sådan definerer du, hvor en nummerserie skal bruges

Følgende procedure viser, hvordan du konfigurerer nummerserieren for området Salg. Trinene er som for andre områder.  

1. Vælg ![Lightbulb, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, angiv **Salg og tilgodehavender**, og vælg derefter det relaterede link.
2. På siden **Salg** i oversigtspanelet **Nummerserie** skal du vælge den ønskede nummerserie for hvert salgskort eller dokument.

Det valgte nummer bliver nu brugt til at udfylde feltet **Nummer** på det relevante kort eller dokument i overensstemmelse med de valgte indstillinger på nummerserielinjen.  

## Se også

[Opsætning af [!INCLUDE[prod_short](includes/prod_short.md)]](setup.md)  
[Arbejd med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
