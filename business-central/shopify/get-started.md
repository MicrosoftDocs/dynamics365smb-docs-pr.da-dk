---
title: Kom i gang med Connector til Shopify
description: Første trin ved konfiguration af forbindelser mellem Business central og Shopify
ms.date: 05/27/2022
ms.topic: article
ms.service: dynamics365-business-central
ms.reviewer: solsen
ms.search.form: 30100, 30101, 30102, 30103, 30104, 30135,
author: AndreiPanko
ms.author: andreipa
ms.openlocfilehash: b79691660ca84309057c3abab3d3a3df47271f58
ms.sourcegitcommit: 5bb13966e9ba8d7a3c2f00dd32f167acccf90b82
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 10/28/2022
ms.locfileid: "9728406"
---
# <a name="get-started-with-the-shopify-connector"></a>Kom i gang med Shopify Connector

Forbind din Shopify-butik (eller butikker) med [!INCLUDE [prod_short](../includes/prod_short.md)], og maksimer produktiviteten. Administrere og få vist indsigter fra din virksomhed og din Shopify-butik som én enhed.

Shopify-connectoren indeholder følgende egenskaber:

- Support til mere end én Shopify-butik
  - Hvert køb har sin egen opsætning, herunder en samling produkter, lokationer, der bruges til at beregne lager, og prislister.  
- Tovejs synkronisering af varer eller produkter.
  - Connectoren synkroniserer billeder, varevarianter, stregkoder, leverandørs varenumre, udvidede tekster og koder.  
  - Eksporte vareattributter til Shopify.  
  - Brug de valgte debitorprisgrupper og rabatter til at definere de priser, der skal udlæses til Shopify.  
  - Beslut, om du kan oprette varer automatisk eller kun tillade opdateringer af eksisterende produkter.  
- Lagerniveausynkronisering.
  - Vælge nogle eller alle tilgængelige placeringer i [!INCLUDE [prod_short](../includes/prod_short.md)].  
  - Opdater lagerniveauer på flere lokationer i Shopify.  
- Tovejs synkronisering af kunder.
  - Med chipkort-kunder pr. telefon og pr. e-mail.  
  - Brug landespecifikke skabeloner, når du opretter debitorer, som er med til at sikre, at skatte indstillingerne er korrekte.  
- Importer ordrer fra Shopify.
  - Under indlæsningen kan du automatisk oprette debitorer i [!INCLUDE [prod_short](../includes/prod_short.md)] eller bestemme, om debitorerne Shopify skal administreres.  
  - Medtage ordrer, der er oprettet i andre kanaler, f. eks Shopify POS eller Amazon.  
  - Forsendelsesomkostninger, gavekort, tip, leverings-og betalingsmetoder, transaktioner og risiko for svig.  
  - Modtage betalingsoplysninger fra Shopify Payments.  
- Spore indfrielsesoplysninger.
  - Du kan vælge at overføre oplysninger om varesporing fra [!INCLUDE [prod_short](../includes/prod_short.md)] til Shopify.  

Hvis du vil bruge Shopify med [!INCLUDE [prod_short](../includes/prod_short.md)], skal du gøre følgende først. Denne artikel fungerer som en vejledning for at integrere din Shopify-butik med [!INCLUDE [prod_short](../includes/prod_short.md)].

## <a name="prerequisites-for-shopify"></a>Forudsætninger Shopify

Du skal have:

- En Shopify-konto.
- En Shopify-onlinebutik.

