---
title: Integrer med Microsoft Dataverse via datasynkronisering
description: Introduktion til integration og brug af Microsoft Dataverse og komponenter til at oprette forbindelse til andre Dynamics 365-programmer.
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bholtorf
ms.topic: conceptual
ms.date: 03/08/2024
ms.custom: bap-template
ms.search.form: 7214_Primary
ms.service: dynamics-365-business-central
---

# Integrer med Microsoft Dataverse via datasynkronisering

Forretningsapps bruger ofte data fra mere end én kilde. [!INCLUDE[prod_short](includes/cds_long_md.md)] kombinerer data til et enkelt sæt logik, som gør det nemmere at forbinde [!INCLUDE[prod_short](includes/prod_short.md)] med andre Dynamics 365-programmer. F.eks. [!INCLUDE[crm_md](includes/crm_md.md)] eller dit eget program bygget på [!INCLUDE[prod_short](includes/cds_long_md.md)]. Du kan få mere at vide om [!INCLUDE[prod_short](includes/cds_long_md.md)] ved at gå til [Hvad er Dataverse?](/powerapps/maker/common-data-service/data-platform-intro).

Nedenfor følger en oversigt over trinnene til integration af [!INCLUDE[prod_short](includes/cds_long_md.md)] med [!INCLUDE[prod_short](includes/prod_short.md)].

> [!Note]  
> Disse opgaver kræver sikkerhedsrollen **Systemadministrator** i [!INCLUDE[prod_short](includes/cds_long_md.md)] og [!INCLUDE[prod_short](includes/prod_short.md)].  

1. Tildel licenser til [!INCLUDE[prod_short](includes/cds_long_md.md)] til de [!INCLUDE[prod_short](includes/prod_short.md)]-brugere, der skal bruge de integrerede apps.

2. Opret en forbindelse til [!INCLUDE[prod_short](includes/cds_long_md.md)]. Du kan få flere oplysninger i [Forbind til Dataverse](admin-how-to-set-up-a-dynamics-crm-connection.md).  

3. Synkroniser data mellem programmer. Du kan finde flere oplysninger i [Synkronisering af Business Central og Dataverse](admin-synchronizing-business-central-and-sales.md). 

## Kom i gang med [!INCLUDE[prod_short](includes/cds_long_md.md)]

