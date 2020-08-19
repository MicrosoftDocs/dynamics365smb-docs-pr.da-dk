---
title: Knyt en salgsordre til en købsordre til direkte levering | Microsoft Docs
description: Beskriver, hvordan du opretter en salgsordre, der er knyttet til en købsordre for at muliggøre levering direkte fra leverandøren til kunden.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: direct shipment
ms.date: 04/01/2020
ms.author: sgroespe
ms.openlocfilehash: 7cc6101fbd63ed7bc4f92372acf651fe8868c7be
ms.sourcegitcommit: 6078bc9b2b571248d779722ce4125f250e7a3922
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 08/07/2020
ms.locfileid: "3666968"
---
# <a name="make-drop-shipments"></a>Foretage direkte leveringer
En direkte levering er en levering af varer fra en af dine leverandører direkte til din kunde.

Når en salgsordre er markeret til direkte levering, og du opretter en købsordre, der angiver kunden i feltet **Leveres til**, **Debitoradresse**, kan du sammenkæde de to dokumenter for at give kreditoren besked om at levere direkte til debitoren.
<br><br>  
  
> [!Video https://www.microsoft.com/en-us/videoplayer/embed/RE4mOyM?rel=0]

## <a name="to-create-a-sales-order-for-drop-shipment"></a>Sådan oprettes en salgsordre til direkte levering
Hvis du vil forberede en direkte levering, skal du oprette en salgsordre for en vare og angive på salgslinjen, at salget kræver direkte levering.

1. Opret en salgsordre for en vare. Du kan finde flere oplysninger i [Sælge produkter](sales-how-sell-products.md).
2. Markér afkrydsningsfeltet **Direkte levering** på salgsordrelinjen for den direkte levering. Brug funktionen **Vis kolonner**, hvis feltet ikke vises. Du kan finde flere oplysninger under [Tilpasse dit arbejdsområde](ui-personalization-user.md).

## <a name="to-create-the-purchase-order-for-drop-shipment"></a>Sådan oprettes købsordren til direkte levering
Hvis du vil forberede en direkte levering, skal du angive på købsordren, at den skal sendes til kunden og ikke til dig selv.

1. Opret en indkøbsordre. Du skal ikke udfylde nogen felter på linjerne. Du kan finde flere oplysninger under [Registrere køb](purchasing-how-record-purchases.md).
2. Vælg **Debitoradresse** i feltet **Leveres til**.
3. Vælg den kunde, du sælger til, i feltet **Debitor**.
3. Vælg handlingen **Direkte leveringer**, og vælg derefter handlingen **Hent salgsordre**.
4. På siden **Salgsoversigt** skal du vælge den salgsordre, du forberedt i [Sådan oprettes en salgsordre til direkte levering](sales-how-drop-shipment.md#to-create-a-sales-order-for-drop-shipment).
5. Vælg knappen **OK**.

Linjeoplysningerne på salgsordren indsættes på købsordrelinjen(erne).

Nu kan du bede leverandøren levere varerne til kunden, f.eks. ved at sende købsordren som en PDF.     

## <a name="to-create-multiple-purchase-orders-for-drop-shipments"></a>Sådan oprettes flere købsordrer til direkte leveringer
Du kan også bruge indkøbskladden til at oprette købsordren til kreditoren. Fordelen ved at bruge indkøbskladden er, at den kan oprette købsordrer til alle udestående direkte leveringer, så du ikke behøver at oprette dem en ad gangen.

1. Vælg ikonet ![Elpære, der åbner funktionen Fortæl mig](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig"), åbn **Indkøbskladder**, og vælg derefter det relaterede link.
2. Vælg handlingen **Direkte leveringer**, og vælg derefter handlingen **Hent salgsordre**.
3. Vælg knappen **OK**.
4. Gennemgå købsordrelinjerne, og vælg den leverandør, der leverer de krævede varer, i feltet **Leverandørnr.**. 
5. Vælg handlingen **Udfør aktionsmeddelelse*** for at konvertere de gennemsete linjer til en købsordre.

## <a name="to-view-the-linked-purchase-order-from-the-sales-order"></a>Sådan får du vist den tilknyttede købsordre fra salgsordren
* Markér salgsordrelinjen til direkte levering, vælg handlingen **Ordre**, vælg handlingen **Direkte levering**, og vælg derefter handlingen **Købsordre**.

## <a name="to-post-a-drop-shipment"></a>Sådan bogfører du en direkte levering
Når kreditoren har leveret varerne, kan du bogføre salgsordren som leveret. Du kan også bogføre købsordren, men kun med indstillingen **Modtag**, indtil salgsordren er faktureret.

1. Vælg ikonet ![Elpære, der åbner funktionen Fortæl mig](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig"), angiv **Salgsordre**, og vælg derefter det relaterede link.
2. Åbn den salgsordre, du oprettede i [Sådan oprettes en salgsordre til direkte levering]()(sales-how-drop-shipment.md#to-create-a-sales-order-for-drop-shipment).
3. I feltet **Levér (antal)** skal du angive, hvor mange varer af ordreantallet der skal leveres, hele eller en del af ordreantallet.
4. Vælg handlingen **Bogfør** eller **Bogfør og send**.
5. Vælg enten indstillingen **Levér** for at fakturere senere, eller vælg indstillingen **Levér og fakturer** for at fakturere med det samme.

## <a name="see-also"></a>Se også
[Oprette specialordrer](sales-how-to-create-special-orders.md)  
[Købe varer til et salg](purchasing-how-purchase-products-sale.md)  
[Sælge produkter](sales-how-sell-products.md)  
[Registrere køb](purchasing-how-record-purchases.md)  
[Salg](sales-manage-sales.md)  
[Lagerbeholdning](inventory-manage-inventory.md)  
[Arbejde med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)
