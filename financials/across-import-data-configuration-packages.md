---
title: Bruge Excel til at importere data til Financials | Microsoft Docs
description: "Brug standardkonfigurationspakken til at tilføje debitordata i Excel og importere dataene tilbage til Dynamics 365 Business edition."
author: edupont04
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: migration, Excel
ms.date: 07/05/2017
ms.author: edupont
ms.translationtype: HT
ms.sourcegitcommit: ba26b354d235981bd7291f9ac6402779f554ac7a
ms.openlocfilehash: 433d014c41d2508d155891b5ac4e0437c41b3d9e
ms.contentlocale: da-dk
ms.lasthandoff: 11/10/2017

---
# <a name="importing-data-from-legacy-accounting-software-using-a-configuration-package"></a>Importere data fra ældre regnskabsprogrammer ved hjælp af en konfigurationspakke
Du kan importere masterdata og nogle transaktionsdata fra andre økonomisystemer baseret på standardkonfigurationspakken i [!INCLUDE[d365fin](includes/d365fin_md.md)]. I vinduet **Konfigurationspakker** kan du arbejde med pakken for at importere og validere data, før du anvender pakken.  

Hvis du er fortrolig med RapidStart-tjenester til Microsoft Dynamics, kender du også til konfigurationspakker. Standardkonfigurationspakken understøtter de mest almindelige typer data, som du vil importere fra det oprindelige system. I Excel kan du derefter tilføje data fra det oprindelige system og konfigurere dem i overensstemmelse med forretningslogikken i [!INCLUDE[d365fin](includes/d365fin_md.md)].  

> [!TIP]  
>   Du kan også bruge dataoverførselsguiderne til at importere data fra QuickBooks eller Dynamics GP. Du kan finde flere oplysninger i [Overførsel af QuickBooks-data](ui-extensions-quickbooks-data-migration.md) eller [Overførsel af data med Dynamics GP](ui-extensions-dynamicsgp-data-migration.md).  

## <a name="working-with-data-in-excel"></a>Arbejde med data i Excel
Når du eksporterer standardkonfigurationspakken til Excel, indeholder den projektmappe, der oprettes, et regneark for hver tabel i pakken. For at forenkle dine opgaver, kan du drage fordel af de XML-manipulationsværktøjer, der er indbygget i Excel. Du kan også bruge indbyggede funktioner i Excel til at hjælpe med dataformatering og til at indsætte data i den korrekte celle. Tilføj f.eks. et tomt regneark, og kopier de oprindelige data til det. Opret derefter en Excel-formel for at afbilde dataene i overflytningsregnearket mellem felterne i det eksporterede regneark og debitorens ældre data. Når du har tilknyttet alle data, skal du kopiere dataområdet ind i regnearket med tabellen.  

> [!IMPORTANT]  
>  Undlad at ændre kolonnerne i regnearkene. Hvis de flyttes, ændres eller slettes, kan regnearket ikke importeres i [!INCLUDE[d365fin](includes/d365fin_md.md)].

## <a name="tables-in-the-default-configuration-package"></a>Tabeller i standardkonfigurationspakken
Standardkonfigurationspakken understøtter følgende tabeller:

-   Betalingsbetingelser
-   Debitorprisgruppe
-   Leveringsform
-   Sælger/indkøber
-   Sted
-   Finanskonto
-   Kunde
-   Kreditor
-   Vare
-   Salgshoved
-   Salgslinje
-   Købshoved
-   Købslinje
-   Finanskladdelinje
-   Varekladdelinje
-   Debitorbogføringsgruppe
-   Kreditorbogføringsgruppe
-   Varebogføringsgruppe
-   Enhed
-   Virksomhedsbogføringsgruppe
-   Produktbogføringsgruppe
-   Bogføringsopsætning
-   Distrikt
-   Varekategori
-   Salgspris
-   Købspris

## <a name="importing-customer-data"></a>Import af debitordata
Når debitordata er indsat i Excel, kan du importere dataene i [!INCLUDE[d365fin](includes/d365fin_md.md)]. I vinduet **Konfigurationspakker** kan du indlæse dataene fra Excel-filen, og du kan kontrollere, at dataene er i overensstemmelse med [!INCLUDE[d365fin](includes/d365fin_md.md)], før du anvender pakken.

## <a name="see-also"></a>Se også
[Importere virksomhedsdata fra andre økonomisystemer](upload-data.md)  
[Overflytning af QuickBooks Data](ui-extensions-quickbooks-data-migration.md)  
[Overførsel af data med Dynamics GP](ui-extensions-dynamicsgp-data-migration.md)  

## [!INCLUDE[d365fin](includes/free_trial_md.md)]

