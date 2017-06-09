---
title: "Fremgangsmåde: Registrere særlige købspriser og rabatter | Microsoft Docs"
description: "Fremgangsmåde: Registrere købspriser og rabatter"
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: special price, alternate price, pricing
ms.date: 03/29/2017
ms.author: sgroespe
ms.translationtype: Human Translation
ms.sourcegitcommit: a31be0f9d07e2abb591e26f6bae34c6f6e4dcda6
ms.openlocfilehash: 67625231d62a72bb0a62ab362bce92aa16b8956e
ms.contentlocale: da-dk
ms.lasthandoff: 05/04/2017


---
# <a name="how-to-record-special-purchase-prices-and-discounts"></a>Fremgangsmåde: Registrere særlige købspriser og rabatter
De forskellige pris- og betalingsaftaler, der gælder, når du køber fra forskellige leverandører, skal defineres, så de aftalte regler og værdier anvendes i de købsdokumenter, der oprettes for leverandørerne.

Når du har registreret særpriser og linjerabatter for salg og køb, sørger [!INCLUDE[d365fin](includes/d365fin_md.md)] for, at dine avance på varehandel altid er optimal ved automatisk at beregne den bedste pris på salgs- og købsdokumenter og på sags- og varekladdelinjer. Du kan finde flere oplysninger under [Avanceret: Beregning af bedste pris](advanced-best-price-calculation.md).

Med hensyn til priser kan du få en særlig købspris indsat på købslinjerne, hvis en bestemt kombination af leverandør, vare, minimumsantal, enhed eller start-/ slutdato findes.

Med hensyn til rabatter kan du oprette og bruge to typer købsrabat:

| Rabattype | Beskrivelse |
| --- | --- |
| **Købslinjerabat** |En beløbsrabat, der indsættes på købslinjerne, hvis en bestemt kombination af leverandør, vare, minimumsantal, enhed eller start-/ slutdato findes. Dette fungerer på samme måde som for købspriser. |
| **Fakturarabat** |En procentvis rabat, der fratrækkes fra dokumenttotalen, hvis værdibeløbet for alle linjer i et købsdokument overstiger et bestemt minimum. |

Da købslinjerabatter og købspriser er baseret på en kombination af vare og leverandør, kan du også angive denne konfiguration fra det varekort, hvor reglerne og værdierne er defineret. Du kan finde flere oplysninger under [Fremgangsmåde: Registrere nye varer](inventory-how-register-new-items.md).

## <a name="to-set-up-a-special-purchase-price-for-a-vendor"></a>Sådan oprettes en særlig købspris for en kreditor
1. I øverste højre hjørne skal du vælge ikonet **Søg efter side eller rapport** ![Søg efter side eller rapport](media/ui-search/search_small.png "Ikonet Søg efter side eller rapport"), angive **Kreditorer** og derefter vælge det relaterede link.
2. Åbn det relevante kreditorkort, og vælg derefter handlingen **Priser**.

    Feltet **Indkøbstype** er på forhånd udfyldt med **Kreditor**, og feltet **Indkøbskode** er på forhånd udfyldt med kreditornummer.
3. Udfyld felterne på linjen efter behov. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
4. Udfyld en linje for hver kombination, som kreditoren yder dig en købslinjerabat for.

## <a name="to-set-up-a-line-discount-for-a-vendor"></a>Sådan oprettes en linjerabat for en kreditor
1. I øverste højre hjørne skal du vælge ikonet **Søg efter side eller rapport** ![Søg efter side eller rapport](media/ui-search/search_small.png "Ikonet Søg efter side eller rapport"), angive **Kreditorer** og derefter vælge det relaterede link.
2. Åbn det relevante kreditorkort, og vælg derefter handlingen **Linjerabatter**.

    Feltet **Indkøbstype** er på forhånd udfyldt med **Kreditor**, og feltet **Indkøbskode** er på forhånd udfyldt med kreditornummer.
3. Udfyld felterne på linjen efter behov. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
4. Udfyld en linje for hver kombination, som kreditoren yder dig en købslinjerabat for.

## <a name="to-set-up-an-invoice-discount-for-a-vendor"></a>Sådan oprettes en fakturarabat for en kreditor
Når dine kreditorer har oplyst, hvilke fakturarabatter de yder, skal du angive fakturarabatkoden på kreditorkortene og definere betingelserne for hver kode.

1. I øverste højre hjørne skal du vælge ikonet **Søg efter side eller rapport** ![Søg efter side eller rapport](media/ui-search/search_small.png "Ikonet Søg efter side eller rapport"), angive **Kreditorer** og derefter vælge det relaterede link.
2. Åbn kreditorkortet for en kreditor, der kan ydes mængderabat til.
3. Vælg en kode i feltet **Fakturarabatkode** for de fakturarabatbetingelser, som skal bruges til automatisk beregning af fakturarabat til kreditoren.

    **Bemærk**: Fakturarabatkoder repræsenteres af eksisterende kreditorkort. Det gør det muligt hurtigt at tildele betingelserne for fakturarabatten til kreditorer ved at vælge navnet på en anden leverandører, der skal have samme betingelser.

    Fortsæt med at angive nye fakturarabatbetingelser for køb.
4. I vinduet **Kreditorkort** skal du vælge handlingen **Fakturarabatter**. Vinduet **Kred./fakt.-rabatter** åbnes.
5. Angiv koden for den valuta, som fakturarabatbetingelserne på linjen gælder for, i feltet **Valutakode**. Lad feltet stå tomt for at angive fakturarabatbetingelser for RV.
6. Angiv det minimumsbeløb, der berettiger til rabatten, i feltet **Min. beløb**.
7. I feltet **Rabatpct.** skal du angive fakturarabatten som en procentdel af fakturabeløbet.
8. Gentag trin 5-7 for hver valuta, som kreditoren får en personlig fakturarabat for.

Fakturarabatten er nu oprettet og knyttet til den pågældende kreditor. Når du vælger kreditorkoden i feltet **Fakturarabatkode** på andre kreditorkort, knyttes samme fakturarabat til den pågældende kreditor.

## <a name="see-also"></a>Se også
[Avanceret: Beregning af bedste pris](advanced-best-price-calculation.md)  
[Opsætning af indkøb](purchasing-setup-purchasing.md)  
[Køb](purchasing-manage-purchasing.md)  
[Arbejde med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

