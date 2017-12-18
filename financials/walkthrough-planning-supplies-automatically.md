---
title: "Gennemgang - Automatisk planlægning af forsyninger | Microsoft Docs"
description: "Betegnelser som \"kør planlægning\" eller \"kør MRP\" refererer til beregningen af hovedplanen (MPS) og materialebehovsplanen (MRP) baseret på det faktiske og det prognosticerede behov."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 09/07/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 2c13559bb3dc44cdb61697f5135c5b931e34d2a8
ms.openlocfilehash: bbe470538bb79e9f6fb6860ee32d75b5d56db9e8
ms.contentlocale: da-dk
ms.lasthandoff: 09/22/2017

---
# <a name="walkthrough-planning-supplies-automatically"></a>Gennemgang: Automatisk planlægning af forsyninger
Betegnelser som "kør planlægning" eller "kør MRP" refererer til beregningen af hovedplanen (MPS) og materialebehovsplanen (MRP) baseret på det faktiske og det prognosticerede behov.  

-   MPS defineres som beregning af en hovedplan på basis af et faktisk behov og produktionsforecast. MPS-beregningen bruges til slutvarer, der har en forecast- eller en salgsordrelinje. Disse varer kaldes "MPS-varer" og identificeres dynamisk, når beregningen begynder.  
-   MRP defineres som beregning af materialebehov på basis af et faktisk komponentbehov og et produktionsforecast på komponentniveau. MRP beregnes kun for varer, der ikke er MPS-varer. Det overordnede formå med MRP er at udarbejde formelle planer med tidsangivelser og opdelt efter varer, så den rigtige vare kan leveres på det rigtige tidspunkt, til det rigtige sted og i det rette antal.  

 Der bruges de samme planlægningsalgoritmer til både MPS og MRP. Planlægningsalgoritmerne bruger sammenligning, genbrug af eksisterende forsyningsordrer og aktionsmeddelelser. Under planlægningen tages der højde for, hvad der er brug for, eller hvad der vil blive brug for (efterspørgsel), og hvad der allerede er på lager eller forventes at være på lager (udbud). Når disse antal er sammenlignet med hinanden, vises der aktionsmeddelelser i planlægningskladden. Aktionsmeddelelserne er forslag om et oprette en ny forsyningsordre, ændre en forsyningsordre (antal eller dato) eller annullere en eksisterende forsyningsordre. Forsyningsordrer kan være produktionsordrer, købsordrer og overflytningsordrer. Du kan finde flere oplysninger i [Designoplysninger: Forsyningsplanlægning](design-details-supply-planning.md)  

 Planlægningsresultatet beregnes delvist ud fra behov-udbudssættet i databasen, og delvist ud fra opsætningen af lagervarekortene eller varekortene, produktionsstyklister og ruter.  

## <a name="about-this-walkthrough"></a>Om denne gennemgang  
 Denne gennemgang viser, hvordan du kan bruge forsyningsplanlægningssystemet til automatisk at planlægge alle de købs- og produktionsordrer, der skal til for at fremstille 15 turcykler, der skal bruges til forskellige salgsordrer. For at opnå en klar og realistisk gennemgang er antallet af planlægningslinjer begrænset ved bortfiltrering af alle andre behov-udbudssæt i demonstrationsvirksomheden CRONUS Danmark A/S med undtagelse af salgsbehovet på lokationen BLÅ.  

 Denne gennemgang illustrerer følgende opgaver:  

-   Oprettelse af salgsordre og beregning af en komplet forsyningsplan.  
-   Visning af planlægningsparametre og ordresporingsposterne bag planlægningslinjerne.  
-   Automatisk oprettelse af forslåede forsyningsordrer.  
-   Oprettelse af nyt salgsbehov og en tilsvarende genplanlægning.  

## <a name="roles"></a>Roller  

-   Produktionsplanlægger  
-   Indkøbsagent  

## <a name="prerequisites"></a>Forudsætninger  
 For at gennemføre denne gennemgang skal du:  

-   Bruge demovirksomheden CRONUS Danmark A/S.  
-   Ændring af forskellige vareopsætningsværdier ved at følge trinnene i afsnittet "Klargøring af eksempeldata" senere i denne gennemgang.  

