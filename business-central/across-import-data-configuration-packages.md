---
title: Bruge Excel til at importere data til Business Central | Microsoft Docs
description: Brug standardkonfigurationspakken til at tilføje debitordata i Excel og importere dataene tilbage til Business Central.
author: edupont04
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: migration, Excel
ms.date: 10/01/2019
ms.author: edupont
ms.openlocfilehash: e4399c16c28d97c0c1c6d8826af14e1b4a48e454
ms.sourcegitcommit: 02e704bc3e01d62072144919774f1244c42827e4
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 10/01/2019
ms.locfileid: "2304968"
---
# <a name="importing-business-data-from-other-finance-systems"></a>Importere virksomhedsdata fra andre økonomisystemer
Når du tilmelder dig [!INCLUDE[d365fin](includes/d365fin_md.md)], kan du oprette en tom virksomhed, så du kan overføre dine egne data og teste den nye virksomhed i [!INCLUDE[d365fin](includes/d365fin_md.md)]. Afhængigt af hvilket økonomisystem, som virksomheden benytter i dag, kan du overføre oplysninger om debitorer, kreditorer, lagerbeholdning og bankkonti.  

Fra rollecenteret kan du starte en assisterede opsætningsvejledning for at overføre forretningsdataene fra en Excel-fil eller fra andre formater. Hvilken type filer, du kan overføre, afhænger af de udvidelser, der findes. F.eks. kan du overføre data fra QuickBooks, da [!INCLUDE[d365fin](includes/d365fin_md.md)] indeholder en udvidelse, der håndterer konverteringen fra QuickBooks. Hvis du vil overføre data fra andre økonomisystemer, skal du enten kontrollere, om en udvidelse er tilgængelig for den pågældende løsning, eller importere fra Excel.  

[!INCLUDE[d365fin](includes/d365fin_md.md)] indeholder skabeloner for konti, debitorer, kreditorer og lagervarer, som du kan vælge at anvende, når du importerer data.

Du kan importere masterdata og nogle transaktionsdata fra andre økonomisystemer baseret på standardkonfigurationspakken i [!INCLUDE[d365fin](includes/d365fin_md.md)]. På siden **Konfigurationspakker** kan du arbejde med pakken for at importere og validere data, før du anvender pakken.  

> [!TIP]  
> Du kan også bruge dataoverførselsguiderne til at importere data fra QuickBooks eller Dynamics GP. Du kan finde flere oplysninger i [Overførsel af QuickBooks-data](ui-extensions-quickbooks-data-migration.md) eller [Overførsel af data med Dynamics GP](ui-extensions-dynamicsgp-data-migration.md).

> [!NOTE]  
> Til større implementeringsarbejde kan du bruge RapidStart Services til [!INCLUDE[d365fin](includes/d365fin_md.md)], som er omfattende værktøj til oprettelse af nye løsninger, der er baseret på kundernes forretningsbehov og opsætningsdata. RapidStart Services indeholder også funktionalitet til import af forretningsdata. Du kan finde flere oplysninger i [Oprette en virksomhed med RapidStart Services](admin-set-up-a-company-with-rapidstart.md).

Du kan bruge en dedikeret funktion på siden **Lageropsætning** til at indlæse varebilleder. Du kan finde flere oplysninger i [Importér flere varebilleder](inventory-how-import-item-pictures.md).

## <a name="importing-data-from-configuration-packages"></a>Importere data fra konfigurationspakker
[!INCLUDE[d365fin](includes/d365fin_md.md)] indeholder en konfigurationspakke, som du kan eksportere til Excel og konfigurere dataene der. Derefter kan du importere dataene fra Excel igen. Pakken indeholder 27 tabeller, herunder masterdata som debitorer, kreditorer, varer og konti, andre grundlæggende opsætningstabeller f.eks. leveringsmetoder og transaktionstabeller, som f.eks. salgshoved og linjer.  

> [!NOTE]  
>   Arbejde med konfigurationspakker er avanceret funktionalitet, og det anbefales, at du kontakter systemadministratoren. Du kan finde flere oplysninger under [Importere data fra ældre regnskabsprogrammer ved hjælp af en konfigurationspakke](across-import-data-configuration-packages.md).

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
-   Finans- kladdelinje
-   Varekladdelinje
-   Debitorbogføringsgruppe
-   Kreditorbogføringsgruppe
-   Varebogføringsgruppe
-   Enhed
-   Finans- Virksomhedsbogf.gruppe
-   Finans- Produktbogf.gruppe
-   Bogføringsopsætning
-   Distrikt
-   Varekategori
-   Salgspris
-   Købspris

## <a name="see-also"></a>Se også
[Oprette en virksomhed med RapidStart Services](admin-set-up-a-company-with-rapidstart.md)  
[Overflytning af QuickBooks Data](ui-extensions-quickbooks-data-migration.md)  
[Overførsel af data med Dynamics GP](ui-extensions-dynamicsgp-data-migration.md)  
[Importér flere varebilleder](inventory-how-import-item-pictures.md)

## [!INCLUDE[d365fin](includes/free_trial_md.md)]  
