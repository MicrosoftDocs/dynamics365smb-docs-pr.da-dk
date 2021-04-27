---
title: Se tabeloplysninger
description: Få mere at vide om, hvordan du kan få vist oplysninger om databasetabeller direkte fra klientgrænsefladen i Business Central.
author: jswymer
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.date: 04/01/2021
ms.author: jswymer
ms.openlocfilehash: 7a01143dd7928d5996c1620676a758ea634bdf5d
ms.sourcegitcommit: 766e2840fd16efb901d211d7fa64d96766ac99d9
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 03/31/2021
ms.locfileid: "5776887"
---
# <a name="viewing-table-information"></a>Sådan ser du tabeloplysninger

Siden **8700-tabeloplysninger** indeholder oplysninger om alle system- og forretningstabeller i en Business Central-løsning. Siden viser især oplysninger om den mængde data, som tabellerne indeholder.

Disse oplysninger kan være nyttige til fejlfinding i forbindelse med ydeevnen, da du kan se fordelingen af datastørrelse på tværs af tabeller.

## <a name="viewing-table-information"></a>Sådan ser du tabeloplysninger

Hvis du vil åbne denne side, skal du klikke på ikonet ![Søg efter side eller rapport](media/ui-search/search_small.png "Ikonet Søg efter side eller rapport"), angive **Tabeloplysninger** og derefter vælge det relaterede link.

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