---
title: Konfiguration af API-skabeloner | Microsoft Docs
description: Beskriver de trin, du skal udføre for at konfigurere API-skabeloner til Dynamics 365 Business Central.
services: project-madeira
documentationcenter: ''
author: SusanneWindfeldPedersen
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: API templates, configuring templates
ms.date: 04/01/2021
ms.author: solsen
ms.openlocfilehash: fef3b56de7724745dcf8385c0e4665e3e2d4743d
ms.sourcegitcommit: a7cb0be8eae6ece95f5259d7de7a48b385c9cfeb
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 07/08/2021
ms.locfileid: "6443988"
---
# <a name="configuring-api-templates"></a>Konfiguration af API-skabeloner
API-biblioteket til [!INCLUDE[prod_short_md](includes/prod_short.md)] giver en forenklet fremstilling af de underliggende objekter. Det er ikke alle egenskaber i programmet, der vises ved hjælp af den tilknyttede API. På siden **API-opsætning** kan du definere skabeloner, der bruges til at angive tomme egenskaber for en enhed, når du opretter en BOGF-handling via API'et. 

Hvis en konfigurationsskabelon defineres for vareobjektet, når der oprettes en ny post ved hjælp af varer-API'et, bliver egenskaber for den nye vare, der ikke er defineret i API-kaldet, f.eks. udfyldt med oplysninger fra den valgte skabelon. Hvis der f.eks. ikke er angivet en værdi i feltet **Produktbogføringsgruppe** ved hjælp af API'et, men der er angivet en værdi i den valgte skabelon, bliver værdien for bogføringsgruppen i skabelonen anvendt på den nye vare. 

## <a name="setting-up-the-entity-template"></a>Opsætning af enhedsskabelonen
Hvis du vil bruge skabeloner med API-biblioteket, skal du først oprette og definere egenskaber for skabelonerne. Du kan oprette skabelonerne på siden **Konfigurationsskabeloner**. Du kan finde flere oplysninger i [Forberede overflytning af debitordata](admin-use-templates-to-prepare-customer-data-for-migration.md). 

## <a name="assign-the-template-to-an-api"></a>Tildele skabelonen til et API

Hvis du vil tildele en skabelon til en API, skal du udføre følgende trin.

1. Vælg ![Lightbulb, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **API-konfiguration**, og vælg derefter det relaterede link.
2. Vælg **Ny**, og vælg derefter **Rækkefølge**-værdien for posten.  
Hvis der er valgt mere end én skabelon for et API (side-id), anvendes skabelonerne i den rækkefølge, der er defineret i kolonnen **Rækkefølge**.   
Når hver skabelon anvendes, anvendes feltværdier, der er defineret i skabelonen, kun til felter, der ikke allerede har en defineret værdi, enten direkte i API'et eller i en tidligere anvendt skabelon i rækkefølgen. 
3. Vælg en værdi for **Side-id**:  
Dette er siden for det API, som skabelonen skal anvendes på. **Side-ID**-opslaget indeholder en oversigt over alle API'er, der er tilgængelige i biblioteket.
4. Vælg en værdi i feltet **Skabelonkode**.  
Skabelonkoden er koden for den skabelon, der blev defineret på siden **Konfigurationsskabeloner**. De definerede skabelonværdier anvendes på API'et. 
5. I feltet **Betingelser** skal du angive, hvilken skabelon der skal anvendes.  
Den definerede skabelon anvendes på en ny post, der oprettes via API'et, hvis og kun hvis de betingelser, der er defineret i feltet **Betingelser**, opfyldes af de værdier, der allerede er defineret for den nye forekomst af enheden.

## <a name="see-also"></a>Se også
[API-dokumentation](/dynamics-nav/fin-graph)  
[Udvikle Connect-apps til [!INCLUDE[prod_short_md](includes/prod_short.md)]](/dynamics365/business-central/dev-itpro/developer/devenv-develop-connect-apps)  
[Aktivere API'erne](/dynamics-nav/enabling-apis-for-dynamics-nav)  
[Slutpunkter for API'erne](/dynamics-nav/endpoints-apis-for-dynamics)  
[Oprette en virksomhed med RapidStart Services](admin-set-up-a-company-with-rapidstart.md)  
[Opsætning](admin-setup-and-administration.md)

[!INCLUDE[footer-include](includes/footer-banner.md)]