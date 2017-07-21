---
title: "Håndtere bankkonti | Microsoft Docs"
description: Normalt skal du afstemme bankposter i Finans med de relaterede banktransaktioner i dine bankkonti.
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: reconcile
ms.date: 06/02/2017
ms.author: sgroespe
ms.translationtype: Human Translation
ms.sourcegitcommit: 81636fc2e661bd9b07c54da1cd5d0d27e30d01a2
ms.openlocfilehash: dcefa921d7e8b901d906085e6bce01d6e0aa6ac4
ms.contentlocale: da-dk
ms.lasthandoff: 07/07/2017


---
# <a name="managing-bank-accounts"></a>Håndtere bankkonti
Med faste intervaller skal du afstemme dine bankposter i [!INCLUDE[d365fin](includes/d365fin_md.md)] med de relaterede banktransaktioner i bankkonti i din bank og derefter bogføre saldoen til din bankkonto. Du kan udføre denne opgave, enten som en del af behandling af betalinger, der er repræsenteret på bankkontoudtoget i feltet **Betalingsudligningskladde**. Eller du kan udføre opgaven adskilt fra betalingsbehandling i vinduet **Bankkontoafstemning**, som understøtter checkposter. I begge tilfælde skal du udfylde vinduerne ved at importere bankkontoudtoget til [!INCLUDE[d365fin](includes/d365fin_md.md)].

Nogle gange skal der overføres beløb mellem bankkonti i [!INCLUDE[d365fin](includes/d365fin_md.md)] for at afspejle overførsler i din bank. Du udfører denne opgave i vinduet **Finanskladde** på forskellige måder afhængigt af valutaen for beløbene.

Før du kan administrere bankkonti, skal du konfigurere hver bankkonto som et bankkontokort. Desuden skal du oprette elektroniske tjenester, som du kan bruge til import af bankens kontoudtog og eksport af betalingsfilen. Du kan finde flere oplysninger i [Oprette bankkonti](bank-setup-banking.md).

Den følgende tabel indeholder en opgavesekvens med links til de emner, der rummer beskrivelserne af opgaverne.

| Hvis du vil | Se |
| --- | --- |
| Afstem bankkonti i forbindelse med betalingsbehandling i vinduet **Betalingudligningskladde** vindue. |[Udligne betalinger automatisk og afstemme bankkonti](receivables-apply-payments-auto-reconcile-bank-accounts.md) |
| Afstemme bankkonti, herunder checkposter, som en separat opgave i vinduet **Bankkontoafstemning**. |[Fremgangsmåde: Afstemme bankkonti separat](bank-how-reconcile-bank-accounts-separately.md) |
| Bogføre overførsler mellem bankkonti i samme valuta eller i forskellige valutaer. |[Fremgangsmåde: Overføre bankbeløb](bank-how-transfer-bank-funds.md) |

## <a name="see-also"></a>Se også
[Konfigurere banktransaktioner](bank-setup-banking.md)  
[Administrere tilgodehavender](receivables-manage-receivables.md)  
[Administrere skyldige beløb](payables-manage-payables.md)    
[Arbejde med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)  
[Generelle forretningsfunktioner](ui-across-business-areas.md)  

