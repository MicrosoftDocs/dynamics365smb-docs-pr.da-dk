---
title: Oprette og ændre brugerdefinerede layout for rapporter og dokumenter | Microsoft Docs
description: Lær, hvordan du kan oprette dine egne brugerdefinerede layout for at tilpasse udseendet af en rapport, når den vises, udskrives eller gemmes.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: customized report, document layout, logo, personalize
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: 5a8267813a37af08dd057e4c67a04237cd350b54
ms.sourcegitcommit: 2e7307fbe1eb3b34d0ad9356226a19409054a402
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 12/17/2020
ms.locfileid: "4760538"
---
# <a name="create-and-modify-custom-report-layouts"></a>Sådan opretter og ændrer du Brugerdefinerede rapportlayouts

Som standard har en rapport et indbygget rapportlayout, som enten kan være et RDLC-rapportlayout eller Word-rapportlayout eller begge typer. Du kan ikke ændre indbyggede layout. Du kan dog oprette dine egne brugerdefinerede layout, der gør det muligt at ændre udseendet af rapporten, når den vises, udskrives eller gemmes. Du kan oprette flere brugerdefinerede rapportlayout til samme rapport og derefter skifte det layout, der bruges af en rapport, efter behov.

> [!NOTE]  
> I [!INCLUDE[prod_short](includes/prod_short.md)] omfatter "rapporter" også eksternt orienterede dokumenter, f.eks. salgsfakturaer og ordrebekræftelser, som du sender til kunder som PDF-filer.

Hvis du vil oprette et brugerdefineret layout, kan du enten oprette en kopi af et eksisterende brugerdefineret layout eller tilføje et nyt brugerdefineret layout, som i de fleste tilfælde er baseret på et indbygget layout. Når du tilføjer et nyt brugerdefineret layout, kan du tilføje en RDLC-rapportlayouttype, Word-rapportlayouttype eller begge dele. Det nye brugerdefinerede layout vil automatisk blive baseret på det indbyggede layout for rapporten, hvis det findes. Hvis der er ingen indbyggede layout for typen, bliver et tomt layout oprettet, som du skal ændre og designe fra bunden. Find flere oplysninger om RDLC- og Word-rapportlayout, indbyggede og brugerdefinerede layout og mere under [Administration af rapportlayout](ui-manage-report-layouts.md).  

> [!TIP]
> Du kan bruge kontoskemaer til at få indsigt i de finansielle oplysninger, der er gemt i din kontoplan. Se [Forberede finansrapporter med kontoskemaer og kontokategorier](bi-how-work-account-schedule.md) for at få flere oplysninger.

Når der er defineret brugerdefinerede rapportlayout, kan du vælge dem fra debitor- og leverandørkortene for at angive, at det valgte layout skal bruges til de dokumenter, som du har oprettet for den pågældende debitor eller leverandør. Du kan finde flere oplysninger i [Definition af Dokumentlayouts til debitorer og leverandører](ui-define-customer-vendor-document-layouts.md).

## <a name="to-create-a-custom-layout"></a>Sådan opretter du et brugerdefineret layout

