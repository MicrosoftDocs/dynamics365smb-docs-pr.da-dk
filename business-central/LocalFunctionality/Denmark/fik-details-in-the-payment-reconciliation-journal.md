---
title: FIK-detaljer i betalingsudligningskladden
description: Feltet Transaktionstekst viser oplysninger om automatisk udligning af betalinger ved hjælp af den danske FIK-standard.
author: brentholtorf
ms.topic: conceptual
ms.devlang: al
ms.search.keywords: null
ms.date: 12/12/2023
ms.author: bholtorf
ms.service: dynamics-365-business-central
---
# FIK-detaljer i betalingsudligningskladden
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

## Se også  
[Lokal funktionalitet for Danmark](denmark-local-functionality.md)  
[Afstemme betalinger ved hjælp af automatisk udligning](../../receivables-how-reconcile-payments-auto-application.md)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]