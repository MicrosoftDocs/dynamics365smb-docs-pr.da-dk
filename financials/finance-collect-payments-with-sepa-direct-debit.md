---
title: SEPA Direct Debit i Dynamics 365 | Microsoft Docs
description: "Du kan opkræve betalinger direkte fra kundens bankkonto i overensstemmelse med SEPA-formatet."
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 08/21/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 8b2e20e694279a8c06188e0e429ef3b4fb43aea2
ms.openlocfilehash: 0447e6c9f84457589df5cbc1efaecb2de24e7295
ms.contentlocale: da-dk
ms.lasthandoff: 09/27/2017

---
# <a name="collecting-payments-with-sepa-direct-debit"></a>Indhente betalinger med SEPA Direct Debit
Du kan opkræve betalinger direkte fra kundens bankkonto i overensstemmelse med SEPA-formatet med kundens samtykke.  

 Opret først eksportformatet for bankfilen, der instruerer din bank i at udføre en Direct Debit. Derefter konfigureres kundens betalingsform. Til sidst oprettes den Direct Debit-betalingsaftale, der afspejler din aftale med kunden om opkrævning af deres betalinger i en bestemt periode i aftalen.  

 For at instruere banken i at overføre det indbetalte beløb fra kundens bankkonto til din virksomheds konto, opretter du en post i den Direct Debit-opkrævning, der indeholder oplysninger om bankkonti, de berørte salgsfakturaer og den Direct Debit-betalingsaftale. Derefter eksporterer du en XML-fil, der er baseret på opkrævningsposten, som du sender til din bank til behandling. Du får besked fra banken om alle betalinger, der ikke kunne behandles af banken, og derefter skal du manuelt afvise de pågældende poster i den Direct Debit-opkrævning.  

 Du kan angive standarddebitorsalgskoder med oplysninger om Direct Debit-betalingsform og -bemyndigelse. Du kan derefter bruge kørslen **Opret standardkundefakturaer** til at generere flere salgsfakturaer med oplysninger om Direct Debit udfyldt på forhånd. Dette kan udføres manuelt eller automatisk, alt efter betalingens forfaldsdato.  

 Når betalinger er behandlet, og banken har informeret om det, kan du bogføre betalingskvitteringer enten direkte fra vinduet **Poster i Direct Debit-opkrævning** eller ved at flytte betalingslinjerne til den kladde, hvor du bogfører betalingskvitteringer, f.eks. vinduet **Indbetalingskladde**. Alternativt kan du, afhængigt af hvordan din likviditetsstyring foregår, vente og kun anvende betalingerne som en del af bankafstemningen.  

> [!NOTE]  
>  Hvis du vil samle betalinger ved hjælp af SEPA Direct Debit, skal valutaen på salgsfakturaen være i EURO.  

 Den følgende tabel indeholder en opgavesekvens med links til de emner, der rummer beskrivelserne af opgaverne.   

|**Hvis du vil**|**Se**|  
|------------|-------------|  
|Udarbejd bankkontoformater, betalingsformer og kundeaftaler til SEPA Direct Debit.|[Fremgangsmåde: Konfigurere SEPA Direct Debit](finance-how-to-set-up-sepa-direct-debit.md)|  
|Bed din bank om at overføre beløb fra din kundes bankkonti til dit firmas konto i overensstemmelse med konfigurationen af SEPA Direct Debit.|[Fremgangsmåde: Opret poster i SEPA Direct Debit-opkrævning, og eksportér til en bankfil](finance-how-create-sepa-direct-debit-collection-entries-export-bank-file.md)|  
|Konfigurer standarddebitorsalgskoder for fakturaer til direkte debitering, og opret salgsfakturaer med oplysninger om direkte debitering, når fakturaerne forfalder til betaling.|[Fremgangsmåde: Oprette gentagne salgs- og købslinjer](sales-how-work-standard-lines.md)|  
|Bogfør betalinger foretaget som SEPA Direct Debit.|[Fremgangsmåde: Bogføre SEPA Direct Debit-betalingskvitteringer](finance-how-to-post-sepa-direct-debit-payment-receipts.md)|  

## <a name="see-also"></a>Se også  
[Administrere tilgodehavender](receivables-manage-receivables.md)

