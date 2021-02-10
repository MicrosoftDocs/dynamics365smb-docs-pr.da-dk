---
author: edupont04
ms.service: dynamics365-accountant
ms.topic: include
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: dcfc54d36b212b296747d28945324ac46c38cada
ms.sourcegitcommit: 2e7307fbe1eb3b34d0ad9356226a19409054a402
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 12/17/2020
ms.locfileid: "4753613"
---
Brugere supporterer nogle gange mere end én virksomhed og er nødt til at skifte fra arbejde med én virksomhed til en anden i [!INCLUDE [prod_short](prod_short.md)]. F.eks. kan en virksomhed have salgskontorer i byer og flere lande, så den har oprettet en separat afdeling for hvert kontor. De kontorer, der befinder sig i samme land, oprettes som separate virksomheder i et delt miljø. Andre kontorer oprettes som virksomheder i separate miljøer, fordi de er geografisk baseret i andre lande.<br><br>  

Hvad er et miljø? Virksomheder i [!INCLUDE[prod_short](prod_short.md)] findes i det, der kaldes *miljøer*. Der findes to typer miljøer, **Produktion** og **Sandkasse**. Kort sagt indeholder produktionsmiljøer live forretningsdata, og sandkassemiljøer bruges som et sikkert sted til at afprøve ting som nye forretningsprocesser eller -funktioner. Du kan finde flere oplysninger i [Miljøtyper](/dynamics365/business-central/dev-itpro/administration/tenant-admin-center-environments#types-of-environments). Hvis du har adgang til en virksomhed, har du adgang til det miljø, hvor den er installeret. Hvis du har adgang til mere end én virksomhed, og disse virksomheder er i forskellige miljøer, skal du angive det miljø, du vil arbejde i, når du logger på [!INCLUDE[prod_short](prod_short.md)]. Miljøer er specifikke for et bestemt land, så hvis din organisation arbejder i flere lande, skal du bruge separate miljøer for hvert land.<br><br>  

Hvad er en virksomhed? En *virksomhed* skal opfattes som en beholder, der indeholder oplysninger om en juridisk enhed. Hvis du bruger eksemplet ovenfor, har firmaet et salgskontor i Seattle og et andet i New York, så det opretter en virksomhed i [!INCLUDE[prod_short](prod_short.md)] for hvert kontor, så det kan håndtere operationer for hvert kontor separat.  
