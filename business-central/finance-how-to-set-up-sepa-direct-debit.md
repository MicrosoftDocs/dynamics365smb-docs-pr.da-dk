---
title: Konfigurere SEPA Direct Debit | Microsoft Docs
description: "Få at vide, hvordan du opsætter SEPA Direct Debit i Business Central."
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 10/01/2018
ms.author: sgroespe
redirect_url: finance-collect-payments-with-sepa-direct-debit
ms.translationtype: HT
ms.sourcegitcommit: d7fb34e1c9428a64c71ff47be8bcff174649c00d
ms.openlocfilehash: 0ba40eb247c1edb2b4d8c7437bf60790545799ee
ms.contentlocale: da-dk
ms.lasthandoff: 03/22/2018

---
# <a name="set-up-sepa-direct-debit"></a>Konfigurere SEPA Direct Debit
Fra vinduet **Direct Debit-opkrævninger** kan du eksportere instruktioner til din netbank for at udføre en direkte debiteringsopkrævning fra debitorens bankkonto til din bankkonto. [!INCLUDE[d365fin](includes/d365fin_md.md)] understøtter SEPA Direct Debit-formatet, men i dit land/område anvendes der muligvis andre formater til elektroniske betalinger.  

For at aktivere eksport af bankfilformater, der ikke umiddelbart understøttes i [!INCLUDE[d365fin](includes/d365fin_md.md)], kan du konfigurere en dataudvekslingsdefinition ved hjælp af dataudvekslingsstrukturen. Du kan finde flere oplysninger i [Konfigurere dataudvekslingsdefinitioner](across-how-to-set-up-data-exchange-definitions.md).  

Før du kan behandle debitorbetalinger elektronisk ved eksport af instruktioner for direkte debitering i SEPA Direct Debit-format, skal du udføre følgende konfigurationstrin:  

* Konfigurer eksportformatet for den bankfil, der instruerer din bank i at udføre en Direct Debit-opkrævning fra kundens bankkonto til din bankkonto.  
* Konfigurer debitorens betalingsform.  
* Konfigurer den Direct Debit-betalingsaftale, der afspejler din aftale med kunden om opkrævning af deres betalinger i en bestemt periode i aftalen.  

### <a name="to-set-up-your-bank-account-for-sepa-direct-debit"></a>Sådan konfigureres din bankkonto til SEPA-Direct Debit  
1. I feltet **Søg** skal du indtaste **Bankkonti** og derefter vælge det relaterede link.  
2. Åbn den bankkonto, du vil bruge til Direct Debit.  
3. I oversigtspanelet **Overfør** i feltet **SEPA Direct Debit-format** skal du vælge indstillingen for SEPA Direct Debit.  

### <a name="to-set-up-the-customers-payment-method-for-sepa-direct-debit"></a>Sådan konfigureres kundens betalingsform til SEPA-Direct Debit  
1. I feltet **Søg** skal du angive **Betalingsformer** og derefter vælge det relaterede link.  
2. Vælg handlingen **Ny**.  
3. Definer en betalingsform. Udfyld de Direct Debit\-specifikke felter som beskrevet i følgende tabel.  

    |Felt|Beskrivelse|  
    |---------------------------------|---------------------------------------|  
    |**Direct Debit**|Angiv, om betalingsformen er til SEPA-Direct Debit-opkrævning.|  
    |**Kode for Direct Debit-betalingsbetingelser**|Angiv betalingsbetingelser, f.eks. BETAL IKKE, der vises på salgsfakturaer, som betales med SEPA-Direct Debit for at angive over for kunden, at betalingen opkræves automatisk. Alternativt kan du lade feltet være tomt.|  

    > [!NOTE]  
    >  Angiv ikke en værdi i feltet **Kontonr.**.  

4. Vælg knappen **OK** for at lukke vinduet **Betalingsformer**.  
5. I feltet **Søg** skal du indtaste **Debitorer** og derefter vælge det relaterede link.  
6. Åbn kortet for den kunde, som du vil konfigurere til SEPA Direct Debit-opkrævning.  
7. Vælg feltet **Betalingsformskode**, og vælg derefter den betalingsformskode, du har angivet i trin 3.  
8. Gentag trin 6 og 7 for alle de debitorer, som du vil konfigurere til SEPA Direct Debit-opkrævning.  

#### <a name="to-set-up-the-direct-debit-mandate-that-represents-the-customer-agreement"></a>Sådan konfigureres den Direct Debit-betalingsaftale, der repræsenterer kundeaftalen  
1. I feltet **Søg** skal du indtaste **Debitorer** og derefter vælge det relaterede link.  
2. Åbn kortet for den kunde, som du vil konfigurere til SEPA Direct Debit.  
3. Vælg handlingen **Bankkonti**.  
4. I vinduet **Debitors bankkontooversigt** skal du vælge den debitorbankkonto, som skal bruge Direct Debiter, og derefter vælge **Direct Debit-betalingsaftaler** under fanen **Startside** i gruppen **Proces**.  
5. I vinduet **SEPA Direct Debit-betalingsaftaler** skal du udfylde felterne som beskrevet i følgende tabel.  

    |Felt|Beskrivelse|  
    |---------------------------------|---------------------------------------|  
    |**Debitors bankkontokode**|Angiver den bankkonto, hvorfra der opkræves Direct Debit\-betalinger. Dette felt udfyldes automatisk.|  
    |**Gyldig fra**|Angiv den dato, hvor Direct Debit\-betalingsaftalen starter.|  
    |**Gyldig til**|Angiv den dato, hvor Direct Debit\-betalingsaftalen slutter.|  
    |**Underskriftsdato**|Angiv den dato, når kunden har underskrevet Direct Debit\-betalingsaftalen.|  
    |**Betalingstype**|Angiv, om aftalen dækker flere (**Tilbagevendende betaling**) eller en enkelt (**Engangsbetaling**) Direct Debit-opkrævning.|  
    |**Forventet antal debiteringer**|Angiv, hvor mange Direct Debit-opkrævninger du forventer at foretage. Dette felt er kun relevant, hvis du har markeret **Tilbagevendende betaling** i feltet **Betalingstype**.|  
    |**Debettæller**|Angiver, hvor mange Direct Debit\-opkrævninger, der er foretaget ved hjælp af denne Direct Debit\-betalingsaftale. Dette felt opdateres automatisk.|  
    |**Spærret**|Angiv, at der ikke kan foretages Direct Debit\-opkrævninger ved hjælp af denne Direct Debit\-betalingsaftale.|  

6.  Gentag trin 1 til 5 for alle de debitorer, som du vil konfigurere til SEPA Direct Debit.  

 Direct Debit-betalingsaftalen indsættes automatisk i feltet **Id for Direct Debit-betalingsaftale**, når du opretter en salgsfaktura til den debitor, som du valgte i trin 2. Du kan finde flere oplysninger i [Oprette gentagne salgs- og købslinjer](sales-how-work-standard-lines.md).  

## <a name="see-also"></a>Se også  
[Indhente betalinger med SEPA Direct Debit](finance-collect-payments-with-sepa-direct-debit.md)  
[Konfigurere dataudvekslingsdefinitioner](across-how-to-set-up-data-exchange-definitions.md)
[Oprette gentagne salgs- og købslinjer](sales-how-work-standard-lines.md)
[Udveksle data elektronisk](across-data-exchange.md)

