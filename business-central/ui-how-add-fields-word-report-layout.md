---
title: 'Fremgangsmåde: Føje felter til et Word-rapportlayout'
description: 'Beskriver, hvor du tilføjer felter fra et rapportdatasæt til et eksisterende Word-rapportlayout for en rapport.'
author: jswymer
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: null
ms.date: 11/25/2021
ms.author: jswymer
---

# <a name="work-with-word-layouts" />Arbejde med Word-layouts

Et Word-rapportlayout bestemmer en rapports indhold og format, når den vises og udskrives fra Business central. Du opretter og redigerer disse layout ved hjælp af Microsoft Word.

[![Eksempel på et dokument med Word-rapportlayout til Business Central.](media/word-layout.png)](media/word-layout.png#lightbox) 

Når du ændrer et Word-rapportlayout, angiver du de felter i rapport sættet, der skal medtages i rapporten, og hvordan felterne arrangeres. Du kan også definere rapportens standardformat, f. eks. tekst skrifttype og størrelse, margener og baggrundsbilleder. Du skal typisk arrangere rapportens indhold ved at føje tabeller til layoutet.

Hvis du vil foretage generelle formaterings- og layoutændringer, f.eks. skifte skrifttype, tilføje og redigere en tabel eller fjerne et datafelt, skal du blot bruge de grundlæggende funktioner til redigering i Word, som du gør med ethvert Word-dokument.

Hvis du designer et Word-rapportlayout fra bunden eller tilføjer nye datafelter, skal du starte med at tilføje en tabel med rækker og kolonner, der efterhånden indeholder datafelter.

> [!TIP]  
> Vis tabelgitterlinjer, så du kan se grænserne for tabelceller. Husk at skjule gitterlinjerne, når du er færdig med redigering. Hvis du vil vise eller skjule tabelgitterlinjer, skal du vælge tabellen og derefter vælge på **Vis gitterlinjer** under **Layout** under fanen **Tabel**.

## <a name="embedding-fonts-in-word-layouts-for-consistency" />Integrere skrifttyper i Word-layout for at skabe ensartethed

For at sikre, at rapporter altid vises og udskrives med de ønskede skrifttyper, uanset hvor brugere åbner eller udskriver rapporter, kan du integrere skrifttyperne i Word-dokumentet. Du skal dog være opmærksom på, at integrering af skrifttyper kan øge størrelsen på Word-filer. Du kan finde flere oplysninger om integrering af skrifttyper i Word i [Integrere skrifttyper i Word, PowerPoint eller Excel](https://support.office.com/article/Embed-fonts-in-Word-PowerPoint-or-Excel-cb3982aa-ea76-4323-b008-86670f222dbc).

## <a name="adding-data-fields" />Tilføje datafelter

Et datasæt i rapporten kan bestå af felter, der viser navne, data og billeder. I dette emne beskrives fremgangsmåden for tilføjelse af felter fra et rapportedatasæt i et eksisterende Word-rapportlayout for en rapport. Du kan tilføje felter ved hjælp af den Word-tilpassede XML-del for rapporten og tilføje indholdskontrolelementer, der er knyttet til felterne i rapportens datasæt. Tilføjelse af felter kræver, at du har kendskab til rapportens datasæt, så du kan identificere de felter, du vil føje til layoutet.  
  
> [!NOTE]  
>  Du kan ikke ændre indbyggede rapportlayout<!--Onprem. Built-in layouts can only be modified by using the development environment-->.  

### <a name="to-open-the-custom-xml-part-for-the-report-in-word" /><a name="OpenXMLPart"></a> Sådan åbner du den brugerdefinerede XML-del for rapporten i Word
  
1. Hvis det ikke allerede åbnet, skal du åbne Word-rapportlayoutdokumentet i Word.  
  
     Du kan finde flere oplysninger i [Oprette og ændre et brugerdefineret rapportlayout](ui-how-create-custom-report-layout.md).  
  
2. Vis fanen **Udvikler** på båndet i Microsoft Word.  
  
     Som standard vises fanen **Udvikler** ikke på båndet. Du kan finde flere oplysninger i [Vise fanen Udvikler på båndet](/visualstudio/vsto/how-to-show-the-developer-tab-on-the-ribbon).  
  
3. Vælg **XML-tilknytningsrude** under **Udvikler**.  
  
4. I ruden **XML-tilknytning** skal du på rullelisten **Brugerdefineret XML-del** vælge den brugerdefinerede XML-del til [!INCLUDE[prod_short](includes/prod_short.md)]-rapporten, som typisk er sidst på listen. Navnet på den brugerdefinerede XML-del har følgende format:  
  
     `urn:microsoft-dynamics-nav/reports/<report_name>/<ID>`  

     `<report_name>` er det navn, der er knyttet til rapporten 

     `<ID>` er identifikationsnummeret på rapporten.  
  
     Når du vælger den brugerdefinerede XML-del, viser ruden XML-tilknytning navne og feltkontrolelementer, der er tilgængelige for rapporten.  
  
### <a name="to-add-a-label-or-data-field" />Sådan tilføjer du et navne- eller datafelt.
  
1. Placer markøren i dokumentet, hvor du vil tilføje kontrolelementet.  
  
2. Brug ruden **XML-tilknytning** til at højreklikke på det kontrolelement, du vil tilføje, vælg **Indsæt indholdskontrolelement**, og vælg derefter **Almindelig tekst**.  
  
    > [!NOTE]  
    >  Du kan ikke tilføje et felt ved manuelt at indtaste feltnavnet på datasættet i indholdskontrolelementet. Du skal bruge ruden **XML-tilknytning** til at tilknytte felterne.  
  
### <a name="to-add-repeating-rows-of-data-fields-to-create-a-list" />Sådan tilføjer du gentagne rækker med datafelter for at oprette en liste
  
1. I en tabel kan du tilføje en tabelrække, der indeholder en kolonne for hvert felt, der skal gentages.  
  
   Denne række skal fungere som en pladsholder for gentagne felter.  
  
2. Markér hele rækken.  
  
3. Brug ruden **XML-tilknytning** til at højreklikke på det kontrolelement, der svarer til det rapportdataelement, der indeholder de felter, der skal gentages, vælg **Indsæt indholdskontrolelement**, og vælg derefter **Gentaget**.  
  
4. Tilføj gentagne felter på rækken som følger:  
  
    1. Placer markøren i en kolonne.  
  
    2. Brug ruden **XML-tilknytning** til at højreklikke på det kontrolelement, du vil tilføje, vælg **Indsæt indholdskontrolelement**, og vælg derefter **Almindelig tekst**.  
  
    3. Gentag trin a og b for hvert felt.  
  
## <a name="adding-image-fields" />Tilføje billedfelter

Et datasæt i rapporten kan indeholde et felt, der indeholder et billede som et firmalogo eller et billede af en vare. Hvis du vil tilføje et billede fra datasættet i rapporten, skal du indsætter et **Billede**-indholdskontrolelement.  
  
Billeder justeres i øverste venstre hjørne af Indholdsstyringen og får automatisk tilpasset størrelsen i forhold til rammen af indholdskontrolelementet.  
  
> [!IMPORTANT]  
> Du kan kun tilføje billeder, der har et format, som understøttes af Word, f.eks. .bmp-, .jpg- og .png-filtyper. Hvis du tilføjer et billede, der har et format, der ikke understøttes af Word, får du en fejl, når du kører rapporten fra [!INCLUDE[prod_short](includes/prod_short.md)]-klienten.  
  
### <a name="to-add-an-image" />Sådan tilføjer du et billede
  
1. Placer markøren i dokumentet, hvor du vil tilføje kontrolelementet.  
  
2. Brug ruden **XML-tilknytning** til at højreklikke på det kontrolelement, du vil tilføje, vælg **Indsæt indholdskontrolelement**, og vælg derefter **Billede**.  
  
3. Hvis du vil forøge eller formindske størrelsen på billedet, skal du trække et størrelseshåndtag væk fra eller mod midten af indholdskontrolelementet.  

## <a name="removing-label-and-data-fields" /><a name="RemoveField"></a> Fjerne navne- og datafelter

Navne- og datafelter i en rapport er indeholdt i indholdskontrolelementer i Word. Følgende figur illustrerer et indholdskontrolelement, når det er markeret i Word-dokumentet.  

![Indholdskontrol af felter i Word-rapportlayout.](media/nav_wordreportlayouts_contentcontrol.png "NAV_WordReportLayouts_ContentControl")  

Navnet på etiketten eller datafeltet vises i kontrolelementet for indhold. I eksemplet er feltnavnet CompanyAddr1.  

### <a name="to-remove-a-label-or-data-field" />Sådan fjerner du et navne- eller datafelt

1. Højreklik på det felt, du vil slette, og vælg derefter **Fjern indholdskontrolelement**.  

     Kontrolelementet for indhold fjernes, men feltnavnet forbliver som tekst.  

2. Slet den resterende tekst efter behov.

## <a name="custom-xml-part-overview" />Oversigt over brugerdefineret XML-del

Word-rapportlayout er baseret på *brugerdefinerede XML-dele*. En brugerdefineret XML-del til en rapport består af elementer, der svarer til de dataelementer, kolonner og etiketter, der udgør rapportens datasæt. <!--OnPrem The data as defined in the Report Dataset Designer in Microsoft Dynamics NAV Development Environment. -->Den brugerdefinerede XML-del bruges til at tilknytte dataene i en rapport, når rapporten køres.

### <a name="xml-structure-of-custom-xml-part" />XML-struktur af brugerdefineret XML-del

Følgende tabel indeholder en forenklet oversigt over XML for en brugerdefineret XML-del.  
  
|XML-elementer|Beskrivelse|  
|------------------|-----------------|  
|`<?xml version="1.0" encoding="utf-16"?>`|Overskrift|  
|`<WordReportXmlPart xmlns="urn:microsoft-dynamics-365/report/<reportname>/<id>/"`|Specifikation af XML-navneområde. `<reportname>` er det navn, der er knyttet til rapporten. `<id>` er det id, der er knyttet til rapporten.|  
|`..<Labels>`<br /><br /> `....<ColumnNameCaption>ColumnNameCaption</ColumnNameCaption>`<br /><br /> `....<LabelName>LabelCaption</LabelName>`<br /><br /> `..</Labels>`|Indeholder alle navne til rapporten.<!--OnPren The element includes labels that are related to columns that have the IncludeCaption Property.--><br />-   Etiketelementer, der er relateret til kolonner, har formatet `<ColumnNameCaption>ColumnNameCaption</ColumnNameCaption>`<!--OnPrem where `ColumnName` is determined by the column's Name Property.-->.<br />- Etiketelementer har formatet `<LabelName>LabelName</LabelName`<!--OnPrem where LabelName is determined by the label's Name Property.-->.<br />-   Etiketter vises i alfabetisk rækkefølge.|  
|`..<DataItem1>`<br /><br /> `....<DataItem1Column1>DataItem1Column1</DataItem1Column1>`|Øverste dataelement og kolonner. Kolonnerne vises i alfabetisk rækkefølge.<!--OnPrem <br /><br /> The element names and values are determined by the Name Property of the data item or column.-->|  
|`....<DataItem2>`<br /><br /> `......<DataItem2Column1>DataItem2Column1</DataItem2Column1>`<br /><br /> `....</DataItem2>`<br /><br /> `....<DataItem3>`<br /><br /> `......<DataItem3Column1>DataItem3Column1</DataItem3Column1>`<br /><br /> `....</DataItem3>`|Dataelementer og kolonner, der er indlejret i dataelementet på øverste niveau. Kolonnerne vises i alfabetisk rækkefølge under det respektive dataelement.|  
|`..</DataItem1>`<br /><br /> `</WordReportXmlPart>`|Lukker element.|  
  
### <a name="custom-xml-part-in-word" />Brugerdefineret XML-del i Word

 I Word kan du åbne den brugerdefinerede XML-del i ruden **XML-tilknytning** og derefter bruge ruden til at knytte elementer til indholdskontrolelementer i Word-dokumentet. Ruden **XML-tilknytning** er tilgængelig fra fanen **Udvikler** (du kan finde flere oplysninger i [Vise fanen Udvikler på båndet](/visualstudio/vsto/how-to-show-the-developer-tab-on-the-ribbon)).  
  
 Elementerne i ruden **XML-tilknytning** vises i en struktur, der svarer til XML-kilden. Navnefelter grupperes under et fælles **navneelement**, og dataelementer og -kolonner er arrangeret i en hierarkisk struktur, der svarer til XML-kilden, med kolonner i alfabetisk rækkefølge. Elementer identificeres ved deres kolonnenavn, som er defineret af rapportens datasæt i AL-kode. Du kan få flere oplysninger [Definere et rapportdatasæt](/dynamics365/business-central/dev-itpro/developer/devenv-report-dataset).  
  
 Følgende figur illustrerer den simple brugerdefinerede XML-del fra det foregående afsnit i ruden **XML-tilknytning** i et Word-dokument.  
  
 ![Klip af XML-tilknytningsruden i Word.](media/nav_reportlayout_xmlmappingpane.png "NAV_ReportLayout_XMLMappingPane")  
  
* Hvis du vil føje et navn eller felt til layoutet, skal du indsætte et indholdskontrolelement, der er knyttet til elementet i ruden **XML-tilknytning**.  
  
* Hvis du vil oprette gentagne rækker af kolonner, skal du indsætte et **Gentaget**-indholdskontrolelement til det overordnede dataelement og derefter tilføje indholdskontrolelement for kolonnerne.  
  
* For navne er den faktiske tekst, der vises i den genererede rapport, værdien af egenskaben **Billedtekst** for feltet i dataelementtabellen (hvis etiketten er relateret til en kolonne i rapportens datasæt) eller et navn i rapportnavnedesigneren (hvis navnet ikke er relateret til en kolonne i datasættet).  
  
* Sproget i teksten, der vises, når du kører rapporten, afhænger af sprogindstillingen af rapportobjektet.  
  
## <a name="see-also" />Se også

[Oprette og ændre et brugerdefineret rapportlayout](ui-how-create-custom-report-layout.md)   


[!INCLUDE[footer-include](includes/footer-banner.md)]
