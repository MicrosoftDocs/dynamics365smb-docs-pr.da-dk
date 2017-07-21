---
title: GIFI-koder i Canada | Microsoft Docs
Description: "I Canada kan du oprette GIFI-koder (General Index of Financial Information) og knytte dem til bogføringskonti"
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: local
ms.date: 06/02/2017
ms.author: SorenGP
ms.translationtype: Human Translation
ms.sourcegitcommit: 81636fc2e661bd9b07c54da1cd5d0d27e30d01a2
ms.openlocfilehash: d5211f5c8265e572ff1d1a809b1046ce89f8c1e6
ms.contentlocale: da-dk
ms.lasthandoff: 07/07/2017


---
# <a name="how-to-work-with-gifi-codes-in-canada"></a>Fremgangsmåde: Arbejde med GIFI-koder i Canada
Finansielle oplysninger kan omfatte finanskonti, rapporter, resultatopgørelsen, balancen og opgørelse af overført resultat. Finansielle oplysninger klassificeres ved hjælp af koder. Brug af koder hjælper myndighederne med at behandle oplysninger, forberede elektronisk arkivering og validere skatteoplysningerne elektronisk. Brug af koder kan også hjælpe statistiske organisationer til at arbejde mere effektivt, fordi finansielle oplysninger er mere tilgængelige. Du kan finde flere oplysninger under [Webstedet Canada Revenue Agency](http://www.cra-arc.gc.ca/).

Canada Revenue Agency bruger GIFI-koder (General Index of Financial Information) til at indsamle, validere og behandle finansielle data og momsoplysninger elektronisk. Det er bedst kun at tildele GIFI-koder til bogføringskonti, så alle sammentællinger udføres af dit skattebehandlingsprogram.

Hvis en konto er knyttet til en GIFI-kode, rapporteres det til skattemyndighederne under denne kode. Flere konti kan have den samme GIFI-kode, men hver konto kan kun have én GIFI-kode.

Du kan eksportere saldooplysninger ved hjælp af GIFI-kode og gemme den eksporterede fil i Excel, som med fordel kan bruges til at overføre oplysninger til dit skattebehandlingsprogram.

## <a name="to-set-up-gifi-codes"></a>Sådan defineres GIFI-koder
I Dynamics NAV skal du angive GIFI-koder for finanskonti, rapporter, balancer, indtægtsopgørelser og opgørelser over overførte resultater.

1. Vælg ikonet ![Søg efter side eller rapport](media/ui-search/search_small.png "Ikonet Søg efter side eller rapport"), angiv **GIFI-koder**, og vælg derefter det relaterede link.
2. I vinduet **GIFI-koder** skal du vælge handlingen **Ny**.
3. Opret GIFI-koder ved at udfylde felterne. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

## <a name="to-associate-gifi-codes-with-gl-accounts"></a>Sådan knyttes GIFI-koder til finanskonti
Hvis du vil rapportere finansielle oplysninger via GIFI-kode, skal hver GIFI-kode være knyttet til de relevante konti i kontoplanen.

1. Vælg ikonet ![Søg efter side eller rapport](media/ui-search/search_small.png "Ikonet Søg efter side eller rapport"), angiv **Kontoplan**, og vælg derefter det relaterede link.
2. Vælg en relevant finanskonto, og vælg derefter handlingen **Rediger**.
3. I oversigtspanelet **Omkostningsregnskab** skal du i feltet **GIFI-kode** vælge den relevante GIFI-kode.

## <a name="to-view-account-balances-using-the-gifi-code-report"></a>Sådan vises kontosaldi ved hjælp af GIFI-koderapporten
Du kan gennemse dine kontosaldi via GIFI-kode ved hjælp af rapporten **Kontosaldi efter GIFI-kode**.

1. Vælg ikonet ![Søg efter side eller rapport](media/ui-search/search_small.png "Ikonet Søg efter side eller rapport"), angiv **GIFI-koder**, og vælg derefter det relaterede link.
2. Angiv, hvad der skal medtages i rapporten, ved at udfylde felterne. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
3. Vælg **Udskriv** eller **Vis udskrift**.

## <a name="to-export-balance-information-using-gifi-codes"></a>Sådan udlæses saldooplysninger med GIFI-koder
Du kan eksportere saldooplysninger ved hjælp af GIFI-koder og gemme den eksporterede fil i Excel. Du kan ændre, gemme eller slette filen. Filen kan bruge filen til at overføre oplysninger til dit skattebehandlingsprogram.

1. Vælg ikonet ![Søg efter side eller rapport](media/ui-search/search_small.png "Ikonet Søg efter side eller rapport"), angiv **GIFI-koder**, og vælg derefter det relaterede link.
2. Angiv, hvad der skal udlæses til Excel, ved at udfylde felterne. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
3. Vælg knappen **OK**.

> [!NOTE]  
>   Excel-filen har følgende egenskaber:

* Saldoen afrundes til nærmeste procent, men celleværdien vedligeholder samme procentsats som i finansbogholderiet.
* Negative tal vises som positive tal i parentes. Derfor repræsenteres -123 som (123).

## <a name="see-also"></a>Se også
[Finans](finance.md)   
[Konfigurere Finans](finance-setup-finance.md)

