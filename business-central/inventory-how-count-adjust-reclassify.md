---
title: Tælle, justere og ompostere inventar
description: Foretag fysisk optælling, foretag negative eller positive reguleringer, og rediger oplysninger, f.eks. placering eller lotnummer, på vareposter eller lagersteder.
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: adjustment, negative, positive, increase, decrease
ms.search.forms: 1327, 393, 392, 390, 7381, 7380, 7319, 7324, 7326, 7365
ms.date: 06/16/2021
ms.author: edupont
ms.openlocfilehash: 4267e7de6f34c3aa419d3d3fc78739c372b48a64
ms.sourcegitcommit: 00a8acc82cdc90e0d0db9d1a4f98a908944fd50a
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 06/29/2022
ms.locfileid: "9078044"
---
# <a name="count-adjust-and-reclassify-inventory-using-journals"></a>Tælle, justere og ompostere inventar ved hjælp af kladder

Mindst én gang hvert regnskabsår skal der foretages lageropgørelse, dvs. alle varer i lagerbeholdningen optælles for at se, om det antal, der er registreret i databasen, svarer til det faktiske fysiske antal på lagerstederne. Når det faktiske fysiske antal kendes, skal det bogføres til Finans som en del af lagervurderingen ved periodeafslutning.

Selvom alle varer på lageret optælles mindst en gang om året, har du måske besluttet, at nogle varer skal optælles oftere. Det kan være fordi, der er tale om særligt dyre vare, eller fordi de har en stor omsætningshastighed og udgør hovedparten af salget. Du kan tildele særlige optællingsperioder til de pågældende varer til dette formål. Du kan finde flere oplysninger i [Sådan udføres periodisk optælling](inventory-how-count-adjust-reclassify.md#to-perform-cycle-counting).

Hivs der er brug for en regulering af de registrerede lagerantal i forbindelse med optælling eller af andre årsager, kan du bruge en varekladde til at ændre lageropgørelsesposterne direkte, uden at bogføre forretningstransaktioner. Du kan også justere for en enkelt vare på varekortet.

Hvis det er nødvendigt at ændre attributter for varekladdeposter, kan du bruge vareomposteringskladden. Blandt de attributter, der typisk omposteres, er dimensioner og salgskampagnekoder, men du kan også udføre "overførsler mellem systemer" ved at ompostere placerings- og lokationskoder. Særlig fremgangsmåde anvendes, når du vil ompostere serie- eller lotnumre og deres udløbsdatoer. Du kan finde flere oplysninger i [Arbejde med serie- og lotnumre](inventory-how-work-item-tracking.md).

> [!NOTE]
> I avancerede lageropsætninger registreres varer på placeringer som lagerposter, ikke som vareposter. Derfor kan du foretage optælling, regulering og ompostering af særlige lagerkladder, der understøtter placeringer. Du kan derefter bruge særlige funktioner til at synkronisere de nye eller ændrede lagerposter med de tilknyttede vareposter, så de afspejler ændringer i lagerbeholdninger og lagerværdier. Dette beskrives i de specifikke procedurer nedenfor, hvis det er relevant.

## <a name="to-perform-a-physical-inventory"></a>Sådan foretages en lageropgørelse

Du skal foretage en lageropgørelse ved udgangen af hvert regnskabsår eller oftere, dvs. tælle antallet af fysiske varer, for at kontrollere, om det antal, der er registreret, er det samme som det fysiske antal varer, der er på lager. Hvis der er forskelle, skal du bogføre dem på de relevante varekonti, før du foretager en værdiansættelse af lageret.

> [!NOTE]
> Denne procedure beskriver, hvordan du foretager en lageropgørelse ved hjælp af en kladde, siden **Lageropgørelseskladde**. Du kan også udføre opgaven ved hjælp af dokumenter, siderne **Lageropgørelsesordre** og **Registrering af lageropgørelse**, som giver mere styring og understøtter distribution af optælling til flere medarbejdere. Du kan finde flere oplysninger i [Lageroptælling ved hjælp af dokumenter](inventory-how-count-inventory-with-documents.md).<br /><br />
> Bemærk, at dokumentbaserede funktioner ikke kan bruges til at optælle varer på placeringer, lagerposter.

Ud over den fysiske optællingsopgave omfatter hele processen følgende tre opgaver:

- Beregning af den forventede lagerbeholdning.
- Udskrivning af rapporten, der skal bruges til optælling.
- Indtastning og bogføring af den faktiske optalte lagerbeholdning.

Du kan udføre lageropgørelsen på følgende måder afhængigt af logistikopsætningen. Der er flere oplysninger under [Konfigurere lokalitetsstyring](warehouse-setup-warehouse.md).  

-   Hvis lokationen ikke benytter styret læg-på-lager og pluk (grundlæggende lageropsætning), skal du bruge siden **Lageropgørelseskladde** i menuen **Lager**, og procedurerne er i så fald meget lig dem, der skal udføres, når du foretager en lageropgørelse uden periodisk optælling.  
-   Hvis lokationen bruger styret læg-på-lager og pluk (avanceret lageropsætning), skal du først bruge siden **Lagersted - fysisk lagerkladde** og derefter bruge siden **Varekladde** til at køre funktionen **Beregn lagerregulering**.

### <a name="to-calculate-the-expected-inventory-in-basic-warehouse-configurations"></a>Sådan beregnes den forventede lagerbeholdning i grundlæggende lageropsætninger

1. Vælg ![Lightbulb, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **Varelageropgørelseskladder**, og vælg derefter det relaterede link.
2. Vælg handlingen **Beregn beholdning**.
3. På siden **Beregn beholdning** skal du angive betingelserne, der skal bruges til at oprette kladdelinjerne, f.eks. om der skal medtages varer med ingen registreret lagerbeholdning.
4. Angiv filtre, hvis du kun vil beregne lagerbeholdningen for visse varer, placeringer, lokationer eller dimensioner.
5. Vælg knappen **OK**.

> [!NOTE]  
>   Vareposterne behandles i overensstemmelse med de oplysninger, du har angivet, og der oprettes linjer i lageropgørelseskladden. Bemærk, at feltet **Antal (optalt)** udfyldes automatisk med det samme antal som feltet **Antal (beregnet)**. Med denne funktion er det ikke nødvendigt at indtaste den optalte lagerbeholdning for varer, der er de samme som det beregnede antal. Men hvis det optalte antal afviger fra det, der er indtastet i feltet **Antal (beregnet)**, skal du overskrive det med det antal, der faktisk er optalt.

### <a name="to-print-the-report-to-be-used-when-counting"></a>Sådan udskrives rapporten, der skal bruges til optælling

1. På siden **Lageropgørelseskladde**, der indeholder den beregnede forventede lagerbeholdning, skal du vælge **Udskriv**.
2. På siden **Lageropgørelsesoversigt** skal du angive, om rapporten skal vise det beregnede antal, og om rapporten skal indeholde lagervarer med serie- og lotnumre.
3. Angiv filtre, hvis du kun vil udskrive rapporten for visse varer, placeringer, lokationer eller dimensioner.
4. Vælg knappen **Udskriv**.

Medarbejderne kan nu fortsætte med at optælle lagerbeholdningen og registrere eventuelle afvigelser på den udskrevne rapport.

> [!NOTE]
> Det kan tage flere dage, før udskrevne rapporter vender tilbage, så de kan blive behandlet og bogført. Når du angiver og bogfører den faktiske optalte lagerbeholdning, justeres lagerbeholdningen, så den afspejler forskellen mellem den forventede og den faktiske optalte lagerbeholdning. Du skal gemme de oprindeligt beregnede kladdelinjer og ikke genberegne den forventede lagerbeholdning, fordi den forventede lagerbeholdning kan blive ændret, hvilket medfører forkerte lagerniveauer. Hvis du skal udstede flere rapporter, f.eks. for forskellige lokationer eller varegrupper, skal du oprette og føre separate kladdenavne.

### <a name="to-enter-and-post-the-actual-counted-inventory-in-basic-warehouse-configurations"></a>Sådan angives og bogføres den faktiske optalte lagerbeholdning i grundlæggende lageropsætninger

1. På hver linje på siden **Lageropgørelseskladde**, hvor den faktiske lagerbeholdning, der er optalt manuelt, afviger fra det beregnede antal, skal du indtaste den faktiske lagerbeholdning i feltet **Antal (optalt)**.

    Relaterede felter opdateres tilsvarende.

    > [!NOTE]  
    >   Hvis den fysiske optælling afslører forskelle, som skyldes, at varer er blevet bogført med forkerte lokationskoder, skal du ikke angive forskellene i lageropgørelseskladden. Brug i stedet omposteringskladden eller en overflytningsordre til at omdirigere varerne til de rigtige steder. Du kan finde flere oplysninger i Vareomposteringskladde eller Oprette overflytningsordrer.

2. Hvis du vil regulere det beregnede antal til det faktiske optalte antal, skal du vælge handlingen **Bogfør**.

    Både vareposter og lageropgørelsesposter oprettes. Åbn varekortet for at få vist de oprettede lageropgørelsesposter.

3. Vælg ![Lightbulb, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **Varer**, og vælg derefter det relaterede link.
4. For at kontrollere lageropgørelsen skal du åbne det relevante varekort og vælge handlingen **Lageropgørelsesposter**.

### <a name="to-calculate-the-expected-inventory-in-advanced-warehouse-configurations"></a>Sådan beregnes den forventede lagerbeholdning i avancerede lageropsætninger

Synkroniser vareposter og lager, før du foretager lagerplaceringsopgørelsen, ellers bliver de resultater, som du bogfører på lageropgørelseskladden og varekladden i sidste trin af proceduren, kombineret med de tidligere reguleringer af de varer, der er optalt. Du kan finde flere oplysninger i [synkronisere mængder i varekladden og lager](inventory-how-count-adjust-reclassify.md#to-synchronize-the-adjusted-warehouse-entries-with-the-related-item-ledger-entries)

1. Vælg ![Lightbulb, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **Lagerplacering - opg.kladde**, og vælg derefter det relaterede link.  
2. Vælg handlingen **Beregn beholdning**. Kørselsanmodningssiden **Lager - beregn beholdning** åbnes.  
3. Angiv filtre for, hvilke varer der skal optælles i kladden, og klik derefter på knappen **OK**.

    Der oprettes en linje for hver placering, der overholder filterkriterierne. Du kan stadig slette nogle af linjerne, men hvis du vil bogføre resultaterne som en lageropgørelse, skal du optælle varen på alle de placeringer, hvor den opbevares.  

     Hvis du kun har tid til at tælle varen på nogle af placeringerne og opdager afvigelser, kan du registrere dem og senere bogføre dem på varekladden ved at bruge funktionen **Beregn lagerregulering**.  

### <a name="to-print-the-report-to-be-used-when-counting"></a>Sådan udskrives rapporten, der skal bruges til optælling

1. Vælg ![Lightbulb, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") Ikon, skriv **Lageropgørelsesordrer**, og vælg derefter det relaterede link.  
2. Åbn rapportanmodningssiden, og udskriv de oversigter, hvor medarbejderne skal angive de vareantal, som de optæller på hver placering.  

Medarbejderne kan nu fortsætte med at optælle lagerbeholdningen og registrere eventuelle afvigelser på den udskrevne rapport.

### <a name="to-enter-and-post-the-actual-counted-inventory-in-advanced-warehouse-configurations"></a>Sådan angives og bogføres den faktiske optalte lagerbeholdning i avancerede lageropsætninger

1. Indtast de optalte antal i feltet **Antal (optalt)** i lageropgørelseskladden, når optællingen er foretaget.  

    > [!NOTE]  
    >  Feltet **Antal (beregnet)** i lagerplaceringsopgørelseskladden udfyldes automatisk på grundlag af lagerplaceringsregistreringerne, og disse antal kopieres til feltet **Antal (optalt)** på hver linje. Hvis det antal, der er optalt af lagermedarbejderen, afviger fra det, der er indsat af programmet i feltet Antal (optalt), skal du indtaste det antal, der faktisk er optalt.  

2. Når du har indtastet alle de optalte antal, skal du vælge handlingen **Registrer**.  

    Når du registrerer kladden, oprettes der to lagerposter i lagerjournalen for hver linje, der er optalt og registreret:  

    -   Hvis det beregnede og det fysiske antal afviger, registreres der et negativt eller positivt antal for placeringen, og der bogføres et udlignende antal til reguleringsplaceringen for lokationen.  
    -   Hvis det beregnede og det fysiske antal er ens, registreres der en post på 0 for både placeringen og reguleringsplaceringen. Posterne angiver, at der på registreringsdatoen blev udført en lagerplaceringsopgørelse, og at der ingen uoverensstemmelser var på lageret for varen.  

Når du bogfører lagerplaceringsopgørelsen, bogfører du hverken på varekladden, lageropgørelseskladden eller lagerværdikladden, men posterne er der til øjeblikkelig afstemning, når som helst det er nødvendigt. Hvis du imidlertid gerne vil have en præcis optegnelse over, hvad der foregår på lagerstedet, og du har optalt alle de placeringer, hvor varerne var registreret, skal du med det samme bogføre optællingsresultaterne som værende den fysiske lagerbeholdning. Du kan finde flere oplysninger i [synkronisere mængder i varekladden og lager](inventory-how-count-adjust-reclassify.md#to-synchronize-the-adjusted-warehouse-entries-with-the-related-item-ledger-entries).

## <a name="to-perform-cycle-counting"></a>Sådan udføres periodisk optælling

Selvom alle varer på lageret optælles mindst en gang om året, har du måske besluttet, at nogle varer skal optælles oftere. Det kan være fordi, der er tale om særligt dyre vare, eller fordi de har en stor omsætningshastighed og udgør hovedparten af salget. Du kan tildele særlige optællingsperioder til de pågældende varer til dette formål.

Du kan udføre periodisk optælling på følgende måder afhængigt af logistikopsætningen. Der er flere oplysninger under [Konfigurere lokalitetsstyring](warehouse-setup-warehouse.md).  

-   Hvis lokationen ikke benytter styret læg-på-lager og pluk (grundlæggende lageropsætning), skal du bruge siden **Lageropgørelseskladde** i menuen **Lager**, og procedurerne er i så fald meget lig dem, der skal udføres, når du foretager en lageropgørelse uden periodisk optælling.  
-   Hvis lokationen bruger styret læg-på-lager og pluk (avanceret lageropsætning), skal du først bruge siden **Lagersted - fysisk lagerkladde** og derefter bruge siden **Varekladde** til at køre funktionen **Beregn lagerregulering**.  

### <a name="to-set-up-counting-periods"></a>Sådan defineres optællingsperioder

Lageropgørelser foretages typisk med et fast interval, f.eks. hver måned, hvert kvartal eller årligt. Der er ingen begrænsninger med hensyn til lageroptællingsperioder.

Du konfigurerer hver lageroptællingsperiode, du vil bruge, og knytter en til hver vare. Når du foretager en lageropgørelse og bruger **Beregn optællingsperiode** i lageropgørelseskladden, bogføres linjer for varerne, der oprettes, automatisk.

1. Vælg ![Lightbulb, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **Lageropgørelse - optællingsperioder**, og vælg derefter det relaterede link.  
2. Udfyld felterne efter behov. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

### <a name="to-assign-a-counting-period-to-an-item"></a>Sådan tildeles en optællingsperiode til en vare

1. Vælg ![Lightbulb, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **Varer**, og vælg derefter det relaterede link.  
2. Vælg den vare, som der skal knyttes en optællingsperiode til.  
3. I feltet **Lageropg.-optællingsperiodekode** skal du vælge den relevante optællingsperiode.  
4. Vælg knappen **Ja** for at ændre koden og beregne den første optællingsperiode for varen. Næste gang du vælger at beregne en optællingsperiode i opgørelseskladden, vises elementet som en linje på siden **Lageropgørelse – varevalg**. Du kan derefter begynde at optælle varen på regelmæssig basis.

### <a name="to-initiate-a-count-based-on-counting-periods-in-basic-warehouse-configurations"></a>Sådan foretages en optælling, der er baseret på optællingsperioder i grundlæggende lageropsætninger

1. Vælg ![Lightbulb, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **Lageropgørelseskladde**, og vælg derefter det relaterede link.
2. Vælg handlingen **Beregn optællingsperiode**.

    Siden **Lageropgørelse - varevalg**, der viser de varer, der er tildelt optællingsperioder til, og som skal optælles, åbnes.
3. Foretag lageropgørelsen. Du kan finde flere oplysninger i [Sådan foretages en lageropgørelse](inventory-how-count-adjust-reclassify.md#to-perform-a-physical-inventory).

### <a name="to-initiate-a-count-based-on-counting-periods-in-advanced-warehouse-configurations"></a>Sådan foretages en optælling, der er baseret på optællingsperioder i avancerede lageropsætninger

1.  Vælg ![Lightbulb, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **Lagerplacering - opg.kladde**, og vælg derefter det relaterede link.  
2. Vælg handlingen **Beregn optællingsperiode**.

    Siden **Lageropgørelse - varevalg**, der viser de varer, der er tildelt optællingsperioder til, og som skal optælles, åbnes.
3. Foretag lageropgørelsen. Du kan finde flere oplysninger i [Sådan foretages en lageropgørelse](inventory-how-count-adjust-reclassify.md#to-perform-a-physical-inventory).  

    > [!NOTE]  
    >  Du skal optælle varen på alle de placeringer, der indeholder den pågældende vare. Hvis du sletter nogle af de placeringsliner, som er hentet til optælling, på siden **Lagerplaceringsopg.oversigt**, vil du ikke tælle alle varer på lageret. Hvis du senere bogfører sådanne ufuldstændige resultater i Lageropgørelseskladde, vil de bogførte beløb være forkerte.  

## <a name="to-adjust-the-inventory-of-one-item"></a>Sådan regulerer du lagerbeholdningen for én vare

Når du har foretaget en fysisk optælling af varen i dit lagerområde, kan du bruge funktionen **Reguler lager** til at registrere den faktiske lagerbeholdning.

1. Vælg ![Lightbulb, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **Varer**, og vælg derefter det relaterede link.
2. Vælg den vare, som du vil regulere lagerbeholdningen for, og vælg derefter handlingen **Reguler lager**.
3. Angiv det maksimale lagerantal, du vil registrere for varen, i feltet **Ny lagerbeholdning**.
4. Vælg knappen **OK**.

Varens lager er nu reguleret. Det nye antal vises i feltet **Beholdning** på siden **Varekort**.

Du kan også bruge funktionen **Reguler lager** som en enkel måde at placere købte varer på lager, hvis du ikke bruger købsfakturaer eller -ordrer til at registrere dine køb. Du kan finde flere oplysninger i [Registrere køb](purchasing-how-record-purchases.md).

> [!NOTE]  
>   Når du har reguleret lageret, skal du opdatere det med den aktuelle, beregnede værdi. Du kan finde flere oplysninger i [Regulere lagerbeholdningen](inventory-how-revalue-inventory.md).

### <a name="to-adjust-the-inventory-quantity-of-multiple-items-in-basic-warehouse-configurations"></a>Sådan reguleres lagerantallet for flere varer i grundlæggende lageropsætninger

På siden **Varekladde** kan du bogføre varetransaktionen direkte for at regulere lagerbeholdningen i forbindelse med køb, salg og op- og nedregulering af lageret uden brug af dokumenter.

Hvis du ofte bruger varekladden til at bogføre de samme eller lignende kladdelinjer, f.eks. i forbindelse med materialeforbrug, kan du bruge siden **Standardvarekladde** til at lette denne gentagne opgave. Du kan finde flere oplysninger i [Arbejde med standardkladder](ui-work-general-journals.md#work-with-standard-journals).

1. Vælg ![Lightbulb, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **Varekladder**, og vælg derefter det relaterede link.
2. Udfyld felterne efter behov. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
3. Vælg handlingen **Bogfør** for at regulere lagerbeholdningen.

### <a name="to-adjust-bin-quantities-in-advanced-warehouse-configurations"></a>Sådan reguleres placeringsantal i avancerede lageropsætninger

Hvis din lokation bruger styret læg-på-lager og pluk, skal du bruge **lagerkladden** til at postere alle positive og negative justeringer i varemængden, som du ved er reelle forøgelse , f.eks. varer, der tidligere er posteret som manglende, og som nu dukker op igen, eller reelle tab, f.eks. skader på varer, uden for det fysiske lager.  

I modsætning til postering af justeringer i varelagerkladden giver lagerkladden dig et yderligere justeringsniveau, som gør dine mængdeposter mere præcise. Lagerstedet har derfor altid en fuldstændig oversigt over, hvor mange varer, der er hjemme, og hvor de er placeret, men hver justering registreres ikke øjeblikkeligt i lageropgørelsen. I registreringsprocessen, krediterer eller debiterer programmet den reelle placering med mængdejustering og opretter en balanceringspost på en justeringsplacering, som er en justerbar placering uden reelle varer. Denne placering er defineret i **Lagerjust. placeringskode** på lokationskortet.

1.  Vælg ![Lightbulb, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **Lagerkladder**, og vælg derefter det relaterede link.  
2.  Udfyld oplysningerne på sidehovedet.  
3.  Udfyld feltet **Varenr.** på linjen.  
4.  Angiv den placering, hvor du anbringer de ekstra varer, eller hvor der er manglende varer.  
5.  Udfyld den mængde, der adskiller sig, i feltet **Mængde**. Hvis du har fundet ekstra varer, skal du angive en positiv mængde. Hvis der mangler varer, skal du angive en negativ mængde.  
6.  Vælg handlingen **Registrer**.

## <a name="to-synchronize-the-adjusted-warehouse-entries-with-the-related-item-ledger-entries"></a>Sådan synkroniseres de regulerede lagerposter med de relaterede vareposter

Du skal med jævne mellemrum (som er fastsat af virksomheden) bogføre posterne fra lagerreguleringsplaceringen i varekladden. Nogle virksomheder bogfører reguleringer på varekladden hver dag, mens andre kan nøjes med at afstemme med længere mellemrum.

1.  Vælg ![Lightbulb, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **Varekladde**, og vælg derefter det relaterede link.  
2.  Udfyld felterne på de enkelte kladdelinjer.  
3.  Vælg handlingen **Beregn lagerregulering**, og udfyld filtrene efter behov på anmodningssiden. Justeringerne beregnes kun for de poster på reguleringsplaceringen, der opfylder filterkriterierne.  
4.  På oversigtspanelet **Indstillinger** skal du udfylde feltet **Bilagsnr.** med et tal, du indtaster manuelt. Da der ikke er defineret nogen nummerserie for kørslen, skal du bruge det nummereringssystem, der er sat op for lagerstedet. Du kan også indtaste dags dato efterfulgt af dine initialer.  
5.  Vælg knappen **OK**. De positive og negative justeringer lægges sammen for hver vare, og der oprettes linjer i varekladden for de varer, hvor summen er et positivt eller negativt antal.  
6.  Bogfør kladdelinjerne for at tilføje afvigelserne i varekladden. Varebeholdningen på lagerplaceringerne svarer nu præcist til beholdningen i varekladden.  

## <a name="to-reclassify-an-items-lot-number"></a>Sådan omposteres en vares lotnummer

Hvis det er nødvendigt at ændre attributter for varekladdeposter, kan du bruge vareomposteringskladden. Blandt de attributter, der typisk omposteres, er dimensioner og salgskampagnekoder, men du kan også udføre "overførsler mellem systemer" ved at ompostere placerings- og lokationskoder.

Særlig fremgangsmåde anvendes, når du vil ompostere serie- eller lotnumre og deres udløbsdatoer. Du kan finde flere oplysninger i [Arbejde med serie- og lotnumre](inventory-how-work-item-tracking.md).

Følgende eksempel er baseret på en lokationskode. Trinene er de samme for andre typer vareattributter.

1. Vælg ![Lightbulb, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **Vareomposteringskladder**, og vælg derefter det relaterede link.
2. På siden **Vareomposteringskladder** skal du udfylde felterne efter behov.
3. I feltet **Lokationskode** skal du angive varens aktuelle lokationskode.
4. I feltet **Ny lokationskode** skal du angive varens nye lokationskode.
5. Vælg handlingen **Bogfør**.

Du kan finde oplysninger om overførsel af varer med fuld kontrol over de antal, der er leveret og modtaget, i [Overflytte lagerbeholdning mellem lokationer](inventory-how-transfer-between-locations.md).

## <a name="see-related-training-at-microsoft-learn"></a>Se relateret træning på [Microsoft Learn](/learn/modules/adjust-inventory/)

## <a name="see-also"></a>Se også

[Lageroptælling ved hjælp af dokumenter](inventory-how-count-inventory-with-documents.md)  
[Lagerbeholdning](inventory-manage-inventory.md)  
[Logistik](warehouse-manage-warehouse.md)  
[Salg](sales-manage-sales.md)  
[Køb](purchasing-manage-purchasing.md)  
[Arbejd med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]