Hvis du vil oprette en ny Shopify-konto eller tilmelde di en gratis 14-dages prøveversion, skal du gå til [Shopify.com](https://www.shopify.com/). Du kan finde flere oplysninger om, hvordan du opretter og tilpasser onlinebutikken, i [Shopify Hjælp-center](https://help.shopify.com/).
  
Andre salgskanaler understøttes f.eks. Shopify POS.

### <a name="recommended-settings"></a>Anbefalede indstillinger

- Deaktiver **Automatisk arkivering af ordren** i sektionen **Ordrebehandling** under indstillingerne [**Tjek ud**](https://www.shopify.com/admin/settings/checkout) i din **Shopify-administrator**.

Flere oplysninger om Shopify-indstillinger for demo-og prøvescenarier på [Test-og uddannelsesscenarier](/dynamics365/business-central/dev-itpro/administration/admin-shopify-connector#preparation).

## <a name="prerequisites-for-business-central"></a>Forudsætninger for Business Central

- Kontroller først, at **[Shopify Connector](https://go.microsoft.com/fwlink/?linkid=2196238)**-appen er installeret.

Appen er forudinstalleret for alle nye logon-vinduer og forsøg. Få mere at vide om at installere apps fra AppSource på [installere og af-installere udvidelser](../ui-extensions-install-uninstall.md#install). Følg de trin, der er angivet nedenfor, hvis du ikke har [!INCLUDE[prod_short](../includes/prod_short.md)].

## <a name="install-the-dynamics-365-business-central-app-to-your-shopify-online-store"></a>Installere Dynamics 365 Business Central-app'en i din Shopify-onlinebutik

For eksisterende [!INCLUDE[prod_short](../includes/prod_short.md)] er dette trin valgfrit og kan springes over.

1. Find [Dynamics 365 Business Central](https://apps.shopify.com/dynamics-365-business-central)-appen på [Shopify AppStore](https://apps.shopify.com/)
2. Vælg knappen **Tilføj app**. Hvis du bliver bedt om det, skal du logge på din Shopify-konto. Vælg den ønskede online-butik, hvis du har flere.
3. Når du har gennemset beskyttelsen af personlige oplysninger og tilladelser, skal du vælge knappen **Installer app**.

   Du kan finde og åbne den installerede **Dynamics 365 Business Central**-app i afsnittet **Apps** på sidepanelet på siden **Shopify admin**.
4. Vælg **Tilmeld dig nu** for at starte [!INCLUDE[prod_short](../includes/prod_short.md)]-prøveversionen, eller **Log på**, hvis du allerede har [!INCLUDE[prod_short](../includes/prod_short.md)]. Du bliver omdirigeret til din side [Business Central](https://businesscentral.dynamics.com).
5. De næste trin i udføres i [!INCLUDE[prod_short](../includes/prod_short.md)].

## <a name="connect-business-central-to-the-shopify-online-store"></a>Forbinde Business central med Shopify-onlinebutikken

1. Vælg ![Lightbulb, der åbner funktionen Fortæl mig.](../media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **Shopify Butik**, og vælg det relevante link.
2. Vælg handlingen **Ny**.  
3. I feltet **Kode** skal du angive den kode, der gør det nemmere at finde i [!INCLUDE[prod_short](../includes/prod_short.md)]. Et navn kan f. eks. vise, hvad et køb sælger, f. eks. "møbler" eller "kaffe", eller det land eller område, det befinder sig i.
4. I feltet **Shopify URL-adresse** skal du angive URL-adressen til dit onlineindkøb, der skal være tilsluttet. Brug følgende format: `https://{shop}.myshopify.com/`.
5. Slå til/fra-feltet **Aktiveret** til, gennemse og accepter vilkår og betingelser.
6. Hvis du bliver bedt om det, skal du logge ind på din Shopify-konto, gennemse personlige oplysninger og tilladelser og derefter vælge knappen **Installer app**.

Gentag trin 2-6 for alle onlinebutikker, du vil oprette forbindelse til.

> [!NOTE]
> Kontroller, at browseren ikke blokerer pop op-vinduer. Når du aktiverer skift til/fra-systemet **Aktiveret**, åbnes siden **Venter på svar-Luk ikke denne side**, som venter på et adgangstoken fra Shopify, hvis siden er lukket eller blokeret - du kan ikke oprette forbindelse til Shopify. Få mere at vide på [Anmod om adgangstoken](troubleshoot.md#request-the-access-token)

### <a name="next-steps"></a>Næste trin

Nu er din online forretning tilsluttet [!INCLUDE[prod_short](../includes/prod_short.md)]. I de næste trin skal du definere, hvordan og hvad der skal synkroniseres.

- [Synkroniserere elementer](synchronize-items.md)
- [Synkronisere debitorer](synchronize-customers.md)
- [Synkronisere ordrer](synchronize-orders.md)

## <a name="see-also"></a>Se også

[Test-og Trænings scenarier](/dynamics365/business-central/dev-itpro/administration/admin-shopify-connector).
