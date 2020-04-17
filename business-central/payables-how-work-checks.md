---
title: Udstede, udskrive og annullere checks | Microsoft Docs
description: Beskriver, hvordan du udsteder checks ved hjælp af udbetalingskladden, udskriver checks og annullerer eller får vist checkposter i Business Central.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: payment journal, print check, vendor payment, creditor, debt, balance due, AP
ms.date: 04/01/2020
ms.author: sgroespe
ms.openlocfilehash: 12de08f6163c141a2c2e8669a814616b2b5fc04b
ms.sourcegitcommit: 88e4b30eaf6fa32af0c1452ce2f85ff1111c75e2
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 04/01/2020
ms.locfileid: "3190223"
---
# <a name="make-check-payments"></a>Foretage betalinger med check
Du kan udstede elektroniske og manuelle check [!INCLUDE[d365fin](includes/d365fin_md.md)]. Udbetalingskladden bruges i begge tilfælde, når der udstedes checks til leverandører/kreditorer. Du kan også annullere checks og se checkposter.

Følgende procedure viser, hvordan du kan betale en kreditor med en computercheck ved at udligne betalingen til den relevante kreditorfaktura, udskrive checken og derefter bogføre betalingen som betalt. Dette resulterer i positive kreditorposter, udlignet til negative bankposter og fysiske checks til behandling i banken.

Du kan betale med to checktyper. Ved begge typer skal feltet **Modkontotype** eller **Kontotype** indeholde **Bankkonto**.

- **Computercheck**: Vælg denne mulighed, hvis du vil udskrive en check på beløbet fra udbetalingskladdelinjen. Du skal udskrive checkene, før du kan bogføre kladdelinjerne.
- **Manuel check**: Vælg denne mulighed, hvis du har oprettet en check manuelt og vil oprette en tilsvarende checkpost på beløbet. Du kan ikke udskrive checken med denne indstilling.

> [!NOTE]  
> Du kan kontrollere, at din bank kun afregner validerede checks og beløb, ved at sende banken en fil, der indeholder kreditor- check- og betalingsoplysninger. Du kan finde flere oplysninger under [Eksportere en Positive Pay-fil](finance-how-positive-pay.md).

Printeren skal være konfigureret korrekt med checkformater, og du skal definere hvilket checklayout, der skal bruges. Du kan finde flere oplysninger under [Vælge et checklayout](finance-how-define-check-layouts.md)

Du kan udskrive op til 10 fakturaer på en side til en checktalon. Hvis en check skal gælde for mere end 10 fakturaer, annullere vi checken på første side, når du udskriver talonen, og skriver ordet ANNULLERET på checken. Vi udskriver derefter resten af fakturaerne og det samlede checkbeløb på den anden side.

## <a name="to-pay-a-vendor-invoice-with-a-computer-check"></a>Sådan betales en kreditorfaktura med en computercheck
I følgende fremgangsmåde vises, hvordan du betaler en kreditor med check. Fremgangsmåden er den samme, hvis du vil refundere en debitor med check.

1. Vælg ikonet ![Elpære, der åbner funktionen Fortæl mig](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig"), angiv **Udbetalingskladder**, og vælg derefter det relaterede link.
2. Udfyld betalingskladdelinjerne. Du kan finde flere oplysninger i [Registrere betalinger og refusioner](payables-how-post-payments-refunds.md).
3. I feltet **Betalingsformkode** skal du vælge **Check**.
4. I feltet **Bankbetalingstype** skal du vælge **Computercheck**.
5. Vælg handlingen **Udskriv check**.
6. På siden **Check** skal du udfylde felterne efter behov. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
7. Vælg knappen **Send til**, vælg indstillingen **PDF-dokument**, og vælg derefter knappen **OK**.

    Den fysiske check kan nu sendes til behandling i banken. Fortsæt med at bogføre betalingen som udlignet til leverandøren og dermed betalt i systemet.
8. Vælg handlingen **Bogfør**.

Der oprettes helt udlignede kreditorposter og bankposter.

> [!NOTE]  
> Hvis du vil udskrive og betale checks i mere end én valuta fra forskellige bankkonti, skal du udføre kørslen **Udskriv check** separat for hver valuta og angive den korrekte bankkonto.

## <a name="to-cancel-printed-checks-that-are-not-posted"></a>Sådan annulleres udskrevne checks, der ikke er blevet bogført
Du kan annullere ikke-bogførte checks, når de er blevet udskrevet, ved hjælp af handlingen **Annuller check** på siden **Udbetalingskladde**.

1. På siden **Udbetalingskladde** skal du vælge **Annuller Check**, og vælg derefter hvilke checks der skal annulleres.

## <a name="to-void-checks"></a>Sådan annulleres checks
Når checkbetalingen er blevet bogført, kan du kun annullere checks fra de resulterende bankposter.

1. Vælg ikonet ![Elpære, der åbner funktionen Fortæl mig](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig"), angiv **Bankkonti**, og vælg derefter det relaterede link.
2. Vælg den relevante bankkonto, vælg handlingen **Rediger**, og vælg derefter handlingen **Checkposter**.
3. På siden **Checkposter** skal du vælge handlingen **Annuller check**.
4. Markér afkrydsningsfeltet **Kun annulleringskontrol**.
5. Vælg knappen **OK**.

## <a name="to-view-a-summary-of-posted-checks"></a>Sådan får du vist en oversigt over bogførte checks
Hvis du vil gennemse bogførte checks, for eksempel for at kontrollere flere checks, der er betalt til én kreditor, kan du bruge rapporten **Bankkonto - checkoplysninger**.
1. Vælg ikonet ![Elpære, der åbner funktionen Fortæl mig](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig"), angiv **Bankkonto - checkoplysninger**, og vælg derefter det relaterede link.
2. Angiv filtre som relevante, og vælg derefter knappen **Eksempel**.

## <a name="see-also"></a>Se også
[Foretage betaling](payables-make-payments.md)  
[Administrere skyldige beløb](payables-manage-payables.md)  
[Konfigurere banktransaktioner](bank-setup-banking.md)  
[Eksportere en Positive Pay-fil](finance-how-positive-pay.md)  
[Arbejde med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)  
