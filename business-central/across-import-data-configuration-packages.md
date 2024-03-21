---
title: Brug Excel til at importere data til Business Central
description: Brug standardkonfigurationspakken til at tilføje debitordata i Excel og importere dataene tilbage til Business Central.
author: brentholtorf
ms.topic: conceptual
ms.devlang: al
ms.search.keywords: 'migration, Excel'
ms.date: 05/10/2022
ms.author: bholtorf
ms.service: dynamics-365-business-central
---
# <a name="import-business-data-from-other-finance-systems"></a>Importere virksomhedsdata fra andre økonomisystemer

Når du tilmelder dig [!INCLUDE[prod_short](includes/prod_short.md)], kan du oprette en tom virksomhed, så du kan overføre dine egne data og teste den nye virksomhed i [!INCLUDE[prod_short](includes/prod_short.md)]. Afhængigt af hvilket økonomisystem, som virksomheden benytter i dag, kan du overføre oplysninger om debitorer, kreditorer, lagerbeholdning og bankkonti.  

Fra rollecenteret kan du starte en assisterede opsætningsvejledning for at overføre forretningsdataene fra en Excel-fil eller fra andre formater. Hvilken type filer, du kan overføre, afhænger af de udvidelser, der findes. F.eks. kan du overføre data fra QuickBooks, da [!INCLUDE[prod_short](includes/prod_short.md)] indeholder en udvidelse, der håndterer konverteringen fra QuickBooks. Hvis du vil overføre data fra andre økonomisystemer, skal du enten kontrollere, om en udvidelse er tilgængelig for den pågældende løsning, eller importere fra Excel.  

[!INCLUDE[prod_short](includes/prod_short.md)] indeholder skabeloner for konti, debitorer, kreditorer og lagervarer, som du kan vælge at anvende, når du importerer data. Du kan bruge en dedikeret funktion på siden **Lageropsætning** til at indlæse varebilleder. Du kan finde flere oplysninger i [Importér flere varebilleder](inventory-how-import-item-pictures.md).

> [!TIP]  
> Vi anbefaler at du bruger dataoverførselsguiderne til at importere data fra Dynamics GP, Dynamics NAV eller QuickBooks. Du kan finde flere oplysninger i [Overførsel af lokale data til Business Central Online](/dynamics365/business-central/dev-itpro/administration/migrate-data) i administrationsindholdet eller [Overførsel af QuickBooks-data](ui-extensions-quickbooks-data-migration.md).

## <a name="work-with-data-in-excel"></a>Arbejde med data i Excel

Du kan føje Excel til at behandle eksisterende budgetposter i [!INCLUDE [prod_short](includes/prod_short.md)]. Du kan finde flere oplysninger i [Vise og redigere i Excel fra Business Central](across-work-with-excel.md).  

## <a name="import-data-from-configuration-packages"></a>Importere data fra konfigurationspakker

Du kan konfigurere løsningsspecifikke konfigurationspakker for større implementeringsopgaver. Du kan finde flere oplysninger i [Oprette konfigurationspakker for virksomheder](/dynamics365/business-central/dev-itpro/administration/set-up-standard-company-configuration-packages) (kun på engelsk) i indholdet til administratorer.  

> [!NOTE]  
> Arbejde med konfigurationspakker er avanceret funktionalitet, og det anbefales, at du kontakter forhandleren. Du kan finde flere oplysninger i [Konfigurere Virksomhedskonfigurationspakker](/dynamics365/business-central/dev-itpro/administration/set-up-standard-company-configuration-packages) (kun på engelsk).

Du kan importere masterdata og nogle transaktionsdata fra andre økonomisystemer baseret på standardkonfigurationspakken i [!INCLUDE[prod_short](includes/prod_short.md)]. På siden **Konfigurationspakker** kan du arbejde med pakken for at importere og validere data, før du anvender pakken. Du kan f.eks. eksportere konfigurationspakken til Excel og konfigurere dataene der. Derefter kan du importere dataene fra Excel igen. Pakken indeholder 27 tabeller, herunder masterdata som debitorer, kreditorer, varer og konti, andre grundlæggende opsætningstabeller f.eks. leveringsmetoder og transaktionstabeller, som f.eks. salgshoved og linjer.  

Når du eksporterer standardkonfigurationspakken til Excel, indeholder den projektmappe, der oprettes, et regneark for hver tabel i pakken. For at forenkle dine opgaver, kan du drage fordel af de XML-manipulationsværktøjer, der er indbygget i Excel. Du kan også bruge indbyggede funktioner i Excel til at hjælpe med dataformatering og til at indsætte data i den korrekte celle. Tilføj f.eks. et tomt regneark, og kopier de oprindelige data til det. Opret derefter en Excel-formel for at afbilde dataene i overflytningsregnearket mellem felterne i det eksporterede regneark og debitorens ældre data. Når du har tilknyttet alle data, skal du kopiere dataområdet ind i regnearket med tabellen.  

> [!IMPORTANT]  
> Undlad at ændre kolonnerne i regnearkene. Hvis de flyttes, ændres eller slettes, kan regnearket ikke importeres i [!INCLUDE[prod_short](includes/prod_short.md)].

> [!NOTE]
> Felter af typen Blob kan ikke eksporteres/importeres ved hjælp af Excel.

### <a name="tables-in-the-default-configuration-package"></a>Tabeller i standardkonfigurationspakken

Standardkonfigurationspakken understøtter følgende tabeller:

- Betalingsbetingelser
- Debitorprisgruppe
- Leveringsform
- Sælger/indkøber
- Sted
- Finanskonto
- Kunde
- Kreditor
- Vare
- Salgshoved
- Salgslinje
- Købshoved
- Købslinje
- Finans- kladdelinje
- Varekladdelinje
- Debitorbogføringsgruppe
- Kreditorbogføringsgruppe
- Varebogføringsgruppe
- Enhed
- Finans- Virksomhedsbogf.gruppe
- Finans- Produktbogf.gruppe
- Bogføringsopsætning
- Distrikt
- Varekategori
- Salgspris
- Købspris

## <a name="see-also"></a>Se også

[Overførsel af data i det lokale miljø til Business Central Online (kun på engelsk)](/dynamics365/business-central/dev-itpro/administration/migrate-data)  
[Konfigurere virksomhedskonfigurationspakker](/dynamics365/business-central/dev-itpro/administration/set-up-standard-company-configuration-packages)  
[Overflytning af QuickBooks Data](ui-extensions-quickbooks-data-migration.md)  
[Importere flere varebilleder](inventory-how-import-item-pictures.md)

## [!INCLUDE[prod_short](includes/free_trial_md.md)]  


[!INCLUDE[footer-include](includes/footer-banner.md)]
