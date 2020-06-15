---
title: Sådan spærres varer mod salg eller køb
description: Du kan forhindre, at en vare bliver brugt, f.eks. på salgs- eller købsdokumenter.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/01/2020
ms.author: sgroespe
ms.openlocfilehash: 467b43b14f1905018c2a26a06c15abc5a0a17e99
ms.sourcegitcommit: 4545bb597dd9dc4c563b30af762977ee1d815497
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 05/29/2020
ms.locfileid: "3410640"
---
# <a name="block-items-from-sales-or-purchasing"></a>Spærre varer mod salg eller køb
Du kan spærre for, at en vare angives på linjer i salgs- eller købsdokumenter og for, at den bogføres i nogen posteringer. Dette er f.eks. nyttigt, hvis en vare har en kendt defekt. Hvis en person vælger en spærret vare på et salgs- eller købsdokument, vil en meddelelse give dem om, at varen er spærret.

Tabellen nedenfor beskriver, hvad der sker, når varer spærres.  

|Indstilling|Description|  
|--------------------|------------|  
|**Spærret salg**|Du kan ikke angive varen i et salgsdokument eller i en salgsvarekladde.|  
|**Spærret køb**|Du kan ikke angive varen i et købsdokument, i en købsvarekladde eller i købsplanlægningsprocesser.|  
|**Spærret**|Du kan ikke bruge varen til nogen varetransaktioner.|  

> [!NOTE]
> Blokerede varer kan returneres. Det betyder, at ingen af indstillingerne ovenfor gælder, når varen bruges på returvareordrer og kreditnotaer.

Når du bruger funktionen **Kopier fra dokument** til at oprette nye dokumenter, der er baserede på eksisterende dokumenter, vises der en meddelelse, hvis varerne på kildedokumentlinjerne er spærret. De spærrede dokumentlinjer medtages ikke i det nye dokument, og der vises en meddelelse indeholdende en oversigt over alle de dokumentlinjer, der er spærrede i kildedokumentet.

## <a name="to-block-an-item-from-being-entered-on-sales-lines"></a>Sådan spærrer du for, at en vare kan angives på salgslinjer  
1.  Vælg ikonet ![Elpære, der åbner funktionen Fortæl mig](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig"), angiv **Varer**, og vælg derefter det relaterede link.  
2.  Vælg den vare, du vil spærre, og marker derefter afkrydsningsfeltet **Spærret salg**.  

## <a name="to-block-an-item-from-being-entered-on-purchase-lines"></a>Sådan spærrer du for, at en vare kan angives på købslinjer  
1.  Vælg ikonet ![Elpære, der åbner funktionen Fortæl mig](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig"), angiv **Varer**, og vælg derefter det relaterede link.  
2.  Vælg den vare, du vil spærre, og marker derefter afkrydsningsfeltet **Spærret køb**.  

## <a name="to-block-an-item-from-being-posted"></a>Sådan spærrer du for, at en vare kan bogføres
1. Vælg ikonet ![Elpære, der åbner funktionen Fortæl mig](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig"), angiv **Varer**, og vælg derefter det relaterede link.
2. Vælg den vare, du vil spærre, og marker derefter afkrydsningsfeltet **Spærret**.

## <a name="see-also"></a>Se også  
[Registrere nye varer](inventory-how-register-new-items.md)  
[Lagerbeholdning](inventory-manage-inventory.md)  
