---
title: "Udlæse betalinger til en elektronisk betalingsfil | Microsoft Docs"
description: "Når du vil oprette kreditorbetalinger, skal du aktivere en tjenesten til konvertering af bankdata, udlæse en bankfil og overføre filen til din netbank for at overføre beløbet."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: bank file export, re-export, bank transfer, AMC, bank data conversion service, funds transfer
ms.date: 06/28/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 2c13559bb3dc44cdb61697f5135c5b931e34d2a8
ms.openlocfilehash: bab124ecc4d98886e41fbee3af00d4913435c993
ms.contentlocale: da-dk
ms.lasthandoff: 09/22/2017

---
# <a name="how-to-export-payments-to-a-bank-file"></a>Fremgangsmåde: Eksportere betalinger til en bankfil
Når du er klar til at bogføre betalinger til dine kreditorer eller refusioner til dine medarbejdere, kan du eksportere en fil med betalingsoplysningerne på kladdelinjerne i vinduet **Udbetalingskladde**. Derefter kan du overføre filen til din bank for at behandle de relaterede pengeoverførsler.

I den generelle version af [!INCLUDE[d365fin_long](includes/d365fin_long_md.md)] bliver en global udbyder af tjenester til konvertering af bankoplysninger til ethvert filformat, som kræves af din bank, konfigureret og tilsluttet. I nordamerikanske versioner kan den samme tjeneste bruges til at sende betalingsfiler som elektronisk pengeoverførsel (EFT), men med en lidt anderledes proces. Se trin 6 i afsnittet "Sådan eksporterer du betalinger til en bankfil".    

> [!NOTE]  
>   Inden du kan udlæse betalingsfiler fra betalingskladden, du skal angive det elektroniske format for den bankkonto, der anvendes, og du skal aktivere tjenesten til konvertering af bankdata. Du kan finde flere oplysninger i [Fremgangsmåde: Oprette bankkonti](bank-how-setup-bank-accounts.md) og [Fremgangsmåde: Konfigurere tjenesten til konvertering af bankdata](bank-how-setup-bank-data-conversion-service.md). Desuden skal du markere afkrydsningsfeltet **Tillad eksport af betaling** i vinduet **Finanskladdenavne**. Du kan finde flere oplysninger under [Arbejde med finanskladder](ui-work-general-journals.md).  

Brug vinduet **Kreditoverførselsjournaler** til at få vist de betalingsfiler, som er eksporteret fra betalingskladden. I dette vindue kan du også udlæse betalingsfiler igen i tilfælde af tekniske fejl eller filændringer. Bemærk dog, at de eksporterede EFT-filer ikke vises i dette vindue og ikke kan reeksporteres.  

## <a name="to-export-payments-to-a-bank-file"></a>Sådan eksporterer du betalinger til en bankfil
1. Vælg ikonet ![Søg efter side eller rapport](media/ui-search/search_small.png "Ikonet Søg efter side eller rapport"), angiv **Udbetalingskladder**, og vælg derefter det relaterede link.
2. Udfyld udbetalingskladdelinjer, f.eks. ved hjælp af funktionen **Lav kreditorbetalingsforslag**. Du kan finde flere oplysninger i [Fremgangsmåde: Lave kreditorbetalingsforslag](payables-how-suggest-vendor-payments.md).
3. Udfyld felterne på betalingskladdelinjerne efter behov. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

> [!NOTE]  
>   Hvis du bruger elektroniske pengeoverførsler, skal du vælge enten **Elektronisk betaling** eller **Elektronisk betaling-IAT** i feltet **Bankbetalingstype**. Andre fileksporttjenester og deres formater kræver andre konfigurationsværdier i vinduerne **Bankkontokort** og **Kreditors bankkontokort**. Du får information om forkerte eller manglende konfigurationsværdier, når du prøver at eksportere filen.

4. Når du har fuldført alle betalingskladdelinjer, skal du vælge handlingen **Eksportér**.
5. I vinduet **Eksportér elektroniske betalinger** skal du udfylde felterne efter behov.

    Eventuelle fejlmeddelelser vises i faktaboksen **Fejl i betalingsfil**, hvor du også kan vælge en fejlmeddelelse for at se detaljerede oplysninger. Du skal løse alle fejl, før betalingsfilen kan eksporteres.

    > [!TIP]  
>   Når du bruger tjenesten til konvertering af bankdata, angiver en fælles fejlmeddelelse, at bankkontonummeret ikke har den længde, der kræves af din bank. For at undgå eller løse fejlen skal du fjerne værdien i feltet **IBAN** i vinduet **Bankkontokort** og derefter bruge feltet **Bankkontonr.** til at angive et bankkontonummer i det format, som kræves af din bank.

6. I vinduet **Gem som** skal du angive den placering, filen eksporteres til, og derefter vælge **Gem**.

    > [!NOTE]  
