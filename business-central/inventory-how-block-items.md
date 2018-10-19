---
title: "Sådan spærres varer mod salg eller køb"
description: "I Business Central kan en vare være markeret som spærret for salg, spærret for køb eller spærret i alle sammenhænge."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 10/01/2018
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 9dbd92409ba02281f008246194f3ce0c53e4e001
ms.openlocfilehash: 0d5ad688cfa6fb58e8383692362105beeee386f8
ms.contentlocale: da-dk
ms.lasthandoff: 09/28/2018

---
# <a name="block-items-from-sales-or-purchasing"></a>Spærre varer mod salg eller køb
Du kan spærre for, at en vare angives på salgs- eller købslinjer og for, at den bogføres i nogen posteringer.  

Tabellen nedenfor viser, hvad der sker, når varer spærres.  

|Indstilling|Beskrivelse|  
|--------------------|------------|  
|**Spærret salg**|Du kan ikke angive varen i et salgsdokument eller i en salgsvarekladde.|  
|**Spærret køb**|Du kan ikke angive varen i et købsdokument, i en købsvarekladde eller i købsplanlægningsprocesser.|  
|**Spærret**|Du kan ikke bruge varen til nogen varetransaktioner. Du kan finde flere oplysninger om spærring af en vare i alle sammenhænge på varekortet.|  

## <a name="to-block-an-item-from-being-entered-on-sales-lines"></a>Sådan spærrer du for, at en vare kan angives på salgslinjer  

1.  Vælg ikonet ![Elpære, der åbner funktionen Fortæl mig](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig"), angiv **Varer**, og vælg derefter det relaterede link.  
2.  Vælg den vare, du vil spærre, og marker derefter afkrydsningsfeltet **Spærret salg**.  

Hvis du forsøger at angive varen på et salgsdokument eller kladdelinje, får du nu en fejlmeddelelse om, at varen er spærret.

## <a name="to-block-an-item-from-being-entered-on-purchase-lines"></a>Sådan spærrer du for, at en vare kan angives på købslinjer  

1.  Vælg ikonet ![Elpære, der åbner funktionen Fortæl mig](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig"), angiv **Varer**, og vælg derefter det relaterede link.  
2.  Vælg den vare, du vil spærre, og marker derefter afkrydsningsfeltet **Spærret køb**.  

Hvis du forsøger at angive varen på et købsdokument eller kladdelinje, får du nu en fejlmeddelelse om, at varen er spærret.

## <a name="to-block-an-item-from-being-posted"></a>Sådan spærrer du for, at en vare kan bogføres
1. Vælg ikonet ![Elpære, der åbner funktionen Fortæl mig](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig"), angiv **Varer**, og vælg derefter det relaterede link.
2. Vælg den vare, du vil spærre, og marker derefter afkrydsningsfeltet **Spærret**.

Hvis du forsøger at bogføre en transaktionstype for varen, får du nu en fejlmeddelelse om, at varen er spærret.

## <a name="see-also"></a>Se også  
[Registrere nye varer](inventory-how-register-new-items.md)  
[Lagerbeholdning](inventory-manage-inventory.md)  

