---
title: "Fremgangsmåde: Registrere nye debitorer | Microsoft Docs"
description: "Fremgangsmåde: Registrere nye debitorer"
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: client
ms.date: 03/29/2017
ms.author: sgroespe
ms.translationtype: Human Translation
ms.sourcegitcommit: a31be0f9d07e2abb591e26f6bae34c6f6e4dcda6
ms.openlocfilehash: 6789e6a4129789e950c7f71ff86e62263ae9c087
ms.contentlocale: da-dk
ms.lasthandoff: 05/04/2017


---
# <a name="how-to-register-new-customers"></a>Fremgangsmåde: Registrere nye debitorer
Debitorer er kilden til din indtægt. Du skal registrere hver debitor, du sælger til som et debitorkort. Debitorkort indeholder de oplysninger, som er en forudsætning for at sælge produkter til debitoren. Du kan finde flere oplysninger i [Fremgangsmåde: Fakturere salg](sales-how-invoice-sales.md) og [Fremgangsmåde: Registrere nye varer](inventory-how-register-new-items.md).  

Før du kan registrere nye debitorer, skal du oprette forskellige salgskoder, som du kan vælge mellem, når du udfylder debitorkort. Der er flere oplysninger i [Konfigurere salg](sales-setup-sales.md).

**Bemærk**: Hvis der er debitorskabeloner for forskellige debitortyper, vises der automatisk et vindue, når du opretter et nyt debitorkort, hvorfra du kan vælge en passende skabelon. Hvis der kun er én debitorskabelon, bruger nye debitorkort altid denne skabelon.

## <a name="to-create-a-new-customer-card"></a>Sådan oprettes et nyt debitorkort
1. På startsiden skal du vælge handlingen **Debitorer** for at åbne oversigten over eksisterende debitorer.  
2. I vinduet **Debitorer** skal du vælge handlingen **Ny**.

    Hvis der kun er ét debitorbilag, åbnes der et nyt debitorkort, hvor nogle felter er udfyldt med oplysninger fra skabelonen.

    Hvis der er mere end én debitorskabelon, åbnes der automatisk et vindue, hvor du kan vælge en debitorskabelon. I dette tilfælde skal du følge de næste to trin.
3. I vinduet **Vælg en skabelon til en ny debitor** skal du vælge den skabelon, som du vil bruge til det nye debitorkort.
4. Vælg knappen **OK**. Et nyt debitorkort åbnes med nogle felter udfyldt med oplysninger fra skabelonen.  
5. Fortsæt med at udfylde eller ændre felterne på debitorkortet efter behov. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

I oversigtspanelet **Salgspriser** kan du se specialpriser eller rabatter, som du tildeler til debitoren, hvis bestemte kriterier opfyldes, f.eks. vare, mindste ordrestørrelse eller slutdato. Hver række repræsenterer en specialpris- eller en linjerabat. Hver kolonne repræsenterer et kriterium, der skal anvendes for at garantere den specialpris, du angiver i feltet **Enhedspris** eller den linjerabat, som du angiver i feltet **Linjerabatpct.** Du kan finde flere oplysninger under [Registrere salgspris, rabat og betalingsaftaler](sales-how-record-sales-price-discount-payment-agreements.md).

Debitoren er nu registreret, og debitorkortet er klar til at blive brugt i salgsdokumenter.

Hvis du vil bruge dette debitorkort som skabelon, når du opretter nye debitorkort, kan du gemme det som en skabelon. Du kan finde flere oplysninger i følgende afsnit.

## <a name="to-save-the-customer-card-as-a-template"></a>Sådan gemmes debitorkortet som en skabelon
1. I vinduet **Debitorkort** skal du vælge handlingen **Gem som skabelon**. Vinduet **Debitorskabelon** åbnes med debitorkortet som skabelon.
2. Udfyld felterne efter behov. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
3. Hvis du vil genbruge dimensioner i kladder, skal du vælge handlingen **Dimensioner**. Vinduet **Skabeloner til dimensioner** åbnes med alle dimensionsværdikoder, der er konfigureret for debitoren.
4. Rediger eller angiv dimensionskoder, der skal gælde for nye debitorkort, oprettes ved hjælp af skabelonen.  
5. Når du har fuldført skabelonen for den nye debitor, skal du vælge knappen **OK**.

Debitorskabelonen føjes til listen over debitorskabeloner, så du kan bruge den til at oprette nye debitorkort.

## <a name="see-also"></a>Se også
[Salg](sales-manage-sales.md)    
[Konfigurere salg](sales-setup-sales.md)    
[Arbejde med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

