---
title: Se status på synkroniseringsjob | Microsoft Docs
description: Få mere at vide om, hvordan du får vist status, når du har synkroniseret sammenkædede poster.
author: bholtorf
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: sales, crm, integration, sync, synchronize
ms.date: 10/01/2019
ms.author: bholtorf
ms.openlocfilehash: 022e364b6a40fe8df1f9c4e3425030d35f729e6a
ms.sourcegitcommit: 02e704bc3e01d62072144919774f1244c42827e4
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 10/01/2019
ms.locfileid: "2304488"
---
# <a name="view-the-status-of-synchronization-jobs"></a>Se status på synkroniseringsjob
Du kan bruge siden **Fejl ved sammenkædet datasynkronisering** til at få vist status for de synkroniseringsjob, der er blevet udført for sammenkædede poster i en [!INCLUDE[crm_md](includes/crm_md.md)]-integration. Dette omfatter job, der er kørt fra opgavekøen, og manuelle synkroniseringsjob, der er kørt på poster fra [!INCLUDE[d365fin](includes/d365fin_md.md)]. Du kan f.eks. se, hvordan deres status er nyttig, når du foretager fejlfinding, fordi det giver dig adgang til detaljer om fejl, der vedrører sammenkædede poster. Denne type fejl forårsages typisk af brugerhandlinger, f.eks. når:  

* To personer har udført en ændring af den samme post i begge forretningsapps.
* Nogen har slettet en post i en af disse apps, men ikke begge.

> [!Note]
> På siden **Fejl ved sammenkædet datasynkronisering** vises oplysninger om job, der er relateret til sammenkædede poster. Hvis du løser alle fejl, men posterne stadig ikke synkroniseres, kan der være noget, der skal udføres med en indstilling for integrationen. Normalt skal din administrator løse disse fejltyper.   

> [!VIDEO https://go.microsoft.com/fwlink/?linkid=2098171]

## <a name="to-view-and-resolve-synchronization-errors-for-coupled-records"></a>Sådan vises og løses synkroniseringsfejl for sammenkædede poster
1. Vælg ![elpære-ikonet, der åbner funktionen Fortæl mig](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig"), gå til **Fejl ved sammenkædet datasynkronisering**, og vælg derefter det tilhørende link.
2. På siden **Fejl ved sammenkædet datasynkronisering** vises problemer, der opstod, da du synkroniserede sammenkoblede poster. Følgende tabel indeholder handlinger, som du kan bruge til at løse problemer et efter et:

|Handling|Beskrivelse|
|----|----|
|**Fjern sammenkædning**|Fjerner sammenkædningen af posterne, og de synkroniseres ikke længere. Hvis du vil fortsætte med at synkronisere posterne, skal du sammenkæde dem igen.|
|**Prøv igen**|For hver post, hvor der er fundet en fejl, springes synkroniseringen over, medmindre du løser problemet manuelt. Hvis du prøver igen, medtages posten i næste synkronisering.|
|**Synkroniser**|Appen forsøger at løse en konflikt, hvor en post er ændret i begge forretningsapps. Du kan vælge, hvilken version af posten der skal bruges, i begge apps.|
|**Gendan poster** og **Slet poster**|Disse er nyttige, når en post er blevet slettet i en af appsene. Slet poster sletter posten i den app, hvor den stadig findes. Gendan gendanner posten i den app, hvor den blev slettet.|

## <a name="to-view-the-synchronization-log-for-a-specific-manually-synchronized-record"></a>Sådan får du vist synkroniseringsloggen for en bestemt (manuelt synkroniseret) post
1. Åbn f.eks. en debitor, vare eller en anden post, der synkroniserer data mellem [!INCLUDE[d365fin](includes/d365fin_md.md)] og [!INCLUDE[crm_md](includes/crm_md.md)].
2. Vælg handlingen **Synkroniseringslog** for at få vist synkroniseringsloggen for en valgt post. En bestemt kunde f.eks., som du har synkroniseret manuelt.

## <a name="see-also"></a>Se også  
[Konfigurere brugerkonti til integration med Dynamics 365 Sales](admin-setting-up-integration-with-dynamics-sales.md)  
[Bruge Dynamics 365 Sales fra Business Central](marketing-integrate-dynamicscrm.md)
