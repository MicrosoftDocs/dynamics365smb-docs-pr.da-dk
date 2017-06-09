---
title: "Fremgangsmåde: Konfigurere salgsprocesser og -procesfaser for leads | Microsoft Docs"
description: Beskriver, hvordan du skal konfigurere salgsprocesser og -faser for leads i Financials
services: project-madeira
documentationcenter: 
author: jswymer
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: relationship, prospect
ms.date: 03/28/2017
ms.author: jswymer
ms.translationtype: Human Translation
ms.sourcegitcommit: a31be0f9d07e2abb591e26f6bae34c6f6e4dcda6
ms.openlocfilehash: 63d3e4689a751e8e56363efcfde1d609762a419e
ms.contentlocale: da-dk
ms.lasthandoff: 05/04/2017


---
# <a name="how-to-set-up-opportunity-sales-cycles-and-cycle-stages"></a>Fremgangsmåde: Konfigurere salgsprocesser og -procesfaser for leads
Før du kan begynde at bruge salgsleads, skal du definere salgsprocesser og salgsprocesfaser. En salgsproces består af en række faser, der går fra den første kontakt til afslutningen af et salg. Hvert trin kan have bestemte krav, der skal opfyldes, f.eks kræve et salgstilbud, før et lead kan gå til næste fase. Du kan også angive, om en fase kan springes over. Du kan definere så mange salgsprocesser, der er behov for, og du kan definere så mange salgsprocesfaser, det er nødvendigt, i en salgsproces.

Implementering salgsprocesser for leads kræver, at du konfigurerer salgsproceskoden, definerer de forskellige faser i processen og derefter tildeler processen til leads.

## <a name="to-set-up-an-opportunity-sales-cycle-code"></a>Sådan defineres en salgsproceskode for leads
1. I øverste højre hjørne skal du vælge ikonet **Søg efter side eller rapport** ![Søg efter side eller rapport](media/ui-search/search_small.png "Ikonet Søg efter side eller rapport"), angive **Salgsprocesser** og derefter vælge det relaterede link. Vinduet **Salgsprocesser** åbnes og viser de eksisterende salgsprocesser.
2. Vælg handlingen **Ny**, og udfyld felterne.

Gentag disse trin for hver salgsproces, du vil oprette. Når du har defineret salgsprocesser for leads, kan du definere de forskellige faser i hver proces.

## <a name="to-define-opportunity-sales-cycle-stages"></a>Sådan defineres salgsprocesfaser for leads
1. I vinduet **Salgsprocesser** skal du vælge den leadsalgsproces, som du vil definere faserne i, og derefter vælge handlingen **Faser**. Vinduet **Salgsprocesfaser** åbnes.
2. Vælg handlingen **Ny** for at oprette en ny fase i salgsprocessen.

Gentag disse trin for hver fase, du vil definere i salgsproces.

## <a name="to-assign-stage-cycle-to-an-opportunity"></a>Sådan tildeles en fase i en salgsproces til et lead
Når du har tilføjet fasen i salgsprocessen for leads, kan du begynde at tilføje salgsprocesser og derefter tildele procesfasen til leads ved at angive feltet **Salgsproceskode**. Du kan finde flere oplysninger under [Fremgangsmåde: Oprette salgsleads](marketing-how-create-opportunities.md).

## <a name="see-also"></a>Se også
[Behandling af salgsleads](marketing-processing-sales-opportunities.md)  
[Salg](sales-manage-sales.md)  
[Arbejde med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

