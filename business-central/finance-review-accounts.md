---
title: Gennemse finanskonti
description: 'Du kan spore din status, når du gennemgår beløb på finanskonti.'
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bholtorf
ms.topic: conceptual
ms.date: 02/28/2023
ms.custom: bap-template
ms.search.form: '22207,'
ms.service: dynamics-365-business-central
---

# <a name="review-amounts-in-general-ledger-accounts"></a>Gennemse beløb i finanskonti

Du kan have finanskonti, som du ofte holder øje med. Du kan også få brug for at gøre gennemsynsprocessen hurtigere i slutningen af måneden. Hvis du vil have hjælp til at holde styr på, hvad du har foretaget, og for at øge hastigheden på korrekturer, skal du bruge handlingen **Gennemse poster** på **Kontoplan** eller **Finanskort**- siden for hver konto. 

## <a name="set-up-accounts-for-reviews"></a>Oprette konti til gennemsyn

På siden **Finanskort** skal du angive, hvordan der skal kunne gennemgås gennemsyn, i feltet **Gennemgå politik** .

|Gennemse politik  |Beskrivlse  |
|---------|---------|
|Ingen     | Du kan ikke markere poster til kontoen som gennemgået. Du kan f. eks. bruge denne indstilling til konti som kreditorer, tilgodehavender og bankkonti, hvor du kan få vist beløbene på andre måder.        |
|Tillad gennemsyn     | Du behøver ikke at medtage poster i en revision, og beløbene fra debet-og Kreditposterne behøver ikke at være balanceret. Du fjerner en korrektur, f. eks. Hvis du har lavet en fejl.        |
|Tillad gennemsyn, og match saldo     | De samlede beløb for debet-og kreditposter i gennemsyn skal stemme overens. Felterne **Debet** og **Kredit** viser disse beløb, og feltet **Saldo** viser totalen. Du kan også bruge denne indstilling til at fjerne en korrektur. Når du fjerner en korrektur fra en eller flere poster, skal debet- og kreditposterne stadig være balanceret.        |

## <a name="mark-entries-as-reviewed"></a>Markere poster som gennemset

Vælg de poster, du har gennemgået, og brug derefter handlingen **Angiv valgt som gennemset**. Hver gang du markerer en eller flere poster som gennemgået, får posterne samme nummer i kolonnen **Revideret id**. Gennemsyns-id'et er en praktisk måde at holde styr på de poster, der blev gennemgået på samme tid. [!INCLUDE [prod_short](includes/prod_short.md)] registrerer også den bruger, som har gennemgået revisionen, og hvornår det gjorde sig.

Hvis du markerer poster som gennemset, men gør det, skal du bruge handlingen **Angiv valgt som ikke-gennemset**.

* Hvis der er tildelt en politik for gennemsyn af tilladelse til kontoen, nulstiller handlingen det gennemsøgte id til 0 og fjerner personen og dato og klokkeslæt for gennemsyn. 
* Hvis politikken for gennemsyn tilladt og match saldoen er tildelt, skal kredit og debet stadig være balanceret. Hvis en af posterne i en anmeldelse f. eks. er en fejl, kan du vælge en anden post med den korrekte værdi. Erstatnings posten behøver ikke at have det samme gennem Review-id.

> [!TIP]
> Du kan hurtigt vælge flere poster ved at holde Ctrl eller Skift nede, mens du vælger posterne. Ctrl gør det muligt at markere bestemte poster, og med Skift markeres alle de poster mellem den første og sidste post, du markerer.

## <a name="review-accounts-that-have-old-entries"></a>Gennemse konti, der har gamle poster

Du kan have poster fra tidligere perioder, som du allerede har gennemgået, eller som du bare ikke har brug for. Du skal blot begynde at gennemgå posterne fra, f. eks. begyndelsen af året eller regnskabsperioden. Du kan efterlade posterne, som de er. Hvis du vil analysere data i Excel eller ved hjælp af analyse tilstand, skal du markere posterne som gennemgået. Du kan få mere at vide om analyseposter ved at gå til [Analysere poster](#analyze-entries). Hvis du vil markere posterne som gennemgået, skal du tilføje et filter i filterruden for kun at få vist de pågældende poster og derefter vælge handlingen **Angiv valgte poster som gennemset**.

## <a name="filter-entries"></a>Filtrere poster

Hvis du vil have et mere klart billede, kan du filtrere posterne på siden **Gennemse finansposter** på flere måder.

* Brug siden **Vis korrekturlæste poster** og **Skjul korrekturlæste poster**, hvis du kun vil have vist de indtastninger, du har eller ikke har læst. Hvis du vil rydde filtrene, skal du bruge handlingen **Vis alle poster**.
* Anvend filterruden. Du kan f. eks. filtrere efter kontonummer eller, hvis du har ældre poster og vil markere dem alle som gennemgået, en bogføringsdato.

## <a name="analyze-entries"></a>Analysér objekter

Du kan analysere de finansposter, du har gennemgået, på flere måder.

* Slå analyse tilstand til, f. eks. for at gruppere poster efter deres gennemset id. Hvis du vil vide mere om analyse tilstand, skal du gå til [Analysere listeside data ved hjælp af analysetilstand](analysis-mode.md).
* Eksporter poster til Excel.

## <a name="see-also"></a>Se også

[Forstå Finansbogholderi og kontoplanen](finance-general-ledger.md)  
[Konfigurere eller ændre kontoplanen](finance-setup-chart-accounts.md)  
