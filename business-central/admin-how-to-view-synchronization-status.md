---
title: Se status på synkroniseringsjob (indeholder video)
description: Du kan bruge siden Fejl ved sammenkædet datasynkronisering til at få vist status for de synkroniseringsjob, der er blevet udført for sammenkædede poster i integrationer.
author: brentholtorf
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: sales, crm, integration, sync, synchronize
ms.search.form: 6250
ms.date: 06/14/2021
ms.author: bholtorf
ms.openlocfilehash: c98cadba0a9bdf21a89a6c50dd61d805f0547685
ms.sourcegitcommit: 8a12074b170a14d98ab7ffdad77d66aed64e5783
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 03/31/2022
ms.locfileid: "8521250"
---
# <a name="view-the-status-of-synchronization-jobs"></a>Se status på synkroniseringsjob


Du kan bruge siden **Fejl ved sammenkædet datasynkronisering** til at se status for de synkroniseringsjob, der er blevet udført for sammenkædede poster i en Dataverse- eller [!INCLUDE[crm_md](includes/crm_md.md)]-integration. Dette omfatter job, der er kørt fra opgavekøen, og manuelle synkroniseringsjob, der er kørt på poster fra [!INCLUDE[prod_short](includes/prod_short.md)]. Du kan f.eks. se, hvordan deres status er nyttig, når du foretager fejlfinding, fordi det giver dig adgang til detaljer om fejl, der vedrører sammenkædede poster. Denne type fejl forårsages typisk af brugerhandlinger, f.eks. når:  

* To personer har udført en ændring af de samme data i begge forretningsapps.
* Nogen har slettet data i en af disse apps, men ikke begge.

> [!Note]
> På siden **Fejl ved sammenkædet datasynkronisering** vises oplysninger om job, der er relateret til sammenkædede poster. Hvis du løser alle fejl, men posterne stadig ikke synkroniseres, kan der være noget, der skal udføres med en indstilling for integrationen. Normalt skal din administrator løse disse fejltyper.   

## <a name="example"></a>Eksempel
I denne video vises et eksempel på, hvordan du retter fejl, der er opstået under synkronisering med [!INCLUDE[prod_short](includes/cds_long_md.md)]. Denne proces vil være den samme for alle integrationer. 

> [!VIDEO https://go.microsoft.com/fwlink/?linkid=2097304]


## <a name="to-view-and-resolve-synchronization-errors-for-coupled-records"></a>Sådan vises og løses synkroniseringsfejl for sammenkædede poster
1. Vælg ![Lightbulb, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, åbn **Fejl ved sammenkædet datasynkronisering**, og vælg derefter det relaterede link.
2. På siden **Fejl ved sammenkædet datasynkronisering** vises problemer, der opstod, da du synkroniserede sammenkoblede poster. Følgende tabel indeholder handlinger, som du kan bruge til at løse problemer et efter et:

|Handling|Beskrivelse|
|----|----|
|**Fjern sammenkædning**|Fjerner sammenkædningen af posterne, og de synkroniseres ikke længere. Hvis du vil genstarte med at synkronisere posterne, skal du sammenkæde dem igen. |
|**Prøv igen**, og **Prøv alle igen**|For hver post, hvor der er fundet en fejl, springes synkroniseringen over, medmindre du løser problemet. Prøv igen medtager den markerede post ved næste synkronisering, og **Prøv alle** medtager alle posterne igen.|
|**Synkroniser**|Appen forsøger at løse en konflikt, hvor data er ændret i begge forretningsapps. Du kan vælge de data, der skal anvendes.|
|**Gendan poster** og **Slet poster**|Disse er nyttige, når en post er blevet slettet i en af dine forretningsapps. Slet poster sletter posten i den app eller række, hvor den stadig findes. Gendan poster gendanner posten eller rækken i den forretningsapp, hvor den blev slettet.|

> [!NOTE]
> Hvis du vil reducere antallet af konflikter, der skal løses, kan du indstille tilknytningerne for integrationstabeller, så disse handlinger anvendes automatisk. Du kan finde flere oplysninger i [Integrationstabeller til tilknytning](admin-how-to-modify-table-mappings-for-synchronization.md#mapping-integration-tables).

## <a name="to-view-the-synchronization-log-for-a-specific-manually-synchronized-record"></a>Sådan får du vist synkroniseringsloggen for en bestemt (manuelt synkroniseret) post
1. Åbn f.eks. en kunde, en vare eller en anden post, der synkroniserer data mellem [!INCLUDE[prod_short](includes/prod_short.md)] og Dataverse or [!INCLUDE[crm_md](includes/crm_md.md)].
2. Vælg handlingen **Synkroniseringslog** for at få vist synkroniseringsloggen for en valgt post. En bestemt kunde f.eks., som du har synkroniseret manuelt.

## <a name="remove-couplings-between-records"></a>Fjerne koblinger mellem poster
Når noget går galt i integrationen, og du har brug for at koble posterne fra, så de ikke længere synkroniseres, kan du gøre det for en eller flere poster ad gangen. Du kan fjerne frakoble en eller flere poster fra listesider eller siden **Koblede datasynkroniseringsfejl** ved at vælge en eller flere linjer og vælge **Slet kobling**. Du kan også fjerne alle koblinger for en eller flere tabeltilknytninger på siden **Tilknytninger til integrationstabel**. 

Hvis en enhed med en envejs kobling slettes i [!INCLUDE[prod_short](includes/prod_short.md)], skal du slette den brudte kobling manuelt. Hvis du vil gøre dette, skal du vælge **Søg efter slettet** handling på siden **Fejl i forbindelse med sammenkoblet datasynkronisering** og derefter slette koblingerne.

## <a name="see-also"></a>Se også  
[Opsætning af brugerkonti til integration med Dynamics 365 Sales](admin-setting-up-integration-with-dynamics-sales.md)  
[Brug Dynamics 365 Sales fra Business Central](marketing-integrate-dynamicscrm.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]