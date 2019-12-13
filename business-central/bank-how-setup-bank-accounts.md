---
title: Oprette bankkonti | Microsoft Docs
description: Du kan afstemme bankkonti med kontoudtog fra banken.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: Yodlee, feed, stream
ms.date: 10/01/2019
ms.author: sgroespe
ms.openlocfilehash: 0e6d9bb39e36ca127ab9d64eb045ab4c64b91d30
ms.sourcegitcommit: cfc92eefa8b06fb426482f54e393f0e6e222f712
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 12/03/2019
ms.locfileid: "2880732"
---
# <a name="set-up-bank-accounts"></a>Sådan oprettes bankkonti
Brug bankkonti i [!INCLUDE[d365fin](includes/d365fin_md.md)] til at holde styr på dine banktransaktioner. Konti kan være i den lokale valuta eller i fremmed valuta. Når du har oprettet bankkonti, kan du også bruge funktionen til kontrol af udskrevne check.<br><br>  

> [!Video https://www.microsoft.com/videoplayer/embed/RE3Vhpl]

## <a name="to-set-up-bank-accounts"></a>Sådan oprettes bankkonti
1. Vælg ikonet ![Elpære, der åbner funktionen Fortæl mig](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig"), angiv **Bankkonti**, og vælg derefter det relaterede link.
2. På siden **Bankkonti** skal du vælge handlingen **Ny**.
3. Udfyld felterne efter behov. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

> [!NOTE]
> For at udfylde feltet **Saldo** med en startsaldo, skal du bogføre en bankkontopost med det pågældende beløb. Du kan gøre dette ved at udføre en afstemning af bankkontoen. Du kan finde flere oplysninger i [Afstemme bankkonti separat](bank-how-reconcile-bank-accounts-separately.md). Du kan også implementere primosaldoen som en del af oprettelse af generelle oplysninger i nye virksomheder ved hjælp af den assisterede opsætningsvejledning **Overflyt virksomhedsdata** . Du kan finde flere oplysninger under [Introduktion](product-get-started.md).

## <a name="to-set-up-your-bank-account-for-import-or-export-of-bank-files"></a>Sådan oprettes bankkontoen for import eller eksport af bankfiler
Felter i oversigtspanelet **Overførsel** på siden **Bankkontokort** er relateret til indlæsning og udlæsning af bankfeeds og -filer. Du kan finde flere oplysninger i [Bruge AMC Banking 365 Fundamentals-udvidelsen](ui-extensions-amc-banking.md) og [Konfigurere tjenesten Envestnet Yodlee Bank Feeds ](bank-how-setup-bank-statement-service.md).

1. Vælg ikonet ![Elpære, der åbner funktionen Fortæl mig](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig"), angiv **Bankkonti**, og vælg derefter det relaterede link.
2. Åbn kortet for en bankkonto, du vil eksportere eller importere bankfiler for.
3. Udfyld felterne efter behov i oversigtspanelet **Overførsel**. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

> [!NOTE]  
>   Andre fileksporttjenester og deres formater kræver andre konfigurationsværdier på siden **Bankkontokort**. Du får information om forkerte eller manglende konfigurationsværdier, når du prøver at eksportere filen. Så læs omhyggeligt korte beskrivelser af felterne, eller se de relaterede emner med fremgangsmåder. Eksport af en betalingsfil med f.eks. nordamerikansk elektronisk pengeoverførsel (EFT) kræver, at både **Sidste remitteringsadvisnr.** og **Transitnr.** er udfyldt. Du kan finde flere oplysninger i [Eksportere betalinger til en bankfil](payables-how-export-payments-bank-file.md).

## <a name="to-set-up-vendor-bank-accounts-for-export-of-bank-files"></a>Sådan konfigureres kreditorbankkonti til eksport af bankfiler
Felter i oversigtspanelet **Overførsel** på siden **Kreditors bankkontokort** er relateret til udlæsning af bankfeeds og -filer. Du kan finde flere oplysninger i [Bruge AMC Banking 365 Fundamentals-udvidelsen](ui-extensions-amc-banking.md) og [Eksportere betalinger til en bankfil](payables-how-export-payments-bank-file.md).

1. Vælg ikonet ![Elpære, der åbner funktionen Fortæl mig](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig"), angiv **Leverandører (Kreditorer)**, og vælg derefter det relaterede link.
2. Åbn kortet for en kreditor, hvis bankkonto du vil eksportere betalingsbankfiler til.
3. Vælg handlingen **Bankkonti**.
3. Udfyld felterne efter behov på siden **Kreditors bankkontokort** i oversigtspanelet **Overførsel**. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

## <a name="see-also"></a>Se også
[Konfigurere banktransaktioner](bank-setup-banking.md)  
[Konfigurere bogføringsgrupper](finance-posting-groups.md)  
[Håndtere bankkonti](bank-manage-bank-accounts.md)  
[Arbejde med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)
