---
title: Designoplysninger – Varebogføring | Microsoft Docs
description: For hver lagertransaktion, f.eks. en købsleverance eller en salgsleverance, bogføres der to forskellige typer poster.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 06/19/2020
ms.author: sgroespe
ms.openlocfilehash: 0603e98bcbfb834de3ab96dcb73f3e33e22e0f0b
ms.sourcegitcommit: ec3034640ed10e0fd028568ec45f21c84498d3de
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 06/19/2020
ms.locfileid: "3486467"
---
# <a name="design-details-inventory-posting"></a>Designoplysninger: Varekladde

For hver lagertransaktion, f.eks. en købsleverance eller en salgsleverance, bogføres der to forskellige typer poster.  

|Posttype|Beskrivelse|  
|----------|-----------|  
|Antal|Afspejler ændringen af lagermængden. Disse oplysninger lagres i vareposter.<br /><br /> Ledsaget af vareudligningsposter.|  
|Værdi|Afspejler ændringen af lagerværdien. Disse oplysninger lagres i værdiposter.<br /><br /> Der kan være en eller flere værdiposter for hver varepost eller kapacitetspost.<br /><br /> Du kan finde flere oplysninger om kapacitetsværdiposter, der er relateret til brugen af produktions- eller montageressourcer, i [Designoplysninger: Bogføring af produktionsordre](design-details-production-order-posting.md).|  

 Vareudligningsposter findes i forhold til antal posteringer for at knytte en lagerforøgelse til lagerreducering. Dette gør det muligt for prisberegningsprogrammet at overføre omkostninger fra forøgelser til relaterede reduceringer og omvendt. Du kan finde flere oplysninger i [Designoplysninger: Vareudligning](design-details-item-application.md).  

 Vareposter, værdiposter og vareudligningsposter oprettes som følge af bogføring af en varekladdelinje enten indirekte ved bogføring af en ordrelinje eller direkte på siden Varekladde.  

 Med jævne mellemrum bogføres værdiposter, der er oprettet i lageropgørelsesposter, til finans for at afstemme de to posttyper af økonomiske kontrolårsager. Du kan finde flere oplysninger i [Designoplysninger: Afstemning med Finans](design-details-reconciliation-with-the-general-ledger.md).  

 ![Posteringsflow ved afstemning af lager med Finans](media/design_details_inventory_costing_1_entry_flow.png "Posteringsflow ved afstemning af lager med Finans")  

## <a name="example"></a>Eksempel

Følgende eksempel viser, hvordan vareposter, værdiposter og vareudligningsposter resulterer i finansposter.  

 Du kan bogføre en købsordre som modtaget og faktureret for 10 varer med en købspris på RV 7 og et IPO-bidrag på RV 1. Bogføringsdatoen er 01-01-20. Der oprettes følgende poster.  

### <a name="item-ledger-entries-1"></a>Vareposter (1)

|Bogføringsdato|Postens type|Kostbeløb (faktisk)|Antal|Løbenr.|  
|------------|----------|--------------------|--------|---------|  
|01-01-20|Køb|80,00|10|1|  

### <a name="value-entries-1"></a>Værdiposter (1)

|Bogføringsdato|Postens type|Kostbeløb (faktisk)|Varepostløbenr.|Løbenr.|  
|------------|----------|--------------------|---------------------|---------|  
|01-01-20|Købspris|70.00|1|1|  
|01-01-20|Indirekte omkostning|10,00|1|2|  

### <a name="item-application-entries-1"></a>Vareudligningsposter (1)

|Løbenr.|Varepostløbenr.|Indgående varepostløbenr.|Udgående varepostløbenr.|Antal|  
|---------|---------------------|----------------------|-----------------------|--------|  
|1|1|1|0|10|  

 Derefter skal bogføre du et salg på 10 enheder af varen med bogføringsdatoen 15-01-20.  

### <a name="item-ledger-entries-2"></a>Vareposter (2)

