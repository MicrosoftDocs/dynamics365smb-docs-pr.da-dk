---
title: Kombinere modtagelser på én enkelt faktura
description: Hvis du vil fakturere mere end én købsleverance ad gangen, kan du bruge funktionen Saml leverancer.
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.search.form: 136, 145, 146, 9308
ms.date: 04/01/2021
ms.author: edupont
ms.openlocfilehash: d108525de00685e0661b4817ecc5919501f14d9f
ms.sourcegitcommit: 5a02f8527faecdffcc54f9c5c70cefe8c4b3b3f4
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 03/04/2022
ms.locfileid: "8380902"
---
# <a name="combine-receipts-on-a-single-invoice"></a>Kombinere modtagelser på én enkelt faktura

Hvis du vil fakturere mere end én købsleverance ad gangen, kan du bruge funktionen **Saml leverancer**.  

Inden du kan oprette en samlet købsleverance, skal der være bogført mere end én leverance fra den samme leverandør i den samme valuta. Du skal med andre ord have udfyldt to eller flere købsordrer og bogført dem som modtaget, men ikke faktureret.  

Når købsleverancer er samlet på en faktura og bogført, oprettes der en bogført købsfaktura for de fakturerede linjer. Feltet **Faktureret (antal)** på den oprindelige købsordre eller rammekøbsordre opdateres på basis af det fakturerede antal. Dog slettes det oprindelige købsdokument ikke, selvom det er blevet fuldt modtaget og faktureret, og du skal derfor slette købsdokumentet.  

> [!NOTE]
> Den købsfaktura, der oprettes, kan ikke senere rettes eller annulleres. Hvis du vil ændre en købsfaktura, der er oprettet på denne måde, skal du bruge købskreditnotaer. Du kan finde flere oplysninger i [Rette eller annullere ubetalte købsfakturaer](purchasing-how-correct-cancel-unpaid-purchase-invoices.md).

## <a name="to-combine-receipts"></a>Sådan samles leverancer

1. Vælg ![Lightbulb, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **Købsfakturaer**, og vælg derefter det relaterede link.  
2. Vælg handlingen **Ny**. Du kan finde flere oplysninger i [Registrere køb](purchasing-how-record-purchases.md).  
3. I oversigtspanelet **Linjer** skal du vælge handlingen **Hent købsleverancelinjer**.  
4. Vælg flere købsleverancelinjer, der skal indgå i fakturaen.  

    Hvis du har valgt en forkert leverancelinje, eller hvis du vil begynde forfra, kan du bare slette linjerne på købsfakturaen og derefter bruge funktionen **Hent købsleverancelinjer** igen.  
5. Vælg handlingen **Bogfør** for at fakturere kladden.  

## <a name="to-remove-open-purchase-orders-after-combined-receipt-posting"></a>Sådan fjernes åbne købsordrer efter bogføring af kombineret modtagelse

1. Vælg ![Lightbulb, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **Slet fakturerede købsordrer**, og vælg derefter det relaterede link.  
2. Udfyld felterne efter behov. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)].
3. Vælg knappen **OK**.  

Du kan også slette de individuelle ordrer manuelt.

Gentag trin 1 til 3 for eventuelle andre berørte dokumenter, f.eks. rammekøbsordrer.

## <a name="see-also"></a>Se også

[Køb](purchasing-manage-purchasing.md)  
[Rette eller annullere ubetalte købsfakturaer](purchasing-how-correct-cancel-unpaid-purchase-invoices.md)  
[Arbejde med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]