---
title: Udtrække komponenter i henhold til operationsafgang
description: 'Dette emne beskriver, hvordan du tømmer komponenter i henhold til operationsafgang samt andre trækmetoder.'
author: brentholtorf
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: null
ms.date: 06/22/2021
ms.author: bholtorf
---
# <a name="flush-components-according-to-operation-output"></a>Udtrække komponenter i henhold til operationsafgang
Du kan definere forskellige trækstrategier for at automatisere registrering af forbruget af komponenter. 

Denne funktion er nyttig, af følgende årsager:  

- **Lagerværdi**

    Værdiposterne for afgang og forbrug oprettes parallelt, efterhånden som produktionsordren behandles. Uden rutebindingskoder vil lagerværdien forøges efterhånden som afgangen bogføres, og derefter formindsk på et senere tidspunkt, når værdien af komponentforbruget bogføres sammen med den færdige produktionsordre.  
- **Varedisponering**

    Med gradvis bogføring af forbrug, vil tilgængeligheden af komponentvarer være mere opdateret, hvilket er vigtigt for at opretholde den interne balance mellem efterspørgsel og udbud. Uden rutebindingskoder vil andre efterspørgsler efter komponenten mene, at den er tilgængelig, så længe der ventes på et forsinket bogføring af forbruget.  
- **JIT (Just-in-Time)**

    Med muligheden for at tilpasse produkter til debitorernes behov, kan du minimere spild ved at sikre, at arbejds- og systemændringer kun forekommer, når de er nødvendige.  

- **Reducere dataindtastning**

    Når det er muligt at trække en operation automatisk, kan hele processen til registrering af forbrug og afgang automatiseres. Ulempen ved at bruge automatisk træk er, at du muligvis ikke kan registrere spild, eller måske ikke engang er opmærksom på spild.

## <a name="automatic-consumption-posting-flushing-methods"></a>Automatisk bogføring af forbrugsmetode (træk)

- Forlæns træk af hele ordren  
- Forlæns træk for én operation ad gangen  
- Baglæns træk for én operation ad gangen  
- Baglæns træk af hele ordren  

### <a name="automatic-reporting---forward-flush-the-entire-order"></a>Automatisk rapportering – forlæns træk af hele ordren
Hvis du bruger forlæns træk til produktionsordren ved sagens start, opfører programmet sig stort set på samme måde som ved manuelt forbrug. Den væsentligste forskel er, at forbruget sker automatisk.  

- Alt indhold på produktionsstyklisten forbruges og trækkes fra lagerbeholdningen på det tidspunkt, hvor den frigivne produktionsordre fornys.  
- Forbrugsantallet er det antal pr. samling, der er angivet på produktionsstyklisten, ganget med det antal samlede eller overordnede varer, der skal produceres.  
- Det er ikke nødvendigt at registrere oplysninger i forbrugskladden, hvis alle varerne skal trækkes.  
- Når der forbruges varer fra lagerbeholdningen, spiller det ingen rolle, hvornår oplysningerne registreres i afgangskladden, fordi afgangskladden ikke har nogen indflydelse på denne form for forbrugsbogføring.  
- Der kan ikke angives rutebindingskoder.  

Forlæns træk af en hel ordre er velegnet i produktionsmiljøer med:  

-   Få defekter  
-   Få operationer  
-   Højt komponentforbrug i tidligere operationer  

### <a name="automatic-reporting---forward-flushing-by-operation"></a>Automatisk rapportering – forlæns træk for én operation ad gangen
Hvis du vælger træk for én operation ad gangen, kan du fratrække lagervarer, mens en bestemt operation udføres på den samlede vares rute. Materialet er knyttet til ruten vha. rutebindingskoder, som svarer til de rutebindingskoder, der bruges til komponenter i produktionsstyklisten.  

Trækket finder sted, når den operation, der har den samme rutebindingskode, starter. At den starter betyder, at der registreres en aktivitet i afgangskladden for den pågældende operation. Aktiviteten behøver ikke være andet end, at der angives en opstillingstid.  

Trækmængden er det antal pr. samling, der er angivet i produktionsstyklisten ganget med det antal samlede varer, der skal produceres (forventet antal).  

Denne teknik egner sig bedst til forhold, hvor der er mange operationer, og hvor visse komponenter først skal bruges sent i samlingsforløbet. I en produktionsmiljø med JIT-produktion (Just-in-Time) er det ikke engang sikkert, at varerne er på lager, når den frigivne produktionsordre sættes i gang.  

