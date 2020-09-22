---
title: 'Designoplysninger: Konti i Finans | Microsoft Docs'
description: For at afstemme lager og kapacitetsposterne med finansmodulet, bogføres de relaterede værdiposter til forskellige konti i finans.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/01/2020
ms.author: edupont
ms.openlocfilehash: 408a510e311573f6573eee286508b9f05f0088dc
ms.sourcegitcommit: a80afd4e5075018716efad76d82a54e158f1392d
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 09/09/2020
ms.locfileid: "3788317"
---
# <a name="design-details-accounts-in-the-general-ledger"></a>Designoplysninger: Konti i Finans
For at afstemme lager og kapacitetsposterne med finansmodulet, bogføres de relaterede værdiposter til forskellige konti i finans. Du kan finde flere oplysninger i [Designoplysninger: Afstemning med Finans](design-details-reconciliation-with-the-general-ledger.md).  

## <a name="from-the-inventory-ledger"></a>Fra lagerposten  
Følgende tabel viser forholdet mellem forskellige typer værdiposter for lager og konti og modkonti i finansmodulet.  

|**Vareposttype**|**Værdiposttype**|**Afvigelsestype**|**Forventet kostpris**|**Konto**|**Modkonto**|  
|--------------------------------|--------------------------|-----------------------|-----------------------|-----------------|---------------------------|  
|Køb|Købspris||Ja|Lager (mellemregningskonto)|Lagerperiod.konto (mellemkto.)|  
|Køb|Købspris||Nej|Lagerbeholdning|Tillagte direkte omkostninger|  
|Køb|Indir. omkostninger||Nej|Lagerbeholdning|Tillagte indir. prod.omkostn.|  
|Køb|Varians|Køb|Nej|Lagerbeholdning|Købsafvigelse|  
|Køb|Værdiregulering||Nej|Lagerbeholdning|Lagerregulering|  
|Køb|Afrunding||Nej|Lagerbeholdning|Lagerregulering|  
|Salg|Købspris||Ja|Lager (mellemregningskonto)|Vareforbrug (mellemkto.)|  
|Salg|Købspris||Nej|Lagerbeholdning|VAREFORBRUG|  
|Salg|Værdiregulering||Nej|Lagerbeholdning|Lagerregulering|  
|Salg|Afrunding||Nej|Lagerbeholdning|Lagerregulering|  
|Opregulering, Nedregulering, Overførsel|Købspris||Nej|Lagerbeholdning|Lagerregulering|  
|Opregulering, Nedregulering, Overførsel|Værdiregulering||Nej|Lagerbeholdning|Lagerregulering|  
|Opregulering, Nedregulering, Overførsel|Afrunding||Nej|Lagerbeholdning|Lagerregulering|  
|(Produktion) Forbrug|Købspris||Nej|Lagerbeholdning|Igv. arb|  
|(Produktion) Forbrug|Værdiregulering||Nej|Lagerbeholdning|Lagerregulering|  
|(Produktion) Forbrug|Afrunding||Nej|Lagerbeholdning|Lagerregulering|  
|Montageforbrug|Købspris||Nej|Lagerbeholdning|Lagerregulering|  
|Montageforbrug|Købspris||Nej|Tillagte direkte omkostninger|Lagerregulering|  
|Montageforbrug|Indir. omkostninger||Nej|Tillagte indir. prod.omkostn.|Lagerregulering|  
|(Produktion), afgang|Købspris||Ja|Lager (mellemregningskonto)|Igv. arb|  
|(Produktion), afgang|Købspris||Nej|Lagerbeholdning|Igv. arb|  
|(Produktion), afgang|Indir. omkostninger||Nej|Lagerbeholdning|Tillagte indir. prod.omkostn.|  
|(Produktion), afgang|Varians|Materiel|Nej|Lagerbeholdning|Mat.kost.afvigelse|  
|(Produktion), afgang|Varians|Kapacitet|Nej|Lagerbeholdning|Kap.kost.afvigelse|  
|(Produktion), afgang|Varians|Fra underleverandører|Nej|Lagerbeholdning|Underlev.kostafvigelse|  
|(Produktion), afgang|Varians|Indirekte kap.kostpris|Nej|Lagerbeholdning|Indir. kap.kostprisafv.|  
|(Produktion), afgang|Varians|Indirekte prod.kostpris|Nej|Lagerbeholdning|Indir. prod.kostprisafv.|  
|(Produktion), afgang|Værdiregulering||Nej|Lagerbeholdning|Lagerregulering|  
|(Produktion), afgang|Afrunding||Nej|Lagerbeholdning|Lagerregulering|  
|Montageafgang|Købspris||Nej|Lagerbeholdning|Lagerregulering|  
|Montageafgang|Værdiregulering||Nej|Lagerbeholdning|Lagerregulering|  
|Montageafgang|Indir. omkostninger||Nej|Lagerbeholdning|Tillagte indir. prod.omkostn.|  
|Montageafgang|Varians|Materiel|Nej|Lagerbeholdning|Mat.kost.afvigelse|  
|Montageafgang|Varians|Kapacitet|Nej|Lagerbeholdning|Kap.kost.afvigelse|  
|Montageafgang|Varians|Indirekte kap.kostpris|Nej|Lagerbeholdning|Indir. kap.kostprisafv.|  
|Montageafgang|Varians|Indirekte prod.kostpris|Nej|Lagerbeholdning|Indir. prod.kostprisafv.|  
|Montageafgang|Afrunding||Nej|Lagerbeholdning|Lagerregulering|  

