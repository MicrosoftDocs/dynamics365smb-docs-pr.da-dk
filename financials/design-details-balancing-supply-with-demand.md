---
title: "Designoplysninger – Afstemning af forsyning med behov | Microsoft Docs"
description: "Kernen i planlægningssystemet omfatter udlignende efterspørgsel og udbud ved at foreslå brugerhandlinger for at revidere forsyningsordrer, når der er ubalance. Dette sker pr. kombination af variant og lokation."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 07/01/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 2c13559bb3dc44cdb61697f5135c5b931e34d2a8
ms.openlocfilehash: 5020c048373f10e72e40f0c9b1e5a11fc45eedb5
ms.contentlocale: da-dk
ms.lasthandoff: 03/22/2018

---
# <a name="design-details-balancing-supply-with-demand"></a>Designoplysninger: Afstemning af forsyning med behov
Kernen i planlægningssystemet omfatter udlignende efterspørgsel og udbud ved at foreslå brugerhandlinger for at revidere forsyningsordrer, når der er ubalance. Dette sker pr. kombination af variant og lokation.  
  
Forestil dig, at hver lagerprofil indeholder en streng af behovshændelser (sorteret efter dato og prioritet) og en tilsvarende streng af forsyningshændelser. Hver hændelse refererer tilbage til dens kildetype og identifikation. Reglerne for afstemning af varen er ligetil. Fire forekomster af tilsvarende behov og forsyning kan ske på et hvilket som helst tidspunkt i processen:  
  
1. Der findes ingen behov eller forsyning for varen = > planlægning er afsluttet (eller bør ikke starte).  
2. Behov findes, men der er ingen forsyning = > forsyning bør foreslås.  
3. Forsyning findes, men der er ingen efterspørgsel for det = > forsyning bør annulleres.  
4. Både behov og forsyning findes = > spørgsmål bør stilles og besvares, før systemet kan sikre, at efterspørgslen imødekommes og forsyningen er tilstrækkelig.  
  
     Hvis tidspunktet for forsyning ikke er egnet, kan den måske planlægges som følger:  
  
   1. Hvis forsyningen er placeret tidligere end behovet, kan forsyningen måske planlægges om, så lageret er så lavt som muligt.  
   2. Hvis levering er senere end behovet, kan levering måske planlægges igen. I modsat fald foreslås ny forsyning.  
   3. Hvis forsyningen opfylder behovet på datoen, kan planlægningssystemet fortsætte med at undersøge, om forsyningsantallet kan dække behovet.  
  
      Når timingen er på plads, kan den passende leveringsmængde beregnes på følgende måde:  
  
   4. Hvis forsyningsantallet er mindre end behovet, er det muligt, at forsyningsantallet kan øges (eller ikke, hvis begrænset af en maksimummængdepolitik).  
   5. Hvis forsyningsantallet er større end behovet, er det muligt, at forsyningsantallet kan reduceres (eller ikke, hvis begrænset af en minimummængdepolitik).  
  
      På nuværende tidspunkt er en af disse to situationer aktuelle:  
  
   6. Det aktuelle behov kan dækkes, i hvilket tilfælde det kan lukkes, og planlægning af næste behov kan starte.  
   7. Forsyningen har nået sit maksimum og efterlader nogle i behovsantallet uafdækkede. I dette tilfælde kan planlægningssystemet lukke den aktuelle forsyning og gå videre til den næste.  
  
   Proceduren starter forfra med det næste behov og den aktuelle forsyning eller omvendt. Den aktuelle forsyning kan måske dække dette næste behov, eller det aktuelle behov er ikke endnu fuldt dækket.  
  
## <a name="rules-concerning-actions-for-supply-events"></a>Regler for handlinger for forsyningshændelser  
Når planlægningssystemet opretter en top-down-beregning, hvor forsyningen skal opfylde behovet, tages behovet for givet, det vil sige, det ligger uden for kontrol af planlægningssystemet. Men forsyningssiden kan administreres. Planlægningssystemet foreslår derfor oprettelse af nye forsyningsordrer, omlægning af eksisterende og/eller ændring af ordreantallet. Hvis en eksisterende forsyningsordre bliver overflødig, foreslår planlægningssystemet, at brugeren annullerer den.  
  
Hvis brugeren ønsker at udelukke en eksisterende forsyningsordre fra planlægningsforslagene, han brugeren angive, at den har ingen planlægningsfleksibilitet (planlægningsfleksibilitet = ingen). Derefter bliver overskydende forsyning fra den pågældende ordre brugt til at dække behov, men der foreslås ingen handling.  
  
Alle forsyninger har generelt en planlægningsfleksibilitet, som er begrænset af betingelserne for hver af de foreslåede handlinger.  
  
