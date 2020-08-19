---
title: Designdetaljer - ændring af kostmetoder for varer
description: Få mere at vide om, hvordan du tildeler en anden kostmetode til en vare, selvom du allerede har brugt varen i transaktioner.
author: bholtorf
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: costing methods, costing, item cost
ms.date: 07/23/2020
ms.author: bholtorf
ms.openlocfilehash: 0560e2bf900af4b49d0ce299dfa751a5c41ea54e
ms.sourcegitcommit: 7b5c927ea9a59329daf1b60633b8290b552d6531
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 07/23/2020
ms.locfileid: "3617727"
---
# <a name="design-details-change-the-costing-method-for-items"></a>Designdetaljer: ændre kostmetoden for varer

I [!INCLUDE[d365fin](includes/d365fin_md.md)] kan du ikke ændre en kostmetode for en vare, efter at du har medtaget varen i en transaktion. Når du f.eks. har købt eller solgt varen. Hvis der er knyttet en forkert kostmetode til varen eller varerne, kan du måske ikke finde problemet, før du foretager en regnskabsaflæggelse.

Dette emne beskriver, hvordan du kan løse dette problem. Den anbefalede metode er at erstatte den vare, der har den forkerte kostmetode, med en ny vare, og bruge en montageordre til at overføre lagerbeholdningen fra den gamle vare til den nye.

> [!NOTE]
> Når du bruger montageordrer, kan omkostningerne stadig flyde, selvom der er udestående købsfakturaer eller forsendelsesgebyrer at bogføre. Derudover kan du fortryde konverteringen og hente mængderne fra de oprindelige varer tilbage, hvis det er nødvendigt.

> [!TIP]
> Hvis du vil være fortrolig med processen, anbefales det, at du starter konverteringsprocessen med en enkelt vare eller et lille sæt varer.

## <a name="about-costing-methods"></a>Om kostmetoder

Kostmetoderne styrer omkostningsberegninger, når varer købes, modtages på lageret og sælges. Kostmetoderne påvirker timingen af de registrerede beløb i VAREFORBRUG, der påvirker bruttofortjeneste. Det er dette flow, der beregner VAREFORBRUG. Vareforbruget og omsætningen bruges til at bestemme bruttofortjeneste på følgende måde:

*bruttoavance* = *omsætning - VAREFORBRUG*

Når du opretter lagervarer, skal du tildele en kostmetode. Metoden kan variere fra virksomhed til virksomhed og fra vare til vare, så det er vigtigt at vælge den rigtige. Følgende kostmetoder understøttes i [!INCLUDE[d365fin](includes/d365fin_md.md)]:

* Gennemsnit
* FIFO
* LIFO
* Standard
* Bestemt

Du kan finde flere oplysninger i [Designoplysninger: Kostmetoder](design-details-costing-methods.md).

## <a name="using-assembly-orders-to-change-costing-method-assignments"></a>Bruge montageordrer til at ændre tildelinger af kostmetode

I dette afsnit beskrives følgende fremgangsmåde for at ændre den kostmetode, der er tildelt en vare:

1. Definer standardkostmetoden.
2. Identificer de varer, der skal have ændret kostmetoden, og nummerer dem igen.
3. Opret nye varer med det gamle nummereringsskema, og kopiér stamdata i en batchkørsel.
4. Kopiér relaterede stamdata manuelt fra den eksisterende vare til den nye vare.
5. Bestem det lagerantal, der skal konverteres fra den oprindelige vare til den nye vare.
6. Overfør lageret til den nye vare.
7. Håndter lagerantal, der er allokeret til behov.
8. Spær den oprindelige vare mod yderligere brug.  

### <a name="define-a-default-costing-method"></a>Definere en standardkostmetode

For at undgå fremtidige fejl kan du angive en standardkostmetode for nye varer. Når en person opretter en ny vare, vil [!INCLUDE[d365fin](includes/d365fin_md.md)] foreslå standardkostmetoden. Du kan angive standardmetoden i feltet **Standardmetode for kostprisberegning** på siden **Lageropsætning**. 

### <a name="identify-the-items-to-change-the-costing-method-for-and-renumber-them"></a>Identificere de varer, der skal have ændret kostmetoden, og nummerere dem igen

