---
title: 'Køre fuld planlægning, MPS eller MRP'
description: 'Planlægningssystemet kan beregne enten MPS (Master Production Schedule) eller MRP (Material Requirements Planning) efter anmodning, eller begge dele kan beregnes på én gang.'
author: brentholtorf
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.form: '99000852, 99000860'
ms.date: 06/22/2021
ms.author: bholtorf
---
# Køre fuld planlægning, MPS eller MRP

At "køre planlægningskladden" eller at "køre MRP" betyder, at du beregner hovedproduktionsplanen (MPS) på basis af eksisterende og forventet efterspørgsel. Planlægningssystemet kan beregne enten MPS (Master Production Schedule) eller MRP (Material Requirements Planning) efter anmodning, eller begge dele kan beregnes på én gang.  

-   MPS defineres som beregning af en hovedplan på basis af et faktisk behov og behovsprognosen. MPS-beregningen bruges til slutvarer, der har en prognose- eller en salgsordrelinje. Disse varer kaldes MPS-varer og identificeres dynamisk, når beregningen begynder.  
-   MRP defineres som beregning af materialebehov på basis af et faktisk komponentbehov og behovsprognosen på komponentniveau. MRP beregnes kun for varer, der ikke er MPS-varer. Det overordnede formål med MRP er at udarbejde formelle planer med tidsangivelser og opdelt efter varer, så den rigtige vare kan leveres på det rigtige tidspunkt, til det rigtige sted og i det rette antal.  

Der bruges de samme planlægningsalgoritmer til både MPS og MRP. Planlægningsalgoritmerne omhandler modregning, genbrug af eksisterende genbestillingsordrer og aktionsmeddelelser. Under planlægningen tages der højde for, hvad der er brug for, eller hvad der vil blive brug for (efterspørgsel), og hvad der allerede er på lager eller forventes at være på lager (udbud). Når disse antal sammenholdes og modregnes, giver [!INCLUDE[prod_short](includes/prod_short.md)] aktionsmeddelelser. Aktionsmeddelelser er forslag til oprettelse af en ny ordre, ændring af en ordre (antal eller dato) eller annullering af en allerede bestilt ordre. Betegnelsen "ordre" omfatter indkøbsordrer, montageordrer, produktionsordrer og overflytningsordrer.

Links, der er oprettet af planlægningssystemet mellem behov og den relaterede levering, kan spores på siden **Ordresporing**. Du kan finde flere oplysninger i [Spore relationer mellem behov og forsyning](production-how-track-demand-supply.md).   

Et ordentligt planlægningsresultat afhænger af de valgte indstillinger til varekort, montagestyklister, produktionsstyklister og ruter.  

## Metoder til oprettelse af en plan  

-   **Beregn totalplan:** Denne funktion behandler eller beregner hele materialeplanen. Processen starter med at slette alle planlagte forsyningsordrer, der er indlæst i øjeblikket. Alle elementer i databasen planlægges om.  
-   **Beregn nettoplan**: Den funktion behandler en nettoplan. Varerne indgår i nettoplanen fra to former for ændringer:  
    - **Ændret behov/forsyning:** Det kan være ændrede antal i salgsordrer, behovsprognoser, montageordrer, produktionsordrer eller købsordrer. En uforudset ændring af lagerbeholdningen kan også betragtes som en ændring af antallet.  
    - **Ændrede planlægningsparametre:** Det kan være ændringer i sikkerhedslager, genbestillingspunkt, stykliste og ændringer i interval eller beregning af leveringstid.  
-   **Hent aktionsmeddelelser:** Denne funktion kan bruges til planlægning på kort sigt, fordi den udsender aktionsmeddelelser, der giver brugeren besked om ændringer, der måtte være sket, siden den sidste totalplan eller nettoplan blev beregnet.  

Hver planlagt metode, genererer [!INCLUDE[prod_short](includes/prod_short.md)] kladdeposter, hvor der forudsættes uendelig kapacitet. Der tages ikke hensyn til arbejdscenter- og produktionsressourcekapacitet, når du udvikler tidsplaner.  

