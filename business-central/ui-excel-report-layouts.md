---
title: Arbejde med Excel-layouts
description: Få mere at vide om, hvordan du kan oprette og redigere rapportlayout, der er oprettet ved hjælp af Excel.
author: jswymer
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: customized report, document layout, logo, personalize
ms.search.form: 9650, 9652
ms.date: 03/14/2022
ms.author: jswymer
ms.openlocfilehash: c0800642804b8e8c9e1dc629224bfac77b174500
ms.sourcegitcommit: 00a8acc82cdc90e0d0db9d1a4f98a908944fd50a
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 06/29/2022
ms.locfileid: "9075729"
---
# <a name="working-with-excel-layouts"></a>Arbejde med Excel-layouts

Excel-rapportlayout er baseret på Microsoft Excel-projektmapper (.xlsx-filer). De giver dig mulighed for at oprette rapporter ved hjælp af velkendte Excel-funktioner til sammenfatning, analyse og præsentation af data, f. eks. formler, pivottabeller og pivotdiagrammer.

![Viser et eksempel på et Excel-layout.](media/excel-layout-2.png)

I denne artikel forklares nogle af de vigtigste ting, du skal vide for at komme i gang med Excel-layout.

## <a name="why-use-excel-layouts"></a>Hvorfor bruge Excel-layout?

Her er nogle flere fordele ved at bruge Excel-layout:

