---
title: Sådan sammenkædes poster med eksterne oplysninger eller programmer | Microsoft Docs
description: Indsæt et hyperlink i et dokument eller websted til en bestemt post, f.eks. en debitor eller et dokument.
author: jswymer
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/12/2019
ms.author: jswymer
ms.openlocfilehash: 602d520043c5192109ccc4e2605ae0e231dafc1e
ms.sourcegitcommit: addfb47612cc2e4e98dfd7e338b6f41cde405d5c
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 04/12/2019
ms.locfileid: "990173"
---
# <a name="add-links-to-websites-documents-or-programs-on-records"></a>Føje links til websteder, dokumenter eller programmer på poster
På en bestemt post, f.eks. en debitor, et dokument eller en salgsordre, kan du tilføje et link til et eksternt dokument, websted eller program. Det kan også være, at du ønsker et link, der åbner en ny tom mail til en bestemt modtager, når du vælger det. På kortsiden på nogle poster, f.eks. debitor- og kreditorkort, er der et felt **Hjemmeside**, hvor du kan angive en URL-adresse (internetadresse). Hvis du vil medtage andre links, kan du bruge den metode, der er beskrevet i denne artikel.  

> [!IMPORTANT]
> I øjeblikket er denne funktion kun tilgængelig på [!INCLUDE [prodshort](includes/prodshort.md)] i lokale installationer med den ældre Dynamics NAV Windows-klient.  

Et andet eksempel kan være, når du modtager en trykt faktura fra kreditorer. Du kan scanne den og gemme den som en .pdf-fil på et SharePoint-websted. Derefter kan du oprette et link fra en købsfaktura i [!INCLUDE[d365fin_md](includes/d365fin_md.md)] til den tilsvarende faktura i SharePoint. Eller du kan oprette et link fra et varekort til den tilsvarende side i kreditorens onlinekatalog.

## <a name="to-add-a-link-on-a-record"></a>Sådan tilføjes et link til en post   

1.  Åbn den post, du vil oprette linket til, f.eks. et debitorkort eller en salgsordre. Hvis linket skal knyttes til en bestemt linje, f.eks. en kladdelinje, skal du placere markøren på linjen.  

2.  Vælg handlingen **Links** for at åbne siderne **Links**, der viser de aktuelle kæder, der føjes til posten.

3. Hvis du vil tilføje et nyt link, skal du vælge **+ny**.

4.  I feltet **Hyperlinkadresse** skal du angive

    -   Hvis du vil sammenkæde med en fil på din computer eller dit netværk, skal du angive den fulde sti og filnavn, f.eks. **C: Min dokumentfaktura1.doc**.
    -   Hvis du vil sammenkæde med et websted, skal du angive URL-adressen (internetadressen), f.eks. **www.microsoft.com**.
    -   Hvis du vil sammenkæde med et websted, skal du angive URL-adressen (internetadressen), f.eks. **www.microsoft.com**.
    -   Hvis du vil sammenkæde med et program, skal du angive en bestemt streng for at åbne programmet. Hvis du f.eks. vil åbne OneNote med en bestemt side, skal du angive **OneNote:///C:Min dokumenttest.one**. Eller hvis du vil åbne Outlook med en ny tom mail til et bestemt alias, skal du angive **mailto:testalias**.  

5.  Angiv oplysninger om linket i feltet **Beskrivelse**.  

6.  Vælg knappen **Gem**.  

## <a name="to-delete-a-link-from-a-record"></a>Sådan slettes et link fra en post  

Hvis du vil slette et link, kan du på siden **Links** vælge **...** og derefter **Slet**.

Hvis du sletter en enkelt post, f.eks. en salgsordrelinje, en salgsordre eller en debitor, så slettes alle links med tilknytning til denne post. Men hvis du sletter poster med en kørsel, f.eks. kørslen **Slet fakturerede salgsordrer**, så lagres linksene stadig i databasen. Hvis du vil slette linkene fra databasen, skal du køre codeunit **Slet underordnede postlinks**. For at gøre dette skal du vælge ikonet ![Elpære, der åbner funktionen Fortæl mig](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig"), angiv **Slet uafhængige posttilknytninger**, og vælg derefter det relaterede link.   

<!-- ### To run delete orphaned record links  

1.  Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Data Deletion**, and then choose the related link.  

2.  On the **Data Deletion** page, choose **Tasks**, and then choose **Delete Orphaned Record Links**.  -->

## <a name="see-also"></a>Se også  
[Arbejde med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)  
