---
title: "Konfigurere særlige salgspriser og rabatter for kunder | Microsoft Docs"
description: "Beskriver, hvordan du definerer de alternative pris- og rabataftaler, som du vil anvende på salgsdokumenter, når du sælger til forskellige kunder."
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: special price, alternate price, pricing
ms.date: 03/16/2018
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: d7fb34e1c9428a64c71ff47be8bcff174649c00d
ms.openlocfilehash: 30a1d6e6e5db6b94787b6b2e250a2824ba3fc8b3
ms.contentlocale: da-dk
ms.lasthandoff: 03/22/2018

---
# <a name="record-special-sales-prices-and-discounts"></a>Registrere specialsalgspriser og -rabatter
De forskellige pris- og rabataftaler, der gælder ved salg til forskellige debitorer, skal defineres, så de aftalte regler og værdier anvendes i de salgsdokumenter, der oprettes for debitorerne.

Når du har registreret særpriser og linjerabatter for salg og køb, sørger [!INCLUDE[d365fin](includes/d365fin_md.md)] for, at dine avance på varehandel altid er optimal ved automatisk at beregne den bedste pris på salgs- og købsdokumenter og på sags- og varekladdelinjer. Du kan finde flere oplysninger i afsnittet "Beregning af bedste pris".

Med hensyn til priser kan du få en særlig salgspris indsat på salgslinjerne, hvis en bestemt kombination af kunde, vare, minimumantal, enhed eller start-/slutdato findes.

Med hensyn til rabatter kan du oprette og bruge to typer salgsrabat:

| Rabattype | Beskrivelse |
| --- | --- |
| **Salgslinjerabat** |En beløbsrabat, der indsættes på salgslinjerne, hvis en bestemt kombination af kunde, vare, minimumsantal, enhed eller start-/slutdato findes. Dette fungerer på samme måde som for salgspriser. |
| **Fakturarabat** |En procentvis rabat, der fratrækkes fra dokumenttotalen, hvis værdibeløbet for alle linjer i et salgsdokument overstiger et bestemt minimum. |

Da salgspriser og salgslinjerabatter er baseret på en kombination af vare og debitor, kan du også udføre denne konfiguration fra varekortet for den vare, som reglerne og værdierne gælder for.

> [!NOTE]  
> Hvis du ikke ønsker, at en vare nogensinde skal sælges med rabat, kan du lade rabatfelterne på varekortet være tomme, og medtag ikke varen i nogen opsætningen af linjerabat.

## <a name="to-set-up-a-sales-price-for-a-customer"></a>Sådan konfigureres salgspriser for en debitor
1. Vælg ikonet ![Søg efter side eller rapport](media/ui-search/search_small.png "Ikonet Søg efter side eller rapport"), angiv **Debitorer**, og vælg derefter det relaterede link.
2. Åbn det relevante debitorkort, og vælg derefter handlingen **Priser**.

    Feltet **Salgstype** er på forhånd udfyldt med **Debitor**, og feltet **Salgskode** er udfyldt med debitornummeret.
3. Udfyld felterne på linjen efter behov. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)] Udfyld en linje for hver kombination, som yder en særlig salgspris til kunden.

## <a name="to-set-up-a-sales-line-discount-for-a-customer"></a>Sådan konfigureres salgslinjerabatter for en debitor
1. Vælg ikonet ![Søg efter side eller rapport](media/ui-search/search_small.png "Ikonet Søg efter side eller rapport"), angiv **Debitorer**, og vælg derefter det relaterede link.
2. Åbn det relevante debitorkort, og vælg derefter handlingen **Linjerabatter**.

    Feltet **Salgstype** er på forhånd udfyldt med **Debitor**, og feltet **Salgskode** er udfyldt med debitornummeret.
3. Udfyld felterne på linjen efter behov. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)] Udfyld en linje for hver kombination, som yder en salgslinjerabat til kunden.

## <a name="to-set-up-an-invoice-discount-for-a-customer"></a>Sådan oprettes en fakturarabat for en debitor
Når du har besluttet, hvilke kunder der skal have fakturarabatter, skal du angive fakturarabatkoden på debitorkortene og definere betingelserne for hver kode.