> [!IMPORTANT]  
>  Funktionen Beregn totalplan er den mest almindelige proces. Men funktionerne Beregn plan og Udfør aktionsmeddelelse kan bruges til kørsel af processen Beregn nettoplan.  
>   
>  Funktionen Hent aktionsmeddelelser kan udføres mellem totalplanlægning og nettoplanlægning, fordi den giver et umiddelbart indtryk af, hvilke følgevirkninger en planændring vil få. Men det er ikke meningen, at denne fremgangsmåde skal bruges i stedet for fuld totalplanlægning eller nettoplanlægning.  

## Sådan beregnes planlægningskladden  
1.  Vælg ![Lightbulb, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **Planlægningskladdeside**, og vælg derefter det relaterede link.  
2.  Vælg handlingen **Beregn totalplan** for at åbne siden **Beregn Plan**.  
3.  I oversigtspanelet **Indstillinger** skal du udfylde felterne som beskrevet i følgende tabel.  

    |Felt|Beskrivelse|  
    |---------------------------------|---------------------------------------|  
    |**MPS**|Vælg det for at starte beregningen af en overordnet produktionsplan. Varer med åbne salgsordrer eller behovsprognoser indgår i kørslen.|  
    |**MRP**|Vælg at starte materialebehovsplanlægningen. Varer med tilhørende behov indgår i kørslen. Typisk køres MPS og MRP på samme tid. Hvis du vil køre MPS og MRP samtidigt, skal du vælge feltet **Kombineret hovedplan-/MRP-beregning** i oversigtspanelet **Planlægning** på siden **Produktionsopsætning**.|  
    |**Startdato**|Denne dato bruges til vurdering af varedisponering. Hvis lagerbeholdningen for en vare er nået ned under genbestillingspunktet, flyttes en genbestillingsordre længere fremad i planen, regnet fra denne dato. Hvis lagerbeholdningen for varen er under det niveau, der regnes som sikkerhedslager (pr. startdatoen), flyttes en genbestillingsordre, der forfalder på datoen for planlægningsstarten længere bagud.|  
    |**Slutdato**|Dette er planlægningshorisontens slutdato. Der tages hverken højde for behov eller forsyning efter denne dato. Hvis genbestillingscyklen for en vare rækker ud over slutdatoen, er den effektive planlægningshorisont for varen lig med ordredato + genbestillingscyklus.<br /><br /> Planlægningshorisonten er den periode, planen omfatter. Hvis horisonten er for kort, kan varer med en længere leveringstid ikke bestilles til tiden. Hvis horisonten er for lang, bruges der for meget tid på at gennemgå og behandle oplysninger, der sandsynligvis vil ændre sig, før de skal bruges. Det er muligt at angive én planlægningshorisont til produktion og en længere horisont til indkøb, selvom det ikke er nødvendigt. Der skal angives en planlægningshorisont til indkøb og produktion for at dække den samlede leveringstid for komponenter.|  
    |**Stop, og vis første fejl**|Vælg denne indstilling, hvis du ønsker, at planlægningskørslen skal stoppe, så snart der registreres en fejl. Samtidig vises en meddelelse med oplysninger om den første fejl. Hvis der er fejl, vises kun de fejlfri planlægningslinjer i planlægningskladden, som blev oprettet, inden fejlen opstod. Hvis du ikke markerer feltet, fortsætter kørslen **Beregn plan**, indtil den er færdig, og fejl afbryder altså ikke kørslen. Hvis der er registreret fejl under kørslen, vil der efter kørslen blive vist en meddelelse om, hvor mange varer, der berøres af fejlene. Derefter åbnes siden **Log over planlægningsfejl** med flere oplysninger om fejlen og hyperlinks til det eller de berørte varekort.|  
    |**Brug forecast**|Vælg et forecast, der skal medtages som efterspørgsel, når planlægningskørslen udføres. Du kan oprette et standardforecast i oversigtspanelet **Planlægning** på siden **Produktionsopsætning**.|  
    |**Udeluk forecast før**|Angiv, hvor stor en del af det valgte forecast, der skal indgå i planlægningskørslen, ved at angive en dato, så forecastbehov før denne dato ikke medregnes. På den måde kan du holde forældede oplysninger ude af planlægningen.|  
    |**Respekter planlægningsparametre for undtagelsesadvarsler**|Feltet er som standard valgt.<br /><br /> Efterspørgsel på planlægningslinjer med advarsler modificeres normalt ikke i henhold til planlægningsparametre. Planlægningssystemet foreslår i stedet for kun en forsyning til at dække det nøjagtige behovsantal. Du kan dog definere visse planlægningsparametre for planlægningslinjer, der skal overholdes med visse advarsler.<br /><br />|  

4.  I oversigtspanelet **Vare** kan du indstille filtre for kørslen af planlægningsrutinerne baseret på vare, varebeskrivelse eller lokation.  
5.  Vælg knappen **OK**. Kørslen starter, og planlægningslinjerne indsættes i planlægningskladden.  

## Udføre aktionsmeddelelser  
1.  På siden **Planlægningskladde** skal du vælge handlingen **Udfør aktionsmeddelelse**.  
2.  Angiv, hvordan du opretter forsyninger i oversigtspanelet **Indstillinger**. Udfyld felterne som beskrevet i følgende tabel.  

    |Felt|Beskrivelse|  
    |---------------------------------|---------------------------------------|  
    |**Produktionsordre**|Angiv, hvordan du vil oprette produktionsordrer. Du kan gøre det direkte fra planlægningslinjeforslagene. Du kan oprette enten planlagte eller fastlagte produktionsordrer.|  
    |**Montageordre**|Angiv, hvordan du vil oprette montageordrer. Du kan gøre det direkte fra planlægningslinjeforslagene.|  
    |**Købsordre**|Angiv, hvordan du vil oprette købsordrer. Du kan gøre det direkte fra planlægningslinjeforslagene.<br /><br /> Hvis du vælger at kopiere forslagene til planlægningslinjer for købsordrer til indkøbskladden, skal du vælge skabelon- og kladdenavnet.|  
    |**Overflytningsordre**|Angiv, hvordan du vil oprette overførselsordrer. Du kan gøre det direkte fra planlægningslinjeforslagene.<br /><br /> Hvis du vælger at kopiere forslagene til planlægningslinjer for overflytningsordrer til indkøbskladden, skal du vælge skabelon- og kladdenavnet.|  
    |**Kombiner overførselsordrer**|Vælg denne indstilling, hvis du vil kombinere overflytningsordrer.|  
    |**Stop, og vis første fejl**|Vælg, om du ønsker at kørslen **Udfør aktionsmedl. - plan.** skal stoppe, så snart der registreres en fejl. Samtidig vises en meddelelse med oplysninger om den første fejl. Hvis der er fejl, vil kun de planlægningslinjer, der blev behandlet, inden fejlen opstod, medføre forsyningsordrer.|  

3.  I oversigtspanelet **Planlægningslinje** kan du angive filtre, der begrænser udførelsen af aktionsmeddelelser.  
4.  Vælg knappen **OK**.  

Kørslen sletter linjerne i planlægningskladden, når aktionsmeddelelsen er udført. De øvrige linjer bliver stående i planlægningskladden, indtil de enten accepteres på et senere tidspunkt eller slettes. Du kan også slette linjerne manuelt.  

## Aktionsmeddelelser  
Aktionsmeddelelser udstedes af ordresporingssystemet, når der ikke kan registreres en saldo inden for det eksisterende ordrenetværk. Du kan få dem vist som forslag til procesændringer, der kan genskabe ligevægten mellem forsyning og behov.  

Aktionsmeddelelser oprettes for ét niveau ad gangen, for hver enkelt vares laveste-niveau-kode. Det sikrer, at der tages højde for alle varer, der udsættes for ændringer i forsyning eller behov.  

Du kan undgå aktionsmeddelelser om mindre, overflødige eller uvæsentlige ændringer ved at oprette aktionsgrænser, som sikrer, at der kun oprettes aktionsmeddelelser om vareantal eller dage, der ligger ud over dine grænseværdier.  

Når du har læst forslaget i aktionsmeddelelsen og bestemt dig til, om du vil efterkomme alle eller nogle af de viste forslag, skal du vælge feltet **Accepter aktionsmeddelelse**, og så er du klar til at opdatere planerne tilsvarende.  

> [!NOTE]  
>  En aktionsmeddelelse er et forslag om at oprette en ny ordre, annullere en ordre eller ændre antallet eller datoen i en ordre. En ordre kan være en købsordre, overflytningsordre eller produktionsordre.  

Hvis der ikke er overensstemmelse mellem forsyning og behov, oprettes følgende aktionsmeddelelser.  

|Aktionsmeddelelse|Beskrivelse|  
|--------------------|---------------------------------------|  
|**Nyt**|Hvis forslagene i aktionsmeddelelserne **Ret antal**, **Omplanlæg** eller **Omplanlæg & ret antal** i eksisterende ordrer ikke er tilstrækkeligt til at imødekomme et behov, oprettes aktionsmeddelelsen **Ny**, som dermed foreslår, at der oprettes en ny ordre. Aktionsmeddelelsen **Ny** oprettes også, hvis der ikke findes eksisterende forsyningsordrer inden for den pågældende vares genbestillingscyklus. Denne parameter bestemmer, hvor mange perioder fremad og bagud i disponeringsprofilen, der skal søges efter en ordre, hvor planlægningen kan ændres.|  
|**Ret antal**|Hvis der sker en ændring af antallet til det behov, der kan spores til en eller flere forsyningsordrer, oprettes aktionsmeddelelsen **Ret antal**, hvilket angiver, at det tilhørende forsyningsantal skal ændres, så det svarer til behovsændringen. Hvis der opstår et nyt behov, søger [!INCLUDE[prod_short](includes/prod_short.md)] efter den nærmeste eksisterende forsyningsordre, der ikke er reserveret, inden for genbestillingscyklen, hvorefter der udstedes en aktionsmeddelelse med forslaget Ret antal til denne ordre.|  
|**Omplanlæg**|Hvis datoen i en forsynings- eller behovsordre ændres, og det forrykker balancen i ordrenetværket, udstedes aktionsmeddelelsen **Omplanlæg**. Hvis forholdet mellem behov og forsyning er en-til-en, udstedes en aktionsmeddelelse med forslag om, at forsyningsordren flyttes tilsvarende. Hvis forsyningsordren dækker behov, der stammer fra flere salgsordrer, omplanlægges forsyningsordren til en dato, der er lige med datoen for det første behov.|  
|**Omplanlæg & ret antal.**|Hvis både datoer og antal i en ordre er ændret, er det nødvendigt at ændre planer, så der tages højde for begge dele. Der udstedes en aktionsmeddelelse, der dækker begge ændringer, **Omplanlæg og ret antal**, for at sikre at balancen i ordrenetværket genoprettes.|  
|**Annuller**|Hvis et behov slettes, som ellers har været dækket fra ordre til ordre, udstedes der en aktionsmeddelelse med forslag om, at alle tilhørende forsyningsordrer annulleres. Hvis forholdet ikke er ordre-til-ordre, oprettes en aktionsmeddelelse med forslag om, at antallet bør rettes for at reducere forsyningen. Hvis det viser sig, at en forsyningsordre af andre årsager, f.eks. lagerreguleringer, ikke er nødvendig på det tidspunkt, hvor aktionsmeddelelserne oprettes af brugeren, opretter [!INCLUDE[prod_short](includes/prod_short.md)] en aktionsmeddelelse med forslag om **Annuller** i kladden.|  

## Se også  
[Skabelon](production-planning.md)  
[Konfigurere produktion](production-configure-production-processes.md)  
[Produktion](production-manage-manufacturing.md)    
[Lagerbeholdning](inventory-manage-inventory.md)  
[Køb](purchasing-manage-purchasing.md)  
[Designoplysninger: Forsyningsplanlægning](design-details-supply-planning.md)   
[Konfigurere bedste fremgangsmåder: Forsyningsplanlægning](setup-best-practices-supply-planning.md)  
[Arbejd med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]