---
title: Visning og redigering i Excel fra Business Central
description: 'Få mere at vide om, hvordan du kan åbne siderne i Microsoft Excel fra Business Central for at få en bedre dataanalyse.'
author: jswymer
ms.topic: conceptual
ms.devlang: al
ms.search.form: 1480
ms.search.keywords: 'accountant, accounting, financial report'
ms.date: 06/13/2024
ms.author: jswymer
ms.service: dynamics-365-business-central
ms.reviewer: jswymer
---
# Vise og redigere i Excel fra Business Central

Med sider, der viser en liste over poster i rækker og kolonner, f.eks. en liste over debitorer, salgsordrer eller fakturaer, kan du eksportere lisen til Microsoft Excel og vise den her. Afhængigt af siden har du to muligheder for at få vist i Excel. Begge muligheder er tilgængelige fra **Del**-ikonet ![Del en side i en anden app.](media/share-icon.png) øverst på siden. Du kan vælge enten handlingen **Åbn i Excel** eller handlingen **Rediger i Excel** på siden. I denne artikel forklares de to handlinger.

## Åbn i Excel

Med handlingen **Åbn i Excel** kan du foretage ændringer af posterne i Excel, men du kan ikke udgive ændringerne igen [!INCLUDE[prod_short](includes/prod_short.md)]. Du kan kun gemme ændringerne i Excel-filen, uden at det påvirker data i [!INCLUDE[prod_short](includes/prod_short.md)].

- Med denne handling respekterer Excel eventuelle filtre på siden, som begrænser, hvilke poster der vises. Excel-projektmappen indeholder de samme rækker og kolonner, der vises på siden i [!INCLUDE[prod_short](includes/prod_short.md)].

- Denne handling fungerer både på Windows og macOS.
- [!INCLUDE[open-edit-excel](includes/open-and-edit-excel.md)]

<!-- 
> [!IMPORTANT]
> For [!INCLUDE[prod_short](includes/prod_short.md)] on-premises, the **Open in Excel** action is available by default. However, if you set up [!INCLUDE[prod_short](includes/prod_short.md)] on-premises for editing data in Excel, then the **Open in Excel** action is replaced by the **Edit in Excel** action.-->

[!INCLUDE [send-report-excel](includes/send-report-excel.md)] 

