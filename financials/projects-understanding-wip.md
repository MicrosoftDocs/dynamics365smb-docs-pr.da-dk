---
title: "Metoder for igangværende arbejde til beregning og registrering af sagsstatus | Microsoft Docs"
description: "Beskriver de forskellige metoder for igangværende arbejde, du kan bruge til at bogføre, overvåge og beregne finansielle oplysninger for igangværende arbejdssager."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: work in process, work in progress, calculate project WIP
ms.date: 06/06/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: eea34afbee429d14ab150894729cb4ea3843bb2b
ms.openlocfilehash: a0472a85be4911adacf3033c2feb6bd1513af925
ms.contentlocale: da-dk
ms.lasthandoff: 12/14/2017

---
# <a name="understanding-wip-methods"></a>Forstå VIA -metoder
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

