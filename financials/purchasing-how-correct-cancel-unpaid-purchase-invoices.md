---
title: "Ændre eller annullere ubetalte købsfakturaer | Microsoft Docs"
description: "Forklarer, hvordan du retter, annuller eller fortryder en bogført købsfaktura og automatisk opretter en købskreditnota."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: undo, credit memo, return
ms.date: 03/29/2017
ms.author: sgroespe
ms.translationtype: Human Translation
ms.sourcegitcommit: 81636fc2e661bd9b07c54da1cd5d0d27e30d01a2
ms.openlocfilehash: 75a56e6089567c456280b2cc287dda62fb4f3f8b
ms.contentlocale: da-dk
ms.lasthandoff: 07/07/2017


---
# <a name="how-to-correct-or-cancel-unpaid-purchase-invoices"></a>Fremgangsmåde: Rette eller annullere ubetalte købsfakturaer
Du kan rette eller annullere en bogført købsfaktura. Dette er nyttigt, hvis du vil rette en skrivefejl, eller hvis du ønsker at ændre købet tidligt i ordreprocessen.

Hvis du allerede har betalt for produkter på den bogførte købsfaktura, kan ikke du rette eller annullere den fra selve den bogførte købsfaktura. I stedet skal du manuelt oprette en købskreditnota for at tilbageføre købet. Du kan finde flere oplysninger i [Fremgangsmåde: Behandle købsreturvarer eller annulleringer](purchasing-how-process-purchase-returns-cancellations.md).

I vinduet **Bogført købsfaktura** kan du vælge knappen **Ret** eller **Annuller**. Når du retter eller annullerer en bogført købsfaktura, anvendes den rettede købskreditnota på alle finanskonti og lageropgørelsesposter, der blev oprettet, da den oprindelige købsfaktura blev bogført. På denne måde tilbageføres den bogførte købsfaktura i dine finansposter, og rettelseskøbskreditnotaen efterlades til revisionsspor. Nedenfor beskrives anvendelsen af **Ret** og **Annuller**.

## <a name="to-correct-a-posted-purchase-invoice"></a>Sådan rettes en bogført købsfaktura
1. Vælg ikonet ![Søg efter side eller rapport](media/ui-search/search_small.png "Ikonet Søg efter side eller rapport"), angiv **Bogførte købsfakturaer**, og vælg derefter det relaterede link.  
2. Vælg den bogførte købsfaktura, som du vil rette.  

    > [!NOTE]  
>   Hvis afkrydsningsfeltet **Annulleret** er markeret, kan du ikke rette den bogførte købsfaktura, da den allerede er rettet eller annulleret.
3. I vinduet **Bogført købsfaktura** skal du vælge **Ret**.

    En ny købsfaktura med de samme oplysninger oprettes, hvor du kan foretage en rettelse. Du kan finde flere oplysninger under [Fremgangsmåde: Registrere køb](purchasing-how-record-purchases.md). Feltet **Annulleret** på den første bogførte købsfaktura ændres til **Ja**.

    En købskreditnota oprettes og bogføres automatisk for at annullere den oprindelige bogførte købsfaktura.
4. Vælg **Vis rettelseskreditnota** for at få vist den bogførte købskreditnota, som gør den oprindelige bogførte købsfaktura ugyldig.

## <a name="to-cancel-a-posted-purchase-invoice"></a>Sådan annulleres en bogført købsfaktura
1. Vælg ikonet ![Søg efter side eller rapport](media/ui-search/search_small.png "Ikonet Søg efter side eller rapport"), angiv **Bogførte købsfakturaer**, og vælg derefter det relaterede link.  
2. Vælg den bogførte købsfaktura, som du vil annullere.

    > [!NOTE]  
>   Hvis afkrydsningsfeltet **Annulleret** er markeret, kan du ikke annullere den bogførte købsfaktura, da den allerede er annulleret eller rettet.
3. I vinduet **Bogført købsfaktura** skal du vælge **Annuller**.

    En købskreditnota oprettes og bogføres automatisk for at annullere den oprindelige bogførte købsfaktura. Feltet **Annulleret** på den første bogførte købsfaktura ændres til **Ja**.
4. Vælg **Vis rettelseskreditnota** for at få vist den bogførte købskreditnota, som gør den oprindelige bogførte købsfaktura ugyldig.

## <a name="see-also"></a>Se også
[Køb](purchasing-manage-purchasing.md)  
[Fremgangsmåde: Registrere køb](purchasing-how-record-purchases.md)  
[Arbejde med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