## <a name="story"></a>Historie  
 Debitoren, Kontorcentralen A/S, bestiller fem turcykler til levering 05-02-2014 (den 5. februar).  

 Erik, der er produktionsplanlægger, står for den rutinemæssige forsyningsplanlægning for den første uge af februar 2014. Han filtrerer selv lokationen, BLÅ, og indtaster planlægningsintervallet for arbejdsdatoen (23-01-2014) til 07-02-2014, før han beregner en foreløbig forsyningsplan.  

 Det eneste efterspørgsel denne uge er en salgsordre for Kontorcentralen. Erik ser, at ingen af planlægningslinjerne har advarsler, og han fortsætter med at oprette forsyningsordrer uden ændringer for de foreslåede planlægningslinjer.  

 Den næste dag, før de første forsyningsordrer startes eller bogføres, får Erik besked om, at en anden debitor har bestilt ti turcykler til afsending den 12-02-2014. Han foretager en genberegning for at justere forsyningsplanen i overensstemmelse med ændringen i behovet. Genberegningsresultatet giver en plan med nettoændringen, der foreslår ændringer i både tid og antal for nogle af de forsyningsordrer, der er oprettet i første kørsel.  

 Under de forskellige planlægningstrin slår Erik de involverede ordrer op og bruger funktionen Ordresporing til at se, hvilket behov der er dækket af hvilken forsyning.  

## <a name="preparing-sample-data"></a>Klargøre eksempeldata  
 Opret lagervarer for turcyklen og et udvalg af dens komponenter, varenumrene 1001 til 1300. (Nogle komponenter medtages ikke for at forenkle procedurerne). Juster planlægningsparametrene for de valgte komponenter for at få et mere gennemskueligt planlægningsresultat.  

### <a name="to-create-stockkeeping-units"></a>Sådan oprettes lagervarer  

1.  Åbn varekortet til vare 1001, turcykel.  
2.  Vælg handlingen **Opret lagervare**.  
3.  Lad alle indstillinger og filtre være uændret i vinduet **Opret lagervare**, og klik derefter vælge knappen **OK**.  
4.  Gentag trin 1 til 3 for alle varer i nummerintervallet fra 1100 til 1300.  

### <a name="to-change-selected-planning-parameters"></a>Ændre valgte planlægningsparametre  

1.  Vælg ikonet ![Søg efter side eller rapport](media/ui-search/search_small.png "Ikonet Søg efter side eller rapport"), angiv **Lagervarer**, og vælg derefter det relaterede link.  
2.  Åbn lagervarekortet BLÅ for vare 1100, forhjul.  
3.  Udfyld felterne i oversigtspanelet **Planlægning** som beskrevet i følgende tabel.  

    |Genbestillingsmetode|Sikkerhedslager|Akkumuleringsperiode for lot|Ændringsperiode|  
    |-------------------------------------------|-----------------------------------------------|-------------------------------------------------|---------------------------------------------|  
    |Lot-for-Lot|Tom|2U|2U|  

4.  Gentag trin 2 og 3 for alle lagervarer i nummerintervallet fra 1100 til 1300.  

 Hermed er klargøringen af eksempeldata til gennemgangen færdig.  

## <a name="creating-a-regenerative-supply-plan"></a>Oprette en total forsyningsplan  
 Som reaktion på en ny salgsordre på fem turcykler, starter Ricardo på planlægningsprocessen ved at angive indstillinger, filtre og planlægningsinterval for at ekskludere anden efterspørgsel med undtagelse af behovet den første uge i februar på lokationen BLÅ. Han begynder så med at beregne en hovedplan (MPS) og fortsætter derefter til beregningen af en komplet forsyningsplan for alle behov på underniveau (MRP).  

### <a name="to-create-the-sales-order"></a>Sådan oprettes salgsordren  

1.  Vælg ikonet ![Søg efter side eller rapport](media/ui-search/search_small.png "Ikonet Søg efter side eller rapport"), angiv **Salgsordrer**, og vælg derefter det relaterede link.  
2.  Vælg handlingen **Ny**.  
3.  I vinduet **Salgsordre** skal du udfylde felterne som beskrevet i følgende tabel.  

    |Kundenavn|Afsendelsesdato|Varenr.|Lokation|Antal|  
    |----------------------------|-------------------|--------------|--------------|--------------|  
    |Kontorcentralen|05-02-2014|1001|BLÅ|5|  

