---
title: Definere anlægsvedligeholdelse | Microsoft Docs
description: For at kunne administrere reparation og service af anlæg skal du angive generelle vedligeholdelsesoplysninger, koder for typen af arbejde og en bogføringskonto for omkostninger.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: repair, service
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: b9077224f4a0b0344b565c55dcfb14db1e90722c
ms.sourcegitcommit: ff2b55b7e790447e0c1fcd5c2ec7f7610338ebaa
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 02/15/2021
ms.locfileid: "5380148"
---
# <a name="set-up-fixed-asset-maintenance"></a>Definere anlægsreparation
For at administrere vedligeholdelse af anlæg, skal du først angive nogle generelle reparationsoplysninger, en bogføringskonto for reparationsomkostninger og reparationskoder for forskellige typer arbejde, f.eks rutineeftersyn eller reparation.

## <a name="to-set-up-general-maintenance-information"></a>Sådan angives generelle reparationsoplysninger
Hvis du definerer felterne til reparation, kan du bogføre reparationsudgifter fra anlægskladden.

1. Vælg ikonet ![Elpære, der åbner funktionen Fortæl mig](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig"), angiv **Anlæg**, og vælg derefter det relaterede link.
2. Vælg det anlægsaktiv, du vil definere forsikringsdækning for, og vælg derefter handlingen **Rediger**.
3. Udfyld felterne efter behov i oversigtspanelet **Reparation**. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

## <a name="to-set-up-maintenance-codes"></a>Sådan defineres reparationskoder
Når du bogfører reparationsudgifter fra en kassekladde, skal du udfylde feltet **Reparationskode** for at registrere, hvilken slags reparation der er blevet udført, f.eks. rutineeftersyn eller reparation.

1. Vælg ikonet ![Elpære, der åbner funktionen Fortæl mig](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig"), angiv **Reparation**, og vælg derefter det relaterede link.
2. På siden **Reparation** skal du oprette koder for de forskellige typer reparationsarbejde.

## <a name="to-set-up-maintenance-expense-accounts"></a>Sådan defineres reparationskonti
Hvis du vil bogføre reparationsudgifter, skal du først angive et kontonummer på siden **Anlægsbogføringsgrupper**.

1. Vælg ikonet ![Elpære, der åbner funktionen Fortæl mig](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig"), angiv **Anlægsbogføringsgrupper**, og vælg derefter det relaterede link.
2. Udfyld feltet **Reparationskonto** for hver enkelt bogføringsgruppe.

> [!NOTE]  
>   Hvis du angive, at reparationsomkostningerne skal allokeres til afdelinger eller projekter, skal du definere allokeringsnøgler. Du kan finde flere oplysninger i [Angive generelle funktioner for anlægsaktiver](fa-how-setup-general.md).

## <a name="see-also"></a>Se også
[Opsætning af Anlægsaktiver](fa-setup.md)  
[Anlægsaktiver](fa-manage.md)  
[Finans](finance.md)  
[Introduktion](product-get-started.md)  
[Arbejde med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]