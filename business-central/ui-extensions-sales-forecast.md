---
title: Bruge udvidelsen Salgs- og lagerprognose til at styre lagerbeholdningen | Microsoft Docs
description: "Udvidelsen hjælper dig med at forudse salg, få et klart billede af forventede lagermangler og oprette genbestillingsanmodninger til kreditorer."
services: project-madeira
documentationcenter: 
author: edupont04
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms. search.keywords: app, add-in, manifest, customize, budget
ms.date: 03/29/2017
ms.author: edupont
ms.translationtype: HT
ms.sourcegitcommit: d7fb34e1c9428a64c71ff47be8bcff174649c00d
ms.openlocfilehash: edddda48fe91ed2e31b9c709a546730ce50dc6d4
ms.contentlocale: da-dk
ms.lasthandoff: 03/22/2018

---
# <a name="sales-and-inventory-forecast-for-business-central"></a>Salgs- og lagerprognose til Business Central 
Lagerstyring håndterer balancen mellem kundeservice og styring af omkostningerne. På én side kræver et lille lager mindre driftskapital, men på den anden side kan manglende lager medføre tabt salg. Udvidelsen Salgs- og lagerprognose forudsiger muligt salg ved hjælp af historiske data og giver et klart overblik over forbruget af lageret. Baseret på prognosen hjælper udvidelsen med at oprette genbestillingsanmodninger til dine leverandører og sparer tid.  

## <a name="setting-up-forecasting"></a>Konfigurere prognose
I [!INCLUDE[d365fin](includes/d365fin_md.md)] er forbindelsen til [Cortana Intelligence](https://www.microsoft.com/en-us/cloud-platform/what-is-cortana-intelligence-suite) allerede konfigureret for dig. Du kan dog konfigurere en prognose, hvis du vil bruge en anden type periode i rapporten, f.eks hvis du vil skifte fra prognose pr. måned til prognose pr. kvartal. Du kan også vælge, hvor mange perioder prognosen skal beregnes for, afhængigt af hvor detaljeret prognosen skal være. Vi anbefaler prognose pr. måned og en horisont på 12 måneder for prognosen.  

## <a name="using-the-forecasts"></a>Brug af prognoser
Udvidelsen bruger Cortana Intelligence til at forudse fremtidigt salg ud fra din salgsoversigt, så du bedre kan undgå manglende lager. Når du f.eks. vælger en vare i vinduet **Varer** , og diagrammet i ruden **Vareprognose** viser det anslåede salg af varen i den kommende periode. På denne måde kan du se, om du sandsynligvis vil løbe tør for lager inden længe.  

Du kan også bruge udvidelsen til at foreslå, hvornår lageret skal øges. Hvis du f.eks. opretter en købsordre for Fabrikam, fordi du vil købe deres nye skrivebordsstol, vil udvidelsen Salgs- og lagerprognose foreslå, at du også øger lageret af LONDON-drejestolen, som du normalt køber hos denne leverandør. Det skyldes, at udvidelsen forudser, at lageret af LONDON-drejestolen vil løbe tørt i de kommende to måneder, så du med fordel kan bestille flere stole allerede nu.  

## <a name="see-also"></a>Se også
[Salg](sales-manage-sales.md)  
[Lagerbeholdning](inventory-manage-inventory.md)  
[Tilpasse [!INCLUDE[d365fin](includes/d365fin_md.md)] ved hjælp af udvidelser](ui-extensions.md)  

