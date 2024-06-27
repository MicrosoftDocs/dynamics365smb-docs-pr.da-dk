---
title: Oprette produktionsstyklister
description: 'Få mere at vide om, hvordan du opretter en produktionsstykliste, nye versioner af en produktionsstykliste, og hvordan mængde beregningsformlen bruges.'
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bholtorf
ms.topic: conceptual
ms.search.keywords: 'production bom, bills of material,'
ms.search.form: '911, 912, 917, 9287, 99000786, 99000787, 99000788, 99000789, 99000795, 99000797, 99000800, 99000809, 99000811, 99000812, 99000818'
ms.date: 05/29/2024
ms.service: dynamics-365-business-central
---
# Oprette produktionsstyklister

En produktionsstykliste indeholder masterdata, som beskriver de komponenter og halvfabrikata, som anvendes til fremstilling af en vare. Når du opretter en produktionsordre for en vare, bestemmer dens produktionsstykliste beregningen af materialebehov, som repræsenteret på siden **Prod.ordrekomponenter**.

[!INCLUDE[prod_short](includes/prod_short.md)] understøtter også montagestyklister. Brug montageordrer til at oprette slutvarer fra komponenter i en enkel proces, at en eller flere grundlæggende ressourcer, som produktions- eller arbejdscentre ikke kan udføre, eller uden nogen ressourcer. Eller en proces, der kan fuldføres uden ressourcer. En montageproces kunne f.eks. være at plukke to vinflasker og én kaffesæk og pakke dem som en gave. Du kan finde flere oplysninger i [Montagestykliste eller produktionsstyklister](inventory-how-work-boms.md#assembly-boms-or-production-boms).  

> [!TIP]
> Appen **Contoso Coffee-demodata** omfatter demonstrationsprodukter til en række forskellige produktionsstyklistescenarier, der kan bruges i et testmiljø, inklusive en prøveversion. Få mere at vide om, hvordan du konfigurerer Contoso Coffee-data og finder gennemgange i forskellige scenarier på [Introduktion til Contoso Coffee-demodata](contoso-coffee/contoso-coffee-intro.md).

Før du kan oprette en rute, skal følgende opsætninger være opfyldt:  

- Der er oprettet varekort for overordnede varer, der indgår i produktionen. Du kan finde flere oplysninger i [Registrere nye varer](inventory-how-register-new-items.md).
- Produktionsressourcer er oprettet. Du kan finde flere oplysninger i [Konfigurere arbejdscentre og produktionsressourcer](production-how-to-set-up-work-and-machine-centers.md).

## Sådan oprettes en produktionsstykliste

1. Vælg ![Lightbulb, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **Produktionsstykliste**, og vælg derefter det relaterede link.  
2. Vælg handlingen **Ny**.  
3. Udfyld felterne efter behov. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
4. Du kan redigere styklisten ved at angive feltet **Status** til **Ny** eller **Under udvikling**. Du kan aktivere den ved at angive feltet **Status** til **Certificeret**.  

    Udfyld linjerne i produktionsstyklisten.
5. Vælg, om varen på denne produktionsstyklistelinje er en almindelig vare eller en produktionsstykliste, i feltet **Type**. Hvis varen på linjen er en produktionsstykliste, skal den findes i forvejen som en godkendt produktionsstykliste.  
6. I feltet **Nummer** skal du søge efter og vælge den pågældende vare eller produktionsstykliste, eller du skal skrive den i feltet.  
7. Angiv, hvor mange enheder af varen, der indgår i den overordnede vare, f.eks. 4 hjul til 1 bil, i feltet **Antal pr**.  
8. Angiv en fast procentdel af komponenterne, der går til spilde under produktionen, i feltet **Spildpct**. Når komponenterne er klar til forbrug i en frigivet produktionsordre, lægges denne procentdel til det forventede antal i feltet **Forbrugsantal** i en produktionskladde. Du kan finde flere oplysninger i [Registrere forbrug og afgang](production-how-to-register-consumption-and-output.md).  

    > [!NOTE]  
    >  Denne spildprocent repræsenterer komponenter, der går til spilde under produktionen, når de tages fra lageret, mens spildprocenten på rutelinjer repræsenterer spild i output, før det lægges på lager.  

9. I feltet **Rutebindingskode** skal du skrive en kode for at knytte komponenten til en bestemt operation. Du kan finde flere oplysninger i [Sådan oprettes rutebindinger](production-how-to-create-routings.md#to-create-routing-links).
10. Du kan kopiere linjer fra en eksisterende produktionsstykliste ved at vælge handlingen **Kopier stykliste** for at vælge eksisterende linjer.  
11. Godkend produktionsstyklisten.  
12. Du kan nu knytte den nye produktionsstykliste til kortet for den pågældende overordnede vare. Du kan finde flere oplysninger i [Registrere nye varer](inventory-how-register-new-items.md).  

> [!NOTE]  
> [!INCLUDE [bom-standard-cost](includes/bom-standard-cost.md)] Hvis du vil genberegne varens standardkostpris fra varekortet, skal du vælge handlingen **Produktion** og derefter vælge handlingen **Beregn standardkostpris**.  

## Sådan oprettes en ny version af en produktionsstykliste

Brug f.eks. nye versioner af produktionsstyklister, når en vare erstattes, eller når en kunde bestiller en speciel version af et produkt. Versionsprincippet gør det muligt at administrere flere versioner af en produktionsstykliste. Ruteversionens struktur svarer til rutens struktur. Forskellen ligger i versionernes tidsmæssige gyldighed. Startdatoen bestemmes af gyldigheden.  

Startdatoen angiver starten på en periode, hvor versionen er gyldig. I alle andre sammenhænge er startdatoen et filterkriterium for beregninger og vurderinger. Styklisteversionen er gyldig, til næste version bliver gyldig efter sin startdato.  

1. Vælg ![Lightbulb, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **Produktionsstykliste**, og vælg derefter det relaterede link.  
2. Vælg produktionsstyklisten, der skal kopieres, og vælg derefter handlingen **Versioner**.  
3. Vælg handlingen **Ny**.  
4. Udfyld felterne efter behov. [!INCLUDE [tooltip-inline-tip_md](includes/tooltip-inline-tip_md.md)]
5. I feltet **Versionskode** skal du angive en entydig identifikation af versionen. Alle kombinationer af tal og bogstaver er tilladt.  

    Den nyoprettede version tildeles automatisk status som **Ny**.
6. Når styklisteversionen er udført, angiver du feltet **Status** til **Certificeret**.  

Gyldigheden i tid for versionen angives i feltet **Startdato**.  

> [!NOTE]  
> Hvis du vil bruge en vare fra varemasterdata i produktionsstyklisten skal du vælge indstillingen **Vare** i feltet **Type**. Hvis varen også har en produktionsstykliste, hvorved **Produktionsstyklistenr.** er udfyldt på kortet, tages denne produktionsstykliste også i betragtning.  
>
> Vælg indstillingen **Produktionsstykliste**, hvis du vil bruge en fantomproduktionsstykliste på linjen.  
>
> Fantomstyklister anvendes til at strukturere produkter. Denne produktionsstyklistetype fører aldrig til et færdigt produkt, men anvendes udelukkende til at bestemme afhængige behov. Fantomstyklister har ikke deres egne stamdata for varer.

## Beregningsformel for mængde på produktionsstyklister

Mængden beregnes under hensyntagen til forskellige dimensioner, der også er angivet på produktionsstyklistens linjer. Dimensionerne henviser til en ordreenhed for den pågældende vare. Længde, bredde, dybde og vægt kan angives som dimensioner.  

Kolonnerne Beregningsformel, Længde, Bredde, Dybde og Vægt vises ikke, fordi de kun anvendes af nogle brugere. Hvis du vil anvende beregninger af mængden, skal du først have vist disse kolonner.  

Beregningsformlen definere relationen af de enkelte komponenter. Du kan vælge mellem følgende beregningsformler:  

- **Tom** - Der anvendes ikke dimensioner. (Antal = Antal pr.)  
- **Længde.** - Antal = Antal pr. * længde  
- **Længde x bredde** - Antal = Antal pr. * længde x bredde  
- **Længde x bredde x dybde** - Antal = Antal pr. x længde x bredde x dybde  
- **Vægt** - Antal = Antal pr. x vægt  
- **Fast antal** - antal = antal pr.

> [!NOTE]
> Formlen til beregning af **fast mængde** sikrer, at en komponents forbrug er den samme, uanset spild-eller afgangsantal. For produktionsordrekomponenter er værdien af feltet **Forventet antal** altid lig med feltet **Antal pr.**, når feltet **Beregningsformel** er indstillet til **Fast antal**. Den spildprocent, der er defineret på samme linje, ignoreres. Fast antal respekteres af rapporten **Disponering pr. stykliste**. Rapporten viser varen som flaskehals, hvis det disponible antal er mindre end antallet i feltet **Antal pr. overordnet**. Felterne **Muligheder for at gøre overordnet** og **kunne gøre de øverste vare** er altid tomme uanset det disponible antal. Fast antal indgår også i beregninger af standardkostpriser. Lotstørrelsen for den producerede vare påvirker den omkostning, der er tildelt én vare.

### Eksempel

En produktionsstykliste kræver 70 metaldele med dimensionernes længde = 0,20 m og bredde = 0,15 m. Angiv værdierne sådan: Beregningsformel = Længde x bredde, længde = 20, bredde = 15, Antal pr. = 70.

Antal pr. x længde * bredde, det vil sige, antal = 70 x 0,20 m x 0,15 m = 2,1 m2 angiver antallet.  

## Se også

[Oprette ruter](production-how-to-create-routings.md)  
[Administrere produktvarianter](inventory-item-variants.md)  
[Gennemgang: Varianter](contoso-coffee/manufacturing/variants.md)  
[Konfigurere produktion](production-configure-production-processes.md)  
[Produktion](production-manage-manufacturing.md)  
[Skabelon](production-planning.md)  
[Arbejde med styklister](inventory-how-work-BOMs.md)  
[Arbejde med montagestyklister](assembly-how-work-assembly-boms.md)  
[Lagerbeholdning](inventory-manage-inventory.md)  
[Køb](purchasing-manage-purchasing.md)  
[Arbejd med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
