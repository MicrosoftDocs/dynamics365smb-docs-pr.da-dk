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
ms.date: 06/11/2019
ms.author: bholtorf
ms.openlocfilehash: bb6d0837f91240eb31abc7c02895cf2da420bf7d
ms.sourcegitcommit: 8fe694b7bbe7fc0456ed5a9e42291218d2251b05
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 07/04/2019
ms.locfileid: "1726786"
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

## <a name="see-also"></a>Se også
[Integration med [!INCLUDE[crm_md](includes/crm_md.md)]](admin-prepare-dynamics-365-for-sales-for-integration.md)  
[Konfigurere brugerkonti til integration med [!INCLUDE[crm_md](includes/crm_md.md)]](admin-setting-up-integration-with-dynamics-sales.md)  
[Oprette en forbindelse til [!INCLUDE[crm_md](includes/crm_md.md)]](admin-how-to-set-up-a-dynamics-crm-connection.md)  
[Sammenkæde og synkronisere poster manuelt](admin-how-to-couple-and-synchronize-records-manually.md)  
[Se status på en synkronisering](admin-how-to-view-synchronization-status.md)  