>   Hvis du bruger elektroniske pengeoverførsler, skal du gemme den kreditorindbetalingsformular, der oprettes, som et Word-dokument eller vælge at få den sendt som e-mail direkte til kreditoren. Betalingerne til føjes nu i vinduet **Generer EFT-fil**, hvor du kan oprette flere betalingsordrer sammen for at spare transmissionsomkostninger. Du kan finde flere oplysninger i følgende trin.
7. I vinduet **Udbetalingskladde** skal du vælg handlingen **Generer EFT-fil**.

    I vinduet **Generer EFT-fil** vises alle betalinger, der er konfigureret til elektroniske pengeoverførsler, som du har eksporteret fra betalingskladden for en bestemt bankkonto, men som endnu ikke er oprettet, i oversigtspanelet **Linjer**.
8. Vælg handlingen **Generer EFT-fil** for at eksportere én fil for alle EFT-betalinger.
9. I vinduet **Gem som** skal du angive den placering, filen eksporteres til, og derefter vælge **Gem**.

Betalingsfilen til banken er eksporteret til den placering, du angiver, og du kan fortsætte med at overføre den til din elektroniske bankkonto og foretage de faktiske betalinger. Derefter kan du bogføre de eksporterede betalingskladdelinjer.

## <a name="to-export-payments-that-represent-customer-refunds"></a>Sådan eksporteres betalinger, der repræsenterer debitorrefusioner
Nedenfor beskrives en løsning på, hvordan du eksporterer elektroniske refusionsbetalinger.

> [!CAUTION]  
>   De betalingskladdelinjer, der oprettes, kan ikke bogføres, slettes eller annulleres.
1. Opret kunden som kreditor. Navngiv kreditoren "Kunde X for refusioner" f.eks. Du kan finde flere oplysninger i [Fremgangsmåde: Registrere nye kreditorer](purchasing-how-register-new-vendors.md).
2. På betalingskladdelinjen for kunden, kan du indstille feltet **Kontotype** til **Debitor** og feltet **Dokumenttype** til **Refusion**.
3. Udfør de normale trin til eksport af betaling som beskrevet i afsnittet "Sådan eksporterer du betalinger til en bankfil".

## <a name="to-plan-when-to-post-exported-payments"></a>Sådan planlægger du, hvornår eksporterede betalinger skal bogføres
Hvis du ikke vil bogføre en betalingskladdelinje for en eksporteret betaling, for eksempel fordi du venter på bekræftelse af, at transaktionen er blevet behandlet af banken, kan du bare slette kladdelinjen. Når du senere opretter en betalingskladdelinje for at betale det resterende beløb på fakturaen, kan du i feltet **Samlet eksporteret beløb** se, hvor meget af betalingsbeløbet der allerede er blevet eksporteret. Du kan også finde detaljerede oplysninger om den eksporterede total ved at vælge knappen **Poster i kreditoverførselsjournal** for at se detaljer om eksporterede betalingsfiler.

Hvis du følger en proces, hvor du ikke bogfører betalinger, før du har fået bekræftet, at de er blevet behandlet i banken, kan du gøre dette på to måder.

* I en betalingskladde med foreslåede betalingslinjer kan du sortere på enten kolonnen **Eksporteret til betalingsfil** eller **Samlet eksporteret beløb** og derefter slette betalingsforslag for åbne fakturaer for betalinger, der allerede er foretaget, og du ikke vil foretage betalinger af.
* I vinduet **Lav kreditorbetalingsforslag**, hvor du angiver, hvilke betalinger der indsættes i betalingskladden, kan du også markere afkrydsningsfeltet **Spring over eksporterede betalinger**, hvis du ikke vil indsætte kladdelinjerne til betalinger, der allerede er eksporteret.

Du kan se oplysninger om eksporterede betalinger ved at vælge handlingen **Historik for eksporterede betalinger**.

## <a name="to-re-export-payments-to-a-bank-file"></a>Sådan reeksporter du betalinger til en bankfil
Du kan eksportere betalingsfiler igen fra vinduet **Kreditoverførselsjournaler**. Før du sletter eller bogfører betalingskladdelinjer, kan du også geneksportere betalingsfilen fra vinduet **Udbetalingskladde** ved bare at eksportere den igen. Hvis du har slettet eller bogført betalingskladdelinjerne efter at have eksporteret dem, kan du geneksportere den samme betalingsfil fra vinduet **Kreditoverførselsjournaler**. Vælg linjen for batch af kreditoverførsler, du vil eksportere igen, og brug derefter handlingen **Reeksportér betalinger til fil**.

> [!NOTE]  
>   Eksporterede EFT-filer vises ikke i vinduet **Kreditoverførselsjournaler** og kan ikke reeksporteres.

1. Vælg ikonet ![Søg efter side eller rapport](media/ui-search/search_small.png "Ikonet Søg efter side eller rapport"), angiv **Kreditoverførselsjournaler**, og vælg derefter det relaterede link.
2. Vælg den betalingseksport, du vil eksportere igen, og vælg derefter handlingen **Reeksportér betalinger til fil**.

## <a name="see-also"></a>Se også
[Gæld](payables-manage-payables.md)  
[Opsætning af indkøb](purchasing-setup-purchasing.md)  
[Arbejde med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

## [!INCLUDE[d365fin](includes/free_trial_md.md)]

