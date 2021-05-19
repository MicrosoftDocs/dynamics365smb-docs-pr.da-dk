---
title: Fejlfinding i forbindelse med synkroniseringsfejl | Microsoft Docs
description: I denne artikel gives vejledning til identifikation og løsning af synkroniseringsfejl.
services: project-madeira
documentationcenter: ''
author: bholtorf
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/01/2021
ms.author: bholtorf
ms.openlocfilehash: 91c64ecbd32ec8fe6a528c87d2e102e1a1322816
ms.sourcegitcommit: 921f0c4043dcda2fb8fc35df1b64310bf32270d7
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 05/11/2021
ms.locfileid: "6017220"
---
# <a name="troubleshooting-synchronization-errors"></a>Fejlfinding i forbindelse med synkroniseringsfejl
[!INCLUDE[prod_short](includes/cc_data_platform_banner.md)]

Der skal flyttes mange forskellige dele, når [!INCLUDE[prod_short](includes/prod_short.md)] skal integreres med [!INCLUDE[prod_short](includes/cds_long_md.md)], og nogle gange går tingene forkert. I dette emne beskrives nogle af de mest almindelige fejl, der opstår, og der angives oplysninger om, hvordan de kan løses.

Fejl opstår ofte, fordi en bruger har udført handlinger på sammenkædede poster, eller fordi, der er noget galt med den måde, integrationen er konfigureret på. Fejl, der vedrører sammenkædede poster, kan brugerne selv løse. Disse fejl skyldes handlinger som f.eks. sletning af data i en, men ikke begge forretningsapps med efterfølgende synkronisering. Du kan finde flere oplysninger i [Se status på en synkronisering](admin-how-to-view-synchronization-status.md).

## <a name="example"></a>Eksempel
I denne video vises et eksempel på, hvordan du retter fejl, der er opstået under synkronisering med [!INCLUDE[prod_short](includes/cds_long_md.md)]. Denne proces vil være den samme for alle integrationer. 

> [!VIDEO https://go.microsoft.com/fwlink/?linkid=2097304]

Fejl, der er relateret til, hvordan integrationen er konfigureret, kræver typisk handlinger udført af en administrator. Du kan få vist fejlene på siden **Integrationssynkroniseringsfejl**. Eksempler på typiske problemer omfatter:  
  
* De tilladelser og roller, der er tildelt til brugere, er ikke korrekte.  
* Administratorkontoen blev angivet som integrationsbrugeren.  
* Integrationsbrugerens adgangskode er indstillet til at kræve en ændring, når brugeren logger på.  
* Valutakurserne er ikke angivet i den ene eller den anden app.  
  
Du skal rette fejlene manuelt, men du kan få visse former for hjælp på siden. Eksempler:  

* Felterne **Kilde** og **Destination** kan indeholde links til den række, hvor fejlen blev fundet. Klik på linket for at undersøge fejlen.  
* Handlingerne **Slet poster, der er ældre end syv dage** og **Slet alle poster** rydder op på listen. Du bruger typisk disse handlinger, når du har fundet årsagen til en fejl, der påvirker mange poster. Men gå forsigtigt frem. Disse handlinger kan muligvis slette fejl, der stadig er relevante.

Tidsstemplerne på poster kan somme tider forårsage konflikter. I tabellen "CDS-integrationsrecord" gemmes tidsstemplerne "Sidste synkr. ændret den" og "Sidst synkr. CDS-ændret den" for den sidste integration, der er udført i begge retninger for en række. Disse tidsstempler sammenlignes med tidsstempler i Business Central og salgsposter. I Business Central findes tidsstemplet i tabellen Integrationsrecord.

Du kan filtrere efter poster, der skal synkroniseres, ved at sammenligne rækkestempler i felterne "Synkr. rettet på filter"og "Synch. Int. Tbl." i "Integrationstabeltilknytning". Rettet på feltnr.".

Konfliktfejlmeddelelsen "Kan ikke opdatere kunderecord, fordi den har en senere ændringsdato end kontorecorden eller "Kan ikke opdatere kontorrecorden, fordi den har en senere ændringsdato end kunderecorden" kan ske, hvis en række har et tidsstempel, der er større end integrationstabeltilknytning Synkr. rettet på filter, men ikke ligger før tidstemplet på Salgsintegrationsrecord. Det betyder, at kilderækken er blevet synkroniseret manuelt og ikke af opgavekøposten. 

Konflikten opstår, fordi destinationsrækken også blev ændret – rækketidsstemplet er nyere end salgsintegrationspostens tidsstempel. Destinationskontrollen sker kun i forbindelse med tovejstabeller. 

Disse records er nu flyttet til siden "Synkroniserede poster, der springes over", som du kan åbne fra siden Konfiguration af Microsoft Dynamics-forbindelse i Business central. Her kan du angive de ændringer, du vil beholde, og derefter synkronisere recordsene igen.

## <a name="remove-couplings-between-records"></a>Fjerne koblinger mellem poster
Når noget går galt i integrationen, og du har brug for at koble posterne fra, så de ikke længere synkroniseres, kan du gøre det for en eller flere poster ad gangen. Du kan fjerne frakoble en eller flere poster fra listesider eller siden **Koblede datasynkroniseringsfejl** ved at vælge en eller flere linjer og vælge **Slet kobling**. Du kan også fjerne alle koblinger for en eller flere tabeltilknytninger på siden **Tilknytninger til integrationstabel**. 

Hvis en enhed med en envejs kobling slettes i [!INCLUDE[prod_short](includes/prod_short.md)], skal du slette den brudte kobling manuelt. Hvis du vil gøre dette, skal du vælge **Søg efter slettet** handling på siden **Fejl i forbindelse med sammenkoblet datasynkronisering** og derefter slette koblingerne.

## <a name="see-also"></a>Se også
[Integration med Microsoft Dataverse](admin-prepare-dynamics-365-for-sales-for-integration.md)  
[Konfigurere brugerkonti til integration med Microsoft Dataverse](admin-setting-up-integration-with-dynamics-sales.md)  
[Oprette en forbindelse til Microsoft Dataverse](admin-how-to-set-up-a-dynamics-crm-connection.md)  
[Sammenkæde og synkronisere poster manuelt](admin-how-to-couple-and-synchronize-records-manually.md)  
[Se status på en synkronisering](admin-how-to-view-synchronization-status.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]