---
title: "Udlæse betalinger til en elektronisk betalingsfil | Microsoft Docs"
description: "Når du vil oprette kreditorbetalinger, skal du aktivere en tjenesten til konvertering af bankdata, udlæse en bankfil og overføre filen til din netbank for at overføre beløbet."
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: bank file export, re-export, bank transfer, AMC, bank data conversion service, funds transfer
ms.date: 10/01/2018
ms.author: sgroespe
redirect_url: finance-make-payments-with-bank-data-conversion-service-or-sepa-credit-transfer
ms.translationtype: HT
ms.sourcegitcommit: 33b900f1ac9e295921e7f3d6ea72cc93939d8a1b
ms.openlocfilehash: 14015c089e3cd6db19a12fe4eed72d523f3aefc5
ms.contentlocale: da-dk
ms.lasthandoff: 11/26/2018

---
# <a name="export-payments-to-a-bank-file"></a>Eksportere betalinger til en bankfil
Når du er klar til at bogføre betalinger til dine kreditorer eller refusioner til dine medarbejdere, kan du eksportere en fil med betalingsoplysningerne på kladdelinjerne på siden **Udbetalingskladde**. Derefter kan du overføre filen til din bank for at behandle de relaterede pengeoverførsler.

I den generelle version af [!INCLUDE[d365fin](includes/d365fin_md.md)] bliver en global udbyder af tjenester til konvertering af bankoplysninger til ethvert filformat, som kræves af din bank, konfigureret og tilsluttet. I nordamerikanske versioner kan den samme tjeneste bruges til at sende betalingsfiler som elektronisk pengeoverførsel (EFT), men med en lidt anderledes proces. Se trin 6 i afsnittet "Sådan eksporterer du betalinger til en bankfil".    

> [!NOTE]  
>   Inden du kan udlæse betalingsfiler fra betalingskladden, du skal angive det elektroniske format for den bankkonto, der anvendes, og du skal aktivere tjenesten til konvertering af bankdata. Du kan finde flere oplysninger i [Oprette bankkonti](bank-how-setup-bank-accounts.md) og [Konfigurere tjenesten til konvertering af bankdata](bank-how-setup-bank-data-conversion-service.md). Desuden skal du markere afkrydsningsfeltet **Tillad eksport af betaling** på siden **Finanskladdenavne**. Du kan finde flere oplysninger under [Arbejde med finanskladder](ui-work-general-journals.md).  

Brug siden **Kreditoverførselsjournaler** til at få vist de betalingsfiler, som er eksporteret fra betalingskladden. På denne side kan du også udlæse betalingsfiler igen i tilfælde af tekniske fejl eller filændringer. Bemærk dog, at de eksporterede EFT-filer ikke vises på denne side og ikke kan reeksporteres.  

## <a name="to-export-payments-to-a-bank-file"></a>Sådan eksporterer du betalinger til en bankfil
I følgende fremgangsmåde vises, hvordan du betaler en kreditor med check. Fremgangsmåden er den samme, hvis du vil refundere en debitor med check.

