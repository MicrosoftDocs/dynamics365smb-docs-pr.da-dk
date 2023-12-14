---
title: 'Konsolidere saldi for en virksomhed, som er debitor og kreditor'
description: 'Beskriver hvordan saldi for en kunde, der også er kreditor, konsolideres.'
author: brentholtorf
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 'payment process, cash receipt'
ms.search.form: '5052, 21, 5050'
ms.date: 10/11/2023
ms.author: bholtorf
---
# Konsolidere saldi for en virksomhed, som er debitor og kreditor
En virksomhed, som du gør forretninger med, kan være både debitor og kreditor. Hvis det er tilfældet, kan du undgå overflødige betalinger eller modtagelser og muligvis gemme på transaktions gebyrer ved at konsolidere virksomhedens debitor-og kreditorsaldi. Konsolideringen sammenligner virksomhedens saldi som leverandør og som kunde, og derefter komprimeres beløbet, så der enten bliver debitor-eller kreditorsaldoen tilbage, afhængigt af hvilket beløb der var højere. 

Hvis du vil konsolidere saldiene, skal du først knytte debitorerne og kreditor regnskaberne til en kontakt, der har typen **virksomhed**. En debitor eller kreditor kan kun have én kontakt af typen **virksomhed**. Du kan finde flere oplysninger i [Oprette kontakter](marketing-create-contact-companies.md).

Når du har knyttet regnskaberne, viser siden **debitorkort** feltet **saldoen som kreditor**, og siden **kreditorkort** indeholder feltet **saldo som kunde**.

Selvom det ikke er et krav, er debitor- og kreditorvirksomheder typisk den samme juridiske enhed. 

## Før du starter
Før du konsoliderer saldi, skal du angive nogle få indstillinger på siden **Marketing opsætning**. 

* I oversigtspanelet **interaktioner** skal du angive koder for forretningsforbindelser i felterne **Debitorer** og **Kreditorer**. [!INCLUDE[prod_short](includes/prod_short.md)] bruger disse oplysninger til at bestemme, hvilken type relation der skal vises for kontakter. 
* Valgfrit: slå Dubler søgning til eller fra i oversigtspanelet **dubletter**. Som standard er dubletsøgning aktiveret. Yderligere oplysninger finder du i [Håndtering af dubletter](#handling-duplicates). 

## Sammenkæd en eksisterende debitor, kreditor eller bankkonto via en kontakt
Følgende fremgangsmåde beskriver, hvordan en debitor og kreditor kædes sammen via en kontaktperson.

1. Vælg ![Lightbulb, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **Debitor** eller **Kreditor**, og vælg derefter det relaterede link.
2. Vælg debitor eller kreditor, og vælg derefter handlingen **Kontakt**.   
3. Vælg kontakten, og vælg derefter handlingen **Link til den eksisterende**.
4. Vælg den type objekt, du vil oprette en forretningsrelation med.
5. Udfyld felterne efter behov. [!INCLUDE [tooltip-inline-tip_md](includes/tooltip-inline-tip_md.md)]

## Oprette en kreditor fra en debitor eller omvendt
Du kan oprette en ny kreditor ud fra en eksisterende debitor eller en ny kunde hos en leverandør. Åbn siden **Kontakt** fra siderne **Debitor** eller **Kreditor**. Vælg handlingen **Opret som**, og vælg derefter enten **Debitor** eller **Kreditor**. 

## Oprette en ny debitor eller kreditor og knytte den til en leverandør eller en kundekontakt
1. Opret ny debitor eller kreditor. Du kan finde flere oplysninger i [Registrere nye debitorer](sales-how-register-new-customers.md) eller [Registrere nye debitorer](sales-how-register-new-customers.md).
2. Når du har oprettet debitoren eller kreditoren, skal du vælge **Opret**, og derefter vælge enten **Debitor**- eller **Kreditor**-indstillinger. 

## Konsolidere saldi for en virksomhed, som er debitor og kreditor
Brug handlingen **netto debitor/kreditorsaldi** på siden **Udbetalingskladde** til at konsolidere debitor-og kreditorsaldi til et enkelt nettobeløb. Aktionen oprettes, men den kan ikke bogføre, betalingskladdelinjer, som indeholder nettosaldiene.

> [!NOTE]
> Hvis debitor-eller kreditorsaldi indeholder beløb, der er i forskellige valutaer, oprettes der en linje for beløbet i hver valuta.

## Håndtere dubletter
Hvis du aktiverer dobbeltsøgning i oversigtspanelet **Dubletter** på siden **Marketingopsætning**, vises der en advarsel, når du ændrer værdierne i felter, som er en del af opsætningen, for dubletsøgestrenge. Når der findes en dublet, kan du udføre følgende handlinger:

* Kombiner de dublerede kontakter til en enkelt kontakt, der er ens for både debitoren og kreditoren ved hjælp af funktionen **fletning med**-muligheden på **kontaktkortet**. Som regel udføres sammenfletning af kontakter kun, når debitor og kreditor er den samme juridiske enhed. Du kan finde flere oplysninger i [Flette dublerede poster](sales-how-merge-duplicate-records.md). 
* Slet kreditorens forretningsrelation for kreditoren eller kontaktpersonen, og brug derefter **Linket til eksisterende**-handling til at oprette en kæde til en anden kontakt.    

## Se også
[Salg](sales-manage-sales.md)  
[Registrere nye debitorer](sales-how-register-new-customers.md)  
