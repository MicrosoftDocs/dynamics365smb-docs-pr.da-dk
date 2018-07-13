---
title: "Håndtere bankkonti | Microsoft Docs"
description: "Du skal afstemme bankposter regelmæssigt med de relaterede banktransaktioner i dine bankkonti."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: reconcile
ms.date: 05/15/2018
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 2286b728a464943841b192031cfea13644441013
ms.openlocfilehash: 319faa64adc93c9e54cf792325daeb6a5a8e0b80
ms.contentlocale: da-dk
ms.lasthandoff: 06/28/2018

---
# <a name="managing-bank-accounts"></a>Håndtere bankkonti
Med faste intervaller skal du afstemme dine bankposter i [!INCLUDE[d365fin](includes/d365fin_md.md)] med de relaterede banktransaktioner i bankkonti i din bank og derefter bogføre saldoen til din bankkonto. Du kan udføre denne opgave, enten som en del af behandling af betalinger, der er repræsenteret på bankkontoudtoget i feltet **Betalingsudligningskladde**. Alternativt kan du udføre opgaven adskilt fra betalingsbehandlingen i vinduet **Bankkontoafstemning**, hvor du sammenholder (afstemmer) bankkontoudtogslinjer i venstre rude med dine interne bankkontoposter i højre rude. I begge vinduer kan du angive oplysninger for bankkontoudtog ved at importere en fil eller et feed, og du kan bruge automatiske sammenholdningsforslag.

> [!NOTE]  
> I nordamerikanske versioner kan du også udføre bankafstemning i vinduet **Bankafstemningskladde**, der er mere velegnet til checks og indskud, men ikke kan bruges til import af bankkontoudtogsfiler. Hvis du vil bruge dette vindue i stedet for vinduet **Bankkontoafstemning**, skal du fjerne markeringen i feltet **Bankafstemning med automatisk match** i vinduet **Regnskabsopsætning**. Du kan finde flere oplysninger i afsnittet "Afstemme bankkonti" under Lokal funktionalitet for USA.

Nogle gange skal der overføres beløb mellem bankkonti i [!INCLUDE[d365fin](includes/d365fin_md.md)] for at afspejle overførsler i din bank. Du udfører denne opgave i vinduet **Finanskladde** på forskellige måder afhængigt af valutaen for beløbene.

Før du kan administrere bankkonti, skal du konfigurere hver bankkonto som et bankkontokort. Desuden skal du oprette elektroniske tjenester, som du kan bruge til import af bankens kontoudtog og eksport af betalingsfilen. Du kan finde flere oplysninger i [Oprette bankkonti](bank-setup-banking.md).

Den følgende tabel indeholder en opgavesekvens med links til de emner, der rummer beskrivelserne af opgaverne.

| Hvis du vil | Se |
| --- | --- |
| Afstem bankkonti i forbindelse med betalingsbehandling i vinduet **Betalingudligningskladde** vindue. |[Udligne betalinger automatisk og afstemme bankkonti](receivables-apply-payments-auto-reconcile-bank-accounts.md) |
| Afstemme bankkonti, herunder checkposter, som en separat opgave i vinduet **Bankkontoafstemning**. |[Afstemme bankkonti separat](bank-how-reconcile-bank-accounts-separately.md) |
| Bogføre overførsler mellem bankkonti i samme valuta eller i forskellige valutaer. |[Overføre bankbeløb](bank-how-transfer-bank-funds.md) |

## <a name="see-also"></a>Se også
[Konfigurere banktransaktioner](bank-setup-banking.md)  
[Administrere tilgodehavender](receivables-manage-receivables.md)  
[Administrere skyldige beløb](payables-manage-payables.md)    
[Arbejde med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)  
[Generelle forretningsfunktioner](ui-across-business-areas.md)  

## [!INCLUDE[d365fin](includes/free_trial_md.md)]  
 

