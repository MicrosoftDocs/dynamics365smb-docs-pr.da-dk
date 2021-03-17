---
title: Lukke vareposter, der stammer fra brug af fast udligning.
description: Se, hvordan du kan oprette en fast udligning mellem en indgående transaktion og den oprindelige udgående transaktion i varekladden.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 01/14/2020
ms.author: edupont
ms.openlocfilehash: 9aa24653d4ae957ff741e85a99c13e0c9a8f7173
ms.sourcegitcommit: ff2b55b7e790447e0c1fcd5c2ec7f7610338ebaa
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 02/15/2021
ms.locfileid: "5381952"
---
# <a name="close-open-item-ledger-entries-resulting-from-fixed-application-in-the-item-journal"></a>Lukke åbne vareposter, der fremkommer ved fast udligning i varekladden

Du kan bruge feltet **Udlign fra-post** på siden **Varekladde** for at oprette en fast udligning mellem en indgående transaktion og den oprindelige udgående transaktion. For eksempel for at rette den udgående transaktion eller behandle dens returvare.  

> [!IMPORTANT]  
> Faste udligninger, der er foretaget på denne måde, gælder kun omkostningen, ikke mængden. Derfor lukker den bogførte positive varepost ikke den udlignede udgående post og vil selv forblive åben. Dette gælder også, når du bogfører en fast udligning for en positiv post til en negativ post, der ikke er lukket ved en almindelig positiv post, derefter forbliver både den negative og den positive post åben.  
>
> Det betyder også, at du ikke kan lukke en lagerperiode, hvis der findes en sådan post.  

Du kan ændre og genanvende udligningsposter under visse betingelser ved hjælp af siden **Applikationskladde**.  

Følgende procedure viser, hvordan du kan lukke disse poster ved at udføre to korrigerende bogføringer i varekladden.  

## <a name="to-close-open-item-ledger-entries-that-result-from-a-fixed-application-in-the-item-journal"></a>Sådan lukkes åbne vareposter, der fremkommer ved fast udligning i varekladden  

1. Brug feltet **Udlign fra-post** for at bogføre en positiv regulering med den tilsvarende mængde. Den oprindelige negative post med fast udligning lukkes.  

    Feltet **Udlign fra post** angiver antallet af udgående vareposter, hvis omkostninger videresendes til den indgående varepost, når du bogfører en indgående transaktion af typen **Opregulering** eller **Køb** med varekladden.  
2. Brug feltet **Udlign.postløbenr.** for at bogføre en negativ regulering. Den oprindelige positive rettelsespost med fast udligning lukkes.  

    Feltet **Udligningspostløbenr.** angiver, om antallet på varekladdelinjen skal udlignes med et bilag, der allerede er bogført. Hvis det er tilfældet, skal du angiver det løbenummer på vareposten, som varekladdelinjen skal udlignes med.

## <a name="see-also"></a>Se også

[Fjerne og genanvende vareposter](finance-how-to-remove-and-reapply-item-entries.md)  
[Behandle salgsreturvarer og annulleringer](sales-how-process-sales-returns-cancellations.md)  
[Opsætte lagerværdi og kostprisberegning](finance-set-up-inventory-valuation-and-costing.md)  
[Administrere lageromkostninger](finance-manage-inventory-costs.md)  
[Designoplysninger: Kostmetoder](design-details-costing-methods.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]