For at komme i gang med [!INCLUDE[prod_short](includes/cds_long_md.md)] skal du have en Microsoft Power Apps-konto. Hvis du ikke allerede har en Power Apps-konto, kan du få en gratis adresse ved at besøge [powerapps.com](https://make.powerapps.com/?utm_source=padocs&utm_medium=linkinadoc&utm_campaign=referralsfromdoc) og vælge hyperlinket **Kom gratis i gang**. Du kan få mere at vide om, hvordan du kommer i gang med [!INCLUDE[prod_short](includes/cds_long_md.md)] i modulet [Kom i gang med Dataverse](/training/modules/get-started-with-powerapps-common-data-service/) fra Microsoft-træning.

## Tovejs eller etvejs datasynkronisering

Du kan synkronisere data enten til eller fra en Dynamics 365-forretningsapp til en anden eller i begge retninger og næsten i realtid via [!INCLUDE[prod_short](includes/cds_long_md.md)]. Hvis du f.eks. integrerer [!INCLUDE[prod_short](includes/prod_short.md)] med [!INCLUDE[crm_md](includes/crm_md.md)], kan en sælger oprette en salgsordre i [!INCLUDE[crm_md](includes/crm_md.md)], hvorefter ordren synkroniseres til [!INCLUDE[prod_short](includes/prod_short.md)]. Fra [!INCLUDE[crm_md](includes/crm_md.md)] kan sælgeren ligeledes se tilgængelighed for objektet i ordren i [!INCLUDE[prod_short](includes/prod_short.md)]. 

## Standardobjekter og brugerdefinerede objekter

[!INCLUDE[prod_short](includes/cds_long_md.md)] gemmer data sikkert i en række tabeller, som er postsæt, der svarer til, hvordan en tabel gemmer data i en database. [!INCLUDE[prod_short](includes/cds_long_md.md)] indeholder et grundlæggende sæt standardtabeller, der dækker typiske scenarier, men du kan også oprette brugerdefinerede tabeller, der er specifikke for din virksomhed. I [!INCLUDE[prod_short](includes/prod_short.md)] kan du se de standardobjekter og brugerdefinerede tabeller, der synkroniseres, på siden Integrationstabeltilknytninger.

## Om Business Central-basisintegrationsløsningen

Business Central-basisintegrationsløsningen er en nøglekomponent i integrationen. Løsningen føjer de nødvendige roller og adgangsniveauer til brugerkontiene for integrationen og opretter de tabeller, der kræves for at knytte [!INCLUDE[prod_short](includes/prod_short.md)]-virksomheden til en afdeling i [!INCLUDE[prod_short](includes/cds_long_md.md)]. 

Som standard vil vejledningen til **Opsætning af [!INCLUDE[prod_short](includes/cds_long_md.md)]-forbindelse** med assisteret opsætning importere løsningen. For at gøre dette bruger opsætningsvejledningen en administratorbrugerkonto, som du angiver. Denne konto skal være en gyldig bruger i [!INCLUDE[prod_short](includes/cds_long_md.md)] med sikkerhedsrollen **Systemadministrator**.  

Hvis du vil vide mere om brugerkonti, skal du gå til følgende artikler:

* [Konfigurere brugerkonti til integration med [!INCLUDE[prod_short](includes/cds_long_md.md)]](admin-setting-up-integration-with-dynamics-sales.md) 
* [Oprette brugere i Microsoft Dynamics 365 (online) og tildele sikkerhedsroller](/dynamics365/customer-engagement/admin/create-users-assign-online-security-roles). 

Administratorkontoen bruges kun én gang i løbet af opsætningen til de konfigurationsændringer, som Business Central-basisintegrationsløsningen udfører i [!INCLUDE[prod_short](includes/cds_long_md.md)]. Når løsningen er importeret, er kontoen ikke længere nødvendig. Integrationen fortsætter med at bruge den brugerkonto, der er automatisk oprettet specielt til integrationen.

Ud over at tilpasse [!INCLUDE [cds_long_md](includes/cds_long_md.md)] opretter løsningen desuden en sikkerhedsrolle i [!INCLUDE [cds_long_md](includes/cds_long_md.md)] til integrationen:

* **Business Central Dataverse Integration** - Gør det muligt at styre forbindelsen mellem [!INCLUDE [prod_short](includes/prod_short.md)] og [!INCLUDE [cds_long_md](includes/cds_long_md.md)]. Denne rolle knyttes som regel kun til den brugerkonto, der oprettes automatisk til synkronisering. Du kan lære mere om denne rolle ved at gå til [Opsætning af brugerkonti til integration med [!INCLUDE[prod_short](includes/cds_long_md.md)]](admin-setting-up-integration-with-dynamics-sales.md).

Når du konfigurerer forbindelsen, oprettes de integrationstabeltilknytninger, der er nødvendige for at synkronisere data. Objekter i [!INCLUDE[prod_short](includes/cds_long_md.md)] knyttes til tabeller og tabelfelter i [!INCLUDE [prod_short](includes/prod_short.md)] ved hjælp af integrationstabeller. Hvis du vil vide mere om tilknytning, skal du gå til [Standardobjekttilknytning for synkronisering](admin-synchronizing-business-central-and-sales.md#standard-table-mapping-for-synchronization).

## Håndter forskelle i lokale og grundlæggende transaktionsvalutaer

Du kan oprette forbindelse til et [!INCLUDE[prod_short](includes/cds_long_md.md)]-miljø med en anden grundvaluta end den lokale valuta i [!INCLUDE[prod_short](includes/prod_short.md)]. Du opretter forbindelsen i [!INCLUDE[prod_short](includes/prod_short.md)] på siden **Dataverse-konfiguration af forbindelse** eller ved at bruge **Installationsforbindelsen til Dataverse**-assisteret opsætningsvejledning.

Hvis du vil oprette forbindelse, skal du kontrollere, at valutaindstillingen i [!INCLUDE[prod_short](includes/cds_long_md.md)] har basisvaluta angivet på siden **Valutaer** i [!INCLUDE [prod_short](includes/prod_short.md)], og at der er angivet mindst én valutakurs for valutaen på siden **Valutakurser**.

Her er et eksempel. Du opretter forbindelse mellem [!INCLUDE[prod_short](includes/cds_long_md.md)] og Euro (EUR) som lokal valuta på siden **Opsætning af Finans** til et [!INCLUDE[prod_short](includes/cds_long_md.md)]-miljø, hvor der er angivet en basistransaktionsvaluta til US dollar (USD). Du skal bruge USD på siden **Valutaer** i [!INCLUDE [prod_short](includes/prod_short.md)] og den relevante valutakurs. 

Når du aktiverer forbindelsen til [!INCLUDE[prod_short](includes/cds_long_md.md)], tilføjer [!INCLUDE [prod_short](includes/prod_short.md)] den lokale valuta til feltet **Valuta** i [!INCLUDE[prod_short](includes/cds_long_md.md)] med valutakursen fra feltet **Valutafaktor** på siden **Valutakurser**.

Synkronisering af valuta er envejs, fra [!INCLUDE [prod_short](includes/prod_short.md)] til [!MEDTAG [!INCLUDE[prod_short](includes/cds_long_md.md)], monetære beløb konverteres og synkroniseres på følgende måde:

* Beløbene i [!INCLUDE[prod_short](includes/cds_long_md.md)]-basisvalutaen konverteres til den [!INCLUDE [prod_short](includes/prod_short.md)] lokale valuta ud fra den seneste valutakurs, der er synkroniseret fra [!INCLUDE [prod_short](includes/prod_short.md)].
* Beløb i den [!INCLUDE [prod_short](includes/prod_short.md)] lokale valuta synkroniseres med den [!INCLUDE [prod_short](includes/prod_short.md)] lokale valuta i en af de andre (ikke-basis) valutaer i [!INCLUDE[prod_short](includes/cds_long_md.md)].

## Hvad sker der, når du kopierer en virksomhed?

Du kan trygt kopiere virksomheder, der integrerer med [!INCLUDE[prod_short](includes/cds_long_md.md)] eller [!INCLUDE[crm_md](includes/crm_md.md)]. Kopiering af virksomheder hjælper med at reducere risikoen for datauoverensstemmelser og kan spare dig værdifuld tid. Du kan få mere at vide om kopiering af virksomheder ved at gå til [Kopiere et regnskab](about-new-company.md#copy-a-company).

[!INCLUDE [dataverse-copy-company](includes/dataverse-copy-company.md)]

## Se også

[Modeller for dataejerskab](admin-cds-company-concept.md)  
<!--needs to be removed as this is moved to dev-itpro docs[Walkthrough: Customizing an Integration with Dataverse](\dynamics365\business-central\dev-itpro\administration\administration-custom-cds-integration) -->


[!INCLUDE[footer-include](includes/footer-banner.md)]
