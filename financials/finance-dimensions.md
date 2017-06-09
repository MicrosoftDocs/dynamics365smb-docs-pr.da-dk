---
title: Dimensioner | Microsoft Docs
description: Du kan bruge dimensioner til at analysere data.
services: project-madeira
documentationcenter: 
author: bholtorf
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: analysis, history, track
ms.date: 03/24/2017
ms.author: bholtorf
ms.translationtype: Human Translation
ms.sourcegitcommit: a31be0f9d07e2abb591e26f6bae34c6f6e4dcda6
ms.openlocfilehash: 7552ee2b3398c203a7f3295f3203c83914fbb15f
ms.contentlocale: da-dk
ms.lasthandoff: 05/04/2017


---
# <a name="dimensions"></a>Dimensioner
For at gøre det lettere at analysere dokumenter som f.eks. salgsordrer kan du bruge dimensioner. Dimensioner er attributter og værdier, der kategoriserer poster, så du kan spore og analysere dem. Dimensioner kan f.eks. angive det projekt eller den afdeling, en post kommer fra.  

I stedet for f.eks. at oprette en særskilt finanskonto til hver afdeling og hvert projekt kan du bruge dimensioner. Det giver en god analysemulighed uden at skulle oprette en kompliceret kontoplan.  

Som et andet eksempel kan du oprette en dimension med navnet *Afdeling* og bruge den, når du bogfører salgsdokumenter. Derved kan du bruge business intelligence-værktøjer til at se, hvilke afdelinger der har solgt hvilke varer.
Jo flere dimensioner, du bruger, jo mere detaljerede rapporter kan du basere forretningsmæssige beslutninger på. F.eks. kan en enkelt salgspost indeholde flere dimensionsoplysninger, f.eks.:  

* Den konto, som varesalget blev bogført på  
* Hvor varen blev solgt
* Hvem, der solgte den
* Hvilken type kunde der købte den  

Du kan oprette lige så mange dimensioner med så mange værdier, du vil.  

**Bemærk**: Denne funktion kræver, at oplevelsen er indstillet til **Pakke**. Du kan finde flere oplysninger i [Tilpasse din [!INCLUDE[d365fin](includes/d365fin_md.md)]-oplevelse](ui-experiences.md).

## <a name="using-dimensions"></a>Bruge dimensioner
I et dokument, f.eks en salgsordre, kan du tilføje dimensionsoplysninger for en individuel dokumentlinje og for selve dokumentet. I vinduet **Salgsordre** kan du f.eks. angive dimensionsværdier for de første to genvejsdimensioner på de enkelte salgslinjer, og du kan tilføje flere dimensionsoplysninger, hvis du vælger knappen **Dimensioner**.  

Hvis du i stedet arbejder i en kladde, kan du tilføje dimensionsoplysninger til en post på samme måde, hvis du har oprettet genvejsdimensioner som felter direkte på kladdelinjer.  

Du kan angive standarddimensioner for konti eller kontotyper, så dimensioner og dimensionsværdier udfyldes automatisk.  

## <a name="dimension-sets"></a>Dimensionsgrupper
En dimensionsgruppe er en entydig kombination af dimensionsværdier. Det er gemt som dimensionsgruppeposter i databasen. Hver dimensionsgruppepost repræsenterer en enkelt dimensionsværdi. Dimensionsgruppen er identificeret med en fælles dimensionsgruppe-id, der tildeles til hver dimensionsgruppepost, der hører til dimensionsgruppen.  

Når du opretter en kladdelinje, et nyt bilagshoved eller en ny bilagslinje, kan du angive en kombination af dimensionsværdier. I stedet for at eksplicit at gemme hver dimensionsværdi i databasen, tildeles kladdelinjen, bilagshovedet eller bilagslinjen en dimensionsgruppe-id, der angiver dimensionsgruppen.  

## <a name="see-also"></a>Se også
[Finans](finance.md)  
[Oprette dimensioner](finance-setup-dimensions.md)  
[Arbejde med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)  

