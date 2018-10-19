---
title: Oprette en debitor eller kreditor fra en kontakt | Microsoft Docs
description: Du kan registrere en eksisterende kontakt som debitor, kreditor eller bankkonto med eksisterende data og angive en forretningsrelation.
services: project-madeira
documentationcenter: 
author: jswymer
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: relationship, client, prospect
ms.date: 10/01/2018
ms.author: jswymer
ms.translationtype: HT
ms.sourcegitcommit: 9dbd92409ba02281f008246194f3ce0c53e4e001
ms.openlocfilehash: 07c56f109ee2e4c348c0f654ceadc4018174c0d5
ms.contentlocale: da-dk
ms.lasthandoff: 09/28/2018

---
# <a name="create-a-customer-vendor-or-bank-account-from-a-contact"></a>Oprette en debitor, kreditor eller bankkonto fra en kontakt
Du har mulighed for at registrere eksisterende kontakter som debitorer, kreditorer eller bankkonti. Når du opretter en debitor, kreditor eller bankkonto fra en kontakt, kan bruge du eksisterende data. Når du opretter en debitor, kreditor eller bankkonto på denne måde, synkroniseres den med kontakten. Synkroniseringen gør oplysninger, der er fælles for kontakter og debitorer, kreditorer eller bankkonti, ens.

Før du kan registrere kontakter på denne måde, skal du angive en forretningsrelationskode for debitorer, kreditorer og bankkonti i vinduet **Marketingopsætning**. Hvis du vil registrere kontakter som bankkonti, skal du også angive nummerserier for bankkonti i vinduet **Opsætning af Finans**.

## <a name="to-create-a-contact-as-a-customer-vendor-or-bank-account"></a>Sådan oprettes en kontakt som debitor, kreditor eller bankkonto.
1. Vælg ikonet ![Elpære, der åbner funktionen Fortæl mig](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig"), angiv **Kontakter**, og vælg derefter det relaterede link.
2. Marker den kontakt, du vil oprette som debitor, kreditor eller bankkonto.
3. Vælg handlingen **Opret som**, og vælg derefter enten **Debitor**, **Kreditor** eller **Bank**.
4. Bekræft den efterfølgende meddelelse.

Kontaktoplysningerne overføres fra kortet **Kontakt** til kortet **Bankkonto**, kortet **Debitor** eller kortet **Kreditor**. Du kan tilføje specifikke oplysninger til hvert kort, f.eks. fakturering og betalingsoplysninger.

## <a name="see-also"></a>Se også
[Opret kontaktvirksomheder](marketing-create-contact-companies.md)  
[Oprette kontaktpersoner](marketing-create-contact-persons.md)  
[Opsætning af Relationsstyring](marketing-setup-marketing.md)  
[Synkronisering af kontakter med debitorer, kreditorer og bankkonti](marketing-synchronize-contacts-customers-vendors-bank-accounts.md)  
[Knytte kontakter til debitorer, kreditorer og bankkonti](marketing-how-link-contact.md)  
[Tildele forretningsrelationer til en kontakt](marketing-business-relations.md#AssignBusRelContact)  
[Arbejde med Business Central](ui-work-product.md)

