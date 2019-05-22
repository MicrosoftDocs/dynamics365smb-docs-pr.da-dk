---
title: Sådan udskrives en rapport til afstemning af moms | Microsoft Docs
description: I Business Central kan du bruge rapporten Momsafstemning til at få vist en oversigt over finanskonti med deres grundlæggende beløb og momsbeløb. Disse beløb er grupperet efter moms-type for at hjælpe med afstemningen for afregning af moms.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.search.keywords: ''
ms.date: 04/01/2019
ms.author: sgroespe
ms.openlocfilehash: f63bdb46b94949420532c86a30f1491f02e1bd3b
ms.sourcegitcommit: 60b87e5eb32bb408dd65b9855c29159b1dfbfca8
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 04/29/2019
ms.locfileid: "1237749"
---
# <a name="print-vat-reconciliation-reports"></a>Udskrive rapporter til afstemning af moms
I [!INCLUDE[d365fin](../../includes/d365fin_md.md)] kan du bruge rapporten **Momsafstemning** til at få vist en oversigt over finanskonti med deres grundlæggende beløb og momsbeløb. Disse beløb er grupperet efter moms-type for at hjælpe med afstemningen for afregning af moms.  

### <a name="to-print-a-vat-reconciliation-report"></a>Sådan udskrives en momsafstemningsrapport  

1.  Vælg ikonet ![Søg efter side eller rapport](../../media/ui-search/search_small.png "Ikonet Søg efter side eller rapport"), angiv **Momsafstemning**, og vælg derefter det relaterede link.  
2.  I oversigtspanelet **Indstillinger** skal du udfylde felterne som beskrevet i følgende tabel.  

    |Felt|Beskrivelse|  
    |---------------------------------|---------------------------------------|  
    |**Vis detaljer**|Vælg for at udskrive alle transaktionsbeløb i rapporten.<br /><br /> Hvis du ikke markerer feltet, udskrives en enkelt akkumuleret linje for hver finanskonto.|  
    |**Vis transaktioner uden moms**|Vælg for at udskrive en linje for hver finanskonto, som transaktioner bogføres på. Du kan bruge denne indstilling for både enkelte konti og flere konti.<br /><br /> Standardværdien er **Nej**. Rapporten indeholder kun de transaktioner, der omfatter momsposter. Hvis du markerer dette felt, medtager rapporten alle posteringer.|  

3.  I oversigtspanelet **Finanspost** skal du vælge de relevante filtre.  
4.  Vælg **Udskriv** for at udskrive rapporten, eller vælg **Vis udskrift** for at se den på skærmen.  

## <a name="see-also"></a>Se også  
 [Lokal funktionalitet for Danmark](denmark-local-functionality.md)  
