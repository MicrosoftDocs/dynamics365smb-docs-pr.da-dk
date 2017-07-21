---
title: Installation af udvidelser til tilpasning af Dynamics 365 for Financials | Microsoft Docs
description: "Få mere at vide om tilføjelse af funktioner og tilpasning af Dynamics 365 for Financials ved at installere udvidelser."
documentationcenter: 
author: edupont04
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: app, add-in, manifest, customize
ms.date: 07/05/2017
ms.author: edupont
ms.translationtype: Human Translation
ms.sourcegitcommit: 85d15de13739e944ff8817b402b37ae1c7e1b144
ms.openlocfilehash: 6bf7d2024ff9f0254e1d885580126fb16c0c6fce
ms.contentlocale: da-dk
ms.lasthandoff: 07/07/2017


---
# <a name="customizing-dynamics-365-for-financials-using-extensions"></a>Tilpasse Dynamics 365 for Financials ved hjælp af udvidelser
Du kan ændre [!INCLUDE[d365fin](includes/d365fin_md.md)] ved at installere udvidelser, der f.eks. tilføjer funktioner, ændrer funktionsmåder eller giver dig adgang til nye onlinetjenester.
Når du starter [!INCLUDE[d365fin](includes/d365fin_md.md)] første gang, er der allerede installeret nogle udvidelser for dig. Med tiden gøres flere udvidelser tilgængelige for dig, og du kan derefter vælge, om du vil bruge udvidelsen eller ej.

Microsoft leverer f.eks. en udvidelse, der giver integration med PayPal Payments Standard. Denne udvidelse er installeret som standard.
Men hvis en anden udvidelse, som tilbyder integration med en anden betalingstjeneste, stilles til rådighed, kan du installere nye udvidelse og derefter vælge, hvilken af to de tjenester du vil bruge.  

Du kan administrere udvidelserne i vinduet **Udvidelsesstyring**. Du kan åbne vinduet fra Start. Du kan også vælge ikonet **Søg efter side eller rapport** ![Søg efter side eller rapport](media/ui-search/search_small.png "Ikonet Søg efter side eller rapport") i det øverste højre hjørne, angive **Udvidelser** og derefter vælge det relaterede link.  

> [!NOTE]  
>   Hvis du mener, at du skal have adgang til en udvidelse, men ikke kan finde de relevante funktioner, skal du vælge vinduet **Udvidelsesstyring** – hvis filtypen ikke er angivet der, kan du installere den som beskrevet i følgende afsnit.  

