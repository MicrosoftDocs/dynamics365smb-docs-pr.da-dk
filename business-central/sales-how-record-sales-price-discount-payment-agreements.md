---
title: Registrere specialsalgspriser og -rabatter
description: Beskriver, hvordan du definerer pris-og rabataftaler for salgsdokumenter.
author: bholtorf
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: special price, alternate price, pricing
ms.search.form: 7022, 7024
ms.date: 06/03/2022
ms.author: bholtorf
ms.openlocfilehash: 5560a9a1b5c5eb031136a7c1320019eac75239e0
ms.sourcegitcommit: a9c778b65925435a4099fad45b3611f310e0b203
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 10/12/2022
ms.locfileid: "9652187"
---
# <a name="record-special-sales-prices-and-discounts"></a>Registrere specialsalgspriser og -rabatter

> [!NOTE]
> I 2020 udgivelsesbølge 2 har vi introduceret nye, strømlinede processer til opsætning og administration af priser og rabatter. Hvis du er ny kunde, der bruger den nyeste version, bruger du den nye oplevelse. Hvis du allerede bruger den nye oplevelse, afhænger det af, om din administrator har aktiveret funktionsopdateringen **Ny vareprissætningsopdatering** i **Funktionsadministration**. Flere oplysninger i [Aktivering af Ahead og Time-funktioner](/dynamics365/business-central/dev-itpro/administration/feature-management) i administrationsindholdet.

[!INCLUDE[prod_short](includes/prod_short.md)] understøtter forskellige pris strategier, f. eks.:

* Én-pris-til-alle modeller, hvor en vare altid sælges til samme pris.
* Specielle prisaftaler med specifikke kunder eller grupper af kunder.
* Kampagner når et salg lever op til kriterier for et særtilbud. F. eks. kan kriterier være, når en ordre overholder et minimumantal, ligger før en bestemt dato eller omfatter en bestemt type vare.  

Hvis du vil bruge en grundlæggende prissætningsmodel, skal du kun angive en salgspris for en vare eller ressource. Prisen vil altid blive brugt i salgsdokumenter. Hvis du f. eks. kører en salgskampagne og vil tilbyde specielle priser for en salgskampagne, kan du for eksempelvis angive kriterier for det på siden **salgspriser**. Du kan tilbyde specielle priser baseret på en kombination af følgende oplysninger:  

* Debitor
* Vare
* Måleenhed
* Min. antal
* Datoer, der definerer den periode, som priserne gælder for.

Når du har konfigurere specielle priser, kan [!INCLUDE[prod_short](includes/prod_short.md)] beregne den bedste pris på salgs-og købsdokumenter og på sags-og varekladdelinjer. Flere oplysninger i [Bedste prisberegning](sales-how-record-sales-price-discount-payment-agreements.md#best-price-calculation).

Du kan konfigurere to typer til salgsrabat:

| Rabattype | Beskrivlse |
| --- | --- |
| **Salgslinjerabat** |Et beløb, der indsættes på salgslinjer, hvis de indeholder en bestemt kombination af kunde, vare, minimumsantal, enhed eller start-/slutdato findes. Dette fungerer på samme måde som for salgspriser. |
| **Fakturarabat** |En procentvis rabat, der fratrækkes fra salgsdokumenttotalen for salg og køb, hvis værdibeløbet for alle linjer i dokumentet overstiger et bestemt minimum. |

> [!TIP]  
> Hvis du ikke ønsker, at en vare nogensinde skal sælges med rabat, kan du lade rabatfelterne på varekortet være tomme, og medtag ikke varen i nogen opsætningen af linjerabat.

## <a name="to-set-up-a-sales-price-for-a-customer"></a>Sådan konfigureres salgspriser for en debitor

Disse trin varierer, afhængigt af, om din administrator har slået funktionsopdateringen **Ny vareprissætningsopdatering** til. Hvis funktionsopdateringen ikke er aktiveret, skal du følge fremgangsmåden under fanen Aktuel oplevelse. 

#### <a name="current-experience"></a>[Aktuel oplevelse](#tab/current-experience/)

1. Vælg ikonet ![Elpære, der åbner funktionen Fortæl mig](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig"), angiv **Debitorer**, og vælg derefter det relaterede link.
2. Vælg debitor, og vælg derefter handlingen **Priser**.
3. Udfyld felterne på linjen efter behov. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)] Udfyld en linje for hver kombination, som yder en særlig salgspris til kunden.

