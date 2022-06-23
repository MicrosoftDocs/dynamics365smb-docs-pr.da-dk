---
title: Oprette og ændre brugerdefinerede layout for rapporter og dokumenter
description: Lær, hvordan du kan oprette brugerdefinerede layout for at tilpasse udseendet af en rapport, når den vises, udskrives eller gemmes.
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: customized report, document layout, logo, personalize
ms.search.form: 9650, 9652
ms.date: 03/06/2022
ms.author: edupont
ms.openlocfilehash: 5e25685241e85a1a90ac23c7eb47f9808f3239b9
ms.sourcegitcommit: 7b6d70798b4da283d1d3e38a05151df2209c2b72
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 06/12/2022
ms.locfileid: "8950378"
---
# <a name="legacy-create-and-modify-custom-report-layouts"></a>(Ældre) Sådan opretter og ændrer du Brugerdefinerede rapportlayouts

[!INCLUDE[legacy-custom-layouts](includes/legacy-custom-layouts.md)]

Som standard har rapporter et indbygget rapportlayout. Layoutet kan være enten et RDLC-rapportlayout, et Word-rapportlayout eller begge dele. Du kan ikke redigere indbyggede layout, men du kan oprette brugerdefinerede layout. En rapport kan have flere brugerdefinerede rapportlayout.

> [!NOTE]  
> I [!INCLUDE[prod_short](includes/prod_short.md)] omfatter "rapporter" også eksternt orienterede dokumenter, f.eks. salgsfakturaer og ordrebekræftelser, som du sender til kunder som PDF-filer.

Hvis du vil oprette et brugerdefineret layout, skal du enten kopiere et eksisterende brugerdefineret layout eller tilføje et nyt brugerdefineret layout. Brugerdefinerede layouts er ofte baseret på indbyggede layout. Når du tilføjer et nyt brugerdefineret layout, kan du tilføje en RDLC- eller Word-rapportlayouttype - eller begge dele. Det nye brugerdefinerede layout vil automatisk blive baseret på det indbyggede layout for rapporten, hvis det findes. Hvis der ikke er noget indbygget layout til teksten, oprettes et nyt tomt layout. Du skal ændre og designe dette tomme layout fra bunden. Find flere oplysninger om RDLC- og Word-rapportlayout, indbyggede og brugerdefinerede layout og mere under [Administration af rapportlayout](ui-manage-report-layouts.md).  

> [!TIP]
> Du kan bruge kontoskemaer til at få indsigt i de finansielle oplysninger, der er gemt i din kontoplan. Se [Forberede Financial Reporting med kontoskemaer og kontokategorier](bi-how-work-account-schedule.md) for at få flere oplysninger.

Når du har defineret tilpassede rapportlayout, kan du vælge dem på debitor- og kreditor-kortsider. Disse layout bruges, når du opretter dokumenter til debitoren eller kreditoren. Du kan finde flere oplysninger i [Definition af Dokumentlayouts til debitorer og leverandører](ui-define-customer-vendor-document-layouts.md).

