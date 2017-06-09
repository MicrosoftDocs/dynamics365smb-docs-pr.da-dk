---
title: "Fremgangsmåde: Registrere særlige salgspriser og rabatter | Microsoft Docs"
description: "Fremgangsmåde: Registrere særlige salgspriser og rabatter"
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
ms.openlocfilehash: 5ceddded2f95e15a6a7449bf2776b7776ce8a55c
ms.contentlocale: da-dk
ms.lasthandoff: 05/04/2017


---
# <a name="how-to-record-special-sales-prices-and-discounts"></a>Fremgangsmåde: Registrere særlige salgspriser og rabatter
De forskellige pris- og rabataftaler, der gælder ved salg til forskellige debitorer, skal defineres, så de aftalte regler og værdier anvendes i de salgsdokumenter, der oprettes for debitorerne.

Når du har registreret særpriser og linjerabatter for salg og køb, sørger [!INCLUDE[d365fin](includes/d365fin_md.md)] for, at dine avance på varehandel altid er optimal ved automatisk at beregne den bedste pris på salgs- og købsdokumenter og på sags- og varekladdelinjer. Du kan finde flere oplysninger under [Avanceret: Beregning af bedste pris](advanced-best-price-calculation.md).

Med hensyn til priser kan du få en særlig salgspris indsat på salgslinjerne, hvis en bestemt kombination af kunde, vare, minimumantal, enhed eller start-/slutdato findes.

Med hensyn til rabatter kan du oprette og bruge to typer salgsrabat:

| Rabattype | Beskrivelse |
| --- | --- |
| **Salgslinjerabat** |En beløbsrabat, der indsættes på salgslinjerne, hvis en bestemt kombination af kunde, vare, minimumsantal, enhed eller start-/slutdato findes. Dette fungerer på samme måde som for salgspriser. |
| **Fakturarabat** |En procentvis rabat, der fratrækkes fra dokumenttotalen, hvis værdibeløbet for alle linjer i et salgsdokument overstiger et bestemt minimum. |

Da salgspriser og salgslinjerabatter er baseret på en kombination af vare og debitor, kan du også udføre denne konfiguration fra varekortet for den vare, som reglerne og værdierne gælder for.

## <a name="to-set-up-a-sales-price-for-a-customer"></a>Sådan konfigureres salgspriser for en debitor
1. I øverste højre hjørne skal du vælge ikonet **Søg efter side eller rapport** ![Søg efter side eller rapport](media/ui-search/search_small.png "Ikonet Søg efter side eller rapport"), angive **Debitorer** og derefter vælge det relaterede link.
2. Åbn det relevante debitorkort, og vælg derefter handlingen **Priser**.

    Feltet **Salgstype** er på forhånd udfyldt med **Debitor**, og feltet **Salgskode** er udfyldt med debitornummeret.
3. Udfyld felterne på linjen efter behov. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)] Udfyld en linje for hver kombination, som yder en særlig salgspris til kunden.

## <a name="to-set-up-a-sales-line-discount-for-a-customer"></a>Sådan konfigureres salgslinjerabatter for en debitor
1. I øverste højre hjørne skal du vælge ikonet **Søg efter side eller rapport** ![Søg efter side eller rapport](media/ui-search/search_small.png "Ikonet Søg efter side eller rapport"), angive **Debitorer** og derefter vælge det relaterede link.
2. Åbn det relevante debitorkort, og vælg derefter handlingen **Linjerabatter**.

    Feltet **Salgstype** er på forhånd udfyldt med **Debitor**, og feltet **Salgskode** er udfyldt med debitornummeret.
3. Udfyld felterne på linjen efter behov. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)] Udfyld en linje for hver kombination, som yder en salgslinjerabat til kunden.

## <a name="to-set-up-an-invoice-discount-for-a-customer"></a>Sådan oprettes en fakturarabat for en debitor
Når du har besluttet, hvilke kunder der skal have fakturarabatter, skal du angive fakturarabatkoden på debitorkortene og definere betingelserne for hver kode.

1. I øverste højre hjørne skal du vælge ikonet **Søg efter side eller rapport** ![Søg efter side eller rapport](media/ui-search/search_small.png "Ikonet Søg efter side eller rapport"), angive **Debitorer** og derefter vælge det relaterede link.
2. Åbn debitorkortet for en debitor, der kan ydes mængderabat til.
3. Vælg en kode i feltet **Fakturarabatkode** for de fakturarabatbetingelser, som skal bruges til automatisk beregning af fakturarabat til debitoren.

    **Bemærk**: Fakturarabatkoder repræsenteres af eksisterende debitorkort. Det gør det muligt hurtigt at tildele betingelserne for fakturarabatten til debitorer ved at vælge navnet på en anden debitor, der skal have samme betingelser.

    Fortsæt med at angive nye fakturarabatbetingelser for salg.
4. I vinduet **Debitorkort** skal du vælge handlingen **Fakturarabatter**. Vinduet **Deb./fakt.-rabatter** åbnes.
5. Angiv koden for den valuta, som fakturarabatbetingelserne på linjen gælder for, i feltet **Valutakode**. Lad feltet stå tomt for at angive fakturarabatbetingelser for RV.
6. Angiv det minimumsbeløb, der berettiger til rabatten, i feltet **Min. beløb**.
7. I feltet **Rabatpct.** skal du angive fakturarabatten som en procentdel af fakturabeløbet.
8. Gentag trin 5-7 for hver valuta, som debitoren får en personlig fakturarabat for.

Fakturarabatten er nu oprettet og knyttet til den pågældende debitor. Når du vælger debitorkoden i feltet **Fakturarabatkode** på andre debitorkort, knyttes samme fakturarabat til den pågældende debitor.

## <a name="see-also"></a>Se også
[Avanceret: Beregning af bedste pris](advanced-best-price-calculation.md)  
[Konfigurere salg](sales-setup-sales.md)  
[Salg](sales-manage-sales.md)  
[Arbejde med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

