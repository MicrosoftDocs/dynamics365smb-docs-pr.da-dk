---
title: Se tabeloplysninger
description: Få mere at vide om, hvordan du kan få vist oplysninger om databasetabeller direkte fra klientgrænsefladen i Business Central.
author: jswymer
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.date: 06/14/2021
ms.author: jswymer
ms.openlocfilehash: 581d92010fa566c33775ffd6238ca6e0cfca0837
ms.sourcegitcommit: a7cb0be8eae6ece95f5259d7de7a48b385c9cfeb
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 07/08/2021
ms.locfileid: "6443075"
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