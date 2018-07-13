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
ms.date: 07/02/2018
ms.author: edupont
ms.translationtype: HT
ms.sourcegitcommit: 046a42582dc66368fded90a4bb45add71a95d979
ms.openlocfilehash: 33987f37c170af9982b86baf20f0c3e0682de2cd
ms.contentlocale: da-dk
ms.lasthandoff: 07/02/2018

---
# <a name="managing-customers-and-sales-created-in-dynamics-365-for-sales"></a>Administration af kunder og salg, der er oprettet i Dynamics 365 for Sales
Hvis du bruger Dynamics 365 for Sales (Sales) til kundeengagementer, kan du bruge [!INCLUDE[d365fin](includes/d365fin_md.md)] til ordrebehandling og økonomi og få problemfri integration i lead-til-kontant-processen.

Når programmet er indstillet til integration med Sales, har du adgang til Sales-data fra [!INCLUDE[d365fin](includes/d365fin_md.md)] og omvendt i nogle tilfælde. Integrationen gør det muligt at arbejde med og synkronisere datatyper, der er fælles for begge tjenester, f.eks. debitorer, kontakter og salgsoplysninger, og holde dataene opdaterede på begge lokationer.  

For eksempel kan sælgeren i Sales bruge prislisterne fra [!INCLUDE[d365fin](includes/d365fin_md.md)], når vedkommende opretter en salgsordre. Når sælgeren føjer varen til salgsordrelinjen i Sales, kan han eller hun også få vist lagerniveauet (disponering) af varen fra [!INCLUDE[d365fin](includes/d365fin_md.md)].

Omvendt kan ordrebehandlere i [!INCLUDE[d365fin](includes/d365fin_md.md)] håndtere særlige karakteristika for salgsordrer, der overføres automatisk eller manuelt fra Sales, f.eks. automatisk oprette og bogføre gyldige salgsordrelinjer for varer eller ressourcer, der blev angivet i Sales som rekvirerede produkter. Du kan finde flere oplysninger i afsnittet "Håndtering af særlige salgsordredata".

> [!IMPORTANT]  
> [!INCLUDE[d365fin](includes/d365fin_md.md)] integrerer kun med Dynamics 365 for Sales. Andre programmer eller løsninger i Dynamics 365, der ændrer standardarbejdsproces eller datamodel i Sales, for eksempel Project Service Automation, kan bryde integrationen mellem [!INCLUDE[d365fin](includes/d365fin_md.md)] og Sales.

## <a name="standard-sales-entity-mapping-for-synchronization"></a>Standardenhedstilknytning i Sales til synkronisering
Sales-enheder, f.eks konti, integreres med tilsvarende [!INCLUDE[d365fin](includes/d365fin_md.md)]-posttyper, f.eks kunder. Når du vil arbejde med Sales-data, skal du oprette tilknytninger, kaldet sammenkædninger, mellem [!INCLUDE[d365fin](includes/d365fin_md.md)]-poster og Sales-enhedsposter. F.eks. kan du oprette en sammenkædning mellem en bestemt kunde i [!INCLUDE[d365fin](includes/d365fin_md.md)] og en tilsvarende konto i Sales.

Følgende tabel indeholder de [!INCLUDE[d365fin](includes/d365fin_md.md)]-posttyper (tabeller) og tilsvarende Sales-enheder, der kan synkroniseres som standard.

|[!INCLUDE[d365fin](includes/d365fin_md.md)]|Salg|Synkroniseringsretning|Standardfilter|
|-------------------------------------------|-----|-------------------------|--------------|
|Sælger/indkøber|Bruger|Sales -> Business Central|Sales-kontaktfilter: **Status** er **Nej**, **Brugerlicenseret** er **Ja** og integrationsbrugertilstand er **Nej**|
|Kunde|Konto|Business Central -> Sales og Sales -> Business Central|Sales-kontofilter: **Relationstype** er **Debitor**, og **Status** er **Aktiv**.|
|Kontakt|Kontakt|Business Central -> Sales og Sales -> Business Central|Business Central-kontaktfilter: **Type** er **Person**, og kontakten er knyttet til en virksomhed. Sales-kontaktfilter: Kontakten er tildelt til en virksomhed, og den overordnede debitortype er **Konto**.|
|Valuta|Transaktionsvaluta|Business Central -> Sales| |
|Enhe.|Enhedsgruppe|Business Central -> Sales| |
|Vare|Produkt|Business Central -> Sales og Sales -> Business Central|Sales-kontaktfilter: **Produkttype** er **Salg lager**|
|Ressource|Produkt|Business Central -> Sales og Sales -> Business Central|Sales-kontaktfilter: **Produkttype** er **Tjenester**|
|Debitorprisgruppe|Prisliste|Business Central -> Sales| |
|Salgspris|Produktprisliste|Business Central -> Sales|Business Central-kontaktfilter: **Salgskode** er ikke tom, **Salgstype** er **Debitorprisgruppe**|
|Salgsmulighed|Salgsmulighed|Business Central -> Sales og Sales -> Business Central| |
|Salgsfakturahoved|Faktura|Business Central -> Sales| |
|Salgsfakturalinje|Fakturaprodukt|Business Central -> Sales| |

