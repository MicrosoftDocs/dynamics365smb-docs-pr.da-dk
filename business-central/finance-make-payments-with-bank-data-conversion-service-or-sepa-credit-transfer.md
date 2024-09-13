---
title: Foretag betalinger med AMC banking (USA) eller SEPA-kreditoverførsel (EU)
description: Du kan behandle betalinger til dine kreditorer ved at eksportere en fil (EFT) sammen med betalingsoplysningerne fra kladdelinjerne.
author: brentholtorf
ms.topic: conceptual
ms.devlang: al
ms.search.keywords: null
ms.search.form: '256, 1205, 1206, 1209, 10810, 10811'
ms.date: 08/26/2024
ms.author: bholtorf
ms.service: dynamics-365-business-central
ms.reviewer: bholtorf
---
# Foretag betalinger med AMC banking 365 fundamentals extension eller SEPA-kreditoverførsel

 **På siden Udbetalingskladder** kan du behandle betalinger til kreditorer ved at udlæse en fil sammen med betalingsoplysningerne fra kladdelinjerne. Derefter kan du uploade filen til din elektroniske bank, hvor de relaterede pengeoverførsler behandles. [!INCLUDE[prod_short](includes/prod_short.md)] understøtter SEPA-kreditoverførselsformatet, men i dit land/område er andre formater til elektroniske betalinger muligvis tilgængelige.

