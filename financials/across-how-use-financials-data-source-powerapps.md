---
title: Bruge dine data til at oprette en app | Microsoft Docs
description: "Du kan gøre dine Financials-data tilgængelige som datakilde og angive en OData URL-adresse til dine webtjenester for at oprette en forretningsapp ved hjælp af PowerApps."
services: project-madeira
documentationcenter: 
author: edupont04
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: Odata, Power App, SOAP
ms.date: 06/02/2017
ms.author: edupont
ms.translationtype: Human Translation
ms.sourcegitcommit: 81636fc2e661bd9b07c54da1cd5d0d27e30d01a2
ms.openlocfilehash: e41a704d3a94abfb58d9547648f0eee46a8ed9b4
ms.contentlocale: da-dk
ms.lasthandoff: 07/07/2017


---
# <a name="connecting-to-your-financials-data-to-build-a-business-app-using-powerapps"></a>Oprette forbindelse til dine Financials-data for at oprette en forretningsapp ved hjælp af PowerApps
Du kan gøre dine [!INCLUDE[d365fin](includes/d365fin_md.md)]-data tilgængelige som en datakilde i PowerApps.  

> [!NOTE]  
>   Du skal have en gyldig konto til [!INCLUDE[d365fin](includes/d365fin_md.md)] og til PowerApps.  

## <a name="to-add-included365finincludesd365finmdmd-as-a-data-source-in-powerapps"></a>Sådan tilføjes [!INCLUDE[d365fin](includes/d365fin_md.md)] som en datakilde i PowerApps
1. Gå til [powerapps.microsoft.com](https://powerapps.microsoft.com/en-us/) i din webbrowser, og log på.
2. Vælg **Ny app** i den venstre navigationsrude.
3. Vælg din editor, PowerApps Studio til Windows eller PowerApps Studio til web.

   PowerApps Studio til Windows er et skrivebordsprogram, der bruges til at oprette og publicere PowerApps. PowerApps Studio til web er onlineløsningen, der bruges til at oprette og publicere PowerApps.
4. Næste trin til oprettelse af en PowerApp er at vælge dataene. Vælg ikonet med pilen, og vælg derefter indstillingen **Ny forbindelse** øverst til venstre side på siden.
5. Vælg **Dynamics 365 for Financials** på listen over tilgængelige forbindelser.
6. PowerApps viser en forbindelsesside, hvor du bliver bedt om de oplysninger, der kræves for at oprette forbindelse til dine [!INCLUDE[d365fin](includes/d365fin_md.md)]-data. Hvis du vil oprette forbindelse, skal du angive en OData URL-adresse, brugernavn, adgangskode og firmanavn.

   For *OData URL-adressen* kan du kopiere OData V4 URL-adressen på en af de webtjenester, der er angivet på siden **Webtjeneste** i [!INCLUDE[d365fin](includes/d365fin_md.md)], f.eks. `https://mycompany.financials.dynamics.com:7048/MS/ODataV4/`.  

   Som *Virksomhedsnavn* skal du bruge det navn, der vises i feltet **Navn** i vinduet **Virksomhedsoplysninger** vindue i [!INCLUDE[d365fin](includes/d365fin_md.md)]. Hvis din [!INCLUDE[d365fin](includes/d365fin_md.md)]-version indeholder flere virksomheder, skal du vælge det relevante virksomhedsnavn på listen i vinduet **Virksomheder**. I begge tilfælde skal du sørge for, at det navn, du angiver i guiden PowerApps, er nøjagtigt det samme som den tekst, der vises i [!INCLUDE[d365fin](includes/d365fin_md.md)], f.eks. `My Company`.

   Som brugernavn og adgangskode skal du bruge navnet og webserviceadgangsnøglen, der er angivet for din konto i vinduet **Brugere** i [!INCLUDE[d365fin](includes/d365fin_md.md)]. Dit brugernavn er f.eks. *Administrator*, og den webtjenesteadgangsnøgle, der fungerer som din adgangskode, er *EgzeUFQ9Uv0o5O0lUMyqCzo1ueUW9yRF3SsLU =*.
7. Vælg knappen **Forbindelse** for at forsætte. PowerApps viser et standarddatasæt for [!INCLUDE[d365fin](includes/d365fin_md.md)]. Vælg **Standard**-datasættet.

   PowerApps viser en liste over tabeller, der er tilgængelige fra [!INCLUDE[d365fin](includes/d365fin_md.md)]. Disse tabeller, eller slutpunkter, repræsenterer de webtjenester, som du har publiceret fra [!INCLUDE[d365fin](includes/d365fin_md.md)].

   Du kan også vælge at oprette en ny URL-adresse for webtjenesten i [!INCLUDE[d365fin](includes/d365fin_md.md)] ved at bruge handlingen **Opret datasæt** på siden **Webtjenester** ved hjælp af guiden Assisteret opsætning for **Konfigurer rapporteringsdata** eller ved at vælge handlingen **Rediger i Excel** på en af listerne.
8. Vælg den tabel, du vil bruge til din PowerApp, og vælg derefter knappen **Opret forbindelse**.
9. Gentag fremgangsmåden for at føje flere [!INCLUDE[d365fin](includes/d365fin_md.md)]-data til dine Power BI-datamodel.

   > [!NOTE]  
>    Når du har oprettet forbindelse til [!INCLUDE[d365fin](includes/d365fin_md.md)], bliver du ikke igen spurgt om OData URL-adresse, brugernavn og adgangskode.

Nu har du oprettet forbindelse til dine Dynamics 365-data og er klar til at opbygge din PowerApp. Du kan finde flere oplysninger i [PowerApps-dokumentationen](https://powerapps.microsoft.com/tutorials/getting-started/).

## <a name="see-also"></a>Se også
[Velkommen til [!INCLUDE[d365fin_long](includes/d365fin_long_md.md)]](index.md)  
[Importere virksomhedsdata fra andre økonomisystemer](upload-data.md)  
[Opsætning af [!INCLUDE[d365fin](includes/d365fin_md.md)]](setup.md)  
[Finans](finance.md)  

