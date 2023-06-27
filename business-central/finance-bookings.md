---
title: Fakturere dine reservationer i Business Central
description: 'Dette emne indeholder en beskrivelse af, hvordan du kan udføre masse fakturering fra Microsoft Bookings Business central.'
author: edupont04
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 'invoicing, bookings'
ms.search.form: '1638, 6702, 6704'
ms.date: 05/20/2022
ms.author: edupont
---
# <a name="bulk-invoicing-for-microsoft-bookings-in-" />Massefakturering for Microsoft Bookings i [!INCLUDE[prod_short](includes/prod_short.md)]

Hvis dit firma bruger Bookings-appen i Microsoft 365, kan du udstede flere fakturaer ad gangen for aftaler. Siden **Ikke-fakturerede Bookings** i [!INCLUDE[prod_short](includes/prod_short.md)] indeholder en oversigt over virksomhedens udførte reservationer. På denne side kan du hurtigt vælge de aftaler, som du vil fakturere, og oprette udkast til fakturaer for de ydede services.  

## <a name="connect-to-bookings" />Oprette forbindelse til Bookings

For at forbinde din [!INCLUDE[prod_short](includes/prod_short.md)] med Bookings skal du angive din Bookings-virksomhed, hvad der skal synkroniseres med Bookings, hvor ofte synkroniseringen skal foretages, og hvilke skabeloner der skal bruges. Du kan oprette oplysningerne på siden **Opsætning af Bookings-synkronisering**, som du kan starte fra siden **Opsætning af Exchange-synkronisering**, som du kan finde via [Søg](ui-search.md).  

Hvis du vil synkronisere kunder mellem Bookings og [!INCLUDE[prod_short](includes/prod_short.md)], skal du angive den standardskabelon, der skal bruges, for at tilføje nye debitorer i [!INCLUDE[prod_short](includes/prod_short.md)] baseret på debitorerne i din Bookings-virksomhed.  

> [!NOTE]
> Appen Bookings er udviklet til bogførte aftaler for individuelle debitorer i stedet for virksomheder. Synkroniseringen med [!INCLUDE[prod_short](includes/prod_short.md)] vil derfor kun synkronisere debitorkontakter med typen *Person*. Der kræves også en mailadresse for kontakten til synkronisering.  

Hvis du på samme måde vil synkronisere serviceartikler mellem Bookings og [!INCLUDE[prod_short](includes/prod_short.md)], skal du angive den standardskabelon, der skal bruges, for at tilføje nye serviceartikler i [!INCLUDE[prod_short](includes/prod_short.md)] baseret på tjenesterne i din Bookings-virksomhed.  

> [!NOTE]
> Kun varer af typen *Service* synkroniseres mellem Bookings og [!INCLUDE[prod_short](includes/prod_short.md)]. Den skabelon, du konfigurerede på siden **Konfigurationsskabeloner**, så den kan bruges til varesynkronisering, skal definere typen som *Service*.

## <a name="invoice-appointments" />Fakturaaftaler

Når du skal sende fakturaer for de færdige reservationer, skal du gå til siden **Ikke-fakturerede Bookings**. Afhængigt af hvor ofte oplysningerne synkroniseres er listen lang eller kort. Du kan oprette fakturaer for alle reservationer på listen eller én reservation ad gangen. Du kan vælge en eller flere poster på listen og fakturere dem som de eneste.  

Understøttelse af faktureringsaftaler fra Bookings er lettere end den fulde arbejdsproces, hvor du arbejder med tilbud, salgsordrer og salgsfakturaer. Du kan finde flere oplysninger i [Fakturere salg](sales-how-invoice-sales.md). Du kan vælge at sælge dine tjenesteydelser ved hjælp af [!INCLUDE[prod_short](includes/prod_short.md)] eller vælge at bruge Bookings, afhængigt af dine forretningsbehov.  

> [!NOTE]
> I maj 2022 har vi fundet en fejl i integrationen med Books. Synkronisere fra Books til [!INCLUDE [prod_short](includes/prod_short.md)] kræver aktuelt, at du manuelt skal knytte fakturaerne til debitorer [!INCLUDE [prod_short](includes/prod_short.md)].

## <a name="see-also" />Se også

[Finans](finance.md)  
[Fakturere salg](sales-how-invoice-sales.md)  
[Konfigurere salg](sales-setup-sales.md)  
[Microsoft Bookings](https://products.office.com/business/scheduling-and-booking-app)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