1. Vælg ikonet ![Søg efter side eller rapport](media/ui-search/search_small.png "Ikonet Søg efter side eller rapport"), angiv **Debitorer**, og vælg derefter det relaterede link.
2. Åbn debitorkortet for en debitor, der kan ydes mængderabat til.
3. Vælg en kode i feltet **Fakturarabatkode** for de fakturarabatbetingelser, som skal bruges til automatisk beregning af fakturarabat til debitoren.

> [!NOTE]  
>   Fakturarabatkoder repræsenteres af eksisterende debitorkort. Det gør det muligt hurtigt at tildele betingelserne for fakturarabatten til debitorer ved at vælge navnet på en anden debitor, der skal have samme betingelser.

Fortsæt med at angive nye fakturarabatbetingelser for salg.

1. I vinduet **Debitorkort** skal du vælge handlingen **Fakturarabatter**. Vinduet **Deb./fakt.-rabatter** åbnes.
2. Angiv koden for den valuta, som fakturarabatbetingelserne på linjen gælder for, i feltet **Valutakode**. Lad feltet stå tomt for at angive fakturarabatbetingelser for RV.
3. Angiv det minimumsbeløb, der berettiger til rabatten, i feltet **Min. beløb**.
4. I feltet **Rabatpct.** skal du angive fakturarabatten som en procentdel af fakturabeløbet.
5. Gentag trin 5-7 for hver valuta, som debitoren får en personlig fakturarabat for.

Fakturarabatten er nu oprettet og knyttet til den pågældende debitor. Når du vælger debitorkoden i feltet **Fakturarabatkode** på andre debitorkort, knyttes samme fakturarabat til den pågældende debitor.

## <a name="to-work-with-sales-invoice-discounts-and-service-charges"></a>Sådan arbejder du med salgsfakturarabatter og servicegebyrer
Når du bruger fakturarabatter, bestemmer fakturabeløbet størrelsen af rabatten.  

I vinduet **Deb./fakt.-rabatter** kan du også føje et servicegebyr til fakturaer over en vis størrelse.  

Du skal angive nogle oplysninger i programmet, før du kan bruge fakturarabatter i forbindelse med salg. Du skal angive:  

- hvilke debitorer der skal tildeles denne type rabat.  
- hvilken rabatprocent du vil bruge.  

Hvis dine fakturarabatter skal beregnes automatisk, kan du angive dette i vinduet **Salgsopsætning**.  

Du kan angive for hver kunde, om du til yde fakturarabat, hvis betingelserne er opfyldt, dvs. hvis fakturabeløbet er stort nok. Du kan definere, at betingelserne for fakturarabatten er DKK for danske debitorer og udenlandsk valuta for udenlandske debitorer.  

Du kan knytte rabatter til bestemte fakturabeløb i vinduerne **Deb./fakt.-rabatter**. Du kan angive et vilkårligt antal procenter i hvert vindue. Hver debitor kan have sit eget vindue, eller du kan sammenkæde flere debitorer i det samme vindue.  

Du kan også knytte et servicegebyr til et bestemt fakturabeløb i tillæg til eller i stedet for rabatprocenten.  

> [!TIP]  
>  Det anbefales, at du forbereder en skitse over den rabatstruktur, der skal anvendes, før du begynder at indtaste oplysninger i programmet. Det gør det nemmere at se, hvilke debitorer der kan knyttes til samme fakturarabatvindue. Jo færre vinduer, du har sat op, jo hurtigere kan du indtaste stamoplysningerne.  

## <a name="best-price-calculation"></a>Beregning af bedste pris
Når du har registreret særpriser og linjerabatter for salg og køb, sørger [!INCLUDE[d365fin](includes/d365fin_md.md)] for, at dine avance på varehandel altid er optimal ved automatisk at beregne den bedste pris på salgs- og købsdokumenter og på sags- og varekladdelinjer.

