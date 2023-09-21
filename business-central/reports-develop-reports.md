---
title: Udvikling af rapportlayout og datasæt
description: Indeholder en oversigt over Business Central-data.
author: kennieNP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.reviewer: bholtorf
ms.search.keywords: feature overview
ms.date: 02/03/2022
ms.author: kepontop
---

# Udvikling af Business Central-rapportlayout og datasæt

En rapport i [!INCLUDE[prod_short](includes/prod_short.md)] består af et rapportobjekt, der definerer _rapportens datasæt_ (hvilke data er tilgængelige) og et antal _rapportlayout_ (hvordan data præsenteres).  

## Udvikle rapportlayout

Vil du redigere eksisterende rapportlayout, som findes i [!INCLUDE[prod_short](includes/prod_short.md)]? Afhængigt af den teknologi, der bruges til layoutet, er det noget, du kan gøre, f. eks. Word-layout, eller måske har du brug for en udvikler til at gøre det (pixel-perfekt RDLC layout).

| Hvis du vil | Skal du se |
|--|--|
| Få mere at vide om de forskellige layouttyper (Word, Excel og RDLC) | [Layouttyper (Word, Excel og RDLC)](ui-manage-report-layouts.md) |
| Få mere at vide om, hvordan du kan oprette et nyt rapportlayout. | [Oprette et nyt layout](ui-how-create-custom-report-layout.md) |
| Få mere at vide om, hvilke skrifttyper der installeres i [!INCLUDE[prod_short](includes/prod_short.md)] online, så de kan bruges i rapportlayout. | [Bruge skrifttyper i layout](ui-fonts.md) |
| For at lære, hvordan du arbejder med Word-layout. | [Arbejd med Word-layouts](ui-how-add-fields-word-report-layout.md) |
| For at lære, hvordan du importerer/eksporterer layoutfiler. | [Importér/eksportér et layout](ui-how-import-and-export-report-layout.md) |
| For at lære, hvordan du opdaterer en layoutdefinition i [!INCLUDE[prod_short](includes/prod_short.md)] med en ny layoutfil. | [Importér/eksportér et layout](ui-how-import-and-export-report-layout.md) |
| For at få mere at vide om, hvordan du ændrer standardlayoutet for en rapport. | [Ændre standardlayoutet](ui-how-change-layout-currently-used-report.md) |
<!-- | For at lære, hvordan du arbejder med Excel-layout | [Arbejd med Excel-layouts](ui-how-add-fields-word-report-layout.md) | -->

## Udvikle rapportdatasæt

 Hvis du vil ændre definitionerne for datasættet, der definerer, hvilke data der er tilgængelige i rapporten, skal du have en udvikler, der kender til programmeringssproget AL-programmering og de værktøjer, der skal bruges til at udvikle rapportobjekter og rapportudvidelser.

| Hvis du vil | Skal du se |
|--|--|
| Lære, hvordan du udlæser programmer i AL | [Rapportudviklingsguide](/dynamics365/business-central/dev-itpro/developer/devenv-reports) |
| Lære, hvordan rapporter udføres | [Rapport om justering af ydeevne](/dynamics365/business-central/dev-itpro/performance/performance-developer#writing-efficient-reports) |

## Se også

[Oversigt over Business Intelligence og rapportering](reports-use-reports.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]