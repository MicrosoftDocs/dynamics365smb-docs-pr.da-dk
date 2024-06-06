---
title: Installere og afinstallere apps
description: Få mere at vide om at installere og afinstallere apps i Business Central.
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bholtorf
ms.topic: conceptual
ms.date: 09/07/2023
ms.custom: bap-template
ms.search.keywords: 'app, add-in, manifest, customize, install, uninstall'
ms.search.form: '2500, 2514, 20350'
ms.service: dynamics-365-business-central
---

# <a name="install-and-uninstall-extensions-apps-in-business-central"></a>Installere og fjerne udvidelser (apps) i Business Central

Du kan ændre [!INCLUDE[prod_short](includes/prod_short.md)] ved at installere apps, der f.eks. tilføjer funktioner, ændrer funktionsmåder eller giver dig adgang til nye onlinetjenester. Du kan finde flere oplysninger i [Tilpasse Business Central ved hjælp af udvidelser](ui-extensions.md).

> [!NOTE]
> Hvis du vil installere eller afinstallere apps fra AppSource eller tilføje apps pr. lejer, skal du have de rigtige rettigheder. Du skal enten være medlem af brugergruppen D365-udvidelse MGT, eller du skal have EXTEND. MGT. - ADM-rettighedssæt Hvis du er administrator, kan du tildele brugergrupper og rettigheder til andre brugere i virksomheden. Du kan finde flere oplysninger om brugergrupper og tilladelser i [Tildele tilladelser til brugere og grupper](ui-define-granular-permissions.md).
>
> Hvis du vil bruge de funktioner, der findes i en udvidelse, f.eks. åbne sider, køre rapporter, vælge handlinger osv., skal du være tildelt de rettighedssæt, der er installeret som en del af udvidelsen.

Hvis du vil bruge et filtypenavn, skal du have fået tildelt de tilladelsessæt, der følger med.

## <a name="install-an-extension"></a><a name="install"></a>Installér en udvidelse

