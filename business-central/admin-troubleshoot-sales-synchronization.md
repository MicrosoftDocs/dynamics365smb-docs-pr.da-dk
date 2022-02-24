---
title: Fejlfinding i forbindelse med synkroniseringsfejl | Microsoft Docs
description: I denne artikel gives vejledning til identifikation og løsning af synkroniseringsfejl.
services: project-madeira
documentationcenter: ''
author: bholtorf
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/01/2019
ms.author: bholtorf
ms.openlocfilehash: 489e66165c5441ea63043a30dee8af314ef5d815
ms.sourcegitcommit: 877af26e3e4522ee234fbba606615e105ef3e90a
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 01/28/2020
ms.locfileid: "2991804"
---
# <a name="troubleshooting-synchronization-errors"></a>Fejlfinding i forbindelse med synkroniseringsfejl
Der skal flyttes mange forskellige dele, når [!INCLUDE[d365fin](includes/d365fin_md.md)] skal integreres med [!INCLUDE[crm_md](includes/crm_md.md)], og nogle gange går tingene forkert. I dette emne beskrives nogle af de mest almindelige fejl, der opstår, og der angives oplysninger om, hvordan de kan løses.

Fejl opstår ofte, fordi en bruger har udført handlinger på sammenkædede poster, eller fordi, der er noget galt med den måde, integrationen er konfigureret på. Fejl, der vedrører sammenkædede poster, kan brugerne selv løse. Disse fejl skyldes handlinger som f.eks. sletning af en post i en, men ikke begge forretningsapps med efterfølgende synkronisering. Du kan finde flere oplysninger under [Se status på en synkronisering](admin-how-to-view-synchronization-status.md).

> [!VIDEO https://go.microsoft.com/fwlink/?linkid=2097304]

Fejl, der er relateret til, hvordan integrationen er konfigureret, kræver typisk handlinger udført af en administrator. Du kan få vist fejlene på siden **Integrationssynkroniseringsfejl**. Eksempler på typiske problemer omfatter:  
  
* De tilladelser og roller, der er tildelt til brugere, er ikke korrekte.  
* Administratorkontoen blev angivet som integrationsbrugeren.  
* Integrationsbrugerens adgangskode er indstillet til at kræve en ændring, når brugeren logger på.  
* Valutakurserne er ikke angivet i den ene eller den anden app.  
  
Du skal rette fejlene manuelt, men du kan få visse former for hjælp på siden. Eksempler:  

* Felterne **Kilde** og **Destination** kan indeholde links til den post, hvor fejlen blev fundet. Klik på linket for at åbne posten og undersøge fejlen.  
* Handlingerne **Slet poster, der er ældre end syv dage** og **Slet alle poster** rydder op på listen. Du bruger typisk disse handlinger, når du har fundet årsagen til en fejl, der påvirker mange poster. Men gå forsigtigt frem. Disse handlinger kan muligvis slette fejl, der stadig er relevante.

Tidsstemplerne på poster kan somme tider forårsage konflikter. I tabellen "CRM-integrationsrecord" gemmes tidsstemplerne "Sidste synkr. ændret den" og "Sidst synkr. CRM-ændret den" for den sidste integration, der er udført i begge retninger for en post. Disse tidsstempler sammenlignes med tidsstempler i Business Central og salgsposter. I Business Central findes tidsstemplet i tabellen Integrationsrecord.

Du kan filtrere efter records, der skal synkroniseres, ved at sammenligne recordstempler i felterne "Synkr. rettet på filter"og "Synch. Int. Tbl." i "Integrationstabeltilknytning" Rettet på feltnr.”.

Konfliktfejlmeddelelsen "Kan ikke opdatere kunderecord, fordi den har en senere ændringsdato end kontorecorden eller "Kan ikke opdatere kontorrecorden, fordi den har en senere ændringsdato end kunderecorden" kan ske, hvis en record har et tidsstempel, der er større end integrationstabeltilknytning Synkr. rettet på filter, men ikke ligger før tidstemplet på Salgsintegrationsrecord. Det betyder, at kilderecorden er blevet synkroniseret manuelt og ikke af opgavekøposten. 

Konflikten opstår, fordi destinationsrecorden også blev ændret – poststemplet er nyere end salgsintegrationsrecordens tidsstempel. Destinationskontrollen sker kun i forbindelse med tovejstabeller. 

Disse records er nu flyttet til siden "Synkroniserede poster, der springes over", som du kan åbne fra siden Konfiguration af Microsoft Dynamics-forbindelse i Business central. Her kan du angive de ændringer, du vil beholde, og derefter synkronisere recordsene igen.

## <a name="see-also"></a>Se også
[Integration med [!INCLUDE[crm_md](includes/crm_md.md)]](admin-prepare-dynamics-365-for-sales-for-integration.md)  
[Konfigurere brugerkonti til integration med [!INCLUDE[crm_md](includes/crm_md.md)]](admin-setting-up-integration-with-dynamics-sales.md)  
[Oprette en forbindelse til [!INCLUDE[crm_md](includes/crm_md.md)]](admin-how-to-set-up-a-dynamics-crm-connection.md)  
[Sammenkæde og synkronisere poster manuelt](admin-how-to-couple-and-synchronize-records-manually.md)  
[Se status på en synkronisering](admin-how-to-view-synchronization-status.md)  