Sales-enheder og [!INCLUDE[d365fin](includes/d365fin_md.md)]-tabeller, der synkroniseres, defineres af tilknytning af poster i tabellen 5335, **Integrationstabeltilknytning**. Du kan få vist tilknytningerne og angive filtre fra siden 5335, **Integrationstabelkoblinger**. Tilknytningen mellem felterne i [!INCLUDE[d365fin](includes/d365fin_md.md)]-poster og felterne i Sales-enheder defineres af felttilknytningsposter i tabellen 5336 **Integrationsfelttilknytninger** og med yderligere tilknytningslogik.

### <a name="field-mapping-for-the-sales-account-option"></a>Felttilknytning for salgskontoindstillingen
Tre tabeller i [!INCLUDE[d365fin](includes/d365fin_md.md)] er knyttet til indstillingsfelterne i enheden **Konto**.   

De poster i tabellen, der ikke er knyttet til de indstillinger, der findes i Sales, springes over under synkroniseringen. Det betyder, at feltet **Indstilling** er tomt i Sales.

Følgende tabel viser tilknytninger fra Business Central-tabeller til feltet **Indstilling** i enheden **Konto**.

|Sortbord|Feltet Indstilling i kontoenheden i Sales|
|----------------------|-------------------------------------------|
|Betalingsbetingelser|Betalingsbetingelser|
|Leveringsform|Adresse 1: Fragtbetingelser|
|Speditør|Adresse 1: Forsendelsesmetode|

### <a name="synchronization-rules"></a>Synkroniseringsregler
I følgende tabel beskrives de regler, der styrer synkroniseringen mellem Business Central-tabeller og Sales-enheder.

> [!NOTE]  
> Ændringer af data i Sales, som udføres af Sales-forbindelseskontoen, ignoreres. Ændringerne synkroniseres ikke. Derfor anbefales det, at du ikke ændrer data ved hjælp af Sales-forbindelseskontoen.

|Sortbord|Regel|
|-----|----|
|Kunder (Debitorer)|Før du kan synkronisere en debitor med en konto, skal den sælger, der er tildelt debitoren, være sammenkædet med en bruger i Sales. Når du derfor kører KUNDER – Dynamics 365 for Sales-synkroniseringsjobbet, og du konfigurerer det til at oprette nye poster, skal du sørge for at synkronisere sælgere med Sales-brugere, før du synkroniserer debitorer med Sales-konti. <br /> <br />KUNDER – Dynamics 365 for Sales-synkroniseringsjobbet synkroniserer kun Sales-konti, der har relationstypen Debitor.|
|Kontakter|Kun kontakter i Sales, der er knyttet til en konto, oprettes i Business Central. Værdien Sælgerkode definerer ejeren af det sammenkoblede objekt i Sales.|
|Valutaer|Valutaer sammenkædes med transaktionsvalutaer i Sales baseret på ISO-koder. Kun valutaer, der har en ISO-standardkoder, sammenkædes og synkroniseres med transaktionsvalutaer.|
|Enheder|Måleenheder synkroniseres med enhedsgrupper i Sales. Der kan kun være én måleenhed defineret i enhedsgruppen.|
|Varer|Når der synkroniseres varer med Sales-produkter, opretter Business Central automatisk en prisliste i Sales. For at undgå synkroniseringsfejl bør du ikke ændre denne prisliste manuelt.|
|Sælgere|Sælgere er koblet til systembrugere i Sales. Brugeren skal være aktiveret og licenseret og må ikke være integrationsbrugeren. Bemærk, at dette er den første tabel, der skal synkroniseres, fordi den bruges i kunder, kontakter, salgsmuligheder og salgsfakturaer.|
|Ressourcer|Ressourcer synkroniseres med produkter i Sales, der har produkttypen Service.|
|Debitorprisgrupper|Debitorprisgrupper synkroniseres med prislister i Sales.|
|Salgspriser|Priser i Sales, der har salgstypen Debitorprisgruppe og har en salgskode defineret, synkroniseres med prislistelinjer i Sales|
|Salgsmuligheder|Salgsmuligheder synkroniseres med salgsmuligheder i Sales. Værdien Sælgerkode definerer ejeren af det sammenkoblede objekt i Sales.|
|Bogførte salgsfakturaer|Bogførte salgsfakturaer synkroniseres med salgsfakturaer. Før en faktura kan synkroniseres, er det bedre at synkronisere alle andre enheder, der kan indgå i fakturaen, fra sælgere til prislister. Værdien Sælgerkode i fakturahovedet definerer ejeren af det sammenkoblede objekt i Sales.|

