---
title: Felter, der kræves for at fuldføre processer | Microsoft Docs
description: Få mere at vide om de felter, der er markeret med en rød stjerne, som angiver, at de er obligatoriske og skal udfyldes for at udføre en proces.
services: project-madeira
documentationcenter: ''
author: SusanneWindfeldPedersen
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.date: 04/01/2021
ms.author: solsen
ms.openlocfilehash: 386025d90301f780f8bf5927de495658a100825f
ms.sourcegitcommit: 766e2840fd16efb901d211d7fa64d96766ac99d9
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 03/31/2021
ms.locfileid: "5775271"
---
# <a name="detecting-mandatory-fields"></a>Registrere obligatoriske felter
Når du indtaster data på siderne i [!INCLUDE[prod_short](includes/prod_short.md)], er visse felter markeret med en rød stjerne. Den røde stjerne betyder, at feltet skal udfyldes for at fuldføre en bestemt proces, der bruger feltet, f.eks. bogføring af en transaktion, der bruger værdien i feltet.

Selv om feltet indeholder en rød stjerne, er du ikke tvunget til at udfylde feltet, før du fortsætter til andre felter eller lukker siden. Den røde stjerne tjener kun som en påmindelse om, at du vil blive blokeret fra at udføre en bestemt proces.

## <a name="examples"></a>Eksempler
På siden **Debitorkort** vises den røde stjerne i feltet **Navn**, i feltet **Skatteområdekode** og i bogføringsgruppefelterne for at angive, at du ikke kan bogføre en salgstransaktion for debitoren, medmindre felterne er udfyldt.

På siden **Varekort** vises den røde stjerne i feltet **Beskrivelse** for at angive, at du ikke kan indsætte varen på en dokumentlinje, såsom en salgsordre, medmindre dette felt udfyldes.

## <a name="see-also"></a>Se også
[Arbejde med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]