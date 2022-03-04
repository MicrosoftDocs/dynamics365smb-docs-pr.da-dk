---
title: 'Fremgangsmåde: Føje felter til et Word-rapportlayout'
description: Beskriver, hvor du tilføjer felter fra et rapportdatasæt til et eksisterende Word-rapportlayout for en rapport.
author: jswymer
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 11/25/2021
ms.author: jswymer
ms.openlocfilehash: 036b6964b8a0e468bdfc4d2f3e44824b3daac9ee
ms.sourcegitcommit: ef80c461713fff1a75998766e7a4ed3a7c6121d0
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 02/15/2022
ms.locfileid: "8144719"
---
# <a name="add-fields-to-a-word-report-layout"></a>Føje felter til et Word-rapportlayout
Et datasæt i rapporten kan bestå af felter, der viser navne, data og billeder. I dette emne beskrives fremgangsmåden for tilføjelse af felter fra et rapportedatasæt i et eksisterende Word-rapportlayout for en rapport. Du kan tilføje felter ved hjælp af den Word-tilpassede XML-del for rapporten og tilføje indholdskontrolelementer, der er knyttet til felterne i rapportens datasæt. Tilføjelse af felter kræver, at du har kendskab til rapportens datasæt, så du kan identificere de felter, du vil føje til layoutet.  
  
> [!NOTE]  
>  Du kan ikke ændre indbyggede rapportlayout<!--Onprem. Built-in layouts can only be modified by using the development environment-->.  

##  <a name="to-open-the-custom-xml-part-for-the-report-in-word"></a><a name="OpenXMLPart"></a> Sådan åbner du den brugerdefinerede XML-del for rapporten i Word  
  
1.  Hvis det ikke allerede åbnet, skal du åbne Word-rapportlayoutdokumentet i Word.  
  
     Du kan finde flere oplysninger i [Oprette og ændre et brugerdefineret rapportlayout](ui-how-create-custom-report-layout.md).  
  
2.  Vis fanen **Udvikler** på båndet i Microsoft Word.  
  
     Som standard vises fanen **Udvikler** ikke på båndet. Du kan finde flere oplysninger i [Vise fanen Udvikler på båndet](/visualstudio/vsto/how-to-show-the-developer-tab-on-the-ribbon).  
  
3.  Vælg **XML-tilknytningsrude** under **Udvikler**.  
  
4.  I ruden **XML-tilknytning** skal du på rullelisten **Brugerdefineret XML-del** vælge den brugerdefinerede XML-del til [!INCLUDE[prod_short](includes/prod_short.md)]-rapporten, som typisk er sidst på listen. Navnet på den brugerdefinerede XML-del har følgende format:  
  
     urn:microsoft-dynamics-nav/reports/*report_name*/*ID*  
  
     *rapportnavn* er det navn, der er knyttet til rapporten<!--OnPrem as specified by the report's [Name Property-duplicate](../FullExperience/nav_dev_long_md.md)]-->.  
  
     *ID* er identifikationsnummeret på rapporten.  
  
     Når du vælger den brugerdefinerede XML-del, viser ruden XML-tilknytning navne og feltkontrolelementer, der er tilgængelige for rapporten.  
  
### <a name="to-add-a-label-or-data-field"></a>Sådan tilføjer du et navne- eller datafelt.  
  
1.  Placer markøren i dokumentet, hvor du vil tilføje kontrolelementet.  
  
2.  Brug ruden **XML-tilknytning** til at højreklikke på det kontrolelement, du vil tilføje, vælg **Indsæt indholdskontrolelement**, og vælg derefter **Almindelig tekst**.  
  
    > [!NOTE]  
    >  Du kan ikke tilføje et felt ved manuelt at indtaste feltnavnet på datasættet i indholdskontrolelementet. Du skal bruge ruden **XML-tilknytning** til at tilknytte felterne.  
  
### <a name="to-add-repeating-rows-of-data-fields-to-create-a-list"></a>Sådan tilføjer du gentagne rækker med datafelter for at oprette en liste  
  
