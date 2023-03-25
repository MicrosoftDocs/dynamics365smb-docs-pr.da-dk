---
title: Kom i gang med Connector til Shopify
description: Første trin ved konfiguration af forbindelser mellem Business central og Shopify
ms.date: 05/27/2022
ms.topic: article
ms.service: dynamics365-business-central
ms.reviewer: solsen
ms.search.form: '30100, 30101, 30102, 30103, 30104, 30135,'
author: AndreiPanko
ms.author: andreipa
---

# Kom i gang med Shopify Connector

Forbind din Shopify-butik (eller butikker) med [!INCLUDE [prod_short](../includes/prod_short.md)], og maksimer produktiviteten. Administrere og få vist indsigter fra din virksomhed og din Shopify-butik som én enhed.

Hvis du vil bruge Shopify med [!INCLUDE [prod_short](../includes/prod_short.md)], skal du gøre følgende først. Denne artikel fungerer som en vejledning for at integrere din Shopify-butik med [!INCLUDE [prod_short](../includes/prod_short.md)].

## Forudsætninger Shopify

Du skal have:

- En Shopify-konto
- En Shopify-onlinebutik

Du kan finde flere oplysninger om, hvordan du opretter Shopify-forsøg og anbefalede indstillinger, ved at gå til [Oprette og konfigurere Shopify-konto](shopify-account.md).

## Forudsætninger for Business Central

- Kontroller først, at **[Shopify Connector](https://go.microsoft.com/fwlink/?linkid=2196238)**-appen er installeret.

  Appen er forudinstalleret for alle nye logon-vinduer og forsøg. Få mere at vide om at installere apps fra AppSource på [installere og af-installere udvidelser](../ui-extensions-install-uninstall.md#install). Følg de trin, der er angivet nedenfor, hvis du ikke har [!INCLUDE[prod_short](../includes/prod_short.md)].

- Kontroller, at brugeren har tilstrækkelige tilladelser. Shopify Connector er dækket af *Shopify – admin (SHPFY – admin)*-rettighedssæt. Du kan finde flere oplysninger i [Oprette brugere i henhold til licenser](../ui-how-users-permissions.md) og [Tildele tilladelser til brugere og grupper](../ui-define-granular-permissions.md)


## Installere Dynamics 365 Business Central-app'en i din Shopify-onlinebutik

For eksisterende [!INCLUDE[prod_short](../includes/prod_short.md)] er dette trin valgfrit og kan springes over.

1. Find [Dynamics 365 Business Central](https://apps.shopify.com/dynamics-365-business-central)-appen på [Shopify AppStore](https://apps.shopify.com/)
2. Vælg knappen **Tilføj app**. Hvis du bliver bedt om det, skal du logge på din Shopify-konto. Vælg den ønskede online-butik, hvis du har flere.
3. Når du har gennemset beskyttelsen af personlige oplysninger og tilladelser, skal du vælge knappen **Installer app**.

   Du kan finde og åbne den installerede **Dynamics 365 Business Central**-app i afsnittet **Apps** på sidepanelet på siden **Shopify admin**.
4. Vælg **Tilmeld dig nu** for at starte [!INCLUDE[prod_short](../includes/prod_short.md)]-prøveversionen, eller **Log på**, hvis du allerede har [!INCLUDE[prod_short](../includes/prod_short.md)]. Du bliver omdirigeret til din side [Business Central](https://businesscentral.dynamics.com).
5. De næste trin i udføres i [!INCLUDE[prod_short](../includes/prod_short.md)].

## Forbinde Business central med Shopify-onlinebutikken

1. Vælg ![Lightbulb, der åbner funktionen Fortæl mig.](../media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **Shopify Butik**, og vælg det relevante link.
2. Vælg handlingen **Ny**.  
3. I feltet **Kode** skal du angive den kode, der gør det nemmere at finde i [!INCLUDE[prod_short](../includes/prod_short.md)]. Et navn kan f. eks. vise, hvad et køb sælger, f. eks. "møbler" eller "kaffe", eller det land eller område, det befinder sig i.
4. I feltet **Shopify URL-adresse** skal du angive URL-adressen til dit onlineindkøb, der skal være tilsluttet. Brug følgende format: `https://{shop}.myshopify.com/`.
5. Slå til/fra-feltet **Aktiveret** til, gennemse og accepter vilkår og betingelser.
6. Hvis du bliver bedt om det, skal du logge ind på din Shopify-konto, gennemse personlige oplysninger og tilladelser og derefter vælge knappen **Installer app**.

Gentag trin 2-6 for alle onlinebutikker, du vil oprette forbindelse til.

### Kendte problemer

- Pop op-vinduet blokeres i browseren. Når du aktiverer skift til/fra-systemet **Aktiveret**, åbnes siden **Venter på svar-Luk ikke denne side**, som venter på et adgangstoken fra Shopify, hvis siden er lukket eller blokeret - du kan ikke oprette forbindelse til Shopify. Få mere at vide på [Anmod om adgangstoken](troubleshoot.md#request-the-access-token)
- [Oauth-fejl invalid_request: Kan ikke finde Shopify API-programmet med api_key](troubleshoot.md#oauth-error-invalid_request-could-not-find-shopify-api-application-with-api_key)
- [Der kan ikke oprettes forbindelse fra sandkasse](troubleshoot.md#verify-and-enable-permissions-to-make-http-requests-when-running-in-a-non-production-environment)


## Næste trin

Nu er din online forretning tilsluttet [!INCLUDE[prod_short](../includes/prod_short.md)]. I de næste trin skal du definere, hvordan og hvad der skal synkroniseres.

- [Synkroniserere elementer](synchronize-items.md)
- [Synkronisere debitorer](synchronize-customers.md)
- [Synkronisere ordrer](synchronize-orders.md)

## Se også

[Gennemgang: oprette og bruge Shopify Connector](walkthrough-setting-up-and-using-shopify.md)  