Den bedste pris er den lavest tilladte pris med den størst tilladte linjerabat på en givet dato. [!INCLUDE[d365fin](includes/d365fin_md.md)] beregner automatisk dette, når enhedsprisen og linjerabatprocenten for varer indsættes på nye dokument- og kladdelinjer.

> [!NOTE]  
>   I det følgende beskrives, hvordan den bedste pris beregnes for salg. Beregningen er den samme for køb.

1. [!INCLUDE[d365fin](includes/d365fin_md.md)] kontrollerer kombinationen af faktureringsdebitoren og varen automatisk og beregner derefter den relevante enhedspris og linjerabatprocent ud fra følgende kriterier:

    - Har denne kunde en pris-/rabataftale, eller tilhører kunden en gruppe, der har en sådan aftale?
    - Er varen eller varerabatgruppen på linjen medtaget i nogen af disse pris/rabataftaler?
    - Ligger ordredatoen (bogføringsdatoen for faktura- eller kreditnotaen) inden for start- og slutdatoen for pris-/rabataftalen?
    - Er enhedskoden angivet? Hvis den gør det, kontrollerer [!INCLUDE[d365fin](includes/d365fin_md.md)], om der er priser/rabatter med samme enhedskode, og om der er priser/rabatter, uden at der er tilknyttet en enhedskode.

2. [!INCLUDE[d365fin](includes/d365fin_md.md)] kontrollerer, om der ligger pris-/ rabataftaler i oplysningerne om dokument- eller kladdelinjen og indsætter derefter den relevante enhedspris og linjerabatprocent ud fra følgende kriterier:

    - Er der et krav om et mindste antal i pris-/ rabataftalen, som er opfyldt?
    - Er der et krav om valuta i pris-/ rabataftalen, som er opfyldt? Hvis der er det, indsættes den laveste pris og den højeste linjerabat for valutaen, selvom den lokale valuta giver en bedre pris. Hvis der ikke er nogen pris-/rabataftale for den angivne valutakode, indsætter [!INCLUDE[d365fin](includes/d365fin_md.md)] den laveste pris og den højeste linjerabat i din lokale valuta.

Hvis der ikke kan beregnes en særpris for varen på linjen, indsættes seneste indirekte omkostning eller enhedsprisen fra varekortet.

## <a name="to-copy-sales-prices"></a>Sådan kopieres salgspriser  
Hvis du vil kopiere en salgspris, f.eks. en individuel kundes salgspriser til brug for en debitorprisgruppe, skal du køre **Forslå salgspris på kladde**. kørsel. Kørslen findes i vinduet **Salgspriskladde**.    

1.  Vælg ikonet ![Søg efter side eller rapport](media/ui-search/search_small.png "Ikonet Søg efter side eller rapport"), angiv **Salgspriskladde**, og vælg derefter det relaterede link.  
2.  Vælg handlingen **Foreslå salgspris på kld.** .  
3.  Udfyld felterne **Salgstype** og **Salgskode** i oversigtspanelet **Salgspriser** med de oprindelige salgspriser, du vil kopiere.  
4.  Udfyld felterne **Salgstype** og **Salgskode** i den øverste del af vinduet med den type og det navn, du vil have salgspriserne kopieret til.  
5.  Hvis kørslen skal oprette nye priser, skal du markere feltet **Opret nye priser**.  
6.  Vælg knappen **OK** for at udfylde linjerne i vinduet **Salgspriskladde** med de foreslåede nye priser for at angive, at de er gyldige for den valgte **Salgstype**.  

> [!NOTE]  
>  Kørslen betyder kun, at der udformes forslag, ikke, at ændringerne bliver gennemført. Hvis du er tilfreds med forslagene, og du vil implementere dem, dvs. indsætte dem i tabellen **Salgspris**, kan du bruge kørslen **Implementer prisændring**, der findes under fanen **Handlinger**, i gruppen **Funktioner** i vinduet **Salgspriskladde**.

## <a name="see-also"></a>Se også
[Konfigurere salg](sales-setup-sales.md)  
[Salg](sales-manage-sales.md)  
[Arbejde med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

