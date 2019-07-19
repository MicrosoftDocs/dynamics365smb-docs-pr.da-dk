---
title: Konfigurere brugerkonti til integration med Dynamics 365 for Sales | Microsoft Docs
description: Få at vide, hvordan du konfigurerer brugerkonti, som apps bruger til at udveksle data, og som brugere anvender til at få adgang til og synkronisere data i de pågældende apps.
services: project-madeira
documentationcenter: ''
author: bholtorf
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/01/2019
ms.author: bholtorf
ms.openlocfilehash: 0f59324e41695e35e09a2dd970492acb3a8dba58
ms.sourcegitcommit: 8fe694b7bbe7fc0456ed5a9e42291218d2251b05
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 07/04/2019
ms.locfileid: "1726878"
---
# <a name="setting-up-user-accounts-for-integrating-with-dynamics-365-for-sales"></a>Konfigurere brugerkonti til integration med Dynamics 365 for Sales
Denne artikel indeholder en oversigt over opsætning af de brugerkonti, der kræves til at integrere [!INCLUDE[crm_md](includes/crm_md.md)] med [!INCLUDE[d365fin](includes/d365fin_md.md)].  

> [!VIDEO https://go.microsoft.com/fwlink/?linkid=2085500]

## <a name="setting-up-the-administrator-user-account-in-sales"></a>Konfigurere administratorbrugerkontoen i Sales
Du skal tilføje din administratorbrugerkonto for [!INCLUDE[d365fin](includes/d365fin_md.md)] som en bruger i [!INCLUDE[crm_md](includes/crm_md.md)] og derefter opgradere brugeren til administrator i [!INCLUDE[crm_md](includes/crm_md.md)]. Administratorbrugerkontoen skal også have rollen Systemtilpasser og mindst én anden ikke-administrativ brugerrolle, f.eks. Salgschef, i [!INCLUDE[crm_md](includes/crm_md.md)].

## <a name="setting-up-the-user-account-for-the-integration"></a>Konfigurere brugerkontoen til integrationen
Du skal oprette en dedikeret brugerkonto i dit Office 365-abonnement, som både [!INCLUDE[d365fin](includes/d365fin_md.md)] og [!INCLUDE[crm_md](includes/crm_md.md)] kan bruge til at synkronisere dataene. Denne brugerkonto skal kunne logge på [!INCLUDE[crm_md](includes/crm_md.md)], hvilket betyder, at brugeren skal have en licens til [!INCLUDE[crm_md](includes/crm_md.md)] og mindst én sikkerhedsrolle, den er tildelt i [!INCLUDE[crm_md](includes/crm_md.md)] som beskrevet [her](https://docs.microsoft.com/en-us/dynamics365/customer-engagement/admin/create-users-assign-online-security-roles#create-a-user-account). Yderligere oplysninger om oprettelse af brugere i [!INCLUDE[crm_md](includes/crm_md.md)] finder du i [Administrere sikkerhed, brugere og team](http://go.microsoft.com/fwlink/?LinkID=616518). Når der er oprettet forbindelse, tildeler [!INCLUDE[d365fin](includes/d365fin_md.md)] brugerkontoen de sikkerhedsroller, den skal bruge i [!INCLUDE[d365fin](includes/d365fin_md.md)], og denne konto kan indstilles til [ikke-interaktiv adgangstilstand](https://docs.microsoft.com/en-us/dynamics365/customer-engagement/admin/create-users-assign-online-security-roles#create-a-non-interactive-user-account) i [!INCLUDE[crm_md](includes/crm_md.md)]

![Den assisterede opsætningsvejledning viser det område, hvor der skal angives brugeroplysninger til synkronisering](media/sync-user-setup.png "Guidesiden til assisteret opsætning af visualisering viser det sted, hvor der skal angives brugeroplysninger til synkronisering")

> [!IMPORTANT]  
> Brug ikke administratorkontoen til [!INCLUDE[crm_md](includes/crm_md.md)] til synkronisering. Hvis du gør det, afbrydes synkroniseringen.
> For at undgå konstant synkronisering synkroniseres ændringer af data, der er foretaget af brugerkontoen til integration, desuden ikke. <!--What changes would this account make?--> Når der er oprettet forbindelse, anbefales det at angive adgangstilstanden til brugerkontoen til integration til ikke-interaktiv tilstand i [!INCLUDE[crm_md](includes/crm_md.md)]. Du kan finde flere oplysninger i [Oprette en ikke-interaktiv brugerkonto](https://docs.microsoft.com/en-us/dynamics365/customer-engagement/admin/create-users-assign-online-security-roles#create-a-non-interactive-user-account).

## <a name="setting-up-accounts-for-sales-people"></a>Konfigurere konti for sælgere
Du skal oprette brugerkonti i [!INCLUDE[crm_md](includes/crm_md.md)] for sælgere fra [!INCLUDE[d365fin](includes/d365fin_md.md)]. For at gøre dette nemmere har Microsoft 365 Administration en Excel-skabelon, du kan bruge. På siden **Aktive brugere** skal du vælge **Flere** og derefter **Importér flere brugere**. Vælg **Download en CSV-fil kun med overskrifter**, og angiv derefter oplysningerne til sælgerne. Du kan få vist et eksempel ved at vælge **Download en CSV-fil med overskrifter og eksempler på brugeroplysninger**. Når du angiver oplysninger om brugerne, er næste trin i processen til import at tildele brugerlicenser til Dynamics 365 Customer Engagement-planen.  

Når du importerer brugerne og tildeler dem licenser til Dynamics 365 Customer Engagement, skal du tildele brugerne til rollen **Sælger** i [!INCLUDE[crm_md](includes/crm_md.md)].

![Sammenkædning af sælgere og brugere i Dynamics 365 for Sales](media/couple-salespeople.png "Visualisering af sammenkædning af sælgerne og brugere i Dynamics 365 for Sales")

## <a name="minimum-permissions-for-user-accounts-in-includecrmmdincludescrmmdmd"></a>Minimumtilladelser for brugerkonti i [!INCLUDE[crm_md](includes/crm_md.md)]
Når du installerer integrationsløsningen, konfigureres tilladelser til integrationsbrugerkontoen i [!INCLUDE[crm_md](includes/crm_md.md)]. Hvis disse tilladelser ændres, skal du muligvis nulstille dem. Det kan du gøre ved at geninstallere integrationsløsningen eller manuelt nulstille dem. I følgende tabeller vises minimumtilladelserne for brugerkontiene i [!INCLUDE[crm_md](includes/crm_md.md)].

### <a name="integration-administrator"></a>Integrationsadministrator
Følgende tabel viser minimumtilladelserne under de enkelte faner for hver sikkerhedsrolle, der kræves til administratorbrugeren.

##### <a name="customization"></a>Tilpasning
|Sikkerhedsrolle|Adgangsniveau|Dynamics NAV 2018 og ældre|Business Central <br> Oktober 2018|Business Central <br> April 2019|
|----|----|-----|----|----|
|Modelstyret app|Global|||Læs|
|Plug-in-montage|Global|Læs|Læs|Læs|
|Plug-in-type|Global|Læs|Læs|Læs|
|Relationer|Global|||Læs|
|SDK-meddelelse|Global|Læs|Læs|Læs|
|Operationstrin for SDK-meddelelse|Global|Læs|Læs|Læs|
|Billede af operationstrin for SDK-meddelelse|Global|Læs|Læs|Læs|
|System fra|Global|||Skriv|

##### <a name="custom-entities"></a>Brugerdefinerede enheder
|Sikkerhedsrolle|Adgangsniveau|Dynamics NAV 2018 og ældre|Business Central <br> Oktober 2018|Business Central <br> April 2019|
|----|----|-----|----|----|
|Statistik for Business Central-konto|Global|Læs|Læs|Læs|
|Business Central-forbindelse|Global|Opret, Læs, Skriv, Slet|Opret, Læs, Skriv, Slet|Opret, Læs, Skriv, Slet|
|Bogføringskonfiguration|Global|||Skriv|

#### <a name="integration-user"></a>Integrationsbruger
Følgende tabel viser minimumtilladelserne under de enkelte faner for hver sikkerhedsrolle, der kræves til integrationsbrugeren.

##### <a name="core-records"></a>Kerneposter
|Sikkerhedsrolle|Adgangsniveau|Dynamics NAV 2018 og ældre|Business Central <br> Oktober 2018|Business Central <br> April 2019|
|----|----|-----|----|----|
|Konto|Global|Opret, Læs, Skriv, Tilføj, Føj til, Tildel|Opret, Læs, Skriv, Tilføj, Føj til, Tildel|Opret, Læs, Skriv, Tilføj, Føj til, Tildel|
|Handlingskort|Global||Læs|Læs|
|Forbindelse|Global|Læs|Læs|Læs|
|Kontakt|Global|Opret, Læs, Skriv, Tilføj, Føj til|Opret, Læs, Skriv, Tilføj, Føj til|Opret, Læs, Skriv, Tilføj, Føj til|
|Note|Global|||Opret, Læs, Skriv, Slet, Tilføj, Tildel|
|Salgsmulighed|Global||Opret, Læs, Skriv, Tilføj, Føj til|Opret, Læs, Skriv, Tilføj, Føj til|
|Post|Global|||Opret, Læs, Føj til|
|Brugergrænseflade for brugerobjekt|Bruger|Opret, Læs, Skriv|Opret, Læs, Skriv|Opret, Læs, Skriv|

##### <a name="sales"></a>Salg
|Sikkerhedsrolle|Adgangsniveau|Dynamics NAV 2018 og ældre|Business Central <br> Oktober 2018|Business Central <br> April 2019|
|----|----|-----|----|----|
|Faktura|Global|Opret, Læs, Skriv, Tilføj, Føj til|Opret, Læs, Skriv, Tilføj, Føj til|Opret, Læs, Skriv, Tilføj, Føj til|
|Sorteringsrækkefølge|Global|Læs, Skriv, Føj til|Læs, Skriv, Føj til|Læs, Skriv, Tilføj, Føj til, Tildel|
|Produkt|Global|Opret, Læs, Skriv, Tilføj, Føj til|Opret, Læs, Skriv, Tilføj, Føj til|Opret, Læs, Skriv, Tilføj, Føj til|
|Egenskab|Global|Læs|Læs|Læs|
|Egenskabstilknytning|Global|Læs|Læs|Læs|
|Element i grupperede egenskabsindstillinger|Global|Læs|Læs|Læs|
|Tilbud|Global|Læs|Læs|Læs|

##### <a name="service"></a>Tjeneste
|Sikkerhedsrolle|Adgangsniveau|Dynamics NAV 2018 og ældre|Business Central <br> Oktober 2018|Business Central <br> April 2019|
|----|----|-----|----|----|
|Sag|Global|Læs|Læs|Læs|

##### <a name="business-management"></a>Virksomhedsledelse
|Sikkerhedsrolle|Adgangsniveau|Dynamics NAV 2018 og ældre|Business Central <br> Oktober 2018|Business Central <br> April 2019|
|----|----|-----|----|----|
|Valuta|Global|Opret, Læs, Skriv|Opret, Læs, Skriv|Opret, Læs, Skriv|
|Organisation|Global|Læse, skrive|Læse, skrive|Læse, skrive|
|Sikkerhedsrolle|Global|||Læs|
|Bruger|Global|Opret, Læs, Skriv, Tilføj, Føj til|Opret, Læs, Skriv, Tilføj, Føj til|Opret, Læs, Skriv, Tilføj, Føj til|
|Brugerindstillinger|Global|Opret, Læs, Skriv, Slet, Føj til|Opret, Læs, Skriv, Slet, Føj til|Opret, Læs, Skriv, Slet, Føj til|
|Handle på vegne af en anden bruger|Global|Ja|Ja|Ja|

##### <a name="customization"></a>Tilpasning
|Sikkerhedsrolle|Adgangsniveau|Dynamics NAV 2018 og ældre|Business Central <br> Oktober 2018|Business Central <br> April 2019|
|----|----|-----|----|----|
|Felt|Global||Læs|Læs|
|Plug-in-montage|Global|Læs|Læs|Læs|
|Plug-in-type|Global|Læs|Læs|Læs|
|SDK-meddelelse|Global|Læs|Læs|Læs|
|Operationstrin for SDK-meddelelse|Global|Læs|Læs|Læs|
|Webressource|Global|Læs|Læs|Læs|

##### <a name="custom-entities"></a>Brugerdefinerede enheder
|Sikkerhedsrolle|Adgangsniveau|Dynamics NAV 2018 og ældre|Business Central <br> Oktober 2018|Business Central <br> April 2019|
|----|----|-----|----|----|
|Dynamics 365 Business Central-kontostatistik|Global|Opret, Læs, Skriv, Føj til|Opret, Læs, Skriv, Føj til|Opret, Læs, Skriv, Føj til|
|Dynamics 365 Business Central-forbindelse|Global|Læs|Læs|Læs|

### <a name="product-availability-user"></a>Produkttilgængelighedsbruger
Du kan give sælgere mulighed for at få vist lagerniveauer for de varer, de sælger, ved at tildele dem de tilladelser, der er beskrevet i følgende tabel.

##### <a name="custom-entities"></a>Brugerdefinerede enheder
|Sikkerhedsrolle|Adgangsniveau|Dynamics NAV 2018 og ældre|Business Central <br> Oktober 2018|Business Central <br> April 2019|
|----|----|-----|----|----|
|Dynamics 365 Business Central-kontostatistik|Global|Opret, Læs, Skriv, Føj til|Opret, Læs, Skriv, Føj til|Opret, Læs, Skriv, Føj til|
|Dynamics 365 Business Central-forbindelse|Global|Læs|Læs|Læs|

## <a name="see-also"></a>Se også  
[Integration med Dynamics 365 for Sales](admin-prepare-dynamics-365-for-sales-for-integration.md)  
