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
ms.translationtype: HT
ms.sourcegitcommit: bec0619be0a65e3625759e13d2866ac615d7513c
ms.openlocfilehash: 094ba95f46d13c5861087bedbe52fb18da9270e9
ms.contentlocale: da-dk
ms.lasthandoff: 03/22/2018

---
# <a name="link-contacts-with-customers-vendors-and-bank-accounts"></a>Sammenkæde kontakter med debitorer, kreditorer og bankkonti
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

