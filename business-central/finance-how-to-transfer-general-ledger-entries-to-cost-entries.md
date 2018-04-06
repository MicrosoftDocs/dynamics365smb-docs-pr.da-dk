---
title: "Sådan overføres finansposter til omkostningsposter | Microsoft Docs"
description: "Du kan overføre finansposter til omkostningsposter."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 07/01/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: d7fb34e1c9428a64c71ff47be8bcff174649c00d
ms.openlocfilehash: cd52387ec1396164f6da1b87a2a97227901df592
ms.contentlocale: da-dk
ms.lasthandoff: 03/22/2018

---
# <a name="transfer-general-ledger-entries-to-cost-entries"></a>Overføre finansposter til omkostningsposter
Du kan overføre finansposter til omkostningsposter.  

Inden du kører processen til overførsel af finansposter til omkostningsposter, skal du forberede overførslen for at undgå manuel korrektionsbogføring.  

## <a name="to-prepare-the-transfer"></a>Sådan forberedes overførslen  

1.  Vælg ikonet ![Søg efter side eller rapport](media/ui-search/search_small.png "Ikonet Søg efter side eller rapport"), angiv **Konfiguration af omkostningsregnskab**, og vælg derefter det relaterede link.  
2.  I vinduet **Konfiguration af omkostningsregnskab** skal du kontrollere, at feltet **Startdato for finansoverførsel** er angivet til den korrekte værdi.  
3.  Vælg ikonet ![Søg efter side eller rapport](media/ui-search/search_small.png "Ikonet Søg efter side eller rapport"), angiv **Diagram over omkostningstyper**, og vælg derefter det relaterede link.  
4.  I vinduet **Omkostningstypekort** skal du kontrollere, at feltet **Finanskontointerval** er sammenkædet korrekt for hver pristype for at tage poster fra regnskabet.  
5.  Vælg ikonet ![Søg efter side eller rapport](media/ui-search/search_small.png "Ikonet Søg efter side eller rapport"), angiv **Kontoplan**, og vælg derefter det relaterede link.  
6.  For hver relevant finanskonto skal du i vinduet **Finanskontokort** kontrollere, at feltet **Omkostningstypenr.** er korrekt knyttet til en omkostningstype. Du kan finde flere oplysninger i [Definition af forholdet mellem omkostningstyper og finanskonti](finance-defining-the-relationship-between-cost-types-and-general-ledger-accounts.md).  
7.  Kontroller, at alle relevante finansposter har dimensionsværdier, der svarer til et omkostningssted og et omkostningsobjekt.  

## <a name="to-transfer-general-ledger-entries-to-cost-entries"></a>Sådan overføres finansposter til omkostningsposter  
1.  Vælg ikonet ![Søg efter side eller rapport](media/ui-search/search_small.png "Ikonet Søg efter side eller rapport"), angiv **Overfør finansposter til CA**, og vælg derefter det relaterede link.  
2.  Vælg knappen **Ja** for at starte overførslen. Processen overfører alle finansposter, der ikke allerede er overført.  

    Under overførslen opretter processen forbindelser i posterne i tabellen **Omkostningspost** og tabellen **Omkostningsregister**. Dette gør det muligt at spore kilden til omkostningsposter.  

## <a name="see-also"></a>Se også  
 [Kriterier for overførsel af finansposter til omkostningsposter.](finance-criteria-for-transferring-general-ledger-entries-to-cost-entries.md)   
 [Automatisk overførsel og kombinerede poster](finance-automatic-transfer-combined-entries.md)   
 [Resultater af overførslen](finance-results-of-the-transfer.md)   
 [Overførsel og bogføring af omkostningsposter](finance-transfer-and-post-cost-entries.md)   
 [Definition af forholdet mellem omkostningstyper og finanskonti.](finance-defining-the-relationship-between-cost-types-and-general-ledger-accounts.md)   

