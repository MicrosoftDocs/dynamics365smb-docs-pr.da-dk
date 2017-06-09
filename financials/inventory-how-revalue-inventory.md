---
title: "Fremgangsmåde: Regulere lagerbeholdningen | Microsoft Docs"
description: "Beskriver, hvordan værdien af en eller flere varer på lageret kan op- eller nedskrives ved at bogføre deres aktuelle, beregnede værdi."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: costing, inventory cost, value entries
ms.date: 03/28/2017
ms.author: sgroespe
ms.translationtype: Human Translation
ms.sourcegitcommit: a31be0f9d07e2abb591e26f6bae34c6f6e4dcda6
ms.openlocfilehash: 0f7137b3ac4e2c68c1c9a9b94b3ba73e0438a4a9
ms.contentlocale: da-dk
ms.lasthandoff: 05/04/2017


---
# <a name="how-to-revalue-inventory"></a>Fremgangsmåde: Regulere lagerbeholdningen
Hvis du vil op- eller nedskrive en vare eller en bestemt varepost, skal du bruge reguleringskladden.

## <a name="to-revalue-inventory"></a>Sådan reguleres lagerbeholdningen
1. I øverste højre hjørne skal du vælge ikonet **Søg efter side eller rapport** ![Søg efter side eller rapport](media/ui-search/search_small.png "Ikonet Søg efter side eller rapport"), angive **Værdireguleringskladde** og derefter vælge det relaterede link.
2. Vælg handlingen **Beregn lagerværdi**.
3. I vinduet **Beregn lagerværdi** skal du udfylde felterne efter behov. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
4. Vælg knappen **OK**.
5. Angiv den nye kostpris på hver linje i vinduet **Værdireguleringskladde** i feltet **Kostpris (reguleret)**. Eller du kan i stedet angive det nye, samlede beløb i feltet **Lagerværdi (reguleret)**.

    De relevante felter opdateres automatisk. Bemærk, at feltet **Beløb** indeholder den faktiske ændring i lagerværdien for den valgte varepost. Det er differencen mellem feltet **Lagerværdi (beregnet)** og feltet **Lagerværdi (reguleret)**, der beregnes.
6. Når du har udfyldt alle linjerne i reguleringskladden, skal du vælge handlingen **Bogfør**.

Nye værdiposter oprettes nu for at afspejle de værdireguleringer, du har bogført. Du kan se de nye værdier på de respektive varekort.

## <a name="see-also"></a>Se også
[Lagerbeholdning](inventory-manage-inventory.md)  
[Salg](sales-manage-sales.md)  
[Køb](purchasing-manage-purchasing.md)  
[Arbejde med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

