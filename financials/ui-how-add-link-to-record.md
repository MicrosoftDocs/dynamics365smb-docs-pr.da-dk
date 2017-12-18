---
title: "Sådan sammenkædes poster med eksterne oplysninger eller programmer | Microsoft Docs"
description: "Indsæt et hyperlink i et dokument eller websted til en bestemt post, f.eks. en debitor eller et dokument."
author: jswymer
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 07/01/2017
ms.author: jswymer
ms.translationtype: HT
ms.sourcegitcommit: ba26b354d235981bd7291f9ac6402779f554ac7a
ms.openlocfilehash: 8eee2a93a56c33fd5cefb70c475e237166017606
ms.contentlocale: da-dk
ms.lasthandoff: 11/10/2017

---
# <a name="adding-links-to-websites-documents-or-programs-on-records"></a>Sådan føjes links til websteder, dokumenter eller programmer på poster
På en bestemt post, f.eks. en debitor, et dokument eller en salgsordre, kan du tilføje et link til et eksternt dokument, websted eller program. Det kan også være, at du ønsker et link, der åbner en ny tom mail til en bestemt modtager, når du vælger det. På kortsiden på nogle poster, f.eks. debitor- og kreditorkort, er der et felt **Hjemmeside**, hvor du kan angive en URL-adresse (internetadresse). Hvis du vil medtage andre links, kan du bruge den metode, der er beskrevet i denne artikel.

Et andet eksempel kan være, når du modtager en trykt faktura fra kreditorer. Du kan scanne den og gemme den som en .pdf-fil på et SharePoint-websted. Derefter kan du oprette et link fra en købsfaktura i [!INCLUDE[d365fin_md](includes/d365fin_md.md)] til den tilsvarende faktura i SharePoint. Eller du kan oprette et link fra et varekort til den tilsvarende side i kreditorens onlinekatalog.

## <a name="to-add-a-link-on-a-record"></a>Sådan tilføjes et link til en post   

1.  Åbn den post, du vil oprette linket til, f.eks. et debitorkort eller en salgsordre. Hvis linket skal knyttes til en bestemt linje, f.eks. en kladdelinje, skal du placere markøren på linjen.  

2.  Vælg handlingen **Links** for at åbne vinduerne **Links**, der viser de aktuelle kæder, der føjes til posten.

3. Hvis du vil tilføje et nyt link, skal du vælge **+ny**.

4.  I feltet **Hyperlinkadresse** skal du angive

    -   Hvis du vil sammenkæde med en fil på din computer eller dit netværk, skal du angive den fulde sti og filnavn, f.eks. **C: Min dokumentfaktura1.doc**.
    -   Hvis du vil sammenkæde med et websted, skal du angive URL-adressen (internetadressen), f.eks. **www.microsoft.com**.
    -   Hvis du vil sammenkæde med et websted, skal du angive URL-adressen (internetadressen), f.eks. **www.microsoft.com**.
    -   Hvis du vil sammenkæde med et program, skal du angive en bestemt streng for at åbne programmet. Hvis du f.eks. vil åbne OneNote med en bestemt side, skal du angive **onenote:///C:Min dokumenttest.one**. Eller hvis du vil åbne Outlook med en ny tom mail til et bestemt alias, skal du angive **mailto:testalias**.  

5.  Angiv oplysninger om linket i feltet **Beskrivelse**.  

6.  Vælg knappen **Gem**.  

## <a name="to-delete-a-link-from-a-record"></a>Sådan slettes et link fra en post  

Hvis du vil slette et link, kan du i vinduet **Links** vælge **...** og derefter **Slet**.

Hvis du sletter en enkelt post, f.eks. en salgsordrelinje, en salgsordre eller en debitor, så slettes alle links med tilknytning til denne post. Men hvis du sletter poster med en kørsel, f.eks. kørslen **Slet fakturerede salgsordrer**, så lagres linksene stadig i databasen. Hvis du vil slette linkene fra databasen, skal du køre codeunit **Slet underordnede postlinks**. For at gøre dette skal du vælge ikonet ![Søg efter side eller rapport](media/ui-search/search_small.png "Ikonet Søg efter side eller rapport"), angive **Slet fakturerede købsreturvareordrer** og derefter vælge det relaterede link.   

<!-- ### To run delete orphaned record links  

1.  Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Data Deletion**, and then choose the related link.  

2.  On the **Data Deletion** page, choose **Tasks**, and then choose **Delete Orphaned Record Links**.  -->

## <a name="see-also"></a>Se også  
[Arbejde med [!INCLUDE[d365fin_long](includes/d365fin_long_md.md)]](ui-work-product.md)  

