---
title: "Oprette et kreditorkort for at registrere en ny leverandør | Microsoft Docs"
description: "Lær, hvordan du opretter et kreditorkort for at registrere en ny kreditor eller leverandør."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: supplier
ms.date: 03/29/2017
ms.author: sgroespe
ms.translationtype: Human Translation
ms.sourcegitcommit: 81636fc2e661bd9b07c54da1cd5d0d27e30d01a2
ms.openlocfilehash: 78710d796ed73d7b4c2505f6cbb8c7d5f41d7320
ms.contentlocale: da-dk
ms.lasthandoff: 07/07/2017


---
# <a name="how-to-register-new-vendors"></a>Fremgangsmåde: Registrere nye kreditorer
Kreditorer leverer de produkter, du sælger. Hver kreditor, som du køber fra, skal registreres som et kreditorkort.

Før du kan registrere nye kreditorer, skal du oprette forskellige købskoder, som du kan vælge mellem, når du udfylder kreditorkort. Når alle de obligatoriske stamoplysninger er oprettet, skan du udføre yderligere konfiguration af kreditoren, f.eks. prioritere kreditoren i forbindelse med betaling og få vist de varer, som kreditoren og andre kreditorer kan levere. En anden gruppe opsætningsopgaver for kreditorer er at registrere aftaler vedrørende rabatter, priser og betalingsmetoder. Du kan finde flere oplysninger under [Opsætning af indkøb](purchasing-setup-purchasing.md).

Kreditorkortene indeholde de oplysninger, som er en forudsætning for at købe produkter fra kreditoren. Du kan finde flere oplysninger i [Fremgangsmåde: Registrere køb](purchasing-how-record-purchases.md) og [Fremgangsmåde: Registrere nye varer](inventory-how-register-new-items.md).

> [!NOTE]  
>   Hvis der er kreditorskabeloner til forskellige kreditortyper, vises der automatisk et vindue, når du opretter et nyt kreditorkort, hvorfra du kan vælge en passende skabelon. Hvis der kun er én kreditorskabelon, bruger nye kreditorkort altid denne skabelon.

## <a name="to-create-a-new-vendor-card"></a>Sådan oprettes et nyt kreditorkort
1. På startsiden skal du vælge **Kreditorer** for at åbne oversigten over eksisterende kreditorer.  
2. I vinduet **Kreditorer** skal du vælge **Ny**.

    Hvis der er mere end én kreditorskabelon, åbnes der automatisk et vindue, hvor du kan vælge en kreditorskabelon. I dette tilfælde skal du følge de næste to trin.
3. I vinduet **Vælg en skabelon til en ny kreditor** skal du vælge den skabelon, som du vil bruge til det nye kreditorkort.
4. Vælg knappen **OK**. Et nyt kreditorkort åbnes med nogle felter udfyldt med oplysninger fra skabelonen.
5. Fortsæt med at udfylde eller ændre felterne på kreditorkortet efter behov. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

Kreditoren er nu registreret, og kreditorkortet er klar til at blive brugt i købsdokumenter.

Hvis du vil bruge dette kreditorkort som skabelon, når du opretter nye kreditorkort, kan du gemme det som en kreditorskabelon. Du kan finde flere oplysninger i følgende afsnit.

## <a name="to-save-the-vendor-card-as-a-template"></a>Sådan gemmes kreditorkortet som en skabelon
1. I vinduet **Kreditorkort** skal du vælge handlingen **Gem som skabelon**. Vinduet **Kreditorskabelon** åbnes og viser kreditorkortet som skabelon.
2. Udfyld felterne efter behov. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
3. Hvis du vil genbruge dimensioner i kladder, skal du vælge handlingen **Dimensioner**. Vinduet **Skabeloner til dimensioner** åbnes med alle dimensionsværdikoder, der er konfigureret for kreditoren.
4. Rediger eller angiv dimensionskoder, der skal gælde for nye kreditorkort, oprettes ved hjælp af skabelonen.
5. Når du har fuldført skabelonen for den nye kreditor, skal du vælge knappen **OK**.  
   Kreditorskabelonen føjes til listen over kreditorskabeloner, så du kan bruge den til at oprette nye kreditorkort.

## <a name="see-also"></a>Se også
[Køb](purchasing-manage-purchasing.md)  
[Fremgangsmåde: Registrere køb](purchasing-how-record-purchases.md)   
[Arbejde med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)  

