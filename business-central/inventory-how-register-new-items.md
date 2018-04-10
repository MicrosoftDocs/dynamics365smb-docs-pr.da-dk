---
title: Oprette kort for varer eller tjenesteydelser | Microsoft Docs
description: "Du kan oprette varekort for tjenester, du sælger som timer, og fysiske produkter, f.eks. montageelementer, færdigvarer, komponenter eller råvarer, som sælges fra lageret."
documentationcenter: 
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: item, finished good, component, raw material, assembly item
ms.date: 08/31/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: ea9b4a6310df319df06d02c53b9d6156caaee24f
ms.openlocfilehash: ac7664480d5a2db4642ecc2cb830c4d7022fb53b
ms.contentlocale: da-dk
ms.lasthandoff: 03/28/2018

---
# <a name="register-new-items"></a>Registrere nye varer
Varer er, blandt andre produkter, grundlaget for din virksomhed og de varer eller tjenester, som du handler med. Hver vare skal registreres som et varekort.

Varekort indeholder de oplysninger, der kræves for at købe, opbevare, sælge, levere og føre regnskab med varer.

Varekortet kan være af typen **Lager** eller **Service** for at angive, om varen er en fysisk enhed eller en arbejdstidsenhed. Bortset fra visse felter, der vedrører de fysiske aspekter af en vare, fungerer alle felter på et varekort på samme måde for lagervarer og tjenester. Du kan finde flere oplysninger om salg af en vare under [Sælge produkter](sales-how-sell-products.md) eller [Fakturere salg](sales-how-invoice-sales.md).

En vare kan struktureres som en overordnet vare med underliggende underordnede varer på en stykliste. I [!INCLUDE[d365fin](includes/d365fin_md.md)] kan en stykliste enten være en montagestykliste eller en produktionsstykliste, afhængigt af dens anvendelse. Du kan finde flere oplysninger under [Arbejde med styklister](inventory-how-work-BOMs.md).

> [!NOTE]  
>   Hvis der er en vareskabelon til forskellige varetyper, vises der et vindue, når du opretter et nyt varekort, hvorfra du kan vælge en passende skabelon. Hvis der kun er én vareskabelon, bruger nye varekort altid denne skabelon.

Hvis du køber den samme vare fra flere forskellige leverandører, kan du forbinde disse leverandører på varekortet. Leverandørerne vises derefter i vinduet **Vare/leverandører**, så du nemt kan vælge en anden leverandør.

## <a name="to-create-a-new-item-card"></a>Sådan oprettes et nyt varekort
1. Vælg ikonet ![Søg efter side eller rapport](media/ui-search/search_small.png "Ikonet Søg efter side eller rapport"), angiv **Varer**, og vælg derefter det relaterede link.  
2. I vinduet **Varer** skal du vælge handlingen **Ny**.

    Hvis der kun er én vareskabelon, åbnes nye varekort med nogle felter, der er udfyldt med oplysninger fra denne skabelon.
3. I vinduet **Vælg en skabelon til en ny vare** skal du vælge den skabelon, som du vil bruge til det nye varekort.
4. Vælg knappen **OK**. Et nyt varekort åbnes med nogle felter udfyldt med oplysninger fra skabelonen.
5. Fortsæt med at udfylde eller ændre felterne på varekortet efter behov. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

> [!NOTE]
> I feltet **Kostmetode** skal du angive, hvordan varens kostpris beregnes på baggrund af antagelser om gennemstrømningen af fysiske varer i virksomheden. Fem kostmetoder er tilgængelige, afhængigt af varetypen. Du kan finde flere oplysninger i [Designoplysninger: Kostmetoder](design-details-costing-methods.md).
>
> Hvis du vælger **Gennemsnit**, beregnes en vares kostpris som den gennemsnitlige kostpris på hvert enkelt tidspunkt efter et køb. Lager værdiansættes ud fra den forudsætning, at alle lagerbeholdninger sælges samtidig. Med denne indstilling kan du vælge feltet **Kostpris** i vinduet **Oversigt over beregning af gns. kostpris** for at få vist en oversigt over transaktioner, som den gennemsnitlige kostpris beregnes ud fra.

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

## <a name="to-set-up-multiple-vendors-for-an-item"></a>Sådan oprettes flere leverandører af en vare  
Hvis du køber den samme vare fra flere forskellige leverandører, skal du angive oplysninger om hver vareleverandør, f.eks. priser, leveringstid og rabatter.  

1.  Vælg ikonet ![Søg efter side eller rapport](media/ui-search/search_small.png "Ikonet Søg efter side eller rapport"), angiv **Varer**, og vælg derefter det relaterede link.  
2.  Markér den relevante vare, og vælg derefter handlingen **Rediger**.  
3.  Vælg handlingen **Leverandører**.  
4.  Vælg feltet **Kreditornr.**, og vælg derefter den kreditor, du vil konfigurere for varen.  
5.  Det er valgfrit, om du vil udfylde de resterende felterne.  
6.  Gentag trin 2 til 5 for hver leverandør, du ønsker at købe varen fra.

Leverandørerne vises nu i vinduet **Vare/leverandører**, som du åbner fra varekortet, så du nemt kan vælge en anden leverandør.

## <a name="see-also"></a>Se også
[Oprette nummerserie](ui-create-number-series.md)  
[Lagerbeholdning](inventory-manage-inventory.md)  
[Køb](purchasing-manage-purchasing.md)  
[Salg](sales-manage-sales.md)  
[Arbejde med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

