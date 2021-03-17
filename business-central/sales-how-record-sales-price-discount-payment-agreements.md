---
title: Konfigurere særlige salgspriser og rabatter for kunder | Microsoft Docs
description: Beskriver, hvordan du definerer de alternative pris- og rabataftaler, som du vil anvende på salgsdokumenter, når du sælger til forskellige kunder.
author: bholtorf
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: special price, alternate price, pricing
ms.date: 01/22/2021
ms.author: bholtorf
ms.openlocfilehash: 27c0674ef3bbb611f965fb32d3a9f264d080127a
ms.sourcegitcommit: a9b771cc2b4b75aed835efca63ef7a6a44219d59
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 02/18/2021
ms.locfileid: "5476791"
---
# <a name="record-special-sales-prices-and-discounts"></a>Registrere specialsalgspriser og -rabatter
> [!NOTE]
> I 2020 udgivelsesbølge 2 har vi udgivet strømlinede processer til opsætning og administration af priser og rabatter. Hvis du er ny kunde, der bruger den version, bruger du den nye oplevelse. Hvis du allerede bruger den nye oplevelse, afhænger det af, om din administrator har aktiveret funktionsopdateringen **Ny vareprissætningsopdatering** i **Funktionsadministration**. Du kan finde flere oplysninger i [Aktivere Upcoming Features Ahead of Time](/dynamics365/business-central/dev-itpro/administration/feature-management).

De pris- og rabataftaler, der gælder ved salg til forskellige debitorer, skal defineres, så de aftalte regler og værdier anvendes i salgsdokumenterne.