Det kan være en god idé at give de nye varer samme numre som dem, de erstatter. Hvis du vil gøre det, skal du ændre numrene på de eksisterende varer. Hvis det eksisterende varenummer f.eks. er "P1000", kan det ændres til "X-P1000". Dette er en manuel ændring, som du skal foretage for hver vare.

### <a name="create-new-items-with-the-old-numbering-scheme-and-copy-the-master-data-in-a-batch"></a>Oprette nye varer med det gamle nummereringsskema og kopiere stamdata i en batchkørsel

Opret de nye varer vha. det aktuelle nummerskema. Med undtagelse af feltet **Kostmetode** skal nye varer indeholde de samme stamdata som de eksisterende varer. Hvis du vil overføre stamdata for varen og relaterede data fra andre funktioner, skal du bruge handlingen **Kopiér vare** på siden **Varekort**. Du kan finde flere oplysninger i [Kopiere eksisterende elementer for at oprette nye varer](inventory-how-copy-items.md).

Når du har oprettet nye varer og overfører stamdataene, skal du tildele den korrekte kostmetode.

### <a name="manually-copy-related-master-data-from-the-original-item-to-the-new-item"></a>Kopiere relaterede stamdata manuelt fra den oprindelige vare til den nye vare

Hvis du vil gøre de nye elementer fuldt anvendelige, skal du manuelt kopiere nogle masterdata fra andre områder som beskrevet i følgende tabel.

|Område  |Hvad der skal kopieres  |Hvordan det skal kopieres  |
|---------|---------|---------|
|Lager     |Lagervarer         |Kontrollér, om der er angivet en lagervare for den oprindelige vare. Hvis der er angivet planlægningsparametre for hvert lagervarekort, skal du manuelt oprette lagervaren for den nye vare. Hvis der ikke er angivet parametre, kan du bruge kørslen **Opret lagervare** fra siden **Varekort** til at oprette dataene.        |
|     |Erstatningsvarer         |Kontrollér, om der er defineret erstatningsvarer for den oprindelige vare. Hvis der er det, skal du overføre dataene til den nye vare. Hvis du vil se erstatningsvarer, skal du bruge handlingen **Erstatninger** på siden **Varekort**.         |
|     |Analyserapporter         |Gennemgå vareanalyse-, salgsanalyse- og købsanalyserapporterne. For dem, der refererer til de oprindelige varer, kan du enten oprette en ny analyserapport med en reference til den nye vare (så den oprindelige analyserapport bruges som historik) eller justere rapporterne, så de henviser til den nye vare.         |
|     |Standardkladder         |Kontrollér, om standardkladder refererer til den oprindelige vare, og overfør dataene til den nye vare, når det er nødvendigt. Disse oplysninger findes i standardkladderne, som er tilgængelige i varekladden.          |
|Salg     |Forudbetalingsprocenter - salg         | Kontrollér, om der er defineret forudbetalingsprocenter for salg af den oprindelige vare, og overfør dataene til den nye vare. Hvis du vil have vist forudbetalingsprocenter, skal du vælge **Salg** på siden **Varekort** og derefter **Forudbetalingsprocenter**.        |
|Køb     |Forudbetalingsprocenter - køb         |Kontrollér, om der er defineret forudbetalingsprocenter for køb af den oprindelige vare, og overfør dataene til den nye vare. Hvis du vil have vist forudbetalingsprocenter, skal du vælge **Køb** på siden **Varekort** og derefter **Forudbetalingsprocenter**.                 |
|Lageragersted     |Placeringsindhold         |Gennemgå det placeringsindhold, der er defineret for den oprindelige vare. Hvis der er kolonner som Min. Antal, Maks. Antal, Standard og Dedikeret, der er blevet angivet individuelt, skal du manuelt oprette placeringsindhold til den nye vare. Hvis ikke, kræves der ingen handling. [!INCLUDE[d365fin](includes/d365fin_md.md)] vedligeholder posterne, når du registrerer lagerdokumenter og kladder.|
|Sag     |Sagspriser         |Kontrollér, om der er defineret sagspriser for den oprindelige vare, og overfør dataene til den nye vare. Disse oplysninger er tilgængelige på siden **Jobkort** i delen **Sagsdetaljer - antal priser** i **faktaboksruden**.         |
|Tjeneste     |Ressourcekvalifikation for service         |Kontrollér, om der er defineret ressourcekvalifikationer for service for den oprindelige vare, og overfør dataene til den nye vare. Hvis du vil have vist ressourcekvalifikationer, skal du bruge handlingen **Ressourcekvalifikationer** på siden **Varekort**.          |
|     |Serviceartikelkomponenter         |Kontrollér, om der er defineret komponenter for den oprindelige service, og overfør dataene til den nye vare. Hvis du vil have vist serviceartikelkomponenter, skal du bruge **Serviceartikel**-handlingen på siden **Varekort** til at åbne listen over relaterede serviceartikler og derefter vælge handlingen **Komponenter**.          |
|Produktion     |Produktionsstyklister         |Kontrollér, om produktionsstyklister indeholder den oprindelige vare, og erstat den med den nye vare. Hvis du vil erstatte den oprindelige vare, skal du vælge handlingen **Erstat prod.styklistevare** på siden **Produktionsstyklister**.         |
|Montage     |Montagestyklister         |Kontrollér, om montagestyklister indeholder den oprindelige vare, og erstat den manuelt med den nye vare.         |

