---
title: Sådan blokeres varer eller varevarianter fra salg eller køb
description: 'Du kan blokere for, at varer og varevarianter ikke angives på linjer i salgs- eller købsdokumenter eller bogføres i en transaktion.'
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bholtorf
ms.topic: conceptual
ms.search.keywords: 'item, variant, product'
ms.date: 05/16/2024
ms.service: dynamics-365-business-central
---

# <a name="block-items-or-item-variants-from-sales-or-purchasing"></a>Blokere varer eller varevarianter fra salg eller køb

Du kan blokere varer og varevarianter fra at blive angivet på linjer i salgs- eller købsdokumenter og for, at den bogføres i nogen transaktioner. Dette er f.eks. nyttigt, hvis en vare har en kendt defekt. Hvis en person vælger en spærret vare eller variant på et salgs- eller købsdokument, vil en meddelelse give dem om, at varen er spærret.

Tabellen nedenfor beskriver, hvad der sker, når varer eller varianter spærres.  

|Indstilling|Beskrivelse|  
|--------------------|------------|  
|**Salg er spærret**|Du kan ikke angive varen eller varianten i et salgsdokument eller i en salgsvarekladde.|  
|**Indkøb er spærret**|Du kan ikke angive varen eller varianten i et købsdokument, i en købsvarekladde eller i købsplanlægningsprocesser.|  
|**Spærret**|Du kan ikke medtage varen eller varianten, når du bogfører transaktioner.|  

> [!NOTE]
> Blokerede varer kan returneres. Det betyder, at ingen af indstillingerne ovenfor gælder på returvareordrer og kreditnotaer.

Når du bruger handlingen **Kopier fra dokument** til at oprette nye dokumenter, der er baserede på eksisterende dokumenter, vises der en meddelelse, hvis varerne eller varianterne på kildedokumentlinjerne er spærret. De spærrede dokumentlinjer medtages ikke i det nye dokument, og der vises en meddelelse indeholdende en oversigt over alle de dokumentlinjer, der er spærrede i kildedokumentet.

## <a name="to-block-an-item"></a>Sådan blokeres en vare

1. Vælg ![Lightbulb, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **Varer**, og vælg derefter det relaterede link.  
2. Afhængigt af, hvad du vil gøre, kan du vælge varen og derefter vælge et eller flere af følgende afkrydsningsfelter.
    * **Spærret**
    * **Salg er spærret**
    * **Indkøb er spærret**  

## <a name="to-block-an-item-variant"></a>Sådan blokeres en varevariant

1. Vælg ![Lightbulb, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **Varer**, og vælg derefter det relaterede link.  
2. Vælg den vare, der har en variant, du vil blokere, vælg **Varianter**, og vælg derefter et eller flere af følgende afkrydsningsfelter:  
    * **Spærret**
    * **Salg er spærret**
    * **Indkøb er spærret**

## <a name="see-also"></a>Se også

[Registrere nye varer](inventory-how-register-new-items.md)  
[Lager](inventory-manage-inventory.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
