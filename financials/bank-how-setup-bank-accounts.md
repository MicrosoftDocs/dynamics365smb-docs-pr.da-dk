---
title: Oprette bankkonti | Microsoft Docs
description: Du kan afstemme bankkonti i Financials med kontoudtog fra banken.
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: Yodlee, feed, stream
ms.date: 06/02/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 81636fc2e661bd9b07c54da1cd5d0d27e30d01a2
ms.openlocfilehash: f46e95e24ef39a93bc93cfda1b9c575b07273566
ms.contentlocale: da-dk
ms.lasthandoff: 09/22/2017

---
# <a name="how-to-set-up-bank-accounts"></a>Fremgangsmåde: Oprette bankkonti
Brug bankkonti i [!INCLUDE[d365fin](includes/d365fin_md.md)] til at holde styr på dine banktransaktioner. Konti kan være i den lokale valuta eller i fremmed valuta. Når du har oprettet bankkonti, kan du også bruge funktionen til kontrol af udskrevne check.

## <a name="to-set-up-bank-accounts"></a>Sådan oprettes bankkonti
1. Vælg ikonet ![Søg efter side eller rapport](media/ui-search/search_small.png "Ikonet Søg efter side eller rapport"), angiv **Bankkonti**, og vælg derefter det relaterede link.
2. I vinduet **Bankkonti** skal du vælge handlingen **Ny**.
3. Udfyld felterne efter behov. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

## <a name="to-set-up-your-bank-account-for-import-or-export-of-bank-files"></a>Sådan oprettes bankkontoen for import eller eksport af bankfiler
Felter i oversigtspanelet **Overførsel** i vinduet **Bankkontokort** er relateret til indlæsning og udlæsning af bankfeeds og -filer. Du kan finde flere oplysninger i [Fremgangsmåde: Konfigurere tjenesten til konvertering af bankdata](bank-how-setup-bank-data-conversion-service.md) og [Fremgangsmåde: Konfigurere tjenesten Envestnet Yodlee Bank Feeds](bank-how-setup-bank-statement-service.md).

1. Vælg ikonet ![Søg efter side eller rapport](media/ui-search/search_small.png "Ikonet Søg efter side eller rapport"), angiv **Bankkonti**, og vælg derefter det relaterede link.
2. Åbn kortet for en bankkonto, du vil eksportere eller importere bankfiler for.
3. Udfyld felterne efter behov i oversigtspanelet **Overførsel**. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

> [!NOTE]  
>   Andre fileksporttjenester og deres formater kræver andre konfigurationsværdier i vinduet **Bankkontokort**. Du får information om forkerte eller manglende konfigurationsværdier, når du prøver at eksportere filen. Så læs omhyggeligt korte beskrivelser af felterne, eller se de relaterede emner med fremgangsmåder. Eksport af en betalingsfil med f.eks. nordamerikansk elektronisk pengeoverførsel (EFT) kræver, at både **Sidste remitteringsadvisnr.** og **Transitnr.** er udfyldt. Du kan finde flere oplysninger i [Fremgangsmåde: Eksportere betalinger til en bankfil](payables-how-export-payments-bank-file.md).

## <a name="to-set-up-vendor-bank-accounts-for-export-of-bank-files"></a>Sådan konfigureres kreditorbankkonti til eksport af bankfiler
Felter i oversigtspanelet **Overførsel** i vinduet **Kreditors bankkontokort** er relateret til udlæsning af bankfeeds og -filer. Du kan finde flere oplysninger i [Fremgangsmåde: Konfigurere tjenesten til konvertering af bankdata](bank-how-setup-bank-data-conversion-service.md) og [Fremgangsmåde: Eksportere betalinger til en bankfil](payables-how-export-payments-bank-file.md).

1. Vælg ikonet ![Søg efter side eller rapport](media/ui-search/search_small.png "Ikonet Søg efter side eller rapport"), angiv **Bankkonti**, og vælg derefter det relaterede link.
2. Åbn kortet for en kreditor, hvis bankkonto du vil eksportere betalingsbankfiler til.
3. Vælg handlingen **Bankkonti**.
3. Udfyld felterne efter behov i vinduet **Kreditors bankkontokort** i oversigtspanelet **Overførsel**. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

## <a name="see-also"></a>Se også
[Konfigurere banktransaktioner](bank-setup-banking.md)  
[Håndtere bankkonti](bank-manage-bank-accounts.md)  
[Arbejde med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

