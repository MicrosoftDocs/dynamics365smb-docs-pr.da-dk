---
title: Konfigurere rapportering til Finance and Operations, Business edition i Power BI | Microsoft Docs
description: "Du kan gøre dine Financials-data tilgængelige som en datakilde i Power BI og opbygge nyttige rapporter over status for din virksomhed."
author: edupont04
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: business intelligence, KPI, Odata, Power App, SOAP, analysis
ms.date: 12/21/2017
ms.author: edupont
ms.translationtype: HT
ms.sourcegitcommit: b34f276a764f0e828fbc1f015429df9852242a4c
ms.openlocfilehash: 73dc6048f7184054c853f9b9187cbb1a8d5131ff
ms.contentlocale: da-dk
ms.lasthandoff: 03/22/2018

---
# <a name="using-included365finincludesd365finmdmd-as-power-bi-data-source-for-building-reports"></a>Brug af [!INCLUDE[d365fin](includes/d365fin_md.md)] som Power BI-datakilde til oprettelse af rapporter
Du kan gøre dine [!INCLUDE[d365fin](includes/d365fin_md.md)]-data tilgængelige som en datakilde i Power BI og opbygge nyttige rapporter over status for din virksomhed.  

> [!NOTE]  
> Du skal have en gyldig konto til [!INCLUDE[d365fin](includes/d365fin_md.md)] og til Power BI. Desuden skal du hente [Power BI Desktop](https://powerbi.microsoft.com/en-us/desktop/).  

## <a name="to-add-included365finincludesd365finmdmd-as-a-data-source-in-power-bi-desktop"></a>Sådan tilføjes [!INCLUDE[d365fin](includes/d365fin_md.md)] som en datakilde i Power BI Desktop
1. I Power BI Desktop skal du i den venstre navigationsrude vælge **Hent data**.
2. I vinduet **Hent data** skal du vælge **Onlinetjenester**, vælge **Dynamics 365 for Finance and Operations, Business edition** og derefter vælge knappen **Opret forbindelse**.
3. Power BI viser en guide, der hjælper dig gennem [forbindelsesprocessen](across-how-to-connect-powerbi-dynamics-365-content-packs-help.md). Det første trin er at logge på tjenesten. Vælg **Log på**, og vælg den konto, du vil logge på som. Det skal være den samme konto, du bruger til at logge på [!INCLUDE[d365fin](includes/d365fin_md.md)].
4. Vælg knappen **Opret forbindelse** for at forsætte. Guiden Power BI viser en liste over [!INCLUDE[d365fin](includes/d365fin_md.md)]-regnskaber og -datakilder. Disse datakilder repræsenterer all de webtjenester, som du har publiceret fra hvert regnskab [!INCLUDE[d365fin](includes/d365fin_md.md)].
5. Du kan også vælge at oprette en ny URL-adresse for webtjenesten i [!INCLUDE[d365fin](includes/d365fin_md.md)] ved at bruge handlingen **Opret datasæt** på siden **Webtjenester** ved hjælp af guiden Assisteret opsætning for **Konfigurer rapporteringsdata** eller ved at vælge handlingen **Rediger i Excel** på en af listerne.
6. Angiv de data, du vil føje til dine datamodel, og vælg derefter knappen **Indlæsning**.
7. Gentag fremgangsmåden for at føje flere [!INCLUDE[d365fin](includes/d365fin_md.md)]-data til dine Power BI-datamodel.

> [!NOTE]  
> Når du har oprettet forbindelse til [!INCLUDE[d365fin](includes/d365fin_md.md)], bliver du ikke bedt om logge på igen.

Når dataene er indlæst, vises de i den rigtige navigation på siden. Nu har du oprettet forbindelse til dine data i Finance and Operations, Business edition og er klar til at opbygge din Power BI-rapport. Du kan finde flere oplysninger i [Power BI-dokumentationen](https://powerbi.microsoft.com/documentation/powerbi-landing-page/).

## <a name="see-also"></a>Se også
[Business Intelligence](bi.md)  
[Velkommen til [!INCLUDE[d365fin_long](includes/d365fin_long_md.md)]](index.md)  
[Importere virksomhedsdata fra andre økonomisystemer](upload-data.md)  
[Opsætning af [!INCLUDE[d365fin](includes/d365fin_md.md)]](setup.md)   
[Finans](finance.md)  
[Forbinde Power BI til [!INCLUDE[d365fin](includes/d365fin_md.md)]](across-how-to-connect-powerbi-dynamics-365-content-packs-help.md)  