4.  Accepter tilgængelighedsadvarslen, og vælg knappen **Ja** for at registrere det nye behovsantal.  

### <a name="to-create-a-regenerative-plan-to-fulfill-demand-at-location-blue"></a>Sådan oprettes en totalplan for at opfylde behovet på lokationen BLÅ  

1.  Vælg ikonet ![Søg efter side eller rapport](media/ui-search/search_small.png "Ikonet Søg efter side eller rapport"), angiv **Planlægningskladde**, og vælg derefter det relaterede link.  
2.  Vælg handlingen **Beregn totalplan**.  
3.  I vinduet **Beregn plan - planlægningskld.** skal du udfylde felterne som beskrevet i følgende tabel.  

    |Beregn plan|Startdato|Slutdato|Vis resultater:|Begræns totaler til|  
    |--------------------|-------------------|-----------------|-------------------|---------------------|  
    |**MPS** = Ja<br /><br /> **MRP** = Nej|01-23-2014<br /><br /> (arbejdsdato)|07-02-2014|1001..1300|Lokationsfilter = BLÅ|  

4.  Vælg knappen **OK** for at starte planlægningskørslen.  

     Der oprettes en planlægningslinje med forslag om, at der udstedes en planlagt produktionsordre for at producere de ti turcykler, vare 1001, til 02-05-2014, der er afsendelsesdatoen på salgsordren.  

     Kontroller nu, at denne planlægningslinje er relateret til salgsordren for Kontorcentralen A/S, ved hjælp af funktionen **Ordresporing**, der tilknytter behov til den pågældende planlagte forsyning dynamisk.  

5.  Vælg den nye planlægningslinje, og vælg derefter handlingen **Ordresporing**.  
6.  I vinduet **Ordresporing** skal du vælge handlingen **Vis**.  

     Salgsordren på de fem turcykler til afsendelse til debitornummer 10000 den 02-05-2014 vises.  

7.  Luk vinduerne **Salgsordre** og **Ordresporing**.  

### <a name="to-calculate-mrp-to-include-underlying-component-needs"></a>Beregne MRP for at medtage underliggende komponentbehov  

1.  Vælg ikonet ![Søg efter side eller rapport](media/ui-search/search_small.png "Ikonet Søg efter side eller rapport"), angiv **Planlægningskladde**, og vælg derefter det relaterede link.  
2.  Vælg handlingen **Beregn totalplan**.  
3.  I vinduet **Beregn plan - planlægningskld.** skal du udfylde felterne som beskrevet i følgende tabel.  

    |Beregn|Startdato|Slutdato|Vis resultater:|Begræns totaler til:|  
    |---------------|-------------------|-----------------|-------------------|----------------------|  
    |**MPS** = Ja<br /><br /> **MRP** = Ja|01-23-2014|07-02-2014|1001..1300|Lokationsfilter = BLÅ|  

4.  Vælg knappen **OK** for at starte planlægningskørslen.  

     Der oprettes nu i alt 14 planlægningslinjer med forslag om forsyningsordrer for alle de behov, som turcyklerne på salgsordren for turcykler på lokation BLÅ repræsenterer.  

## <a name="analyzing-the-planning-result"></a>Analyse af planlægningsresultatet  
 For at analysere de foreslåede antal går Erik ned i lagene af de valgte planlægningslinjer for at få vist ordresporingsposter og planlægningsparametre.  

 Bemærk i vinduet **Planlægningskladde**, at de foreslåede forsyningsordrer i kolonnen **Forfaldsdato** er planlagt baglæns fra forfaldsdatoen på salgsordren, 05-02-2014. Tidslinjen starter på planlægningslinjen med produktionsordren for samlingen af de færdige turcykler. Tidslinjen slutter på nederste planlægningslinje med købsordren på en af varerne på et lavere niveau, 1255, Baglygteholder, med forfald den 30-01-2014. Ligesom planlægningslinjen for vare 1251, en baghjulsaksel, repræsenterer denne linje en købsordre for komponenter, som er forfaldne på den overordnede vares startdato, den underordnede vare 1250, som igen er forfalden 02-03-2014. I kladden kan du se, at alle underliggende varer er forfaldne på startdatoen for deres overordnede varer.  

 Planlægningslinjen for vare 1300, Kædesaml, foreslår ti stykker. Dette afviger fra de fem stykker, som vi forventer at få brug for ved opfyldning af salgsordren. Fortsæt ved at vise ordresporingsposterne.  

