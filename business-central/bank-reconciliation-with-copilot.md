---
title: Afstemme ved hjælp af afstemning af bankkonti
description: 'Flere oplysninger om, hvordan du kan bruge Copilot til at afstemme bankkonti i Business Central.'
author: jswymer
ms.author: jswymer
ms.reviewer: jswymer
ms.topic: how-to
ms.collection:
  - get-started
  - bap-ai-copilot
ms.date: 04/15/2024
ms.custom: bap-template
---

# <a name="reconcile-bank-accounts-with-copilot-preview"></a>Afstemme bankkonti med Copilot (forhåndsversion)

[!INCLUDE[preview-banner](includes/preview-banner.md)]

I denne artikel forklares det, hvordan du bruger hjælp til afstemning af bankkonto som en hjælp til at afstemme banktransaktioner med finansposter i Business Central.

[!INCLUDE[production-ready-preview-dynamics365](includes/production-ready-preview-dynamics365.md)]

## <a name="about-bank-account-reconciliation-assist"></a>Om hjælp til afstemning af bankkonto

Hjælp til bankkontoafstemning er et sæt AI-drevne funktioner, der hjælper dig med at afstemme bankkonti. Hjælp til afstemning af bankkonto giver dig to forskellige opgaver via Copilot:

- Forbedret matchning af transaktioner med poster

   Du kender måske allerede handlingen **Afstem automatisk** på siden **Bankkontoafstemning**, der automatisk afstemmes med de fleste banktransaktioner med posterne. Vi henviser til denne operation som *automatisk*. Selvom automatch fungerer godt, kan de algoritmer, den bruger, nogle gange resultere i mange ikke-matchede transaktioner. Copilot bruger AI-teknologi til at inspicere resterende transaktioner og identificere flere matches baseret på datoer, beløb og beskrivelser. Hvis flere fakturaer f.eks. blev betalt som et engangsbeløb af en kunde, afstemmer Copilot linjen med det enkelte bankkontoudtog med flere fakturaposter.

   Gå til [Afstem bankkonti med Copilot](#reconcile-bank-accounts-with-copilot).

- Foreslåede finanskonti

  For resterende banktransaktioner, der ikke kunne matches med nogen poster, sammenligner Copilot transaktionsbeskrivelsen med finanskontonavne, hvilket foreslår den mest sandsynlige finanskonto at bogføre til. Copilot kan f.eks. foreslå, at transaktioner med fortællingen "Fuel Stop24" bogføres på kontoen "Transport".
  
   Gå til [Bogfør ikke-matchede banktransaktionsbeløb til foreslåede finanskonti](#post-unmatched-bank-transaction-amounts-to-suggested-general-ledger-accounts).

## <a name="prerequisites"></a>Forudsætninger

- Hjælp til afstemning af bankkonto er aktiveret. Denne opgave udføres af en administrator. [Få mere at vide om konfigurering af Copilot- og AI-funktioner](enable-ai.md).
- Bankkonti i Business Central, som du vil afstemme, er knyttet til en onlinebankkonto eller konfigureret med format til import af bankkontoudtog. 
- Du kender bankkontoafstemning i Business Central som beskrevet i [Afstem bankkonti](bank-how-reconcile-bank-accounts-separately.md). 

<!--H2s. Required. A how-to article explains how to do a task. The bulk of each H2 should be a procedure.-->
## <a name="reconcile-bank-accounts-with-copilot"></a>Afstemme bankkonti med Copilot

<!-- Similar to the **Match Automatically** capability on the **Bank Acc. Reconciliation** page, Bank account reconciliation assist can also automatically matches transactions in banks statements with bank entries. The difference is that **Match Automatically** uses a native rules-based algorithm, while Bank account reconciliation assist is based AI technology though Copilot. Bank account reconciliation assist is intended to supplement the **Match Automatically** capability. While **Match Automatically** is fairly successful at matching transactions, there are some instances where it can't&mdash;which is where Bank account reconciliation assist comes. By using the **Reconcile with Copilot** action on **Bank Acc. Reconciliation** page, you can find even more matches.-->

Copilot i bankkontoafstemning er beregnet til at blive brugt som et supplement til automatchhandlingen. Når du bruger Copilot, kører automatchhandlingen derfor først for at foretage de første matches. Derefter kører Copilot for at forsøge at matche transaktioner, som automatchhandlingen ikke håndterede.   

Der er to metoder til afstemning af bankkonti med Copilot. Du kan bruge Copilot til at starte en ny afstemning på en bankkonto direkte fra listen **Bankkontoafstemning**, eller du kan bruge Copilot på en ny eller eksisterende afstemning på **bankkontoafstemningskortet**.

# [Fra listen med bankkontoafstemninger](#tab/fromlist) 

Med denne tilgang kan du oprette og afstemme en ny bankkontoafstemning fra bunden. Denne fremgangsmåde kræver, at du vælger bankkontoen og importerer bankkontoudtogsfilen, hvis bankkontoen ikke er knyttet til en onlinekonto.

1. Vælg ![Lightbulb, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **Bankkontoafstemninger**, og vælg derefter det relaterede link. 
1. Vælg handlingen **Afstem med Copilot** for at åbnevinduet **Afstem med Copilot**.
1. Angiv feltet **Udfør afstemning for dette bankkontofelt** med den bankkonto, du vil afstemme.

   ![Viser vinduet Afstem med copilot til afstemning fra bunden](media/reconcile-bank-accounts-new-copilot.svg) 
 
1. Hvis den valgte bankkontoen ikke er knyttet til en onlinebankkonto, kan du importere bankkontoudtogsfilen. Hvis du vil importere filen, skal du enten vælge værdien i feltet **Brug transaktionsdata fra** eller vælge papirclipsknappen ved siden af knappen **Generer**. Brug derefter **Vælg den fil, der skal importeres** til at importere bankkontoudtogsfilen ved enten at trække den fra enheden eller gennemse enheden.
1. Hvis du vil afstemme med Copilot, skal du vælge **Generer**.

   Copilot begynder at generere foreslåede matches. Når det er fuldført, åbner vinduet Afstem med Copilot resultaterne af matchningsprocessen.

1. Gennemse de foreslåede matches som beskrevet i følgende afsnit.

# [Fra et bankkontoafstemningskort](#tab/fromcard) 

Med denne fremgangsmåde kan du bruge Copilot enten på en ny bankkontoafstemning, som du opretter manuelt, eller ved at redigere en eksisterende afstemning. 


1. Vælg ![Lightbulb, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **Bankkontoafstemninger**, og vælg derefter det relaterede link. 
1. Gør ét af følgende:

   - Vælg **Ny** for at starte en ny afstemning. 
   - Vælg og åbn en eksisterende afstemning på listen.
1. På kortet **Bankkontoafstemning** skal du vælge **Afstem med Copilot**

   ![Viser handlingen Afstem med copilot på kortet Bankkontoafstemning](media/bank-reconciliation-copilot-card.svg) 

   Copilot begynder at generere foreslåede matches. Når det er fuldført, åbner vinduet **Afstem med Copilot** resultaterne af matchningsprocessen. 

1. Gennemse de foreslåede matches som beskrevet i følgende afsnit. 
---

### <a name="review-save-or-discard-proposed-matches"></a>Gennemgå, gem eller kassér foreslåede matches

Når du har kørt Copilot, viser vinduet **Afstem med Copilot** de detaljerede resultater, herunder eventuelle foreslåede matches. På dette tidspunkt er ingen kampe foreslået af Copilot blevet gemt, så det giver dig mulighed for at inspicere forslagene og gemme eller kassere, som du vil.

![Viser vinduet Afstem med copilot med foreslåede matches](media/bank-reconciliation-copilot-window.png) 

Copilot-vinduet er opdelt i to sektioner. Den øverste del indeholder nogle generelle oplysninger om resultatet, som beskrevet i følgende tabel.  Den nederste sektion **Matchet forslag** viser de matches, der er foreslået af Copilot.

|Felt|Beskrivelse|
|-|-|
|Automatisk matchet|Angiver, hvor mange linjer i bankkontoen stemmer overens med automatchhandlingen. Vælg værdien for at få vist afstemningskortet.  |
|Copilot matchet|Angiver, hvor mange linjer i bankkontoen stemmer overens med forslag fra Copilot. Du kan se detaljer om kampene i afsnittet **Foreslåede matches**.|
|Slutsaldo for kontoudtog|Angiver slutsaldoen, der vises på bankens kontoudtog, og som du vil afstemme med|
|Bogfør, hvis det er anvendt fuldt ud|Aktivér denne knap, hvis du vil bogføre bankkontoafstemningen automatisk, når alle linjer (100 %) er matchet, og du har valgt **Behold den**.|

#### <a name="save-or-discard-proposed-matches"></a>Gem eller kassér foreslåede matches

I afsnittet **Matchede forslag** skal du gennemgå de foreslåede resultater linje for linje og derefter foretage den nødvendige handling:

- Hvis du vil kassere et enkelt foreslået match, skal du markere det på listen og derefter vælge handlingen **Slet linje**.

- Hvis du vil kassere alle foreslåede matches og lukke Copilot-vinduet, skal du vælge knappen Kassér (papirkurv) ![Viser skraldespandsikonet til sletning af alle Copilot-forslag til bankkontoafstemning](media/copilot-delete-trash-can.png) ved siden knappen **Behold det** nederst i vinduet.

- Hvis du vil bogføre den fuldt matchede afstemning automatisk, når du gemmer den, skal du aktivere kontakten **Bogfør, hvis den er fuldt udlignet**.  
- Hvis du vil gemme de matches, der aktuelt vises i Copilot-vinduet, skal du vælge **Behold det**.

## <a name="post-unmatched-bank-transaction-amounts-to-suggested-general-ledger-accounts"></a>Bogfør ikke-matchede banktransaktionsbeløb til foreslåede finanskonti

I dette afsnit lærer du, hvordan du bruger Copilot til at bogføre ikke-afstemte bankkontoudtogs linjebeløb (angivet i feltet **Forskel**) i en finanskonto. Denne opgave kan kun udføres fra en eksisterende afstemning.

1. Gå til listen **Bankkontoafstemninger**, og åbn den eksisterende afstemning, der indeholder de ikke-afstemte linjer.

   Start med at åbne en eksisterende bankkontoafstemning. Dette trin giver et klart overblik over alle ikke-afstemte bankkontoudtogslinjer, der skal overføres til finanskontoen.

1. I ruden **Bankkontoudtogslinjer** skal du identificere ruden Ikke-matchede bankkontoudtogslinjer og vælge en eller flere linjer, som du vil afstemme.

   Disse linjer er de kontoudtogslinjer, som Copilot fokuserer på til bogføring af nye betalinger til finanskontoen.

1. Vælg **Bogfør forskel til finanskonto** for at starte processen.

   ![Viser handlingen Overfør til finanskonto med copilot på kortet Bankkontoafstemning](media/bank-reconciliation-transfer-gl-copilot-card.png) 

   Dette trin beder Copilot om at begynde at generere forslag til bogføring af nye betalinger.

1. Når Copilot er færdig med at generere forslag, åbnes vinduet **Copilot-finanskontooverførselsforslag**.

   I dette vindue vises forslagene i sektionen **Matchet forslag**. Oplevelsen ligner forsoning med Copilot.

   ![Viser siden med overførsel til finans med copilot-foreslåede matches til bankkontoafstemning](media/bank-reconciliation-gl-transfer-proposed-matches.png) 

1. Gennemgå hvert forslag linje for linje for at sikre nøjagtigheden af de foreslåede overførsler.

   - Hvis du analyserer forslaget ved at vælge det på listen, føres du til en liste over konti. Herfra kan du vælge en anden konto. Denne form for manuel rettelse er kun mulig, når du bruger flowet **Bogfør forskelle til finanskonto**, ikke i match-flowet. 
   - Hvis du vælger **Gem...** ud for et forslag kan du føje tilknytningen til siden **Tilknytning af tekst til konto**, så næste gang teksten vises under matchning, knyttes den tilden foreslåede konto.

1. Kassér eller gem forslag.

   - Hvis du vil kassere et bestemt forslag, skal du markere det på listen og derefter vælge handlingen **Slet linje**. Hvis du vil kassere alle forslag og lukke Copilot-vinduet, skal du vælge knappen Kassér (papirkurv) ![Viser skraldespandsikonet til sletning af alle Copilot-forslag til bankkontoafstemning](media/copilot-delete-trash-can.png) ved siden knappen **Behold det** nederst i vinduet.

   - Hvis forslagene opfylder dine krav, og du vil gemme dem, skal du vælge **Behold det**.

      Dette trin bekræfter overførslen af de aktuelt valgte forslag fra bankkontoen til finanskontoen. Der bogføres nye betalinger på de foreslåede finanskonti, og der indsættes tilsvarende linjer i de oprettede bankkontoposter.

## <a name="next-steps"></a>Næste trin

[Validere din bankkontoafstemning](bank-how-reconcile-bank-accounts-separately.md#validate-your-bank-reconciliation)  

## <a name="see-also"></a>Se også
[Fejlfinde Copilot- og AI-funktioner](ai-copilot-troubleshooting.md)  
[Ofte stillede spørgsmål om ansvarlig AI til hjælp til bankafstemning](faqs-bank-reconciliation.md)  
[Konfigurere banktransaktioner](bank-setup-banking.md)  
[Afstemme bankkonti](bank-how-reconcile-bank-accounts-separately.md)  
[Udligne betalinger automatisk og afstemme bankkonti](receivables-apply-payments-auto-reconcile-bank-accounts.md) 
