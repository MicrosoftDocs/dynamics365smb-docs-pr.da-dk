---
title: Regulere varepriser manuelt
description: 'Du kan manuelt regulere lagerværdien for en vare ved hjælp af FIFO eller gennemsnitlige kostmetoder, f.eks., når varepriser ændres af andre årsager end transaktioner.'
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 'cost adjustment, cost forwarding, costing method, inventory valuation, costing'
ms.date: 06/16/2021
ms.author: edupont
---
# <a name="adjust-item-costs"></a><a name="adjust-item-costs"></a><a name="adjust-item-costs"></a>Regulere varepriser
Kostprisen for en vare (lagerværdi), du køber og senere sælger, kan ændres i varens levetid, fordi f.eks. en fragtomkostning føjes til købsprisen, når du har solgt varen. Omkostningsregulering er især relevant i de situationer, hvor du sælger varer, inden du fakturerer købet af varerne. Hvis du altid vil kende den korrekte lagerværdi, skal varepriser regelmæssigt reguleres. Dette sikrer, at salgs- og indtjeningsstatistikkerne er opdateret, og at finansielle nøgletal er korrekte. Du kan finde flere oplysninger i [Designoplysninger: Omkostningsregulering](design-details-cost-adjustment.md).

Som regel er værdien i feltet **Kostpris** på varekortet baseret på standardkostprisen for varer, der følger standardkostmetoden. For varer, der følger andre kostmetoder, baseres værdien på en beregning af lagerbeholdningen (fakturerede kostpriser og forventede kostpriser) divideret med varebeholdningen. Der er flere oplysninger i [Om kostværdi pr. enhed](inventory-how-adjust-item-costs.md#understanding-unit-cost-calculation).

I [!INCLUDE[prod_short](includes/prod_short.md)] reguleres varepriser automatisk, hver gang der forekommer en lagertransaktion, f.eks. når du bogfører en købsfaktura for en vare.

Du kan også bruge en funktion til at regulere omkostningerne for en eller flere varer manuelt. Dette er nyttigt, når du f.eks. ved, at varepriser er ændret af andre årsager end varetransaktioner.

Varepriser reguleres efter FIFO eller den gennemsnitlige kostmetode, afhængigt af dit valg i den assisterede opsætningsvejledning **Konfigurer min virksomhed** eller i feltet **Kostmetode** på varekortet. Du kan finde flere oplysninger i [Registrere nye varer](inventory-how-register-new-items.md).  

Hvis du bruger kostmetoden FIFO, er en vares kostpris er den faktiske værdi af alle modtagelser af varen. Lager vurderes ud fra den forudsætning, at de første varer, der lægges på lager, bliver solgt først.

Hvis du bruger kostmetoden Gennemsnit, beregnes en vares kostpris som den gennemsnitlige kostpris på hvert enkelt tidspunkt efter et køb. Lager værdiansættes ud fra den forudsætning, at alle lagerbeholdninger sælges samtidig. For varer, der bruger denne kostmetode, kan du vælge feltet **Kostpris** på varekortet for at få vist en oversigt over transaktioner, som den gennemsnitlige kostpris beregnes ud fra

Funktionen til regulering af kostpriser behandler kun de værdiposter, der endnu ikke er reguleret. Hvis der opstår en situation, hvor funktionen skal overføre ændrede indgående omkostninger til tilknyttede udgående poster, oprettes nye justeringsværdiposter, som er baseret på oplysningerne i de oprindelige værdiposter, men som indeholder justeringsbeløbet. Omkostningsreguleringsfunktionen bruger bogføringsdatoen for den oprindelige værdipost i justeringsposten, medmindre den dato er inden for en lukket lagerperiode. Hvis det er tilfældet, bruges startdatoen for den næste åbne lagerperiode. Hvis der ikke anvendes lagerperioder, er det datoen i feltet **Bogf. tilladt fra** på siden **Regnskabsopsætning**, der definerer, hvornår reguleringsposten bogføres.

## <a name="to-adjust-item-costs-manually"></a><a name="to-adjust-item-costs-manually"></a><a name="to-adjust-item-costs-manually"></a>Sådan reguleres varekostpriser manuelt
1. Vælg ![Lightbulb, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **uster kostpris – Vareposter**, og vælg derefter det relaterede link.
2. På siden **Reguler kostværdi - vareposter** skal du angive de varer, hvis omkostninger skal reguleres.
3. Vælg knappen **OK**.

## <a name="to-make-general-changes-in-the-direct-unit-cost"></a><a name="to-make-general-changes-in-the-direct-unit-cost"></a><a name="to-make-general-changes-in-the-direct-unit-cost"></a>Sådan foretages generelle rettelser af købspris
Hvis du skal rette købsprisen for en række varer, kan du bruge kørslen **Reguler varepriser**.  

 Kørslen bruges til at rette oplysningerne i feltet **Købspris** på varekortet. Felterne ændres på samme måde for alle varer eller for de valgte varer. Det sker, ved at værdien i feltet ganges med en reguleringsfaktor, som du angiver.  

1. Vælg ![Lightbulb, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **Reguler varepriser**, og vælg derefter det relaterede link.  
2. Angiv, hvilket vare- eller lagervarekortfelt, du vil justere, i feltet **Reguler felt**.  
3. Angiv den faktor, som værdien skal reguleres med i feltet **Ganges med**. Skriv for eksempel **1,5** for at forøge værdien med 50 %.  
4. Angiv f.eks. filtre for at specificere, hvilke varer der skal behandles med kørslen i oversigtspanelet **Vare**.  
5. Vælg knappen **OK**.  

## <a name="understanding-unit-cost-calculation"></a><a name="understanding-unit-cost-calculation"></a><a name="understanding-unit-cost-calculation"></a>Om kostværdi pr. enhed
Som regel er værdien i feltet **Kostpris** på varekortet baseret på standardkostprisen for varer, der følger standardkostmetoden. For varer, der følger andre kostmetoder, baseres værdien på en beregning af lagerbeholdningen (fakturerede kostpriser og forventede kostpriser) divideret med varebeholdningen.  

 Nedenfor beskrives, hvordan indholdet af feltet **Kostmetode** påvirker beregningen af kostprisen for både køb og salg.  

## <a name="unit-cost-calculation-for-purchases"></a><a name="unit-cost-calculation-for-purchases"></a><a name="unit-cost-calculation-for-purchases"></a>Beregne kostpris ved køb
 Når du køber varer, overføres værdien i feltet **Sidste købspris** på varekortet altid til feltet **Købspris** på en købslinje eller til linjen Pris på en serviceartikelkladdelinje.  

 Det, du vælger i feltet **Kostmetode**, har indflydelse på, hvordan [!INCLUDE[prod_short](includes/prod_short.md)] beregner indholdet i felterne **Kostpris** på linjerne.  

### <a name="costing-method-fifo-lifo-specific-or-average"></a><a name="costing-method-fifo-lifo-specific-or-average"></a><a name="costing-method-fifo-lifo-specific-or-average"></a>Kostmetoden FIFO, LIFO, Serienummer eller Gennemsnit
 [!INCLUDE[prod_short](includes/prod_short.md)] beregner indholdet af feltet **Kostpris RV** på købslinjen og indholdet af feltet **Kostpris** på serviceartikelkladdelinjen beregnes efter følgende formel:  

 Kostpris (RV) = (Direkte kostpris - (Fakturarabatbeløb/Antal)) x (1 + Omkostningspct./100) + IPO-bidrag  

### <a name="costing-method-standard"></a><a name="costing-method-standard"></a><a name="costing-method-standard"></a>Kostmetoden Standard
 Feltet **Kostpris (RV)** på købslinjen eller feltet **Kostpris** udfyldes på varekladdelinjen ved at kopiere værdien i feltet **Kostpris** på varekortet. Ved at bruge kostmetoden som Standard, er værdien altid baseret på standardkostprisen.  

 Når du bogfører købet, kopieres kostprisen fra købslinjen eller varekladdelinjen til købsfakturaposten, og den kan ses på varens postoversigt.  

### <a name="all-costing-methods"></a><a name="all-costing-methods"></a><a name="all-costing-methods"></a>Alle kostmetoder
 Programmet bruger altid kostprisen fra kildedokumentlinjen til at beregne indholdet af feltet **Kostbeløb faktisk**, eller hvis det er relevant, feltet **Kostbeløb forventet** i forbindelse med denne post, uanset hvilken kostmetode der anvendes for varen.  

## <a name="unit-cost-calculation-for-sales"></a><a name="unit-cost-calculation-for-sales"></a><a name="unit-cost-calculation-for-sales"></a>Beregne kostpris ved salg
 Når du sælger varer, overføres kostprisen altid fra feltet Kostpris på varekortet til salgslinjen eller serviceartikelkladdelinjen.  

 Når du bogfører overføres kostprisen til salgsfakturaposten, og den kan ses på varens postoversigt. [!INCLUDE[prod_short](includes/prod_short.md)] bruger kostprisen fra kildedokumentlinjen til beregne indholdet af feltet **Kostbeløb faktisk** eller, hvis det er relevant, feltet **Kostbeløb forventet** i den værdipost, der er forbundet med denne varepost.  

## <a name="see-also"></a><a name="see-also"></a><a name="see-also"></a>Se også
[Administrere lageromkostninger](finance-manage-inventory-costs.md)  
[Lagerbeholdning](inventory-manage-inventory.md)  
[Salg](sales-manage-sales.md)  
[Køb](purchasing-manage-purchasing.md)  
[Arbejd med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]