### <a name="to-view-order-tracking-entries-for-item-1300"></a>Få vist ordresporingsposter for vare 1300  

1.  Vælg planlægningslinjen for vare 1300, og vælg derefter handlingen **Ordresporing**.  

     De to linjer i vinduet **Ordresporing** viser, at der er sporet fem stykker fra planlægningslinjen (første ordresporingslinje) til salgsordre 1001 (anden ordresporingslinje). De sidste fem stykker, der er foreslået på planlægningslinjen, er ikke relateret til nogen dokumentlinjer, men til en planlægningsparameter, forecastpost eller rammeordrepost. Sådanne ikke-sporede antal opsummeres i feltet **Ikkesporet antal** i hovedet i vinduet **Ordresporing**.  

2.  Vælg feltet **Ikkesporet antal**.  

     Vinduet **Ikkesporede planlægningselementer** viser, at vare 1300 bruger en planlægningsparameter, Min. ordrestørrelse, på 10,00. Planlægningslinjen er derfor på ti stykker i alt, men kun fem af dem kan spores til et behov. De sidste fem stykker er et ikke-sporet antal, der skal bruges ifm. planlægningsparameteren. Fortsæt med at gennemse planlægningsparameteren.  

### <a name="to-check-the-planning-parameter"></a>Kontrollere planlægningsparameteren  

1.  I vinduet **Ikke-sporede planlægningselementer** vælger du ordresporingslinjen for vare 1300.  
2.  Vælg feltet **Varenr.**, og vælg derefter handlingen **Avanceret**.  
3.  I vinduet **Varekort** skal du vælge handlingen **Lagervarer**.  
4.  I vinduet **Lagervareoversigt** skal du åbne det BLÅ lagervarekort.  
5.  Bemærk i oversigtspanelet **Planlægning**, at feltet **Min. ordrestørrelse** indeholder 10.  
6.  Luk alle vinduer undtagen vinduet **Planlægningskladde**.  

### <a name="to-view-more-order-tracking-entries"></a>Få vist flere ordresporingsposter  

1.  Vælg planlægningslinjen for vare 1110, Fælg, og vælg derefter handlingen **Ordresporing**.  

     Vinduet **Ordresporing** viser fem fælge, der er nødvendige for hver produktionsordre for henholdsvis for- og baghjul.  

     Samme ordresporing gælder planlægningslinjerne for vare 1120, 1160 og 1170. For vare 1120 er feltet **Antal pr.** på produktionsstyklisten for hver hjultype 50 stk., hvilket medfører et samlet behov på 100.  

     Planlægningslinjen for vare 1150 for seks stykker ser uregelmæssig ud. Fortsæt ved at analysere.  

2.  Vælg planlægningslinjen for vare 1150, og vælg derefter handlingen **Ordresporing**.  

     Vinduet **Ordresporing** viser, at fem enheder spores til forhjulet, og én enhed er ikke-sporet. Fortsæt ved at vise det ikke-sporede antal.  

3.  Vælg feltet **Ikkesporet antal**.  

     Vinduet **Ikke-sporede planlægningselementer** viser som standard, at vare 1150 bruger en planlægningsparameter, Oprundingsfaktor, på 2,00, hvilket angiver, at når varen er bestilt, skal den være i et antal, der er deleligt med 2. Det tal, der er tættest på fem og kan divideres med 2, er seks.  

     Den samme ordresporing gælder for planlægningslinjerne for fornavskomponenterne, vare 1151 og 1155, bortset fra at de hver skal ganges med spildprocenten, som for vare 1150 defineres i feltet **Spildprocent** på varekortet.  

 Dermed er analysen af den første forsyningsplan færdig. Bemærk, at afkrydsningsfeltet **Accepter aktionsmeddelelse** er markeret på alle planlægningslinjerne for at indikere, at de er klar til at blive konverteret til forsyningsordrer.  