Du kan administrere apps og udvidelser på siden **Udvidelsesstyring**. Du kan åbne siden fra Start. Alternativt kan du vælge ikonet **Søg efter side eller rapport** ![Lightbulb, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") Skriv **Udvidelse** i øverste højre hjørne , og vælg derefter det relaterede link.  

Du kan få nye apps fra markedspladsen på [AppSource.microsoft.com](https://go.microsoft.com/fwlink/?linkid=2081646). Markedspladsen tilbyder alle tilgængelige apps til [!INCLUDE[prod_short](includes/prod_short.md)], plus apps og indholdspakker til andre Microsoft-produkter. Angiv de relevante filtre, kig på oplysningerne om hver udvidelse og hent en udvidelse til [!INCLUDE[prod_short](includes/prod_short.md)].  

> [!NOTE]  
> Log på [AppSource.microsoft.com](https://appsource.microsoft.com/) ved hjælp af den mailkonto, du bruger til [!INCLUDE[prod_short](includes/prod_short.md)]. Brug den samme mailkonto til andre tjenester og produkter for at opnå en ensartet oplevelse.  

Du kan også komme til AppSource fra [!INCLUDE[prod_short](includes/prod_short.md)]. På siden **Udvidelsesstyring** kan du se de apps, der er installeret, og du kan åbne siden **Markedsplads for udvidelse** for at se de apps til [!INCLUDE[prod_short](includes/prod_short.md)], der er tilgængelige i AppSource. Hvis du vælger linket *Flere apps*, åbnes [AppSource.microsoft.com](https://go.microsoft.com/fwlink/?linkid=2081646).  

Vælg en app for at lære, hvad appen gør, og du kan få adgang til hjælp for at få mere at vide om appen. Når du vælger at hente en app, skal du acceptere vilkårene for anvendelse. Hvis du henter appen fra AppSource-webstedet, logges du på [!INCLUDE[prod_short](includes/prod_short.md)] for at fuldføre installationen.  

Når du har installeret en app, skal du muligvis konfigurere den. Nogle apps kræver, at du angiver nogle oplysninger, før du kan bruge dem. Når du f. eks. har installeret **PayPal Payments Standard**-programmet, skal du angive e-mail-adressen eller forhandlerkonto-id'et for din PayPal-konto. Hvis du vil oprette en app eller finde ud af, hvilke oplysninger du skal bruge, skal du vælge **opsætningshandlingen** på siden **installerede udvidelser**.  

Andre apps føjer simpelthen felter til en eksisterende side, eller de tilføjer en ny side f.eks.

Hvis du fjerner en app, og du senere skifter mening, kan du installere den igen. Når du fjerner en app, som du har brugt dine data, er de ikke slettet. Dataene er tilgængelige, hvis du installerer appen igen.

Nogle apps er fra Microsoft, mens andre apps leveres af [andre virksomheder](ui-extensions-other.md). Det anbefales, at du lærer mere om appen, inden du vælger at installere den.

Microsoft tilbyder følgende apps:

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
* [Import af QuickBooks-lønfiler](ui-extensions-quickbooks-payroll.md)
* [Salgs- og lagerprognose](ui-extensions-sales-forecast.md)
* [Momsgruppe](ui-extensions-vat-group.md)
* [WorldPay Payments Standard](ui-extensions-worldpay-payments-standard.md)
* [DK – C5-dataoverførsel](ui-extensions-c5-data-migration.md)
* [DK - Betalinger og afstemninger](ui-extensions-payments-reconciliation-formats-dk.md)
* [DK – Tax File Formats](ui-extensions-tax-file-formats-dk.md)
* [Udvidelse til britiske GetAddress.io-postnumre](LocalFunctionality/UnitedKingdom/ui-extensions-getaddressio.md)  
* [US/CA/UK/AU/NZ/ZA - Send remitteringsadvis](ui-extensions-send-remittance-advice.md)

## <a name="set-up-an-app"></a>Konfigurere en app

Når du har installeret en app, skal du muligvis konfigurere den. F. eks. skal du angive den PayPal-konto, der skal bruges, for **PayPal Payments Standard for [!INCLUDE[prod_short](includes/prod_short.md)]**-appen. Hvis det er tilfældet, bliver du spurgt, om du vil konfigurere appen med det samme, når installationen har fuldført [!INCLUDE[prod_short](includes/prod_short.md)]. Der kan kræves opsætninger, før appen kan fungere, eller eventuelt.

Hvis du vælger at konfigurere din app med det samme, og den har en nødvendig installation, [!INCLUDE[prod_short](includes/prod_short.md)] åbnes den nødvendige installation. Opsætningen kan enten være en side, hvor du indtaster oplysninger, eller en assisteret opsætningsvejledning, der kan hjælpe dig gennem trinnene. Hvis du ikke fuldfører installationsprogrammet på én gang, kan du bruge **opsætningerne til _navnet på den app_**-side, som viser alle opsætninger for appen. Krævede opsætninger angivet med **fede bogstaver**.

## <a name="upload-a-per-tenant-extension-pte"></a>Overfører en udvidelse pr. lejer (PTE)

Du kan overføre en PTE ved hjælp af siden **styring af udvidelser**. Gå til **Administrer** på siden **udvidelsesstyring**, og vælg derefter **Overfør udvidelse**. Angiv den. programfil, der skal overføres, på siden **Overfør og installér udvidelse**. Hvis du vil fortsætte, skal du vælge knappen **Acceptér** og derefter knappen **Implementér** for at implementere PTE.

Hvis PTE indeholder ændringer af skemaændringer, er det muligt at *gennemtvinge* overførslen. Hvis du vil gøre det, skal du vælge indstillingen **Gennemtving** i tilstanden **Skemasynkronisering**. Du får vist en bekræftelsesdialogboks, før du fortsætter.  

## <a name="uninstall-an-app"></a>AfInstaller en app

Du fjerner en app via siden **Udvidelsesstyring**. Hvis du vil fjerne en app, skal du markere den på siden og derefter vælge handlingen til **afinstallation**. Hvis du fjerner en app, og du senere skifter mening, kan du installere appen igen.

Når du fjerner en app, som du har brugt dine data, er de som standard ikke slettet. Hvis du er sikker på, at du ikke vil installere appen igen, kan du slette dataene, når du fjerner den. Hvis du vil slette data, når du fjerner en app, skal du aktivere funktionen **Slet udvidelsesdata**. Du får vist en bekræftelsesdialogboks, og du skal vælge **Ja** for at slå den til. Når afkrydsningsfeltet **Slet udvidelsesdata** er aktiveret, kan du nu fjerne appen, og du bliver på ny bedt om at bekræfte, at du vil fjerne appen og slette dataene.

> [!IMPORTANT]  
> * Der kan være andre apps, der kræver eller afhænger af den app, du vil fjerne. Disse andre apps kaldes for *afhængigheder*. Du kan ikke fjerne en app, medmindre du også fjerner dens afhængigheder. Når du fjerner en app, der har afhængigheder, vises en dialogboks med en liste over afhængigheder. Hvis du vil fortsætte, skal du vælge **Ja** for at fjerne appen og dens afhængigheder.
> * Hvis du aktiverer til/fra-feltet **Slet udvidelsesdata**, slettes alle data for appen *plus* data til alle afhængige apps, når du fjerner appen. Handlingen kan ikke fortrydes.
> * Nogle apps kræves, og du kan ikke slette dem på siden **Udvidelsesstyring**.  

Hvis du vil beholde dataene for en afinstalleret app, kan du slette dataene senere. Siden **Slet underordnede udvidelsesdata** viser de apps, du stadig har data til. Slet dataene ved at vælge appen og derefter vælge **Slet data**. 

## <a name="see-also"></a>Se også

[Tilpasse Business Central](ui-customizing-overview.md)  
[Business Central-udvidelser fra andre leverandører](ui-extensions-other.md)  
[Konfigurere tjenesten Envestnet Yodlee Bank Feeds](bank-how-setup-bank-statement-service.md)  
[Aktivere debitorbetaling via PayPal](sales-how-enable-payment-service-extensions.md)  
[Overføre Business Data fra andre økonomisystemer](across-import-data-configuration-packages.md)  
[Konfigurere udvidelsen Britiske GetAddress.io-postnumre](LocalFunctionality/UnitedKingdom/uk-setup-postal-code-service.md)  
[[!INCLUDE[prod_short](includes/prod_short.md)]-udvidelser fra andre leverandører](ui-extensions-other.md)  
[Blive køreklar](ui-get-ready-business.md)  

## [!INCLUDE[prod_short](includes/free_trial_md.md)]  


[!INCLUDE[footer-include](includes/footer-banner.md)]
