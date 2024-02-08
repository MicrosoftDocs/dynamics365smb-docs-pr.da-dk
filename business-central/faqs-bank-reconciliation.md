---
title: Ofte stillede spørgsmål om bankkontoafstemning med Copilot (forhåndsversion)
description: 'Disse ofte stillede spørgsmål indeholder oplysninger om den AI-teknologi, der bruges til at afstemme bankkonti og kontoudtog Business Central. De indeholder vigtige overvejelser og detaljer om, hvordan AI bruges, hvordan det blev testet og evalueret, og eventuelle specifikke begrænsninger.'
ms.date: 11/07/2023
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

# <a name="faq-for-bank-account-reconciliation-assist-preview-with-copilot"></a>Ofte stillede spørgsmål om bankkontoafstemning med Copilot (forhåndsversion)

[!INCLUDE[production-ready-preview-dynamics365](includes/production-ready-preview-dynamics365.md)]

Disse ofte stillede spørgsmål (FAQ) beskriver AI-effekten af Copilot-assistance med bankkontoafstemning i [!INCLUDE[prod_short](includes/prod_short.md)]. 

## <a name="what-is-bank-reconciliation-assist"></a>Hvad er bankafstemningshjælp?

Bankafstemning er en almindelig regnskabsopgave, hvor organisationer gennemgår deres bankkontoudtog for at identificere transaktioner, der skal registreres i [!INCLUDE[prod_short](includes/prod_short.md)]. Denne opgave vil f.eks. blive brugt til at identificere periodiske bankgebyrer eller mindre medarbejderudgifter. Denne opgave er typisk en proces i flere trin, der starter med import af bankkontoudtog til [!INCLUDE[prod_short](includes/prod_short.md)], efterfulgt af matchning af transaktioner med finansposter og bogføring af nye poster for at afspejle eventuelle resterende transaktioner, som ikke tidligere var kendt af dine finansposter. Copilot i [!INCLUDE[prod_short](includes/prod_short.md)] reducerer den manuelle indsats ved at matche flere transaktioner og foreslå finanskonti, som du kan bogføre til. 

## <a name="what-are-capabilities-of-bank-reconciliation-assist"></a>Hvad er funktionerne i bankafstemningshjælp?

Copilot yder AI-drevet assistance med to forskellige opgaver: 

- Forbedret matchning af transaktioner med poster 

   [!INCLUDE[prod_short](includes/prod_short.md)] tilbyder automatiserede regler, der automatisk matcher mange banktransaktioner med poster. Disse regler er imidlertid ufleksible og resulterer ofte i mange ikke-matchede transaktioner, der hver især kræver manuel inspektion og sammenligning. Copilot bruger AI-teknologi til at inspicere resterende transaktioner og identificere flere matches baseret på datoer, beløb og beskrivelser. Hvis flere fakturaer f.eks. blev betalt som et engangsbeløb af en kunde, afstemmer Copilot linjen med det enkelte bankkontoudtog med flere fakturaposter. 
 
- Foreslåede finanskonti 

   For resterende banktransaktioner, der ikke kunne matches med nogen poster, bruger Copilot AI-teknologi til at sammenligne transaktionsbeskrivelsen med finanskontonavne, hvilket foreslår den mest sandsynlige finanskonto at bogføre til. Copilot kan f.eks. foreslå, at transaktionen med fortællingen "Fuel Stop24" bogføres på kontoen "Transport". 

Copilot opretter ikke forbindelse til din bank for at hente eller sende transaktioner. Denne opgave forbliver fuldt ud under din kontrol og er en forudsætning for at begynde at bruge Copilots assistance, uanset om disse transaktioner føjes til [!INCLUDE[prod_short](includes/prod_short.md)] ved hjælp af en digital bankforbindelse, importeres fra en bankkontoudtogsfil eller indtastes manuelt. 

## <a name="what-is-the-intended-use-of-bank-reconciliation-assist"></a>Hvad er den tilsigtede brug af bankafstemningshjælp?

Hjælp til bankkontoafstemning er designet til at hjælpe med at identificere nye transaktioner, som kunderne skal tage højde for i [!INCLUDE[prod_short](includes/prod_short.md)] for at forbedre nøjagtigheden af deres finansposter. Denne aktivitet er ikke beregnet til at opdage svindel eller identificere, om kunderne har betalt til tiden.   

## <a name="how-was-bank-reconciliation-assist-evaluated-what-metrics-are-used-to-measure-performance"></a>Hvordan blev bankafstemningshjælp evalueret? Hvilke metrikværdier bruges til at måle ydeevnen?

Denne funktionalitet er testet ved hjælp af syntetiske banktransaktionsdata og lignende finanskonti og poster, der dækker de typiske variationer og datagrænser for hvert felt og på forskellige sprog. Testdata repræsenterer både typisk brug og brug af dårlige aktører. Ydeevnen blev målt sammenlignet med manuel afstemning af de samme data. 

