---
title: Afstemme lagerværdier med finansregnskabet
description: 'Ved afslutningen af regnskabsperioder skal der udføres en række handlinger til omkostningsstyring og revision, så der rapporteres en korrekt og afstemt lagerværdi.'
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 'warehouse, stock'
ms.search.form: 9297
ms.date: 06/16/2021
ms.author: edupont
---
# <a name="reconcile-inventory-costs-with-the-general-ledger" />Afstemme lagerværdier med finansregnskabet

Når du bogfører lagertransaktioner, f.eks. salgsleverancer, købsfakturaer eller lagerreguleringer, registreres ændringen i varepriser i værdiposterne. For at afspejle ændringen af lagerværdien i dine finansielle regnskaber bogføres lagerværdien automatisk i de relaterede lagerkonti i finansbogholderiet. For hver lagertransaktion du bogfører, bogføres den relevante værdi på lagerkontoen, reguleringskontoen og vareforbrugskontoen i finansregnskabet.

Automatisk lagerværdibogføring er defineret i feltet **Aut. lagerværdibogføring** på siden **Lageropsætning**.

Selvom lagerværdien automatisk bogføres i Finans, er det stadig nødvendigt at sikre, at værdien af varerne overføres til de relaterede udgående transaktioner, f.eks salg eller overflytninger. Dette er især vigtigt i de situationer, hvor du sælger varer, inden du fakturerer købet af varerne. Dette omtales som omkostningsregulering. Varepriser reguleres automatisk, når du bogfører transaktioner, men du kan også justere varepriser manuelt. Du kan finde flere oplysninger i [Regulere varepriser](inventory-how-adjust-item-costs.md).

## <a name="to-post-inventory-costs-manually" />Sådan bogføres lagerværdier manuelt

