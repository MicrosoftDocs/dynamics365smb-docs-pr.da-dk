---
title: Sådan blokeres salg til kunder
description: 'Hvis det er nødvendigt, kan du spærre en kunde, så kunden ikke kan medtages i salgsdokumenter og andre salgstransaktioner.'
author: brentholtorf
ms.topic: conceptual
ms.devlang: al
ms.search.keywords: null
ms.date: 07/05/2024
ms.author: bholtorf
ms.service: dynamics-365-business-central
ms.reviewer: bholtorf
---
# <a name="block-customers"></a>Bloker kunder
Du kan blokere en kunde, f.eks. på grund af insolvens, så kunden ikke kan føjes til salgsdokumenter, eller så der ikke kan bogføres transaktioner for kunden.

Foruden at blokere for en debitor kan du sætte tilgodehavendetransaktioner for kunden på hold i forbindelse med rykkere. Du kan finde flere oplysninger i [Indhente udestående beløb](receivables-collect-outstanding-balances.md).   

Den følgende tabel beskriver indstillingerne for spærring af kunder.  

|Indstilling|Beskrivelse|  
|--------------------|------------|  
|**Tomt**|Transaktioner er tilladt for kunden.|
|**Lever**|Der kan ikke oprettes nye ordrer og nye leverancer til kunden. Eksisterende leverancer, der ikke er faktureret, kan faktureres.|  
|**Faktura**|Der kan ikke oprettes nye ordrer, nye leverancer og nye fakturaer til kunden. Eksisterende leverancer, der endnu ikke er faktureret, kan ikke faktureres. Du kan stadig sende rykkere og rentenotaer til kunden.|  
|**Alle**|Ingen transaktioner er tilladt for kunden – heller ikke indbetalinger.|  

## <a name="to-block-a-customer"></a>Sådan blokeres en kunde
1. Vælg ![Lightbulb, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **Kunder**, og vælg derefter det relaterede link.
2. Vælg en kunde, og vælg derefter handlingen **Rediger**.
3. I feltet **Spærret** skal du vælge, hvad der skal spærres, som beskrevet i tabellen ovenfor.

## <a name="see-also"></a>Se også
[Registrere nye debitorer](sales-how-register-new-customers.md)  
[Indhente udestående beløb](receivables-collect-outstanding-balances.md)  
[Administrere tilgodehavender](receivables-manage-receivables.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
