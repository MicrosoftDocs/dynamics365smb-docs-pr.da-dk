---
title: Konfigurere brugerkonti til integration med Microsoft Dataverse | Microsoft Docs
description: 'Få at vide, hvordan du konfigurerer brugerkonti, som apps bruger til at udveksle data, og som brugere anvender til at få adgang til og synkronisere data i de pågældende apps.'
author: brentholtorf
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: null
ms.date: 04/01/2021
ms.author: bholtorf
---
# <a name="setting-up-user-accounts-for-integrating-with-microsoft-dataverse" />Konfigurere brugerkonti til integration med Microsoft Dataverse

Denne artikel indeholder en oversigt over opsætning af de brugerkonti, der kræves til at integrere [!INCLUDE[prod_short](includes/cds_long_md.md)] med [!INCLUDE[prod_short](includes/prod_short.md)].

## <a name="set-up-the-administrator-user-account" />Konfigurere administratorbrugerkontoen

Hvis du vil oprette forbindelsen mellem [!INCLUDE[prod_short](includes/prod_short.md)] og [!INCLUDE[prod_short](includes/cds_long_md.md)], skal du logge på [!INCLUDE[prod_short](includes/prod_short.md)] med en brugerkonto, der er tildelt til licensen [!INCLUDE[prod_short](includes/prod_short.md)] Essentiel eller [!INCLUDE[prod_short](includes/prod_short.md)] Premium. Vi bruger denne konto én gang til at installere og konfigurere nogle påkrævede komponenter.

> [!IMPORTANT]
> Under installationen bliver du bedt om at angive legitimationsoplysninger til [!INCLUDE[prod_short](includes/cds_long_md.md)]-miljøet. Angiv de oplysninger til en konto, der tilhører en licenseret bruger og er tildelt sikkerhedsrollen **Systemadministrator** i miljøet [!INCLUDE[prod_short](includes/cds_long_md.md)] og den globale administrator på den lejer, som miljøet tilhører. Denne konto har ikke brug for en licens til [!INCLUDE[prod_short](includes/prod_short.md)], da den kun skal bruges til klargøringsopgaver i [!INCLUDE[prod_short](includes/cds_long_md.md)]-miljøet.
>
> Når forbindelseskonfiguration er fuldført, kan du fjerne denne [!INCLUDE[prod_short](includes/cds_long_md.md)]-bruger. Integrationen fortsætter med at bruge den brugerkonto, der er automatisk oprettet specielt til integrationen.

## <a name="permissions-and-security-roles-for-user-accounts-in-includeprodshortincludescdslongmdmd" />Tilladelser og sikkerhedsroller for brugerkonti i [!INCLUDE[prod_short](includes/cds_long_md.md)]

Basisintegrationsløsningen opretter følgende roller i [!INCLUDE[cds_long](includes/cds_long_md.md)] til integrationen:

* **Integrationsadministrator**: Gør det muligt at styre forbindelsen mellem [!INCLUDE[prod_short](includes/prod_short.md)] og [!INCLUDE[cds_long](includes/cds_long_md.md)]. Dette knyttes som regel kun til den automatisk oprettede brugerkonto til synkronisering.
* **Integrationsbruger**: Giver brugere adgang til synkroniserede data. Dette knyttes typisk til den automatisk oprettede brugerkonto til synkronisering og alle andre brugere, der skal se eller have adgang til de synkroniserede data.

> [!NOTE]
>
> Rollerne **Integrationsadministrator** og **Integrationsbruger** rollerne bør kun bruges af den programbruger, der kører integrationen. Programbrugeren behøver ikke at få licens til [!INCLUDE[prod_short](includes/prod_short.md)] eller [!INCLUDE[cds_long](includes/cds_long_md.md)] tildelt.

Når du installerer basisintegrationsløsningen, konfigureres tilladelser til integrationsbrugerkontoen. Hvis disse tilladelser ændres manuelt, kan du nulstille dem. Vælg **Geninstaller integrationsløsning** på siden **Konfiguration af Dataverse-forbindelse** for at geninstallere basisintegrationsløsningen. Dette trin udruller Business Central-integrationssikkerhedsrollen.

<!--
The following tables list the minimum permissions for the user accounts in [!INCLUDE[prod_short](includes/cds_long_md.md)].

### <a name="minimum-permissions-for-the-administrator" />Minimum Permissions for the Administrator
The following table displays the minimum permissions on each tab for each security role that is required for the administrator user.

##### <a name="customization" />Customization
|Security Role|Access Level|Dynamics NAV 2018 and Earlier|Business Central <br> October 2018|Business Central <br> April 2019|
|----|----|-----|----|----|
|Model Driven App|Global|||Read|
|Plugin Assembly|Global|Read|Read|Read|
|Plugin Type|Global|Read|Read|Read|
|Relationship|Global|||Read|
|SDK Message|Global|Read|Read|Read|
|SDK Message Proessing Step|Global|Read|Read|Read|
|SDK Message Proessing Step Image|Global|Read|Read|Read|
|System From|Global|||Write|

