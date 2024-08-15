---
title: Gennemgå og udlign betalinger manuelt efter automatisk udligning
description: 'Når betalinger udlignes automatisk, kan du gennemse alle poster for en betaling og genanvende dem, der blev udlignet forkert, manuelt.'
author: brentholtorf
ms.topic: conceptual
ms.devlang: al
ms.search.keywords: 'payment process, reconcile payment, expenses, cash receipts'
ms.search.form: '1290, 1294, 1287'
ms.date: 05/30/2024
ms.author: bholtorf
ms.service: dynamics-365-business-central
ms.reviewer: bholtorf
---
# Gennemgå og udlign betalinger manuelt efter automatisk udligning
For hver kladdelinje, der repræsenterer en betaling på siden **Betalingsudligningskladde**, kan du åbne siden **Betalingsudligning** for at få vist alle åbne kandidatposter for betalingen og se detaljerede oplysninger for hver post om den dataafstemning, som en betalingsudligning er baseret på. Her kan du manuelt udligne betalinger eller udligne betalinger igen, der er udlignet automatisk til en forkert post. Du kan finde flere oplysninger om automatisk udligning i [Afstemme betalinger ved hjælp af automatisk udligning](receivables-how-reconcile-payments-auto-application.md).

> [!IMPORTANT]  
>   Når den bankkonto, som du afstemmer betalinger for, er sat op til den lokale valuta, viser siden **Betalingsudligning** alle åbne poster i den lokale valuta, herunder åbne poster for dokumenter, der oprindeligt blev faktureret i udenlandsk valuta. Betalinger, der er udlignet til poster med de omregnede valutaer, kan derfor blive bogført med andre beløb end i det oprindelige dokument på grund af de potentielt forskellige valutakurser, der bruges af henholdsvis banken og [!INCLUDE[prod_short](includes/prod_short.md)].

Vi anbefaler derfor, at du ser efter udenlandske valutakoder i feltet **Valutakode** på siden **Betalingsudligning** for at kontrollere, om udligninger er baseret på omregnede valutaer. Gennemgå det oprindelige dokumentbeløb i udenlandsk valuta og se den valutakurs, der bruges, ved at vælge feltet **Udlign.løbenr.** og derefter bruge genvejsmenuen til at vælge knappen Specificer for at åbne siden **Debitorposter** eller siden **Kreditorposter**.

Eventuelle gevinst- og tabsjusteringer, der kræves på grund af valutaomregninger, håndteres ikke automatisk af [!INCLUDE[prod_short](includes/prod_short.md)].

> [!NOTE]  
>   Du kan udligne poster med et andet fortegn end tegnet for betalingen. For eksempel skal du for at lukke en kreditnota med negativt fortegn og dens relaterede faktura med positivt fortegn først udligne kreditnotaen med fakturaen og derefter udligne betalingen med fakturaen med reduceret restbeløb.

> [!WARNING]  
>   Hvis du bruger kontantrabatter, og hvis betalingsdatoen ligger før betalingens forfaldsdato, bruges feltet **Restbeløb inkl. rabat** på siden **Betalingsudligning** til afstemning. Ellers bruges værdien i feltet **Restbeløb**. Hvis betalingen blev foretaget med et rabatbeløb efter betalingens forfaldsdato, eller det fulde beløb er betalt, men der blev givet en rabat, vil beløbet ikke matche.

> [!NOTE]  
>   Du kan kun udligne en betaling på én konto. Hvis du vil fordele udligningen på flere åbne poster, for eksempel for at udligne et fast beløb, skal de åbne poster være for den samme konto. Yderligere oplysninger finder du i trin 7 og 8 i proceduren i dette emne.

## Sådan gennemser eller udligner du betalinger efter automatisk udligning
1. Vælg ![Lightbulb, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **Betalingsudligningskladder**, og vælg derefter det relaterede link.
2. Åbn kladden for betalingsafstemning for en bankkonto, som du vil afstemme betalinger for. Du kan finde flere oplysninger i [Afstemme betalinger ved hjælp af automatisk udligning](receivables-how-reconcile-payments-auto-application.md).
3. På siden **Betalingsudligningskladde** skal du markere en betaling, du vil gennemse eller udligne manuelt til en eller flere åbne poster og derefter vælge handlingen **Anvend manuelt**.
4. Markér afkrydsningsfeltet **Udlignet** på linjen for den åbne post, som du vil udligne betalingen på.
5. Det betalte beløb, som også vises i feltet **Transaktionsbeløb** på siden **Betalingsudligning**, er indsat i feltet **Udligningsbeløb**, men du kan redigere feltet, for eksempel hvis du vil anvende beløbet på flere åbne poster.
6. Hvis du vil udligne en del af det betalte beløb til en anden åben post for kontoen, for eksempel for at udligne et fast beløb, skal du markere afkrydsningsfeltet **Udlignet** ud for linjen. Det udlignede beløb fratrækkes automatisk transaktionsbeløbet for at afspejle fordelingen på de to åbne poster.
7. Hvis du vil udligne en del af en betaling med en eller flere åbne poster, der ikke findes i databasen, skal du oprette en ny linje under linjen for den samme konto. I feltet **Udligningsbeløb** skal du indtaste det beløb, der skal udlignes på den nye linje, og derefter justere feltet **Udligningsbeløb** på den eksisterende linje.
8. Gentag trin 5, 6 eller 7 for andre åbne poster, du vil udligne et fuldt eller delvist betalingsbeløb til.
9. Når du har gennemset en betalingsudligning eller manuelt har udlignet på en eller flere åbne poster, skal du vælge handlingen **Accepter udligning**.

Siden **Udligningsbeløb** lukkes, og på siden **Betalingsudligningskladde** ændres værdien i **Matchtillid** til **Accepteret** for at angive, at du har gennemset eller manuelt udlignet betalingen.

## Se også
[Administrere tilgodehavender](receivables-manage-receivables.md)  
[Salg](sales-manage-sales.md)  
[Arbejd med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]