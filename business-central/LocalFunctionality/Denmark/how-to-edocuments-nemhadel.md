---
title: Konfigurere elektronisk fakturering i NemHandel
description: 'Få mere at vide om, hvordan du konfigurerer funktionaliteten for NemHandel i Danmark.'
author: altotovi
ms.topic: conceptual
ms.devlang: al
ms.search.keywords: 'electronic document, electronic invoice, e-document, e-invoice, access-point, endpoint, nemhandel, denmark, dk'
ms.search.form: '359, 360, 6103, 6133'
ms.date: 07/10/2024
ms.author: altotovi
ms.service: dynamics-365-business-central
ms.reviewer: bholtorf
---

# Konfigurere elektronisk fakturering i NemHandel

I Danmark kan du konfigurere dit e-fakturasystem til at fungere med NemHandel ved at bruge tredjeparts certificerede adgangspunkter. Før du begynder, skal du læse om, hvordan du kan [bruge e-dokumenter med eksterne tjenester](../../finance-how-setup-edocuments-external.md), og lav en kontrakt med en af ​​de understøttede eksterne certificerede adgangspunktudbydere.

Før du starter opsætningen, skal du åbne **Udvidelsesstyring**-siden, og kontroller, at følgende apps er installeret:

- E-dokumentkerne
- E-Documents Connector med eksterne endepunkter
- OIOUBL
- E-dokumentformat for OIOUBL

I Dansk E-Dokumenter funktionalitet kan du vælge OIOUBL og PEPPOL BIS 3 som dokumentformater i **E-dokumenttjenester**.

## E-dokumenttjenester-opsætning

> [!NOTE]
> For at etablere disse forbindelser er det nødvendigt at kommunikere med eksterne tjenesteudbydere, som kan kræve yderligere betaling og kontrakter. Kontakt tjenesteudbyderne for at få alle de nødvendige legitimationsoplysninger.

Hvis du vil konfigurere services, skal du udføre følgende trin:   

### Sådan bruges OIOUBL-format  

1. Vælg ![Lightbulb, der åbner funktionen Fortæl mig.](../../media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **e-dokumenttjeneste**, og vælg derefter det relaterede link.
2. Vælg **Ny** for at oprette OIOUBL-tjenesten.
3. Udfyld alle data som forklaret i [Indstil E-Documents-stikket med eksterne endepunkter](../../finance-how-setup-edocuments-external.md).
4. I **Dokumentformat**-feltet skal du vælge **OIOUBL** som eksportformat for den elektroniske eksportopsætning.
5. I **Serviceintegration** skal du angive det serviceadgangspunkt, du vil bruge.
6. Vælg **Setup Service Integration**, og følg instruktionerne for [brug af E-Documents Connector med eksterne endepunkter](../../finance-how-setup-edocuments-external.md). Luk derefter siden.

### Sådan bruges Peppol-format  

1. Vælg den ![pære, der åbner funktionen Fortæl mig det.](../../media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **e-dokumenttjeneste**, og vælg derefter det relaterede link.
2. Vælg **Ny** for at oprette PEPPOL-tjenesten.
3. Udfyld alle data som forklaret i [Indstil E-Documents-stikket med eksterne endepunkter](../../finance-how-setup-edocuments-external.md).
4. I **Dokumentformat**-feltet skal du vælge **PEPPOL BIS 3.0** som eksportformat for den elektroniske eksportopsætning.
5. I **Serviceintegration** skal du angive det serviceadgangspunkt, du vil bruge.
6. Vælg **Setup Service Integration**, og følg instruktionerne for [brug af E-Documents Connector med eksterne endepunkter](../../finance-how-setup-edocuments-external.md). Luk derefter siden.

> [!NOTE]
> Hvis du ikke har et **GLN-nr.** , der er **angivet i** Virksomhedsopsætning **, bruges virksomhedens SE/CVR-nr. til eksport af alle elektroniske dokumenter.** som identifikator i de elektroniske dokumenter. I dette tilfælde er momsordningen **, der anvendes til elektroniske dokumenter i Danmark,** sat til 0184. Du kan kontrollere **momsordningens** værdi på siden **Land/område** for hvert af land/område. Det betyder, at denne værdi bruges i alle noder, når det er relevant. Det er også tilføjet et præfiks DK til **momsregistreringsnr.** når det er relevant.  

For at konfigurere arbejdsgange, kunder og leverandører, se [Sådan konfigureres E-Documents](../../finance-how-setup-edocuments.md) og [Indstil E-Documents-forbindelsen med eksterne slutpunkter](../../finance-how-setup-edocuments-external.md). 

## Se også

[Lokal funktionalitet for Danmark](denmark-local-functionality.md)  
[Sådan konfigureres e-dokumenter i Business Central](../../finance-how-setup-edocuments.md)  
[Sådan bruges e-dokumenter i Business Central](../../finance-how-use-edocuments.md)  
[Sådan udvides e-dokumenter i Business Central](/dynamics365/business-central/dev-itpro/developer/devenv-extend-edocuments)  
[Fakturasalg](../../sales-how-invoice-sales.md)  
[Registrere køb med købsfakturaer og ordrer](../../purchasing-how-record-purchases.md)  
[Arbejde med Business Central](../../ui-work-product.md)

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
