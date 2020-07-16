---
title: Brug Business Central i Power BI rapporter | Microsoft Docs
description: Gøre dine data tilgængelige som en datakilde i Power BI og opbygge nyttige rapporter over status for din virksomhed.
author: edupont04
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: business intelligence, KPI, Odata, Power App, SOAP, analysis
ms.date: 04/01/2020
ms.author: edupont
ms.openlocfilehash: b42437f0759ecb6d977797b31222bfa2b88cdb13
ms.sourcegitcommit: 3e9c89f90db5eaed599630299353300621fe4007
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 07/01/2020
ms.locfileid: "3528458"
---
# <a name="using-prodlong-as-power-bi-data-source-for-building-reports"></a>Brug af [!INCLUDE[prodlong](includes/prodlong.md)] som Power BI-datakilde til oprettelse af rapporter

Du kan gøre dine [!INCLUDE[prodlong](includes/prodlong.md)]-data tilgængelige som datakilde i Power BI og opbygge nyttige rapporter over status for din virksomhed.  

Du skal have en gyldig konto til [!INCLUDE[prodshort](includes/prodshort.md)] og til Power BI. Desuden skal du også hente [Power BI Desktop](https://powerbi.microsoft.com/desktop/). Du kan finde flere oplysninger under [Hurtig start: Opret forbindelse til data i Power BI Desktop](/power-bi/desktop-quickstart-connect-to-data).  

## <a name="to-add-prodshort-as-a-data-source-in-power-bi-desktop"></a>Sådan tilføjes [!INCLUDE[prodshort](includes/prodshort.md)] som en datakilde i Power BI Desktop

1. I Power BI Desktop skal du i den venstre navigationsrude vælge **Hent data**.
2. På siden **Hent data** skal du vælge **Onlinetjenester**, vælge **Microsoft Dynamics 365 Business Central** og derefter vælge knappen **Opret forbindelse**.
3. Power BI viser en guide, der hjælper dig gennem forbindelsesprocessen, deriblandt at logge ind på [!INCLUDE[prodshort](includes/prodshort.md)]. Vælg **Log på**, og vælg derefter den relevante konto. Brug den samme konto, som du bruger til at logge på [!INCLUDE[prodshort](includes/prodshort.md)].
4. Vælg knappen **Opret forbindelse** for at forsætte. Guiden Power BI viser en liste over Microsoft [!INCLUDE[d365fin](includes/d365fin_md.md)]-miljøer, -regnskaber og -datakilder. Disse datakilder repræsenterer de webtjenester, som du har publiceret fra [!INCLUDE[prodshort](includes/prodshort.md)].

    Du kan også oprette en ny URL-adresse til en webtjeneste i [!INCLUDE[prodshort](includes/prodshort.md)] i stedet. Vælg en af følgende metoder:

      - Brug handlingen **Opret datasæt** på siden **Webtjenester**
      - Brug vejledningen **Opsæt rapportering** med assisteret opsætning
      - Vælg handlingen **Rediger i Excel** på en vilkårlig liste

5. Angiv de data, du vil føje til dine datamodel, og vælg derefter knappen **Indlæsning**.
6. Gentag fremgangsmåden for at tilføje flere [!INCLUDE[prodshort](includes/prodshort.md)] eller andre data til din Power BI-datamodel.

> [!NOTE]  
> Når du har oprettet forbindelse til [!INCLUDE[prodshort](includes/prodshort.md)], bliver du ikke bedt om at logge på igen.

Når dataene er indlæst, kan du se dem i den højre navigation på siden. Du har oprettet forbindelse til dine [!INCLUDE[prodshort](includes/prodshort.md)]-data, og du kan begynde at oprette din Power BI-rapport.  

Før du opretter rapporten, anbefales det, at du importerer [!INCLUDE[prodshort](includes/prodshort.md)]-temafilen.  Temafilen opretter en farvepalet, så du kan oprette rapporter med de samme farvenuancer som [!INCLUDE[prodshort](includes/prodshort.md)]-apps, uden at du skal definere brugerdefinerede farver til hvert visuelle element.

Der er flere oplysninger i [Power BI-dokumentationen](/power-bi/consumer/).

## <a name="see-related-training-at-microsoft-learn"></a>Se relateret oplæring på [Microsoft Learn](/learn/modules/configure-powerbi-excel-dynamics-365-business-central/index)

## <a name="see-also"></a>Se også

[Aktivere virksomhedens data til Power BI](admin-powerbi.md)  
[Business Intelligence](bi.md)  
[Introduktion](product-get-started.md)  
[Importere virksomhedsdata fra andre økonomisystemer](across-import-data-configuration-packages.md)  
[Opsætning af [!INCLUDE[d365fin](includes/d365fin_md.md)]](setup.md)  
[Finans](finance.md)  
[Hurtig start: Opret forbindelse til data i Power BI Desktop](/power-bi/desktop-quickstart-connect-to-data)  