##### <a name="custom-entities" />Custom Entities
|Security Role|Access Level|Dynamics NAV 2018 and Earlier|Business Central <br> October 2018|Business Central <br> April 2020|
|----|----|-----|----|----|
|Business Central Account Statistics|Global|Read|Read|Read|
|Business Central Connection|Global|Create, Read, Write, Delete|Create, Read, Write, Delete|Create, Read, Write, Delete|
|Post Configuration|Global|||Write|

### <a name="minimum-permissions-for-automatically-created-includeprodshortincludesprodshortmd-integration-application-user" />Minimum Permissions for automatically created [!INCLUDE[prod_short](includes/prod_short.md)] Integration application user
The following table displays the minimum permissions on each tab for each security role that is required for the automatically created [!INCLUDE[prod_short](includes/prod_short.md)] Integration application user.

##### <a name="core-records" />Core Records
|Security Role|Access Level|Dynamics NAV 2018 and Earlier|Business Central <br> October 2018|Business Central <br> April 2019|
|----|----|-----|----|----|
|Account|Global|Create, Read, Write, Append, Append To, Assign|Create, Read, Write, Append, Append To, Assign|Create, Read, Write, Append, Append To, Assign|
|Action Card|Global||Read|Read|
|Connection|Global|Read|Read|Read|
|Contact|Global|Create, Read, Write, Append, Append To|Create, Read, Write, Append, Append To|Create, Read, Write, Append, Append To|
|Note|Global|||Create, Read, Write, Delete Append, Assign|
|Opportunity|Global||Create, Read, Write, Append, Append To|Create, Read, Write, Append, Append To|
|Post|Global|||Create, Read, Append To|
|User Entity UI|User|Create, Read, Write|Create, Read, Write|Create, Read, Write|

##### <a name="sales" />Sales
|Security Role|Access Level|Dynamics NAV 2018 and Earlier|Business Central <br> October 2018|Business Central <br> April 2019|
|----|----|-----|----|----|
|Invoice|Global|Create, Read, Write, Append, Append To|Create, Read, Write, Append, Append To|Create, Read, Write, Append, Append To|
|Order|Global|Read, Write, Append To|Read, Write, Append To|Read, Write, Append, Append To, Assign|
|Product|Global|Create, Read, Write, Append, Append To|Create, Read, Write, Append, Append To|Create, Read, Write, Append, Append To|
|Property|Global|Read|Read|Read|
|Property Association|Global|Read|Read|Read|
|Property Option Set Item|Global|Read|Read|Read|
|Quote|Global|Read|Read|Read|

##### <a name="service" />Service
|Security Role|Access Level|Dynamics NAV 2018 and Earlier|Business Central <br> October 2018|Business Central <br> April 2019|
|----|----|-----|----|----|
|Case|Global|Read|Read|Read|

##### <a name="business-management" />Business Management
|Security Role|Access Level|Dynamics NAV 2018 and Earlier|Business Central <br> October 2018|Business Central <br> April 2019|
|----|----|-----|----|----|
|Currency|Global|Create, Read, Write|Create, Read, Write|Create, Read, Write|
|Organization|Global|Read, Write|Read, Write|Read, Write|
|Security Role|Global|||Read|
|User|Global|Create, Read, Write, Append, Append To|Create, Read, Write, Append, Append To|Create, Read, Write, Append, Append To|
|User Settings|Global|Create, Read, Write, Delete, Append To|Create, Read, Write, Delete, Append To|Create, Read, Write, Delete, Append To|
|Act on Behalf of Another User|Global|Yes|Yes|Yes|

##### <a name="customization" />Customization
|Security Role|Access Level|Dynamics NAV 2018 and Earlier|Business Central <br> October 2018|Business Central <br> April 2019|
|----|----|-----|----|----|
|Field|Global||Read|Read|
|Plug-in Assembly|Global|Read|Read|Read|
|Plug-in Type|Global|Read|Read|Read|
|SDK Message|Global|Read|Read|Read|
|SDK Message Processing Step|Global|Read|Read|Read|
|Web Resource|Global|Read|Read|Read|

##### <a name="custom-entities" />Custom Entities
|Security Role|Access Level|Dynamics NAV 2018 and Earlier|Business Central <br> October 2018|Business Central <br> April 2019|
|----|----|-----|----|----|
|Dynamics 365 Business Central Account Statistics|Global|Create, Read, Write, Append To|Create, Read, Write, Append To|Create, Read, Write, Append To|
|Dynamics 365 Business Central Connection|Global|Read|Read|Read|

### <a name="product-availability-user" />Product Availability User
You can allow sales people to view inventory levels for the items they sell by granting them the permissions described in the following table.

##### <a name="custom-entities" />Custom Entities
|Security Role|Access Level|Dynamics NAV 2018 and Earlier|Business Central <br> October 2018|Business Central <br> April 2019|
|----|----|-----|----|----|
|Dynamics 365 Business Central Account Statistics|Global|Create, Read, Write, Append To|Create, Read, Write, Append To|Create, Read, Write, Append To|
|Dynamics 365 Business Central Connection|Global|Read|Read|Read|

-->

## <a name="see-also" />Se også

[Integration med Microsoft Dataverse](admin-common-data-service.md)  
[Integration med Dynamics 365 Sales](admin-prepare-dynamics-365-for-sales-for-integration.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
