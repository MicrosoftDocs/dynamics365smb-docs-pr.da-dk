---
title: Ofte stillede spørgsmål om analyseassistent (forhåndsversion)
description: 'Disse ofte stillede spørgsmål indeholder oplysninger om den AI-teknologi, der bruges til at analysere data på sider i Business Central. De indeholder vigtige overvejelser og detaljer om, hvordan AI bruges, hvordan det blev testet og evalueret, og eventuelle specifikke begrænsninger.'
ms.date: 06/13/2024
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

# Ofte stillede spørgsmål om analyseassistent (forhåndsversion)

[!INCLUDE [preview-banner](~/../shared-content/shared/preview-includes/preview-banner.md)]

Disse ofte stillede spørgsmål beskriver AI-effekten af AI-funktionen i analyseassistentfunktionen i [!INCLUDE[prod_short](includes/prod_short.md)].

[!INCLUDE [preview-note](~/../shared-content/shared/preview-includes/production-ready-preview-dynamics365.md)]

## Hvad er analyseassistent?

Analyseassistent er en copilot, der yder hjælp til at arbejde med [dataanalysetilstanden](analysis-mode.md) i Business Central. Dataanalysetilstanden giver dig mulighed for at organisere, samle og opsummere data på sider og forespørgsler for at gøre dem mere velegnede til analyse og udtrækning af meningsfuld indsigt. Med Analyseassistent kan du automatisk oprette en visning af de data, du vil analysere, ved at udtrykke dine behov i et enkelt, naturligt sprog som f.eks. "Vis leverandører efter lokation sorteret efter antal køb". Analyseassistenten gør det nemmere at arbejde med data uden behov for komplekse tekniske færdigheder.

## Hvad er funktionerne i analysehjælp?

Analyseassistenten bygger på udviklerværktøjerne til Copilot i Business Central. Den bruger Azure OpenAI-servicen til at konvertere ustrukturerede instruktioner til et struktureret design til visning af data i analysetilstand uden at oprette, ændre eller opdatere selve kundens forretningsdata.

## Hvad er den tilsigtede brug af analysehjælp?

Analyseassistent hjælper med at oprette analysefaner i dataanalysetilstand for at præsentere data på en måde, der gør det lettere at drage konklusioner. Det er dog vigtigt at bemærke, at analysehjælp ikke giver direkte indsigt eller konklusioner om dataene. Det er et værktøj, der hjælper brugerne med at organisere og se deres data. Det er op til brugeren at udtrække handlingsrettede oplysninger, opdage tendenser og træffe informerede beslutninger for at skabe forretningsværdi.

## Hvordan blev analysehjælp evalueret? Hvilke metrikværdier bruges til at måle ydeevnen?

- Den funktion undergik omfattende test baseret på [!INCLUDE[prod_short](includes/prod_short.md)]-demonstrationsdata og andre fiktive produktkataloger. Copilot fik adskillige prompter i de understøttede engelske lokaliteter. Prompterne dækkede en bred vifte af dataanalyseinstruktioner og måder at udtrykke hensigt på. Resultaterne blev evalueret i forhold til nøjagtighed, relevans og sikkerhed.

- Denne funktion er bygget i overensstemmelse med ansvarlig brug af AI-standard i Microsoft. [Få mere at vide om ansvarlig AI fra Microsoft.](https://aka.ms/RAI)

## Hvordan overvåger Microsoft kvaliteten af genereret indhold?

Microsoft har forskellige systemer på plads for at sikre, at indhold, der genereres af Copilot, er af højeste kvalitet, registrerer misbrug og sikrer sikkerheden for vores kunder og deres data.

Brugere har mulighed for at give feedback til alle Copilot-svar og rapportere unøjagtigt eller upassende indhold for at hjælpe Microsoft med at forbedre denne funktion.

- Hvis du støder på upassende genereret indhold, skal du rapportere det til Microsoft ved hjælp af denne feedbackformular: [Rapportér misbrug](https://go.microsoft.com/fwlink/?linkid=2249810)

- Vi analyserer brugerfeedback på funktionen og bruger den til at hjælpe os med at forbedre svarene.

  Du giver feedback ved at bruge ikonet synes godt om (tommelfinger op) eller antipati (tommelfinger ned) på **Copilot-ruden** i [!INCLUDE[prod_short](includes/prod_short.md)].

- Microsoft deaktiverer muligvis de Copilot-drevne funktioner for udvalgte kunder, hvis der registreres misbrug af funktionaliteten.

## Hvad er begrænsningerne af analysehjælp? Hvordan kan brugerne minimere virkningen af analysebegrænsningerne, når de bruger systemet?

- Generelle AI-begrænsninger:

  AI-systemer er værdifulde værktøjer, men de er ikke-deterministiske. Det indhold, de genererer, er muligvis ikke nøjagtigt. Hvis det er vigtigt at bruge din dømmekraft til at gennemgå og verificere svar, før du træffer beslutninger, der kan påvirke interessenter som kunder og partnere.

- Tilgængelige sprog

   [!INCLUDE[analysis-assist-language-support](includes/analysis-assist-language-support.md)]

   Kvaliteten af svarene kan også være lavere, hvis sprogindstillingen for brugeren i Business Central adskiller sig fra det primære sprog for forretningsdataene i [!INCLUDE[prod_short](includes/prod_short.md)]-databasen.
  
- Geografisk begrænsning:
  
   Denne funktion er tilgængelig i alle understøttede [Business Central-lande/områder](/dynamics365/business-central/dev-itpro/compliance/apptest-countries-and-translations).<!-- except for Canada-->. Men funktionen bruger Microsoft Azure OpenAI-tjenester, som i øjeblikket kun er tilgængelig for Business Central i nogle geografiske områder. Hvis dit miljø er placeret i et land/område, hvor Azure OpenAI-tjeneste ikke er tilgængelig, skal administratorer tillade, at data flyttes på tværs af geografiske områder. Få mere at vide om [Copilot-dataflytning på tværs af geografiske områder](/dynamics365/business-central/ai-copilot-data-movement).

- Visse branche-, produkt- og emnebegrænsninger:

  Organisationer, der opererer inden for nogle forretningsområder, såsom medicinsk, narkotika, juridisk og våben, kan opleve lavere servicekvalitet.

## Hvilke data indsamler analyse, og hvordan bruges den?

Analysehjælp-funktionen indsamler de data, der som minimum kræves af Business Central for at kunne tilbyde tjenesten. Microsoft bruger ikke dine virksomhedsdata, herunder den tekst, du sender til Copilot, til at træne de grundlæggende modeller til gavn for andre. Du kan finde flere oplysninger i [Dynamics 365-vilkår for Azure OpenAI-drevne funktioner](https://go.microsoft.com/fwlink/?linkid=2236010).

Det indsamler også data fra den feedback, brugere kan give, ved hjælp af ikonerne synes godt om (tommelfinger op) eller antipati (tommelfinger ned) øverst på siden **Copilot**. Dataene er anonyme og omfatter valget af synes om eller synes ikke om, hvis den leveres, og Copilot-funktionen, som feedbacken gælder for.

## Se også

[Analysere data med Copilot (forhåndsversion)](analysis-assist.md)
