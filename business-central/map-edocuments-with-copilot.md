---
title: Knytte e-dokumenter til købsordrelinjer med Copilot
description: 'Få mere at vide om, hvordan du bruger Copilot til at knytte e-dokumenter til købsordrelinjer.'
author: brentholtorf
ms.author: bholtorf
ms.reviewer: altotovi
ms.topic: how-to
ms.collection:
  - get-started
  - bap-ai-copilot
ms.date: 02/23/2024
ms.custom: bap-template
---

# Knytte e-dokumenter til købsordrelinjer med Copilot (forhåndsversion)

[!INCLUDE[preview-banner](includes/preview-banner.md)]

Efterhånden som indkøbsprocesserne bliver mere digitale, spiller e-dokumentfunktionen i Business Central en central rolle i automatiseringen af modtagelsen og behandlingen af kreditorfakturaer. Copilot kan hjælpe med denne proces ved at forbedre tilknytningen og matchningen af kreditorfakturaer med købsordrer. Dette reducerer tidskrævende opgaver, der normalt ville indbefatte omfattende søgning, opslag og dataindtastning. Fordelen bliver større af det faktum, at kreditorfakturaer ofte ikke relateret præcist til indkøbsordrer, i hvilket tilfælde Copilot er bedre til at identificere de tilsvarende indkøbsordrer. Forbedrede matchingsfunktioner gavner især små og mellemstore organisationer, der har brug for effektiv dokumentsporing for indkøbsordrelinjer. Copilot er den AI-drevne assistent til arbejde, der øger kreativiteten og forbedrer produktiviteten for Business Central-brugere.

> [!IMPORTANT]
> - Det er en produktionsklar prøveversionsfunktion til produktions- og sandkassemiljøer i alle landes lokaliseringer med undtagelse af Canada.
> - De supplerende vilkår for anvendelse i en produktionsklar forhåndsversion. Flere oplysninger: [Supplerende vilkår for anvendelse af Dynamics 365 Forhåndsversion](https://go.microsoft.com/fwlink/?linkid=2105274)
> - AI-genereret indhold kan være forkert.

I den første version af appen **e-dokument** introducerede vi grundlæggende scenarier for e-dokumenter for hele salgsprocessen. Der er dog behov for forbedringer og automatisering i håndteringen af de modtagne dokumenter, især i forbindelse med købsprocesser. Copilot forfiner, hvordan du administrerer e-dokumenter i købsprocessen, især med hensyn til indkøbsordrer. Med strukturen i e-dokumenter kan du angive den type købsdokument, der skal oprettes for hver kreditor, når du modtager e-fakturaer fra dem. Tidligere var den eneste mulighed at oprette en købsfaktura, enten som et dokument eller en finanskladde.

Du kan nu opdatere en eksisterende indkøbsordre i Business Central med de oplysninger, der modtages i e-fakturaen.

<!--
> [!NOTE]
> - This feature is available as a production-ready preview for production and sandbox environments in any country localization, with the exception of Canada. Production-ready previews are subject to supplemental terms of use. For more information, see [Supplemental terms of use for Dynamics 365 preview](https://go.microsoft.com/fwlink/?linkid=2105274).
> - AI-generated content may be incorrect.-->


## Identificere købsordrer

Først kan du identificere de købsordrer, som du kan matche automatisk.

## Tilknytte linjer

Copilot hjælper dig med automatisk at matche e-fakturalinjer med indkøbsordrelinjer og tilbyder ekstra matchende intelligens for at forbedre matchene.

Når de er matchet og tilknyttet, opdaterer Business Central den matchede købsordre med de relevante modtagelsesoplysninger for at sikre, at de rigtige antal er modtaget på ordrelinjerne.

## Se også

[Oversigt over e-dokumenter](finance-edocuments-overview.md)  
[Bruge e-dokumenter i salg og køb](finance-how-use-edocuments.md)  
[Fejlfinde Copilot- og AI-funktioner](ai-copilot-troubleshooting.md)  
[Ofte stillede spørgsmål om ansvarlig AI til hjælp til bankafstemning](faqs-bank-reconciliation.md)  
