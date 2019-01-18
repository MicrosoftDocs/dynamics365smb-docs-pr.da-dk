---
title: Synkronisering af kontakter med debitorer og kreditorer | Microsoft Docs
description: "Du kan sammenkæde eller synkronisere kontaktoplysninger for kontakter, der også er debitorer, kreditorer eller bankkonti, så du kun opdaterer oplysninger ét sted."
services: project-madeira
documentationcenter: 
author: edupont04
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: relationship, CRM, integration, couple
ms.date: 10/01/2018
ms.author: edupont
redirect_url: marketing-create-contact-companies
ms.translationtype: HT
ms.sourcegitcommit: 33b900f1ac9e295921e7f3d6ea72cc93939d8a1b
ms.openlocfilehash: 84cb3a6a96826ad5e3d1824ed5182dfcd972d0b3
ms.contentlocale: da-dk
ms.lasthandoff: 11/26/2018

---
# <a name="synchronizing-contacts-with-customers-vendors-and-bank-accounts"></a>Synkronisering af kontakter med debitorer, kreditorer og bankkonti
Hvis nogle af dine kontakter også er debitorer, kreditorer eller bankkonti, kan du synkronisere kontaktoplysningerne med den relaterede debitor, kreditor eller bankkonto. Synkroniseringen gør oplysninger, der er fælles for kontakter og debitorer, kreditorer eller bankkonti, ens.  

Du skal angive en forretningsrelationskode for debitorer, kreditorer eller bankkonti på siden **Marketingopsætning**, før du kan synkronisere kontakter med disse. Du kan finde flere oplysninger under [Konfigurere Relationsstyring](marketing-setup-marketing.md).

## <a name="different-ways-to-synchronize-contacts-with-customers-vendors-and-bank-accounts"></a>Forskellige måder at synkronisere kontakter med debitorer, kreditorer og bankkonti
Du kan synkronisere kontakter med debitorer, kreditorer eller bankkonti på tre måder:

* knytte kontakter sammen med eksisterende debitorer, kreditorer eller bankkonti fra kontaktkortet. Du kan finde flere oplysninger under [Knytte kontakter til debitorer, kreditorer og bankkonti](marketing-how-link-contact.md).
* Opret debitorer, kreditorer eller bankkonti ud fra kontakten. Du kan finde flere oplysninger under [Oprette en debitor, kreditor eller bankkonto fra en kontakt](marketing-how-create-contacts-new-customers-vendors-bank-accounts.md).
* Oprette kontakter ud fra debitorer, kreditorer eller bankkonti. Du kan finde flere oplysninger under [Oprette en virksomhedskontakt ud fra en debitor, kreditor eller bankkonto](marketing-how-create-contact-companies.md).

## <a name="consequences-of-synchronization"></a>Resultater af synkronisering
Hvis kontakten synkroniseres med debitoren, kreditoren, bankkontoen:

* Du behøver kun opdatere oplysninger ét sted. Ændrer du f.eks. telefonnummeret på kontakten, opdateres telefonnummeret automatisk med samme ændring på debitoren, kreditoren eller bankkontoen.
* Hvis du har angivet en nummerserie til kontakter, og du opretter et debitor-, kreditor- eller bankkontokort, oprettes der automatisk et kontaktkort for den pågældende debitor, kreditor eller bankkonto.
* Du kan oprette salgstilbud og -ordrer og købsrekvisitioner og -ordrer ud fra kontakten.
* Du kan automatisk få registreret dine interaktioner, når du udfører handlinger, f.eks. udskriver ordrer, rammeordrer, opretter serviceordrer, sender mails osv.
* Hvis du sletter en kontakt, som er knyttet sammen med en debitor, kreditor eller bankkonto, er det kun kontakten, som bliver slettet. Debitor, kreditor eller bankkonto slettes ikke.
* Hvis du sletter en debitor, kreditor eller bankkonto, som er knyttet til en kontakt, forbliver kontakten.

> [!NOTE]  
>   Visse detaljer, som fakturerings og bogføringsoplysninger, vises ikke på kontaktkortet. Derfor kan du tilføje dem manuelt på debitorkortet, kreditorkortet eller bankkontokortet, når du opretter kontakter som debitorer, kreditorer eller bankkonti.

## <a name="see-also"></a>Se også
[Administrere kontakter](marketing-contacts.md)  
[Arbejde med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

