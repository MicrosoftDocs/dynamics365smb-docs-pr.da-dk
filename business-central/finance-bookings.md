---
title: Fakturere dine reservationer i Business Central | Microsoft Docs
description: Få mere at vide, hvordan du kan udstede flere fakturaer ad gangen fra Microsoft Bookings i Business Central.
author: edupont04
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: invoicing, bookings
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: 9b683fa14801c00904c131ada5bcce1f669c9b2a
ms.sourcegitcommit: 2e7307fbe1eb3b34d0ad9356226a19409054a402
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 12/17/2020
ms.locfileid: "4751001"
---
# <a name="bulk-invoicing-for-microsoft-bookings-in-prod_short"></a>Massefakturering for Microsoft Bookings i [!INCLUDE[prod_short](includes/prod_short.md)]
Hvis dit firma bruger Bookings-appen i Microsoft 365, kan du udstede flere fakturaer ad gangen for aftaler. Siden **Ikke-fakturerede Bookings** i [!INCLUDE[prod_short](includes/prod_short.md)] indeholder en oversigt over virksomhedens udførte reservationer. På denne side kan du hurtigt vælge de aftaler, som du vil fakturere, og oprette udkast til fakturaer for de ydede services.  

## <a name="connect-to-bookings"></a>Oprette forbindelse til Bookings
For at forbinde din [!INCLUDE[prod_short](includes/prod_short.md)] med Bookings skal du angive din Bookings-virksomhed, hvad der skal synkroniseres med Bookings, hvor ofte synkroniseringen skal foretages, og hvilke skabeloner der skal bruges. Du kan oprette oplysningerne på siden **Opsætning af Bookings-synkronisering**, som du kan starte fra siden **Opsætning af Exchange-synkronisering**, som du kan finde via [Søg](ui-search.md).  

Hvis du vil synkronisere kunder mellem Bookings og [!INCLUDE[prod_short](includes/prod_short.md)], skal du angive den standardskabelon, der skal bruges, for at tilføje nye debitorer i [!INCLUDE[prod_short](includes/prod_short.md)] baseret på debitorerne i din Bookings-virksomhed.  

> [!NOTE]
> Appen Bookings er udviklet til bogførte aftaler for individuelle debitorer i stedet for virksomheder. Synkroniseringen med [!INCLUDE[prod_short](includes/prod_short.md)] vil derfor kun synkronisere debitorkontakter med typen "Person". Der kræves også en mailadresse for kontakten til synkronisering.  

Hvis du på samme måde vil synkronisere serviceartikler mellem Bookings og [!INCLUDE[prod_short](includes/prod_short.md)], skal du angive den standardskabelon, der skal bruges, for at tilføje nye serviceartikler i [!INCLUDE[prod_short](includes/prod_short.md)] baseret på tjenesterne i din Bookings-virksomhed.  

> [!NOTE]
> Kun varer af typen *Service* synkroniseres mellem Bookings og [!INCLUDE[prod_short](includes/prod_short.md)]. Den skabelon, du konfigurerede på siden **Konfigurationsskabeloner**, så den kan bruges til varesynkronisering, skal definere typen som *Service*.

## <a name="invoice-appointments"></a>Fakturaaftaler
Når du skal sende fakturaer for de færdige reservationer, skal du gå til siden **Ikke-fakturerede Bookings**. Afhængigt af hvor ofte oplysningerne synkroniseres er listen lang eller kort. Du kan oprette fakturaer for alle reservationer på listen eller én reservation ad gangen. Du kan vælge en eller flere poster på listen og fakturere dem som de eneste.  

Understøttelse af faktureringsaftaler fra Bookings er lettere end den fulde arbejdsproces, hvor du arbejder med tilbud, salgsordrer og salgsfakturaer. Du kan finde flere oplysninger i [Fakturere salg](sales-how-invoice-sales.md). Du kan vælge at sælge dine tjenesteydelser ved hjælp af [!INCLUDE[prod_short](includes/prod_short.md)] eller vælge at bruge Bookings, afhængigt af dine forretningsbehov.  

## <a name="see-also"></a>Se også
[Finans](finance.md)  
[Fakturere salg](sales-how-invoice-sales.md)  
[Konfigurere salg](sales-setup-sales.md)  
[Microsoft Bookings](https://products.office.com/business/scheduling-and-booking-app)  


[!INCLUDE[footer-include](includes/footer-banner.md)]