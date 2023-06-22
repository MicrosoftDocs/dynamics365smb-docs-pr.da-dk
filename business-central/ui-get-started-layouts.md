---
title: Introduktion til oprettelse af layout
description: 'Lær, hvordan du kan oprette brugerdefinerede layout for at tilpasse udseendet af en rapport, når den vises, udskrives eller gemmes.'
author: jswymer
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 'customized report, document layout, logo, personalize'
ms.search.form: '9650, 9652'
ms.date: 03/23/2022
ms.author: jswymer
---
# <a name="get-started-creating-report-layouts" />Introduktion til oprettelse af rapportlayout

Business central leveres med mange indbyggede layouts, som du kan bruge i rapporter. Andre layouts kan være tilføjet som en del af andre udvidelser. Men du kan også oprette dine egne rapporter fra bunden eller ud fra et eksisterende layout.

> [!IMPORTANT]
> Du kan også bruge rapportlayouts til at føje indhold til e-mailmeddelelser. F.eks. rapportlayout kan spare tid og være med til at sikre konsistensen ved at genbruge det samme indhold, når du kommunikerer med kunderne. Hvis du vil bruge brugerdefinerede rapportlayout med e-mail, skal det være et Word-filtypeformat. Du kan ikke bruge RDLC-filtypen. Du kan finde flere oplysninger i [angive genanvendelige e-mail-tekst og layout](admin-how-setup-email.md#set-up-reusable-email-texts-and-layouts). 

## <a name="overview" />Oversigt

Når du arbejder med rapportlayout, er det en hjælp at tænke på layoutet som en fil, der importeres og tildeles til en rapport. Uanset layouttypen er det grundlæggende at administrere layout i Business central. Normalt kommer du til at arbejde fra siden **rapportlayout**. Den væsentligste forskel er, hvordan du designer layoutet, hvilket gøres ved hjælp af den programsoftware, som layoutet bygger på, f. eks. Word, Excel eller SQL Server Report Builder.

Med dette begreb. der er grundlæggende tre eller fire opgaver involveret i oprettelse af et layout på en rapport:

1. Vælg layouttype.
2. Eksportere en kopi af et eksisterende layout, der skal bruges som udgangspunkt.
3. Foretage ændringer af layout filen i det relevante program.
4. Tilføje den nye layoutfil til rapporten.

> [!IMPORTANT]
> Du kan ikke ændre eller erstatte et udvidelseslayout, hvilket er et layout, der stammer fra en forlængelse. Kun brugerdefinerede layout kan ændres eller fjernes. På siden **Rapportlayout** kan du se, om layout er et udvidelseslayout eller brugerdefineret layout ved at se på kolonnen **Udvidelse**. Et udvidelseslayout viser oplysninger om kildeudvidelsen i kolonnen. **Udvidelseskolonnen** vil være tom for et brugerdefineret layout.
>
> Du kan få mere at vide om forskellen mellem udvidelses layout og brugerdefinerede layout i [layoutkilde](ui-manage-report-layouts.md#layout-sources).

## <a name="get-started" />Kom i gang

Afhængigt af hvad din situation er, vil de faktiske opgaver variere. Brug følgende tabel som en hjælp til at komme i gang.

|Hvad vil du foretage dig?|Se...|
|-----------------------|------|
|Finde ud af den bedste layouttype, som du kan bruge i min situation|[Bestemme, hvilken type layout du vil bruge](#decide)|
|Oprette et nyt layout til en rapport, der er baseret på et eksisterende layout, så det aktuelle layout holdes.|[Oprette et nyt layout](#create)|
|Ændre et eksisterende layout, der bruges i en rapport|[Redigere et layout](#modify)|
|Jeg har en ny version af en fil med en layout til en rapport. Jeg vil erstatte den eksisterende layoutfil.|[Erstat et layout](#replace)|
|Ændre det aktuelle layout, som bruges af en rapport, til et andet layout|[Angive det layout, der bruges af en rapport](ui-set-report-layout.md)|
|Ændre et layouts navn og beskrivelse|[Omdøbe et layout](#rename)|

## <a name="a-namedecideadecide-what-type-of-layout-you-want" /><a name="decide"></a>Bestemme, hvilken type layout du vil bruge

Det første, når du opretter et layout, er at bestemme, hvilken [layouttype](ui-manage-report-layouts.md#layout-types) du vil have. Du kan vælge mellem Word, Excel eller RDLC. Layouttypen afhænger af, hvordan den genererede rapport skal se ud. Desuden afhænger det af din viden om programsoftware til oprettelse af layouterne, f. eks. Word, Excel og SQL Server Report Builder.

<!--
* The process for setting up Word, Excel, and RDLC layouts on reports is the same. The main difference is in the way you modify the layouts. Excel and Word layouts are typically easier to create and modify than RDLC layouts because you use Word and Excel. RDLC report layouts are modified by using SQL Server Report builder, which targets more advanced users.-->

* Excel-layout er generelt den letteste at oprette og ændre, fordi de funktioner, der bruges til at opsummere data, tilføje grafik og design, er almindelige Excel-funktioner.

* Ikke alle rapporter og dokumenter har et datasæt, der er optimeret til brug med et Excel-layout. Aggregeringer og komplekse beregninger fungerer bedst med RDLC-eller Word-layout. Det samme gælder for dokumenter.

* Hvis du kun foretager typografiændringer som f. eks. skrifttype, størrelse og farve, er et Word-layout også et godt valg.

* At tilføje datafelter eller arrangere datafelter i Word eller RDLC er mere avancerede end med Excel.

* Word-og RDLC layout kan bruges til rapporter, der skal udskrives til sidst.  

* De generelle designkoncepter for Word- og RDLC-layout er ens. Hver type har visse designfunktioner, der påvirker, hvordan den genererede rapport skal vises i [!INCLUDE[prod_short](includes/prod_short.md)]. Den samme rapport måske ser anderledes ud, når du bruger Word-rapportlayout sammenlignet med RDLC-rapportlayoutet.

## <a name="a-namecreateacreate-a-new-layout" /><a name="create"></a>Oprette et nyt layout

Du kan oprette et nyt layout på baggrund af et eksisterende layout på to måder. Den ene måde er at gemme det eksisterende layout i en kopi. Den anden måde er at eksportere det eksisterende layout.

## [Kopierer](#tab/copy)

Ved at kopiere kan du hurtigt oprette et nyt layout, der er det samme som et eksisterende layout. Når du har kopieret, skal du foretage ændringerne ved at eksportere layoutet. 

[!INCLUDE[open-report-layouts-page](includes/open-report-layouts-page.md)]
2. Vælg det layout, som du vil have en kopi af det nye layout, og vælg derefter handlingen **Rediger oplysninger**.

    Hvis du har valgt et udvidelses layout, bliver du spurgt, om du vil redigere en kopi. Vælg **Ja** for at fortsætte.

    > [!TIP]
    > Hvis du vil have hjælp til at finde layoutet, skal du bruge feltet **Søg**, ruden **Filter** og kolonnerne sortere.
3. Ændre **layout-navnet**.
4. Aktiver kopien **Gem ændringer, der skal kopieres** til **Vælg** og derefter **OK**

   Det nye layout vises på siden **Rapportlayout**.
5. Hvis du vil ændre det nye layout, skal du se [Ændre et eksisterende layout](#modify).

### [Eksportere/importere](#tab/export)

[!INCLUDE[open-report-layouts-page](includes/open-report-layouts-page.md)]
2. Vælg det layout, som du vil have en kopi af det nye layout, og vælg derefter handlingen **Eksportere layout**.

   Layout-filen vil blive downloadet på din enhed. 

    > [!TIP]
    > Hvis du vil have hjælp til at finde layoutet, skal du bruge feltet **Søg**, ruden **Filter** og kolonnerne sortere.

3. Åbn layout filen i det relevante program, f. eks. Word (for en. docx-fil) eller Excel (til en. xlsx-fil).

   Du kan finde flere oplysninger i:

   * [Arbejd med Word-layouts](ui-how-add-fields-word-report-layout.md)
   * [Arbejd med Excel-layouts](ui-excel-report-layouts.md)
   * [Arbejd med RDLC-layouts](ui-rdlc-report-layouts.md)

   Foretag ændringer af filen, og Gem den.

4. Tilbage til **Rapportlayouts** vælge handlingen **Nyt layout**.
5. Udfyld følgende felter:

   |Felt|Beskrivlse|Obligatorisk|
   |-----|-----------|---------|
   |Rapport-id|Konfigurere det id, der er knyttet til rapporten|ja|
   |Layoutnavn| Skriv et kort beskrivelsesnavn til layoutet, så du let kan identificere det.|ja|
   |Beskrivlse| Skriv mere detaljerede oplysninger om layoutet. |nummer|
   |Formateringsindstillinger|Angive dette felt, så det svarer til layouttypen, f. eks. Word, Excel eller RDLC.|ja|

6. Vælg **OK**, og benyt derefter en af følgende fremgangsmåder for at uploade layout-filen til rapporten:

   [!INCLUDE[file-upload](includes/file-upload.md)]

   Den valgte fil overføres til layoutet, og du vender tilbage til siden med siden **Rapport-layouts**.

Hvis du vil se, hvordan rapporten ser ud med det nye layout, skal du vælge layoutet på listen og derefter vælge **Kør rapport**.

---

## <a name="a-namemodifyamodify-a-layout" /><a name="modify"></a>Redigere et layout

Benyt følgende fremgangsmåde for at ændre et eksisterende brugerdefineret layout.

[!INCLUDE[open-report-layouts-page](includes/open-report-layouts-page.md)]
2. Vælg det layout, som du vil redigere, og vælg derefter handlingen **Eksporter layout**.

   Layout-filen vil blive downloadet på din enhed. 

   > [!TIP]
   > Hvis du vil have hjælp til at finde layoutet, skal du bruge feltet **Søg**, ruden **Filter** og kolonnerne sortere.

3. Åbn layout filen i det relevante program, f. eks. Word (for en. docx-fil) eller Excel (til en. xlsx-fil).

   Du kan finde flere oplysninger i:

   * [Arbejd med Word-layouts](ui-how-add-fields-word-report-layout.md)
   * [Arbejd med Excel-layouts](ui-excel-report-layouts.md)
   * [Arbejd med RDLC-layouts](ui-rdlc-report-layouts.md)

   Foretag ændringer af filen, og Gem den.

4. På siden **Rapportlayout** skal du vælge det eksisterende layout og derefter vælge handlingen **Erstat layout**.
5. Klik på **OK** > **Vælg** for at åbne Stifinder på enheden.
6. Find og vælg Excel-filen, og vælg derefter **Åbn**.

   Den valgte fil overføres til layoutet, og du vender tilbage til siden med siden **Rapport-layouts**.
7. Hvis du vil se, hvordan rapporten ser ud med det nye layout, skal du vælge layoutet på listen og derefter vælge **Kør rapport**.

## <a name="a-namereplaceareplace-a-layout" /><a name="replace"></a>Erstat et layout

Følg disse trin for at erstatte den eksisterende brugerdefinerede fil med en ny fil.

[!INCLUDE[open-report-layouts-page](includes/open-report-layouts-page.md)]
2. Vælg det eksisterende layout, og vælg derefter handlingen **Erstat layout**.
3. Klik på **OK** > **Vælg** for at åbne Stifinder på enheden.
4. Find og vælg Excel-filen, og vælg derefter **Åbn**.

   Den valgte fil overføres til layoutet, og du vender tilbage til siden med siden **Rapport-layouts**.
5. Hvis du vil se, hvordan rapporten ser ud med det nye layout, skal du vælge layoutet på listen og derefter vælge **Kør rapport**.

## <a name="a-namerenamearename-a-layout" /><a name="rename"></a>Omdøbe et layout

Følg disse trin, hvis du vil ændre navnet på og beskrivelsen af et brugerdefineret layout.

[!INCLUDE[open-report-layouts-page](includes/open-report-layouts-page.md)]
2. Vælg det layout, som du vil omdøbe, og vælg derefter handlingen **Rediger oplysninger**.

    > [!TIP]
    > Hvis du vil have hjælp til at finde layoutet, skal du bruge feltet **Søg**, ruden **Filter** og kolonnerne sortere.
3. Skift **layout-navn**, og vælg derefter **OK**.

## <a name="see-related-microsoft-trainingtrainingmoduleschange-documents-dynamics--business-centralindex" />Se relateret [Microsoft-træning](/training/modules/change-documents-dynamics-365-business-central/index)

## <a name="see-also" />Se også

[Administration af rapportlayout](ui-manage-report-layouts.md)  
[Arbejde med Word-layouts](ui-how-add-fields-word-report-layout.md)  
[Arbejde med Excel-layouts](ui-excel-report-layouts.md)  
[Arbejde med rapporter, kørsler og XMLporte](ui-work-report.md)  
[Arbejde med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
