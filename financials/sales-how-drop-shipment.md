---
title: "Oprette en salgsordre, der er knyttet til en købsordre for en direkte levering | Microsoft Docs"
description: "Beskriver, hvordan du opretter en salgsordre, der er knyttet til en købsordre for at muliggøre levering direkte fra leverandøren til kunden."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: direct shipment
ms.date: 03/29/2017
ms.author: sgroespe
ms.translationtype: Human Translation
ms.sourcegitcommit: 81636fc2e661bd9b07c54da1cd5d0d27e30d01a2
ms.openlocfilehash: 977debf7386ad1113ef54147b20fd24c7c285a78
ms.contentlocale: da-dk
ms.lasthandoff: 07/07/2017


---
# <a name="how-to-make-drop-shipments"></a>Fremgangsmåde: Foretage direkte leveringer
En direkte levering er en levering af varer fra en af dine leverandører direkte til din kunde.

Når en salgsordre er markeret til direkte levering, og du opretter en købsordre, som angiver kunden i feltet **Sælg til kundenr.**, kan du sammenkæde de to dokumenter og dermed bede leverandøren levere direkte til kunden.

## <a name="to-create-a-sales-order-for-drop-shipment"></a>Sådan oprettes en salgsordre til direkte levering
Hvis du vil forberede en direkte levering, skal du oprette en salgsordre for en vare som normalt, bortset fra at du skal angive på salgslinjen, at salget kræver direkte levering.

1. Opret en salgsordre for en vare. Du kan finde flere oplysninger i [Fremgangsmåde: Sælge produkter](sales-how-sell-products.md).
2. Markér afkrydsningsfeltet **Direkte levering** på salgsordrelinjen for den direkte levering. Brug funktionen **Vis kolonner**, hvis feltet ikke vises. Du kan finde flere oplysninger under [Brugertilpasning](ui-user-personalization.md).

> [!NOTE]  
>   Denne funktion kræver, at oplevelsen er indstillet til **Pakke**. Du kan finde flere oplysninger under [Tilpasse din [!INCLUDE[d365fin](includes/d365fin_md.md)]-oplevelse](ui-experiences.md).

## <a name="to-create-the-purchase-order-for-drop-shipment"></a>Sådan oprettes købsordren til direkte levering
Hvis du vil forberede en direkte levering af den vare, der skal sælges, kan du oprette en købsordre som normalt, bortset fra skal du angive på købsordren, at den skal leveres til kunden, ikke til dig selv.

1. Opret en indkøbsordre. Du skal ikke udfylde nogen felter på linjerne. Du kan finde flere oplysninger under [Fremgangsmåde: Registrere køb](purchasing-how-record-purchases.md).
2. I feltet **Kundenr** skal du vælge den kunde, som du sælger til.
3. Vælg handlingen **Direkte leveringer**, og vælg derefter handlingen **Hent salgsordre**.
4. I vinduet **Salgsoversigt** skal du vælge den salgsordre, du forberedt i afsnittet "Sådan oprettes en salgsordre til direkte levering".
5. Vælg knappen **OK**.

Linjeoplysningerne på salgsordren indsættes på købsordrelinjen(erne).

Nu kan du bede leverandøren levere varerne til kunden, f.eks. ved at sende købsordren som en PDF.     

## <a name="to-view-the-linked-purchase-order-from-the-sales-order"></a>Sådan får du vist den tilknyttede købsordre fra salgsordren
* Markér salgsordrelinjen til direkte levering, vælg handlingen **Ordre**, vælg handlingen **Direkte levering**, og vælg derefter handlingen **Købsordre**.

## <a name="to-post-a-drop-shipment"></a>Sådan bogfører du en direkte levering
Når kreditoren har leveret varerne, kan du bogføre salgsordren som leveret. Du kan også bogføre købsordren, men kun med indstillingen **Modtag**, indtil salgsordren er faktureret.

1. Vælg ikonet ![Søg efter side eller rapport](media/ui-search/search_small.png "Ikonet Søg efter side eller rapport"), angiv **Salgsordrer**, og vælg derefter det relaterede link.
2. Åbn den salgsordre, du oprettede i afsnittet "Sådan oprettes en salgsordre til direkte levering".
3. I feltet **Levér (antal)** skal du angive, hvor mange varer af ordreantallet der skal leveres, hele eller en del af ordreantallet.
4. Vælg handlingen **Bogfør** eller **Bogfør og send**.
5. Vælg enten indstillingen **Levér** for at fakturere senere, eller vælg indstillingen **Levér og fakturer** for at fakturere med det samme.

## <a name="see-also"></a>Se også
[Fremgangsmåde: Sælge produkter](sales-how-sell-products.md)  
[Fremgangsmåde: Registrere køb](purchasing-how-record-purchases.md)  
[Salg](sales-manage-sales.md)  
[Lagerbeholdning](inventory-manage-inventory.md)  
[Arbejde med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

