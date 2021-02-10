---
title: Oprette kort for varer eller tjenesteydelser | Microsoft Docs
description: Du kan oprette varekort for tjenester, du sælger som timer, og fysiske produkter, f.eks. montageelementer, færdigvarer, komponenter eller råvarer, som sælges fra lageret.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: item, finished good, component, raw material, assembly item
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: 6e4bf13885ccd7888e1750f4351741150df7b7df
ms.sourcegitcommit: 2e7307fbe1eb3b34d0ad9356226a19409054a402
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 12/17/2020
ms.locfileid: "4746212"
---
# <a name="register-new-items"></a>Registrere nye varer

Varer er, blandt andre produkter, grundlaget for din virksomhed og de varer eller tjenester, som du handler med. Hver vare skal registreres som et varekort.

Varekort indeholder de oplysninger, der kræves for at købe, opbevare, sælge, levere og føre regnskab med varer.

Varekortet kan være af typen **Lager**, **Service** eller **Ikke-lager** for at angive, om varekortet repræsenterer en fysisk lagerenhed, en arbejdstidsenhed eller en fysisk enhed, der ikke spores på lageret. Du kan finde flere oplysninger i [Om varetyper](inventory-about-item-types.md).

En vare kan struktureres som en overordnet vare med underliggende underordnede varer på en stykliste. I [!INCLUDE[prod_short](includes/prod_short.md)] kan en stykliste enten være en montagestykliste eller en produktionsstykliste, afhængigt af dens anvendelse. Du kan finde flere oplysninger under [Arbejde med styklister](inventory-how-work-BOMs.md).

Hvis du køber den samme vare fra flere forskellige leverandører, kan du forbinde disse leverandører på varekortet. Leverandørerne vises derefter på siden **Vare/leverandører**, så du nemt kan vælge en anden leverandør.

Varer, som du tilbyder til dine kunder, men som du ikke vil administrere i dit system, før du begynder at sælge dem, kan oprettes som katalogvarer. Katalogvarer må ikke forveksles med almindelige varer af typen **Ikke-lager**. Du kan finde flere oplysninger under [Arbejde med katalogvarer](inventory-how-work-nonstock-items.md).  

> [!NOTE]  
> Hvis der er en vareskabelon til forskellige varetyper, vises der en side, når du opretter et nyt varekort, hvorfra du kan vælge en passende skabelon. Hvis der kun er én vareskabelon, bruger nye varekort altid denne skabelon.

Følgende fremgangsmåde beskriver, hvordan du opretter et varekort fra bunden. Du kan også oprette nye varekort ved at kopiere eksisterende kort. Du kan finde flere oplysninger i [Kopiere eksisterende elementer for at oprette nye varer](inventory-how-copy-items.md).  

