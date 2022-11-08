---
title: Synkronisere varer og lager
description: Oprette og køre synkroniseringer af varer mellem Shopify og Business Central
ms.date: 05/27/2022
ms.topic: article
ms.service: dynamics365-business-central
ms.search.form: 30116, 30117, 30126, 30127,
author: AndreiPanko
ms.author: andreipa
ms.reviewer: solsen
ms.openlocfilehash: 90144dfb2f84853f43ae85bf5a162f46cdb65286
ms.sourcegitcommit: 5bb13966e9ba8d7a3c2f00dd32f167acccf90b82
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 10/28/2022
ms.locfileid: "9728379"
---
# <a name="synchronize-items-and-inventory"></a>Synkronisere varer og lager

**Varerne** i [!INCLUDE[prod_short](../includes/prod_short.md)] svarer til *produkterne* i Shopify og inkluderer fysiske produkter, digitale overførsler, tjenester og gavekort, som du kan sælge. Der er to grunde til at synkronisere varerne:

1. Datastyring udføres primært i [!INCLUDE[prod_short](../includes/prod_short.md)]. Du skal eksportere alle eller nogle data derfra til Shopify, så de bliver synlige. Du kan eksportere varenavn, beskrivelse, billede, priser, tilgængelighed, varianter, leverandør detaljer og stregkode. Når du har eksporteret, kan du gennemse elementerne eller få dem vist med det samme.
2. Når en ordre importeres fra Shopify, er oplysningerne om elementerne nødvendige for at kunne behandle dokumentet yderligere i [!INCLUDE[prod_short](../includes/prod_short.md)].

Følgende to scenarier er altid aktiverede.

Et tredje scenario er at administrere data i Shopify, men indlæse disse elementer samlet i [!INCLUDE[prod_short](../includes/prod_short.md)]i. Dette scenario kan være nyttigt i forbindelse med dataoverførselshændelser, når du vil forbinde en eksisterende online shop med en ny [!INCLUDE[prod_short](../includes/prod_short.md)].

## <a name="define-item-synchronizations"></a>Definere synkronisering af elementer

