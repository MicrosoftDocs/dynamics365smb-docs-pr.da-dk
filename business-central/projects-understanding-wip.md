---
title: Metoder for igangværende arbejde til beregning og registrering af sagsstatus | Microsoft Docs
description: Beskriver de forskellige metoder for igangværende arbejde, du kan bruge til at bogføre, overvåge og beregne finansielle oplysninger for igangværende arbejdssager.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: work in process, work in progress, calculate project WIP
ms.date: 02/04/2020
ms.author: sgroespe
ms.openlocfilehash: ac6b41d9fe03968531b7d99e534055b6a9955f57
ms.sourcegitcommit: 0cb8a646dcba8f6d6336ebd008587874d25f4629
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 02/07/2020
ms.locfileid: "3030288"
---
# <a name="understanding-wip-methods"></a>Forstå VIA -metoder
Efterhånden som status for en sag ændrer sig, forbruges der materialer, ressourcer og andre udgifter, og disse skal bogføres i sagen. Igangværende arbejde er en funktion, som giver dig mulighed for at estimere den økonomiske værdi af sager i finansregnskabet under udførelsen af sagen. Du kan i mange tilfælde bogføre udgifterne for en sag, før sagen faktureres. Hvis der kun er bogført udgifter, vil din regnskabsopgørelse ikke være helt korrekt.

Du kan beregne VIA og bogføre værdien i finansregnskabet for at spore værdien i finansregnskabet. Du kan finde flere oplysninger under [Overvåge jobstatus og -udførelse](projects-how-monitor-progress-performance.md).

[!INCLUDE[d365fin](includes/d365fin_md.md)] understøtter følgende metoder til beregning og registrering af værdien af igangværende arbejde.

| VIA-metode | Beregningsformel | Beregningsbeskrivelse |
| --- | --- | --- |
| Kostværdi |Realiserede indtægter = Fakturerbar faktureret pris<br /><br /> Anslået kostbeløb = Fakturerbart salgsbeløb x Budgetomkostninger<br /><br /> VIA-omkostninger = (Færdiggørelsesgrad -faktureret % x Anslået kostbeløb<br /><br /> Færdiggørelsesgrad = Forbrug-kostbeløb/Budget-kostbeløb<br /> Faktureret % = Fakturerbar faktureret pris<br /><br /> Fakturerbart salgsbeløb realiserede omkostninger = Forbrug-kostbeløb - Igangværende arbejde |I beregninger af kostværdi startes der med at beregne værdien af det, der er leveret, idet der tages en del af det anslåede kostbeløb baseret på færdiggørelsesgrad. Fakturerede kostbeløb fratrækkes, ved at der tages en del af det anslåede kostbeløb baseret på faktureringsprocenten.<br /><br /> Denne beregning kræver, at fakturerbart salgsbeløb, budget-salgsbeløb og budget-kostbeløb angives korrekt for hele sagen. |
| Salgsomkostning |Realiserede indtægter = Fakturerbar faktureret pris<br /><br /> Realiserede omkostninger = Budget-kostbeløb x faktureringsprocent<br /><br /> Faktureret % = Fakturerbart faktureret salgsbeløb / Fakturerbart salgsbeløb<br /><br /> (Faktureret % findes som kolonne i sagsopgavelinjer)<br /><br /> Igangv. arbejder køb = Forbrug-kostbeløb – realiserede omkostninger |Beregninger af salgsomkostninger starter med beregning af realiserede omkostninger. Omkostninger realiseres proportionalt baseret på budgetteret kostbeløb.<br /><br /> Denne beregning kræver, at det fakturerbare salgsbeløb og det budgetterede kostbeløb angives korrekt for hele sagen. |
| Salgsværdi |Realiserede omkostninger = Forbrug-kostbeløb<br /><br /> Realiseret indtægt = Forbrug-salgsbeløb x Forventet faktureringsforhold<br /><br /> Omkostningsdækningspct. % = Fakturerbart salgsbeløb/Budgetteret salgsbeløb<br /><br /> Igangværende arbejde salg = Realiseret salg - Fakturerbart faktureret salgsbeløb |I beregninger af salgsværdi realiseres indtægter proportionalt baseret på Forbrug-kostbeløb og det forventede omkostningsdækningsforhold.<br /><br /> Denne beregning kræver, at det fakturerbare salgsbeløb og det budgetterede salgsbeløb angives korrekt for hele sagen. |
| Færdiggørelsesgrad |Realiserede omkostninger = Forbrug-kostbeløb<br /><br /> Realiseret indtægt = Fakturerbar salgspris x Færdiggørelsesgrad<br /><br /> Færdiggørelsesgrad = Forbrug-kostbeløb/Budget-kostbeløb<br /> (Kaldes “Fuldførelse af omkostning i % “ på sagsopgavelinjer)<br /><br /> Igangværende arbejde salg = Realiseret salg - Fakturerbart faktureret salgsbeløb |I beregninger af færdiggørelsesgrad realiseres indtægt proportionalt baseret på færdiggørelsesgraden, dvs. Forbrug-kostbeløb over for Budgetomkostninger.<br /><br /> Denne beregning kræver, at det fakturerbare salgsbeløb og det budgetterede kostbeløb angives korrekt for hele sagen. |
| Afsluttet kontrakt |VIA-beløb = VIA-kostbeløb = Forbrug (kostbeløb)<br /><br /> Igangværende arbejde - salgsbeløb = Fakturerbar (faktureret salg) |Afsluttet kontrakt realiserer ikke indtægter og omkostninger, før sagen er afsluttet. Du kan vælge denne metode, hvis der er stor tvivl omkring de anslåede kostbeløb og sagens omsætning.<br /><br /> Alt forbrug bogføres til kontoen til VIA-omkostninger (aktiv), og alt faktureret salg bogføres til kontoen til faktureret VIA-salg (kreditorkonto), indtil sagen er afsluttet. |

## <a name="see-also"></a>Se også
[Projektstyring](projects-manage-projects.md)  
[Finans](finance.md)  
[Køb](purchasing-manage-purchasing.md)         
[Salg](sales-manage-sales.md)      
[Arbejde med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)  