## <a name="setting-up-the-connection"></a>Indstilling af forbindelsen
Fra startsiden kan du åbne opsætningsvejledningen **Konfiguration af Microsoft Dynamics 365-forbindelse**, der hjælper dig med at oprette forbindelsen. Når det er gjort, får du en problemfri sammenkædning af Sales-poster og [!INCLUDE[d365fin](includes/d365fin_md.md)]-poster.  

> [!NOTE]  
>   I det følgende forklares den assisterende opsætning, men du kan udføre de samme opgaver manuelt i vinduet **Konfiguration af Sales-forbindelse**.

I den assisterende opsætningsvejledning kan du vælge, hvilke data der skal synkroniseres mellem de to tjenester. Du kan også angive, at du vil importere din eksisterende Sales-løsning. Hvis du vil det, skal du angive en administratorbrugerkonto.

### <a name="setting-up-the-user-account-for-importing-the-solution"></a>Konfigurere brugerkontoen til import af løsningen
Når du vil importere en eksisterende Sales-løsning, bruger opsætningsvejledningen en administratorkonto. Denne konto skal være en gyldig bruger i Sales med følgende sikkerhedsroller:

* Systemadministrator  
* Løsningsoptimerer  

Du kan finde flere oplysninger under [Oprette brugere i Microsoft Dynamics 365 (online) og tildele sikkerhedsroller](/dynamics365/customer-engagement/admin/create-users-assign-online-security-roles) og [Administrere brugere og tilladelser](ui-how-users-permissions.md).  

Denne konto bruges kun under opsætningen. Når løsningen indlæses i [!INCLUDE[d365fin](includes/d365fin_md.md)], er kontoen ikke længere nødvendig.

### <a name="setting-up-the-user-account-for-synchronization"></a>Konfigurere brugerkontoen til synkronisering
Integration er baseret på en delt brugerkonto. Derfor skal du i dit Office 365-abonnement oprette en dedikeret bruger, der skal bruges til synkronisering mellem de to tjenester. Denne konto skal allerede være en gyldig bruger i Sales, men du behøver ikke at tildele sikkerhedsroller til kontoen, da opsætningsvejledningen gør det for dig. Du skal angive denne brugerkonto en eller flere gange i opsætningsvejledningen, afhængigt af den grad af synkronisering du ønsker. Du kan finde flere oplysninger under [Oprette brugere i Microsoft Dynamics 365 (online) og tildele sikkerhedsroller](/dynamics365/customer-engagement/admin/create-users-assign-online-security-roles).

Hvis du vælger at aktivere *varetilgængelighed*, skal integrationsbrugerkontoen have en adgangsnøgle til webtjenesten. Dette foregår i to trin. På siden [!INCLUDE[d365fin](includes/d365fin_md.md)] for brugerkontoen skal du vælge knappen **Ændr webtjenestenøgle**, og i opsætningsvejledningen til Sales-forbindelsen skal du angive denne bruger som brugeren af OData-webtjenesten.

Hvis du vælger at aktivere *integration af salgsordre*, skal du angive en bruger, der kan håndtere denne synkronisering - integrationsbrugeren eller en anden brugerkonto.

### <a name="coupling-records"></a>Sammenkæde poster
I den assisterende opsætningsvejledning kan du vælge at synkronisere mellem de to tjenester. Men senere kan du også indstille synkroniseringen af bestemte typer data. Dette kaldes *sammenkædning*, og dette afsnit indeholder anbefalinger for, hvad du skal tage hensyn til.

