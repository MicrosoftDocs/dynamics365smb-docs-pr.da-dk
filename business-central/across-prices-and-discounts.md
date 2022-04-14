---
title: Konfigurere priser og rabatter
description: Beskriver, hvordan du definerer standard- specialpris- og rabataftaler for salg og køb.
author: brentholtorf
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: price, pricing, discount, discounting, rebate, sale, purchase, invoice
ms.search.form: 459, 460, 7001, 7011, 7015, 7016, 7017, 7018
ms.date: 04/01/2021
ms.author: bholtorf
ms.openlocfilehash: c4ea2854ccc287b95c42bf942389d4dbfb2fd2e3
ms.sourcegitcommit: 8a12074b170a14d98ab7ffdad77d66aed64e5783
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 03/31/2022
ms.locfileid: "8523601"
---
# <a name="set-up-prices-and-discounts"></a>Konfigurere priser og rabatter
> [!NOTE]
> I 2020 udgivelsesbølge 2 har vi udgivet strømlinede processer til opsætning og administration af priser og rabatter. Hvis du er ny kunde, der bruger den version, bruger du den nye oplevelse. Hvis du allerede bruger den nye oplevelse, afhænger det af, om din administrator har aktiveret funktionsopdateringen **Ny vareprissætningsopdatering** på siden **Funktionsadministration**. Du kan finde flere oplysninger i [Aktivere Upcoming Features Ahead of Time](/dynamics365/business-central/dev-itpro/administration/feature-management).

Pris-og rabatstrategier for køb og salg af varer og tjenester er grundlæggende værktøjer til virksomheder med succes. Når du har defineret de varer og servicer, som din virksomhed køber og sælger, kan du definere, hvad du betaler eller debiterer den, og beløbene vil automatisk blive føjet til salgs- og købsdokumenter. 

## <a name="setting-up-prices-and-discounts"></a>Konfigurere priser og rabatter
Før du opretter prislister, skal du definere dine pris-og rabat strategier på siderne **Salgsopsætning** og **Købsopsætning**.

Du kan konfigurere og bruge to typer salgsrabat:

| Rabattype | Description |
| --- | --- |
| **Linjerabat** |Et rabatbeløb, der er givet på linjer i salgs- og købsdokumenter. Linjerabatter er typisk baseret på en kombination af debitor, vare, minimumsantal, enhed eller periode, som du definerer for salg og køb på siderne **Salgsopsætning** og **Købsopsætning**.|
| **Fakturarabat** |En procentvis rabat, der fratrækkes fra dokumenttotalen for salg og køb, hvis værdibeløbet for alle linjer i dokumentet overstiger et bestemt minimum. |

Da salgspriser og salgslinjerabatter er baseret på en kombination af vare og debitor, kan du også udføre denne konfiguration fra varesiden for den vare, som reglerne og værdierne gælder for.

> [!TIP]  
> Hvis du ikke ønsker, at en vare nogensinde skal sælges med rabat, kan du lade rabatfelterne på varekortet være tomme, og medtag ikke varen i nogen opsætningen af linjerabat.

## <a name="about-price-lists"></a>Om prislister
Prislister er fleksible og giver dig mulighed for at angive den samarbejdspartner eller-aktivitet, som de gælder for. Du kan f.eks. oprette en prisliste, der gælder for alle kreditorer og debitorer, eller tilbyde special priser eller rabatter for hver forretningspartner, eventuelt baseret på et minimumantal på købs- eller salgsordrer eller en bestemt kombination af debitor, vare, minimumsantal, enhed eller tidsperioder. De priser og rabatter, du definerer, anvendes automatisk på købs- og salgsdokumenter. 

## <a name="set-up-prices"></a>Oprette priser

Disse trin varierer, afhængigt af, om din administrator har slået funktionsopdateringen **Ny vareprissætningsopdatering** til. 

#### <a name="current-experience"></a>[Aktuel oplevelse](#tab/current-experience)  

1. Vælg ![Lightbulb, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **Kunder**, og vælg derefter det relaterede link.
2. Vælg debitor, og vælg derefter handlingen **Priser**.
3. Udfyld felterne på linjen efter behov. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)] Udfyld en linje for hver kombination, som yder en særlig salgspris til kunden.

#### <a name="new-experience"></a>[Ny oplevelse](#tab/new-experience)  
Du kan tilføje varer og tjenester manuelt for hver linje, eller du kan bruge handlingen **Foreslå linjer** til at oprette nye priser for udvalgte varer, varerabatgrupper, ressourcer og andre produkttyper. Hvis du vælger **Foreslå linjer**, på siden **Prislinjer - Opret ny**, kan du bruge filtre til at vælge de varer eller tjenester, der skal medtages på prislisten. Du kan også angive, om der skal tages højde for et minimumantal ved beregning af priser, den reguleringsfaktor, der skal gælde for nye prisliste linjer, og den afrundingsmetode, der skal anvendes for priser. 

Som standard er status for nye prislister **Kladde**. Når du er klar til at begynde at bruge listen, kan du ændre status til **Aktiv**.

