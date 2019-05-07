---
title: Konfigurere rapportering til Business Central i Power BI | Microsoft Docs
description: Gøre dine data tilgængelige som en datakilde i Power BI og opbygge nyttige rapporter over status for din virksomhed.
author: edupont04
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: business intelligence, KPI, Odata, Power App, SOAP, analysis
ms.date: 04/01/2019
ms.author: edupont
ms.openlocfilehash: 8dfedbc2685e086f9bdc63706d70327ebb95c2b5
ms.sourcegitcommit: bd78a5d990c9e83174da1409076c22df8b35eafd
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 03/31/2019
ms.locfileid: "919887"
---
# <a name="using-included365finlongmdincludesd365finlongmdmd-as-power-bi-data-source-for-building-reports"></a>Brug af [!INCLUDE[d365fin_long_md](includes/d365fin_long_md.md)] som Power BI-datakilde til oprettelse af rapporter
Du kan gøre dine [!INCLUDE[d365fin_long_md](includes/d365fin_long_md.md)]-data tilgængelige som datakilde i Power BI og opbygge nyttige rapporter over status for din virksomhed.  

Du skal have en gyldig konto til [!INCLUDE[d365fin_long_md](includes/d365fin_long_md.md)] og til Power BI. Desuden skal du hente [Power BI Desktop](https://powerbi.microsoft.com/en-us/desktop/).  

## <a name="to-add-included365finlongmdincludesd365finlongmdmd-as-a-data-source-in-power-bi-desktop"></a>Sådan tilføjes [!INCLUDE[d365fin_long_md](includes/d365fin_long_md.md)] som en datakilde i Power BI Desktop
1. I Power BI Desktop skal du i den venstre navigationsrude vælge **Hent data**.
2. På siden **Hent data** skal du vælge **Onlinetjenester**, vælge **Microsoft Dynamics 365 Business Central** og derefter vælge knappen **Opret forbindelse**.
3. Power BI viser en guide, der hjælper dig gennem [forbindelsesprocessen](across-how-to-connect-powerbi-dynamics-365-content-packs-help.md). Du bliver bedt om at logge på tjenesten. Vælg **Log på**, og vælg den konto, du vil logge på som. Det skal være den samme konto, du bruger til at logge på [!INCLUDE[d365fin_long_md](includes/d365fin_long_md.md)].
4. Vælg knappen **Opret forbindelse** for at forsætte. Guiden Power BI viser en liste over Microsoft [!INCLUDE[d365fin](includes/d365fin_md.md)]-regnskaber og -datakilder. Disse datakilder repræsenterer all de webtjenester, som du har publiceret fra hvert regnskab i Microsoft [!INCLUDE[d365fin_long_md](includes/d365fin_long_md.md)].
5. Du kan også vælge at oprette en ny URL-adresse for webtjenesten i [!INCLUDE[d365fin_long_md](includes/d365fin_long_md.md)] ved at bruge handlingen **Opret datasæt** på siden **Webtjenester** ved hjælp af guiden Assisteret opsætning for **Konfigurer rapporteringsdata** eller ved at vælge handlingen **Rediger i Excel** på en af listerne.
6. Angiv de data, du vil føje til dine datamodel, og vælg derefter knappen **Indlæsning**.
7. Gentag fremgangsmåden for at føje flere Microsoft [!INCLUDE[d365fin_long_md](includes/d365fin_long_md.md)]-data eller andre data til dine Power BI-datamodel.

> [!NOTE]  
> Når du har oprettet forbindelse til Microsoft [!INCLUDE[d365fin_long_md](includes/d365fin_long_md.md)], bliver du ikke bedt om logge på igen.

Når dataene er indlæst, vises de i den rigtige navigation på siden. Nu har du oprettet forbindelse til dine Microsoft [!INCLUDE[d365fin_long_md](includes/d365fin_long_md.md)]-data og er klar til at opbygge din Power BI-rapport. 

Før du opretter rapporten, anbefales det, at du importerer Microsoft [!INCLUDE[d365fin_long_md](includes/d365fin_long_md.md)]-temafilen.  Temafilen opretter en farvepalet, så du kan oprette rapporter med de samme farvenuancer som Microsoft [!INCLUDE[d365fin_long_md](includes/d365fin_long_md.md)]-indholdspakker, uden at du skal definere brugerdefinerede farver til hvert visuelle element.

Der er flere oplysninger i [Power BI-dokumentationen](https://powerbi.microsoft.com/documentation/powerbi-landing-page/).

## <a name="see-also"></a>Se også
[Business Intelligence](bi.md)  
[Introduktion](product-get-started.md)  
[Importere virksomhedsdata fra andre økonomisystemer](across-import-data-configuration-packages.md)  
[Opsætning af [!INCLUDE[d365fin](includes/d365fin_md.md)]](setup.md)   
[Finans](finance.md)  
[Forbinde Power BI med [!INCLUDE[d365fin](includes/d365fin_md.md)]](across-how-to-connect-powerbi-dynamics-365-content-packs-help.md)  