## <a name="carrying-out-action-messages"></a>Udføre aktionsmeddelelser  
 Erik konverterer nu de foreslåede planlægningslinjer til forsyningsordrer ved hjælp af funktionen **Udfør aktionsmeddl.**.  

### <a name="to-automatically-create-the-suggested-supply-orders"></a>Sådan oprettes de forslåede forsyningsordrer automatisk.  

1.  Marker afkrydsningsfeltet **Accepter aktionsmeddelelse** på alle planlægningslinjer med en advarsel af typen Undtagelse.  
2.  Vælg handlingen **Udfør aktionsmeddelelse**.  
3.  Udfyld felterne i vinduet **Udfør aktionsmedl.-plan.** som beskrevet i følgende tabel.  

    |Produktionsordre|Købsordre|Overflytningsordre|  
    |----------------------|--------------------|--------------------|  
    |Fastlagt|Opret købsordrer|Opret overførselsordrer|  

4.  Klik på **OK**-knappen for at oprette alle de foreslåede forsyningsordrer automatisk.  
5.  Luk det tomme vindue **Planlægningskladde**.  

 Dermed er den første beregning, analyse og oprettelse af en forsyningsplan for behov på lokationen BLÅ i første uge af februar færdig. I det følgende afsnit bestiller en anden kunde ti turcykler, og Erik skal foretage en omplanlægning.  

## <a name="creating-a-net-change-plan"></a>Oprette en nettoplan  
 Den næste dag før nogen af forsyningsordrerne er startet eller bogført, ankommer en ny salgsordre fra Libros S.A. på ti turcykler til afsendelse den 02-12-2014. Erik får besked om det nye behov, og han fortsætter til at foretage en genplanlægning for at justere den aktuelle forsyningsplan. Erik bruger funktionen til nettoplanlægning til kun at beregne de ændringer, der er foretaget i behov og forsyning, siden den sidste planlægning blev kørt. Derudover udvider han planlægningsperioden til 14-02-2014 for at inkludere det nye salgsbehov den 12-02-2014.  

 Planlægningssystemet beregner den bedste måde at dække behovet for disse to identiske produkter på, som f.eks. at konsolidere nogle købs- og produktionsordrer, genplanlægge andre ordrer og oprette nye ordrer, hvor dette er nødvendigt.  

### <a name="to-create-the-new-sales-demand-and-replan-accordingly"></a>Sådan oprettes det nye salgsbehov og en tilsvarende genplanlægning  

1.  Vælg handlingen **Ny**.  
2.  I vinduet **Salgsordre** skal du udfylde felterne som beskrevet i følgende tabel.  

    |Kundenavn|Afsendelsesdato|Varenr.|Lokation|Antal|  
    |----------------------------|-------------------|--------------|--------------|--------------|  
    |Libros S.A.|12-02-2014|1001|BLÅ|10|  

3.  Accepter tilgængelighedsadvarslen, og vælg knappen **Ja** for at registrere behovsantallet.  
4.  Fortsæt med at foretage en genplanlægning for at justere den aktuelle forsyningsplan.  
5.  Vælg ikonet ![Søg efter side eller rapport](media/ui-search/search_small.png "Ikonet Søg efter side eller rapport"), angiv **Planlægningskladde**, og vælg derefter det relaterede link.  
6.  Vælg handlingen **Beregn nettoplan**.  
7.  I vinduet **Beregn plan - planlægningskld.** skal du udfylde felterne som beskrevet i følgende tabel.  

    |Beregn plan|Startdato|Slutdato|Vis resultater:|Begræns totaler til|  
    |--------------------|-------------------|-----------------|-------------------|---------------------|  
    |**MPS** = Ja<br /><br /> **MRP** = Ja|01-23-2014|14-02-2014|1001..1300|Lokationsfilter = BLÅ|  

