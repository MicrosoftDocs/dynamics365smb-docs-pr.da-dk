---
title: Arkivere salgs- og købsdokumenter
description: Du kan arkivere salgs- og købsdokumenter, ordrer, tilbud, returvareordrer og rammeordrer, og du kan bruge det arkiverede dokument til at genskabe det dokument, som det blev arkiveret fra.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 06/29/2021
ms.author: edupont
ms.openlocfilehash: a12d8d7a11e581a6cfe93b6a1f4588cd87efc98f
ms.sourcegitcommit: a486aa1760519c380b8cdc8fdf614bed306b65ea
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 07/13/2021
ms.locfileid: "6543268"
---
# <a name="archive-documents"></a>Arkivere dokumenter
Du kan arkivere salgs- og købsordrer, tilbud, returvareordrer og rammeordrer, f.eks. fordi du vil gemme en kopi af et dokument til senere genbrug. Du kan arkiverer et salgs- eller købsdokument flere gange og gemme en ny arkiveret version hver gang.

For arkiverede salgsdokumenter, hvor originalen stadig findes og ikke er bogført, kan du bruge funktionen **Gendan**, hvis du vil overskrive originalen med den arkiverede version af dokumentet. Dette er nyttigt, hvis du vil gendanne indholdet af et dokument i en tidligere tilstand.

Du kan kun genbruge indholdet i arkiverede dokumenter, hvis originalen er slettet, ved at kopiere dataene, for eksempel med funktionen **Kopiér fra dokument**.  

## <a name="to-set-up-automatic-document-archiving"></a>Sådan konfigurerer du automatisk dokumentarkivering

Du kan konfigurere automatisk arkivering af salgs- og indkøbsordrer, tilbud, rammeordrer og returordrer, før du sletter dokumenter.

Nedenstående fremgangsmåde beskriver konfigurationen af automatisk arkivering af salgsdokumenter. Fremgangsmåden er den samme for købsdokumenter.

1. Vælg ![Lightbulb, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, angiv **Salgsopsætning**, og vælg derefter det relaterede link.
2. På siden **Salgsopsætning** skal du udfylde følgende felter. [!INCLUDE [tooltip-inline-tip_md](includes/tooltip-inline-tip_md.md)]

Specielt til feltet **Arkiv tilbud** kan følgende tabel bruges til at optegne forskellen mellem indstillingerne.

|Indstilling|Beskrivlse|
|------|-----------|
|**Aldrig**| Aldrig, hvis du aldrig vil arkivere salgstilbud, når de slettes.|
|**Spørgsmål**|Vælg at spørge brugeren om at vælge, om salgstilbud skal arkiveres, når de slettes.|
|**Altid**|Vælg at arkivere automatisk salgstilbud, når de slettes.|

## <a name="to-archive-a-sales-order"></a>Sådan arkiveres en salgsordre

Nedenstående procedure beskriver, hvordan du arkiverer en salgsordre. Fremgangsmåden er den samme for alle ordrer, rammeordrer, returvareordrer og tilbud.

1. Vælg ![Lightbulb, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **Salgsordrer**, og vælg derefter det relaterede link.  
2. Åbn en salgsordre, som du vil arkivere.  
3. Vælg handlingen **Arkivér bilag**.

Salgsordren arkiveres. Du kan se den på siden **Arkiverede salgsordrer**.

## <a name="to-restore-a-non-posted-sales-order-from-the-archive"></a>Sådan gendannes en ikke-bogført salgsordre fra arkivet

Følgende procedure beskriver, hvordan du får indholdet af en arkiveret salgsordre tilbage til den oprindelige salgsordre. Det er kun muligt, når det oprindelige dokument ikke er bogført. Fremgangsmåden er den samme for alle ordrer, rammeordrer, returvareordrer og tilbud.

1. Vælg ![Lightbulb, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **Salgsordrearkiver**, og vælg derefter det relaterede link.
2. Vælg den arkiverede salgsordre eller en version af den, som du vil gendanne, og vælg derefter handlingen **Gendan**.  

Oplysningerne i den oprindelige salgsordre erstattes med oplysningerne fra den valgte arkiverede version.

## <a name="to-delete-archived-sales-orders"></a>Sådan sletter du arkiverede salgsordrer

Nedenstående procedure beskriver, hvordan du sletter arkiverede salgsordrer. Trinene er de samme for andre arkiverede salgs- og købsdokumenter.

1. Vælg ![Lightbulb, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **Salgsordrearkiver**, og vælg derefter det relaterede link.  
2. Vælg handlingen **Slet arkiverede salgsordreversioner**, og vælg derefter de relevante filtre på siden **Slet arkiverede salgsordreversioner**.  
3. Vælg knappen **OK**.

## <a name="see-also"></a>Se også

[Spor dokumentlinjer](across-how-to-track-document-lines.md)  
[Salg](sales-manage-sales.md)  
[Generelle forretningsfunktioner](ui-across-business-areas.md)  
[Arbejde med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]
