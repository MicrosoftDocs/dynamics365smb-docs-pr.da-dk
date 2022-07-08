---
title: Sådan oprettes specialordrer
description: Du kan oprette en specialordre på en bestemt katalogvare, der skal sendes til en bestemt kunde.
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 06/23/2021
ms.author: edupont
ms.openlocfilehash: 3f9cb0690bf21c3b4571ff65486038499af010e9
ms.sourcegitcommit: 00a8acc82cdc90e0d0db9d1a4f98a908944fd50a
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 06/29/2022
ms.locfileid: "9078540"
---
# <a name="create-special-orders"></a>Oprette specialordrer

Du kan oprette en specialordre på en bestemt katalogvare, der skal sendes til en bestemt kunde. Din leverandør sender varen til dit lagersted, og derfra kan du levere varen til debitoren, enten alene eller sammen med andre varer fra en anden ordre.  

Specialordrer medfører, at købs- og salgsordrer sammenkædes for at sikre, at en bestemt katalogvare plukkes og leveres til kunden.  

Før du kan bruge denne funktion, skal du oprette den kunde, den leverandør, og det varekort, som skal bruges i ordren.  

## <a name="to-create-a-special-order"></a>Sådan oprettes en specialordre

1.  Vælg ![Lightbulb, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **Salgsordre**, og vælg derefter det relaterede link.  
2. Vælg handlingen **Ny**. Opret og udfyld en  salgsordre for varen. Du kan finde flere oplysninger i [Sælge produkter](sales-how-sell-products.md).
3.  Udfyld salgslinjen på oversigtspanelet **Linjer**. I feltet **Indkøbskode** skal du vælge en indkøbskode, hvor der er en markering i feltet **Specialordre**.

    Du skal nu oprette købsordren fra en indkøbskladde.  
4. Vælg ![Lightbulb, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **Indkøbskladde**, og vælg derefter det relaterede link.  
5. Vælg handlingen **Specialordre**, og vælg derefter handlingen **Hent salgsordrer**.  
6.  På siden **Hent salgsordrer** skal du vise de resultater, hvor **Bilagsnr.** er nummeret på salgsordren. Vælg knappen **OK**. Der oprettes en indkøbskladdelinje for varen.  
7.  Vælg **Ny** i feltet **Aktionsmeddelelse** på indkøbskladdelinjen.  
8.  På siden **Indkøbskladde** skal du vælge handlingen **Udfør aktionsmeddelelse**. Siden **Udfør aktionsmeddl. - Indk.** åbnes. Vælg knappen **OK**.  

    Du får vist en meddelelse om, at købsordrerne er oprettet. Vælg knappen **OK**.  

En indkøbsordre, der er oprettet som en specialordre for en salgsordre, respekteres i planlægningssystemet, når efterspørgsel og udbud afstemmes. Dvs. at købsordren (forsyning) forbliver tilknyttet salgsordren (behov), også selvom den pågældende købsordre kunne forsyne et andet tidligere behov. Du kan finde flere oplysninger i [Designoplysninger: Genbestillingsmetoder](design-details-reservation-order-tracking-and-action-messaging.md).  

> [!NOTE]  
>  Du kan ikke bruge funktionen til specialordre, hvis varen allerede er reserveret. For varer, der sælges på specialordrer, skal du derfor sørge for, at feltet **Reserver** på varekortet ikke er angivet til **Altid**.  

## <a name="see-related-training-at-microsoft-learn"></a>Se relateret træning på [Microsoft Learn](/learn/modules/create-sales-documents-dynamics-365-business-central/)

## <a name="see-also"></a>Se også

[Arbejde med katalogvarer](inventory-how-work-nonstock-items.md)  
[Salg](sales-manage-sales.md)  
[Foretage direkte leveringer](sales-how-drop-shipment.md)   
[Designoplysninger: Genbestillingsmetoder](design-details-reservation-order-tracking-and-action-messaging.md)  
[Arbejd med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]