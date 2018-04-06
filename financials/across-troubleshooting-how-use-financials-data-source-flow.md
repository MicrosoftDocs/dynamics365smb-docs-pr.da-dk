---
title: Fejlfinding af integration med Microsoft Flow | Microsoft Docs
description: "Du kan bruge fejlfinding til at gøre dine Financials-data tilgængelige som datakilde og angive en OData URL-adresse til dine webtjenester for at oprette et automatiseret workflow."
documentationcenter: 
author: SusanneWindfeldPedersen
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: workflow, Odata, Power App, SOAP
ms.date: 01/25/2018
ms.author: solsen
ms.translationtype: HT
ms.sourcegitcommit: bec0619be0a65e3625759e13d2866ac615d7513c
ms.openlocfilehash: 4c28b5b6dce6152399cf599877180e806227b5ef
ms.contentlocale: da-dk
ms.lasthandoff: 03/22/2018

---
# <a name="troubleshooting-integration-with-microsoft-flow---request-url-too-long"></a>Fejlfinding af integration med Microsoft Flow - URL-adresse til anmodning er for lang
Du kan bruge dine [!INCLUDE[d365fin](includes/d365fin_md.md)]-data som en del af en arbejdsproces i Microsoft Flow.  

> [!NOTE]  
>   Du skal have en gyldig konto til [!INCLUDE[d365fin](includes/d365fin_md.md)] og til Flow.  

Hvis du opretter et Microsoft Flow ved hjælp af [!INCLUDE[d365fin](includes/d365fin_md.md)]-konnektoren, får du vist en fejlmeddelelse om, at den anmodede URL-adresse er for lang, når du har oprettet flowet, f.eks. som følgende: **RequestUriTooLong**.

## <a name="cause"></a>Årsag
For at et flow kan udløses, søges der efter ændringer i dine data. Når det afgøres, om dataene er blevet ændret, sammenligner konnektorerne de cachede data med de nye data, der anmodes om fra kilden.  

Hvis dataanmodningen opretter en URL-adresse, der er for lang, mislykkes anmodningen. Almindelige årsager kan omfatte:
- Som regel enhver kildetabel med mere end 250 rækker
- Kildetabeller, der indeholder flere tusinde poster

## <a name="workaround"></a>Løsning
Følg disse trin for at løse problemet.
1. Vælg at redigere det flow, der er problemer med.
2. Udvid **Vis avancerede indstillinger** på udløseren til flowet.
3. Angiv antallet af poster, der skal springes over, i feltet **Antal, der skal springes over**.  
Hvis den tabel, der bruges som datakilde har 4.000 poster, skal du f.eks. angive 4.000 som det antal poster, der skal springes over.
4. Opdater dit flow.

> [!NOTE]  
> Konnektoren er i øjeblikket i Beta. Opdateringer til hvordan dataændringer beregnes i en senere version.


## <a name="see-also"></a>Se også
[Bruge [!INCLUDE[d365fin](includes/d365fin_md.md)] i et automatisk workflow](across-how-use-financials-data-source-flow.md)  
[Velkommen til [!INCLUDE[d365fin_long](includes/d365fin_long_md.md)]](index.md)  
[Importere virksomhedsdata fra andre økonomisystemer](upload-data.md)  
[Administrere brugere og deres rettigheder](ui-how-users-permissions.md)    
[Opsætning af [!INCLUDE[d365fin](includes/d365fin_md.md)]](setup.md)  
[Finans](finance.md)  

