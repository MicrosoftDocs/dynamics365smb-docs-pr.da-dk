---
title: Definere forholdet mellem omkostningstyper og finanskonti | Microsoft Docs
description: "Få at vide, hvordan du definerer forholdet mellem omkostningstypen og finanskontoen."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: cost types, general ledger
ms.date: 07/01/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: d7fb34e1c9428a64c71ff47be8bcff174649c00d
ms.openlocfilehash: 7709edb214804f52ee9b495c43b5302e2a23bd6b
ms.contentlocale: da-dk
ms.lasthandoff: 03/22/2018

---
# <a name="defining-the-relationship-between-cost-types-and-general-ledger-accounts"></a>Definition af forholdet mellem omkostningstyper og finanskonti.
Forholdet mellem pristype og finanskontoen oprettes i pristypen og finanskontoen.  

* Feltet **Finanskontointerval** i tabellen **Omkostningstype** fastlægger, hvilke finanskonti der hører til en pristype.  
* Feltet **Omkostningstypenr.** i kontoplanen fastlægger, hvilken pristype en finanskonto tilhører.  

Disse to felter udfyldes automatisk, når du bruger funktionen **Få omkostningstyper fra kontoplanen**.  

## <a name="relationship-between-general-ledger-accounts-and-cost-types"></a>Forholdet mellem finanskonti og pristyper  
Der er et n:1 forhold mellem finanskonti og pristyper. Flere finanskonti kan tilhøre én pristype, men hver finanskonto tilhører kun én pristype. Følgende tabel beskriver detaljerne om relationen.  

|Relationer|**Finanskontointerval**|**Omkostningstypenr.**|  
|------------------|------------------------------------------------|-------------------------------------------|  
|En finanskonto for hver pristype|Én finanskonto|En pristype|  
|Flere finanskonti for en pristype|Finanskontointerval, f.eks. 7110..7193, for finanskonto|For hver finanskonto i området er det kun én pristype|  
|Pristyper uden tilsvarende finanskonti|<Empty>||  
|Finanskonti, hvis poster ikke bliver overført||<Empty>|  

## <a name="cost-types-without-a-relationship-to-the-general-ledger"></a>Pristyper uden relation til finanskontoen  
En pristype kan ikke have en relation til finanskonti, hvis en af følgende betingelser er opfyldt:  

* Konti til operationelt regnskab, f.eks, Beregn Renter og afskrivning, henter kun omkostninger fra operationelt regnskab.  
* Hjælpeomkostningstyper, f.eks. 9901, 9902 og 9903 i [!INCLUDE[d365fin](includes/d365fin_md.md)]-databasen, bruges som kredit- og debetkonti for tildelinger.  
* Hjælpekontoen, 9920 i [!INCLUDE[d365fin](includes/d365fin_md.md)]-databasen, indeholder faktiske periodiseringer, der viser forskellen mellem omkostningerne og udgifterne fra finansregnskabet.  

## <a name="see-also"></a>Se også  
[Regnskab for omkostninger](finance-manage-cost-accounting.md)  
[Konfigurere omkostningsregnskab](finance-set-up-cost-accounting.md)   
[Om omkostningsregnskab](finance-about-cost-accounting.md)  
[Arbejde med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

