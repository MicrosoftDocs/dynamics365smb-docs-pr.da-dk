---
title: Sådan blokeres salg til debitor varer fra salg eller køb
description: I Business Central kan en vare være markeret som spærret for salg, spærret for køb eller spærret i alle sammenhænge.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/01/2019
ms.author: sgroespe
ms.openlocfilehash: c1b055e5101b99f0b0e1b69169d5c9f2f7e21d09
ms.sourcegitcommit: cfc92eefa8b06fb426482f54e393f0e6e222f712
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 12/03/2019
ms.locfileid: "2882990"
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
