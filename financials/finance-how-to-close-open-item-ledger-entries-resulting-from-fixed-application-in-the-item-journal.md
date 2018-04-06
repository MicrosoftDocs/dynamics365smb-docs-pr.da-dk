---
title: "Sådan lukker du åbne vareposter, der fremkommer ved fast udligning i varekladden | Microsoft Docs"
description: "Du kan bruge feltet **Udlign fra-post** i vinduet **Varekladde** for at oprette en fast udligning mellem en indgående transaktion og den oprindelige udgående transaktion. For eksempel for at rette den udgående transaktion eller behandle dens returvare."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 08/09/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: bec0619be0a65e3625759e13d2866ac615d7513c
ms.openlocfilehash: 1553b5f85cd9f00f9de15b59bcf258fba412967b
ms.contentlocale: da-dk
ms.lasthandoff: 03/22/2018

---
# <a name="close-open-item-ledger-entries-resulting-from-fixed-application-in-the-item-journal"></a>Lukke åbne vareposter, der fremkommer ved fast udligning i varekladden
Du kan bruge feltet **Udlign fra-post** i vinduet **Varekladde** for at oprette en fast udligning mellem en indgående transaktion og den oprindelige udgående transaktion. For eksempel for at rette den udgående transaktion eller behandle dens returvare. Du kan finde flere oplysninger i Udlign fra-post.  

> [!IMPORTANT]  
>  Faste udligninger, der er foretaget på denne måde, gælder kun omkostningen, ikke mængden. Derfor lukker den bogførte positive varepost ikke den udlignede udgående post og vil selv forblive åben. Dette gælder også, når du bogfører en fast udligning for en positiv post til en negativ post, der ikke er lukket ved en almindelig positiv post, derefter forbliver både den negative og den positive post åben.  
>   
>  Det betyder også, at du ikke kan lukke en lagerperiode, hvis der findes en sådan post.  

Følgende procedure viser, hvordan du kan lukke disse poster ved at udføre to korrigerende bogføringer i varekladden.  

## <a name="to-close-open-item-ledger-entries-that-result-from-a-fixed-application-in-the-item-journal"></a>Sådan lukkes åbne vareposter, der fremkommer ved fast udligning i varekladden  

1.  Brug feltet **Udlign fra-post** for at bogføre en positiv regulering med den tilsvarende mængde. Den oprindelige negative post med fast udligning lukkes.  
2.  Brug feltet **Udlign.postløbenr.** for at bogføre en negativ regulering. Den oprindelige positive rettelsespost med fast udligning lukkes.  

## <a name="see-also"></a>Se også  
[Fjerne og genanvende vareposter](finance-how-to-remove-and-reapply-item-entries.md)  
 [Behandle salgsreturvarer og annulleringer](sales-how-process-sales-returns-cancellations.md)   
 [Opsætte lagerværdi og kostprisberegning](finance-set-up-inventory-valuation-and-costing.md)   
 [Administrere lageromkostninger](finance-manage-inventory-costs.md)   
 [Designoplysninger: Kostmetoder](design-details-costing-methods.md)

