---
author: edupont04
ms.service: dynamics365-accountant
ms.topic: include
ms.date: 07/03/2020
ms.author: edupont
ms.openlocfilehash: d4d7e1ce5da2a59e4a682746035684e76dd55eef
ms.sourcegitcommit: ca5bf1d934997ef8c0bc9f8ab0e5568f0ed42fa4
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 07/06/2020
ms.locfileid: "3535481"
---
Brugere supporterer nogle gange mere end én virksomhed og er nødt til at skifte fra arbejde med én virksomhed til en anden i [!INCLUDE [prodshort](prodshort.md)]. F.eks. kan en virksomhed have salgskontorer i byer og flere lande, så den har oprettet en separat afdeling for hvert kontor. De kontorer, der befinder sig i samme land, oprettes som separate virksomheder i et delt miljø. Andre kontorer oprettes som virksomheder i separate miljøer, fordi de er geografisk baseret i andre lande.  

Hvad er et miljø? Virksomheder i [!INCLUDE[prodshort](prodshort.md)] findes i det, der kaldes *miljøer*. Der findes to typer miljøer, **Produktion** og **Sandkasse**. Kort sagt indeholder produktionsmiljøer live forretningsdata, og sandkassemiljøer bruges som et sikkert sted til at afprøve ting som nye forretningsprocesser eller -funktioner. Du kan finde flere oplysninger i [Miljøtyper](/dynamics365/business-central/dev-itpro/administration/tenant-admin-center-environments#types-of-environments). Hvis du har adgang til en virksomhed, har du adgang til det miljø, hvor den er installeret. Hvis du har adgang til mere end én virksomhed, og disse virksomheder er i forskellige miljøer, skal du angive det miljø, du vil arbejde i, når du logger på [!INCLUDE[prodshort](prodshort.md)]. Miljøer er specifikke for et bestemt land, så hvis din organisation arbejder i flere lande, skal du bruge separate miljøer for hvert land.  

Hvad er en virksomhed? En *virksomhed* skal opfattes som en beholder, der indeholder oplysninger om en juridisk enhed. Hvis du bruger eksemplet ovenfor, har firmaet et salgskontor i Seattle og et andet i New York, så det opretter en virksomhed i [!INCLUDE[prodshort](prodshort.md)] for hvert kontor, så det kan håndtere operationer for hvert kontor separat.  
