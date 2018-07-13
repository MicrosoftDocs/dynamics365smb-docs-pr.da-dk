---
title: Konfigurere konvertering af bankdata | Microsoft Docs
description: "Du kan oprette bankkonti for at holde styr på transaktioner og importere eller eksportere bankfeeds, f.eks. Yodlee."
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: Yodlee, feed, stream, data exchange, AMC, bank file import, bank file export, re-export, bank transfer, AMC, bank data conversion service, funds transfer
ms.date: 06/08/2018
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: e73c2dd0533aade4aa6225c9d2f385baaea3cfd1
ms.openlocfilehash: 5bf6e0c961e35b2fdb23eb1ba470da0f5c098d81
ms.contentlocale: da-dk
ms.lasthandoff: 06/11/2018

---
# <a name="set-up-the-bank-data-conversion-service"></a>Konfigurere tjenesten til konvertering af bankdata
En global udbyder af tjenester til konvertering af betalingsoplysninger til ethvert dataformat, som din bank kræver, er forbundet og klar til at blive aktiveret i [!INCLUDE[d365fin](includes/d365fin_md.md)]. Dette kaldes for tjenesten til konvertering af bankdata i [!INCLUDE[d365fin](includes/d365fin_md.md)].

Du kan eksportere betalingslinjer fra vinduet **Udbetalingskladde** til en fil eller en datastrøm, som du derefter overfører til din bank til automatisk behandling, så du ikke behøver at foretage elektroniske betalinger individuelt. Du kan finde flere oplysninger i [Eksportere betalinger til en bankfil](payables-how-export-payments-bank-file.md).

Du kan indlæse bankkontoudtogsfiler i vinduet **Betalingsudligningskladde** ved hjælp af tjenesten til konvertering af bankdata for at konvertere en fil, du modtager fra banken, til en datastrøm, som [!INCLUDE[d365fin](includes/d365fin_md.md)] kan importere. Du kan finde flere oplysninger under [Udligne betalinger automatisk og afstemme bankkonti](receivables-apply-payments-auto-reconcile-bank-accounts.md).

Du kan også bruge tjenesten Envestnet Yodlee Bank Feeds i stedet for at indlæse bankkontoudtog med tjenesten til konvertering af bankdata. Du kan finde flere oplysninger under [Konfigurere tjenesten Envestnet Yodlee Bank Feeds](bank-how-setup-bank-statement-service.md).

Når du vil importere eller eksportere bankfiler, skal du konfigurere din egen bankkonto og dine kreditorers bankkonti. Du kan finde flere oplysninger i [Oprette bankkonti](bank-how-setup-bank-accounts.md).

> [!NOTE]  
>   Tjenesten til konvertering af bankdata kan angive en grænse for antallet af linjer, der kan eksporteres i en fil. Du modtager en fejlmeddelelse, hvis grænsen er overskredet. Det anbefales, at bankkontofiler ikke overstiger 1000 linjer, da behandlingstiden i tjenesten til konvertering af bankdata ellers bliver væsentligt forøget.

## <a name="to-sign-your-company-up-for-the-bank-data-conversion-service"></a>Sådan tilmeldes din virksomhed tjenesten til konvertering af bankdata.
1. Vælg ikonet ![Søg efter side eller rapport](media/ui-search/search_small.png "Ikonet Søg efter side eller rapport"), angiv **Opsætning af tjeneste til konvertering af bankdata**, og vælg derefter det relaterede link.  
2. Vinduet **Opsætning af tjeneste til konvertering af bankdata** åbnes med tre felter udfyldt med relevante URL-adresser på udbyderen af tjenesten for omregning af bankdata.

    > [!NOTE]  
    >   I CRONUS International Ltd.-demonstrationsdatabasen er felterne Brugernavn og Adgangskode udfyldt på forhånd med demonstration af logonoplysninger, som du erstatter med din virksomheds faktiske oplysninger, når du tilmelder dig konverteringstjenesten for bankdata.
3. I feltet **URL-adresse til tilmelding** skal du vælge browserknappen for at åbne serviceudbyderens tilmeldingsside.  
4. Angiv brugernavnet og adgangskoden til din virksomheds abonnement på tjenesten på tilmeldingssiden af bankens dataserviceudbyder, og fuldfør derefter tilmeldingsprocessen som angivet af serviceudbyderen.

  Din virksomhed er nu tilmeldt tjenesten til konvertering af bankdata. Fortsæt med at angive det brugernavn og adgangskode, du har angivet for tjenesten i de relaterede konfigurationsfelter i [!INCLUDE[d365fin](includes/d365fin_md.md)].
5. I vinduet **Opsætning af tjeneste til konvertering af bankdata** skal du i feltet **Brugernavn** angive den samme værdi, som du har angivet som logonnavnet på serviceudbyderens side i trin 4.
6. I feltet **Adgangskode** skal du angive den samme værdi, som du har angivet i feltet **Adgangskode** på serviceudbyderens side i trin 4.

> [!NOTE]  
> Dine logondata krypteres automatisk.

## <a name="to-view-or-update-the-list-of-currently-supported-bank-data-formats"></a>Sådan ser eller opdaterer du listen over aktuelt understøttede bankdataformater
1. Vælg ikonet ![Søg efter side eller rapport](media/ui-search/search_small.png "Ikonet Søg efter side eller rapport"), angiv **Opsætning af tjeneste til konvertering af bankdata**, og vælg derefter det relaterede link.
2. I vinduet **Opsætning af tjeneste til konvertering af bankdata** skal du vælge handlingen **Banknavn - datakonverteringsoversigt** for at åbne listen over banknavne, der repræsenterer bankdataformater, der understøttes af konverteringstjenesten.
3. På siden **Banknavn - datakonverteringsoversigt** skal du vælge handlingen **Opdater liste over banknavne**.

Listen over bankdataformater, der understøttes af tjenesten til konvertering af bankdata, er nu opdateret. Dette er listen over banknavne, der er filtreret efter det land/område, som du kan vælge i feltet **Banknavn - datakonvertering** i vinduet **Bankkontokort**.

> [!NOTE]  
>   Opdatering af understøttede bankdataformater opstår også, når du vælger eller angiver en værdi i feltet **Banknavn - datakonvertering** på bankkontoen.

Du er nu tilmeldt tjenesten til konvertering af bankdata. Fortsæt med at afspejle tilmeldingsoplysningerne for hver bankkonto, der bruger tjenesten.

## <a name="see-also"></a>Se også
[Konfigurere banktransaktioner](bank-setup-banking.md)  
[Håndtere bankkonti](bank-manage-bank-accounts.md)  
[Arbejde med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

