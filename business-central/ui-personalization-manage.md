---
title: Tilpasse sider til roller | Microsoft Docs
description: Få mere at vide om, hvordan du tilpasser brugergrænsefladen for en profil (rolle), så alle brugere, der har fået tildelt denne rolle, kan se et tilpasset arbejdsområde.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: customize, personalize, personalization, hide columns, remove fields, move fields
ms.date: 04/01/2020
ms.author: edupont
ms.openlocfilehash: cee71cea69468a45b2e731632fce3827c54794c1
ms.sourcegitcommit: a80afd4e5075018716efad76d82a54e158f1392d
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 09/09/2020
ms.locfileid: "3781331"
---
# <a name="customize-pages-for-profiles"></a>Tilpasse sider til profiler
Brugerne kan tilpasse de sider, som udgør deres arbejdsområde, så de passer til deres egne præferencer. Du kan finde flere oplysninger under [Tilpasse dit arbejdsområde](ui-personalization-user.md).

Administratorer kan tilpasse sider til en profil i henhold til den tilknyttede forretningsrolle eller -afdeling, f.eks. så alle de brugere, der er tildelt profilen, kan se det tilpassede sidelayout. Administratoren tilpasser sider ved at bruge de samme funktioner som brugerne, når de tilpasser sider.

> [!NOTE]
> Den typiske forretningsbrug af en profil er en rolle. En profil har derfor navnet *Profil (rolle)* i brugergrænsefladen.

Sidetilpasningen begynder på siden **Profiler (roller)**, som er administratorens udgangspunkt for styring af brugerprofiler for individuelle profilkort. Ud over at tilpasse sidelayoutet kan du styre forskellige andre indstillinger for profiler på siden **Profil (rolle)** for hver profil. Du kan finde flere oplysninger under [Administrere profiler](admin-users-profiles-roles.md).

## <a name="to-customize-pages-for-a-profile"></a>Sådan tilpasses sider for en profil
1. Vælg ikonet ![Elpære, der åbner funktionen Fortæl mig](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig"), angiv **Profiler (roller)**, og vælg derefter det relaterede link.
2. Marker linjen for den profil, du vil tilpasse sider for, og vælg derefter handlingen **Rediger**.
3. Vælg handlingen **Tilpas sider**.

    [!INCLUDE[d365fin](includes/d365fin_md.md)] åbner en ny webbrowserfane for den valgte profil, hvor banneret **Tilpasning** er aktiveret. Banneret **Tilpasning** har samme funktionalitet som banneret **Tilpas**, der er tilgængeligt for brugerne.

4. Tilpas sider efter den pågældende rolles eller afdelings behov på samme måde som en bruger gør. Du kan finde flere oplysninger under [Tilpasse dit arbejdsområde](ui-personalization-user.md).

    > [!NOTE]
    > Hvis du vil navigere under tilpasningen, skal du bruge Ctrl + klikke på en handling, hvis den er fremhævet af pilespidsen.

5. Når du er færdig med at ændre layoutet for en eller flere sider, skal du vælge knappen **Udført** på banneret **Tilpasning**.
6. Luk fanen i webbrowseren.

Tilpasningen af sider er nu registreret for profilen.

## <a name="to-view-all-customized-pages-for-a-profile"></a>Sådan får du vist alle tilpassede sider for en profil
Du kan få vist en oversigt over, hvilke sider der er tilpasset for en profil, f.eks. hvis du vil planlægge, hvilke sider, der skal tilpasses yderligere eller slettes.

- Vælg handlingen **Tilpassede sider** på siden **Profil (rolle)**.

## <a name="to-delete-all-customizations-for-a-profile"></a>Sådan slettes alle tilpasninger for en profil
Du kan annullere alle tilpasninger, du har foretaget for en profil. Tilpasninger, som er introduceret med en udvidelse, og tilpasninger, der er udført af en bruger, slettes ikke. Du kan slette alle tilpasninger med en anden handling. Du kan finde flere oplysninger under [Sådan slettes alle tilpasninger, der er foretaget af en bruger](admin-users-profiles-roles.md#to-delete-all-personalizations-made-by-a-user).

- På siden **Profil (rolle)** for en tilpasset profil skal du vælge handlingen **Fjern brugerdefinerede sider**.

Layoutet på siderne i profilen nulstilles til standardlayoutet.  

## <a name="to-delete-customization-for-specific-pages-for-a-profile"></a>Sådan slettes tilpasning af bestemte sider for en profil
Du kan slette enkelte sidetilpasninger, du har foretaget for en profil. Tilpasninger, som er introduceret med en udvidelse, og tilpasninger, der er udført af en bruger, slettes ikke. Du kan slette bestemte sidetilpasninger med en anden handling. Du kan finde flere oplysninger i [Sådan slettes tilpasninger for bestemte sider](admin-users-profiles-roles.md#to-delete-personalizations-for-specific-pages).

1. Vælg handlingen **Tilpassede sider** på siden **Profil (rolle)**.
2. På siden **Profiltilpasninger** skal du vælge en eller flere linjer for sidetilpasninger, som du vil slette, og derefter vælge handlingen **Slet**.

Layoutet på de valgte sider justeres til de ændringer, du har foretaget.

## <a name="see-also"></a>Se også
[Tilpasse dit arbejdsområde](ui-personalization-user.md)  
[Administrere profiler](admin-users-profiles-roles.md)  
[Ændre grundlæggende indstillinger](ui-change-basic-settings.md)  
[Ændre, hvilke funktioner der vises](ui-experiences.md)  
[Arbejde med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)  
