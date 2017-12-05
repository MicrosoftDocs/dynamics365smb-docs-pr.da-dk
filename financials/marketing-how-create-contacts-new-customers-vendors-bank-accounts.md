---
title: Oprette en debitor eller kreditor fra en kontakt | Microsoft Docs
description: Du kan registrere en eksisterende kontakt som debitor, kreditor eller bankkonto med eksisterende data og angive en forretningsrelation.
services: project-madeira
documentationcenter: 
author: jswymer
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: relationship, client, prospect
ms.date: 06/06/2017
ms.author: jswymer
ms.translationtype: HT
ms.sourcegitcommit: ba26b354d235981bd7291f9ac6402779f554ac7a
ms.openlocfilehash: 289213b9c44b07387fd0dcf315b9d08750bdd9f7
ms.contentlocale: da-dk
ms.lasthandoff: 11/10/2017

---
# <a name="how-to-create-a-customer-vendor-or-bank-account-from-a-contact"></a>Fremgangsmåde: Oprette en debitor, kreditor eller bankkonto fra en kontakt
Du har mulighed for at registrere eksisterende kontakter som debitorer, kreditorer eller bankkonti. Når du opretter en debitor, kreditor eller bankkonto fra en kontakt, kan bruge du eksisterende data. Når du opretter en debitor, kreditor eller bankkonto på denne måde, synkroniseres den med kontakten. Synkroniseringen gør oplysninger, der er fælles for kontakter og debitorer, kreditorer eller bankkonti, ens.

Før du kan registrere kontakter på denne måde, skal du angive en forretningsrelationskode for debitorer, kreditorer og bankkonti i vinduet **Marketingopsætning**. Hvis du vil registrere kontakter som bankkonti, skal du også angive nummerserier for bankkonti i vinduet **Regnskabsopsætning**.

## <a name="to-create-a-contact-as-a-customer-vendor-or-bank-account"></a>Sådan oprettes en kontakt som debitor, kreditor eller bankkonto.
1. Vælg ikonet ![Søg efter side eller rapport](media/ui-search/search_small.png "Ikonet Søg efter side eller rapport"), angiv **Kontakter**, og vælg derefter det relaterede link.
2. Marker den kontakt, du vil oprette som debitor, kreditor eller bankkonto.
3. Vælg handlingen **Opret som**, og vælg derefter enten **Debitor**, **Kreditor** eller **Bank**.
4. Bekræft den efterfølgende meddelelse.

Kontaktoplysningerne overføres fra kortet **Kontakt** til kortet **Bankkonto**, kortet **Debitor** eller kortet **Kreditor**. Du kan tilføje specifikke oplysninger til hvert kort, f.eks. fakturering og betalingsoplysninger.

## <a name="see-also"></a>Se også
[Fremgangsmåde: Oprette kontaktvirksomheder](marketing-create-contact-companies.md)  
[Fremgangsmåde: Oprette kontaktpersoner](marketing-create-contact-persons.md)  
[Opsætning af Relationsstyring](marketing-setup-marketing.md)  
[Synkronisering af kontakter med debitorer, kreditorer og bankkonti](marketing-synchronize-contacts-customers-vendors-bank-accounts.md)  
[Fremgangsmåde: Knytte kontakter til debitorer, kreditorer og bankkonti](marketing-how-link-contact.md)  
[Tildele forretningsrelationer til en kontakt](marketing-business-relations.md#AssignBusRelContact)  
[Arbejde med Dynamics 365](ui-work-product.md)

