---
title: Forslag til marketingtekst med Copilot-oversigt
description: 'Få overblik over de AI-funktioner, der genereres som indhold i Business central.'
author: jswymer
ms.author: jswymer
ms.reviewer: jswymer
ms.topic: overview
ms.date: 10/29/2023
ms.custom: bap-template
ms.collection:
  - bap-ai-copilot
---
# <a name="marketing-text-suggestions-with-copilot-overview"></a>Forslag til marketingtekst med Copilot-oversigt

<!--[!INCLUDE[ai-preview](includes/ai-preview.md)]-->

Denne artikel giver en oversigt over den AI-drevne facilitet, der leveres af Copilot, i Business central.

## <a name="what-is-ai-powered-item-marketing-text-with-copilot"></a>Hvad er AI-drevet marketingtekst med Copilot

Copilot giver mulighed for AI-drevet skrivning til Business Central-brugere, som har ansvaret for at udarbejde marketingtekst (produktbeskrivelser) på varer, der sælges i onlinebutikker, som Shopify. Med et klik på en knap genereres Copilot tekst, der er spændende og kreativ, og at centrale punkter for det specifikke element. Med en smule korrektur og redigering er den klar til at blive udgivet.

Copilot bruger [Microsoft Azure OpenAI-tjeneste](/azure/cognitive-services/openai/overview) til at få adgang til de sprogmodeller, der genkender, forudsiger og genererer tekst, der er baseret på oplærte datasæt.

<br><br>  

> [!Video https://www.microsoft.com/en-us/videoplayer/embed/RWZdAr]

*Videoen afspejler ikke nøjagtigt, hvordan funktionen arbejder i øjeblikket, eller ser ud i produktet. Funktionen er ændret, siden videoen blev fremstillet. Men det giver dig en generel ide om funktionen, og hvad du kan bruge den til.*
  
## <a name="where-its-used"></a>Bruges i

Copilot er tilgængelig til varekort i Business Central. I Business Central er varer som produkter i andre programmer og butikker. Hver vare kan administreres fra et kort, hvor du angiver oplysninger om varen, f.eks. dimensioner, omkostninger eller billede. Dette kort indeholder også en boks til angivelse af marketingtekst. Denne marketingtekst kan udgives på din online-butik for at gøre reklame for varen. Her får du brug for Copilot. Hvis du blot vælger handlingen **Udarbejd forslag med Copilot** på varekortet, vil Copilot oprette en intelligent kladdetekst for dig. Når du har hentet den første kladde, kan du køre Copilot igen og igen, indtil du får en kladde, du synes om. Når du har et forslag, du kan lide, kan du gennemse og redigere den for at opnå en nøjagtighed og derefter gemme det.

Hvis Business Central er konfigureret til at oprette forbindelse til din onlinebutik på Shopify, kan du gøre denne tekst endnu bedre ved at udgive den med emnet direkte ved at vælge **Tilføj til Shopify**.

## <a name="why-and-how-to-use-it"></a>Hvorfor bruge den, og hvordan

AI-genereret tekst kan hjælpe med at accelerere fremtiden for produkter på onlinebutikker ved at begrænse den tid, der bruges på kopiskrivning. Nogle vigtige fordele omfatter:

- Hjælper brugere med at overvinde skriverens blok ved at få dem startet med et intelligent udkast.
- Oplåsning af kreativitet for at kunne levere mere spændende produktbeskrivelser.
- Forbedrer konsistensen af marketingindhold til produktlinjer.

Du bør overveje den AI-genererede tekst som *kun forslag*. Forslagene kan i visse tilfælde indeholde fejl og meget upassende tekst, så der kræves overblik og gennemgang af mennesker. Før du gør teksten offentligt tilgængelig, skal du gennemse den for at sikre, at du har de nødvendige ændringer.

## <a name="current-limitations"></a>Gældende begrænsninger

I dette afsnit forklares de aktuelle begrænsninger for funktionen AI-genereret tekst, som leveres af Copilot.

- [!INCLUDE[copilot-supported-languages.md](includes/copilot-supported-languages.md)]
- Dårlige forslag kan resultere i, at vague eller generiske produktnavne bruges, og der mangler specifikke oplysninger om et element, f. eks. nøgleattributter eller en kategori.
- Copilot understøttes kun i Business central online-prøveversioner - ikke i private cloudmiljøer eller Business Central-lokale miljøer.
- Copilot understøttes ikke via forbindelser til din egen Azure OpenAI-tjenesteressource i dit Azure-abonnement.

<!-- Partner extensibility of the AI capability by using AL code isn't supported.-->

## <a name="next-steps"></a>Næste trin

For at komme i gang skal du bruge et Business Central (v23.1 og senere)-miljø, som er aktiveret med Copilot.

- Hvis du allerede er en kunde hos Business Central, skal din Business Central-administrator konfigurere et miljø, der er aktiveret til forslag til marketingtekst. Du kan finde flere oplysninger ved at gå til [Konfigurer Copilot- og AI-funktioner](enable-ai.md).

- Hvis du ikke er Business Central-kunde, men gerne vil prøve det, kan du tilmelde dig og få en gratis prøveversion. Du kan finde flere oplysninger i [Tilmeld dig en gratis Dynamics 365 Business Central-prøveversion](trial-signup.md).

Når du har et miljø eller spor, der er klar, skal du gå til [Føj marketingtekst til varer med Copilot](item-marketing-text.md).  

## <a name="see-also"></a>Se også

[Konfigurer Copilot- og AI-funktioner](enable-ai.md)  
[Tilføje marketingtekst til varer med Copilot](item-marketing-text.md)  
[Ofte stillede spørgsmål til forslag til marketingtekst](faqs-marketing-text.md)  
[Kom i gang med Shopify-connectoren](shopify/get-started.md)  
