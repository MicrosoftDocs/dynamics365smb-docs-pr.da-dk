---
title: Designoplysninger – Bogføring af produktionsordre | Microsoft Docs
description: 'I lighed med montageordrebogføring bliver de forbrugte komponenter og den anvendte computertid konverteret og udlæst som den producerede vare, når produktionsordren er afsluttet.'
author: brentholtorf
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: null
ms.date: 06/08/2021
ms.author: bholtorf
---
# Designoplysninger: Bogføring af produktionsordre
I lighed med montageordrebogføring bliver de forbrugte komponenter og den anvendte computertid konverteret og udlæst som den producerede vare, når produktionsordren er afsluttet. Du kan finde flere oplysninger i [Designoplysninger: Bogføring af montageordre](design-details-assembly-order-posting.md). Men montageordrers kost-flow er mindre kompliceret, især fordi montageomkostninger kun bogføres én gang og derfor ikke opretter lageret for igangværende arbejde.


Transaktioner, der forekommer under produktionsprocessen, kan spores via følgende faser:  

1.  Indkøb af materialer og andre tilgange til produktion.  
2.  Konvertering til igangværende arbejde.  
3.  Konvertering til færdigvarelager.  
4.  Salg af færdigvarer  

Udover almindelige lagerkonti skal en produktionsvirksomhed derfor oprette tre separate lagerkontoer for at registrere transaktioner på forskellige stadier af produktionen.  

|Lagerkonto|Beskrivelse|  
|-----------------------|---------------------------------------|  
|**Konto for råmaterialer**|Omfatter køb af råvarer, der er købt, men som endnu ikke er overført til produktion. Saldoen på kontoen for råvarer angiver omkostningerne ved råvarer på lager.<br /><br /> Når råvarer flyttes til produktionsafdelingen, overføres kostprisen for materialerne fra kontoen Råvarer til IVA-kontoen.|  
|**VIA-konto (VIA)**|Akkumulerer de omkostninger, der er påløbet i produktionsprocessen i regnskabsperioden. VIA-kontoen debiteres for omkostningerne i forbindelse med råmaterialer, der overføres fra lagerstedet for råvarer, omkostningerne ved direkte udført arbejde og de faste produktionsomkostninger, der er påløbet.<br /><br /> VIA-kontoen krediteres de samlede produktionsomkostninger for enheder, der er udført på fabrikken og overført til lageret for færdigvarer.|  
|**Konto for færdigvarer**|Denne konto indeholder de samlede produktionsomkostninger for enheder, der er fuldført, men som endnu ikke er solgt. På salgstidspunktet overføres kostprisen for solgte enheder fra kontoen for færdigvarer til kontoen for solgte varer.|  

Lagerværdien beregnes ved at spore omkostninger for alle forøgelser og reduceringer, som udtrykt i følgende ligning:  

* lagerværdi = startsaldo for lager + værdi af alle forøgelser - værdi af alle reduceringer  

Afhængigt af typen af lager repræsenteres forøgelser og reduceringer af forskellige posteringer.  

||Forøgelse|Reducering|  
|-|---------------|---------------|  
|**Lager af råmaterialer**|-   Nettokøb af materiale<br />-   Output af halvfabrikata<br />-   Negativt forbrug|Materialeforbrug|  
|**VIA-lagerbeholdning**|-   Materialeforbrug<br />-   Forbrugskapacitet<br />-   Indirekte prod.kostpris|Afgang af færdigvarer (omkostninger af fremstillede varer)|  
|**Færdigvarelager**|Afgang af færdigvarer (omkostninger af fremstillede varer)|-   Salg (vareforbrug)<br />-   Negativt output|  
|**Lager af råmaterialer**|-   Nettokøb af materiale<br />-   Output af halvfabrikata<br />-   Negativt forbrug|Materialeforbrug|  

Værdierne for forøgelser og reduceringer registreres i de forskellige typer af produceret lager på samme måde som for købt lager. Hver gang en lagerforøgelses- eller lagerreduceringstransaktion finder sted, oprettes der en varepost og en tilsvarende finanspost for beløbet. Du kan finde flere oplysninger i [Designoplysninger: Varekladde](design-details-inventory-posting.md).  

Selvom værdier af transaktioner, der vedrører købte varer, kun bogføres som vareposter med relaterede værdiposter, bogføres transaktioner, der er knyttet til producerede varer, som kapacitetsposter med relaterede værdiposter, udover vareposterne.  

## Bogføringsstruktur  
Bogføring af produktionsordrer til igangværende arbejdslager omfatter afgang, forbrug og kapacitet.  

Følgende diagram viser de involverede bogføringsrutiner i kodeenhed 22.  

