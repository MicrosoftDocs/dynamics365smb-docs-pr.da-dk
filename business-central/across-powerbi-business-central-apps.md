---
title: Bruge Business Central-apps i Power BI
description: Du kan nemt få indsigt, business intelligence og nøgletal i dine Business Central-data med Business Central-apps for Power BI.
author: jswymer
ms.topic: get-started-article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: account schedule, analysis, reporting, financial report, business intelligence, KPI
ms.date: 04/01/2021
ms.author: jswymer
ms.openlocfilehash: 7a6b6de60f6262906429127b0588ca62c9dcca1b
ms.sourcegitcommit: 8b95e1700a9d1e5be16cbfe94fdf7b660f1cd5d7
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 09/09/2022
ms.locfileid: "9461071"
---
# <a name="use-the-prod_short-apps-in-power-bi"></a>Bruge [!INCLUDE [prod_short](includes/prod_short.md)]-apps i Power BI

> **GÆLDER FOR:** [!INCLUDE [prod_long](includes/prod_long.md)] online 

[!INCLUDE [prod_long](includes/prod_long.md)] udgiver følgende Power BI-apps, som indeholder detaljerede dashboards til visning af data:

- [!INCLUDE [prod_long](includes/prod_long.md)] - CRM  
- [!INCLUDE [prod_long](includes/prod_long.md)] - Finance  
- [!INCLUDE [prod_long](includes/prod_long.md)] - Sales

## <a name="overview"></a>Oversigt

Hver app indeholder flere rapporter, som du kan se detaljerede data i, herunder følgende funktioner:

- Vælg en visualisering på dashboardet for at få vist en af de underliggende rapporter.  
- Filtrer rapporten, eller tilføj felter, du vil overvåge.  
- Fastgør en brugerdefineret visning til dashboardet for fortsat sporing.  
  Du kan opdatere dataene manuelt, og kan du oprette en tidsplan for opdatering. Du kan finde flere oplysninger i [Konfiguration af planlagt opdatering](/power-bi/refresh-scheduled-refresh).  

Apps er designet til at arbejde med data fra alle de virksomheder i [!INCLUDE[prod_short](includes/prod_short.md)]. Når du installerer Power BI-app'en, angiver du en eller flere parametre for at oprette forbindelse til din [!INCLUDE [prod_short](includes/prod_short.md)].  

> [!NOTE]
> Du kan også oprette dine egne rapporter og dashboards i Power BI baseret på dine [!INCLUDE[prod_short](includes/prod_short.md)]-data. Du kan finde flere oplysninger i [Forbinde dine virksomhedsdata med Power BI](across-how-use-financials-data-source-powerbi.md). 

## <a name="prerequisites"></a>Forudsætninger

Power BI-apps kræver tilladelser til de tabeller, hvor der hentes data fra, og de webtjenester, der bruges til at hente data. I følgende tabel vises de webtjenester, der kræves for hver enkelt Power BI-app:
    
|App | Webtjenester|
|----|-------------|
|[!INCLUDE[prod_short](includes/prod_short.md)] – CRM| <ul><li>Salgsmuligheder</li><li>Vis virksomhedsoplysninger i Excel-skabelon</li><li>Power BI-rapportetiketter</li></ul>|
|[!INCLUDE[prod_short](includes/prod_short.md)] – Finance| <ul><li>PowerBIFinance</li><li>Vis virksomhedsoplysninger i Excel-skabelon</li><li>Power BI-rapportetiketter</li></ul>|
|[!INCLUDE[prod_short](includes/prod_short.md)] – Sales| <ul><li>Varestatistik efter kunde</li><li>Salgsdashboard</li><li>Vis virksomhedsoplysninger i Excel-skabelon</li><li>Power BI-rapportetiketter</li></ul>|

> [!TIP]
> En nem måde at finde webtjenesterne på er at søge efter *webtjenester* i [!INCLUDE[prod_short](includes/prod_short.md)]. På siden **Webtjenester** skal du sørge for, at feltet **Udgiv** er markeret for de webtjenester, der er angivet ovenfor. Du kan finde flere oplysninger i [Udgive en webtjeneste](across-how-publish-web-service.md).

