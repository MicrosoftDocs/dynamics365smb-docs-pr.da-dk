---
title: Oprette en købsrekvisition for at få et tilbud
description: Beskriver, hvordan du opretter et salgstilbuds- eller tilbudsanmodningsdokument (RQF) for at registrere dit tilbud til en kunde om at sælge produkter i henhold til bestemte betingelser.
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: rfq
ms.search.form: 49, 97, 9306, 9346
ms.date: 08/08/2022
ms.author: edupont
ms.openlocfilehash: 6444b795bf95b4da45d5d09bd6d6b7d5177c277a
ms.sourcegitcommit: 8b95e1700a9d1e5be16cbfe94fdf7b660f1cd5d7
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 09/09/2022
ms.locfileid: "9461125"
---
# <a name="request-quotes"></a>Anmode om tilbud

Du kan bruge en købsrekvisition som foreløbig kladde til en købsordre for senere at konvertere ordren til en købsfaktura eller en ordre.

## <a name="create-a-purchase-quote"></a>Opret en købsrekvisition

1. Vælg ![Lightbulb, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **Købsrekvisitioner**, og vælg derefter det relaterede link.
2. Opret et nyt dokument på samme måde, som du opretter en købsordre. Flere oplysninger i [Registrere Køb](purchasing-how-record-purchases.md).

## <a name="convert-a-purchase-quote-to-a-purchase-order"></a>Konvertere en rekvisition til en købsordre

Når du har accepteret leverandørtilbuddet, kan du konvertere det til en købsordre for at behandle den.

1. Åbn den købsrekvisition, du vil konvertere, og vælg derefter handlingen **Lav ordre**.

Købsrekvisitionen fjernes fra databasen. En købsfaktura eller indkøbsordre oprettes på grundlag af oplysningerne i købsrekvisitionen, hvor du kan behandle købet, og bogfør derefter en købsfaktura. I feltet **Tilbudsnr.** på både købsordren og købsfakturaen kan du se nummeret på den købsrekvisition, de blev oprettet ud fra.

> [!NOTE]
> Det er ikke muligt at konvertere en købsrekvisition til en købsfaktura direkte, ligesom det er muligt med salgstilbud. Du kan finde flere oplysninger om, hvordan du opretter en købsfaktura, ved at læse [Registrere køb med købsfakturaer](purchasing-how-record-purchases.md).

## <a name="see-related-training-at-microsoft-learn"></a>Se relateret træning på [Microsoft Learn](/learn/modules/create-purchase-documents-dynamics-365-business-central/).

## <a name="see-also"></a>Se også

[Køb](purchasing-manage-purchasing.md)  
[Opsætning af indkøb](purchasing-setup-purchasing.md)  
[Sende dokumenter som mail](ui-how-send-documents-email.md)  
[Arbejd med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
