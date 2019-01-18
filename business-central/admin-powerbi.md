---
title: Business Central og indholdspakker til Power BI | Microsoft Docs
description: "Du kan nemt få indsigt, business intelligence og nøgletal i dine Business Central-data med Power BI og Business Central-indholdspakker."
author: edupont04
ms.service: dynamics365-business-central
ms.topic: get-started-article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: account schedule, analysis, reporting, financial report, business intelligence, KPI
ms.date: 10/01/2018
ms.author: edupont
ms.translationtype: HT
ms.sourcegitcommit: caf7cf5afe370af0c4294c794c0ff9bc8ff4c31c
ms.openlocfilehash: 26fe722a863ada2bcd017e2bc614b976a7119a25
ms.contentlocale: da-dk
ms.lasthandoff: 11/22/2018

---
# <a name="enabling-your-business-data-for-power-bi"></a>Aktivere virksomhedens data til Power BI
Du kan nemt få indsigt i dine [!INCLUDE[d365fin](includes/d365fin_md.md)]-data med Power BI og [!INCLUDE[d365fin](includes/d365fin_md.md)]-indholdspakker. Power BI henter dine data og opretter derefter et out-of-the-box dashboard og rapporter baseret på dataene.  

Du skal have en gyldig konto til Dynamics 365 og til Power BI. Desuden skal du hente [Power BI Desktop](https://powerbi.microsoft.com/en-us/desktop/), hvis du vil oprette dine egne Power BI-rapporter. Power BI-indholdspakker kræver tilladelser til de tabeller, hvor data hentes fra. Yderligere oplysninger om kravene beskrives nedenfor.  

Microsoft er udgivet følgende indholdspakker:

| App | Beskrivelse |
| --- | --- |
| Microsoft Business Central | Indeholder et dashboard med de vigtigste finansielle data over en periode, f.eks. indtægter og udgifter, driftsavance og kassebeholdningsproces.|
| Microsoft Business Central - CRM | Indeholder et dashboard med vigtige oplysninger om salgsmuligheder og kontakter.  |
| Microsoft Business Central - Sales | Indeholder et dashboard med vigtige oplysninger om salg og lager. |

## <a name="using-the-dashboards"></a>Brug af dashboards
Hver indholdspakke indeholder rapporter, som du kan dykke ned i:

* Vælg en visualisering på dashboardet for at få vist en af de underliggende rapporter.  
* Filtrer rapporten, eller tilføj felter, du vil overvåge.  
* Fastgør denne brugerdefinerede visning til dashboardet for fortsat sporing.  
  Du kan opdatere dataene manuelt, og kan du oprette en tidsplan for opdatering. Du kan finde flere oplysninger i [Konfiguration af planlagt opdatering](https://powerbi.microsoft.com/en-us/documentation/powerbi-refresh-scheduled-refresh/).  

Indholdspakkerne er konfigureret til arbejde med data fra demonstrationsvirksomheden, som du får, når du tilmelder dig eksempelvisningen af [!INCLUDE[d365fin](includes/d365fin_md.md)]. Når du installerer de pågældende apps i Power BI, og du opretter forbindelse til dine egne data, fungerer nogle rapporter ikke, fordi de skal bruge data, som virksomheden ikke har. I så fald kan du ganske enkelt fjerne rapporten fra dashboardet.  

> [!NOTE]  
>   Du kan også oprette dine egne rapporter og dashboards i Power BI baseret på dine [!INCLUDE[d365fin](includes/d365fin_md.md)]-data. Du kan finde flere oplysninger under [Forbinde dine virksomhedsdata med Power BI](across-how-use-financials-data-source-powerbi.md).  

## <a name="how-to-connect"></a>Sådan oprettes forbindelse
1. Vælg **Hent data** nederst i venstre navigationsrude.  
![Navigere til Hent data](./media/across-how-to-connect-powerbi-d365-content-packs/powerbi-get-data.png)

Du kan også starte fra Dynamics 365 Business Edition. I rollecentret kan du gå til **Rapportvalg** i Power BI Rollecenter-delen. Vælg enten **Service** eller **Min virksomhed** på båndet. Hvis en af disse handlinger er markeret, åbnes enten galleriet Organisation i Power BI eller tjenestebiblioteket i Power BI, som også bliver filtreret, så det kun viser indholdspakker, der er relateret til [!INCLUDE[d365fin_long_md](includes/d365fin_long_md.md)].

2. I feltet **Tjenester** skal du vælge **Hent**. Der åbnes en side med **AppSource** og **Apps til Power BI-apps**.  
![Vælg indholdspakker fra onlinetjenester](./media/across-how-to-connect-powerbi-d365-content-packs/powerbi-online-services-get.png)
3. Vælg **Apps** under fanen **Apps til Power BI-apps**, vælg den **Microsoft Dynamics 365 Business Central**-indholdspakke, du vil bruge, og vælg derefter **Hent nu**.  
![Vælg Dynamics 365 Business Central, og vælg Hent det nu](./media/across-how-to-connect-powerbi-d365-content-packs/powerbi-dynamics365-for-financials-get-it-now.png)
4. Når du bliver bedt om det, skal du angive navnet på *virksomheden* i [!INCLUDE[d365fin_md](includes/d365fin_long_md.md)]. Dette er ikke det viste navn. Virksomhedsnavnet findes på siden 'Virksomheder' i din [!INCLUDE[d365fin_md](includes/d365fin_long_md.md)]-forekomst.  
![Vælg Dynamics 365 Business Central, og vælg Hent det nu](./media/across-how-to-connect-powerbi-d365-content-packs/powerbi-connect-to-d365-finance-and-operations-crm.png)
5. Når der er oprettet forbindelse, indlæses et dashboard, en rapport og et datasæt automatisk i dit Power BI-arbejdsområde. Når dette er fuldført, opdateres felterne med data fra din [!INCLUDE[d365fin_md](includes/d365fin_long_md.md)]-virksomhed.
![Vælg Dynamics 365 Business Central, og vælg Hent det nu](./media/across-how-to-connect-powerbi-d365-content-packs/powerbi-workspace-dashboard-report-dataset.png)

## <a name="what-now"></a>Hvad nu?

- Prøv [at stille et spørgsmål i feltet Spørgsmål og svar](https://docs.microsoft.com/en-us/power-bi/service-q-and-a-tips) øverst i dashboardet.
- [Ændre felterne](https://docs.microsoft.com/en-us/power-bi/service-dashboard-edit-tile) i dashboardet.  
- [Vælg et felt](https://docs.microsoft.com/en-us/power-bi/service-dashboard-tiles) for at åbne den underliggende rapport.  
- Selv om dit datasæt planlægges til at blive opdateret dagligt, kan du ændre tidsplanen for opdatering eller prøve at opdatere det på behov ved hjælp af **Opdater nu**.

## <a name="system-requirements"></a>Systemkrav
Hvis du vil importere dine [!INCLUDE[d365fin_long_md](includes/d365fin_long_md.md)]-data i Power BI, skal du have rettigheder til de webtjenester, der bruges til at hente data. De webtjenester, der er nødvendige for hver indholdspakke omfatter:

## <a name="role-center-reports"></a>Rollecenter-rapporter

**Microsoft Dynamics 365 Business Central – CRM**
- Salgsmuligheder
- Vis virksomhed i Excel-skabelon
- Power BI-rapportetiketter

**Microsoft Dynamics 365 Business Central – Finance**
- PowerBIFinance
- Vis virksomhed i Excel-skabelon
- Power BI-rapportetiketter

**Microsoft Dynamics 365 Business Central – Jobs**
- Sagsoversigt
- Sagsplanlægningslinjer
- Sagsopgavelinjer
- Power BI-rapportetiketter
- Vis virksomhed i Excel-skabelon

**Microsoft Dynamics 365 Business Central – Sales**
- Salgsdashboard
- Vis virksomhed i Excel-skabelon
- Power BI-rapportetiketter

## <a name="list-page-reports"></a>Oversigtssiderapporter

**Microsoft Dynamics 365 Business Central – Customers List**
- Varestatistik efter kunde
- Power BI-varekøbsoversigt
- Power BI-varesalgsoversigt
- Salgsdashboard
- Power BI-debitoroversigt
- ExcelTemplateViewCompany
- Power BI-rapportetiketter

**Microsoft Dynamics 365 Business Central - General Ledger Entries List**
- Power BI-finansbeløboversigt
- Budgetteret Power BI-finansbeløb
- ExcelTemplateViewCompany
- Power BI-rapportetiketter

**Microsoft Dynamics 365 Business Central – Items List**
- Varestatistik efter kunde
- Power BI-varekøbsoversigt
- Power BI-varesalgsoversigt
- Salgsdashboard
- ExcelTemplateViewCompany
- Power BI-rapportetiketter

**Microsoft Dynamics 365 Business Central – Jobs List**
- Power BI-sagsoversigt
- ExcelTemplateViewCompany
- Power BI-rapportetiketter

**Microsoft Dynamics 365 Business Central – Purchase Invoices List**
- Power BI-købsoversigt
- ExcelTemplateViewCompany
- Power BI-rapportetiketter

**Microsoft Dynamics 365 Business Central – Sales Orders List**
- Power BI-salgsoversigt
- ExcelTemplateViewCompany
- Power BI-rapportetiketter


**Microsoft Dynamics 365 Business Central – Vendors List**
- Power BI-varekøbsoversigt
- Power BI-varesalgsoversigt
- Power BI-kreditoroversigt
- ExcelTemplateViewCompany
- Power BI-rapportetiketter

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
[Business Intelligence](bi.md)  
[Introduktion](product-get-started.md)  
[Importere virksomhedsdata fra andre økonomisystemer](across-import-data-configuration-packages.md)  
[Opsætning af [!INCLUDE[d365fin](includes/d365fin_md.md)]](setup.md)  
[Importere virksomhedsdata fra andre økonomisystemer](across-import-data-configuration-packages.md)  
[Bruge [!INCLUDE[d365fin](includes/d365fin_md.md)] som Power BI-datakilde](across-how-use-financials-data-source-powerbi.md)  
[Bruge [!INCLUDE[d365fin](includes/d365fin_md.md)] som PowerApps-datakilde](across-how-use-financials-data-source-powerapps.md)  
[Bruge [!INCLUDE[d365fin](includes/d365fin_md.md)] i Microsoft Flow](across-how-use-financials-data-source-flow.md)   

## [!INCLUDE[d365fin](includes/free_trial_md.md)]  

