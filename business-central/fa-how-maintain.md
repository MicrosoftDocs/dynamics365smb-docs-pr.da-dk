---
title: "Vedligeholde anlægsaktiver | Microsoft Docs"
description: "Du registrerer løbende vedligeholdelsesarbejde af reparationer og service på et anlægsaktiv."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: repair, service
ms.date: 10/01/2018
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 9dbd92409ba02281f008246194f3ce0c53e4e001
ms.openlocfilehash: b3bf2590b60081ab954ac4918a65853da32d38e0
ms.contentlocale: da-dk
ms.lasthandoff: 09/28/2018

---
# <a name="maintain-fixed-assets"></a>Vedligeholde anlægsaktiver
Reparationsudgifter er periodisk forekommende rutineomkostninger, der afholdes for at bevare anlægsaktivernes værdi. I modsætning til kapitalforbedringer forøges deres værdi ikke.

Du kan registrere og vedligeholde en opdateret fil om anlægsreparation og -service, så du har en nemt tilgængelig og fuldstændig fortegnelse over reparation af et anlæg. Hver gang et anlægsaktiv bliver sendt til service, registrerer du alle relevante oplysninger som f.eks. dato, kreditornummer og reparatørens telefonnummer. Der bliver foretaget reparationsregistrering for hvert enkelt anlægsaktiv fra anlægskortet.

Indeksering anvendes til at justere for ændringer af det generelle prisniveau. Kørslen **Indeksér anlæg** kan bruges til at genberegne reparationsomkostningerne.

## <a name="to-record-maintenance-work-on-a-fixed-asset"></a>Sådan registreres reparationsarbejde på et anlægsaktiv
Hver gang der er udført reparationsopgaver, f.eks. et servicebesøg, kan du registrere det for det pågældende anlægsaktiv i vinduet **Reparationsregistreringer**.  

1. Vælg ikonet ![Elpære, der åbner funktionen Fortæl mig](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig"), angiv **Anlægsaktiver**, og vælg derefter det relaterede link.  
2. Vælg det anlægsaktiv, du vil registrere vedligeholdelse for, og vælg derefter handlingen **Reparationsregistrering**.
3. I vinduet **Reparationsregistrering** skal du udfylde felterne efter behov. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]  

