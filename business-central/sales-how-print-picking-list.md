---
title: Udskriv en plukliste fra en salgsordre
description: 'Du kan udskrive en lagerplukliste direkte i salgsordrer, salg, fakturaer og andre udgående salgsdokumenter.'
author: brentholtorf
ms.topic: conceptual
ms.devlang: al
ms.search.keywords: null
ms.date: 06/25/2021
ms.author: bholtorf
ms.service: dynamics-365-business-central
---
# <a name="print-the-picking-list"></a>Udskrive pluklisten

Du kan udskrive en lagerplukliste direkte i salgsordrer, en salgsfakturaer og andre udgående salgsdokumenter, der bruges til at starte leverance af varer.

Denne rapport bruges typisk i virksomheder uden dedikeret funktionalitet til lagerstyring, så en lagermedarbejder kan nøjes med at se eller udskrive pluklisten fra det relaterede salgsdokument. I virksomheder med større eller mere komplicerede processer planlægges og udføres forsendelse og plukning i dedikerede lagerdokumenter. Få mere at vide på [Udgående lagerstedsflow](design-details-outbound-warehouse-flow.md).

## <a name="to-print-a-picking-list-from-a-sales-order"></a>Sådan udskriver du en plukliste fra en salgsordre

Følgende procedure er baseret på en salgsordre. Fremgangsmåden er den samme for alle andre salgsdokumenter, der kan bruges til at starte leverance af varer, f.eks. en overflytningsordre.

1. Vælg ![Søg efter side eller rapport.](media/ui-search/search_small.png "Ikonet Søg efter side eller rapport") ikon, skriv **Salgsordrer**, og vælg derefter det relaterede link.  
2. Åbn den salgsordre, som du vil plukke varer til.  
3. Vælg handlingen **Rapport**, og vælg derefter handlingen **Plukliste efter ordre**.  
4. Klik på **Udskriv** for at udskrive pluklisten, eller klik på **Vis udskrift** for at se den på skærmen.

Du kan også gemme pluklisten som et dokument, hvis du f.eks. vil sende den til en anden person eller tilføje den som en vedhæftet fil i salgsordren. Flere oplysninger i [Administrere vedhæftede filer, links og noter på kort og dokumenter](ui-how-add-link-to-record.md)

> [!NOTE]
> Hvis du har brugt funktionen **Udfold stykliste** på salgsordren, vises kun de komponenter, der hører til det relaterede montageelement, i rapporten. Du kan finde flere oplysninger i [Arbejde med styklister](inventory-how-work-BOMs.md).

## <a name="see-also"></a>Se også

[Lagerbeholdning](inventory-manage-inventory.md)  
[Udgående lagerstedsflow](design-details-outbound-warehouse-flow.md)
[Arbejde med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
