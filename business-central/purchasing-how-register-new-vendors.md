---
title: Oprette et kreditorkort for at registrere en ny leverandør | Microsoft Docs
description: Lær, hvordan du opretter et kreditorkort for at registrere en ny kreditor eller leverandør.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: supplier
ms.date: 04/01/2021
ms.author: edupont
ms.openlocfilehash: f1028b91101f8faa38d4d4d5d2695ee498ff6d2e
ms.sourcegitcommit: 766e2840fd16efb901d211d7fa64d96766ac99d9
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 03/31/2021
ms.locfileid: "5772650"
---
# <a name="register-new-vendors"></a>Registrere nye kreditorer

Kreditorer leverer de produkter, du sælger. Hver kreditor, som du køber fra, skal registreres som et kreditorkort.

Før du kan registrere nye kreditorer, skal du oprette forskellige købskoder, som du kan vælge mellem, når du udfylder kreditorkort. Når alle de obligatoriske stamoplysninger er oprettet, skan du udføre yderligere konfiguration af kreditoren, f.eks. prioritere kreditoren i forbindelse med betaling og få vist de varer, som kreditoren og andre kreditorer kan levere. En anden gruppe opsætningsopgaver for kreditorer er at registrere aftaler vedrørende rabatter, priser og betalingsmetoder. Du kan finde flere oplysninger i [Opsætning af indkøb](purchasing-setup-purchasing.md).

Kreditorkortene indeholde de oplysninger, som er en forudsætning for at købe produkter fra kreditoren. Du kan finde flere oplysninger i [Registrere køb](purchasing-how-record-purchases.md) og [Registrere nye varer](inventory-how-register-new-items.md).

> [!NOTE]  
> Hvis der er kreditorskabeloner til forskellige kreditortyper, vises der automatisk en side, når du opretter et nyt kreditorkort, hvorfra du kan vælge en passende skabelon. Hvis der kun er én kreditorskabelon, bruger nye kreditorkort altid denne skabelon.
<br><br>  

> [!Video https://www.microsoft.com/videoplayer/embed/RE3PZtd?rel=0]

## <a name="adding-new-vendors"></a>Tilføjelse af nye kreditorer

Hvis du vil registrere en ny kreditor, skal du udfylde et kreditorkort. Du kan oprette skabeloner til forskellige kreditorprofiler, eller du kan tilføje kreditorer uden skabeloner. Du kan også oprette en kreditor ud fra en kontakt. Du kan finde flere oplysninger i [Sådan oprettes en debitor-, kreditor-, medarbejder- eller bankkonto fra en kontakt](marketing-create-contact-companies.md#to-create-a-customer-vendor-employee-or-bank-account-from-a-contact).  

> [!NOTE]  
> Hvis der er kreditorskabeloner til forskellige kreditortyper, vises der automatisk en side, når du opretter et nyt kreditorkort, hvorfra du kan vælge en passende skabelon. Hvis der kun er én kreditorskabelon, bruger nye kreditorkort altid denne skabelon.  

### <a name="to-create-a-new-vendor-card"></a>Sådan oprettes et nyt kreditorkort

1. Vælg ikonet ![Elpære, der åbner funktionen Fortæl mig](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig"), angiv **Leverandører (Kreditorer)**, og vælg derefter det relaterede link.  
2. På siden **Kreditorer** skal du vælge **Ny**.

    Hvis der er mere end én kreditorskabelon, åbnes der automatisk en side, hvor du kan vælge en kreditorskabelon. I dette tilfælde skal du følge de næste to trin.
    1. På siden **Vælg en skabelon til en ny kreditor** skal du vælge den skabelon, som du vil bruge til det nye kreditorkort.
    2. Vælg knappen **OK**. Et nyt kreditorkort åbnes med nogle felter udfyldt med oplysninger fra skabelonen.
3. Fortsæt med at udfylde eller ændre felterne på kreditorkortet efter behov. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

    > [!TIP]  
    > Hvis du ikke på forhånd kender den faktureringsadresse, der skal bruges til alle fakturaer fra en kreditor, skal du ikke udfylde feltet **Kreditornr.**. Vælg i stedet nummeret, efter du har oprettet et dokumenthoved (købsrekvisition, ordre eller faktura)

Kreditoren er nu registreret, og kreditorkortet er klar til at blive brugt i købsdokumenter.

Hvis du vil bruge dette kreditorkort som skabelon, når du opretter nye kreditorkort, kan du gemme det som en kreditorskabelon. Du kan finde flere oplysninger i afsnittet [Sådan gemmes kreditorkortet som en skabelon](#to-save-the-vendor-card-as-a-template).

### <a name="deleting-vendor-cards"></a>Sletning af kreditorkort

Hvis du har bogført en postering for en kreditor, kan du ikke slette kortet, da posterne muligvis er nødvendige med henblik på revision. Hvis du vil slette kreditorkort med poster, skal du kontakte din Microsoft-partner for at gøre dette via kode.

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

[!INCLUDE[footer-include](includes/footer-banner.md)]