---
title: Tilknytning af virksomhed og afdeling | Microsoft Docs
description: Virksomheder er både juridiske og virksomhedsmæssige strukturer, og de bruges til at sikre og visualisere forretningsdata.
author: bholtorf
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: CDS, Common Data Service, integration, sync
ms.date: 10/01/2020
ms.author: bholtorf
ms.openlocfilehash: 4f8e5959098e01cd08134a37ae706aa852d88729
ms.sourcegitcommit: ddbb5cede750df1baba4b3eab8fbed6744b5b9d6
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 10/01/2020
ms.locfileid: "3911652"
---
# <a name="data-ownership-models"></a>Modeller for ejerskab af data
[!INCLUDE[d365fin](includes/cds_long_md.md)] kræver, at du angiver en ejer af de data, du gemmer. Du kan få flere oplysninger i [Ejerskab af objekter](https://docs.microsoft.com/powerapps/maker/common-data-service/types-of-entities#entity-ownership) i Power Apps-dokumentationen. Når du konfigurerer integrationen mellem [!INCLUDE[d365fin](includes/cds_long_md.md)] og [!INCLUDE[d365fin](includes/d365fin_md.md)], skal du vælge en af to ejerskabsmodeller til poster, der er synkroniserede:

* Team 
* Person (bruger)

Handlinger, der kan udføres på disse poster, kan styres på et brugerniveau. Du kan få flere oplysninger i [Bruger- og teamobjekter](https://docs.microsoft.com/powerapps/developer/common-data-service/user-team-entities). Vi anbefaler modellen Teamejerskab, da den gør det nemmere at administrere ejerskab for flere personer.

## <a name="team-ownership"></a>Teamejerskab
I [!INCLUDE[d365fin](includes/d365fin_md.md)] er en virksomhed et juridisk og virksomhedsmæssigt objekt, der kan bruges til at sikre og visualisere forretningsdata. Brugere arbejder altid i en virksomheds kontekst. Det tætteste, som [!INCLUDE[d365fin](includes/cds_long_md.md)] kommer på dette begreb, er virksomhedsafdelingsobjektet, som ikke har juridiske eller forretningsmæssige konsekvenser.

Da forretningsenheder ikke har nogen juridiske og forretningsmæssige konsekvenser, kan du ikke gennemtvinge en-til-en-tilknytning (1:1) mellem en virksomhed og en koncernvirksomhed, enten etvejs eller tovejs. Hvis du vil gøre synkroniseringen mulig, når du aktiverer synkronisering for en virksomhed i [!INCLUDE[d365fin](includes/d365fin_md.md)], sker der følgende i [!INCLUDE[d365fin](includes/cds_long_md.md)]:

* Vi opretter et forretningsobjekt, der svarer til virksomhedsobjektet i [!INCLUDE[d365fin](includes/d365fin_md.md)]. Navnet på virksomheden har suffikset "BC-virksomheds-ID". Cronus International Ltd. har for eksempel (93555b1a-af3e-ea11-bb35-000d3a492db1).
* Vi opretter en standard-virksomhedsafdeling, der har samme navn som virksomheden. Cronus International Ltd. har for eksempel (93555b1a-af3e-ea11-bb35-000d3a492db1).
* Vi opretter en særskilt ejergruppe med samme navn som virksomheden og knytter den til afdelingen. Navnet på teamet har præfikset "BCI-". BCI - Cronus International Ltd. har for eksempel (93555b1a-af3e-ea11-bb35-000d3a492db1).
* Poster, der oprettes og synkroniseres til [!INCLUDE[d365fin](includes/cds_long_md.md)], knyttes til den "BCI-ejer"-gruppe, som er knyttet til afdelingen.

> [!NOTE]
> Hvis du omdøber et firma i [!INCLUDE[d365fin](includes/d365fin_md.md)], opdateres navnene på virksomheden, forretningen og det team, som vi opretter automatisk i [!INCLUDE[d365fin](includes/cds_long_md.md)], ikke. Da det kun er virksomheds-id'et, der bruges til integration, påvirker dette ikke synkroniseringen. Hvis navnene skal stemme overens, skal du opdatere virksomheden, afdelingen og teamet i [!INCLUDE[d365fin](includes/cds_long_md.md)].

Følgende billede viser et eksempel på dataopsætning i [!INCLUDE[d365fin](includes/cds_long_md.md)].

![Rodafdelingen er øverst, er grupperne er i midten, og derefter er virksomhederne nederst.](media/cds_bu_team_company.png)

I denne konfiguration ejes poster, der er relateret til virksomheden Cronus US, af en gruppe, der er knyttet til Cronus US-<ID>afdelingen i [!INCLUDE[d365fin](includes/cds_long_md.md)]. Brugere, som kan få adgang til denne afdeling via en sikkerhedsrolle, der er indstillet til at vise synlighed på forretningsniveau i [!INCLUDE[d365fin](includes/cds_long_md.md)], kan nu se disse poster. Følgende eksempel viser, hvordan du kan bruge teams til at give adgang til disse poster.

* Rollen Salgschef tildeles til medlemmer af Cronus US-salgsteamet.
* Brugere med rollen Salgschef kan få adgang til kontoposter for medlemmer af samme afdeling.
* Cronus US-salgsgruppen er kædet sammen med den Cronus US-afdeling, der er nævnt tidligere. Medlemmer af Cronus US-salgsteamet kan se alle de virksomheder, der tilhører Cronus US<ID>-brugeren, som ville være kommet fra Cronus US-objektet i [!INCLUDE[d365fin](includes/d365fin_md.md)].

Men 1:1-tilknytningen mellem afdelingen, virksomheden og teamet er kun udgangspunktet som vist på følgende billede.

![Sikkerhedsrollen styrer datasynlighed.](media/cds_bu_team_company_2.png)

I dette eksempel oprettes der en ny rod for en EUR-afdeling (Europa) i [!INCLUDE[d365fin](includes/cds_long_md.md)] som overordnet for både Cronus DE (Tyskland) og Cronus ES (Spanien). EUR-afdelingen er ikke relateret til synkronisering. Den kan dog give medlemmer af EUR-salgsteamet adgang til kontodata i både Cronus DE og Cronus ES ved at angive datasynligheden for **Overordnet/underordnet afdeling** på den tilknyttede sikkerhedsrolle i [!INCLUDE[d365fin](includes/cds_long_md.md)].

Synkroniseringen bestemmer, hvilket team der skal eje regnskaber. Dette styres af feltet **Standard-ejerteam** i BCI - <ID>-posten. Når en BCI- <ID>-post er aktiveret til synkronisering, opretter vi automatisk den tilknyttede afdeling og ejerens team (hvis det ikke allerede findes) og udfylder feltet **Standard-ejerteam**. Når synkronisering er aktiveret for et objekt, kan administratorer ændre ejerteamet, men der skal altid tildeles et team.

> [!NOTE]
> Posterne bliver skrivebeskyttet, når en virksomhed er blevet tilføjet og gemt. Derfor skal du sørge for at vælge den rigtige virksomhed.

## <a name="choosing-a-different-business-unit"></a>Sådan vælger du en anden afdeling
Du kan vælge en ny afdeling, hvis du bruger ejerskabsmodellen Teams. Hvis du bruger ejerskabsmodellen Person, vælges standardafdelingen altid. 

Hvis du vælger en anden afdeling, f. eks den, som du har oprettet tidligere i [!INCLUDE[d365fin](includes/cds_long_md.md)], beholder den sit oprindelige navn. Det vil sige, at den ikke får et suffiks med virksomheds-id'et. Vi opretter et team, der bruger navngivningskonventionen.

Når du ændrer en afdeling, kan du kun vælge de afdelinger, der er ét niveau under rodafdelingen.

## <a name="person-ownership"></a>Personejerskab
Hvis du vælger modellen Personejerskab, skal du angive hver sælger, der skal eje nye poster. Afdelingen og teamet oprettes som beskrevet i sektionen [Teamejerskab](admin-cds-company-concept.md#team-ownership).

Standardafdelingen bruges, når ejerskabsmodellen Person vælges, og du kan ikke vælge en anden afdeling. Det team, der er knyttet til standardafdelingen, vil eje poster for fælles objekter, f. eks. produktobjekter, som ikke er knyttet til bestemte sælgere.

Når du sætter sælgere i [!INCLUDE[d365fin](includes/d365fin_md.md)] sammen med brugere i [!INCLUDE[d365fin](includes/cds_long_md.md)], [!INCLUDE[d365fin](includes/d365fin_md.md)], tilføjes brugeren til standardteamet i [!INCLUDE[d365fin](includes/cds_long_md.md)]. Du kan kontrollere, at brugerne er tilføjet ved at se på **Standardteammedlem** på siden **Brugere - Common Data Service**. Hvis brugeren ikke er tilføjet, kan du tilføje dem manuelt ved hjælp af handlingen **Tilføj sammenkødede brugere til team**. Du kan finde flere oplysninger under [Synkronisering af data i Business Central med Common Data Service](admin-synchronizing-business-central-and-sales.md).

## <a name="see-also"></a>Se også
[Om [!INCLUDE[d365fin](includes/cds_long_md.md)]](admin-common-data-service.md)