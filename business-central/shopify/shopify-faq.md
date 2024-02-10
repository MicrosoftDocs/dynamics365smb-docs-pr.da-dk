---
title: Ofte stillede spørgsmål til tekniske detaljer
description: Implementeringsdetaljer vedrørende Shopify-connector.
ms.date: 01/24/2024
ms.topic: article
ms.service: dynamics-365-business-central
author: brentholtorf
ms.author: bholtorf
---

# Ofte stillede spørgsmål vedrørende tekniske detaljer

Denne artikel besvarer ofte stillede spørgsmål om Shopify-connectoren.

## Hvad er Shopify?

Shopify er et abonnementsbaseret program, der gør det muligt for alle at konfigurere en onlinebutik og sælge deres produkter. Shopify-platformen tilbyder onlinebutikker en række tjenester, herunder betalinger, marketing-, leverings- og kundeengagementsværktøjer.

## Hvad er Microsoft Dynamics 365 Business Central Shopify-connector?

Shopify-connector giver virksomheder mulighed for at tilslutte din deres Shopify-butik (eller butikker) med [!INCLUDE[prod_short](../includes/prod_short.md)] for at maksimere produktiviteten. Ved hjælp af Shopify-connector kan indsigter administreres og vises fra virksomheden og deres Shopify-online butik som én enhed.

### Funktioner

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
  - Brug lande/områdespecifikke skabeloner, når du opretter debitorer, som er med til at sikre, at skatte indstillingerne er korrekte.  
- Importer ordrer fra Shopify
  - Medtage ordrer, der er oprettet i andre kanaler, f. eks Online-butik eller **Shopify POS**.
  - Forsendelsesomkostninger, gavekort, tip, leverings-og betalingsmetoder, transaktioner og risiko for svig.  
  - Under indlæsningen kan du automatisk oprette debitorer i [!INCLUDE [prod_short](../includes/prod_short.md)] eller bestemme, om debitorerne i Shopify skal administreres.  
  - Modtage betalingsoplysninger fra Shopify Payments.
- Spore indfrielsesoplysninger
  - Du kan vælge at overføre oplysninger om varesporing fra [!INCLUDE [prod_short](../includes/prod_short.md)] til Shopify.  

## Hvorfor har Microsoft og Shopify formular dette partnerskab?

[!INCLUDE[prod_short](../includes/prod_long.md)] er hjælper vores kunder sammen med Shopify for at opnå en bedre indkøbsoplevelse. Mens Shopify leverer en nem, komplet løsning til virksomhedsadministration, tilbyder [!INCLUDE[prod_short](../includes/prod_short.md)] omfattende virksomhedsadministration på tværs af finansielle transaktioner, salg, service og drift. Problemfri forbindelse mellem de to systemer synkroniserer ordrer, lager og kundeoplysninger for at sikre, at handlende kan opfylde ordrer hurtigere og give bedre kunder.

## Hvilke Microsoft-produkter er Shopify-connectoren tilgængelige for?

