---
title: Installation af udvidelser til tilpasning af Business Central
description: Få mere at vide om tilføjelse af funktioner og tilpasning af Business Central ved at installere udvidelser.
author: edupont04
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.search.keywords: app, add-in, manifest, customize
ms.date: 03/02/2021
ms.author: edupont
ms.openlocfilehash: d92fbe7c21da74c7818be4f249cdb373ed73539f
ms.sourcegitcommit: a9d48272ce61e5d512a30417412b5363e56abf30
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 03/04/2021
ms.locfileid: "5493274"
---
# <a name="customizing-business-central-online-using-extensions"></a>Tilpasse Business Central Online ved brug af udvidelser

Du kan ændre [!INCLUDE[prod_short](includes/prod_short.md)] online ved at installere udvidelser, der f.eks. tilføjer funktioner, ændrer funktionsmåder eller giver dig adgang til nye onlinetjenester.

> [!NOTE]
> Hvis du vil installere udvidelser fra AppSource eller tilføje udvidelser pr. lejer, skal du have de rigtige rettigheder. Du skal enten være medlem af brugergruppen D365 EXTENSION MGT, eller du skal have rettighedssættet D365 EXTENSION MGT. Hvis du er administrator, kan du tildele brugergrupper og rettigheder til andre brugere i virksomheden.

Hvis du vil bruge de funktioner, der findes i en udvidelse, f. eks. åbne sider, køre rapporter, vælge handlinger osv., skal du være tildelt de rettighedssæt, der er installeret som en del af udvidelsen.

> [!IMPORTANT]  
> Overførsel af udvidelser pr. lejer og installation af AppSource-udvidelser understøttes ikke via siden **Udvidelsesstyring** til lokale installationer. Du kan ikke installere AppSource-lokalnumre, herunder i Docker-baserede installationer.

Når du starter [!INCLUDE[prod_short](includes/prod_short.md)] første gang, er der allerede installeret nogle udvidelser for dig. Med tiden gøres flere udvidelser tilgængelige for dig, og du kan derefter vælge, om du vil bruge udvidelsen eller ej.

Microsoft leverer f.eks. en udvidelse, der giver integration med PayPal Payments Standard. Denne udvidelse er installeret som standard.
Men hvis en anden udvidelse, som tilbyder integration med en anden betalingstjeneste, stilles til rådighed, kan du installere nye udvidelse og derefter vælge, hvilken af to de tjenester du vil bruge.  