1. Vælg ![Lightbulb, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **Bogfør lagerregulering**, og vælg derefter det relaterede link.
2. Du kan bogføre lagerværdier i finansregnskabet ved at udføre kørslen. Når du udfører denne kørsel, oprettes finansposter ud fra værdiposterne. Du kan bogføre posterne, så de opsummeres pr. bogføringsgruppe.

> [!NOTE]  
> Når du udfører kørslen, kan du finde fejl, der relaterer til manglende opsætning eller inkompatibel opsætning af dimensioner. Hvis kørslen finder fejl i opsætningen af dimensioner, bliver disse fejl tilsidesat, og kørslen bruger dimensionerne for værdiposten. For alle andre typer fejl springer kørslen bogføring af værdiposter over, og anfører dem i slutningen af rapporten under overskriften “Poster, der er sprunget over”. Du skal rette fejlene, inden du kan bogføre posterne.

Hvis du vil se en liste over fejl før kørslen af bogføringen, kan du køre rapporten **Bogfør lageromkostning - kontrol**. Denne kontrolrapport viser alle de fejl, som fanges under en bogføringstest. Du kan derefter rette fejlene og udføre kørslen til bogføring af lagerreguleringer uden at springe nogen poster over.

Hvis du ganske enkelt vil have en oversigt over, hvilke værdier der kan bogføres i finansregnskabet uden at gennemføre bogføringen, kan du udføre kørslen **Bogfør lagerregulering** uden at bogføre værdierne i finansregnskabet. Dette kan du gøre ved at fjerne markeringen i feltet **Bogfør** på anmodningssiden. Når du derefter udfører kørslen, oprettes der kun en rapport, der viser de værdier, der er klar til at blive bogført i finansregnskabet, men de er ikke bogført.

## <a name="to-audit-the-reconciliation-between-the-inventory-ledger-and-the-general-ledger" />Sådan reviderer du afstemningen mellem lagerposterne og finansposterne
Siden **Lagerbeholdning - afstemning** indeholder følgende:

- Vise afstemningsdifferencer ved at sammenligne det, der er registreret i finans, og det, der er registreret i lageropgørelsen (værdiposter).
- Vise ikke-afstemte kostbeløb i værdiposter i lageropgørelsen, som om de var koblet til tilsvarende lagerrelaterede konti i finans og sammenligne disse med de totaler, der faktisk registreres i de samme konti i finans.
- Afspejle dobbeltindtastningsstrukturen i finans ved visuelt at præsentere data som sådan. En vareforbrugsindtastning har f.eks. en tilsvarende lagerpost.
- Lade brugerne specificere og få vist de poster, der udgør kostbeløb.
- Inkludere filtre, der begrænser analysen efter dato, vare og lokation.
- Forklare årsager til afstemningsdifferencer i informative meddelelser.


Kolonnen **Navn** yderst til venstre i gitteret viser de forskellige finanskontotyper, der er tilknyttet lager.

Kolonnerne **Lager**, **Lager (mellemkonto)** og **Igangværende lager** viser de fakturerede og ikke-fakturerede totaler og totaler for igangværende arbejde for hver finanskontotype. Disse beregnes ud fra værdiposter, dvs. de projiceres over på de finanskontotyper, hvor de skal være, når de til sidste bogføres til finans.

Kolonnen **Total** viser summen (med fed tekst) af værdipostbeløbene i de tre lagerkolonner.

Kolonnen **Finanstotal** viser beløbene (med fed skrift) for hver finanskontotype, der findes i finans. Disse beregnes ud fra finansposter, dvs. de repræsenterer lagerreguleringer, der allerede er bogført til finans.

Kolonnen **Difference** repræsenterer forskellen mellem værdien i feltet **Finanstotal** og **Total**.

Øverst på siden **Lagerbeholdning - afstemning** kan du filtre for at begrænse, hvilke oplysninger der skal vises, f.eks. inden for en bestemt periode.

Hvis du vælger afkrydsningsfeltet **Vis advarsel**, og hvis der er uoverensstemmelser mellem lagertotaler og finanstotaler, vises meddelelser i feltet **Advarsel** for gitteret, som beskriver uoverensstemmelserne. Hvis du klikker på feltet Advarsel, får du yderligere oplysninger om, hvad advarslen betyder.

Vælg handlingen **Vis matrix**, når du har angivet alle relevante filtre. Dataene udregnes og matrixsiden vises.

I den venstre kolonne i gitteret vises forskellige finanskontotyper, som er tilknyttet lageret. Gitteret viser derefter totalerne for fakturerede, ufakturerede (foreløbige) og VIA-værdi for hver kontotype. Disse totaler beregnes ud fra værdiposterne.

De næste kolonner viser totalerne for de samme kontotyper beregnet ud fra finansposterne.

Vælg beløbet i en af totalerne for at se de poster i lagerrapporten, der blev brugt til at beregne totalerne. For lagertotalerne er posterne i lagerrapporten summen af værdiposterne for varerne. For finanstotalerne er posterne i lagerrapporten summen fra finansposterne.

## <a name="reporting-costs-and-reconciling-with-the-general-ledger" />Rapportere omkostninger og afstemme med regnskabet
Andre rapporter, sporingsfunktioner og et særligt afstemnings værktøj er tilgængelige for den revisor eller controller, der er ansvarlig for at rapportere en korrekt og afstemt lagerværdi til finansafdelingen.

Den følgende tabel beskriver dem.    

|**Hvis du vil**|**Se**|  
|------------|-------------|  
|Have vist lagerværdien for de valgte varer, herunder oplysninger om antal og værdi af lagertilgange og -afgange i en valgt periode.|**Lagerværdirapport**|  
|Have vist lagerværdien for valgte produktionsordrer i lageret for igangværende arbejde (VIA), f.eks. antal og værdi af forbrug, kapacitetsudnyttelse og output i igangværende produktionsordrer.|**Lagerværdi – igangværende arbejde**, rapport|  
|Have vist lagerværdien af valgte varer, herunder deres faktiske og forventede kostpris på den angivne dato.|**Lagerværdi – kostspecifikation**, rapport|  
|Bruge en rapport til at analysere årsagerne til kostprisuoverensstemmelser eller få indsigt i vareforbruget for solgte varer.|**Grundlag for kostprisfordeling**, rapport|  

## <a name="see-also" />Se også
[Administrere lageromkostninger](finance-manage-inventory-costs.md)  
[Køb](purchasing-manage-purchasing.md)  
[Salg](sales-manage-sales.md)    
[Arbejd med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  
[Generelle forretningsfunktioner](ui-across-business-areas.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]
