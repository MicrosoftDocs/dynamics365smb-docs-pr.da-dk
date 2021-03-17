---
title: Foretage betalinger med AMC Banking  (US) eller SEPA Credit Transfer (EU)
description: Du kan behandle betalinger til dine kreditorer ved at eksportere en fil sammen med betalingsoplysningerne fra kladdelinjerne.
author: bholtorf
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/01/2020
ms.author: bholtorf
ms.openlocfilehash: 210dbfd3450d4cc703f73fc2cd078b0155c599da
ms.sourcegitcommit: ff2b55b7e790447e0c1fcd5c2ec7f7610338ebaa
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 02/15/2021
ms.locfileid: "5391845"
---
# <a name="make-payments-with-the-amc-banking-365-fundamentals-extension-or-sepa-credit-transfer"></a>Foretage betalinger med AMC Banking 365 Fundamentals-udvidelsen eller SEPA-kreditoverførsel

På sien **Udbetalingskladde** kan du behandle betalinger til dine kreditorer ved at eksportere en fil sammen med betalingsoplysningerne fra kladdelinjerne. Derefter kan du uploade filen til din elektroniske bank, hvor de relaterede pengeoverførsler behandles. [!INCLUDE[prod_short](includes/prod_short.md)] understøtter SEPA-kreditoverførselsformatet, men i dit land/område anvendes der muligvis andre formater til elektroniske betalinger.

