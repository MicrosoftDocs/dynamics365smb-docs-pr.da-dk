---
title: Konfigurere salgsprocesser og -procesfaser for leads | Microsoft Docs
description: Beskriver, hvordan du definerer salgsfaser fra første kontakt til afslutningen for at oprette en salgsproces og tildele den til leads i Business Central.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: relationship, prospect
ms.date: 04/01/2019
ms.author: jswymer
ms.openlocfilehash: 0ed3ae09c42cad7978bc00bf04b6065909e2fd98
ms.sourcegitcommit: 60b87e5eb32bb408dd65b9855c29159b1dfbfca8
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 04/29/2019
ms.locfileid: "1239977"
---
# <a name="set-up-opportunity-sales-cycles-and-cycle-stages"></a>Konfigurere salgsprocesser og -procesfaser for leads
Før du kan begynde at bruge salgsleads, skal du definere salgsprocesser og salgsprocesfaser. En salgsproces består af en række faser, der går fra den første kontakt til afslutningen af et salg. Hvert trin kan have bestemte krav, der skal opfyldes, f.eks kræve et salgstilbud, før et lead kan gå til næste fase. Du kan også angive, om en fase kan springes over. Du kan definere så mange salgsprocesser, der er behov for, og du kan definere så mange salgsprocesfaser, det er nødvendigt, i en salgsproces.

Implementering af salgsprocesser for leads kræver, at du konfigurerer salgsprocessen, definerer de forskellige faser i processen og derefter tildeler processen til leads. Tildeling af den pågældende aktivitet eller opgaver til et lead kan være en del af oprettelsen af en salgsproces.

I dette emne beskrives også opsætning af opgaver og aktiviteter, og hvordan du kan tildele opgaver til aktiviteter. Du kan finde flere oplysninger i afsnittet [Sådan oprettes aktiviteter til opgaver](marketing-how-setup-opportunity-sales-cycles-stages.md#to-set-up-activities-with-tasks).

## <a name="to-set-up-opportunity-sales-cycle-codes"></a>Sådan oprettes salgsproceskoder for leads
1. Vælg ikonet ![Elpære, der åbner funktionen Fortæl mig](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig"), angiv **Salgsproces**, og vælg derefter det relaterede link. Siden **Salgsprocesser** åbnes og viser de eksisterende salgsprocesser.
2. Vælg handlingen **Ny**, og udfyld felterne efter behov. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

Gentag disse trin for hver salgsproces, du vil oprette. Når du har defineret salgsprocesser for leads, kan du definere de forskellige faser i hver proces.

## <a name="to-define-opportunity-sales-cycle-stages"></a>Sådan defineres salgsprocesfaser for leads
1. På siden **Salgsprocesser** skal du vælge den leadsalgsproces, som du vil definere faserne i, og derefter vælge handlingen **Faser**. Siden **Salgsprocesfaser** åbnes.
2. Vælg handlingen **Ny** for at oprette en ny fase i salgsprocessen.

Gentag disse trin for hver fase, du vil definere i salgsproces.

## <a name="to-assign-stage-cycles-to-opportunities"></a>Sådan tildeles faser i salgsprocesser til leads
Når du har tilføjet fasen i salgsprocessen for leads, kan du begynde at tilføje salgsprocesser og derefter tildele procesfasen til leads ved at angive feltet **Salgsproceskode**. Du kan finde flere oplysninger under [Oprette salgsleads](marketing-how-create-opportunities.md).

## <a name="to-set-up-activities-with-tasks"></a>Sådan defineres aktiviteter til opgaver
Du kan samle flere opgaver, for eksempel opgaver, der hver repræsenterer et trin, i aktiviteter. Aktivitetsopgaver er forbundet med hinanden vha. en datoformel. Du kan tildele aktiviteter til leads, sælgere og kontaktpersoner.

1. Vælg ikonet ![Elpære, der åbner funktionen Fortæl mig](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig"), angiv **Aktiviteter**, og vælg derefter det relaterede link.
2. Vælg handlingen **Ny**, og udfyld felterne efter behov.
3. I oversigtspanelet **Linjer** skal du udfylde felterne efter behov for at definere en eller flere opgaver i aktiviteten.

## <a name="to-assign-tasks-or-activities-of-tasks-to-opportunities"></a>Sådan tildeles opgaver eller aktiviteter til leads
Når du har oprettet en opgave, kan du tildele den til et salgslead og dermed tildele aktiviteten, som opgaven tilhører.

> [!NOTE]  
>   Nedenfor beskrives, hvordan aktivitetsopgaver tildeles til leads. Trinene er de samme, når du tildeler opgaver til sælgere og kontaktpersoner.

1. Vælg ikonet ![Elpære, der åbner funktionen Fortæl mig](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig"), angiv **Salgsmuligheder**, og vælg derefter det relaterede link.
2. Vælg et lead, og vælg derefter handlingen **Opgaver**.
3. Vælg handlingen **Opret opgave** på siden **Opgaveliste**.
4.  På siden **Opret opgave** skal du udfylde felterne efter behov.

    Bemærk, at i feltet **Lead** tildeles det automatisk til det pågældende lead.
5. Vælg knappen **OK**.
6. På siden **Opgaveliste** skal du vælge den nye opgave og derefter vælge handlingen **Tildel aktiviteter**.
7. På siden **Tildel aktivitet** skal du udfylde felterne efter behov, og derefter vælge knappen **OK**.

## <a name="see-also"></a>Se også
[Behandling af salgsleads](marketing-processing-sales-opportunities.md)  
[Salg](sales-manage-sales.md)  
[Arbejde med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)
