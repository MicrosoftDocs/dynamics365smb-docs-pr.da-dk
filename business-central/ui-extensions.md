---
title: Tilpasse Business Central Online ved brug af udvidelser
description: Få mere at vide om tilføjelse af funktioner og tilpasning af Business Central ved at installere udvidelser.
author: edupont04
ms.topic: conceptual
ms.search.keywords: app, add-in, manifest, customize
ms.search.form: 2500, 2502
ms.date: 03/22/2022
ms.author: edupont
ms.openlocfilehash: 56c564274e396d9699286b18d882c2a21f8721ef
ms.sourcegitcommit: 8a12074b170a14d98ab7ffdad77d66aed64e5783
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 03/31/2022
ms.locfileid: "8510683"
---
# <a name="customizing-business-central-online-using-extensions"></a>Tilpasse Business Central Online ved brug af udvidelser

Du kan ændre [!INCLUDE[prod_short](includes/prod_short.md)] online ved at installere udvidelser, der f.eks. tilføjer funktioner, ændrer funktionsmåder eller giver dig adgang til nye onlinetjenester.

> [!NOTE]
> Hvis du vil installere eller afinstallere udvidelser fra AppSource eller tilføje udvidelser pr. lejer, skal du have de rigtige rettigheder. Du skal enten være medlem af brugergruppen **D365-udvid.styring**, eller du skal have tilladelsessættet **EXTEN. MGT. - ADMIN**. Hvis du er administrator, kan du tildele brugergrupper og rettigheder til andre brugere i virksomheden. Du kan finde flere oplysninger i [Oprette brugere i henhold til licenser](ui-how-users-permissions.md).  
>
> Hvis du vil bruge de funktioner, der findes i en udvidelse, f.eks. åbne sider, køre rapporter, vælge handlinger osv., skal du være tildelt de rettighedssæt, der er installeret som en del af udvidelsen.

<!-- [!NOTE]  
> The **EXTEN. MGT. - ADMIN** permission set was introduced in 2021 release wave 1 as a replacement for the **D365 EXTENSION MGT** permission set in earlier versions.-->

> [!IMPORTANT]  
> Overførsel af udvidelser pr. lejer og installation af AppSource-udvidelser understøttes ikke via siden **Udvidelsesstyring** til lokale installationer. Du kan ikke installere AppSource-lokalnumre, herunder i Docker-baserede installationer.

Når du starter [!INCLUDE[prod_short](includes/prod_short.md)] første gang, er der allerede installeret nogle udvidelser for dig. Med tiden gøres flere udvidelser tilgængelige for dig, og du kan derefter vælge, om du vil bruge udvidelsen eller ej.

Microsoft leverer f.eks. en udvidelse, der giver integration med PayPal Payments Standard. Denne udvidelse er installeret som standard.
Men hvis en anden udvidelse, som tilbyder integration med en anden betalingstjeneste, stilles til rådighed, kan du installere nye udvidelse og derefter vælge, hvilken af to de tjenester du vil bruge.  

Du kan administrere udvidelserne på siden **Udvidelsesstyring**. Du kan åbne siden fra Start. Du kan også vælge ikonet **Søg efter side eller rapport** ![Elpære, der åbner funktionen Fortæl mig](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig"), skrive **Udvidelse** i øverste højre hjørne og derefter vælge det relaterede kæde. Du kan finde flere oplysninger i [Installere og fjerne udvidelser](ui-extensions-install-uninstall.md).

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

> [!NOTE]  
> Du kan holde øje med nye udvidelser fra Microsoft og andre leverandører på [AppSource.microsoft.com](https://appsource.microsoft.com/marketplace/apps?product=dynamics-365%3Bdynamics-365-business-central&page=1).


## <a name="extensions-and-data-transfer"></a>Udvidelser og dataoverførsel

Da følgende udvidelser kommunikerer med andre tjenester, kan de overføre data uden for [!INCLUDE[prod_short](includes/prod_short.md)]-miljøet:

* Udvidelsen AMC Banking 365 Fundamentals
* Billedanalyse
* Forudsigelse af forsinket betaling
* PayPal Payments Standard
* Salgs- og lagerprognose
* WorldPay Payments Standard

Dette gælder også nogle funktioner i basisprogrammet, f.eks. følgende funktioner:

* Pengestrømsprognose
* Dokumentudvekslingstjeneste
* Dataverse-forbindelser
* OCR-tjeneste
* Online Map
* EU-momsregistreringsnr. Tjeneste

## <a name="recommended-apps"></a>Anbefalede apps
Microsoft-partnere og -forhandlere kan oprette en udvidelse, som de kan bruge til at kompilere lister over apps, som de ofte anbefaler til deres kunder. Hvis de gør det og har installeret udvidelsen til din lejer, vil appsene være tilgængelige på siden **Anbefalede apps**. Der kan du læse om hver app og beslutte, om du vil installere dem.

> [!NOTE]
> Hvis du er Microsoft-partner eller -forhandler, og du er interesseret i at levere en liste over anbefalede apps, skal du se [Anbefal apps fra AppSource](/dynamics365/business-central/dev-itpro/administration/recommend-apps).

## <a name="see-also"></a>Se også

[Installere og fjerne udvidelser](ui-extensions-install-uninstall.md)  
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