#### <a name="new-experience"></a>[Ny oplevelse](#tab/new-experience/)  

Som standard er status for nye prislister **Kladde**. Kladdeprislister medtages ikke i prisberegninger. Når du er færdig med at tilføje linjer, og du vil starte med at bruge priserne, kan du ændre status til **Aktiv**.

1. Vælg ikonet ![Elpære, der åbner funktionen Fortæl mig](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig"), angiv **Kunder**, og vælg derefter det relaterede link.
2. Vælg debitor, og vælg derefter handlingen **Salgsprislister**. 
3. Vælg **Ny** for at oprette en ny salgsprisliste.
4. Udfyld felterne efter behov i oversigtspanelerne **Generelt** og **Skat**. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
5. Benyt en af følgende fremgangsmåder for at føje elementer til listen:
   * Hvis du vil tilføje mange varer, skal du vælge **Foreslå linjer** og derefter angive filterkriterier for at angive, hvilke varetyper der skal tilføjes. Du kan også vælge at angive yderligere indstillinger for de varer, der er specifikke for prislisten. Om nødvendigt kan du ændre disse indstillinger senere.
   * Hvis du vil kopiere varer fra en anden prisliste, skal du vælge **Kopier linjer** og derefter vælge den prisliste, der skal kopieres.
   * Hvis du vil tilføje varer manuelt i gitteret, skal du i feltet **Produkttype** vælge den produkttype, som prislisten vedrører. Afhængig af dine valg skal du udfylde de resterende felter efter behov. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
6. Hvis du vil begynde at bruge prislisten, skal du vælge **Aktiv** i feltet **Status**.  

---

## <a name="using-sales-and-purchase-price-lists"></a>Bruge salgs-og købsprislister

> [!NOTE]
> Hvis du bruger prislister, kræver det, at administratoren har aktiveret funktionsopdatering **Ny salgspriserfaring** i **Funktionsstyring**. Flere oplysninger i [Aktivering af Ahead og Time-funktioner](/dynamics365/business-central/dev-itpro/administration/feature-management) i administrationsindholdet.

De fleste nye salgspriserfaringer svarer til den aktuelle oplevelse, men der er nogle få forskelle. Disse forskelle beskrives i de følgende afsnit.

Felterne **Gælder for type** og **Gælder for nr.** felterne, hvor du kan vælge, hvad en prisliste skal gælde for, f.eks. debitor eller debitorprisgruppe. Du kan bruge **Vis kolonner til** for at vise eller skjule kolonner, der er relevante for priser, rabatter eller priser og rabatter.

### <a name="converting-existing-prices-when-you-turn-on-the-pricing-feature-update"></a>Konvertering af eksisterende priser, når du aktiverer opdatering af prissætningsfunktionen

Når du aktiverer funktionsopdateringen **Ny salgsprisoplevelse** på siden **Funktionsstyring**, åbnes vejledningen **Funktionsopdatering**. Brug **Brug standardpriser** til at skifte mellem følgende:

* Hvis du vil arbejde med alle priser på en enkelt side, skal du aktivere den. Eksisterende priser konverteres til én standardprisliste for hver af følgende dokumenter:

    * Salg
    * Køb
    * Salg af sag
    * Køb af sag

    Du kan redigere alle priser for disse områder på siden **Priskladde**. Standardprislisterne angives i siderne **Konfiguration af salgsopsætning**, **Konfiguration af købsopsætning** og **Sagsopsætning**. 

> [!NOTE]
> Hvis der kun er angivet priser på vare-eller ressourcekort, vil standard prislisterne ikke blive udfyldt med disse priser under dataopdateringen. Du kan dog åbne en af standardprislisterne eller siden **Priskladde** og bruge handlingen **Foreslå linjer** til at tilføje de priser, der er angivet på vare-eller ressourcekortene.

* Hvis du vil bruge salgspris lister, skal du slå den fra. Eksisterende priser konverteres til en ny prisliste for hver af følgende kombinationer af følgende: 

* Kunde (Debitor)
* Debitorgruppe eller kampagne
* Start-og slutdatoer
* Valutaer 

Hvis du har mange kombinationer, har du mange prislister.

Hvis du allerede har aktiveret den nye prissætningsoplevelse, kan du oprette prislister manuelt eller angive en eksisterende prisliste som standard. Hvis du vil angive en eksisterende prisliste som standard, skal du aktivere funktionen **Tillad opdatering af standarder** på prislisten. Standardprislisterne angives på siderne **Konfiguration af salgsopsætning**, **Konfiguration af købsopsætning** eller **Sagsopsætning**.

### <a name="editing-active-price-lists"></a>Redigere aktive prislister

Hvis du vil give brugere tilladelse til at redigere priser på aktive prislister for varer, ressourcer, debitorer, kreditorer eller andre enheder, der bruger priser, skal du aktivere funktionen til/fra til **Tillad redigering af aktiv pris** på siderne **Salgsopsætning** og **Købsopsætning**.

Når funktionen **Tillad redigering af aktiv pris** er deaktiveret, skal du ændre prislistens status til **Kladde**, foretage ændringerne og derefter aktivere prislisten igen, hvis du vil opdatere priser på en prisliste.

Siden **Prisoversigt** indeholder en oversigt over alle priser på prislister. Du kan angive filtre for at begrænse listen over de priser, du kan ændre eller tilføje i. Når du har ændret priserne, skal du bruge handlingen **Kontroller linjer** for at kontrollere priserne mod andre prislistelinjer. Ved at kontrollere priserne undgår du dubletter og flertydighed under prisberegningen.

> [!NOTE]
> Når du redigerer en linje i en aktiv prisliste, bliver linjens status **Kladde**, og linjen vil ikke blive medtaget i prisberegninger, før du bruger handlingen til **Bekræft linjer**. Når du har kontrolleret prisen, bliver linjens status **Aktiv**, og den bruges i prisberegninger.

Hvis du vil tilføje nye priser, skal du bruge handlingen **Tilføj nye linjer** på siden **Prisoversigt**. Siden **Priskladde** åbnes, og du kan tilføje pris linjer enten ved at foreslå dem på basis af kriterier, kopiere dem fra andre prislister eller manuelt angive dem. Derefter kan du bruge handlingen **Implementer prisændring** til at sammenligne de nye priser med andre prislister for at undgå dubletter og flertydighed under prisberegningen.

#### <a name="create-sales-price-lines-based-on-the-unit-price"></a>Oprette salgsprislinjer ud fra salgspris

1. På siden **Pengestrømskladde** skal du vælge handlingen **Foreslå kladdelinjer**.
2. På siden **Prislinjer - Opret ny** skal du udfylde felterne efter behov. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
3. I feltet **produktfilter** skal du angive filtre for den valgte **produkttype**.
4. Vælg feltet **Standarder** for at angive indstillinger som f. eks.:
   * Hvilke enheder prislisten tildeles til.
   * Datoer, hvor prisen er gyldig.
   * Valutakode.
   * Det beløbstypefilter, der definerer de kolonner, som vises i prislistelinjerne.
5. Vælg **OK**. Nye linjer føjes til **priskladde**-siden med de valgte indstillinger og salgspriserne fra varekortene.
6. Rediger de oprettede linjer med de nye salgspriser eller rabatter. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

#### <a name="create-sales-price-lines-based-on-existing-price-lists"></a>Oprette salgsprislinjer ud fra eksisterende prislister

1. På siden **Pengestrømskladde** skal du vælge handlingen **Kopier linjer**.
2. På siden **Prislinjer - kopier eksisterende** skal du vælge en eksisterende prisliste i feltet **Fra prisliste**.
3. Angiv filtre for produkterne på den valgte prisliste i feltet **Prislinjefilter**.
4. Vælg feltet **Standarder** for at angive indstillinger som f. eks.:
   * Hvilke enheder prislisten tildeles til.
   * Datoer, hvor prisen er gyldig.
   * Valutakode.
   * Det beløbstypefilter, der definerer de kolonner, som vises i prislistelinjerne.
5. Udfyld de resterende felter efter behov. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
6. Vælg **OK**. Nye linjer føjes til **Priskladde**-siden med de valgte indstillinger.
7. Rediger de oprettede linjer med de nye salgspriser eller rabatter. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

## <a name="to-copy-sales-prices"></a>Sådan kopieres salgspriser

Disse trin varierer, afhængigt af, om din administrator har slået funktionsopdateringen **Ny vareprissætningsopdatering** til. Hvis funktionsopdateringen ikke er aktiveret, skal du følge fremgangsmåden under fanen Aktuel oplevelse.

#### <a name="current-experience"></a>[Aktuel oplevelse](#tab/current-experience/)  

Hvis du vil kopiere en salgspris, f.eks. en individuel kundes salgspriser til brug for en debitorprisgruppe, skal du køre **Forslå salgspris på kladde.** batch-jobbet på siden **Salgspriskladde**.  

1. Vælg ikonet ![Lightbulb, der åbner funktionen Fortæl mig](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig"), angiv **Salgspriskladde**, og vælg derefter det relaterede link.  
2. Vælg handlingen **Foreslå salgspris på kld.** .  
3. Udfyld felterne **Salgstype** og **Salgskode** i oversigtspanelet **Salgspriser** med de oprindelige salgspriser, du vil kopiere.  
4. Udfyld felterne **Salgstype** og **Salgskode** i den øverste del af siden med den type og det navn, du vil have salgspriserne kopieret til.  
5. Hvis kørslen skal oprette nye priser, skal du markere afkrydsningsfeltet **Opret nye priser**.  
6. Vælg knappen **OK** for at udfylde linjerne på siden **Salgspriskladde** med de foreslåede nye priser for at angive, at de er gyldige for den valgte salgstype.  

   > [!NOTE]  
   > Kørslen betyder kun, at der udformes forslag, ikke, at ændringerne bliver gennemført. Hvis du er tilfreds med forslagene, og du vil implementere dem, dvs. indsætte dem på siden **Salgspriser**, skal du vælge handlingen **Implementer prisændringer** på siden **Salgspriskladde**.

#### <a name="new-experience"></a>[Ny oplevelse](#tab/new-experience/)  

Du kan angive, om den nye prisliste skal bruge indstillingerne fra hovedet på den liste, du kopierer, eller indstillingerne fra den nye liste, du vil kopiere til. Hvis du vil bruge indstillingerne fra den prisliste, du kopierer priser til, skal du aktivere funktionen **Brug standarder fra destination** til/fra.

1. Vælg ikonet ![Lightbulb, der åbner funktionen Fortæl mig](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig"), angiv **Salgsprislister**, og vælg derefter det relaterede link. 
2. Vælg den prisliste, du vil kopiere, og vælg derefter **Kopier linjer**.
3. Udfyld felterne efter behov. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

   > [!NOTE]
   > Du kan ikke have to linjer, der har samme indstillinger, men forskellige priser. Hvis det sker, vises en meddelelse, når du aktiverer prislisten. Du kan vælge den pris, der skal bruges, ved at åbne listen og slette den forkerte pris.  
  
---

## <a name="to-bulk-update-item-prices"></a>Sådan masseopdateres varepriser

Disse trin varierer, afhængigt af, om din administrator har slået funktionsopdateringen **Ny vareprissætningsopdatering** til. Hvis funktionsopdateringen ikke er aktiveret, skal du følge fremgangsmåden under fanen Aktuel oplevelse.

#### <a name="current-experience"></a>[Aktuel oplevelse](#tab/current-experience/)

Hvis du vil masseopdatere varepriser, f.eks. forøge alle varepriser med en procentsats, skal du udfylde Salgspriskladde ved at bruge følgende batchjobs:

* **Foreslå salgspris på kladde** foreslår ændringer på en af to måder. Enten ved at anvende en justeringsfaktor på eksisterende salgspriser eller ved at kopiere eksisterende salgsprisaftaler til andre debitorer, debitorprisgrupper eller salgskampagner.
* **Foreslå varepris på kladde** foreslår ændringer på en af to måder. Eller ved at anvende en justeringsfaktor på eksisterende salgspriser på varekortet eller ved at foreslå priser på nye kombinationer af valuta, enheder osv. Salgsprisen på varer ændres ikke af denne kørsel.  

1. Vælg ikonet ![Elpære, der åbner funktionen Fortæl mig](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig"), angiv **Salgspriskladde**, og vælg derefter det relaterede link.  
2. Vælg handlingen **Foreslå varepris på kladde** .  
3. I oversigtspanelet **Vare** skal du udfylde **Nummer**. eller **Varebogføringsgruppe** eller andre felter med de oprindelige varepriser, du vil opdatere.  
4. Udfyld felterne **Salgstype** og **Salgskode** i den øverste del af siden med den type og det navn, du vil have salgspriserne kopieret til.
5. Hvis kørslen automatisk skal justere foreslåede varepriser, skal du angive justeringen i feltet **Ganges med**. F.eks. skal du angive 1,15 i **Ganges med** for 15 % stigning i varepris.  
6. Hvis kørslen skal oprette nye priser, skal du markere til/fra-afkrydsningsfeltet **Opret nye priser**.  
7. Klik på **OK** for at udfylde linjerne på siden **Salgspriskladde** med de foreslåede nye priser.
8. Brug handlingen **Implementer prisændringer** til at implementere forslagene. Kørslen opretter forslag, men implementerer dem ikke. 

#### <a name="new-experience"></a>[Ny oplevelse](#tab/new-experience/)

Hvis du vil opdatere priser for flere varer, skal du oprette en ny prisliste og derefter kopiere linjerne fra en eksisterende prisliste. Når du kopierer linjer, kan du angive, hvad der skal kopieres, og du kan angive et heltal eller decimaltal i feltet **Ganges med** for at øge eller reducere priserne. Status for prisliste skal være **Kladde**. Hvis det er nødvendigt, kan du deaktivere den gamle prisliste.

> [!NOTE]
> Du kan ikke have to linjer, der har samme indstillinger, men forskellige priser. Hvis det sker, vises en meddelelse, når du aktiverer en prisliste. Du kan vælge den pris, der skal bruges, ved at åbne listen og slette den forkerte pris.  

---

## <a name="best-price-calculation"></a>Beregning af bedste pris

Når du har oprettet special postpriser og linjerabatter for salg og køb, beregner [!INCLUDE[prod_short](includes/prod_short.md)] den bedste pris på salgs-og købsdokumenter og på sags-og varekladdelinjer.

Den bedste pris er den lavest tilladte pris med den størst tilladte linjerabat på en givet dato. [!INCLUDE[prod_short](includes/prod_short.md)] beregner bedste priser, når enhedsprisen og linjerabatprocenten for varer indsættes på nye dokument- og kladdelinjer.

> [!NOTE]  
> I det følgende beskrives, hvordan den bedste pris beregnes for salg. For køb er beregningen tilsvarende, men er baseret på de tilgængelige parametre. Varerabatgrupper understøttes f. eks. ikke ved indkøb.

1. [!INCLUDE[prod_short](includes/prod_short.md)] kontrollerer kombinationen af faktureringsdebitoren og varen automatisk og beregner derefter den relevante enhedspris og linjerabatprocent ud fra følgende kriterier:

    * Har denne kunde en pris-/rabataftale, eller tilhører kunden en gruppe, der har en sådan aftale?
    * Er varen eller varerabatgruppen på linjen medtaget i nogen af disse pris/rabataftaler?
    * Ligger ordredatoen (bogføringsdatoen for faktura- eller kreditnotaen) inden for start- og slutdatoen for pris-/rabataftalen?
    * Er enhedskoden angivet? Hvis den gør det, kontrollerer [!INCLUDE[prod_short](includes/prod_short.md)], om der er priser/rabatter med samme enhedskode, og om der er priser/rabatter, uden at der er tilknyttet en enhedskode.

2. [!INCLUDE[prod_short](includes/prod_short.md)] undersøger, om der gælder pris/rabataftaler for oplysninger om dokumentet eller kladdelinjen. Derefter indsættes den gældende salgspris og linjerabatprocent med følgende kriterier:

    * Er der et krav om et mindste antal i pris-/ rabataftalen, som er opfyldt?
    * Er der et krav om valuta i pris-/ rabataftalen, som er opfyldt? Hvis der er det, indsættes den laveste pris og den højeste linjerabat for valutaen, selvom den lokale valuta giver en bedre pris. Hvis der ikke er nogen pris-/rabataftale for den angivne valutakode, indsætter [!INCLUDE[prod_short](includes/prod_short.md)] den laveste pris og den højeste linjerabat i din lokale valuta.

Hvis der ikke kan beregnes en særpris for varen på linjen, indsættes seneste indirekte omkostning eller enhedsprisen fra varekortet.

## <a name="sales-invoice-discounts-and-service-charges"></a>Salgsfakturarabatter og servicegebyrer

Når du bruger fakturarabatter, bestemmer det samlede fakturabeløb størrelsen af rabatten. På siden **Deb./fakt.rabatter** kan du også føje et servicegebyr til fakturaer over en vis størrelse.  

Du skal angive nogle oplysninger, før du kan bruge fakturarabatter i forbindelse med salg. Du skal beslutte følgende:  

* Hvilke debitorer der skal tildeles denne type rabat?  
* Hvilken rabatprocent du vil bruge?  

Hvis dine fakturarabatter skal beregnes automatisk, kan du angive dette på siden **Salgsopsætning**, aktivere til/fra-funktionen **Beregn fakturarabat**.  

Du kan angive, om du vil tilbyde fakturarabatter, når en faktura opfylder visse kriterier for hver debitor. F. eks. hvis fakturabeløbet er stort nok. Fakturarabatter kan være i lokal valuta for indenlandske debitorer eller i udenlandsk valuta for udenlandske debitorer.  

Du kan knytte rabatter til bestemte fakturabeløb på siderne **Deb./fakt.-rabatter**. Du kan angive et vilkårligt antal procenter. Hver debitor kan have sin egen side, eller du kan sammenkæde flere debitorer på den samme side.  

Du kan også knytte et servicegebyr til et bestemt fakturabeløb i tillæg til eller i stedet for rabatprocenten.  

> [!TIP]  
> Det anbefales, at du forbereder en skitse over den rabatstruktur, der skal anvendes, før du begynder at indtaste disse oplysninger. Strukturen gør det nemmere at se, hvilke debitorer der kan knyttes til samme fakturarabatside. Jo færre sider, du har sat op, jo hurtigere kan du indtaste stamoplysningerne.

Du finder flere øvelser i rabatter under [Konfiguration af rabatter til dine kunder på](/training/modules/customer-discounts-dynamics-365-business-central/index).

### <a name="calculating-invoice-discounts-on-sales"></a>Beregne fakturarabatter på salg

[!INCLUDE [sales-invoice-discounts](includes/sales-invoice-discounts.md)]

## <a name="to-set-up-a-sales-line-discount-for-a-customer"></a>Sådan konfigureres salgslinjerabatter for en debitor

Disse trin varierer, afhængigt af, om din administrator har slået funktionsopdateringen **Ny vareprissætningsopdatering** til. Hvis funktionsopdateringen ikke er aktiveret, skal du følge fremgangsmåden under fanen Aktuel oplevelse.

#### <a name="current-experience"></a>[Aktuel oplevelse](#tab/current-experience/)  

1. Vælg ikonet ![Elpære, der åbner funktionen Fortæl mig](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig"), angiv **Debitorer**, og vælg derefter det relaterede link.
2. Åbn det relevante debitorkort, og vælg derefter handlingen **Linjerabatter**.
3. Udfyld felterne på linjen efter behov. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)] Udfyld en linje for hver kombination, som yder en salgslinjerabat til kunden.

> [!NOTE]
> Når du åbner siderne **Salgspriser** og **Salgslinjerabatter** fra en bestemt kunde, er felterne **Salgstypefilter** og **Salgskodefilter** er angivet for debitoren og kan ikke ændres eller fjernes.
>
> Hvis du vil oprette priser eller linjerabatter for alle debitorer, en debitorprisgruppe eller en kampagne, skal du åbne siderne fra et varekort. Du kan alternativt bruge siden **Salgspriskladde** til salgspriser. Flere oplysninger i [Sådan masseopdateres varepriser](sales-how-record-sales-price-discount-payment-agreements.md#to-bulk-update-item-prices).  

#### <a name="new-experience"></a>[Ny oplevelse](#tab/new-experience/)  

1. Vælg ikonet ![Elpære, der åbner funktionen Fortæl mig](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig"), angiv **Kunder**, og vælg derefter det relaterede link.
2. Vælg debitor, og vælg derefter handlingen **Salgsprislister**.
3. Åbn den prisliste, som du vil angive linjerabat for.
4. Opret en ny linje, eller vælg en eksisterende linje, og udfyld derefter felterne efter behov. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
5. I feltet **Definer** skal du vælge enten **Pris og rabat** eller kun **Rabat**. 
6. I feltet **Linjerabat i procent** specificeres i rabatprocenten.

    > [!TIP]
    > Hvis du redigerer en eksisterende linje, kan du filtrere linjerne ved at vælge den relevante indstilling i feltet **Vis kolonner for**.

    > [!NOTE]  
    > Fakturarabatkoder repræsenteres af eksisterende debitorkort. Det gør det muligt hurtigt at tildele betingelserne for fakturarabatten til debitorer ved at vælge navnet på en anden debitor, der skal have samme betingelser. Hvis du vil oprette debitorspecifikke fakturarabatbetingelser, skal du angive feltet **Fakturarabatkode** til debitorens debitorkode og derefter fortsætte til næste trin.

---

## <a name="to-set-up-an-invoice-discount-for-a-customer"></a>Sådan oprettes en fakturarabat for en debitor

Når du har besluttet, hvilke kunder der skal have fakturarabatter, skal du angive fakturarabatkoden på debitorkortene og definere betingelserne for hver kode. Angiv derefter betingelserne for hver kode.

1. Vælg ikonet ![Elpære, der åbner funktionen Fortæl mig](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig"), angiv **Kunder**, og vælg derefter det relaterede link.
2. Åbn debitorkortsiden for en debitor, der kan ydes fakturarabat til.
3. Vælg en kode i feltet **Fakturarabatkode** for de fakturarabatbetingelser, som skal bruges til automatisk beregning af fakturarabat til debitoren.

> [!NOTE]  
> Fakturarabatkoder repræsenteres af eksisterende debitorkort. Det gør det muligt hurtigt at tildele betingelserne for fakturarabatten til debitorer ved at vælge navnet på en anden debitor, der skal have samme betingelser.

Fortsæt med at angive nye fakturarabatbetingelser for salg.

1. På siden **Kunder** skal du vælge handlingen **Fakturarabatter**. Siden **Deb./fakt.-rabatter** åbnes.
2. Angiv koden for den valuta, som fakturarabatbetingelserne på linjen gælder for, i feltet **Valutakode**. Lad feltet stå tomt for at angive fakturarabatbetingelser for DKK.
3. Angiv det minimumsbeløb, der berettiger til rabatten, i feltet **Min. beløb**.
4. I feltet **Rabatpct.** skal du angive fakturarabatten som en procentdel af fakturabeløbet.
5. Gentag trin 5-7 for hver valuta, som debitoren får en personlig fakturarabat for.

## <a name="see-related-microsoft-training"></a>Se relateret [Microsoft-træning](/training/modules/manage-sales-prices-dynamics-365-business-central/index)

## <a name="see-also"></a>Se også

[Konfigurere salg](sales-setup-sales.md)  
[Salg](sales-manage-sales.md)  
[Konfigurere debitorprisgrupper](sales-how-to-set-up-customer-price-groups.md)  
[Konfigurere debitorrabatgrupper](sales-how-to-set-up-customer-discount-groups.md)  
[Arbejde med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