Denne funktion er kun tilgængelig for [!INCLUDE[prod_short](../includes/prod_short.md)] online, startende med version 20.1. Funktionen understøttes ikke i lokale installationer. Connectoren er forudinstalleret for at give nye miljøer. Organisationer med eksisterende miljøer kan hente og installere connectoren fra AppSource. Organisationen skal have både en [!INCLUDE [prod_short](../includes/prod_short.md)]-licens og en Shopify-licens for at kunne bruge connectoren. Du kan finde flere oplysninger om understøttede lande/områder, sprog og udgaver af [!INCLUDE[prod_short](../includes/prod_short.md)] på [Shopify Connector på AppSource](https://go.microsoft.com/fwlink/?linkid=2196238).

Shopify-connectoren kan ikke bruges til en [indlejret app](/dynamics365/business-central/dev-itpro/deployment/embed-app-overview), hvor klientens URL-adresse har formatet: `https://[application name].bc.dynamics.com`.

## Hvilken support tilbydes til Shopify-connector?

### [!INCLUDE[prod_short](../includes/prod_short.md)]

Shopify-connectoren er dækket af den aktuelle supportmodel. Du kan finde flere oplysninger i [Teknisk support](/dynamics365/business-central/dev-itpro/administration//manage-technical-support) (kun på engelsk).

Få hjælp fra en konsulent, som kender Shopify-connectoren til [!INCLUDE[prod_short](../includes/prod_short.md)] med henblik på at opfylde dine specifikke forretningsspecifikke krav. Søge efter [Konsulent Service](https://aka.ms/BCShopifyConsultant).

### Shopify

Hvis du vil have hjælp til Shopify, kan du starte med [Generel Shopify Help-center](https://help.shopify.com/) eller [24/7 support til din butik som Shopify-forhandler](https://help.shopify.com/questions#/).

Du kan også udforske [Eksperter på markedet](https://experts.shopify.com/) for at finde de rigtige eksperter, som tilbyder services til Shopify- forhandlere.

## Understøttes ikke i øjeblikket, men vi holder styr på dem og kan evt. tilføje dem

- B2B-funktioner, herunder virksomheder, prislister og betalingsbetingelser
  - Udvidet understøttelse af B2B vil være tilgængelig i udgivelsesbølge 1 i 2024. Du kan finde flere oplysninger i [Connect Business Central med Shopify B2B](/dynamics365/release-plan/2023wave2/smb/dynamics365-business-central/connect-business-central-shopify-b2b)
- Markeder
  - Flere oversættelser af master data. Du kan vælge ét sprog, der skal bruges til eksport af produktoplysninger.
  - Priser pr. land/område. Én prisliste er tilgængelig for den valgte valuta. Omregningen til andre valutaer håndteres af Shopify.
- Udkast til ordrer

## Kan Shopify-connectoren udvides?

Ja, Shopify-connectoren kan udvides. Kontroller GitHub for at få adgang til [listen med udvidelsespunkter](https://github.com/microsoft/ALAppExtensions/tree/main/Apps/W1/Shopify), og udforsk nogle [eksempler](https://github.com/microsoft/ALAppExtensions/blob/main/Apps/W1/Shopify/extensibility_examples.md).

## Er Shopify-connectoren åben for bidrag

Ja, denne udvidelse er åben for bidrag fra vores community. Du kan finde [kildekoden](https://github.com/microsoft/ALAppExtensions/tree/main/Apps/W1/Shopify) i Microsoft AL-tilføjelsesprogrammet til alle programmer.

## Opbygning af din version af Shopify Connector

Ifølge Shopify, hvis du vil bygge og udgive en connector-app på Shopify-markedspladsen, der har det primære formål at overføre eller dele forhandlerdata til en tredjepart ([!INCLUDE [prod_short](../includes/prod_short.md)]), skal du have skriftligt samtykke fra Shopify. Som en del af denne proces skal du indhente samtykke fra Microsoft i "End Recipient Data Acknowledgement Form". Vi er nødt til at bede dig om at håndtere sagen med Shopify, fordi Microsoft ikke kan underskrive 3. parts aftaler.

### Hvad du skal gøre

Tjek kravene fra Shopify, fordi du muligvis stadig kan have en skjult app.

Alternativt får Shopify Connector til [!INCLUDE [prod_short](../includes/prod_short.md)] konstant nye funktioner og nye kunder. Hvis du opdager et specifikt hul, kan du overveje at indsende et produktforslag (https://aka.ms/bcideas) eller et kodebidrag til [!INCLUDE [prod_short](../includes/prod_short.md)]. For krav, der muligvis ikke er relevante for et flertal af kunderne, og som ikke let kan løses med den nuværende udvidelsesmodel, bedes du kontakte [!INCLUDE [prod_short](../includes/prod_short.md)] udviklingsteamet for at diskutere brugssagen. Vi bør være i stand til at finde en gennemførlig løsning.

## Se også

[Kom i gang med Connectoren til Shopify](get-started.md)  
