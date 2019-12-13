---
title: Oprette kort for varer eller tjenesteydelser | Microsoft Docs
description: Du kan oprette varekort for tjenester, du sælger som timer, og fysiske produkter, f.eks. montageelementer, færdigvarer, komponenter eller råvarer, som sælges fra lageret.
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: item, finished good, component, raw material, assembly item
ms.date: 11/27/2019
ms.author: sgroespe
ms.openlocfilehash: 3cb9ffd6dadaeba7aab782c0bd8f45d3f4aa5387
ms.sourcegitcommit: cfc92eefa8b06fb426482f54e393f0e6e222f712
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 12/03/2019
ms.locfileid: "2878337"
---
# <a name="register-new-items"></a>Registrere nye varer
Varer er, blandt andre produkter, grundlaget for din virksomhed og de varer eller tjenester, som du handler med. Hver vare skal registreres som et varekort.

Varekort indeholder de oplysninger, der kræves for at købe, opbevare, sælge, levere og føre regnskab med varer.

Varekortet kan være af typen **Lager**, **Service** eller **Ikke-lager** for at angive, om varekortet repræsenterer en fysisk lagerenhed, en arbejdstidsenhed eller en fysisk enhed, der ikke spores på lageret. Du kan finde flere oplysninger i [Om varetyper](inventory-about-item-types.md).

En vare kan struktureres som en overordnet vare med underliggende underordnede varer på en stykliste. I [!INCLUDE[d365fin](includes/d365fin_md.md)] kan en stykliste enten være en montagestykliste eller en produktionsstykliste, afhængigt af dens anvendelse. Du kan finde flere oplysninger under [Arbejde med styklister](inventory-how-work-BOMs.md).

Hvis du køber den samme vare fra flere forskellige leverandører, kan du forbinde disse leverandører på varekortet. Leverandørerne vises derefter på siden **Vare/leverandører**, så du nemt kan vælge en anden leverandør.

Varer, som du tilbyder til dine kunder, men som du ikke vil administrere i dit system, før du begynder at sælge dem, kan oprettes som katalogvarer. Katalogvarer må ikke forveksles med almindelige varer af typen **Ikke-lager**. Du kan finde flere oplysninger under [Arbejde med katalogvarer](inventory-how-work-nonstock-items.md).  

> [!NOTE]  
> Hvis der er en vareskabelon til forskellige varetyper, vises der en side, når du opretter et nyt varekort, hvorfra du kan vælge en passende skabelon. Hvis der kun er én vareskabelon, bruger nye varekort altid denne skabelon.

Følgende fremgangsmåde beskriver, hvordan du opretter et varekort fra bunden. Du kan også oprette nye varekort ved at kopiere eksisterende kort. Du kan finde flere oplysninger i [Kopiere eksisterende elementer for at oprette nye varer](inventory-how-copy-items.md).<br><br>  

> [!Video https://www.microsoft.com/videoplayer/embed/RE47eLx]

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

Du kan se eller redigere specialpriser eller rabatter, som du tildeler til varen, hvis bestemte kriterier opfyldes, f.eks. debitor, mindste ordrestørrelse eller slutdato. Det gør du ved at vælge handlingerne **Angiv særlige priser** eller **Angiv særlig rabat**. Hver række på eksempelvis siden **Salgspriser** repræsenterer en særlig pris. Hver kolonne repræsenterer et kriterium, der skal gælde for at tildele en debitor den specielle pris, som du angiver i feltet **Enhedspris** på siden **Salgspriser**. Du kan finde flere oplysninger under [Registrere salgspris, rabat og betalingsaftaler](sales-how-record-sales-price-discount-payment-agreements.md).

Varen er nu registreret, og varekortet er klar til at blive brugt i købs- og salgsdokumenter.

Hvis du vil bruge dette varekort som skabelon, når du opretter nye varekort, kan du gemme det som en skabelon. Du kan finde flere oplysninger i følgende afsnit.

## <a name="to-save-the-item-card-as-a-template"></a>Sådan gemmes varekortet som en skabelon
1. På siden **Varekort** skal du vælge handlingen **Gem som skabelon**. Siden **Vareskabelon** åbnes med varekortet som skabelon.
2. Udfyld felterne efter behov. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
3. Hvis du vil genbruge dimensioner i kladder, skal du vælge handlingen **Dimensioner**. Siden **Skabeloner til dimensioner** åbnes med alle dimensionsværdikoder, der er konfigureret for varen.
4. Rediger eller angiv dimensionskoder, der skal gælde for nye debitorkort, oprettes ved hjælp af skabelonen.
5. Når du har fuldført skabelonen for den nye vare, skal du vælge knappen **OK**.

Vareskabelonen føjes til listen over vareskabeloner, så du kan bruge den til at oprette nye varekort.

## <a name="to-set-up-multiple-vendors-for-an-item"></a>Sådan oprettes flere leverandører af en vare  
Hvis du køber den samme vare fra flere forskellige leverandører, skal du angive oplysninger om hver vareleverandør, f.eks. priser, leveringstid og rabatter.  

1.  Vælg ikonet ![Elpære, der åbner funktionen Fortæl mig](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig"), angiv **Varer**, og vælg derefter det relaterede link.  
2.  Markér den relevante vare, og vælg derefter handlingen **Rediger**.  
3.  Vælg handlingen **Leverandører**.  
4.  Vælg feltet **Kreditornr.**, og vælg derefter den kreditor, du vil konfigurere for varen.  
5.  Det er valgfrit, om du vil udfylde de resterende felterne.  
6.  Gentag trin 2 til 5 for hver leverandør, du ønsker at købe varen fra.

Leverandørerne vises nu på siden **Vare/leverandører**, som du åbner fra varekortet, så du nemt kan vælge en anden leverandør.

## <a name="see-also"></a>Se også
[Oprette nummerserie](ui-create-number-series.md)  
[Lagerbeholdning](inventory-manage-inventory.md)  
[Køb](purchasing-manage-purchasing.md)  
[Salg](sales-manage-sales.md)  
[Arbejde med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)
