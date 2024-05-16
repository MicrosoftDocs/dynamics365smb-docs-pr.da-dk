---
title: Synkronisere varer og lager
description: Oprette og køre synkroniseringer af varer mellem Shopify og Business Central
ms.date: 04/28/2024
ms.topic: article
ms.search.form: '30116, 30117, 30126, 30127,'
author: brentholtorf
ms.author: bholtorf
ms.reviewer: andreipa
ms.collection:
  - bap-ai-copilot
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
   |**Tomt**| Produkter importeres sammen med import af ordrer. Produkter eksporteres til Shopify, hvis brugeren kører handlingen **Tilføj vare** fra siden **Shopify Produkter**. Denne indstilling er standardprocessen.|
   |**Hvis du vil Shopify**| Vælg denne indstilling, hvis du vil opdatere produkterne manuelt ved hjælp af handlingen **Synkroniser produkt** eller vis jobkø for tilbagevendende opdateringer, når den første synkronisering blev udløst med handlingen **Tilføj vare**. Husk at aktivere feltet **Kan opdatere Shopify produkt**. Hvis den ikke er aktiveret, er den lig med indstillingen **Tom** (standardproces). Få flere oplysninger i afsnittet [Eksportere varer til Shopify](synchronize-items.md#export-items-to-shopify)|
   |**Fra Shopify**| Vælg denne indstilling, hvis du planlægger at masseimportere produkter fra Shopify enten manuelt ved hjælp af handlingen **Synkroniseringsprodukt** eller via jobkø for tilbagevendende opdateringer. Få flere oplysninger i afsnittet [Importere varer fra Shopify](synchronize-items.md#import-items-from-shopify)|

   > [!NOTE]
   > Hvis du ændrer **Synkroniseringselement** fra **Fra Shopify** til **Til Shopify**, vil det ikke have en effekt, medmindre du aktiverer **Kan opdatere Shopify-produkter**.

## <a name="import-items-from-shopify"></a>Indlæs varer fra Shopify

Du kan enten masseimportere varer fra Shopify eller sammen med import af ordrer, lægge disse varer til tabellen **Shopify produkt** og **Shopify Variant** først. Knyt derefter importerede produkter og varianter til varer og varianter i [!INCLUDE[prod_short](../includes/prod_short.md)]. Du kan bruge følgende indstillinger til at administrere processen:

|Felt|Beskrivlse|
|------|-----------|
|**Opret automatisk ukendte elementer**|Når Shopify-produkter og -varianter importeres til [!INCLUDE[prod_short](../includes/prod_short.md)], forsøger [!INCLUDE[prod_short](../includes/prod_short.md)]-funktionen altid først t finde den tilsvarende post på varelisten først. **SKU-tilknytning** påvirker, hvordan match ingen udføres, og opretter en ny vare og/eller varevariant. Aktiver denne indstilling, hvis du vil oprette en ny vare, eller hvis der ikke findes en matchende post. Den nye vare oprettes med den importerede data- og **vareskabelonkode**. Hvis denne indstilling ikke er aktiveret, skal du oprette en vare manuelt og bruge handlingen **Tilknyt produkt** fra siden **Shopify Produkter**.|
|**Vareskabelonkode**|Brug dette felt sammen med til/fra-feltet **Automatisk oprettelse af ukendte varer**.<br>Vælg den standardskabelon, der skal bruges til automatisk oprettede varer.|
|**SKU-tilknytning**|Vælg, hvordan du vil bruge **SKU**-værdien importeret fra Shopify under vare/variant-tilknytning og -oprettelse. Flere oplysninger i [Effekt af Shopify-SKU-produkter og stregkoder ved tilknytning og oprettelse af varer og varianter i Business Central](synchronize-items.md#effect-of-shopify-product-skus-and-barcodes-on-mapping-and-creating-items-and-variants-in-business-central)-afsnittet.|
|**SKU-feltseparator**|Brug dette felt med **SKU-tilknytning** angivet til indstillingen **[Varenr. + variantkode](synchronize-items.md#effect-of-shopify-product-skus-and-barcodes-on-mapping-and-creating-items-and-variants-in-business-central)**.<br>Definer en separator, der skal bruges til at opdele SKU.<br>Hvis du f.eks. i Shopify opretter varianten med SKU '1000/001', skal du skrive '/' i feltet **SKU-feltseparator** for at få varenummeret i [!INCLUDE[prod_short](../includes/prod_short.md)] som '1000' og varevariantkoden som '001'. Bemærk, at hvis du opretter varianten med SKU '1000/001/111' i Shopify, vil varenummeret i [!INCLUDE[prod_short](../includes/prod_short.md)] være '1000' og varevariantkoden '001'. '111'-delen ignoreres. |
|**Variantpræfiks**|Bruges sammen med **SKU-tilknytning** angivet til **variantkode** eller **varenr. + variantkode**-indstillinger som fallback-strategi, når SKU, der kommer fra Shopify, er tom.<br>Hvis du vil oprette varevarianten i [!INCLUDE[prod_short](../includes/prod_short.md)] automatisk, skal du angive en værdi i **koden**. Den værdi, der er angivet i feltet SKU, som er indlæst fra Shopify, bruges som standard. Men hvis LAGERVAREN er tom, genereres kode, der starter med et defineret præfiks, og '001'.|
|**Shopify Kan opdatere vare**|Vælg denne mulighed, hvis du vil opdatere varer og/eller varianter automatisk.|
|**UOM som variant**| Vælg denne indstilling, hvis alle vareenheder skal eksporteres som separate varianter. Tilpas siden for at tilføje feltet. Få mere at vide i afsnittet [Enhed som variant](synchronize-items.md#unit-of-measure-as-variant).|
|**Navn på variantindstilling for UOM**| Brug dette felt sammen med **UoM som variant** til at angive, under hvilken indstilling der skal tilføjes varianter, der repræsenterer enheder. Standardværdien er *Enhed*. Brug tilpasning for at tilføje feltet til siden.|

## <a name="export-items-to-shopify"></a>Eksporter til Excel Shopify

Du kan eksportere elementer til Shopify på flere måder:

* Brug handlingen **Føj element til Shopify** direkte fra siden **Varekort**.
* Brug handlingen  **Tilføj element**  på siden  **Shopify Produkter** .
* Kør varesynkronisering én gang eller gentagne gange med automatisering.

Uanset hvordan du eksporterer varer, overføres specifikke vareoplysninger til Shopify-produktlisten afhængigt af dit valg af indstillinger for varesynkronisering.

> [!IMPORTANT]
> Produktet vil kun blive føjet til salgskanalen **Onlinebutik**. Du skal udgive produkter til andre salgskanaler, f. eks Shopify POS, fra Shopify.

Du kan bruge følgende indstillinger til at administrere processen med at eksportere varer:

|Felt|Beskrivlse|
|------|-----------|
|**Udvidet tekst til synkroniseret vare**|Markér dette felt for at synkronisere den udvidede tekst for varen. Da det kan føjes til feltet **Beskrivelsen**, kan det indeholde HTML-kode. |
|**Synkroniser vareattributter**|Markér dette for at synkronisere vareattributterne. Attributterne er formateret som en tabel og medtages i feltet **Beskrivelse** i Shopify.|
|**Marketingtekst til synkroniseret vare**|Markér dette felt for at synkronisere marketingtekst for varen. Selvom marketingtekst er en slags beskrivelse, er den forskellig fra en vares **Beskrivelsesfelt**. Feltet **Beskrivelse** bruges typisk som et kort vist navn til at identificere produktet hurtigt. Marketingteksten er derimod en mere omfattende og beskrivende tekst. Formålet er at tilføje marketing- og reklameindhold. Denne tekst kan derefter udgives sammen med elementet i Shopify. Der er to måder at oprette en marketingtekst på. Den nemmeste måde at komme i gang på er ved at bruge Copilot, som foreslår AI-genereret tekst for dig.|
|**Sprogkode**|Markér dette felt, hvis de oversatte versioner skal bruges til titel, attributter og udvidet tekst.|
|**SKU-tilknytning**|Vælg, hvordan du vil udfylde feltet Lagervare i Shopify. Understøttede indstillinger er:<br> - **Varenr.** for at bruge varenummeret for både produkter og varianter.<br> - **Varenr. + variantkode** for at oprette et varenummer ved at sammenkæde værdier fra to felter. For varer uden varianter er bruges kun varenr.<br>- **Vare/leverandør nr.** for at bruge vareleverandørnumre, der er defineret på **varekortet** for både produkter og varianter.<br> - **Stregkode** for at bruge **varereferencen** til stregkodetype. Denne indstilling respekterer varianter.<br>Hvis **Kan opdatere Shopify-produkter** er aktiveret, overføres ændringer i feltet **SKU-tilknytning** til Shopify efter næste synkronisering for alle produkter, og varianter, der er angivet i **Shopify-produkter** er angivet for den valgte butik.|
|**Feltseparator til varenumre**|Definer en separator for indstillingen **varenr. + variantkode**.|
|**Lager sporet**| Vælg, hvordan systemet skal udfylde feltet **Spor lager** for de produkter, der eksporteres til Shopify. Du kan opdatere tilgængelighedsoplysninger fra [!INCLUDE[prod_short](../includes/prod_short.md)] for produkter i Shopify, hvor spor lager er aktiveret. Der er flere oplysninger i [Lager](synchronize-items.md#sync-inventory-to-shopify)-afsnittet.|
|**Standardlagerpolitik**|Vælg *Afvis* for at forhindre negativ beholdning af Shopify-siden. <br>Hvis **Kan opdatere Shopify produkter** er aktiveret, overføres ændringer i feltet **Standardlagerpolitik** til Shopify efter næste synkronisering for alle produkter, og varianter, der er angivet i **Shopify-produkter** er angivet for den valgte butik.|
|**Kan opdatere Shopify Produkter**|Definer, om [!INCLUDE[prod_short](../includes/prod_short.md)] kun kan oprette varer, eller om der også kan opdateres varer. Vælg denne indstilling, hvis du vil opdatere produkterne manuelt ved hjælp af handlingen **Synkroniser produkt** eller vis jobkø for tilbagevendende opdateringer, når den første synkronisering blev udløst med handlingen **Tilføj vare**. Husk at vælge **Til Shopify** i feltet **Varesynkronisering**.<br>**Kan opdatere Shopify-produkter** påvirker ikke synkronisering af priser, billeder eller lagerniveauer, som er konfigureret af uafhængige kontroller.<br>Hvis **Kan opdatere Shopify-produkter** er aktiveret, opdateres følgende felter for produktet på Shopify-siden og eventuelt variantniveauet: **SKU**, **Stregkode**, **Vægt**. **Titel**, **Produkttype**, **Leverandør** og **Beskrivelse** for produktet opdateres også, hvis de eksporterede værdier ikke er tomme. Hvis det er en beskrivelse, betyder det, at du skal aktivere et af til/fra-felterne **Udvidet tekst til synkroniseret vare**, **Marketingtekst til synkroniseret vare** og **Synkroniser vareattributter** samt og attributterne, udvidet tekst eller marketingtekst skal have værdier. Hvis produktet bruger varianter, tilføjes eller fjernes varianten, hvis det er nødvendigt. <br>Hvis produktet på Shopify er konfigureret til at bruge variantmatrix, der kombinerer to eller flere indstillinger, kan Shopify Connector ikke oprette variant for det pågældende produkt. I [!INCLUDE[prod_short](../includes/prod_short.md)] er ingen måde at definere indstillingsmatrix på, derfor bruger connectoren **Variantkoden** som den eneste mulighed. Shopify forventer dog flere muligheder og nægter at oprette variant, hvis der mangler oplysninger om en anden og andre muligheder. |
|**UOM som variant**| Vælg denne indstilling, hvis visse indstillinger skal eksporteres eller importeres som enheder i stedet for varianter. Tilpas siden for at tilføje feltet. Få mere at vide i afsnittet [Enhed som variant](synchronize-items.md#unit-of-measure-as-variant).|
|**Navn på variantindstilling for UOM**| Brug dette felt sammen med **UoM som variant** til at angive, hvilken indstilling der indeholder varianter, der repræsenterer enheder. Standardværdien er *Enhed*. Tilpas siden for at tilføje feltet.|

> [!NOTE]
> Når du vil eksportere mange varer og varianter, kan der være nogle, der er blokeret. Du kan ikke medtage spærrede varer og varianter i prisberegninger, så de eksporteres ikke. Connectoren springer disse varer og varianter over, så du ikke behøver at filtrere dem på anmodningssiden **Tilføj vare til Shopify**.

## <a name="advanced-details"></a>Avancerede detaljer

### <a name="effect-of-shopify-product-skus-and-barcodes-on-mapping-and-creating-items-and-variants-in-business-central"></a>Effekten af SKU og stregkoder i Shopify-produkt, der påvirker tilknytning og oprettelse af varer og varianter i Business Central

Når produkter importeres fra Shopify til **tabellerneShopify Produkter** og **Shopify Varianter**, forsøger [!INCLUDE[prod_short](../includes/prod_short.md)] at finde eksisterende poster.

Den følgende tabel beskriver de forskellen mellem indstillingerne i feltet **SKU-tilknytning**.

|Indstilling|Indvirkning på tilknytning|Indvirkning på oprettelsen|
|------|-----------------|------------------|
|**Tomt**|Feltet SKU bruges ikke i varetilknytningsrutinen.|Ingen indflydelse på oprettelsen af varen.<br>Denne indstilling forhindrer oprettelsen af varianter. Hvis du arbejder i salgsordrer, anvendes kun hovedvaren. En variant kan stadig tilknyttes manuelt fra siden **Shopify Produkt**.|
|**Varenr.**|Vælg, hvis feltet SKU indeholder varenummeret.|Ingen indflydelse på oprettelsen af varen uden varianter. For en vare med varianter oprettes hver enkelt variant som en separat vare.<br>Hvis f.eks. Shopify har et produkt med to varianter, og deres varenumre er "1000" og "2000", oprettes der to varer med numrene "1000" og "2000" i [!INCLUDE[prod_short](../includes/prod_short.md)]-systemet.|
|**Variantkode**|Feltet SKU bruges ikke i varetilknytningsrutinen.|Ingen indflydelse på oprettelsen af varen. Når der oprettes en varevariant, bruges værdien i feltet Lagervare som en kode. Hvis LAGERVAREN er tom, genereres en kode med brug af feltet **Variantkode**.|
|**Varenr. + variantkode**|Vælg denne indstilling, hvis feltet SKU indeholder et varenummer. og varevariantkoden er separeret med den værdi, der er defineret i feltet **SKU-feltseparator**.|Når der oprettes en vare, bruges den første del af værdien i feltet SKU som **Nr.** Hvis SKU er tom, vil varenr. genereres ved hjælp af de nummerserier, der er defineret i **vareskabelonkoden** eller **varenumrene** fra siden **Lageropsætning**.<br>Når der oprettes en vare, bruger funktionen variant den anden del af værdien af feltet SKU som **kode**. Hvis SKU er tom, genereres en kode med brug af feltet **Variantkode**.|
|**Kreditors varenr.**|Vælg, hvis feltet SKU indeholder kreditorvarenr. I dette tilfælde **Vare/leverandørnr.** //leverandør ikke på siden **varekort** i stedet bruges **leverandør/varenr.** fra **Vare/leverandører-kataloget**. Hvis den fundne *vare-leverandørkatalog*-post indeholder en variantkode, anvendes denne variantkode til at tilknytte Shopify-varianten.|Hvis der findes en tilsvarende kreditor i [!INCLUDE[prod_short](../includes/prod_short.md)], bruges SKU-værdien som **Leverandør/varenr.** på siden **varekort** og som **varereference** for *typen af kreditor*. <br>Forhindrer oprettelse af varianter. Det er nyttigt, hvis du kun vil bruge hoved varen i salgsordren. Du kan stadig tilknytte en variant manuelt fra siden **Shopify Produkt**.|
|**Stregkode**|Vælg, hvis feltet SKU indeholder feltet en stregkode. Der udføres en søgning blandt **varereferencer** af typen *stregkode*. Hvis den fundne varereferencepost indeholder en variantkode, anvendes denne variantkode til at tilknytte Shopify-varianten.|Ingen indflydelse på oprettelsen af varen. <br>Forhindrer oprettelse af varianter. Det er nyttigt, hvis du kun vil bruge hoved varen i salgsordren. Du kan stadig tilknytte en variant manuelt fra siden **Shopify Produkt**.|

Følgende tabel beskriver effekten af feltet **Stregkode**.

|Indvirkning på tilknytning|Indvirkning på oprettelsen|
|-----------------|------------------|
|Der udføres en søgning blandt **varereferencer** af typen stregkode for den værdi, der er defineret i **Stregkode**-feltet i Shopify. Hvis den fundne varereferencepost indeholder en variantkode, anvendes denne variantkode til at tilknytte Shopify-varianten.|Stregkoden gemmes som **varereference** for vare og varevariant.|

> [!NOTE]  
> Du kan udløse tilknytningen for de valgte produkter/varianter ved at vælge **Prøv Find produkttilknytning** eller alle importerede ikke-tilknyttede produkter **Prøv at finde tilknytninger**.

### <a name="fields-mapping-overview"></a>Oversigt over felttilknytning

|Shopify|Kilde, når den eksporteres fra [!INCLUDE[prod_short](../includes/prod_short.md)]|Destinationen, når den importeres til [!INCLUDE[prod_short](../includes/prod_short.md)]|
|------|-----------------|-----------------|
|Status|Ifølge **Status for oprettede produkter** på **Shopify Produktionskortet**. Få flere oplysninger i sektionen [Ad hoc-opdateringer af Shopify-produkter](synchronize-items.md#ad-hoc-updates-of-shopify-products).|Bruges ikke.|
|Titel | **Beskrivelse**. Hvis sprogkoden er defineret, og der findes en tilsvarende vareoversættelse, bruges vareoversættelsen i stedet for beskrivelse.|**Beskrivelse**|
|Varianttitel | **Variantkode**.|**Beskrivelse** af variant|
|Beskrivelse|Kombinerer udvidede tekster, marketingtekst og attributter, hvis tilsvarende skift er aktiveret på Shopify-produktionskortet. Respekterer sprogkoden.|Bruges ikke.|
|SEO-sidetitel|Fast værdi: tom. Få flere oplysninger i sektionen [Ad hoc-opdateringer af Shopify-produkter](synchronize-items.md#ad-hoc-updates-of-shopify-products).|Bruges ikke.|
|SEO-metabeskrivelse|Fast værdi: tom. Få flere oplysninger i sektionen [Ad hoc-opdateringer af Shopify-produkter](synchronize-items.md#ad-hoc-updates-of-shopify-products).|Bruges ikke.|
|Medier|**Billede**. Få mere at vide i afsnittet [Synkronisere vare billeder](synchronize-items.md#sync-item-images)|**Billede**|
|Pris|Beregningen af slutkundepris beregnes med hensyn til vareprisgruppe, kundeprisgruppe, kunderabatgruppe og valutakode. Få mere at vide i afsnittet [Synkronisere priser](synchronize-items.md#sync-prices-with-shopify)|**Enhedspris**. Prisen importeres kun til nyoprettede varer, men den bliver ikke opdateret i senere versioner.|
|Sammenlign med pris|Beregningen af prisen uden en rabat. Hvis værdien er mindre end eller lig med **Pris**, sender stikket 0 (nul) i stedet for den faktiske værdi.|Bruges ikke.|
|Sager pr. vare|**Kostpris**|**Kostpris**. Kostprisen importeres kun til nyoprettede varer, men den bliver ikke opdateret i senere versioner.|
|Varenummer|Få mere at vide om lagervarer under **SKU-tilknytning** i afsnittet [Eksporter varer til Shopify](synchronize-items.md#export-items-to-shopify).|Få flere oplysninger i sektionen [Effekt af Shopify-SKU-produkter og stregkoder ved tilknytning og oprettelse af varer og varianter i Business Central](synchronize-items.md#effect-of-shopify-product-skus-and-barcodes-on-mapping-and-creating-items-and-variants-in-business-central).|
|Stregkode|**Varereferencer** til stregkodetypen.|**Varereferencer** til stregkodetypen.|
|Lagerbeholdningen vil blive lagerført på| Afhænger af Shopify-butiksplaceringer. Hvis **Business Central-opfyldelsesservicer** har feltet **Placering af standardprodukt** aktiveret, lagerføres og sendes der lager fra **Business Central-opfyldelsesservicer**. Ellers anvendes Shopify primær lokation eller flere lokationer. Få mere at vide i afsnittet [To fremgangsmåder for administration af opfyldelse](synchronize-items.md#two-approaches-to-manage-fulfillments).| Bruges ikke.|
|Spor antal|I henhold til feltet **Lager sporet** på siden **Shopify produktionskortet**. Der er flere oplysninger i [Lager](synchronize-items.md#sync-inventory-to-shopify)-afsnittet. Bruges kun, når du eksporterer et produkt første gang.|Bruges ikke.|
|Fortsætte med at sælge, når der ikke er mere lager|I henhold til **Lager sporet** i **Shopify produktionskortet**.|Bruges ikke.|
|Enhedstype|**Beskrivelse** af **Varekategorikode**. Hvis type ikke er angivet til Shopify, tilføjes den som en brugerdefineret type.|**Varekategorikode**. Tilknytning efter beskrivelse.|
|Leverandør (Kreditor)|**Navn** på kreditor fra **Leverandørnr.**|**Leverandørnr.** Tilknytning efter navn.|
|Vægt|**Bruttovægt**.|Bruges ikke.|
|Skattepligtig|Fast værdi: aktiveret.|Bruges ikke.|
|Momskoder|**Momsgruppekode**. Kun relevant i forbindelse med moms. Få flere oplysninger [Konfigurere moms](setup-taxes.md).|Bruges ikke.|

### <a name="tags"></a>Koder

Gennemse importerede koder i faktaboksen **Koder** på siden **Shopify-produkt**. På samme side redigeres koder ved at vælge handlingen **Koder**.

Hvis indstillingen **Til Shopify** er valgt i feltet **Synkroniser vare**, eksporteres tilknyttede tags til Shopify ved næste synkronisering.

### <a name="unit-of-measure-as-variant"></a>Enhed som variant

Shopify understøtter ikke flere enheder. Hvis du vil sælge samme produkt som f.eks. styk og sæt og bruge forskellige priser eller rabatter, skal du oprette en enhedskode som produktvarianter.
Shopify-connectoren kan konfigureres til at eksportere enheder som varianter eller importere varianter som enhed.

For at aktivere denne funktion skal du bruge felterne **UoM som variant** og **Navn på variantindstilling** på **Shopify-butikskortet**. Felterne er som standard skjulte, så brug tilpasning til at føje dem til siden.

**Bemærkninger om enhed som variant**

* Når produktet importeres til [!INCLUDE[prod_short](../includes/prod_short.md)], oprettes der enheder i connectoren. Du skal opdatere **Antal pr enhed**.
* Når du arbejder med en matrix af varianter, f.eks. farve og UoM, og du vil importere produkter, skal du angive *Varenr. + variantkode* i feltet **SKU-tilknytning** og sørge for, at feltet **SKU** i Shopify har samme værdi for alle enheder og indeholder både varenummer og variantkode.
* I [!INCLUDE[prod_short](../includes/prod_short.md)] beregnes disponering pr. vare/varevariant og ikke pr. enhed. Det betyder, at der tildeles samme disponering til hver variant, der repræsenterer enhed (med hensyn til **Antal pr. Enhed**), hvilket kan føre til tilfælde, hvor den tilgængelige mængde i Shopify ikke er nøjagtig. Eksempel: Vare, der sælges i stk. og kasse med 6. Beholdningen i [!INCLUDE[prod_short](../includes/prod_short.md)] er 6 stk. Varen eksporteres til Shopify tom produkt med to varianter. Når lagersynkroniseringen er udført, vil lagerniveauet i Shopify være 6 for varianten Stk. og 1 for varianten Kasse. Køber kan udforske lageret og se, at produktet er tilgængeligt i begge muligheder og afgive en ordre på 1 kasse. Den næste køber vil se, at Kasse ikke er tilgængelig, men der er stadig 6 stk. Dette vil blive rettet efter næste lagersynkronisering.

### <a name="url-and-preview-url"></a>URL-adresse og URL-adresse til forhåndsvisning

Et element, der føjes til Shopify eller importeres fra Shopify, kan have **URL-adressen** eller udfyldt **Forhåndsversion af URL-adresse**. Feltet **URL-adresse** er tomt, hvis produktet ikke udgives i onlinebutikken, f.eks. fordi dets status er kladde. **URL-adressen** vil være tom, hvis butikken er beskyttet med adgangskode, for eksempel fordi dette er udviklingsbutik. I de fleste tilfælde kan du bruge **Forhåndsversion af URL-adresse** til at kontrollere, hvordan produktet vil se ud, når det er offentliggjort.

## <a name="run-item-synchronization"></a>Kør varesynkronisering

Du kan udføre fuldstændig eller delvis synkronisering af elementer på mange forskellige måder.

### <a name="initial-sync-of-items-from-business-central-to-shopify"></a>Oprindelig synkronisering af varer fra Business Central til Shopify

1. Gå til søgning søg ![Lightbulb, der åbner funktionen Fortæl mig.](../media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **Shopify Produkter**, og vælg det relevante link.
2. Vælg handlingen **Tilføj varer**.
3. Angiv koden i feltet **Butikskode**. Hvis du åbner vinduet **Shopify Produkt** fra vinduet **Butikskort**, bliver Butikskode automatisk udfyldt.
4. Hvis du har konfigureret billed- og lagersynkronisering, kan du medtage dem i den samme proces. Det er praktisk at medtage dem i den samme proces i forbindelse med demoscenarier, eller når der håndteres mindre datamængder.
5. Angiv filtre for varerne efter behov. Du kan f.eks. filtrere efter varenummer eller varekategorikode.
6. Vælg **OK**.

De resulterende varer oprettes automatisk i Shopify med priser. Afhængigt af de valg, du har foretaget, kan billeder og lagerniveauer være medtaget. Handlingen kan tage noget tid, hvis der tilføjes et stort antal elementer.

Alternativt kan du synkronisere ét element ved at vælge **Tilføj til Shopify**- handlingen på siden **Varekort**.  

> [!NOTE]  
> Indledende synkronisering af elementer fra [!INCLUDE[prod_short](../includes/prod_short.md)] til Shopify overvejer ikke indstillingerne **Synkroniser element** og **Kan opdatere Shopify-produkter**. 

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

* **Tom**: Der sker ikke noget. Hvis det er nødvendigt, skal brugeren udføre den ønskede handling fra **Shopify-administratoren**.
* **Status til kladde**: Status for produktet i Shopify er angivet til *Kladde*.
* **Status til arkiveret**: Produkt er arkiveret i Shopify.

## <a name="sync-item-images"></a>Synkroniser varebilleder

Synkronisering af afbildninger kan konfigureres for synkroniserede elementer. Vælg mellem følgende indstillinger:

* **Deaktiveret**: Billedsynkronisering er deaktiveret.
* **Til Shopify**: Billeder af varer eksporteres til Shopify.
* **Fra Shopify**: Billeder fra Shopify importeres til [!INCLUDE[prod_short](../includes/prod_short.md)]

Billedsynkronisering kan initialiseres på to måder.

### <a name="sync-product-images-from-the-shopify-shop-page"></a>Synkronisere produktbilleder fra siden Shopify-butik

1. Gå til søgning ![Lightbulb, der åbner funktionen Fortæl mig.](../media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **Shopify-butikker**, og vælg det relevante link.
2. Marker den butik, som du vil synkronisere billeder til for at åbne **Shopify-butikskortsiden**.
3. Vælg handlingen **Synkroniser produktbilleder**.

### <a name="sync-product-images-from-the-shopify-products-page"></a>Synkronisere produktbilleder fra Shopify-produktvinduet

1. Gå til søgning ![Lightbulb, der åbner funktionen Fortæl mig.](../media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **Shopify Produkter**, og vælg det relevante link.
2. Vælg handlingen **Synkroniser produktbilleder**.

### <a name="image-synchronization-remarks"></a>Bemærkninger til billedsynkronisering

* Når du eksporterer billeder fra [!INCLUDE[prod_short](../includes/prod_short.md)] til Shopify, erstatter billederne dem, du har eksporteret tidligere. De tidligere billeder er ikke længere tilgængelige.
* Hvis du sletter et billede i [!INCLUDE[prod_short](../includes/prod_short.md)], bliver billedet Shopify ikke også slettet. Du skal manuelt slette de gamle billeder i **Shopify-administratoren**.
* De billeder, du eksporterer til Shopify, skal opfylde Shopify-kravene. Ellers kan du ikke indlæse dem. Du kan finde flere oplysninger om mediekrav i [Produktmedietyper på help.shopify.com](https://help.shopify.com/en/manual/products/product-media/product-media-types#images).

## <a name="sync-prices-with-shopify"></a>Synkroniser priser med Shopify

Du kan bruge følgende indstillinger til at administrere processen med at eksportere priser:

|Felt|Beskrivlse|
|------|-----------|
|**Debitorprisgruppe**|Bestemmer prisen på en vare i Shopify. Salgsprisen for denne Debitorprisgruppe er taget. Hvis der ikke er angivet en gruppe, bruges prisen på varekortet.|
|**Debitorrabatgruppe**|Angiv den rabat, der skal bruges til beregning af prisen på en vare i Shopify. Rabatpriser lagres i feltet **Pris**, og den fulde pris lagres i feltet **Sammenlign med pris**.|
|**Tillad linjerabat**|Angiver, om linjerabat er tilladt ved beregning af priser for Shopify. Denne indstilling gælder kun for priser på varen. Priserne for debitorprisgruppen kan f. eks. skifte til linjer.|
|**Priser inkl. moms**|Angiver, om prisberegbninger for Shopify skal inkludere moms. Få flere oplysninger [Konfigurere moms](setup-taxes.md).|
|**Momsvirksomhedsbogf.gruppe**|Angiver, hvilken momsvirksomhedsbogføringsgruppe bruges til at beregne priser i Shopify. Dette skal være den gruppe, du bruger til indenlandske debitorer. Få flere oplysninger [Konfigurere moms](setup-taxes.md).|
|**Valutakode**|Husk at angive en Valutakode, hvis din online-butik bruger en anden valuta end den relevante regnskabsvaluta. Der skal være konfigureret valutakurser for den angivne valuta. Hvis dit onlineindkøb bruger samme valuta som [!INCLUDE[prod_short](../includes/prod_short.md)], skal du lade feltet stå tomt.|

Priser for synkroniserede varer kan eksporteres på to måder, der er beskrevet nedenfor.

### <a name="sync-prices-from-the-shopify-products-page"></a>Synkronisere priser fra siden Shopify-produkter

1. Gå til søgning ![Lightbulb, der åbner funktionen Fortæl mig.](../media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **Shopify Produkter**, og vælg det relevante link.
2. Vælg handlingen **Synkroniser priser til Shopify**.

### <a name="price-calculation-remarks"></a>Bemærkninger til prisberegning

* Når du fastlægger en pris, [!INCLUDE[prod_short](../includes/prod_short.md)] bruges logikken "laveste kurs". Den laveste pris logik ignorerer imidlertid den salgspris, der er defineret på varekortet, hvis der er defineret en pris i prisgruppen. Dette gælder også, hvis vareprisen fra varekortprisen er lavere.
* Med henblik på beregning af priser opretter forbindelsen et midlertidigt salgstilbud på varen med et antal på 1 og bruger beregningslogik for standardpris. Kun priser og rabatter, der er gældende for antal 1, bruges. Du kan ikke eksportere forskellige priser eller rabatter baseret på antal.
* Connectoren sender en anmodning om at opdatere priserne i Shopify, hvis prisen i [!INCLUDE[prod_short](../includes/prod_short.md)] er ændret. Hvis du for eksempel synkroniserede produkter og priser og derefter ændrede en pris i Shopify, vil handlingen **Synkroniser priser til Shopify** ikke have nogen indflydelse på prisen i Shopify, da ny pris beregnet af connector er den samme som pris gemt i Shopify Variant fra tidligere synkronisering. **Sammenlign til pris** opdateres kun, hvis hovedprisen er ændret.

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
6. Vælg den lager beregningsmetode, der skal bruges til de valgte Shopify-lokationer.
7. Aktivér **Standardproduktplacering**, hvis lokationen skal bruges til oprettelse af lagerposter og deltage i synkroniseringen af lageret.

Du kan initialisere lagersynkronisering på to måder, som beskrevet herunder.

### <a name="sync-inventory-from-the-shopify-shop-page"></a>Synkronisere lager fra Shopify-butiksvinduet

1. Gå til søgning ![Lightbulb, der åbner funktionen Fortæl mig.](../media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **Shopify-butikker**, og vælg det relevante link.
2. Marker den butik, som du vil synkronisere lager med for at åbne **Shopify Butikskort**-siden.
3. Vælg handlingen **Synkroniser lager**.

### <a name="sync-inventory-from-the-shopify-products-page"></a>Synkronisere lager fra Shopify-produktsiden

1. Gå til søgning ![Lightbulb, der åbner funktionen Fortæl mig.](../media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **Shopify Produkter**, og vælg det relevante link.
2. Vælg handlingen **Synkroniser lager**.

### <a name="inventory-remarks"></a>Lagerokmmentarer

* Der er to standardmetoder til lagerberegning: **Planlagt disponible resultat til dato** og **Fri lagerbeholdning (ikke reserveret)**. Du kan også bruge udvidelsesmulighederne til at tilføje flere indstillinger. Du kan få mere at vide om udvidelser ved at gå til [eksempler](/dynamics365/business-central/dev-itpro/developer/devenv-extending-shopify#stock-calculation). 
* Du kan kontrollere de modtagne lageroplysninger fra Shopify på siden **Shopify Lager-faktaboks**. I denne faktaboks får du en oversigt over Shopify-lagerbeholdningen og den sidst beregnede lagerbeholdning i [!INCLUDE[prod_short](../includes/prod_short.md)]. Der er en post pr. lokation.
* Hvis lageroplysningerne i Shopify er forskellige fra **Planlagt disponibel resultat** i [!INCLUDE[prod_short](../includes/prod_short.md)], opdateres lageret i Shopify.
* Når du tilføjer en ny placering i Shopify, skal du også tilføje lagerposter for den. Shopify gør det ikke automatisk for eksisterende produkter og varianter, og connector synkroniserer ikke lagerniveauer for de pågældende varer på en ny lokation. Hvis du vil vide mere, skal du gå til [Tildele lagervarer til lokationer](https://help.shopify.com/manual/locations/assigning-inventory-to-locations).
* Både **Business Central-opfyldelsesservicer** og normale lokationer understøttes og kan bruges til levering og lager.

#### <a name="example-of-calculation-of-projected-available-balance"></a>Eksempel på beregning af planlagt disponibel balance

Der er 10 enheder af varen tilgængelig på lager og to udestående salgsordrer. En for mandag med mængde *En* og en for torsdag med antal *To*. Afhængigt af, hvornår du synkroniserer lageret, opdaterer systemet lagerniveauet Shopify med forskellige mængder:

|Når der køres synkroniseringslager|Værdi, der bruges til at opdatere lagerniveau|Kommentar|
|------|-----------------|-----------------|
|Tirsdag|9|Lagerbeholdning 10 minus angivet i salgsordre til afsendelse mandag|
|Fredag|7|Lager 10 minus begge salgsordrer|

### <a name="two-approaches-to-manage-fulfillments"></a>To fremgangsmåder for administration af opfyldelse

Der er to måder at håndtere opfyldelse på i Shopify:

* "Indbygget" Shopify-opfyldelse og lagersporing
* Tredjepartsopfyldelse og lagersporing

Lagerbeholdning for hvert produkt i Shopify kan enten lagerføres af Shopify eller af tredjepart.

Hvis du bruger Shopify-opfyldelse, kan du også definere flere lokationer i Shopify. Når ordren er oprettet, vælger Shopify lokation baseret på tilgængelighed og prioritet. Du kan også angive, på hvilke lokationer du planlægger at spore et bestemt produkt, for eksempel aldrig sælge fra lokation *ShowRoom*.

Hvis du bruger tredjepart, håndteres den fysiske håndtering af tredjepartsudbyderen, så lokationer er ikke nødvendige. I forbindelse med tredjepart bliver SKU-feltet obligatorisk.

Når du beslutter, hvilken lokation der skal spores varer på, opretter Shopify poster i tabellen **Lagerniveauer**, som kan opdateres manuelt med varedisponering.

Connector understøtter begge tilstande. Det kan sende lager til flere Shopify-lokationer eller fungere som opfyldelsesservice.

Fra et [!INCLUDE[prod_short](../includes/prod_short.md)]-perspektiv kan du, når du opretter en vare og vil sende den til Shopify, skal du også:

* Bruge til/fra-knappen **Standardproduktplacering** til at angive, om denne vare skal opfyldes af Shopify eller af 3PL. Der er altid en **Business Central-opfyldelsesservice**, men der kan være flere opfyldelsesservicer, hvis der installeres flere apps. Du kan kun aktivere **Standardproduktplacering** i én post, hvis du vil bruge en opfyldelsesservice. 
* Brug til/fra-knappen **Standardproduktplacering** til at angive, hvilke lokationer du vil bruge til at spore lagerbeholdning. Du kan aktivere **Standardproduktplacering** for flere placeringer, hvor **Er opfyldelsesservice** er deaktiveret. Bemærk, at lagerbeholdning altid spores for primær lokation.

#### <a name="whats-the-difference"></a>Hvad er forskellen?

Shopify-opfyldelse er nyttig, når du bruger Shopify POS, og der er flere fysiske butikker. Du ønsker, at medarbejderen i den fysiske butik skal kende den aktuelle lagerbeholdning. I dette tilfælde opretter du flere lokationer i Shopify, flere lokationer i [!INCLUDE[prod_short](../includes/prod_short.md)] og aktiverer **Standardproduktplacering** for alle disse lokationer.  

Hvis logistik håndteres i [!INCLUDE[prod_short](../includes/prod_short.md)], hvor der kan være så mange lokationer som nødvendigt, der repræsenterer distributionscentre, opretter du ikke lokationer i Shopify, opretter Business Central-opfyldelsesservicer, og du kan linke lager via lokationsfiltre fra flere lokationer til én post for opfyldelsesservice. Som følge heraf er der ingen oplysninger i Shopify om, hvor varer sendes fra - det har kun sporingsoplysninger, mens i [!INCLUDE[prod_short](../includes/prod_short.md)] kan du vælge baseret på tilgængelighed og nærhed til destinationen.

#### <a name="example-of-using-default-product-location-toggle"></a>Eksempel på brug af til/fra-knappen Standardproduktplacering

Når du har valgt handlingen **Hent Shopify-placeringer** på siden **Shopify-lokationer**, kan du se følgende placeringer:

|Navn|Er opfyldelsesservice|Er primær|
|------|-----------------|-----------------|
|Primær| |**Ja**|
|Sekundær| | |
|Business Central-opfyldelsesservice|**Ja**| |

Lad os se på virkningen af aktivering af til/fra-knappen Standardproduktplacering:

|Navn på lokationer, hvor til/fra-knappen Standardproduktplacering er slået til|Indvirkning på, hvordan produktet oprettes i Shopify|
|------|-----------------|
|Primær| Lagerbeholdningen lagerføres på: Flere lokationer; Udvalgte lokationer: Primær |
|Primær og sekundær| Lagerbeholdningen lagerføres på: Flere lokationer; Udvalgte lokationer: Primær og sekundær |
|Business Central-opfyldelsesservice|Lagerbeholdningen lagerføres på: Business Central-opfyldelsesservice; Valgte lokationer: (App) Business Central-opfyldelsesservice|
|Business Central-opfyldelsesservice og primær| Fejl: Du kan ikke bruge Shopify-standardplaceringer med opfyldelsesserviceplaceringer|

## <a name="see-also"></a>Se også

[Kom i gang med Connectoren til Shopify](get-started.md)  
