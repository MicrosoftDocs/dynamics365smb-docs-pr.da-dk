---
title: Oprette og konfigurere Shopify-konto
description: 'Få mere at vide om, hvordan du får en Shopify-konto, så du kan demonstrere arbejdsgangen for integrering af Shopify og Business central.'
ms.date: 06/21/2022
ms.topic: article
ms.service: dynamics365-business-central
ms.search.form: '30101, 30102'
ms.reviewer: solsen
author: AndreiPanko
ms.author: andreipa
---

# <a name="create-and-set-up-a-shopify-account"></a>Oprette og konfigurere Shopify-konto

Hvis du overvejer, om du skal bruge Shopify som e-handelsløsning og har brug for en Shopify-konto til at validere integreret arbejdsgang, har du følgende muligheder:

- Få en prøveversion. Dette er det typiske udgangspunkt for slutbrugere.  
- Oprette udviklingsbutikker. Denne fremgangsmåde gælder for partnere, som har brug for gentagende demoer, kurser og yder support.

## <a name="trial-end-user"></a>Prøveversion (slutbruger)

Gå til [Shopify-webstedet](https://www.shopify.com), og brug din mailkonto til administratorkontoen for at tilmelde dig og få en gratis prøveversion. Du kan finde flere oplysninger om, hvordan du opretter og tilpasser onlinebutikken, i [Shopify Hjælp-center](https://help.shopify.com/).

I **Shopify Administration** til den oprettede butik skal du anvende følgende **Indstillinger**:

- Deaktiver **Automatisk arkivering af ordren** i sektionen **Ordrebehandling** under indstillingerne [**Tjek ud**](https://www.shopify.com/admin/settings/checkout) i din **Shopify-administrator**.
- Overvej at aktivere linket *Vis logon i butiksfacade og ved kassen* i sektionen **Kundekontoindstillinger** i indstillingerne for udlevering.
- Overvej at vælge indstillingen *Firmanavn - valgfri* i sektionen **Kundeoplysninger** under indstillingerne for udlevering.
- Aktiver indstillingen **Vis indstillinger for udlevering ved kassen** i sektionen **Drikkepenge** ved udgangskassen, hvis du vil give drikkepenge.
- Aktiver testbetalinger. Du har to muligheder. Start med at gå til [**Betalinger**](https://www.shopify.com/admin/settings/payments)-indstillinger:  
  1. *(til test) Bogus Gateway*. Du kan finde flere oplysninger i [Aktivering af Bogus Gateway til test](https://help.shopify.com/en/manual/checkout-settings/test-orders#place-a-test-order-by-simulating-a-transaction).
  2. *Shopify payments* i testtilstand. Du kan finde flere oplysninger i [Teste Shopify Payments](https://help.shopify.com/en/manual/payments/shopify-payments/testing-shopify-payments).

- Vælg en plan i [**Plan**](https://www.shopify.com/admin/settings/plan) indstillingerne, der skal kunne afprøve processen til betaling ved kassen.

> [!Important]  
> Hvis du vil undgå betalinger, skal du huske at annullere din Shopify-prøveversion.

## <a name="development-store"></a>Udviklingsbutik

Begynd at deltage i [Shopify Partner-programmet](https://help.shopify.com/partners/about). Derefter skal du bruge **Partner-dashboardet** til at oprette udviklingsbutikken. Flere oplysninger i [Oprette udviklingsbutikker](https://help.shopify.com/partners/dashboard/managing-stores/development-stores).

Efter oprettelse af butikken i **Shopify Administration** til den oprettede butik skal du anvende følgende **Indstillinger**:

- Deaktiver **Automatisk arkivering af ordren** i sektionen **Ordrebehandling** under indstillingerne [**Tjek ud**](https://www.shopify.com/admin/settings/checkout) i din **Shopify-administrator**.
- Overvej at aktivere linket *Vis logon i butiksfacade og ved kassen* i sektionen **Kundekontoindstillinger** i indstillingerne for udlevering.
- Overvej at vælge indstillingen *Firmanavn - valgfri* i sektionen **Kundeoplysninger** under indstillingerne for udlevering.
- Hvis du vil give drikkepenge, skal du aktivere indstillingen **Vis indstillinger for udlevering ved kassen** i sektionen **Drikkepenge** ved udgangskassen.
- Aktiver testbetalinger. Du har to muligheder. Start med at gå til [**Betalinger**](https://www.shopify.com/admin/settings/payments)-indstillinger:  
  1. *(til test) Bogus Gateway*. Du kan finde flere oplysninger i [Aktivering af Bogus Gateway til test](https://help.shopify.com/en/manual/checkout-settings/test-orders#place-a-test-order-by-simulating-a-transaction).
  2. *Shopify payments* i testtilstand. Flere oplysninger i [Test af Shopify Payments](https://help.shopify.com/en/manual/payments/shopify-payments/testing-shopify-payments).

> [!Note]  
> Udviklingslagre er normalt beskyttet med adgangskode. Når du forsøger at åbne en bestemt side i din onlinebutik fra [!INCLUDE [prod_short](../includes/prod_short.md)], f.eks. for at gå til et bestemt produkt eller en bestemt ordre, skal du angive din adgangskode. Mens du tester, skal du logge på din Shopify-administrator og åbne dit lager derfra for at undgå at skulle angive adgangskoden. Du behøver ikke at angive lageradgangskoden, før du lukker browseren, eller hvis din session udløber.  

## <a name="see-also"></a>Se også

[Kom i gang med Shopify-connectoren](get-started.md)  
[Gennemgang: oprette og bruge Shopify Connector](walkthrough-setting-up-and-using-shopify.md)
