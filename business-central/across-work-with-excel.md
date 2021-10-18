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
ms.openlocfilehash: 012fedb26c4d98d4014efdb53327c82b8a6877c8
ms.sourcegitcommit: 6ad0a834fc225cc27dfdbee4a83cf06bbbcbc1c9
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 10/01/2021
ms.locfileid: "7587552"
---
# <a name="viewing-and-editing-in-excel-from-business-central"></a>Visning og redigering i Excel fra Business Central

Med sider, der viser en liste over poster i rækker og kolonner, f.eks. en liste over debitorer, salgsordrer eller fakturaer, kan du eksportere lisen til Microsoft Excel og vise den her. Afhængigt af siden har du to muligheder for at få vist i Excel. Begge muligheder er tilgængelige fra **Del**-ikonet ![Del en side i en anden app.](media/share-icon.png) øverst på siden. Du kan vælge enten handlingen **Åbn i Excel** eller handlingen **Rediger i Excel** på siden. I denne artikel forklares forskellene mellem de to handlinger.

## <a name="open-in-excel"></a>Åbn i Excel

Med handlingen **Åbn i Excel** kan du foretage ændringer af posterne i Excel, men du kan ikke udgive ændringerne igen [!INCLUDE[prod_short](includes/prod_short.md)]. Du kan kun gemme ændringerne i Excel-filen, uden at det påvirker data i [!INCLUDE[prod_short](includes/prod_short.md)].

- Med denne handling respekterer Excel eventuelle filtre på siden, som begrænser, hvilke poster der vises. Excel-projektmappen indeholder de samme rækker og kolonner, der vises på siden i [!INCLUDE[prod_short](includes/prod_short.md)].

- Denne handling fungerer både på Windows og macOS.

- Fra og med opdatering 18,3 kan du også få vist lister, der vises i Sidedele, f. eks. linjerne i en salgsordre. 

> [!NOTE]
> For [!INCLUDE[prod_short](includes/prod_short.md)] i det lokale miljø er handlingen **Åbn i Excel** tilgængelig som standard. Men hvis du konfigurerer [!INCLUDE[prod_short](includes/prod_short.md)] i det lokale miljø til redigering af data i Excel, erstattes handlingen **Åbn i Excel** med handlingen **Rediger i Excel**.

[!INCLUDE [send-report-excel](includes/send-report-excel.md)]  

## <a name="edit-in-excel"></a>Rediger i Excel

Handlingen **Rediger i Excel** er tilgængelig på de fleste lister, men ikke for alle. Med handlingen **Rediger i Excel** kan du foretage ændringer af posterne i Excel, men du kan ikke udgive ændringerne igen [!INCLUDE[prod_short](includes/prod_short.md)]. Når Excel åbnes, vises ruden **Excel-Tilføjelsesprogrammet** til højre.

- Med denne handling respekterer Excel de fleste filtre på siden, der begrænser de viste poster, så Excel-projektmappen indeholder næsten de samme poster og kolonner.

- Hvis du vil hente de nyeste data fra [!INCLUDE[prod_short](includes/prod_short.md)], skal du vælge **Opdater** i ruden Excel-Tilføjelsesprogrammet.

- Du kan skifte den virksomhed, du arbejder med. Hvis du vil skifte regnskab, skal du vælge **ikonet indstillinger for** ![Excel-Tilføjelsesprogrammet.](media/cogwheel.png "Valgmuligheder for Excel-tilføjelsesprogrammet") I Excel-tilføjelses ruden skal du vælge regnskabet fra feltet **virksomhed**.  

    > [!IMPORTANT]
    > Når du skifter virksomhed, skal du sikre, at feltet **Miljø** ikke er tomt. Hvis det er, skal du angive det som en af de tilgængelige indstillinger. Ellers fungerer tilføjelsesprogrammet ikke korrekt.  

Hvis du foretager ændringer af tilføjelsesprogrammet, skal du genindlæse det for at opdatere forbindelsen. Hvis du vil genindlæse, skal du bruge ![menuen Excel-tilføjelsesprogram](media/excel-addin-menu.png "Menuen Excel-tilføjelsesprogram") i øverste højre hjørne af tilføjelsesprogrammet. Hvis du ikke kan indlæse tilføjelsesprogrammet, skal du tale med administratoren. Hvis du er administrator, skal du se [Hent Excel-tilføjelsesprogrammet til redigering af Business Central](admin-deploy-excel-addin.md).

> [!NOTE]
> Tilføjelsesprogrammet fungerer sammen med Excel til Web (online) fra enhver enhed, så blot som brug af en understøttet webbrowser. Den fungerer også sammen med Excel-appen til Windows (PC) - men ikke til macOS.
>
> For [!INCLUDE[prod_short](includes/prod_short.md)] i det lokale miljø er handlingen **Rediger i Excel** kun tilgængelig, hvis Excel-tilføjelsesprogrammet er konfigureret af administratoren, og kun tilgængelig til webklienten. Til administratorer, hvis du vil vide, hvordan du installerer Excel-tilføjelsesprogrammet, skal du se [Konfigurere Excel-tilføjelsesprogrammet til redigering af Business Central-data](/dynamics365/business-central/dev-itpro/administration/configuring-excel-addin).


<!-- Note for later: here we're immediately jumping to pretty advanced topics like changing company or reloading the addin. Fine to keep them for now. In the future, we will first need to explain in more detail the actual functionality of the addin, primarily these sub-sections:

Refreshing record data in Excel
Editing and publishing back to Business Central
Creating new records from Excel
Crafting your own editable Excel.
Point (4) is where it gets interesting for changing/specifying company, environment and other connection settings-->

### <a name="first-time-sign-in"></a>Log på første gang

Handlingen **Rediger i Excel** kræver, at det Business Central-tilføjelsesprogram er installeret i Excel. Det kan ske, at din administrator har konfigureret, at tilføjelsesprogrammet automatisk bliver installeret. I dette tilfælde skal du blot logge på Business central i **Excel-Tilføjelsesprogram** med dit brugernavn og din adgangskode. Hvis du ikke gør det, åbnes **Nyt Office-tilføjelsesprogram**. Hvis du vil installere tilføjelsesprogrammet, skal du vælge **Hav tillid til tilføjelsesprogrammet**, som vil installere tilføjelsesprogrammet direkte fra Office store.

Hvis tilføjelsesprogrammet af en eller anden grund ikke installeres, skal du kontakte administratoren eller prøve at installere det manuelt. Du kan finde flere oplysninger i [installere tilføjelsesprogrammet manuelt til eget brug](admin-deploy-excel-addin.md#install).

## <a name="see-the-differences-between-the-options"></a>Se forskellene mellem indstillingerne
<br><br>  

> [!Video https://go.microsoft.com/fwlink/?linkid=2086039]

## <a name="see-related-training-at-microsoft-learn"></a>Se relateret træning på [Microsoft Learn](/learn/modules/configure-powerbi-excel-dynamics-365-business-central/index)

## <a name="see-also"></a>Se også

[Analysere regnskaber i Microsoft Excel](finance-analyze-excel.md)  
[Arbejde med Business Central](ui-work-product.md)  
[Forbedringer af Excel-integration i frigivelsesbølge 2 i 2019](/dynamics365-release-plan/2019wave2/dynamics365-business-central/enhancements-excel-integration)  


[!INCLUDE[footer-include](includes/footer-banner.md)]