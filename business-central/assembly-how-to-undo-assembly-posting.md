---
title: Sådan fortryder du bogføring af montage | Microsoft Docs
description: Nogle gange kan du fortryde en bogført montageordre, for eksempel, når ordren er bogført med fejl, der skal rettes, eller ikke skulle være bogført i første omgang, og den skal annulleres.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: kit, kitting
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: d672b28dda7c586bd68412fbbb89fb8e33cba1b8
ms.sourcegitcommit: 2e7307fbe1eb3b34d0ad9356226a19409054a402
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 12/17/2020
ms.locfileid: "4747311"
---
# <a name="undo-assembly-posting"></a>Fortryde bogføring af montage
Nogle gange kan du fortryde en bogført montageordre, for eksempel, når ordren er bogført med fejl, der skal rettes, eller ikke skulle være bogført i første omgang, og den skal annulleres.

Når du fortryder en bogført montageordre, oprettes der et sæt korrigerende vareposter til at tilbageføre de oprindelige poster. Hver positive afgangspost for montageelementet tilbageføres af en negativ afgangspost. Hver negative forbrugspost for en montagekomponent tilbageføres af en positiv forbrugspost. Fast omkostningsanvendelse oprettes automatisk mellem korrigerende og oprindelige poster for at sikre præcis kostprisudligning.  

Når du fortryder en fuldt bogført montageordre, kan du vælge at genskabe montageordren til den oprindelige tilstand, for eksempel at foretage rettelser før du bogfører den igen. Alternativt kan du vælge ikke at genoprette montageordren.  

Når du fortryder en delvist bogført montageordre, gendannes alle berørte antalsfelter, f.eks i felterne **Monteret antal**, **Forbrugt antal** og **Restantal**, til de værdier, de havde, inden den pågældende bogføring.  

Hvis du vil genoprette eller gendanne montageordrer, skal følgende betingelser være opfyldt for det montageelement, der var afgangselementet i den oprindelige postering:  

-   Det skal stadig være på lager, dvs. ikke solgt eller på anden måde forbrugt af udgående transaktioner.  
-   Det må ikke være reserveret.  
-   Det skal findes på den placering, som det afgik til.  

Eksisterende montageordrer kan desuden kun gendannes, hvis antallet af linjer og rækkefølgen af linjerne i den oprindelige montageordre ikke ændres.  

> [!TIP]  
>  Hvis du vil løse konflikter som følge af linjeændringer, kan du manuelt tilbageføre ændringerne på de pågældende linjer, før du fortryder den relaterede bogførte montageordre. Du kan også bogføre montageordren fuldstændigt og derefter vælge at oprette den igen, når du annullerer bogføringen.  

Følgende procedure beskriver, hvordan du fortryder bogførte montageordrer, hvor der var tale om montage til lager-varer. Hvis du vil fortryde bogførte montageordrer, hvor der var tale om montage efter salgsordre-varer, skal du bruge funktionen **Annuller leverance** på den bogførte leverance, der er relateret til den bogførte montageordre. Du kan finde flere oplysninger i [Tilbageføre kladdeposteringer og annullere modtagelser/leverancer](finance-how-reverse-journal-posting.md). Tilbageførslen af den bogførte montageordre sker så automatisk på samme måde som beskrevet i dette emne.  

## <a name="to-undo-posting-of-an-assembly-order"></a>Sådan fortrydes bogføring af en montageordre  
1.  For at fortryde en helt eller delvist bogført montageordre skal du vælge ikonet ![Elpære, der åbner funktionen Fortæl mig](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig"), angive **Bogførte montageordrer** og vælge det relaterede link.  

    Siden **Bogførte montageordrer** åbnes med en eller flere bogførte montageordrer, der er bogført fra den pågældende montageordre. Hver delvis bogføring opretter en separat bogført montageordre.  
2.  Åbn den bogførte montageordre, du vil tilbageføre, og vælg derefter handlingen **Fortryd montage**.  

    Hvis den bogført montageordre, du vil fortryde, vedrører et fuldt bogført montageordre, der nu er slettet, har du mulighed for at genoprette den, typisk fordi du ønsker at genbehandle den.  
3.  Hvis du vil genoprette montageordren, skal du vælge knappen **Ja**. Du kan fortryde bogføringen uden at genoprette den relaterede montageordre ved at vælge knappen **Nr.**.  

Feltet **Tilbageført** på montageordrehovedet ændres til **Ja**. Montageordrebogføringen er nu tilbageført, og du kan fortsætte med at behandle hele montageordren, hvis du har valgt at genoprette den eller den åbne montageordre, du har gendannet til den oprindelige tilstand.  

> [!NOTE]  
>  Hvis du vil gendanne mængder fra flere delvise bogføringer i en montageordre, skal du fortryde alle de pågældende bogførte montageordrer ved at følge trin 1 til 3 ovenfor for hver enkelt bogførte montageordre.  

## <a name="see-also"></a>Se også  
[Montagestyring](assembly-assemble-items.md)  
[Tilbageføre kladdeposteringer og annullere modtagelser/leverancer](finance-how-reverse-journal-posting.md)  
[Behandle salgsreturvarer eller annulleringer](sales-how-process-sales-returns-cancellations.md)    
[Arbejde med styklister](inventory-how-work-BOMs.md)  
[Lagerbeholdning](inventory-manage-inventory.md)  
[Designoplysninger: Logistik](design-details-warehouse-management.md)  
[Arbejde med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]