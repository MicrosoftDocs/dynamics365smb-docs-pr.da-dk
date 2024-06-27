---
title: Ofte stillede spørgsmål om bankkontoafstemning med Copilot (forhåndsversion)
description: 'Disse ofte stillede spørgsmål indeholder oplysninger om den AI-teknologi, der bruges til at afstemme bankkonti og kontoudtog i Business Central. De indeholder vigtige overvejelser og detaljer om, hvordan AI bruges, hvordan det blev testet og evalueret, og eventuelle specifikke begrænsninger.'
ms.date: 03/27/2024
ms.custom:
  - responsible-ai-faqs
ms.topic: article
author: jswymer
ms.author: jswymer
ms.reviewer: jswymer
ms.search.keywords: 'copilot, AI'
ms.collection:
  - bap-ai-copilot
---

# Ofte stillede spørgsmål om bankkontoafstemning med Copilot (forhåndsversion)

[!INCLUDE [preview-banner](~/../shared-content/shared/preview-includes/preview-banner.md)]

Disse ofte stillede spørgsmål (FAQ) beskriver AI-effekten af Microsoft Copilot-assistance med bankkontoafstemning i [!INCLUDE[prod_short](includes/prod_short.md)].

[!INCLUDE [preview-note](~/../shared-content/shared/preview-includes/production-ready-preview-dynamics365.md)]

## Hvad er bankafstemningshjælp?

Bankafstemning er en almindelig regnskabsopgave, hvor organisationer gennemgår deres bankkontoudtog for at identificere transaktioner, der skal registreres i [!INCLUDE[prod_short](includes/prod_short.md)]. Denne opgave bruges f.eks. til at identificere periodiske bankgebyrer eller mindre medarbejderudgifter.

Bankafstemning er typisk en proces i flere trin. Først indlæses bankkontoudtog til [!INCLUDE[prod_short](includes/prod_short.md)]. Derefter matches af transaktioner med finansposter. Endelig bogføres nye poster for at afspejle eventuelle resterende transaktioner, som dine finansposter ikke tidligere kendte.

Copilot i [!INCLUDE[prod_short](includes/prod_short.md)] reducerer den manuelle indsats ved at matche flere transaktioner og foreslå finanskonti (G/L), som du kan bogføre til.

## Hvad er funktionerne i bankafstemningshjælp?

Copilot yder AI-drevet assistance med to forskellige opgaver:

- Forbedret matchning af transaktioner med poster

    [!INCLUDE[prod_short](includes/prod_short.md)] tilbyder automatiserede regler, der automatisk matcher mange banktransaktioner med poster. Disse regler er imidlertid ufleksible og resulterer ofte i mange ikke-matchede transaktioner, der hver især kræver manuel inspektion og sammenligning. Copilot bruger AI-teknologi til at inspicere disse ikke-matchede transaktioner og identificere flere matches baseret på datoer, beløb og beskrivelser. Hvis en debitor f.eks. betaler flere fakturaer som et engangsbeløb, afstemmer Copilot linjen med det enkelte bankkontoudtog med flere fakturaposter.

- Foreslåede finanskonti

    For resterende banktransaktioner, der ikke kan matches med nogen poster, bruger Copilot AI-teknologi til at sammenligne transaktionsbeskrivelsen med finanskontonavne og foreslår derefter den mest sandsynlige finanskonto at bogføre til. Hvis ikke-matchede transaktioner har fortællingen *Fuel Stop24*, kan Copilot f.eks. foreslå, at du bogføre dem til kontoen *Transaktioner*.

Copilot opretter ikke forbindelse til din bank for at hente eller sende transaktioner. Denne opgave forbliver fuldt ud inden for din kontrol. Det er en forudsætning for at bruge Copilots assistance, uanset om disse transaktioner føjes til [!INCLUDE[prod_short](includes/prod_short.md)] ved hjælp af en digital bankforbindelse, importeres fra en bankkontoudtogsfil eller indtastes manuelt.

## Hvad er den tilsigtede brug af bankafstemningshjælp?

Hjælp til bankkontoafstemning er designet til at forbedre nøjagtigheden af finansposter ved at hjælpe debitorerne med nye transaktioner, som de skal tage højde for i [!INCLUDE[prod_short](includes/prod_short.md)]. Den er ikke beregnet til at opdage svindel eller identificere, om kunderne har betalt til tiden.

## Hvordan blev bankafstemningshjælp evalueret? Hvilke metrikværdier bruges til at måle ydeevnen?

