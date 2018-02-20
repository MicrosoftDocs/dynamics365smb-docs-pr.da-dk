---
title: "Administrere medarbejders fravær | Microsoft Docs"
description: "Beskriver, hvordan du registrerer medarbejderes fravær og analyserer statistik over fravær."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.date: 09/08/2017
ms.author: SorenGP
ms.translationtype: HT
ms.sourcegitcommit: bec0619be0a65e3625759e13d2866ac615d7513c
ms.openlocfilehash: 13461418fd89c8eb743b88b5a2ed98f24a520571
ms.contentlocale: da-dk
ms.lasthandoff: 01/30/2018

---
# <a name="manage-employee-absence"></a>Administrere medarbejderfravær
Hvis du vil administrere en medarbejders fravær, skal du registrere fraværet i vinduet **Fraværsregistrering**. Det kan derefter vises på forskellige måder i forbindelse med analyse og rapportering.

Du kan få vist medarbejderfravær i to forskellige vinduer:

* I vinduet **Fraværsregistrering** registreres alt medarbejderfravær med en linje for hvert fravær.
* I vinduet **Employee Absences** vises kun fravær for én medarbejder. Det er disse oplysninger, du har angivet i vinduet **Fraværsregistrering**, og de er her filtreret efter den enkelte medarbejder.

For at statistikkerne kan bruges, skal der altid bruges de samme måleenheder (timer eller dage) ved registrering af medarbejderfravær.

## <a name="to-register-employee-absence"></a>Sådan registreres medarbejderfravær
Du kan registrere medarbejderfravær dagligt eller med andre intervaller, der opfylder virksomhedens behov.

1. I øverste højre hjørne skal du vælge ikonet **Søg efter side eller rapport**, angive **Fraværsregistrering** og derefter vælge det relaterede link.
2. Vælg handlingen **Ny**.
3. Udfyld en linje for hvert medarbejderfravær, du vil registrere.
4. Luk vinduet.

    > [!Tip]
    > Du skal sikre dig brugbare statistikker ved altid at bruge samme måleenhed, time eller dag, når du registrerer medarbejderfravær.

## <a name="to-view-an-individual-employees-absence"></a>Sådan får du vist en enkelt medarbejders fravær
1. I øverste højre hjørne skal du vælge ikonet **Søg efter side eller rapport**, angive **Medarbejdere** og derefter vælge det relaterede link.
2. Markér den relevante medarbejder, og vælg derefter handlingen **Fravær**.

    Vinduet **Medarbejderfravær** åbnes og viser alt fravær med start- og slutdato for fraværet.

## <a name="to-view-an-employees-absence-by-categories"></a>Sådan får du vist en medarbejders fravær pr. kategori
1. I øverste højre hjørne skal du vælge ikonet **Søg efter side eller rapport**, angive **Medarbejdere** og derefter vælge det relaterede link.
2. Markér den relevante medarbejder, og vælg derefter handlingen **Fravær pr. kategori**.
3. I vinduet **Medarbejderfravær pr. kategori** skal du udfylde filterfelterne efter behov, og derefter vælg handlingen **Vis Matrix**.

    Vinduet **Medarbejderfravær pr. kategori** åbnes og viser alle fravær, opdelt efter fraværsårsag.

## <a name="to-view-all-employee-absences-by-category"></a>Sådan vises alle medarbejderfravær pr. kategori
1. I øverste højre hjørne skal du vælge ikonet **Søg efter side eller rapport**, angive **Fraværsregistrering** og derefter vælge det relaterede link.
2. I vinduet **Fraværsregistrering** skal du vælge handlingen **Oversigt pr. kategori**.
3. I vinduet **Fraværsoversigt pr. kategori** skal du oprette et filter i feltet **Medarbejdernr.filter** for at få vist medarbejderfraværet for en enkelt medarbejder eller en udvalgt gruppe af medarbejdere.
4. Vælg handlingen **Vis matrix**.

    Vinduet **Fraværsoversigt pr. kategori** åbnes og viser alle medarbejdernes fravær opdelt efter forskellige fraværsårsager.

## <a name="to-view-all-employee-absences-by-period"></a>Sådan vises alle medarbejderfravær pr. periode
1. I øverste højre hjørne skal du vælge ikonet **Søg efter side eller rapport**, angive **Fraværsregistrering** og derefter vælge det relaterede link.
   I vinduet **Fraværsregistrering** skal du vælge handlingen **Oversigt pr. periode**.
2. I vinduet **Fraværsoversigt pr. periode** skal du vælge et filter i feltet **Fraværsårsagsfilter** for at få vist medarbejderfravær, der har bestemte årsager.
3. Vælg handlingen **Vis matrix**.

    Vinduet **Fraværsoversigt pr. periode** åbnes og viser alle medarbejdernes fravær opdelt efter periode.

## <a name="see-also"></a>Se også
[Administrere personale](hr-manage-human-resources.md)  
[Finans](finance.md)  
[Arbejde med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)  
[Tilpasse din [!INCLUDE[d365fin](includes/d365fin_md.md)]-oplevelse](ui-experiences.md)

