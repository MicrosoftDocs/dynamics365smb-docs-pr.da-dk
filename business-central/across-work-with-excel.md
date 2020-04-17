---
title: Visning og redigering i Excel fra Business Central | Microsoft Docs
description: Få mere at vide om, hvordan du kan åbne siderne i Microsoft Excel fra Business Central for at få en bedre dataanalyse.
author: jswymer
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: accountant, accounting, financial report
ms.date: 04/01/2020
ms.author: jswymer
ms.openlocfilehash: 2c6600ac7fe9f6e0aa44554883209039faabbd99
ms.sourcegitcommit: 88e4b30eaf6fa32af0c1452ce2f85ff1111c75e2
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 04/01/2020
ms.locfileid: "3187504"
---
# <a name="viewing-and-editing-in-excel-from-business-central"></a>Visning og redigering i Excel fra Business Central

Med sider, der viser en liste over poster i rækker og kolonner, f.eks. en liste over debitorer, salgsordrer eller fakturaer, kan du også få vist posterne ved hjælp af Microsoft Excel. Du har to muligheder for at gøre dette. Du kan vælge enten handlingen **Åbn i Excel** eller handlingen **Rediger i Excel** på siden. Forskellen på de to handlinger er følgende:  

## <a name="open-in-excel"></a>Åbn i Excel

- Med denne handling respekterer Excel eventuelle filtre på siden, som begrænser, hvilke poster der vises. Det betyder, at Excel-projektmappen indeholder de samme rækker og kolonner, der vises på siden i [!INCLUDE[prodshort](includes/prodshort.md)].

- Du kan foretage ændringer af posterne i Excel, men du kan ikke publicere ændringerne tilbage til [!INCLUDE[prodshort](includes/prodshort.md)]. Du kan kun gemme ændringerne til en Excel-fil på computeren.

- Denne handling fungerer både på Windows og macOS.

> [!NOTE]
> For [!INCLUDE[prodshort](includes/prodshort.md)] i det lokale miljø er handlingen **Åbn i Excel** tilgængelig som standard. Men hvis du konfigurerer [!INCLUDE [prodshort](includes/prodshort.md)] i det lokale miljø til redigering af data i Excel, erstattes handlingen **Åbn i Excel** med handlingen **Rediger i Excel**.

## <a name="edit-in-excel"></a>Rediger i Excel

- Med denne handling respekterer Excel de fleste filtre på siden, som begrænser, hvilke poster der vises. Det betyder, at Excel-projektmappen indeholder næsten de samme poster og kolonner.

- Fordelen ved handlingen **Rediger i Excel** er, at du kan ændre poster i Excel og derefter publicere ændringerne tilbage til [!INCLUDE[prodshort](includes/prodshort.md)].

- Det fungerer kun i Windows, ikke i macOS.

- Du kan skifte den virksomhed, du arbejder med. Du kan gøre dette ved at vælge ikonet **Valgmuligheder** ![Valgmuligheder for Excel-tilføjelsesprogram](media/cogwheel.png "Valgmuligheder for Excel-tilføjelsesprogrammet") i ruden Excel-tilføjelsesprogram og derefter vælge virksomheden i feltet **Virksomhed**. 

    > [!IMPORTANT]
    > Når du skifter virksomhed, skal du sikre, at feltet **Miljø** ikke er tomt. Hvis det er, skal du angive det som en af de tilgængelige indstillinger. Ellers fungerer tilføjelsesprogrammet ikke korrekt.  

Excel-Tilføjelsesprogrammet er udvidet i 2019-udgivelsesbølge 2. Du kan finde flere oplysninger [Forbedringer af Excel-integration](/dynamics365-release-plan/2019wave2/dynamics365-business-central/enhancements-excel-integration)af Excel.

> [!NOTE]
> For [!INCLUDE[prodshort](includes/prodshort.md)] i det lokale miljø er handlingen **Rediger i Excel** kun tilgængelig, hvis Excel-tilføjelsesprogrammet er konfigureret af administratoren, og kun tilgængelig til webklienten. Til administratorer, hvis du vil vide, hvordan du installerer Excel-tilføjelsesprogrammet, skal du se [Konfigurere Excel-tilføjelsesprogrammet til redigering af Business Central-data](/dynamics365/business-central/dev-itpro/administration/configuring-excel-addin). For [!INCLUDE[prodshort](includes/prodshort.md)] i det lokale miljø.

### <a name="see-the-differences-between-the-options"></a>Se forskellene mellem indstillingerne
<br><br>  

> [!Video https://go.microsoft.com/fwlink/?linkid=2086039]

## <a name="see-related-training-at-microsoft-learn"></a>Se relateret oplæring på [Microsoft Learn](/learn/modules/configure-powerbi-excel-dynamics-365-business-central/index)

## <a name="see-also"></a>Se også
[Arbejde med Business Central](ui-work-product.md)  
