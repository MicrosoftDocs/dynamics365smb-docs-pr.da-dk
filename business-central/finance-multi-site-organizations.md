---
title: Business central til internationale organisationer med flere lokationer | Microsoft Docs
description: Business Central giver mulighed for at understøtte en hub-and-spoke-forretningsmodel.
author: brentholtorf
ms.topic: conceptual
ms.devlang: al
ms.search.keywords: 'hub-and-spoke, multi-site, headquarter, sites'
ms.date: 10/01/2020
ms.author: bholtorf
ms.service: dynamics-365-business-central
ms.reviewer: bholtorf
---

# Business Central til internationale organisationer med flere lokationer
Organisationer med flere lokationer bruger ofte en hub-and-spoke-forretningsmodel, hvor virksomheden eller hovedkontoret administrerer virksomhedens overordnede aktiviteter, mens hvert websted fungerer som en enkelt, selvstændig enhed. Websteder distribueres ofte geografisk og har forskellige behov for at dele oplysninger med hovedkvarteret. Desuden har websteder typisk ikke brug for det samme kompleksitetsniveau, og de mangler ofte ressourcerne til at opretholde et stort system.

[!INCLUDE[prod_short](includes/prod_short.md)] giver små og mellemstore virksomheder en løsning med forretningsstyring, der er let at bruge og for at sikre lave ejeromkostninger.

I denne artikel beskrives nogle af de måder, som [!INCLUDE[prod_short](includes/prod_short.md)] understøtter en hub-and-spoke-forretningsmodel.

## Integration af hovedkvarter og flere lokationer

[!INCLUDE[prod_short](includes/prod_short.md)] kan integreres med hovedkvarterets regnskabssystem, mens det opfylder forskellige websteders forskellige behov, uanset størrelse, placering eller virksomhedstype.

Følgende diagram er et eksempel på forskellige steder integreret med et hovedkvarter.

![Diagrambeskrivelse genereret automatisk.](media/multisite-headquarter-sites.png)

## Opfylde behovene på indenlandske og internationale lokationer

Virksomhedernes behov på steder er ofte forskellige afhængigt af industrien, forretningsmetoderne eller deres forhold til hovedkvarteret. [!INCLUDE[prod_short](includes/prod_short.md)] kan let tilpasses og udvides til forskellige typer virksomheder og standarder. Microsoft AppSource tilbyder en lang række apps fra Microsoft og vores partnere, og partnere kan hurtigt implementere [!INCLUDE[prod_short](includes/prod_short.md)] med minimal afbrydelse af daglige operationer.

I forbindelse med multinationale organisationer understøtter [!INCLUDE[prod_short](includes/prod_short.md)] lokale juridiske krav og forretningspraksis.

* Hvis der er onlineversioner, er der over [40 lokaliserede lande/områdeversioner](/dynamics365/business-central/dev-itpro/compliance/apptest-countries-and-translations?toc=/dynamics365/business-central/toc.json), som du kan installere som udvidelser fra Microsoft AppSource.  
* I lokale versioner er [lande/områdeversioner](/azure/architecture/solution-ideas/articles/business-central) enten tilgængelige som Microsoft-lokaliserede versioner eller tilføjelsesprogrammet af partnerstyrede lokaliseringer.

Et netværk med mere end 4.000 Microsoft-partnere over hele verden tilbyder lokal ekspertise.

