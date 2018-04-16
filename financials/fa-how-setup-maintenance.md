---
title: "Definere anlægsvedligeholdelse | Microsoft Docs"
description: "For at kunne administrere reparation og service af anlæg skal du angive generelle vedligeholdelsesoplysninger, koder for typen af arbejde og en bogføringskonto for omkostninger."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: repair, service
ms.date: 06/02/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: bec0619be0a65e3625759e13d2866ac615d7513c
ms.openlocfilehash: 7ae4abacf22d3610194ea56bbaa997390cb7df0a
ms.contentlocale: da-dk
ms.lasthandoff: 03/22/2018

---
# <a name="set-up-fixed-asset-maintenance"></a>Definere anlægsreparation
For at administrere vedligeholdelse af anlæg, skal du først angive nogle generelle reparationsoplysninger, en bogføringskonto for reparationsomkostninger og reparationskoder for forskellige typer arbejde, f.eks rutineeftersyn eller reparation.

## <a name="to-set-up-general-maintenance-information"></a>Sådan angives generelle reparationsoplysninger
Hvis du definerer felterne til reparation, kan du bogføre reparationsudgifter fra anlægskladden.

1. Vælg ikonet ![Søg efter side eller rapport](media/ui-search/search_small.png "Ikonet Søg efter side eller rapport"), angiv **Anlægsaktiver**, og vælg derefter det relaterede link.
2. Vælg det anlægsaktiv, du vil definere forsikringsdækning for, og vælg derefter handlingen **Rediger**.
3. Udfyld felterne efter behov i oversigtspanelet **Reparation**. [!INCLUDE [tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

## <a name="to-set-up-maintenance-codes"></a>Sådan defineres reparationskoder
Når du bogfører reparationsudgifter fra en kassekladde, skal du udfylde feltet **Reparationskode** for at registrere, hvilken slags reparation der er blevet udført, f.eks. rutineeftersyn eller reparation.

1. Vælg ikonet ![Søg efter side eller rapport](media/ui-search/search_small.png "Ikonet Søg efter side eller rapport"), angiv **Reparation**, og vælg derefter det relaterede link.
2. I feltet **Reparation** skal du oprette koder for de forskellige typer reparationsarbejde.

## <a name="to-set-up-maintenance-expense-accounts"></a>Sådan defineres reparationskonti
Hvis du vil bogføre reparationsudgifter, skal du først angive et kontonummer i vinduet **Anlægsbogføringsgrupper**.

1. Vælg ikonet ![Søg efter side eller rapport](media/ui-search/search_small.png "Ikonet Søg efter side eller rapport"), angiv **Anlægsbogføringsgrupper**, og vælg derefter det relaterede link.
2. Udfyld feltet **Reparationskonto** for hver enkelt bogføringsgruppe.

> [!NOTE]  
>   Hvis du angive, at reparationsomkostningerne skal allokeres til afdelinger eller projekter, skal du definere allokeringsnøgler. Du kan finde flere oplysninger i [Angive generelle funktioner for anlægsaktiver](fa-how-setup-general.md).

## <a name="see-also"></a>Se også
[Opsætning af anlægsaktiver](fa-setup.md)  
[Anlægsaktiver](fa-manage.md)  
[Finans](finance.md)  
[Velkommen til [!INCLUDE[d365fin_long](includes/d365fin_long_md.md)]](index.md)  
[Arbejde med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

