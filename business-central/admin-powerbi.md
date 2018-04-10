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
ms.date: 09/05/2017
ms.author: edupont
ms.translationtype: HT
ms.sourcegitcommit: e7dcdc0935a8793ae226dfc2f9709b5b8f487a62
ms.openlocfilehash: 7b62652e34c15831b44975a7c33b088e2be873e4
ms.contentlocale: da-dk
ms.lasthandoff: 03/22/2018

---
# <a name="enabling-your-business-data-for-power-bi"></a>Aktivere virksomhedens data til Power BI
Du kan nemt få indsigt i dine [!INCLUDE[d365fin](includes/d365fin_md.md)]-data med Power BI og [!INCLUDE[d365fin](includes/d365fin_md.md)]-indholdspakker. Power BI henter dine data og opretter derefter et out-of-the-box dashboard og rapporter baseret på dataene.  

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

## <a name="accessing-included365finincludesd365finmdmd-in-power-bi"></a>Adgang til [!INCLUDE[d365fin](includes/d365fin_md.md)] i Power BI
Når du vil have vist dine [!INCLUDE[d365fin](includes/d365fin_md.md)]-data i Power BI, skal du have følgende:  

* Adgang til [!INCLUDE[d365fin](includes/d365fin_md.md)]. Du kan finde flere oplysninger i [Business Central](http://go.microsoft.com/fwlink/?LinkID=759714).  
* Adgang til Power BI. Du kan finde flere oplysninger i [Power BI](https://powerbi.microsoft.com).

Du kan finde flere oplysninger på Power BI-webstedet om at [oprette forbindelse til tjenester med indholdspakker til Power BI](http://go.microsoft.com/fwlink/?LinkID=760850).  

Når du vil have adgang til dine [!INCLUDE[d365fin](includes/d365fin_md.md)]-data skal du på forbindelsessiden i Power BI angive følgende oplysninger:

| Felt | Beskrivelse |
| --- | --- |
| **URL-adresse til OData Feed** |URL-adressen til OData så Power BI kan få adgang til data fra din virksomhed, f.eks. https://mybusiness.financials.dynamics.com:7048/MS/ODataV4/Company('My%2Business'). |
| **Godkendelsesmetode** |Vælg **Basic**. |
| **Brugernavn** |Dit navn som det vises for kontoen i [!INCLUDE[d365fin](includes/d365fin_md.md)], f.eks. *John Smith*. |
| **Adg.kode** |Dette er webtjenesteadgangsnøglen til din brugerkonto i [!INCLUDE[d365fin](includes/d365fin_md.md)]. |

Det betyder, at du skal have tre oplysninger fra [!INCLUDE[d365fin](includes/d365fin_md.md)]: *OData URL-adressen* og *webtjenesteadgangsnøglen* til brugerkontoen.  

### <a name="getting-the-url"></a>Hente URL-adressen
Når du tilføjer [!INCLUDE[d365fin](includes/d365fin_md.md)] til Power BI, skal du angive en URL-adresse, så Power BI kan få adgang til data fra din virksomhed. På forbindelsessiden omtales URL-adressen som **URL-adresse til OData Feed**, og den skal have følgende format:

         https://mybusiness.financials.dynamics.com:7048/MS/ODataV4/Company('CRONUS%20US')  
I dette eksempel er *mybusiness* navnet på [!INCLUDE[d365fin](includes/d365fin_md.md)]-tjenesten, og *CRONUS US* er navnet på demonstrationsvirksomheden, hvor *%20* repræsenterer området i navnet.   
Du henter URL-adressen ved i [!INCLUDE[d365fin](includes/d365fin_md.md)] at søge efter og åbne vinduet **Webtjeneste**. Dette vindue viser de webtjenester, der aktuelt er tilgængelige, og du kan kopiere linket fra feltet **URL-adresse til OData** til en af standard OData-webtjenesterne.  

### <a name="getting-the-user-name-and-the-web-service-access-key"></a>Få brugernavnet og adgangsnøglen til webtjenesten
Hvis du vil bruge data fra [!INCLUDE[d365fin](includes/d365fin_md.md)] i Power BI skal du i vinduet **Opret forbindelse til Financials** angive et brugernavn og en adgangskode. Brugernavnet er dit navn som det vises for kontoen i [!INCLUDE[d365fin](includes/d365fin_md.md)], så Power BI kan logge det i [!INCLUDE[d365fin](includes/d365fin_md.md)]. Adgangskoden er den webtjenesteadgangsnøgle, der er konfigureret til din brugerkonto i [!INCLUDE[d365fin](includes/d365fin_md.md)].  

Du finder disse oplysninger ved i [!INCLUDE[d365fin](includes/d365fin_md.md)] at søge efter vinduet **Brugere** og derefter åbne kortet for din brugerkonto. I oversigtspanelet **Generelt** skal du kopiere indholdet af feltet **Brugernavn** og i oversigtspanelet **Webtjenesteadgang** kopiere indholdet af feltet **Webtjenesteadgangsnøgle**. Hvis feltet **Webtjenesteadgangsnøgle** er tomt, skal du på båndet vælge **Angiv webtjenesteadgangsnøgle**, vælge feltet **Nøglen udløber aldrig** og derefter klikke på knappen OK. Derefter kan du kopiere nøglen.  

## <a name="getting-data-from-included365finincludesd365finmdmd"></a>Hente data fra [!INCLUDE[d365fin](includes/d365fin_md.md)]
[!INCLUDE[d365fin](includes/d365fin_md.md)]-dashboardet viser de mest almindelige rapporter, du kan bruge til at registrere din virksomhed. Dataene er hentet fra [!INCLUDE[d365fin](includes/d365fin_md.md)]-virksomheden ved hjælp af webtjenester, der læser data direkte. I [!INCLUDE[d365fin](includes/d365fin_md.md)] indeholder vinduet **Webtjenester** de webtjenester, der er oprettet for dig.

> [!NOTE]  
>   Hvis du ændrer navnet på en af disse webtjenester, vises data ikke i Power BI.  
Hvis du vil tilføje andre data i Power BI, skal du finde tabellerne i [!INCLUDE[d365fin](includes/d365fin_md.md)], vise dem som webtjenester og derefter føje dem til indholdspakken. Dette er et avanceret scenarie, og det anbefales, at du starter med de data, der allerede findes i Power BI.  

## <a name="troubleshooting"></a>Fejlfinding
Power BI-dashboardet er baseret på de publicerede webtjenester, der er anført ovenfor, og viser data fra demonstrationsvirksomheden eller din egen virksomhed, hvis du indlæser data fra dit aktuelle økonomisystem. Men hvis noget går galt indeholder dette afsnit en løsning til de mest almindelige problemer.  

**"Parametervalideringen mislykkedes, kontroller, at alle parametre er gyldige"**  
Hvis du får denne fejlmeddelelse, når du har angivet URL-adressen til [!INCLUDE[d365fin](includes/d365fin_md.md)], skal du kontrollere, at følgende krav opfyldt:  

* URL-adressen følger dette mønster nøjagtigt:

    https://mybusiness.financials.dynamics.com:7048/MS/ODataV4/Company('CRONUS%20US')  
* Slet tekst, der evt. står efter firmanavn i parentes  
* Kontroller, at der ikke er nogen efterfølgende skråstreg i slutningen af URL-adressen.  
* Sørg for, at det er en sikker forbindelse, som når URL-adressen starter med *https*.  

**"Logon mislykkedes"**  
Hvis fejlmeddelelsen "Logon mislykkedes" vises, når du logger på dashboardet ved hjælp af dine legitimationsoplysninger til [!INCLUDE[d365fin](includes/d365fin_md.md)], kan det skyldes en af følgende situationer:

* Den konto, du bruger, har ikke rettigheder til at læse [!INCLUDE[d365fin](includes/d365fin_md.md)]-data fra din konto.

    Kontroller din brugerkonto i [!INCLUDE[d365fin](includes/d365fin_md.md)], og kontroller, at du har brugt den rigtige webtjenesteadgangsnøgle som adgangskode, og prøv derefter igen.  
* Den [!INCLUDE[d365fin](includes/d365fin_md.md)]-forekomst, du prøver at oprette forbindelse til, har ikke et gyldigt SSL-certifikat. I dette tilfælde kan du se en mere detaljeret fejlmeddelelse ("kan ikke etablere SSL-tillidsrelation").

    > [!NOTE]  
    >   Selvsignerede certifikater understøttes ikke.  

**"UPS"**  
Hvis du får vist en "UPS"-fejlmeddelelse, når du er færdig med godkendelsesdialogboksen, skyldes dette oftest problemer med forbindelsen til dataene til indholdspakken.

* Kontroller, at URL-adressen følger det mønster, der blev angivet tidligere:

    `https://mybusiness.financials.dynamics.com:7048/MS/ODataV4/Company('CRONUS%20US')`  
* En almindelig fejl er at angive hele URL-adressen til en bestemt webtjeneste:

    `https://mybusiness.financials.dynamics.com:7048/MS/ODataV4/Company('CRONUS%20US')/powerbifinance`
* Eller du kan have glemt at angive firmanavnet:

    `https://mybusiness.financials.dynamics.com:7048/MS/ODataV4/`

## <a name="see-also"></a>Se også
[Business Intelligence](bi.md)  
[Introduktion](product-get-started.md)  
[Overføre virksomhedsdata fra andre økonomisystemer](upload-data.md)  
[Bruge [!INCLUDE[d365fin](includes/d365fin_md.md)] som Power BI-datakilde](across-how-use-financials-data-source-powerbi.md)  
[Bruge [!INCLUDE[d365fin](includes/d365fin_md.md)] som PowerApps-datakilde](across-how-use-financials-data-source-powerapps.md)  
[Bruge [!INCLUDE[d365fin](includes/d365fin_md.md)] i Microsoft Flow](across-how-use-financials-data-source-flow.md)   

## [!INCLUDE[d365fin](includes/free_trial_md.md)]  
## [!INCLUDE[d365fin](includes/training_link_md.md)]