| **Forretningsbehov** | **Sådan understøttes Business Central** | **Flere oplysninger** |
|-------------------------|-------------------------|-------------------------|
| Skræddersy systemet, så det passer til virksomheden. | Nyd et system, der er udviklet fra begyndelsen af mellemstore virksomheder. | [Oversigt](https://dynamics.microsoft.com/business-central/overview/) |
| Forskriftsmæssig og lokal praksis. | Overholde kravene til lokal og forretningsmæssig praksis. | [Lokal funktionalitet](about-localization.md) |
| Få adgang til flere firmaer fra en enkelt side. | Få hurtig adgang til alle Business Central-virksomheder i organisationen. | [Virksomhedshub](ui-extensions-company-hub.md) |
| Håndtere flere sprog og valutaer. | Understøttelsen af flere sprog og valutaer er med til at imødekomme lokale behov. | [Funktioner til flere sprog](about-locale-language.md)<br></br>[Funktioner til flere valutaer](finance-how-setup-additional-currencies.md) |


## Konsolidere finansielle data

En kernefacet for hub-and-spoke-forretningsmodellen er evnen til at hovedkvarteret og afdelingerne udveksler økonomiske data, også når hovedkvarter og afdelingerne bruger forskellige systemer, regnskabsstrukturer, sprog og valutaer.

| **Forretningsbehov** | **Sådan understøttes Business Central** | **Flere oplysninger** |
|-------------------------|-------------------------|-------------------------|
| Konsolidere finansielle data fra afdelinger. | Konsolidere regnskabsopgørelser for lokationer, uanset om de kører Business Central eller et andet program i en enkelt forretningsenhed (virksomhed). | [Konsolidering af finansielle oplysninger fra flere regnskaber](finance-consolidated-company-reporting.md) |
| Integrere regnskabsstrukturer. | Overfør konsolideringsdata fra forskellige regnskabsstrukturer til dine egne. Indbygget filformat til F&O (fås med Wave 2, 2020) | [Import af virksomhedsdata fra andre økonomisystemer](across-import-data-configuration-packages.md)<br></br>[Klargøre finanskonti til konsolidering](finance-consolidated-company-reporting-setup.md#glacc) |
| Transaktion i flere valutaer. | Være med til at sikre, at regnskabsopgørelser i forskellige valutaer er nøjagtige og korrekte valutakurser. | [Opdatere valutakurser](finance-how-update-currencies.md) |

## Dele forretningsindsigt med integreret analyse

Du kan tilpasse organisationen i forhold til forretningsmål ved at give dig en fælles forståelse af den aktuelle virkelighed. Integreret analyse kan hjælpe folk med at basere deres beslutninger på samme sæt oplysninger.

| **Forretningsbehov** | **Sådan understøttes Business Central** | **Flere oplysninger** |
|-------------------------|-------------------------|-------------------------|
| Dele indsigt med websteder uden omfattende IT-support. | Opret KPI'er og Business Intelligence-dashboards i Power BI baseret på dine data. | [Opret forbindelse til Power BI fra Business Central i det lokale miljø](across-working-with-business-central-in-powerbi.md) |
| Udarbejde brugerdefinerede finansrapporter. | Oprette parameterbaserede finansrapporter. | [Business Intelligence](bi.md) |
| Juster fakta. | Generere, få vist og dele rapporter med interne og eksterne involverede. | [Finansrapporter](finance-reports.md) |
| Analysere data i Excel. | Find fakta, fejlfind og foretag ad hoc-analyser i Microsoft Excel. | [Analysere regnskabsopgørelser i Excel](finance-analyze-excel.md) |


## Udveksle data ved hjælp af API'er og XML-porte

API'er og XML-porte gør det nemmere at forbinde forekomster af [!INCLUDE[prod_short](includes/prod_short.md)], herunder dem, der er tilpasset til hvert websted.

| **Forretningsbehov** | **Sådan understøttes Business Central** | **Flere oplysninger** |
|-------------------------|-------------------------|-------------------------|
| Forbinde tilpassede versioner mellem steder og hovedkvarteret. | API-sider kan vise enhver repræsentation af et objekt, herunder dets tilpasninger. | [Aktivere API'er til Business Central](/dynamics-nav/enabling-apis-for-dynamics-nav) |
| Versionering og sikkerhed. | API'er bruger ODataV4, som omfatter versionering, webhooks og registrering af ændringer. | [Sikkerhed og beskyttelse](/dynamics365/business-central/dev-itpro/security/security-and-protection) |
| Bogføre og importere XLM-dokumenter | Codeunits kan eksponeres som ubundne handlinger for at understøtte bogføring og indtagelse af XML-dokumenter. I forbindelse med behandling af XML-dokumenter kan XML-porte anvendes. Ubundne handlinger kan også generere et XML- eller JSON-dokument. | [XMLport Objekter](/dynamics365/business-central/dev-itpro/developer/devenv-xmlport-object) |
| Gøre vedligeholdelse nemmere gennem elektronisk dataudveksling. | Der kan tilføjes en elektronisk dataudvekslingsløsning for at fungere som et integrationslag mellem hovedkvarteret og afdelinger. | [Ramme for dataudveksling](across-about-the-data-exchange-framework.md) |
| Udveksle data mellem forskellige systemer. | Brug XML-porte til at oprette XML-dokumenter, som derefter kan udveksles mellem et hovedkvarter, der bruger ét system og afdelinger, der bruger Business Central. | [XMLport Oversigt](/dynamics365/business-central/dev-itpro/developer/devenv-xmlport-overview) |
| Organisering af komplekse dataudvekslinger. | Brug en kombination af XML-porte med Business Central og Microsoft BizTalk Server til at imødekomme specifikke behov i dine afdelinger.</br>Til komplekse behov skal du bruge en elektronisk dataudvekslingsløsning, der er baseret på BizTalk Server og Commerce Gateway i Business Central i kombination med XML-porte. | [Arbejde med rapporter, kørsler og XMLporte](ui-work-report.md) |
| Opret forbindelse til 3<sup>.</sup> partsløsninger og tjenester. | API'er opretter en punkt-til-punkt-forbindelse mellem Business Central og 3<sup>.</sup> parts løsninger og tjenester. | [API v2.0](/dynamics-nav/api-reference/v2.0/) |


## Forfremme en effektiv intern forsyningskæde

Afdelingerne har ofte brug for adgang til forsyningskæden og muligheden for at håndtere visse aspekter af den. F. eks. kan afdelingerne bruge samme leverandør, men administrere deres aktiver og fysiske lokationer separat.

| **Forretningsbehov** | **Sådan understøttes Business Central** | **Flere oplysninger** |
|-------------------------|-------------------------|-------------------------|
| Behandle inter-divisionstransaktioner som normale salgs- og købstransaktioner. | Bruge intercompany-bogføringer til at oprette salgs-og købsdokumenter og finansposter for hele arbejdsgange og for mere end én virksomhed ad gangen for at fjerne dobbeltdata indtastning. | [Administrere Intercompany-transaktioner](intercompany-manage.md) |
| Bruge processer, der ikke er på papir. | Undgå omkostningerne ved at sende, modtage og udskrive dokumenter. | [Indgående bilag](across-income-documents.md)<br><br> [Administrere vedhæftede filer, links og noter på kort og dokumenter](ui-how-add-link-to-record.md) |

## Reagere hurtigt på nye forretningsbetingelser

Hovedkvarteret skal kunne reagere hurtigt på forretningsændringer i hver afdeling. Kombineret med Power Automate kan [!INCLUDE[prod_short](includes/prod_short.md)] fungere som en tidlig advarselsmekanisme.

![Et skærmbillede af en beskrivelse af et socialt medieindlæg genereres automatisk.](media/multisite-apps.png)

| **Forretningsbehov** | **Sådan understøttes Business Central** | **Flere oplysninger** |
|-------------------------|-------------------------|-------------------------|
| Opret automatisk e-mailbeskeder. | Konfigurere påmindelser i Power Automate, der vil generere e-mails, der skal informere dig om vigtige forretningsbetingelser på steder eller i forsyningskædepartnere. | [Business Central og Power BI](admin-powerbi.md) |
| Bruge standard- eller brugerdefinerede beskeder. | Brug 12 forskellige skabeloner, der følger med Business Central, eller opsætte egne beskeder, så de passer til din virksomhed. | [Bruge Business Central i et automatisk workflow](across-how-use-financials-data-source-flow.md) |

## Se også
[Administrationsopgaver i Business Central Online](/dynamics365/business-central/dev-itpro/administration/tenant-administration)  
[Arbejd med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
