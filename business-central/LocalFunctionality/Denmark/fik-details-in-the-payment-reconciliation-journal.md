---
title: FIK-detaljer i betalingsudligningskladden | Microsoft Docs
description: "Feltet Transaktionstekst på siden **Betalingsudligningskladde** viser oplysninger om automatisk udligning af betalinger ved hjælp af den danske FIK-standard."
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
ms.sourcegitcommit: 33b900f1ac9e295921e7f3d6ea72cc93939d8a1b
ms.openlocfilehash: 4d4dc86f3238fae185d131da58365bcd42e720c3
ms.contentlocale: da-dk
ms.lasthandoff: 11/26/2018

---
# <a name="fik-details-in-the-payment-reconciliation-journal"></a>FIK-detaljer i betalingsudligningskladden
Feltet **Transaktionstekst** på siden **Betalingsudligningskladde** viser oplysninger om automatisk udligning af betalinger ved hjælp af den danske FIK-standard. Du kan finde flere oplysninger i [Afstemme betalinger ved hjælp af automatisk udligning](../../receivables-how-reconcile-payments-auto-application.md).  

 I følgende tabel beskrives seks værdier, der kan vises i feltet **Transaktionstekst**.  

|Transaktionstekst|Beskrivelse|  
|-----------------------------------------|---------------------------------------|  
|**Tilsvarende beløb**|Det betalte beløb dækker nøjagtigt det resterende beløb på en ubetalte salgsfaktura, der er identificeret af FIK-nummeret.|  
|**Delvist beløb**|Det betalte beløb er mindre end det resterende beløb på en ubetalte salgsfaktura, der er identificeret af FIK-nummeret.|  
|**Overskydende beløb**|Det betalte beløb er mere end det resterende beløb på en ubetalte salgsfaktura, der er identificeret af FIK-nummeret.|  
|**Ingen matchende FIK-kode**|Systemet har ikke fundet nogen skyldige eller betalte salgsfakturaer med et FIK-nummer, der svarer til FIK-nummeret på betalingen.|  
|**FIK-dubletnummer**|Systemet har registreret, at der er betalinger, der har lignende FIK-numre.|  
|**Fakturaen er allerede betalt**|Systemet har registreret, at nogle FIK-numre på en betaling svarer til en salgsfaktura, som er fuldt udlignet og lukket.|  

## <a name="see-also"></a>Se også  
[Lokal funktionalitet for Danmark](denmark-local-functionality.md)  
[Afstemme betalinger ved hjælp af automatisk udligning](../../receivables-how-reconcile-payments-auto-application.md)

