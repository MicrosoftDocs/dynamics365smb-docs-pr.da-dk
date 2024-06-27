---
title: Afstemme bankkonti med Copilot (forhåndsversion)
description: 'Få mere at vide om, hvordan du kan bruge Copilot til at afstemme bankkonti i Business Central.'
author: jswymer
ms.author: jswymer
ms.reviewer: jswymer
ms.topic: how-to
ms.collection:
  - get-started
  - bap-ai-copilot
ms.date: 06/13/2024
ms.custom: bap-template
---

# Afstemme bankkonti med Copilot (forhåndsversion)

[!INCLUDE [preview-banner](~/../shared-content/shared/preview-includes/preview-banner.md)]

I denne artikel forklares det, hvordan du kan bruge hjælp til afstemning af bankkonto som en hjælp til at afstemme banktransaktioner med finansposter i Microsoft Dynamics 365 Business Central.

[!INCLUDE [preview-note](~/../shared-content/shared/preview-includes/production-ready-preview-dynamics365.md)]

## Om hjælp til afstemning af bankkonto

Hjælp til bankkontoafstemning er et sæt funktioner, der drives af kunstig intelligens, og som hjælper dig med at afstemme bankkonti. Det tilbyder to forskellige opgaver gennem Copilot:

- Forbedret matchning af transaktioner med poster

    Du kender måske allerede knappen **Afstem automatisk** på siden **Bankkontoafstemning**, der automatisk afstemmes med de fleste banktransaktioner med posterne. Vi henviser til denne operation som *automatisk*. Selvom automatch fungerer godt, kan de algoritmer, den bruger, nogle gange resultere i mange ikke-matchede transaktioner. Copilot bruger AI-teknologi til at inspicere disse ikke-matchede transaktioner og identificere flere matches baseret på datoer, beløb og beskrivelser. Hvis en debitor f.eks. betaler flere fakturaer som et engangsbeløb, afstemmer Copilot linjen med det enkelte bankkontoudtog med flere fakturaposter.

    [Få mere at vide om denne opgave](#reconcile-bank-accounts-with-copilot).

- Foreslåede finanskonti (G/L)

    For resterende banktransaktioner, der ikke kunne matches med nogen poster, sammenligner Copilot transaktionsbeskrivelsen med finanskontonavne for den mest sandsynlige finanskonto at bogføre til. Hvis ikke-matchede transaktioner har fortællingen *Fuel Stop24*, kan Copilot f.eks. foreslå, at du bogføre dem til kontoen *Transaktioner*.

    [Få mere at vide om denne opgave](#post-unmatched-bank-transaction-amounts-to-suggested-gl-accounts).

## Tilgængelige sprog

[!INCLUDE[bank-recon-assist-language-support](includes/bank-recon-assist-language-support.md)]

## Forudsætninger

- Hjælp til afstemning af bankkonto er aktiveret. En administrator skal afslutte denne opgave. [Få mere at vide om, hvordan du konfigurerer Copilot- og AI-funktioner](enable-ai.md).
- Bankkontiene i Business Central, som du vil afstemme, er knyttet til en onlinebankkonto, eller de er konfigureret med format til import af et bankkontoudtog.
- Du kender bankkontoafstemning i Business Central som beskrevet i [Afstem bankkonti](bank-how-reconcile-bank-accounts-separately.md).

## Afstemme bankkonti med Copilot

<!-- Similar to the **Match Automatically** capability on the **Bank Acc. Reconciliation** page, Bank account reconciliation assist can also automatically matches transactions in banks statements with bank entries. The difference is that **Match Automatically** uses a native rules-based algorithm, while Bank account reconciliation assist is based AI technology though Copilot. Bank account reconciliation assist is intended to supplement the **Match Automatically** capability. While **Match Automatically** is fairly successful at matching transactions, there are some instances where it can't&mdash;which is where Bank account reconciliation assist comes. By using the **Reconcile with Copilot** action on **Bank Acc. Reconciliation** page, you can find even more matches.-->

Copilot i bankkontoafstemning er beregnet som et supplement til automatchhandlingen. Når du derfor bruger Copilot, kører automatchhandlingen først for at foretage de første matches. Derefter kører Copilot for at forsøge at matche transaktioner, som automatchhandlingen ikke håndterede.

Du kan bruge to metoder til at afstemme bankkonti med Copilot:

- Brug Copilot til at starte en ny afstemning af en bankkonto direkte fra listen **Bankkontoafstemning** .
- Brug Copilot på en ny eller eksisterende afstemning på et **bankkontoafstemningskort** .

# [Fra listen Bankkontoafstemning](#tab/fromlist)

Til denne tilgang kan du oprette og afstemme en ny bankkontoafstemning fra bunden. Denne fremgangsmåde kræver, at du vælger bankkontoen. Hvis bankkontoen ikke er knyttet til en onlinebankkonto, skal du også importere bankkontoudtogsfilen.

1. Vælg ![Lightbulb, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **Bankkontoafstemninger**, og vælg derefter det relaterede link.
1. Vælg **Afstem med Copilot** for at åbne vinduet **Afstem med Copilot**.
1. Angiv feltet **Udfør afstemning for dette bankkontofelt** med den bankkonto, du vil afstemme.

    ![Skærmbillede, der viser vinduet Afstem med Copilot til afstemning fra bunden.](media/reconcile-bank-accounts-new-copilot.svg)

1. Hvis den valgte bankkontoen ikke er knyttet til en onlinebankkonto, kan du importere bankkontoudtogsfilen. Hvis du vil importere filen, skal du vælge værdien i feltet **Brug transaktionsdata fra** eller vælge papirclipsknappen ved siden af knappen **Generer**. Brug derefter **Vælg den fil, der skal importeres** til at importere bankkontoudtogsfilen ved at trække den fra enheden eller gennemse enheden.
1. Hvis du vil afstemme med Copilot, skal du vælge **Generer**.

    Copilot begynder at generere foreslåede matches. Når det er fuldført, viser vinduet **Afstem med Copilot** resultaterne af matchningsprocessen.

1. Gennemse de foreslåede matches som beskrevet i næste afsnit.

# [Fra et bankkontoafstemningskort](#tab/fromcard)

Til denne fremgangsmåde kan du bruge Copilot på en ny bankkontoafstemning, som du opretter manuelt, eller ved at redigere en eksisterende afstemning.

1. Vælg ![Lightbulb, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **Bankkontoafstemninger**, og vælg derefter det relaterede link.
1. Udfør ét af følgende trin:

    - Vælg **Ny** for at starte en ny afstemning.
    - Vælg, og åbn en eksisterende afstemning på listen.

1. På kortet **Bankkontoafstemning** skal du vælge **Afstem med Copilot**.

    ![Skærmbillede, der viser knappen Afstem med Copilot på kortet Bankkontoafstemning.](media/bank-reconciliation-copilot-card.svg)

    Copilot begynder at generere foreslåede matches. Når det er fuldført, viser vinduet **Afstem med Copilot** resultaterne af matchningsprocessen.

1. Gennemse de foreslåede matches som beskrevet i næste afsnit.
---

### Gennemgå, gem eller kassér foreslåede matches

Når du har kørt Copilot, viser vinduet **Afstem med Copilot** de detaljerede resultater, herunder eventuelle foreslåede matches. På nuværende tidspunkt er ingen match, som Copilot foreslog, blevet gemt. Derfor har du mulighed for at inspicere forslagene og gemme eller kassere dem, som du vil.

![Skærmbillede, der viser foreslåede matches i vinduet Afstem med Copilot. ](media/bank-reconciliation-copilot-window.png)

Vinduet **Afstem med Copilot** er opdelt i to sektioner. Den øverste del indeholder nogle generelle oplysninger om resultatet. Den nederste sektion **Matchet forslag** viser de matches, som Copilot har forslået.

I følgende tabel beskrives de felterne i den øverste sektion.

| Felt | Beskrivelse |
|---|---|
| Automatisk matchet | Antallet af kontoopgørelseslinjer, som automatchhandlingen matchede. Vælg værdien for at få vist afstemningskortet. |
| Copilot matchet | Det antal bankkontoudtogslinjer, som Copilot foreslog matches for. Du kan få vist detaljer om matchene i sektionen **Match forslag**. |
| Slutsaldo for kontoudtog | Slutsaldoen, der vises på bankens kontoudtog, og som du vil afstemme med. |
| Bogfør, hvis det er anvendt fuldt ud | Slå denne indstilling til, hvis du vil bogføre bankkontoafstemningen automatisk, når alle linjer (100 procent) er matchet, og du har valgt **Behold den**. |

I afsnittet **Match forslag** skal du gennemgå de foreslåede matches linje for linje. Udfør derefter den nødvendige handling:

- Hvis du vil kassere et enkelt foreslået match, skal du markere det på listen og derefter vælge **Slet linje**.
- Hvis du vil kassere alle foreslåede matches og lukke vinduet **Afstem med Copilot**, skal du vælge knappen Kassér (papirkurv) ![knappen Kassér.](media/copilot-delete-trash-can.png) ud for knappen **Behold den** nederst i vinduet.
- Hvis du vil bogføre den fuldt matchede afstemning automatisk, når du gemmer den, skal du aktivere indstillingen **Bogfør, hvis den er fuldt udlignet**.
- Hvis du vil gemme de matches, der aktuelt vises i vinduet **Afstem med Copilot**, skal du vælge **Behold det**.

## Bogfør ikke-matchede banktransaktionsbeløb til foreslåede finanskonti (G/L)

I dette afsnit beskrives, hvordan du bruger Copilot til at bogføre ikke-afstemte bankkontoudtogs linjebeløb (som angivet i feltet **Forskel**) i en finanskonto. Denne opgave kan kun udføres fra en eksisterende afstemning.

1. Gå til listen **Bankkontoafstemninger**, og åbn den eksisterende afstemning, der indeholder de ikke-afstemte linjer.

    Dette trin giver et klart overblik over alle ikke-afstemte bankkontoudtogslinjer, der skal overføres til finanskontoen.

1. I ruden **Bankkontoudtogslinjer** skal du identificere Ikke-matchede bankkontoudtogslinjer og vælge en eller flere linjer, som du vil afstemme.

    Copilot fokuserer på de valgte linjer til bogføring af nye betalinger på finanskontoen.

1. Vælg **Bogfør forskel til finanskonto** for at starte processen.

    ![Skærmbillede, der viser knappen Bogfør difference på finanskonto på kortet Bankkontoafstemning.](media/bank-reconciliation-transfer-gl-copilot-card.png)

    Copilot begynder at generere forslag til bogføring af nye betalinger.

1. Når Copilot er færdig med at generere forslag, åbnes vinduet **Copilot-finanskontooverførselsforslag**.

    Sektion **Matchet forslag** i dette vindue vises forslagene. Oplevelsen ligner oplevelsen af at forene sig med Copilot.

    ![Skærmbillede, der viser Copilot-forslagene for vinduet Bogføring af forskelle på finanskonti.](media/bank-reconciliation-gl-transfer-proposed-matches.png)

1. Gennemgå forslagene linje for linje for at sikre nøjagtigheden af de foreslåede betalinger til bogføring.

    - Hvis du analyserer forslaget ved at vælge det på listen, føres du til en liste over konti. Herfra kan du vælge en anden konto. Du kan gøre denne form for manuel rettelse kun, når du bruger flowet **Bogfør forskelle til finanskonto**, ikke matchingsflowet.
    - Hvis du vælger **Gem** ud for et forslag, kan du føje tilknytningen til siden **Tilknytning af tekst til konto**. Næste gang denne tekst vises under matchning, knyttes den til den foreslåede konto.

1. Kassér eller gem forslag.

    - Du kasserer et bestemt forslag ved at markere det på listen og derefter vælge handlingen **Slet linje**. Hvis du vil kassere alle forslag og lukke Copilot, skal du vælge knappen Kassér (skraldespand) ![knappen Kassér.](media/copilot-delete-trash-can.png) ud for knappen **Behold den** nederst i vinduet.
    - Hvis forslagene opfylder dine krav, og du vil gemme dem, skal du vælge **Behold det**.

         Dette trin bekræfter overførslen af de aktuelt valgte forslag fra bankkontoen til finanskontoen. Der bogføres nye betalinger på de foreslåede finanskonti, og der indsættes tilsvarende linjer i de oprettede bankkontoposter.

## Næste trin

[Validere din bankkontoafstemning](bank-how-reconcile-bank-accounts-separately.md#validate-your-bank-reconciliation)

## Se også

[Fejlfinde Copilot- og AI-funktioner](ai-copilot-troubleshooting.md)  
[Ofte stillede spørgsmål om ansvarlig AI til hjælp til bankafstemning](faqs-bank-reconciliation.md)  
[Konfigurere banktransaktioner](bank-setup-banking.md)  
[Afstemme bankkonti](bank-how-reconcile-bank-accounts-separately.md)  
[Udligne betalinger automatisk og afstemme bankkonti](receivables-apply-payments-auto-reconcile-bank-accounts.md)
