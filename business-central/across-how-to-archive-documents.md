---
title: Arkivere salgs- og købsdokumenter
description: Du kan arkivere salgs-og købsordrer, tilbud, returvareordrer og rammeordrer og gendanne originalerne, hvis det er nødvendigt.
author: brentholtorf
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.form: 42, 49, 50, 459, 460, 5159, 5162, 5164, 5167, 6627, 6630, 6644, 9305, 9306, 9346, 9347, 9348, 9349
ms.date: 03/06/2022
ms.author: bholtorf
ms.openlocfilehash: c81248844f603f80304822c0ce089c666f9be9bc
ms.sourcegitcommit: 7b6d70798b4da283d1d3e38a05151df2209c2b72
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 06/12/2022
ms.locfileid: "8950325"
---
# <a name="archive-documents"></a>Arkivere dokumenter
Du kan arkivere salgs-og købsordrer, tilbud, returvareordrer og rammeordrer. Hvis du arkiverer dokumenter, kan du gendanne originalen. Du kan arkiverer et salgs- eller købsdokument flere gange og gemme en ny arkiveret version hver gang.

For arkiverede salgsdokumenter, hvor originalen stadig findes og ikke er bogført, kan du bruge funktionen **Gendan**, hvis du vil overskrive det aktuelle dokument med en arkiveret version. 

Du kan kun genbruge indholdet i arkiverede dokumenter, hvis originalen er slettet, ved at kopiere dataene, for eksempel med handlingen **Kopiér fra dokument**.  

## <a name="to-set-up-automatic-document-archiving"></a>Sådan konfigurerer du automatisk dokumentarkivering

Du kan konfigurere automatisk arkivering af salgs- og indkøbsordrer, tilbud, rammeordrer og returordrer. Når automatisk arkivering er aktiveret, oprettes der en ny version af det arkiverede dokument, når nogen udfører følgende opgaver:

* Ændrer eller sletter et dokument.
* Udskriver, henter eller sender et dokument med e-mail.
* Konverterer et tilbud til en ordre eller en faktura.
* Bogfører en ordre.

Nedenstående fremgangsmåde beskriver konfigurationen af automatisk arkivering af salgsdokumenter. Fremgangsmåden er den samme for købsdokumenter.

1. Vælg ![Lightbulb, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, angiv **Salgsopsætning**, og vælg derefter det relaterede link.
2. I oversigtspanelet **arkivering** skal du angive, om der skal slås automatisk arkivering til de forskellige typer salgsdokumenter. [!INCLUDE [tooltip-inline-tip_md](includes/tooltip-inline-tip_md.md)]

I følgende tabel beskrives indstillingerne for feltet **Arkivér tilbud**.

|Indstilling|Beskrivelse|
|------|-----------|
|**Aldrig**| Arkivér aldrig salgstilbud, når de er slettet.|
|**Spørgsmål**|Spørg brugeren om at vælge, om salgstilbud skal arkiveres, når de slettes.|
|**Altid**|Arkivér automatisk salgstilbud, når de slettes.|

## <a name="to-archive-a-sales-order"></a>Sådan arkiveres en salgsordre

Nedenstående procedure beskriver, hvordan du arkiverer en salgsordre. Fremgangsmåden er den samme for alle ordrer, rammeordrer, returvareordrer og tilbud.

1. Vælg ![Lightbulb, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **Salgsordrer**, og vælg derefter det relaterede link.  
2. Åbn en salgsordre, som du vil arkivere.  
3. Vælg handlingen **Arkivér bilag**.

Salgsordren arkiveres. Du kan se den på siden **Arkiverede salgsordrer**.

## <a name="to-restore-a-non-posted-sales-order-from-the-archive"></a>Sådan gendannes en ikke-bogført salgsordre fra arkivet

Følgende procedure beskriver, hvordan du gendanner en arkiveret salgsordre tilbage til den oprindelige salgsordre. Gendannelse af et dokument er kun muligt, når det oprindelige dokument ikke er bogført. Fremgangsmåden er den samme for alle ordrer, rammeordrer, returvareordrer og tilbud.

1. Vælg ![Lightbulb, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **Salgsordrearkiver**, og vælg derefter det relaterede link.
2. Vælg den arkiverede salgsordre eller en version af den, som du vil gendanne, og vælg derefter handlingen **Gendan**.  

Oplysningerne i den oprindelige salgsordre erstattes med oplysningerne fra den valgte arkiverede version.

## <a name="to-delete-archived-sales-orders"></a>Sådan sletter du arkiverede salgsordrer

Nedenstående procedure beskriver, hvordan du sletter arkiverede salgsordrer. Trinene er de samme for andre arkiverede salgs- og købsdokumenter.

1. Vælg ![Lightbulb, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **Salgsordrearkiver**, og vælg derefter det relaterede link.  
2. Vælg handlingen **Slet ældre versioner**, og vælg derefter de relevante filtre på siden **Slet arkiverede salgsordreversioner**.  
3. Vælg knappen **OK**.

## <a name="see-also"></a>Se også

[Spor dokumentlinjer](across-how-to-track-document-lines.md)  
[Salg](sales-manage-sales.md)  
[Generelle forretningsfunktioner](ui-across-business-areas.md)  
[Arbejd med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]
