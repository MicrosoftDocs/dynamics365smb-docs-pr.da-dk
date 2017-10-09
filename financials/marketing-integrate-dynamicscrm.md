---
title: "Administrere kunder ved hjælp af Dynamics 365 for Sales | Microsoft Docs"
description: "Du kan bruge Dynamics 365 for Sales fra Dynamics 365 for Financials til at tilknytte data og få gnidningsløs integration og synkronisering i lead-til-kontant-processen."
documentationcenter: 
author: edupont04
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: integration, synchronize, map
ms.date: 06/06/2017
ms.author: edupont
ms.translationtype: HT
ms.sourcegitcommit: 2c13559bb3dc44cdb61697f5135c5b931e34d2a8
ms.openlocfilehash: bc0b9c8141c6c2eac78abc9cd3f5c89af3c89fbb
ms.contentlocale: da-dk
ms.lasthandoff: 09/22/2017

---
# <a name="managing-your-customer-relationships-using-dynamics-365-for-sales-from-inside-dynamics-365-for-financials"></a>Administrere kunderelationer med Dynamics 365 for Sales fra Dynamics 365 for Financials
Hvis du bruger Dynamics 365 for Sales til kundeengagementer, kan du bruge [!INCLUDE[d365fin](includes/d365fin_md.md)] til ordrebehandling og økonomi og få problemfri integration i lead-til-kontant-processen.

Når programmet er indstillet til integration med Dynamics 365 for Sales, har du adgang til Sales-data fra [!INCLUDE[d365fin](includes/d365fin_md.md)] og omvendt i nogle tilfælde. Integrationen gør det muligt at arbejde med og synkronisere datatyper, der er fælles for begge tjenester, f.eks. debitorer, kontakter og salgsoplysninger, og holde dataene opdaterede på begge lokationer.  

For eksempel kan sælgeren i Dynamics 365 for Sales bruge prislisterne fra [!INCLUDE[d365fin](includes/d365fin_md.md)], når vedkommende opretter en salgsordre. Når sælgeren føjer varen til salgsordrelinjen i Dynamics 365 for Sales, kan han eller hun også få vist lagerniveauet (disponering) af varen fra [!INCLUDE[d365fin](includes/d365fin_md.md)]. Disse data publiceres som en del af den assisterende opsætningsvejledning **Konfiguration af Dynamics 365-forbindelse**.  

> [!NOTE]  
>   Denne funktion kræver, at oplevelsen er indstillet til **Suite**. Du kan finde flere oplysninger under [Tilpasse din [!INCLUDE[d365fin](includes/d365fin_md.md)]-oplevelse](ui-experiences.md).  

## <a name="setting-up-the-connection"></a>Indstilling af forbindelsen
Fra startsiden kan du åbne opsætningsvejledningen **Konfiguration af Dynamics 365-forbindelse**, der hjælper dig med at oprette forbindelsen. Når det er gjort, får du en problemfri sammenkædning af Dynamics 365 for Sales-poster og [!INCLUDE[d365fin](includes/d365fin_md.md)]-poster.  

> [!NOTE]  
>   I det følgende forklares den assisterende opsætning, men du kan udføre de samme opgaver manuelt i vinduet **Konfiguration af Dynamics 365-forbindelse**.

I den assisterende opsætningsvejledning kan du vælge, hvilke data der skal synkroniseres mellem de to tjenester. Du kan også angive, at du vil importere din eksisterende Dynamics 365 for Sales-løsning. Hvis du vil det, skal du angive en administratorbrugerkonto.

### <a name="setting-up-the-user-account-for-importing-the-solution"></a>Konfigurere brugerkontoen til import af løsningen
Når du vil importere en eksisterende Dynamics 365 for Sales-løsning, bruger opsætningsvejledningen en administratorkonto. Denne konto skal være en gyldig bruger i Dynamics 365 for Sales med følgende sikkerhedsroller:

* Systemadministrator  
* Løsningsoptimerer  

