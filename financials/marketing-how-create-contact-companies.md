---
title: Oprette kontaktvirksomheder | Microsoft Docs
description: Beskriver, hvordan du kan oprette en kontaktperson for hver ny virksomhed eller potentielle virksomhed, du arbejder sammen med eller har en relation til.
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
ms.openlocfilehash: ed0f75f1e0ee8a282b58458e4fed3b4eef7c46fb
ms.contentlocale: da-dk
ms.lasthandoff: 01/30/2018

---
# <a name="create-contact-companies"></a>Oprette kontaktvirksomheder
Du kan oprette en kontakt for hver ny virksomhed, du er i interaktion med, f.eks. kunde, leverandør, kundeemne, bank, advokatfirma eller konsulentfirma.

Du kan oprette en kontakt på to måder: forfra eller fra en eksisterende debitor, kreditor eller bankkonto.

Kontroller eventuelt indstillingerne i vinduet **Marketingopsætning**, før du opretter en kontakt. Du kan finde flere oplysninger under [Konfigurere Relationsstyring](marketing-setup-marketing.md).

## <a name="create-a-company-contact-from-scratch"></a>Oprette en virksomhedskontakt fra bunden
1. Vælg ikonet ![Søg efter side eller rapport](media/ui-search/search_small.png "Ikonet Søg efter side eller rapport"), angiv **Kontakter**, og vælg derefter det relaterede link.
2. Vælg handlingen **Ny**.
3. I feltet **Nummer** skal du skrive et nummer på kontakten.

    Hvis du har defineret en nummerserie for kontakter i vinduet **Marketingopsætning**, kan du i stedet trykke på Enter og vælge det næste tilgængelige nummer.  
4. Indstil **Type** til **Virksomhed**.
5. Udfyld de øvrige felter efter behov.

## <a name="to-create-a-company-contact-from-a-customer-vendor-or-bank-account"></a>Sådan oprettes en virksomhedskontakt fra en debitor, kreditor eller bankkonto
Hvis du allerede har defineret en række debitorer, kreditorer eller bankkonti, kan du oprette kontakter på grundlag af de eksisterende kreditordata. Når du opretter en kontakt på denne måde, synkroniseres kontaktoplysningerne med oplysningerne om debitor, kreditor eller bankkonto.

> [!NOTE]  
>   Før du kan oprette kontaktvirksomheder på denne måde, skal du angive en forretningsrelationskode for debitorer, kreditorer og bankkonti i vinduet **Marketingopsætning**. Hvis du vil oprette kontakter fra en bankkonto, skal du også angive nummerserier for bankkonti i vinduet **Regnskabsopsætning**.

1. Vælg ikonet ![Søg efter side eller rapport](media/ui-search/search_small.png "Ikonet Søg efter side eller rapport"), angiv et af følgende, afhængigt af hvorfra du vil oprette kontakter, og vælg derefter det relaterede link.
   * **Opret kontakter fra debitorer**
   * **Oprette kontakter fra kreditorer**
   * **Oprette kontakter fra bankkonti**
2. I det kørselsvindue, der åbnes, skal du angive filtre i sektionen **Debitor**, **Kreditor** eller **Bankkonto**, hvis du vil oprette kontakter ud fra bestemte debitorer, kreditorer eller bankkonti.
3. Vælg **OK** for at begynde at oprette kontakter.

    De næste numre i nummerserien er tildelt de nye kontakter. Den forretningsrelation for kreditorer, som er angivet i vinduet **Marketingopsætning**, tildeles til de nyoprettede kontakter.

> [!TIP]  
>   Du kan også oprette en debitor, kreditor eller bankkonto fra en kontakt. Du kan finde flere oplysninger under [Oprette en debitor, kreditor eller bankkonto fra en kontakt](marketing-how-create-contacts-new-customers-vendors-bank-accounts.md).

## <a name="see-also"></a>Se også
[Synkronisering af kontakter med debitorer, kreditorer og bankkonti](marketing-synchronize-contacts-customers-vendors-bank-accounts.md)  
[Tildele forretningsrelationer til en kontakt](marketing-business-relations.md#AssignBusRelContact)  
[Tildele brancher til en kontakt](marketing-industry-groups.md#AssignIndustryGroupContact)  
[Tildele mailgrupper til en kontakt](marketing-mailing-groups.md#AssignMailGroupContact)  
[Oprette kontaktpersoner](marketing-create-contact-persons.md)  
[Arbejde med Finance and Operations, Business edition](ui-work-product.md)

