---
title: Afstemme bankkonti og udligne betalinger | Microsoft Docs
description: "Beskriver opgaver, du kan bruge til at afstemme bankkonti, tilgodehavender og skyldige beløb, bogføre indbetalinger eller udgifter og udligne betalinger automatisk."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: payment process, direct payment posting, reconcile payment, expenses, cash receipts
ms.date: 10/01/2018
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 33b900f1ac9e295921e7f3d6ea72cc93939d8a1b
ms.openlocfilehash: e76e83344bafd4c2599c2adccc8a68c6f21ed1ad
ms.contentlocale: da-dk
ms.lasthandoff: 11/26/2018

---
# <a name="applying-payments-automatically-and-reconciling-bank-accounts"></a>Udligne betalinger automatisk og afstemme bankkonti
Rutinemæssigt skal du afstemme dine bank-, debet- og kreditkonti ved at udligne betalinger, der er registreret på din bankkonto, til deres relaterede ubetalte fakturaer og kreditnotaer eller andre åbne poster i [!INCLUDE[d365fin](includes/d365fin_long_md.md)].  

Du kan udføre denne opgave på siden **Betalingsudligningskladde** ved at importere en bankkontoudtogsfil eller et -feed for hurtigt at registrere betalinger. Betalinger udlignes til åbne debitor- eller kreditorposter baseret på sammenligninger i betalingstekst og oplysninger i poster. Du kan gennemse og ændre automatiske programmer, før du bogfører kladden. Du kan vælge at lukke alle åbne bankposter vedrørende de udlignede poster, når du bogfører kladden. Bankkontoen udlignes automatisk, når alle betalinger er udlignet.

Du kan også afstemme bankkonti uden at udligne betalinger samtidigt. Du kan udføre dette arbejde på siden **Bankkontoafstemning**. Du kan finde flere oplysninger i [Afstemme bankkonto separat](bank-how-reconcile-bank-accounts-separately.md).   

For at gøre det muligt at importere bankkontoudtog som feeds, skal du først konfigurere og aktivere tjenesten Envestnet Yodlee Bank kilder og derefter knytte dine bankkonti til de relaterede onlinebankkonti. Du kan finde flere oplysninger under [Konfigurere tjenesten Envestnet Yodlee Bank Feeds](bank-how-setup-bank-statement-service.md).  

Du kan også bruge tjenesten til konvertering af bankdata til at konvertere en bankudtogsfil fra ethvert filformat til en datastrøm, som du kan importere i [!INCLUDE[d365fin](includes/d365fin_long_md.md)]. Du kan finde flere oplysninger under [Konfigurere tjenesten til konvertering af bankdata](bank-how-setup-bank-data-conversion-service.md).  

Den følgende tabel indeholder en opgavesekvens med links til de emner, der rummer beskrivelserne af opgaverne.  

| Hvis du vil | Se |
| --- | --- |
| Udlign betalinger for at åbne debitor- eller kreditorposter ved at importere et bankkontoudtog og afstemme bankkontoen, når alle betalinger er udlignet. |[Afstemme betalinger ved hjælp af automatisk udligning](receivables-how-reconcile-payments-auto-application.md) |
| Udlign manuelt betalinger ved at få vist detaljerede oplysninger om afstemte data og forslag til åbne kandidatposter for at udligne betalinger til dem. |[Gennemse eller udligne betalinger efter automatisk udligning](receivables-how-review-apply-payments-auto-application.md) |
| Behandle betalinger, der ikke kan udlignes automatisk til de relaterede åbne poster. For eksempel fordi beløbene er forskellige, eller fordi en relateret post ikke findes. |[Afstemme betalinger, der ikke kan udlignes automatisk](receivables-how-reconcile-payments-cannot-apply-auto.md) |
| Sammenkæd teksten på betalinger til bestemte debitor-, kreditor- eller finanskonti for altid at bogføre tilbagevendende indbetalinger eller udgifter til disse konti, når der ikke findes nogen dokumenter at anvende dem på. |[Knytte tekst på tilbagevendende betalinger til automatisk afstemning af konti](receivables-how-map-text-recurring-payments-accounts-auto-reconcilliation.md) |

## <a name="see-also"></a>Se også
[Administrere tilgodehavender](receivables-manage-receivables.md)  
[Salg](sales-manage-sales.md)  
[Arbejde med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

