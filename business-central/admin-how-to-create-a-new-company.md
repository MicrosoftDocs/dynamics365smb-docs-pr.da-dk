---
title: Sådan oprettes en nyt virksomhed | Microsoft Docs
description: Brug RapidStart Services-tabeller og sider til at oprette en ny virksomhed, som du ønsker at udføre en kundeimplementering for.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 06/14/2021
ms.author: edupont
ms.openlocfilehash: bb2e3e8d431160c94f7944fe8986ea9cc115ffe7
ms.sourcegitcommit: a7cb0be8eae6ece95f5259d7de7a48b385c9cfeb
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 07/08/2021
ms.locfileid: "6439631"
---
# <a name="create-a-new-company"></a>Oprette en ny virksomhed
Hvis du vil bruge RapidStart Services til [!INCLUDE[prod_short](includes/prod_short.md)], skal du først oprette en ny virksomhed, som du ønsker at udføre en kundeimplementering for. Når du opretter en ny virksomhed, oprettes standardtabellerne og -siderne i [!INCLUDE[prod_short](includes/prod_short.md)], men der er ingen data i dem.

Du kan også anvende specifikke konfigurationsdata til din virksomhed, når du har initialiseret den. Oplysningerne leveres i en konfigurationspakke, en .rapidstart-fil., som leverer indhold i et komprimeret format.  

Eksempelkonfigurationspakker, herunder lande-/områdespecifikke filer, følger med CRONUS-demoregnskabet. Brug følgende fremgangsmåder for at bruge pakken med eksempelkonfiguration af et nyt firma.  

## <a name="to-use-the-sample-basicconfig-configuration-package"></a>Sådan bruger du eksempelkonfigurationspakken BASICCONFIG  
1. Åbn regnskabet CRONUS Danmark A/S. Du kan finde flere oplysninger i [Ændre grundlæggende indstillinger](ui-change-basic-settings.md).
2. Vælg ![Lightbulb, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **Pakker til konfiguration**, og vælg derefter det relaterede link.  
3. Vælg pakken BASICCONFIG på listen, og vælg derefter handlingen **Udlæs pakke**.  

Brug følgende fremgangsmåde for at oprette en ny virksomhed, og brug pakken BASICCONFIG som en del af proceduren.  

## <a name="to-create-a-new-company"></a>Sådan oprettes en ny virksomhed  
1. Oprette en ny virksomhed. Du kan finde flere oplysninger om oprettelse af pluk under [Oprettelse af nye virksomheder i [!INCLUDE[prod_short](includes/prod_short.md)]](about-new-company.md).
2. Du kan nu importere konfigurationspakken, du har eksporteret fra demonstrationsvirksomheden CRONUS Danmark A/S, fra rollecentret RapidStart Services-implementering.

Når du opretter en ny virksomhed, udfyldes nogle tabeller automatisk, selvom der ikke anvendes nogen virksomhedsskabelon. Du kan f.eks. gennemse standardkoderne for bogføring og batchposteringer på siden **Kildekode**. Hvis du angiver en lokal version af [!INCLUDE[prod_short](includes/prod_short.md)], bør du gennemgå denne tabel og overveje eventuelle problemer med lokalt sprog.

## <a name="about-data-tables"></a>Om datatabeller
[!INCLUDE[prod_short](includes/prod_short.md)]-datatabeller leveres i to grundlæggende typer: Master og Konfiguration. Når du konfigurerer en virksomhedskonfiguration, kan du bruge disse typer for at fokusere din konfigurationsstrategi.  

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

Ud over konfigurationsdatatabeller har [!INCLUDE[prod_short](includes/prod_short.md)] også datatabeller med opsætningstype, der angiver centrale oplysninger om virksomheden og dens forretningsprocesser. Følgende tabel indeholder nogle af dem.  

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


[!INCLUDE[footer-include](includes/footer-banner.md)]