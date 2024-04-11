---
title: Metoder for igangværende arbejde til beregning og registrering af projektstatus
description: 'Beskriver de forskellige metoder for igangværende arbejde, du kan bruge til at bogføre, overvåge og beregne finansielle oplysninger for igangværende projekter.'
author: brentholtorf
ms.author: bholtorf
ms.reviewer: andreipa
ms.topic: conceptual
ms.search.keywords: 'work in process, work in progress, calculate project WIP'
ms.search.form: '1010,'
ms.date: 02/22/2024
ms.service: dynamics-365-business-central
ms.custom: bap-template
---
# Forstå via-metoder i projektstyring

Efterhånden som status for et projekt ændrer sig, forbruges der materialer, ressourcer og andre udgifter, og disse skal bogføres i projektet. Igangværende arbejde er en funktion, som giver dig mulighed for at estimere den økonomiske værdi af projekter i finansregnskabet under udførelsen af projektet. Du kan i mange tilfælde bogføre udgifterne for et projekt, før projektet faktureres. Hvis der kun er bogført udgifter, vil din regnskabsopgørelse ikke være helt korrekt.

Du kan beregne VIA og bogføre værdien i finansregnskabet for at spore værdien i finansregnskabet. Du kan finde flere oplysninger i [Overvåge projektstatus og -udførelse](projects-how-monitor-progress-performance.md).

[!INCLUDE[prod_short](includes/prod_short.md)] understøtter følgende metoder til beregning og registrering af værdien af igangværende arbejde.

| VIA-metode | Beregningsformel | Beregningsbeskrivelse |
| --- | --- | --- |
| Kostværdi |Realiserede indtægter = Fakturerbar faktureret pris <br /><br />Budgetterede omkostninger = Budgetteret kostbeløb / Budgetteret salgsbeløb <br /><br />Anslået kostbeløb = Fakturerbart salgsbeløb x Budgetomkostninger <br /><br />Færdiggørelsesgrad = Forbrug-kostbeløb/Budget-kostbeløb <br /><br />Faktureret % = Fakturerbart faktureret salgsbeløb / Fakturerbart salgsbeløb <br /><br />VIA-omkostninger = (Færdiggørelsesgrad -faktureret %) x Anslået kostbeløb <br /><br />Realiserede omkostninger = Forbrug-kostbeløb – Igangværende omkostninger|I beregninger af kostværdi startes der med at beregne værdien af det, der er leveret, idet der tages en del af det anslåede kostbeløb baseret på færdiggørelsesgrad. Fakturerede kostbeløb fratrækkes, ved at der tages en del af det anslåede kostbeløb baseret på faktureringsprocenten.<br /><br />Denne beregning kræver, at fakturerbart salgsbeløb, budget-salgsbeløb og budget-kostbeløb angives korrekt for hele projektet. |
| Salgsomkostning |Realiserede indtægter = Fakturerbar faktureret pris<br /><br /> Realiserede omkostninger = Budget-kostbeløb x faktureringsprocent<br /><br /> Faktureret % = Fakturerbart faktureret salgsbeløb / Fakturerbart salgsbeløb<br /> (Faktureret % findes som en kolonne i projektopgavelinjer)<br /><br /> Igangv. arbejder køb = Forbrug-kostbeløb – realiserede omkostninger |Beregninger af salgsomkostninger starter med beregning af realiserede omkostninger. Omkostninger realiseres proportionalt baseret på budgetteret kostbeløb.<br /><br /> Denne beregning kræver, at det fakturerbare salgsbeløb og det budgetterede kostbeløb angives korrekt for hele projektet. |
| Salgsværdi |Realiserede omkostninger = Forbrug-kostbeløb<br /><br /> Realiseret indtægt = Forbrug-salgsbeløb x Forventet faktureringsforhold<br /><br /> Omkostningsdækningspct. % = Fakturerbart salgsbeløb/Budgetteret salgsbeløb<br /><br /> Igangværende arbejde salg = Realiseret salg - Fakturerbart faktureret salgsbeløb |I beregninger af salgsværdi realiseres indtægter proportionalt baseret på Forbrug-kostbeløb og det forventede omkostningsdækningsforhold.<br /><br /> Denne beregning kræver, at det fakturerbare salgsbeløb og det budgetterede salgsbeløb angives korrekt for hele projektet. |
| Færdiggørelsesgrad |Realiserede omkostninger = Forbrug-kostbeløb<br /><br /> Realiseret indtægt = Fakturerbar salgspris x Færdiggørelsesgrad<br /><br /> Færdiggørelsesgrad = Forbrug-kostbeløb/Budget-kostbeløb<br /> (Hentet i feltet **Fuldførelse af omkostning i %** på projektopgavelinjer)<br /><br /> Igangværende arbejde salg = Realiseret salg - Fakturerbart faktureret salgsbeløb |I beregninger af færdiggørelsesgrad realiseres indtægt proportionalt baseret på færdiggørelsesgraden, dvs. Forbrug-kostbeløb over for Budgetomkostninger.<br /><br /> Denne beregning kræver, at det fakturerbare salgsbeløb og det budgetterede kostbeløb angives korrekt for hele projektet. |
| Afsluttet kontrakt |VIA-beløb = VIA-kostbeløb = Forbrug (kostbeløb)<br /><br /> Igangværende arbejde - salgsbeløb = Fakturerbar (faktureret salg) |Afsluttet kontrakt realiserer ikke indtægter og omkostninger, før projektet er afsluttet. Du kan vælge denne metode, hvis der er stor tvivl omkring de anslåede kostbeløb og projektets omsætning.<br /><br /> Alt forbrug bogføres til kontoen til omkostninger for igangværende arbejde (aktiv), og alt faktureret salg bogføres til kontoen til faktureret salg af igangværende arbejde (kreditorkonto), indtil projektet er afsluttet. |

## Se også

[Projektstyring](projects-manage-projects.md)  
[Finans](finance.md)  
[Køb](purchasing-manage-purchasing.md)  
[Salg](sales-manage-sales.md)  
[Arbejd med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
