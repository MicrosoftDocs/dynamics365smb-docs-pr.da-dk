---
title: Oprette en købsrekvisition for at få et tilbud | Microsoft Docs
description: Beskriver, hvordan du opretter et salgstilbuds- eller tilbudsanmodningsdokument for at registrere dit tilbud til en kunde om at sælge produkter i henhold til bestemte betingelser.
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: rfq
ms.date: 04/01/2020
ms.author: edupont
ms.openlocfilehash: bc7bb92185d979871298a3312019e3116fecdab5
ms.sourcegitcommit: a80afd4e5075018716efad76d82a54e158f1392d
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 09/09/2020
ms.locfileid: "3782922"
---
# <a name="request-quotes"></a>Anmode om tilbud
Du kan bruge en købsrekvisition som foreløbig kladde til en købsordre for senere at konvertere ordren til en købsfaktura eller en ordre.


## <a name="to-create-a-purchase-quote"></a>Sådan oprettes en købsrekvisition
1. Vælg ikonet ![Elpære, der åbner funktionen Fortæl mig](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig"), angiv **Købsrekvisitioner**, og vælg derefter det relaterede link.
2. Opret et nyt dokument på samme måde, som du opretter en købsordre. Du kan finde flere oplysninger under [Registrere køb](purchasing-how-record-purchases.md).

## <a name="to-convert-a-purchase-quote-to-a-purchase-order"></a>Sådan konverteres en rekvisition til en købsordre
Når du har accepteret leverandørtilbuddet, kan du konvertere det til en købsfaktura eller ordre for at behandle den.

1. Åbn en købsrekvisition, der er klar til at konvertere, og vælg derefter handlingen **Lav ordre**.

Købsrekvisitionen fjernes fra databasen. En købsfaktura eller indkøbsordre oprettes på grundlag af oplysningerne i købsrekvisitionen, hvor du kan behandle købet. I feltet **Tilbudsnr.** på købsfakturaen eller købsordren kan du se nummeret på den købsrekvisition, den blev oprettet ud fra.

## <a name="see-also"></a>Se også
[Køb](purchasing-manage-purchasing.md)  
[Opsætning af indkøb](purchasing-setup-purchasing.md)  
[Sende dokumenter som mail](ui-how-send-documents-email.md)  
[Arbejde med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)
