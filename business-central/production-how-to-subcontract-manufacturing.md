---
title: Produktion hos underleverandør
description: Dette emne giver en udvidet oversigt over den udvidede funtionality af underleverandørarbejde i Business Central inkl. arbejdscenterfelter og -rute.
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 99000886
ms.date: 06/22/2021
ms.author: edupont
---
# Produktion hos underleverandør

Det er almindeligt for mange produktionsvirksomheder at placere udvalgte operationer hos underleverandører. Det er normal procedure i mange produktionsvirksomheder, selvom det hos nogle virksomheder måske kun sker engang imellem, mens det hos andre er en integreret del af produktionsprocessen.

[!INCLUDE[prod_short](includes/prod_short.md)] omfatter flere værktøjer til håndtering af arbejde, der udføres af underleverandører:  

- Arbejdscenter med tildelt leverandør: Denne funktion giver dig mulighed for at oprette et arbejdscenter, der har en leverandør (underleverandør) tilknyttet. Dette kaldes et arbejdscenter med underleverance. Du kan angive et arbejdscenter med underleverance til en ruteoperation, så du let kan behandle den aktivitet, der foregår hos underleverandøren. Desuden kan de omkostninger, der er forbundet med operationen, angives på rute- eller arbejdscenterniveau.  
- Arbejdscenteromkostninger baseret på enheder eller tid: Denne funktion giver dig mulighed for at angive, om de omkostninger, der er forbundet med arbejdscentret, er baseret på produktionstiden eller på en engangspris pr. enhed. Selvom underleverandører ofte bruger en engangspris pr. enhed som udgangspunkt, når de fakturerer deres arbejde, kan programmet håndtere begge indstillinger (produktionstid og engangspris pr. enhed).  
- Underleverandørkladde: Denne funktion giver dig mulighed for at finde produktionsordrer med materiale, der allerede er parat til afsendelse til en underleverandør og automatisk oprette købsordrer på operationer fra produktionsordreruter, der skal udføres hos en underleverandør. Programmet bogfører derefter automatisk de udgifter, der er forbundet med købsordren, på produktionsordren i forbindelse med bogføringen af købsordren. Det er kun produktionsordrer med frigivet som status, der kan åbnes og bruges fra en underleverandørkladde.  

## Arbejdscentre til underleverance  
Arbejdscentre til underleverance oprettes på samme måde som almindelige arbejdscentre – der kræves bare flere oplysninger. De knyttes til ruter på samme måde som andre arbejdscentre.  

### Felter for arbejdscenter til underleverance  
Dette felt med **underleverandør nr.** angiver arbejdscenter som underleverancearbejdscenter. Du kan angive nummeret på den underleverandør, der leverer til arbejdscentret. Feltet kan bruges til at administrere eksterne arbejdscentre, som udfører kontraktarbejde.  

Hvis du aftaler prisen med leverandøren for hver proces for sig, kan du markere afkrydsningsfeltet **Specifik kostpris**. Det giver dig mulighed for at oprette en kostpris for hver rutelinje, så du undgår at bruge tid på at angive hver eneste købsordre igen. Kostprisen på rutelinjen bruges i behandlingen i stedet for kostprisen i arbejdscentrets kostprisfelter. Hvis du markerer feltet **Specifik kostpris**, beregnes kostpriser for leverandøren for hver ruteoperation.  

Hvis du har aftalt én enkelt sats med hver leverandør, skal du ikke udfylde feltet **Specifik kostpris**. Kostpriserne oprettes i stedet, når du udfylder felterne **Købspris**, **Indir. omkost.pct.** og **IMO-bidrag**.  

### Ruter, der bruger arbejdscentre til underleverancer  
Arbejdscentre til underleverance kan bruges til operationer på ruter på samme måde som almindelige arbejdscentre.  

Du kan oprette en rute, der bruger et eksternt arbejdscenter som et standardoperationstrin. Du kan også redigere ruten for en bestemt produktionsordre, så den omfatter en ekstern operation. Dette kan være nødvendigt i en nødsituation, f.eks. en server, der ikke fungerer korrekt, eller en midlertidig periode med højere efterspørgsel, hvor det arbejde, der normalt udføres internt, skal sendes til en underleverandør.  

Du kan finde flere oplysninger i [Oprette ruter](production-how-to-create-routings.md).  

