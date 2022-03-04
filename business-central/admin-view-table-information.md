---
title: Se tabeloplysninger
description: Få mere at vide om, hvordan du kan få vist oplysninger om databasetabeller direkte fra klientgrænsefladen i Business Central.
author: jswymer
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.form: 8700
ms.date: 06/14/2021
ms.author: jswymer
ms.openlocfilehash: db1a5ef84d4174b960de6f3e20f7d4e29c8c44c8
ms.sourcegitcommit: ef80c461713fff1a75998766e7a4ed3a7c6121d0
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 02/15/2022
ms.locfileid: "8133092"
---
# <a name="viewing-table-information"></a>Sådan ser du tabeloplysninger

Siden **8700-tabeloplysninger** indeholder oplysninger om alle system- og forretningstabeller i en Business Central-løsning. Siden viser især oplysninger om den mængde data, som tabellerne indeholder.

Disse oplysninger kan være nyttige til fejlfinding i forbindelse med ydeevnen, da du kan se fordelingen af datastørrelse på tværs af tabeller.

## <a name="viewing-table-information"></a>Sådan ser du tabeloplysninger

Hvis du vil åbne denne side, skal du vælge ![Søg efter side eller rapport.](media/ui-search/search_small.png "Ikonet Søg efter side eller rapport") ikon, åbn **Tabeloplysninger**, og vælg derefter det relaterede link.

Følgende tabel indeholder en beskrivelse af de oplysninger, der er angivet for hver tabel:

|Kolonne|Description|
|------|-----------|
|Virksomhedsnavn|Navnet på den virksomhed, som tabellen tilhører (hvis det er relevant).|
|Tabelnavn|Navnet på tabellen.|
|Tabelnr.|Tabellens ID|
|Nummer Poster|Det samlede antal poster, der er gemt i tabellen.|
|Poststørrelse|Den gennemsnitlige poststørrelse i KB/post. Værdien beregnes ved hjælp af følgende formel: 1024 (størrelse)/(antal poster). |

## <a name="see-also"></a>Se også

[Inspicere sider](across-inspect-page.md)  
[Artikler om ydeevne til udviklere](/dynamics365/business-central/dev-itpro/performance/performance-developer)  


[!INCLUDE[footer-include](includes/footer-banner.md)]