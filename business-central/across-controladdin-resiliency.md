---
title: Styre tilføjelsesprogrammet resiliency i Business central
description: 'Det, hvis kontrol tilføjelsesprogrammer eller brugerdefinerede kontrolelementer medfører reduceret funktionalitet i Business central.'
ms.topic: conceptual
author: brentholtorf
ms.author: bholtorf
ms.date: 12/12/2023
ms.service: dynamics-365-business-central
ms.reviewer: bholtorf
---

# Styre tilføjelsesprogrammet resiliency i Business central

Fra opdatering 20.0 i [!INCLUDE[prod_short](includes/prod_short.md)] skal der automatisk registreres tilføjelsesprogrammer, som udfører langsomt, og der vises en dialogboks, der ligner nedenstående.

![Aktiv tilføjelseskontrolelement.](media/controladdin-resiliency.png "Aktiv tilføjelseskontrolelement.")

Et tilføjelsesprogram til en usund styring kan påvirke din Business Central-oplevelse og medføre, at den side, du arbejder på, starter langsomt. Den har ingen indflydelse på data, og ændringerne gemmes altid. Hvis du får vist advarslen som vist ovenfor, kan du skjule den, men den kan komme tilbage, hvis problemet fortsætter, skal du kontakte administratoren.

## Se også
[Styr bedste praksis for tilføjelsesydelse](/dynamics365/business-central/dev-itpro/developer/devenv-control-addin-bestpractices)  