> [!IMPORTANT]
> Hvis den nye kostmetode er Standard, skal du angive en værdi i feltet **Standardkostpris** på siden **Varekort**. Du kan bruge siden **Standardkostpriskladde** til at angive kostprisfordelingen i overensstemmelse hermed. Du kan finde flere oplysninger i [Opdatere standardkostpriser](finance-how-to-update-standard-costs.md).

### <a name="determine-the-inventory-quantity-to-convert-from-the-original-item-to-the-new-item"></a>Bestemme det lagerantal, der skal konverteres fra den oprindelige vare til den nye vare

> [!NOTE]
> Dette trin tager ikke højde for antal, der er medtaget i ikke-leverede ordrer. Du kan finde flere oplysninger i [Håndtere lagerantal, der er allokeret til behov](design-details-changing-costing-methods.md#handle-inventory-quantities-that-are-allocated-to-demand). 

Brug en lageropgørelseskladde til at oprette en liste over antal på lager. Afhængig af opsætning af lagerlokationen skal du bruge en af følgende:

* Lageropgørelseskladder
* Regul.plac. Lagerplacering - opg.kladder

Begge kladder kan beregne lagerbeholdningen for varen, herunder lokation, variant, placering og lagerplacering. Du kan finde flere oplysninger i [Tælle, justere og ompostere inventar ved hjælp af kladder](inventory-how-count-adjust-reclassify.md).

### <a name="transfer-the-inventory-to-the-new-item"></a>Overføre lageret til den nye vare

Opret og bogfør montageordrer for at overføre kostprisen og lagerbeholdningen fra den oprindelige vare til den nye vare. Montageordrer kan konvertere en vare til en anden, samtidig med at omkostningerne bevares. Det er med til at sikre, at nettototalerne for lagerkontoen og VAREFORBRUG ikke påvirkes (undtagen når den nye kostmetode er Standard, og i dette tilfælde kan omkostningerne fordeles på afvigelseskonti). Du kan finde flere oplysninger i [Montagestyring](assembly-assemble-items.md).

Når du opretter montageordrer, skal du bruge oplysningerne fra Lageropgørelseskladder eller Regul.plac. Lagerplacering - opg.kladde I følgende tabel beskrives de oplysninger i rapporterne, der skal angives i hovedet og linjerne på montageordren.

#### <a name="header"></a>Overskrift

|Felt  |Værdi, der skal indsættes  |
|---------|---------|
|Varenr.     |Nummeret på den nye vare.         |
|Antal     |Antallet i lageropgørelseskladden.<br> **Bemærk:** De antal, der er beregnet af lageropgørelseskladderne, inkluderer ikke de antal, der er angivet i ordrer, der endnu ikke er leveret.          |
|Variantkode     |Det samme som i lageropgørelseskladden.          |
|Lokationskode     |Det samme som i lageropgørelseskladden.         |
|Enhedskode     |Det samme som i lageropgørelseskladden.         |
|Placeringskode     |Det samme som i lageropgørelseskladden.         |

#### <a name="lines"></a>Linjer

|Felt  |Værdi, der skal indsættes  |
|---------|---------|
|Type     |Vare         |
|Nummer     |Nummeret på den oprindelige vare.         |
|Antal pr.     |1         |
|Variantkode     |Det samme som i lageropgørelseskladden.         |
|Lokationskode     |Det samme som i lageropgørelseskladden.         |
|Enhedskode     |Det samme som i lageropgørelseskladden.         |

> [!NOTE]
> En montageordre kan kun håndtere én lagervare ad gangen. Du skal oprette en montageordre for hver kombination af lagervare, der har et antal på lager.

> [!NOTE]
> Du skal muligvis oprette pluk, før du kan bogføre montageordren, for en lagerlokation. Du kan undersøge dette ved at gennemgå opsætningen af plukning på siden **Lokationskort**. Du kan finde flere oplysninger i [Konfigurere varer og lokationer til styret læg-på-lager og pluk](warehouse-how-to-set-up-items-for-directed-put-away-and-pick.md).

### <a name="handle-inventory-quantities-that-are-allocated-to-demand"></a>Håndtere lagerantal, der er allokeret til behov

Ideelt bør lagerbeholdningen for den oprindelige vare blive nul, efter at du har overført lagerantal. Der kan imidlertid være udestående ordrer, regneark og kladder (se nedenstående tabel), der stadig kræver et antal af den oprindelige vare. Antallet kan også være spærret af en reservation eller varesporing.

**Eksempel** Der er 1000 stk. på lager, og 20 stk. er reserveret til en salgsordre, der endnu ikke er leveret. Hvis det er tilfældet, kan du vælge at beholde 20 stk. af den gamle vare, så du kan opfylde den udestående ordre.

> [!NOTE]
> Der er funktionsområder, der kan påvirke antallet, som angivet i tabellen nedenfor, så det kan være vanskeligt at finde det rigtige antal. Hvis du bruger eksemplet ovenfor, kan du for at være på den sikre side beholde 100 stk. og overføre de resterende 900 stk. i stedet. Du kan også vælge at behandle dokumenterne og kladderne, så der kun er få tilbage. Endnu et alternativ er at overføre hele antallet til den nye vare og derefter overføre nogle af dem tilbage til den oprindelige vare vha. montageordren.

I følgende tabel vises funktionelle områder, hvor der kan være udestående antal.

|Område  |Her kan du se, om der er udestående antal  |
|---------|---------|
|Salg     |Salgsdokumenter, herunder ordrer, returordrer, fakturaer, tilbud, rammeordrer og kreditnotaer         |
|Lager     |Varekladder, reservationer, varesporing og standardkostpriskladde         |
|Køb     |Købsdokumenter, herunder ordrer, returordrer, fakturaer, tilbud, rammeordrer og kreditnotaer         |
|Planlægning     |Indkøbskladde, planlægningskladde og ordreplanlægning         |
|Lageragersted     |Overflytningsordrer, lagerleverancer, lagerkladder og pluk (logistik), læg-på-lager-aktiviteter og bevægelser, interne pluk og læg-på-lager-aktiviteter og placeringsoprettelseskladder         |
|Montage     |Montagedokumenter, herunder ordrer, returvareordrer og rammeordrer         |
|Sager     |Sagsplanlægningslinjer og sagskladdelinjer         |
|Tjeneste     |Servicedokumenter og servicekontrakter         |
|Produktion     |Produktionsordrer (planlagte, fastlagte og frigivne)         |

### <a name="block-the-original-item-from-further-use"></a>Spærre den oprindelige vare mod yderligere brug

Når lagerbeholdningen for den oprindelige vare er nul, kan du spærre varen for at forhindre, at den bruges i nye transaktioner. Hvis du vil spærre varen, skal du slå **Spærret** til på siden **Varekort**. Du kan finde flere oplysninger i [Spærre varer mod salg eller køb](inventory-how-block-items.md).

## <a name="summary"></a>Oversigt

Ændring af kostmetoden for varer, der er brugt i transaktioner, er en proces og ikke en standardhandling i [!INCLUDE[d365fin](includes/d365fin_md.md)]. Du kan bruge de trin, der er beskrevet i dette emne, som en skabelon til processen.

Processen kan være tidskrævende, fordi der er flere manuelle trin. Hvis du imidlertid har tid til at fuldføre det, minimerer du fejlene i Finans.

Vi anbefaler følgende:

1. Du kan vurdere, om processen er gennemførlig, ved at tage et eller måske nogle få, repræsentative varer gennem hele processen.
2. Overvej at kontakte en erfaren partner, som kan hjælpe dig med processen.

## <a name="see-also"></a>Se også

[Designoplysninger: Kostmetoder](design-details-costing-methods.md)  
[Oversigt](design-details-inventory-costing.md)
