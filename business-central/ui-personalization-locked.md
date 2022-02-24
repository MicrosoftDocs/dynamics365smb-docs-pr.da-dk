---
title: Hvorfor kan jeg ikke tilpasse en side | Microsoft Docs
description: Forklarer, hvorfor du ikke kan tilpasse en side, og hvad du kan gøre for at låse den op, så du kan tilpasse den.
author: jswymer
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: customize, personalize, personalization, hide columns, remove fields, move fields
ms.date: 04/01/2019
ms.author: jswymer
ms.openlocfilehash: 1a3edaca2e76388d82ea8991c3196410dd9c7288
ms.sourcegitcommit: a88d1e9c0ab647cb8d9d81d32c0bdc82843f4145
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 07/31/2019
ms.locfileid: "1796753"
---
# <a name="why-a-page-is-locked-from-personalization"></a>Hvorfor er en side låst mod tilpasning

Der er to forhold, der forhindrer dig i at tilpasse en side. Enten er siden låst (som angivet af ![Tilpasning låst](media/personalization-lock-icon.png "Tilpasning låst")), eller den er spærret (som angivet af ![Tilpasning spærret](media/personalization-blocked-icon.png "Tilpasning spærret")).

## <a name="locked-from-personalizing"></a>Låst mod tilpasning

Hvis der er et ikon ![Tilpasning låst](media/personalization-lock-icon.png "Tilpasning låst") i banneret **Tilpasning**, når du åbner en side (som vist), betyder det, at du i øjeblikket er forhindret i at foretage flere tilpasningsændringer af siden.

![Tilpasning låst](media/personalization-locked.png "Tilpasning låst")


<!-- This is because we changed the way personalization works behind the scenes since the last time that you personalized the page. Unfortunately, the old way and new of doing things do not work together.

The page currently includes the last personalization changes that you made. If you want to continue personalizing the page, then you can choose the lock icon and then **Unlock**. Just be aware that if you choose to unlock the page, the current personalization of the page will be cleared, and you will have to start from scratch.
-->

Der kan være to grunde til dette:

1. Du har tilpasset siden før, men det er gjort ved hjælp af en tidligere version af produktet. Vi har ændret den måde, hvorpå tilpasning fungerer i baggrunden, siden sidste gang du har tilpasset siden. Desværre arbejder den gamle måde og den nye måde at gøre tingene på ikke sammen.

2. Indtil nu har du kun brugt [!INCLUDE[nav_windows_md](includes/nav_windows_md.md)] til at tilpasse siden.

### <a name="unlocking-the-page"></a>Oplåsning af siden

Hvis du vil låse en side op og fortsætte med at tilpasse den, skal du vælge ![Tilpasning låst](media/personalization-lock-icon.png "Tilpasning låst") og derefter **Lås op**.  

Før du låser siden op, skal du være opmærksom på følgende:

- Den aktuelle tilpasning af siden fjernes. Siden vender tilbage til sit oprindelige format, og du skal starte forfra.

- I feltet [!INCLUDE[nav_windows_md](includes/nav_windows_md.md)] forbliver siden, som den er, og bliver ikke påvirket af nye tilpasningsændringer i Business Central-klienten. Fremover vil tilpasningen i [!INCLUDE[nav_windows_md](includes/nav_windows_md.md)] og Business Central-klienten være helt adskilt fra hinanden.

## <a name="blocked-from-personalizing"></a>Spærret mod tilpasning

Hvis der er et ikon ![Tilpasning spærret](media/personalization-blocked-icon.png "Tilpasning spærret") i banneret Tilpasning, betyder det, at du er spærret mod at foretage nogen form for tilpasning af siden.

![Tilpasning spærret](media/personalization-blocked.png "Tilpasning låst")

Det skyldes, at det rollecenter eller den rolle, der aktuelt er knyttet til brugerkontoen, ændrer denne side specifikt til din rolle. Du kan kontakte systemadministratoren for at få hjælp, eller også kan du, hvis det giver mening, forsøge at skifte til et Rollecenter (fra [**Mine indstillinger**](https://businesscentral.dynamics.com?page=9176 "Gå direkte til siden med dine brugerindstillinger i Business Central")), der inkluderer specifik tilpasning til rollen for denne side.

## <a name="see-also"></a>Se også
[Tilpasse dit arbejdsområde](ui-personalization-manage.md)  
[Administration af tilpasning](ui-personalization-manage.md)  
[Ændring af grundlæggende indstillinger](ui-change-basic-settings.md)  
[Ændre, hvilke funktioner der vises](ui-experiences.md)  