## <a name="installing-an-extension"></a>Installation af en udvidelse
Du kan få nye udvidelser fra markedspladsen på [AppSource.microsoft.com](https://appsource.microsoft.com/en-us/marketplace/apps?product=dynamics-365%3Bdynamics-365-for-financials&page=1). Her kan du se alle tilgængelige udvidelser for [!INCLUDE[d365fin](includes/d365fin_md.md)], og du kan få apps, udvidelser og indholdspakker til andre Microsoft-produkter. Angiv de relevante filtre, kig på oplysningerne om hver udvidelse og hent en udvidelse til [!INCLUDE[d365fin](includes/d365fin_md.md)].  
> [!NOTE]  
>   Log på [AppSource.microsoft.com](https://appsource.microsoft.com/) ved hjælp af den mailkonto, du bruger til [!INCLUDE[d365fin](includes/d365fin_md.md)]. Brug den samme mailkonto til andre tjenester og produkter for at opnå en ensartet oplevelse.  

Du kan også få adgang til markedspladsen i [!INCLUDE[d365fin](includes/d365fin_md.md)]. I vinduet **Udvidelsesstyring** kan du se de udvidelser, der er installeret, og du kan åbne siden **Markedsplads for udvidelse** for at se de udvidelser til [!INCLUDE[d365fin](includes/d365fin_md.md)], der er tilgængelige i AppSource. Hvis du vælger linket *Flere apps*, åbnes [AppSource.microsoft.com](https://appsource.microsoft.com/en-us/marketplace/apps?product=dynamics-365%3Bdynamics-365-for-financials&page=1).  

Hvis du vælger en udvidelse, du kan finde oplysninger om, hvad den gør, og du kan få adgang til hjælp for at få mere at vide om udvidelsen. Når du vælger at hente en udvidelse, skal du acceptere vilkårene for anvendelse. Hvis du henter udvidelsen fra AppSource-webstedet, logges du på [!INCLUDE[d365fin](includes/d365fin_md.md)] for at fuldføre installationen.  

Når du installerer en udvidelse, kan det være nødvendigt at konfigurere den, f.eks. angive en konto til brug sammen med udvidelsen **PayPal Payments Standard til [!INCLUDE[d365fin](includes/d365fin_md.md)]**.
Andre udvidelser føjer simpelthen felter til en eksisterende side, eller de tilføjer en ny side f.eks.   

Hvis du fjerner en udvidelse, og du senere skifter mening, kan du installere den igen. Når du fjerner en udvidelse, som du har brugt, bevares dataene, så de stadig tilgængelige, hvis du installerer udvidelsen igen.  

Nogle udvidelser er fra Microsoft, mens andre udvidelser leveres af [andre virksomheder](ui-extensions-other.md). Alle udvidelser testes, før de bliver tilgængelige for dig, men det anbefales, at du bruger de links, der følger med hver udvidelse, for at få mere at vide om udvidelsen, før du vælger at installere den.  

Microsoft tilbyder følgende udvidelser:  

* [Overførsel af data med Dynamics GP](ui-extensions-dynamicsgp-data-migration.md)  
* [Envestnet Yodlee Bank Feeds](ui-extensions-yodlee-bank-feeds.md)  
* [PayPal Payments Standard](ui-extensions-paypal-payments-standard.md)  
* [Overflytning af QuickBooks Data](ui-extensions-quickbooks-data-migration.md)  
* [Salgs- og lagerprognose](ui-extensions-sales-forecast.md)  
* [Ceridian løn](ui-extensions-ceridian-payroll.md)  
* [Import af Quickbooks-lønfiler](ui-extensions-quickbooks-payroll.md)  
* [WorldPay Payments Standard](ui-extensions-worldpay-payments-standard.md)
* [Britiske GetAddress.io-postnumre](ui-extensions-getaddressio.md)
* [Overførsel af QuickBooks Online-data](ui-extensions-quickbooks-online-data-migration.md)
* [Revisorportal](ui-extensions-accountant-portal.md)  
* [Billedanalyse](ui-extensions-image-analyzer.md)

> [!NOTE]  
>  Der findes ingen nye udvidelser i AppSource umiddelbart efter, at vi har oplyst om en opdatering. Du kan holde øje med udvidelser på [AppSource.microsoft.com](https://appsource.microsoft.com/en-us/marketplace/apps?product=dynamics-365%3Bdynamics-365-for-financials&page=1).

## <a name="see-also"></a>Se også
[Fremgangsmåde: Konfigurere tjenesten Envestnet Yodlee Bank Feeds](bank-how-setup-bank-statement-service.md)  
[Fremgangsmåde: Aktivere debitorbetaling via PayPal](sales-how-enable-payment-service-extensions.md)  
[Overføre virksomhedsdata fra andre økonomisystemer](upload-data.md)  
[Konfigurere den britiske GetAddress.io-postnummerudvidelse](uk-setup-postal-code-service.md)  
[[!INCLUDE[d365fin](includes/d365fin_md.md)]-udvidelser fra andre leverandører](ui-extensions-other.md)  
[Velkommen til [!INCLUDE[d365fin_long](includes/d365fin_long_md.md)]](index.md)  

## [!INCLUDE[d365fin](includes/free_trial_md.md)]