Du kan administrere udvidelserne på siden **Udvidelsesstyring**. Du kan åbne siden fra Start. Du kan også vælge ikonet **Søg efter side eller rapport** ![Elpære, der åbner funktionen Fortæl mig](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig"), skrive **Udvidelse** i øverste højre hjørne og derefter vælge det relaterede kæde. Du kan finde flere oplysninger under [Installere og fjerne udvidelser](ui-extensions-install-uninstall.md).

> [!NOTE]  
> Hvis du mener, at du skal have adgang til en udvidelse, men ikke kan finde de relevante funktioner, skal du vælge siden **Udvidelsesstyring** – hvis filtypen ikke er angivet der, kan du installere den som beskrevet i følgende afsnit.  

> [!NOTE]  
> Log på [AppSource.microsoft.com](https://appsource.microsoft.com/) ved hjælp af den mailkonto, du bruger til [!INCLUDE[prod_short](includes/prod_short.md)] online. Brug den samme mailkonto til andre tjenester og produkter for at opnå en ensartet oplevelse.  

Du kan også få adgang til markedspladsen i [!INCLUDE[prod_short](includes/prod_short.md)]. På siden **Udvidelsesstyring** kan du se de udvidelser, der er installeret, og du kan åbne siden **Markedsplads for udvidelse** for at se de udvidelser til [!INCLUDE[prod_short](includes/prod_short.md)], der er tilgængelige i AppSource. Hvis du vælger linket *Flere apps*, åbnes [AppSource.microsoft.com](https://appsource.microsoft.com/marketplace/apps?product=dynamics-365%3Bdynamics-365-business-central&page=1).  

Hvis du vælger en udvidelse, du kan finde oplysninger om, hvad den gør, og du kan få adgang til hjælp for at få mere at vide om udvidelsen. Når du vælger at hente en udvidelse, skal du acceptere vilkårene for anvendelse. Hvis du henter udvidelsen fra AppSource-webstedet, logges du på [!INCLUDE[prod_short](includes/prod_short.md)] for at fuldføre installationen.  

Når du installerer en udvidelse, kan det være nødvendigt at konfigurere den, f.eks. angive en konto til brug sammen med udvidelsen **PayPal Payments Standard til [!INCLUDE[prod_short](includes/prod_short.md)]**.
Andre udvidelser føjer simpelthen felter til en eksisterende side, eller de tilføjer en ny side f.eks.   

Hvis du fjerner en udvidelse, og du senere skifter mening, kan du installere den igen. Når du fjerner en udvidelse, som du har brugt, bevares dataene, så de stadig tilgængelige, hvis du installerer udvidelsen igen. Nogle udvidelser er obligatoriske. Du kan ikke fjerne disse fra siden **Udvidelsesstyring**. Hvis du prøver, vises der en fejlmeddelelse.  

Nogle udvidelser er fra Microsoft, mens andre udvidelser leveres af [andre virksomheder](ui-extensions-other.md). Alle udvidelser testes, før de bliver tilgængelige for dig, men det anbefales, at du bruger de links, der følger med hver udvidelse, for at få mere at vide om udvidelsen, før du vælger at installere den.  

Microsoft tilbyder følgende udvidelser:  

* [AMC Banking 365 Fundamentals-udvidelse](ui-extensions-amc-banking.md)
* [Ceridian løn](ui-extensions-ceridian-payroll.md)
* [Virksomhedshub](ui-extensions-company-hub.md)  
* [Dynamics GP Dataoverførsel](ui-extensions-dynamicsgp-data-migration.md)
* [Envestnet Yodlee Bank Feeds](ui-extensions-yodlee-bank-feeds.md)
* [Vigtig forretningsindsigt](ui-extensions-essential-business-insights.md)
* [Billedanalyse](ui-extensions-image-analyzer.md)
* [Intelligent sky](ui-extensions-data-replication.md)
* [Intelligent sky basis](ui-extensions-intelligent-cloud.md)  
* [Forudsigelser af forsinkede betalinger](ui-extensions-late-payment-prediction.md)
* [Microsoft Pay](ui-extensions-microsoft-pay-payments.md)
* [PayPal Payments Standard](ui-extensions-paypal-payments-standard.md)
* [Overflytning af QuickBooks Data](ui-extensions-quickbooks-data-migration.md)
* [QuickBooks Online Dataoverførsel](ui-extensions-quickbooks-online-data-migration.md)
* [Import af Quickbooks-lønfiler](ui-extensions-quickbooks-payroll.md)
* [Salgs- og lagerprognose](ui-extensions-sales-forecast.md)
* [Momsgruppe](ui-extensions-vat-group.md)
* [WorldPay Payments Standard](ui-extensions-worldpay-payments-standard.md)
* [DK – C5-dataoverførsel](ui-extensions-c5-data-migration.md)
* [DK - Betalinger og afstemninger](ui-extensions-payments-reconciliation-formats-dk.md)
* [DK – Tax File Formats](ui-extensions-tax-file-formats-dk.md)
* [Udvidelsen Britiske GetAddress.io-postnumre](LocalFunctionality/UnitedKingdom/ui-extensions-getaddressio.md)  
* [US/CA/UK/AU/NZ/ZA - Send remitteringsadvis](ui-extensions-send-remittance-advice.md)

> [!NOTE]  
> Du kan holde øje med nye udvidelser fra Microsoft og andre leverandører på [AppSource.microsoft.com](https://appsource.microsoft.com/marketplace/apps?product=dynamics-365%3Bdynamics-365-business-central&page=1).

## <a name="see-also"></a>Se også

[Tilpasse Business Central](ui-customizing-overview.md)  
[Business Central-udvidelser fra andre leverandører](ui-extensions-other.md)  
[Konfigurere tjenesten Envestnet Yodlee Bank Feeds](bank-how-setup-bank-statement-service.md)  
[Aktivere debitorbetaling via PayPal](sales-how-enable-payment-service-extensions.md)  
[Overførsel af virksomhedsdata fra andre økonomisystemer](across-import-data-configuration-packages.md)  
[Konfiguration af den britiske GetAddress.io-postnummerudvidelse](LocalFunctionality/UnitedKingdom/uk-setup-postal-code-service.md)  
[[!INCLUDE[prod_short](includes/prod_short.md)]-udvidelser fra andre leverandører](ui-extensions-other.md)  
[Introduktion](product-get-started.md)  

## [!INCLUDE[prod_short](includes/free_trial_md.md)]  


[!INCLUDE[footer-include](includes/footer-banner.md)]
