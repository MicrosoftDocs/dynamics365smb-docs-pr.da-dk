---
title: Ofte stillede spørgsmål til tekniske detaljer
description: Implementeringsdetaljer vedrørende Shopify-connector.
ms.date: 03/27/2023
ms.topic: article
ms.service: dynamics365-business-central
author: AndreiPanko
ms.author: andreipa
---

# <a name="faq-for-technical-details" />Ofte stillede spørgsmål vedrørende tekniske detaljer

Denne artikel besvarer ofte stillede spørgsmål om Shopify-connectoren.

## <a name="what-is-shopify" />Hvad er Shopify?

Shopify er et abonnementsbaseret program, der gør det muligt for alle at konfigurere en onlinebutik og sælge deres produkter. Shopify-platformen tilbyder onlinebutikker en række tjenester, herunder betalinger, marketing-, leverings- og kundeengagementsværktøjer.

## <a name="what-is-the-microsoft-dynamics--business-central-shopify-connector" />Hvad er Microsoft Dynamics 365 Business Central Shopify-connector?

Shopify-connector giver virksomheder mulighed for at tilslutte din deres Shopify-butik (eller butikker) med [!INCLUDE[prod_short](../includes/prod_short.md)] for at maksimere produktiviteten. Ved hjælp af Shopify-connector kan indsigter administreres og vises fra virksomheden og deres Shopify-online butik som én enhed.

### <a name="capabilities" />Funktioner

- Support til mere end én Shopify-butik
  - Hvert køb har sin egen opsætning, herunder en samling produkter, lokationer, der bruges til at beregne lager, og prislister.  
- Tovejs synkronisering af varer eller produkter
  - Connectoren synkroniserer billeder, varevarianter, stregkoder, leverandørs varenumre, udvidede tekster og koder.  
  - Eksporte vareattributter til Shopify.  
  - Brug de valgte debitorprisgrupper og rabatter til at definere de priser, der skal udlæses til Shopify.  
  - Beslut, om du kan oprette varer automatisk eller kun tillade opdateringer af eksisterende produkter.  
- Lagerniveausynkronisering
  - Vælge nogle eller alle tilgængelige placeringer i [!INCLUDE [prod_short](../includes/prod_short.md)].  
  - Opdater lagerniveauer på flere lokationer i Shopify.  
- Tovejs synkronisering af kunder
  - Med chipkort-kunder pr. telefon og pr. e-mail.  
  - Brug landespecifikke skabeloner, når du opretter debitorer, som er med til at sikre, at skatte indstillingerne er korrekte.  
- Importer ordrer fra Shopify
  - Medtage ordrer, der er oprettet i andre kanaler, f. eks Online-butik eller **Shopify POS**.
  - Forsendelsesomkostninger, gavekort, tip, leverings-og betalingsmetoder, transaktioner og risiko for svig.  
  - Under indlæsningen kan du automatisk oprette debitorer i [!INCLUDE [prod_short](../includes/prod_short.md)] eller bestemme, om debitorerne i Shopify skal administreres.  
  - Modtage betalingsoplysninger fra Shopify Payments.
- Spore indfrielsesoplysninger
  - Du kan vælge at overføre oplysninger om varesporing fra [!INCLUDE [prod_short](../includes/prod_short.md)] til Shopify.  

## <a name="why-did-microsoft-and-shopify-form-this-partnership" />Hvorfor har Microsoft og Shopify formular dette partnerskab?

[!INCLUDE[prod_short](../includes/prod_long.md)] er hjælper vores kunder sammen med Shopify for at opnå en bedre indkøbsoplevelse. Mens Shopify leverer en nem, komplet løsning til virksomhedsadministration, tilbyder [!INCLUDE[prod_short](../includes/prod_short.md)] omfattende virksomhedsadministration på tværs af finansielle transaktioner, salg, service og drift. Problemfri forbindelse mellem de to systemer synkroniserer ordrer, lager og kundeoplysninger for at sikre, at handlende kan opfylde ordrer hurtigere og give bedre kunder.