-   **Omplanlæg ud**: Datoen for en eksisterende forsyningsordre kan planlægges ud til at imødekomme behovets forfaldsdato, medmindre:  
  
    -   Det repræsenterer lager (altid på dag nul).  
    -   Den har en ordre-til-ordre, der er knyttet til et andet behov.  
    -   Det ligger uden for den omplanlægningsramme, der er defineret i intervallet.  
    -   Der er en forsyning tættere på, der kan anvendes.  
    -   På den anden side kan brugeren beslutte at omplanlægge, fordi:  
    -   Forsyningsordren er allerede knyttet til et andet behov på en tidligere dato.  
    -   Den nødvendige ændring i planen er så minimal, at brugeren finder den ubetydelig.  
  
-   **Omplanlæg ind**: Datoen for en eksisterende forsyningsordre, der kan planlægges, undtagen under følgende betingelser:  
  
    -   Det er knyttet direkte til et andet behov.  
    -   Det ligger uden for den omplanlægningsramme, der er defineret i intervallet.  
  
> [!NOTE]  
>  Ved planlægning af en vare ved hjælp af et genbestillingspunkt kan forsyningsordrer altid planlægges med, hvis der er behov for det. Det er almindeligt i forbindelse med forsyningsordrer, der er planlagt fremad, og som er udløst af et genbestillingspunkt.  
  
-   **Øg antal**: Antallet af en eksisterende forsyningsordre kan øges for at imødekomme behovet, medmindre forsyningsordren er knyttet direkte til et behov efter et ordre-til-ordre-link.  
  
> [!NOTE]  
>  Selvom det er muligt at øge forsyningsordren, kan det være begrænset på grund af et defineret maksimalt ordreantal.  
  
-   **Reducer antal**: En eksisterende forsyningsordre med et overskud sammenlignet med et eksisterende behov kan reduceres for at opfylde behovet.  
  
> [!NOTE]  
>  Selvom antallet kan blive reduceret, kan der stadig være overskud, sammenlignet med behovet, på grund af et defineret minimumsordreantal eller en oprundingsfaktor.  
  
-   **Annuller**: Som et særligt tilfælde af handlingen, der reducerer antallet, kan forsyningsordren blive annulleret, hvis den er reduceret til nul.  
-   **Ny**: Hvis der ikke allerede findes en forsyningsordre, eller en eksisterende ikke kan ændres for at opfylde det nødvendige antal på den efterspurgte forfaldsdato, foreslås der en ny forsyningsordre.  
  
## <a name="determining-the-supply-quantity"></a>Bestemmelse af forsyningsantallet  
Planlægningsparametre, der er defineret af brugeren, styrer det foreslåede antal af hver forsyningsordre.  
  
Når planlægningssystemet beregner antallet af en ny forsyningsordre eller ændring af antallet på en eksisterende, kan det foreslåede antal være forskelligt fra det, der faktisk kræves.  
  
Hvis en maksimal lager- eller fast ordremængde er valgt, kan det foreslåede antal øges for at opfylde det faste antal eller det maksimale lagerniveau. Hvis genbestillingsmetoden bruger et genbestillingspunkt, kan antallet forhøjes for i det mindste at opfylde genbestillingspunktet.  
  
 Det foreslåede antal kan ændres i denne rækkefølge:  
  
1. Ned til det højst tilladte ordreantal (hvis der er et).  
2. Op til det mindste ordreantal.  
3. Op til at opfylde den nærmeste oprundingsfaktor. (I tilfælde af forkerte indstillinger kan den højst tilladte ordrestørrelse overskrides).  
  
## <a name="order-tracking-links-during-planning"></a>Ordresporingsbindinger under planlægning  
Med hensyn til ordresporing under planlægning, er det vigtigt at nævne, at planlægningssystemet omarrangerer de dynamisk oprettede ordresporingsbindinger til vare-/variant-/lokationskombinationerne.  
  
Der er to grunde til dette:  
  
-   Planlægningssystemet skal være i stand til at begrunde sine forslag om at alle behov er dækket, og at ingen forsyningsordrer er overflødige.  
-   Dynamisk oprettede ordresporingsbindinger skal regelmæssigt afstemmes.  
  
I tidens løb bliver dynamiske ordresporingslinks uafstemte, da hele ordresporingsnetværket ikke omarrangeres, før et behov eller en forsyningshændelse faktisk er lukket.  
  
Før udligning af forsyning med behov, sletter programmet alle eksisterende ordresporingsbindinger. Under den udlignende procedure, når en behov- eller forsyningshændelse er lukket, etablerer det derefter nye ordresporingsbindinger mellem behov og forsyning.  
  
> [!NOTE]  
>  Selvom varen ikke er konfigureret til dynamisk ordresporing, opretter planlægningssystemet afstemte ordresporingsbindinger, som forklaret ovenfor.  
  
## <a name="see-also"></a>Se også  
[Designoplysninger: Afstemning mellem behov og forsyning](design-details-balancing-demand-and-supply.md)   
[Designoplysninger: Centrale begreber i planlægningssystemet](design-details-central-concepts-of-the-planning-system.md)   
[Designoplysninger: Forsyningsplanlægning](design-details-supply-planning.md)
