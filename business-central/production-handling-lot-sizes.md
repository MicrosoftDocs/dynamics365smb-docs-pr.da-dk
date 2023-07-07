---
title: Håndtering af lotstørrelse
description: I dette emne beskrives forskellige måder at håndtere lotstørrelser på.
author: brentholtorf
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.form: null
ms.date: 04/01/2021
ms.author: bholtorf
---

# <a name="handling-lot-sizes-in-production"></a>Håndtering af lotstørrelser i produktionen
Med hensyn til antal korrelerer antallet af varer, du producerer i en produktionsoperation, muligvis ikke til, hvordan de sælges. Du producerer måske hundredvis af varer i et enkelt parti, men sælger hver vare individuelt. Når du konfigurerer dine produktionsruter og styklister, er der få nuancer, du bør overveje med hensyn til lotstørrelser. I dette emne beskrives, hvordan lotstørrelser påvirker omkostningsberegninger og ressourceplanlægning.

## <a name="units-of-measure-in-production-bill-of-materials"></a>Måleenheder i produktionsstyklister
Selvom du angiver basisenheden (UOM) for en vare, kan styklisten bruge en anden UOM til det færdige produkt. Basis-UOM for en vare kan f.eks. være PCS, mens styklisten registrerer en palle eller et ton. Dette er praktisk, når dine maskiner eller rå komponenter dikterer lydstyrken. Du vil for eksempel sandsynligvis ikke bage en enkelt muffin, fordi det er svært at bruge en del af et æg. I stedet bager du et parti muffins for at reducere spild. Du kan finde flere oplysninger i [Oprette produktionsstyklister](production-how-to-create-production-boms.md).

## <a name="lot-size-on-routing-lines"></a>Lotstørrelse på rutelinjer
Fra et ruteperspektiv kan du angive en lotstørrelse på rutelinjer for at justere med kapaciteten for de maskiner, der producerer varerne. Kørselstiden på rutelinjer reduceres proportionalt med lotstørrelsen. 

Dette fungerer godt, når antallet på en produktionsordre er en faktor for partiets størrelse på ruten. For eksempel, hvis din bageplade kan rumme 10 muffins, bør du bage 10, 20, 30, og så videre, og ikke 5 eller 15.  Dette er langt mindre af et problem, hvis du har at gøre med store mængder.

Lotstørrelse er også populær i produktionsmiljøer, hvor output måles som antal, du kan foretage i løbet af den faste tid. Hvis rumfanget pr. 9 timers skift er 25000 kubikfod, kan du indstille køretiden til 9 timer og lotstørrelse som 25000.
Produktionsordreantallet bliver mindre vigtigt, da driftstiden på produktionsordren beregnes som driftstid-/lotstørrelsen for at få driftstiden pr. styk.
 
> [!NOTE]
> Den værdi, der er defineret i Lotstørrelse, har ikke indflydelse på den tid, der er angivet i feltet **Opstillingstid** på rutelinjen. Opsætningen vil kun ske én gang, selvom der er flere partier. For eksempel, så du ikke behøver at varme ovnen til den anden masse muffins. Du kan finde flere oplysninger i [Oprette ruter](production-how-to-create-routings.md).

## <a name="lot-sizes-for-items-and-stockkeeping-units"></a>Lotstørrelser for varer og lagervarer
Lotstørrelser, der er defineret for ruter, er ikke de samme som lotstørrelser for varer eller lagervarer. Disse værdier bruges til et andet formål og påvirker ikke produktionskapaciteten. 

## <a name="lot-size-on-item-and-stockkeeping-units"></a>Lotstørrelser for varer og lagervarerenheder
For varer og lagervarer har lotstørrelser følgende indvirkning på omkostningsberegning og forsyningsplanlægning:

* Hvis du aktiverer **Omkostningsbaseret installation** på siden **Produktionsopsætning** til standardpris, føjes omkostningerne for opsætningen til standardkostprisen. Hvis du angiver en lotstørrelse, reduceres opsætningsomkostningerne for rutedrift i henhold til én lotstørrelse. For eksempel, hvis din partistørrelse defineret på varekort er 10, og det tager 15 minutter at opvarme ovnen, vil udgifterne til brændstoffet blive afsat til de 10 muffins som omkring 1,5 minutter. 

> [!NOTE]
> Opsætningsomkostninger håndteres forskelligt fra standardomkostnings- og kapacitetsfordelingsperspektiver. Hvis produceret antal ikke svarer til den lotstørrelse, der er defineret på varekortet, vil det føre til variation. Der er flere oplysninger i [Administration af lageromkostninger](finance-manage-inventory-costs.md). <!--not sure that I got this part right seems to repeat the first example.-->

I forbindelse med forsyningsplanlægning fungerer lotstørrelsesindstillingen for varer med **Standardbuffer %** på siden **Produktionsopsætning**. [!INCLUDE[prod_short](includes/prod_short.md)] ignorerer ændringer i behovet, der ligger under aktionsgrænseprocenten, og opretter ikke planlægningsforslag. For eksempel er 15 angivet i feltet Standardgrænseprocent, og vi har en produktionsordre på 20 muffins til at brødføde 20 gæster, men en gæst kan ikke deltage. [!INCLUDE[prod_short](includes/prod_short.md)] ignorerer den enkelte manglende gæst, fordi den kun er 10 % af lotstørrelsen 10, der er defineret på varen. Men hvis to gæster ikke kommer, vil [!INCLUDE[prod_short](includes/prod_short.md)] foreslå, at vi reducere ordremængden, fordi to er 20 % af partiets størrelse. Du kan finde flere oplysninger i planlægning i [Planlægning](production-planning.md).

## <a name="see-also"></a>Se også
[Oprette produktionsstyklister](production-how-to-create-production-boms.md)  
[Arbejde med produktionskladdeenheder](production-how-to-use-the-manufacturing-batch-unit-of-measure.md)
[Oprette ruter](production-how-to-create-routings.md)  
[Administrere lageromkostninger](finance-manage-inventory-costs.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]
