---
title: Konfiguration af rykkerbetingelser og -niveauer
description: 'Få mere at vide om, hvordan du konfigurere Business Central, så du kan sende en påmindelse til kunden om en betaling, der er forfalden, og lægger gebyrer til betalingen på grund af forsinkelsen.'
author: brentholtorf
ms.topic: conceptual
ms.devlang: al
ms.search.keywords: 'payment due, debt, overdue, fee, charge, reminder'
ms.search.form: '431, 432, 436, 478'
ms.date: 03/12/2024
ms.author: bholtorf
ms.service: dynamics-365-business-central
---
# Konfiguration af rykkerbetingelser og -niveauer

Du kan bruge rykkere til at minde debitorer om forfaldne beløb og opkræve betaling. [!INCLUDE [reminder-terms](includes/reminder-terms.md)]

> [!TIP]
> Når du har oprettet betingelser og niveauer for rykkere, kan du medtage dem i automatiserede processer til oprettelse, udstedelse og afsendelse af rykkere. Du kan få mere at vide om den automatiserede proces ved at gå til [Automatisere påmindelser i samlinger](finance-automate-reminders.md).

## Rykkerbetingelser

Hvis debitorer har forfaldne beløb, skal du afgøre, om der skal sendes en rykker. Desuden vil du evt. debitere deres konti for rente eller gebyrer. Du kan angive et hvilket som helst antal betingelser for rykkere.  

