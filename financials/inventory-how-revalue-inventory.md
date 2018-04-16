---
title: "Oprette nye værdiposter for varer i lagerbeholdningen | Microsoft Docs"
description: "Beskriver, hvordan værdiposterne for en eller flere varer på lageret kan op- eller nedskrives ved at bogføre deres aktuelle, beregnede værdi."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: costing, inventory cost, value entries
ms.date: 08/07/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: bec0619be0a65e3625759e13d2866ac615d7513c
ms.openlocfilehash: 8460dac8478fa101a255d93110578fa9ea20516f
ms.contentlocale: da-dk
ms.lasthandoff: 03/22/2018

---
# <a name="revalue-inventory"></a>Regulere lagerbeholdning
Hvis du vil op- eller nedskrive en vare eller en bestemt varepost, skal du bruge reguleringskladden.

## <a name="to-revalue-inventory"></a>Sådan reguleres lagerbeholdningen
1. Vælg ikonet ![Søg efter side eller rapport](media/ui-search/search_small.png "Ikonet Søg efter side eller rapport"), angiv **Værdireguleringskladde**, og vælg derefter det relaterede link.
2. Vælg handlingen **Beregn lagerværdi**.
3. I vinduet **Beregn lagerværdi** skal du udfylde felterne efter behov. [!INCLUDE [tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
4. Vælg knappen **OK**.
5. Angiv den nye kostpris på hver linje i vinduet **Værdireguleringskladde** i feltet **Kostpris (reguleret)**. Eller du kan i stedet angive det nye, samlede beløb i feltet **Lagerværdi (reguleret)**.

    De relevante felter opdateres automatisk. Bemærk, at feltet **Beløb** indeholder den faktiske ændring i lagerværdien for den valgte varepost. Det er differencen mellem feltet **Lagerværdi (beregnet)** og feltet **Lagerværdi (reguleret)**, der beregnes.
6. Når du har udfyldt alle linjerne i reguleringskladden, skal du vælge handlingen **Bogfør**.

Nye værdiposter oprettes nu for at afspejle de værdireguleringer, du har bogført. Du kan se de nye værdier på de respektive varekort.

## <a name="see-also"></a>Se også
[Designoplysninger: Regulering](design-details-revaluation.md)  
[Lagerbeholdning](inventory-manage-inventory.md)  
[Salg](sales-manage-sales.md)  
[Køb](purchasing-manage-purchasing.md)  
[Arbejde med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