1. Vælg ikonet ![Elpære, der åbner funktionen Fortæl mig](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig"), angiv **Valg af rapportlayout**, og vælg derefter det relaterede link.

    Siden **Valg af rapportlayout** viser en liste over alle de rapporter, der er tilgængelige i den virksomhed, der er angivet i feltet **Virksomhedsnavn** øverst på siden.
2. Indstil feltet **Virksomhed** til den virksomhed, hvor du vil oprette rapportlayoutet.
3. Vælg rækken med den rapport, du vil oprette layoutet for, og vælg derefter handlingen **Brugerdefinerede layout**.  

   Siden **Brugerdefinerede layout** vises med alle brugerdefinerede layout, der er tilgængelige for den valgte rapport.
4. Hvis du vil oprette en kopi af et eksisterende brugerdefineret layout, skal du vælge det eksisterende brugerdefinerede layout på listen og derefter vælge handlingen **Kopiér**.  

   Kopien af det brugerdefinerede layout vises på siden **Brugerdefinerede layout** og indeholder ordene *Kopi af* i feltet **Beskrivelse**.
5. Hvis du vil tilføje et nyt brugerdefineret layout, der er baseret på et indbygget layout, skal du gøre følgende:  
   1. Vælg handlingen **Ny**. Siden **Indsæt indbygget layout til en rapport** åbnes. Felterne **Id** og **Navn** udfyldes automatisk.
   2. Hvis du vil tilføje en brugerdefineret Word-rapportlayouttype, skal du markere afkrydsningsfeltet **Indsæt Word-layout**.
   3. Hvis du vil tilføje en brugerdefineret RDLC-rapportlayouttype, skal du markere afkrydsningsfeltet **Indsæt RDLC-layout**.
   4. Vælg knappen **OK**.  

    Det nye brugerdefinerede layout vises nu på siden **Tilpassede rapportlayouts**. Hvis et nyt layout er baseret på et indbygget layout, så har den ordene **Kopi af et indbygget layout** i feltet **Beskrivelse**. Hvis der ikke var noget indbygget layout for rapporten, har det nye layout ordene **Nyt layout** i feltet **Beskrivelse**, fordi det brugerdefinerede layout er tomt.
6. Som standard er feltet **Virksomhedsnavn** tomt, hvilket betyder, at det brugerdefinerede layout bliver tilgængeligt for rapporten i alle firmaer. Hvis du kun vil gøre det brugerdefinerede layout tilgængeligt i en bestemt virksomhed, skal du vælge **Rediger** og derefter indstille feltet **Virksomhedsnavn** til den ønskede virksomhed.

Det brugerdefinerede layout er oprettet. Du kan nu redigere det brugerdefinerede layout efter behov.

## <a name="modifying-a-custom-layout"></a><a name="ModifyCustomLayout"></a>Redigere et brugerdefineret layout

Hvis du vil ændre et rapportlayout, skal du først eksportere rapportlayoutet som en fil til en placering på din computer eller netværket og derefter åbne det eksporterede dokument og foretage ændringerne. Når du er færdig med at foretage ændringerne, skal du importere rapportlayoutet.

### <a name="to-modify-a-custom-layout"></a>Sådan ændres et brugerdefineret layout

1.  Du kan eksportere et brugerdefineret layout på siden **Brugerdefinerede rapportlayouts**. Hvis siden ikke allerede er åben, skal du søge efter og åbne siden **Valg af rapportlayout**, vælge den rapport, der har det layout, du vil ændre, og derefter vælge handlingen **Brugerdefinerede layout**.  
2.  På siden **Brugerdefinerede rapportlayouts** skal du vælge det layout, du vil ændre, vælge handlingen **Eksportér layout** og derefter klikke på **Gem** eller **Gem som** for at gemme rapportlayoutdokumentet på en placering på din computer eller dit netværk.  

3.  Åbn det rapportlayoutdokument, du har lige har gemt, og foretag derefter ændringerne.

      Hvis du ændrer et Word-layout, skal du åbne layoutdokumentet i Word. Hvis du vil vide mere om redigering af oplysninger, skal du se næste afsnit [Ændringer af rapportlayoutet](ui-how-create-custom-report-layout.md#MakeChangesToLayout).

      RDLC-rapportlayout er mere avanceret end Word-rapportlayout. Du kan finde flere oplysninger om ændring af RDLC-rapportlayout i [Designe RDLC-rapportlayout](/dynamics-nav/Designing-RDLC-Report-Layouts).

      Husk at gemme ændringerne, når du er færdig.

4.  Vend tilbage til siden **Brugerdefinerede rapportlayout**, vælg det rapportlayout, som du har eksporteret og ændret, og vælg derefter handlingen **Importér layout**.  

5. I dialogboksen **Importér** skal du markere **Vælg** for at finde og vælge rapportlayoutdokumentet, og derefter skal du vælge **Åbn**.

##  <a name="create-and-modify-custom-report-layouts"></a><a name="MakeChangesToLayout"></a> Sådan opretter og ændrer du Brugerdefinerede rapportlayouts

Hvis du vil foretage generelle formaterings- og layoutændringer, f.eks. skifte skrifttype, tilføje og redigere en tabel eller fjerne et datafelt, skal du blot bruge de grundlæggende funktioner til redigering i Word, som du gør med ethvert Word-dokument.

Hvis du designer et Word-rapportlayout fra bunden eller tilføjer nye datafelter, skal du starte med at tilføje en tabel med rækker og kolonner, der efterhånden indeholder datafelter.

> [!TIP]  
> Vis tabelgitterlinjer, så du kan se grænserne for tabelceller. Husk at skjule gitterlinjerne, når du er færdig med redigering. Hvis du vil vise eller skjule tabelgitterlinjer, skal du vælge tabellen og derefter vælge på **Vis gitterlinjer** under **Layout** under fanen **Tabel**.

### <a name="embedding-fonts-in-word-layouts-for-consistency"></a>Integrere skrifttyper i Word-layout for at skabe ensartethed

For at sikre, at rapporter altid vises og udskrives med de ønskede skrifttyper, uanset hvor brugere åbner eller udskriver rapporter, kan du integrere skrifttyperne i Word-dokumentet. Du skal dog være opmærksom på, at integrering af skrifttyper kan øge størrelsen på Word-filer. Du kan finde flere oplysninger om integrering af skrifttyper i Word i [Integrere skrifttyper i Word, PowerPoint eller Excel](https://support.office.com/article/Embed-fonts-in-Word-PowerPoint-or-Excel-cb3982aa-ea76-4323-b008-86670f222dbc).

###  <a name="removing-label-and-data-fields-in-word-layouts"></a><a name="RemoveField"></a> Fjernelse af navne- og datafelter i Word-layout

 Navne- og datafelter i en rapport er indeholdt i indholdskontrolelementer i Word. Følgende figur illustrerer et indholdskontrolelement, når det er markeret i Word-dokumentet.  

 ![Indholdskontrol af felter i Word-rapportlayout](media/nav_wordreportlayouts_contentcontrol.png "NAV_WordReportLayouts_ContentControl")  

 Navnet på etiketten eller datafeltet vises i kontrolelementet for indhold. I eksemplet er feltnavnet CompanyAddr1.  

### <a name="to-remove-a-label-or-data-field"></a>Sådan fjerner du et navne- eller datafelt  

1. Højreklik på det felt, du vil slette, og vælg derefter **Fjern indholdskontrolelement**.  

     Kontrolelementet for indhold fjernes, men feltnavnet forbliver som tekst.  

2. Slet den resterende tekst efter behov.  

### <a name="adding-data-fields"></a>Tilføje datafelter

Tilføjelse af datafelter fra en rapports datasæt er mere avanceret og kræver kendskab til rapportdatasættet. Du kan finde oplysninger om tilføjelse af felter til data, etiketter, data og billeder i [Føje felter til et Word-rapportlayout](ui-how-add-fields-word-report-layout.md).  

## <a name="see-related-training-at-microsoft-learn"></a>Se relateret oplæring på [Microsoft Learn](/learn/modules/change-documents-dynamics-365-business-central/index)

## <a name="see-also"></a>Se også

[Administration af rapportlayout](ui-manage-report-layouts.md)  
[Ændre det aktuelle rapportlayout](ui-how-change-layout-currently-used-report.md)  
[Importere og eksportere et brugerdefineret rapport- eller dokumentlayout](ui-how-import-and-export-report-layout.md)  
[Arbejde med rapporter, kørsler og XMLporte](ui-work-report.md)  
[Forberede finansrapporter med kontoskemaer og kontokategorier](bi-how-work-account-schedule.md) 
[Business Intelligence](bi.md)  
[Arbejde med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]