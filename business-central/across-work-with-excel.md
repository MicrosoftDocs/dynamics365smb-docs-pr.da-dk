---
title: Visning og redigering i Excel fra Business Central
description: Få mere at vide om, hvordan du kan åbne siderne i Microsoft Excel fra Business Central for at få en bedre dataanalyse.
author: jswymer
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: accountant, accounting, financial report
ms.date: 11/06/2020
ms.author: jswymer
ms.openlocfilehash: 5e585d4bc7d9f7ce159671c10298f734fd5a09d5
ms.sourcegitcommit: ff2b55b7e790447e0c1fcd5c2ec7f7610338ebaa
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 02/15/2021
ms.locfileid: "5378819"
---
# <a name="viewing-and-editing-in-excel-from-business-central"></a>Visning og redigering i Excel fra Business Central

Med sider, der viser en liste over poster i rækker og kolonner, f.eks. en liste over debitorer, salgsordrer eller fakturaer, kan du også få vist posterne ved hjælp af Microsoft Excel. Du har to muligheder for at gøre dette. Du kan vælge enten handlingen **Åbn i Excel** eller handlingen **Rediger i Excel** på siden. Forskellen på de to handlinger er følgende:  

## <a name="open-in-excel"></a>Åbn i Excel

- Med denne handling respekterer Excel eventuelle filtre på siden, som begrænser, hvilke poster der vises. Excel-projektmappen indeholder de samme rækker og kolonner, der vises på siden i [!INCLUDE[prod_short](includes/prod_short.md)].

- Du kan foretage ændringer af posterne i Excel, men du kan ikke publicere ændringerne tilbage til [!INCLUDE[prod_short](includes/prod_short.md)]. Du kan kun gemme ændringerne til en Excel-fil på computeren.

- Denne handling fungerer både på Windows og macOS.

> [!NOTE]
> For [!INCLUDE[prod_short](includes/prod_short.md)] i det lokale miljø er handlingen **Åbn i Excel** tilgængelig som standard. Men hvis du konfigurerer [!INCLUDE[prod_short](includes/prod_short.md)] i det lokale miljø til redigering af data i Excel, erstattes handlingen **Åbn i Excel** med handlingen **Rediger i Excel**.

## <a name="edit-in-excel"></a>Rediger i Excel

- Med denne handling respekterer Excel de fleste filtre på siden, der begrænser de viste poster, så Excel-projektmappen indeholder næsten de samme poster og kolonner.

- Fordelen ved handlingen **Rediger i Excel** er, at du kan ændre poster i Excel og derefter publicere ændringerne tilbage til [!INCLUDE[prod_short](includes/prod_short.md)].

- Det fungerer kun i Windows, ikke i macOS.

- Du kan skifte den virksomhed, du arbejder med. Skift virksomhed ved at vælge ikonet **Valgmuligheder** ![Valgmuligheder for Excel-tilføjelsesprogram](media/cogwheel.png "Valgmuligheder for Excel-tilføjelsesprogrammet") i ruden Excel-tilføjelsesprogram og derefter vælge virksomheden i feltet **Virksomhed**.  

    > [!IMPORTANT]
    > Når du skifter virksomhed, skal du sikre, at feltet **Miljø** ikke er tomt. Hvis det er, skal du angive det som en af de tilgængelige indstillinger. Ellers fungerer tilføjelsesprogrammet ikke korrekt.  

Hvis du foretager ændringer af tilføjelsesprogrammet, skal du genindlæse det for at opdatere forbindelsen. Hvis du vil genindlæse, skal du bruge ![menuen Excel-tilføjelsesprogram](media/excel-addin-menu.png "Menuen Excel-tilføjelsesprogram") i øverste højre hjørne af tilføjelsesprogrammet. Hvis du ikke kan indlæse tilføjelsesprogrammet, skal du tale med administratoren. Hvis du er administrator, skal du se [Konfigurere Excel-tilføjelsesprogrammet til redigering af Business Central-data](/dynamics365/business-central/dev-itpro/administration/configuring-excel-addin).

> [!NOTE]
> For [!INCLUDE[prod_short](includes/prod_short.md)] i det lokale miljø er handlingen **Rediger i Excel** kun tilgængelig, hvis Excel-tilføjelsesprogrammet er konfigureret af administratoren, og kun tilgængelig til webklienten. Til administratorer, hvis du vil vide, hvordan du installerer Excel-tilføjelsesprogrammet, skal du se [Konfigurere Excel-tilføjelsesprogrammet til redigering af Business Central-data](/dynamics365/business-central/dev-itpro/administration/configuring-excel-addin).

### <a name="see-the-differences-between-the-options"></a>Se forskellene mellem indstillingerne
<br><br>  

> [!Video https://go.microsoft.com/fwlink/?linkid=2086039]

## <a name="see-related-training-at-microsoft-learn"></a>Se relateret træning på [Microsoft Learn](/learn/modules/configure-powerbi-excel-dynamics-365-business-central/index)

## <a name="see-also"></a>Se også

[Analysere regnskaber i Microsoft Excel](finance-analyze-excel.md)  
[Arbejde med Business Central](ui-work-product.md)  
[Forbedringer af Excel-integration i frigivelsesbølge 2 i 2019](/dynamics365-release-plan/2019wave2/dynamics365-business-central/enhancements-excel-integration)  


[!INCLUDE[footer-include](includes/footer-banner.md)]