1.  I en tabel kan du tilføje en tabelrække, der indeholder en kolonne for hvert felt, der skal gentages.  
  
     Denne række skal fungere som en pladsholder for gentagne felter.  
  
2.  Markér hele rækken.  
  
3.  Brug ruden **XML-tilknytning** til at højreklikke på det kontrolelement, der svarer til det rapportdataelement, der indeholder de felter, der skal gentages, vælg **Indsæt indholdskontrolelement**, og vælg derefter **Gentaget**.  
  
4.  Tilføj gentagne felter på rækken som følger:  
  
    1.  Placer markøren i en kolonne.  
  
    2.  Brug ruden **XML-tilknytning** til at højreklikke på det kontrolelement, du vil tilføje, vælg **Indsæt indholdskontrolelement**, og vælg derefter **Almindelig tekst**.  
  
    3.  Gentag trin a og b for hvert felt.  
  
## <a name="adding-image-fields"></a>Tilføjelse af billedfelter  
 Et datasæt i rapporten kan indeholde et felt, der indeholder et billede som et firmalogo eller et billede af en vare. Hvis du vil tilføje et billede fra datasættet i rapporten, skal du indsætter et **Billede**-indholdskontrolelement.  
  
 Billeder justeres i øverste venstre hjørne af Indholdsstyringen og får automatisk tilpasset størrelsen i forhold til rammen af indholdskontrolelementet.  
  
> [!IMPORTANT]  
>  Du kan kun tilføje billeder, der har et format, som understøttes af Word, f.eks. .bmp-, .jpg- og .png-filtyper. Hvis du tilføjer et billede, der har et format, der ikke understøttes af Word, får du en fejl, når du kører rapporten fra [!INCLUDE[prod_short](includes/prod_short.md)]-klienten.  
  
#### <a name="to-add-an-image"></a>Sådan tilføjer du et billede  
  
1.  Placer markøren i dokumentet, hvor du vil tilføje kontrolelementet.  
  
2.  Brug ruden **XML-tilknytning** til at højreklikke på det kontrolelement, du vil tilføje, vælg **Indsæt indholdskontrolelement**, og vælg derefter **Billede**.  
  
3.  Hvis du vil forøge eller formindske størrelsen på billedet, skal du trække et størrelseshåndtag væk fra eller mod midten af indholdskontrolelementet.  

## <a name="custom-xml-part-overview"></a>Oversigt over brugerdefineret XML-del
Word-rapportlayout er baseret på *brugerdefinerede XML-dele*. En brugerdefineret XML-del til en rapport består af elementer, der svarer til de dataelementer, kolonner og etiketter, der udgør rapportens datasæt. <!--OnPrem The data as defined in the Report Dataset Designer in Microsoft Dynamics NAV Development Environment. -->Den brugerdefinerede XML-del bruges til at tilknytte dataene i en rapport, når rapporten køres.

  
### <a name="xml-structure-of-custom-xml-part"></a>XML-struktur af brugerdefineret XML-del  
Følgende tabel indeholder en forenklet oversigt over XML for en brugerdefineret XML-del.  
  
