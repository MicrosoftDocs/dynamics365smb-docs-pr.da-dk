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
ms.openlocfilehash: e59dd0dcf757fbcf76d4068756adfe7bc9475f54
ms.sourcegitcommit: 38b1272947f64a473de910fe81ad97db5213e6c3
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 08/29/2022
ms.locfileid: "9361551"
---
# <a name="get-started-with-the-shopify-connector"></a>Kom i gang med Shopify Connector

Forbind din Shopify-butik (eller butikker) med [!INCLUDE [prod_short](../includes/prod_short.md)], og maksimer produktiviteten. Administrere og få vist indsigter fra din virksomhed og din Shopify-butik som én enhed. 

Shopify-connectoren indeholder følgende egenskaber:

- Support til mere end én Shopify-butik  

  - Hvert køb har sin egen opsætning, herunder en samling produkter, lokationer, der bruges til at beregne lager, og prislister.  
- Tovejs synkronisering af varer eller produkter  

  - Connectoren synkroniserer billeder, varevarianter, stregkoder, leverandørs varenumre, udvidede tekster og koder.  
  -    Eksporte vareattributter til Shopify.  
  -    Brug de valgte debitorprisgrupper og rabatter til at definere de priser, der skal udlæses til Shopify.  
  -    Beslut, om du kan oprette varer automatisk eller kun tillade opdateringer af eksisterende produkter.  
- Lagerniveausynkronisering  

  -    Vælge nogle eller alle tilgængelige placeringer i [!INCLUDE [prod_short](../includes/prod_short.md)].  
  -    Opdater lagerniveauer på flere lokationer i Shopify.  
- Tovejs synkronisering af kunder  

  -    Med chipkort-kunder pr. telefon og pr. e-mail.  
  -    Brug landespecifikke skabeloner, når du opretter debitorer, som er med til at sikre, at skatte indstillingerne er korrekte.  
- Importer ordrer fra Shopify  

  -    Under indlæsningen kan du automatisk oprette debitorer i [!INCLUDE [prod_short](../includes/prod_short.md)] eller bestemme, om debitorerne Shopify skal administreres.  
  -    Medtage ordrer, der er oprettet i andre kanaler, f. eks Shopify POS eller Amazon.  
  -    Forsendelsesomkostninger, gavekort, tip, leverings-og betalingsmetoder, transaktioner og risiko for svig.  
  - Modtage betalingsoplysninger fra Shopify Payments.  
- Nem sporing af indfrielsesoplysninger  

  -    Du kan vælge at skrive oplysninger om varesporing fra [!INCLUDE [prod_short](../includes/prod_short.md)] til Shopify.  

Hvis du vil bruge Shopify med [!INCLUDE [prod_short](../includes/prod_short.md)], skal du gøre følgende først. Denne artikel fungerer som en vejledning for at fuldføre integrationen af din Shopify-butik med [!INCLUDE [prod_short](../includes/prod_short.md)].

## <a name="prerequisites-for-shopify"></a>Forudsætninger Shopify

Du skal have:

- En Shopify-konto
- En Shopify-onlinebutik

Hvis du vil oprette en ny Shopify-konto eller tilmelde di en gratis 14-dages prøveversion, skal du gå til [Shopify](https://www.shopify.com/). Du kan finde flere oplysninger om, hvordan du opretter og tilpasser onlinebutikken, i [Shopify Hjælp-center](https://help.shopify.com/).
  
Andre salgskanaler understøttes f.eks. Shopify POS.

### <a name="recommended-settings"></a>Anbefalede indstillinger

- Deaktiver **Automatisk arkivering af ordren** i sektionen **Ordrebehandling** under indstillingerne [**Tjek ud**](https://www.shopify.com/admin/settings/checkout) i din **Shopify-administrator**.

Hvis du vil vide mere om Shopify-indstillinger for demo-og prøvescenarier, skal du se [Test-og uddannelsesscenarier](/dynamics365/business-central/dev-itpro/administration/admin-shopify-connector#preparation).

## <a name="prerequisites-for-business-central"></a>Forudsætninger for Business Central

- Kontroller først, at **[Shopify Connector](https://go.microsoft.com/fwlink/?linkid=2196238)**-appen er installeret.

Appen er forudinstalleret for alle nye logon-vinduer og forsøg. Få mere at vide om at installere apps fra markedsstedet på [installation og af-installation af udvidelser](../ui-extensions-install-uninstall.md#install). Følg de trin, der er angivet nedenfor, hvis du ikke har [!INCLUDE[prod_short](../includes/prod_short.md)].

## <a name="installing-the-dynamics-365-business-central-app-to-your-shopify-online-store"></a>Installation af **Dynamics 365 Business Central**-app'en i din Shopify-onlinebutik

For eksisterende [!INCLUDE[prod_short](../includes/prod_short.md)] er dette trin valgfrit og kan springes over.

1. Find [Dynamics 365 Business Central](https://apps.shopify.com/dynamics-365-business-central)-appen på [Shopify AppStore](https://apps.shopify.com/)
2. Vælg knappen **Tilføj app**. Log på din Shopify-konto, hvis du bliver bedt om det. Vælg den ønskede online-butik, hvis du har flere.
3. Når du har gennemset beskyttelsen af personlige oplysninger og tilladelser, skal du vælge knappen **Installer app**.
  Du kan finde og åbne den installerede **Dynamics 365 Business Central**-app i afsnittet **Apps** på sidepanelet i **Shopify admin**.
4. Vælg **Tilmeld dig nu** for at starte [!INCLUDE[prod_short](../includes/prod_short.md)]-prøveversionen, eller **Log på**, hvis du allerede har [!INCLUDE[prod_short](../includes/prod_short.md)]. Du bliver omdirigeret til din [!INCLUDE[prod_short](../includes/prod_short.md)] på [Business Central](https://businesscentral.dynamics.com).
5. De næste trin i udføres i [!INCLUDE[prod_short](../includes/prod_short.md)].

## <a name="connecting-business-central-to-the-shopify-online-store"></a>Forbinde Business central med Shopify-onlinebutikken

1. Gå til søgning ![Lightbulb, der åbner funktionen Fortæl mig.](../media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **Shopify Butik**, og vælg det relevante link.
2. Vælg handlingen **Ny**.  
3. Angiv den ønskede kode i feltet **Kode**.  
4. I feltet **Shopify URL-adresse** skal du skrive URL-adressen til dit onlineindkøb, der skal være tilsluttet. Brug følgende format: `https://{shop}.myshopify.com/`.
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

