---
title: Projekt rapporter og analyser
description: Se, hvilke rapporter og analyser der er tilgængelige i standardversionen af Business Central, så du kan holde styr på virksomheden.
author: AndreiPanko
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.search.keywords: reporting
ms.date: 06/01/2021
ms.author: andreipa
ms.openlocfilehash: ff5294df5cdbeaf0054249f017906bfd60ee4bf7
ms.sourcegitcommit: 0953171d39e1232a7c126142d68cac858234a20e
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 06/09/2021
ms.locfileid: "6216337"
---
# <a name="project-reports-and-analytics-in-business-central"></a>Rapporter og analyser i Business Central

Projektrapportering i [!INCLUDE [prod_short](includes/prod_short.md)] gør det muligt for projekt-og erhvervs medarbejdere at få indsigt i og statistikker om aktuelle og tidligere projektaktiviteter.  

## <a name="reports"></a>Rapporter

I følgende tabel beskrives nogle af nøglerapporterne i jobsrapporter.

|Report |Objekt-id|Beskrivelse  |
|---------|---------|---------|
|**Sagsanalyse**|1008|Analyserer dit job ved hjælp af de indstillinger, du angiver. Du kan f.eks. oprette en rapport, der viser de planlagte priser, brugspriser og kontraktpriser, og som sammenligner de tre sæt priser.<br>Brug en kombination af de tilgængelige felter **Beløb** til at oprette din egen analyse. For hvert felt skal du vælge en af følgende værdier for pris, omkostninger eller avance: Planlæg, Brug, Kontrakt og Faktureret. <br>Vælg, om valutaen angives i Lokal valuta eller Udenlandsk valuta. |
|**Sagsplanlægningslinjer**|1006|Denne rapport viser de forskellige Sagsplanlægningslinjer – herunder linjetype, antal, Enhedskode, samlede omkostninger osv.|
|**Sag - realiseret/budget**|1009|Sammenligner planlagt og brugte beløb for valgte sager. Alle linjerne i den valgte sag viser mængde, kostbeløb og linjebeløb. <br>Rapporten er først og fremmest beregnet til afsluttede sager, men du kan bruge den på et hvilket som helst tidspunkt i sagsforløbet.<br>I USA, Canada og Mexico er denne rapport ikke tilgængelig. Brug i stedet felterne **faktisk til budget (kostbeløb) (kostpris)** (10210) eller **faktisk antal job (faktisk) til budget (pris)** (10211).|
|**Sag - faktureringsforslag**|1011|Viser en liste over alle sager pr. debitor. Den viser, hvor meget debitoren allerede er blevet faktureret, og hvor meget der mangler at blive faktureret (faktureringsforslag). <br>I USA, Canada og Mexico er denne rapport ikke tilgængelig. Brug i stedet **rapporten foreslået fakturering af sag** (10219).|
|**Sager pr. debitor**|1012|Viser en oversigt over sager fordelt på debitorer. Du kan bruge rapporten til at sammenligne den planlagte salgspris og færdiggørelsesgraden med den fakturerede salgspris og faktureringsgraden for hver **debitor**.|
|**Varer pr. sag** eller **job pr. vare.**|1013 eller 1014|En oversigt over de anvendte varer i en sag. Afhængigt af den rapport, du vil bruge til at få vist en oversigt over de planlagte varer i et projekt, kan du angive et ekstra filter. Rapporten viser de relevante varer og en akkumulerende værdi om omkostningerne.|
|**Sag - kontokort**|1007|Denne rapport giver dig et overblik over de bogførte sagsopgaver, f. eks. ressourcer og varer. Indeholder detaljerede oplysninger om kostpriser og salgspriser samt oplysninger om linjerabatter osv. Rapporten viser data fra sagsposter.|
|**VIA - finansafstemning**|1010|Viser værdien af igangværende arbejde i de sager, som du vælger, sammenlignet med de beløb, der er bogført i regnskabet.|




## <a name="tasks"></a>Opgaver

I følgende artikler beskrives nogle af de vigtigste opgaver i forbindelse med analyse af virksomhedens tilstand:

* [Overvåge jobstatus og -udførelse](projects-how-monitor-progress-performance.md)  


## <a name="see-also"></a>Se også

[Konfigurere projektstyring](projects-setup-projects.md)  
[Projektstyring](projects-manage-projects.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