1. Vælg søgningen ![Lightbulb, der åbner funktionen Fortæl mig.](../media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, og skriv **Shopify Butik**. Åbn butikken, som du vil konfigurere vare synkronisering for.
2. Vælg den ønskede indstilling i feltet **Synkroniser element**.

   Den følgende tabel beskriver indstillingerne.

|Indstilling|Beskrivelse|
|------|-----------|
|**Tomt**| Produkter importeres sammen med import af ordrer. Produkter eksporteres til Shopify, hvis brugeren kører handlingen **Tilføj vare** fra siden **Shopify Produkter**. Dette er standardprocessen.|
|**Hvis du vil Shopify**| Vælg denne indstilling, hvis du vil opdatere produkterne manuelt ved hjælp af handlingen **Synkroniser produkt** eller vis jobkø for tilbagevendende opdateringer, når den første synkronisering blev udløst med handlingen **Tilføj vare**. Husk at aktivere feltet **Kan opdatere Shopify produkt**. Hvis den ikke er aktiveret, er den lig med indstillingen **Tom** (standardproces). Få flere oplysninger i afsnittet [Eksportere varer til Shopify](synchronize-items.md#export-items-to-shopify)|
|**Fra Shopify**| Vælg denne indstilling, hvis du planlægger at masseimportere produkter fra Shopify enten manuelt ved hjælp af handlingen **Synkroniseringsprodukt** eller via jobkø for tilbagevendende opdateringer. Få flere oplysninger i afsnittet [Importere varer fra Shopify](synchronize-items.md#import-items-from-shopify)|

## <a name="import-items-from-shopify"></a>Indlæs varer fra Shopify

Du kan enten masseimportere varer fra Shopify eller sammen med import af ordrer, lægge disse varer til tabellen **Shopify produkt** og **Shopify Variant** først. Knyt derefter importerede produkter og varianter til varer og varianter i [!INCLUDEprod_short]. Du kan bruge følgende indstillinger til at administrere processen:

|Felt|Beskrivelse|
|------|-----------|
|**Opret automatisk ukendte elementer**|Når Shopify-produkter og -varianter importeres til [!INCLUDE[prod_short](../includes/prod_short.md)], forsøger [!INCLUDE[prod_short](../includes/prod_short.md)]-funktionen altid først t finde den tilsvarende post på varelisten først. **SKU-tilknytning** påvirker, hvordan match ingen udføres, og opretter en ny vare og/eller varevariant. Aktiver denne indstilling, hvis du vil oprette en ny vare, eller hvis der ikke findes en matchende post. Den nye vare oprettes med den importerede data- og **vareskabelonkode**. Hvis denne indstilling ikke er aktiveret, skal du oprette en vare manuelt og bruge handlingen **Tilknyt produkt** fra siden **Shopify Produkter**.|
|**Vareskabelonkode**|Bruges sammen med til/fra-feltet **Automatisk oprettelse af ukendte varer**.<br>Vælg den standardskabelon, der skal bruges til automatisk oprettede varer.|
|**SKU-tilknytning**|Vælg, hvordan du vil bruge **SKU**-værdien importeret fra Shopify under vare/variant-tilknytning og -oprettelse. Flere oplysninger i [Effekt af Shopify-SKU-produkter og stregkoder ved tilknytning og oprettelse af varer og varianter i Business Central](synchronize-items.md#effect-of-shopify-product-skus-and-barcodes-on-mapping-and-creating-items-and-variants-in-business-central)-afsnittet.|
|**SKU-feltseparator**|Brug denne med **SKU-tilknytning** indstillet til **[Varenr. + Variantkode](synchronize-items.md#effect-of-shopify-product-skus-and-barcodes-on-mapping-and-creating-items-and-variants-in-business-central)**-indstlilingen.<br>Definer en separator, der skal bruges til at opdele SKU.<br>Hvis du f.eks. i Shopify opretter varianten med SKU '1000/001', skal du skrive '/' i feltet **SKU-feltseparator** for at få varenummeret i [!INCLUDE[prod_short](../includes/prod_short.md)] som '1000' og varevariantkoden som '001'.|
|**Variantpræfiks**|Bruges sammen med **SKU-tilknytning** angivet til **variantkode** eller **varenr. + variantkode**-indstillinger som fallback-strategi, når SKU, der kommer fra Shopify, er tom.<br>Hvis du vil oprette varevarianten i [!INCLUDE[prod_short](../includes/prod_short.md)] automatisk, skal du angive en værdi i **koden**. Den værdi, der er angivet i feltet SKU, som er indlæst fra Shopify, bruges som standard. Men hvis LAGERVAREN er tom, genereres kode, der starter med et defineret præfiks, og "001".|
|**Shopify Kan opdatere vare**|Vælg denne mulighed, hvis du vil opdatere varer og/eller varianter automatisk.|

### <a name="effect-of-shopify-product-skus-and-barcodes-on-mapping-and-creating-items-and-variants-in-business-central"></a>Effekten af SKU og stregkoder i Shopify-produkt, der påvirker tilknytning og oprettelse af varer og varianter i Business Central

Når produkter importeres fra Shopify til **tabellerneShopify Produkter** og **Shopify Varianter**, forsøger [!INCLUDE[prod_short](../includes/prod_short.md)] at finde eksisterende poster.

Den følgende tabel beskriver de forskellen mellem indstillingerne i feltet **SKU-tilknytning**.

|Indstilling|Indvirkning på tilknytning|Indvirkning på oprettelsen|
|------|-----------------|------------------|
|**Tomt**|Feltet Varenummer bruges ikke i varetilknytningsrutinen.|Ingen indflydelse på oprettelsen af varen.<br>Denne indstilling forhindrer oprettelsen af varianter. Det er nyttigt, hvis du arbejder i salgsordrer, men kun hoved varen bruges. En variant kan stadig tilknyttes manuelt fra siden **Shopify Produkt**.|
|**Varenr.**|Vælg, hvis feltet SKU indeholder varenr.|Ingen indflydelse på oprettelsen af varen uden varianter. For en vare med varianter oprettes hver enkelt variant som en separat vare.<br>Hvis f.eks. Shopify har et produkt med to varianter, og deres varenumre er "1000" og "2000", oprettes der to varer med numrene "1000" og "2000" i [!INCLUDE[prod_short](../includes/prod_short.md)]-systemet.|
|**Variantkode**|Feltet Varenummer bruges ikke i varetilknytningsrutinen.|Ingen indflydelse på oprettelsen af varen. Når der oprettes en varevariant, bruges værdien i feltet Lagervare som en kode. Hvis LAGERVAREN er tom, genereres en kode med brug af feltet **Variantkode**.|
|**Varenr. + variantkode**|Marker feltet, hvis feltet SKU indeholder et varenummer. og varevariant koden separeret med den værdi, der er defineret i feltet **SKU-feltseparator**.|Når der oprettes en vare, bruges den første del af værdien i feltet SKU som **Nr.** Hvis SKU er tom, vil varenr. genereres ved hjælp af de nummerserier, der er defineret i **vareskabelonkoden** eller **varenumrene** fra siden **Lageropsætning**.<br>Når der oprettes en vare, bruger funktionen variant den anden del af værdien af feltet SKU som **kode**. Hvis SKU er tom, genereres en kode med brug af feltet **Variantkode**.|
|**Kreditors varenr.**|Vælg, hvis feltet SKU indeholder kreditorvarenr. I dette tilfælde **Vare/leverandørnr.** //leverandør ikke på siden **varekort** i stedet bruges **leverandør/varenr.** fra **Vare/leverandører-kataloget**. Hvis den fundne *vare-leverandørkatalog*-post indeholder en variantkode, anvendes denne variantkode til at tilknytte Shopify-varianten.|Hvis der findes en tilsvarende kreditor i [!INCLUDE[prod_short](../includes/prod_short.md)], bruges lagerværdien som **Leverandør/varenr.** på siden **varekort** og som **varereference** for typen af kreditor. <br>Forhindrer oprettelse af varianter. Det er nyttigt, hvis du kun vil bruge hoved varen i salgsordren. Du kan stadig tilknytte en variant manuelt fra siden **Shopify Produkt**.|
|**Stregkode**|Vælg, hvis feltet SKU indeholder feltet en stregkode. Der udføres en søgning blandt **varereferencer** af typen leverandør. Hvis den fundne varereferencepost indeholder en variantkode, anvendes denne variantkode til at tilknytte Shopify-varianten.|Ingen indflydelse på oprettelsen af varen. <br>Forhindrer oprettelse af varianter. Det er nyttigt, hvis du kun vil bruge hoved varen i salgsordren. Du kan stadig tilknytte en variant manuelt fra siden **Shopify Produkt**.|

Følgende tabel beskriver effekten af feltet **Stregkode**.

|Indvirkning på tilknytning|Indvirkning på oprettelsen|
|-----------------|------------------|
|Der udføres en søgning blandt **varereferencer** af typen stregkode for den værdi, der er defineret i **Stregkode**-feltet i Shopify. Hvis den fundne varereferencepost indeholder en variantkode, anvendes denne variantkode til at tilknytte Shopify-varianten.|Stregkoden gemmes som **varereference** for vare og varevariant.|

> [!NOTE]  
> Du kan udløse tilknytningen for de valgte produkter/varianter ved at vælge **Prøv Find produkttilknytning** eller alle importerede ikke-tilknyttede produkter **Prøv at finde tilknytninger**.

## <a name="export-items-to-shopify"></a>Eksporter til Excel Shopify

Vælg de elementer på listen, som skal eksporteres til Shopify. Brug handlingen **Tilføj vare** fra vinduet **Shopify produkter** til at føje varer til listen med Shopify-produkter.

Du kan bruge følgende indstillinger til at administrere processen med at eksportere varer:

|Felt|Beskrivelse|
|------|-----------|
|**Debitorprisgruppe**|Bestemmer prisen på en vare i Shopify. Salgsprisen for denne Debitorprisgruppe er taget. Hvis der ikke er angivet en gruppe, bruges prisen på varekortet.|
|**Debitorrabatgruppe**|Angiv den rabat, der skal bruges til beregning af prisen på en vare i Shopify. Rabatpriser lagres i feltet **Pris**, og den fulde pris lagres i feltet **Sammenlign med pris**.|
|**Udvidet tekst til synkroniseret vare**|Vælg dette for at synkronisere den udvidede tekst for varen. Det kan indeholde HTML-kode, da den vil blive føjet til *beskrivelsen*. |
|**Synkroniser vareattributter**|Vælg dette for at synkronisere vareattributterne. Attributterne er formateret som en tabel og medtages i feltet *Beskrivelse* i Shopify.|
|**Sprogkode**|Hvis dette vælges, bruges de oversatte versioner til titel, attributter og udvidet tekst.|
|**SKU-tilknytning**|Vælg, hvordan du vil udfylde feltet Lagervare i Shopify. Understøttede indstillinger er:<br> - **Varenr.** for at bruge varenr. for både produkter og varianter.<br> - **Varenr. + variantkode**  for at oprette et varenummer ved at sammenkæde værdier fra to felter. For varer uden varianter er bruges kun varenr.<br>- **Vare/leverandør nr.** for at bruge vareleverandørnumre, der er defineret på *varekortet* for både produkter og varianter.<br> - **Stregkode** for at bruge **varereferencen** til stregkodetype. Denne indstilling respekterer varianter.|
|**SKU-feltseparator**|Definer en separator for indstillingen **varenr. + variantkode**.|
|**Lager sporet**| Vælg, hvordan systemet skal udfylde feltet **Spor lager** for de produkter, der eksporteres til Shopify. Du kan opdatere toilgængelighedsoplysninger fra [!INCLUDE[prod_short](../includes/prod_short.md)] for produkter i Shopify, hvor spor lager er aktiveret. Der er flere oplysninger i [Lager](synchronize-items.md#sync-inventory-to-shopify)-afsnittet.|
|**Standardlagerpolitik**|Vælg *Afvis* for at forhindre negativ beholdning af Shopify-siden.|
|**Kan opdatere Shopify Produkter**|Definer, om [!INCLUDE[prod_short](../includes/prod_short.md)] kun kan oprette varer, eller om der også kan opdateres varer. Vælg denne indstilling, hvis du vil opdatere produkterne manuelt ved hjælp af handlingen **Synkroniser produkt** eller vis jobkø for tilbagevendende opdateringer, når den første synkronisering blev udløst med handlingen **Tilføj vare**. Husk at vælge **Til Shopify** i feltet **Varesynkronisering**.|
|**Debitorskabelonkode**|Vælg den standardskabelon, der skal bruges ved prisberegningen. Få flere oplysninger [Konfigurere moms](setup-taxes.md).|

### <a name="fields-mapping-overview"></a>Oversigt over felttilknytning

|Shopify|Kilde, når den eksporteres fra [!INCLUDE[prod_short](../includes/prod_short.md)]|Destinationen, når den importeres til [!INCLUDE[prod_short](../includes/prod_short.md)]|
|------|-----------------|-----------------|
|Status|Ifølge **Status for oprettede produkter** på **Shopify Produktionskortet**. Flere oplysninger i [ad-Hoc-opdateringer af Shopify-produkter](synchronize-items.md#ad-hoc-updates-of-shopify-products).|Bruges ikke.|
|Titel | **Beskrivelse**. Hvis sprogkoden er defineret, og der findes en tilsvarende vareoversættelse, bruges vareoversættelsen i stedet for beskrivelse.|**Beskrivelse**|
|Beskrivelse|Kombinerer udvidede tekster og attributter, hvis tilsvarende skift er aktiveret på Shopify-produktionskortet. Respekterer sprogkoden.|Bruges ikke.|
|SEO-sidetitel|Fast værdi: tom. Flere oplysninger i [ad-Hoc-opdateringer af Shopify-produkter](synchronize-items.md#ad-hoc-updates-of-shopify-products).|Bruges ikke.|
|SEO-metabeskrivelse|Fast værdi: tom. Flere oplysninger i [ad-Hoc-opdateringer af Shopify-produkter](synchronize-items.md#ad-hoc-updates-of-shopify-products).|Bruges ikke.|
|Medier|**Billede**. Få mere at vide i afsnittet [Synkronisere vare billeder](synchronize-items.md#sync-item-images)|**Billede**|
|Pris|Beregningen af slutkundepris beregnes med hensyn til vareprisgruppe, varerabatgruppe, valutakode og debitorskabelonkode.|**Enhedspris**|
|Sammenlign med pris|Beregningen af pris uden rabat omfatter vareprisgruppe, varerabatgruppe, valutakode og debitorskabelonkode.|Bruges ikke.|
|Sager pr. vare|**Kostpris**|**Kostpris**|
|Varenummer|Få mere at vide om dette under **SKU-tilknytning** i afsnittet [Eksportere varer til Shopify](synchronize-items.md#export-items-to-shopify).|Flere oplysninger i [Effekt af Shopify-SKU-produkter og stregkoder ved tilknytning og oprettelse af varer og varianter i Business Central](synchronize-items.md#effect-of-shopify-product-skus-and-barcodes-on-mapping-and-creating-items-and-variants-in-business-central)-afsnittet.|
|Stregkode|**Varereferencer** til stregkodetypen.|**Varereferencer** til stregkodetypen.|
|Spor antal|I henhold til feltet **Lager sporet** på siden **Shopify produktionskortet**. Der er flere oplysninger i [Lager](synchronize-items.md#sync-inventory-to-shopify)-afsnittet.|Bruges ikke.|
|Fortsætte med at sælge, når der ikke er mere lager|I henhold til **Lager sporet** i **Shopify produktionskortet**. Ikke importeret.|Bruges ikke.|
|Enhedstype|**Beskrivelse** af **Varekategorikode**. Hvis type ikke er angivet til Shopify, tilføjes den som en brugerdefineret type.|**Varekategorikode**. Tilknytning efter beskrivelse.|
|Leverandør (Kreditor)|**Navn** på kreditor fra **Leverandørnr.**|**Leverandørnr.** Tilknytning efter navn.|
|Vægt|**Bruttovægt**.|Bruges ikke.|
|Skattepligtig|Fast værdi: aktiveret.|Bruges ikke.|
|Momskoder|**Momsgruppekode**. Kun relevant i forbindelse med moms. Få flere oplysninger [Konfigurere moms](setup-taxes.md).|Bruges ikke.|

### <a name="tags"></a>Koder

Gennemse importerede koder i faktaboksen **Koder** på siden **Shopify-produkt**. På samme side redigeres koder ved at vælge handlingen **Koder**.
Hvis indstillingen **Til Shopify** er valgt i feltet **Synkroniser vare**, eksporteres tilknyttede tags til Shopify ved næste synkronisering.

## <a name="run-item-synchronization"></a>Kør varesynkronisering

Du kan udføre fuldstændig eller delvis synkronisering af elementer på mange forskellige måder.

### <a name="initial-sync-of-items-from-business-central-to-shopify"></a>Oprindelig synkronisering af varer fra Business Central til Shopify

1. Gå til søgning søg ![Lightbulb, der åbner funktionen Fortæl mig.](../media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **Shopify Produkter**, og vælg det relevante link.
2. Vælg handlingen **Tilføj varer**.
3. Angiv koden i feltet **Butikskode**. Hvis du åbner vinduet **Shopify Produkt** fra vinduet **Butikskort**, bliver Butikskode automatisk udfyldt.
4. Angiv filtre for varerne efter behov. Du kan f. eks. filtrere efter varenummer. eller varekategorikode.
5. Vælg **OK**.

De oprettede varer oprettes automatisk i Shopify med priser, men der medtages ikke billeder og lagerniveauer. Handlingen kan tage noget tid, hvis der tilføjes et stort antal elementer.

### <a name="sync-products-from-shopify-to-business-central"></a>Synkroniser produkter fra Shopify til Business central

1. Gå til søgning ![Lightbulb, der åbner funktionen Fortæl mig.](../media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **Shopify Butik**, og vælg det relevante link.
2. Marker den butik, som du vil synkronisere varer til for at åbne siden **Shopify-købskort**.
3. Vælg handlingen **Synkroniser produkter**.

Du kan også bruge handlingen **Synkroniser produkter** i vinduet **Shopify Produkter** eller søg efter **Synkroniseringsprodukter**.

Du kan planlægge, at følgende tilbagevendende aktiviteter skal udføres automatisk. Få mere at vide, når du [planlægger tilbagevendende opgaver](background.md#to-schedule-recurring-tasks).

### <a name="ad-hoc-updates-of-shopify-products"></a>Ad-Hoc-opdateringer for Shopify-produkter

Når posterne opdateres i tabellen **Shopify Produkt**, synkroniseres følgende ændringer med Shopify.

Opdater:

* **Status** - du kan vælge mellem aktiv, arkiveret eller kladde.
* **SEO-titel**
* **SEO-beskrivelse**

Sletning:

På baggrund af værdien i **Handling for fjernede produkter** på side **Shopify Butikskort**, opdateres produktet i Shopify, når posten slettes fra siden **Shopify Produkter**.

* **Tom** - Der sker ikke noget. Hvis det er nødvendigt, skal brugeren udføre den ønskede handling fra **Shopify-administratoren**.
* **Status til kladde** - Status for produktet i Shopify er angivet til *Kladde*.
* **Status til arkiveret** - Produkt er arkiveret i Shopify.

## <a name="sync-item-images"></a>Synkroniser varebilleder

Synkronisering af afbildninger kan konfigureres for synkroniserede elementer. Vælg mellem følgende indstillinger:

* **Deaktiveret** - Billedsynkronisering er deaktiveret.
* **Til Shopify** - Billeder af varer eksporteres til Shopify.
* **Fra Shopify** - Billeder fra Shopify importeres til [!INCLUDE[prod_short](../includes/prod_short.md)]

Billedsynkronisering kan initialiseres på to måder.

### <a name="sync-product-images-from-the-shopify-shop-page"></a>Synkronisere produktbilleder fra siden Shopify-butik

1. Gå til søgning ![Lightbulb, der åbner funktionen Fortæl mig.](../media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **Shopify-butikker**, og vælg det relevante link.
2. Marker den butik, som du vil synkronisere billeder til for at åbne **Shopify-butikskortsiden**.
3. Vælg handlingen **Synkroniser produktbilleder**.

### <a name="sync-product-images-from-the-shopify-products-page"></a>Synkronisere produktbilleder fra Shopify-produktvinduet

1. Gå til søgning ![Lightbulb, der åbner funktionen Fortæl mig.](../media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **Shopify Produkter**, og vælg det relevante link.
2. Vælg handlingen **Synkroniser produktbilleder**.

### <a name="image-synchronization-remarks"></a>Bemærkninger til billedsynkronisering

* Når du eksporterer billeder fra [!INCLUDE[prod_short](../includes/prod_short.md)] til Shopify, føjes de nye billeder til Shopify, gamle billeder holdes intakt. Hvis et billede opdateres i [!INCLUDE[prod_short](../includes/prod_short.md)], skal du slette gamle billeder i **Shopify Administrator**.
* Billeder, der eksporteres til Shopify og ikke opfylder kravene angivet i Shopify, importeres ikke. Du kan finde flere oplysninger i [Produktmedietyper på help.shopify.com](https://help.shopify.com/en/manual/products/product-media/product-media-types#images).

## <a name="sync-prices-with-shopify"></a>Synkroniser priser med Shopify

Priser for synkroniserede varer kan eksporteres på to måder, der er beskrevet nedenfor.

### <a name="sync-prices-from-the-shopify-products-page"></a>Synkronisere priser fra siden Shopify-produkter

1. Gå til søgning ![Lightbulb, der åbner funktionen Fortæl mig.](../media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **Shopify Produkter**, og vælg det relevante link.
2. Vælg handlingen **Synkroniser priser til Shopify**.

### <a name="price-calculation-remarks"></a>Bemærkninger til prisberegning

* Ved prisberegning er det vigtigt, at der er en værdi i feltet **Standarddebitorskabelon**. Få flere oplysninger [Konfigurere moms](setup-taxes.md).
* Husk at angive en **Valutakode**, hvis din online-butik bruger en anden valuta end den relevante regnskabsvaluta. Der skal være konfigureret valutakurser for den angivne valuta. Hvis dit onlineindkøb bruger samme valuta som [!INCLUDE[prod_short](../includes/prod_short.md)], skal du lade feltet stå tomt.
* Når du fastlægger en pris, [!INCLUDE[prod_short](../includes/prod_short.md)] bruges logikken "laveste kurs". Det betyder, at hvis den enhedspris, der er defineret på varekortet, er lavere end det, der er defineret i prisgruppen, bruges salgsprisen fra varekortet.

## <a name="sync-inventory-to-shopify"></a>Synkroniser lager med Shopify

Lagersynkronisering kan konfigureres for allerede synkroniserede elementer. Der skal være to betingelser, der skal overholdes:

1. Lagersporing skal aktiveres for et produkt i Shopify. Hvis varerne eksporteres til Shopify, skal du overveje at aktivere til/fra-feltet **Lagersporing** på siden **Shopify Butik**. Få flere oplysninger i afsnittet [Eksportere varer til Shopify](synchronize-items.md#export-items-to-shopify)
2. Lagersynkronisering skal være aktiveret for **Shopify Lokationer**.

### <a name="to-enable-inventory-sync"></a>Sådan aktiveres lagersynkronisering

1. Gå til søgning ![Lightbulb, der åbner funktionen Fortæl mig.](../media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **Shopify Butik**, og vælg det relevante link.
2. Marker den butik, som du vil synkronisere lager med for at åbne **Shopify Butikskort**-siden.
3. Vælg handlingen **Lokationer** for at åbne **Shopify Butikslokationer**.
4. Vælg handlingen **Hent Shopify Lokationer** for at importere alle de placeringer, der er defineret i Shopify. Du kan finde dem under [**Lokations**](https://www.shopify.com/admin/settings/locations)-indstillinger i **Shopify Admin**.
5. Tilføj lokationer i feltet **Lokationsfilter**, hvis du kun vil medtage lagerbeholdningen fra bestemte lokationer. Du kan f. eks. skrive *ØST|VEST*, så lageret kun er tilgængeligt fra disse to lokationer for salg via online-butik.
6. Fjern markeringen fra til/fra-feltet **Deaktiveret** for at aktivere lagersynkronisering for udvalgte Shopify lokationer.

Du kan initialisere lagersynkronisering på to måder, som beskrevet herunder.

### <a name="sync-inventory-from-the-shopify-shop-page"></a>Synkronisere lager fra Shopify-butiksvinduet

1. Gå til søgning ![Lightbulb, der åbner funktionen Fortæl mig.](../media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **Shopify-butikker**, og vælg det relevante link.
2. Marker den butik, som du vil synkronisere lager med for at åbne **Shopify Butikskort**-siden.
3. Vælg handlingen **Synkroniser lager**.

### <a name="sync-inventory-from-the-shopify-products-page"></a>Synkronisere lager fra Shopify-produktsiden

1. Gå til søgning ![Lightbulb, der åbner funktionen Fortæl mig.](../media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **Shopify Produkter**, og vælg det relevante link.
2. Vælg handlingen **Synkroniser lager**.

### <a name="inventory-remarks"></a>Lagerokmmentarer

* Connectoren beregner det **planlagte disponible resultat** og eksporterer den til Shopify.
* Du kan kontrollere de modtagne lageroplysninger fra Shopify på siden **Shopify Lager-faktaboks**. I denne faktaboks får du en oversigt over Shopify-lagerbeholdningen og den sidst beregnede lagerbeholdning i [!INCLUDE[prod_short](../includes/prod_short.md)]. Der er en post pr. lokation.
* Hvis lageroplysningerne i Shopify er forskellige fra **Planlagt disponibel resultat** i [!INCLUDE[prod_short](../includes/prod_short.md)], opdateres lageret i Shopify.

## <a name="see-also"></a>Se også

[Kom i gang med Connectoren til Shopify](get-started.md)  
