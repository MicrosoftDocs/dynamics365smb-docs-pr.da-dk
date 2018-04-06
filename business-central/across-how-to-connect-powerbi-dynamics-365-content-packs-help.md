---
title: "Sådan forbindes Power BI med Business Central | Microsoft Docs"
description: "Du kan nemt få indsigt, business intelligence og nøgletal i dine Business Central-data med Power BI og Business Central-indholdspakker."
author: SusanneWindfeldPedersen
ms.service: dynamics365-business-central
ms.topic: get-started-article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: account schedule, analysis, reporting, financial report, business intelligence, KPI
ms.date: 03/16/2018
ms.author: solsen
ms.translationtype: HT
ms.sourcegitcommit: d7fb34e1c9428a64c71ff47be8bcff174649c00d
ms.openlocfilehash: 315d4b188cdd834e82676a0c5ef77272ad873eb7
ms.contentlocale: da-dk
ms.lasthandoff: 03/22/2018

---
# <a name="connecting-power-bi-to-business-central-content-packs"></a>Forbinde Power BI med Business Central-indholdspakker
Du kan nemt få indsigt i dine Microsoft [!INCLUDE[d365fin_long_md](includes/d365fin_long_md.md)]-data med Power BI og Microsoft [!INCLUDE[d365fin_long_md](includes/d365fin_long_md.md)]-indholdspakker. Power BI henter dine data og opretter derefter et out-of-the-box dashboard og rapporter baseret på dataene.