Du kan også bruge brugerdefinerede rapportlayouts til at føje indhold til e-mailmeddelelser. Rapportlayout kan spare tid og være med til at sikre konsistensen ved at genbruge det samme indhold, når du kommunikerer med kunderne. Hvis du vil bruge brugerdefinerede rapportlayout med e-mail, skal det være et Word-filtypeformat. Du kan ikke bruge RDLC-filtypen. Du kan finde flere oplysninger i [angive genanvendelige e-mail-tekst og layout](admin-how-setup-email.md#set-up-reusable-email-texts-and-layouts). 

## <a name="to-create-a-custom-layout"></a>Sådan opretter du et brugerdefineret layout

1. Vælg ![Lightbulb, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **Valg af rapportlayout**, og vælg derefter det relaterede link.

    Siden **Valg af rapportlayout** viser en liste over alle de rapporter, der er tilgængelige i den virksomhed, der er angivet i feltet **Virksomhedsnavn** øverst på siden.
2. Indstil feltet **Virksomhedsnavn** skal du vælge det firma, som du vil oprette rapportlayout for.
3. Vælg rækken med den rapport, du vil oprette layoutet for, og vælg derefter handlingen **Brugerdefinerede layout**.  

   Siden **Brugerdefinerede layout** vises med alle brugerdefinerede layout, der er tilgængelige for den valgte rapport.
4. Hvis du vil oprette en kopi af et eksisterende brugerdefineret layout, skal du vælge det eksisterende brugerdefinerede layout på listen og derefter vælge handlingen **Kopiér**.  

   Kopien af det brugerdefinerede layout vises på siden **Brugerdefinerede layout** og indeholder ordene *Kopi af* i feltet **Beskrivelse**.
5. Hvis du vil tilføje et nyt brugerdefineret layout, der er baseret på et indbygget layout, skal du gøre følgende:  
   1. Vælg handlingen **Ny**. Siden **Indsæt indbygget layout til en rapport** åbnes. Felterne **Id** og **Navn** udfyldes automatisk.
   2. Hvis du vil tilføje en brugerdefineret Word-rapportlayouttype, skal du aktivere afkrydsningsfeltet **Indsæt Word-layout**.
   3. Hvis du vil tilføje en brugerdefineret RDLC-rapportlayouttype, skal du aktivere afkrydsningsfeltet **Indsæt RDLC-layout**.
   4. Vælg knappen **OK**.  

    Det nye brugerdefinerede layout vises nu på siden **Tilpassede rapportlayouts**. Hvis et nyt layout er baseret på et indbygget layout, så har den ordene **Kopi af et indbygget layout** i feltet **Beskrivelse**. Hvis der ikke var noget indbygget layout for rapporten, har det nye layout ordene **Nyt layout** i feltet **Beskrivelse**, fordi det brugerdefinerede layout er tomt.
6. Som standard er feltet **Virksomhedsnavn** tomt, hvilket betyder, at det brugerdefinerede layout bliver tilgængeligt for rapporten i alle firmaer. Hvis du kun vil gøre det brugerdefinerede layout tilgængeligt i en bestemt virksomhed, skal du vælge **Rediger** og derefter indstille feltet **Virksomhedsnavn** til den ønskede virksomhed.

Det brugerdefinerede layout er oprettet. Du kan nu redigere det brugerdefinerede layout efter behov.

> [!TIP]
> Du kan godt eksportere rapportresultaterne til en Excel-fil, så du kan få vist hele datasættet, inklusive alle kolonner men uden layout. Excel-filen kan hjælpe dig med at kontrollere, at rapporten returnerer de forventede data eller diagnoseproblemer. Du kan finde flere oplysninger i [Analyse af rapportdata med Excel](report-analyze-excel.md).

## <a name="modifying-a-custom-layout"></a><a name="ModifyCustomLayout"></a>Redigere et brugerdefineret layout

Hvis du vil ændre et rapportlayout, skal du først eksportere rapportlayoutet som en fil til en placering på din computer eller dit netværk. Åbn derefter det udlæste dokument, og foretag ændringerne. Når du er færdig med at foretage ændringerne, skal du importere rapportlayoutet.

### <a name="to-modify-a-custom-layout"></a>Sådan ændres et brugerdefineret layout

1. Du kan eksportere et brugerdefineret layout på siden **Brugerdefinerede rapportlayouts**. Hvis siden ikke allerede er åben, skal du søge efter og åbne siden **Valg af rapportlayout**, vælge den rapport, der har det layout, du vil ændre, og derefter vælge handlingen **Brugerdefinerede layout**.  
2. På siden **Brugerdefinerede rapportlayouts** skal du vælge det layout, du vil ændre, vælge handlingen **Eksportér layout** og derefter klikke på **Gem** eller **Gem som** for at gemme rapportlayoutdokumentet på en placering på din computer eller dit netværk.  
3. Åbn det rapportlayoutdokument, du har gemt, og foretag derefter ændringerne.

   Hvis du ændrer et Word-layout, skal du åbne layoutdokumentet i Word. Du kan redigere detaljer i [arbejde med Word-layout](ui-how-add-fields-word-report-layout.md)<!--the next section [Making Changes to the Report Layout](ui-how-create-custom-report-layout.md#MakeChangesToLayout)-->.

   RDLC-rapportlayout er mere avanceret end Word-rapportlayout. Du kan finde flere oplysninger om ændring af RDLC-rapportlayout i [Designe RDLC-rapportlayout](/dynamics-nav/Designing-RDLC-Report-Layouts).

   Husk at gemme ændringerne, når du er færdig.

4. Vend tilbage til siden **Brugerdefinerede rapportlayout**, vælg det rapportlayout, som du har eksporteret og ændret, og vælg derefter handlingen **Importér layout**.  

5. I dialogboksen **Importér** skal du markere **Vælg** for at finde og vælge det tilpassede rapportlayoutdokument, og derefter skal du vælge **Åbn**.

> [!IMPORTANT]
> Husk at indlæse det rapportlayout dokument, du har ændret. Ellers vil det nye rapportlayout ikke være tilgængeligt.

<!--
##  <a name="MakeChangesToLayout"></a> Create and Modify Custom Report Layouts

To make general formatting and layout changes, such as changing text font, adding and modifying a table, or removing a data field, just use the basic editing features of Word, like you do with any Word document.

If you're designing a Word report layout from scratch or adding new data fields, then start by adding a table that includes rows and columns that will eventually hold the data fields.

> [!TIP]  
> Show the table gridlines so that you see the boundaries of table cells. Remember to hide the gridlines when you're done editing. To show or hide table gridlines, select the table, and then under **Layout** on the **Table** tab, choose **View Gridlines**.

### Embedding Fonts in Word Layouts for Consistency

To ensure that reports always display and print with the intended fonts, wherever users open or print the reports, you can embed the fonts in the Word document. However, embedding fonts can significantly increase the size of the Word files. For more information about embedding fonts in Word, see [Embed fonts in Word, PowerPoint, or Excel](https://support.office.com/article/Embed-fonts-in-Word-PowerPoint-or-Excel-cb3982aa-ea76-4323-b008-86670f222dbc).

###  <a name="RemoveField"></a> Removing Label and Data Fields in Word Layouts

 Label and data fields of a report are contained in content controls in Word. The following figure illustrates a content control when it's selected in the Word document.  

 ![Content control for field in Word report layout.](media/nav_wordreportlayouts_contentcontrol.png "NAV_WordReportLayouts_ContentControl")  

 The name of the label or data field name displays in the content control. In the example, the field name is CompanyAddr1.  

### To remove a label or data field  

1. Right-click the field that you want to delete, and then choose **Remove Content Control**.  

     The content control is removed, but the field name remains as text.  

2. Delete the remaining text as needed.  

### Adding data fields

Adding data fields from a report dataset is a more advanced and requires some knowledge of the report dataset. For information about adding fields for data, labels, data, and images, see [Add Fields to a Word Report Layout](ui-how-add-fields-word-report-layout.md).  -->

## <a name="see-related-training-at-microsoft-learn"></a>Se relateret oplæring på [Microsoft Learn](/learn/modules/change-documents-dynamics-365-business-central/index)

## <a name="see-also"></a>Se også

[Administration af rapportlayout](ui-manage-report-layouts.md)  
[Ændre det aktuelle rapportlayout](ui-how-change-layout-currently-used-report.md)  
[Importere og eksportere et brugerdefineret rapport- eller dokumentlayout](ui-how-import-and-export-report-layout.md)  
[Arbejde med rapporter, kørsler og XMLporte](ui-work-report.md)  
[Forberede Financial Reporting med kontoskemaer og kontokategorier](bi-how-work-account-schedule.md) 
[Business Intelligence](bi.md)  
[Arbejd med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]