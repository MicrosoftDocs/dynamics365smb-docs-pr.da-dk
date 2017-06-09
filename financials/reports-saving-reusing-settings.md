---
title: Gemte indstillinger i rapporter
description: Beskriver, hvordan du bruger gemte indstillinger i rapporter.
services: project-madeira
documentationcenter: 
author: jswymer
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: customization, personalization
ms.date: 12/12/2016
ms.author: jswymer
ms.translationtype: Human Translation
ms.sourcegitcommit: a31be0f9d07e2abb591e26f6bae34c6f6e4dcda6
ms.openlocfilehash: 7afbd31e77a4f53ee99fbb192dd8a32a660f87eb
ms.contentlocale: da-dk
ms.lasthandoff: 05/04/2017


---
# <a name="saved-settings-on-reports"></a>Gemte indstillinger i rapporter
Afhængigt af den rapport, der køres, kan du få vist en side, hvor du kan angive bestemte indstillinger og filtre for at ændre, hvilke data der medtages i den genererede rapport. Denne side kaldes rapportanmodningssiden. En rapport kan medtage én eller flere *gemte indstillinger*, som du kan anvende til rapporten fra anmodningssiden. *Gemte indstillinger* er grundlæggende foruddefinerede indstillinger og filtre. Med gemte indstillinger kan du hurtigt og pålideligt generere ensartede rapporter, der indeholder de korrekte data.

Du kan se de gemte indstillinger, der er tilgængelige for en rapport, i afsnittet **Gemte indstillinger** på rapportanmodningssiden.  

## <a name="to-apply-saved-settings-to-a-report"></a>Sådan anvendes gemte indstillinger til en rapport
1. Åbn rapporten.

   Rapportanmodningssiden vises.    
2. I sektionen **Gemte indstillinger** på siden skal du angive feltet **Navn** til de gemte indstillinger, du vil bruge.

   Afsnittet **Gemte indstillinger** vises kun, hvis rapporten er blevet kørt før, eller hvis der findes poster for gemte indstillinger. Posten for gemte indstillinger, som kaldes **Sidst anvendte indstillinger og filtre**, er altid tilgængelig. Disse indstillinger er de værdier for indstillinger og filtre, som blev brugt, sidste gang du kørte rapporten.

## <a name="administer-saved-report-settings-for-users"></a>Administrere gemte rapportindstillinger for brugere
Hvis du har de nødvendige tilladelser, kan du få vist, oprette og redigere de gemte indstillinger for alle rapporter for alle brugere i virksomheden. Du kan tildele gemte indstillinger for en rapport til enkelte brugere eller alle brugere i virksomheden.

Du administrerer gemte indstillinger fra side 1506 **Rapportindstillinger**. For at åbne denne side skal du i øverste højre hjørne vælge ikonet **Søg efter side eller rapport** ![Søg efter side eller rapport](media/ui-search/search_small.png "Ikonet Søg efter side eller rapport"), angive **Rapportindstillinger** og derefter vælge det relaterede link.

Fra siden **Rapportindstillinger** kan du oprette nye indstillinger fra bunden, eller du kan kopiere og redigere eksisterende indstillinger. Hvis du vil ændre indstillinger og filtre for en indstilling, skal du vælge handlingen **Rediger**.

**Bemærk!**

* Funktionen for gemte indstillinger for rapporter er kun relevant, hvis egenskaben SaveValues for anmodningssiden er angivet til Ja. Egenskaben SaveValues angives i udviklingsmiljøet.
* Hvis du opretter et element for gemte indstillinger for alle brugere, og det hedder det samme som en eksisterende gemt indstilling for en bestemt bruger, kan den pågældende bruger ikke anvende de gemte indstillinger, der er tildelt til alle.  I feltet Gemte indstillinger på rapportanmodningssiden får brugeren vist to valgmuligheder for gemte indstillinger med det samme navn. Men uanset hvilken indstilling brugeren vælger, anvendes de brugerspecifikke gemte indstillinger.

## <a name="see-also"></a>Se også
[Planlægge kørsel af en rapport](ui-schedule-report.md)  

