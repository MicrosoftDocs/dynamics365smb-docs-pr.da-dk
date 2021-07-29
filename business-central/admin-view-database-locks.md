---
title: Se databaselåse
description: Få mere at vide om, hvordan du kan få vist oplysninger om kundedatabaselåse direkte fra klientgrænsefladen i Business Central.
author: jswymer
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.date: 06/14/2021
ms.author: jswymer
ms.openlocfilehash: fb42b07832d33c995299d5033b8c548a37a86f56
ms.sourcegitcommit: a7cb0be8eae6ece95f5259d7de7a48b385c9cfeb
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 07/08/2021
ms.locfileid: "6443100"
---
# <a name="viewing-database-locks"></a>Sådan ser du databaselåse

Låsning af databaser styrer adgangen for flere brugere til de samme data på samme tid. Hvis du vil beskytte en transaktion mod andre transaktioner, der ændrer de samme data, medfører den første transaktion en låsning af dataene. Låsen forbliver aktiv, indtil transaktionen er udført.

Brugere kan forhindres i at fuldføre transaktioner på de låste data. De vil typisk se en meddelelse, der angiver låsetilstanden.

## <a name="to-view-database-locks"></a>Sådan ser du databaselåse

Vælg ![Søg efter side eller rapport.](media/ui-search/search_small.png "Ikonet Søg efter side eller rapport") ikon, skriv **Databaselåse**, og vælg derefter det relaterede link.

Siden **Databaselåse** viser et øjebliksbillede af alle aktuelle databaselåse.

Få flere oplysninger om låsning af databaser i [Overvågning af databaselåsninger](/dynamics365/business-central/dev-itpro/administration/monitor-database-locks) i hjælp til Business Central-udviklere og it-eksperter.

## <a name="see-also"></a>Se også

[Overvåg låsninger af databaser](/dynamics365/business-central/dev-itpro/administration/monitor-database-locks) 


[!INCLUDE[footer-include](includes/footer-banner.md)]