---
title: Arbejde med styklister for at styre komponenter | Microsoft Docs
description: "Du opretter en montagestykliste for at angive de komponenter eller ressourcer, der kræves for at sammensætte den vare, som montagestyklisten repræsenterer, og du kan få vist komponenterne for et montageelement."
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.date: 05/06/2017
ms.author: sgroespe
ms.translationtype: Human Translation
ms.sourcegitcommit: 81636fc2e661bd9b07c54da1cd5d0d27e30d01a2
ms.openlocfilehash: e6aef60ee5b206b0ae978f72b92e6f8778290509
ms.contentlocale: da-dk
ms.lasthandoff: 07/07/2017


---
# <a name="how-to-work-with-bills-of-material"></a>Fremgangsmåde: Arbejde med styklister
> [!NOTE]  
>   Den aktuelle version af [!INCLUDE[d365fin](includes/d365fin_md.md)] indeholder kun den første del af funktionen Montagestyring. Indtil videre kan du kun oprette montagestyklister og håndtere de relaterede overordnede varer som almindelige varer. Med en senere opdatering kan du styre den egentlige montage af varer fra komponenter, enten i montage til lager- eller montage til ordre-flows, og du kan sælge komponenter som pakker.

Du bruger styklister til at strukturere overordnede varer, du sælger som pakker, der består af den overordnede vares komponenter eller af montage til ordre- eller montage til lager-pakker.

I [!INCLUDE[d365fin](includes/d365fin_md.md)] kaldes en stykliste en "montagestykliste". Montagestyklister angiver, hvilke komponenter der er indeholdt i overordnede varer. En overordnet vare omtales som et "montageelement" i denne dokumentation.

Montagestyklister indeholder normalt varer, men kan også indeholde en eller flere ressourcer, der er påkrævet for at sammensætte montageelementet.

Montagestyklister kan have flere niveauer, hvilket betyder, at en komponent på montagestyklisten selv kan være et montageelement. I så fald skal feltet **Montagestykliste** på montagestyklistelinjen vise **Ja**.

Der gælder særlige krav for elementerne på montagestyklister for så vidt angår varedisponering. Du kan finde flere oplysninger i afsnittet "Sådan får du vist tilgængeligheden af en vare via brugen af den i montagestyklister" i [Sådan gør du: Vise varedisponering](inventory-how-availability-overview.md).

> [!NOTE]  
>   Denne funktion kræver, at oplevelsen er indstillet til **Pakke**. Du kan finde flere oplysninger under [Tilpasse din Financials-oplevelse](ui-experiences.md).

## <a name="to-create-an-assembly-bom"></a>Sådan oprettes en montagestykliste
For at definere en overordnet vare, der består af andre elementer og potentielt af ressourcer, der kræves for at sammensætte den overordnede vare, skal du oprette en montagestykliste.  

Montagestyklister oprettes ad to omgange:
- Oprette en ny vare
- Angive montageelementets styklistestruktur.

1. Opret en ny vare. Du kan finde flere oplysninger under [Fremgangsmåde: Registrere nye varer](inventory-how-register-new-items.md).

    Fortsæt med at angive komponenter eller ressourcer på montagestyklisten.  
2. I vinduet **Varekort** for et montageelement skal du vælge handlingen **Montage** og derefter vælge handlingen **Montagestykliste**.
3. I vinduet **Montagestykliste** skal du udfylde felterne efter behov. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

## <a name="to-view-the-components-of-an-assembly-item-indented-according-to-the-bom-structure"></a>Sådan får du vist komponenterne for et montageelement indrykket i overensstemmelse med styklistestrukturen
Fra vinduet **Montagestykliste** kan du åbne et separat vindue, der viser komponenterne og evt. ressourcer, der er indrykket i henhold til deres placering på styklisten under montageelementet.

1. Vælg ikonet ![Søg efter side eller rapport](media/ui-search/search_small.png "Ikonet Søg efter side eller rapport"), angiv **Varer**, og vælg derefter det relaterede link.
2. Åbn kortet for et montageelement. (Feltet **Montagestykliste** i vinduet **Varer** indeholder **Ja**).
3. I vinduet **Varekort** skal du vælge handlingen **Montage** og derefter vælge handlingen **Montagestykliste**.
4. I vinduet **Montagestykliste** skal du vælge handlingen **Vis stykliste**.

## <a name="to-buy-sell-or-transfer-assembly-items"></a>Sådan køber, sælger eller overfører du montageelementer
Da den aktuelle version af [!INCLUDE[d365fin](includes/d365fin_md.md)] kun giver mulighed for at definere og tildele montagestyklister til varer, kan du kun håndtere montageelementer på dokumentlinjer som almindelige varer.

**Advarsel!** Lagerantallet for styklistekomponenter reguleres ikke, hvis du gør dette.

## <a name="see-also"></a>Se også
[Fremgangsmåde: Registrere nye varer](inventory-how-register-new-items.md)  
[Sådan gør du: Vise varedisponering](inventory-how-availability-overview.md)     
[Lagerbeholdning](inventory-manage-inventory.md)  
[Arbejde med [!INCLUDE[d365fin_long](includes/d365fin_long_md.md)]](ui-work-product.md)

