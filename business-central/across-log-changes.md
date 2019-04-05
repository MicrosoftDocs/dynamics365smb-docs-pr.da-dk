---
title: Spore brugeraktivitet i en ændringslog | Microsoft Docs
description: Du kan aktivere en brugerlog for at få en oversigt over ændringer af data i registrerede tabeller.
author: edupont04
ms.service: dynamics365-business-central
ms.topic: get-started-article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: user log, user activity, tracking
ms.date: 11/14/2018
ms.author: edupont
ms.openlocfilehash: 2a71909faf66c13a0923a10bfc12369127642875
ms.sourcegitcommit: d09f5ee0e164c7716f4ccb2ed71e2f9732a1f4f9
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 03/19/2019
ms.locfileid: "852880"
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

## <a name="see-also"></a>Se også
[Ændring af grundlæggende indstillinger](ui-change-basic-settings.md)  
[Sortering](ui-sorting.md)  
[Bruge Fortæl mig til at finde funktioner og oplysninger](ui-search.md)  
[Administrere brugere og deres rettigheder](ui-how-users-permissions.md)    
[Arbejde med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)  