Hjælp til bankkontoafstemning blev testet ved at bruge en kombination af syntetiske banktransaktionsdata og lignende finanskonti og poster, der dækker de typiske variationer og datagrænser for hvert felt og på forskellige sprog. Testdata repræsenterer både typisk brug og brug af dårlige aktører. Ydeevnen blev målt sammenlignet med manuel afstemning af de samme data.

## Hvad er begrænsningerne af bankafstemningshjælp? Hvordan kan brugere minimere disse begrænsninger, når de bruger systemet?

Hjælp til afstemning af bankkonto fungerer bedst, når finanskontonavne, postbeskrivelser og banktransaktionsbeskrivelser alle er på samme sprog. Blandede sprog eller blandede sprog til transaktionsbeskrivelser resulterer ofte i færre matches og forslag.

Foreslåede finanskonti klarer sig bedst på et af de understøttede sprog (se en liste over sprog i næste afsnit). Brugere kan opleve færre transaktionsmatch og færre foreslåede finanskonti på andre sprog.

## I hvilke geografiske områder og på hvilke sprog er bankafstemningshjælp tilgængelig? 

- Tilgængelige geografiske områder

  Hjælp til bankkontoafstemning er tilgængelig i alle understøttede [Business Central-lande/områder](/dynamics365/business-central/dev-itpro/compliance/apptest-countries-and-translations). For kundemiljøer, der er placeret i lande/områder, hvor Azure OpenAI-servicen ikke er udrullet, skal administratorer først give samtykke til, at data flyttes på tværs af grænser, for at [!INCLUDE [prod_short](includes/prod_short.md)] kan oprette forbindelse til Azure OpenAI-servicen. Få mere at vide om [Copilot-dataflytning på tværs af geografiske områder](ai-copilot-data-movement.md).

- Tilgængelige sprog

  [!INCLUDE[bank-recon-assist-language-support](includes/bank-recon-assist-language-support.md)]

Du kan finde flere oplysninger om sprog under det forrige spørgsmål om begrænsninger.

## Hvad forventes der af systembrugere, når de bruger bankkontoafstemning?

### Under bankkontoafstemning

AI-drevne matches og forslag kan nogle gange være forkerte eller ufuldstændige. Brugere af bankkontoafstemningsassistance skal gennemgå nøjagtigheden af de matches og forslag, som Copilot leverer, før de vælger at beholde dem. Copilots matches og forslag gemmes ikke i [!INCLUDE[prod_short](includes/prod_short.md)]-databasen, før du vælger knappen **Behold den** og lukker Copilot-vinduet. Du kan også redigere og rette eventuelle matches eller forslag, før du vælger at beholde dem.

### Når bankkontoafstemning er fuldført

Vi anbefaler, at brugerne også kontrollerer nøjagtigheden og retter eventuelle uoverensstemmelser, når de lukker Copilot-vinduet. Denne proces skal omfatte følgende aktiviteter:

- Gennemse afstemningstestrapporten.
- Sørg for, at din organisation har de relevante gennemgangs- og revisionsprocesser på plads.
- Genåbne alle bogførte afstemninger ved hjælp af funktionen **Fortryd**.
- Rette eventuelle fejlposter ved tilbageførsel af poster.

## Hvad forventes der af administratorer og systembrugere, når de bruger bankkontoafstemning?

Systembrugere, såsom revisorer, kasserere eller andre, der arbejder med virksomhedsregnskab, bør altid gennemgå nøjagtigheden af matches og forslag, som Copilot leverer, før de vælger at beholde dem. Efter afstemning med Copilot anbefaler vi, at disse brugere gennemser afstemningstestrapporten for at bekræfte nøjagtigheden og identificere eventuelle uoverensstemmelser.

Administratorer bør sikre, at de relevante regnskabsbrugere har adgang til denne funktion.

## Er Copilot det eneste middel til at gennemføre bankkontoafstemning?

Nej Brug af Copilot er valgfrit. [!INCLUDE[prod_short](includes/prod_short.md)] tilbyder traditionelle, ikke-AI-drevne metoder til import af bankkontoudtog, kørsel af foruddefinerede matchregler og manuel anvendelse af matches og bogføring på relevante finanskonti. Både den traditionelle tilgang og Copilot kan bruges samtidigt i en organisation.

## Hvordan giver jeg feedback om AI-genereret indhold?

Hver gang Copilot leverer matches eller forslag, kan du give feedback til Microsoft direkte fra Copilot-vinduet ved hjælp af kontrolelementerne Synes godt om (tommelfinger opad) og Synes ikke op (tommelfinger nedad). Dit feedback forbliver anonymt, og vi bruger disse data til at evaluere og forbedre kvaliteten af tjenesten.

## Se også

[Afstemme bankkonti med Copilot (forhåndsversion)](bank-reconciliation-with-copilot.md)
