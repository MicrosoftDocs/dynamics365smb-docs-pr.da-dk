---
title: Designoplysninger – Varebogføring | Microsoft Docs
description: 'For hver lagertransaktion, f.eks. en købsleverance eller en salgsleverance, bogføres der to forskellige typer poster.'
author: brentholtorf
ms.topic: conceptual
ms.devlang: al
ms.search.keywords: null
ms.date: 06/08/2021
ms.author: bholtorf
ms.service: dynamics-365-business-central
ms.reviewer: bholtorf
---
# Designoplysninger: Varekladde

For hver lagertransaktion, f.eks. en købsleverance eller en salgsleverance, bogføres der to forskellige typer poster.  

|Posttype|Beskrivelse|  
|----------|-----------|  
|Antal|Afspejler ændringen af lagermængden. Disse oplysninger lagres i vareposter.<br /><br /> Ledsaget af vareudligningsposter.|  
|Værdi|Afspejler ændringen af lagerværdien. Disse oplysninger lagres i værdiposter.<br /><br /> Der kan være en eller flere værdiposter for hver varepost eller kapacitetspost.<br /><br /> Du kan finde flere oplysninger om kapacitetsværdiposter, der er relateret til brugen af produktions- eller montageressourcer, i [Designoplysninger: Bogføring af produktionsordre](design-details-production-order-posting.md).|  

 Vareudligningsposter findes i forhold til antal posteringer for at knytte en lagerforøgelse til lagerreducering. Dette gør det muligt for prisberegningsprogrammet at overføre omkostninger fra forøgelser til relaterede reduceringer og omvendt. Du kan finde flere oplysninger i [Designoplysninger: Vareudligning](design-details-item-application.md).  

 Vareposter, værdiposter og vareudligningsposter oprettes som følge af bogføring af en varekladdelinje enten indirekte ved bogføring af en ordrelinje eller direkte på siden Varekladde.  

 Med jævne mellemrum bogføres værdiposter, der er oprettet i lageropgørelsesposter, til finans for at afstemme de to posttyper af økonomiske kontrolårsager. Du kan finde flere oplysninger i [Designoplysninger: Afstemning med Finans](design-details-reconciliation-with-the-general-ledger.md).  

 ![Posteringsflow ved afstemning af lager med Finans.](media/design_details_inventory_costing_1_entry_flow.png "Posteringsflow ved afstemning af lager med Finans")  

## Eksempel

Følgende eksempel viser, hvordan vareposter, værdiposter og vareudligningsposter resulterer i finansposter.  

 Du kan bogføre en købsordre som modtaget og faktureret for 10 varer med en købspris på RV 7 og et IPO-bidrag på RV 1. Bogføringsdatoen er 01-01-20. Der oprettes følgende poster.  

### Vareposter (1)

|Bogføringsdato|Postens type|Kostbeløb (faktisk)|Antal|Løbenr.|  
|------------|----------|--------------------|--------|---------|  
|01-01-20|Køb|80,00|10|1|  

### Værdiposter (1)

|Bogføringsdato|Postens type|Kostbeløb (faktisk)|Varepostløbenr.|Løbenr.|  
|------------|----------|--------------------|---------------------|---------|  
|01-01-20|Købspris|70.00|1|1|  
|01-01-20|Indirekte omkostning|10,00|1|2|  

### Vareudligningsposter (1)

|Løbenr.|Varepostløbenr.|Indgående varepostløbenr.|Udgående varepostløbenr.|Antal|  
|---------|---------------------|----------------------|-----------------------|--------|  
|1|1|1|0|10|  

 Derefter skal bogføre du et salg på 10 enheder af varen med bogføringsdatoen 15-01-20.  

### Vareposter (2)

|Bogføringsdato|Postens type|Kostbeløb (faktisk)|Antal|Løbenr.|  
|------------|----------|--------------------|--------|---------|  
|01-15-20|Salg|-80,00|-10|2|  

### Værdiposter (2)

|Bogføringsdato|Postens type|Kostbeløb (faktisk)|Varepostløbenr.|Løbenr.|  
|------------|----------|--------------------|---------------------|---------|  
|01-15-20|Købspris|-80,00|2|3|  

### Vareudligningsposter (2)

|Løbenr.|Varepostløbenr.|Indgående varepostløbenr.|Udgående varepostløbenr.|Antal|  
|---------|---------------------|----------------------|-----------------------|--------|  
|2|2|1|2|-10|  

I slutningen af regnskabsperioden skal du udføre kørslen **Bogfør lagerregulering** for at afstemme disse lagertransaktioner i Finans.  

 Du kan finde flere oplysninger i [Designoplysninger: Konti i Finans](design-details-accounts-in-the-general-ledger.md).  

 Følgende tabeller viser resultatet af afstemning af lagertransaktioner i dette eksempel med finans.  

### Værdiposter (3)  

|Bogføringsdato|Postens type|Kostbeløb (faktisk)|Bogført kostværdi|Varepostløbenr.|Løbenr.|  
|------------|----------|--------------------|------------------|---------------------|---------|  
|01-01-20|Købspris|70.00|70.00|1|1|  
|01-01-20|Indirekte omkostning|10,00|10,00|1|2|  
|01-15-20|Købspris|-80,00|-80,00|2|3|  

### Finansposter (3)

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

### Relationsposter i finans – relationstabel for varepost (3)

|Finansløbenr.|Værdiløbenr.|Finansjournalnr.|  
|-------------|---------------|----------------|  
|1|1|1|  
|2|1|1|  
|3|2|1|  
|4|2|1|  
|5|3|1|  
|6|3|1|  

## Montage og produktionsbogføring

Kapacitet og ressourceposter repræsenterer den tid, der er bogført som brugt i produktionen eller montagen. Disse behandlingsomkostninger bogføres som værdiposter i finans sammen med de involverede materialeomkostninger på en tilsvarende måde, som beskrevet for vareposter i dette emne.  

Du kan finde flere oplysninger i [Designoplysninger: Bogføring af montageordre](design-details-assembly-order-posting.md).  

## Se også

 [Designoplysninger: Lagerkostmetode](design-details-inventory-costing.md)  
 [Designoplysninger: Konti i Finans](design-details-accounts-in-the-general-ledger.md)  
 [Designoplysninger: Omkostningskomponenter](design-details-cost-components.md) [Administrere lageromkostninger](finance-manage-inventory-costs.md)  
 [Finans](finance.md)  
 [Arbejd med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]