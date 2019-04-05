---
title: Sådan blokeres salg til debitor varer fra salg eller køb
description: I Business Central kan en vare være markeret som spærret for salg, spærret for køb eller spærret i alle sammenhænge.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/01/2018
ms.author: sgroespe
ms.openlocfilehash: 268d098318b77cb89a369e8edc14729a44bedae6
ms.sourcegitcommit: 1bcfaa99ea302e6b84b8361ca02730b135557fc1
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 03/08/2019
ms.locfileid: "792769"
---
# <a name="block-customers"></a>Blokere debitorer
Du kan spærre en debitor, for eksempel på grund af insolvens, så kunden ikke kan føjes til salgsdokumenter, eller ingen transaktioner kan bogføres for debitoren.

Foruden at blokere for en debitor kan du sætte tilgodehavendetransaktioner for kunden på hold i forbindelse med rykkere. Du kan finde flere oplysninger under [Indhente udestående beløb](receivables-collect-outstanding-balances.md).   

Den følgende tabel beskriver de forskellige blokeringsindstillinger.  

|Indstilling|Beskrivelse|  
|--------------------|------------|  
|**Tomt**|Transaktioner er tilladt for kunden.|
|**Lever**|Der kan ikke oprettes nye ordrer og nye leverancer til kunden. Eksisterende leverancer, der ikke er faktureret, kan faktureres.|  
|**Faktura**|Der kan ikke oprettes nye ordrer, nye leverancer og nye fakturaer til kunden. Eksisterende leverancer, der ikke er faktureret, kan ikke faktureres.|  
|**Alle**|Ingen transaktioner er tilladt for kunden – heller ikke indbetalinger.|  

## <a name="to-block-a-customer"></a>Sådan blokeres en kunde  
1. Vælg ikonet ![Elpære, der åbner funktionen Fortæl mig](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig"), angiv **Debitorer**, og vælg derefter det relaterede link.
2. Vælg en kunde, og vælg derefter handlingen **Rediger**.
3. Udfyld feltet **Spærret** med en af følgende indstillinger, der er beskrevet ovenfor.

## <a name="see-also"></a>Se også  
[Registrere nye debitorer](sales-how-register-new-customers.md)  
[Indhente udestående beløb](receivables-collect-outstanding-balances.md)  
[Administrere tilgodehavender](receivables-manage-receivables.md)  
