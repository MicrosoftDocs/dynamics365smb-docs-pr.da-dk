---
title: Ofte stillede spørgsmål om tilknytning af e-dokumenter med købsordrer
description: 'Ofte stillede spørgsmål om AI indeholder oplysninger om den AI-teknologi, der bruges i Business Central, sammen med vigtige overvejelser og detaljer om, hvordan AI''en bruges, hvordan den blev testet og evalueret og eventuelle specifikke begrænsninger.'
ms.date: 02/23/2024
ms.custom:
  - responsible-ai-faqs
ms.topic: article
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bholtorf
ms.collection:
  - bap-ai-copilot
---

# <a name="faq-for-mapping-e-documents-with-purchase-orders-using-copilot-preview"></a>Ofte stillede spørgsmål om tilknytning af e-dokumenter med indkøbsordrer vha. Copilot (forhåndsversion)

[!INCLUDE[preview-banner](includes/preview-banner.md)]

Disse ofte stillede spørgsmål beskriver AI-effekten af **Hjælp til matchning af e-dokumenter**-funktionen i [!INCLUDE [prod_short](includes/prod_short.md)].

[!INCLUDE[production-ready-preview-dynamics365](includes/production-ready-preview-dynamics365.md)]

## <a name="what-is-e-documents-matching-assistance"></a>Hvad er Hjælp til matchning af e-dokumenter?

Elektroniske dokumenter (e-dokumenter) er basis for moderne forretningstransaktioner. De repræsenterer kritisk papirarbejde som fakturaer og kvitteringer, der flyder i begge retninger gennem levering og modtagelse. Du kan generere og overføre elektroniske fakturaer digitalt i et struktureret format, der letter automatiseret fakturabehandling. Håndtering af indgående digitale fakturaer kan dog være mere indviklet for kreditorteams.  

