---
title: Importere dine eksisterende virksomhedsdata i Financials | Microsoft Docs
description: "Du kan overføre data for debitorer, kreditorer og lageret, f.eks. fra Excel, QuickBooks eller Dynamics GP, til Financials."
author: edupont04
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: migrate, initialize, implement
ms.date: 07/05/2017
ms.author: edupont
ms.translationtype: HT
ms.sourcegitcommit: 2a38dc36cb9ff609c5582acd489841b20013d4bc
ms.openlocfilehash: dd6eb5a6b19bf4c8fd92674a48e8cd29ce912eee
ms.contentlocale: da-dk
ms.lasthandoff: 09/22/2017

---
# <a name="importing-business-data-from-other-finance-systems"></a>Importere virksomhedsdata fra andre økonomisystemer
Når du tilmelder dig [!INCLUDE[d365fin](includes/d365fin_md.md)], kan du oprette en tom virksomhed, så du kan overføre dine egne data og teste den nye virksomhed i [!INCLUDE[d365fin](includes/d365fin_md.md)]. Afhængigt af hvilket økonomisystem, som virksomheden benytter i dag, kan du overføre oplysninger om debitorer, kreditorer, lagerbeholdning og bankkonti.  

Fra Start kan du starte en assisterede opsætningsvejledning for at overføre forretningsdataene fra en Excel-fil eller fra andre formater. Hvilken type filer, du kan overføre, afhænger af de udvidelser, der findes. F.eks. kan du overføre data fra QuickBooks, da [!INCLUDE[d365fin](includes/d365fin_md.md)] indeholder en udvidelse, der håndterer konverteringen fra QuickBooks. Hvis du vil overføre data fra andre økonomisystemer, skal du enten kontrollere, om en udvidelse er tilgængelig for den pågældende løsning, eller importere fra Excel.  

[!INCLUDE[d365fin](includes/d365fin_md.md)] indeholder skabeloner for konti, debitorer, kreditorer og lagervarer, som du kan vælge at anvende, når du importerer data.  

## <a name="importing-data-from-quickbooks-or-dynamics-gp"></a>Importere data fra QuickBooks eller Dynamics GP
Hvis virksomheden bruger QuickBooks eller Dynamics GP i dag, kan du eksportere de relevante oplysninger til en fil. Du kan derefter åbne den assisterede opsætningsvejledning for at overføre data.
F.eks. hvis filen omfatter debitorer og kreditorer, kan du kun overføre debitordata. Du kan derefter overføre resterende oplysninger senere.  

Den assisterede opsætning omfatter en mulighed for at ændre standardkonfigurationen af overførslen, men det anbefales, at du kun bruger denne avancerede opsætning, hvis du har erfaring med databasetabeller. I de fleste virksomheder overfører standardtilknytningen fra QuickBooks eller Dynamics GP til [!INCLUDE[d365fin](includes/d365fin_md.md)] de ønskede oplysninger.  

Du kan finde flere oplysninger i [Overførsel af QuickBooks-data](ui-extensions-quickbooks-data-migration.md) eller [Overførsel af data med Dynamics GP](ui-extensions-dynamicsgp-data-migration.md).

## <a name="importing-data-from-configuration-packages"></a>Importere data fra konfigurationspakker
[!INCLUDE[d365fin](includes/d365fin_md.md)] indeholder en konfigurationspakke, som du kan eksportere til Excel og konfigurere dataene der. Derefter kan du importere dataene fra Excel igen. Pakken indeholder 27 tabeller, herunder masterdata som debitorer, kreditorer, varer og konti, andre grundlæggende opsætningstabeller f.eks. leveringsmetoder og transaktionstabeller, som f.eks. salgshoved og linjer.  

> [!NOTE]  
>   Arbejde med konfigurationspakker er avanceret funktionalitet, og det anbefales, at du kontakter systemadministratoren. Du kan finde flere oplysninger under [Importere data fra ældre regnskabsprogrammer ved hjælp af en konfigurationspakke](across-import-data-configuration-packages.md).  

## <a name="see-also"></a>Se også
[Finans](finance.md)  
[Importere data fra ældre regnskabsprogrammer ved hjælp af en konfigurationspakke](across-import-data-configuration-packages.md)  
[Overflytning af QuickBooks Data](ui-extensions-quickbooks-data-migration.md)  
[Overførsel af data med Dynamics GP](ui-extensions-dynamicsgp-data-migration.md)  
[Tilpasse [!INCLUDE[d365fin](includes/d365fin_md.md)] ved hjælp af udvidelser](ui-extensions.md)   
[Opsætning af [!INCLUDE[d365fin](includes/d365fin_md.md)]](setup.md)

## [!INCLUDE[d365fin](includes/free_trial_md.md)]

