---
title: Introduktion til Business Central og Power BI
description: Få over brug af Power BI for at få indsigt, business intelligence og KPI'er fra Business Central-data.
author: jswymer
ms.topic: get-started-article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: account schedule, analysis, reporting, financial report, business intelligence, KPI
ms.search.form: 6316, 6317
ms.reviewer: edupont
ms.date: 04/01/2021
ms.author: jswymer
ms.openlocfilehash: c1935c51fbcabfc0371530532f18b2aaf6005dbb
ms.sourcegitcommit: 8a12074b170a14d98ab7ffdad77d66aed64e5783
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 03/31/2022
ms.locfileid: "8511801"
---
# <a name="prod_short-and-power-bi"></a>[!INCLUDE[prod_short](includes/prod_short.md)] og Power BI

Det er nemt at få indblik i dine [!INCLUDE[prod_short](includes/prod_short.md)]-data med [Power BI](https://powerbi.microsoft.com) - et datavisualiseringssystem fra Microsoft. Power BI henter [!INCLUDE[prod_short](includes/prod_short.md)]-data, der giver dig mulighed for at oprette dashboards og rapporter, der er baseret på disse data. Power BI giver et fleksibelt alternativ til rapporter indbygget i [!INCLUDE[prod_short](includes/prod_short.md)], så du kan se og tilpasse visualiseringen og endda flette data fra forskellige virksomheder i [!INCLUDE[prod_short](includes/prod_short.md)]. Nogle Power BI-rapporter kan også integreres i Business Central og vises uden at forlade systemet. Mere komplekse dashboards kan opleves bedre fra Power BI-webstedet.

![Power BI og Business Central.](media/power-bi-intro.png)

## <a name="what-you-can-do-with-power-bi-and-prod_short"></a>Hvad du kan gøre med Power BI og [!INCLUDE[prod_short](includes/prod_short.md)]

Du kan arbejde med forskellige funktioner i [!INCLUDE[prod_short](includes/prod_short.md)] og Power BI. Nogle ting kan du foretage dig i Power BI, mens andre ting sker fra [!INCLUDE[prod_short](includes/prod_short.md)]. Nogle funktioner er også tilgængelige med [!INCLUDE[prod_short](includes/prod_short.md)] online, men ikke i det lokale miljø. Følgende tabel giver dig et overblik.

|Funktion|Beskrivelse|Online|I det lokale miljø|Flere oplysninger|
|-------|-----------|--------------|-----------|----------------|
|Se [!INCLUDE[prod_short](includes/prod_short.md)]-data i Power BI|Du kan få vist dine data fra [!INCLUDE[prod_short](includes/prod_short.md)] i rapporter i Power BI. [!INCLUDE[prod_short](includes/prod_short.md)] online indeholder nogle foruddefinerede Power BI-rapporter. Eller din organisation har måske oprettet nogle brugerdefinerede rapporter, som er tilgængelige for dig.|![Arbejder online.](media/check.png)|![Arbejder i det lokale miljø](media/check.png)|[Se...](across-working-with-business-central-in-powerbi.md)|
|Se Power BI-rapporter i [!INCLUDE[prod_short](includes/prod_short.md)]-klienten.| Power BI-rapporter, der viser [!INCLUDE[prod_short](includes/prod_short.md)]-data, kan integreres direkte på dele af [!INCLUDE[prod_short](includes/prod_short.md)]-sider. Du kan ændre delen, så den viser enhver rapport, der er tilgængelig for dig. |![arbejder online.](media/check.png)|![Arbejder i det lokale miljø](media/check.png)<sup>[*](#onprem)</sup>|[Se...](across-working-with-powerbi.md).|
|Opret rapporter og dashboards i Power BI, som viser [!INCLUDE[prod_short](includes/prod_short.md)]-data.|Brug Power BI Desktop til at oprette dine egne rapporter og dashboards. Du kan udgive rapporterne til din egen Power BI-tjeneste eller dele dem med andre i din organisation.|![Arbejder online.](media/check.png)|![arbejder i det lokale miljø](media/check.png)|[Se...](across-how-use-financials-data-source-powerbi.md)
|[!INCLUDE[prod_short](includes/prod_short.md)]-apps i Power BI| [!INCLUDE[prod_short](includes/prod_short.md)] publicerer tre apps til Power BI på Microsoft AppSource. Disse apps opretter detaljerede rapporter og dashboards i din Power BI-tjeneste, så du kan se [!INCLUDE[prod_short](includes/prod_short.md)]-data. Tilgængelige apps omfatter: <ul><li>[!INCLUDE [prod_long](includes/prod_long.md)] - CRM </li><li>[!INCLUDE [prod_long](includes/prod_long.md)] - Finance </li><li>[!INCLUDE [prod_long](includes/prod_long.md)] - Sales </li></ul>  |![Arbejder online.](media/check.png)||[Se...](across-powerbi-business-central-apps.md)

<a name="onprem"><sup>*</sup></a> Denne funktion kræver et registreret program til Business Central i Microsoft Azure. Du kan finde flere oplysninger i [Registrering af Business Central i det lokale miljø i Azure AD til integration med andre tjenester](/dynamics365/business-central/dev-itpro/administration/register-app-azure).

## <a name="getting-ready-to-use-power-bi"></a>Gøre klar til at bruge Power BI

Der er nogle få opgaver, der skal udføres, før du kan bruge Power BI sammen med [!INCLUDE[prod_short](includes/prod_short.md)]. <!-- Some of the tasks are typically only done by administrators or super users.--> Opgaverne afhænger af din rolle i organisationen, og hvad du skal gøre med Power BI:

- Som *forretningsbruger* kan du få vist Power BI-rapporter enten i Power BI-service eller i Business central
- Som *administrator* har du ansvaret for styringen af de indstillinger, der gælder for hele organisationen, som styrer, hvordan Business Central Power BI fungerer.
- Som *rapportopretter* skal du bygge brugerdefinerede Power BI-rapporter, du kan dele med andre brugere.

|Opgave|Forretningsbruger|Administrator|Rapportopretter|Flere oplysninger|
|----|-------------|-------------|-----------------------|----------------|
|Få en Power BI-konto.|![endnu en markering.](media/check.png)|![det er en markering](media/check.png)|![endnu en markering](media/check.png)|Gå til [https://powerbi.microsoft.com](https://powerbi.microsoft.com). Hvis du vil tilmelde dig en konto, skal du bruge din mailadresse og adgangskode. <br /><br/>Tilmelding kræver, at du har en licens, men i de fleste tilfælde bør du allerede have en gratis licens. Der er flere oplysninger under [Power BI Licens](admin-powerbi-setup.md#license).|
|Hent Power BI Desktop|||![endnu en markering.](media/check.png)|Hvis du vil hente, skal du gå til [Power BI Desktop](https://powerbi.microsoft.com/desktop/). Du kan finde flere oplysninger i [Hente Power BI Desktop](/power-bi/fundamentals/desktop-get-the-desktop).
|Vise Business Central-data i Power BI||![det er en markering.](media/check.png)|![endnu en markering](media/check.png)|[Vise data ved hjælp af API-sider eller OData-webtjenester](admin-powerbi-setup.md#exposedata)
|Aktivér Power BI-integration<br />(kun lokalt)||![det er en markering.](media/check.png)||[Konfigurer Business Central lokalt til Power BI-integration](admin-powerbi-setup.md#setup)|


<!--



1. If you're using [!INCLUDE[prod_short](includes/prod_short.md)] on-premises, make sure your deployment meets the requirements outlined in [Set up [!INCLUDE[prod_short](includes/prod_short.md)] on-premises for Power BI integration](admin-powerbi-setup.md#setup). This task is typically an administrative task.

2. Expose Business Central data through API pages or published web services.

    Business Central online automatically included several pages as APIs. For more information, see [Business Central API V2.0](/dynamics365/business-central/dev-itpro/api-reference/v2.0/). Application developers for Business Central online can create custom API pages that you can then consume in reports. For more information, see [Developing a Custom API](/dynamics365/business-central/dev-itpro/developer/devenv-develop-custom-api).

   Codeunit, page, and query objects can be published as OData web services. There are many web services published by default. An easy way to find the web services is to search for *web services* in [!INCLUDE[prod_short](includes/prod_short.md)]. For more information about publishing web services, see [Publish a Web Service](across-how-publish-web-service.md).

3. Get a Power BI account.

   To do anything with Power BI and [!INCLUDE[prod_short](includes/prod_short.md)], whether you're an administrator or just a consumer, you'll need Power BI service account. To get an account, go to [https://powerbi.microsoft.com](https://powerbi.microsoft.com). To sign up for an account, use your work email address and password. Sign-up requires that you have a license, but in most cases you should already have a free license. For more information, see [Power BI Licensing](admin-powerbi-setup.md#license).

4. If you want to create your own Power BI reports, get Power BI Desktop.

   You can download [Power BI Desktop](https://powerbi.microsoft.com/desktop/). For more information, see [Get Power BI Desktop](/power-bi/fundamentals/desktop-get-the-desktop).

-->

## <a name="see-related-training-at-microsoft-learn"></a>Se relateret træning på [Microsoft Learn](/learn/modules/configure-powerbi-excel-dynamics-365-business-central/index)

## <a name="see-also"></a>Se også

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