- Oprette interaktive rapporter ved hjælp af visuelle effekter som udsnit
- Få vist rådata fra rapportens datasæt med henblik på at forstå, hvordan rapporten fungerer, og hvor dataene om visuelle elementer kommer fra
- Brug indbyggede Office-funktioner til efter behandling af gengivne rapporter som f. eks.:
  - [Beskytte regnearkene](https://support.microsoft.com/en-us/office/protect-a-worksheet-3179efdb-1285-4d49-a9c3-f4ca36276de6)
  - [Anvende følsomhedsbeskrivelser](https://support.microsoft.com/en-us/office/apply-sensitivity-labels-to-your-files-and-email-in-office-2f96e7cd-d5a4-403b-8bd7-4cc636bae0f9)
  - [Tilføje kommentarer og noter](https://support.microsoft.com/en-us/office/insert-comments-and-notes-in-excel-65f504d8-160b-4a05-ac30-46fbd5227a52)
  - [Prognoser og analyser](https://support.microsoft.com/en-us/office/introduction-to-what-if-analysis-22bffa5f-e891-4acc-bf7a-e4645c446fb4) 
- Brug installerede tilføjelsesprogrammer og app-integrationer, f. eks Power Automate-flow eller OneDrive.

## <a name="get-started"></a>Kom i gang

Der er grundlæggende to opgaver involveret i oprettelse af et Excel-layout på en rapport:

1. Opret den nye Excel-layoutfil.
2. Føj det nye layout til rapporten.

## <a name="task-1-create-the-excel-layout-file"></a>Opgave 1: Opret den nye Excel-layoutfil

Du kan oprette en Excel-fil med en rapport, der er forklaret i dette afsnit, på tre måder

### <a name="from-any-report"></a>[Fra enhver rapport](#tab/any-report)

Du kan bruge følgende fremgangsmåde til at oprette et Excel-layout fra enhver rapport uanset den aktuelle layouttype. Excel-layoutet vil indeholde det krævede **dataark** og den krævede tabel, et **Rapport-metadata**-ark og intet andet.

[!INCLUDE[open-report-layouts-page](includes/open-report-layouts-page.md)]
2. Vælg et layout til rapporten i oversigten **Rapportlayout**, og vælg derefter **Kør rapport**.
3. Vælg **Send til** > **Microsoft Excel-dokument (kun data)** > **OK** på siden med rapportanmodning.

   Dette trin henter en Excel-projektmappe, der indeholder rapportdata sættet.
4. Åbn den downloadede Excel-fil, foretag dine opdateringer, og gem derefter filen.

### <a name="from-another-excel-layout-on-a-report"></a>[Fra et andet Excel-layout på en rapport](#tab/other-layout)

Hvis der allerede findes et Excel-layout til en rapport, skal du bruge det eksisterende layout som udgangspunkt. Du kan få en kopi af layoutet på to måder. Du kan eksportere det eksisterende layout fra siden **Rapportlayout** eller hente layoutet fra rapportens anmodnings side. Begge måder at hente en Excel-fil, der indeholder alle arkene i den eksisterende fil. Forskellen er, at på anmodningssiden, vil layoutet indeholde faktiske data. Dataene er ikke nødvendige, men den hjælper, når du designer layoutet.

#### <a name="approach-1-export-the-layout-from-the-report-layouts-page"></a>Metode 1: Eksporter layoutet fra siden **Rapportlayout**

[!INCLUDE[open-report-layouts-page](includes/open-report-layouts-page.md)]
2. Vælg Excel-layoutet på listen, og vælg handlingen **Eksporter layout** øverst på siden.
3. Åbn den downloadede Excel-fil, foretag dine opdateringer, og gem derefter filen.

#### <a name="approach-2-download-the-layout-from-the-reports-request-page"></a>Metode 2: Hent layoutet fra rapportens anmodnings side

[!INCLUDE[open-report-layouts-page](includes/open-report-layouts-page.md)]
2. Vælg et layout til rapporten i oversigten **Rapportlayout**, og vælg derefter **Kør rapport**.
3. Vælg **Download** på rapportanmodningssiden.
4. Åbn den downloadede Excel-fil, foretag dine opdateringer, og gem derefter filen.

### <a name="from-al-code"></a>[Fra AL-kode](#tab/from-code)

Denne måde er den mest avancerede. Det kræver viden om AL kode, så it-programmører bliver til destination. Excel-layoutene er i dette tilfælde en del af en udvidelsespakke, som du installerer. Du kan finde flere oplysninger i [Oprette en Excel-layourrapport](/dynamics365/business-central/dev-itpro/developer/devenv-howto-excel-report-layout) i hjælp til udviklere og it-eksperter.

---

## <a name="task-2-add-the-excel-layout-to-the-report"></a>Opgave 2: Tilføje Excel-layout til rapporten

Når du har layout filen i Excel, skal den næste opgave tilføjes som et nyt layout til rapporten.

[!INCLUDE[open-report-layouts-page](includes/open-report-layouts-page.md)]
2. Vælg **Nyt Layout**.
3. Indstil **rapport-id** til at rapportere.
4. Angiv et navn i **Layout-navn**.
5. Angiv **Formatindstillinger** til **Excel**.
6. Klik på **OK** > **Vælg** for at åbne Stifinder på enheden. 
7. Find og vælg Excel-filen, og vælg derefter **Åbn**.

   Den valgte fil overføres til layoutet, og du vender tilbage til siden med siden **Rapport-layouts**.
8. Hvis du vil se, hvordan rapporten ser ud med det nye layout, skal du vælge layoutet på listen og derefter vælge **Kør rapport**.


<!--

**Data** sheet
  - An Excel layout must contain a sheet named **Data**.
  - The **Data** sheet can only include one table named **Data**.

**Data** table
  - The **Data** sheet must include a table that has the name **Data**.
  - The table must have at least one column and can only include columns that are also in report dataset.
  - The table must start in the first cell A1 of the **Data** sheet.

3. Report Metadata 
-->

## <a name="understanding-excel-layouts"></a>Om Excel-layout

Der er få ting, du skal kende eller overveje, når du begynder at oprette eller ændre Excel-layout. Alle Excel-layout skal indeholde to elementer: et **dataark** og en **datatabel**. Disse elementer fra basis af layoutet ved at definere forretningsdataene fra Business central, som du kan arbejde med. Du kan betragte **Dataarket** som en type kontrakt mellem layoutet i forretningsdataene. Disse data bruges som kilde til beregninger og visuelle effekter, som du vil vise i andre ark.

Der er bestemte krav til strukturen i Excel-projektmappen. Hvis kravene ikke er opfyldt, har du problemer med at bruge layoutet. I følgende diagram og tabel opstilles elementerne i et Excel-layout og kravene.

[![Viser forskellige elementer i et Excel-layout.](media/excel-layout-callouts-2.png)](media/excel-layout-callouts-2.png#lightbox)

|Nummer|Element|Beskrivlse|Obligatorisk|
|---|-------|----|---|
|1|**Dataark**|<ul><li>Skal have **Data**</li><li>Kun kan indeholde én tabel, og tabellen skal navngives **Data**</li></ul>|![Er obligatorisk](media/check.png) | 
|2|**Datatabel**|<ul><li>Skal have **Data**</li><li>Der skal være mindst én kolonne.</li><li>Der kan kun være kolonner i rapportdatasættet.</li><li>Skal starte i den første celle **A1** i **dataarket**</li></ul>|![Er obligatorisk](media/check.png)|
|3|Diagramark|<ul><li>Bruges til at vise data.</li><li>Dataene stammer fra **dataarket**. </li></ul>||
|4|**Rapportmetadataark**|<ul><li>Medtages automatisk, hvis layoutet blev oprettet ved at eksportere en anden rapport som Excel</li><li>Indeholder generelle oplysninger om rapporten</li><li>Kan slettes</li></ul>|

Sådan opsummeres det, du kan og ikke kan gøre i **dataark**:

- Du må ikke ændre navnet på **dataarket**, **datatabel** eller kolonnerne.
- Du kan slette eller skjule kolonner.
- Undlad at tilføje kolonner, medmindre de medtages i rapportens datasæt.
- Du kan placere arkene i vilkårlig rækkefølge. F.eks. **Dataarket** kan være først eller sidst.

## <a name="see-related-training-at-microsoft-learn"></a>Se relateret oplæring på [Microsoft Learn](/learn/modules/change-documents-dynamics-365-business-central/index)

## <a name="see-also"></a>Se også

[Administration af rapportlayout](ui-manage-report-layouts.md)  
[Ændre det aktuelle rapportlayout](ui-how-change-layout-currently-used-report.md)  
[Importere og eksportere et brugerdefineret rapport- eller dokumentlayout](ui-how-import-and-export-report-layout.md)  
[Arbejde med rapporter, kørsler og XMLporte](ui-work-report.md)  
[Forberede Financial Reporting med kontoskemaer og kontokategorier](bi-how-work-account-schedule.md)  
[Business Intelligence](bi.md)  
[Arbejde med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  
[Analyse af rapportdata med Excel](report-analyze-excel.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]