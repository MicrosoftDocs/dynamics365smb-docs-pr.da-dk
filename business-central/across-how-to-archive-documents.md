---
title: "Sådan arkiveres salgs- og købsdokumenter | Microsoft Docs"
description: "Du kan arkivere salgs- og købsdokumenter, ordrer, tilbud, returvareordrer og rammeordrer, og du kan bruge det arkiverede dokument til at genskabe det dokument, som det blev arkiveret fra."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 12/21/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: d7fb34e1c9428a64c71ff47be8bcff174649c00d
ms.openlocfilehash: 74460bfcff36d293006229f4a89719f8c05c2631
ms.contentlocale: da-dk
ms.lasthandoff: 03/22/2018

---
# <a name="archive-documents"></a>Arkivere dokumenter
Du kan arkivere salgs- og købsdokumenter, ordrer, tilbud, returvareordrer og rammeordrer, og du kan bruge det arkiverede dokument til at genskabe det dokument, som det blev arkiveret fra.

## <a name="to-set-up-automatic-document-archiving"></a>Sådan konfigurerer du automatisk dokumentarkivering  
Du kan konfigurere automatisk arkivering af salgs- og indkøbsordrer, tilbud, rammeordrer og returordrer, før du sletter dokumenter.

Nedenstående fremgangsmåde beskriver konfigurationen af automatisk arkivering af salgsdokumenter. Fremgangsmåden er den samme for købsdokumenter.
1.  Vælg ikonet ![Søg efter side eller rapport](media/ui-search/search_small.png "Ikonet Søg efter side eller rapport"), angiv **Salgsopsætning**, og vælg derefter det relaterede link.
2. I vinduet **Opsætning af salg og tilgodehavender** skal du udfylde følgende felter:

|Felt|Description|
|-----|-----------|
|**Arkivering af salgstilbud**|**Aldrig**, hvis du aldrig vil arkivere salgstilbud, når de slettes. **Spørgsmål**, hvis brugeren skal vælge, om salgstilbud skal arkiveres, når de slettes. **Altid**, hvis du automatisk vil arkivere salgstilbud, når de slettes.|
|**Arkivering af rammesalgsordrer**|Vælg dette, hvis du vil arkivere rammesalgsordrer automatisk, hver gang de slettes.|
|**Arkivering af ordrer og returvareordrer**|Vælg dette, hvis du vil arkivere salgsordrer automatisk, hver gang de slettes.|

## <a name="to-archive-a-sales-order"></a>Sådan arkiveres en salgsordre
Nedenstående procedure beskriver, hvordan du arkiverer en salgsordre. Fremgangsmåden er den samme for alle ordrer, rammeordrer, returvareordrer og tilbud.

1.  Vælg ikonet ![Søg efter side eller rapport](media/ui-search/search_small.png "Ikonet Søg efter side eller rapport"), angiv **Salgsordrer**, og vælg derefter det relaterede link.  
2.  Åbn en salgsordre, som du vil arkivere.  
3.  Vælg handlingen **Arkivér bilag**.

Salgsordren arkiveres. Du kan se den i vinduet **Arkiverede salgsordrer**. Her kan du også bruge den til at genskabe den salgsordre, som den blev arkiveret fra.

## <a name="to-recreate-a-sales-order-from-the-archive"></a>Sådan genoprettes en salgsordre fra arkivet
Nedenstående procedure beskriver, hvordan du genopretter en salgsordre. Fremgangsmåden er den samme for alle ordrer, rammeordrer, returvareordrer og tilbud.

1.  Vælg ikonet ![Søg efter side eller rapport](media/ui-search/search_small.png "Ikonet Søg efter side eller rapport"), angiv **Arkiverede salgsordrer**, og vælg derefter det relaterede link.
2.  Vælg den arkiverede salgsordre, du vil genoprette, og vælg derefter handlingen **Gendan**.  

Salgsordren oprettes og føjes til vinduet **Salgsordrer**.

## <a name="to-delete-archived-sales-orders"></a>Sådan sletter du arkiverede salgsordrer
Nedenstående procedure beskriver, hvordan du sletter arkiverede salgsordrer. Trinene er de samme for andre arkiverede salgs- og købsdokumenter.

1.  Vælg ikonet ![Søg efter side eller rapport](media/ui-search/search_small.png "Ikonet Søg efter side eller rapport"), angiv **Slet arkiverede salgsordreversioner**, og vælg derefter det relaterede link.  
2.  I feltet **Slet arkiverede salgsordreversioner** skal du vælge de relevante filtre.  
3.  Vælg knappen **OK**.

## <a name="see-also"></a>Se også
[Spor dokumentlinjer](across-how-to-track-document-lines.md)  
[Salg](sales-manage-sales.md)  
[Generelle forretningsfunktioner](ui-across-business-areas.md)  
[Arbejde med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