## <a name="which-microsoft-products-are-the-shopify-connector-available-for" />Hvilke Microsoft-produkter er Shopify-connectoren tilgængelige for?

Denne funktion er kun tilgængelig for [!INCLUDE[prod_short](../includes/prod_short.md)] online, startende med version 20.1. Funktionen understøttes ikke i lokale installationer. Connectoren er forudinstalleret for at give nye miljøer. Organisationer med eksisterende miljøer kan hente og installere connectoren fra AppSource. Organisationen skal have både en [!INCLUDE [prod_short](../includes/prod_short.md)]-licens og en Shopify-licens for at kunne bruge connectoren. Du kan finde flere oplysninger om understøttede lande, sprog og udgaver af [!INCLUDE[prod_short](../includes/prod_short.md)] på [Shopify Connector på AppSource](https://go.microsoft.com/fwlink/?linkid=2196238).

Shopify-connectoren kan ikke bruges til en [indlejret app](/dynamics365/business-central/dev-itpro/deployment/embed-app-overview), hvor klientens URL-adresse har formatet: `https://[application name].bc.dynamics.com`.

## <a name="what-support-is-offered-for-the-shopify-connector" />Hvilken support tilbydes til Shopify-connector?

### <a name="includeprodshortincludesprodshortmd" />[!INCLUDE[prod_short](../includes/prod_short.md)]

Shopify-connectoren er dækket af den aktuelle supportmodel. Du kan finde flere oplysninger i [Teknisk support](/dynamics365/business-central/dev-itpro/administration//manage-technical-support) (kun på engelsk).

Få hjælp fra en konsulent, som kender Shopify-connectoren til [!INCLUDE[prod_short](../includes/prod_short.md)] med henblik på at opfylde dine specifikke forretningsspecifikke krav. Søge efter [Konsulent Service](https://aka.ms/BCShopifyConsultant).

### <a name="shopify" />Shopify

Hvis du vil have hjælp til Shopify, kan du starte med [Generel Shopify Help-center](https://help.shopify.com/) eller [24/7 support til din butik som Shopify-forhandler](https://help.shopify.com/questions#/).

Du kan også udforske [Eksperter på markedet](https://experts.shopify.com/) for at finde de rigtige eksperter, som tilbyder services til Shopify- forhandlere.

## <a name="currently-unsupported-features-however-were-tracking-them-and-may-consider-adding-them" />Understøttes ikke i øjeblikket, men vi holder styr på dem og kan evt. tilføje dem

- B2B-funktioner, herunder virksomheder, prislister og betalingsbetingelser
- Markeder
  - Flere oversættelser af master data. Du kan vælge ét sprog, der skal bruges til eksport af produktoplysninger.
  - Priser pr. land/område. Én prisliste er tilgængelig for den valgte valuta. Omregningen til andre valutaer håndteres af Shopify.

## <a name="is-the-shopify-connector-extensible" />Kan Shopify-connectoren udvides?

Ja, Shopify-connectoren kan udvides. Kontroller GitHub for at få adgang til [listen med udvidelsespunkter](https://github.com/microsoft/ALAppExtensions/tree/main/Apps/W1/Shopify), og udforsk nogle [eksempler](https://github.com/microsoft/ALAppExtensions/blob/main/Apps/W1/Shopify/extensibility_examples.md).

## <a name="is-the-shopify-connector-open-for-contribution" />Er Shopify-connectoren åben for bidrag

Ja, denne udvidelse er åben for bidrag fra vores community. Du kan finde [kildekoden](https://github.com/microsoft/ALAppExtensions/tree/main/Apps/W1/Shopify) i Microsoft AL-tilføjelsesprogrammet til alle programmer.

## <a name="see-also" />Se også

[Kom i gang med Connectoren til Shopify](get-started.md)  
