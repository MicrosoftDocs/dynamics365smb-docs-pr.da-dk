---
title: Se databaselåse
author: jswymer
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.date: 04/01/2020
ms.author: jswymer
ms.openlocfilehash: 1153ffc97d0f22c889ff23c5a27a8c0446b17018
ms.sourcegitcommit: 88e4b30eaf6fa32af0c1452ce2f85ff1111c75e2
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 04/01/2020
ms.locfileid: "3196372"
---
# <a name="viewing-database-locks"></a>Sådan ser du databaselåse

## <a name="about-locks"></a>Om låse

Låsning af databaser styrer adgangen for flere brugere til de samme data på samme tid. Hvis du vil beskytte en transaktion mod andre transaktioner, der ændrer de samme data, medfører den første transaktion en låsning af dataene. Låsen forbliver aktiv, indtil transaktionen er udført.

Brugere kan forhindres i at fuldføre transaktioner på de låste data. De vil typisk se en meddelelse, der angiver låsetilstanden.

## <a name="to-view-database-locks"></a>Sådan ser du databaselåse

Vælg ikonet ![Søg efter side eller rapport](media/ui-search/search_small.png "Ikonet Søg efter side eller rapport"), angiv **Databaselåse**, og vælg derefter det relaterede link.

Siden **Databaselåse** viser et øjebliksbillede af alle aktuelle databaselåse.

Få flere oplysninger om låsning af databaser i [Overvågning af databaselåsninger](/dynamics365/business-central/a/dev-itpro/administration/monitor-database-locks) i hjælp til Business Central-udviklere og it-eksperter.

## <a name="see-also"></a>Se også

[Overvåg låsninger af databaser](/dynamics365/business-central/a/dev-itpro/administration/monitor-database-locks) 
