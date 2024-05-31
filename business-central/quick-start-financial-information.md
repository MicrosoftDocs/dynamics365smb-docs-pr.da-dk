---
title: Virksomhedsoplysninger Finansielle oplysninger
description: Gør din virksomhed klar til virksomheder ved at oprette økonomiske oplysninger i Business central.
author: brentholtorf
ms.topic: conceptual
ms.devlang: al
ms.search.keywords: quickstart
ms.search.form: null
ms.date: 08/25/2022
ms.author: bholtorf
ms.service: dynamics-365-business-central
---

# Virksomhedsoplysninger Finansielle oplysninger

Når du har angivet grundlæggende virksomhedsoplysninger i [!INCLUDE[prod_short](includes/prod_short.md)], udfyldes et af de næste trin den økonomiske sektion. Du behøver ikke blot at modtage eller foretage betalinger, men også for at administrere og rapportere virksomhedens numre korrekt.

## Kontoplanen

Kontoplanen giver dig et overblik over virksomhedens økonomi og viser konti i strukturerede grupper, f. eks. aktiver, passiver, indkomst, vareforbrug og udgifter. [!INCLUDE[prod_short](includes/prod_short.md)] indeholder en standardkontoplan, du kan tilpasse til din virksomheds regnskabspraksis.

## Konfigurere kontoplanen

Følgende video viser, hvordan du opretter en kontoplan i [!INCLUDE[prod_short](includes/prod_short.md)].

<br /><br />

> [!Video https://www.microsoft.com/videoplayer/embed/RE43KO9?rel=0]

### Tilføj en konto i kontoplanen

Hvis du f. eks. vil tilføje en konto, der ikke er inkluderet som standard i [!INCLUDE[prod_short](includes/prod_short.md)]- f.eks. havearbejde - skal du benytte følgende fremgangsmåde:

1. Vælg ![Lightbulb, der åbner funktionen Fortæl mig 1.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **Kontoplan**, og derefter vælge det relaterede link.
2. Vælg handlingen **ny** for at åbne siden **Finanskort**.
3. På oversigtspanelet **Generelt** skal du udfylde felterne som beskrevet i følgende tabel. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

   | Felt | Data |
   | --- | --- |
   | **Nummer** | 61250 |
   | **Navn** | Havearbejde |
   | **Indtægter/saldo** | Resultatopgørelse |
   | **Kontokategori** | Udgift |
   | **Kontoens underkategori** | Reparations- og vedligeholdelsesudgifter |
   | **Debet/Kredit** | Begge |
   | **Kontotype** | Bogfører |

4. Indtast følgende data i oversigtspanelet **Bogføring**:

   | Felt | Data |
   | --- | --- |
   | **Bogføringstype** | Køb |
   | **Virksomhedsbogføringsgruppe** | Indenlandsk |
   | **Produktbogføringsgruppe** | Services |

5. På siden **Finanskontokort** skal du udfylde felterne efter behov. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

### Få vist en oversigt over kontoplanen

Hvis du har brug for en mere kompakt visning af kontoplanen, uden at der er angivet kolonner til bogføringsgrupper, bogføringstype eller omkostningstype, viser oversigten over **Kontoplan** hovedoplysningerne for hver konto i en mindre tabel. Du kan også skjule eller udvide grupper for at skjule kontiene i dem.

Hvis du vil have vist oversigten, skal du vælge handlingen **Oversigt over kontoplan** på siden **Kontoplan** eller søge efter funktionen med ![lightbulb, der åbner funktionen Fortæl mig 1.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig").

Få mere at vide om kontoplanen og finansregnskabet i [Forstå finansregnskabet og kontoplanen](finance-general-ledger.md).

## Opret bankkonti

Bankkonti i [!INCLUDE[prod_short](includes/prod_short.md)]-register med banktransaktioner, og som er knyttet til poster i kontoplanen. Følgende video viser, hvordan du opretter bankkonti.

<br /><br />

> [!Video https://www.microsoft.com/videoplayer/embed/RE3Vhpl?rel=0]

1. Vælg ![Lightbulb, der åbner funktionen Fortæl mig 1.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **Bankkonti**, vælg derefter det relaterede link.
2. På siden **Bankkonti** skal du vælge handlingen **Ny**.
3. I feltet **Nummer** felt, vil der automatisk blive indsat et id, f.eks. *B010*, hvis der er angivet en nummereret serie for bankkonti. Hvis det ikke er tilfældet, skal du derefter angive en entydig kombination.

   Feltet er ikke det samme som feltet **Bankkontonr.**, der også tilgængeligt i oversigtspanelet **Generelt**.
4. På siden **Kreditorbankkontokort** skal du udfylde felterne efter behov. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

## Se også

[Konfigurere kontoplaner](finance-setup-chart-accounts.md)  
[Konfigurere bankkonti](bank-how-setup-bank-accounts.md)  
[Køre og udskrive rapporter](ui-work-report.md)  
[Hurtig start af Business Central](quick-start-business-central.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