|Bogføringsdato|Postens type|Kostbeløb (faktisk)|Antal|Løbenr.|  
|------------|----------|--------------------|--------|---------|  
|01-15-20|Salg|-80,00|-10|2|  

### <a name="value-entries-2"></a>Værdiposter (2)

|Bogføringsdato|Postens type|Kostbeløb (faktisk)|Varepostløbenr.|Løbenr.|  
|------------|----------|--------------------|---------------------|---------|  
|01-15-20|Købspris|-80,00|2|3|  

### <a name="item-application-entries-2"></a>Vareudligningsposter (2)

|Løbenr.|Varepostløbenr.|Indgående varepostløbenr.|Udgående varepostløbenr.|Antal|  
|---------|---------------------|----------------------|-----------------------|--------|  
|2|2|1|2|-10|  

I slutningen af regnskabsperioden skal du udføre kørslen **Bogfør lagerregulering** for at afstemme disse lagertransaktioner i Finans.  

 Du kan finde flere oplysninger i [Designoplysninger: Konti i Finans](design-details-accounts-in-the-general-ledger.md).  

 Følgende tabeller viser resultatet af afstemning af lagertransaktioner i dette eksempel med finans.  

### <a name="value-entries-3"></a>Værdiposter (3)  

|Bogføringsdato|Postens type|Kostbeløb (faktisk)|Bogført kostværdi|Varepostløbenr.|Løbenr.|  
|------------|----------|--------------------|------------------|---------------------|---------|  
|01-01-20|Købspris|70.00|70.00|1|1|  
|01-01-20|Indirekte omkostning|10,00|10,00|1|2|  
|01-15-20|Købspris|-80,00|-80,00|2|3|  

### <a name="general-ledger-entries-3"></a>Finansposter (3)

|Bogføringsdato|Finanskonto|Kontonummer (En-US Demo)|Beløb|Løbenr.|  
|------------|-----------|------------------------|------|---------|  
|01-01-20|[Lagerkonto]|2130|70.00|1|  
|01-01-20|[Tillagte dir. omkost.konto]|7291|-70,00|2|  
|01-01-20|[Lagerkonto]|2130|10,00|3|  
|01-01-07|[Tillagte indir. prod.omkost.konto]|7292|-10,00|4|  
|01-15-20|[Lagerkonto]|2130|-80,00|5|  
|01-15-20|[Vareforbrugskonto]|7290|80,00|6|  

> [!NOTE]  
> Bogføringsdatoen for Finans er den samme som for de relaterede værdiposter.  
> 
> Feltet **Bogført kostværdi** i tabellen **Værdipost** udfyldes.  

 Relationen mellem værdioplysninger og finansposter lagres i tabellen **Finans - varetilknytning**.  

### <a name="relation-entries-in-the-gl--item-ledger-relation-table-3"></a>Relationsposter i finans – relationstabel for varepost (3)

|Finansløbenr.|Værdiløbenr.|Finansjournalnr.|  
|-------------|---------------|----------------|  
|1|1|1|  
|2|1|1|  
|3|2|1|  
|4|2|1|  
|5|3|1|  
|6|3|1|  

## <a name="assembly-and-production-posting"></a>Montage og produktionsbogføring

Kapacitet og ressourceposter repræsenterer den tid, der er bogført som brugt i produktionen eller montagen. Disse behandlingsomkostninger bogføres som værdiposter i finans sammen med de involverede materialeomkostninger på en tilsvarende måde, som beskrevet for vareposter i dette emne.  

Du kan finde flere oplysninger i [Designoplysninger: Bogføring af montageordre](design-details-assembly-order-posting.md).  

## <a name="see-also"></a>Se også

 [Designoplysninger: Lagerkostmetode](design-details-inventory-costing.md)  
 [Designoplysninger: Konti i Finans](design-details-accounts-in-the-general-ledger.md)  
 [Designoplysninger: Omkostningskomponenter](design-details-cost-components.md) [Administrere lageromkostninger](finance-manage-inventory-costs.md)  
 [Finans](finance.md)  
 [Arbejde med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)  
