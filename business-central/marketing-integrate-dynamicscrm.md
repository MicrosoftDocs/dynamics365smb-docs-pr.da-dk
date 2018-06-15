---
title: "Administrere kunder ved hjælp af Dynamics 365 for Sales | Microsoft Docs"
description: "Du kan bruge Dynamics 365 for Sales fra Business Central til at tilknytte data og få gnidningsløs integration og synkronisering i lead-til-kontant-processen."
documentationcenter: 
author: edupont04
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: integration, synchronize, map
ms.date: 05/24/2018
ms.author: edupont
ms.translationtype: HT
ms.sourcegitcommit: 4fceff1a6cf728608a49182a9704f187d31767fe
ms.openlocfilehash: f9ac1c1e1a9f4ca043ddd87c98c8014ca96d8c87
ms.contentlocale: da-dk
ms.lasthandoff: 05/28/2018

---
# <a name="managing-customers-and-sales-created-in-dynamics-365-for-sales"></a>Administration af kunder og salg, der er oprettet i Dynamics 365 for Sales
Hvis du bruger Dynamics 365 for Sales til kundeengagementer, kan du bruge [!INCLUDE[d365fin](includes/d365fin_md.md)] til ordrebehandling og økonomi og få problemfri integration i lead-til-kontant-processen.

Når programmet er indstillet til integration med Dynamics 365 for Sales, har du adgang til Sales-data fra [!INCLUDE[d365fin](includes/d365fin_md.md)] og omvendt i nogle tilfælde. Integrationen gør det muligt at arbejde med og synkronisere datatyper, der er fælles for begge tjenester, f.eks. debitorer, kontakter og salgsoplysninger, og holde dataene opdaterede på begge lokationer.  

For eksempel kan sælgeren i Dynamics 365 for Sales bruge prislisterne fra [!INCLUDE[d365fin](includes/d365fin_md.md)], når vedkommende opretter en salgsordre. Når sælgeren føjer varen til salgsordrelinjen i Dynamics 365 for Sales, kan han eller hun også få vist lagerniveauet (disponering) af varen fra [!INCLUDE[d365fin](includes/d365fin_md.md)].

Omvendet kan ordrebehandlere i [!INCLUDE[d365fin](includes/d365fin_md.md)] håndtere særlige karakteristika for salgsordrer, der overføres automatisk eller manuelt fra Dynamics 365 For Sales, f.eks. automatisk oprette og bogføre gyldige salgsordrelinjer for varer eller ressourcer, der blev angivet i Salg som rekvirerede produkter. Du kan finde flere oplysninger i afsnittet "Håndtering af særlige salgsordredata".  

## <a name="setting-up-the-connection"></a>Indstilling af forbindelsen
Fra startsiden kan du åbne opsætningsvejledningen **Konfiguration af Microsoft Dynamics 365-forbindelse**, der hjælper dig med at oprette forbindelsen. Når det er gjort, får du en problemfri sammenkædning af Dynamics 365 for Sales-poster og [!INCLUDE[d365fin](includes/d365fin_md.md)]-poster.  

> [!NOTE]  
>   I det følgende forklares den assisterende opsætning, men du kan udføre de samme opgaver manuelt i vinduet **Konfiguration af Dynamics 365 for Sales-forbindelse**.

I den assisterende opsætningsvejledning kan du vælge, hvilke data der skal synkroniseres mellem de to tjenester. Du kan også angive, at du vil importere din eksisterende Dynamics 365 for Sales-løsning. Hvis du vil det, skal du angive en administratorbrugerkonto.

### <a name="setting-up-the-user-account-for-importing-the-solution"></a>Konfigurere brugerkontoen til import af løsningen
Når du vil importere en eksisterende Dynamics 365 for Sales-løsning, bruger opsætningsvejledningen en administratorkonto. Denne konto skal være en gyldig bruger i Dynamics 365 for Sales med følgende sikkerhedsroller:

* Systemadministrator  
* Løsningsoptimerer  

Du kan finde flere oplysninger under [Oprette brugere i Microsoft Dynamics 365 (online) og tildele sikkerhedsroller](/dynamics365/customer-engagement/admin/create-users-assign-online-security-roles) og [Administrere brugere og tilladelser](ui-how-users-permissions.md).  

Denne konto bruges kun under opsætningen. Når løsningen indlæses i [!INCLUDE[d365fin](includes/d365fin_md.md)], er kontoen ikke længere nødvendig.

