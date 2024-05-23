---
title: Regulere varepriser manuelt
description: 'Du kan regulere lagerværdien for en vare ved hjælp af FIFO eller gennemsnitlige kostmetoder, f.eks., når varepriser ændres af andre årsager end transaktioner.'
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bholtorf
ms.topic: conceptual
ms.search.keywords: 'cost adjustment, cost forwarding, costing method, inventory valuation, costing'
ms.date: 03/08/2024
ms.service: dynamics-365-business-central
ms.custom: bap-template
---
# Justere varepriser

Kostprisen for en vare (lagerværdi), du køber og senere sælger, kan ændres i varens levetid, fordi f.eks. en fragtomkostning føjes til købsprisen, når du har solgt varen. Omkostningsregulering er især relevant i de situationer, hvor du sælger varer, inden du fakturerer købet af varerne. Hvis du altid vil kende den korrekte lagerværdi, skal du regelmæssigt regulere varepriser. Rigtige kostpriser er med til at sikre, at salgs- og indtjeningsstatistikkerne er opdateret, og at finansielle nøgletal er korrekte. Du kan finde flere oplysninger i [Designoplysninger: Omkostningsregulering](design-details-cost-adjustment.md).

Værdien i feltet **Kostpris** på varekortet er baseret på standardkostprisen for varer, der følger standardkostmetoden. For varer, der følger andre kostmetoder, er værdien baseret på en beregning af den disponible lagerbeholdning (fakturerede kostpriser og forventede kostpriser) divideret med varebeholdningen. Der er flere oplysninger i [Om kostværdi pr. enhed](inventory-how-adjust-item-costs.md#understanding-unit-cost-calculation).

I [!INCLUDE[prod_short](includes/prod_short.md)] reguleres varepriser automatisk, hver gang der forekommer en lagertransaktion, f.eks. når du bogfører en købsfaktura for en vare.

Du kan også regulere omkostningerne for en eller flere varer manuelt. En manuel regulering er f.eks. nyttig, når du ved, at varepriser er ændret af andre årsager end varetransaktioner.

Varepriser reguleres efter FIFO eller den gennemsnitlige kostmetode, afhængigt af dit valg i den assisterede opsætningsvejledning **Konfigurer min virksomhed** eller i feltet **Kostmetode** på varekortet. Du kan finde flere oplysninger i [Registrere nye varer](inventory-how-register-new-items.md).  

For kostmetoden FIFO er en vares kostpris den faktiske værdi af alle modtagelser af varen. Lager vurderes ud fra den forudsætning, at de første varer, der lægges på lager, bliver solgt først.

Hvis du bruger kostmetoden Gennemsnit, beregnes en vares kostpris som den gennemsnitlige kostpris på hvert enkelt tidspunkt efter et køb. Lager værdiansættes ud fra den forudsætning, at alle lagerbeholdninger sælges samtidig. For varer, der bruger denne kostmetode, kan du vælge feltet **Kostpris** på varekortet for at få vist en oversigt over transaktioner, som den gennemsnitlige kostpris beregnes ud fra

Regulering af kostpriser behandler kun de værdiposter, der ikke er reguleret. I en situation, hvor ændrede indgående kostpriser skal overføres til relaterede udgående poster, oprettes der nye reguleringsværdiposter. Reguleringsværdiposterne er baseret på oplysningerne i de oprindelige værdiposter, men indeholder reguleringsbeløbet. Omkostningsreguleringsfunktionen bruger bogføringsdatoen for den oprindelige værdipost i justeringsposten, medmindre den dato er inden for en lukket lagerperiode. Hvis det er tilfældet, bruges startdatoen for den næste åbne lagerperiode. Hvis der ikke anvendes lagerperioder, er det datoen i feltet **Bogf. tilladt fra** på siden **Regnskabsopsætning**, der definerer, hvornår reguleringsposten bogføres.

## Sådan reguleres varekostpriser manuelt

1. Vælg ![Lightbulb, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **uster kostpris – Vareposter**, og vælg derefter det relaterede link.
2. På siden **Reguler kostværdi - vareposter** skal du angive de varer, hvis omkostninger skal reguleres.
3. Vælg knappen **OK**.

## Sådan foretages generelle rettelser af købspris

Hvis du skal rette købsprisen for en række varer, kan du bruge kørslen **Reguler varepriser**.  

Kørslen bruges til at rette oplysningerne i feltet **Købspris** på varekortet. Felterne ændres på samme måde for alle varer eller for de valgte varer. Det sker, ved at værdien i feltet ganges med en reguleringsfaktor, som du angiver.  

1. Vælg ![Lightbulb, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **Reguler varepriser**, og vælg derefter det relaterede link.  
2. Angiv, hvilket vare- eller lagervarekortfelt, du vil justere, i feltet **Reguler felt**.  
3. Angiv den faktor, som værdien skal reguleres med, i feltet **Ganges med**. Skriv for eksempel **1,5** for at forøge værdien med 50 %.  
4. Angiv f.eks. filtre for at specificere, hvilke varer der skal behandles med kørslen i oversigtspanelet **Vare**.  
5. Vælg knappen **OK**.  

## Om beregning af kostpris

Værdien i feltet **Kostpris** på varekortet er baseret på standardkostprisen for varer, der følger standardkostmetoden. For varer, der følger andre kostmetoder, er værdien baseret på en beregning af den disponible lagerbeholdning (fakturerede kostpriser og forventede kostpriser) divideret med varebeholdningen.  

Nedenfor beskrives, hvordan indholdet af feltet **Kostmetode** påvirker beregningen af kostprisen for både køb og salg.  

## Beregne kostpris ved køb  

Når du køber varer, overføres værdien i feltet **Sidste købspris** på varekortet altid til feltet **Købspris** på en købslinje eller til linjen **Pris** på en varekladdelinje.  

Det, du vælger i feltet **Kostmetode**, har indflydelse på, hvordan [!INCLUDE[prod_short](includes/prod_short.md)] beregner indholdet i felterne **Kostpris** på linjerne.  

### Kostmetoderne FIFO, LIFO, Specifik eller Gennemsnit  

[!INCLUDE[prod_short](includes/prod_short.md)] bruger følgende formel til at beregne indholdet af feltet **Kostpris RV** på købslinjen eller indholdet af feltet **Kostpris** på varekladdelinjen:  

Kostpris (RV) = (Direkte kostpris - (Fakturarabatbeløb/Antal)) x (1 + Omkostningspct./100) + IPO-bidrag  

### Standardkostmetoden  

Feltet **Kostpris (RV)** på købslinjen eller feltet **Kostpris** udfyldes på varekladdelinjen ved at kopiere værdien i feltet **Kostpris** på varekortet. Hvis du bruger standardkostmetoden, er værdien altid baseret på standardkostprisen.  

Når du bogfører et køb, kopieres kostprisen fra købslinjen eller varekladdelinjen til købsfakturaposten. Den vises på varens postoversigt.  

### Alle kostmetoder  

Kostprisen fra kildedokumentlinjen bruges til at beregne værdien i feltet **Kostbeløb faktisk** eller, hvis det er relevant, feltet **Kostbeløb forventet**, der er forbundet med denne varepost. Kostprisen medtages i beregningen, uanset hvilken kostmetode varen har.  

## Beregne kostpris ved salg  

Når du sælger varer, overføres kostprisen altid fra feltet **Kostpris** på varekortet til salgslinjen eller varekladdelinjen.  

Når du bogfører, overføres kostprisen til salgsfakturaposten, og den kan ses på varens postoversigt. [!INCLUDE[prod_short](includes/prod_short.md)] bruger kostprisen fra kildedokumentlinjen til at beregne indholdet af feltet **Kostbeløb faktisk** eller, hvis det er relevant, feltet **Kostbeløb forventet** i den værdipost, der er forbundet med denne varepost.  

## Spore vareprisreguleringer

Der kan være mange årsager til, at vareomkostningerne ændrer sig, så det er vigtigt, at du kan holde styr på vareprisreguleringer. Brug siden **Regulering af lageromkostninger** til at administrere og overvåge omkostningsreguleringsprocessen. På denne side vises varer sammen med deres omkostningsparametre og status for omkostningsregulering. Du kan filtrere listen for at fokusere på varer, der kræver regulering, eller som ikke er medtaget i omkostningsreguleringen. Du kan få mere at vide om sporing af omkostningsreguleringer ved at gå til [Spore vareprisreguleringer](finance-track-inventory-costs.md).

## Se også

[Administrere lageromkostninger](finance-manage-inventory-costs.md)  
[Lagerbeholdning](inventory-manage-inventory.md)  
[Salg](sales-manage-sales.md)  
[Køb](purchasing-manage-purchasing.md)  
[Arbejd med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)

[!INCLUDE[footer-include](includes/footer-banner.md)]