---
title: "Sådan oprettes brugerdefinerede virksomhedsskabeloner | Microsoft Docs"
description: "Efterhånden som din virksomhed vokser, vil du sandsynligvis have oprettet et sæt virksomhedstyper, som du kan bruge til de fleste af dine kunder. Du kan strømline implementeringsprocessen ved at gøre disse typiske typer til virksomhedskonfigurationsskabeloner, der kan genbruges."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 10/01/2018
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 9dbd92409ba02281f008246194f3ce0c53e4e001
ms.openlocfilehash: e26174fcf723e13ef5a9ed0b386006c0439e1c7a
ms.contentlocale: da-dk
ms.lasthandoff: 09/28/2018

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

For at få vist en komplet liste over opsætningstabeller skal du vælge ikonet ![Elpære, der åbner funktionen Fortæl mig](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig"), angiv **Opsætning**, og vælg derefter det relaterede link.  

## <a name="to-create-a-custom-company-configuration-package"></a>Sådan oprettes en brugerdefineret virksomhedskonfigurationspakke  
1.  Oprette et ny [!INCLUDE[d365fin](includes/d365fin_md.md)]. ***IKKE muligt Link til hjælp til "Oprette en ny lejer"***.   
2.  Oprette en ny virksomhed for skabelonen industri eller løsning. Du kan finde flere oplysninger i [Oprette en ny virksomhed](admin-how-to-create-a-new-company.md).  
3.  Konfigurer den nye virksomhed på den måde, som du har brug for. Udfyld alle nødvendige konfigurationstabeller.  
4.  Åbn det nye regnskab.
5. Åbn vinduet **Konfigurationsregneark**.  
6.  Tilføj de tabeller, du vil overføre til en anden virksomhed, til regnearket. Tildel kladdelinjerne til pakken.  
7.  Opret et spørgeskema til de hyppigst anvendte konfigurationstabeller.  
8.  Opret konfigurationsskabeloner til at gøre det lettere at oprette masterdata, f.eks. kunder eller varer.  
9.  Udlæs pakken som en .rapidstart-fil.  

## <a name="see-also"></a>Se også  
[Oprette en virksomhed med RapidStart Services](admin-set-up-a-company-with-rapidstart.md)  
[Opsætning](admin-setup-and-administration.md)