Materialet kan forbruges under operationerne vha. rutebindingskoder. Nogle komponenter skal måske først bruges på de sidste produktionsstadier og skal derfor ikke trækkes fra lageret før det tidspunkt, hvor de skal bruges i operationerne.  

### <a name="automatic-reporting---back-flushing-by-operation"></a>Automatisk rapportering – baglæns træk for én operation ad gangen
Hvis du bruger baglæns træk for én operation ad gangen, registreres forbruget, efter at operationen er bogført i afgangskladden.  

Fordelen ved denne metode er, at antallet af færdige samlede varer i denne operation er kendt.  

Materialet i produktionsstyklisten knyttes sammen med ruteposterne vha. rutebindingskoder. Det baglæns træk sker, når en operation med en bestemt rutebindingskode bogføres med et færdigt antal.  

Trækmængden er det antal pr. samling, der er angivet i produktionsstyklisten, ganget med det antal samlede varer, der er bogført som afgangsantal på den pågældende operation. Det kan være anderledes end det forventede antal.  

### <a name="automatic-reporting---back-flushing-the-entire-order"></a>Automatisk rapportering – baglæns træk af hele ordren
I denne rapporteringsmetode tages der ikke højde for rutebindingskoder.  

Der plukkes ingen komponenter, før den frigivne ordres status ændres til *Færdig*. Trækmængden er det antal pr. samling, der er angivet på produktionsstyklisten, ganget med det antal samlede varer, der er færdige og overført til lageret.  

Baglæns træk af hele produktionsordren forudsætter samme opsætning som til fremadtræk: Rapporteringsmetoden skal være angivet til baglæns på hvert enkelt varekort for alle varer inden for den overordnede stykliste, der skal rapporteres. Desuden skal alle rutebindingskoder fjernes fra produktionsstyklisten. 



Hvis f.eks. en produktionsordre om at fremstille 800 meter kræver 8 kg af en komponent, bogføres derefter, når du bogfører 200 meter som afgang, 2 kg automatisk som forbrug. Du kan opnå dette ved at kombinere baglæns trækmetode og rutebindingskoder, så den mængde, der udtrækkes for hver operation er proportional med den faktiske afgang af den afsluttede operation. For varer, der er konfigureret med baglæns trækmetode, er standardfunktionsmåden at beregne og bogføre komponentforbrug, når du ændrer status på en frigivet produktionsordre til **Afsluttet**. Hvis du også definerer rutebindingskoder, forekommer beregning og bogføring, når hver operation er afsluttet, og den mængde, der rent faktisk er forbrugt i handlingen, der er bogført. Du kan finde flere oplysninger i [Oprette ruter](production-how-to-create-routings.md).  

## <a name="to-flush-components-according-to-operation-output"></a>Udtrække komponenter i henhold til operationsafgang

