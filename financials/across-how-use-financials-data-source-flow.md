---
title: Forbinde dataene med Flow | Microsoft Docs
description: "Du kan gøre dine Financials-data tilgængelige som datakilde og angive en OData URL-adresse til dine webtjenester for at oprette et automatiseret workflow."
documentationcenter: 
author: edupont04
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: workflow, Odata, Power App, SOAP
ms.date: 01/25/2018
ms.author: solsen
ms.translationtype: HT
ms.sourcegitcommit: bec0619be0a65e3625759e13d2866ac615d7513c
ms.openlocfilehash: ef4d841723b6bb0af37695a8c3ed1d805319be78
ms.contentlocale: da-dk
ms.lasthandoff: 01/30/2018

---
# <a name="using-included365finincludesd365finmdmd-in-an-automated-workflow"></a>Bruge [!INCLUDE[d365fin](includes/d365fin_md.md)] i et automatisk workflow
Du kan bruge dine [!INCLUDE[d365fin](includes/d365fin_md.md)]-data som en del af en arbejdsproces i Microsoft Flow.  

> [!NOTE]  
>   Du skal have en gyldig konto til [!INCLUDE[d365fin](includes/d365fin_md.md)] og til Flow.  

## <a name="to-add-included365finincludesd365finmdmd-as-a-data-source-in-flow"></a>Sådan tilføjes [!INCLUDE[d365fin](includes/d365fin_md.md)] som en datakilde i Flow
1. Gå til [flow.microsoft.com](https://flow.microsoft.com/en-us/) i din webbrowser, og log på.
2. Vælg **Mine Flows** på båndet øverst på siden.
3. I vinduet **Mine Flows** skal du vælge indstillingen **Opret fra tom**.
4. På listen over tilgængelige udløsere, skal du vælge en af de [!INCLUDE[d365fin](includes/d365fin_md.md)]-udløsere, der er tilgængelige:  
    *Når en post oprettes*,  
    *Når en post slettes*,  
    *Når en post ændres*,  
    *Når der anmodes om godkendelse af en debitor*,  
    *Når der anmodes om godkendelse af en finanskladdekørsel*,  
    *Når der anmodes om godkendelse af en finanskladdelinje*,  
    *Når der anmodes om godkendelse af en vare*,  
    *Når der anmodes om godkendelse af et købsdokument*,  
    *Når der anmodes om godkendelse af et salgsdokument* eller  
    *Når der anmodes om godkendelse af en kreditor*.
5. Flow beder dig om de oplysninger, der kræves for at oprette forbindelse til dine [!INCLUDE[d365fin](includes/d365fin_md.md)]-data. Hvis du har valgt en af følgende udløsere: *Når en post oprettes*, *Når en post ændres*, eller *Når en post slettes*, skal du vælge en firmanavn og tabelnavn. Til andre udløsere er kun firmanavnet påkrævet for at oprette forbindelse.

   Flow viser en liste over regnskaber og tabeller, der er tilgængelige fra [!INCLUDE[d365fin](includes/d365fin_md.md)]. Disse tabeller, eller slutpunkter, repræsenterer de webtjenester, som du har publiceret fra [!INCLUDE[d365fin](includes/d365fin_md.md)].

   Du kan også vælge at oprette en ny URL-adresse for webtjenesten i [!INCLUDE[d365fin](includes/d365fin_md.md)] ved at bruge handlingen **Opret datasæt** på siden **Webtjenester** ved hjælp af guiden Assisteret opsætning for **Konfigurer rapporteringsdata** eller ved at vælge handlingen **Rediger i Excel** på en af listerne.

Nu har du oprettet forbindelse til dine data i Finance and Operations, Business edition og er klar til at opbygge dit flow. Du kan finde flere oplysninger i [Flow-dokumentationen](https://flow.microsoft.com/documentation/getting-started/).

For fejlfinding af Microsoft Flow skal du se [Fejlfinding af integration med Microsoft Flow](across-troubleshooting-how-use-financials-data-source-flow.md).

## <a name="see-also"></a>Se også
[Velkommen til [!INCLUDE[d365fin_long](includes/d365fin_long_md.md)]](index.md)  
[Importere virksomhedsdata fra andre økonomisystemer](upload-data.md)  
[Administrere brugere og deres rettigheder](ui-how-users-permissions.md)    
[Opsætning af [!INCLUDE[d365fin](includes/d365fin_md.md)]](setup.md)  
[Finans](finance.md)  

