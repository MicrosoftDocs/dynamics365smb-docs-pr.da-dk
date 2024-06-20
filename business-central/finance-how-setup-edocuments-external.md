---
title: Indstil E-Documents-stikket med eksterne endepunkter
description: 'Denne artikel forklarer, hvordan du opsætter E-Documents-funktionalitet, når den er forbundet til eksterne slutpunkter.'
author: altotovi
ms.topic: conceptual
ms.devlang: al
ms.search.keywords: 'electronic document, electronic invoice, e-document, e-invoice, access-point, endpoint'
ms.search.form: '359, 360, 6103, 6133'
ms.date: 12/13/2023
ms.author: altotovi
ms.service: dynamics-365-business-central
ms.reviewer: bholtorf
---

# Indstil E-Documents-stikket med eksterne endepunkter

Denne artikel forklarer, hvordan du opsætter E-Documents-funktionalitet, når den er forbundet til eksterne slutpunkter.

Inden du bruger den funktionalitet, der er beskrevet i denne artikel, skal du installere **E-Documents Connector med eksterne endepunkter** appen på toppen af ​​den globale **E- Document Core** app. Denne app kan bruges til standardintegration med de eksterne (tredjeparts) adgangspunkter for at automatisere e-dokumentflowet. Fordi denne app kun repræsenterer nogle af de valgte connectors, er du ikke begrænset til eksisterende integrationer i den. De fleste stik vil være tilgængelige på AppSource i fremtiden.

## Konfigurere forbindelsen

For at starte din opsætning skal du følge trinene i [E-document core app](finance-how-setup-edocuments.md). Når du har gennemført disse trin, skal du vende tilbage til denne artikel og udføre følgende trin:

1. Vælg ![Lightbulb, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **e-dokumenttjeneste**, og vælg derefter det relaterede link.
2. I feltet **Service Integration** skal du vælge en af de integrationskoder, der tilbydes til opsætningen af slutpunktstjenesten.
3. Vælg **Opsætning af serviceintegration**.
4. På siden **E-Document External Connection Setup** skal du vælge **Request Authorization Code**. Du bliver omdirigeret til den eksterne tjenestegodkendelseswebside og bliver bedt om dine loginoplysninger.
5. Kopiér autorisationskoden i feltet **Indtast autorisationskode**.
6. Vælg **Opdater adgangstoken** for at sikre, at du kan opdatere tokenet.

    > [!NOTE]
    > Denne forbindelse kræver kommunikation med eksterne tjenesteudbydere, der kan være genstand for yderligere betaling og kræver kontrakter med dem. Kontakt tjenesteudbyderne for at få alle de nødvendige legitimationsoplysninger.

7. På siden **E-Document External Connection Setup** skal du udfylde følgende felter:

    | Feltnavn | Beskrivelse |
    |---|---|
    | URL-adresse til FileAPI | Angiv URL-adressen til fil-API. |
    | URL-adresse til fildele | Angiv URL-adressen til fildele. |
    | URL-adresse til DocumentAPI | Angiv URL-adressen til dokument-API'en. |
    | Virksomheds-id | Angiv virksomheds-id'et. |
    | Send tilstand | Angiv sendetilstanden. Du kan vælge **Produktion**, **Test** eller **Certificering**. |

    > [!NOTE]
    > Bed din tjenesteudbyder om alle de tidligere detaljer for at oprette forbindelse til deres adgangspunkt.

## Opsæt dine virksomhedsoplysninger

Før du begynder at bruge e-dokumenter, skal du opdatere din **Virksomhedsoplysninger**-side ved at udføre følgende trin:

1. Vælg ![Lightbulb, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, åbn **Virksomhedsoplysninger**, og vælg derefter det relaterede link.
2. Udover at udfylde de sædvanlige felter, skal du også udfylde følgende felter:

    | Feltnavn | Beskrivelse |
    |---|---|
    | SWIFT-kode | Angiv SWIFT-koden (internationalt bank-id) for din primære bank. |
    | Bankregistreringsnr. | Angiv bankens fire-cifrede registreringsnummer. |
    | Momsregistreringsnummer | Angiv virksomhedens momsregistreringsnummer. |

3. Luk siden.

## Indstil kunder til at modtage e-dokumenter

For at give kunderne mulighed for at modtage dine e-dokumenter skal du udføre følgende trin:

1. Vælg ![Lightbulb, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **Kunder**, og vælg derefter det relaterede link.
2. Åbn **debitorkortet**.
3. Udover at udfylde de sædvanlige felter, angives i feltet **GLN** kunden i forbindelse med fremsendelse af elektroniske dokumenter.
4. Marker feltet **Brug GLN i elektroniske dokumenter** for at angive, om det globale lokationsnummer (GLN) bruges som et partsidentifikationsnummer i elektroniske dokumenter.
5. Luk siden.

## Anden konfiguration

Inden du begynder at arbejde med e-dokumenter, skal du konfigurere e-dokument **workflows** og **dokumentafsendelsesprofilerne** til bruge dine arbejdsgange. Efter at serviceforbindelsen er etableret, kan du begynde at bruge din e-dokumentløsning.

## Disponible serviceudbydere

Microsoft ønsker at opfordre adgangspunktudbydere til at tilføje deres stik oven på vores **E-Document Core** rammer.

I øjeblikket er Pagero den eneste adgangspunktudbyder, der er dækket af dette system. Microsoft har ingen kontraktlig forpligtelse med Pagero. Derfor skal du lave en kontrakt med dem for at få alle de nødvendige legitimationsoplysninger.

Vi vil opdatere denne liste, efterhånden som vi får nye udbydere af e-dokumentudvekslingsadgangspunkter.

## Se også

[Sådan konfigureres e-dokumenter i Business Central](finance-how-setup-edocuments.md)  
[Sådan bruges e-dokumenter i Business Central](finance-how-use-edocuments.md)  
[Sådan udvides e-dokumenter i Business Central](/dynamics365/business-central/dev-itpro/developer/devenv-extend-edocuments)  
[Økonomistyring](finance.md)  
[Fakturasalg](sales-how-invoice-sales.md)  
[Registrere køb med købsfakturaer og ordrer](purchasing-how-record-purchases.md)  
[Arbejd med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)

[!INCLUDE[footer-include](includes/footer-banner.md)]