8.  Vælg knappen **OK** for at starte planlægningskørslen.  

 Der oprettes 14 planlægningslinjer i alt. Bemærk i den første planlægningslinje, at feltet **Aktionsmeddelelse** indeholder **Ny**, at feltet **Antal** viser 10, og at feltet **Forfaldsdato** viser 12-02-14. Denne nye linje til den øverste overordnende vare, 1001, Turcykel, oprettes, da varen bruger en genbestillingsordrepolitik på **Ordre**, der betyder, at den skal leveres i et én-til-én-forhold ift. det pågældende behov, salgsordren på ti stykker.  

 De næste to planlægningslinjer er produktionsordrerne for turcykelhjul. Hver eksisterende ordre på fem i feltet **Oprindeligt antal** øges til 15 i feltet **Antal**. Begge produktionsordrer har uændrede forfaldsdatoer som anført i feltet **Aktionsmeddelelse**, der indeholder **Ret antal**. Det er også tilfældet for planlægningslinjen for vare 1300, bortset fra at dens oprundingsfaktor på 10,00 runder det sporede behov for 15 styk op til 20.  

 Alle andre planlægningslinjer indeholder aktionsmeddelelsen **Omplanlæg & ret antal**. Dette betyder, at bortset fra stigningen i antal så flyttes forfaldsdatoerne i relation til forsyningsplanen for at kunne inkludere det ekstra antal i den tilgængelige produktionstid (kapacitet). Købte komponenter omplanlægges og øges for at forsyne produktionsordrene. Fortsæt ved at analysere den nye plan.  

## <a name="analyzing-the-changed-planning-result"></a>Analyse af det ændrede planlægningsresultatet  
 Fordi alle lot-for-lot-planlagte elementer i filteret, 1100 og 1300, har en ændringsperiode på to uger, ændres alle deres eksisterende forsyningsordrer , så de opfylder det nye behov, som finder sted inden for de angivne to uger.  

 Flere planlægningslinjer ganges bare med tre for at angive 15 turcykler i stedet for 5, og forfaldsdatoerne flyttes tilbage i tiden for at levere det øgede antal til Kontorcentralen inden salgsordrens afsendelsesdato. For disse planlægningslinjer er alle mængder sporet. De resterende planlægningslinjer øges med ti stykker, og deres forfaldsdatoer flyttes. Disse planlægningslinjer har en vis mængde, som på grund af forskellige planlægningsparametre ikke er sporet. Fortsæt ved at vise nogle af disse ordresporingsposter.  

### <a name="to-view-order-tracking-entries-for-item-1250"></a>Få vist ordresporingsposter for vare 1250  

1.  Vælg planlægningslinjen for vare 1250, og vælg derefter handlingen **Ordresporing**.  

     De syv linjer i vinduet **Ordresporing** viser, hvordan fem eller ti stykker via baghjulet spores til turcyklerne på de to forskellige salgsordrer.  

     De sidste fem stykker er ikke-sporede. Fortsæt ved at analysere.  

2.  Vælg feltet **Ikkesporet antal**.  

     Vinduet **Ikkesporede planlægningselementer** viser, at vare 1250 bruger en planlægningsparameter, Oprundingsfaktor, på 10,00. Planlægningslinjen er derfor på 20 stykker i alt for at runde det faktiske behov op til nærmeste hele tal, der er deleligt med 10. De sidste fem stykker er et ikke-sporet antal, der skal bruges ifm. planlægningsparameteren.  

3.  Luk alle vinduer undtagen vinduet **Planlægningskladde**.  

### <a name="to-view-an-existing-order"></a>Sådan får du vist en eksisterende ordre  

1.  Vælg feltet **Referenceordrenr.** i planlægningslinjen for vare 1250 .  
2.  I vinduet **Fastlagt produktionsordre** for bagnavet. Den eksisterende ordre på ti stykker, som du oprettede i den første planlægningskørsel, åbnes.  
3.  Luk den fastlagte produktionsordre.  

 Hermed er gennemgangen af, hvordan planlægningssystemet bruges til automatisk registrering af behov, beregning af relevante forsyningsordrer iht. behovs- og planlægningsparametre samt efterfølgende automatisk oprettelse af andre typer forsyningsordrer med relevante datoer og antal færdig.  

## <a name="see-also"></a>Se også  
 [Gennemgang af forretningsprocesser](walkthrough-business-process-walkthroughs.md)   
 [Gennemgang: Manuel planlægning af forsyninger](walkthrough-planning-supplies-manually.md)   
 [Designoplysninger: Forsyningsplanlægning](design-details-supply-planning.md)

