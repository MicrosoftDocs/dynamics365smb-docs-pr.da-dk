---
title: Foreslå salgslinjer med Copilot
description: 'Lær, hvordan du foreslår linjer på salgsordrer med Copilot.'
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bholtorf
ms.topic: how-to
ms.search.keywords: 'Copilot, AI, sell'
ms.search.form: null
ms.date: 02/02/2024
ms.service: dynamics-365-business-central
ms.custom: bap-template
ms.collection: bap-ai-copilot
---

# <a name="suggest-lines-on-sales-documents-with-copilot-preview"></a>Foreslå linjer på salgsdokumenter med Copilot (forhåndsversion)

[!INCLUDE [preview-banner](~/../shared-content/shared/preview-includes/preview-banner.md)]

I denne artikel forklares det, hvordan du hurtigere kan oprette salgsdokumenter ved at lade Copilot foreslå de varer, der skal føjes til linjerne i salgsdokumenter til dine kunder.

[!INCLUDE [preview-note](~/../shared-content/shared/preview-includes/production-ready-preview-dynamics365.md)]

## <a name="about-sales-line-suggestions-with-copilot"></a>Om forslag til salgslinje med Copilot

Forslag til salgslinjer med Copilot kan hjælpe med at oprette linjer i salgsdokumenter, f.eks. salgstilbud, ordrer og fakturaer baseret på struktureret input eller naturligt sprog. Funktionen er ikke til generel chat, men en meget specifik og integreret oplevelse, som du kan bruge på salgsdokumenter. Funktionen tilbyder to forskellige færdigheder, der hjælper dig med at finde data om individuelle produkter eller hele dokumenter.

* Find produkter

  Oplysninger, der beskriver produkter, gemmes flere steder i [!INCLUDE [prod_short](includes/prod_short.md)]. Varenumre og beskrivelser gemmes f.eks. i tabellen **Vare**, flere stregkoder gemmes i tabellen **Varereference**, og produktegenskaber gemmes i tabellen **Vareattributter**. Selvom du måske beder om *rød cykel*, kan det faktiske produkt være *Crimson tourer*, hvor *cykel* er en produktkategori, og *rød* er en attribut.

* Søg efter dokumenter efter reference

  Folk gentager ofte en tidligere ordre eller bruger den i det mindste som udgangspunkt. Men det kan være vanskeligt at finde den rigtige ordre i en bunke af ordrer. Du husker måske noget af ordrens id, som kan være et nummer tildelt af virksomheden eller et referencenummer, der er modtaget fra en kunde. Hvis du bruger prompter som f.eks. *Skal bruge faktura fra april*, kan det hjælpe dig med at finde en ordre hurtigere.

## <a name="available-languages"></a>Tilgængelige sprog

[!INCLUDE[sales-lines-suggestions-language-support](includes/sales-lines-suggestions-language-support.md)]

## <a name="prerequisites"></a>Forudsætninger

* Salgslinjeforslag med Copilot muliggøres og aktiveres af en administrator. Du kan få mere at vide om, hvordan du aktiverer AI-funktioner, ved at gå til [Konfigurere Copilot- og AI-funktioner](enable-ai.md).
* Du er fortrolig med oprettelse af salgsordrer.

## <a name="examples-of-prompts"></a>Eksempler på prompter

Foreslå salgslinjer med Copilot kan håndtere en lang række promptinput. Dette afsnit indeholder nogle eksempler på prompter til forskellige scenarier, vi har testet.

### <a name="sample-inquiry-to-repeat-the-past-document"></a>Eksempelforespørgsel til gentagelse af det forrige dokument

Prompt: *Skal bruge alle produkterne fra faktura 103031*

### <a name="during-phone-call-user-quickly-types-list-of-required-products-and-quantities-not-always-accurate-enough-or-using-internal-product-names"></a>Under telefonopkald skriver brugeren hurtigt en liste over ønskede produkter og mængder, ikke altid nøjagtige nok eller ved hjælp af interne produktnavne

Prompt: *2 rød børncykle*

Bemærk, at prompten virker, selv med flere stavefejl.

### <a name="a-user-copies-an-inquiry-from-an-inbound-communication-and-pastes-it-to-the-sales-lines-suggestions-page"></a>En bruger kopierer en forespørgsel fra indgående kommunikation og indsætter den på siden Forslag til salgslinjer

Prompt: *Hej, jeg er interesseret i at købe noget tilbehør til min XXXX Laptop, såsom en trådløs mus, et tastaturcover og en taske til den bærbare. Jeg spekulerer på, om du har nogen anbefalinger eller forslag til disse emner. Har I særlige tilbud eller rabatter til loyale kunder som mig? Med venlig hilsen M*

Bemærk, at XXXX Laptop ikke er inkluderet i søgningen.

## <a name="suggest-lines-on-a-sales-document"></a>Foreslå linjer på et salgsdokument

Denne proces beskriver, hvordan du foreslår linjer på en salgsordre. Trinene er de samme for salgstilbud og fakturaer.

1. Vælg ![Lightbulb, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **Salgsordre**, og vælg derefter det relaterede link.
1. Åbn salgsordren.
1. I oversigtspanelet **Linjer** skal du vælge **Hent forslag til linjer**.
1. I vinduet **Foreslå linjer med Copilot** skal du indtaste din prompt eller vælge en fra promptguider.

## <a name="review-save-discard-or-regenerate-suggestions"></a>Gennemse, gem, kassér eller generer forslag igen

Når Copilot har foreslået de elementer, der skal føjes til linjerne, skal du gennemgå forslagene og beslutte, om de er, som du ønsker:

* Hvis du vil kassere et enkelt foreslået linje, skal du markere det på listen og derefter vælge handlingen **Slet linje**.
* Hvis du vil kassere alle foreslåede linjer og lukke Copilot-vinduet, skal du vælge knappen Kassér (papirkurv) ud for knappen **Behold den**.
* Hvis du vil overføre linjerne i Copilot-vinduet, skal du vælge **Behold den**. 

I feltet **Pålidelighed** vises scorerne **Høj (80+)**, **Medium (60-80)** og **Lav (60-)** score og henviser til linjer, der kræver opmærksomhed.

Dette trin bekræfter, at du vil overføre linjerne til et salgsdokument. Du kan også slette eller redigere de overførte linjer dér eller slette hele dokumentet.

## <a name="see-also"></a>Se også

[Ofte stillede spørgsmål om salgslinjeforslag med Copilot](faq-sales-suggest-sales-lines-with-copilot.md)
[Konfigurere Copilot- og AI-funktioner](enable-ai.md)
