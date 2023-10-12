---
title: Kom i gang med Connector til Shopify
description: Første trin ved konfiguration af forbindelser mellem Business central og Shopify
ms.date: 03/27/2023
ms.topic: article
ms.service: dynamics365-business-central
ms.reviewer: solsen
ms.search.form: '30100, 30101, 30102, 30103, 30104, 30135,'
author: brentholtorf
ms.author: bholtorf
---

# <a name="get-started-with-the-shopify-connector"></a>Kom i gang med Shopify Connector

Forbind din Shopify-butik (eller butikker) med [!INCLUDE [prod_short](../includes/prod_short.md)], og maksimer produktiviteten. Administrere og få vist indsigter fra din virksomhed og din Shopify-butik som én enhed.

Hvis du vil bruge Shopify med [!INCLUDE [prod_short](../includes/prod_short.md)], skal du gøre følgende først. Denne artikel fungerer som en vejledning for at integrere din Shopify-butik med [!INCLUDE [prod_short](../includes/prod_short.md)].

## <a name="prerequisites-for-shopify"></a>Forudsætninger Shopify

Du skal have:

- En Shopify-konto
- En Shopify-onlinebutik

Du kan finde flere oplysninger om, hvordan du opretter Shopify-forsøg og anbefalede indstillinger, ved at gå til [Oprette og konfigurere Shopify-konto](shopify-account.md).

## <a name="prerequisites-for-business-central"></a>Forudsætninger for Business Central

