---
title: Tilknytning af kontakter til debitorer og kreditorer | Microsoft Docs
description: "Beskriver, hvordan du sammenkæder en kontakt med en debitor, kreditor eller bankkonto fra samme virksomhed, så du kan synkronisere fælles data."
services: project-madeira
documentationcenter: 
author: jswymer
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: relationship, prospect
ms.date: 06/06/2017
ms.author: jswymer
ms.translationtype: Human Translation
ms.sourcegitcommit: 81636fc2e661bd9b07c54da1cd5d0d27e30d01a2
ms.openlocfilehash: f5bbadb37a40dbc7b06668d940d2be9569aaa8e8
ms.contentlocale: da-dk
ms.lasthandoff: 07/07/2017


---
# <a name="how-to-link-contacts-with-customers-vendors-and-bank-accounts"></a>Fremgangsmåde: Knytte kontakter til debitorer, kreditorer og bankkonti
Hvis du har en kontakt og enten en debitor, kreditor eller bankkonto til samme virksomhed, kan du knytte de to poster til hinanden. Når du knytter de to poster til hinanden, kan du synkronisere data, som er fælles, så det er de samme i begge steder.

## <a name="link-a-contact-to-an-existing-customer-vendor-or-bank-account"></a>Knytte en kontakt til en eksisterende debitor, kreditor eller bankkonto.
1. Åbn den kontakt, du vil tilknytte.
2. Vælg handlingen **Opret kæde til eksist.**, og vælg derefter **Debitor**, **Kreditor** eller **Bank**.
3. Vælg den debitor, kreditor eller bankkonto, der skal oprettes en tilknytning til.

   I **Aktuelle overord. felter** kan du angive, hvilke felter der skal have prioritet i tilfælde af uoverensstemmende oplysninger i felter, som er fælles for kontakten og debitoren, kreditoren eller kontoen. Hvis sælgerkoden f.eks. ikke er ens for kontakten og debitoren, kan du ved at markere **Kontakt** bestemme, at det er oplysningerne for kontakten, som skal bruges.

## <a name="see-also"></a>Se også
[Synkronisering af kontakter med debitorer, kreditorer og bankkonti](marketing-synchronize-contacts-customers-vendors-bank-accounts.md)  
[Oprette og administrere kontakter](marketing-contacts.md)  
[Arbejde med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)  