Hvis du f.eks. vil have vist Sales-konti som debitorer i [!INCLUDE[d365fin](includes/d365fin_md.md)], skal du sammenkæde de to typer poster. Det er ikke særlig vanskeligt - du skal åbne vinduet **Debitoroversigt** i [!INCLUDE[d365fin](includes/d365fin_md.md)], hvor der er en handling på båndet til sammenkædning af disse data med Sales. Derefter skal du angive, hvilke [!INCLUDE[d365fin](includes/d365fin_md.md)]-kunder der svarer til hvilke konti i Sales.

I visse områder kræver funktionaliteten, at du sammenkæder bestemte datasæt før andre datasæt som vist i følgende liste:

* Debitorer og konti  
  * Sammenkæd først sælgere med Sales-brugere  
* Varer og ressourcer  
  * Sammenkæd først enheder med Sales-enhedsgrupper  
* Priser på varer og ressourcer  
  * Sammenkæd først debitorprisgrupper med Sales-priser  

> [!NOTE]  
>   Hvis du bruger priser i udenlandsk valuta, skal du sørge for at sammenkæde valutaer med Sales-transaktionsvalutaer.

I Sales afhænger salgsordrer af ekstra oplysninger, f.eks. kunder, enheder, valutaer, debitorprisgrupper, varer og/eller ressourcer. For at integration med salgsordrer skal fungere uden problemer, skal du skal sammenkæde kunder, enheder, valutaer, debitorprisgrupper, varer og/eller ressourcer først.

### <a name="synchronizing-records-fully"></a>Fuld synkronisering af poster
I slutningen af den assisterede opsætningsvejledning kan du vælge handlingen **Kør fuld synkronisering** for at starte synkronisering af alle [!INCLUDE[d365fin](includes/d365fin_md.md)]-poster med alle relaterede poster i den tilknyttede Sales-løsning. I vinduet **Fuld CRM-synkroniseringsgennemgang** skal du vælge handlingen **Start**. Synkroniseringen begynder derefter at udføre opgaver i overensstemmelse med afhængigheder. For eksempel synkroniseres valutaposter før debitorposter. Fuld synkronisering kan tage lang tid og køres derfor i baggrunden, så du kan fortsætte med at arbejde i [!INCLUDE[d365fin](includes/d365fin_md.md)].

For at kontrollere status for individuelle job i en fuldstændig synkronisering skal du fokusere på felterne **Status for opgavekøpost**, **Status for til int. tabel-job** eller **Status for fra int. tabel-job** i vinduet **Fuld CRM-synkroniseringsgennemgang**.

Fra vinduet **Konfiguration af Microsoft Dynamics 365-forbindelse** kan du få oplysninger om fuld synkronisering, når som helst. Her kan du også åbne vinduet **Integrationstabelkoblinger** for at få vist detaljer om tabellerne i [!INCLUDE[d365fin](includes/d365fin_md.md)] og i Sales-løsningen, som skal synkroniseres.

## <a name="handling-special-sales-order-data"></a>Håndtering af særlige salgsordredata
Salgsordrer i Sales vil automatisk blive overført til [!INCLUDE[d365fin](includes/d365fin_md.md)], hvis du vælger afkrydsningsfeltet **Opret salgsordrer automatisk** i vinduet **Konfiguration af Microsoft Dynamics 365-forbindelse**. På sådanne salgsordrer overføres og knyttes feltet **Navn** på den oprindelige ordre til feltet **Eksternt bilagsnummer** i [!INCLUDE[d365fin](includes/d365fin_md.md)].

Dette kan også fungere, hvis den oprindelige salgsordre indeholder rekvirerede produkter, hvilket betyder varer eller ressourcer, der ikke er registreret i noget produkt. I så fald skal du udfylde felterne **Rekvireret produkttype** og **Rekvireret produktnr.** i vinduet **Opsætning af salg og tilgodehavender**, så sådanne ikke-registrerede produktsalg knyttes til et bestemt vare/ressourcenummer for finansielle analyser.

Hvis varebeskrivelsen på den oprindelige salgsordre er meget lang, oprettes der en ekstra salgsordrelinje af typen Bemærkning for at holde hele teksten på salgsordren i [!INCLUDE[d365fin](includes/d365fin_md.md)].

## <a name="see-also"></a>Se også
[Relationsstyring](marketing-relationship-management.md)  
[Arbejde med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)  
[Ændre, hvilke funktioner der vises](ui-experiences.md)  
[Administrere brugere og deres rettigheder](ui-how-users-permissions.md)    
[Onboarding af din organisation og dine brugerne i Dynamics 365 (online)](/dynamics365/customer-engagement/admin/onboard-your-organization-and-users-to-dynamics-365-online)  

## [!INCLUDE[d365fin](includes/free_trial_md.md)]  

