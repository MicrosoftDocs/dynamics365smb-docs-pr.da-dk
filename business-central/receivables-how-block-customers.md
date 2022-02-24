---
title: Sådan spærrer du salg til kunder
description: Hvis det er nødvendigt, kan du spærre en kunde, så kunden ikke kan medtages i salgsdokumenter og andre salgstransaktioner.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/01/2020
ms.author: sgroespe
ms.openlocfilehash: 7cc82ab0aaf28b355117571d0d2cc5869141693f
ms.sourcegitcommit: 4545bb597dd9dc4c563b30af762977ee1d815497
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 05/29/2020
ms.locfileid: "3410712"
---
# <a name="block-customers"></a>Blokere debitorer
Du kan spærre en debitor, for eksempel på grund af insolvens, så kunden ikke kan føjes til salgsdokumenter, eller ingen transaktioner kan bogføres for debitoren.

Foruden at blokere for en debitor kan du sætte tilgodehavendetransaktioner for kunden på hold i forbindelse med rykkere. Du kan finde flere oplysninger under [Indhente udestående beløb](receivables-collect-outstanding-balances.md).   

Den følgende tabel beskriver indstillingerne for spærring af kunder.  

|Indstilling|Description|  
|--------------------|------------|  
|**Tomt**|Transaktioner er tilladt for kunden.|
|**Lever**|Der kan ikke oprettes nye ordrer og nye leverancer til kunden. Eksisterende leverancer, der ikke er faktureret, kan faktureres.|  
|**Faktura**|Der kan ikke oprettes nye ordrer, nye leverancer og nye fakturaer til kunden. Eksisterende leverancer, der ikke er faktureret, kan ikke faktureres. Du kan stadig sende rykkere og rentenotaer til kunden.|  
|**Alle**|Ingen transaktioner er tilladt for kunden – heller ikke indbetalinger.|  

## <a name="to-block-a-customer"></a>Sådan blokeres en kunde  
1. Vælg ikonet ![Elpære, der åbner funktionen Fortæl mig](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig"), angiv **Debitorer**, og vælg derefter det relaterede link.
2. Vælg en kunde, og vælg derefter handlingen **Rediger**.
3. I feltet **Spærret** skal du vælge, hvad der skal spærres, som beskrevet i tabellen ovenfor.

## <a name="see-also"></a>Se også  
[Registrere nye debitorer](sales-how-register-new-customers.md)  
[Indhente udestående beløb](receivables-collect-outstanding-balances.md)  
[Administrere tilgodehavender](receivables-manage-receivables.md)  