> [!Video https://www.microsoft.com/videoplayer/embed/RE47eLx?rel=0]

## <a name="to-create-a-new-item-card"></a>Sådan oprettes et nyt varekort

1. Vælg ikonet ![Elpære, der åbner funktionen Fortæl mig](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig"), angiv **Varer**, og vælg derefter det relaterede link.  
2. På siden **Varer** skal du vælge handlingen **Ny**.

    Hvis der kun er én vareskabelon, åbnes nye varekort med nogle felter, der er udfyldt med oplysninger fra denne skabelon.
3. På siden **Vælg en skabelon til en ny vare** skal du vælge den skabelon, som du vil bruge til det nye varekort.
4. Vælg knappen **OK**. Et nyt varekort åbnes med nogle felter udfyldt med oplysninger fra skabelonen.
5. Fortsæt med at udfylde eller ændre felterne på varekortet efter behov. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

> [!NOTE]
> I feltet **Kostmetode** skal du angive, hvordan varens kostpris beregnes på baggrund af antagelser om gennemstrømningen af fysiske varer i virksomheden. Fem kostmetoder er tilgængelige, afhængigt af varetypen. Du kan finde flere oplysninger i [Designoplysninger: Kostmetoder](design-details-costing-methods.md).
>
> Hvis du vælger **Gennemsnit**, beregnes en vares kostpris som den gennemsnitlige kostpris på hvert enkelt tidspunkt efter et køb. Lager værdiansættes ud fra den forudsætning, at alle lagerbeholdninger sælges samtidig. Med denne indstilling kan du vælge feltet **Kostpris** på siden **Oversigt over beregning af gns. kostpris** for at få vist en oversigt over transaktioner, som den gennemsnitlige kostpris beregnes ud fra.

Du kan se eller redigere specialpriser eller rabatter, som du tildeler til varen, eller som din leverandør giver dig, hvis bestemte kriterier opfyldes, f.eks. debitor, mindste ordrestørrelse eller slutdato. Det gør du ved at vælge handlingerne **Angiv særlige priser** eller **Angiv særlig rabat**. Hver række på eksempelvis siden **Salgspriser** repræsenterer en særlig pris. Hver kolonne repræsenterer et kriterium, der skal gælde for at tildele en debitor den specielle pris, som du angiver i feltet **Enhedspris** på siden **Salgspriser**. Du kan finde flere oplysninger i [Registrere salgspris, rabat og betalingsaftaler](sales-how-record-sales-price-discount-payment-agreements.md) eller [Registrere særlige købspriser og rabatter](purchasing-how-record-purchase-price-discount-payment-agreements.md).

Varen er nu registreret, og varekortet er klar til at blive brugt i købs- og salgsdokumenter.

Hvis du vil bruge dette varekort som skabelon, når du opretter nye varekort, kan du gemme det som en skabelon. Du kan finde flere oplysninger i følgende afsnit.  

### <a name="to-save-the-item-card-as-a-template"></a>Sådan gemmes varekortet som en skabelon

1. På siden **Varekort** skal du vælge handlingen **Gem som skabelon**. Siden **Vareskabelon** åbnes med varekortet som skabelon.
2. Udfyld felterne efter behov. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
3. Hvis du vil genbruge dimensioner i kladder, skal du vælge handlingen **Dimensioner**. Siden **Skabeloner til dimensioner** åbnes med alle dimensionsværdikoder, der er konfigureret for varen.
4. Rediger eller angiv dimensionskoder, der skal gælde for nye debitorkort, oprettes ved hjælp af skabelonen.
5. Når du har fuldført skabelonen for den nye vare, skal du vælge knappen **OK**.

Vareskabelonen føjes til listen over vareskabeloner, så du kan bruge den til at oprette nye varekort.

### <a name="items-used-in-production-orders"></a>Varer, der bruges i produktionsordrer

Hvis du vil registrere varer, der derefter bruges i produktionsordrer, skal du angive genbestillingssystemet som *Prod.ordre* i oversigtspanelet **Genbestilling**. Du kan finde flere oplysninger i [Om produktionsordrer](production-about-production-orders.md).  

## <a name="to-set-up-multiple-vendors-for-an-item"></a>Sådan oprettes flere leverandører af en vare

Hvis du køber den samme vare fra flere forskellige leverandører, skal du angive oplysninger om hver vareleverandør, f.eks. priser, leveringstid og rabatter.  

1. Vælg ikonet ![Elpære, der åbner funktionen Fortæl mig](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig"), angiv **Varer**, og vælg derefter det relaterede link.  
2. Markér den relevante vare, og vælg derefter handlingen **Rediger**.  
3. Vælg handlingen **Leverandører**.  
4. Vælg feltet **Kreditornr.**, og vælg derefter den kreditor, du vil konfigurere for varen.  
5. Det er valgfrit, om du vil udfylde de resterende felterne.  
6. Gentag trin 2 til 5 for hver leverandør, du ønsker at købe varen fra.

Leverandørerne vises nu på siden **Vare/leverandører**, som du åbner fra varekortet, så du nemt kan vælge en anden leverandør.

## <a name="categories-attributes-and-variants"></a>Kategorier, attributter og varianter

[!INCLUDE[inventory_variant](includes/inventory_variant.md)]

## <a name="deleting-item-cards"></a>Sletning af varekort

Hvis du har bogført en postering for en vare, kan du ikke slette kortet, da posterne muligvis er nødvendige med henblik på værdiansættelse eller revision af lageret. Hvis du vil slette varekort med poster, skal du kontakte Microsoft-partneren for at gøre dette via kode.  

## <a name="manage-inventory-in-warehouses"></a>Administration af lager på lagersteder

Når du registrerer en ny vare, kan du se de felter, der er relateret til lagerstedsstyringen, især i oversigtspanelet **Lagersted**. Hvis organisationen ikke bruger warehouse management capabilities i [!INCLUDE [prod_short](includes/prod_short.md)], kan du ignorere disse felter.  

Hvis organisationen på et senere tidspunkt opsætter logistik, skal du i de fleste tilfælde gå tilbage til hver eksisterende vare for at sikre, at det indeholder de relevante oplysninger i de forskellige felter, så lager processerne kan køre som forventet. Disse oplysninger kan omfatte felter som **Lagerklassekode** eller **Læg på lager-skabelonkode**. Du kan finde flere oplysninger i [Designoplysninger: Opsætning af lager](design-details-warehouse-setup.md)  

## <a name="see-also"></a>Se også

[Lagerbeholdning](inventory-manage-inventory.md)  
[Oprette måleenheder](inventory-how-setup-units-of-measure.md)  
[Varekoder](finance-how-setup-report-intrastat.md#tariff-numbers)  
[Afstemme lageromkostninger med finansregnskabet](finance-how-to-post-inventory-costs-to-the-general-ledger.md)  
[Oprette nummerserie](ui-create-number-series.md)  
[Konfigurere bogføringsgrupper](finance-posting-groups.md)  
[Køb](purchasing-manage-purchasing.md)  
[Salg](sales-manage-sales.md)  
[Arbejde med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  
