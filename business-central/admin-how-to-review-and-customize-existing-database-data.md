---
title: Sådan gennemgås og tilpasses de eksisterende databasedata | Microsoft Docs
description: Efterhånden som du opretter en konfigurationspakke for en løsning, kan du få vist og tilpasse tilgængelige databasedata, så de passer til debitorens behov. Databasetabellen skal have en tilknyttet side.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/01/2019
ms.author: sgroespe
redirect_url: admin-how-to-create-custom-company-configuration-packages
ms.openlocfilehash: 95b16dc77bcdb0051447a4f153dd720661c52cf9
ms.sourcegitcommit: 60b87e5eb32bb408dd65b9855c29159b1dfbfca8
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 04/29/2019
ms.locfileid: "1244557"
---
# <a name="review-and-customize-existing-database-data"></a>Gennemgå og tilpasse de eksisterende databasedata
Efterhånden som du opretter en konfigurationspakke for en løsning, kan du få vist og tilpasse tilgængelige databasedata, så de passer til debitorens behov. Databasetabellen skal have en tilknyttet side.  

### <a name="to-customize-data-in-the-database"></a>Tilpasse data i databasen  

1.  I konfigurationsregnearket skal du identificere de tabeller, hvis data du ønsker at se eller tilpasse.  

    > [!NOTE]  
    >  Sørg for, at hver enkelt tabel har fået tildelt et side-id. For standardtabeller i [!INCLUDE[d365fin](includes/d365fin_md.md)] angives værdien automatisk. For brugerdefinerede tabeller skal du angive id'et.  

2.  Under fanen **Handlinger** i gruppen **Vis** skal du vælge **Databasedata**.  

     Siden [!INCLUDE[d365fin](includes/d365fin_md.md)] for siden åbnes.  

3.  Gennemse de tilgængelige oplysninger. Rediger dem efter behov ved at slette poster, der ikke er relevante, eller ved tilføje nye.  

## <a name="see-also"></a>Se også  
 [Administrere virksomhedskonfigurationen i et regneark](admin-how-to-manage-company-configuration-in-a-worksheet.md)
