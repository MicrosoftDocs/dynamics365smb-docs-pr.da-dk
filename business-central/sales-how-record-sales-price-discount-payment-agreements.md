---
title: Konfigurere særlige salgspriser og rabatter for kunder | Microsoft Docs
description: Beskriver, hvordan du definerer de alternative pris- og rabataftaler, som du vil anvende på salgsdokumenter, når du sælger til forskellige kunder.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: special price, alternate price, pricing
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: 0873c45262dd9606ac187f5aab07b09677f6c1c8
ms.sourcegitcommit: adf1a87a677b8197c68bb28c44b7a58250d6fc51
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 01/21/2021
ms.locfileid: "5035602"
---
# <a name="record-special-sales-prices-and-discounts"></a>Registrere specialsalgspriser og -rabatter

De forskellige pris- og rabataftaler, der gælder ved salg til forskellige debitorer, skal defineres, så de aftalte regler og værdier anvendes i de salgsdokumenter, der oprettes for debitorerne.

Når du har registreret særpriser og linjerabatter for salg og køb, sørger [!INCLUDE[prod_short](includes/prod_short.md)] for, at dine avance på varehandel altid er optimal ved automatisk at beregne den bedste pris på salgs- og købsdokumenter og på sags- og varekladdelinjer. Du kan finde flere oplysninger under [Beregning af bedste pris](sales-how-record-sales-price-discount-payment-agreements.md#best-price-calculation).

Med hensyn til priser kan du få en særlig salgspris indsat på salgslinjerne, hvis en bestemt kombination af kunde, vare, minimumantal, enhed eller start-/slutdato findes. Du kan finde flere oplysninger i sektionerne [Sådan konfigureres salgspriser til en debitor](#to-set-up-a-sales-price-for-a-customer)og [Bedste prisberegning](#best-price-calculation).  

Med hensyn til rabatter kan du oprette og bruge to typer salgsrabat:

| Rabattype | Beskrivelse |
| --- | --- |
| **Salgslinjerabat** |En beløbsrabat, der indsættes på salgslinjerne, hvis en bestemt kombination af kunde, vare, minimumsantal, enhed eller start-/slutdato findes. Dette fungerer på samme måde som for salgspriser. |
| **Fakturarabat** |En procentvis rabat, der fratrækkes fra dokumenttotalen, hvis værdibeløbet for alle linjer i et salgsdokument overstiger et bestemt minimum. |

Da salgspriser og salgslinjerabatter er baseret på en kombination af vare og debitor, kan du også udføre denne konfiguration fra varekortet for den vare, som reglerne og værdierne gælder for.

> [!NOTE]  
> Hvis du ikke ønsker, at en vare nogensinde skal sælges med rabat, kan du lade rabatfelterne på varekortet være tomme, og medtag ikke varen i nogen opsætningen af linjerabat.

## <a name="sales-invoice-discounts-and-service-charges"></a>Salgsfakturarabatter og servicegebyrer

Når du bruger fakturarabatter, bestemmer fakturabeløbet størrelsen af rabatten.  

På siden **Deb./fakt.rabatter** kan du også føje et servicegebyr til fakturaer over en vis størrelse.  

Du skal angive nogle oplysninger, før du kan bruge fakturarabatter i forbindelse med salg. Du skal beslutte følgende:  

- Hvilke debitorer der skal tildeles denne type rabat.  
- Hvilken rabatprocent du vil bruge.  

Hvis dine fakturarabatter skal beregnes automatisk, kan du angive dette på siden **Salgsopsætning**.  

Du kan angive for hver kunde, om du til yde fakturarabat, hvis betingelserne er opfyldt, dvs. hvis fakturabeløbet er stort nok. Du kan definere, at betingelserne for fakturarabatten er DKK for danske debitorer og udenlandsk valuta for udenlandske debitorer.  

Du kan knytte rabatter til bestemte fakturabeløb på siderne **Deb./fakt.-rabatter**. Du kan angive et vilkårligt antal procenter. Hver debitor kan have sin egen side, eller du kan sammenkæde flere debitorer på den samme side.  

Du kan også knytte et servicegebyr til et bestemt fakturabeløb i tillæg til eller i stedet for rabatprocenten.  

> [!TIP]  
> Det anbefales, at du forbereder en skitse over den rabatstruktur, der skal anvendes, før du begynder at indtaste oplysninger. Det gør det nemmere at se, hvilke debitorer der kan knyttes til samme fakturarabatside. Jo færre sider, du har sat op, jo hurtigere kan du indtaste stamoplysningerne.

Du finder flere øvelser i rabatter under [Konfiguration af rabatter til dine kunder](/learn/modules/customer-discounts-dynamics-365-business-central/index) på Microsoft Learn.  

### <a name="calculating-invoice-discounts-on-sales"></a>Beregning af fakturarabatter på salg

[!INCLUDE [sales-invoice-discounts](includes/sales-invoice-discounts.md)]

## <a name="to-set-up-a-sales-line-discount-for-a-customer"></a>Sådan konfigureres salgslinjerabatter for en debitor

1. Vælg ikonet ![Elpære, der åbner funktionen Fortæl mig](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig"), angiv **Debitorer**, og vælg derefter det relaterede link.
2. Åbn det relevante debitorkort, og vælg derefter handlingen **Linjerabatter**.

    På siden **Salgslinjerabatter** er feltet **Salgstype** på forhånd udfyldt med **Debitor**, og feltet **Salgskode** er udfyldt med debitornummeret.
3. Udfyld felterne på linjen efter behov. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)] Udfyld en linje for hver kombination, som yder en salgslinjerabat til kunden.

> [!Note]
> Når du åbner vinduerne **Salgspriser** og **Salgslinjerabatter** fra en bestemt kunde, er felterne **Salgstypefilter**  og **Salgskodefilter** angivet for debitoren og kan ikke ændres eller fjernes, hvilket er angivet med den grå værdi i feltet **Salgskodefilter.**
>
> Hvis du vil oprette priser eller linjerabatter for alle debitorer, en debitorprisgruppe eller en kampagne, skal du åbne vinduerne fra et varekort. Du kan alternativt bruge siden **Salgspriskladde** til salgspriser. Du kan finde flere oplysninger [Sådan masseopdateres varepriser](sales-how-record-sales-price-discount-payment-agreements.md#to-bulk-update-item-prices).  

## <a name="to-set-up-an-invoice-discount-for-a-customer"></a>Sådan oprettes en fakturarabat for en debitor

Når du har besluttet, hvilke kunder der skal have fakturarabatter, skal du angive fakturarabatkoden på debitorkortene og definere betingelserne for hver kode.

1. Vælg ikonet ![Elpære, der åbner funktionen Fortæl mig](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig"), angiv **Kunder**, og vælg derefter det relaterede link.
2. Åbn debitorkortet for en debitor, der kan ydes mængderabat til.
3. Vælg en kode i feltet **Fakturarabatkode** for de fakturarabatbetingelser, som skal bruges til automatisk beregning af fakturarabat til debitoren.

    > [!NOTE]  
    > Fakturarabatkoder repræsenteres af eksisterende debitorkort. Det gør det muligt hurtigt at tildele betingelserne for fakturarabatten til debitorer ved at vælge navnet på en anden debitor, der skal have samme betingelser. Hvis du vil oprette debitorspecifikke fakturarabatbetingelser, skal du angive feltet **Fakturarabatkode** til debitorens debitorkode og derefter fortsætte til næste trin.

4. På siden **Debitorkort** skal du vælge handlingen **Fakturarabatter**. Siden **Deb./fakt.-rabatter** åbnes.
5. Angiv koden for den valuta, som fakturarabatbetingelserne på linjen gælder for, i feltet **Valutakode**. Lad feltet stå tomt for at angive fakturarabatbetingelser for DKK.
6. Alternativt kan du angive det minimumsbeløb, der berettiger til rabatten, i feltet **Min. beløb**.
7. I feltet **Rabatpct.** skal du angive fakturarabatten som en procentdel af fakturabeløbet.
8. Gentag trin 5-7 for hver valuta, som debitoren får en personlig fakturarabat for.

Fakturarabatten er nu oprettet og knyttet til den pågældende debitor. Når du vælger debitorkoden i feltet **Fakturarabatkode** på andre debitorkort, knyttes samme fakturarabat til den pågældende debitor.

## <a name="to-set-up-a-sales-price-for-a-customer"></a>Sådan konfigureres salgspriser for en debitor

1. Vælg ikonet ![Elpære, der åbner funktionen Fortæl mig](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig"), angiv **Kunder**, og vælg derefter det relaterede link.
2. Åbn det relevante debitorkort, og vælg derefter handlingen **Priser**.

    På siden **Salgspriser** er feltet **Salgstype** på forhånd udfyldt med **Debitor**, og feltet **Salgskode** er udfyldt med debitornummeret.
3. Udfyld felterne på linjen efter behov. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)] Udfyld en linje for hver kombination, som yder en særlig salgspris til kunden.

## <a name="to-copy-sales-prices"></a>Sådan kopieres salgspriser

Hvis du vil kopiere en salgspris, f.eks. en individuel kundes salgspriser til brug for en debitorprisgruppe, skal du køre **Forslå salgspris på kladde**. batchjob, som du starter fra siden **Salgspriskladde**.  

1. Vælg ikonet ![Elpære, der åbner funktionen Fortæl mig](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig"), angiv **Salgspriskladde**, og vælg derefter det relaterede link.  
2. Vælg handlingen **Foreslå salgspris på kld.** .  
3. Udfyld felterne **Salgstype** og **Salgskode** i oversigtspanelet **Salgspriser** med de oprindelige salgspriser, du vil kopiere.  
4. Udfyld felterne **Salgstype** og **Salgskode** i den øverste del af siden med den type og det navn, du vil have salgspriserne kopieret til.  
5. Hvis kørslen skal oprette nye priser, skal du markere afkrydsningsfeltet **Opret nye priser**.  
6. Vælg knappen **OK** for at udfylde linjerne på siden **Salgspriskladde** med de foreslåede nye priser for at angive, at de er gyldige for den valgte salgstype.  

> [!NOTE]  
> Kørslen betyder kun, at der udformes forslag, ikke, at ændringerne bliver gennemført. Hvis du er tilfreds med forslagene, og du vil implementere dem, dvs. indsætte dem på siden **Salgspriser**, skal du vælge handlingen **Implementer prisændringer** på siden **Salgspriskladde**.

## <a name="to-bulk-update-item-prices"></a>Sådan masseopdateres varepriser

Hvis du vil masseopdatere varepriser, f.eks. forøge alle varepriser med en procentsats, skal du køre **Foreslå varepris på kladde.** kørsel. Du kan finde et link til kørslen på siden **Salgspriskladde**.  

1. Vælg ikonet ![Elpære, der åbner funktionen Fortæl mig](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig"), angiv **Salgspriskladde**, og vælg derefter det relaterede link.  
2. Vælg handlingen **Foreslå varepris på kladde** .  
3. I oversigtspanelet **Vare** skal du udfylde **Nummer**. eller **Varebogføringsgruppe** eller andre felter med de oprindelige varepriser, du vil opdatere.  
4. Udfyld felterne **Salgstype** og **Salgskode** i den øverste del af siden med den type og det navn, du vil have salgspriserne kopieret til.
5. Hvis kørslen automatisk skal justere foreslåede varepriser, skal du angive justeringen i feltet **Ganges med**. F.eks. skal du angive 1,15 i **Ganges med** for 15 % stigning i varepris.  
6. Hvis kørslen skal oprette nye priser, skal du markere feltet **Opret nye priser**.  
7. Vælg knappen **OK** for at udfylde linjerne på siden **Salgspriskladde** med de foreslåede nye priser for at angive, at de er gyldige for den valgte **Vare**.  

> [!NOTE]
> Kørslen betyder kun, at der udformes forslag, ikke, at ændringerne bliver gennemført. Hvis du er tilfreds med forslagene, og du vil implementere dem, dvs. indsætte dem i tabellen **Salgspris**, kan du bruge kørslen **Implementer prisændring**, der findes under fanen **Handlinger**, i gruppen **Funktioner** på siden **Salgspriskladde**.

## <a name="best-price-calculation"></a>Beregning af bedste pris

Når du har registreret særpriser og linjerabatter for salg og køb, sørger [!INCLUDE[prod_short](includes/prod_short.md)] for, at dine avance på varehandel altid er optimal ved automatisk at beregne den bedste pris på salgs- og købsdokumenter og på sags- og varekladdelinjer.

Den bedste pris er den lavest tilladte pris med den størst tilladte linjerabat på en givet dato. [!INCLUDE[prod_short](includes/prod_short.md)] beregner automatisk dette, når enhedsprisen og linjerabatprocenten for varer indsættes på nye dokument- og kladdelinjer.

> [!NOTE]  
> I det følgende beskrives, hvordan den bedste pris beregnes for salg. Beregningen er den samme for køb.

1. [!INCLUDE[prod_short](includes/prod_short.md)] kontrollerer kombinationen af faktureringsdebitoren og varen automatisk og beregner derefter den relevante enhedspris og linjerabatprocent ud fra følgende kriterier:

    - Har denne kunde en pris-/rabataftale, eller tilhører kunden en gruppe, der har en sådan aftale?
    - Er varen eller varerabatgruppen på linjen medtaget i nogen af disse pris/rabataftaler?
    - Ligger ordredatoen (bogføringsdatoen for faktura- eller kreditnotaen) inden for start- og slutdatoen for pris-/rabataftalen?
    - Er enhedskoden angivet? Hvis den gør det, kontrollerer [!INCLUDE[prod_short](includes/prod_short.md)], om der er priser/rabatter med samme enhedskode, og om der er priser/rabatter, uden at der er tilknyttet en enhedskode.

2. [!INCLUDE[prod_short](includes/prod_short.md)] kontrollerer, om der ligger pris-/ rabataftaler i oplysningerne om dokument- eller kladdelinjen og indsætter derefter den relevante enhedspris og linjerabatprocent ud fra følgende kriterier:

    - Er der et krav om et mindste antal i pris-/ rabataftalen, som er opfyldt?
    - Er der et krav om valuta i pris-/ rabataftalen, som er opfyldt? Hvis der er det, indsættes den laveste pris og den højeste linjerabat for valutaen, selvom den lokale valuta giver en bedre pris. Hvis der ikke er nogen pris-/rabataftale for den angivne valutakode, indsætter [!INCLUDE[prod_short](includes/prod_short.md)] den laveste pris og den højeste linjerabat i din lokale valuta.

Hvis der ikke kan beregnes en særpris for varen på linjen, indsættes seneste indirekte omkostning eller enhedsprisen fra varekortet.

## <a name="see-related-training-at-microsoft-learn"></a>Se relateret oplæring på [Microsoft Learn](/learn/modules/manage-sales-prices-dynamics-365-business-central/index)

## <a name="see-also"></a>Se også

[Konfigurere salg](sales-setup-sales.md)  
[Salg](sales-manage-sales.md)  
[Arbejde med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]