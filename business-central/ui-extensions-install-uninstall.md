---
title: Installere og fjerne udvidelser i Business Central | Microsoft Docs
description: Få mere at vide om at installere og fjerne udvidelser i Business Central.
documentationcenter: ''
author: SusanneWindfeldPedersen
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: app, add-in, manifest, customize, install, uninstall
ms.date: 06/03/2021
ms.author: solsen
ms.openlocfilehash: 09d1998bcd8cdf522b1533fe4768a0bbf0aca776
ms.sourcegitcommit: a7cb0be8eae6ece95f5259d7de7a48b385c9cfeb
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 07/08/2021
ms.locfileid: "6434982"
---
# <a name="installing-and-uninstalling-extensions-in-business-central"></a>Installere og fjerne udvidelser i Business Central

Du kan ændre [!INCLUDE[prod_short](includes/prod_short.md)] ved at installere udvidelser, der f.eks. tilføjer funktioner, ændrer funktionsmåder eller giver dig adgang til nye onlinetjenester. Du kan finde flere oplysninger i [Tilpasse Business Central ved hjælp af udvidelser](ui-extensions.md).

> [!NOTE]
> Hvis du vil installere udvidelser fra AppSource eller tilføje udvidelser pr. lejer, skal du have de rigtige rettigheder. Du skal enten være medlem af filen EXTEND. MGT. - ADM-brugergruppe, eller du skal have funktionen EXTEND. MGT. - ADM-rettighedssæt Hvis du er administrator, kan du tildele brugergrupper og rettigheder til andre brugere i virksomheden.
>
> Hvis du vil bruge de funktioner, der findes i en udvidelse, f.eks. åbne sider, køre rapporter, vælge handlinger osv., skal du være tildelt de rettighedssæt, der er installeret som en del af udvidelsen.

> [!NOTE]  
> Funktionen **EXTEND. MGT. - ADMIN**-tilladelsessættet blev introduceret i Business Central 2021 Release Wave 1 som en erstatning for **D365 EXTENSION MGT**-tilladelsessættet i tidligere versioner.

## <a name="installing-an-extension"></a>Installation af en udvidelse

Du kan administrere udvidelser på siden **Udvidelsesstyring**. Du kan åbne siden fra Start. Alternativt kan du vælge ikonet **Søg efter side eller rapport** ![Lightbulb, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") Skriv **Udvidelse** i øverste højre hjørne , og vælg derefter det relaterede link.  

Du kan få nye udvidelser fra markedspladsen på [AppSource.microsoft.com](https://go.microsoft.com/fwlink/?linkid=2081646). Her kan du se alle tilgængelige udvidelser for [!INCLUDE[prod_short](includes/prod_short.md)], og du kan få apps, udvidelser og indholdspakker til andre Microsoft-produkter. Angiv de relevante filtre, kig på oplysningerne om hver udvidelse og hent en udvidelse til [!INCLUDE[prod_short](includes/prod_short.md)].  

> [!NOTE]  
> Log på [AppSource.microsoft.com](https://appsource.microsoft.com/) ved hjælp af den mailkonto, du bruger til [!INCLUDE[prod_short](includes/prod_short.md)]. Brug den samme mailkonto til andre tjenester og produkter for at opnå en ensartet oplevelse.  

Du kan også få adgang til markedspladsen i [!INCLUDE[prod_short](includes/prod_short.md)]. På siden **Udvidelsesstyring** kan du se de udvidelser, der er installeret, og du kan åbne siden **Markedsplads for udvidelse** for at se de udvidelser til [!INCLUDE[prod_short](includes/prod_short.md)], der er tilgængelige i AppSource. Hvis du vælger linket *Flere apps*, åbnes [AppSource.microsoft.com](https://go.microsoft.com/fwlink/?linkid=2081646).  

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

## <a name="uninstalling-an-extension"></a>Fjerne en udvidelse

Du fjerner en udvidelse via siden **Udvidelsesstyring**. Hvis du fjerner en udvidelse, og du senere skifter mening, kan du installere udvidelsen igen. Når du fjerner en udvidelse, som du har brugt, bevares dataene som standard, hvis du installerer udvidelsen igen. Du kan i stedet vælge at slette dataene med udvidelsen. Dette styres af afkrydsningsfeltet **Slet udvidelsesdata**. Dette afkrydsningsfelt er som standard *ikke aktiveret*.

> [!IMPORTANT]  
> Hvis du aktiverer afkrydsningsfeltet **Slet udvidelsesdata**, skal du vælge **OK** i den viste bekræftelsesdialogboks. Når afkrydsningsfeltet **Slet udvidelsesdata** er aktiveret, kan du nu fjerne udvidelsen, og du bliver på ny bedt om at bekræfte, at du vil fjerne udvidelsen og slette dataene. Handlingen kan ikke fortrydes.
Visse udvidelser er påkrævet. Du kan ikke fjerne disse fra siden **Udvidelsesstyring**. Hvis du prøver, vises der en fejlmeddelelse.  

## <a name="see-also"></a>Se også

[Tilpasse Business Central](ui-customizing-overview.md)  
[Business Central-udvidelser fra andre leverandører](ui-extensions-other.md)  
[Konfigurere tjenesten Envestnet Yodlee Bank Feeds](bank-how-setup-bank-statement-service.md)  
[Aktivere debitorbetaling via PayPal](sales-how-enable-payment-service-extensions.md)  
[Overførsel af virksomhedsdata fra andre økonomisystemer](across-import-data-configuration-packages.md)  
[Konfiguration af den britiske GetAddress.io-postnummerudvidelse](LocalFunctionality/UnitedKingdom/uk-setup-postal-code-service.md)  
[[!INCLUDE[prod_short](includes/prod_short.md)]-udvidelser fra andre leverandører](ui-extensions-other.md)  
[Blive køreklar](ui-get-ready-business.md)  

## [!INCLUDE[prod_short](includes/free_trial_md.md)]  


[!INCLUDE[footer-include](includes/footer-banner.md)]