> [!NOTE]  
>  Du skal have en gyldig konto til [!INCLUDE[d365fin](includes/d365fin_md.md)] og til Power BI. Desuden skal du hente [Power BI Desktop](https://powerbi.microsoft.com/en-us/desktop/).  
>  Power BI-indholdspakker kræver tilladelser til de tabeller, hvor data hentes fra. Yderligere oplysninger om kravene beskrives nedenfor.  

## <a name="how-to-connect"></a>Sådan oprettes forbindelse
1. Vælg **Hent data** nederst i venstre navigationsrude.  
![Navigere til Hent data](./media/across-how-to-connect-powerbi-d365-content-packs/powerbi-get-data.png)
2. I feltet **Tjenester** skal du vælge **Hent**. Dermed åbnes et vindue med **AppSource** og **Apps til Power BI-apps**.  
![Vælg indholdspakker fra onlinetjenester](./media/across-how-to-connect-powerbi-d365-content-packs/powerbi-online-services-get.png)
3. Vælg **Apps** under fanen **Apps til Power BI-apps**, og vælg den **Microsoft Dynamics 365 Business Central**-indholdspakke, du vil bruge, og vælg derefter **Hent nu**.  
![Vælg Dynamics 365 Business Central, og vælg Hent det nu](./media/across-how-to-connect-powerbi-d365-content-packs/powerbi-dynamics365-for-financials-get-it-now.png)
4. Når du bliver bedt om det, skal du angive navnet på *virksomheden* i [!INCLUDE[d365fin_md](includes/d365fin_long_md.md)]. Dette er ikke det viste navn.  
![Vælg Dynamics 365 Business Central, og vælg Hent det nu](./media/across-how-to-connect-powerbi-d365-content-packs/powerbi-connect-to-d365-finance-and-operations-crm.png)
5. Når der er oprettet forbindelse, indlæses et dashboard, en rapport og et datasæt automatisk i dit Power BI-arbejdsområde. Når dette er fuldført, opdateres felterne med data fra din konto.
![Vælg Dynamics 365 Business Central, og vælg Hent det nu](./media/across-how-to-connect-powerbi-d365-content-packs/powerbi-workspace-dashboard-report-dataset.png)

## <a name="what-now"></a>Hvad nu?

- [Ændre felterne](https://docs.microsoft.com/en-us/power-bi/service-dashboard-edit-tile) i dashboardet.  
- [Vælg et felt](https://docs.microsoft.com/en-us/power-bi/service-dashboard-tiles) for at åbne den underliggende rapport.  
- Selv om dit datasæt planlægges til at blive opdateret dagligt, kan du ændre tidsplanen for opdatering eller prøve at opdatere det på behov ved hjælp af **Opdater nu**.

## <a name="system-requirements"></a>Systemkrav
Hvis du vil importere dine [!INCLUDE[d365fin_long_md](includes/d365fin_long_md.md)]-data i Power BI, skal du have rettigheder til de webtjenester, der bruges til at hente data. De webtjenester, der er nødvendige for hver indholdspakke omfatter:

**Microsoft Dynamics 365 Business Central – CRM**
- SalesOpportunities
- ExcelTemplateViewCompany

**Microsoft Dynamics 365 Business Central – Sales**
- ItemSalesbyCustomer
- SalesDashboard
- ExcelTemplateViewCompany

**Microsoft Dynamics 365 Business Central – Finance**
- PowerBIFinance
- ExcelTemplateViewCompany

**Microsoft Dynamics 365 Business Central – Jobs**
- Sagsoversigt
- Sagsplanlægningslinjer
- Sagsopgavelinjer

**Microsoft Dynamics 365 Business Central – Debitorliste**
- ItemSalesbyCustomer
- Power_BI_Item_Purchase_List
- Power_BI_Item_Sales_List
- SalesDashboard
- Power BI-debitorliste
- ExcelTemplateViewCompany

**Microsoft Dynamics 365 Business Central – Vareliste**
- ItemSalesbyCustomer
- Power_BI_Item_Purchase_List
- Power_BI_Item_Sales_List
- Varer
- SalesDashboard
- ExcelTemplateViewCompany

**Microsoft Dynamics 365 Business Central – Kreditorliste**
- ItemSalesbyCustomer
- Power_BI_Item_Purchase_List
- Power_BI_Item_Sales_List
- Varer
- SalesDashboard
- Power BI-debitorliste
- ItemSalesbyCustomer
- Power_BI_Vendor_List
- ExcelTemplateViewCompany

## <a name="web-services"></a>Webtjeneste
En nem måde at finde webtjenesterne på er at søge efter webtjenester i [!INCLUDE[d365fin_long_md](includes/d365fin_long_md.md)]. På listen skal du sørge for at feltet Publicer er markeret for de webtjenester, der er anført ovenfor.

## <a name="troubleshooting"></a>Fejlfinding
Power BI-dashboardet er baseret på de publicerede webtjenester, der er anført ovenfor, og viser data fra demonstrationsvirksomheden eller din egen virksomhed, hvis du indlæser data fra dit aktuelle økonomisystem. Men hvis noget går galt indeholder dette afsnit en løsning til de mest almindelige problemer.

### <a name="incorrect-company-name"></a>Forkert navn på virksomhed  
Det er en normal fejl at angive fælles virksomhedens visningsnavn i stedet for navnet på virksomheden. Du kan finde navnet på virksomheden ved at søge efter **virksomheder**. Brug derefter feltet **Navn**, når du angiver navnet på virksomheden.

### <a name="incorrect-user-name-and-password"></a>Forkert brugernavn og adgangskode  
Brugernavnet og adgangskoden, der bruges til at oprette forbindelse, skal være de samme, som bruges til at oprette forbindelse til din Microsoft Office 365-konto.  

Indholdspakkerne kræver også, at du har en Microsoft [!INCLUDE[d365fin_long_md](includes/d365fin_long_md.md)]-konto. Når du har indtastet dine legitimationsoplysninger, får du automatisk vist alle Microsoft [!INCLUDE[d365fin_long_md](includes/d365fin_long_md.md)]-lejere, du har adgang til. Hvis du ikke har en licenseret eller prøveversion af Microsoft [!INCLUDE[d365fin_long_md](includes/d365fin_long_md.md)]-konto, får du vist en fejlmeddelelse.

### <a name="the-key-didnt-match-any-rows-in-the-table"></a>Nøglen svarer ikke nogen rækker i tabellen
Hvis du angiver et ikke gyldigt firmanavn under oprettelsen af forbindelsen, kan du få vist meddelelsen "Nøglen svarer ikke nogen rækker i tabellen". Angiv det korrekte firmanavn, og forsøg igen.

## <a name="see-also"></a>Se også
[Kom i gang med Power BI](https://docs.microsoft.com/en-us/power-bi/service-get-started)  
[Power BI - grundlæggende begreber](https://docs.microsoft.com/en-us/power-bi/service-basic-concepts)
["Business Intelligence"](bi.md)  
[Velkommen til [!INCLUDE[d365fin_long](includes/d365fin_long_md.md)]](index.md)  
[Importere virksomhedsdata fra andre økonomisystemer](upload-data.md)  
[Opsætning af [!INCLUDE[d365fin](includes/d365fin_md.md)]](setup.md)  
[Finans](finance.md)  
[Opsætning af rapportering for [!INCLUDE[d365fin](includes/d365fin_md.md)] i Power BI](across-how-use-financials-data-source-powerbi.md)  