> [!NOTE]
> I den generelle version af [!INCLUDE[prod_short](includes/prod_short.md)] bliver en global udbyder af tjenester til konvertering af bankoplysninger til ethvert filformat, som kræves af din bank, konfigureret og tilsluttet. I nordamerikanske versioner kan den samme tjeneste bruges til at sende betalingsfiler som elektronisk pengeoverførsel (EFT), men med en lidt anderledes proces. Se trin 6 i [Sådan eksporterer du betalinger til en bankfil](finance-make-payments-with-bank-data-conversion-service-or-sepa-credit-transfer.md#to-export-payments-to-a-bank-file).  

 Hvis du vil aktivere SEPA-kreditoverførsler, skal du først angive en bankkonto, en kreditor og finanskladdenavnet, som betalingskladden er baseret på. Derefter forbereder du betalinger til kreditorer ved automatisk at udfylde siden **Udbetalingskladde** med forfaldne betalinger med angivne bogføringsdatoer.  

> [!NOTE]  
> Når du har kontrolleret, at betalingerne er behandlet af banken, kan du fortsætte med at bogføre udbetalingskladdens linjer.  

## <a name="setting-up-the-amc-banking-365-fundamentals-extension"></a>Konfigurere AMC Banking 365 Fundamentals-udvidelsen

Aktivér AMC Banking 365 Fundamentals-udvidelsen for at konvertere en fil med bankkontoudtog til et format, som du kan importere, eller for at få dine eksporterede betalingsfiler konverteret tilbage til det format, som din bank kræver. Du kan finde flere oplysninger i [Bruge AMC Banking 365 Fundamentals-udvidelsen](ui-extensions-amc-banking.md).

## <a name="setting-up-sepa-credit-transfer"></a>Konfigurere SEPA-kreditoverførsel

Fra siden **Udbetalingskladde** kan du eksportere betalinger til en fil til overførsel til din elektroniske bank til behandling af de relaterede pengeoverførsler. [!INCLUDE[prod_short](includes/prod_short.md)] understøtter SEPA-kreditoverførselsformatet, men i dit land/område anvendes der muligvis andre formater til elektroniske betalinger.  

For at aktivere eksport af bankfilformater, der ikke umiddelbart understøttes i [!INCLUDE[prod_short](includes/prod_short.md)], kan du konfigurere en dataudvekslingsdefinition ved hjælp af dataudvekslingsstrukturen. Du kan finde flere oplysninger i [Konfigurere dataudvekslingsdefinitioner](across-how-to-set-up-data-exchange-definitions.md).  

Før du kan behandle betalingen elektronisk ved eksport af betalingsfiler i formatet SEPA-kreditoverførsel, skal du udføre følgende trin:  

* Konfigurere bankkontoen til at håndtere formatet SEPA-kreditoverførsel  
* Konfigurere kreditorkortene for at behandle betalinger ved at eksportere filer i formatet SEPA-kreditoverførsler  
* Konfigurere den relaterede finanskladde til at aktivere betalingseksport fra siden **Udbetalingskladde**  
* Forbinde dataudvekslingsdefinitionen for en eller flere betalingstyper med den eller de relevante betalingsmetode(r)  

### <a name="to-set-up-a-bank-account-for-sepa-credit-transfer"></a>Sådan opsættes en konto til SEPA-kreditoverførsler

1. I feltet **Søg** skal du indtaste **Bankkonti** og derefter vælge det relaterede link.  
2. Åbn kortet for den bankkonto, som du vil eksportere betalingsfiler fra i formatet SEPA-kreditoverførsler.  
3. I oversigtspanelet **Overfør** skal du i feltet **Format til eksport af betaling** vælge **SEPACT**.  
4. I oversigtspanelet **Generelt** skal du i feltet **Kreditoverførselsmedd.numre** vælge en nummerserie, hvorfra numrene tildeles SEPA-kreditoverførselsposter.  
5. Sørg for, at feltet **IBAN** er udfyldt.  

    > [!NOTE]  
    > Feltet **Valutakode** skal indstilles til **EUR**, da SEPA-kreditoverførsler kun kan foretages i EURO-valuta.  

### <a name="to-set-up-a-vendor-card-for-sepa-credit-transfer"></a>Sådan opsættes et kreditorkort til SEPA-kreditoverførsler

1. I feltet **Søg** skal du angive **Leverandører** og derefter vælge det relaterede link.  
2. Åbn kortet for den kreditor, som du vil betale elektronisk ved at eksportere betalingsfiler i formatet SEPA-kreditoverførsler.  
3. I oversigtspanelet **Betaling** i feltet **Betalingsformkode** skal du vælge **BANK**.  
4. I feltet **Foretrukken bankkontokode** skal du vælge den bank, som pengene skal overføres til, når de behandles af din elektroniske bank.  

     Værdien i feltet **Foretrukken bankkontokode** kopieres til feltet **Modtagers bankkonto** på siden **Udbetalingskladde**.  

### <a name="to-set-the-payment-journal-up-to-export-payment-files"></a>Sådan opsættes betalingskladden til eksport af betalingsfiler

1. Indtast **Udbetalingskladder** i feltet **Søg**, og vælg derefter det relaterede link.  
2. Åbn den betalingskladde, som du kan bruge til at behandle betalinger, ved at eksportere filer i formatet SEPA-kreditoverførsler.  
3. Vælg rulle\-knappen i feltet **Kladdenavn**.  
4. På siden **Finanskladdenavne** skal du vælge handlingen **Rediger liste**.  
5. Markér afkrydsningsfeltet **Tillad eksport af betaling** på linjen for den betalingskladde, som du vil bruge til eksport af betalinger.  

### <a name="to-connect-the-data-exchange-definition-for-one-or-more-payment-types-with-the-relevant-payment-method-or-methods"></a>Sådan forbindes dataudvekslingsdefinitionen for en eller flere betalingstyper med den eller de relevante betalingsmetode(r)

1. I feltet **Søg** skal du angive **Betalingsformer** og derefter vælge det relaterede link.  
2. På siden **Betalingsformer** skal du vælge den betalingsmåde, der bruges til eksport af betalinger fra, og derefter vælge feltet **Definition af betalingseksportlinje**.  
3. På siden **Definitioner af betalingseksportlinjer** skal du vælge den kode, du angav i feltet **Kode** i oversigtspanelet **Linjedefinitioner** i trin 4 i afsnittet "Sådan beskrives formateringen af linjer og kolonner i filen" i [Konfigurere dataudvekslingsdefinitioner](across-how-to-set-up-data-exchange-definitions.md).  

## <a name="preparing-the-payment-journal"></a>Forberede udbetalingskladden

Udfyld betalingskladdelinjerne for forfaldne betalinger til kreditorer med mulighed for at indsætte bogføringsdatoer, der er baseret på forfaldsdatoen for de relaterede købsdokumenter. Du kan finde flere oplysninger under [Administrere skyldige beløb](payables-manage-payables.md).

## <a name="exporting-payments-to-a-bank-file"></a>Eksportere betalinger til en bankfil

Når du er klar til at bogføre betalinger til dine kreditorer eller refusioner til dine medarbejdere, kan du eksportere en fil med betalingsoplysningerne på kladdelinjerne på siden **Udbetalingskladde**. Derefter kan du overføre filen til din bank for at behandle de relaterede pengeoverførsler.

I den generiske version af AMC Banking 365 Fundamentals er [!INCLUDE[prod_short](includes/prod_short.md)]-udvidelsen tilgængelig. I nordamerikanske versioner kan den samme udvidelse bruges til at sende betalingsfiler som elektronisk pengeoverførsel (EFT), men med en lidt anderledes proces. Se trin 6 i [Sådan eksporterer du betalinger til en bankfil](finance-make-payments-with-bank-data-conversion-service-or-sepa-credit-transfer.md#to-export-payments-to-a-bank-file).

> [!NOTE]  
> Inden du kan eksportere betalingsfiler fra betalingskladden, skal du angive det elektroniske format for den bankkonto, der anvendes, og du skal aktivere AMC Banking 365 Fundamentals-udvidelsen. Du kan finde flere oplysninger i [Konfigurere bankkonti](bank-how-setup-bank-accounts.md) og [Bruge AMC Banking 365 Fundamentals-udvidelsen](ui-extensions-amc-banking.md). Desuden skal du markere afkrydsningsfeltet **Tillad eksport af betaling** på siden **Finanskladdenavne**. Du kan finde flere oplysninger under [Arbejde med finanskladder](ui-work-general-journals.md).  

Brug siden **Kreditoverførselsjournaler** til at få vist de betalingsfiler, som er eksporteret fra betalingskladden. På denne side kan du også udlæse betalingsfiler igen i tilfælde af tekniske fejl eller filændringer. Bemærk dog, at de eksporterede EFT-filer ikke vises på denne side og ikke kan reeksporteres.  

### <a name="to-export-payments-to-a-bank-file"></a>Sådan eksporterer du betalinger til en bankfil

I følgende fremgangsmåde vises, hvordan du betaler en kreditor med check. Fremgangsmåden er den samme, hvis du vil refundere en debitor med check.

1. Vælg ikonet ![Elpære, der åbner funktionen Fortæl mig](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig"), angiv **Udbetalingskladder**, og vælg derefter det relaterede link.
2. Udfyld betalingskladdelinjerne. Du kan finde flere oplysninger i [Registrere betalinger og refusioner](payables-how-post-payments-refunds.md).

    > [!NOTE]
    > Hvis du bruger elektroniske pengeoverførsler, skal du vælge enten **Elektronisk betaling** eller **Elektronisk betaling-IAT** i feltet **Bankbetalingstype**. Andre fileksporttjenester og deres formater kræver andre konfigurationsværdier på siderne **Bankkontokort** og **Kreditors bankkontokort**. Du får information om forkerte eller manglende konfigurationsværdier, når du prøver at eksportere filen.
    >
    > ETF-funktionen kan kun bruges til bankkonti i den lokale valuta. Den kan ikke bruges med en fremmed valuta, der er angivet med en værdi i feltet **Valutakode**. (Tom værdi i felt betyder lokal valuta.)

3. Når du har fuldført alle betalingskladdelinjer, skal du vælge handlingen **Eksportér**.
4. På siden **Eksportér elektroniske betalinger** skal du udfylde felterne efter behov.

    Eventuelle fejlmeddelelser vises i faktaboksen **Fejl i betalingsfil**, hvor du også kan vælge en fejlmeddelelse for at se detaljerede oplysninger. Du skal løse alle fejl, før betalingsfilen kan eksporteres.

    > [!TIP]  
    > Når du bruger AMC Banking 365 Fundamentals-udvidelsen, angiver en typisk fejlmeddelelse, at bankkontonummeret ikke har den længde, der kræves af din bank. For at undgå eller løse fejlen skal du fjerne værdien i feltet **IBAN** på siden **Bankkontokort** og derefter bruge feltet **Bankkontonr.** til at angive et bankkontonummer i det format, som kræves af din bank.

5. På siden **Gem som** skal du angive den placering, filen eksporteres til, og derefter vælge **Gem**.

    > [!NOTE]  
    > Hvis du bruger elektroniske pengeoverførsler, skal du gemme den kreditorindbetalingsformular, der oprettes, som et Word-dokument eller vælge at få den sendt som e-mail direkte til kreditoren. Betalingerne til føjes nu på siden **Generer EFT-fil**, hvor du kan oprette flere betalingsordrer sammen for at spare transmissionsomkostninger. Du kan finde flere oplysninger i følgende trin.
6. På siden **Udbetalingskladde** skal du vælge handlingen **Generer EFT-fil**.

    På siden **Generer EFT-fil** vises alle betalinger, der er konfigureret til elektroniske pengeoverførsler, som du har eksporteret fra betalingskladden for en bestemt bankkonto, men som endnu ikke er oprettet, i oversigtspanelet **Linjer**.
7. Vælg handlingen **Generer EFT-fil** for at eksportere én fil for alle EFT-betalinger.
8. På siden **Gem som** skal du angive den placering, filen eksporteres til, og derefter vælge **Gem**.

Betalingsfilen til banken er eksporteret til den placering, du angiver, og du kan fortsætte med at overføre den til din elektroniske bankkonto og foretage de faktiske betalinger. Derefter kan du bogføre de eksporterede betalingskladdelinjer.

### <a name="to-plan-when-to-post-exported-payments"></a>Sådan planlægger du, hvornår eksporterede betalinger skal bogføres

Hvis du ikke vil bogføre en betalingskladdelinje for en eksporteret betaling, for eksempel fordi du venter på bekræftelse af, at transaktionen er blevet behandlet af banken, kan du bare slette kladdelinjen. Når du senere opretter en betalingskladdelinje for at betale det resterende beløb på fakturaen, kan du i feltet **Samlet eksporteret beløb** se, hvor meget af betalingsbeløbet der allerede er blevet eksporteret. Du kan også finde detaljerede oplysninger om den eksporterede total ved at vælge knappen **Poster i kreditoverførselsjournal** for at se detaljer om eksporterede betalingsfiler.

Hvis du følger en proces, hvor du ikke bogfører betalinger, før du har fået bekræftet, at de er blevet behandlet i banken, kan du gøre dette på to måder.

* I en betalingskladde med foreslåede betalingslinjer kan du sortere på enten kolonnen **Eksporteret til betalingsfil** eller **Samlet eksporteret beløb** og derefter slette betalingsforslag for åbne fakturaer for betalinger, der allerede er foretaget, og du ikke vil foretage betalinger af.
* På siden **Lav kreditorbetalingsforslag**, hvor du angiver, hvilke betalinger der indsættes i betalingskladden, kan du også markere afkrydsningsfeltet **Spring over eksporterede betalinger**, hvis du ikke vil indsætte kladdelinjerne til betalinger, der allerede er eksporteret.

Du kan se oplysninger om eksporterede betalinger ved at vælge handlingen **Historik for eksporterede betalinger**.

### <a name="to-re-export-payments-to-a-bank-file"></a>Sådan reeksporter du betalinger til en bankfil

Du kan eksportere betalingsfiler igen fra siden **Kreditoverførselsjournaler**. Før du sletter eller bogfører betalingskladdelinjer, kan du også geneksportere betalingsfilen fra siden **Udbetalingskladde** ved bare at eksportere den igen. Hvis du har slettet eller bogført betalingskladdelinjerne efter at have eksporteret dem, kan du geneksportere den samme betalingsfil fra siden **Kreditoverførselsjournaler**. Vælg linjen for batch af kreditoverførsler, du vil eksportere igen, og brug derefter handlingen **Reeksportér betalinger til fil**.

> [!NOTE]  
> Eksporterede EFT-filer vises ikke på siden **Kreditoverførselsjournaler** og kan ikke reeksporteres.

1. Vælg ikonet ![Elpære, der åbner funktionen Fortæl mig](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig"), angiv **Kreditoverførselsjournaler**, og vælg derefter det relaterede link.
2. Vælg den betalingseksport, du vil eksportere igen, og vælg derefter handlingen **Reeksportér betalinger til fil**.

## <a name="posting-the-payments"></a>Bogføre betalingerne

Når elektronisk betaling er behandlet af banken, kan du bogføre betalingerne. Du kan finde flere oplysninger under [Foretage betalinger](payables-make-payments.md).

## <a name="see-also"></a>Se også

[Brug af AMC Banking 365 Fundamentals-udvidelsen](ui-extensions-amc-banking.md)  
[Administrere skyldige beløb](payables-manage-payables.md)  
[Arbejde med finanskladder](ui-work-general-journals.md)  
[Indhente betalinger med SEPA Direct Debit](finance-collect-payments-with-sepa-direct-debit.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]