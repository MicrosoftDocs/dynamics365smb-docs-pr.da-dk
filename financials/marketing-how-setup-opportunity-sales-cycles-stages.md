---
title: Konfigurere salgsprocesser og -procesfaser for leads | Microsoft Docs
description: "Beskriver, hvordan du definerer salgsfaser fra første kontakt til afslutningen for at oprette en salgsproces og tildele den til leads i Financials."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: relationship, prospect
ms.date: 06/06/2017
ms.author: jswymer
ms.translationtype: HT
ms.sourcegitcommit: 81636fc2e661bd9b07c54da1cd5d0d27e30d01a2
ms.openlocfilehash: 29f9caa8f01fe8e4cfd0f65cc290d82a49fb36bb
ms.contentlocale: da-dk
ms.lasthandoff: 09/22/2017

---
# <a name="how-to-set-up-opportunity-sales-cycles-and-cycle-stages"></a>Fremgangsmåde: Konfigurere salgsprocesser og -procesfaser for leads
Før du kan begynde at bruge salgsleads, skal du definere salgsprocesser og salgsprocesfaser. En salgsproces består af en række faser, der går fra den første kontakt til afslutningen af et salg. Hvert trin kan have bestemte krav, der skal opfyldes, f.eks kræve et salgstilbud, før et lead kan gå til næste fase. Du kan også angive, om en fase kan springes over. Du kan definere så mange salgsprocesser, der er behov for, og du kan definere så mange salgsprocesfaser, det er nødvendigt, i en salgsproces.

Implementering af salgsprocesser for leads kræver, at du konfigurerer salgsprocessen, definerer de forskellige faser i processen og derefter tildeler processen til leads. Tildeling af den pågældende aktivitet eller opgaver til et lead kan være en del af oprettelsen af en salgsproces.

I dette emne beskrives også opsætning af opgaver og aktiviteter, og hvordan du kan tildele opgaver til aktiviteter. Du kan finde flere oplysninger i afsnittet "Sådan oprettes aktiviteter til opgaver".

## <a name="to-set-up-opportunity-sales-cycle-codes"></a>Sådan oprettes salgsproceskoder for leads
1. Vælg ikonet ![Søg efter side eller rapport](media/ui-search/search_small.png "Ikonet Søg efter side eller rapport"), angiv **Salgsprocesser**, og vælg derefter det relaterede link. Vinduet **Salgsprocesser** åbnes og viser de eksisterende salgsprocesser.
2. Vælg handlingen **Ny**, og udfyld felterne efter behov. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

Gentag disse trin for hver salgsproces, du vil oprette. Når du har defineret salgsprocesser for leads, kan du definere de forskellige faser i hver proces.

## <a name="to-define-opportunity-sales-cycle-stages"></a>Sådan defineres salgsprocesfaser for leads
1. I vinduet **Salgsprocesser** skal du vælge den leadsalgsproces, som du vil definere faserne i, og derefter vælge handlingen **Faser**. Vinduet **Salgsprocesfaser** åbnes.
2. Vælg handlingen **Ny** for at oprette en ny fase i salgsprocessen.

Gentag disse trin for hver fase, du vil definere i salgsproces.

## <a name="to-assign-stage-cycles-to-opportunities"></a>Sådan tildeles faser i salgsprocesser til leads
Når du har tilføjet fasen i salgsprocessen for leads, kan du begynde at tilføje salgsprocesser og derefter tildele procesfasen til leads ved at angive feltet **Salgsproceskode**. Du kan finde flere oplysninger under [Fremgangsmåde: Oprette salgsleads](marketing-how-create-opportunities.md).

## <a name="to-set-up-activities-with-tasks"></a>Sådan defineres aktiviteter til opgaver
Du kan samle flere opgaver, for eksempel opgaver, der hver repræsenterer et trin, i aktiviteter. Aktivitetsopgaver er forbundet med hinanden vha. en datoformel. Du kan tildele aktiviteter til leads, sælgere og kontaktpersoner.

1. Vælg ikonet ![Søg efter side eller rapport](media/ui-search/search_small.png "Ikonet Søg efter side eller rapport"), angiv **Aktiviteter**, og vælg derefter det relaterede link.
2. Vælg handlingen **Ny**, og udfyld felterne efter behov.
3. I oversigtspanelet **Linjer** skal du udfylde felterne efter behov for at definere en eller flere opgaver i aktiviteten.

## <a name="to-assign-tasks-or-activities-of-tasks-to-opportunities"></a>Sådan tildeles opgaver eller aktiviteter til leads
Når du har oprettet en opgave, kan du tildele den til et salgslead og dermed tildele aktiviteten, som opgaven tilhører.

> [!NOTE]  
>   Nedenfor beskrives, hvordan aktivitetsopgaver tildeles til leads. Trinene er de samme, når du tildeler opgaver til sælgere og kontaktpersoner.

1. Vælg ikonet ![Søg efter side eller rapport](media/ui-search/search_small.png "Ikonet Søg efter side eller rapport"), angiv **Leads**, og vælg derefter det relaterede link.
2. Vælg et lead, og vælg derefter handlingen **Opgaver**.
3. Vælg handlingen **Opret opgave** i vinduet **Opgaveliste**.
4.  I vinduet **Opret opgave** skal du udfylde felterne efter behov.

    Bemærk, at i feltet **Lead** tildeles det automatisk til det pågældende lead.
5. Vælg knappen **OK**.
6. I vinduet **Opgaveliste** skal du vælge den nye opgave og derefter vælge handlingen **Tildel aktiviteter**.
7. I vinduet **Tildel aktivitet** skal du udfylde felterne efter behov, og derefter vælge knappen **OK**.

## <a name="see-also"></a>Se også
[Behandling af salgsleads](marketing-processing-sales-opportunities.md)  
[Salg](sales-manage-sales.md)  
[Arbejde med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