## <a name="to-post-maintenance-costs-from-a-fixed-asset-gl-journal"></a>Sådan bogføres reparationsomkostninger fra en anlægskassekladde
1. Vælg ikonet ![Elpære, der åbner funktionen Fortæl mig](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig"), angiv **Afskrivningsprofiloversigt**, og vælg derefter det relaterede link.  
2. Vælg den afskrivningsprofil, der er tildelt anlægsaktivet, og vælg derefter handlingen **Rediger**.
3. I vinduet **Afskrivningsprofilkort** skal du kontrollere, at afkrydsningsfeltet **Vedligeholdese** ikke er markeret. Dette sikrer, at vedlligeholdelsesomkostninger ikke bogføres i finansregnskabet.
4. Vælg ikonet ![Elpære, der åbner funktionen Fortæl mig](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig"), angiv **Anlægsfinanskladder**, og vælg derefter det relaterede link.  
5. Opret en første kladdelinje, og udfyld felterne efter behov.
6. I feltet **Anlægsbogføringstype** skal du vælge **Reparation**.
7. Vælg handlingen **Indsæt anlægsmodkonto**. Der oprettes en anden kladdelinje til den modkonto, der er oprettet til bogføring af vedligeholdelse.

    > [!NOTE]  
    >   Trin 7 fungerer kun, hvis du har angivet følgende: I vinduet **Anlægsbogføringsgruppekort** for bogføringsgruppen for anlægsaktivet indeholder feltet **Reparationskonto** finansdebetkontoen og feltet **Reparationsmodkonto** indeholder den finanskonto, hvor du vil bogføre modposter for opskrivning. Du kan finde flere oplysninger i afsnittet "Sådan oprettes anlægsbogføringsgrupper" i [Angive generelle oplysninger om anlægsaktiver](fa-how-setup-general.md).
8. Vælg handlingen **Bogfør**.

## <a name="to-follow-up-on-fixed-assets-service-visits"></a>Sådan følger du op på servicebesøg på anlæg
Du kan udskrive rapporten **Reparation - næste service** for at se, hvilke anlæg der er planlagt servicebesøg for. Du kan også bruge denne rapport, når du opdaterer feltet **Næste servicedato** på anlægskort.  

1. Vælg ikonet ![Elpære, der åbner funktionen Fortæl mig](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig"), angiv **Reparation - næste service**, og vælg derefter det relaterede link.  
2. Udfyld felterne **Startdato** og **Slutdato**  
3. Vælg knappen **Udskriv** eller **Vis udskrift**.

## <a name="to-monitor-maintenance-costs"></a>Sådan overvåges reparationsomkostningerne
Du kan se reparationsomkostningerne i statistikken for et anlægsaktiv.  

1. Vælg ikonet ![Elpære, der åbner funktionen Fortæl mig](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig"), angiv **Anlægsaktiver**, og vælg derefter det relaterede link.
2. Vælg det anlægsaktiv, du vil have vist reparationsomkostninger for, og vælg derefter handlingen **Afskrivningsprofiler**.
3. I vinduet **Anlægsafskrivningsprofiler** skal du vælge den relevante anlægsafskrivningsprofil og derefter vælge handlingen **Statistik**.
4. I vinduet **Anlægsstatistik** skal du vælge feltet **Reparation**.

Vinduet **Reparationsposter** åbnes med de poster, som indgår i beløbet i feltet **Reparation**.

## <a name="to-view-or-print-maintenance-costs-for-multiple-fixed-assets"></a>Sådan får du vist eller udskriver reparationsomkostninger for flere anlægsaktiver
I rapporten **Reparation - analyse** kan du vælge, om du vil have vist vedligeholdelse ud fra en, to eller tre reparationskoder på en bestemt dato eller i en bestemt periode. Du kan se totalen for alle valgte aktiver eller totalen for hvert enkelt aktiv.

1. Vælg ikonet ![Elpære, der åbner funktionen Fortæl mig](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig"), angiv **Reparationsanalyse**, og vælg derefter det relaterede link.
2. Udfyld felterne efter behov.
3. Vælg knappen **Udskriv** eller **Vis udskrift**.

## <a name="to-view-maintenance-ledger-entries"></a>Sådan får du vist reparationsposter
Du kan også undersøge reparationsomkostningerne ved at se på reparationsposterne.  

1. Vælg ikonet ![Elpære, der åbner funktionen Fortæl mig](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig"), angiv **Anlægsaktiver**, og vælg derefter det relaterede link.
2. Vælg det anlægsaktiv, du vil have vist poster for, og vælg derefter handlingen **Afskrivningsprofiler**.
3. I vinduet **Anlægsafskrivningsprofiler** skal du vælge den relevante anlægsafskrivningsprofil og derefter vælge handlingen **Reparationsposter**.

## <a name="to-view-or-print-maintenance-ledger-entries-for-multiple-fixed-assets"></a>Sådan får du vist eller udskriver reparationsposter for flere anlægsaktiver
I feltet **Reparationsposter** kan du få vist eller udskrive reparationsposter for et eller flere anlægsaktiver.  

1. Vælg ikonet ![Elpære, der åbner funktionen Fortæl mig](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig"), angiv **Reparationsposter**, og vælg derefter det relaterede link.
2. Udfyld felterne efter behov.
3. Vælg knappen **Udskriv** eller **Vis udskrift**.

## <a name="see-also"></a>Se også
[Anlægsaktiver](fa-manage.md)  
[Opsætning af anlægsaktiver](fa-setup.md)  
[Finans](finance.md)  
[Introduktion](product-get-started.md)  
[Arbejde med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