1. Vælg ikonet ![Elpære, der åbner funktionen Fortæl mig](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig"), angiv **Udbetalingskladder**, og vælg derefter det relaterede link.
2. Udfyld betalingskladdelinjerne. Du kan finde flere oplysninger i [Registrere betalinger og refusioner](payables-how-post-payments-refunds.md).

> [!NOTE]  
>   Hvis du bruger elektroniske pengeoverførsler, skal du vælge enten **Elektronisk betaling** eller **Elektronisk betaling-IAT** i feltet **Bankbetalingstype**. Andre fileksporttjenester og deres formater kræver andre konfigurationsværdier på siderne **Bankkontokort** og **Kreditors bankkontokort**. Du får information om forkerte eller manglende konfigurationsværdier, når du prøver at eksportere filen.

3. Når du har fuldført alle betalingskladdelinjer, skal du vælge handlingen **Eksportér**.
4. På siden **Eksportér elektroniske betalinger** skal du udfylde felterne efter behov.

    Eventuelle fejlmeddelelser vises i faktaboksen **Fejl i betalingsfil**, hvor du også kan vælge en fejlmeddelelse for at se detaljerede oplysninger. Du skal løse alle fejl, før betalingsfilen kan eksporteres.

    > [!TIP]  
    >   Når du bruger tjenesten til konvertering af bankdata, angiver en fælles fejlmeddelelse, at bankkontonummeret ikke har den længde, der kræves af din bank. For at undgå eller løse fejlen skal du fjerne værdien i feltet **IBAN** på siden **Bankkontokort** og derefter bruge feltet **Bankkontonr.** til at angive et bankkontonummer i det format, som kræves af din bank.

5. På siden **Gem som** skal du angive den placering, filen eksporteres til, og derefter vælge **Gem**.

    > [!NOTE]  
    >   Hvis du bruger elektroniske pengeoverførsler, skal du gemme den kreditorindbetalingsformular, der oprettes, som et Word-dokument eller vælge at få den sendt som e-mail direkte til kreditoren. Betalingerne til føjes nu på siden **Generer EFT-fil**, hvor du kan oprette flere betalingsordrer sammen for at spare transmissionsomkostninger. Du kan finde flere oplysninger i følgende trin.
6. På siden **Udbetalingskladde** skal du vælge handlingen **Generer EFT-fil**.

    På siden **Generer EFT-fil** vises alle betalinger, der er konfigureret til elektroniske pengeoverførsler, som du har eksporteret fra betalingskladden for en bestemt bankkonto, men som endnu ikke er oprettet, i oversigtspanelet **Linjer**.
7. Vælg handlingen **Generer EFT-fil** for at eksportere én fil for alle EFT-betalinger.
8. På siden **Gem som** skal du angive den placering, filen eksporteres til, og derefter vælge **Gem**.

Betalingsfilen til banken er eksporteret til den placering, du angiver, og du kan fortsætte med at overføre den til din elektroniske bankkonto og foretage de faktiske betalinger. Derefter kan du bogføre de eksporterede betalingskladdelinjer.

## <a name="to-plan-when-to-post-exported-payments"></a>Sådan planlægger du, hvornår eksporterede betalinger skal bogføres
Hvis du ikke vil bogføre en betalingskladdelinje for en eksporteret betaling, for eksempel fordi du venter på bekræftelse af, at transaktionen er blevet behandlet af banken, kan du bare slette kladdelinjen. Når du senere opretter en betalingskladdelinje for at betale det resterende beløb på fakturaen, kan du i feltet **Samlet eksporteret beløb** se, hvor meget af betalingsbeløbet der allerede er blevet eksporteret. Du kan også finde detaljerede oplysninger om den eksporterede total ved at vælge knappen **Poster i kreditoverførselsjournal** for at se detaljer om eksporterede betalingsfiler.

Hvis du følger en proces, hvor du ikke bogfører betalinger, før du har fået bekræftet, at de er blevet behandlet i banken, kan du gøre dette på to måder.

* I en betalingskladde med foreslåede betalingslinjer kan du sortere på enten kolonnen **Eksporteret til betalingsfil** eller **Samlet eksporteret beløb** og derefter slette betalingsforslag for åbne fakturaer for betalinger, der allerede er foretaget, og du ikke vil foretage betalinger af.
* På siden **Lav kreditorbetalingsforslag**, hvor du angiver, hvilke betalinger der indsættes i betalingskladden, kan du også markere afkrydsningsfeltet **Spring over eksporterede betalinger**, hvis du ikke vil indsætte kladdelinjerne til betalinger, der allerede er eksporteret.

Du kan se oplysninger om eksporterede betalinger ved at vælge handlingen **Historik for eksporterede betalinger**.

## <a name="to-re-export-payments-to-a-bank-file"></a>Sådan reeksporter du betalinger til en bankfil
Du kan eksportere betalingsfiler igen fra siden **Kreditoverførselsjournaler**. Før du sletter eller bogfører betalingskladdelinjer, kan du også geneksportere betalingsfilen fra siden **Udbetalingskladde** ved bare at eksportere den igen. Hvis du har slettet eller bogført betalingskladdelinjerne efter at have eksporteret dem, kan du geneksportere den samme betalingsfil fra siden **Kreditoverførselsjournaler**. Vælg linjen for batch af kreditoverførsler, du vil eksportere igen, og brug derefter handlingen **Reeksportér betalinger til fil**.

> [!NOTE]  
>   Eksporterede EFT-filer vises ikke på siden **Kreditoverførselsjournaler** og kan ikke reeksporteres.

1. Vælg ikonet ![Elpære, der åbner funktionen Fortæl mig](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig"), angiv **Kreditoverførselsjournaler**, og vælg derefter det relaterede link.
2. Vælg den betalingseksport, du vil eksportere igen, og vælg derefter handlingen **Reeksportér betalinger til fil**.

## <a name="see-also"></a>Se også
[Foretage betaling](payables-make-payments.md)  
[Gæld](payables-manage-payables.md)  
[Opsætning af indkøb](purchasing-setup-purchasing.md)  
[Arbejde med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