Hvis du vil have vist prislister og priser, der gælder for bestemte debitorer eller kreditorer, skal du på siderne **Kunde** eller **Kreditor** enten vælge **Salgsprislister** eller **Købsprislister**. Du kan få vist prislistelinjer for varer og ressourcer ved at vælge **Salgspriser** eller **Købspriser** på siderne **Vare** og **Ressource**.

1. Vælg ![Lightbulb, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **Kunder**, og vælg derefter det relaterede link.
2. Vælg debitor, og vælg derefter handlingen **Salgsprislister**. 
3. Vælg **Ny** for at oprette en ny salgsprisliste.
4. Udfyld felterne efter behov i oversigtspanelerne **Generelt** og **Skat**. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
5. Benyt en af følgende fremgangsmåder for at føje elementer til listen:
   * Hvis du vil tilføje mange varer, skal du vælge **Foreslå linjer** og derefter angive filterkriterier for at angive, hvilke varetyper der skal tilføjes. Du kan også vælge at angive yderligere indstillinger for de varer, der er specifikke for prislisten. Om nødvendigt kan du ændre den.
   * Hvis du vil kopiere varer fra en anden prisliste, skal du vælge **Kopier linjer** og derefter vælge den prisliste, der skal kopieres.
   * Hvis du vil tilføje varer manuelt, skal du i feltet **Produkttype** vælge den produkttype, som prislisten vedrører. Afhængig af dine valg skal du udfylde de resterende felter efter behov. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
6. Hvis du vil begynde at bruge prislisten, skal du vælge **Aktiv** i feltet **Status**.  

---

## <a name="to-set-up-a-sales-line-discount-for-a-customer"></a>Sådan konfigureres salgslinjerabatter for en debitor
Disse trin varierer, afhængigt af, om din administrator har slået funktionsopdateringen **Ny vareprissætningsopdatering** til. 

#### <a name="current-experience"></a>[Aktuel oplevelse](#tab/current-experience/)  

1. Vælg ![Lightbulb, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **Kunder**, og vælg derefter det relaterede link.
2. Åbn det relevante debitorkort, og vælg derefter handlingen **Linjerabatter**.
3. Udfyld felterne på linjen efter behov. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)] Udfyld en linje for hver kombination, som yder en salgslinjerabat til kunden.