> [!NOTE]
> I Excel vil hele tal i kolonner være angivet med decimaltegn i slutningen (f. eks. et punktum `.` eller et komma `,`), selvom decimaltegnet ikke vises i Business Central. Decimaltegnet afhænger af indstillingerne for enhedens område. I Business Central kan f. eks. `10` være vist som `10.` eller `10,` i Excel. Du kan ændre formatet i Excel ved at markere værdierne og derefter vælge <kbd>Ctrl</kbd>+<kbd>1</kbd>. Hvis du vil vide mere om ændring af talformatet i Excel, skal du gå til [Formatere tal](https://support.microsoft.com/office/format-numbers-f27f865b-2dc5-4970-b289-5286be8b994a).

## Rediger i Excel

Handlingen **Rediger i Excel** er tilgængelig på de fleste lister, men ikke for alle. Med handlingen **Rediger i Excel** kan du foretage ændringer af posterne i Excel, men du kan ikke udgive ændringerne igen [!INCLUDE[prod_short](includes/prod_short.md)]. Når Excel åbnes, vises ruden **Excel-Tilføjelsesprogrammet** til højre.

- Med denne handling respekterer Excel de fleste filtre på siden, der begrænser de viste poster, så Excel-projektmappen indeholder næsten de samme poster og kolonner.

- Hvis du vil hente de nyeste data fra [!INCLUDE[prod_short](includes/prod_short.md)], skal du vælge **Opdater** i ruden Excel-tilføjelsesprogram.
- [!INCLUDE[open-edit-excel](includes/open-and-edit-excel.md)]

### Log på første gang

Handlingen **Rediger i Excel** kræver, at det Business Central-tilføjelsesprogram er installeret i Excel. Det kan ske, at din administrator har konfigureret, at tilføjelsesprogrammet automatisk bliver installeret. I dette tilfælde skal du blot logge på Business central i **Excel-Tilføjelsesprogram** med dit brugernavn og din adgangskode. Hvis du ikke gør det, åbnes **Nyt Office-tilføjelsesprogram**. Hvis du vil installere tilføjelsesprogrammet, skal du vælge **Hav tillid til tilføjelsesprogrammet**, som vil installere tilføjelsesprogrammet direkte fra Office store.

Hvis tilføjelsesprogrammet ikke installeres, skal du enten kontakte administratoren eller prøve at installere det manuelt. Du kan finde flere oplysninger i [installere tilføjelsesprogrammet manuelt til eget brug](admin-deploy-excel-addin.md#install).

### Arbejde på tværs af miljøer og virksomheder

Du kan skifte den virksomhed, du arbejder med. Hvis du vil skifte regnskab, skal du vælge **ikonet indstillinger for** ![Excel-Tilføjelsesprogrammet.](media/cogwheel.png "Valgmuligheder for Excel-tilføjelsesprogrammet") I Excel-tilføjelses ruden skal du vælge regnskabet fra feltet **virksomhed**.  

> [!IMPORTANT]
> Når du skifter virksomhed, skal du sikre, at feltet **Miljø** ikke er tomt. Hvis det er, skal du angive det som en af de tilgængelige indstillinger. Ellers fungerer tilføjelsesprogrammet ikke korrekt.  

Hvis du foretager ændringer af tilføjelsesprogrammet, skal du genindlæse det for at opdatere forbindelsen. Hvis du vil genindlæse, skal du bruge ![menuen Excel-tilføjelsesprogram](media/excel-addin-menu.png "Menuen Excel-tilføjelsesprogram") i øverste højre hjørne af tilføjelsesprogrammet. Hvis du ikke kan indlæse tilføjelsesprogrammet, skal du tale med administratoren. Hvis du er administrator, skal du se [Hent Excel-tilføjelsesprogrammet til redigering af Business Central](admin-deploy-excel-addin.md).

> [!NOTE]
> Tilføjelsesprogrammet fungerer sammen med Excel til Web (online) fra enhver enhed, så blot som brug af en understøttet webbrowser. Den fungerer også sammen med Excel-appen til Windows (PC) - men ikke til macOS.
>
> For [!INCLUDE[prod_short](includes/prod_short.md)] i det lokale miljø er handlingen **Rediger i Excel** kun tilgængelig, hvis Excel-tilføjelsesprogrammet er konfigureret af administratoren, og kun tilgængelig til webklienten. Til administratorer, hvis du vil vide, hvordan du installerer Excel-tilføjelsesprogrammet, skal du se [Konfigurere Excel-tilføjelsesprogrammet til redigering af Business Central-data](/dynamics365/business-central/dev-itpro/administration/configuring-excel-addin).

### Grænser for brug af Excel på internettet

Når **Rediger i Excel** bruges på listesider til tabeller med mange kolonner, kan den resulterende projektmappe indeholde for mange kolonner, så filen ikke kan ses i Excel på internettet. [!INCLUDE[prod_short](includes/prod_short.md)] begrænser automatisk den eksporterede projektmappe til 100 kolonner, når OneDrive er konfigureret til systemfunktioner. 

<!--## See the differences between the options
<br><br>  

> [!Video https://go.microsoft.com/fwlink/?linkid=2086039]-->

## Se også

[Analysere regnskaber i Microsoft Excel](finance-analyze-excel.md)  
[Arbejde med Business Central](ui-work-product.md)  
[Forbedringer af Excel-integration i frigivelsesbølge 2 i 2019](/dynamics365-release-plan/2019wave2/dynamics365-business-central/enhancements-excel-integration)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
