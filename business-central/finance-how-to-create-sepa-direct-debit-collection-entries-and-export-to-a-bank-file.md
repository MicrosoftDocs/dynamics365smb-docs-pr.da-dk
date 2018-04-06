---
title: "SEPA Direct Debit-opkrævning | Microsoft Docs"
description: "Opret en Direct Debit-opkrævningen og eksporter en XML-fil, som du sender eller overfører til din elektroniske bank til behandling."
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: direct-debit, collection, payment, sepa
ms.date: 08/21/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: d7fb34e1c9428a64c71ff47be8bcff174649c00d
ms.openlocfilehash: 769d37db4547e292f12ac95f814f450b489792d4
ms.contentlocale: da-dk
ms.lasthandoff: 03/22/2018

---
# <a name="create-sepa-direct-debit-collection-entries-and-export-to-a-bank-file"></a>Oprette poster i SEPA Direct Debit-opkrævning, og eksportere til en bankfil
For at instruere banken i at overføre det indbetalte beløb fra kundens bankkonto til din virksomheds konto, opretter du en post i den Direct Debit-opkrævning, der indeholder oplysninger om kundens bankkonto, de berørte salgsfakturaer og den Direct Debit-betalingsaftale. Fra posten i den direkte debiteringsopkrævning, som fås som resultat, kan du derefter eksportere en XML-fil, som du sender eller overfører til din elektroniske bank til behandling. Du får besked fra banken om alle betalinger, der ikke kunne behandles af banken, og derefter skal du manuelt afvise de pågældende poster i Direct Debit-opkrævningen.  

> [!NOTE]  
>  Hvis du vil samle betalinger ved hjælp af SEPA Direct Debit, skal valutaen på salgsfakturaen være i EURO.  

### <a name="to-create-a-direct-debit-collection"></a>Sådan oprettes en direkte debiteringsopkrævning  
1. Vælg ikonet ![Søg efter side eller rapport](media/ui-search/search_small.png "Ikonet Søg efter side eller rapport"), angiv **Direct Debit-opkrævninger**, og vælg derefter det relaterede link.  
2. Vælg **Opret Direct Debit-opkrævning** i gruppen **Ny** under fanen **Startside** i vinduet **Direct Debit-opkrævninger**.  
3. I vinduet **Opret Direct Debit-opkrævning** skal du udfylde felterne som beskrevet i følgende tabel.  

    |Felt|Beskrivelse|  
    |---------------------------------|---------------------------------------|  
    |**Fra forfaldsdato**|Angiv den tidligste forfaldsdato for betaling på salgsfakturaer, som du vil oprette en direkte debiteringsopkrævning for.|  
    |**Til forfaldsdato**|Angiv den seneste forfaldsdato for betaling på salgsfakturaer, som du vil oprette en direkte debiteringsopkrævning for.|  
    |**Partnertype**|Angiver, om der foretages direkte debiteringsopkrævning for debitorer af typen **Virksomhed** eller **Person**.|  
    |**Kun kunder med gyldig bemyndigelse**|Angiv, om der oprettes en Direct Debit-opkrævning for debitorer, der har en gyldig Direct Debit-betalingsaftale. **Bemærk:** Der oprettes en Direct Debit-opkrævning, også selvom feltet **Id for Direct Debit-betalingsaftale** ikke er udfyldt på salgsfakturaen.|  
    |**Kun fakturaer med gyldig betalingsaftale**|Angiv, om der kun oprettes en Direct Debit-opkrævning for salgsfakturaer, hvis der er valgt en gyldig Direct Debit-betalingsaftale i feltet **Id for Direct Debit-betalingsaftale** på salgsfakturaen.|  
    |**Bankkontonr.**|Angiv, hvilke af firmaets bankkonti den opkrævede betaling skal overføres til fra debitors bankkonto.|  
    |**Bankkontonavn**|Angiver navnet på den bankkonto, som du vælger i feltet **Bankkontonr.**. Dette felt udfyldes automatisk.|  

4. Vælg knappen **OK**.  

     Der føjes en Direct Debit-opkrævning til vinduet **Direct Debit-opkrævninger**, og der oprettes en eller flere poster med Direct Debit-opkrævning.  

### <a name="to-export-a-direct-debit-collection-entry-to-a-bank-file"></a>Sådan eksporteres en post i en direkte debiteringsopkrævning til en bankfil  
1. Vælg **Poster i Direct Debit-opkrævning** i gruppen **Behandle** under fanen **Startside** i vinduet **Direct Debit-opkrævninger**.  
2. I vinduet **Poster i Direct Debit-opkrævning** skal du markere den post, du vil eksportere, og derefter vælge **Opret fil til Direct Debit-fil** under fanen **Startside** i gruppen **Behandl**.  
3. Gem eksportfilen på det sted, hvorfra du sender eller overfører den til din elektroniske bank.  

     I vinduet **Poster i Direct Debit-opkrævning** ændres feltet **Status for Direct Debit-opkrævning** til Fil oprettet. I vinduet **SEPA Direct Debit-betalingsaftaler** opdateres feltet **Debettæller** med et styk.  

Hvis den eksporterede fil ikke kan behandles, f.eks. fordi debitoren er insolvent, kan du afvise posten i den direkte debiteringsopkrævning. Hvis den eksporterede fil er blevet behandlet af banken, opkræves forfaldne betalinger for de involverede salgsfakturaer automatisk fra de berørte debitorer. I så fald kan du lukke opkrævningen.  

### <a name="to-reject-a-direct-debit-collection-entry"></a>Sådan afvises en post i en direkte debiteringsopkrævning  
* I vinduet **Poster i Direct Debit-opkrævning** skal du markere den post, der ikke blev behandlet korrekt, og derefter vælge **Afvis post** under fanen **Startside** i gruppen **Behandl**.  

     I vinduet **Poster i Direct Debit-opkrævning** ændres feltet **Status** til **Afvist**.  

### <a name="to-close-a-direct-debit-collection"></a>Sådan lukkes en direkte debiteringsopkrævning  
* I vinduet **Poster i Direct Debit-opkrævning** skal du markere den post, der blev behandlet korrekt, og derefter vælge **Luk opkrævning** under fanen **Startside** i gruppen **Behandl**.  

     Den relaterede direkte debiteringsopkrævning er lukket.  

Du kan nu bogføre kvitteringer for betalinger for de involverede salgsfakturaer. Du kan gøre dette, mens du typisk bogfører betalingskvitteringer, f.eks. i vinduet **Betalingsregistrering**, eller du kan bogføre de relaterede betalingskvitteringer direkte fra vinduet **Poster i Direct Debit-opkrævning**. Du kan finde flere oplysninger i [Bogføre SEPA Direct Debit-betalingskvitteringer](finance-how-to-post-sepa-direct-debit-payment-receipts.md).  

## <a name="see-also"></a>Se også  
[Konfigurere SEPA Direct Debit](finance-how-to-set-up-sepa-direct-debit.md)   
[Bogføre SEPA Direct Debit-betalingskvitteringer](finance-how-to-post-sepa-direct-debit-payment-receipts.md)   
[Indhente betalinger med SEPA Direct Debit](finance-collect-payments-with-sepa-direct-debit.md)   