> [!NOTE]
> Hvis du vil beregne rente for forfaldne betalinger, kan du gøre det, når du opretter rykkere. Hvis du imidlertid bare vil beregne rente og informere debitorerne om dette uden at sende en rykker, kan du bruge en [rentenota](finance-setup-finance-charges.md). Du kan finde flere oplysninger i [Rykkere](receivables-collect-outstanding-balances.md#reminders) eller [Rentegebyrer](receivables-collect-outstanding-balances.md#finance-charges).

### Konfigurere vedhæftede filer og brødtekster til meddelelser

På siden **Opsætning af rykkervilkår** kan du konfigurere tekster til vedhæftede filer og standardmails, der enten skal bruges til alle rykkerniveauer eller oprette specifikke meddelelser for hvert niveau. Tonen eller indholdet i den meddelelse, du sender for det første rykkerniveau, kan f.eks. være anderledes end i anden eller tredje meddelelse. Hvis du vil oprette tekst til vedhæftede filer og mails til alle niveauer, skal du vælge **Debitorkommunikation** øverst på siden. Hvis du vil oprette meddelelser til bestemte linjer, skal du vælge en linje i oversigtspanelet **Rykkerniveau** og derefter vælge handlingen **Debitorkommunikation** i oversigtspanelet.

Som standard bruger tekster til vedhæftede filer og mails din sprogindstilling. Men hvis du udsteder rykkere til kunder i andre lande, kan det være en god idé at kommunikere på forskellige sprog. Du kan oprette tekster til hvert sprog, som [!INCLUDE [prod_short](includes/prod_short.md)] understøtte, ved hjælp af handlingen **Føj tekst til sprog**. Hvis du gør det, skal du sikre dig, at sprogene er de samme for tekster til vedhæftede filer og mailtekster. Hvis de ikke stemmer overens, og rykkervilkårene har mere end ét niveau, kan automatiseringen muligvis ikke tilpasse meddelelsen for et eller flere niveauer. Du kan kontrollere, at sprogene stemmer overens, ved at bruge handlingen **Oversigt over kommunikation** og sammenligne kommunikationen for teksterne.

Når du sender en mail, er påmindelsen en rapport, du vedhæfter til mailen. Du definerer den rapport, der genererer rykkeren, på siden **Rapportvalg - rykkere og rentenotaer**, hvor du også vælger den rapport, der indeholder brødteksten i mailen, i feltet **Navn på layout for brødtekst i mail**. Når du sender mails til dine kunder, indsættes teksterne i oversigtspanelet **Mailtekst** i den rapport, der er valgt i feltet **Navn på layout for brødtekst i mail**. Standardrapporten indeholder et tekstfelt til denne tekst. Hvis du vil, kan du redigere rapporten, f.eks. for at tilføje eller fjerne indhold. Rediger layoutet af disse rapporter på siden **Rapportlayout**. Du kan få mere at vide om rapportlayout ved at gå til [Introduktion til oprettelse af rapportlayout](ui-get-started-layouts.md).

> [!NOTE]
> Kommunikation via mail direkte fra [!INCLUDE [prod_short](includes/prod_short.md)] kræver, at du er konfigureret til at gøre det. Du kan få mere at vide om, hvordan du knytter mailkonti til [!INCLUDE [prod_short](includes/prod_short.md)], ved at gå til [Konfigurere mail](admin-how-setup-email.md).

### Konfigurere rykkerbetingelser

1. Vælg det ![lyspæreikon, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **Rykkerbetingelser**, og vælg derefter det relaterede link.  
2. Udfyld felterne efter behov. [!INCLUDE [tooltip-inline-tip_md](includes/tooltip-inline-tip_md.md)]  
3. Hvis du vil bruge mere end én kombination af rykkerbetingelser, kan du angive en kode for hver enkelt.

## Rykkerniveauer

For hver rykkerbetingelse kan du definere et ubegrænset antal rykkerniveauer, selvom de fleste virksomheder kun bruger to eller tre niveauer. Første gang en rykker oprettes til en debitor, bruges indstillingen fra niveau 1. Når rykkeren er udstedt, registreres niveaunummeret på de rykkerposter, der er oprettet og sammenkædet med de individuelle debitorposter. Hvis det er nødvendigt at rykke debitoren igen, markeres alle de rykkerposter, der er sammenkædet med åbne debitorposter, så nummeret på det højeste niveau bliver fundet. Derefter vil betingelserne fra det næste niveaunummer blive brugt til den nye rykker.

Hvis du opretter flere rykkere end du har defineret niveauer til, bruges betingelserne for det højeste niveau. Du kan oprette så mange rykkere, som tillades ifølge feltet **Maks. antal rykkere** under rykkerbetingelserne.

### Sådan angives rykkerniveauer

1. Vælg ![Lightbulb, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **Rykkerbetingelser**, og vælg derefter det relaterede link.  
2. Vælg den linje med de betingelser, du vil oprette niveauer for, på siden **Rykkerbetingelser**, og vælg derefter handlingen **Niveauer**.  
3. Udfyld felterne efter behov. [!INCLUDE [tooltip-inline-tip_md](includes/tooltip-inline-tip_md.md)]  

    > [!TIP]
    > Indstillingen i feltet **Beregn rente** angiver, om der vises rente på rykkeren, når rykkeren udstedes. Men feltet **Bogfør rente** på siden **Rykkerbetingelser** angiver, om den beregnede rente skal bogføres på finans-og debitorkonti.
    >
    > For at angive, at renten skal beregnes, skal du vælge feltet **Beregn rente**.

    Du kan også angive opkrævningsgebyrer i både RV og i udenlandsk valuta for hvert rykkerniveau. Du kan definere adskillige opkrævningsgebyrer i udenlandsk valuta for hver kode på siden **Rykkerniveauer**.  

    Opkrævnings gebyrerne kan beregnes på tre forskellige måder, der er defineret af værdien i feltet **Tilføj gebyr beregnings type**.  

    - **Fast**

        Gebyrer beregnes på grundlag af værdierne i felterne **Opkrævningsgebyr** på linjen for selve rykkerniveauet.  
    - **Enkelt dynamisk**

        Gebyrer beregnes på grundlag af værdierne i felterne **Konfiguration af opkrævningsgebyr** på den relevante linje for selve rykkerniveauet.
    - **Akkumuleret dynamisk**

        Gebyrer beregnes på grundlag af værdierne i felterne på siden **Konfiguration af opkrævningsgebyr** på de kombinerede linjer til selve rykkerniveauet.

4. Vælg handlingen **Valutaer**.
5. På siden **Valutaer til rykkerniveau** definerer du for hver rykkerniveaukode og tilsvarende rykkerniveaunummer en valutakode og et opkrævningsgebyr.

    > [!NOTE]  
    > Når du opretter rykkere i en udenlandsk valuta, bruges betingelserne for udenlandsk valuta, som du angiver her, til automatisk at oprette rykkere. Hvis der ikke er defineret rykkerbetingelser i udenlandske valutaer, bruges de rykkerbetingelser, der er angivet på siden **Rykkerniveauer**, og derefter konverteres de til den relevante valuta.

    For hvert rykkerniveau kan du angive tekst, som bliver udskrevet inden (**Starttekst**) eller efter (**Sluttekst**) på posterne på rykkeren.

6. Vælg henholdsvis handlingen **Starttekst** eller **Sluttekst**, og udfyld på siden **Rykkertekst**.
7. Hvis du vil indsætte relaterede værdier i rykkerteksten automatisk, kan du angive følgende pladsholdere i feltet **Tekst**.  

    |Pladsholder|Værdi|  
    |-----------------|-----------|  
    |%1|Indholdet af feltet **Bilagsdato** på rykkerhovedet|  
    |%2|Indholdet af feltet **Forfaldsdato** på rykkerhovedet|  
    |%3|Indholdet af feltet **Rentesats** på de relaterede rentebetingelser|  
    |%4|Indholdet af feltet **Restbeløb** på rykkerhovedet|  
    |%5|Indholdet af feltet **Rentebeløb** på rykkerhovedet|  
    |%6|Indholdet af feltet **Opkrævningsgebyr** på rykkerhovedet|  
    |%7|Rykkerens totalbeløb|  
    |%8|Indholdet af feltet **Rykkerniveau** på rykkerhovedet|  
    |%9|Indholdet af feltet **Valutakode** på rykkerhovedet|  
    |%10|Indholdet af feltet **Bogføringsdato** på rykkerhovedet|  
    |%11|Firmanavnet.|  
    |%12|Indholdet af feltet **Opkrævningsgebyr pr. linje** på rykkerhovedet|  

    Hvis du f.eks. skriver **Du skylder %9 %7, der forfalder den %2.**, vil rykkeren indeholde følgende tekst: **Du skylder RV 1.200,50, der forfalder den 02-02-2024.**

    > [!NOTE]
    > [!INCLUDE [prod_short](includes/prod_short.md)] beregner forfaldsdatoen i overensstemmelse med den datoformel, som du angiver. Du kan finde flere oplysninger i [Bruge datoformler](ui-enter-date-ranges.md#use-date-formulas).

8. Hvis du vil angive sproget for en mail, skal du vælge handlingen **Tilføj tekst til sprog**. Feltet **Sprogkode** opdateres, så dit valg vises. Angiv indholdet af meddelelsen på det valgte sprog i oversigtspanelet **Mailtekst**.

Når du har oprettet rykkerbetingelserne, kan du knytte dem til debitorer på siderne med debitorkort. Du kan finde flere oplysninger i [Registrere nye debitorer](sales-how-register-new-customers.md).  

## Se også

[Indhente udestående beløb](receivables-collect-outstanding-balances.md)  
[Send rykkere til udestående saldi](receivables-send-reminders.md)  
[Konfiguration af Rentebetingelser](finance-setup-finance-charges.md)  
[Konfigurere Finans](finance-setup-finance.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
