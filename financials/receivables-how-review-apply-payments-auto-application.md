---
title: Kontrollere automatisk udlignede betalinger og udligne betalinger igen manuelt | Microsoft Docs
description: "Når betalinger udlignes automatisk, kan du gennemse alle poster for en betaling og genanvende dem, der blev udlignet forkert, manuelt."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: payment process, reconcile payment, expenses, cash receipts
ms.date: 03/29/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: bec0619be0a65e3625759e13d2866ac615d7513c
ms.openlocfilehash: 745766657fe7e993aaa689f0074c4f4a41e0090c
ms.contentlocale: da-dk
ms.lasthandoff: 03/22/2018

---
# <a name="review-or-apply-payments-manually-after-automatic-application"></a>Gennemse eller udligne betalinger manuelt efter automatisk udligning
For hver kladdelinje, der repræsenterer en betaling i vinduet **Betalingsudligningskladde**, kan du åbne vinduet **Betalingsudligning** for at få vist alle åbne kandidatposter for betalingen og se detaljerede oplysninger for hver post om den dataafstemning, som en betalingsudligning er baseret på. Her kan du manuelt udligne betalinger eller udligne betalinger igen, der er udlignet automatisk til en forkert post. Du kan finde flere oplysninger om automatisk udligning i [Afstemme betalinger ved hjælp af automatisk udligning](receivables-how-reconcile-payments-auto-application.md).

> [!IMPORTANT]  
>   Når den bankkonto, som du afstemmer betalinger for, er sat op til den lokale valuta, viser vinduet **Betalingsudligning** alle åbne poster i den lokale valuta, herunder åbne poster for dokumenter, der oprindeligt blev faktureret i udenlandsk valuta. Betalinger, der er udlignet til poster med de omregnede valutaer, kan derfor blive bogført med andre beløb end i det oprindelige dokument på grund af de potentielt forskellige valutakurser, der bruges af henholdsvis banken og [!INCLUDE[d365fin](includes/d365fin_md.md)].

Vi anbefaler derfor, at du ser efter udenlandske valutakoder i feltet **Valutakode** i vinduet **Betalingsudligning** for at kontrollere, om udligninger er baseret på omregnede valutaer. Gennemgå det oprindelige dokumentbeløb i udenlandsk valuta og se den valutakurs, der bruges, ved at vælge feltet **Udlign.løbenr.** og derefter bruge genvejsmenuen til at vælge knappen Specificer for at åbne vinduet **Debitorposter** eller vinduet **Kreditorposter**.

Eventuelle justeringer af gevinster og tab, der kræves på grund af valutaomregninger, behandles ikke automatisk af [!INCLUDE[d365fin](includes/d365fin_md.md)].

> [!NOTE]  
>   Du kan udligne poster med et andet fortegn end tegnet for betalingen. For eksempel skal du for at lukke en kreditnota med negativt fortegn og dens relaterede faktura med positivt fortegn først udligne kreditnotaen med fakturaen og derefter udligne betalingen med fakturaen med reduceret restbeløb.

> [!WARNING]  
>   Hvis du bruger kontantrabatter, og hvis betalingsdatoen ligger før betalingens forfaldsdato, bruges feltet **Restbeløb inkl. rabat** i vinduet **Betalingsudligning** til afstemning. Ellers bruges værdien i feltet **Restbeløb**. Hvis betalingen blev foretaget med et rabatbeløb efter betalingens forfaldsdato, eller det fulde beløb er betalt, men der blev givet en rabat, vil beløbet ikke matche.

> [!NOTE]  
>   Du kan kun udligne en betaling på én konto. Hvis du vil fordele udligningen på flere åbne poster, for eksempel for at udligne et fast beløb, skal de åbne poster være for den samme konto. Yderligere oplysninger finder du i trin 7 og 8 i proceduren i dette emne.

## <a name="to-review-or-apply-payments-after-automatic-application"></a>Sådan gennemser eller udligner du betalinger efter automatisk udligning
1. Vælg ikonet ![Søg efter side eller rapport](media/ui-search/search_small.png "Ikonet Søg efter side eller rapport"), angiv **Betalingsudbetalingskladder**, og vælg derefter det relaterede link.
2. Åbn kladden for betalingsafstemning for en bankkonto, som du vil afstemme betalinger for. Du kan finde flere oplysninger i [Afstemme betalinger ved hjælp af automatisk udligning](receivables-how-reconcile-payments-auto-application.md).
3. I vinduet **Betalingsudligningskladde** skal du markere en betaling, du vil gennemse eller udligne manuelt til en eller flere åbne poster og derefter vælge handlingen **Anvend manuelt**.
4. Markér afkrydsningsfeltet **Udlignet** på linjen for den åbne post, som du vil udligne betalingen på.
5. Det betalte beløb, som også vises i feltet **Transaktionsbeløb** i vinduet **Betalingsudligning**, er indsat i feltet **Udligningsbeløb**, men du kan redigere feltet, for eksempel hvis du vil anvende beløbet på flere åbne poster.
6. Hvis du vil udligne en del af det betalte beløb til en anden åben post for kontoen, for eksempel for at udligne et fast beløb, skal du markere afkrydsningsfeltet **Udlignet** ud for linjen. Det udlignede beløb fratrækkes automatisk transaktionsbeløbet for at afspejle fordelingen på de to åbne poster.
7. Opret en ny linje under linjen for den samme konto for at udligne en del af en betaling til en eller flere åbne poster, der ikke findes i databasen. I feltet **Udligningsbeløb** skal du indtaste det beløb, der skal udlignes på den nye linje, og derefter justere feltet **Udligningsbeløb** på den eksisterende linje.
8. Gentag trin 5, 6 eller 7 for andre åbne poster, du vil udligne et fuldt eller delvist betalingsbeløb til.
9. Når du har gennemset en betalingsudligning eller manuelt har udlignet på en eller flere åbne poster, skal du vælge handlingen **Accepter udligning**.

Vinduet **Udligningsbeløb** lukkes, og i vinduet **Betalingsudligningskladde** ændres værdien i **Matchtillid** til **Accepteret** for at angive, at du har gennemset eller manuelt udlignet betalingen.

## <a name="see-also"></a>Se også
[Administrere tilgodehavender](receivables-manage-receivables.md)  
[Salg](sales-manage-sales.md)  
[Arbejde med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

