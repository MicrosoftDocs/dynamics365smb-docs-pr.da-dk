---
title: 'Tælle, justere og ompostere inventar'
description: 'Få mere at vide om, hvordan du foretager fysisk optælling og foretager reguleringer og omposteringer.'
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bholtorf
ms.service: dynamics365-business-central
ms.topic: how-to
ms.date: 12/20/2022
ms.custom: bap-template
---
# <a name="count-adjust-and-reclassify-inventory-using-journals"></a>Tælle, justere og ompostere inventar ved hjælp af kladder

Fysisk optælling af alle varerne på lager for at sikre, at antallet er korrekte. Nogle virksomheder foretager en årlig optælling af alle eller blot nogle emner. Når du har talt varerne med, skal du bruge kladder til at bogføre de faktiske antal i finansregnskabet. F.eks. når du værdisætter lager ved slutningen af en periode.

Hvis du vil optælle nogle varer hyppigere end andre, f.eks. på grund af deres værdi, skal du bruge periodisk optælling. Du kan tildele særlige optællingsperioder til varerne til dette formål. Få mere at vide i [Prøv at foretage en periodisk optælling](inventory-how-count-adjust-reclassify.md#to-do-cycle-counting).

Hvis du vil justere antal efter en fysisk optælling eller andre formål, skal du bruge en varekladde til at ændre lagerposterne uden bogføringstransaktioner. Du kan også justere mængden for en enkelt vare på varekortet.

Brug en vareomposteringskladde til at ændre attributter for varekladdeposter. Standardattributter, der genklassificeres, omfatter dimensioner og salgskampagnekoder. Omposteringskladder kan også bruges til overførsler ved at genklassificere placeringer og lokationskoder. Særlig fremgangsmåde anvendes, når du vil ompostere serie- eller lotnumre og deres udløbsdatoer. Du kan finde flere oplysninger i [Arbejde med serie- og lotnumre](inventory-how-work-item-tracking.md).

> [!NOTE]
> I processer med flere trin registreres varer på placeringer som lagerposter, ikke som vareposter. Derfor kan du foretage optælling, regulering og ompostering af særlige lagerkladder, der understøtter placeringer. Du kan derefter bruge særlige funktioner til at synkronisere de nye eller ændrede lagerposter med de tilknyttede vareposter, så de afspejler ændringer i lagerbeholdninger og lagerværdier.

[!INCLUDE [edit-in-excel](includes/edit-in-excel.md)]

## <a name="to-count-physical-inventory"></a>Fysisk lagerbeholdningsoptælling

Foretag en lageropgørelse ved udgangen af hvert regnskabsår eller oftere, dvs. tælle antallet af fysiske varer, for at kontrollere, om det antal, der er registreret, er det samme som det fysiske antal varer, der er på lager. Optællinger sker typisk i slutningen af et regnskabsår, men nogle gange sker det oftere. Hvis der er differencer, skal du bogføre det aktuelle antal varekonti <!--accounts, or ledger?--> Inden du foretager lagerværdien.

> [!NOTE]
> Denne procedure beskriver, hvordan du foretager en lageropgørelse ved hjælp af en kladde, siden **Lageropgørelseskladde**. Du kan bruge dokumenter på siderne **Fysisk lagerordre** og **Fysisk lagerregistrering**. Disse dokumenter giver mere kontrol og support til distribution af optællingsarbejdet til flere medarbejdere. Flere oplysninger i [Tæl lageropgørelse ved hjælp af dokumenter](inventory-how-count-inventory-with-documents.md)<br /><br />
> Bemærk, at dokumentbaserede funktioner ikke kan bruges til at optælle varer på placeringer, lagerposter.

Optællingsprocessen omfatter også følgende opgaver:

- Beregning af den forventede lagerbeholdning.
- Udskrivning af rapporten, der skal bruges til optælling.
- Indtastning og bogføring af faktiske mængder.

Du kan udføre lageropgørelsen på følgende måder afhængigt af logistikopsætningen. Der er flere oplysninger under [Konfigurere lokalitetsstyring](warehouse-setup-warehouse.md).  

- Hvis lokationen ikke bruger styret læg-på-lager og pluk, skal du bruge siden **Lageropgørelseskladde**. Fremgangsmåden svarer til det fysiske lager uden periodisk optælling.  
- Hvis lokationen bruger styret læg-på-lager og pluk, skal du bruge siden **Lagerplaceringsopgørelseskladde**. Brug derefter **Varekladder**-siden til at udføre beregningen af **Lagerstedsregulering**-handlingen. <!--We should say what to do on each of these pages.-->

### <a name="to-calculate-expected-inventory-in-basic-warehouse-configurations"></a>Sådan beregnes den forventede lagerbeholdning i grundlæggende lageropsætninger

1. Vælg ![Lightbulb, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **Varelageropgørelseskladder**, og vælg derefter det relaterede link.
2. Vælg handlingen **Beregn beholdning**.
3. På siden **Beregn beholdning** skal du angive betingelserne, der skal bruges til at oprette kladdelinjerne, f.eks. om der skal medtages varer med ingen registreret lagerbeholdning.
4. Angiv filtre, hvis du kun vil beregne lagerbeholdningen for visse varer, placeringer, lokationer eller dimensioner.
5. Vælg knappen **OK**.

> [!NOTE]  
> Vareposter behandles i overensstemmelse med de oplysninger, du har angivet, og der oprettes linjer i lageropgørelseskladden. Bemærk, at feltet **Antal (lager)** udfyldes automatisk med det samme antal som feltet **Antal (beregnet)**. Du behøver ikke at angive den optalte mængde for varer, hvor disse værdier stemmer overens. Hvis det optalte antal imidlertid er forskelligt, skal du angive det antal, der er optalt.

### <a name="to-print-the-report-to-be-used-when-counting"></a>Sådan udskrives rapporten, der skal bruges til optælling

1. På siden **Lageropgørelseskladde**, der indeholder den beregnede forventede lagerbeholdning, skal du vælge **Udskriv**.
2. På siden **Lageropgørelsesoversigt** skal du angive, om rapporten skal vise det beregnede antal, og om rapporten skal indeholde lagervarer med serie- og lotnumre.
3. Angiv filtre, hvis du kun vil udskrive rapporten for visse varer, placeringer, lokationer eller dimensioner.
4. Vælg **Udskriv**.

Lagermedarbejderne kan nu fortsætte med at optælle lagerbeholdningen og registrere eventuelle afvigelser på den udskrevne rapport.

> [!NOTE]
> Det kan tage flere dage, før udskrevne rapporter vender tilbage, så de kan blive behandlet og bogført. Når du angiver og bogfører den faktiske optalte lagerbeholdning, justeres lagerbeholdningen, så den afspejler forskellen mellem den forventede og den faktiske optalte lagerbeholdning. Du skal gemme de oprindeligt beregnede kladdelinjer og ikke genberegne den forventede lagerbeholdning, fordi den forventede lagerbeholdning kan blive ændret, hvilket medfører forkerte lagerniveauer. Hvis du skal udstede flere rapporter, f.eks. for forskellige lokationer eller varegrupper, skal du oprette og føre separate kladdenavne.

### <a name="to-enter-and-post-the-actual-counted-inventory-in-basic-warehouse-configurations"></a>Sådan angives og bogføres den faktiske optalte lagerbeholdning i grundlæggende lageropsætninger

1. På hver linje på siden **Lageropgørelseskladde**, hvor den faktiske lagerbeholdning, der er optalt manuelt, afviger fra det beregnede antal, skal du indtaste den faktiske lagerbeholdning i feltet **Antal (optalt)**.
  
  > [!NOTE]  
  > Hvis den fysiske optælling afslører forskelle, som skyldes, at varer er blevet bogført med forkerte lokationskoder, skal du ikke angive forskellene i lageropgørelseskladden. Brug i stedet omposteringskladden eller en overflytningsordre til at omdirigere varerne til de rigtige steder. 

2. Hvis du vil regulere det beregnede antal til det faktiske optalte antal, skal du vælge handlingen **Bogfør**.

    Bogføring opretter vareposter og lageropgørelsesposter. Åbn varekortet for at få vist de oprettede lageropgørelsesposter. <!--Where are they shown on an item?-->

3. Vælg ![Lightbulb, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **Varer**, og vælg derefter det relaterede link.
4. For at kontrollere lageropgørelsen skal du åbne det relevante varekort og vælge handlingen **Lageropgørelsesposter**. <!--I don't see this action -->

### <a name="to-calculate-the-expected-inventory-in-advanced-warehouse-configurations"></a>Sådan beregnes den forventede lagerbeholdning i avancerede lageropsætninger

Synkronisere vareposter og lagersteder <!--warehouse what?--> før du beregner lagerbeholdning. Ellers bliver det, du bogfører til lageropgørelseskladden, det fysiske lager resultat kombineret med andre lagerreguleringer for varerne. Du kan finde flere oplysninger i [Synkronisere mængder i varekladden og lager](inventory-how-count-adjust-reclassify.md#to-synchronize-the-adjusted-warehouse-entries-with-the-related-item-ledger-entries)

1. Vælg ![Lightbulb, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **Lagerplaceringsopgørelseskladde**, og vælg derefter det relaterede link.  
2. Vælg handlingen **Beregn lager** for at åbne siden **Beregn lager på lagersted**.  
3. Angiv filtre for, hvilke varer der skal optælles i kladden, og klik derefter på knappen **OK**.

   [!INCLUDE [prod_short](includes/prod_short.md)] opretter en linje for hver placering, der overholder filterkriterierne. Du kan stadig slette nogle af linjerne, men hvis du vil bogføre resultaterne som en lageropgørelse, skal du optælle varen på alle de placeringer, hvor den opbevares.  

   Hvis du kun har tid til at tælle varen på nogle af placeringerne og opdager afvigelser, kan du registrere dem og senere bogføre dem på varekladden ved at bruge funktionen **Beregn lagerregulering**. <!--I don't see this action-->  

### <a name="to-enter-and-post-the-actual-counted-inventory-in-advanced-warehouse-configurations"></a>Sådan angives og bogføres den faktiske optalte lagerbeholdning i avancerede lageropsætninger

1. Indtast de optalte antal i feltet **Antal (optalt)** i **Lagerplaceringsopgørelseskladde**, når optællingen er foretaget.  

    > [!NOTE]  
    >  Feltet **Antal (beregnet)** udfyldes på basis af placeringsposter. Denne mængde er kopieret til feltet **Antal (optalt)** på hver linje. Hvis antallene i disse felter ikke stemmer overens, skal du angive det faktiske antal.  

2. Når du har indtastet alle de optalte antal, skal du vælge handlingen **Registrer**.  

    Når du registrerer kladden, opretter [!INCLUDE [prod_short](includes/prod_short.md)] to lagerposter i lagerjournalen for hver linje, der er optalt og registreret:  

    - Hvis det beregnede og det fysiske antal afviger, registreres der et negativt eller positivt antal for placeringen, og der bogføres et udlignende antal til reguleringsplaceringen for lokationen.  
    - Hvis det beregnede og det fysiske antal er ens, registrerer [!INCLUDE [prod_short](includes/prod_short.md)] **0** for både placeringen og reguleringsplaceringen. 

Når du registrerer det fysiske lager, skal du ikke bogføre på varen, lagerbeholdningen eller værdiposterne. Posterne er dog tilgængelige til afstemning, når der er behov for det. Hvis du vil bevare antallet nøjagtige, efter at du har talt varerne på alle placeringer, skal du bogføre resultaterne som et lagerplaceringsopgørelse <!--physical inventory journal-->. Du kan finde flere oplysninger i [Synkronisere mængder i varekladden og lager](inventory-how-count-adjust-reclassify.md#to-synchronize-the-adjusted-warehouse-entries-with-the-related-item-ledger-entries).

## <a name="to-do-cycle-counting"></a>Sådan udføres periodisk optælling

Du kan tælle elementer, så ofte du vil. F. eks. fordi de er mere værdifulde, eller fordi de er hurtigt og nemt at flytte og en stor del af virksomheden. Angiv optællingsfrekvensen ved at tildele varerne særlige optællingsperioder.

Du kan udføre periodisk optælling på følgende måder afhængigt af logistikopsætningen. Flere oplysninger i [Sådan konfigureres Warehouse Management](warehouse-setup-warehouse.md).  

- Hvis lokationen ikke bruger styret læg-på-lager og pluk, skal du bruge siden **Lageropgørelseskladde**. Fremgangsmåden svarer til det fysiske lager uden periodisk optælling.  
- Hvis lokationen bruger styret læg-på-lager og pluk, skal du bruge siden **Lagerplaceringsopgørelseskladde**. Brug derefter **Varekladder**-siden til at udføre beregningen af **Lagerstedsregulering**-handlingen. <!--we should say what to do on each of these pages-->  

### <a name="to-set-up-counting-periods"></a>Sådan defineres optællingsperioder

Lageropgørelser foretages typisk med et fast interval, f.eks. hver måned, hvert kvartal eller årligt. Du konfigurerer hver lageroptællingsperiode, du vil bruge, og knytter en til hver vare. Når du foretager en lageropgørelse og bruger **Beregn optællingsperiode** i **lageropgørelseskladden**, bogføres linjer for varerne, der oprettes, automatisk.

1. Vælg ![Lightbulb, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **Lageropgørelse - optællingsperioder**, og vælg derefter det relaterede link.  
2. Udfyld felterne efter behov. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

### <a name="to-assign-a-counting-period-to-an-item"></a>Sådan tildeles en optællingsperiode til en vare

1. Vælg ![Lightbulb, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **Varer**, og vælg derefter det relaterede link.  
2. Vælg den vare, som der skal knyttes en optællingsperiode til.  
3. I feltet **Lageropg.-optællingsperiodekode** skal du vælge den relevante optællingsperiode.  

> [!NOTE]
> Hvis du ændrer optællingsperioden, vises der oplysninger om resultatet af ændringen i en meddelelse. Vælg knappen **Ja** for at ændre koden og beregne den første optællingsperiode for varen. Næste gang du vælger at beregne en optællingsperiode i opgørelseskladden, vises elementet som en linje på siden **Lageropgørelse – varevalg**. Derefter kan du optælle varen regelmæssigt.

### <a name="to-start-a-count-based-on-counting-periods-in-basic-warehouse-configurations"></a>Sådan foretages en optælling, der er baseret på optællingsperioder i grundlæggende lageropsætninger

1. Vælg ![Lightbulb, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **Lageropgørelseskladde**, og vælg derefter det relaterede link.
2. Vælg handlingen **Beregn optællingsperiode**.

    Siden **Lageropgørelse - varevalg**, der viser de varer, der er tildelt optællingsperioder til, og som skal optælles, åbnes.
3. Fysisk lagerbeholdningsoptælling. Flere oplysninger i [Tæl lageropgørelse ved hjælp af dokumenter](inventory-how-count-adjust-reclassify.md#to-count-physical-inventory).

### <a name="to-start-a-count-based-on-counting-periods-in-advanced-warehouse-configurations"></a>Sådan foretages en optælling, der er baseret på optællingsperioder i avancerede lageropsætninger

1. Vælg ![Lightbulb, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **Lagerplaceringsopgørelseskladde**, og vælg derefter det relaterede link.  
2. Vælg handlingen **Beregn optællingsperiode**.

    Siden **Lageropgørelse - varevalg**, der viser de varer, der er tildelt optællingsperioder til, og som skal optælles, åbnes.
3. Fysisk lagerbeholdningsoptælling. Flere oplysninger i [Tæl lageropgørelse ved hjælp af dokumenter](inventory-how-count-adjust-reclassify.md#to-count-physical-inventory).  

   > [!NOTE]  
   > Optælle varen på alle de placeringer, der indeholder den. Hvis du sletter nogle af de placeringsliner, som er hentet til optælling, på siden **Lagerplaceringsopg.oversigt**, vil du ikke tælle alle varer på lageret.  

## <a name="to-adjust-the-quantity-of-one-item"></a>Sådan regulerer du lagerbeholdningen for én vare

Når du har foretaget en fysisk optælling af varen i dit lagerområde, kan du bruge funktionen **Reguler lager** til at registrere den faktiske lagerbeholdning.

1. Vælg ![Lightbulb, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **Varer**, og vælg derefter det relaterede link.
2. Vælg den vare, som du vil regulere lagerbeholdningen for, og vælg derefter handlingen **Reguler lager**.
3. Angiv resultatet af optællingen i feltet **Nyt lager** for lokationen.
4. Vælg knappen **OK**.

<!-- I don't see a "Quantity on Hand" field on the Item Card page. Should this point to the options for viewing availability?

The item’s inventory is adjusted. The new quantity is shown in the **Quantity on Hand** field on the **Item Card** page.-->

Du kan også bruge funktionen **Reguler lager** som en enkel måde at placere købte varer på lager, hvis du ikke bruger købsfakturaer eller -ordrer til at registrere dine køb. Flere oplysninger i [Registrere Køb](purchasing-how-record-purchases.md).

> [!NOTE]  
> Når du har reguleret lageret, skal du opdatere den aktuelle værdi. Du kan finde flere oplysninger i [Regulere lagerbeholdningen](inventory-how-revalue-inventory.md).

### <a name="to-adjust-the-quantities-of-multiple-items-in-basic-warehouse-configurations"></a>Sådan reguleres antallet for flere varer i grundlæggende lageropsætninger

På siden **Varekladde** kan du bogføre varetransaktionen direkte for at regulere lagerbeholdningen i forbindelse med køb, salg og op- og nedregulering af lageret uden brug af dokumenter.

Hvis du ofte bruger varekladden til at bogføre de samme eller lignende kladdelinjer, f.eks. i forbindelse med materialeforbrug, kan du bruge siden **Standardvarekladde** til at lette denne gentagne opgave. Du kan finde flere oplysninger i [Arbejde med standardkladder](ui-work-general-journals.md#work-with-standard-journals).

1. Vælg ![Lightbulb, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **Varekladder**, og vælg derefter det relaterede link.
2. Udfyld felterne efter behov. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
3. Vælg handlingen **Bogfør** for at bogføre forbruget.

### <a name="to-adjust-bin-quantities-in-advanced-warehouse-configurations"></a>Sådan reguleres placeringsantal i avancerede lageropsætninger

Hvis lokationen bruger styret læg-på-lager og pluk, skal du bruge siden **Lagerkladde** til at bogføre ikke-planlagte positive og negative ændringer i antal. F.eks. for varer, der er bogført som manglende, eller tab, der er opstået uventet.  

Lagerkladder giver dig større reguleringsniveauer, så du kan gøre mængderne mere nøjagtige. Lagerstedet ved, hvor mange varer der er på lager, og hvor de er gemt, men hver regulering bogføres ikke på varekladden. Kreditter eller debet foretages til den reelle placering med mængdereguleringen. En modpostering oprettes på en reguleringsplacering. Reguleringsplaceringen er en virtuel placering uden virkelige varer. Du angiver den virtuelle placering i tabellen **Lagerjust. placeringskode** på **Lokationskort**-sider.

1. Vælg ![Lightbulb, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **Lagerkladde**, og vælg derefter det relaterede link.  
2. Udfyld oplysningerne på sidehovedet.  
3. Udfyld feltet **Varenr.** på linjen.  
4. Angiv den placering, hvor du anbringer de ekstra varer, eller hvor der er manglende varer.  
5. I feltet **Antal**, hvis du har fundet ekstra varer, skal du angive en positiv mængde. Hvis der mangler varer, skal du angive en negativ mængde.  
6. Vælg handlingen **Registrer**.

## <a name="to-synchronize-the-adjusted-warehouse-entries-with-the-related-item-ledger-entries"></a>Sådan synkroniseres de regulerede lagerposter med de relaterede vareposter

Bogfør reguleringsplaceringsposterne i varekladden for de perioder, du har defineret. Nogle virksomheder bogfører dagligt reguleringer på varekladden, mens andre afstemmer mindre ofte.

1. Vælg ![Lightbulb, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **Varekladde**, og vælg derefter det relaterede link.  
2. Udfyld felterne på de enkelte kladdelinjer.  
3. Vælg **Beregn lagerregulerings**-handling, og Tilføj derefter filtre på **Beregn lagerregulerings**-siden. Justeringer beregnes kun for de poster på reguleringsplaceringen, der opfylder filterkriterierne.  
4. På oversigtspanelet **Indstillinger** skal du udfylde feltet **Bilagsnr.** med et tal, du indtaster manuelt. Da der ikke er defineret nogen nummerserie for kørslen, skal du bruge det nummereringssystem, der er sat op for lagerstedet. Du kan også indtaste dags dato efterfulgt af dine initialer.  
5. Vælg **OK**. De positive og negative justeringer lægges sammen for hver vare, og der oprettes linjer i varekladden.  
6. Bogfør kladdelinjerne for at tilføje afvigelserne i varekladden. Oversigterne på placeringer og vareposter passer nu.  

## <a name="see-also"></a>Se også

[Lageroptælling ved hjælp af dokumenter](inventory-how-count-inventory-with-documents.md)  
[Lagerbeholdning](inventory-manage-inventory.md)  
[Oversigt over Warehouse Management](design-details-warehouse-management.md)  
[Salg](sales-manage-sales.md)  
[Køb](purchasing-manage-purchasing.md)  
[Arbejd med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]