Du kan finde flere oplysninger under [Oprette brugere og tildele Microsoft Dynamics 365 (online) sikkerhedsroller](https://technet.microsoft.com/library/jj191623.aspx) på TechNet og [Fremgangsmåde: Administrere brugere og tilladelser](ui-how-users-permissions.md).  

Denne konto bruges kun under opsætningen. Når løsningen indlæses i [!INCLUDE[d365fin](includes/d365fin_md.md)], er kontoen ikke længere nødvendig.

### <a name="setting-up-the-user-account-for-synchronization"></a>Konfigurere brugerkontoen til synkronisering
Integration er baseret på en delt brugerkonto. Derfor skal du i dit Office 365-abonnement oprette en dedikeret bruger, der skal bruges til synkronisering mellem de to tjenester. Denne konto skal allerede være en gyldig bruger i Dynamics 365 for Sales, men du behøver ikke at tildele sikkerhedsroller til kontoen, da opsætningsvejledningen gør det for dig. Du skal angive denne brugerkonto en eller flere gange i opsætningsvejledningen, afhængigt af den grad af synkronisering du ønsker. Du kan finde flere oplysninger under [Oprette brugere og tildele Microsoft Dynamics 365 (online) sikkerhedsroller](https://technet.microsoft.com/library/jj191623.aspx) på TechNet.

Hvis du vælger at aktivere *varetilgængelighed*, skal integrationsbrugerkontoen have en adgangsnøgle til webtjenesten. Dette foregår i to trin. På siden [!INCLUDE[d365fin](includes/d365fin_md.md)] for brugerkontoen skal du vælge knappen **Ændr webtjenestenøgle**, og i opsætningsvejledningen til Dynamics 365-forbindelsen skal du angive denne bruger som brugeren af OData-webtjenesten.

Hvis du vælger at aktivere *integration af salgsordre*, skal du angive en bruger, der kan håndtere denne synkronisering - integrationsbrugeren eller en anden brugerkonto.

### <a name="coupling-records"></a>Sammenkæde poster
I den assisterende opsætningsvejledning kan du vælge at synkronisere mellem de to tjenester. Men senere kan du også indstille synkroniseringen af bestemte typer data. Dette kaldes *sammenkædning*, og dette afsnit indeholder anbefalinger for, hvad du skal tage hensyn til.

Hvis du f.eks. vil have vist Dynamics 365 for Sales-konti som debitorer i [!INCLUDE[d365fin](includes/d365fin_md.md)], skal du sammenkæde de to typer poster. Det er ikke særlig vanskeligt - du skal åbne vinduet **Debitoroversigt** i [!INCLUDE[d365fin](includes/d365fin_md.md)], hvor der er en handling på båndet til sammenkædning af disse data med Dynamics 365 for Sales. Derefter skal du angive, hvilke [!INCLUDE[d365fin](includes/d365fin_md.md)]-kunder der svarer til hvilke konti i Dynamics 365 for Sales.

I visse områder kræver funktionaliteten, at du sammenkæder bestemte datasæt før andre datasæt som vist i følgende liste:

* Debitorer og konti  
  * Sammenkæd først sælgere med Dynamics 365 for Sales-brugere  
* Varer og ressourcer  
  * Sammenkæd først enheder med Dynamics 365 for Sales-enhedsgrupper  
* Priser på varer og ressourcer  
  * Sammenkæd først debitorprisgrupper med Dynamics 365 for Sales-priser  

> [!NOTE]  
>   Hvis du bruger priser i udenlandsk valuta, skal du sørge for at sammenkæde valutaer med Dynamics 365 for Sales-transaktionsvalutaer.

Dynamics 365 for Sales-salgsordrer afhænger af ekstra oplysninger, f.eks. kunder, enheder, valutaer, debitorprisgrupper, varer og/eller ressourcer. Hvis Dynamics 365 for Sales-salgsordrer skal fungere uden problemer, skal du skal sammenkæde kunder, enheder, valutaer, debitorprisgrupper, varer og/eller ressourcer først.

### <a name="synchronizing-records-fully"></a>Fuld synkronisering af poster
I slutningen af den assisterede opsætningsvejledning kan du vælge handlingen **Kør fuld synkronisering** for at starte synkronisering af alle [!INCLUDE[d365fin](includes/d365fin_md.md)]-poster med alle relaterede poster i den tilknyttede Dynamics 365 for Sales-løsning. I vinduet **Fuld CRM-synkroniseringsgennemgang** skal du vælge handlingen **Start**. Synkroniseringen begynder derefter at udføre opgaver i overensstemmelse med afhængigheder. For eksempel synkroniseres valutaposter før debitorposter. Fuld synkronisering kan tage lang tid og køres derfor i baggrunden, så du kan fortsætte med at arbejde i [!INCLUDE[d365fin](includes/d365fin_md.md)].

For at kontrollere status for individuelle job i en fuldstændig synkronisering skal du fokusere på felterne **Status for opgavekøpost**, **Status for til int. tabel-job** eller **Status for fra int. tabel-job** i vinduet **Fuld CRM-synkroniseringsgennemgang**.

Fra vinduet **Konfiguration af Dynamics 365-forbindelse** kan du få oplysninger om fuld synkronisering, når som helst. Her kan du også åbne vinduet **Integrationstabelkoblinger** for at få vist detaljer om tabellerne i Financials og Dynamics 365 for Sales-løsningen, som skal synkroniseres.

## <a name="see-also"></a>Se også
[Relationsstyring](marketing-relationship-management.md)  
[Arbejde med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)  
[Tilpasse din [!INCLUDE[d365fin](includes/d365fin_md.md)]-oplevelse](ui-experiences.md)  
[Fremgangsmåde: Administrere brugere og rettigheder](ui-how-users-permissions.md)    
[Onboarding af din organisation og dine brugerne i Dynamics 365 (online)](https://www.microsoft.com/en-US/Dynamics/crm-customer-center/onboard-your-organization-and-users-to-dynamics-365-online.aspx)  

## [!INCLUDE[d365fin](includes/free_trial_md.md)]

