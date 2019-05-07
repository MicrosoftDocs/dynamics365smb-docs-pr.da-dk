---
title: Konfigurere betalingsformer | Microsoft Docs
description: Du bruger betalingsformer, for eksempel check, bankoverførsel, kontant eller PayPal, til at definere, hvordan salgs- og købsfakturaer skal betales.
author: bholtorf
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: check, bank transfer, cash, PayPal
ms.date: 04/01/2019
ms.author: bholtorf
ms.openlocfilehash: c9eace037f6a30fafdd5bc2a3af0af83da73b3f5
ms.sourcegitcommit: bd78a5d990c9e83174da1409076c22df8b35eafd
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 03/31/2019
ms.locfileid: "926339"
---
# <a name="defining-payment-methods"></a>Definere betalingsformer
Betalingsformer definerer, hvordan du foretrækker, at debitorer skal betale dig, og hvordan du foretrækker at betale dine kreditorer. Metoden kan variere for hver debitor eller kreditor. Eksempler på typiske betalingsformer er **bank**, **kontant**, **check** eller **konto**. 

Du kan knytte en betalingsmetode til debitorer og kreditorer, så den samme metode altid bruges på de salgs- og købsdokumenter, du opretter til dem. Du kan om nødvendigt ændre metoden på salgs- eller købsdokumentet. F.eks. hvis du vil betale en bestemt købsfaktura kontant og frem for med check. Dette ændrer ikke den betalingsmetode, der som standard er knyttet til kreditoren.

De samme betalingsmetoder bruges til salgs- og købsdokumenter. F.eks. bruges en _kontant_-betalingsmetode både ved indbetalinger, du foretager, og når du modtager betalinger. [!INCLUDE[d365fin](includes/d365fin_md.md)] ved, at når du opretter en salgsfaktura, forventer du at modtage betaling, og det modsatte for købsfakturaer. 

Kreditnotaer for returneringer er dog undtagelser, fordi pengene flyder den modsatte vej, dvs. fra dig til dine kunder og fra din leverandør til dig. Derfor tildeles der ikke en standardbetalingsmetode til kreditnotaer. Der er dog en løsning, hvis du har angivet betalingsbetingelser for debitoren eller kreditoren. Selvom feltet **Beregn kont.rabat på kred.notaer** ikke er beregnet til dette, og du markerer afkrydsningsfeltet på siden **Betalingsbetingelser**, tilføjes en standardbetalingsmetode, når du opretter en kreditnota.

## <a name="to-set-up-a-payment-method"></a>Sådan defineres en betalingsform
[!INCLUDE[d365fin](includes/d365fin_md.md)] indeholder et par betalingsmetoder, som virksomheder ofte bruger. Du kan dog tilføje lige så mange, du vil.

1. Vælg ikonet ![Elpære, der åbner funktionen Fortæl mig](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig"), angiv **Betalingsformer**, og vælg derefter det relaterede link.
2. Udfyld felterne efter behov. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

## <a name="to-assign-a-payment-method-to-a-customer-or-vendor"></a>Sådan tildeles en betalingsmetode til en debitor eller kreditor
1. Vælg ikonet ![Elpære, der åbner funktionen Fortæl mig](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig"), angiv **Debitor** eller **Kreditor**, og vælg derefter det relaterede link.
2. I feltet **Betalingsform** skal du vælge metoden, der skal bruges som standard til debitoren eller kreditoren.

## <a name="see-also"></a>Se også
[Finans](finance.md)  
[Arbejde med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)  
