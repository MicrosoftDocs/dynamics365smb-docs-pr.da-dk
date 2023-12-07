---
title: Introduktion til Microsoft Fabric og Business Central
description: 'Få over brug af Microsoft Fabric for at få indsigt, business intelligence og KPI''er fra Business Central-data.'
author: kennienp
ms.topic: overview
ms.search.keywords: 'account schedule, analysis, reporting, financial report, business intelligence, KPI'
ms.search.form: '6316, 6317'
ms.reviewer: jswymer
ms.date: 10/10/2023
ms.author: kepontop
ms.custom: bap-template
---
# <a name="introduction-to-microsoft-fabric-and-business-central"></a>Introduktion til Microsoft Fabric og Business Central

[!INCLUDE[microsoft_fabric](includes/microsoft_fabric.md)] er en komplet analyseløsning med komplette funktioner, herunder dataflytning, datasøer, datateknik, dataintegration, datavidenskab, realtidsanalyse og business intelligence – alt sammen understøttet af en delt platform, der leverer robust datasikkerhed, styring og overholdelse. Din organisation behøver ikke længere at sammensætte individuelle analysetjenester fra flere leverandører. Brug i stedet en strømlinet løsning, der er nem at tilslutte, onboarde og betjene.

> [!NOTE]
> [!INCLUDE[microsoft_fabric](includes/microsoft_fabric.md)] er aktuelt i forhåndsversion. Du kan finde flere oplysninger om Microsoft Fabric-frigivelsesplan i [aka.ms/FabricRoadmap](https://aka.ms/FabricRoadmap)
> 
> Den regelmæssige offentliggørelse af denne køreplan vil hjælpe dig med at holde dig informeret om, hvordan [!INCLUDE[microsoft_fabric](includes/microsoft_fabric.md)] vil imødekomme dine behov.

## <a name="where-does--fit-into-includeprod_short-analytics"></a>Hvor [!INCLUDE[microsoft_fabric](includes/microsoft_fabric.md)] passer ind i [!INCLUDE[prod_short](includes/prod_short.md)] analyser

[!INCLUDE[prod_short](includes/prod_short.md)] leveres med mange standardrapporter og dataanalysefunktioner såsom finansiel rapportering, åben i Excel og analysetilstand på lister og forespørgsler. Derudover er det nemt at definere Power BI rapporter, der læser data fra standard- og brugerdefinerede API'er, definerer Power BI scorecards for målepunkter og integrerer alle disse direkte i [!INCLUDE[prod_short](includes/prod_short.md)]-klienten. Men for kunder med mere avanceret datavidenskab eller business intelligence-scenarier, der kræver mere omfattende datateknik eller dataintegration, kan [!INCLUDE[microsoft_fabric](includes/microsoft_fabric.md)] være en god mulighed. 

## <a name="onelake"></a>OneLake

En vigtig del af [!INCLUDE[microsoft_fabric](includes/microsoft_fabric.md)] tilbuddet er OneLake. OneLake er en enkelt, samlet, logisk data Lake for hele organisationen. Du kan tænke på OneLake som OneDrive til data. Det giver dig Data Lake som en tjeneste uden at skulle bygge den selv. OneLake leveres automatisk med hver [!INCLUDE[microsoft_fabric](includes/microsoft_fabric.md)] lejer uden infrastruktur at administrere. Alle data, der lander i OneLake, deltager automatisk i standarddatastyring såsom dataafstamning, databeskyttelse, certificering og katalogintegration. Det nedbryder datasiloer ved at gøre det muligt for forskellige dele af organisationen at arbejde uafhængigt, mens de stadig bidrager til den samme Data Lake.

[!INCLUDE[microsoft_fabric](includes/microsoft_fabric.md)] elementer gemmer dine data i OneLake i et åbent filformat. For strukturerede tabeldata er dette format *delta parquet*. Delta parquet giver alle analyseprogrammer i [!INCLUDE[microsoft_fabric](includes/microsoft_fabric.md)] adgang til data fra andre analyseprogrammer. På denne måde giver det fleksibilitet for databehandlere til at bruge de værktøjer, du vælger.

> [!NOTE]
> Vi forventer, at data med en af vores fremtidige udgivelser [!INCLUDE[prod_short](includes/prod_short.md)] også vil blive gjort tilgængelige i OneLake for de kunder, der bruger både [!INCLUDE[microsoft_fabric](includes/microsoft_fabric.md)] og [!INCLUDE[prod_short](includes/prod_short.md)] og har unikke krav på de områder, der [!INCLUDE[microsoft_fabric](includes/microsoft_fabric.md)] understøtter. Tidslinjen afhænger af tidslinjen for den generelle tilgængelighed af [!INCLUDE[microsoft_fabric](includes/microsoft_fabric.md)] og de tilhørende komponenter, der kræves for at muliggøre denne oplevelse. Vi vil opdatere denne artikel med en mere præcis tidslinje, når vi ved mere.

## <a name="see-also"></a>Se også
[Bruge Power BI med Business Central](admin-powerbi.md)   

[!INCLUDE[footer-include](includes/footer-banner.md)]
