---
title: FIK-detaljer i betalingsudligningskladden
description: Feltet Transaktionstekst viser oplysninger om automatisk udligning af betalinger ved hjælp af den danske FIK-standard.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 06/18/2021
ms.author: edupont
ms.openlocfilehash: 57cc6265825950c500b69971fd1b35b01f76b333
ms.sourcegitcommit: e562b45fda20ff88230e086caa6587913eddae26
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 06/30/2021
ms.locfileid: "6325236"
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


[!INCLUDE[footer-include](../../includes/footer-banner.md)]