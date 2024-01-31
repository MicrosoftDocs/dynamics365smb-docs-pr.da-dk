---
title: Hvorfor er en side låst mod tilpasning
description: 'Du kan være blokeret for at tilpasse en side. Læs her, om hvad du kan gøre for at låse den op, så du kan tilpasse den.'
author: brentholtorf
ms.topic: conceptual
ms.devlang: al
ms.search.keywords: 'customize, personalize, personalization, hide columns, remove fields, move fields'
ms.search.form: null
ms.date: 04/01/2021
ms.author: bholtorf
ms.service: dynamics-365-business-central
---
# Hvorfor er en side låst mod tilpasning

Der er to forhold, der forhindrer dig i at tilpasse en side. Enten er siden låst (som angivet med ikonet for ![Tilpasning låst.](media/personalization-lock-icon.png "Tilpasning låst")), eller også er den spærret (angivet med ikonet for ![Tilpasning spærret.](media/personalization-blocked-icon.png "Tilpasning blokeret") ikon).

## Låst mod tilpasning

Hvis der er en ![Tilpasning låst.](media/personalization-lock-icon.png "Tilpasning låst") ikon i bjælken **Tilpasning**, når du åbner en side (som vist), betyder det, at du i øjeblikket er forhindret i at foretage flere tilpasningsændringer af siden.

<!-- This is because we changed the way personalization works behind the scenes since the last time that you personalized the page. Unfortunately, the old way and new of doing things do not work together.

The page currently includes the last personalization changes that you made. If you want to continue personalizing the page, then you can choose the lock icon and then **Unlock**. Just be aware that if you choose to unlock the page, the current personalization of the page will be cleared, and you will have to start from scratch.
-->

Der kan være to grunde til dette:

1. Du har tilpasset siden før, men det er gjort ved hjælp af en tidligere version af produktet. Vi har ændret den måde, hvorpå tilpasning fungerer i baggrunden, siden sidste gang du har tilpasset siden. Desværre arbejder den gamle måde og den nye måde at gøre tingene på ikke sammen.

2. Indtil nu har du kun brugt [!INCLUDE[nav_windows_md](includes/nav_windows_md.md)] til at tilpasse siden.

### Oplåsning af siden

Hvis du vil låse en side op og fortsætte med at tilpasse den, skal du vælge ikonet ![Tilpasning låst](media/personalization-lock-icon.png "Tilpasning låst") og derefter vælge handlingen **Lås op**.  

> [!CAUTION]
> Den aktuelle tilpasning af siden fjernes. Siden vender tilbage til sit oprindelige format, og du skal starte forfra.  

## Spærret mod tilpasning

Hvis du kan se ikonet ![Tilpasning spærret](media/personalization-blocked-icon.png "Tilpasning blokeret") i banneret **Tilpasning**, betyder det, at du ikke kan foretage nogen form for tilpasning af siden.

<!-- Only text is translated, so removing this image for non-English UX reasons.  ![Personalize blocked.](media/personalization-blocked.png "Personalize lock") -->

Det skyldes, at det rollecenter eller den rolle, der aktuelt er knyttet til brugerkontoen, ændrer denne side specifikt til din rolle. Kontakt din administrator for at få hjælp. Du kan også prøve at skifte til et rollecenter, der omfatter rolletilpasning for denne side. Du kan finde flere oplysninger i [Ændre grundlæggende indstillinger](ui-change-basic-settings.md).

## Se også

[Tilpasse dit arbejdsområde](ui-personalization-user.md)  
[Tilpasse sider til profiler](ui-personalization-manage.md)  
[Ændre grundlæggende indstillinger](ui-change-basic-settings.md)  
[Ændre, hvilke funktioner der vises](ui-experiences.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
