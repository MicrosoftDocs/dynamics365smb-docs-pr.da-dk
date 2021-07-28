---
title: Oversigt over Power BI-integrationskomponent og -arkitektur for Business central| Microsoft Docs
description: Flere oplysninger om forskellige aspekter ved Power BI-integration med Business central.
author: jswymer
ms.service: dynamics365-business-central
ms.topic: get-started-article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: account schedule, analysis, reporting, financial report, business intelligence, KPI
ms.reviewer: edupont
ms.date: 04/01/2021
ms.author: jswymer
ms.openlocfilehash: b1328b618761a33d3dc0856c7623bd986008d283
ms.sourcegitcommit: a7cb0be8eae6ece95f5259d7de7a48b385c9cfeb
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 07/08/2021
ms.locfileid: "6437437"
---
# <a name="power-bi-integration-component-and-architecture-overview-for-prod_short"></a>Oversigt over Power BI-integrationskomponent og -arkitektur for [!INCLUDE[prod_short](includes/prod_short.md)]

I denne artikel kan du læse om de forskellige aspekter ved Power BI-integration med [!INCLUDE[prod_short](includes/prod_short.md)] som hjælp til at forstå implementering og brug.

## <a name="components"></a>Komponenter

I følgende tabel beskrives de vigtigste komponenter, der indgår i Power BI-integrationen.

|Komponent|Beskrivelse|
|---------|-----------|
|Power BI|En skybaseret rapporttjeneste, der er baseret på vært og administration.|
|Power BI Desktop|Et oprettelsesværktøj til opbygning af rapporter og dashboards, og du kan køre rapporter. Den kan hentes gratis på Microsoft Store og installeres lokalt.|
|[!INCLUDE[prod_short](includes/prod_short.md)]|Online eller lokal løsning med connectorer til Power BI og mulighed for at integrere en Power BI-del.|

## <a name="whats-available-from-the-start"></a>Hvad er tilgængeligt fra begyndelsen

Følgende tabel beskriver de tilgængelige funktioner.

|Funktion|[!INCLUDE[prod_short](includes/prod_short.md)] online eller lokal understøttelse|
|-------|---------------------|
|Power BI-connectorer|Begge dele. Forskellige connectorer til online og lokal version. Samme connector, der bruges til Power BI Desktop og Power BI-service |
|Integreret oplevelse ved visning af en bestemt rapport i en faktaboks i [!INCLUDE[prod_short](includes/prod_short.md)]|Begge dele. Kræver konfiguration for at vise rapporter lokalt.|
|Power BI-rapportstyring fra [!INCLUDE[prod_short](includes/prod_short.md)]|Online|
|Standardrapporter fra Power BI i rollecentre, der er udrullet til Power BI|Online|
|Power BI-apps på Microsoft AppSource|Online|

## <a name="architecture"></a>Arkitektur

[!INCLUDE[prod_short](includes/prod_short.md)] integreres med Power BI via en connector, der bruger OData. Datakilden til Power BI-rapporter vises som API-sider og OData-webtjenester.

![Power BI-arkitektur til integration med Business Central.](./media/power-bi-architecture.png)

## <a name="general-flow"></a>Generelt flow

I følgende diagram illustreres den grundlæggende arbejdsgang for brugere, når der oprettes forbindelse mellem [!INCLUDE[prod_short](includes/prod_short.md)] og Power BI.

![Power BI-arbejdsgang til integration med Business Central.](./media/power-bi-flow.png)

1. Bruger tilmelder sig en Power BI-konto.
2. Bruger opretter forbindelse til Power BI fra [!INCLUDE[prod_short](includes/prod_short.md)].
3. [!INCLUDE[prod_short](includes/prod_short.md)] kontrollerer licensen.
4. [!INCLUDE[prod_short](includes/prod_short.md)] installerer standardrapporter til Power BI-tjenesten. Dette trin forekommer kun for [!INCLUDE[prod_short](includes/prod_short.md)] online.
5. [!INCLUDE[prod_short](includes/prod_short.md)] gør rapporter i Power BI tilgængelige for valg i [!INCLUDE[prod_short](includes/prod_short.md)]. Standardrapporter vises automatisk i Power BI-dele.
6. Bruger opretter en rapport i Power BI Desktop.
7. Bruger udgiver rapporten til Power BI-tjenesten. Rapporterne kan derefter vælges i [!INCLUDE[prod_short](includes/prod_short.md)].

## <a name="see-related-training-at-microsoft-learn"></a>Se relateret oplæring på [Microsoft Learn](/learn/modules/configure-powerbi-excel-dynamics-365-business-central/index)

## <a name="see-also"></a>Se også

[Business Central og Power BI](admin-powerbi.md)  
[Power BI for forbrugere](/power-bi/consumer/end-user-consumer)  
[Power BI-tjenestens nye udseende](/power-bi/service-new-look)  
[Hurtig start: Opret forbindelse til data i Power BI Desktop](/power-bi/desktop-quickstart-connect-to-data)  
[Power BI-dokumentation](/power-bi/)  
[Business Intelligence](bi.md)  
[Blive køreklar](ui-get-ready-business.md)  
[Import af virksomhedsdata fra andre økonomisystemer](across-import-data-configuration-packages.md)  
[Opsætning af [!INCLUDE[prod_short](includes/prod_short.md)]](setup.md)  
[Bruge [!INCLUDE[prod_short](includes/prod_short.md)] som Power BI-datakilde](across-how-use-financials-data-source-powerbi.md)  
[Bruge [!INCLUDE[prod_short](includes/prod_short.md)] som Power Apps-datakilde](across-how-use-financials-data-source-powerapps.md)  
[Bruge [!INCLUDE[prod_short](includes/prod_short.md)] i Power Automate](across-how-use-financials-data-source-flow.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]