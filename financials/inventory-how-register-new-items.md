---
title: "Fremgangsmåde: Registrere nye varer | Microsoft Docs"
description: "Opret kort for nye fysiske produkter, som du sælger fra lageret, f.eks. stk., eller som du sælger som timer."
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: item, finished good, component, raw material, assembly item
ms.date: 03/28/2017
ms.author: sgroespe
ms.translationtype: Human Translation
ms.sourcegitcommit: a31be0f9d07e2abb591e26f6bae34c6f6e4dcda6
ms.openlocfilehash: 582e006291e51e19d80304d24ae055ce6ac8d698
ms.contentlocale: da-dk
ms.lasthandoff: 05/04/2017


---
# <a name="how-to-register-new-items"></a>Fremgangsmåde: Registrere nye varer
Varer er, blandt andre produkter, grundlaget for din virksomhed og de varer eller tjenester, som du handler med. Hver vare skal registreres som et varekort.

Varekort indeholder de oplysninger, der kræves for at købe, opbevare, sælge, levere og føre regnskab med varer.

Varekortet kan være af typen **Lager** eller **Service** for at angive, om varen er en fysisk enhed eller en arbejdstidsenhed. Bortset fra visse felter, der vedrører de fysiske aspekter af en vare, fungerer alle felter på et varekort på samme måde for lagervarer og tjenester. Du kan finde flere oplysninger om salg af en vare under [Fremgangsmåde: Sælge produkter](sales-how-sell-products.md) eller [Fremgangsmåde: Fakturere salg](sales-how-invoice-sales.md).

En vare kan struktureres som en overordnet vare med underliggende underordnede varer på en stykliste. I [!INCLUDE[d365fin](includes/d365fin_md.md)] kaldes en stykliste en "montagestykliste". Du bruger montagestyklister til at strukturere overordnede varer, du sælger som pakker, der består af den overordnede vares komponenter eller af montage til ordre- eller montage til lager-pakker. Du kan finde flere oplysninger under [Fremgangsmåde: Arbejde med styklister](inventory-how-work-BOMs.md).

**Bemærk**: Hvis der er en vareskabelon til forskellige varetyper, vises der et vindue, når du opretter et nyt varekort, hvorfra du kan vælge en passende skabelon. Hvis der kun er én vareskabelon, bruger nye varekort altid denne skabelon.

## <a name="to-create-a-new-item-card"></a>Sådan oprettes et nyt varekort
1. På startsiden skal du vælge handlingen **Varer** for at åbne oversigten over eksisterende varer.  
2. I vinduet **Varer** skal du vælge handlingen **Ny**.

    Hvis der kun er én vareskabelon, åbnes nye varekort med nogle felter, der er udfyldt med oplysninger fra denne skabelon.
3. I vinduet **Vælg en skabelon til en ny vare** skal du vælge den skabelon, som du vil bruge til det nye varekort.
4. Vælg knappen **OK**. Et nyt varekort åbnes med nogle felter udfyldt med oplysninger fra skabelonen.
5. Fortsæt med at udfylde eller ændre felterne på varekortet efter behov. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

I oversigtspanelet **Pris og bogføring** kan du se specialpriser eller rabatter, som du tildeler til varen, hvis bestemte kriterier opfyldes, f.eks. debitor, mindste ordrestørrelse eller slutdato. Hver række repræsenterer en specialpris- eller en linjerabat. Hver kolonne repræsenterer et kriterium, der skal anvendes for at garantere den specialpris, du angiver i feltet **Enhedspris** eller den linjerabat, som du angiver i feltet **Linjerabatpct.** Du kan finde flere oplysninger under [Registrere salgspris, rabat og betalingsaftaler](sales-how-record-sales-price-discount-payment-agreements.md).

Varen er nu registreret, og varekortet er klar til at blive brugt i købs- og salgsdokumenter.

Hvis du vil bruge dette varekort som skabelon, når du opretter nye varekort, kan du gemme det som en skabelon. Du kan finde flere oplysninger i følgende afsnit.

## <a name="to-save-the-item-card-as-a-template"></a>Sådan gemmes varekortet som en skabelon
1. I vinduet **Varekort** skal du vælge handlingen **Gem som skabelon**. Vinduet **Vareskabelon** åbnes med varekortet som skabelon.
2. Udfyld felterne efter behov. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
3. Hvis du vil genbruge dimensioner i kladder, skal du vælge handlingen **Dimensioner**. Vinduet **Skabeloner til dimensioner** åbnes med alle dimensionsværdikoder, der er konfigureret for varen.
4. Rediger eller angiv dimensionskoder, der skal gælde for nye debitorkort, oprettes ved hjælp af skabelonen.
5. Når du har fuldført skabelonen for den nye vare, skal du vælge knappen **OK**.

Vareskabelonen føjes til listen over vareskabeloner, så du kan bruge den til at oprette nye varekort.

## <a name="see-also"></a>Se også
  [Lagerbeholdning](inventory-manage-inventory.md)  
  [Køb](purchasing-manage-purchasing.md)  
  [Salg](sales-manage-sales.md)  
  [Arbejde med [!INCLUDE[d365fin_long](includes/d365fin_long_md.md)]](ui-work-product.md)

## [!INCLUDE[d365fin](includes/free_trial_md.md)]
