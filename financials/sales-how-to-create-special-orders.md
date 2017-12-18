---
title: "Sådan oprettes specialordrer | Microsoft Docs"
description: "Du kan oprette en specialordre på en bestemt katalogvare, der skal sendes til en bestemt kunde. Din leverandør sender varen til dit lagersted, og derfra kan du levere varen til debitoren, enten alene eller sammen med andre varer fra en anden ordre."
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 09/08/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 2c13559bb3dc44cdb61697f5135c5b931e34d2a8
ms.openlocfilehash: c7e5d7cda12abd94a999031af3bc8d505b7f6c5e
ms.contentlocale: da-dk
ms.lasthandoff: 09/22/2017

---
# <a name="how-to-create-special-orders"></a>Sådan oprettes specialordrer
Du kan oprette en specialordre på en bestemt katalogvare, der skal sendes til en bestemt kunde. Din leverandør sender varen til dit lagersted, og derfra kan du levere varen til debitoren, enten alene eller sammen med andre varer fra en anden ordre.  

Specialordrer medfører, at købs- og salgsordrer sammenkædes for at sikre, at en bestemt katalogvare plukkes og leveres til kunden.  

Før du kan bruge denne funktion, skal du oprette den kunde, den leverandør, og det varekort, som skal bruges i ordren.  

## <a name="to-create-a-special-order"></a>Sådan oprettes en specialordre  
1.  Vælg ikonet ![Søg efter side eller rapport](media/ui-search/search_small.png "Ikonet Søg efter side eller rapport"), angiv **Salgsordre**, og vælg derefter det relaterede link.  
2. Vælg handlingen **Ny**. Opret og udfyld en salgsordre for varen. Du kan finde flere oplysninger i [Fremgangsmåde: Sælge produkter](sales-how-sell-products.md).
3.  Udfyld salgslinjen på oversigtspanelet **Linjer**. I feltet **Indkøbskode** skal du vælge en indkøbskode, hvor der er en markering i feltet **Specialordre**.

    Du skal nu oprette købsordren fra en indkøbskladde.  
4. Vælg ikonet ![Søg efter side eller rapport](media/ui-search/search_small.png "Ikonet Søg efter side eller rapport"), angiv **Indkøbskladde**, og vælg derefter det relaterede link.  
5. Vælg handlingen **Specialordre**, og vælg derefter handlingen **Hent salgsordrer**.  
6.  I vinduet **Hent salgsordrer** skal du vise de resultater, hvor **Bilagsnr.** er nummeret på salgsordren. Vælg knappen **OK**. Der oprettes en indkøbskladdelinje for varen.  
7.  Vælg **Ny** i feltet **Aktionsmeddelelse** på indkøbskladdelinjen.  
8.  I vinduet **Indkøbskladde** skal du vælge handlingen **Udfør aktionsmeddelelse**. Vinduet **Udfør aktionsmeddl. - Indk.** åbnes. Vælg knappen **OK**.  

    Du får vist en meddelelse om, at købsordrerne er oprettet. Vælg knappen **OK**.  

En indkøbsordre, der er oprettet som en specialordre for en salgsordre, respekteres i planlægningssystemet, når efterspørgsel og udbud afstemmes. Dvs. at købsordren (forsyning) forbliver tilknyttet salgsordren (behov), også selvom den pågældende købsordre kunne forsyne et andet tidligere behov. Du kan finde flere oplysninger i [Designoplysninger: Genbestillingsmetoder](design-details-reservation-order-tracking-and-action-messaging.md).  

> [!NOTE]  
>  Du kan ikke bruge funktionen til specialordre, hvis varen allerede er reserveret. For varer, der sælges på specialordrer, skal du derfor sørge for, at feltet **Reserver** på varekortet ikke er angivet til **Altid**.  

## <a name="see-also"></a>Se også  
[Fremgangsmåde: Arbejde med katalogvarer](inventory-how-work-nonstock-items.md)  
[Salg](sales-manage-sales.md)  
[Fremgangsmåde: Foretage direkte leveringer](sales-how-drop-shipment.md)   
[Designoplysninger: Genbestillingsmetoder](design-details-reservation-order-tracking-and-action-messaging.md)  
[Arbejde med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