|XML-elementer|Beskrivelse|  
|------------------|-----------------|  
|`<?xml version="1.0" encoding="utf-16"?>`|Overskrift|  
|`<WordReportXmlPart xmlns="urn:microsoft-dynamics-365/report/<reportname>/<id>/"`|Specifikation af XML-navneområde. `<reportname>` er det navn, der er knyttet til rapporten. `<id>` er det id, der er knyttet til rapporten.|  
|`..<Labels>`<br /><br /> `....<ColumnNameCaption>ColumnNameCaption</ColumnNameCaption>`<br /><br /> `....<LabelName>LabelCaption</LabelName>`<br /><br /> `..</Labels>`|Indeholder alle navne til rapporten.<!--OnPren The element includes labels that are related to columns that have the IncludeCaption Property.--><br />-   Etiketelementer, der er relateret til kolonner, har formatet `<ColumnNameCaption>ColumnNameCaption</ColumnNameCaption>`<!--OnPrem where `ColumnName` is determined by the column's Name Property.-->.<br />- Etiketelementer har formatet `<LabelName>LabelName</LabelName`<!--OnPrem where LabelName is determined by the label's Name Property.-->.<br />-   Etiketter vises i alfabetisk rækkefølge.|  
|`..<DataItem1>`<br /><br /> `....<DataItem1Column1>DataItem1Column1</DataItem1Column1>`|Øverste dataelement og kolonner. Kolonnerne vises i alfabetisk rækkefølge.<!--OnPrem <br /><br /> The element names and values are determined by the Name Property of the data item or column.-->|  
|`....<DataItem2>`<br /><br /> `......<DataItem2Column1>DataItem2Column1</DataItem2Column1>`<br /><br /> `....</DataItem2>`<br /><br /> `....<DataItem3>`<br /><br /> `......<DataItem3Column1>DataItem3Column1</DataItem3Column1>`<br /><br /> `....</DataItem3>`|Dataelementer og kolonner, der er indlejret i dataelementet på øverste niveau. Kolonnerne vises i alfabetisk rækkefølge under det respektive dataelement.|  
|`..</DataItem1>`<br /><br /> `</WordReportXmlPart>`|Lukker element.|  
  
### <a name="custom-xml-part-in-word"></a>Brugerdefineret XML-del i Word  
 I Word kan du åbne den brugerdefinerede XML-del i ruden **XML-tilknytning** og derefter bruge ruden til at knytte elementer til indholdskontrolelementer i Word-dokumentet. Ruden **XML-tilknytning** er tilgængelig fra fanen **Udvikler** (du kan finde flere oplysninger i [Vise fanen Udvikler på båndet](/visualstudio/vsto/how-to-show-the-developer-tab-on-the-ribbon)).  
  
 Elementerne i ruden **XML-tilknytning** vises i en struktur, der svarer til XML-kilden. Navnefelter grupperes under et fælles **navneelement**, og dataelementer og -kolonner er arrangeret i en hierarkisk struktur, der svarer til XML-kilden, med kolonner i alfabetisk rækkefølge. Elementer identificeres ved deres kolonnenavn, som er defineret af rapportens datasæt i AL-kode. Du kan få flere oplysninger [Definere et rapportdatasæt](/dynamics365/business-central/dev-itpro/developer/devenv-report-dataset).  
  
 Følgende figur illustrerer den simple brugerdefinerede XML-del fra det foregående afsnit i ruden **XML-tilknytning** i et Word-dokument.  
  
 ![Klip af XML-tilknytningsruden i Word.](media/nav_reportlayout_xmlmappingpane.png "NAV_ReportLayout_XMLMappingPane")  
  
-   Hvis du vil føje et navn eller felt til layoutet, skal du indsætte et indholdskontrolelement, der er knyttet til elementet i ruden **XML-tilknytning**.  
  
-   Hvis du vil oprette gentagne rækker af kolonner, skal du indsætte et **Gentaget**-indholdskontrolelement til det overordnede dataelement og derefter tilføje indholdskontrolelement for kolonnerne.  
  
-   For navne er den faktiske tekst, der vises i den genererede rapport, værdien af egenskaben **Billedtekst** for feltet i dataelementtabellen (hvis etiketten er relateret til en kolonne i rapportens datasæt) eller et navn i rapportnavnedesigneren (hvis navnet ikke er relateret til en kolonne i datasættet).  
  
-   Sproget i teksten, der vises, når du kører rapporten, afhænger af sprogindstillingen af rapportobjektet.  
  
## <a name="see-also"></a>Se også  
 [Oprette og ændre et brugerdefineret rapportlayout](ui-how-create-custom-report-layout.md)   


[!INCLUDE[footer-include](includes/footer-banner.md)]