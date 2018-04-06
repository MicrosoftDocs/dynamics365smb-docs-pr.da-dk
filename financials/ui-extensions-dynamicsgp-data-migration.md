---
title: "Overførsel af data fra Dynamics GP med udvidelsen Dataoverførsel | Microsoft Docs"
description: "Du kan bruge udvidelsen Dataoverførsel i Dynamics GP til at overføre debitorer, kreditorer, lagervarer og konti fra Dynamics GP til Finance and Operations, Business edition."
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
ms.sourcegitcommit: bec0619be0a65e3625759e13d2866ac615d7513c
ms.openlocfilehash: bfd3ca3e28b6eb3efa2a16cc131b508db6bd1590
ms.contentlocale: da-dk
ms.lasthandoff: 03/22/2018

---
# <a name="the-dynamics-gp-data-migration-extension-for-finance-and-operations-business-edition"></a>Udvidelsen Dynamics GP-dataoverførsel til Finance and Operations, Business edition 
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
[Tilpasse [!INCLUDE[d365fin](includes/d365fin_md.md)] ved hjælp af udvidelser](ui-extensions.md)  

