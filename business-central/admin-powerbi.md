---
title: Introduktion til Business Central og Power BI| Microsoft Docs
description: Få over brug af Power BI for at få indsigt, business intelligence og KPI'er fra Business Central-data.
author: jswymer
ms.service: dynamics365-business-central
ms.topic: get-started-article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: account schedule, analysis, reporting, financial report, business intelligence, KPI
ms.reviewer: edupont
ms.date: 10/01/2020
ms.author: jswymer
ms.openlocfilehash: 9768fca2bea274a8124c34e151d399baa23f9f03
ms.sourcegitcommit: a9d48272ce61e5d512a30417412b5363e56abf30
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 03/04/2021
ms.locfileid: "5493113"
---
# <a name="prod_short-and-power-bi"></a>[!INCLUDE[prod_short](includes/prod_short.md)] og Power BI

Det er nemt at få indblik i dine [!INCLUDE[prod_short](includes/prod_short.md)]-data med [Power BI](https://powerbi.microsoft.com) - et datavisualiseringssystem fra Microsoft. Power BI henter [!INCLUDE[prod_short](includes/prod_short.md)]-data, der giver dig mulighed for at oprette dashboards og rapporter, der er baseret på disse data. Power BI giver et fleksibelt alternativ til rapporter indbygget i [!INCLUDE[prod_short](includes/prod_short.md)], så du kan se og tilpasse visualiseringen og endda flette data fra forskellige virksomheder i [!INCLUDE[prod_short](includes/prod_short.md)]. Nogle Power BI-rapporter kan også integreres i Business Central og vises uden at forlade systemet. Mere komplekse dashboards kan opleves bedre fra Power BI-webstedet.

![Power BI og Business Central](media/power-bi-intro.png)

## <a name="what-you-can-do-with-power-bi-and-prod_short"></a>Hvad du kan gøre med Power BI og [!INCLUDE[prod_short](includes/prod_short.md)]

Du kan arbejde med forskellige funktioner i [!INCLUDE[prod_short](includes/prod_short.md)] og Power BI. Nogle ting kan du foretage dig i Power BI, mens andre ting sker fra [!INCLUDE[prod_short](includes/prod_short.md)]. Nogle funktioner er også tilgængelige med [!INCLUDE[prod_short](includes/prod_short.md)] online, men ikke i det lokale miljø. Følgende tabel giver dig et overblik.

|Funktion|Beskrivelse|Online|I det lokale miljø|Flere oplysninger|
|-------|-----------|--------------|-----------|----------------|
|Se [!INCLUDE[prod_short](includes/prod_short.md)]-data i Power BI|Du kan få vist dine data fra [!INCLUDE[prod_short](includes/prod_short.md)] i rapporter i Power BI. [!INCLUDE[prod_short](includes/prod_short.md)] online indeholder nogle foruddefinerede Power BI-rapporter. Eller din organisation har måske oprettet nogle brugerdefinerede rapporter, som er tilgængelige for dig.|![Arbejder online](media/check.png)|![Arbejder i det lokale miljø](media/check.png)|[Se...](across-working-with-business-central-in-powerbi.md)|
|Se Power BI-rapporter i [!INCLUDE[prod_short](includes/prod_short.md)]-klienten.| Power BI-rapporter, der viser [!INCLUDE[prod_short](includes/prod_short.md)]-data, kan integreres direkte på dele af [!INCLUDE[prod_short](includes/prod_short.md)]-sider. Du kan ændre delen, så den viser enhver rapport, der er tilgængelig for dig. |![arbejder online](media/check.png)|![Arbejder i det lokale miljø](media/check.png)<sup>[*](#onprem)</sup>|[Se...](across-working-with-powerbi.md).|
|Opret rapporter og dashboards i Power BI, som viser [!INCLUDE[prod_short](includes/prod_short.md)]-data.|Brug Power BI Desktop til at oprette dine egne rapporter og dashboards. Du kan udgive rapporterne til din egen Power BI-tjeneste eller dele dem med andre i din organisation.|![Arbejder online](media/check.png)|![arbejder i det lokale miljø](media/check.png)|[Se...](across-how-use-financials-data-source-powerbi.md)
|[!INCLUDE[prod_short](includes/prod_short.md)]-apps i Power BI| [!INCLUDE[prod_short](includes/prod_short.md)] publicerer tre apps til Power BI på Microsoft AppSource. Disse apps opretter detaljerede rapporter og dashboards i din Power BI-tjeneste, så du kan se [!INCLUDE[prod_short](includes/prod_short.md)]-data. Tilgængelige apps omfatter: <ul><li>[!INCLUDE [prod_long](includes/prod_long.md)] - CRM </li><li>[!INCLUDE [prod_long](includes/prod_long.md)] - Finance </li><li>[!INCLUDE [prod_long](includes/prod_long.md)] - Sales </li></ul>  |![Arbejder online](media/check.png)||[Se...](across-powerbi-business-central-apps.md)

<a name="onprem"><sup>*</sup></a> Denne funktion kræver et registreret program til Business Central i Microsoft Azure. Du kan finde flere oplysninger under [Registrering af Business Central i det lokale miljø i Azure AD til integration med andre tjenester](/dynamics365/business-central/dev-itpro/administration/register-app-azure).

## <a name="getting-ready-to-use-power-bi"></a>Gøre klar til at bruge Power BI

Der er nogle få opgaver, der skal udføres, før du kan bruge Power BI sammen med [!INCLUDE[prod_short](includes/prod_short.md)]. Nogle af opgaverne udføres typisk kun af administratorer eller superbrugere.

1. Hvis du bruger [!INCLUDE[prod_short](includes/prod_short.md)] i det lokale miljø, skal du sørge for, at din installation opfylder de krav, der er opstillet i [Konfigurere [!INCLUDE[prod_short](includes/prod_short.md)] i det lokale miljø til Power BI-integration](admin-powerbi-setup.md#setup). Denne opgave er typisk en administrativ opgave.

2. Udgiv data som webtjenester.

    Codeunits, sider og forespørgsler, som du vil bruge som datakilder i Power BI-rapporter, skal udgives som webtjenester. Der udgives mange webtjenester som standard. En nem måde at finde webtjenesterne på er at søge efter *webtjenester* i [!INCLUDE[prod_short](includes/prod_short.md)].

    Du kan finde flere oplysninger om udgivelse af webtjenester under [Udgive en webtjeneste](across-how-publish-web-service.md).

3. Få en Power BI-konto.

    For at gøre noget med Power BI og [!INCLUDE[prod_short](includes/prod_short.md)], uanset om du er administrator eller bare forbruger, skal du have en Power BI-servicekonto. Hvis du vil have en konto, skal du gå til [https://powerbi.microsoft.com](https://powerbi.microsoft.com). Hvis du vil tilmelde dig en konto, skal du bruge din mailadresse og adgangskode. Tilmelding kræver, at du har en licens, men i de fleste tilfælde bør du allerede have en gratis licens. Du kan finde flere oplysninger i [Power BI-licenser](admin-powerbi-setup.md#license).

4. Hvis du vil oprette dine egne Power BI-rapporter, skal du have Power BI Desktop.

    Du kan downloade [Power BI Desktop](https://powerbi.microsoft.com/desktop/). Du kan finde flere oplysninger under [Hente Power BI Desktop](/power-bi/fundamentals/desktop-get-the-desktop).

## <a name="see-related-training-at-microsoft-learn"></a>Se relateret oplæring på [Microsoft Learn](/learn/modules/configure-powerbi-excel-dynamics-365-business-central/index)

## <a name="see-also"></a>Se også

[Power BI for forbrugere](/power-bi/consumer/end-user-consumer)  
[Power BI-tjenestens nye udseende](/power-bi/service-new-look)  
[Hurtig start: Opret forbindelse til data i Power BI Desktop](/power-bi/desktop-quickstart-connect-to-data)  
[Power BI-dokumentation](/power-bi/)  
[Business Intelligence](bi.md)  
[Introduktion](product-get-started.md)  
[Importere virksomhedsdata fra andre økonomisystemer](across-import-data-configuration-packages.md)  
[Opsætning af [!INCLUDE[prod_short](includes/prod_short.md)]](setup.md)  
[Bruge [!INCLUDE[prod_short](includes/prod_short.md)] som Power BI-datakilde](across-how-use-financials-data-source-powerbi.md)  
[Bruge [!INCLUDE[prod_short](includes/prod_short.md)] som Power Apps-datakilde](across-how-use-financials-data-source-powerapps.md)  
[Bruge [!INCLUDE[prod_short](includes/prod_short.md)] i Power Automate](across-how-use-financials-data-source-flow.md)  

## [!INCLUDE[prod_short](includes/free_trial_md.md)]  


[!INCLUDE[footer-include](includes/footer-banner.md)]