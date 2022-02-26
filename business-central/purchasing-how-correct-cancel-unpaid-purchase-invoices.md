---
title: Ændre eller annullere ubetalte købsfakturaer (indeholder video)
description: Forklarer, hvordan du retter, annuller eller fortryder en bogført købsfaktura og automatisk opretter en købskreditnota.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: undo, credit memo, return
ms.search.form: 138, 140, 146
ms.date: 04/01/2021
ms.author: edupont
ms.openlocfilehash: 3f4e936b0cdc65efde28fb0833458f4286a7b7eb
ms.sourcegitcommit: e008b3d7003c256475d6c606e5f7c9866a6bbb72
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 01/10/2022
ms.locfileid: "7953470"
---
# <a name="correct-or-cancel-unpaid-purchase-invoices"></a>Rette eller annullere ubetalte købsfakturaer

Du kan rette eller annullere en bogført købsfaktura. Dette er nyttigt, hvis du vil rette en skrivefejl, eller hvis du ønsker at ændre købet tidligt i ordreprocessen.

Hvis du allerede har betalt for produkter på den bogførte købsfaktura, kan ikke du rette eller annullere den fra selve den bogførte købsfaktura. I stedet skal du manuelt oprette en købskreditnota for at tilbageføre købet eventuelt styret via en købsreturvareordre. Det samme gælder, hvis du vil ændre en bogført købsfaktura, der er baseret på kombinerede købsleverancer. Du kan finde flere oplysninger i [Behandle købsreturvarer eller annulleringer](purchasing-how-process-purchase-returns-cancellations.md).

På siden **Bogført købsfaktura** kan du vælge knappen **Ret** eller **Annuller**. Når du retter eller annullerer en bogført købsfaktura, anvendes den rettede købskreditnota på alle finanskonti og lageropgørelsesposter, der blev oprettet, da den oprindelige købsfaktura blev bogført. På denne måde tilbageføres den bogførte købsfaktura i dine finansposter, og rettelseskøbskreditnotaen efterlades til revisionsspor. Nedenfor beskrives anvendelsen af **Ret** og **Annuller**.
<br><br>
> [!Video https://www.microsoft.com/videoplayer/embed/RE4dhoc?rel=0]

## <a name="to-correct-a-posted-purchase-invoice"></a>Sådan rettes en bogført købsfaktura
1. Vælg ![Lightbulb, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **Bogførte købsfakturaer**, og vælg derefter det relaterede link.  
2. Vælg den bogførte købsfaktura, som du vil rette.  

    > [!NOTE]  
    >   Hvis afkrydsningsfeltet **Annulleret** er markeret, kan du ikke rette den bogførte købsfaktura, da den allerede er rettet eller annulleret.
3. På siden **Bogført købsfaktura** skal du vælge **Ret**.

    En ny købsfaktura med de samme oplysninger oprettes, hvor du kan foretage en rettelse. Du kan finde flere oplysninger i [Registrere køb](purchasing-how-record-purchases.md). Feltet **Annulleret** på den første bogførte købsfaktura ændres til **Ja**.

    En købskreditnota oprettes og bogføres automatisk for at annullere den oprindelige bogførte købsfaktura.
4. Vælg **Vis rettelseskreditnota** for at få vist den bogførte købskreditnota, som gør den oprindelige bogførte købsfaktura ugyldig.

## <a name="to-cancel-a-posted-purchase-invoice"></a>Sådan annulleres en bogført købsfaktura
1. Vælg ![Lightbulb, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **Bogførte købsfakturaer**, og vælg derefter det relaterede link.  
2. Vælg den bogførte købsfaktura, som du vil annullere.

    > [!NOTE]  
    >   Hvis afkrydsningsfeltet **Annulleret** er markeret, kan du ikke annullere den bogførte købsfaktura, da den allerede er annulleret eller rettet.
3. På siden **Bogført købsfaktura** skal du vælge **Annuller**.

    En købskreditnota oprettes og bogføres automatisk for at annullere den oprindelige bogførte købsfaktura. Feltet **Annulleret** på den første bogførte købsfaktura ændres til **Ja**.
4. Vælg **Vis rettelseskreditnota** for at få vist den bogførte købskreditnota, som gør den oprindelige bogførte købsfaktura ugyldig.

### <a name="partial-invoice-posting-also-supported"></a>Delvis fakturabogføring understøttes også
Hvis annulleringen vedrører en delvis fakturabogføring, opdateres den oprindelige indkøbsordrelinje, så den afspejler det annullerede fakturerede antal. Felterne **Fakturer antal** og **Fakt. antal** på den relaterede købsordrelinje nulstilles til værdierne før den delvise fakturabogføring.

## <a name="see-also"></a>Se også
[Køb](purchasing-manage-purchasing.md)  
[Registrere køb](purchasing-how-record-purchases.md)  
[Arbejde med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]