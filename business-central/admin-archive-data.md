---
title: Dataarkivudvidelsen
description: Når du arkiverer data, oprettes der en billig sikkerhedskopi af posterne.
author: bholtorf
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.form: 630
ms.date: 06/14/2021
ms.author: bholtorf
ms.openlocfilehash: e2df40494f72260a1ce7e66f57ea1c96fb35b301
ms.sourcegitcommit: ef80c461713fff1a75998766e7a4ed3a7c6121d0
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 02/15/2022
ms.locfileid: "8130822"
---
# <a name="the-data-archive-extension"></a>Dataarkivudvidelsen
Med tiden vil virksomheden samle en betydelig mængde data, og som administrator kan det være en god ide at finde en strategi til arkivering af data. Når mange data kan gøre tingene langsommere, kan det f. eks. tage lidt længere tid at oprette rapporter, eller du kan endda låse poster. Derudover kan store mængder data medføre øgede lageromkostninger.

Dataarkivudvidelsen udgør en grundlæggende ramme for arkivering og sikkerhedskopiering af data som en del af datokomprimeringen. Når du bruger datokomprimering, konsolideres relaterede poster til en enkelt post, og de originaler slettes. Du kan finde flere oplysninger i [komprimering af data med datokomprimering](admin-manage-documents.md#compress-data-with-date-compression). Der kan imidlertid være en værdi, som forhindrer, at dataene gemmes, ved at arkivere den til senere brug.

## <a name="start-archiving-data"></a>Start arkivering af data
Udvidelsen er forudinstalleret og tilgængelig i **administration af udvidelser**, så du behøver ikke at foretage dig noget for at komme i gang. Filtypenavnet er også tilgængelig i Microsoft AppSource. 

Dine data arkiver vises på siden **Dataarkivliste**. Hvert arkiv kan indeholde data fra flere tabeller og kan indeholde op til 10.000 poster. Hvis der er mere end 10.000 poster i en tabel, oprettes der endnu et arkiv for de næste 10.000 poster osv. Hvis du f. eks. arkiverer 10.100 finansposter, opretter Business Central et "finanspost"-Arkiv for de første 10.000, og derefter et ekstra arkiv for de resterende 100 poster. 

Når du har arkiveret data, kan du udforske dem med Microsoft Excel eller som en CSV-fil.

* Hvis du bruger Excel-indstillingen, vil projektmappen indeholde én kladde for hver dataarkivtabel.
* Hvis du bruger CSV-indstillingen, får du en ZIP-fil med én CSV-fil til hver dataarkivtabel.

> [!TIP]
> Indstillingerne i Excel og CSV gør det nemmere at bruge en anden app eller tjeneste til at flytte dataene til en anden placering, f. eks. Azure blob Storage eller Analysis Tool, f.eks. Microsoft Power BI.

Disse filtypenavne bruges af følgende kørsler til datokomprimering.

|Kørsler  |
|---------|
|Dato comp. Varebudgetposter |
|Datokomprimer bankposter |
|Datokomprimer debitorposter |
|Datokomprimer anlægsposter |
|Datokomprimer finansposter |
|Datokomprimer forsik.poster |
|Datokomprimer rep.poster Finans |
|Datokomprimer rep.poster Finans |
|Datokomprimer ressourceposter |
|Datokomprimer momsposter |
|Datokomprimer kreditorposter |
|Datokomprimer lagerposter Poster |
|Dato comp. Finansbudgetposter |

Hvis du vil begynde at arkivere data, når du kører en af kørslerne, skal du aktivere funktionen **arkiver slettede poster**.

## <a name="storage-considerations"></a>Lagerovervejelser
De arkiverede data gemmes i tabellen med **lejermediet**. Denne tabel er ikke medtaget, når databasestørrelsen beregnes i henhold til licensbetingelserne. Det tælles i stedet som fillager. Det anbefales dog, at du eksporterer gamle filer, f. eks. en CSV-fil, og derefter sletter de gamle Arkiv poster.

## <a name="see-also"></a>Se også
[Administrere lager ved at slette dokumenter eller komprimere data](admin-manage-documents.md)