## <a name="get-ready"></a>Gør dig klar

Tilmeld dig Power BI-tjenesten. Hvis du ikke allerede har tilmeldt dig, skal du gå til [https://powerbi.microsoft.com](https://powerbi.microsoft.com). Når du tilmelder dig, skal du bruge din mailadresse og adgangskode.

## <a name="install-a-prod_short-app-in-power-bi"></a>Installere en [!INCLUDE[prod_short](includes/prod_short.md)]-app i Power BI

1. Åbn browseren, gå til [https://powerbi.microsoft.com](https://powerbi.microsoft.com), og log på din konto.
2. Vælg **Hent data** nederst i venstre navigationsrude.  

    ![Navigere til Hent data.](./media/across-how-to-connect-powerbi-d365-content-packs/powerbi-get-data.png)

    Du kan også komme i gang inde fra [!INCLUDE [prod_short](includes/prod_short.md)]. Naviger til **Rapportvalg** i afsnittet Power BI fra startsiden. Vælg enten **Service** eller **Min virksomhed** på båndet. Enten er organisationsgalleriet i Power BI eller Microsoft AppSource åbnet, filtreret til kun at vise apps, der relaterer til [!INCLUDE[prod_short](includes/prod_short.md)].

3. I feltet **Tjenester** skal du vælge **Hent**.

    Dette trin åbner siden **Power BI-apps**, som du kan bruge til at søge efter Power BI-app, som er tilgængelig i **AppSource**.  

4. I feltet **Søg** skal du angive **Dynamics 365 Business Central**.
5. Vælg den app, du vil bruge, vælg **Hent den nu**, og derefter **Installer**.  

    Bagefter vil appen væge tilgængelig fra **Apps** i navigationsmenuen i Power BI.

## <a name="connect-the-prod_short-app-to-your-data"></a>Forbinde [!INCLUDE[prod_short](includes/prod_short.md)]-appen med dine data

1. Vælg Business Central-appen under **Apps**, og vælg derefter **Opret forbindelse**.
2. Når du bliver bedt om det, skal du udfylde **Virksomhedsnavn** og **Miljø** med oplysninger om den [!INCLUDE[prod_short](includes/prod_short.md)]-forekomst, som du vil oprette forbindelse til.

    - Fo **Virksomhedsnavn** skal du sørge for at bruge det fulde navn, ikke det viste navn. Virksomhedsnavnet findes på siden **Virksomheder** i [!INCLUDE[prod_short](includes/prod_short.md)]. 
    - Hvis du ikke har oprettet flere miljøer, skal du angive **Produktion** for **Miljø**.

3. Vælg **Næste**.
4. Vælg **Log på**.
5. Skriv brugernavnet og adgangskoden for at logge på [!INCLUDE[prod_short](includes/prod_short.md)], når du bliver bedt om det .
6. Når forbindelsen er oprettet, føjes der et dashboard og rapporter til dit Power BI-arbejdsområde. Når dette er fuldført, viser felterne data fra din [!INCLUDE[prod_short](includes/prod_short.md)]-virksomhed.

    ![Vælg Dynamics 365 Business Central, og vælg Hent nu.](./media/across-how-to-connect-powerbi-d365-content-packs/powerbi-workspace-dashboard-report-dataset.png)

## <a name="fixing-problems"></a>Løsning af problemer

Power BI-dashboardet er baseret på de udgivne webtjenester, der er angivet ovenfor. Det viser data fra demoregnskabet eller din egen virksomhed, hvis du importerer data fra den aktuelle økonomiløsning. Men hvis noget går galt indeholder dette afsnit en løsning til de mest almindelige problemer.  

### <a name="you-dont-have-a-power-bi-account"></a>Du har ikke en Power BI-konto

Der er ikke blevet oprettet en Power BI-konto. Du skal have en licens for at få en gyldig Power BI-konto. Du skal også tidligere have logget på Power BI for at oprette dit Power BI-arbejdsområde.  

### <a name="message-there-are-no-enabled-reports-choose-select-report-to-see-a-list-of-reports-that-you-can-display"></a>Meddelelse: Der er ingen aktiverede rapporter. Vælg Vælg rapport for at få vist en oversigt over de rapporter, du kan få vist.

Denne meddelelse vises, hvis standardrapporten ikke blev implementeret i Power BI-arbejdsområdet. Eller rapporten blev installeret, men blev ikke opdateret. Hvis dette problem opstår, skal du gå til rapporten i dit Power BI-arbejdsområde, vælge **Datasæt**, **Indstillinger** og derefter opdatere legitimationsoplysningerne manuelt. Når datasættet er opdateret, skal du gå tilbage til [!INCLUDE[prod_short](includes/prod_short.md)] og vælge rapporten manuelt på siden **Vælg rapporter**.

### <a name="you-need-a-power-bi-pro-license-to-install-the-prod_short-app-in-power-bi"></a>Du skal have Power BI-en Pro-licens for at kunne installere [!INCLUDE[prod_short](includes/prod_short.md)]-appen i Power BI

Du skal have en [Power BI Pro-licens](/power-bi/service-features-license-type) for at kunne dele indholdet, og de personer, du deler det med, skal også. Indholdet skal være i et arbejdsområde med en [Premium-kapacitet](/power-bi/service-premium-what-is). Du kan få flere oplysninger i [Sådan deler du dit arbejde i Power BI](/power-bi/service-how-to-collaborate-distribute-dashboards-reports).  

### <a name="parameter-validation-failed-please-make-sure-all-parameters-are-valid"></a>"Parametervalideringen mislykkedes, kontrollér, at alle parametre er gyldige"

Denne fejl angiver, at en eller flere af parametrene er ugyldige.

- Den angivne miljøparameter passer ikke til noget eksisterende [!INCLUDE[prod_short](includes/prod_short.md)]-produktions- eller sandkassemiljø.
- Den angivne virksomhedsparameter passer ikke til nogen eksisterende [!INCLUDE[prod_short](includes/prod_short.md)]-virksomheder. Kontrollér virksomhedsnavnet på siden **Virksomheder** i [!INCLUDE[prod_short](includes/prod_short.md)]
- Hvis du opretter forbindelse til [!INCLUDE[prod_short](includes/prod_short.md)] i det lokale miljø, angav du en ugyldig URL-adresse. Du kan kontrollere URL-adressen på siden **Webtjeneste** i [!INCLUDE[prod_short](includes/prod_short.md)]  
- En port er ikke åben, så anmodningen kan passere gennem firewall'en.

### <a name="cant-sign-in"></a>Kan ikke logge på

Hvis fejlmeddelelsen "logon mislykkedes" vises, efter at du har brugt dine legitimationsoplysninger for [!INCLUDE[prod_short](includes/prod_short.md)] til at logge på, kan det skyldes en af følgende situationer:

- Den konto, du bruger, har ikke rettigheder til at hente [!INCLUDE[prod_short](includes/prod_short.md)]-data fra din konto. Kontrollér, at du har tilladelse til de nødvendige data i [!INCLUDE[prod_short](includes/prod_short.md)], og prøv igen.
- Du har valgt en anden godkendelsestype end basis, hvis der oprettes forbindelse til [!INCLUDE[prod_short](includes/prod_short.md)] on-premises.
- Du har ikke angivet et gyldigt brugernavn eller en gyldig adgangskode.

### <a name="message-your-data-source-cant-be-refreshed-because-the-credentials-are-invalid-please-update-your-credentials-and-try-again"></a>Meddelelse: Datakilden kan ikke opdateres, fordi legitimationsoplysningerne er ugyldige. Opdater dine legitimationsoplysninger, og prøv igen

For [!INCLUDE[prod_short](includes/prod_short.md)] on-premises kan problemet skyldes, at URL-adressen til OData kun er synlig for det lokale netværk.

### <a name="incorrect-company-name"></a>Forkert virksomhedsnavn

Det er en normal fejl at angive fælles virksomhedens visningsnavn i stedet for navnet på virksomheden. Du kan finde navnet på virksomheden ved at søge efter **virksomheder**. Brug derefter feltet **Navn**, når du angiver navnet på virksomheden.

### <a name="the-key-didnt-match-any-rows-in-the-table"></a>Nøglen svarer ikke til nogen rækker i tabellen

Hvis du angiver et ikke gyldigt firmanavn under oprettelsen af forbindelsen, kan du få vist meddelelsen "Nøglen svarer ikke nogen rækker i tabellen". Angiv det korrekte firmanavn, og forsøg igen.

### <a name="historical-data-appears-to-be-missing"></a>Der mangler tilsyneladende historiske data

Når Power BI-appen er installeret, og dine data vises i Power BI, bemærker du måske, at du ikke kan se alle dine data. Datasættene er filtrerede til kun at returnere de tidligere 365 dages data. Denne standard er på plads for at gøre det hurtigere at lave rapporterne.  

### <a name="i-only-see-data-for-a-single-company"></a>Jeg kan kun se data for en enkelt virksomhed

Power BI-appen viser kun data fra den [!INCLUDE[prod_short](includes/prod_short.md)]-virksomhed, der blev defineret, da Power BI-appen blev installeret. Du kan føje data fra yderligere virksomheder til rapporterne ved at tilføje nye forespørgsler, der bruger forskellige virksomheder som datakilde.  

### <a name="what-now"></a>Hvad nu?

- Prøv [at stille et spørgsmål i feltet Spørgsmål og svar](/power-bi/service-q-and-a-tips) øverst i dashboardet.
- [Ændre felterne](/power-bi/service-dashboard-edit-tile) i dashboardet.  
- [Vælg et felt](/power-bi/service-dashboard-tiles) for at åbne den underliggende rapport.  
- Som standard er dit datasæt ikke planlagt til opdatering. Du kan ændre tidsplanen for opdatering eller prøve at opdatere det efter behov ved hjælp af **Opdater nu**. Du kan finde flere oplysninger i [Konfiguration af planlagt opdatering](/power-bi/refresh-scheduled-refresh).

## <a name="see-related-training-at-microsoft-learn"></a>Se relateret oplæring på [Microsoft Learn](/learn/modules/configure-powerbi-excel-dynamics-365-business-central/index)

## <a name="see-also"></a>Se også

[Business Central og Power BI](admin-powerbi.md)  
[Oversigt over Power BI-integrationskomponent og -arkitektur for [!INCLUDE[prod_short](includes/prod_short.md)]](admin-powerbi-overview.md)  
[Arbejde med [!INCLUDE [prod_short](includes/prod_short.md)] data i Power BI](across-working-with-business-central-in-powerbi.md)  
[Oprette Power BI-rapporter, der viser [!INCLUDE [prod_long](includes/prod_long.md)]-data](across-how-use-financials-data-source-powerbi.md)  
[Business Intelligence](bi.md)  
[Bliv klar til at agere](ui-get-ready-business.md)  
[Importere virksomhedsdata fra andre økonomisystemer](across-import-data-configuration-packages.md)  
[Konfigurere [!INCLUDE[prod_short](includes/prod_short.md)]](setup.md)  
[Brug af [!INCLUDE[prod_short](includes/prod_short.md)] som Power BI-datakilde](across-how-use-financials-data-source-powerbi.md)  
[Brug af [!INCLUDE[prod_short](includes/prod_short.md)] som Power Apps-datakilde](across-how-use-financials-data-source-powerapps.md)  
[Brug [!INCLUDE[prod_short](includes/prod_short.md)] i Power Automate](across-how-use-financials-data-source-flow.md)  
[Power BI-dokumentation](/power-bi/)  
[Hvad er Power BI?](/power-bi/fundamentals/power-bi-overview)  
[Hurtig start: Opret forbindelse til data i Power BI Desktop](/power-bi/desktop-quickstart-connect-to-data)  
[Introduktion til datamarts](/power-bi/transform-model/datamarts/datamarts-overview)  
[Introduktion til dataflows og forberedelse af selvbetjeningsdata](/power-bi/transform-model/dataflows/dataflows-introduction-self-service)  


[!INCLUDE[footer-include](includes/footer-banner.md)]