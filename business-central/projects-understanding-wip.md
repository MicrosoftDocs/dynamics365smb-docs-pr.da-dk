---
title: Metoder for igangværende arbejde til beregning og registrering af sagsstatus
description: Beskriver de forskellige metoder for igangværende arbejde, du kan bruge til at bogføre, overvåge og beregne finansielle oplysninger for igangværende arbejdssager.
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: work in process, work in progress, calculate project WIP
ms.search.form: 1010
ms.date: 04/01/2021
ms.author: edupont
ms.openlocfilehash: 09568ab62f9bbc52014583cfc322bfefaf5102e4
ms.sourcegitcommit: 93f30ce3349233cbcd03f300e74b654b49fa5518
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 05/24/2022
ms.locfileid: "8799508"
---
# <a name="understanding-wip-methods-in-project-management"></a>Forstå via-metoder i projektstyring

Efterhånden som status for en sag ændrer sig, forbruges der materialer, ressourcer og andre udgifter, og disse skal bogføres i sagen. Igangværende arbejde er en funktion, som giver dig mulighed for at estimere den økonomiske værdi af sager i finansregnskabet under udførelsen af sagen. Du kan i mange tilfælde bogføre udgifterne for en sag, før sagen faktureres. Hvis der kun er bogført udgifter, vil din regnskabsopgørelse ikke være helt korrekt.

Du kan beregne VIA og bogføre værdien i finansregnskabet for at spore værdien i finansregnskabet. Du kan finde flere oplysninger i [Overvåge jobstatus og -udførelse](projects-how-monitor-progress-performance.md).

[!INCLUDE[prod_short](includes/prod_short.md)] understøtter følgende metoder til beregning og registrering af værdien af igangværende arbejde.

| VIA-metode | Beregningsformel | Beregningsbeskrivelse |
| --- | --- | --- |
| Kostværdi |Realiserede indtægter = Fakturerbar faktureret pris<br /><br /> Anslået kostbeløb = Fakturerbart salgsbeløb x Budgetomkostninger<br /><br /> VIA-omkostninger = (Færdiggørelsesgrad -faktureret %) x Anslået kostbeløb<br /><br /> Færdiggørelsesgrad = Forbrug-kostbeløb/Budget-kostbeløb<br /><br />Faktureret % = Fakturerbar faktureret pris<br /><br /> Fakturerbart salgsbeløb realiserede omkostninger = Forbrug-kostbeløb - Igangværende arbejde |I beregninger af kostværdi startes der med at beregne værdien af det, der er leveret, idet der tages en del af det anslåede kostbeløb baseret på færdiggørelsesgrad. Fakturerede kostbeløb fratrækkes, ved at der tages en del af det anslåede kostbeløb baseret på faktureringsprocenten.<br /><br />Denne beregning kræver, at fakturerbart salgsbeløb, budget-salgsbeløb og budget-kostbeløb angives korrekt for hele sagen. |
| Salgsomkostning |Realiserede indtægter = Fakturerbar faktureret pris<br /><br /> Realiserede omkostninger = Budget-kostbeløb x faktureringsprocent<br /><br /> Faktureret % = Fakturerbart faktureret salgsbeløb / Fakturerbart salgsbeløb<br /> (Faktureret % findes som en kolonne i sagsopgavelinjer)<br /><br /> Igangv. arbejder køb = Forbrug-kostbeløb – realiserede omkostninger |Beregninger af salgsomkostninger starter med beregning af realiserede omkostninger. Omkostninger realiseres proportionalt baseret på budgetteret kostbeløb.<br /><br /> Denne beregning kræver, at det fakturerbare salgsbeløb og det budgetterede kostbeløb angives korrekt for hele sagen. |
| Salgsværdi |Realiserede omkostninger = Forbrug-kostbeløb<br /><br /> Realiseret indtægt = Forbrug-salgsbeløb x Forventet faktureringsforhold<br /><br /> Omkostningsdækningspct. % = Fakturerbart salgsbeløb/Budgetteret salgsbeløb<br /><br /> Igangværende arbejde salg = Realiseret salg - Fakturerbart faktureret salgsbeløb |I beregninger af salgsværdi realiseres indtægter proportionalt baseret på Forbrug-kostbeløb og det forventede omkostningsdækningsforhold.<br /><br /> Denne beregning kræver, at det fakturerbare salgsbeløb og det budgetterede salgsbeløb angives korrekt for hele sagen. |
| Færdiggørelsesgrad |Realiserede omkostninger = Forbrug-kostbeløb<br /><br /> Realiseret indtægt = Fakturerbar salgspris x Færdiggørelsesgrad<br /><br /> Færdiggørelsesgrad = Forbrug-kostbeløb/Budget-kostbeløb<br /> (Hentet i feltet **Fuldførelse af omkostning i %** på Sagsopgavelinjer)<br /><br /> Igangværende arbejde salg = Realiseret salg - Fakturerbart faktureret salgsbeløb |I beregninger af færdiggørelsesgrad realiseres indtægt proportionalt baseret på færdiggørelsesgraden, dvs. Forbrug-kostbeløb over for Budgetomkostninger.<br /><br /> Denne beregning kræver, at det fakturerbare salgsbeløb og det budgetterede kostbeløb angives korrekt for hele sagen. |
| Afsluttet kontrakt |VIA-beløb = VIA-kostbeløb = Forbrug (kostbeløb)<br /><br /> Igangværende arbejde - salgsbeløb = Fakturerbar (faktureret salg) |Afsluttet kontrakt realiserer ikke indtægter og omkostninger, før sagen er afsluttet. Du kan vælge denne metode, hvis der er stor tvivl omkring de anslåede kostbeløb og sagens omsætning.<br /><br /> Alt forbrug bogføres til kontoen til VIA-omkostninger (aktiv), og alt faktureret salg bogføres til kontoen til faktureret VIA-salg (kreditorkonto), indtil sagen er afsluttet. |

## <a name="see-also"></a>Se også

[Projektstyring](projects-manage-projects.md)  
[Finans](finance.md)  
[Køb](purchasing-manage-purchasing.md)  
[Salg](sales-manage-sales.md)  
[Arbejd med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]