Når du har registreret særpriser og linjerabatter for salg og køb, sørger [!INCLUDE[prod_short](includes/prod_short.md)] for, at dine avance på varehandel altid er optimal ved automatisk at beregne den bedste pris på salgs- og købsdokumenter og på sags- og varekladdelinjer. Du kan finde flere oplysninger under [Beregne bedste pris](sales-how-record-sales-price-discount-payment-agreements.md#best-price-calculation).

Med hensyn til priser kan du få en særlig salgspris indsat på salgslinjerne, hvis en bestemt kombination af kunde, vare, minimumantal, enhed eller start-/slutdato findes. Du kan finde flere oplysninger i sektionerne [Sådan konfigureres salgspriser til en debitor](#to-set-up-a-sales-price-for-a-customer)og [Bedste prisberegning](#best-price-calculation).  

Med hensyn til rabatter kan du oprette og bruge to typer salgsrabat:

| Rabattype | Beskrivelse |
| --- | --- |
| **Salgslinjerabat** |En beløbsrabat, der indsættes på salgslinjerne, hvis en bestemt kombination af kunde, vare, minimumsantal, enhed eller start-/slutdato findes. Dette fungerer på samme måde som for salgspriser. |
| **Fakturarabat** |En procentvis rabat, der fratrækkes fra salgsdokumenttotalen for salg og køb, hvis værdibeløbet for alle linjer i dokumentet overstiger et bestemt minimum. |

Da salgspriser og salgslinjerabatter er baseret på en kombination af vare og debitor, kan du også udføre denne konfiguration fra varesiden for den vare, som reglerne og værdierne gælder for.

> [!TIP]  
> Hvis du ikke ønsker, at en vare nogensinde skal sælges med rabat, kan du lade rabatfelterne på varekortet være tomme, og medtag ikke varen i nogen opsætningen af linjerabat.

Felterne **Gælder for type** og **Gælder for nr.** felterne, hvor du kan vælge, hvad denne prisliste skal gælde for, f. eks. debitor eller debitorprisgruppe. Du kan bruge **Vis kolonner til** for at vise eller skjule kolonner, der er relevante for priser, rabatter eller priser og rabatter.

Du kan konfigurere prislister manuelt, eller du kan bruge handlingen **Foreslå linjer** til at oprette nye priser for udvalgte varer, varerabatgrupper, ressourcer og andre produkttyper. Hvis du vælger Foreslå linjer, kan du oprette filtre for at vælge produkter, som du vil oprette nye prisliste linjer til, på siden Opret pris linjer. Du kan også angive, om der skal tages højde for et minimumantal ved beregning af priser, den reguleringsfaktor, der skal gælde for nye prisliste linjer, og den afrundingsmetode, der skal anvendes for priser. med handlingen **Kopier linjer** kan du kopiere eksisterende prisliste linjer mellem prislister.

Som standard er status for nye prislister Kladde. Når du er færdig med at tilføje linjer, og du vil have prisberegningsprogrammet til at omfatte den, kan du ændre status til aktiv.

Hvis du vil have vist prislister og priser, der gælder for bestemte debitorer eller kreditorer, skal du på siden **Kunde** vælge **Salgsprisliste** eller på siden **Kreditor** vælge **Købsprislister**. Du kan få vist prislistelinjer i forskellige prislister ved at vælge **Salgspriser** eller **Købspriser** fra siderne **Vare** og **Ressource**.

## <a name="to-set-up-a-sales-price-for-a-customer"></a>Sådan konfigureres salgspriser for en debitor

Disse trin varierer, afhængigt af, om din administrator har slået funktionsopdateringen **Ny vareprissætningsopdatering** til.  

#### <a name="current-experience"></a>[Aktuel oplevelse](#tab/current-experience/)

1. Vælg ikonet ![Elpære, der åbner funktionen Fortæl mig](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig"), angiv **Debitorer**, og vælg derefter det relaterede link.
2. Vælg debitor, og vælg derefter handlingen **Priser**.
3. Udfyld felterne på linjen efter behov. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)] Udfyld en linje for hver kombination, som yder en særlig salgspris til kunden.

#### <a name="new-experience"></a>[Ny oplevelse](#tab/new-experience/)  

1. Vælg ikonet ![Elpære, der åbner funktionen Fortæl mig](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig"), angiv **Kunder**, og vælg derefter det relaterede link.
2. Vælg debitor, og vælg derefter handlingen **Salgsprislister**. 
3. Vælg **Ny** for at oprette en ny salgsprisliste.
4. Udfyld felterne efter behov i oversigtspanelerne **Generelt** og **Skat**. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
5. Benyt en af følgende fremgangsmåder for at føje elementer til listen:
   * Hvis du vil tilføje mange varer, skal du vælge **Foreslå linjer** og derefter angive filterkriterier for at angive, hvilke varetyper der skal tilføjes. Du kan også vælge at angive yderligere indstillinger for de varer, der er specifikke for prislisten. Om nødvendigt kan du ændre den.
   * Hvis du vil kopiere varer fra en anden prisliste, skal du vælge **Kopier linjer** og derefter vælge den prisliste, der skal kopieres.
   * Hvis du vil tilføje varer manuelt i gitteret, skal du i feltet **Produkttype** vælge den produkttype, som prislisten vedrører. Afhængig af dine valg skal du udfylde de resterende felter efter behov. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
6. Hvis du vil begynde at bruge prislisten, skal du vælge **Aktiv** i feltet **Status**.  

---

## <a name="sales-invoice-discounts-and-service-charges"></a>Salgsfakturarabatter og servicegebyrer
Når du bruger fakturarabatter, bestemmer det samlede fakturabeløb størrelsen af rabatten. På siden **Deb./fakt.rabatter** kan du også føje et servicegebyr til fakturaer over en vis størrelse.  

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

### <a name="calculating-invoice-discounts-on-sales"></a>Beregne fakturarabatter på salg

[!INCLUDE [sales-invoice-discounts](includes/sales-invoice-discounts.md)]

## <a name="to-set-up-a-sales-line-discount-for-a-customer"></a>Sådan konfigureres salgslinjerabatter for en debitor
Disse trin varierer, afhængigt af, om din administrator har slået funktionsopdateringen **Ny vareprissætningsopdatering** til. 

#### <a name="current-experience"></a>[Aktuel oplevelse](#tab/current-experience/)  

1. Vælg ikonet ![Elpære, der åbner funktionen Fortæl mig](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig"), angiv **Kunder**, og vælg derefter det relaterede link.
2. Åbn det relevante debitorkort, og vælg derefter handlingen **Linjerabatter**.
3. Udfyld felterne på linjen efter behov. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)] Udfyld en linje for hver kombination, som yder en salgslinjerabat til kunden.

> [!Note]
> Når du åbner siderne **Salgspriser** og **Salgslinjerabatter** fra en bestemt kunde, er felterne **Salgstypefilter** og **Salgskodefilter** angivet for debitoren og kan ikke ændres eller fjernes.
>
> Hvis du vil oprette priser eller linjerabatter for alle debitorer, en debitorprisgruppe eller en kampagne, skal du åbne siderne fra et varekort. Du kan alternativt bruge siden **Salgspriskladde** til salgspriser. Du kan finde flere oplysninger [Sådan masseopdateres varepriser](sales-how-record-sales-price-discount-payment-agreements.md#to-bulk-update-item-prices).  

#### <a name="new-experience"></a>[Ny oplevelse](#tab/new-experience/)  

1. Vælg ikonet ![Elpære, der åbner funktionen Fortæl mig](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig"), angiv **Debitorer**, og vælg derefter det relaterede link.
2. Vælg debitor, og vælg derefter handlingen **Salgsprislister**.
3. Åbn den prisliste, som du vil angive linjerabat for.
4. Slå linjen **Tillad linjerabat** til/fra.
5. Opret en ny linje, eller vælg en eksisterende linje, og udfyld derefter felterne efter behov. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
6. I feltet **Definer** skal du vælge enten **Pris og rabat** eller kun **Rabat**. 
7. I feltet **Linjerabat i procent** specificeres i rabatprocenten.

    > [!TIP]
    > Hvis du redigerer en eksisterende linje, kan du filtrere linjerne ved at vælge den relevante indstilling i feltet **Vis kolonner for**.

    > [!NOTE]  
    > Fakturarabatkoder repræsenteres af eksisterende debitorkort. Det gør det muligt hurtigt at tildele betingelserne for fakturarabatten til debitorer ved at vælge navnet på en anden debitor, der skal have samme betingelser. Hvis du vil oprette debitorspecifikke fakturarabatbetingelser, skal du angive feltet **Fakturarabatkode** til debitorens debitorkode og derefter fortsætte til næste trin.

8. På siden **Debitorkort** skal du vælge handlingen **Fakturarabatter**. Siden **Deb./fakt.-rabatter** åbnes.
9. Angiv koden for den valuta, som fakturarabatbetingelserne på linjen gælder for, i feltet **Valutakode**. Lad feltet stå tomt for at angive fakturarabatbetingelser for DKK.
10. Alternativt kan du angive det minimumsbeløb, der berettiger til rabatten, i feltet **Min. beløb**.
11. I feltet **Rabatpct.** skal du angive fakturarabatten som en procentdel af fakturabeløbet.
12. Gentag trin 5-7 for hver valuta, som debitoren får en personlig fakturarabat for.

Fakturarabatten er nu oprettet og knyttet til debitor. Når du vælger debitorkoden i feltet **Fakturarabatkode** på andre debitorkort, knyttes samme fakturarabat til den pågældende debitor.

---

## <a name="to-set-up-an-invoice-discount-for-a-customer"></a>Sådan oprettes en fakturarabat for en debitor
Når du har besluttet, hvilke kunder der skal have fakturarabatter, skal du angive fakturarabatkoden på debitorkortene og definere betingelserne for hver kode.

1. Vælg ikonet ![Elpære, der åbner funktionen Fortæl mig](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig"), angiv **Debitorer**, og vælg derefter det relaterede link.
2. Åbn debitorkortsiden for en debitor, der kan ydes fakturarabat til.
3. Vælg en kode i feltet **Fakturarabatkode** for de fakturarabatbetingelser, som skal bruges til automatisk beregning af fakturarabat til debitoren. <!--Looks like I can only choose customers in this list-->

> [!NOTE]  
> Fakturarabatkoder repræsenteres af eksisterende debitorkort. Det gør det muligt hurtigt at tildele betingelserne for fakturarabatten til debitorer ved at vælge navnet på en anden debitor, der skal have samme betingelser.

Fortsæt med at angive nye fakturarabatbetingelser for salg.

1. På siden **Kunder** skal du vælge handlingen **Fakturarabatter**. Siden **Deb./fakt.-rabatter** åbnes.
2. Angiv koden for den valuta, som fakturarabatbetingelserne på linjen gælder for, i feltet **Valutakode**. Lad feltet stå tomt for at angive fakturarabatbetingelser for DKK.
3. Angiv det minimumsbeløb, der berettiger til rabatten, i feltet **Min. beløb**.
4. I feltet **Rabatpct.** skal du angive fakturarabatten som en procentdel af fakturabeløbet.
5. Gentag trin 5-7 for hver valuta, som debitoren får en personlig fakturarabat for.

## <a name="to-copy-sales-prices"></a>Sådan kopieres salgspriser
Disse trin varierer, afhængigt af, om din administrator har slået funktionsopdateringen **Ny vareprissætningsopdatering** til. 

#### <a name="current-experience"></a>[Aktuel oplevelse](#tab/current-experience/)  

Hvis du vil kopiere en salgspris, f.eks. en individuel kundes salgspriser til brug for en debitorprisgruppe, skal du køre **Forslå salgspris på kladde.** batch-jobbet på siden **Salgspriskladde**.  

1. Vælg ikonet ![Elpære, der åbner funktionen Fortæl mig](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig"), angiv **Salgspriskladde**, og vælg derefter det relaterede link.  
2. Vælg handlingen **Foreslå salgspris på kld.** .  
3. Udfyld felterne **Salgstype** og **Salgskode** i oversigtspanelet **Salgspriser** med de oprindelige salgspriser, du vil kopiere.  
4. Udfyld felterne **Salgstype** og **Salgskode** i den øverste del af siden med den type og det navn, du vil have salgspriserne kopieret til.  
5. Hvis kørslen skal oprette nye priser, skal du markere afkrydsningsfeltet **Opret nye priser**.  
6. Vælg knappen **OK** for at udfylde linjerne på siden **Salgspriskladde** med de foreslåede nye priser for at angive, at de er gyldige for den valgte salgstype.  

   > [!NOTE]  
   > Kørslen betyder kun, at der udformes forslag, ikke, at ændringerne bliver gennemført. Hvis du er tilfreds med forslagene, og du vil implementere dem, dvs. indsætte dem på siden **Salgspriser**, skal du vælge handlingen **Implementer prisændringer** på siden **Salgspriskladde**.

#### <a name="new-experience"></a>[Ny oplevelse](#tab/new-experience/)  

Status for prislistelinjen skal være **Kladde**. 

1. Vælg ikonet ![Elpære, der åbner funktionen Fortæl mig](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig"), angiv **Salgsprislister**, og vælg derefter det relaterede link. 
2. Vælg den prisliste, du vil kopiere, og vælg derefter **Kopier linjer**.
3. Udfyld felterne efter behov. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

   > [!NOTE]
   > Du kan ikke have to linjer, der har samme indstillinger, men forskellige priser. Hvis det sker, vises en meddelelse, når du aktiverer en prisliste. Du kan vælge den pris, der skal bruges, ved at åbne listen og slette den forkerte pris.  
  
---

## <a name="to-bulk-update-item-prices"></a>Sådan masseopdateres varepriser
Disse trin varierer, afhængigt af, om din administrator har slået funktionsopdateringen **Ny vareprissætningsopdatering** til. 

#### <a name="current-experience"></a>[Aktuel oplevelse](#tab/current-experience/)

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

#### <a name="new-experience"></a>[Ny oplevelse](#tab/new-experience/)

Hvis du vil opdatere priser for flere varer, skal du oprette en ny prisliste og derefter kopiere linjerne fra en eksisterende prisliste. Når du kopierer linjer, kan du angive, hvad der skal kopieres, og du kan angive et heltal eller decimaltal i feltet **Ganges med** for at øge eller reducere priserne. Status for prisliste skal være **Kladde**. Hvis det er nødvendigt, kan du deaktivere den gamle prisliste.

> [!NOTE]
> Du kan ikke have to linjer, der har samme indstillinger, men forskellige priser. Hvis det sker, vises en meddelelse, når du aktiverer en prisliste. Du kan vælge den pris, der skal bruges, ved at åbne listen og slette den forkerte pris.  

---

## <a name="best-price-calculation"></a>Beregning af bedste pris
Når du har registreret særpriser og linjerabatter for salg og køb, sørger [!INCLUDE[d365fin](includes/d365fin_md.md)] for, at dine avance på varehandel altid er optimal ved automatisk at beregne den bedste pris på salgs- og købsdokumenter og på sags- og varekladdelinjer.

Den bedste pris er den lavest tilladte pris med den størst tilladte linjerabat på en givet dato. [!INCLUDE[d365fin](includes/d365fin_md.md)] beregner automatisk dette, når enhedsprisen og linjerabatprocenten for varer indsættes på nye dokument- og kladdelinjer.

> [!NOTE]  
> I det følgende beskrives, hvordan den bedste pris beregnes for salg. Beregningen er den samme for køb.

1. [!INCLUDE[d365fin](includes/d365fin_md.md)] kontrollerer kombinationen af faktureringsdebitoren og varen automatisk og beregner derefter den relevante enhedspris og linjerabatprocent ud fra følgende kriterier:

    - Har denne kunde en pris-/rabataftale, eller tilhører kunden en gruppe, der har en sådan aftale?
    - Er varen eller varerabatgruppen på linjen medtaget i nogen af disse pris/rabataftaler?
    - Ligger ordredatoen (bogføringsdatoen for faktura- eller kreditnotaen) inden for start- og slutdatoen for pris-/rabataftalen?
    - Er enhedskoden angivet? Hvis den gør det, kontrollerer [!INCLUDE[d365fin](includes/d365fin_md.md)], om der er priser/rabatter med samme enhedskode, og om der er priser/rabatter, uden at der er tilknyttet en enhedskode.

2. [!INCLUDE[d365fin](includes/d365fin_md.md)] kontrollerer, om der ligger pris-/ rabataftaler i oplysningerne om dokument- eller kladdelinjen og indsætter derefter den relevante enhedspris og linjerabatprocent ud fra følgende kriterier:

    - Er der et krav om et mindste antal i pris-/ rabataftalen, som er opfyldt?
    - Er der et krav om valuta i pris-/ rabataftalen, som er opfyldt? Hvis der er det, indsættes den laveste pris og den højeste linjerabat for valutaen, selvom den lokale valuta giver en bedre pris. Hvis der ikke er nogen pris-/rabataftale for den angivne valutakode, indsætter [!INCLUDE[d365fin](includes/d365fin_md.md)] den laveste pris og den højeste linjerabat i din lokale valuta.

Hvis der ikke kan beregnes en særpris for varen på linjen, indsættes seneste indirekte omkostning eller enhedsprisen fra varekortet.

## <a name="see-related-training-at-microsoft-learn"></a>Se relateret oplæring på [Microsoft Learn](/learn/modules/manage-sales-prices-dynamics-365-business-central/index)

## <a name="see-also"></a>Se også

[Konfigurere salg](sales-setup-sales.md)  
[Salg](sales-manage-sales.md)  
[Arbejde med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]