- Kontroller først, at **[Shopify Connector](https://go.microsoft.com/fwlink/?linkid=2196238)**-appen er installeret.

  Appen er forudinstalleret for alle nye logon-vinduer og forsøg. Få mere at vide om at installere apps fra AppSource på [installere og af-installere udvidelser](../ui-extensions-install-uninstall.md#install). Følg de trin, der er angivet nedenfor, hvis du ikke har [!INCLUDE[prod_short](../includes/prod_short.md)].

- Kontroller, at brugeren har de rette tilladelser. Shopify Connector er dækket af **Shopify – admin (SHPFY – admin)**-rettighedssæt. Du kan finde flere oplysninger i [Oprette brugere i henhold til licenser](../ui-how-users-permissions.md) og [Tildele tilladelser til brugere og grupper](../ui-define-granular-permissions.md).

## <a name="install-the-dynamics-365-business-central-app-to-your-shopify-online-store"></a>Installere Dynamics 365 Business Central-app'en i din Shopify-onlinebutik

For eksisterende tilfælde af [!INCLUDE[prod_short](../includes/prod_short.md)] er dette trin valgfrit og kan springes over.

1. Find [Dynamics 365 Business Central](https://apps.shopify.com/dynamics-365-business-central)-appen på [Shopify AppStore](https://apps.shopify.com/)
2. Vælg knappen **Tilføj app**. Hvis du bliver bedt om det, skal du logge på din Shopify-konto. Vælg den ønskede online-butik, hvis du mere end en.
3. Når du har gennemset beskyttelsen af personlige oplysninger og tilladelser, skal du vælge knappen **Installer app**.

   Du kan finde og åbne den installerede **Dynamics 365 Business Central**-app i afsnittet **Apps** på sidepanelet på siden **Shopify admin**.
4. Vælg **Tilmeld dig nu** for at starte [!INCLUDE[prod_short](../includes/prod_short.md)]-prøveversionen, eller **Log på**, hvis du allerede har [!INCLUDE[prod_short](../includes/prod_short.md)]. Du bliver omdirigeret til din side [Business Central](https://businesscentral.dynamics.com).
5. Gør ét af følgende i [!INCLUDE[prod_short](../includes/prod_short.md)].

## <a name="connect-business-central-to-the-shopify-online-store"></a>Forbinde Business central med Shopify-onlinebutikken

1. Vælg ![Lightbulb, der åbner funktionen Fortæl mig.](../media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **Shopify Butik**, og vælg det relevante link.
2. Vælg handlingen **Ny**.  
3. I feltet **Kode** skal du angive en kode, der gør det nemmere at finde i [!INCLUDE[prod_short](../includes/prod_short.md)]. Et navn kan f. eks. vise, hvad et køb sælger, f. eks. "møbler" eller "kaffe", eller det land eller område, det befinder sig i.
4. Angiv den URL-adresse, du vil oprette forbindelse til, i feltet **Shopify URL**. Brug følgende format: `https://{shop}.myshopify.com/`.
5. Slå til/fra-feltet **Aktiveret** til, gennemse og accepter vilkår og betingelser.
6. Hvis du bliver bedt om det, skal du logge på din Shopify-konto. Når du har gennemset beskyttelsen af personlige oplysninger og tilladelser, skal du vælge knappen **Installer app**.

Gentag trin 2-6 for alle onlinebutikker, du vil oprette forbindelse til.

### <a name="known-issues"></a>Kendte problemer

- Pop op-vinduet blokeres i browseren. Når du aktiverer til/fra-funktionen **Aktiveret**, åbner [!INCLUDE [prod_short](../includes/prod_short.md)] siden **Venter på svar - lad være med at lukke siden**, mens den venter på, at der er en adgangstoken fra Shopify. Hvis siden er lukket eller blokeret, kan du ikke oprette forbindelse til Shopify. Få mere at vide på [Anmod om adgangstoken](troubleshoot.md#request-the-access-token)
- Det kan være en god ide at have Shopify-administration åben i samme browser som [!INCLUDE [prod_short](../includes/prod_short.md)]
- [Fejl: Oauth-fejl invalid_request: Kan ikke finde Shopify API-programmet med api_key](troubleshoot.md#error-oauth-error-invalid_request-could-not-find-shopify-api-application-with-api_key)
- [Fejl: Oauth fejl invalid_request: Din konto har ikke tilladelse til at give den ønskede adgang til denne app.](troubleshoot.md#error-oauth-error-invalid_request-your-account-does-not-have-permission-to-grant-the-requested-access-for-this-app)
- [Der kan ikke oprettes forbindelse fra sandkasse](troubleshoot.md#verify-and-enable-permissions-to-make-http-requests-in-a-non-production-environment)

## <a name="next-steps"></a>Næste trin

Nu er din online forretning tilsluttet [!INCLUDE[prod_short](../includes/prod_short.md)]. I de næste trin skal du definere, hvordan og hvad der skal synkroniseres.

- [Synkroniserere elementer](synchronize-items.md)
- [Synkronisere debitorer](synchronize-customers.md)
- [Synkronisere ordrer](synchronize-orders.md)

## <a name="testing-strategies"></a>Teststrategier

Der er forskellige metoder til at teste en integration, og hver enkelt indfaldsvinkel har sine egne medarbejdere og ulemper.

Du kan forbinde kontiene [!INCLUDE[prod_short](../includes/prod_short.md)] og Shopify, så ofte du vil. Shopify-connector påvirker kun miljøet eller er mere præcis den virksomhed, hvor den er aktiveret. Du kan oprette forbindelse til den samme Shopify-onlinebutik fra flere forskellige miljøer eller firmaer. Du kan deaktivere og genaktivere connector.

Det er nemt at køre synkroniseringstest igen. Med connectoren kan du slette importerede data, f. eks. produkter, kunder og ordrer, og derefter importere dem igen. Sørg for at [nulstille synkronisering](troubleshoot.md#reset-sync).

### <a name="shopify-sandbox-and-business-central-sandbox"></a>Shopify-sandkasse og Business central-sandkasse

Det er sandsynligvis den sikreste måde at teste integration på. I stedet for at bruge en Shopify-sandkasse kan du også bruge et prøveabonnement eller udviklingslager. I [!INCLUDE[prod_short](../includes/prod_short.md)] kan du også bruge et testfirma i et produktionsmiljø.

Hvis du vil vide mere om [!INCLUDE[prod_short](../includes/prod_short.md)]-sandkasser, skal du gå til [Oprette et nyt miljø](/dynamics365/business-central/dev-itpro/administration/tenant-admin-center-environments#create-a-new-environment).

### <a name="shopify-sandbox-and-business-central-production"></a>Shopify-sandkasse og Business central-produktion

Det er *ikke* en anbefalet konfigurationen til test, fordi Shopify-connectoren kan oprette eller ændre varer og kunder. Du kan også oprette salgsdokumenter, f. eks. ordrer og fakturaer. Det kan være svært at fortryde disse dokumenter.
 
Hvis du skal bruge denne konfiguration, anbefales det, at du gennemser og deaktiverer følgende indstillinger:

* **Opret automatisk ukendt post** til ikke at oprette elementer
* **Shopify kan opdatere varer**, så tilknyttede varer ikke opdateres
* **Opret automatisk ukendt kunde**, så der ikke oprettes kunder og kontakter
* **Shopify kan opdatere debitorer**, så de eksisterende debitorer ikke opdateres
* **Opret salgsordre automatisk**, så der ikke oprettes salgsordrer og salgsfakturaer

Du kan finde flere oplysninger i [Gendanne et miljø](/dynamics365/business-central/dev-itpro/administration/tenant-admin-center-backup-restore).

### <a name="shopify-production-and-business-central-sandbox"></a>Shopify-produktion og Business central-sandkasse

Det kan være en god idé at sikkerhedskopiere dine data. Du kan f. eks. eksportere produkter og kunder. Du kan finde flere oplysninger i [Bruge CSV-filer til at sikkerhedskopiere lagrede oplysninger](https://help.shopify.com/en/manual/shopify-admin/duplicate-store#using-csv-files-to-back-up-store-information).

Deaktiver **Tillad data synkronisering til Shopify**-til/fra-feltet, så [!INCLUDE[prod_short](../includes/prod_short.md)] ikke skriver til Shopify. I så fald kan du indlæse produkter, billeder, kunder og ordrer fra Shopify. Men du kan ikke sende varer, priser, lagerniveauer, debitorer, indfrielses oplysninger til Shopify.

Hvis indstillingen **Tillad datasynkronisering til Shopify**-til/fra-feltet er aktiveret, er der følgende beskyttelsesforanstaltninger:

*   Vælg **Kladde** i feltet **Status for Opret produkt** for at sikre, at de udlæste produkter ikke er disponible til købere. Du kan kontrollere, hvordan produkter ser ud i onlinebutikken, synkronisere priser, indstillinger og lagerniveauer. Du skal blot sørge for at bruge filtre på siden **Tilføj elementet til Shopify** for at begrænse antallet af udlæste varer.
* Deaktiver til/fra-feltet **eksporter kunde til Shopify**, så du ikke sender kunderne til Shopify.

## <a name="see-also"></a>Se også

[Gennemgang: oprette og bruge Shopify Connector](walkthrough-setting-up-and-using-shopify.md)  

