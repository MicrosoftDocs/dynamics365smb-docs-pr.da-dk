---
title: Integrere med Microsoft Dynamics 365 Field Service
description: Integrer Business Central med Field Service.
ms.date: 02/21/2024
ms.topic: article
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bholtorf
ms.custom: bap-template
---

# <a name="integrate-with-microsoft-dynamics-365-field-service"></a>Integrere med Microsoft Dynamics 365 Field Service

Serviceorganisationer kræver et front-to-back-program, hvor økonomi, lager og indkøb er tæt forbundet med servicelevering. De genererer økonomiske data med hver transaktion. Hver arbejdsordre repræsenterer omkostninger og indtægter, og hver ressource genererer overskud og tab. Debitorinteraktioner tilføjer poster i finansmodulet. Integrationen mellem [!INCLUDE [prod_short](includes/prod_short.md)] og [!INCLUDE [field-service-short](includes/field-service-short.md)] strømliner end-to-end-processen til styring af serviceoperationer og sikrer en jævn informationsstrøm mellem de to systemer.  

Du kan nemt oprette og administrere arbejdsordrer i [!INCLUDE [field-service-short](includes/field-service-short.md)], spore status for serviceopgaver, tildele ressourcer og registrere forbrugsoplysninger. Når du udfylder en arbejdsordre i [!INCLUDE [field-service-short](includes/field-service-short.md)], muliggør integrationen en jævn overførsel af data til [!INCLUDE [prod_short](includes/prod_short.md)] videre behandling.  

Integrationen letter også fakturering og opfyldelse af arbejdsordrer i [!INCLUDE [prod_short](includes/prod_short.md)]. Du kan generere nøjagtige fakturaer baseret på serviceaktiviteterne og det forbrug, der er registreret i [!INCLUDE [field-service-short](includes/field-service-short.md)].  

Ved at integrere [!INCLUDE [prod_short](includes/prod_short.md)] med [!INCLUDE [field-service-short](includes/field-service-short.md)] behøver du ikke at indtaste data manuelt eller duplikere indsatsen. Integration giver også et omfattende overblik over servicedrift og økonomi, hvilket muliggør bedre beslutningstagning og driftseffektivitet.

## <a name="prerequisites"></a>Forudsætninger

