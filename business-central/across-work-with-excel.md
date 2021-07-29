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
ms.date: 04/01/2021
ms.author: jswymer
ms.openlocfilehash: 6bf12f55f6bce843c4ed12f2a40db542367fffde
ms.sourcegitcommit: a7cb0be8eae6ece95f5259d7de7a48b385c9cfeb
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 07/08/2021
ms.locfileid: "6443465"
---
# <a name="viewing-and-editing-in-excel-from-business-central"></a>Visning og redigering i Excel fra Business Central

Med sider, der viser en liste over poster i rækker og kolonner, f.eks. en liste over debitorer, salgsordrer eller fakturaer, kan du også få vist posterne ved hjælp af Microsoft Excel. Afhængigt af siden har du to muligheder for at få vist i Excel. Du kan vælge enten handlingen **Åbn i Excel** eller handlingen **Rediger i Excel** på siden. I denne artikel forklares forskellene mellem de to handlinger.

## <a name="open-in-excel"></a>Åbn i Excel

Med handlingen **Åbn i Excel** kan du foretage ændringer af posterne i Excel, men du kan ikke udgive ændringerne igen [!INCLUDE[prod_short](includes/prod_short.md)]. Du kan kun gemme ændringerne til en Excel-fil på computeren.

- Med denne handling respekterer Excel eventuelle filtre på siden, som begrænser, hvilke poster der vises. Excel-projektmappen indeholder de samme rækker og kolonner, der vises på siden i [!INCLUDE[prod_short](includes/prod_short.md)].

- Denne handling fungerer både på Windows og macOS.

- Fra og med opdatering 18,3 kan du også få vist lister, der vises i Sidedele, f. eks. linjerne i en salgsordre. For øjeblikket er denne funktion valgfri, hvilket kræver, at du aktiverer **Eksporter alle lister til Excel** i **funktionsstyring**. Du kan finde flere oplysninger i [Aktivere Upcoming Features Ahead of Time](/dynamics365/business-central/dev-itpro/administration/feature-management). 

> [!NOTE]
> For [!INCLUDE[prod_short](includes/prod_short.md)] i det lokale miljø er handlingen **Åbn i Excel** tilgængelig som standard. Men hvis du konfigurerer [!INCLUDE[prod_short](includes/prod_short.md)] i det lokale miljø til redigering af data i Excel, erstattes handlingen **Åbn i Excel** med handlingen **Rediger i Excel**.

[!INCLUDE [send-report-excel](includes/send-report-excel.md)]  

## <a name="edit-in-excel"></a>Rediger i Excel

Med handlingen **Rediger i Excel** kan du foretage ændringer af posterne i Excel, men du kan ikke udgive ændringerne igen [!INCLUDE[prod_short](includes/prod_short.md)].

- Med denne handling respekterer Excel de fleste filtre på siden, der begrænser de viste poster, så Excel-projektmappen indeholder næsten de samme poster og kolonner.

- Det fungerer kun i Windows, ikke i macOS.

- Du kan skifte den virksomhed, du arbejder med. Hvis du vil skifte regnskab, skal du vælge **ikonet indstillinger for** ![Excel-Tilføjelsesprogrammet.](media/cogwheel.png "Valgmuligheder for Excel-tilføjelsesprogrammet") I Excel-tilføjelses ruden skal du vælge regnskabet fra feltet **virksomhed**.  

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