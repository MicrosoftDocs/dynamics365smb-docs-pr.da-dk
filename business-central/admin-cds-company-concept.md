---
title: Dataejerskabsmodeller til synkronisering
description: 'Virksomheder er både juridiske og virksomhedsmæssige strukturer, og de bruges til at sikre og visualisere forretningsdata.'
author: brentholtorf
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 'CDS, Dataverse, integration, sync'
ms.date: 04/01/2021
ms.author: bholtorf
---

# Dataejerskabsmodeller til synkronisering

[!INCLUDE[prod_short](includes/cds_long_md.md)] kræver, at du angiver en ejer af de data, du gemmer. Du kan få flere oplysninger i [Tabeltyper](/powerapps/maker/data-platform/types-of-entities) i Power Apps-dokumentationen. Når du konfigurerer integrationen mellem [!INCLUDE[prod_short](includes/cds_long_md.md)] og [!INCLUDE[prod_short](includes/prod_short.md)], skal du vælge ejerskabet **Bruger eller team** for de poster, der skal synkroniseres. Handlinger, der kan udføres på disse poster, kan styres på et brugerniveau. <!--We recommend the Team ownership model because it makes it easier to manage ownership for multiple people.NO LONGER TRUE IN DATAVERSE-->

## Teamejerskab
I [!INCLUDE[prod_short](includes/prod_short.md)], en virksomhed en juridisk og virksomhedsmæssig tabel, der kan bruges til at sikre og visualisere forretningsdata. Brugere arbejder altid i en virksomheds kontekst. Det tætteste, som [!INCLUDE[prod_short](includes/cds_long_md.md)] kommer på dette begreb, er virksomhedsafdelingstabeller, som ikke har juridiske eller forretningsmæssige konsekvenser.

Da forretningsenheder ikke har nogen juridiske og forretningsmæssige konsekvenser, kan du ikke gennemtvinge en-til-en-tilknytning (1:1) mellem en virksomhed og en koncernvirksomhed, enten etvejs eller tovejs. Hvis du vil gøre synkroniseringen mulig, når du aktiverer synkronisering for en virksomhed i [!INCLUDE[prod_short](includes/prod_short.md)], sker der følgende i [!INCLUDE[prod_short](includes/cds_long_md.md)]:

* Vi opretter en forretningstabel, der svarer til virksomhedstabeller i [!INCLUDE[prod_short](includes/prod_short.md)]. Navnet på virksomheden har suffikset "BC-virksomheds-ID". Cronus International Ltd. har for eksempel (93555b1a-af3e-ea11-bb35-000d3a492db1).
* Vi opretter en standard-virksomhedsafdeling, der har samme navn som virksomheden. Cronus International Ltd. har for eksempel (93555b1a-af3e-ea11-bb35-000d3a492db1).
* Vi opretter en særskilt ejergruppe med samme navn som virksomheden og knytter den til afdelingen. Navnet på teamet har præfikset "BCI-". BCI - Cronus International Ltd. har for eksempel (93555b1a-af3e-ea11-bb35-000d3a492db1).
* Poster, der oprettes og synkroniseres til [!INCLUDE[prod_short](includes/cds_long_md.md)], knyttes til den "BCI-ejer"-gruppe, som er knyttet til afdelingen.

> [!NOTE]
> Hvis du omdøber et firma i [!INCLUDE[prod_short](includes/prod_short.md)], opdateres navnene på virksomheden, forretningen og det team, som vi opretter automatisk i [!INCLUDE[prod_short](includes/cds_long_md.md)], ikke. Da det kun er virksomheds-id'et, der bruges til integration, påvirker dette ikke synkroniseringen. Hvis navnene skal stemme overens, skal du opdatere virksomheden, afdelingen og teamet i [!INCLUDE[prod_short](includes/cds_long_md.md)].

Følgende billede viser et eksempel på dataopsætning i [!INCLUDE[prod_short](includes/cds_long_md.md)].

![Rodafdelingen er øverst, er grupperne er i midten, og derefter er virksomhederne nederst.](media/cds_bu_team_company.png)

I denne konfiguration ejes poster, der er relateret til virksomheden Cronus US, af en gruppe, der er knyttet til Cronus US-afdelingen i [!INCLUDE[prod_short](includes/cds_long_md.md)]. Brugere, som kan få adgang til denne afdeling via en sikkerhedsrolle, der er indstillet til at vise synlighed på forretningsniveau i [!INCLUDE[prod_short](includes/cds_long_md.md)], kan nu se disse poster. Følgende eksempel viser, hvordan du kan bruge teams til at give adgang til disse poster.