I små og mellemstore virksomheder (SMB'er) spiller kreditorteamet en afgørende rolle i nøjagtig sporing af leverandørforpligtelser. Deres primære ansvar er at registrere indgående fakturaer nøjagtigt. Det kan kræve en indsats at opnå præcision, især når de afstemmer eksterne fakturaer fra leverandører med eksisterende indkøbsordrer. Uoverensstemmelser i koder, beskrivelser og måleenheder giver ofte udfordringer, fordi disse elementer muligvis ikke stemmer overens på tværs af forskellige systemer og virksomheder. Uventede omkostninger, f.eks. transportgebyrer, kan også vises som separate linjeposter, der skal justeres manuelt. Revisorer skal også medtage fakturanumre og datoer i dokumenterne. Det er vigtigt, at forholdet mellem indkøbsordrer og eksterne fakturaer ikke altid er en-til-en. Du modtager muligvis flere eksterne fakturaer for samme købsordre.

Historisk set [!INCLUDE [prod_short](includes/prod_short.md)] kunne generere nye købsfakturaer baseret på modtagne elektroniske fakturaer. Manuel matchning af fakturaer med eksisterende indkøbsordrer var imidlertid en tidskrævende og fejlbehæftet proces.

**Hjælp til matchning af e-dokumenter** bruger generativ AI til at strømline denne proces ved at automatisere analysen af eksterne elektroniske fakturaer. Funktionen giver revisorer mulighed for at bede Copilot om at matche linjer på indgående elektroniske fakturaer med linjer på købsordrer i [!INCLUDE [prod_short](includes/prod_short.md)].

## <a name="what-are-capabilities-of-the-e-documents-matching-assistance"></a>Hvilke funktioner findes der i Hjælp til matchning af e-dokumenter?

Copilot yder AI-drevet assistance til at matche modtaget digital faktura med eksisterende indkøbsordrer i [!INCLUDE [prod_short](includes/prod_short.md)]. Copilot matcher linjer baseret på følgende:

- Lighed mellem beskrivelser
- Måleenhed
- Mængder, der kan faktureres
- Beløb

Copilot identificerer lignende beskrivelser, hvis de har korrekt måleenhed og priser, men det kan også finde match i mere komplekse tilfælde. Den kan f.eks. identificere, om der i en elektronisk faktura er to linjer med en variant af samme vare og kun én linje i købsordren. [!INCLUDE [prod_short](includes/prod_short.md)] matcher disse linjer, så længe beskrivelserne er ens, og priserne er de samme.

Copilot opretter ikke forbindelse til din e-dokumentslutpunktstjeneste for at hente eller sende digitale kuponer. Denne opgave forbliver fuldt ud under din kontrol og er en forudsætning for at bruge Copilots assistance. Dette gælder, uanset om de digitale dokumenter tilføjes [!INCLUDE [prod_short](includes/prod_short.md)] ved hjælp af en forbindelse til en slutpunktstjeneste eller angives manuelt.  

## <a name="what-is-the-intended-use-of-the-e-documents-matching-assistance"></a>Hvad er den tilsigtede brug af Hjælp til matchning af e-dokumenter?

Målet med funktionen **Hjælp til matchning af e-dokumenter** er at hjælpe kreditorteamet med at matche eksisterende købsordrer med indgående elektroniske fakturaer. Meget af denne aktivitet drejer sig om strengmatchning. [!INCLUDE [prod_short](includes/prod_short.md)] tilbyder en funktion, der automatiserer noget af denne aktivitet, og LLM'er er blevet identificeret som en mulighed for at supplere denne funktion og yderligere reducere manuel indsats.  

## <a name="how-was-e-documents-matching-assistance-evaluated-what-metrics-are-used-to-measure-performance"></a>Hvordan blev Hjælp til matchning af e-dokumenter evalueret? Hvilke metrikværdier bruges til at måle ydeevnen?

Denne funktion blev testet ved hjælp af kombinationer af følgende oplysninger:

- Eksterne varebeskrivelser
- Måleenhed
- Mængder og beløb
- Standardvarebeskrivelser
- Forskellige sprog
- Andre parametre, der dækker de typiske variationer og datagrænser for hvert felt 

Testdata repræsenterer både typisk brug og brug af dårlige aktører. Ydeevnen blev målt sammenlignet med manuel matchning af de samme data i elektroniske fakturaer og købsordrer.

## <a name="what-are-the-limitations-of-e-documents-matching-assistance-how-can-users-minimize-the-impact-of-the-e-documents-matching-assistance-limitations-when-using-the-system"></a>Hvilke begrænsninger findes der i Hjælp til matchning af e-dokumenter? Hvordan kan brugerne minimere virkningen af Hjælp til matchning af e-dokumentbegrænsningerne, når de bruger systemet?

**Hjælp til matchning af e-dokumenter** fungerer bedst, når eksterne (e-faktura) og interne ([!INCLUDE [prod_short](includes/prod_short.md)]) varebeskrivelser og enheder alle er på samme sprog. Blandede sprog eller blandet sprog i varebeskrivelser resulterer ofte i færre matches og forslag.  

Den foreslåede matchning af varer fra e-fakturaer med varer i købsordrer fungerer bedst på engelsk. Selvom du kan bruge denne funktion på alle sprog, som [!INCLUDE [prod_short](includes/prod_short.md)] understøtter, kan du opleve færre varematch på andre sprog.

## <a name="in-which-geographies-and-languages-is-e-documents-matching-assistance-available"></a>I hvilke geografiske områder og på hvilke sprog er Hjælp til matchning af e-dokumenter tilgængelig?

Denne funktion er tilgængelig for alle miljøer, lande-/områdelokaliseringer og på alle brugersprog med undtagelse af Canada. På grund af begrænset sprogunderstøttelse vil funktionen i første omgang ikke være tilgængelig for canadiske kunder på grund af overholdelse af lovgivningsmæssige sprog. 

For kundemiljøer, der er placeret i lande/områder, hvor Azure OpenAI-tjenesten ikke er udrullet, skal denne funktion være tilgængelig for administratorer først give samtykke til, at data flyttes på tværs af grænser for [!INCLUDE [prod_short](includes/prod_short.md)] for at oprette forbindelse til Azure OpenAI-tjenesten.  

Du kan finde flere oplysninger om sprog ved at gå til [Hvad er begrænsningerne ved Hjælp til matchning af e-dokumenter? Hvordan kan brugerne minimere virkningen af begrænsningerne for hjælp til matchning af e-dokumenter, når de bruger systemet?](#what-are-the-limitations-of-e-documents-matching-assistance-how-can-users-minimize-the-impact-of-the-e-documents-matching-assistance-limitations-when-using-the-system).   

## <a name="what-operational-factors-and-settings-allow-for-effective-and-responsible-use-of-the-feature"></a>Hvilke driftsmæssige faktorer og indstillinger gør det muligt at bruge funktionen på en effektiv og ansvarlig måde?

Copilot supplerer den kortlægningsalgoritme, der [!INCLUDE [prod_short](includes/prod_short.md)] allerede leverer, og kortlægger de linjer, som algoritmen ikke gjorde.

### <a name="what-is-expected-of-users-while-using-e-documents-matching-assistance"></a>Hvad forventes der af slutbrugere, når de bruger Hjælp til matchning af e-dokumenter?

<!--Not sure that this is the right content for this section. Seems like it belongs more in the overview article because it's more related to how to use the feature-->

Når du har knyttet indgående elektroniske fakturaer til købsordrer, skal du knytte linjerne på dokumenterne sammen.

Siden **Købsordretilknytning** viser alle linjer fra begge dokumenter. Her kan du lave kortlægningen manuelt, hvilket kan være svært, hvis der er mange linjer.

Du kan bruge **Hjælp til matchning af e-dokumenter** til at kortlægge linjer ud fra følgende kriterier:

- Lighed i deres beskrivelser
- Måleenhed
- Mængder, der kan faktureres
- Beløb

Copilots matches kan være forkerte eller ufuldstændige. Du bør altid gennemgå deres nøjagtighed, før du vælger at beholde dem. Copilots matches og forslag gemmes i [!INCLUDE [prod_short](includes/prod_short.md)], når du vælger **Behold det** og afslut Copilot. Du kan også redigere og rette eventuelle matches eller forslag, før du vælger at beholde dem. 

### <a name="what-is-expected-of-administrators-and-users-when-operating-e-documents-matching-assistance"></a>Hvad forventes der af administratorer og slutbrugere, når du hjælper med at betjene Hjælp til matchning af e-dokumenter?

Slutbrugere, såsom revisorer, kasserere eller andre, der modtager e-fakturaer, bør altid gennemgå nøjagtigheden af matches og forslag fra Copilot, før de vælger at beholde dem. Det anbefales, at du gennemser købsordrelinjerne for at kontrollere deres nøjagtighed og finde eventuelle uoverensstemmelser. Du bestemmer, om du vil bruge **Hjælp til matchning af e-dokumenter**. Selv når funktionen **Hjælp til matchning af e-dokumenter** er aktiveret af administratorer og tilgængelig, kan du vælge at bruge den altid, nogle gange eller aldrig.  

Administratorer træffer den overordnede beslutning om, hvorvidt Copilot i [!INCLUDE [prod_short](includes/prod_short.md)]. Hvis de aktiverer Copilot, skal administratorer sørge for at give adgang til de relevante brugere.

> [BEMÆRK!]
> - Vi understøtter ikke denne funktion for [!INCLUDE [prod_short](includes/prod_short.md)] i det lokale miljø eller private cloudmiljø.
> - Partnere kan ikke udvide denne funktion. Partnerudviklere kan ikke ændre, erstatte eller udvide funktionen. 

## <a name="is-copilot-the-only-way-to-match-e-documents-to-purchase-orders"></a>Er Copilot den eneste måde at matche e-dokumenter med indkøbsordrer på?

Nej, om du bruger Copilot er op til dig. [!INCLUDE [prod_short](includes/prod_short.md)] tilbyder ikke-AI-drevne måder at matche varer fra modtaget elektronisk faktura med varer på indkøbsordrer i [!INCLUDE [prod_short](includes/prod_short.md)]. Organisationer kan også bruge begge metoder på samme tid.  

## <a name="how-do-i-give-feedback-about-ai-generated-content"></a>Hvordan giver jeg feedback om AI-genereret indhold?

Hver gang Copilot giver matches eller forslag, kan du give feedback til Microsoft direkte fra Copilot-vinduet ved hjælp af kontrolelementerne Synes godt om og Afvis. Dit feedback forbliver anonymt, og vi bruger disse data til at evaluere og forbedre kvaliteten af tjenesten.  

## <a name="see-also"></a>Se også

[E-dokumenter-oversigt](finance-edocuments-overview.md)
[Tilknyt e-dokumenter til at købe ordrelinjer med Copilot](map-edocuments-with-copilot.md)

[!INCLUDE[footer-include](includes/footer-banner.md)]
