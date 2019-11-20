---
title: Overvågning af ændringer | Microsoft Docs
description: Du kan aktivere en brugerlog for at få en oversigt over ændringer af data i registrerede tabeller. Du kan også spore aktiviteter med bestemte typer aktivitetslogge.
author: edupont04
ms.service: dynamics365-business-central
ms.topic: get-started-article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: user log, user activity, tracking
ms.date: 10/01/2019
ms.author: edupont
ms.openlocfilehash: cffa7d23b7c09561914cc00a8a4b9820ed743c29
ms.sourcegitcommit: cd5d3d288feee76d058d325720135275f4c8ad85
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 11/08/2019
ms.locfileid: "2775351"
---
# <a name="auditing-changes-in-business-central"></a>Ændringer af revision i Business Central

Du kan aktivere ændringsloggen i [!INCLUDE[d365fin](includes/d365fin_md.md)], så du har en oversigt over aktiviteter. Loggen er baseret på ændringer, der er foretaget i de tabeller, som du sporer. På siden **Ændringslogposter** registreres posterne i kronologisk rækkefølge og viser de ændringer, der er foretaget i felterne på de angivne tabeller. Ændringsloggen indsamler alle ændringer, der foretages i tabellen.

> [!Important]
> En brugers ændringer vises ikke i **Ændringslogposter**, før brugerens session startes igen, hvilket sker i følgende tilfælde:
<br />
> * Sessionen er udløbet og er blevet opdateret.
> * Brugeren har valgt et andet regnskab eller Rollecenter.
> * Bruger har logget af og på igen.

## <a name="working-with-the-change-log"></a>Arbejde med ændringsloggen

Et almindeligt problem i mange økonomisystemer er at finde årsagen til fejl og ændringer i data. Det kan være alt fra et forkert kundetelefonnummer til en forkert postering i regnskabet. Du kan bruge funktionaliteten i ændringsloggen til at spore alle direkte modifikationer, som en bruger foretager af data i databasen. Du skal for hver tabel og hvert felt angive, hvad der skal registreres i loggen. Derefter skal du aktivere ændringsloggen.  

Du aktiverer og deaktiverer ændringsloggen på siden **Opsætning af ændringslog**. Når en bruger aktiverer eller deaktiverer ændringsloggen, logføres denne aktivitet, så du altid kan se, hvilken bruger der har deaktiveret eller aktiveret ændringsloggen.

Hvis du på siden **Opsætning af ændringslog** vælger handlingen **Tabeller**, kan du angive, hvilke tabeller du vil spore ændringer for, og hvilke ændringer du vil spore. [!INCLUDE[d365fin](includes/d365fin_md.md)] sporer også en række systemtabeller.

Når du har konfigureret ændringsloggen, aktiveret den og ændret data, kan du få vist og filtrere ændringerne på siden **Ændringslogposter**. Hvis du vil slette poster, kan du gøre det på siden **Slet ændringslogposter**, hvor du kan angive filtre baseret på datoer og tidspunkter.  

## <a name="working-with-activity-logs"></a>Arbejde med aktivitetslogge

Fra nogle sider i [!INCLUDE [prodshort](includes/prodshort.md)] kan du få vist en aktivitetslog, der viser status og eventuelle fejl i filer, som du eksporterer fra eller importerer til [!INCLUDE [prodshort](includes/prodshort.md)].  

Oplysningerne vises på siden **Aktivitetslog** i overensstemmelse med den kontekst, de åbnes fra. Du kan åbne vinduet fra siderne **Opsætning af dokumentudvekslingstjeneste**, **Indgående dokument**, **Bogført salgsfaktura** og **Bogført salgskreditnota**. Du kan tømme listen med logposter eller blot rydde oversigten over poster, der er ældre end 7 dage.  

## <a name="see-also"></a>Se også
[Ændre grundlæggende indstillinger](ui-change-basic-settings.md)  
[Sortering](ui-sorting.md)  
[Søge efter sider og oplysninger med Fortæl mig](ui-search.md)  
[Tildele tilladelser til brugere og grupper](ui-define-granular-permissions.md)    
[Arbejde med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)  
