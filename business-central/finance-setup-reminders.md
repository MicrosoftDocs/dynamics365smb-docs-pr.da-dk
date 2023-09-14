---
title: Konfiguration af rykkerbetingelser og -niveauer
description: 'Få mere at vide om, hvordan du konfigurere Business Central, så du kan sende en påmindelse til kunden om en betaling, der er forfalden, og lægger gebyrer til betalingen på grund af forsinkelsen.'
author: brentholtorf
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 'payment due, debt, overdue, fee, charge, reminder'
ms.search.form: '431, 432, 436, 478'
ms.date: 02/09/2022
ms.author: bholtorf
---
# Konfiguration af rykkerbetingelser og -niveauer

Du kan bruge rykkere til at minde debitorer om forfaldne beløb. [!INCLUDE [reminder-terms](includes/reminder-terms.md)]

## Rykkerbetingelser

Hvis debitorer har forfaldne beløb, skal du afgøre, om der skal sendes en rykker. Desuden vil du evt. debitere deres konti for rente eller gebyrer. Du kan angive et hvilket som helst antal betingelser for rykkere.  

> [!NOTE]
> Hvis du vil beregne rente for forfaldne betalinger, kan du gøre det, når du opretter rykkere. Hvis du imidlertid bare vil beregne rente og informere debitorerne om dette uden at sende rykkere, bør du bruge [rentenotaer](finance-setup-finance-charges.md). Du kan finde flere oplysninger i [Rykkere](receivables-collect-outstanding-balances.md#reminders) eller [Rentegebyrer](receivables-collect-outstanding-balances.md#finance-charges).

### Sådan defineres rykkerbetingelser

1. Vælg ![Lightbulb, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **Rykkerbetingelser**, og vælg derefter det relaterede link.  
2. Udfyld felterne efter behov. [!INCLUDE [tooltip-inline-tip_md](includes/tooltip-inline-tip_md.md)]  
3. Hvis du vil bruge mere end én kombination af rykkerbetingelser, kan du angive en kode for hver enkelt.

## Rykkerniveauer

For hver rykkerbetingelseskode kan du definere et ubegrænset antal rykkerniveauer. Første gang en rykker oprettes til en debitor, bruges indstillingen fra niveau 1. Når rykkeren er udstedt, registreres niveaunummeret på de rykkerposter, der er oprettet og sammenkædet med de individuelle debitorposter. Hvis det er nødvendigt at rykke debitoren igen, markeres alle de rykkerposter, der er sammenkædet med åbne debitorposter, så nummeret på det højeste niveau bliver fundet. Derefter vil betingelserne fra det næste niveaunummer blive brugt til den nye rykker.

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
7. Hvis du vil indsætte relaterede værdier i den resulterende rykkertekst automatisk, skal du angive følgende pladsholdere i feltet **Tekst**.  

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

    Hvis du f.eks. skriver **Du skylder %9 %7, der forfalder den %2.**, vil den resulterende rykker indeholde følgende tekst: **Du skylder RV 1.200,50, der forfalder den 02-02-2014.**

    > [!NOTE]
    > Forfaldsdatoen beregnes i overensstemmelse med den datoformel, som du angiver. Du kan finde flere oplysninger i [Bruge datoformler](ui-enter-date-ranges.md#use-date-formulas).

Angiv en af koderne på hvert enkelt kundekort, når du har oprettet rykkerbetingelserne med ekstra niveauer og tekst. Du kan finde flere oplysninger i [Registrere nye debitorer](sales-how-register-new-customers.md).  

## Se relateret [Microsoft-træning](/training/modules/send-reminders-dynamics-365-business-central/)

## Se også

[Indhente udestående beløb](receivables-collect-outstanding-balances.md)  
[Send rykkere til udestående saldi](receivables-send-reminders.md)  
[Konfiguration af Rentebetingelser](finance-setup-finance-charges.md)  
[Konfigurere Finans](finance-setup-finance.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