> [!NOTE]
> I den generelle version af [!INCLUDE[prod_short](includes/prod_short.md)] bliver en global udbyder af tjenester til konvertering af bankoplysninger til ethvert filformat, som kræves af din bank, konfigureret og tilsluttet. I den nordamerikanske version kan den samme service bruges til at sende betalingsfiler som elektronisk pengeoverførsel, f. eks. det almindeligt brugte ACH-netværk (Automated Clearing House), men med en lidt anden proces. Se trin 6 i [Sådan eksporterer du betalinger til en bankfil](finance-make-payments-with-bank-data-conversion-service-or-sepa-credit-transfer.md#to-export-payments-to-a-bank-file).  

 Hvis du vil aktivere SEPA-kreditoverførsler, skal du først angive en bankkonto, en kreditor og finanskladdenavnet, som betalingskladden er baseret på. Derefter forbereder du betalinger til kreditorer **ved automatisk at udfylde** siden Udbetalingskladder med forfaldne betalinger med angivne bogføringsdatoer.  

Når du har bekræftet, at banken har behandlet betalingerne, kan du bogføre linjerne i udbetalingskladden.  

## Opsætning af AMC Banking 365 Fundamentals udvidelsen

Aktivér AMC Banking 365 Fundamentals udvidelsen for at:

* Konverter bankkontoudtogsfiler til et format, du kan importere.
* Konverter dine eksporterede betalingsfiler til det format, din bank kræver.

Du kan finde flere oplysninger i [Brug AMC Banking 365 Fundamentals-udvidelsen](ui-extensions-amc-banking.md).

## Konfiguration af SEPA-kreditoverførsel

Fra siden **Udbetalingskladder** kan du eksportere betalinger til en fil, så de kan overføres til din netbank til behandling af de relaterede pengeoverførsler. [!INCLUDE[prod_short](includes/prod_short.md)] understøtter SEPA-kreditoverførselsformatet, men i dit land/område er andre formater til elektroniske betalinger muligvis tilgængelige.  

Hvis du vil kunne eksportere et bankfilformat, der ikke understøttes som standard [!INCLUDE[prod_short](includes/prod_short.md)], skal du konfigurere en dataudvekslingsdefinition. Du kan finde flere oplysninger i [Konfigurere dataudvekslingsdefinitioner](across-how-to-set-up-data-exchange-definitions.md).  

Før du kan behandle betalingen elektronisk ved eksport af betalingsfiler i formatet SEPA-kreditoverførsel, skal du udføre følgende trin:  

* Konfigurere bankkontoen til at håndtere formatet SEPA-kreditoverførsel  
* Konfigurere kreditorkortene for at behandle betalinger ved at eksportere filer i formatet SEPA-kreditoverførsler  
* Konfigurere det relaterede finanskladdenavn for at aktivere eksport af betaling fra siden **Udbetalingskladder**   
* Forbinde dataudvekslingsdefinitionen for en eller flere betalingstyper med den eller de relevante betalingsmetode(r)  

> [!NOTE]
> Business Central understøtter både CT-smerter i SEPA-format.001.001.03 og CT-smerter.001.001.09. Du kan vælge et hvilket som helst format på **siden Bankkonto kort** .  

> [!TIP]
> Denne artikel gælder for den generelle version af [!INCLUDE [prod_short](includes/prod_short.md)]. I det aktuelle land/område kan der være tilføjet yderligere obligatoriske felter til de forskellige sider. [!INCLUDE [tooltip-inline-tip_md](includes/tooltip-inline-tip_md.md)]

### Sådan opsættes en konto til SEPA-kreditoverførsler

1. Vælg det ![lyspæreikon, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **Bankkonti**, og vælg derefter det relaterede link.  
2. Vælg den bankkonto, du vil eksportere betalingsfiler fra, i SEPA-kreditoverførselsformatet.
3. I oversigtspanelet **Generelt** skal du i feltet **Kreditoverførselsmedd.numre** vælge en nummerserie, hvorfra numrene tildeles SEPA-kreditoverførselsposter.
4.  **I oversigtspanelet Kommunikation** skal du angive bankens adresse og kontaktoplysninger. 

   > [!NOTE]
   > Du skal udfylde feltet **Lande-/områdekode** . Hvis feltet er tomt, kan du ikke eksportere betalinger for kontoen. Desuden skal landet/området have en gyldig ISO-kode.

5.  **Angiv valutaen for bankkontoen i feltet** Valutakode **i oversigtspanelet Bogføring** .  

   > [!NOTE]  
   > Feltet **Valutakode** skal indstilles til **EUR**, da SEPA-kreditoverførsler kun kan foretages i EURO-valuta.  

6. Vælg det **SEPA-format, du vil bruge, i feltet** Format for betalingseksport **i oversigtspanelet Overførsel** .  
7.  **Angiv kontoens internationale bankkontonummer i feltet IBAN** .  

### Sådan opsættes et kreditorkort til SEPA-kreditoverførsler

1. Vælg ![Lightbulb, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **Leverandører**, og vælg derefter det relaterede link.  
2. Åbn kort for den kreditor, du betaler, elektronisk ved hjælp af eksportbetalingsfiler i formatet SEPA-kreditoverførsel.  
3. Gå til oversigtspanelet **Betalinger** og feltet **Betalingsformskode**, og vælg **BANK.**  
4. I feltet **Foretrukken bankkonto** skal du vælge den bank, som pengene overføres til, når de behandles af din elektroniske bank.  

    Hvis du ikke har en bank, kontogruppe for denne kreditor, kan du gøre det nu. Du kan finde flere oplysninger i [Konfigurere kreditors bankkonti til eksport af bankfiler](bank-how-setup-bank-accounts.md#to-set-up-vendor-bank-accounts-for-export-of-bank-files). Værdien i feltet **Foretrukken bankkontokode** kopieres til feltet **Modtagers bankkonto** på siden **Udbetalingskladde**.  

### Sådan opsættes betalingskladden til eksport af betalingsfiler

1. Vælg det ![lyspæreikon, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **Udbetalingskladder**, og vælg derefter det relaterede link.  
2. Vælg rulle\-knappen i feltet **Kladdenavn**.  
3. På siden **Finanskladdenavne** skal du vælge handlingen **Rediger liste**.  
4. Markér afkrydsningsfeltet Tillad eksport af betaling **på linjen for den betalingskladde, du bruger til at eksportere betalinger.**   

### Sådan forbindes dataudvekslingsdefinitionen for en eller flere betalingstyper med den eller de relevante betalingsmetode(r)

1. Vælg ikonet ![Lightbulb, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **Betalingsformer**, og vælg derefter det relaterede link.  
2. På siden **Betalingsformer** skal du vælge den betalingsmåde, der bruges til eksport af betalinger fra, og derefter vælge feltet **Definition af betalingseksportlinje**.  
3. På siden **Definitioner af betalingseksportlinjer** skal du vælge den kode, du angav i feltet **Kode** i oversigtspanelet **Linjedefinitioner** i trin 4 i afsnittet "Sådan beskrives formateringen af linjer og kolonner i filen" i [Konfigurere dataudvekslingsdefinitioner](across-how-to-set-up-data-exchange-definitions.md).  

## Klargøring af udbetalingskladden

Udfyld betalingskladdelinjerne for forfaldne betalinger til kreditorer med mulighed for at indsætte bogføringsdatoer, der er baseret på forfaldsdatoen for de relaterede købsdokumenter. Du kan finde flere oplysninger i [Administrere skyldige beløb](payables-manage-payables.md).

## Udlæse betalinger til en bankfil

Når du er klar til at foretage betalinger til dine kreditorer eller refusioner til dine medarbejdere, kan du eksportere en fil med betalingsoplysningerne på linjerne på **siden Udbetalingskladder** . Derefter kan du overføre filen til din bank for at behandle de relaterede pengeoverførsler.

I den generiske version af AMC Banking 365 Fundamentals er [!INCLUDE[prod_short](includes/prod_short.md)]-udvidelsen tilgængelig. I nordamerikanske versioner kan den samme udvidelse bruges til at sende betalingsfiler som elektronisk pengeoverførsel (EFT), men med en lidt anderledes proces. Se trin 6 i [Sådan eksporterer du betalinger til en bankfil](finance-make-payments-with-bank-data-conversion-service-or-sepa-credit-transfer.md#to-export-payments-to-a-bank-file).

> [!NOTE]  
> Inden du kan eksportere betalingsfiler fra betalingskladden, skal du angive det elektroniske format for den bankkonto, der anvendes, og du skal aktivere AMC Banking 365 Fundamentals-udvidelsen. Du kan finde flere oplysninger i [Konfigurere bankkonti](bank-how-setup-bank-accounts.md) og [Bruge AMC Banking 365 Fundamentals-udvidelsen](ui-extensions-amc-banking.md). Desuden skal du markere afkrydsningsfeltet **Tillad eksport af betaling** på siden **Finanskladdenavne**. Du kan finde flere oplysninger i [Arbejde med finanskladder](ui-work-general-journals.md).  

Brug siden **Kreditoverførselsjournaler** til at få vist de betalingsfiler, der er eksporteret fra betalingskladden. Fra denne side kan du også geneksportere betalingsfiler, hvis der var tekniske fejl eller filændringer. Bemærk dog, at eksporterede EFT-filer ikke vises på denne side og ikke kan eksporteres igen.  

### Sådan eksporterer du betalinger til en bankfil

Følgende trin beskriver, hvordan du betaler en kreditor med check. Fremgangsmåden er den samme, hvis du vil refundere en debitor med check.

1. Vælg ikonet ![Lightbulb, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **Udbetalingskladder**, og vælg derefter det relaterede link.
2. Udfyld betalingskladdelinjerne. Du kan finde flere oplysninger i [Registrere betalinger og refusioner](payables-how-post-payments-refunds.md).

    > [!NOTE]
    > Hvis du bruger elektroniske pengeoverførsler, skal du vælge enten **Elektronisk betaling** eller **Elektronisk betaling-IAT** i feltet **Bankbetalingstype**. Andre fileksporttjenester og deres formater kræver andre konfigurationsværdier på siderne **Bankkontokort** og **Kreditors bankkontokort**. Du får information om forkerte eller manglende konfigurationsværdier, når du prøver at eksportere filen.
    >
    > ETF-funktionen kan kun bruges til bankkonti i den lokale valuta. Den kan ikke bruges med en fremmed valuta, der er angivet med en værdi i feltet **Valutakode**. (Tom værdi i felt betyder lokal valuta.)

3. Når du har udfyldt alle betalingskladdelinjer, skal du vælge handlingen **Eksporter** .
4. På siden **Eksportér elektroniske betalinger** skal du udfylde felterne efter behov.

    Der vises fejlmeddelelser **i faktaboksen Fejl** i betalingsfil, hvor du også kan vælge en fejlmeddelelse for at få adgang til flere oplysninger. Du skal løse alle fejl, før du kan eksportere betalingsfilen.

    > [!TIP]  
    > Når du bruger AMC Banking 365 Fundamentals-udvidelsen, angiver en typisk fejlmeddelelse, at bankkontonummeret ikke har den længde, der kræves af din bank. For at undgå eller løse fejlen skal du fjerne værdien i feltet **IBAN** på siden **Bankkontokort** og derefter bruge feltet **Bankkontonr.** til at angive et bankkontonummer i det format, som kræves af din bank.

5. På siden **Gem som** skal du angive den placering, filen eksporteres til, og derefter vælge **Gem**.

    > [!NOTE]  
    > Hvis du bruger elektroniske pengeoverførsler, skal du gemme den kreditorindbetalingsformular, der oprettes, som et Word-dokument eller vælge at få den sendt som e-mail direkte til kreditoren. Betalingerne til føjes nu på siden **Generer EFT-fil**, hvor du kan oprette flere betalingsordrer sammen for at spare transmissionsomkostninger. Du kan finde flere oplysninger i følgende trin.
6.  **På siden Udbetalingskladder** skal du vælge handlingen **Opret EFT-fil** .

     **På siden Opret EFT-fil** viser oversigtspanelet Linjer **alle EFT-betalinger, som du har eksporteret fra udbetalingskladden for en bankkonto,** men som endnu ikke er genereret.
7. Vælg handlingen **Generer EFT-fil** for at eksportere én fil for alle EFT-betalinger.
8. På siden **Gem som** skal du angive den placering, filen eksporteres til, og derefter vælge **Gem**.

Bankbetalingsfilen udlæses til den placering, du har angivet. Du kan uploade det til din elektroniske bankkonto og foretage de faktiske betalinger. Derefter kan du bogføre de eksporterede betalingskladdelinjer.

### Sådan planlægger du, hvornår eksporterede betalinger skal bogføres

Hvis du ikke vil bogføre en betalingskladdelinje for en eksporteret betaling, kan du blot slette kladdelinjen. For eksempel fordi du venter på bekræftelse på, at banken har behandlet transaktionen. Når du senere opretter en betalingskladdelinje til betaling af restbeløbet, viser feltet Udlæst beløb **i alt,** hvor meget af betalingsbeløbet der allerede er eksporteret. Du kan også finde detaljerede oplysninger om den eksporterede total ved at vælge knappen **Poster i kreditoverførselsjournal** for at se detaljer om eksporterede betalingsfiler.

Hvis du ikke vil bogføre betalinger, før banken har bekræftet, at de er behandlet, kan du:

* I en betalingskladde **med foreslåede betalingslinjer kan du sortere enten kolonnen Udlæst til betalingsfil** eller **det eksporterede beløb** i alt og derefter slette betalingsforslag for åbne fakturaer, som der allerede er foretaget betalinger for.
*  **På siden Lav kreditorbetalingsforslag**, hvor du angiver, hvilke betalinger der skal indsættes i betalingskladden, kan du markere afkrydsningsfeltet **Spring eksporterede betalinger** over, hvis du ikke vil indsætte kladdelinjer for betalinger, der allerede er eksporteret.

Du kan se oplysninger om eksporterede betalinger ved at vælge handlingen **Historik for eksporterede betalinger**.

### Sådan reeksporter du betalinger til en bankfil

Du kan eksportere betalingsfiler igen fra siden **Kreditoverførselsjournaler**. Inden du sletter eller bogfører betalingskladdelinjer, kan du også geneksportere betalingsfilen fra **siden Udbetalingskladder** ved at eksportere den igen. Hvis du sletter eller bogfører betalingskladdelinjerne efter eksporten, kan du geneksportere den samme betalingsfil fra siden **Kreditoverførselsjournaler** . Vælg linjen for batch af kreditoverførsler, du vil eksportere igen, og brug derefter handlingen **Reeksportér betalinger til fil**.

> [!NOTE]  
> Eksporterede EFT-filer vises ikke på siden **Kreditoverførselsjournaler** og kan ikke reeksporteres.

1. Vælg ikonet ![Lightbulb, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **Kreditoverførselsjournaler**, og vælg derefter det relaterede link.
2. Vælg den betalingseksport, du vil eksportere igen, og vælg derefter handlingen **Reeksportér betalinger til fil**.

## Bogføring af betalingerne

Når din bank har behandlet den elektroniske betaling, skal du bogføre betalingerne. Du kan finde flere oplysninger i [Foretage betalinger](payables-make-payments.md).

## Se også

[Bruge AMC Banking 365 Fundamentals-udvidelsen](ui-extensions-amc-banking.md)  
[Administrere skyldige beløb](payables-manage-payables.md)  
[Arbejde med finanskladder](ui-work-general-journals.md)  
[Indhente betalinger med SEPA Direct Debit](finance-collect-payments-with-sepa-direct-debit.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
