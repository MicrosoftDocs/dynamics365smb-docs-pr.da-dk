---
title: Bruge Dynamics 365 for Financials som Power BI-datakilde | Microsoft Docs
description: "Du kan gøre dine Financials-data tilgængelige som en datakilde i Power BI og opbygge nyttige rapporter over status for din virksomhed."
services: project-madeira
documentationcenter: 
author: edupont04
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: business intelligence, KPI, Odata, Power App, SOAP, analysis
ms.date: 12/02/2016
ms.author: edupont
ms.translationtype: Human Translation
ms.sourcegitcommit: a31be0f9d07e2abb591e26f6bae34c6f6e4dcda6
ms.openlocfilehash: 5213b515dfdf1f0e538a6d003cf921781ca6b3ff
ms.contentlocale: da-dk
ms.lasthandoff: 05/04/2017


---
# <a name="using-dynamics-365-for-financials-as-a-power-bi-data-source"></a>Bruge Dynamics 365 for Financials som Power BI-datakilde
Du kan gøre dine [!INCLUDE[d365fin](includes/d365fin_md.md)]-data tilgængelige som en datakilde i Power BI og opbygge nyttige rapporter over status for din virksomhed.  

**Bemærk**: Du skal have en gyldig konto til [!INCLUDE[d365fin](includes/d365fin_md.md)] og til Power BI. Desuden skal du hente [Power BI Desktop](https://powerbi.microsoft.com/en-us/desktop/).  

## <a name="to-add-included365finincludesd365finmdmd-as-a-data-source-in-power-bi-desktop"></a>Sådan tilføjes [!INCLUDE[d365fin](includes/d365fin_md.md)] som en datakilde i Power BI Desktop
1. I Power BI Desktop skal du i den venstre navigationsrude vælge **Hent data**.
2. I vinduet **Hent data** skal du vælge **Onlinetjenester**, vælge **Dynamics 365 for Financials** og derefter vælge knappen **Opret forbindelse**.

   Power BI viser en guide, der hjælper dig gennem forbindelsesprocessen. Som det første trin skal du angive en OData URL-adresse og det firmanavn, der er knyttet til din [!INCLUDE[d365fin](includes/d365fin_md.md)]-konto.  

   For *OData URL-adressen* kan du kopiere OData V4 URL-adressen på en af de webtjenester, der er angivet på siden **Webtjeneste** i [!INCLUDE[d365fin](includes/d365fin_md.md)], f.eks. `https://mycompany.financials.dynamics.com:7048/MS/ODataV4/`.  

   Som *Virksomhedsnavn* skal du bruge det navn, der vises i feltet **Navn** i vinduet **Virksomhedsoplysninger** vindue i [!INCLUDE[d365fin](includes/d365fin_md.md)]. Hvis din [!INCLUDE[d365fin](includes/d365fin_md.md)]-version indeholder flere virksomheder, skal du vælge det relevante virksomhedsnavn på listen i vinduet **Virksomheder**. I begge tilfælde skal du sørge for, at det navn, du angiver i guiden Power BI, er nøjagtigt det samme som den tekst, der vises i [!INCLUDE[d365fin](includes/d365fin_md.md)], f.eks. `My Company`.
3. Vælg knappen OK, når du har angivet oplysningerne. Som det næste trin i guiden skal du angive brugernavn og adgangskode.

   **Bemærk**: Hvis der er andre indstillinger for godkendelse i venstre navigationsrude, skal du vælge *Basis*.
4. Angiv dit brugernavn og adgangskode. Du kan finde disse oplysninger i vinduet **Brugere** i [!INCLUDE[d365fin](includes/d365fin_md.md)]. Brug **Webadgangsnøgle** som adgangskode.

   Dit brugernavn er f.eks. *Administrator*, og den webtjenesteadgangsnøgle, der fungerer som din adgangskode, er *EgzeUFQ9Uv0o5O0lUMyqCzo1ueUW9yRF3SsLU =*.
5. Vælg knappen **Forbindelse** for at forsætte. Der vises en liste over [!INCLUDE[d365fin](includes/d365fin_md.md)]-datakilder. Disse datakilder repræsenterer de webtjenester, som du har publiceret fra [!INCLUDE[d365fin](includes/d365fin_md.md)].

   Du kan også vælge at oprette en ny URL-adresse for webtjenesten i [!INCLUDE[d365fin](includes/d365fin_md.md)] ved at bruge handlingen **Opret datasæt** på siden **Webtjenester** ved hjælp af guiden Assisteret opsætning for **Konfigurer rapporteringsdata** eller ved at vælge handlingen **Rediger i Excel** på en af listerne.
6. Angiv de data, du vil føje til dine datamodel, og vælg derefter knappen **Indlæsning**.
7. Gentag fremgangsmåden for at føje flere [!INCLUDE[d365fin](includes/d365fin_md.md)]-data til dine Power BI-datamodel.

   **Bemærk**: Når du har oprettet forbindelse til [!INCLUDE[d365fin](includes/d365fin_md.md)], bliver du ikke igen spurgt om OData URL-adresse, brugernavn og adgangskode.

Når dataene er indlæst, vises de i den rigtige navigation på siden. Nu har du oprettet forbindelse til dine Dynamics 365-data og er klar til at opbygge din Power BI-rapport. Du kan finde flere oplysninger i [Power BI-dokumentationen](https://powerbi.microsoft.com/documentation/powerbi-landing-page/).

## <a name="see-also"></a>Se også
[Velkommen til [!INCLUDE[d365fin_long](includes/d365fin_long_md.md)]](index.md)  
[Importere forretningsdata fra andre økonomisystemer] (upload-data.md)  
[Konfigurere [!INCLUDE[d365fin](includes/d365fin_md.md)]](setup.md)  
[Finans](finance.md)  