Da [!INCLUDE [field-service-short](includes/field-service-short.md)] er bygget oven på Dynamics 365 Sales, skal du [konfigurere en forbindelse til Dataverse](/dynamics365/business-central/admin-how-to-set-up-a-dynamics-crm-connection#to-use-the-dataverse-connection-setup-assisted-setup-guide) og [aktivere integration til Dynamics 365 Sales](/dynamics365/business-central/admin-prepare-dynamics-365-for-sales-for-integration#connection-settings-in-the-setup-guide).

### <a name="permissions-and-security-roles-for-user-accounts"></a>Tilladelser og sikkerhedsroller for brugerkonti

Når du installerer integrationsløsningen, konfigureres tilladelser til integrationsbrugerkontoen. Hvis disse tilladelser ændres, skal du muligvis nulstille dem. Det kan du gøre ved at geninstallere integrationsløsningen fra **Geninstaller integrationsløsning** på siden **Opsætning af Dynamics 365-forbindelse**. I følgende afsnit vises de tilladelser og sikkerhedsroller, som løsningen installerer for hver app.

#### <a name="sales"></a>Salg

* Dynamics 365 [!INCLUDE [prod_short](includes/prod_short.md)]-integrationsadministrator
* Dynamics 365 [!INCLUDE [prod_short](includes/prod_short.md)] Integrationsbruger
* Dynamics 365 [!INCLUDE [prod_short](includes/prod_short.md)]-produkttilgængelighedsbruger

#### <a name="business-central"></a>Business Central

Brugere, der bogfører projektkladder, skal have følgende tilladelse:

* Dynamics 365 Sales Integration

#### <a name="field-service"></a>Teknisk service

Hvis du vil bruge de integrerede data, skal brugerne have følgende sikkerhedsrolle:

* Business Central Field Service-integration

Brugere skal f.eks. have denne rolle at knytte arbejdsordrer til [!INCLUDE [prod_short](includes/prod_short.md)] til behandling.

> [!NOTE]
> Sørg for, at brugere tildeles standardsikkerhedsroller og -profiler i [!INCLUDE [field-service-short](includes/field-service-short.md)].  
>
> Du kan få mere at vide om kolonnesikkerhedsprofiler i [!INCLUDE [field-service-short](includes/field-service-short.md)] ved at gå til [Field Service-sikkerhedsroller](/dynamics365/field-service/users-licenses-permissions#field-service-security-roles).
>
> Administratorer skal føje en af de relevante kolonnesikkerhedsprofiler til brugere i Power Platform. Du kan få mere at vide ved at gå til [Føj teams eller brugere til en kolonnesikkerhedsprofil for at styre adgangen](/power-platform/admin/add-teams-users-field-security-profile).

> [!NOTE]
> Hvis du vil bruge handlingen **Åbn i Business Central** i Sales, skal du have følgende rettigheder til følgende tabeller:
>
> * Du skal have **læsetilladelser** til tabellen **Dynamics 365 Business Central Connection** (nav_connection).
> * Du skal have **Læse**-, **Skrive**- og **Slette**- tilladelser til tabellen **Standard Dynamics 365 Business Central-forbindelse** (nav_defaultconnection).

### <a name="other-settings-in-field-service"></a>Andre indstillinger i Field Service

Foretag følgende ændringer på siden **Field Service-indstilling**:

* Under fanen **Køb** skal du fjerne markeringen i feltet **Brug af produkter, der ikke er på lager**. Ellers får du muligvis advarslen "ikke på lager", når du vælger et produkt, der ikke er på lager i [!INCLUDE [field-service-short](includes/field-service-short.md)], men som er på lager i [!INCLUDE [prod_short](includes/prod_short.md)].
* På fanen **Arbejdsordre/reservation** skal du slå til/fra-knapperne **Beregn pris** og **Beregn kostpris** fra. I feltet **Aldrig** skal du vælge **Opret arbejdsordre**.

> [!NOTE]
> Hvis du konfigurerer en forbindelse til [!INCLUDE [field-service-short](includes/field-service-short.md)], fjernes koblingen mellem ressourcer og produkter. Hvis du vil gøre [!INCLUDE [prod_short](includes/prod_short.md)] varer tilgængelige i [!INCLUDE [field-service-short](includes/field-service-short.md)], skal du opdatere feltet **Field Service-produkttype**, så det svarer til feltet **Type** på varerne i [!INCLUDE [prod_short](includes/prod_short.md)]. Du kan få mere at vide ved at gå til [Oprette et produkt eller en tjeneste](/dynamics365/field-service/create-product-or-service#create-a-product-or-service).

## <a name="set-up-the-integration-in-business-central"></a>Konfigurere integration i Business Central

Når du har oprettet forbindelse til Dataverse og Salg, kan du konfigurere integrationen til [!INCLUDE [field-service-short](includes/field-service-short.md)]. På siden **Assisteret opsætning** i [!INCLUDE [prod_short](includes/prod_short.md)] skal du vælge **Konfigurer integration til Dynamics 365 Field Service** for at køre den assisterede opsætningsvejledning. I dette afsnit beskrives nøgleindstillingerne i programguiden.

Hvis du vil lade brugere bogføre forbrug af varer og tjenester i [!INCLUDE [field-service-short](includes/field-service-short.md)] arbejdsordrer, skal du angive den **projektkladdetype** og **projektkladdebatch** , der skal bruges til at bogføre forbrug af produkter og tjenester.

Da serviceydelser udtrykkes i varighed i [!INCLUDE [field-service-short](includes/field-service-short.md)], skal du angive den **timeenhed**, der skal bruges til at konvertere varighed til antal i [!INCLUDE [prod_short](includes/prod_short.md)].

Du kan også angive, hvornår arbejdsordreprodukter og arbejdsordreservices skal synkroniseres til [!INCLUDE [prod_short](includes/prod_short.md)]. De kan f.eks. synkronisere, når arbejdsordrelinjer bruges, eller når nogen fuldfører en arbejdsordre. Vælg den relevante indstilling i feltet **Synkroniser arbejdsordreprodukter/-tjenester**.

Når produkter og tjenester fra arbejdsordrer synkroniseres med projektkladder i [!INCLUDE [prod_short](includes/prod_short.md)], kan du vælge, om projektkladderne skal bogføres manuelt. Vælg den relevante indstilling i feltet **Bogfør projektkladder automatisk**:

* Når arbejdsordren er fuldført.
* Når der bruges arbejdsordreprodukter eller -tjenester.

Når du er færdig med konfigurationen, skal du køre en fuld synkronisering fra siden **Dynamics 365 Field Service Integrationsopsætning**. Denne handling synkroniserer tabeltilknytninger for ting som:

* Projektopgaver for projekter med linket **Anvend brug**. Denne synkronisering gør [!INCLUDE [prod_short](includes/prod_short.md)] projekter tilgængelige til udvælgelse i [!INCLUDE [field-service-short](includes/field-service-short.md)].
* Ressourcer, der ikke er blokeret, har ikke valgte **Brug timeseddel** og har angivet **timer** som måleenhed på siden **Dynamics 365 Field Service Integrationsopsætning**.
* Serviceartikler (kræver, at du bruger Premium-oplevelsen i [!INCLUDE [prod_short](includes/prod_short.md)]).

## <a name="standard-field-service-entity-mapping-for-synchronization"></a>Standardenhedstilknytning i Field Service til synkronisering

Grundlaget for synkronisering af data er tilknytning af tabeller og felter i [!INCLUDE [prod_short](includes/prod_short.md)] med data og kolonner i Dataverse, så de kan udveksle data. Tilknytningen sker via integrationstabeller. Du kan få mere at vide om tabeltilknytninger ved at gå til [Tilknytning af de tabeller og felter, der skal synkroniseres](/dynamics365/business-central/admin-how-to-modify-table-mappings-for-synchronization).

Integration med [!INCLUDE [field-service-short](includes/field-service-short.md)] introducerer følgende standardintegrationstabeltilknytninger:

* **PJLINE-WORDERPRODUCT** - Knytter arbejdsordreprodukter i [!INCLUDE [field-service-short](includes/field-service-short.md)] til projektkladdelinjer i [!INCLUDE [prod_short](includes/prod_short.md)].
* **PJLINE-WORDERSERVICE** - Knytter arbejdsordretjenester i [!INCLUDE [field-service-short](includes/field-service-short.md)] til projektkladdelinjer i [!INCLUDE [prod_short](includes/prod_short.md)].
* **PROJECTTASK** - Tilknytter projekter og projektopgaver i [!INCLUDE [prod_short](includes/prod_short.md)] til produkter i eksterne projekter i [!INCLUDE [field-service-short](includes/field-service-short.md)].
* **RESOURCE-BOOKABLERSC** - Tilknytter ressourcer i [!INCLUDE [prod_short](includes/prod_short.md)] til reserverbare ressourcer i [!INCLUDE [field-service-short](includes/field-service-short.md)].
* **SVCITEM-CUSTASSET** - (Kun Premium-oplevelse) Tilknytter serviceartikler i [!INCLUDE [prod_short](includes/prod_short.md)] til kundeaktiver i [!INCLUDE [field-service-short](includes/field-service-short.md)].

## <a name="use-data-in-both-applications"></a>Brug data i begge programmer

I følgende afsnit beskrives de funktioner, hvor du kan bruge dataene fra [!INCLUDE [prod_short](includes/prod_short.md)] og [!INCLUDE [field-service-short](includes/field-service-short.md)].

### <a name="field-service-1"></a>Teknisk service

Du kan [oprette arbejdsordrer](/dynamics365/field-service/create-work-order) ved hjælp af **tjenestekontoen** og **faktureringskontoen** fra [!INCLUDE [prod_short](includes/prod_short.md)]. På arbejdsordrer skal du vælge **Business Central-projektopgaven** i feltet **Eksternt projekt**. Når du vælger et projekt, kan du synkronisere arbejdsordreprodukter og -tjenester med den relevante projektopgave i [!INCLUDE [prod_short](includes/prod_short.md)].

Du kan tilføje lagervarer og ikke-lagervarer som **arbejdsordreprodukter** på arbejdsordrer og få den disponible beholdning og omkostninger og priser fra [!INCLUDE [prod_short](includes/prod_short.md)]. Du kan få mere at vide ved at gå til [Oprette en arbejdsordre fra arbejdsordreformularen og postlisten](/dynamics365/field-service/create-work-order#create-a-work-order-from-the-work-order-form-and-record-list).

Du kan tilføje varer af typen service som **Arbejdsordreservice** og hente omkostninger og priser fra [!INCLUDE [prod_short](includes/prod_short.md)]. Du kan få mere at vide ved at gå til fanen [Produkter og tjenester](/dynamics365/field-service/work-order-experience#products-and-services-tab).

> [!NOTE]
> Når status for et produkt eller en tjeneste i en arbejdsordre ændres fra **Anslået** til **Brugt** i [!INCLUDE [field-service-short](includes/field-service-short.md)], synkroniseres de til projektkladdelinjerne i [!INCLUDE [prod_short](includes/prod_short.md)].

Du kan reservere en ressource og relatere **Reservationer** til arbejdsordretjenester ved hjælp af en **Reserverbar ressource** fra [!INCLUDE [prod_short](includes/prod_short.md)].

### <a name="business-central-1"></a>Business Central

Afhængigt af dine indstillinger på siden **Opsætning af Field Service-integration** overføres og bogføres forbrugsoplysninger ved hjælp af en **projektkladde** i [!INCLUDE [prod_short](includes/prod_short.md)].

Værdierne **Antal til fakturering** og **Varighed til fakturering** kopieres til feltet **Antal - Overfør til faktura**. Baseret på disse værdier kan du oprette og bogføre salgsfakturaer i [!INCLUDE [prod_short](includes/prod_short.md)] for at fakturere kunden. Når fakturaen er bogført, eller forbruget er behandlet i [!INCLUDE [prod_short](includes/prod_short.md)], vises det fakturerede antal og det forbrugte antal under fanen [!INCLUDE [prod_short](includes/prod_short.md)] på siderne **Arbejdsordreprodukt** og **Arbejdsordreservice**.  

Brug siden **Projektplanlægningslinjer** til at spore bogføring og fakturering af forbrug på arbejdsordrer. Fra siden **Projektplanlægningslinjer** kan du oprette og bogføre salgsfakturaer i [!INCLUDE [prod_short](includes/prod_short.md)]. Derefter kan du synkronisere dem med [!INCLUDE [field-service-short](includes/field-service-short.md)] og holde styr på status for fakturaerne.

> [!NOTE]
> Arbejdsordretjenester med en reservation, der bruger en reserverbar ressource, der er koblet til en [!INCLUDE [prod_short](includes/prod_short.md)] ressource, synkroniseres med to projektkladdelinjer: en linje af typen **Budget** for den koblede ressource og en anden linje af typen **Fakturerbar** for den vare, der repareres.
>
> Det produkt, der er valgt på arbejdsordreservicen, skal kobles til en vare af typen **Service** i [!INCLUDE [prod_short](includes/prod_short.md)]. Desuden skal basisenheden for varen angives til den **enhed for timer**, der er valgt på siden **Dynamics 365 Field Service Integrationsopsætning**.
>
> Du kan oprette en faktura for en vare af typen **Service** fra den fakturerbare projektplanlægningslinje og bruge budgetprojektplanlægningslinjen til at registrere omkostninger med ressourcen.

## <a name="see-also"></a>Se også

[Integrere med Microsoft Dataverse via datasynkronisering](admin-common-data-service.md)  
[Tilknytning af tabeller og felter til synkronisering](admin-how-to-modify-table-mappings-for-synchronization.md)
