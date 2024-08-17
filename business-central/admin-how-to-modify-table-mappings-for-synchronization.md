---
title: 'Tilknytning de tabeller og felter, der skal synkroniseres'
description: 'Få mere at vide om, hvordan du kan tilknytte tabeller og felter til synkronisering af data mellem Business central og Microsoft Dataverse.'
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bholtorf
ms.topic: conceptual
ms.date: 08/07/2024
ms.custom: bap-template
ms.search.keywords: 'sales, crm, integration, sync, synchronize, table mapping'
ms.service: dynamics-365-business-central
---
# <a name="mapping-the-tables-and-fields-to-synchronize"></a>Tilknytning de tabeller og felter, der skal synkroniseres

Grundlaget for synkronisering af data er tilknytning af tabeller og felter i [!INCLUDE[prod_short](includes/prod_short.md)] med data og kolonner i [!INCLUDE[prod_short](includes/cds_long_md.md)], så de kan udveksle data. Tilknytningen sker via integrationstabeller.

## <a name="mapping-integration-tables"></a>Tilknytte integrationstabeller

En integrationstabel er en tabel i databasen [!INCLUDE[prod_short](includes/prod_short.md)], der repræsenterer en tabel som f.eks. en konti i [!INCLUDE[cds_long_md](includes/cds_long_md.md)]. Integrationstabeller omfatter felter, der svarer til kolonner i tabellen [!INCLUDE[cds_long_md](includes/cds_long_md.md)]. Integrationstabellen Konto opretter f.eks. forbindelse til objektet Kontotabel i [!INCLUDE[cds_short_md](includes/cds_long_md.md)]. Der skal være en integrationstabel, der tilknytter hver tabel i [!INCLUDE[cds_short_md](includes/cds_short_md.md)], som du vil synkronisere med data i [!INCLUDE[prod_short](includes/prod_short.md)].

