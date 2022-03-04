---
title: Hvorfor kan jeg ikke tilpasse en side
description: Forklarer, hvorfor du ikke kan tilpasse en side, og hvad du kan gøre for at låse den op, så du kan tilpasse den.
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: customize, personalize, personalization, hide columns, remove fields, move fields
ms.search.form: 9020, 9022, 9026, 9027, 9030, 9000, 9004, 9005, 9018, 9006, 9007, 9010, 9016, 9017
ms.date: 04/01/2021
ms.author: edupont
ms.openlocfilehash: dd94d467961cf4f01fdffa35241d84371be64527
ms.sourcegitcommit: cdb57f14960f58b1d36a1b373fbf35dfed5fad9e
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 02/23/2022
ms.locfileid: "8335289"
---
# <a name="why-a-page-is-locked-from-personalization"></a>Hvorfor er en side låst mod tilpasning

Der er to forhold, der forhindrer dig i at tilpasse en side. Enten er siden låst (som angivet med ikonet for ![Tilpasning låst.](media/personalization-lock-icon.png "Tilpasning låst")), eller også er den spærret (angivet med ikonet for ![Tilpasning spærret.](media/personalization-blocked-icon.png "Tilpasning blokeret") ikon).

## <a name="locked-from-personalizing"></a>Låst mod tilpasning

Hvis der er en ![Tilpasning låst.](media/personalization-lock-icon.png "Tilpasning låst") ikon i bjælken **Tilpasning**, når du åbner en side (som vist), betyder det, at du i øjeblikket er forhindret i at foretage flere tilpasningsændringer af siden.

<!-- This is because we changed the way personalization works behind the scenes since the last time that you personalized the page. Unfortunately, the old way and new of doing things do not work together.

The page currently includes the last personalization changes that you made. If you want to continue personalizing the page, then you can choose the lock icon and then **Unlock**. Just be aware that if you choose to unlock the page, the current personalization of the page will be cleared, and you will have to start from scratch.
-->

Der kan være to grunde til dette:

1. Du har tilpasset siden før, men det er gjort ved hjælp af en tidligere version af produktet. Vi har ændret den måde, hvorpå tilpasning fungerer i baggrunden, siden sidste gang du har tilpasset siden. Desværre arbejder den gamle måde og den nye måde at gøre tingene på ikke sammen.

2. Indtil nu har du kun brugt [!INCLUDE[nav_windows_md](includes/nav_windows_md.md)] til at tilpasse siden.

### <a name="unlocking-the-page"></a>Oplåsning af siden

Hvis du vil låse en side op og fortsætte med at tilpasse den, skal du vælge ikonet ![Tilpasning låst](media/personalization-lock-icon.png "Tilpasning låst") og derefter vælge handlingen **Lås op**.  

Før du låser siden op, skal du være opmærksom på følgende:

- Den aktuelle tilpasning af siden fjernes. Siden vender tilbage til sit oprindelige format, og du skal starte forfra.

- I feltet [!INCLUDE[nav_windows_md](includes/nav_windows_md.md)] forbliver siden, som den er, og bliver ikke påvirket af nye tilpasningsændringer i Business Central-klienten. Fremover vil tilpasningen i [!INCLUDE[nav_windows_md](includes/nav_windows_md.md)] og Business Central-klienten være helt adskilt fra hinanden.

## <a name="blocked-from-personalizing"></a>Spærret mod tilpasning

Hvis du kan se ikonet ![Tilpasning spærret](media/personalization-blocked-icon.png "Tilpasning blokeret") i banneret **Tilpasning**, betyder det, at du ikke kan foretage nogen form for tilpasning af siden.

<!-- Only text is translated, so removing this image for non-English UX reasons.  ![Personalize blocked.](media/personalization-blocked.png "Personalize lock") -->

Det skyldes, at det rollecenter eller den rolle, der aktuelt er knyttet til brugerkontoen, ændrer denne side specifikt til din rolle. Kontakt din administrator for at få hjælp. Du kan også prøve at skifte til et rollecenter, der omfatter rolletilpasning for denne side. Du kan finde flere oplysninger i [Ændre grundlæggende indstillinger](ui-change-basic-settings.md).

## <a name="see-also"></a>Se også
[Tilpasse dit arbejdsområde](ui-personalization-user.md)  
[Tilpasse sider til profiler](ui-personalization-manage.md)  
[Ændre grundlæggende indstillinger](ui-change-basic-settings.md)  
[Ændre, hvilke funktioner der vises](ui-experiences.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
