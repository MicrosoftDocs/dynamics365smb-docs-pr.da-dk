---
title: "Oversigt over opsætninger for serviceartikler og serviceartikelkomponenter | Microsoft Docs"
description: "Få mere at vide om de ting, du skal konfigurere, før du kan bruge serviceartikler, herunder standardværdier som f.eks. svartid, kontraktrabatprocent og serviceprisgruppe."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 07/01/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: bec0619be0a65e3625759e13d2866ac615d7513c
ms.openlocfilehash: 068d141ee8490cc34e8b2092b7dcfda36139660d
ms.contentlocale: da-dk
ms.lasthandoff: 01/30/2018

---
# <a name="set-up-service-items-and-service-item-components"></a>Konfigurere serviceartikler og serviceartikelkomponenter
Hvis du vil arbejde med serviceartikler, skal du oprette følgende

* Serviceartikelgrupper. 
* Valgfri

## <a name="to-set-up-service-item-groups"></a>Sådan defineres serviceartikelgrupper
Du kan definere grupper af varer, der er beslægtede med hensyn til reparation og vedligeholdelse. Du kan definere standardværdier for serviceartikler i en serviceartikelgruppe, som f.eks. svartid, kontraktrabatprocent og serviceprisgruppe. Du kan vælge, at varer i en serviceartikelgruppe automatisk registreres som serviceartikler, når de bliver solgt.  
  
Du tildeler serviceartikelgrupper til varer på **Vare**-kortet og til serviceartikler på **Serviceartikel**-kortet.  
  
1. Vælg ikonet ![Søg efter side eller rapport](media/ui-search/search_small.png "Ikonet Søg efter side eller rapport"), angiv **Serviceartikelgrupper**, og vælg derefter det relaterede link.  
2. Opret en ny serviceartikelgruppe.  
3. Udfyld felterne **Kode** og **Beskrivelse**.  
4. Angiv den standardkontraktrabatprocent, som skal gælde for serviceartiklerne i gruppen, i feltet **Kontraktrabatpct. (standard)**.  
5. Angiv den standardserviceprisgruppekode, som serviceartiklerne i gruppen skal have, i feltet **Serviceprisgrp.kode (standard)**.  
6. Angiv den standardsvartid i timer, der skal gælde for serviceartiklerne i gruppen, i feltet **Standardsvartid (timer)**.  
7. Hvis varerne i gruppen skal registreres som serviceartikler, når de bliver solgt, skal du markere feltet **Opret serviceartikel**.  

## <a name="to-set-up-service-item-components"></a>Sådan defineres serviceartikelkomponenter
En serviceartikel kan bestå af flere komponenter, som kan udskiftes med reservedele, når varen repareres. Komponenterne defineres på siden **Komponentoversigt – serviceart**. Hvis du desuden vil definere komponenter for serviceartikler, som er styklister, kan du kopiere styklistevarerne og oprette dem som serviceartikelkomponenter. 
  
1. Vælg ikonet ![Søg efter side eller rapport](media/ui-search/search_small.png "Ikonet Søg efter side eller rapport"), angiv **Serviceartikler**, og vælg derefter det relaterede link. 
2. Åbn den serviceartikel, som du vil definere komponenter for.  
3. Vælg handlingen **Komponenter**. Vinduet **Komponentoversigt - serviceart.** åbnes.  
4. Tilføj en ny komponent.  
5. I feltet **Type** skal du vælge **Serviceartikel**, hvis komponenten selv er en registreret serviceartikel. Ellers skal du vælge **Vare**.  
6. I feltet **Nummer** skal du vælge den artikel eller serviceartikel, som er en komponent i serviceartiklen.  

## <a name="to-set-up-service-item-components-from-a-bom"></a>Sådan defineres serviceartikelkomponenter fra styklister
1.  Vælg ikonet ![Søg efter side eller rapport](media/ui-search/search_small.png "Ikonet Søg efter side eller rapport"), angiv **Serviceartikler**, og vælg derefter det relaterede link.  
2. Åbn den serviceartikel, som du vil definere komponenter for ud fra en stykliste.  
3. Vælg handlingen **Komponenter**. Vinduet **Komponentoversigt - serviceart.** åbnes.  
4. Vælg handlingen **Kopier fra stykliste**.  
  
    Hvis varen, som serviceartiklen er knyttet til, er en stykliste, oprettes der automatisk komponenter for alle varerne i styklisten.  

## <a name="to-set-up-a-service-shelf"></a>Sådan defineres serviceplaceringer
Du kan oprette serviceplaceringer, der identificerer, hvor du gemmer dine serviceartikler. Du tildeler serviceplaceringer til serviceartikler på siden **Serviceordre** og siden **Serviceartikelkladde**.  
  
1. Vælg ikonet ![Søg efter side eller rapport](media/ui-search/search_small.png "Ikonet Søg efter side eller rapport"), angiv **Serviceplaceringer**, og vælg derefter det relaterede link.
2. Udfyld felterne efter behov.

## <a name="see-also"></a>Se også
[Definere koder for standardservices](service-how-setup-service-coding.md)   
[Konfigurere fejlfinding](service-how-setup-troubleshooting.md)
