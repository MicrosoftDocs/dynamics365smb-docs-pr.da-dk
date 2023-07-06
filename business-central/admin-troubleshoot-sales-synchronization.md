---
title: Fejlfinding i forbindelse med synkroniseringsfejl
description: 'I denne artikel gives vejledning til identifikation, fejlfinding og løsning af synkroniseringsfejl.'
author: brentholtorf
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: null
ms.date: 06/14/2021
ms.author: bholtorf
---
# <a name="troubleshooting-synchronization-errors"></a><a name="troubleshooting-synchronization-errors"></a><a name="troubleshooting-synchronization-errors"></a>Fejlfinding i forbindelse med synkroniseringsfejl


Der skal flyttes mange forskellige dele, når [!INCLUDE[prod_short](includes/prod_short.md)] skal integreres med [!INCLUDE[prod_short](includes/cds_long_md.md)], og nogle gange går tingene forkert. I dette emne beskrives nogle af de mest almindelige fejl, der opstår, og der angives oplysninger om, hvordan de kan løses.

Fejl opstår ofte, fordi en bruger har udført handlinger på sammenkædede poster, eller fordi, der er noget galt med den måde, integrationen er konfigureret på. Fejl, der vedrører sammenkædede poster, kan brugerne selv løse. Disse fejl skyldes handlinger som f.eks. sletning af data i en, men ikke begge forretningsapps med efterfølgende synkronisering. Du kan finde flere oplysninger under [Se status på en synkronisering](admin-how-to-view-synchronization-status.md).

Fejl, der er relateret til, hvordan integrationen er konfigureret, kræver typisk handlinger udført af en administrator. Du kan få vist fejlene på siden **Integrationssynkroniseringsfejl**. 

Følgende tabel indeholder eksempler på typiske spørgsmål:  

|Udsted  |Løsning  |
|---------|---------|
|De tilladelser og roller, der er tildelt til integrationsbrugere, er ikke korrekte. | Denne fejl kommer fra [!INCLUDE[prod_short](includes/cds_long_md.md)], og den indeholder ofte følgende tekst "Principal User (id=\<user id>, type = 8) mangler \<privilegeName>-rettighed". Denne fejl opstår, fordi integrationsbrugeren mangler en rettighed, som gør det muligt at få adgang til et objekt. Denne fejl opstår typisk, hvis du synkroniserer brugerdefinerede objekter, eller hvis du har installeret en app i [!INCLUDE[prod_short](includes/cds_long_md.md)], som kræver tilladelse til at få adgang til andre [!INCLUDE[prod_short](includes/cds_long_md.md)]-enheder. Du kan løse denne fejl ved at tildele tilladelsen til integrationsbrugeren i [!INCLUDE[prod_short](includes/cds_long_md.md)].<br><br> Du kan finde brugernavnet integration på siden **Konfiguration af Dataverse-forbindelse**. Fejlmeddelelsen viser navnet på tilladelsen, som kan hjælpe dig med at identificere det objekt, du skal bruge tilladelse til. Hvis du vil tilføje de manglende rettigheder, skal du logge på [!INCLUDE[prod_short](includes/cds_long_md.md)] med en administratorkonto og redigere den sikkerhedsrolle, som integrationsbrugeren har fået tildelt. Du kan finde flere oplysninger i [Oprette eller redigere sikkerhedsregel til administration af adgang](/power-platform/admin/create-edit-security-role). |
|Du er ved at koble en post, der bruger en anden post, som ikke er kombineret. En kunde, hvis valuta ikke er koblet, eller en vare, som enheden ikke er koblet til. | Du skal først opkoble den afhængige post, f. eks. en valuta eller enhed, og derefter prøve koblingen igen. |

Følgende værktøjer findes på siden integrations synkroniseringsfejl, som du kan bruge til at løse problemerne manuelt.  

* Felterne **Kilde** og **Destination** kan indeholde links til den række, hvor fejlen blev fundet. Klik på linket for at undersøge fejlen.  
* Handlingerne **Slet poster, der er ældre end syv dage** og **Slet alle poster** rydder op på listen. Du bruger typisk disse handlinger, når du har fundet årsagen til en fejl, der påvirker mange poster. Men gå forsigtigt frem. Disse handlinger kan muligvis slette fejl, der stadig er relevante.
* Handlingen **Vis stak af fejlkald** viser oplysninger, der kan hjælpe med at identificere årsagen til fejlen. Hvis du ikke kan løse problemet selv, og du beslutter dig for at sende en supportanmodning, skal du medtage oplysningerne i supportanmodningen.

## <a name="see-also"></a><a name="see-also"></a><a name="see-also"></a>Se også
[Integration med Microsoft Dataverse](admin-prepare-dynamics-365-for-sales-for-integration.md)  
[Konfigurere brugerkonti til integration med Microsoft Dataverse](admin-setting-up-integration-with-dynamics-sales.md)  
[Oprette en forbindelse til Microsoft Dataverse](admin-how-to-set-up-a-dynamics-crm-connection.md)  
[Sammenkæde og synkronisere poster manuelt](admin-how-to-couple-and-synchronize-records-manually.md)  
[Se status på en synkronisering](admin-how-to-view-synchronization-status.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
