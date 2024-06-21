---
title: Konfigurere konvertering af bankdata
description: 'Du kan oprette bankkonti for at holde styr på transaktioner og importere eller eksportere bankfeeds, f.eks. Yodlee.'
author: brentholtorf
ms.topic: conceptual
ms.devlang: al
ms.search.keywords: 'Yodlee, feed, stream, data exchange, AMC, bank file import, bank file export, re-export, bank transfer, AMC, AMC Banking 365 Fundamentals extension, funds transfer'
ms.search.form: '304, 20106, 20105, 20100, 20101, 20107, 20109'
ms.date: 04/01/2021
ms.author: bholtorf
ms.service: dynamics-365-business-central
ms.reviewer: bholtorf
---
# <a name="set-up-the-amc-banking-365-fundamentals-extension"></a>Konfigurere AMC Banking 365 Fundamentals-udvidelsen
En global udbyder af tjenester til konvertering af betalingsoplysninger til ethvert dataformat, som din bank kræver, er forbundet og klar til at blive aktiveret i [!INCLUDE[prod_short](includes/prod_short.md)]. Dette omtales i [!INCLUDE[prod_short](includes/prod_short.md)] som AMC Banking 365 Fundamentals-udvidelsen.

Du kan eksportere betalingslinjer fra siden **Udbetalingskladde** til en fil eller en datastrøm, som du derefter overfører til din bank til automatisk behandling, så du ikke behøver at foretage elektroniske betalinger individuelt. Du kan finde flere oplysninger i [Eksportere betalinger til en bankfil](finance-make-payments-with-bank-data-conversion-service-or-sepa-credit-transfer.md#exporting-payments-to-a-bank-file).

Du kan indlæse bankkontoudtogsfiler på siden **Betalingsudligningskladde** ved hjælp af AMC Banking 365 Fundamentals-udvidelsen for at konvertere en fil, du modtager fra banken, til en datastrøm, som [!INCLUDE[prod_short](includes/prod_short.md)] kan importere. Du kan finde flere oplysninger i [Udligne betalinger automatisk og afstemme bankkonti](receivables-apply-payments-auto-reconcile-bank-accounts.md).

Du kan også bruge Envestnet Yodlee Bank Feeds-tjenesten i stedet for at indlæse bankkontoudtog med AMC Banking 365 Fundamentals-udvidelsen. Du kan finde flere oplysninger i [Konfigurere tjenesten Envestnet Yodlee Bank Feeds](bank-how-setup-bank-statement-service.md).

Når du vil importere eller eksportere bankfiler, skal du konfigurere din egen bankkonto og dine kreditorers bankkonti. Du kan finde flere oplysninger i [Oprette bankkonti](bank-how-setup-bank-accounts.md).

> [!NOTE]  
> AMC Banking 365 Fundamentals-udvidelsen kan angive en grænse for antallet af linjer, der kan eksporteres i en fil. Du modtager en fejlmeddelelse, hvis grænsen er overskredet. Det anbefales, at bankkontofiler ikke overstiger 1000 linjer, da behandlingstiden i AMC Banking 365 Fundamentals-udvidelsen ellers bliver væsentligt forøget.

## <a name="to-sign-your-company-up-for-the-amc-banking-365-fundamentals-extension"></a>Sådan tilmelder din virksomhed sig AMC Banking 365 Fundamentals-udvidelsen
1. Vælg ![Lightbulb, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, angiv **Opsætning af tjeneste til konvertering af bankdata**, og vælg derefter det relaterede link.  
2. Siden **Opsætning af tjeneste til konvertering af bankdata** åbnes med tre felter udfyldt med relevante URL-adresser på udbyderen af AMC Banking 365 Fundamentals-udvidelsen.

    > [!NOTE]  
    >   I CRONUS International Ltd.-demonstrationsdatabasen er felterne Brugernavn og Adgangskode udfyldt på forhånd med demonstration af logonoplysninger, som du erstatter med din virksomheds faktiske oplysninger, når du tilmelder dig AMC Banking 365 Fundamentals-udvidelsen.
3. I feltet **URL-adresse til tilmelding** skal du vælge browserknappen for at åbne serviceudbyderens tilmeldingsside.  
4. Angiv brugernavnet og adgangskoden til din virksomheds abonnement på tjenesten på tilmeldingssiden af bankens dataserviceudbyder, og fuldfør derefter tilmeldingsprocessen som angivet af serviceudbyderen.

    Din virksomhed er nu tilmeldt AMC Banking 365 Fundamentals-udvidelsen. Fortsæt med at angive det brugernavn og adgangskode, du har angivet for tjenesten i de relaterede konfigurationsfelter i [!INCLUDE[prod_short](includes/prod_short.md)].

5. På siden **Opsætning af tjeneste til konvertering af bankdata** skal du i feltet **Brugernavn** angive den samme værdi, som du har angivet som logonnavnet på serviceudbyderens side i trin 4.
6. I feltet **Adgangskode** skal du angive den samme værdi, som du har angivet i feltet **Adgangskode** på serviceudbyderens side i trin 4.

> [!NOTE]  
> Dine logondata krypteres automatisk.

## <a name="to-view-or-update-the-list-of-currently-supported-bank-data-formats"></a>Sådan ser eller opdaterer du listen over aktuelt understøttede bankdataformater
1. Vælg ![Lightbulb, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, angiv **Opsætning af tjeneste til konvertering af bankdata**, og vælg derefter det relaterede link.
2. På siden **Opsætning af tjeneste til konvertering af bankdata** skal du vælge handlingen **Banknavn - datakonverteringsoversigt** for at åbne listen over banknavne, der repræsenterer bankdataformater, der understøttes af konverteringstjenesten.
3. På siden **Banknavn - datakonverteringsoversigt** skal du vælge handlingen **Opdater liste over banknavne**.

Listen over bankdataformater, der understøttes af AMC Banking 365 Fundamentals-udvidelsen, er nu opdateret. Dette er listen over banknavne, der er filtreret efter det land/område, som du kan vælge i feltet **Banknavn - datakonvertering** på siden **Bankkontokort**.

> [!NOTE]  
>   Opdatering af understøttede bankdataformater opstår også, når du vælger eller angiver en værdi i feltet **Banknavn - datakonvertering** på bankkontoen.

Du har nu tilmeldt dig AMC Banking 365 Fundamentals-udvidelsen. Fortsæt med at afspejle tilmeldingsoplysningerne for hver bankkonto, der bruger tjenesten.

## <a name="see-also"></a>Se også
[Konfigurere banktransaktioner](bank-setup-banking.md)  
[Bankkontoafstemning](bank-manage-bank-accounts.md)  
[Arbejd med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]
