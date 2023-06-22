---
title: Oversigt over AI-styret marketingtekst med element (forhåndsversion) med Copilot
description: 'Få overblik over de AI-funktioner, der genereres som indhold i Business central'
author: jswymer
ms.author: jswymer
ms.reviewer: jswymer
ms.topic: overview
ms.date: 03/16/2023
ms.custom: bap-template
---
# <a name="overview-of-ai-powered-item-marketing-text-preview-with-copilot" />Oversigt over AI-styret marketingtekst med element (forhåndsversion) med Copilot

[!INCLUDE[ai-preview](includes/ai-preview.md)]

Denne artikel giver en oversigt over den AI-drevne facilitet, der leveres af CoPilot, i Business central.

## <a name="what-is-ai-powered-item-marketing-text-with-copilot" />Hvad er AI-drevet marketingtekst med Copilot

CoPilot giver mulighed for AI-drevet skrivning til Business Central-brugere, som har ansvaret for at udarbejde marketingtekst (produktbeskrivelser) på varer, der sælges i onlinebutikker, som Shopify. Med et klik på en knap genereres CoPilot tekst, der har spændende, kreative og centrale punkter for det specifikke element. Med en smule korrektur og redigering er den klar til at blive udgivet.

CoPilot bruger [Microsoft Azure OpenAI service](/azure/cognitive-services/openai/overview) til at få adgang til de sprogmodeller, der genkender, forudsiger og genererer tekst, der er baseret på oplærte datasæt.

<br><br>  

> [!Video https://www.microsoft.com/en-us/videoplayer/embed/RWZdAr]

*Videoen afspejler ikke nøjagtigt, hvordan funktionen arbejder i øjeblikket, eller ser ud i produktet. Funktionen er lidt ændret, siden videoen blev fremstillet. Men det giver dig en generel ide om funktionen, og hvad du kan bruge den til.*
  
## <a name="where-its-used" />Hvor den bruges

Copilot er tilgængelig til varekort i Business Central. I Business Central er varer som produkter i andre programmer og butikker. Hver vare kan administreres fra et kort, hvor du angiver oplysninger om varen, f.eks. dimensioner, omkostninger eller billede. Dette kort indeholder også en boks til angivelse af marketingtekst. Denne marketingtekst kan udgives på din online-butik for at gøre reklame for varen. Her får du brug for Copilot. Hvis du blot vælger handlingen **Opret med CoPilot** på varekortet, vil CoPilot oprette en intelligent kladdetekst for dig. Når du har hentet den første kladde, kan du køre CoPilot igen og igen, indtil du får en kladde, du synes om. Når du har et forslag, du kan lide, kan du gennemse og redigere den for at opnå en nøjagtighed og derefter gemme det.

Hvis Business Central er konfigureret til at oprette forbindelse til din onlinebutik på Shopify, kan du gøre denne tekst endnu bedre ved at udgive den med emnet direkte ved at vælge **Tilføj til Shopify**.

## <a name="why-and-how-to-use-it" />Hvorfor bruge den, og hvordan

AI-genereret tekst kan hjælpe med at accelerere fremtiden for produkter på onlinebutikker ved at begrænse den tid, der bruges på kopiskrivning. Nogle vigtige fordele omfatter:

- Hjælper brugere med at overvinde skriverens blok ved at få dem startet med et intelligent udkast
- Oplåsning af kreativitet for at kunne levere mere spændende produktbeskrivelser
- Forbedrer konsistensen af marketingindhold til produktlinjer

Du bør overveje den AI-genererede tekst som **kun forslag**. Forslagene kan i visse tilfælde indeholde fejl og meget upassende tekst, så der kræves overblik og gennemgang af mennesker. Før du gør teksten offentligt tilgængelig, skal du gennemse den for at sikre, at du har de nødvendige ændringer.

## <a name="current-limitations" />Hvad er nuværende begrænsninger

I dette afsnit forklares de aktuelle begrænsninger for funktionen AI-genereret tekst, som leveres af CoPilot.

- AI-genererede tekstforslag er kun på engelsk.
- Dårlige forslag kan resultere i, at vague eller generiske produktnavne bruges, og der mangler specifikke oplysninger om et element, f. eks. nøgleattributter eller en kategori.
- CoPilot understøttes kun i forbindelse med Business central online-prøveversioner og sandkassemiljøer - ikke i produktionsmiljøer, private cloudmiljøer eller virksomhedscentrale miljøer.
- CoPilot understøttes ikke via forbindelser til din egen Azure OpenAI-tjenesteressource i dit Azure-abonnement.
- Partner udvidelser af AI-muligheden ved hjælp af AL-kode understøttes ikke.

## <a name="next-steps" />Næste trin

For at komme i gang skal du bruge en dedikeret version af Business Central forhåndsversion, som er aktiveret med CoPilot.

- Hvis du allerede er en central kunde hos Business Central, skal din Business Central-administrator konfigurere forhåndsversionen i et sandkassemiljø til dig.
- Hvis du ikke er Business Central-kunde, men gerne vil prøve det, kan du tilmelde dig og få en gratis prøveversion.

Yderligere oplysninger finder du i [Hent Business Central-forhåndsversion - CoPilot-udgave](ai-preview-getstarted.md).  

## <a name="see-also" />Se også

[Konfigurere marketingtekst med AI-styret vare som en administrator](enable-ai.md)  
[Oprette marketingtekst med CoPilot](item-marketing-text.md)  
[AI-drevet varemarketingtekst med Copilot, ofte stillede spørgsmål](ai-faq.md)  
[Kom i gang med Shopify-connectoren](shopify/get-started.md)  
