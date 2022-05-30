---
title: Kom i gang med Connector til Shopify
description: Første trin ved konfiguration af forbindelser mellem Business central og Shopify
ms.date: 05/16/2022
ms.topic: article
ms.service: dynamics365-business-central
ms.reviewer: solsen
author: AndreiPanko
ms.author: andreipa
ms.openlocfilehash: 2b88995cad8cfe0c3688ca062643f2d339fed9bf
ms.sourcegitcommit: f071aef3660cc3202006e00f2f790faff849a240
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 05/18/2022
ms.locfileid: "8768108"
---
# <a name="get-started-with-the-shopify-connector"></a>Kom i gang med Shopify Connector

[!INCLUDE [prod_short](../includes/prod_short.md)] giver dig mulighed for at tilslutte din Shopify-butik (eller butikker) med henblik på at maksimere produktiviteten. Du kan administrere og få vist indblik fra din virksomhed og din Shopify-onlinebutik som én enhed ved at bruge Shopify-connectoren. Hvis du vil bruge den sammen Shopify med [!INCLUDE [prod_short](../includes/prod_short.md)], skal du udføre nogle trin. Denne side fungerer som en vejledning for at fuldføre integrationen af din Shopify butik med [!INCLUDE [prod_short](../includes/prod_short.md)].

## <a name="prerequisites-for-shopify"></a>Forudsætninger Shopify

Du skal have:

- En Shopify-konto
- En Shopify-onlinebutik

Hvis du vil oprette en ny Shopify-konto eller tilmelde di en gratis 14-dages prøveversion, skal du gå til [Shopify](https://www.shopify.com/). Du kan finde flere oplysninger om, hvordan du opretter og tilpasser onlinebutikken, i [Shopify Hjælp-center](https://help.shopify.com/).
  
- Andre salgskanaler understøttes f.eks. Shopify POS.

### <a name="recommended-settings"></a>Anbefalede indstillinger

- Deaktiver **Automatisk arkivering af ordren** i sektionen **Ordrebehandling** under indstillingerne [**Tjek ud**](https://www.shopify.com/admin/settings/checkout) i din **Shopify-administrator**.

Hvis du vil vide mere om Shopify-indstillinger for demo-og prøvescenarier, skal du se [Test-og uddannelsesscenarier](/dynamics365/business-central/dev-itpro/administration/admin-shopify-connector#preparation).

## <a name="prerequisites-for-business-central"></a>Forudsætninger for Business Central

- Kontroller først, at udvidelsen **Forbind til Shopify for [!INCLUDE[prod_short](../includes/prod_short.md)]** er installeret.

Udvidelsen er forudinstalleret for alle nye logon-vinduer og forsøg. Hvis du skal installere udvidelser fra markedsstedet, skal du gå til [installation og fjernelse af udvidelser](../ui-extensions-install-uninstall.md#install). Følg de trin, der er angivet nedenfor, hvis du ikke har [!INCLUDE[prod_short](../includes/prod_short.md)].
<!--
## Installing the **Dynamics 365 Business Central** app to your Shopify online store

For existing [!INCLUDE[prod_short](../includes/prod_short.md)], this step is optional and can be skipped.

1. Locate the [Dynamics 365 Business Central](https://apps.shopify.com/dynamics-365-business-central) app on the [Shopify AppStore](https://apps.shopify.com/)
2. Choose the **Add App** button. Sign-in into your Shopify account if prompted. Select the required online shop if you've more than one.
3. After reviewing privacy and permissions, choose the **Install App** button.
  You can find and open the installed **Dynamics 365 Business Central** app in the **Apps** section on the sidebar of **Shopify admin**.
4. Choose **Sign up now** to start [!INCLUDE[prod_short](../includes/prod_short.md)] trial or **Sign in** if you already have [!INCLUDE[prod_short](../includes/prod_short.md)]. You'll be redirected to your [!INCLUDE[prod_short](../includes/prod_short.md)] at [Business Central](https://businesscentral.dynamics.com).
5. The next steps should be done in [!INCLUDE[prod_short](../includes/prod_short.md)].
-->
## <a name="connecting-business-central-to-the-shopify-online-store"></a>Forbinde Business central med Shopify-onlinebutikken

1. Gå til søgning ![Lightbulb, der åbner funktionen Fortæl mig.](../media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **Shopify Butik**, og vælg det relevante link.
2. Vælg handlingen **Ny**.  
3. Angiv den ønskede kode i feltet **Kode**.  
4. I feltet **Shopify URL-adresse** skal du skrive URL-adressen til dit onlineindkøb, der skal være tilsluttet.
5. Slå til/fra-feltet **Aktiveret** til, gennemse og accepter vilkår og betingelser.
6. Hvis du bliver bedt om det, skal du logge ind på din Shopify-konto, gennemse personlige oplysninger og tilladelser og derefter vælge knappen **Installer app**.

Gentag trin 2-6 for alle onlinebutikker, du vil oprette forbindelse til.

### <a name="next-steps"></a>Næste trin

Nu er din online forretning tilsluttet [!INCLUDE[prod_short](../includes/prod_short.md)]. I de næste trin skal du definere, hvordan og hvad der skal synkroniseres.

- [Synkroniserere elementer](synchronize-items.md)
- [Synkronisere debitorer](synchronize-customers.md)
- [Synkronisere ordrer](synchronize-orders.md)

## <a name="see-also"></a>Se også

[Test-og Trænings scenarier](/dynamics365/business-central/dev-itpro/administration/admin-shopify-connector).

