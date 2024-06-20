---
title: Konfigurere elektronisk fakturering i NemHandel
description: 'Få mere at vide om, hvordan du konfigurerer funktionaliteten for NemHandel i Danmark.'
author: altotovi
ms.topic: conceptual
ms.devlang: al
ms.search.keywords: 'electronic document, electronic invoice, e-document, e-invoice, access-point, endpoint, nemhandel, denmark, dk'
ms.search.form: '359, 360, 6103, 6133'
ms.date: 12/13/2023
ms.author: altotovi
ms.service: dynamics-365-business-central
ms.reviewer: bholtorf
---

# <a name="set-up-electronic-invoicing-with-nemhandel"></a>Konfigurere elektronisk fakturering i NemHandel

I Danmark kan du konfigurere dit e-fakturasystem til at fungere med NemHandel ved at bruge tredjeparts certificerede adgangspunkter. Før du begynder, skal du læse om, hvordan du kan [bruge e-dokumenter med eksterne tjenester](../../finance-how-setup-edocuments-external.md), og lav en kontrakt med en af ​​de understøttede eksterne certificerede adgangspunktudbydere.

Før du starter opsætningen, skal du åbne **Udvidelsesstyring**-siden, og kontroller, at følgende apps er installeret:

- E-dokumentkerne
- E-Documents Connector med eksterne endepunkter
- OIOUBL
- E-dokumentformat for OIOUBL

I Dansk E-Dokumenter funktionalitet kan du vælge OIOUBL og PEPPOL BIS 3 som dokumentformater i **E-dokumenttjenester**.

## <a name="e-document-services-setup"></a>E-dokumenttjenester-opsætning

Hvis du vil konfigurere services, skal du udføre følgende trin:

1. Vælg ![Lightbulb, der åbner funktionen Fortæl mig.](../../media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **e-dokumenttjeneste**, og vælg derefter det relaterede link.
2. Vælg **Ny** for at oprette OIOUBL-tjenesten.
3. Udfyld alle data som forklaret i [Indstil E-Documents-stikket med eksterne endepunkter](../../finance-how-setup-edocuments-external.md).
4. I **Dokumentformat**-feltet skal du vælge **OIOUBL** som eksportformat for den elektroniske eksportopsætning.
5. I **Serviceintegration** skal du angive det serviceadgangspunkt, du vil bruge.
6. Vælg **Setup Service Integration**, og følg instruktionerne for [brug af E-Documents Connector med eksterne endepunkter](../../finance-how-setup-edocuments-external.md). Luk derefter siden.
7. Vælg **Ny** for at oprette PEPPOL-tjenesten.
8. Udfyld alle data som forklaret i [Indstil E-Documents-stikket med eksterne endepunkter](../../finance-how-setup-edocuments-external.md).
9. I **Dokumentformat**-feltet skal du vælge **PEPPOL BIS 3.0** som eksportformat for den elektroniske eksportopsætning.
10. I **Serviceintegration** skal du angive det serviceadgangspunkt, du vil bruge.
11. Vælg **Setup Service Integration**, og følg instruktionerne for [brug af E-Documents Connector med eksterne endepunkter](../../finance-how-setup-edocuments-external.md). Luk derefter siden.

> [!NOTE]
> Denne forbindelse kræver kommunikation med eksterne tjenesteudbydere, der kan være genstand for yderligere betaling og kræver kontrakter med dem. Kontakt tjenesteudbyderne for at få alle de nødvendige legitimationsoplysninger.

For at konfigurere arbejdsgange, kunder og leverandører, se [Sådan konfigureres E-Documents](../../finance-how-setup-edocuments.md) og [Indstil E-Documents-forbindelsen med eksterne slutpunkter](../../finance-how-setup-edocuments-external.md).

## <a name="see-also"></a>Se også

[Lokal funktionalitet for Danmark](denmark-local-functionality.md)  
[Sådan konfigureres e-dokumenter i Business Central](../../finance-how-setup-edocuments.md)  
[Sådan bruges e-dokumenter i Business Central](../../finance-how-use-edocuments.md)  
[Sådan udvides e-dokumenter i Business Central](/dynamics365/business-central/dev-itpro/developer/devenv-extend-edocuments)  
[Fakturasalg](../../sales-how-invoice-sales.md)  
[Registrere køb med købsfakturaer og ordrer](../../purchasing-how-record-purchases.md)  
[Arbejde med Business Central](../../ui-work-product.md)

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
