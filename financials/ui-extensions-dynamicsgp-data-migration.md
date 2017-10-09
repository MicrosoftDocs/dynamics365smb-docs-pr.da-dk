---
title: "Overførsel af data fra Dynamics GP med udvidelsen Dataoverførsel | Microsoft Docs"
description: "Du kan bruge udvidelsen Dataoverførsel i Dynamics GP til at overføre debitorer, kreditorer, lagervarer og konti fra Dynamics GP til Dynamics 365 for Financials."
documentationcenter: 
author: edupont04
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms. search.keywords: app, add-in, manifest, customize, import, implement
ms.date: 03/29/2017
ms.author: edupont
ms.translationtype: HT
ms.sourcegitcommit: 81636fc2e661bd9b07c54da1cd5d0d27e30d01a2
ms.openlocfilehash: 31b698aea884da162cc18f16a912ebd57e35aed9
ms.contentlocale: da-dk
ms.lasthandoff: 09/22/2017

---
# <a name="the-dynamics-gp-data-migration-extension-for-dynamics-365-for-financials"></a>Udvidelsen Overførsel af data med Dynamics GP til Dynamics 365 for Financials
Denne udvidelse gør det nemt at overføre debitorer, kreditorer, lagervarer og konti fra Dynamics GP til [!INCLUDE[d365fin](includes/d365fin_md.md)]. Hvis din virksomhed bruger Dynamics GP i dag, kan du eksportere de relevante stamdataposter og derefter åbne en assisteret opsætningsvejledning for at tilføje dataene i [!INCLUDE[d365fin](includes/d365fin_md.md)]. Du kan finde flere oplysninger under [Overføre virksomhedsdata fra andre økonomisystemer](upload-data.md).

## <a name="exporting-data-from-dynamics-gp"></a>Eksportere data fra Dynamics GP
Du skal have eksporteret nogle af eller alle dine eksisterende debitorer, kreditorer, lagervarer og konti til en fil ved hjælp af funktionen til dataeksport i Dynamics GP. I forbindelse med [!INCLUDE[d365fin](includes/d365fin_md.md)] kan du eksportere følgende datatyper:

* Konto  
* Kunde  
* Vare  
* Kreditor  

Udvidelsen til overførsel af data til Dynamics GP tilknyttes automatisk de udlæste data, så dataene hurtigt er tilgængelige i det nye regnskab i [!INCLUDE[d365fin](includes/d365fin_md.md)]. Under processen oprettes understøttende opsætningsoplysninger som f.eks. bogføringsgrupper. Lagervarer overføres til systemet med FIFO som omkostningsevalueringsmetoden. Konti oprettes som hovedkontosegmentet fra Dynamics GP med dimensioner, fordi [!INCLUDE[d365fin](includes/d365fin_long_md.md)] ikke har kontosegmenter.

## <a name="see-also"></a>Se også
[Importere virksomhedsdata fra andre økonomisystemer](upload-data.md)  
[Tilpasse [!INCLUDE[d365fin](includes/d365fin_md.md)] ved hjælp af udvidelser ](ui-extensions.md)  

