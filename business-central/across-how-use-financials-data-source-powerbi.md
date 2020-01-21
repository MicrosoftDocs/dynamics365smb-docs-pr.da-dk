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
ms.date: 01/13/2020
ms.author: edupont
ms.openlocfilehash: a069fb7df3738b1f42aa2ddc86ce95144c39daff
ms.sourcegitcommit: ead69ebe5b29927876a4fb23afb6c066f8854591
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 01/14/2020
ms.locfileid: "2952838"
---
# <a name="using-include-prodlongincludesprodlongmd-as-power-bi-data-source-for-building-reports"></a>Brug af [!INCLUDE [prodlong](includes/prodlong.md)] som Power BI-datakilde til oprettelse af rapporter

Du kan gøre dine [!INCLUDE[prodlong](includes/prodlong.md)]-data tilgængelige som datakilde i Power BI og opbygge nyttige rapporter over status for din virksomhed.  

Du skal have en gyldig konto til [!INCLUDE[prodshort](includes/prodshort.md)] og til Power BI. Desuden skal du hente [Power BI Desktop](https://powerbi.microsoft.com/desktop/). Du kan finde flere oplysninger under [Hurtig start: Opret forbindelse til data i Power BI Desktop](/power-bi/desktop-quickstart-connect-to-data).  

## <a name="to-add-includeprodshortincludesprodshortmd-as-a-data-source-in-power-bi-desktop"></a>Sådan tilføjes [!INCLUDE[prodshort](includes/prodshort.md)] som en datakilde i Power BI Desktop

1. I Power BI Desktop skal du i den venstre navigationsrude vælge **Hent data**.
2. På siden **Hent data** skal du vælge **Onlinetjenester**, vælge **Microsoft Dynamics 365 Business Central** og derefter vælge knappen **Opret forbindelse**.
3. Power BI viser en guide, der hjælper dig gennem forbindelsesprocessen. Du bliver bedt om at logge på [!INCLUDE [prodshort](includes/prodshort.md)]. Vælg **Log på**, og vælg den konto, du vil logge på som. Det skal være den samme konto, du bruger til at logge på [!INCLUDE [prodshort](includes/prodshort.md)].
4. Vælg knappen **Opret forbindelse** for at forsætte. Guiden Power BI viser en liste over Microsoft [!INCLUDE[d365fin](includes/d365fin_md.md)]-miljøer, -regnskaber og -datakilder. Disse datakilder repræsenterer all de webtjenester, som du har publiceret fra hver lejer/regnskab i [!INCLUDE [prodshort](includes/prodshort.md)].
5. Du kan også vælge at oprette en ny URL-adresse for webtjenesten i [!INCLUDE [prodshort](includes/prodshort.md)] ved at bruge handlingen **Opret datasæt** på siden **Webtjenester** ved hjælp af guiden Assisteret opsætning for **Konfigurer rapporteringsdata** eller ved at vælge handlingen **Rediger i Excel** på en af listerne.
6. Angiv de data, du vil føje til dine datamodel, og vælg derefter knappen **Indlæsning**.
7. Gentag fremgangsmåden for at tilføje flere [!INCLUDE [prodshort](includes/prodshort.md)] eller andre data til din Power BI-datamodel.

> [!NOTE]  
> Når du har oprettet forbindelse til [!INCLUDE [prodshort](includes/prodshort.md)], bliver du ikke bedt om at logge på igen.

Når dataene er indlæst, vises de i den rigtige navigation på siden. Nu har du oprettet forbindelse til dine [!INCLUDE [prodshort](includes/prodshort.md)]-data og er klar til at begynde at oprette din Power BI-rapport.  

Før du opretter rapporten, anbefales det, at du importerer [!INCLUDE [prodshort](includes/prodshort.md)]-temafilen.  Temafilen opretter en farvepalet, så du kan oprette rapporter med de samme farvenuancer som [!INCLUDE [prodshort](includes/prodshort.md)]-apps, uden at du skal definere brugerdefinerede farver til hvert visuelle element.

Der er flere oplysninger i [Power BI-dokumentationen](/power-bi/consumer/power-bi-consumer-landing/).

## <a name="see-related-training-at-microsoft-learnlearnmodulesconfigure-powerbi-excel-dynamics-365-business-centralindex"></a>Se relateret oplæring på [Microsoft Learn](/learn/modules/configure-powerbi-excel-dynamics-365-business-central/index)

## <a name="see-also"></a>Se også

[Aktivere virksomhedens data til Power BI](admin-powerbi.md)  
[Business Intelligence](bi.md)  
[Introduktion](product-get-started.md)  
[Importere virksomhedsdata fra andre økonomisystemer](across-import-data-configuration-packages.md)  
[Opsætning af [!INCLUDE[d365fin](includes/d365fin_md.md)]](setup.md)  
[Finans](finance.md)  
[Hurtig start: Opret forbindelse til data i Power BI Desktop](/power-bi/desktop-quickstart-connect-to-data)  