## Beregne underleverandørkladder og oprette købsordrer på underleverance  
Når du har beregnet underleverandørkladden, oprettes det relevante dokument, hvilket i dette tilfælde er en købsordre.  

Siden **Underleverandørkladde** fungerer ligesom **Planlægningskladde** ved at beregne de nødvendige forsyninger, i dette tilfælde indkøbsordrer, som du kan gennemgå i regnearket og derefter oprette med funktionen **Udfør aktionsmeddelelse**.  

> [!NOTE]  
>  Det er kun produktionsordrer med **Frigivet** som status, der kan åbnes og bruges fra en underleverandørkladde.  

### Sådan beregnes underleverandørkladden  
1.  Vælg ![Lightbulb, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **Underleverandørkladde**, og vælg derefter det relaterede link.  
2.  Hvis du vil beregne kladden, skal du vælge handlingen **Beregn underleverancer**.  
3.  Sæt filtre på underleverandøroperationer eller arbejdscentre, hvor de udføres, for kun at beregne de relevante produktionsordrer på siden **Beregn underleverancer**.  
4.  Vælg knappen **OK**.  

    Gennemgå linjerne på siden **Underleverandørkladde**. Oplysningerne i kladden hentes fra produktionsordren og produktionsordrens rutelinjer og overføres til købsordren, når det dokument oprettes. Du kan slette en række, uden at det påvirker de oprindelige oplysninger, som du kan med andre kladder. Oplysningerne vises igen, næste gang du kører funktionen **Beregn underleverancer**.  

### Sådan oprettes købsordre på underleverance  
1.  Vælg ![Lightbulb, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **Underleverandørkladde**, og vælg derefter det relaterede link.  
2.  Vælg handlingen **Udfør aktionsmeddelelse**.  
3.  Vælg feltet **Udskriv ordrer**, hvis du vil udskrive købsordren, når den oprettes.  
4.  Vælg knappen **OK**.  

Hvis alle underleveranceoperationer sendes til den samme leverandørlokation, oprettes der kun én købsordre.  

Den kladde, der nu udgør købsordren, slettes i kladden. Når en købsordre er oprettet, vises den ikke i regnearket igen.  

## Bogføre købsordrer på underleverancer  
Når der er oprettet en købsordre på en underleverance, kan den bogføres. Når ordren modtages, bogføres en kapacitetspost på produktionsordren, og ved fakturering af ordren bogføres de direkte omkostninger, der er forbundet med købsordren, på produktionsordren.  

## Sådan bogføres en købsordre på en underleverance  
1.  Vælg ![Lightbulb, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **købsordrer**, og vælg derefter det relaterede link.  
2.  Åbn den købsordre, der er oprettet på basis af underleverandørkladden.  

    På købsordrelinjerne kan du se de samme oplysninger som i regnearket. Felterne **Prod.ordrenr.**, **Prod.ordrelinjenr.**, **Operationsnr.** og **Arbejdscenternr.** udfyldes med oplysningerne fra kildeproduktionsordren.  

3.  Vælg handlingen **Bogfør**.  

Når købet er bogført som modtaget, bogføres en afgangskladdelinjepost automatisk for produktionsordren. Dette gælder kun, hvis underleverandøroperationen er den sidste operation på produktionsordreruten.  

> [!CAUTION]  
>  Der ønskes muligvis ikke automatisk bogføring af afgang for en igangværende produktionsordre, når der modtages varer fra underleverandører. Årsagerne til dette kan være, at det forventede afgangsantal, som bogføres, kan være forskelligt fra det faktiske antal, og at bogføringsdatoen for den automatiske afgang er vildledende.  
>   
>  Hvis du vil undgå, at en produktionsordres forventede afgang bogføres, når der modtages køb på underleverancer, skal du sørge for, at underleverandøroperationen ikke er den sidste. Du kan også indsætte en ny sidste operation for det endelige afgangsantal.  

Når købsordren er bogført som faktureret, bogføres den direkte omkostning for købsordren til produktionen.  

## Se også  
[Produktion](production-manage-manufacturing.md)    
[Konfigurere produktion](production-configure-production-processes.md)  
[Planlægning](production-planning.md)      
[Lagerbeholdning](inventory-manage-inventory.md)  
[Køb](purchasing-manage-purchasing.md)  
[Arbejd med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]