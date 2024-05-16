---
title: Introduktion til Business Central og Power BI
description: Få over brug af Power BI for at få indsigt og KPI'er fra Business Central-data.
author: jswymer
ms.topic: overview
ms.search.keywords: 'account schedule, analysis, reporting, financial report, business intelligence, KPI'
ms.search.form: '6316, 6317'
ms.reviewer: jswymer
ms.date: 04/24/2024
ms.author: jswymer
ms.custom: bap-template
ms.service: dynamics-365-business-central
---
# Introduktion til Business Central og Power BI

[!INCLUDE[azure-ad-to-microsoft-entra-id](~/../shared-content/shared/azure-ad-to-microsoft-entra-id.md)]

Det er nemt at få indblik i dine [!INCLUDE[prod_short](includes/prod_short.md)]-data med [Power BI](https://powerbi.microsoft.com) - et datavisualiseringssystem fra Microsoft. Power BI henter [!INCLUDE[prod_short](includes/prod_short.md)]-data, så du kan oprette dashboards og rapporter, der er baseret på disse data. Power BI giver et fleksibelt alternativ til rapporter indbygget i [!INCLUDE[prod_short](includes/prod_short.md)], så du kan se og tilpasse visualiseringen og endda flette data fra forskellige virksomheder i [!INCLUDE[prod_short](includes/prod_short.md)]. Nogle Power BI-rapporter kan også integreres i Business Central og vises uden at forlade systemet. Mere komplekse dashboards kan opleves bedre fra Power BI-webstedet.

![Power BI og Business Central.](media/power-bi-intro.png)

## Hvad du kan foretage dig med Power BI og Business Central

Du kan arbejde med forskellige funktioner i [!INCLUDE[prod_short](includes/prod_short.md)] og Power BI. Nogle ting kan du foretage dig i Power BI, mens andre ting sker fra [!INCLUDE[prod_short](includes/prod_short.md)]. Nogle funktioner er også tilgængelige med [!INCLUDE[prod_short](includes/prod_short.md)] online, men ikke i det lokale miljø. Følgende tabel giver dig et overblik.

|Funktion|Beskrivelse|Online|Det lokale miljø|Lær mere|
|-------|-----------|--------------|-----------|----------------|
|Se [!INCLUDE[prod_short](includes/prod_short.md)]-data i Power BI|Du kan få vist dine data fra [!INCLUDE[prod_short](includes/prod_short.md)] i rapporter i Power BI. [!INCLUDE[prod_short](includes/prod_short.md)] online indeholder nogle foruddefinerede Power BI-rapporter. Eller din organisation har måske oprettet nogle brugerdefinerede rapporter.|![Arbejder online.](media/check.png)|![Arbejder i det lokale miljø](media/check.png)|[Her...](across-working-with-powerbi.md)|
|Se Power BI-rapporter i [!INCLUDE[prod_short](includes/prod_short.md)]-klienten.| Power BI-rapporter, der viser [!INCLUDE[prod_short](includes/prod_short.md)]-data, kan integreres direkte på dele af [!INCLUDE[prod_short](includes/prod_short.md)]-sider. Du kan ændre delen, så den viser enhver rapport, der er tilgængelig for dig. |![arbejder online.](media/check.png)|![Arbejder i det lokale miljø](media/check.png)<sup>[*](#onprem)</sup>|[Her...](across-working-with-powerbi.md).|
|Opret rapporter og dashboards i Power BI, som viser [!INCLUDE[prod_short](includes/prod_short.md)]-data.|Brug Power BI Desktop til at oprette dine egne rapporter og dashboards. Du kan udgive rapporterne til din egen Power BI-tjeneste eller dele dem med andre i din organisation.|![Arbejder online.](media/check.png)|![arbejder i det lokale miljø](media/check.png)|[Her...](across-how-use-financials-data-source-powerbi.md)|
|[!INCLUDE[prod_short](includes/prod_short.md)]-apps i Power BI| [!INCLUDE[prod_short](includes/prod_short.md)] publicerer tre apps til Power BI på Microsoft AppSource. Disse apps opretter detaljerede rapporter og dashboards i din Power BI-tjeneste, så du kan se [!INCLUDE[prod_short](includes/prod_short.md)]-data. Tilgængelige apps omfatter: <ul><li>[!INCLUDE [prod_long](includes/prod_long.md)] - CRM </li><li>[!INCLUDE [prod_long](includes/prod_long.md)] - Finance </li><li>[!INCLUDE [prod_long](includes/prod_long.md)] - Sales </li></ul>  |![Arbejder online.](media/check.png)||[Her...](across-powerbi-business-central-apps.md)|
|Arbejde med [!INCLUDE [prod_short](includes/prod_short.md)]-data i datamarts og dataflows|Fra og med juli 2022 kan du bruge [!INCLUDE [prod_short](includes/prod_short.md)]-connectoren i Power Query Online til dataflows, som du deler på tværs af forskellige rapporter og dashboards.|![arbejder online.](media/check.png)||[Her...](across-powerbi-business-central-apps.md)|

<a name="onprem"><sup>*</sup></a> Denne funktion kræver et registreret program til Business Central i Microsoft Azure. Du kan finde flere oplysninger i [Registrering af Business Central i det lokale miljø i Microsoft Entra ID til integration med andre tjenester](/dynamics365/business-central/dev-itpro/administration/register-app-azure).

## Gøre klar til at bruge Power BI

Der er nogle få opgaver, der skal udføres, før du kan bruge Power BI sammen med [!INCLUDE[prod_short](includes/prod_short.md)].<!-- Some of the tasks are typically only done by administrators or super users.--> Opgaverne afhænger af din rolle i organisationen, og hvad du skal gøre med Power BI:

- Som *forretningsbruger* kan du få vist Power BI-rapporter enten i Power BI-service eller i Business central
- Som *administrator* har du ansvaret for styringen af de indstillinger, der gælder for hele organisationen, som styrer, hvordan Business Central Power BI fungerer.
- Som *rapportopretter* skal du bygge brugerdefinerede Power BI-rapporter, du kan dele med andre brugere.

|Opgave|Forretningsbruger|Administrator|Rapportopretter|Flere oplysninger|
|----|-------------|-------------|-----------------------|----------------|
|Få en Power BI-konto.|![endnu en markering.](media/check.png)|![det er en markering](media/check.png)|![endnu en markering](media/check.png)|Gå til [https://powerbi.microsoft.com](https://powerbi.microsoft.com). Hvis du vil tilmelde dig en konto, skal du bruge din mailadresse og adgangskode. <br /><br/>Tilmelding kræver, at du har en licens, men i de fleste tilfælde bør du allerede have en gratis licens. Der er flere oplysninger under [Power BI Licens](admin-powerbi-setup.md#license).|
|Hent Power BI Desktop|||![endnu en markering.](media/check.png)|Hvis du vil hente, skal du gå til [Power BI Desktop](https://powerbi.microsoft.com/desktop/). Du kan finde flere oplysninger i [Hente Power BI Desktop](/power-bi/fundamentals/desktop-get-the-desktop).
|Vise Business Central-data i Power BI||![det er en markering.](media/check.png)|![endnu en markering](media/check.png)|[Vise data ved hjælp af API-sider eller OData-webtjenester](admin-powerbi-setup.md#exposedata)
|Aktivér Power BI-integration<br />(kun lokalt)||![det er en markering.](media/check.png)||[Konfigurer Business Central lokalt til Power BI-integration](across-working-with-business-central-in-powerbi.md#setup)|


## Næste trin

- Hvis du er administrator, som skal konfigurere Power BI i [!INCLUDE[prod_short](includes/prod_short.md)], skal du gå til [Aktivering af Power BI-integration](admin-powerbi-setup.md).
- Hvis Power BI allerede er oprettet, og du vil prøve funktionerne, skal du gå til [Arbejde med Power BI-rapporter i Business central](across-working-with-powerbi.md).

## Se også

[Oversigt over analyse](reports-bi-reporting.md)   
[Spore KPI'er med Power BI metrikværdier](track-kpis-with-power-bi-metrics.md)   
[Brug af [!INCLUDE[prod_short](includes/prod_short.md)] som Power BI-datakilde](across-how-use-financials-data-source-powerbi.md)  
[Brug af [!INCLUDE[prod_short](includes/prod_short.md)] som Power Apps-datakilde](across-how-use-financials-data-source-powerapps.md)  
[Brug [!INCLUDE[prod_short](includes/prod_short.md)] i Power Automate](across-how-use-financials-data-source-flow.md)  
[Power BI-dokumentation](/power-bi/)  
[Hvad er Power BI?](/power-bi/fundamentals/power-bi-overview)  
[Hurtig start: Opret forbindelse til data i Power BI Desktop](/power-bi/desktop-quickstart-connect-to-data)  
[Introduktion til datamarts](/power-bi/transform-model/datamarts/datamarts-overview)  
[Introduktion til dataflows og forberedelse af selvbetjeningsdata](/power-bi/transform-model/dataflows/dataflows-introduction-self-service)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
