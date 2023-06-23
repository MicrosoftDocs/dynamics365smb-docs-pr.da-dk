---
title: Oversigt over Power BI-integrationskomponent og -arkitektur for Business central| Microsoft Docs
description: Flere oplysninger om forskellige aspekter ved Power BI-integration med Business central.
author: jswymer
ms.topic: overview
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 'account schedule, analysis, reporting, financial report, business intelligence, KPI'
ms.reviewer: edupont
ms.date: 04/01/2021
ms.author: jswymer
---
# <a name="power-bi-integration-component-and-architecture-overview-for-includeprodshortincludesprodshortmd" />Oversigt over Power BI-integrationskomponent og -arkitektur for [!INCLUDE[prod_short](includes/prod_short.md)]

I denne artikel kan du læse om de forskellige aspekter ved Power BI-integration med [!INCLUDE[prod_short](includes/prod_short.md)] som hjælp til at forstå implementering og brug.

## <a name="components" />Komponenter

I følgende tabel beskrives de vigtigste komponenter, der indgår i Power BI-integrationen.

|Komponent|Beskrivelse|
|---------|-----------|
|Power BI|En skybaseret rapporttjeneste, der er baseret på vært og administration.|
|Power BI Desktop|Et oprettelsesværktøj til opbygning af rapporter og dashboards, og du kan køre rapporter. Den kan hentes gratis på Microsoft Store og installeres lokalt.|
|[!INCLUDE[prod_short](includes/prod_short.md)]|Online eller lokal løsning med connectorer til Power BI og mulighed for at integrere en Power BI-del.|

## <a name="whats-available-from-the-start" />Hvad er tilgængeligt fra begyndelsen

Følgende tabel beskriver de tilgængelige funktioner.

|Funktion|[!INCLUDE[prod_short](includes/prod_short.md)] online eller lokal understøttelse|
|-------|---------------------|
|Power BI-connectorer|Begge dele. Forskellige connectorer til online og lokal version. Samme connector, der bruges til Power BI Desktop og Power BI-service |
|Integreret oplevelse ved visning af en bestemt rapport i en faktaboks i [!INCLUDE[prod_short](includes/prod_short.md)]|Begge dele. Kræver konfiguration for at vise rapporter lokalt.|
|Power BI-rapportstyring fra [!INCLUDE[prod_short](includes/prod_short.md)]|Online|
|Standardrapporter fra Power BI i rollecentre, der er udrullet til Power BI|Online|
|Power BI-apps på Microsoft AppSource|Online|

## <a name="architecture" />Arkitektur

[!INCLUDE[prod_short](includes/prod_short.md)] integreres med Power BI via en connector, der bruger OData. Datakilden til Power BI-rapporter vises som API-sider og OData-webtjenester.

:::image type="content" source="./media/power-bi-architecture.png" alt-text="Alternativ billedtekst." lightbox="./media/power-bi-architecture.png":::

Fra og med februar 2022 er Power BI-rapporter om [!INCLUDE[prod_short](includes/prod_short.md)] Online baseret på en sekundær, skrivebeskyttet databasereplika. Database-replika er en del af [read scale-out](/dynamics365/business-central/dev-itpro/administration/database-read-scale-out-overview)-funktionen i [!INCLUDE[prod_short](includes/prod_short.md)] online. Denne konfiguration frigør hoveddatabasen til transaktioner, hvilket forbedrer systemets ydeevne. Når du opretter forbindelse til den skrivebeskyttede databasereplika, er det en integreret del af Business Central online-connector og kræver ingen ekstra opsætning. Alle nye rapporter opretter som standardforbindelse til den skrivebeskyttede databasereplika. Gamle rapporter bruger stadig hoveddatabasen. Du kan finde flere oplysninger i [Business Central 2021 Release Wave 2-plan ](/dynamics365-release-plan/2021wave2/smb/dynamics365-business-central/use-secondary-read-only-database-power-bi-reporting).

## <a name="general-flow" />Generelt flow

I følgende diagram illustreres den grundlæggende arbejdsgang for brugere, når der oprettes forbindelse mellem [!INCLUDE[prod_short](includes/prod_short.md)] og Power BI.

![Power BI-arbejdsgang til integration med Business Central.](./media/power-bi-flow.png)

1. Bruger tilmelder sig en Power BI-konto.
2. Bruger opretter forbindelse til Power BI fra [!INCLUDE[prod_short](includes/prod_short.md)].
3. [!INCLUDE[prod_short](includes/prod_short.md)] kontrollerer licensen.
4. [!INCLUDE[prod_short](includes/prod_short.md)] installerer standardrapporter til Power BI-tjenesten. Dette trin forekommer kun for [!INCLUDE[prod_short](includes/prod_short.md)] online.
5. [!INCLUDE[prod_short](includes/prod_short.md)] gør rapporter i Power BI tilgængelige for valg i [!INCLUDE[prod_short](includes/prod_short.md)]. Standardrapporter vises automatisk i Power BI-dele.
6. Bruger opretter en rapport i Power BI Desktop.
7. Bruger udgiver rapporten til Power BI-tjenesten. Rapporterne kan derefter vælges i [!INCLUDE[prod_short](includes/prod_short.md)].

## <a name="see-related-microsoft-trainingtrainingmodulesconfigure-powerbi-excel-dynamics-365-business-centralindex" />Se relateret [Microsoft-træning](/training/modules/configure-powerbi-excel-dynamics-365-business-central/index)

## <a name="see-also" />Se også

[Business Central og Power BI](admin-powerbi.md)  
[Power BI for forbrugere](/power-bi/consumer/end-user-consumer)  
[Power BI-tjenestens nye udseende](/power-bi/service-new-look)  
[Hurtig start: Opret forbindelse til data i Power BI Desktop](/power-bi/desktop-quickstart-connect-to-data)  
[Power BI-dokumentation](/power-bi/)  
[Business Intelligence](bi.md)  
[Blive køreklar](ui-get-ready-business.md)  
[Import af virksomhedsdata fra andre økonomisystemer](across-import-data-configuration-packages.md)  
[Opsætning af [!INCLUDE[prod_short](includes/prod_short.md)]](setup.md)  
[Brug af [!INCLUDE[prod_short](includes/prod_short.md)] som Power BI-datakilde](across-how-use-financials-data-source-powerbi.md)  
[Brug af [!INCLUDE[prod_short](includes/prod_short.md)] som Power Apps-datakilde](across-how-use-financials-data-source-powerapps.md)  
[Brug [!INCLUDE[prod_short](includes/prod_short.md)] i Power Automate](across-how-use-financials-data-source-flow.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
