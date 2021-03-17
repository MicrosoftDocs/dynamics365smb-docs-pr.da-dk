---
title: Sådan udskrives en rapport til afstemning af moms | Microsoft Docs
description: I Business Central kan du bruge rapporten Momsafstemning til at få vist en oversigt over finanskonti med deres grundlæggende beløb og momsbeløb. Disse beløb er grupperet efter moms-type for at hjælpe med afstemningen for afregning af moms.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.search.keywords: ''
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: 49f4241d1baa4d4c9872d10dd78fd6a492fcedab
ms.sourcegitcommit: ff2b55b7e790447e0c1fcd5c2ec7f7610338ebaa
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 02/15/2021
ms.locfileid: "5379459"
---
# <a name="print-vat-reconciliation-reports"></a>Udskrive rapporter til afstemning af moms
I [!INCLUDE[prod_short](../../includes/prod_short.md)] kan du bruge rapporten **Momsafstemning** til at få vist en oversigt over finanskonti med deres grundlæggende beløb og momsbeløb. Disse beløb er grupperet efter moms-type for at hjælpe med afstemningen for afregning af moms.  

### <a name="to-print-a-vat-reconciliation-report"></a>Sådan udskrives en momsafstemningsrapport  

1.  Vælg ikonet ![Elpære, der åbner funktionen Fortæl mig](../../media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig"), åbn **Momsafstemning**, og vælg derefter det relaterede link.  
2.  I oversigtspanelet **Indstillinger** skal du udfylde felterne som beskrevet i følgende tabel.  

    |Felt|Beskrivelse|  
    |---------------------------------|---------------------------------------|  
    |**Vis detaljer**|Vælg for at udskrive alle transaktionsbeløb i rapporten.<br /><br /> Hvis du ikke markerer feltet, udskrives en enkelt akkumuleret linje for hver finanskonto.|  
    |**Vis transaktioner uden moms**|Vælg for at udskrive en linje for hver finanskonto, som transaktioner bogføres på. Du kan bruge denne indstilling for både enkelte konti og flere konti.<br /><br /> Standardværdien er **Nej**. Rapporten indeholder kun de transaktioner, der omfatter momsposter. Hvis du markerer dette felt, medtager rapporten alle posteringer.|  

3.  I oversigtspanelet **Finanspost** skal du vælge de relevante filtre.  
4.  Vælg **Udskriv** for at udskrive rapporten, eller vælg **Vis udskrift** for at se den på skærmen.  

## <a name="see-also"></a>Se også  
 [Lokal funktionalitet for Danmark](denmark-local-functionality.md)  


[!INCLUDE[footer-include](../../includes/footer-banner.md)]