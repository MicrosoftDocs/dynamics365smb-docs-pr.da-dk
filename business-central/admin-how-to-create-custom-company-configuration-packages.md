---
title: Sådan oprettes brugerdefinerede virksomhedsskabeloner | Microsoft Docs
description: Efterhånden som din virksomhed vokser, vil du sandsynligvis have oprettet et sæt virksomhedstyper, som du kan bruge til de fleste af dine kunder. Du kan strømline implementeringsprocessen ved at gøre disse typiske typer til virksomhedskonfigurationsskabeloner, der kan genbruges.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/01/2020
ms.author: sgroespe
ms.openlocfilehash: 8bbd9b07976dc4d54f8bee9f5eb8c23270c5a10c
ms.sourcegitcommit: 88e4b30eaf6fa32af0c1452ce2f85ff1111c75e2
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 04/01/2020
ms.locfileid: "3187168"
---
# <a name="create-custom-company-configuration-packages"></a>Oprette brugerdefinerede virksomhedsskabeloner
Efterhånden som din virksomhed vokser, vil du sandsynligvis have oprettet et sæt virksomhedstyper, som du kan bruge til de fleste af dine kunder. Du kan strømline implementeringsprocessen ved at gøre disse typiske typer til virksomhedskonfigurationsskabeloner, der kan genbruges.  

Generelt skal du oprette en konfigurationspakke pr. funktionsområde. Du skal f.eks. oprette en pakke til produktionsfunktionerne. På den måde kan du anvende og konfigurere nye områder i en virksomhed, efterhånden som du har brug for dem.  

En anden fremgangsmåde er at oprette en pakke, der indeholder de tabeller, der definerer konfigurationen, som følgende:  

-   Anlægsopsætning  
-   Opsætning af Finans  
-   Opsætning af Lager  
-   Produktionsopsætning  
-   Købsopsætning  
-   Marketingopsætning  
-   Serviceopsætning  
-   Salgsopsætning  
-   Logistikopsætning  
-   Bogføringsopsætning  
-   Momsbogf.opsætning  
-   Opsætning af varebogføring  

For at få vist en komplet liste over opsætningstabeller skal du vælge ikonet ![Elpære, der åbner funktionen Fortæl mig](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig"), angive **Manuel opsætning**, og vælg derefter det relaterede link.  

## <a name="to-create-a-custom-company-configuration-package"></a>Sådan oprettes en brugerdefineret virksomhedskonfigurationspakke  
1.  Oprette en ny virksomhed. Du kan finde flere oplysninger i [Oprettelse af ny virksomheder i Business Central](about-new-company.md).  
3.  Konfigurer den nye virksomhed på den måde, som du har brug for. Udfyld alle nødvendige konfigurationstabeller.  
4.  Åbn det nye regnskab.
5. Åbn siden **Konfigurationskladde**.  
6.  Tilføj de tabeller, du vil overføre til en anden virksomhed, til regnearket. Tildel kladdelinjerne til pakken.  
7.  Opret et spørgeskema til de hyppigst anvendte konfigurationstabeller.  
8.  Opret konfigurationsskabeloner til at gøre det lettere at oprette masterdata, f.eks. kunder eller varer.  
9.  Udlæs pakken som en .rapidstart-fil.  

## <a name="see-also"></a>Se også  
[Oprette en virksomhed med RapidStart Services](admin-set-up-a-company-with-rapidstart.md)  
[Opsætning](admin-setup-and-administration.md)