## <a name="from-the-capacity-ledger"></a>Fra kapacitetsposten  
 Følgende tabel viser forholdet mellem forskellige typer værdiposter for kapacitet og konti og modkonti i finansmodulet. Kapacitetsposter repræsenterer arbejdstid i forbindelse med montage- eller produktionsarbejde.  

|**Arbejdstype**|**Kapacitetsposttype**|**Værdiposttype**|**Konto**|**Modkonto**|  
|-------------------|------------------------------------|--------------------------|-----------------|---------------------------|  
|Montage|Ressource|Købspris|Tillagte direkte omkostninger|Lagerregulering|  
|Montage|Ressource|Indirekte omkostning|Tillagte indir. prod.omkostn.|Lagerregulering|  
|Produktion|Produktionsressource/Arbejdscenter|Købspris|VIA-konto|Tillagte direkte omkostninger|  
|Produktion|Produktionsressource/Arbejdscenter|Indirekte omkostning|VIA-konto|Tillagte indir. prod.omkostn.|  

## <a name="assembly-costs-are-always-actual"></a>Montageomkostninger er altid faktiske omkostninger  
 Som vist i tabellen ovenfor, er bogføring af montage ikke repræsenteret i mellemregningskontoer. Dette skyldes, at begrebet igangværende arbejde ikke gælder i montageafgangsbogføring i modsætning til i produktionsafgangsbogføring. Montageomkostninger bogføres kun som faktiske omkostninger, aldrig som forventede omkostninger.  

 Du kan finde flere oplysninger i [Designoplysninger: Bogføring af montageordre](design-details-assembly-order-posting.md).  

## <a name="calculating-the-amount-to-post-to-the-general-ledger"></a>Beregning af det beløb, der skal bogføres til Finans  
 Følgende felter i tabellen **Værdipost** bruges til at beregne det forventede kostbeløb, der bogføres i finans:  

-   Kostbeløb (faktisk)  
-   Bogført kostværdi  
-   Kostbeløb (forventet)  
-   Bogført forventet kostpris  

Følgende tabel viser, hvordan beløbene, der skal bogføres i finansregnskabet, beregnes for de to forskellige omkostningstyper.  

|Omkostningstype|Beregning|  
|---------------|-----------------|  
|Faktisk kostpris|Kostbeløb (Faktisk) – Bogført kostværdi|  
|Forventet kostpris|Kostbeløb (Forventet) – Bogført forventet kostpris|  

## <a name="see-also"></a>Se også  
 [Designoplysninger: Lagerkostmetode](design-details-inventory-costing.md)   
 [Designoplysninger: Varekladde](design-details-inventory-posting.md)   
 [Designoplysninger: Bogføring af forventet kostpris](design-details-expected-cost-posting.md)  
 [Administrere lageromkostninger](finance-manage-inventory-costs.md)  
 [Finans](finance.md)  
 [Arbejde med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)  
