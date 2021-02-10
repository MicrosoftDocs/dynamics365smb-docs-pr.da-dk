---
title: Felter, der kræves for at fuldføre processer | Microsoft Docs
description: Få mere at vide om de felter, der er markeret med en rød stjerne, som angiver, at de er obligatoriske og skal udfyldes for at udføre en proces.
services: project-madeira
documentationcenter: ''
author: SusanneWindfeldPedersen
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.date: 10/01/2020
ms.author: solsen
ms.openlocfilehash: f525077069107e1365728aaaaf1e4791a250c6ee
ms.sourcegitcommit: 2e7307fbe1eb3b34d0ad9356226a19409054a402
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 12/17/2020
ms.locfileid: "4760363"
---
# <a name="detecting-mandatory-fields"></a>Registrere obligatoriske felter
Når du indtaster data på siderne i [!INCLUDE[prod_short](includes/prod_short.md)], er visse felter markeret med en rød stjerne. Den røde stjerne betyder, at feltet skal udfyldes for at fuldføre en bestemt proces, der bruger feltet, f.eks. bogføring af en transaktion, der bruger værdien i feltet.

Selv om feltet indeholder en rød stjerne, er du ikke tvunget til at udfylde feltet, før du fortsætter til andre felter eller lukker siden. Den røde stjerne tjener kun som en påmindelse om, at du vil blive blokeret fra at udføre en bestemt proces.

## <a name="examples"></a>Eksempler
På siden **Debitorkort** vises den røde stjerne i feltet **Navn**, i feltet **Skatteområdekode** og i bogføringsgruppefelterne for at angive, at du ikke kan bogføre en salgstransaktion for debitoren, medmindre felterne er udfyldt.

På siden **Varekort** vises den røde stjerne i feltet **Beskrivelse** for at angive, at du ikke kan indsætte varen på en dokumentlinje, såsom en salgsordre, medmindre dette felt udfyldes.

## <a name="see-also"></a>Se også
[Arbejde med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)
