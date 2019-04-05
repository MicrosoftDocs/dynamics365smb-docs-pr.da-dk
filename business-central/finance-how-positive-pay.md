---
title: Eksportere Positive Pay-filer | Microsoft Docs
description: Du kan sikre dig, at din bank kun afregner validerede checks og beløb, ved at eksportere en Positive Pay-fil, der indeholder kreditor- og betalingsoplysninger.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: check, clearing
ms.date: 10/01/2018
ms.author: sgroespe
ms.openlocfilehash: 61f3d3fcd093c9fca4e23481ff3b527714b85379
ms.sourcegitcommit: 1bcfaa99ea302e6b84b8361ca02730b135557fc1
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 03/08/2019
ms.locfileid: "792492"
---
# <a name="export-a-positive-pay-file"></a>Eksportere en Positive Pay-fil
Du kan sikre dig, at din bank kun afregner validerede checks og beløb, ved at eksportere en Positive Pay-fil, der indeholder relevante betalingsoplysninger, checknummer og betalingsbeløb, som du sender til banken som reference, når du behandler betalinger.

[!INCLUDE[d365fin](includes/d365fin_md.md)] er konfigureret til at understøtte Positive Pay-filer for Bank of America og City Bank.

## <a name="to-set-up-a-bank-account-for-positive-pay"></a>Sådan konfigureres en bankkonto til Positive Pay
1. Vælg ikonet ![Elpære, der åbner funktionen Fortæl mig](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig"), angiv **Bankkonti**, og vælg derefter det relaterede link.
2. Åbn kortet for den bank, som du vil bruge Positive Pay til.
3. I feltet **Eksportkode for Positive Pay** skal du angive POSPAYBANK.
4. Luk siden.

## <a name="to-export-a-positive-pay-file"></a>Sådan eksporteres en Positive Pay-fil
1. Vælg ikonet ![Elpære, der åbner funktionen Fortæl mig](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig"), angiv **Bankkonti**, og vælg derefter det relaterede link.
2. Vælg den bankkonto, du vil eksportere en Positive Pay-fil for.
3. Vælg handlingen **Eksport af Positive Pay-betalingsposter**.

    Siden **Eksport af Positive Pay-betalingsposter** åbnes og viser betalinger, der er foretaget for bankkontoen, siden den sidste overførselsdato, som vist i felterne **Sidst uploadet den** og **Sidst uploadet kl.**.
4. I feltet **Skæringsdato for upload** skal du angiver en dato, før hvilken betalinger ikke inkluderes i den eksporterede fil.
5. Vælg handlingen **Eksportér**.
6. På siden **Udlæs fil** skal du klikke på knappen **Gem** og derefter gemme filen på et relevant sted.
7. Overfør filen til din netbank.
8. Notér det bekræftelsesnummer, der vises, når filoverførslen er fuldført, og kopiér det.

Sådan får du vist eksporterede Positive Pay-poster

1. Vælg ikonet ![Elpære, der åbner funktionen Fortæl mig](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig"), angiv **Bankkonti**, og vælg derefter det relaterede link.
2. Vælg den bankkonto, du vil have vist Positive Pay-eksportposter for.
3. Vælg handlingen **Positive Pay-betalingsposter**.

    På siden **Positive Pay-betalingsposter** kan du se alle de eksporterede Positive Pay-poster for bankkontoen.
4. I feltet **Bekræftelsesnr.** skal du for hver eksportpost angive bekræftelsesnummeret, der vises, når filen er overført til banken.
5. For at få vist de relaterede betalingslinjer skal du vælge handlingen **Oplysninger om Positive Pay-betalingspost**.

Sådan reeksporteres Positive Pay-filer

1. Vælg ikonet ![Elpære, der åbner funktionen Fortæl mig](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig"), angiv **Bankkonti**, og vælg derefter det relaterede link.
2. Vælg den bankkonto, du vil reeksportere Positive Pay-filer for.
3. Vælg handlingen **Positive Pay-betalingsposter**.
4. Vælg den linje for den Positive Pay-eksportfil, som du vil reeksportere.
5. På siden **Positive Pay-betalingsposter** skal du vælge handlingen **Reeksportér Positive Pay-betaling til fil**.

## <a name="see-also"></a>Se også
[Finans](finance.md)  
[Konfigurere Finans](finance-setup-finance.md)  
[Arbejde med finanskladder](ui-work-general-journals.md)  
[Arbejde med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)
