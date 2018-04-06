---
title: "Opsætte SEPA-kreditoverførsel | Microsoft Docs"
description: "Få at vide, hvordan du opsætter SEPA-kreditoverførsel i Business Central."
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: sepa, credit, transfer, payment,
ms.date: 08/21/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: d7fb34e1c9428a64c71ff47be8bcff174649c00d
ms.openlocfilehash: 64abd01caa2a2f6845bb3d54c7721333a0a360b3
ms.contentlocale: da-dk
ms.lasthandoff: 03/22/2018

---
# <a name="set-up-sepa-credit-transfer"></a>Opsætte SEPA-kreditoverførsel
Fra vinduet **Udbetalingskladde** kan du eksportere betalinger til en fil til overførsel til din elektroniske bank til behandling af de relaterede pengeoverførsler. [!INCLUDE[d365fin](includes/d365fin_md.md)] understøtter SEPA-kreditoverførselsformatet, men i dit land/område anvendes der muligvis andre formater til elektroniske betalinger.  

For at aktivere eksport af bankfilformater, der ikke umiddelbart understøttes i [!INCLUDE[d365fin](includes/d365fin_md.md)], kan du konfigurere en dataudvekslingsdefinition ved hjælp af dataudvekslingsstrukturen. Du kan finde flere oplysninger i [Konfigurere dataudvekslingsdefinitioner](across-how-to-set-up-data-exchange-definitions.md).  

Før du kan behandle betalingen elektronisk ved eksport af betalingsfiler i formatet SEPA-kreditoverførsel, skal du udføre følgende trin:  

* Konfigurere bankkontoen til at håndtere formatet SEPA-kreditoverførsel  
* Konfigurere kreditorkortene for at behandle betalinger ved at eksportere filer i formatet SEPA-kreditoverførsler  
* Konfigurere den relaterede finanskladde til at aktivere betalingseksport fra vinduet **Udbetalingskladde**  
* Forbinde dataudvekslingsdefinitionen for en eller flere betalingstyper med den eller de relevante betalingsmetode(r)  

### <a name="to-set-up-a-bank-account-for-sepa-credit-transfer"></a>Sådan opsættes en konto til SEPA-kreditoverførsler  
1. I feltet **Søg** skal du indtaste **Bankkonti** og derefter vælge det relaterede link.  
2. Åbn kortet for den bankkonto, som du vil eksportere betalingsfiler fra i formatet SEPA-kreditoverførsler.  
3. I oversigtspanelet **Overfør** i feltet **Format til eksport af betaling** skal du vælge **SEPADD**.  
4. I feltet **Nr.serie f. medd.-id for SEPA-kreditoverf.** skal du vælge en nummerserie, hvorfra numre tildeles SEPA kreditoverførselsposter.  
5. Sørg for, at feltet **IBAN** er udfyldt.  

    > [!NOTE]  
    >  Feltet **Valutakode** skal indstilles til **EUR**, da SEPA-kreditoverførsler kun kan foretages i EURO-valuta.  

### <a name="to-set-up-a-vendor-card-for-sepa-credit-transfer"></a>Sådan opsættes et kreditorkort til SEPA-kreditoverførsler  
1. I feltet **Søg** skal du angive **Leverandører** og derefter vælge det relaterede link.  
2. Åbn kortet for den kreditor, som du vil betale elektronisk ved at eksportere betalingsfiler i formatet SEPA-kreditoverførsler.  
3. I oversigtspanelet **Betaling** i feltet **Betalingsformkode** skal du vælge **BANK**.  
4. I feltet **Foretrukken bankkontokode** skal du vælge den bank, som pengene skal overføres til, når de behandles af din elektroniske bank.  

     Værdien i feltet **Foretrukken bankkontokode** kopieres til feltet **Modtagers bankkonto** i vinduet **Udbetalingskladde**.  

### <a name="to-set-the-payment-journal-up-to-export-payment-files"></a>Sådan opsættes betalingskladden til eksport af betalingsfiler  
1. Indtast **Udbetalingskladder** i feltet **Søg**, og vælg derefter det relaterede link.  
2. Åbn den betalingskladde, som du kan bruge til at behandle betalinger ved at eksportere filer i formatet SEPA-kreditoverførsler.  
3. Vælg rulle\-knappen i feltet **Kladdenavn**.  
4. I vinduet **Finanskladdenavne** under fanen **Startside** skal du i gruppen **Administrer** vælge **Rediger liste**.  
5. Markér afkrydsningsfeltet **Tillad eksport af betaling** på linjen for den betalingskladde, som du vil bruge til eksport af betalinger.  

### <a name="to-connect-the-data-exchange-definition-for-one-or-more-payment-types-with-the-relevant-payment-method-or-methods"></a>Sådan forbindes dataudvekslingsdefinitionen for en eller flere betalingstyper med den eller de relevante betalingsmetode(r)  
1. I feltet **Søg** skal du angive **Betalingsformer** og derefter vælge det relaterede link.  
2. I vinduet **Betalingsformer** skal du vælge den betalingsmåde, der bruges til eksport af betalinger fra, og derefter vælge feltet **Definition af betalingseksportlinje**.  
3. I vinduet **Definitioner af betalingseksportlinjer** skal du vælge den kode, du angav i feltet **Kode** i oversigtspanelet **Linjedefinitioner** i trin 4 i afsnittet "Sådan beskrives formateringen af linjer og kolonner i filen" i [Konfigurere dataudvekslingsdefinitioner](across-how-to-set-up-data-exchange-definitions.md).  

    Direct Debit-betalingsaftalen indsættes automatisk i feltet **Id for Direct Debit-betalingsaftale**, når du opretter en salgsfaktura til den debitor, som du valgte i trin 2. Du kan finde flere oplysninger i [Oprette gentagne salgs- og købslinjer](sales-how-work-standard-lines.md).  

## <a name="see-also"></a>Se også  
[Indhente betalinger med SEPA Direct Debit](finance-collect-payments-with-sepa-direct-debit.md)  
[Konfigurere dataudvekslingsdefinitioner](across-how-to-set-up-data-exchange-definitions.md)  
[Oprette gentagne salgs- og købslinjer](sales-how-work-standard-lines.md)  
[Udveksle data elektronisk](across-data-exchange.md)  

