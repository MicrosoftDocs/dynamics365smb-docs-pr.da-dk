---
author: edupont04
ms.topic: include
ms.date: 04/01/2021
ms.author: edupont
ms.openlocfilehash: 44cd8156e66be7736da4f1c51f507715d7842478
ms.sourcegitcommit: ef80c461713fff1a75998766e7a4ed3a7c6121d0
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 02/15/2022
ms.locfileid: "8147410"
---
Når du angiver dato/klokkeslæt, som en dato og klokkeslæt kombineret i ét felt, skal du angive et mellemrum mellem datoen og klokkeslættet. Datodelen kan kun indeholde mellemrum i form af officielle datoseparatorer af indstillingerne for land/område. Tidsangivelsen, der kan indeholde mellemrum omkring AM/PM-symbolet i de relevante indstillinger for området.

<!--It is also possible to enter only a date in a datetime field, but it is not possible to enter only a time.-->

I den følgende tabel kan du se, hvordan du kan skrive dato og klokkeslæt, og hvordan de fortolkes.  

|Post|Fortolkning|
|---------------|------------------------|
|08-01-2022 05:48:12 PM|08\-01\-2022 05:48:12 PM|
|131222 132455|13-12-22 13:24:55|
|1-12-22 10|01-12-22 10:00:00|
|1.12.22 5|01-12-22 05:00:00|
|1.12.22|01-12-22 00:00:00|
|11 12|11-løbende måned-løbende år 12:00:00|
|1112 12|11-12-aktuelt år 12:00:00|
|d eller dags dato|dags dato 00:00:00|
|d tid|dags dato aktuelt klokkeslæt|
|d 10:30|dags dato 10:30:00|
|d 3:3:3|dags dato 03:03:03|
|a eller arbejdsdato|arbejdsdato 00:00:00|
|m eller mandag|Mandag i den aktuelle uge 00:00:00|
|ti eller tirsdag|Tirsdag i den aktuelle uge 00:00:00|
|on eller onsdag|Onsdag i den aktuelle uge 00:00:00|
|to eller torsdag|Torsdag i den aktuelle uge 00:00:00|
|f eller fredag|Fredag i den aktuelle uge 00:00:00|
|l eller lørdag|Lørdag i den aktuelle uge 00:00:00|
|s eller søndag|Søndag i den aktuelle uge 00:00:00|
|ti 10:30|Tirsdag i den aktuelle uge 10:30:00|
|ti 3:3:3|Tirsdag i den aktuelle uge 03:03:03|
|ti23 t|Tirsdag i uge 23 i året for arbejdsdatoen, det aktuelle tidspunkt på dagen|
|ti23|Tirsdag i uge 23 i året for arbejdsdatoen|
|ti 23|Dags dato 23:00:00|
|ti-1|Tirsdag i uge 1 i året for arbejdsdatoen|