1.  Vælg ![Lightbulb, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **Varer**, og vælg derefter det relaterede link.  
2.  Vælg handlingen **Rediger**.  
3.  Vælg **Baglæns** i feltet **Trækmetode** i oversigtspanelet **Genbestilling**.  

    > [!NOTE]  
    >  Vælg **Pluk + Baglæns**, hvis komponenten bruges på en lokation, der er sat op til styret læg-på-lager og pluk.  

4.  Vælg ![Lightbulb, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **Rute**, og vælg derefter det relaterede link.  
5.  Definer rutebindingskoder for hver operation, der bruger komponenten. Du kan finde flere oplysninger i [Oprette ruter](production-how-to-create-routings.md).  
    > [!IMPORTANT]  
    > Brug ikke samme link til rutebinding for forskellige operationer i ruten, da det vil medføre registrering af komponentforbrug for hver tilknyttet operation.  
6.  Vælg ![Lightbulb, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **Produktionsstykliste**, og vælg derefter det relaterede link.  
7.  Definer rutebindingskoder fra hver forekomst af komponenten til den operation, hvor den forbruges.

Forbruget bogføres automatisk, når du registrerer afgang. Du kan finde flere oplysninger i [Massebogføre afgang og operationstider](production-how-to-post-output-quantity.md)

## <a name="flushing-methods"></a>Trækmetoder

I følgende tabel beskrives de tilgængelige indstillinger for trækmetode, som du kan angive på kort af typerne **Vare** og **Lagervare (pr. lok.)**.

|Indstilling|Beskrivelse|
|------------|-------------|  
|Manuelt|Kræver, at du manuelt indtaster og bogfører forbruget i forbrugskladden.|
|Forlæns|Bogfører automatisk forbruget i henhold til produktionsordrens komponentlinjer. <br><br>Som standard forekommer bogføring af komponentforbrug, når du ændrer status for en produktionsordre til **Frigivet**. Men hvis du bruger feltet **Rutebindingskode** på produktionsordrens komponentlinjer, udføres bogføring pr. operation, når operationen startes. Du kan finde flere oplysninger i [Sådan gør du: Oprette rutebindinger](production-how-to-create-routings.md#to-create-routing-links). <br><br> **Bemærk**<br>Ved forlæns træk er den operationsspecifikke bogføring, som du opnår med rutebindingskoder, baseret på det forventede antal, der er defineret på komponentlinjen. Du kan finde oplysninger om operationsspecifikt træk baseret på faktisk afgang i beskrivelsen af **Baglæns** i dette emne.<br><br>Hvis den lokation eller de ressourcer, hvor komponenten forbruges, er konfigureret med en standardplaceringsstruktur, forbruges varen fra **Åben prod.placeringskode**. Du kan finde flere oplysninger i [Sådan gør du: Oprette grundlæggende lagersteder med handlingsområder](warehouse-how-to-set-up-basic-warehouses-with-operations-areas.md). <br><br> **Vigtigt** <br>Forlæns træk udføres også, når du vælger **Opdater** på en frigivet produktionsordre , der er oprettet fra bunden. På disse frigivne produktionsordrer, der er oprettet direkte, kan du ikke ændre placeringsoplysninger, fordi produktionsordrens komponentlinjer genereres, når du opdaterer ordren, som samtidigt udfører forlæns træk af komponenterne. Hvis du vil ændre placeringsoplysningerne på produktionsordrens komponentlinjer, inden forlæns træk udføres, skal ordren oprettes med statussen *Planlagt* eller *Fastlagt*.|
|Baglæns|Beregner og bogfører forbrug automatisk i henhold til produktionsordrens komponentlinjer.<br><br> Som standard udføres beregning og bogføring af komponentforbrug, når du ændrer status på en frigivet produktionsordre til **Udført**. Hvis du bruger feltet **Rutebindingskode** på produktionsordrens komponentlinjer, udføres beregning og bogføring derimod, når hver operation er afsluttet.<br><br> **Bemærk** <br>Baglæns træk og rutebindingskoder kan kombineres, så den mængde, der trækkes pr. operation er proportional med den faktiske afgang for den pågældende operation. Du kan finde flere oplysninger i [Sådan gør du: Udtrække komponenter i henhold til operationsafgang](#to-flush-components-according-to-operation-output).<br><br> Hvis den lokation eller produktionsressource, hvor komponenten forbruges, er konfigureret med en standardplaceringsstruktur, forbruges varen fra **Åben prod.placeringskode**.|
|Pluk + Forlæns|Samme som for forlæns trækmetode, undtagen den kan kun bruges til lokationer, der bruger avanceret Lageropsætning eller grundlæggende Lageropsætning med obligatoriske placeringer.<br><br> Forbruget beregnes og bogføres fra den placering, der er defineret i feltet **Til-produktionsplaceringskode** på lokationen eller produktionsressourcen, når komponenten er blevet plukket fra lageret.<br><br> **Bemærk** <br>Hvis en komponent er indstillet til trækmetoden Pluk + Forlæns, kan den ikke have en rutebindingskode til en operation, der er konfigureret med trækmetoden Forlæns. Komponenten vil derefter automatisk blive udtrukket, når operationen starter, hvilket gør det umuligt at anmode om plukaktiviteten.|
|Pluk + Baglæns|Samme som for baglæns trækmetode, undtagen den kan kun bruges til lokationer, der bruger avanceret Lageropsætning eller grundlæggende Lageropsætning med obligatoriske placeringer.<br><br> Forbruget beregnes og bogføres fra den placering, der er defineret i feltet **Til-produktionsplaceringskode** på lokationen eller produktionsressourcen, når komponenten er blevet plukket fra lageret.|

## <a name="see-also"></a>Se også

[Oprette produktionsstyklister](production-how-to-create-production-boms.md)  
[Konfigurere produktion](production-configure-production-processes.md)  
[Produktion](production-manage-manufacturing.md)  
[Skabelon](production-planning.md)  
[Lagerbeholdning](inventory-manage-inventory.md)  
[Køb](purchasing-manage-purchasing.md)  
[Arbejd med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