## <a name="what-are-the-limitations-of-bank-reconciliation-assist-how-can-users-minimize-the-impact-of-the-bank-reconciliation-limitations-when-using-the-system"></a>Hvad er begrænsningerne af bankafstemningshjælp? Hvordan kan brugerne minimere virkningen af bankafstemningsbegrænsningerne, når de bruger systemet?

Hjælp til afstemning af bankkonto fungerer bedst, når finanskontonavne, postbeskrivelser og banktransaktionsbeskrivelser alle er på samme sprog. Blandede sprog eller blandet sprog i transaktionsbeskrivelser resulterer ofte i færre matches og forslag. 

Foreslåede finanskonti klarer sig bedst på engelsk. Selvom denne funktion kan betjenes på alle de tilgængelige [!INCLUDE[prod_short](includes/prod_short.md)]-sprog, kan brugerne opleve færre transaktionsmatch og færre foreslåede finanskonti på andre sprog. 
<!--

## <a name="what-operational-factors-and-settings-allow-for-effective-and-responsible-use-of-the-feature"></a>What operational factors and settings allow for effective and responsible use of the feature?


-->
## <a name="in-which-geographies-and-languages-is-bank-reconciliation-assist-available"></a>I hvilke geografiske områder og på hvilke sprog er bankafstemningshjælp tilgængelig?

+Denne funktion er tilgængelig for alle miljøer, lande-/områdelokaliseringer og på alle brugersprog. For kundemiljøer, der er placeret i lande/områder, hvor Azure OpenAI-tjenesten ikke er udrullet, skal administratorer først give samtykke til, at data flyttes på tværs af grænser for [!INCLUDE[prod_short](includes/prod_short.md)] for at oprette forbindelse til Azure OpenAI-tjenesten, og for at denne funktion er tilgængelig. 

Du kan finde flere oplysninger om sprog under forrige spørgsmål om begrænsninger.  

## <a name="what-is-expected-of-end-users-when-operating-bank-account-reconciliation-assist"></a>Hvad forventes der af slutbrugere, når du hjælper med at betjene bankkontoafstemning?

### <a name="while-using-bank-account-reconciliation"></a>Under brug af bankkontoafstemning

AI-drevne matches og forslag kan nogle gange være forkerte eller ufuldstændige. Brugere af bankkontoafstemningsassistance skal gennemgå nøjagtigheden af matches og forslag fra Copilot, før de vælger at beholde dem. Copilots matches og forslag gemmes ikke i [!INCLUDE[prod_short](includes/prod_short.md)]-databasen, før du vælger knappen Behold den og forlader Copilot-vinduet. Du kan også redigere og rette eventuelle matches eller forslag, før du vælger at beholde dem. 

### <a name="after-completing-bank-account-reconciliation"></a>Efter fuldført bankkontoafstemning

Det anbefales, at brugerne også kontrollerer nøjagtigheden og retter eventuelle uoverensstemmelser efter at have forladt Copilot-vinduet, herunder følgende aktiviteter: 

- Gennemse afstemningstestrapporten. 
- Sørg for, at din organisation har de relevante gennemgangs- og revisionsprocesser på plads. 
- Genåbne alle bogførte afstemninger ved hjælp af funktionen Fortryd. 
- Rette eventuelle fejlposter ved tilbageførsel af poster. 

## <a name="what-is-expected-of-administrators-and-end-users-when-operating-bank-account-reconciliation-assist"></a>Hvad forventes der af administratorer og slutbrugere, når du hjælper med at betjene bankkontoafstemning?

Slutbrugere, såsom revisorer, kasserere eller andre, der arbejder med virksomhedsregnskab, bør altid gennemgå nøjagtigheden af matches og forslag fra Copilot, før de vælger at beholde dem. Når du har afstemt med Copilot, anbefaler vi, at du gennemser afstemningstestrapporten for at bekræfte nøjagtigheden og identificere eventuelle uoverensstemmelser. 

Administratorer bør sikre, at de relevante regnskabsbrugere har fået adgang til denne funktion. 

## <a name="is-copilot-the-only-means-to-completing-bank-account-reconciliation"></a>Er Copilot det eneste middel til at gennemføre bankkontoafstemning?

Nej – brug af Copilot er valgfrit. [!INCLUDE[prod_short](includes/prod_short.md)] tilbyder traditionelle, ikke-AI-drevne metoder til import af bankkontoudtog, kørsel af foruddefinerede matchregler og manuel anvendelse af matches og bogføring på relevante finanskonti. Både den traditionelle tilgang og Copilot kan bruges samtidigt i en organisation. 

## <a name="how-do-i-give-feedback-about-ai-generated-content"></a>Hvordan giver jeg feedback om AI-genereret indhold?

Hver gang Copilot giver matches eller forslag, kan du give feedback til Microsoft direkte fra Copilot-vinduet ved hjælp af kontrolelementerne Synes godt om og Afvis. Dit feedback forbliver anonymt, og vi bruger disse data til at evaluere og forbedre kvaliteten af tjenesten.


## <a name="see-also"></a>Se også

[Afstemme bankkonti ved hjælp af bankkontoafstemning (forhåndsversion)](bank-reconciliation-with-copilot.md)