### <a name="setting-up-the-user-account-for-synchronization"></a>Konfigurere brugerkontoen til synkronisering
Integration er baseret på en delt brugerkonto. Derfor skal du i dit Office 365-abonnement oprette en dedikeret bruger, der skal bruges til synkronisering mellem de to tjenester. Denne konto skal allerede være en gyldig bruger i Dynamics 365 for Sales, men du behøver ikke at tildele sikkerhedsroller til kontoen, da opsætningsvejledningen gør det for dig. Du skal angive denne brugerkonto en eller flere gange i opsætningsvejledningen, afhængigt af den grad af synkronisering du ønsker. Du kan finde flere oplysninger under [Oprette brugere i Microsoft Dynamics 365 (online) og tildele sikkerhedsroller](/dynamics365/customer-engagement/admin/create-users-assign-online-security-roles).

Hvis du vælger at aktivere *varetilgængelighed*, skal integrationsbrugerkontoen have en adgangsnøgle til webtjenesten. Dette foregår i to trin. På siden [!INCLUDE[d365fin](includes/d365fin_md.md)] for brugerkontoen skal du vælge knappen **Ændr webtjenestenøgle**, og i opsætningsvejledningen til Dynamics 365 for Sales-forbindelsen skal du angive denne bruger som brugeren af OData-webtjenesten.

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

I Dynamics 365 for Sales afhænger salgsordrer af ekstra oplysninger, f.eks. kunder, enheder, valutaer, debitorprisgrupper, varer og/eller ressourcer. For at integration med salgsordrer skal fungere uden problemer, skal du skal sammenkæde kunder, enheder, valutaer, debitorprisgrupper, varer og/eller ressourcer først.

### <a name="synchronizing-records-fully"></a>Fuld synkronisering af poster
I slutningen af den assisterede opsætningsvejledning kan du vælge handlingen **Kør fuld synkronisering** for at starte synkronisering af alle [!INCLUDE[d365fin](includes/d365fin_md.md)]-poster med alle relaterede poster i den tilknyttede Dynamics 365 for Sales-løsning. I vinduet **Fuld CRM-synkroniseringsgennemgang** skal du vælge handlingen **Start**. Synkroniseringen begynder derefter at udføre opgaver i overensstemmelse med afhængigheder. For eksempel synkroniseres valutaposter før debitorposter. Fuld synkronisering kan tage lang tid og køres derfor i baggrunden, så du kan fortsætte med at arbejde i [!INCLUDE[d365fin](includes/d365fin_md.md)].

For at kontrollere status for individuelle job i en fuldstændig synkronisering skal du fokusere på felterne **Status for opgavekøpost**, **Status for til int. tabel-job** eller **Status for fra int. tabel-job** i vinduet **Fuld CRM-synkroniseringsgennemgang**.

Fra vinduet **Konfiguration af Microsoft Dynamics 365-forbindelse** kan du få oplysninger om fuld synkronisering, når som helst. Her kan du også åbne vinduet **Integrationstabelkoblinger** for at få vist detaljer om tabellerne i [!INCLUDE[d365fin](includes/d365fin_md.md)] og Dynamics 365 for Sales-løsningen, som skal synkroniseres.  

## <a name="handling-special-sales-order-data"></a>Håndtering af særlige salgsordredata
Salgsordrer i Dynamics 365 for Sales vil automatisk blive overført til [!INCLUDE[d365fin](includes/d365fin_md.md)], hvis du vælger afkrydsningsfeltet **Opret salgsordrer automatisk** i vinduet **Konfiguration af Microsoft Dynamics 365-forbindelse**. På sådanne salgsordrer overføres og knyttes feltet **Navn** på den oprindelige ordre til feltet **Eksternt bilagsnummer** i [!INCLUDE[d365fin](includes/d365fin_md.md)].

Dette kan også fungere, hvis den oprindelige salgsordre indeholder rekvirerede produkter, hvilket betyder varer eller ressourcer, der ikke er registreret i noget produkt. I så fald skal du udfylde felterne **Rekvireret produkttype** og **Rekvireret produktnr.** i vinduet **Opsætning af salg og tilgodehavender**, så sådanne ikke-registrerede produktsalg knyttes til et bestemt vare/ressourcenummer for finansielle analyser.

Hvis varebeskrivelsen på den oprindelige salgsordre er meget lang, oprettes der en ekstra salgsordrelinje af typen Bemærkning for at holde hele teksten på salgsordren i [!INCLUDE[d365fin](includes/d365fin_md.md)].

## <a name="see-also"></a>Se også
[Relationsstyring](marketing-relationship-management.md)  
[Arbejde med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)  
[Ændre, hvilke funktioner der vises](ui-experiences.md)  
[Administrere brugere og deres rettigheder](ui-how-users-permissions.md)    
[Onboarding af din organisation og dine brugerne i Dynamics 365 (online)](/dynamics365/customer-engagement/admin/onboard-your-organization-and-users-to-dynamics-365-online)  

## [!INCLUDE[d365fin](includes/free_trial_md.md)]  
## [!INCLUDE[d365fin](includes/training_link_md.md)]