Når du opretter forbindelsen mellem appsene, opretter [!INCLUDE[prod_short](includes/prod_short.md)] nogle standardtilknytninger. Hvis du vil, kan du ændre tabelknytningerne. Få flere oplysninger i [Standard-tabeltilknytning til synkronisering](admin-synchronizing-business-central-and-sales.md#standard-table-mapping-for-synchronization). Hvis du har ændret standardtilknytningerne og vil gendanne dine ændringer, skal du på siden **Integration af tabeltilknytninger** vælge **Brug standardopsætning af synkronisering**.

> [!Note]
> Hvis du bruger en lokal version af [!INCLUDE[prod_short](includes/prod_short.md)], gemmes integrationstabellens tilknytninger i tabellen 5335 Integrationstabeltilknytninger, hvor du kan se og redigere tilknytninger. Komplekse tilknytninger og synkroniseringsregler defineres i codeunit 5341.

> [!TIP]
> Når en kombineret post skifter, synkroniseres [!INCLUDE [prod_short](includes/prod_short.md)] automatisk dataene med Dataverse. Automatisk synkronisering er godt i de fleste tilfælde. Men hyppige ændringer af store mængder sammenkoblede poster i en tabel kan medføre en langsom datasynkronisering.
>
> Du kan undgå langsom ydeevne ved at aktivere eller deaktivere hændelsesbaseret datasynkronisering for en hvilken som helst tabel på siden **integration af integrationstabel**. Som standard er hændelsesbaseret synkronisering aktiveret, så eksisterende integrationer ikke påvirkes. Administratoren kan slå funktionen til eller fra for bestemte tabeller.

### <a name="add-table-and-field-mappings-to-existing-integration-tables"></a>Føje tabel- og felttilknytninger til eksisterende integrationstabeller

På siden **integrationstabel Tilknytninger** kan du bruge handlingen Ny tabeltilknytning til at føje nye tabeltilknytninger til integrationstabeller. Handlingen starter den **assisterede opsætningsvejledning Opret nye integrationstilknytninger**, som hjælper dig med at konfigurere nye integrationstabel- og felttilknytninger.

I vejledningen kan du knytte tabellerne til [!INCLUDE [prod_short](includes/prod_short.md)] de eksisterende integrationstabeller Dataverse. Du kan også angive tabellens Dataverse entydige id i **integrationstabel Feltnavn** for entydigt id og integrationstabel **Ændret den feltnavn**, som skal bruges, for at datasynkroniseringen kan fungere.

> [!NOTE]
> Opslaget i kolonnen Tabel viser alle [!INCLUDE [prod_short](includes/prod_short.md)] tabeller, herunder brugerdefinerede tabeller, der endnu ikke er tilknyttet. Det udelukker dem, der allerede findes på din integrationstabel Mappings-side. Opslaget i kolonnen integrationstabel viser kun Dataverse tabeller (AL-proxytabeller), der er en del af standardintegrationer. Hvis du vil tilføje yderligere eller brugerdefinerede Dataverse tabeller, skal du have hjælp fra en udvikler til at oprette og udrulle dem via en udvidelse.

Handlingen Avanceret åbner yderligere tabeltilknytning indstillinger, som du kan konfigurere. I feltet Tabelfilter kan du angive filtre for **under** fanen **Avanceret** . [!INCLUDE [prod_short](includes/prod_short.md)]  **Brug feltet integrationstabel filter** til Dataverse data, der skal tages i betragtning ved datasynkronisering sammen med konfigurationsskabelonkoderne i **Tabelkonfiguration. Skabelonkode** og **Int. Tbl. Config. Kode** til forhåndsudfyldning af manglende data, når der kommer nye data fra et af programmerne.

Vejledningen hjælper dig også med at angive de felter, som det nye tilknytning skal indeholde. Du kan matche et [!INCLUDE [prod_short](includes/prod_short.md)] felt i **kolonnen Feltnavn** med et Dataverse feltnavn i kolonnen Feltnavn **for** integration. Du kan også angive en **retning**, om feltet altid har den samme værdi i **kolonnen Konstant**, og om valideringer eller transformationer skal anvendes under felt tilknytning.

> [!NOTE]
> Hvis du vil reducere antallet af fejl, filtreres opslaget for **kolonnen integrationstabel felt** til en liste over tilgængelige felter. Hvis du vil tilknytte felter, som filtrene ikke indeholder, skal du have hjælp fra en udvikler.
>
> * Felter skal være aktiveret.
> * Du kan ikke bruge vejledningen til at tilknytte felterne FlowField og FlowFilter.
> * Du kan kun tilknytte felter af typen BigInteger, boolesk, Code, Date, DateFormula, DateTime, Decimal, Duration, GUID, Heltal, Alternativ og Tekst.

> [!TIP]
> Du kan også føje nye felttilknytninger til eksisterende integrationstabel tilknytninger via **listesiden Felttilknytninger** for integration, som du kan få adgang til ved at vælge **Felter på siden**  integrationstabel **tilknytninger** .
>
> Du skal blot vælge **Nyt felt tilknytning**  for at åbne feltet tilknytning trin i den **assisterede opsætningsvejledning Opret nye integrationstilknytninger** og derefter fortsætte som beskrevet i denne artikel.

Nye felttilknytninger, du føjer til en eksisterende tabeltilknytning, er i deaktiveret tilstand. Du kan vælge **Rediger liste** for at aktivere dem senere.

### <a name="synchronization-rules"></a>Synkroniseringsregler

En integrationstabeltilknytning indeholder også regler, der styrer, hvordan integrationssynkroniseringsjob synkroniserer poster i en [!INCLUDE[prod_short](includes/prod_short.md)]-tabel og en tabel i [!INCLUDE[prod_short](includes/cds_long_md.md)]. Hvis du vil have eksempler på regler for integration med salg, skal du gå til [Synkroniseringsregler](#synchronization-rules).

### <a name="strategies-for-auto-resolving-conflicts"></a>Strategier til automatisk løsning af konflikter

Datakonflikter kan nemt forekomme, når forretningsprogrammer udveksler data løbende. Du kan f.eks. slette eller ændre en række i et af programmerne eller begge dele. Du kan reducere antallet af konflikter, som du skal løse manuelt, ved at angive løsningsstrategier, og [!INCLUDE[prod_short](includes/prod_short.md)] vil dermed løse konflikterne i overensstemmelse med reglerne i strategierne.

Tilknytninger til integrationstabeller omfatter regler, der styrer, hvordan synkroniseringsjob synkroniserer poster. På siden **Integrationstabeltilknytning** i kolonnerne **Løs sletningskonflikter** og **Løs opdateringskonflikter** kan du angive, hvordan [!INCLUDE[prod_short](includes/prod_short.md)] skal løse de konflikter, der opstår, skal løses, fordi posterne blev slettet i tabeller i et eller et andet forretningsprogram eller blev opdateret i begge. 

I kolonne **Løs sletningskonflikter** kan du vælge, at [!INCLUDE[prod_short](includes/prod_short.md)] automatisk gendanner slettede poster, fjerner koblingen mellem posterne eller gør ingenting. Hvis du ikke gør noget, skal du løse problemerne manuelt. 

I kolonnen **Løs opdateringskonflikter** kan du vælge, at [!INCLUDE[prod_short](includes/prod_short.md)] automatisk sender en dataopdatering til integrationstabellen, når du sender data til [!INCLUDE[prod_short](includes/cds_long_md.md)], eller henter en dataopdatering fra integrationstabellen, når der hentes data fra [!INCLUDE[prod_short](includes/cds_long_md.md)], eller du kan vælge ikke at gøre noget. Hvis du ikke gør noget, skal du løse problemerne manuelt.

Når du har angivet strategien på siden **Fejl ved sammenkædet datasynkronisering**, kan du vælge handlingen **Prøv alle igen** for at løse konflikter automatisk.

## <a name="mapping-integration-fields"></a>Felter til integrationstilknytning

Tilknytningstabeller er kun det første trin. Du skal også tilknytte felterne i tabellerne. Integrationsfelttilknytninger sammenkæder felter i [!INCLUDE[prod_short](includes/prod_short.md)]-tabeller med tilsvarende kolonner i [!INCLUDE[prod_short](includes/cds_long_md.md)] og bestemmer, om data skal synkroniseres i hver tabel. Den standardtabeltilknytning, som [!INCLUDE[prod_short](includes/prod_short.md)] giver, omfatter felttilknytninger, men du kan ændre dem, hvis du vil. Du kan finde flere oplysninger i [Visning af tabeltilknytninger](admin-synchronizing-business-central-and-sales.md#tip-for-admins-viewing-table-mappings).

> [!Note]
> Hvis du bruger en lokal version af [!INCLUDE[prod_short](includes/prod_short.md)], defineres integrationsfelttilknytninger i tabellen 5336 Integrationsfelttilknytning.

Du kan tilknytte felterne manuelt, eller du kan automatisere processen ved at tilknytte flere felter på samme tid baseret på kriterier for at matche deres værdier. Yderligere oplysninger finder du under [Sådan parres flere poster baseret på matching af feltværdi](admin-how-to-couple-and-synchronize-records-manually.md).

### <a name="handle-differences-in-field-values"></a>Håndtering af forskelle i feltværdier

Nogle gange er værdierne i de felter, du vil tilknytte, forskellige. For eksempel er sprogkoden for USA i [!INCLUDE[crm_md](includes/crm_md.md)] "U.S.", mens den i [!INCLUDE[prod_short](includes/prod_short.md)] er "US". Det betyder, at du skal transformere værdien, når du synkroniserer data. Dette sker gennem transformationsregler, som du definerer for felterne. Du kan definere transformationsregler på siden **Integrationstabeltilknytninger** ved at vælge **Tilknytning** og derefter **Felter**. Der findes foruddefinerede regler, men du kan også oprette dine egne. Du kan finde flere oplysninger i [Transformationsregler](across-how-to-set-up-data-exchange-definitions.md#transformation-rules).

### <a name="handle-missing-option-values"></a>Håndtering af manglende indstillingsværdier

[!INCLUDE[prod_short](includes/cds_long_md.md)] indeholder kolonner til at vælge indstillinger, som indeholder værdier, du kan knytte til [!INCLUDE[prod_short](includes/prod_short.md)]-felter af typen **Indstilling** for automatisk synkronisering. Under synkroniseringen ignoreres ikke-tilknyttede indstillinger, og de manglende indstillinger vedhæftes til den relaterede [!INCLUDE[prod_short](includes/prod_short.md)]-tabel og føjes til systemtabellen **CDS-indstillingstilknytning**, så de kan håndteres manuelt senere. For eksempel ved at tilføje de manglende indstillinger i hvert produkt og derefter opdatere tilknytningen. Få flere oplysninger i [Håndtering af manglende indstillingsværdier](admin-cds-missing-option-values.md).

## <a name="couple-records"></a>Sammenkædede poster

Sammenkædning knytter rækker i [!INCLUDE[prod_short](includes/cds_long_md.md)] til poster i [!INCLUDE[prod_short](includes/prod_short.md)]. F.eks. sammenkædes [!INCLUDE[prod_short](includes/cds_long_md.md)]-konti typisk med kunder i [!INCLUDE[prod_short](includes/prod_short.md)]. Sammenkædning af poster giver følgende fordele:

* Den gør synkroniseringen mulig.
* Brugere kan åbne poster eller tækker i én forretningsapp på den anden. Dette kræver, at programmerne allerede er integreret.

Sammenkædninger kan konfigureres automatisk ved hjælp af synkroniseringsjob eller manuelt ved at redigere posten i [!INCLUDE[prod_short](includes/prod_short.md)]. Du finder flere oplysninger i [Synkronisering af data i [!INCLUDE[prod_short](includes/prod_short.md)]i [!INCLUDE[prod_short](includes/cds_long_md.md)]](admin-synchronizing-business-central-and-sales.md) og [Sammenkæde og synkronisere poster manuelt](admin-manual-synchronization-of-table-mappings.md#synchronize-individual-table-mappings).

## <a name="filter-records-and-rows"></a>Filtrere poster og rækker

Hvis du ikke vil synkronisere alle rækker for en bestemt tabel i [!INCLUDE[prod_short](includes/cds_long_md.md)] eller tabel i [!INCLUDE[prod_short](includes/prod_short.md)], du kan indstille filtre for at begrænse antallet af poster, der synkroniseres. Du indstiller filtre på siden **Integrationstilknytninger til tabeller**.  

1. Vælg ![Lightbulb, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") Vælg ikonet , åbn **Integrationstabeltilknytninger**, og vælg derefter det relaterede link.
2. Du filtrerer [!INCLUDE[prod_short](includes/prod_short.md)] records ved at indstille feltet **Tabelfiltrering**.  
3. Du filtrerer [!INCLUDE[prod_short](includes/cds_long_md.md)] rækker ved at indstille feltet **Integration af tabelfilter**.  

## <a name="create-new-records"></a>Oprette nye poster

Som standard synkroniseres kun rækker i [!INCLUDE[prod_short](includes/prod_short.md)] og [!INCLUDE[prod_short](includes/cds_long_md.md)], der er sammenkædet gennem integrationssynkroniseringsjob. Du kan konfigurere tabeltilknytninger, så nye poster eller rækker oprettes på destinationen (f.eks. [!INCLUDE[prod_short](includes/prod_short.md)]) for hver række i kilden (f.eks. [!INCLUDE[prod_short](includes/cds_long_md.md)]), der ikke allerede er sammenkædet.  

SÆLGERE – Dynamics 365 Sales-synkroniseringsjob bruger f.eks. tabeltilknytningen SÆLGERE. Synkroniseringsjobbene kopierer data fra brugere i [!INCLUDE[prod_short](includes/cds_long_md.md)] til sælgere i [!INCLUDE[prod_short](includes/prod_short.md)]. Hvis du har konfigureret tabeltilknytningen til at oprette nye records for hver bruger i [!INCLUDE[prod_short](includes/cds_long_md.md)], der ikke allerede er sammenkædet med en sælger i [!INCLUDE[prod_short](includes/prod_short.md)], oprettes en ny sælgerrække i [!INCLUDE[prod_short](includes/prod_short.md)].  

### <a name="to-create-new-records-during-synchronization"></a>Sådan oprettes nye records under synkronisering

1. Vælg ![Lightbulb, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") Vælg ikonet , åbn **Integrationstabeltilknytninger**, og vælg derefter det relaterede link.
2. Fjern markeringen i feltet **Synkroniser kun sammenkædede records** i tabeltilknytningsposten på listen.  

## <a name="use-configuration-templates-on-table-mappings"></a>Brug konfigurationsskabeloner på tabeltilknytninger

Du kan tildele konfigurationsskabeloner til tabeltilknytninger og bruge dem til nye rækker, der oprettes i [!INCLUDE[prod_short](includes/prod_short.md)] eller [!INCLUDE[prod_short](includes/cds_long_md.md)]. For hver tabeltilknytning kan du angive en konfigurationsskabelon, som skal bruges til nye [!INCLUDE[prod_short](includes/prod_short.md)]-rækker, og en anden skabelon, du vil bruge til nye [!INCLUDE[prod_short](includes/cds_long_md.md)]-rækker.  

Hvis du installerer standardsynkroniseringsopsætningen, oprettes og bruges der for det meste to skabeloner automatisk i tabeltilknytningen for [!INCLUDE[prod_short](includes/prod_short.md)]-kunder og [!INCLUDE[crm_md](includes/crm_md.md)]-konti: **CDSCUST** og **CDSACCOUNT**.  

* **CDSCUST** bruges til at oprette og synkronisere nye kunder i [!INCLUDE[prod_short](includes/prod_short.md)], baseret på konti i [!INCLUDE[crm_md](includes/crm_md.md)].  

     Opret denne skabelon ved at kopiere en eksisterende konfigurationsskabelon for kunder. **CDSCUST** oprettes kun, hvis der er en eksisterende konfigurationsskabelon, og feltet **Valutakode** i skabelonen er tomt. Hvis et felt i konfigurationsskabelonen indeholder en værdi, bruges værdien i stedet for værdien i den tilknyttede kolonne for [!INCLUDE[prod_short](includes/cds_long_md.md)]-kontoen. Hvis f.eks. kolonnen **Land/område** på en konto i [!INCLUDE[prod_short](includes/cds_long_md.md)] indeholder *U.S.*, og feltet **Land/område** i konfigurationsskabelonen er **GB**, bruges **GB** som **Land/område** på den oprettede kunde i [!INCLUDE[prod_short](includes/prod_short.md)].  

* **CDSACCOUNT** bruges til at oprette og synkronisere nye konti i [!INCLUDE[prod_short](includes/cds_long_md.md)], baseret på en konto i [!INCLUDE[prod_short](includes/prod_short.md)].  

### <a name="to-specify-configuration-templates-on-a-table-mapping"></a>Sådan angiver du konfigurationsskabeloner i en tabeltilknytning

1. Vælg ![Lightbulb, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") Vælg ikonet , åbn **Integrationstabeltilknytninger**, og vælg derefter det relaterede link.
2. I tabeltilknytningsposten på listen i feltet **Kode til tabelkonfigurationsskabelon**, skal du vælge den konfigurationsskabelon, der skal bruges til nye records i [!INCLUDE[prod_short](includes/prod_short.md)].  
3. Konfigurer feltet **Kode for int. tbl. konfigurationsskabelon** til den konfigurationsskabelon, der skal bruges til nye records i [!INCLUDE[prod_short](includes/cds_long_md.md)].

## <a name="see-also"></a>Se også

[Om integration Dynamics 365 Business Central med [!INCLUDE[prod_short](includes/cds_long_md.md)]](admin-prepare-dynamics-365-for-sales-for-integration.md )  
[Synkronisere Business Central og [!INCLUDE[prod_short](includes/cds_long_md.md)]](admin-synchronizing-business-central-and-sales.md)  
[Planlæg en synkronisering](admin-scheduled-synchronization-using-the-synchronization-job-queue-entries.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
