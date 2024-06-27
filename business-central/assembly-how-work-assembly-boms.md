---
title: Arbejde med montagestyklister
description: 'Du opretter en montagestykliste for at angive de komponenter, der kræves for at sammensætte den vare, som styklisten repræsenterer.'
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bholtorf
ms.topic: conceptual
ms.devlang: al
ms.search.keywords: 'assembly bom, bills of material,'
ms.search.form: '36, 5870, 5872, 5874'
ms.date: 06/13/2024
ms.service: dynamics-365-business-central
---
# Arbejde med montagestyklister

Du kan bruge montagestyklister til at strukturere overordnede varer, der skal samles ud fra komponenter med få eller ingen ressourcer. En montagestykliste kan f.eks. bruges til at sælge en overordnet vare som en pakke bestående af komponentvarer.

Brug montageordrer til at oprette slutvarer fra komponenter i en enkel proces, at en eller flere grundlæggende ressourcer, som produktions- eller arbejdscentre ikke kan udføre, eller uden nogen ressourcer. En montageproces kunne f.eks. være at plukke to vinflasker og én kaffesæk og pakke dem som en gave.  

En montagestykliste er masterdata, der definerer, hvilke komponentvarer der indgår i en monteret færdigvare, og hvilke ressourcer der bruges til at montere montageelementet. Når du angiver et montageelement og et antal på en montageordre, udfyldes montageordrelinjerne i overensstemmelse med montagestyklisten. Ordren indeholder én montageordrelinje pr. komponent eller ressource. Flere oplysninger i [Montagestyring](assembly-assemble-items.md).

[!INCLUDE[prod_short](includes/prod_short.md)] understøtter også produktionsstyklister. Produktionsstyklister adskiller sig fra montagestyklister, fordi de involverer mere komplekse procedurer, f.eks. ressourceforbrug, produktionsrute og arbejdscentre eller produktionsressourcer. Få mere at vide om forskellene i [Arbejde med tyklister](inventory-how-work-BOMs.md) og [Oprette produktionsstyklister](production-how-to-create-production-boms.md).

## Sådan oprettes en montagestykliste

For at definere en vare, der består af andre elementer og måske ressourcerne, der kræves for at montere varen, skal du oprette en montagestykliste.  

Montagestyklister kan have flere niveauer, hvilket betyder, at en komponent på montagestyklisten selv kan være et montageelement. I så fald skal feltet **Montagestykliste** på montagestyklistelinjen vise **Ja**.

