---
title: Sådan oprettes en nyt virksomhed | Microsoft Docs
description: For at du kan bruge RapidStart Services, er tabeller og sider oprettet, men der er ingen data i dem.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/01/2019
ms.author: sgroespe
ms.openlocfilehash: 8b534af530a7ce6d91a71ca7802938fe3573c2c2
ms.sourcegitcommit: bd78a5d990c9e83174da1409076c22df8b35eafd
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 03/31/2019
ms.locfileid: "932076"
---
# <a name="create-a-new-company"></a>Oprette en ny virksomhed
Hvis du vil bruge RapidStart Services til [!INCLUDE[d365fin](includes/d365fin_md.md)], skal du først oprette en ny virksomhed, som du ønsker at udføre en kundeimplementering for. Når du opretter en ny virksomhed, oprettes standardtabellerne og -siderne i [!INCLUDE[d365fin](includes/d365fin_md.md)], men der er ingen data i dem.

Du kan også anvende specifikke konfigurationsdata til din virksomhed, når du har initialiseret den. Oplysningerne leveres i en konfigurationspakke, en .rapidstart-fil., som leverer indhold i et komprimeret format.  

Eksempelkonfigurationspakker, herunder lande-/områdespecifikke filer, følger med CRONUS-demoregnskabet. Brug følgende fremgangsmåder for at bruge pakken med eksempelkonfiguration af et nyt firma.  

## <a name="to-use-the-sample-basicconfig-configuration-package"></a>Sådan bruger du eksempelkonfigurationspakken BASICCONFIG  
1. Åbn regnskabet CRONUS Danmark A/S. Du kan finde flere oplysninger under [Ændring af grundlæggende indstillinger](ui-change-basic-settings.md).
2. Vælg ikonet ![Elpære, der åbner funktionen Fortæl mig](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig"), angiv **Konfigurationspakker**, og vælg derefter det relaterede link.  
3. Vælg pakken BASICCONFIG på listen, og vælg derefter handlingen **Udlæs pakke**.  

Brug følgende fremgangsmåde for at oprette en ny virksomhed, og brug pakken BASICCONFIG som en del af proceduren.  

## <a name="to-create-a-new-company"></a>Sådan oprettes en ny virksomhed  
1. Oprette en ny virksomhed. Du kan finde flere oplysninger om oprettelse af pluk under [Oprettelse af nye virksomheder i [!INCLUDE[d365fin](includes/d365fin_md.md)]](about-new-company.md).
2. Du kan nu importere konfigurationspakken, du har eksporteret fra demonstrationsvirksomheden CRONUS Danmark A/S fra rollecentret RapidStart Services-implementering.

Når du opretter en ny virksomhed, udfyldes nogle tabeller automatisk, selvom der ikke anvendes nogen virksomhedsskabelon. Du kan f.eks. gennemse standardkoderne for bogføring og batchposteringer på siden **Kildekode**. Hvis du angiver en lokal version af [!INCLUDE[d365fin](includes/d365fin_md.md)], bør du gennemgå denne tabel og overveje eventuelle problemer med lokalt sprog.

## <a name="about-data-tables"></a>Om datatabeller
[!INCLUDE[d365fin](includes/d365fin_md.md)]-datatabeller leveres i to grundlæggende typer: Master og Konfiguration. Når du konfigurerer en virksomhedskonfiguration, kan du bruge disse typer for at fokusere din konfigurationsstrategi.  

### <a name="master-data-tables"></a>Masterdatatabeller  
I følgende tabel vises nogle eksempler på masterdatatabellerne. Når du starter en ny virksomhed, vil disse tabeller være tomme.  

|Tabel-id|Tabelnavn|  
|-------------------|--------------------|  
|15|Finanskonto|  
|18|Kunde|  
|23|Kreditor|  
|27|Vare|  
|5050|Kontakt|  

### <a name="setup-data-tables"></a>Konfigurationsdatatabeller  
Følgende tabel viser nogle af konfigurationsdatatabeller, hvor du henter konfigurationsoplysninger i konfigurationsspørgeskemaet. Disse tabeller indeholder basisoplysninger, når virksomheden oprettes.  

|Tabel-id|Tabelnavn|  
|-------------------|--------------------|  
|98|Opsætning af Finans|  
|311|Salgsopsætning|  
|312|Købsopsætning|  
|313|Opsætning af Lager|  

Ud over konfigurationsdatatabeller har [!INCLUDE[d365fin](includes/d365fin_md.md)] også datatabeller med opsætningstype, der angiver centrale oplysninger om virksomheden og dens forretningsprocesser. Følgende tabel indeholder nogle af dem.  

|Tabel-id|Tabelnavn|  
|-------------------|--------------------|  
|3|Betalingsbetingelser|  
|4|Valuta|  
|6|Debitorprisgrupper|  
|5700|Lagervare (pr. lok.)|

  

## <a name="see-also"></a>Se også  
[Anvende konfigurationer på nye virksomheder](admin-apply-configuration-to-new-companies.md)  
[Oprette en virksomhed med RapidStart Services](admin-set-up-a-company-with-rapidstart.md)  
[Opsætning](admin-setup-and-administration.md)