![Posteringsrutiner for produktionsordrer.](media/design_details_inventory_costing_14_production_posting_1.png "Posteringsrutiner for produktionsordrer")  

I følgende diagram vises tilknytninger mellem de oprettede poster og omkostningsemnerne.  

![Produktionspostflow.](media/design_details_inventory_costing_14_production_posting_2.png "Produktionspostflow")  

Kapacitetsposten beskriver kapacitetsforbrug i tidsenheder, hvorimod den tilknyttede værdipost beskriver værdien af det specifikke kapacitetsforbrug.  

Vareposten beskriver materialeforbrug eller afgang med hensyn til mængder, mens den tilknyttede værdipost beskriver værdien af dette specifikke materialeforbrug eller afgangen.  

En værdipost, der beskriver det igangværendes arbejdes værdi, kan være knyttet til en af følgende kombinationer af omkostningsemner:  

-   En produktionsordrelinje, et arbejdscenter eller en produktionsressource og en kapacitetspost.  
-   En produktionsordrelinje, en vare og en varepost.  
-   Kun en produktionsordrelinje  

Du kan finde flere oplysninger om, hvordan omkostninger fra produktion og montage bogføres i finansregnskabet, i [Designoplysninger: Varekladde](design-details-inventory-posting.md).  

## Bogføring af kapacitet  
Bogføring af afgang fra den sidste produktionsordrerutelinje resulterer i en kapacitetsfinanspost for færdigvaren, i tillæg til dens lagerforøgelse.  

 Kapacitetsposten er en post over den tid, der er brugt til at producere varen. Den relaterede værdipost beskrives i VIA-lagerværdien, som er værdien af konverteringsomkostningerne. Du kan finde flere oplysninger i "Fra kapacitetsposten" i [Designoplysninger: Konti i Finans](design-details-accounts-in-the-general-ledger.md).  

## Produktionsordrekostmetode  
 Med henblik på at kontrollere lager- og produktionsomkostninger skal en produktionsvirksomhed måle omkostningerne for produktionsordrer, da de standardomkostninger, der er fastsat på forhånd for hver produceret vare, kapitaliseres i balancen. Hvis du ønsker oplysninger om, hvorfor producerede varer bruger kostmetoden Standard, kan du se [Designoplysninger: Kostmetoder](design-details-costing-methods.md).  

> [!NOTE]  
>  I miljøer, der ikke bruger kostmetoden Standard, aktiveres den faktiske værdi i stedet for standardkostprisen for fremstillede varer på balancen.  

De faktiske omkostninger for en produktionsordre består af følgende omkostningskomponenter:  

-   Faktisk materialekostpris  
-   Faktiske kapacitetsomkostninger eller omkostninger til underleverandør  
-   Indirekte prod.kostpris  

Disse faktiske omkostninger bogføres til produktionsordren og sammenlignes med standardkostprisen for at beregne afvigelser. Afvigelser beregnes for hver af varekomponentomkostningerne: råvarer, kapacitet, underleverandør-, kapacitets- og produktionsomkostninger. Afvigelserne kan analyseres for at afgøre, om der er problemer, som f.eks. overdrevent tab i behandlingen.  

I miljøer med standardkostpriser er omkostninger for en produktionsordre baseret på følgende metode:  

1.  Når den sidste ruteoperation bogføres, bogføres kostprisen for produktionsordren til vareposten og indstilles til de forventede omkostninger.  

    Disse omkostninger er lig med det afgangsantal, der er bogført i afgangskladden ganget med de standardomkostninger, der er kopieret fra varekortet. Omkostninger behandles som forventet kostpris, indtil produktionsordren er afsluttet. Du kan finde flere oplysninger i [Designoplysninger: Bogføring af forventet kostpris](design-details-expected-cost-posting.md).  

    > [!NOTE]  
    >  Dette adskiller sig fra montageordrebogføring, hvor der altid bogføres faktiske omkostninger. Du kan finde flere oplysninger i [Designoplysninger: Bogføring af montageordre](design-details-assembly-order-posting.md).  
2.  Når produktionsordren er indstillet til **Færdig**, faktureres ordren ved at udføre kørslen **Juster kostpris - vareposter**. Som resultat beregnes de samlede omkostninger for ordren baseret på standardkostprisen for de anvendte materialer og kapacitet. Afvigelserne mellem de beregnede standardkostpriser og de faktiske produktionskostpriser beregnes og bogføres.  

## Se også  
 [Designoplysninger: Lagerkostmetode](design-details-inventory-costing.md)   
 [Designoplysninger: Bogføring af montageordre](design-details-assembly-order-posting.md)  
 [Administrere lageromkostninger](finance-manage-inventory-costs.md) [Finans](finance.md)  
 [Arbejde med Business Central](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]