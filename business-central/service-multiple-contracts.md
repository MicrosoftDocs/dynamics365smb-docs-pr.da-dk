---
title: Flere kontrakter | Microsoft Docs
description: Afhængigt af dine serviceaftaler med en kunde, skal du evt. håndtere en serviceartikel under flere servicekontrakter.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/01/2019
ms.author: sgroespe
ms.openlocfilehash: ccb677f128262435427f819ba0c24da254e3ce5c
ms.sourcegitcommit: 02e704bc3e01d62072144919774f1244c42827e4
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 10/01/2019
ms.locfileid: "2315944"
---
# <a name="multiple-contracts"></a>Flere kontrakter
Afhængigt af dine serviceaftaler med en kunde, skal du evt. håndtere en serviceartikel under flere servicekontrakter.  
  
Ved at håndtere en serviceartikel under flere kontrakter kan du gøre følgende:  
  
* Udstede forskellige kontrakter for samme serviceartikel.  
* Servicere delene separat.  
* Tage forskellige kvalifikationer, der kræves til forskellige dele af serviceartiklen, i betragtning, f.eks. mekaniske komponenter og software.  
* Angive forskellige svartidspunkter og intervaller for servicering af forskellige dele af en serviceartikel.  
* Angive, at der skal foretages forskellige typer aktiviteter på en serviceartikel, når serviceartiklen kræver forskellige typer service på forskellige tidspunkter.  
* Vælge og tildele det korrekte kontraktnummer til en serviceartikellinje, når du opretter en serviceordre.  
* Håndtere relevante finansielle oplysninger om serviceartikler og serviceaftaler.  
  
Følgende viser eksempler på brugen af flere kontrakter.  
  
## <a name="creating-multiple-contracts-per-service-item"></a>Oprette flere kontrakter pr. serviceartikel  
Du kan oprette en servicekontrakt eller et kontrakttilbud manuelt for de serviceartikler, der allerede er registreret i ikke-annullerede kontrakter, der tilhører den samme kunde. Det kan gøres ved at følge standardproceduren til oprettelse af servicekontrakter og servicekontrakttilbud. Du kan finde flere oplysninger i [Arbejde med servicekontrakter og servicekontrakttilbud](service-how-to-create-service-contracts-and-service-contract-quotes.md).  
  
Når du tilføjer en serviceartikel på en kontraktlinje, som er registreret i andre servicekontrakter eller kontrakttilbud, vises en advarsel om, at serviceartiklen allerede tilhører en eller flere servicekontrakter eller et eller flere kontrakttilbud. Hvis du bekræfter advarslen, kopieres alle relevante oplysninger om serviceartiklen til en nyoprettet kontraktlinje.  
  
## <a name="copying-documents"></a>Kopiere linjer  
Du kan automatisk oprette en servicekontrakt eller et kontrakttilbud for serviceartikler, der allerede er registreret i andre servicekontrakter eller kontrakttilbud ved hjælp af handlingen **Kopiér dokument**.  
  
## <a name="creating-service-orders-for-multiple-contracts"></a>Oprette serviceordrer for flere kontrakter  
Du kan oprette en serviceordre manuelt for en serviceartikel, der er registreret i flere aktive kontrakter. En servicekontrakt er aktiv, når den er underskrevet og ikke er udløbet.  
  
## <a name="see-also"></a>Se også  
[Opfylde servicekontrakter](service-fulfill-service-contracts.md)  
[Oprette serviceordrer](service-how-to-create-service-orders.md)  
