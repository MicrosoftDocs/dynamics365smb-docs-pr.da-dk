---
title: Tilpasse Business Central Online ved brug af apps
description: Få mere at vide om tilføjelse af funktioner og tilpasning af Business Central ved at installere apps i denne artikel.
author: edupont04
ms.topic: conceptual
ms.search.keywords: 'app, add-in, manifest, customize'
ms.search.form: '2500, 2502, 20350, 20353'
ms.date: 09/27/2022
ms.author: edupont
---
# <a name="customizing-business-central-online-with-apps"></a>Tilpasse Business Central Online med apps

Du kan ændre [!INCLUDE[prod_short](includes/prod_short.md)] online ved at installere apps, der f.eks. tilføjer funktioner, ændrer funktionsmåder eller giver dig adgang til nye onlinetjenester. Disse apps kaldes også *udvidelser*, fordi de *udvider* [!INCLUDE [prod_short](includes/prod_short.md)].

## <a name="manage-apps"></a>Administrere apps

[!INCLUDE [2023rw1-sec-group-short](includes/2023rw1-sec-group-short.md)]

Når du starter [!INCLUDE[prod_short](includes/prod_short.md)] første gang, er der allerede installeret nogle apps for dig. Med tiden gøres flere apps tilgængelige for dig, og du kan derefter vælge, om du vil bruge appen eller ej.

Microsoft leverer f.eks. en app, der giver integration med PayPal Payments Standard. Denne udvidelse er installeret som standard. Men hvis en anden udvidelse, som tilbyder integration med en anden betalingstjeneste, stilles til rådighed, kan du installere nye udvidelse og derefter vælge, hvilken af to de tjenester du vil bruge.  

Hvis du vil bruge de funktioner, der findes i en app, f.eks. åbne sider, køre rapporter, vælge handlinger osv., skal du være tildelt de rettighedssæt, der er installeret som en del af appen.

Hvis du vil installere eller afinstallere apps fra AppSource eller tilføje udvidelser pr. lejer, skal du have de rigtige rettigheder. Du skal enten være medlem af brugergruppen **D365-udvid.styring**, eller du skal have tilladelsessættet **EXTEN. MGT. - ADMIN**. Hvis du er administrator, kan du tildele brugergrupper og rettigheder til andre brugere i virksomheden. Du kan finde flere oplysninger i [Oprette brugere i henhold til licenser](ui-how-users-permissions.md).  

> [!IMPORTANT]  
> For [!INCLUDE [prod_short](includes/prod_short.md)] lokalt kan du ikke overføre udvidelser pr. lejer eller installere AppSource-apps via siden **Udvidelsesstyring**. Du kan ikke installere AppSource-apps, herunder i Docker-baserede installationer.

