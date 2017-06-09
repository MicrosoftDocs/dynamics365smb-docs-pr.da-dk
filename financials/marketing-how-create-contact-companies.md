---
title: Oprette kontaktvirksomheder | Microsoft Docs
description: Beskriver, hvordan du opretter kontaktvirksomheder i Financials
services: project-madeira
documentationcenter: 
author: jswymer
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: relationship, prospect
ms.date: 02/28/2017
ms.author: jswymer
ms.translationtype: Human Translation
ms.sourcegitcommit: a31be0f9d07e2abb591e26f6bae34c6f6e4dcda6
ms.openlocfilehash: bd8dfb8abc9387ad6b9c500f25feb181878b6cfe
ms.contentlocale: da-dk
ms.lasthandoff: 05/04/2017


---
# <a name="create-contact-companies"></a>Oprette kontaktvirksomheder
Du kan oprette en kontakt for hver ny virksomhed, du er i interaktion med, f.eks. kunde, leverandør, kundeemne, bank, advokatfirma eller konsulentfirma.

Du kan oprette en kontakt på to måder: forfra eller fra en eksisterende debitor, kreditor eller bankkonto.

Kontroller eventuelt indstillingerne i vinduet **Marketingopsætning**, før du opretter en kontakt. Du kan finde flere oplysninger under [Konfigurere Relationsstyring](marketing-setup-marketing.md).

## <a name="create-a-company-contact-from-scratch"></a>Oprette en virksomhedskontakt fra bunden
1. I øverste højre hjørne skal du vælge ikonet **Søg efter side eller rapport** ![Søg efter side eller rapport](media/ui-search/search_small.png "Ikonet Søg efter side eller rapport"), angive **Kontakter** og derefter vælge det relaterede link.
2. Vælg handlingen **Ny**.
3. I feltet **Nummer** skal du skrive et nummer på kontakten.

    Hvis du har defineret en nummerserie for kontakter i vinduet **Marketingopsætning**, kan du i stedet trykke på Enter og vælge det næste tilgængelige nummer.  
4. Indstil **Type** til **Virksomhed**.
5. Udfyld de øvrige felter efter behov.

## <a name="create-a-company-contact-from-a-customer-vendor-or-bank-account"></a>Oprette en virksomhedskontakt fra en debitor, kreditor eller bankkonto
Hvis du allerede har defineret en række debitorer, kreditorer eller bankkonti, kan du oprette kontakter på grundlag af de eksisterende kreditordata. Når du opretter en kontakt på denne måde, synkroniseres kontaktoplysningerne med oplysningerne om debitor, kreditor eller bankkonto.

**Bemærk**: Før du kan oprette kontaktvirksomheder på denne måde, skal du angive en forretningsrelationskode for debitorer, kreditorer og bankkonti i vinduet **Marketingopsætning**. Hvis du vil oprette kontakter fra en bankkonto, skal du også angive nummerserier for bankkonti i vinduet **Regnskabsopsætning**.

1. I øverste højre hjørne skal du vælge ikonet **Søg efter side eller rapport** ![Søg efter side eller rapport](media/ui-search/search_small.png "Ikonet Søg efter side eller rapport"), angive et af følgende, afhængigt af hvor du vil oprette kontakter fra, og derefter vælge det relaterede link.
   * **Opret kontakter fra debitorer**
   * **Oprette kontakter fra kreditorer**
   * **Oprette kontakter fra bankkonti**
2. I det kørselsvindue, der åbnes, skal du angive filtre i sektionen **Debitor**, **Kreditor** eller **Bankkonto**, hvis du vil oprette kontakter ud fra bestemte debitorer, kreditorer eller bankkonti.
3. Vælg **OK** for at begynde at oprette kontakter.

    De næste numre i nummerserien er tildelt de nye kontakter. Den forretningsrelation for kreditorer, som er angivet i vinduet **Marketingopsætning**, tildeles til de nyoprettede kontakter.

**Tip**: Du kan også oprette en debitor, kreditor eller bankkonto fra en kontakt. Du kan finde flere oplysninger under [Oprette en debitor, kreditor eller bankkonto fra en kontakt](marketing-how-create-contacts-new-customers-vendors-bank-accounts.md).

## <a name="see-also"></a>Se også
[Synkronisering af kontakter med debitorer, kreditorer og bankkonti](marketing-synchronize-contacts-customers-vendors-bank-accounts.md)  
[Tildele forretningsrelationer til en kontakt](marketing-business-relations.md#AssignBusRelContact)  
[Tildele brancher til en kontakt](marketing-industry-groups.md#AssignIndustryGroupContact)  
[Tildele mailgrupper til en kontakt](marketing-mailing-groups.md#AssignMailGroupContact)  
[Fremgangsmåde: Oprette kontaktpersoner](marketing-create-contact-persons.md)  
[Arbejde med Financials](ui-work-product.md)

