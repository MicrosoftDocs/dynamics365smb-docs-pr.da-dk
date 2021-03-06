---
title: Oprette et debitorkort for at registrere nye kunder | Microsoft Docs
description: Beskriver, hvordan du opretter et debitorkort for at registrere oplysninger om hver ny kunde, du sælger til.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: client
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: 86527387653d198bc8cf6f7817058b5ff551e1d0
ms.sourcegitcommit: 2e7307fbe1eb3b34d0ad9356226a19409054a402
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 12/17/2020
ms.locfileid: "4748315"
---
# <a name="register-new-customers"></a>Registrere nye debitorer

Debitorer er kilden til din indtægt. Du skal registrere hver debitor, du sælger til som et debitorkort. Debitorkort indeholder de oplysninger, som er en forudsætning for at sælge produkter til debitoren. Du kan finde flere oplysninger i [Fakturere salg](sales-how-invoice-sales.md) og [Registrere nye varer](inventory-how-register-new-items.md).  

Før du kan registrere nye debitorer, skal du oprette forskellige salgskoder, som du kan vælge mellem, når du udfylder debitorkort. Der er flere oplysninger i [Konfigurere salg](sales-setup-sales.md).

> [!VIDEO https://www.microsoft.com/videoplayer/embed/RE3PZsM]

## <a name="adding-new-customers"></a>Tilføje nye debitorer

Hvis du vil registrere en ny debitor, skal du udfylde et debitorkort. Du kan oprette skabeloner til forskellige debitorprofiler, eller du kan tilføje debitorer uden skabeloner.  

> [!NOTE]  
> Hvis der er debitorskabeloner for forskellige debitortyper, vises der automatisk på side, når du opretter et nyt debitorkort, hvorfra du kan vælge en passende skabelon. Hvis der kun er én debitorskabelon, bruger nye debitorkort altid denne skabelon.  

### <a name="to-create-a-new-customer-card"></a>Sådan oprettes et nyt debitorkort

1. Vælg ikonet ![Elpære, der åbner funktionen Fortæl mig](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig"), angiv **Debitorer**, og vælg derefter det relaterede link.  
2. På siden **Debitorer** skal du vælge handlingen **Ny**.

    Hvis der kun er ét debitorbilag, åbnes der et nyt debitorkort, hvor nogle felter er udfyldt med oplysninger fra skabelonen.

    Hvis der er mere end én debitorskabelon, åbnes der automatisk på side, hvor du kan vælge en debitorskabelon. I dette tilfælde skal du følge de næste to trin.
3. På siden **Vælg en skabelon til en ny debitor** skal du vælge den skabelon, som du vil bruge til det nye debitorkort.
4. Vælg knappen **OK**. Et nyt debitorkort åbnes med nogle felter udfyldt med oplysninger fra skabelonen.  
5. Fortsæt med at udfylde eller ændre felterne på debitorkortet efter behov. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

I oversigtspanelet **Salgspriser** kan du se specialpriser eller rabatter, som du tildeler til debitoren, hvis bestemte kriterier opfyldes, f.eks. vare, mindste ordrestørrelse eller slutdato. Hver række repræsenterer en specialpris- eller en linjerabat. Hver kolonne repræsenterer et kriterium, der skal anvendes for at garantere den specialpris, du angiver i feltet **Enhedspris** eller den linjerabat, som du angiver i feltet **Linjerabatpct.** Du kan finde flere oplysninger under [Registrere salgspris, rabat og betalingsaftaler](sales-how-record-sales-price-discount-payment-agreements.md).

Debitoren er nu registreret, og debitorkortet er klar til at blive brugt i salgsdokumenter.

Hvis du vil bruge dette debitorkort som skabelon, når du opretter nye debitorkort, kan du gemme det som en skabelon. Du kan finde flere oplysninger i følgende afsnit.  

### <a name="to-save-the-customer-card-as-a-template"></a>Sådan gemmes debitorkortet som en skabelon

1. På siden **Debitorkort** skal du vælge handlingen **Gem som skabelon**. Siden **Debitorskabelon** åbnes med debitorkortet som skabelon.
2. Udfyld felterne efter behov. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
3. Hvis du vil genbruge dimensioner i kladder, skal du vælge handlingen **Dimensioner**. Siden **Skabeloner til dimensioner** åbnes med alle dimensionsværdikoder, der er konfigureret for debitoren.
4. Rediger eller angiv dimensionskoder, der skal gælde for nye debitorkort, oprettes ved hjælp af skabelonen.  
5. Når du har fuldført skabelonen for den nye debitor, skal du vælge knappen **OK**.

Debitorskabelonen føjes til listen over debitorskabeloner, så du kan bruge den til at oprette nye debitorkort.

## <a name="deleting-customer-cards"></a>Slette debitorkort

Hvis du har bogført en postering for en debitor, kan du ikke slette kortet, da posterne muligvis er nødvendige med henblik på revision. Hvis du vil slette debitorkort med poster, skal du kontakte din Microsoft-partner for at gøre dette via kode.  

## <a name="see-also"></a>Se også

[Definere betalingsformer](finance-payment-methods.md)  
[Flette dublerede poster](sales-how-merge-duplicate-records.md)  
[Oprette nummerserie](ui-create-number-series.md)  
[Salg](sales-manage-sales.md)  
[Konfigurere salg](sales-setup-sales.md)  
[Arbejde med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]