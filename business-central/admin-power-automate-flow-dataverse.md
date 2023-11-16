---
title: Brug et Power Automate-flow til beskeder om ændringer af enheden
description: 'Få mere at vide om, hvordan du opretter et flow i Power Automate, der giver dig besked, når en enhed ændres i Dataverse-miljøet.'
author: brentholtorf
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 'Power Automate, Flow, Dataverse'
ms.search.form: null
ms.date: 09/05/2022
ms.author: bholtorf
---
# <a name="use-a-power-automate-flow-to-timely-synchronize-dataverse-entity-changes"></a>Brug et Power Automate-flow til beskeder til Dataverse om ændringer af enheden

Administratorer kan oprette et automatiseret flow i Power Automate, som giver din [!INCLUDE[prod_short](includes/prod_short.md)] besked om ændringer af poster i [!INCLUDE [cds_long_md](includes/cds_long_md.md)]-organisationen.

> [!NOTE]
> I denne artikel antages det, at du har tilsluttet din onlineversion af [!INCLUDE[prod_short](includes/prod_short.md)] med [!INCLUDE [cds_long_md](includes/cds_long_md.md)] og planlagt synkronisering mellem de to programmer.

## <a name="import-the-flow-template"></a>Importer Flow-skabelonen

> [!TIP]
> Vi har oprettet en skabelon, der definerer flowudløseren og flowbetingelsen for dig, for at gøre det nemmere at opsætte flowet. Hvis du vil bruge skabelonen, skal du følge fremgangsmåden i dette afsnit. Hvis du selv vil oprette et flow, skal du springe dette afsnit over og starte med trinnene i [Definer flowudløseren](#define-the-flow-trigger).

1. Log på [Power Automate](https://powerautomate.microsoft.com).
2. Vælg **Skabeloner**, og søg efter **Giv Business Central besked**.

:::image type="content" source="media/power-automate-import-template.png" alt-text="Nøgleord for at finde flowskabelonen.":::
3. Vælg **Giv Business Central besked, når en konto skifter** skabelon.
4. Gå videre til trinene i sektionen [Giv Business Central besked om en ændring](#notify-business-central-about-a-change).

## <a name="define-the-flow-trigger"></a>Definer flowudløseren

1. Log på [Power Automate](https://flow.microsoft.com).
2. Opret et automatiseret cloudflow, der starter, når en række til et [!INCLUDE [cds_long_md](includes/cds_long_md.md)]-objekt tilføjes, ændres eller slettes. Flere oplysninger i [Udløs flows, når en række tilføjes, ændres eller slettes](/power-automate/dataverse/create-update-delete-trigger). I dette eksempel bruges objektet **Firmaer**. Følgende billede viser indstillingerne for det første trin til definition af en flowudløser.

:::image type="content" source="media/power-automate-flow-dataverse-trigger.png" alt-text="Indstillinger for flowets udløser":::
3. Brug knappen **AssistEdit (...)** i øverste højre hjørne til at tilføje forbindelsen til [!INCLUDE [cds_long_md](includes/cds_long_md.md)]-miljøet.
4. Vælg **Vis avancerede indstillinger**, og Indtast **customertypecode EQ 3** eller **customertypecode EQ 11** og **statecode EQ 0** i feltet **Filtrer rækker**. Disse værdier betyder, at udløseren kun reagerer, når der er foretaget ændringer af de aktive konti af typen **kunde** eller **leverandør**.

## <a name="define-the-flow-condition"></a>Definer flowbetingelsen

Data synkroniseres mellem [!INCLUDE[prod_short](includes/prod_short.md)] og [!INCLUDE [cds_long_md](includes/cds_long_md.md)] via en integrationsbrugerkonto. Hvis du vil ignorere de ændringer, der er foretaget af synkroniseringen, skal du oprette et betingelsestrin i flowet, som udelukker ændringer, der er foretaget af integrationsbruger kontoen.  

1. Tilføj et **Hent en række efter id fra Dataverse**-trin efter flowudløseren med følgende indstillinger. Du kan finde flere oplysninger i [Hent en række efter id fra Dataverse](/power-automate/dataverse/get-row-id).

    1. I feltet **Tabelnavn** skal du vælge **Brugere**
    2. I feltet **Række-id** skal du vælge **Ændret af (værdi)** fra flowudløseren.  

2. Tilføj et betingelsestrin med følgende **eller**-Indstillinger for at identificere brugerkontoen til integration.
    1. Brugerens **primære e-mail-adresse** indeholder **contoso.com**
    2. Brugerens **fulde navn** indeholder **[!INCLUDE[prod_short](includes/prod_short.md)]**.

3. Tilføj en afslutningskontrol for at stoppe flowet, hvis objektet blev ændret af integrationsbrugerkontoen.

Følgende billede viser, hvordan flowudløseren og flowbetingelsen defineres.

:::image type="content" source="media/power-automate-flow-dataverse.png" alt-text="Oversigt over indstillinger for flowudløsere og betingelser":::

## <a name="notify-business-central-about-a-change"></a>Giv Business Central besked om en ændring

Hvis flowet ikke stoppes af betingelsen, skal du give besked [!INCLUDE[prod_short](includes/prod_short.md)] om, at der er foretaget en ændring. Brug [!INCLUDE[prod_short](includes/prod_short.md)]-connectoren til det.

1. I fork **Ingen** af betingelsestrinnet skal du tilføje en handling og søge efter **Dynamics 365 [!INCLUDE[prod_short](includes/prod_short.md)]**. Vælg connector-ikonet på listen.
2. Vælg handlingen **Opret post (V3)**.

:::image type="content" source="media/power-automate-flow-dataverse-connector.png" alt-text="Indstillinger for [!MEDTAG[prod_short](includes/prod_short.md)] Connector":::

3. Brug knappen **Assisteret redigering (...)** i øverste højre hjørne til at tilføje forbindelsen til [!INCLUDE[prod_short](includes/prod_short.md)].
4. Udfyld felter **miljønavn** og **firmanavn**, når du har oprettet forbindelse.
5. I feltet **API-kategori** skal du angive **Microsoft/dataverse/v 1.0**.
6. I feltet **Tabelnavn** skal du angive **dataverseEntityChanges**.
7. Indtast **Konto** i feltet **entityName**.
8. Gem flowet.

Følgende billede viser, hvordan dit flow bør se ud.

:::image type="content" source="media/power-automate-flow-dataverse-summary.png" alt-text="Oversigt over alle indstillinger for flowet":::

Når du tilføjer, sletter eller ændrer en konto i dit [!INCLUDE [cds_long_md](includes/cds_long_md.md)]-miljø, foretager dette flow følgende handlinger:

1. Ring til det [!INCLUDE[prod_short](includes/prod_short.md)]-miljø, du har angivet i [!INCLUDE[prod_short](includes/prod_short.md)]-connectoren.
2. Brug [!INCLUDE[prod_short](includes/prod_short.md)]-API til at indsætte en post med navnet **Enhedsnavn** angivet for **kontoen** i tabellen **Dataverse-postændring**. Denne parameter er det præcise navn på det Dataverse-objekt, du opretter flowet for.
3. [!INCLUDE[prod_short](includes/prod_short.md)] starter opgavekøposten, der synkroniserer debitorer med firmaer.

## <a name="see-also"></a>Se også

[Bruge Business Central i Power Automate Flows](across-how-use-financials-data-source-flow.md)  
[Konfigurere automatiserede workflows](/dynamics365/business-central/dev-itpro/powerplatform/automate-workflows)  
[Integration med Microsoft Dataverse](admin-common-data-service.md)  
[Synkronisering af data i Business Central med Microsoft Dataverse](admin-synchronizing-business-central-and-sales.md)  
