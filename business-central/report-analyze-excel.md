---
title: Analyse af rapportdata med Excel
description: Få mere at vide om, hvordan du bruger Excel til at analysere et rapportdatasæt.
author: jswymer
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: task, process, report, print, schedule, save, Excel, PDF, Word, dataset
ms.date: 02/09/2022
ms.author: jswymer
ms.openlocfilehash: f3996c051eed69974de9511aa570f232e44764fa
ms.sourcegitcommit: ef80c461713fff1a75998766e7a4ed3a7c6121d0
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 02/15/2022
ms.locfileid: "8145468"
---
# <a name="analyzing-report-data-with-excel"></a>Analyse af rapportdata med Excel

[!INCLUDE[2021_releasewave2](includes/2021_releasewave2.md)]

Som udvikler eller erfaren bruger er det en hjælp at kontrollere de data, der er genereret for et givet rapportdatasæt, når du opretter nye rapporter eller redigerer eksisterende. For at understøtte denne funktion kan du eksportere et rapport datasæt som rådata til et Excel-regneark - direkte fra rapport anmodningssiden i klienten. I Excel kan du derefter foretage ad hoc-analyser af dataene og diagnosticere problemer.

## <a name="get-started"></a>Kom i gang

Hvis du vil eksportere rapportdatasæt til Excel, skal du åbne rapporten i klienten og vælge **Send til** > **Microsoft Excel -dokument (kun data)** på anmodningssiden. 

**Microsoft Excel-dokument (kun data)** eksporterer rapportresultaterne og de kriterier, der blev brugt til at oprette dem, men som ikke omfatter rapportlayoutet. Excel-filen vil indeholde hele datasættet, som rådata, arrangeret i rækker og kolonner. Alle datakolonner i rapportens datasæt medtages, uanset om de bruges i rapportlayoutet.

Når du har Excel-filen, kan du starte analysen af data. Du kan f. eks. filtrere dataene og bruge Power Pivot til at få dem vist.

Hver gang du eksporterer resultater, oprettes der et nyt regneark. Når du bruger **Microsoft Excel-dokument (kun data)** kan du udføre samme rapport og genbruge formateringsændringer. F.eks. for Power Pivot kan du køre rapporten igen i en anden tidsperiode, kopiere resultaterne til regnearket og derefter opdatere regnearket. Du kan også finde en app til rapportering på [AppSource](https://appsource.microsoft.com/).

> [!NOTE]
> Du kan ikke eksportere en rapport, der indeholder mere end 1,048,576 rækker eller 16.384 kolonner. Med Business Central lokalt kan det maksimale antal udlæste rækker være endnu mindre. Business central server indeholder en konfigurationsindstilling, der kaldes **Maks. antal tilladte datarækker, der kan sendes til Excel**, med henblik på at reducere grænsen fra maksimumværdien. Du kan finde flere oplysninger i [konfigurere Business central server](/dynamics365/business-central/dev-itpro/administration/configure-server-instance#General) eller ved at kontakte administratoren.

## <a name="for-administrators"></a>Til administratorer

- **Microsoft Excel-dokument (kun data)** blev introduceret som en valgfri funktion i 2021 Release Wave 1, opdatering 18,3. Hvis du vil give brugere adgang til denne funktion, når du kører 2021 udgivelsesbølge 1, skal du aktivere funktionen **Gem rapportdatasæt i Microsoft Excel-dokument** i **Funktionsstyring**. Du kan finde flere oplysninger i [Aktivere Upcoming Features Ahead of Time](/dynamics365/business-central/dev-itpro/administration/feature-management). I 2021 udgivelsesbølge 2 er denne funktion permanent, så du behøver ikke at aktivere den.

- Hvis du vil bruge **Microsoft Excel-dokument (kun data)**, skal brugerkonti bruge funktionen **Tillad handlingseksport af rapportdatasæt til Excel**-tilladelse. Du kan give brugere denne tilladelse ved at tildele et **Fejlfindingsværktøjer** eller **Eksporter rapport til Excel**-tilladelsessæt. Du kan finde flere oplysninger i [Tildele rettigheder til brugere og grupper](ui-define-granular-permissions.md)  

## <a name="for-developers-and-advanced-users"></a>For udviklere og erfarne brugere

Funktionen **Microsoft Excel-dokument (kun data)** eksporterer alle kolonner, herunder kolonner, der indeholder filtre og oplysninger om formatering af andre værdier. Her er nogle af interessepunkterne:

- Binære data i et felt, f. eks. et billede, eksporteres ikke.

  I kolonner, der indeholder binære data, vil felter indeholde teksten **Binære data ({0} byte)**, hvor **{0}** angiver antallet af byte.
- Fra og med Business Central 2021 Release Wave 2 indeholder Excel-filen også regnearket **Rapport-metadata**.

  I dette regneark vises de filtre, der anvendes til rapporten, og de generelle rapportegenskaber, f. eks. navn, ID og udvidelsesdetaljer. Filtrene vises i kolonnen **Filter (dataelement::tabel::FilterGroupNo::feltnavn)**. Filtrene i denne kolonne indeholder filtersæt, der er angivet på rapportens anmodningsside. Den indeholder også filtre, der er defineret i AL kode, f. eks. ved at bruge [egenskaben DataItemLink](/dynamics365/business-central/dev-itpro/developer/properties/devenv-dataitemlink-reports-property) og [egenskaben DataItemTableView](/dynamics365/business-central/dev-itpro/developer/properties/devenv-dataitemtableview-property).

Du kan finde flere oplysninger om rapportdesign i [rapportoversigt](/dynamics365/business-central/dev-itpro/developer/devenv-reports).

## <a name="see-also"></a>Se også

[Arbejde med rapporter](ui-work-report.md)  
[Administrere rapport- og dokumentlayout](ui-manage-report-layouts.md)  
[Tildel rettigheder til brugere og grupper](ui-define-granular-permissions.md)  
[Arbejde med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)

[!INCLUDE[footer-include](includes/footer-banner.md)]