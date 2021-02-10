---
title: Oprette et kreditorkort for at registrere en ny leverandør | Microsoft Docs
description: Lær, hvordan du opretter et kreditorkort for at registrere en ny kreditor eller leverandør.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: supplier
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: 8efd74c3ae6962a383e5b127056d744dd7c1892f
ms.sourcegitcommit: 2e7307fbe1eb3b34d0ad9356226a19409054a402
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 12/17/2020
ms.locfileid: "4748789"
---
# <a name="register-new-vendors"></a>Registrere nye kreditorer

Kreditorer leverer de produkter, du sælger. Hver kreditor, som du køber fra, skal registreres som et kreditorkort.

Før du kan registrere nye kreditorer, skal du oprette forskellige købskoder, som du kan vælge mellem, når du udfylder kreditorkort. Når alle de obligatoriske stamoplysninger er oprettet, skan du udføre yderligere konfiguration af kreditoren, f.eks. prioritere kreditoren i forbindelse med betaling og få vist de varer, som kreditoren og andre kreditorer kan levere. En anden gruppe opsætningsopgaver for kreditorer er at registrere aftaler vedrørende rabatter, priser og betalingsmetoder. Du kan finde flere oplysninger under [Opsætning af indkøb](purchasing-setup-purchasing.md).

Kreditorkortene indeholde de oplysninger, som er en forudsætning for at købe produkter fra kreditoren. Du kan finde flere oplysninger i [Registrere køb](purchasing-how-record-purchases.md) og [Registrere nye varer](inventory-how-register-new-items.md).

> [!NOTE]  
> Hvis der er kreditorskabeloner til forskellige kreditortyper, vises der automatisk en side, når du opretter et nyt kreditorkort, hvorfra du kan vælge en passende skabelon. Hvis der kun er én kreditorskabelon, bruger nye kreditorkort altid denne skabelon.
<br><br>  

> [!Video https://www.microsoft.com/videoplayer/embed/RE3PZtd?rel=0]

## <a name="to-create-a-new-vendor-card"></a>Sådan oprettes et nyt kreditorkort

1. Vælg ikonet ![Elpære, der åbner funktionen Fortæl mig](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig"), angiv **Leverandører (Kreditorer)**, og vælg derefter det relaterede link.  
2. På siden **Kreditorer** skal du vælge **Ny**.

    Hvis der er mere end én kreditorskabelon, åbnes der automatisk en side, hvor du kan vælge en kreditorskabelon. I dette tilfælde skal du følge de næste to trin.
3. På siden **Vælg en skabelon til en ny kreditor** skal du vælge den skabelon, som du vil bruge til det nye kreditorkort.
4. Vælg knappen **OK**. Et nyt kreditorkort åbnes med nogle felter udfyldt med oplysninger fra skabelonen.
5. Fortsæt med at udfylde eller ændre felterne på kreditorkortet efter behov. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

> [!NOTE]  
> Hvis du ikke på forhånd kender den faktureringsadresse, der skal bruges til alle fakturaer fra en kreditor, skal du ikke udfylde feltet **Kreditornr.**. Vælg i stedet nummeret, efter du har oprettet et dokumenthoved (købsrekvisition, ordre eller faktura)

Kreditoren er nu registreret, og kreditorkortet er klar til at blive brugt i købsdokumenter.

Hvis du vil bruge dette kreditorkort som skabelon, når du opretter nye kreditorkort, kan du gemme det som en kreditorskabelon. Du kan finde flere oplysninger i følgende afsnit.

### <a name="deleting-vendor-cards"></a>Slette kreditorkort
Hvis du har bogført en postering for en kreditor, kan du ikke slette kortet, da posterne muligvis er nødvendige med henblik på revision. Hvis du vil slette kreditorkort med poster, skal du kontakte Microsoft-partneren for at gøre dette via kode.

## <a name="to-save-the-vendor-card-as-a-template"></a>Sådan gemmes kreditorkortet som en skabelon
1. På siden **Kreditorkort** skal du vælge handlingen **Gem som skabelon**. Siden **Kreditorskabelon** åbnes og viser kreditorkortet som skabelon.
2. Udfyld felterne efter behov. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
3. Hvis du vil genbruge dimensioner i kladder, skal du vælge handlingen **Dimensioner**. Siden **Skabeloner til dimensioner** åbnes med alle dimensionsværdikoder, der er konfigureret for kreditoren.
4. Rediger eller angiv dimensionskoder, der skal gælde for nye kreditorkort, oprettes ved hjælp af skabelonen.
5. Når du har fuldført skabelonen for den nye kreditor, skal du vælge knappen **OK**.  
   Kreditorskabelonen føjes til listen over kreditorskabeloner, så du kan bruge den til at oprette nye kreditorkort.

## <a name="see-also"></a>Se også
[Flette dublerede poster](sales-how-merge-duplicate-records.md)  
[Oprette nummerserie](ui-create-number-series.md)  
[Køb](purchasing-manage-purchasing.md)  
[Registrere køb](purchasing-how-record-purchases.md)   
[Arbejde med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  