Der gælder særlige krav for varerne på montagestyklister for så vidt angår tilgængelighed. Du kan finde flere oplysninger i [Sådan får du vist tilgængeligheden af en vare via brugen af den i montagestyklister](inventory-how-availability-overview.md#to-view-the-availability-of-an-item-by-its-use-in-assembly-or-production-boms).

Montagestyklister oprettes ad to omgange:

- Oprette en ny vare.
- Angive montageelementets styklistestruktur.

1. Opret en ny vare. Flere oplysninger i [Registrere nye emner](inventory-how-register-new-items.md).

   Fortsæt med at angive komponenter eller ressourcer på montagestyklisten.  
2. På siden **Varekort** for et montageelement skal du vælge handlingen **Montage** og derefter vælge handlingen **Montagestykliste**.
3. På siden **Montagestykliste** skal du udfylde felterne efter behov. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

> [!TIP]
> Montagevarer kan have forskellige varianter angivet ligesom alle andre varer, hvilket hjælper dig med at holde listen over produkter kortere. Få mere at vide om funktionen i [Administrer produktvarianter](inventory-item-variants.md).

## Sådan redigeres montagestyklister

Du kan til enhver tid redigere linjerne på en montagestykliste. Styklisten kan dog være i brug af løbende salg eller af modervirksomhedens samlinger. Hvis du ændrer styklisten, kan det påvirke disse aktiviteter. Vælg **Indgår-i** for at se de varer, den bruges i, og om salgs- eller montageordrer kan blive påvirket.

1. Vælg det ![lyspæreikon, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, angiv **Varer**, og vælg derefter det relaterede link.
2. Vælg værdien **Ja**  i kolonnen **Montagestykliste**.
3. Gå til siden **Montagestykliste**, vælg handlingen **Rediger liste**, og rediger derefter felter efter behov.

## Sådan får du vist komponenter og ressourcer indrykket i overensstemmelse med styklistestrukturen

Fra siden **Montagestykliste** kan du åbne en separat side, der viser komponenterne og evt. ressourcer, der er indrykket i henhold til deres placering på styklisten under montageelementet.

1. Vælg ![Lightbulb, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, angiv **Varer**, og vælg derefter det relaterede link.
2. Åbn kortet for et montageelement. (Feltet **Montagestykliste** på siden **Varer** indeholder **Ja**).
3. På siden **Varekort** skal du vælge handlingen **Montage** og derefter vælge handlingen **Montagestykliste**.
4. På siden **Montagestykliste** skal du vælge handlingen **Vis stykliste**.

## Sådan erstattes montageelementet med dets komponenter på dokumentlinjer

Du kan bruge en særlig handling til at erstatte linjen for montageelementet med nye linjer til dets komponenter fra et salgs- og købsdokument, som indeholder et montageelement. Denne handling er nyttig f.eks., hvis du vil sælge komponenterne som en pakke, der repræsenterer et montageelement.

Funktionen **Udfold stykliste** er også tilgængelig på siden **Montagestykliste** og kan bruges til at se halvfabrikata på en montagestykliste.

> [!CAUTION]  
> Når du har brugt handlingen **Udfold stykliste**, er det svært at annullere den igen. Du skal slette de salgsordrelinjer, for komponenterne og derefter indsætte en salgsordrelinje for montageelementet igen.

Følgende procedure er baseret på en salgsfaktura. Samme fremgangsmåde gælder for andre salgsdokumenter og alle købsdokumenter.

1. Vælg ![Lightbulb, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **Salgsfakturaer**, og vælg derefter det relaterede link.
2. Åbn en salgsfaktura, som indeholder en linje for et montageelement.
3. Vælg linjen for et montageelement og vælg derefter linjehandlingen **Udfold stykliste**.

Alle felter på salgsfakturalinjen for montageelementet fjernes med undtagelse af felterne **Vare** og **Beskrivelse**. Fuldførte salgsfakturalinjer indsættes for komponenterne og eventuelle ressourcer, der udgør montageelementet.

> [!NOTE]
> Rapporten **Plukliste efter ordre** ændres også til kun at vise komponenterne. Det betyder, at en lagermedarbejder, som plukker den overordnede vare (montageelementet), ikke kan se den på pluklisten. Få mere at vide i [Udskrive pluklisten](sales-how-print-picking-list.md).

## Sådan beregnes standardkostprisen et montageelement

Du kan beregne kostprisen for et montageelement ved at akkumulere kostprisen for hver komponent og ressource i elementets montagestykliste.

Du kan også beregne og opdatere standardkostprisen for en eller flere varer på siden **Standardkostpriskladde**. Få mere at vide i [Opdatere standardkostpriser](finance-how-to-update-standard-costs.md).  

En montagestyklistes kostpris svarer altid til den samlede kostpris for dens komponenter, herunder andre montagestyklister, og eventuelle ressourcer.  

> [!NOTE]
> [!INCLUDE [bom-standard-cost](includes/bom-standard-cost.md)]

1. Vælg ![Lightbulb, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, angiv **Varer**, og vælg derefter det relaterede link.
2. Åbn kortet for et montageelement. (Feltet **Montagestykliste** på siden **Varer** indeholder **Ja**).
3. På siden **Varekort** skal du vælge handlingen **Montagestykliste**.
4. På siden **Montagestykliste** skal du vælge handlingen **Beregn kostpris**.
5. Vælg en af følgende muligheder, og vælg derefter knappen **OK**.

|Indstilling |Beskrivelse |
|-------|------------|
|**Øverste niveau**|Beregner montageelementets standardkostpris som kostbeløbet for alle elementer, der er købt eller monteret på montagestyklisten uanset eventuelle underliggende montagestyklister.|
|**Alle niveauer**|Beregner montageelementets standardkostpris som summen af:</br></br>* Den beregnede kostpris for alle underliggende montagestyklister på montagestyklisten.</br>* Kostprisen for alle indkøbte varer på montagestyklisten.|

Omkostningerne ved de elementer, der udgør montagestyklisten, kopieres fra komponentvarekortene. Kostprisen på hver vare ganges med antallet, og den samlede kostpris vises i feltet **Kostpris** på varekortet.

## Se også

[Registrere nye varer](inventory-how-register-new-items.md)  
[Administrere produktvarianter](inventory-item-variants.md)  
[Vise varer, der er disponible](inventory-how-availability-overview.md)  
[Lagerbeholdning](inventory-manage-inventory.md)  
[Arbejde med styklister](inventory-how-work-BOMs.md)  
[Oprette produktionsstyklister](production-how-to-create-production-boms.md)  
[Arbejd med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