> [!Note]
> Når du åbner siderne **Salgspriser** og **Salgslinjerabatter** fra en bestemt kunde, er felterne **Salgstypefilter** og **Salgskodefilter** angivet for debitoren og kan ikke ændres eller fjernes.
>
> Hvis du vil oprette priser eller linjerabatter for alle debitorer, en debitorprisgruppe eller en kampagne, skal du åbne siderne fra et varekort. Du kan alternativt bruge siden **Salgspriskladde** til salgspriser. Du kan finde flere oplysninger [Sådan masseopdateres varepriser](sales-how-record-sales-price-discount-payment-agreements.md#to-bulk-update-item-prices).  

#### <a name="new-experience"></a>[Ny oplevelse](#tab/new-experience/)  

1. Vælg ![Lightbulb, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **Kunder**, og vælg derefter det relaterede link.
2. Vælg debitor, og vælg derefter handlingen **Salgsprislister**.
3. Åbn den prisliste, som du vil angive linjerabat for.
4. Slå linjen **Tillad linjerabat** til/fra.
5. Opret en ny linje, eller vælg en eksisterende linje, og udfyld derefter felterne efter behov. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
6. I feltet **Definer** skal du vælge enten **Pris og rabat** eller kun **Rabat**. 
7. I feltet **Linjerabat i procent** specificeres i rabatprocenten.

   > [!TIP]
   > Hvis du redigerer en eksisterende linje, kan du filtrere linjerne ved at vælge den relevante indstilling i feltet **Vis kolonner for**.

---

## <a name="work-with-invoice-discounts-and-service-charges"></a>Arbejde med fakturarabatter og servicegebyrer
Når du bruger fakturarabatter, bestemmer fakturabeløbet størrelsen af rabatten. På siden **Fakturarabatter** kan du også tilføje et servicegebyr til fakturaer over en vis størrelse.  <!--The Invoice Discounts page is hard to find.-->

Du skal angive nogle oplysninger i programmet, før du kan bruge fakturarabatter i forbindelse med salg. Du skal beslutte, hvilke debitorer der skal tildeles denne type rabat, og de rabatprocenter, du vil bruge.  

Hvis dine fakturarabatter skal beregnes automatisk, kan du angive dette på siden **Salgsopsætning**.  

Du kan angive for hver kunde, om du til yde fakturarabat, hvis betingelserne er opfyldt, dvs. hvis fakturabeløbet er stort nok. Du kan definere, at betingelserne for fakturarabatten er DKK for danske debitorer og udenlandsk valuta for udenlandske debitorer.  

Du kan knytte rabatter til bestemte fakturabeløb på siden **Fakturarabatter**. Du kan angive så mange procentsatser, du har brug for. Hver debitor kan have sin egen side, eller du kan sammenkæde flere debitorer på den samme side.  

Du kan også knytte et servicegebyr til et bestemt fakturabeløb i tillæg til eller i stedet for rabatprocenten.  

> [!TIP]  
> Før du begynder at indtaste disse oplysninger, er det en god idé at forberede rabatstrukturen på forhånd, så det er nemmere at se, hvilke kunder der skal have forbindelse til den samme fakturarabatside. Du finder flere oplysninger om rabatter under [Konfigurere rabatter for dine kunder](/learn/modules/customer-discounts-dynamics-365-business-central/index) på Microsoft Learn.  

### <a name="to-set-up-an-invoice-discount-for-a-customer"></a>Sådan oprettes en fakturarabat for en debitor
Når du har besluttet, hvilke kunder der skal have fakturarabatter, skal du angive fakturarabatkoden på debitorkortene og definere betingelserne for hver kode.

1. Vælg ![Lightbulb, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **Kunder**, og vælg derefter det relaterede link.
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

Fakturarabatten er nu oprettet og knyttet til den pågældende debitor. Når du vælger debitorkoden i feltet **Fakturarabatkode** på andre debitorkort, knyttes samme fakturarabat til den pågældende debitor.

## <a name="to-copy-sales-prices"></a>Sådan kopieres salgspriser
Disse trin varierer, afhængigt af, om din administrator har slået funktionsopdateringen **Ny vareprissætningsopdatering** til. 

#### <a name="current-experience"></a>[Aktuel oplevelse](#tab/current-experience/)  

Hvis du vil kopiere en salgspris, f.eks. en individuel kundes salgspriser til brug for en debitorprisgruppe, skal du køre **Forslå salgspris på kladde.** batch-jobbet på siden **Salgspriskladde**.  

1. Vælg ![Lightbulb, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **Salgspriskladdeside**, og vælg derefter det relaterede link.  
2. Vælg handlingen **Foreslå salgspris på kld.** .  
3. Udfyld felterne **Salgstype** og **Salgskode** i oversigtspanelet **Salgspriser** med de oprindelige salgspriser, du vil kopiere.  
4. Udfyld felterne **Salgstype** og **Salgskode** i den øverste del af siden med den type og det navn, du vil have salgspriserne kopieret til.  
5. Hvis kørslen skal oprette nye priser, skal du markere afkrydsningsfeltet **Opret nye priser**.  
6. Vælg knappen **OK** for at udfylde linjerne på siden **Salgspriskladde** med de foreslåede nye priser for at angive, at de er gyldige for den valgte salgstype.  

   > [!NOTE]  
   > Kørslen betyder kun, at der udformes forslag, ikke, at ændringerne bliver gennemført. Hvis du er tilfreds med forslagene, og du vil implementere dem, dvs. indsætte dem på siden **Salgspriser**, skal du vælge handlingen **Implementer prisændringer** på siden **Salgspriskladde**.

#### <a name="new-experience"></a>[Ny oplevelse](#tab/new-experience/)  

Status for prislistelinjen skal være **Kladde**. 

1. Vælg ![Lightbulb, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **Salgsprislister**, og vælg derefter det relaterede link. 
2. Vælg den prisliste, du vil kopiere, og vælg derefter **Kopier linjer**.
3. Udfyld felterne efter behov. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

   > [!NOTE]
   > Du kan ikke have to linjer, der har samme indstillinger, men forskellige priser. Hvis det sker, vises en meddelelse, når du aktiverer en prisliste. Du kan vælge den pris, der skal bruges, ved at åbne listen og slette den forkerte pris.  
  
---

## <a name="to-bulk-update-item-prices"></a>Sådan masseopdateres varepriser
Disse trin varierer, afhængigt af, om din administrator har slået funktionsopdateringen **Ny vareprissætningsopdatering** til. 

#### <a name="current-experience"></a>[Aktuel oplevelse](#tab/current-experience/)

Hvis du vil masseopdatere varepriser, f.eks. forøge alle varepriser med en procentsats, skal du køre **Foreslå varepris på kladde.** kørsel. Du kan finde et link til kørslen på siden **Salgspriskladde**.  

1. Vælg ![Lightbulb, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **Salgspriskladdeside**, og vælg derefter det relaterede link.  
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

## <a name="calculating-the-best-price"></a>Beregne bedste pris
Når du har registreret særpriser og linjerabatter for salg og køb, sørger [!INCLUDE[d365fin](includes/d365fin_md.md)] for, at dine avance på varehandel altid er optimal ved automatisk at beregne den bedste pris på salgs- og købsdokumenter og på sags- og varekladdelinjer. Du kan finde flere oplysninger i [Beregne bedste pris](sales-how-record-sales-price-discount-payment-agreements.md#best-price-calculation).

## <a name="see-also"></a>Se også
[Konfigurere salg](sales-setup-sales.md)  
[Salg](sales-manage-sales.md)  
[Arbejd med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)