Du kan administrere apps på siden **Udvidelsesstyring**. Du kan åbne siden fra Start. Du kan også vælge ikonet **Søg efter side eller rapport** ![Elpære, der åbner funktionen Fortæl mig](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig"), skrive **Udvidelse** i øverste højre hjørne og derefter vælge det relaterede kæde. Du kan finde flere oplysninger i [Installere og afinstallere apps](ui-extensions-install-uninstall.md).

> [!NOTE]  
> Hvis du mener, at du skal have adgang til en app, men ikke kan finde de relevante funktioner, skal du vælge siden **Udvidelsesstyring** – hvis appen ikke er angivet der, kan du installere den som beskrevet i følgende afsnit.  

> [!NOTE]  
> Log på [AppSource.microsoft.com](https://appsource.microsoft.com/) ved hjælp af den mailkonto, du bruger til [!INCLUDE[prod_short](includes/prod_short.md)] online. Brug den samme mailkonto til andre tjenester og produkter for at opnå en ensartet oplevelse.  

Du kan også få adgang til markedspladsen i [!INCLUDE[prod_short](includes/prod_short.md)]. På siden **Udvidelsesstyring** kan du se de apps, der er installeret, og du kan åbne siden **Markedsplads for udvidelse** for at se de apps til [!INCLUDE[prod_short](includes/prod_short.md)], der er tilgængelige i AppSource. Hvis du vælger linket *Flere apps*, åbnes [AppSource.microsoft.com](https://appsource.microsoft.com/marketplace/apps?product=dynamics-365%3Bdynamics-365-business-central&page=1).  

Hvis du vælger en app, du kan finde oplysninger om, hvad appen gør, og du kan få adgang til hjælp for at få mere at vide om appen. Når du vælger at hente en app, skal du acceptere vilkårene for anvendelse. Hvis du henter appen fra AppSource-webstedet, logges du på [!INCLUDE[prod_short](includes/prod_short.md)] for at fuldføre installationen.  

Når du installerer en app, kan det være nødvendigt at konfigurere den, f.eks. angive en konto til brug sammen med udvidelsen **PayPal Payments Standard til [!INCLUDE[prod_short](includes/prod_short.md)]**.
Andre apps føjer simpelthen felter til en eksisterende side, eller de tilføjer en ny side f.eks.   

Hvis du fjerner en app, og du senere skifter mening, kan du installere den igen. Når du fjerner en app, som du har brugt, bevares dataene, så de stadig tilgængelige, hvis du installerer appen igen. Nogle apps er obligatoriske. Du kan ikke fjerne disse fra siden **Udvidelsesstyring**. Hvis du prøver, vises der en fejlmeddelelse.  

Nogle apps er fra Microsoft, mens andre apps leveres af [andre virksomheder](ui-extensions-other.md). Alle apps testes, før de bliver tilgængelige for dig, men det anbefales, at du bruger de links, der følger med hver udvidelse, for at få mere at vide om appen, før du vælger at installere den.  

> [!NOTE]  
> Du kan holde øje med nye apps fra Microsoft og andre leverandører på [AppSource.microsoft.com](https://appsource.microsoft.com/marketplace/apps?product=dynamics-365%3Bdynamics-365-business-central&page=1).

## <a name="apps-and-data-transfer"></a>Apps og dataoverførsel

Da følgende apps kommunikerer med andre tjenester, kan de overføre data uden for [!INCLUDE[prod_short](includes/prod_short.md)]-miljøet:

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
* Online kort
* EU-momsregistreringsnr. Tjeneste

## <a name="connect-your-business"></a>Opret forbindelse til din virksomhed

Fra 2022 udgivelsesbølge 2 kan [!INCLUDE [prod_short](includes/prod_short.md)] onlinemiljøer vise en liste over en eller flere apps på siderne **forbindelsesapps** og **Bank-apps**. Disse apps kan oprette forbindelse mellem din virksomhed og eksterne tjenester for at øge produktiviteten ved at automatisere processerne. Du kan f. eks. oprette forbindelse til banker og automatisk importere banktransaktioner. Det er nemt at installere og konfigurere apps direkte fra denne side. Vælg en app for at få mere at vide om egenskaber og priser.  

Vis listen over foreslåede apps ved at vælge handlingen **Forbindelses-apps** på siden **Udvidelsesstyring**.  

> [!NOTE]
> Den første person, der åbner siden **Forbindelses-apps**, skal tillade, at udvidelsen opretter forbindelse til en ekstern tjeneste. Tillad forbindelsen én gang eller altid. Hvis du vælger at spærre forbindelsen, skal du finde de relevante apps på AppSource.

Denne eksterne tjeneste opretter en liste over relevante apps, der er baseret på dit land eller område

## <a name="recommended-apps"></a>Anbefalede apps

Microsoft-partnere og -forhandlere kan oprette en app, som de kan bruge til at kompilere lister over apps, som de ofte anbefaler til deres kunder. Hvis de gør det og har installeret appen til din lejer, vil appsene være tilgængelige på siden **Anbefalede apps**. Der kan du læse om hver app og beslutte, om du vil installere dem.

> [!NOTE]
> Hvis du er Microsoft-partner eller -forhandler, og du er interesseret i at levere en liste over anbefalede apps, skal du se [Anbefal apps fra AppSource](/dynamics365/business-central/dev-itpro/administration/recommend-apps) i administrationsindholdet.

## <a name="see-related-microsoft-training"></a>Se relateret [Microsoft-træning](/training/modules/customize-dynamics-365-business-central/)

## <a name="see-also"></a>Se også

[Installere og afinstallere apps](ui-extensions-install-uninstall.md)  
[Tilpasse Business Central](ui-customizing-overview.md)  
[Business Central-apps fra andre leverandører](ui-extensions-other.md)  
[Konfigurere tjenesten Envestnet Yodlee Bank Feeds](bank-how-setup-bank-statement-service.md)  
[Aktivere debitorbetalinger via betalingstjenester](sales-how-enable-payment-service-extensions.md)  
[Overføre Business Data fra andre økonomisystemer](across-import-data-configuration-packages.md)  
[Konfigurere udvidelsen Britiske GetAddress.io-postnumre](LocalFunctionality/UnitedKingdom/uk-setup-postal-code-service.md)  
[[!INCLUDE[prod_short](includes/prod_short.md)]-apps fra andre leverandører](ui-extensions-other.md)  
[Blive køreklar](ui-get-ready-business.md)  

## [!INCLUDE[prod_short](includes/free_trial_md.md)]


[!INCLUDE[footer-include](includes/footer-banner.md)]
