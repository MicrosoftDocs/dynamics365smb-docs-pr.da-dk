---
title: Sådan spærres varer mod salg eller køb
description: 'Du kan spærre for, at en vare angives på linjer i salgs- eller købsdokumenter og for, at den bogføres i nogen posteringer.'
author: brentholtorf
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: null
ms.date: 11/03/2022
ms.author: bholtorf
---
# <a name="block-items-from-sales-or-purchasing"></a>Spærre varer mod salg eller køb

Du kan spærre for, at en vare angives på linjer i salgs- eller købsdokumenter og for, at den bogføres i posteringer. Dette er f.eks. nyttigt, hvis en vare har en kendt defekt. Hvis en person vælger en spærret vare på et salgs- eller købsdokument, vil en meddelelse give dem om, at varen er spærret.

Tabellen nedenfor beskriver, hvad der sker, når varer spærres.  

|Indstilling|Beskrivelse|  
|--------------------|------------|  
|**Spærret salg**|Du kan ikke angive varen i et salgsdokument eller i en salgsvarekladde.|  
|**Spærret køb**|Du kan ikke angive varen i et købsdokument, i en købsvarekladde eller i købsplanlægningsprocesser.|  
|**Spærret**|Du kan ikke medtage varen i transaktioner.|  

> [!NOTE]
> Blokerede varer kan returneres. Det betyder, at ingen af indstillingerne ovenfor gælder på returvareordrer og kreditnotaer.

Når du bruger handlingen **Kopier fra dokument** til at oprette nye dokumenter, der er baserede på eksisterende dokumenter, vises der en meddelelse, hvis varerne på kildedokumentlinjerne er spærret. De spærrede dokumentlinjer medtages ikke i det nye dokument, og der vises en meddelelse indeholdende en oversigt over alle de dokumentlinjer, der er spærrede i kildedokumentet.

## <a name="to-block-an-item-from-being-entered-on-sales-lines"></a>Sådan spærrer du for, at en vare kan angives på salgslinjer

1. Vælg ![Lightbulb, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **Varer**, og vælg derefter det relaterede link.  
2. Vælg den vare, du vil spærre, og marker derefter afkrydsningsfeltet **Spærret salg**.  

## <a name="to-block-an-item-from-being-entered-on-purchase-lines"></a>Sådan spærrer du for, at en vare kan angives på købslinjer

1. Vælg ![Lightbulb, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **Varer**, og vælg derefter det relaterede link.  
2. Vælg den vare, du vil spærre, og marker derefter afkrydsningsfeltet **Spærret køb**.  

## <a name="to-block-an-item-from-being-posted"></a>Sådan spærrer du for, at en vare kan bogføres

1. Vælg ![Lightbulb, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **Varer**, og vælg derefter det relaterede link.
2. Vælg den vare, du vil spærre, og marker derefter afkrydsningsfeltet **Spærret**.

## <a name="see-also"></a>Se også

[Registrere nye varer](inventory-how-register-new-items.md)  
[Lagerbeholdning](inventory-manage-inventory.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
