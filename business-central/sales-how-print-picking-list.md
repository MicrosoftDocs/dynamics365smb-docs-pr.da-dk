---
title: Udskriv en plukliste fra en salgsordre
description: Du kan udskrive en lagerplukliste direkte i salgsordrer, salg, fakturaer og andre udgående salgsdokumenter.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 06/25/2021
ms.author: edupont
ms.openlocfilehash: 50c0a9836a45bac0dfd4a190040c908d28d5617f
ms.sourcegitcommit: a7cb0be8eae6ece95f5259d7de7a48b385c9cfeb
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 07/08/2021
ms.locfileid: "6436822"
---
# <a name="print-the-picking-list"></a>Udskrive pluklisten

Du kan udskrive en lagerplukliste direkte i salgsordrer, en salgsfakturaer og andre udgående salgsdokumenter, der bruges til at starte leverance af varer.

Denne rapport bruges typisk i virksomheder uden dedikeret funktionalitet til lagerstyring, så en lagermedarbejder kan nøjes med at se eller udskrive pluklisten fra det relaterede salgsdokument. I virksomheder med større eller mere komplicerede processer planlægges og udføres plukningen i dedikerede lagerdokumenter. Du kan finde flere oplysninger i [Plukkevarer](warehouse-pick-items.md).

## <a name="to-print-a-picking-list-from-a-sales-order"></a>Sådan udskriver du en plukliste fra en salgsordre

Følgende procedure er baseret på en salgsordre. Fremgangsmåden er den samme for alle andre salgsdokumenter, der kan bruges til at starte leverance af varer, f.eks. en overflytningsordre.

1. Vælg ![Søg efter side eller rapport.](media/ui-search/search_small.png "Ikonet Søg efter side eller rapport") ikon, skriv **Salgsordrer**, og vælg derefter det relaterede link.  
2. Åbn den salgsordre, som du vil plukke varer til.  
3. Vælg handlingen **Rapport**, og vælg derefter handlingen **Plukliste efter ordre**.  
4. Klik på **Udskriv** for at udskrive pluklisten, eller klik på **Vis udskrift** for at se den på skærmen.

Du kan også gemme pluklisten som et dokument, hvis du f.eks. vil sende den til en anden person eller tilføje den som en vedhæftet fil i salgsordren. Du kan få flere oplysninger i [Administrere vedhæftede filer, links og noter på kort og dokumenter](ui-how-add-link-to-record.md).

> [!NOTE]
> Hvis du har brugt funktionen **Udfold stykliste** på salgsordren, vises kun de komponenter, der hører til det relaterede montageelement, i rapporten. Du kan finde flere oplysninger i [Arbejde med styklister](inventory-how-work-BOMs.md).

## <a name="see-also"></a>Se også

[Lagerbeholdning](inventory-manage-inventory.md)  
[Plukke varer](warehouse-pick-items.md)  
[Arbejde med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]