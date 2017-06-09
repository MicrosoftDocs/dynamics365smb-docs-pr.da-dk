---
title: "Fremgangsmåde: Eksportere Positive Pay-filer | Microsoft Docs"
description: "Beskriver, hvordan du sikrer dig, at din bank kun afregner validerede checks og beløb, ved at eksportere en Positive Pay-fil, der indeholder kreditor- og betalingsoplysninger."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: check, clearing
ms.date: 03/24/2017
ms.author: sgroespe
ms.translationtype: Human Translation
ms.sourcegitcommit: a31be0f9d07e2abb591e26f6bae34c6f6e4dcda6
ms.openlocfilehash: ee93f8eb889ae1d635bca22ff133e1523fd1b825
ms.contentlocale: da-dk
ms.lasthandoff: 05/04/2017


---
# <a name="how-to-export-a-positive-pay-file"></a>Fremgangsmåde: Eksportere en Positive Pay-fil
Du kan sikre dig, at din bank kun afregner validerede checks og beløb, ved at eksportere en Positive Pay-fil, der indeholder relevante betalingsoplysninger, checknummer og betalingsbeløb, som du sender til banken som reference, når du behandler betalinger.

[!INCLUDE[d365fin](includes/d365fin_md.md)] er konfigureret til at understøtte Positive Pay-filer for Bank of America og City Bank.

## <a name="to-set-up-a-bank-account-for-positive-pay"></a>Sådan konfigureres en bankkonto til Positive Pay
1. I øverste højre hjørne skal du vælge ikonet **Søg efter side eller rapport** ![Søg efter side eller rapport](media/ui-search/search_small.png "Ikonet Søg efter side eller rapport"), angive **Bankkonti** og derefter vælge det relaterede link.
2. Åbn kortet for den bank, som du vil bruge Positive Pay til.
3. I feltet **Eksportkode for Positive Pay** skal du angive POSPAYBANK.
4. Luk vinduet.

## <a name="to-export-a-positive-pay-file"></a>Sådan eksporteres en Positive Pay-fil
1. I øverste højre hjørne skal du vælge ikonet **Søg efter side eller rapport** ![Søg efter side eller rapport](media/ui-search/search_small.png "Ikonet Søg efter side eller rapport"), angive **Bankkonti** og derefter vælge det relaterede link.
2. Vælg den bankkonto, du vil eksportere en Positive Pay-fil for.
3. Vælg handlingen **Eksport af Positive Pay-betalingsposter**.

    Vinduet **Eksport af Positive Pay-betalingsposter** åbnes og viser betalinger, der er foretaget for bankkontoen, siden den sidste overførselsdato, som vist i felterne **Sidst uploadet den** og **Sidst uploadet kl.**.
4. I feltet **Skæringsdato for upload** skal du angiver en dato, før hvilken betalinger ikke inkluderes i den eksporterede fil.
5. Vælg handlingen **Eksportér**.
6. I vinduet **Udlæs fil** skal du klikke på knappen **Gem** og derefter gemme filen på et relevant sted.
7. Overfør filen til din netbank.
8. Notér det bekræftelsesnummer, der vises, når filoverførslen er fuldført, og kopiér det.

Sådan får du vist eksporterede Positive Pay-poster

1. I øverste højre hjørne skal du vælge ikonet **Søg efter side eller rapport** ![Søg efter side eller rapport](media/ui-search/search_small.png "Ikonet Søg efter side eller rapport"), angive **Bankkonti** og derefter vælge det relaterede link.
2. Vælg den bankkonto, du vil have vist Positive Pay-eksportposter for.
3. Vælg handlingen **Positive Pay-betalingsposter**.

    I vinduet **Positive Pay-betalingsposter** kan du se alle de eksporterede Positive Pay-poster for bankkontoen.
4. I feltet **Bekræftelsesnr.** skal du for hver eksportpost angive bekræftelsesnummeret, der vises, når filen er overført til banken.
5. For at få vist de relaterede betalingslinjer skal du vælge handlingen **Oplysninger om Positive Pay-betalingspost**.

Sådan reeksporteres Positive Pay-filer

1. I øverste højre hjørne skal du vælge ikonet **Søg efter side eller rapport** ![Søg efter side eller rapport](media/ui-search/search_small.png "Ikonet Søg efter side eller rapport"), angive **Bankkonti** og derefter vælge det relaterede link.
2. Vælg den bankkonto, du vil reeksportere Positive Pay-filer for.
3. Vælg handlingen **Positive Pay-betalingsposter**.
4. Vælg den linje for den Positive Pay-eksportfil, som du vil reeksportere.
5. I vinduet **Positive Pay-betalingsposter** skal du vælge handlingen **Reeksportér Positive Pay-betaling til fil**.

## <a name="see-also"></a>Se også
[Finans](finance.md)  
[Konfigurere Finans](finance-setup-finance.md)  
[Fremgangsmåde: Arbejde med finanskladder](ui-work-general-journals.md)  
[Arbejde med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