* Rollen Salgschef tildeles til medlemmer af Cronus US-salgsteamet.
* Brugere med rollen Salgschef kan få adgang til kontoposter for medlemmer af samme afdeling.
* Cronus US-salgsgruppen er kædet sammen med den Cronus US-afdeling, der er nævnt tidligere. Medlemmer af Cronus US-salgsteamet kan se alle de virksomheder, der tilhører Cronus US-brugeren, som ville være kommet fra Cronus US-tabelen i [!INCLUDE[prod_short](includes/prod_short.md)].

Men 1:1-tilknytningen mellem afdelingen, virksomheden og teamet er kun udgangspunktet som vist på følgende billede.

![Sikkerhedsrollen styrer datasynlighed.](media/cds_bu_team_company_2.png)

I dette eksempel oprettes der en ny rod for en EUR-afdeling (Europa) i [!INCLUDE[prod_short](includes/cds_long_md.md)] som overordnet for både Cronus DE (Tyskland) og Cronus ES (Spanien). EUR-afdelingen er ikke relateret til synkronisering. Den kan dog give medlemmer af EUR-salgsteamet adgang til kontodata i både Cronus DE og Cronus ES ved at angive datasynligheden for **Overordnet/underordnet afdeling** på den tilknyttede sikkerhedsrolle i [!INCLUDE[prod_short](includes/cds_long_md.md)].

Synkroniseringen bestemmer, hvilket team der skal eje regnskaber. Dette styres af feltet **Standard-ejerteam** i BCI-rækken. Når en BCI-post er aktiveret til synkronisering, opretter vi automatisk den tilknyttede afdeling og ejerens team (hvis det ikke allerede findes) og udfylder feltet **Standard-ejerteam**. Når synkronisering er aktiveret for en tabel, kan administratorer ændre ejerteamet, men der skal altid tildeles et team.

> [!NOTE]
> Posterne bliver skrivebeskyttet, når en virksomhed er blevet tilføjet og gemt. Derfor skal du sørge for at vælge den rigtige virksomhed.

## Sådan vælger du en anden afdeling
Du kan vælge en ny afdeling, hvis du bruger ejerskabsmodellen Teams. Hvis du bruger ejerskabsmodellen Person, vælges standardafdelingen altid. 

Hvis du vælger en anden afdeling, f. eks den, som du har oprettet tidligere i [!INCLUDE[prod_short](includes/cds_long_md.md)], beholder den sit oprindelige navn. Det vil sige, at den ikke får et suffiks med virksomheds-id'et. Vi opretter et team, der bruger navngivningskonventionen.

Når du ændrer en afdeling, kan du kun vælge de afdelinger, der er ét niveau under rodafdelingen.

## Personejerskab
Hvis du vælger modellen Personejerskab, skal du angive hver sælger, der skal eje nye poster. Afdelingen og teamet oprettes som beskrevet i sektionen [Teamejerskab](admin-cds-company-concept.md#team-ownership).

Standardafdelingen bruges, når ejerskabsmodellen Person vælges, og du kan ikke vælge en anden afdeling. Det team, der er knyttet til standardafdelingen, vil eje poster for fælles tabeller, f.eks. produkttabeller, som ikke er knyttet til bestemte sælgere.

Når du sætter sælgere i [!INCLUDE[prod_short](includes/prod_short.md)] sammen med brugere i [!INCLUDE[prod_short](includes/cds_long_md.md)], [!INCLUDE[prod_short](includes/prod_short.md)], tilføjes brugeren til standardteamet i [!INCLUDE[prod_short](includes/cds_long_md.md)]. Du kan kontrollere, at brugerne er tilføjet ved at se på **Standardteammedlem** på siden **Brugere - Common Data Service**. Hvis brugeren ikke er tilføjet, kan du tilføje dem manuelt ved hjælp af handlingen **Tilføj sammenkødede brugere til team**. Du kan finde flere oplysninger i [Synkronisering af data i Business Central med Dataverse](admin-synchronizing-business-central-and-sales.md).

## Se også
[Om [!INCLUDE[prod_short](includes/cds_long_md.md)]](admin-common-data-service.md)

[!INCLUDE[footer-include](includes/footer-banner.md)]