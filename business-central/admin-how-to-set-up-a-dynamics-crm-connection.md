---
title: Tilslut til Microsoft Dataverse (indeholder video)
description: Oprette forbindelse mellem Business Central og Dataverse. Virksomheder opretter typisk forbindelsen for at integrere og synkronisere data med en anden Dynamics 365-forretningsapp.
author: brentholtorf
ms.topic: conceptual
ms.workload: na
ms.search.keywords: null
ms.search.forms: '7200, 7201'
ms.date: 09/28/2023
ms.author: bholtorf
---
# <a name="connect-to-microsoft-dataverse"></a>Opret forbindelse til Microsoft Dataverse

[!INCLUDE[azure-ad-to-microsoft-entra-id](~/../shared-content/shared/azure-ad-to-microsoft-entra-id.md)]

Denne artikel beskriver, hvordan du konfigurerer en forbindelse mellem [!INCLUDE[prod_short](includes/prod_short.md)] og [!INCLUDE[cds_long_md](includes/cds_long_md.md)]. Virksomheder opretter typisk forbindelsen for at integrere og synkronisere data med en anden Dynamics 365-forretningsapp såsom [!INCLUDE[crm_md](includes/crm_md.md)].  

## <a name="before-you-start"></a>Før du starter

Der er et par oplysninger, som du skal have klar, før du opretter forbindelsen:  

* URL-adressen til det [!INCLUDE[cds_long_md](includes/cds_long_md.md)]-miljø, som du vil oprette forbindelse til. Hvis du bruger den **Konfiguration af Dataverse-forbindelse**-assisterende installationsvejledning til at oprette forbindelsen, vil vi finde dine miljøer. Du kan også angive URL-adressen på et andet miljø i din lejer.  
* Brugernavn og adgangskode til en konto, der har administratorrettigheder i [!INCLUDE[prod_short](includes/prod_short.md)] og [!INCLUDE[cds_long_md](includes/cds_long_md.md)].  
* Hvis du har en lokal [!INCLUDE[prod_short](includes/prod_short.md)] 2020 Release Wave 1, version 16,5, skal du læse [Kendte problemer](/dynamics365/business-central/dev-itpro/upgrade/known-issues#wrong-net-assemblies-for-external-connected-services)-artikler. Du skal fuldføre den beskrevne løsning, før du kan oprette forbindelsen til [!INCLUDE[cds_long_md](includes/cds_long_md.md)].
* De lokale valutaer, som hvert firma bruger. [!INCLUDE [prod_short](includes/prod_short.md)]-firmaer kan oprette forbindelse til et [!INCLUDE [cds_long_md](includes/cds_long_md.md)]-miljø, der har en basisvaluta, der er anderledes end deres lokale valuta.. Du kan få mere at vide om, hvordan du håndterer konfigurationer af flere valutaer, ved at gå til [Tillad for forskellige valutaer](#allow-for-different-currencies).

> [!IMPORTANT]
> Det [!INCLUDE[cds_long_md](includes/cds_long_md.md)]-miljø må ikke være i administrationstilstand. Administrationstilstand forårsager, at forbindelsen mislykkes, fordi integrationsbruger kontoen for forbindelsen ikke har administratorrettigheder. Der er flere oplysninger i [Administrationstilstand](/power-platform/admin/admin-mode).

> [!Note]
> I fremgangsmåden nedenfor beskrives proceduren for onlineversionen af [!INCLUDE[prod_short](includes/prod_short.md)].
> Hvis du bruger [!INCLUDE[prod_short](includes/prod_short.md)] on-premises og ikke bruger en Microsoft Entra-konto til at oprette forbindelse til [!INCLUDE [cds_long_md](includes/cds_long_md.md)], skal du også angive brugernavn og adgangskode for en brugerkonto til integrationen. Denne konto kaldes "integrationsbruger"-kontoen. Hvis du bruger en Microsoft Entra-konto, er integrationsbrugerkontoen ikke påkrævet og vises ikke. Integrationsbrugeren konfigureres automatisk og kræver ikke en licens.

## <a name="allow-for-different-currencies"></a>Tillad for forskellige valutaer

[!INCLUDE [prod_short](includes/prod_short.md)]-firmaer kan oprette forbindelse til et [!INCLUDE [cds_long_md](includes/cds_long_md.md)]-miljø, der har en basisvaluta, der er anderledes end deres lokale valuta..

> [!NOTE]
> Synkronisering af flere valutaer kræver, at du bruger en ensrettet synkronisering, fra [!INCLUDE [prod_short](includes/prod_short.md)] til [!INCLUDE [cds_long_md](includes/cds_long_md.md)].

Du kan få mere at vide om basisvalutaen i [!INCLUDE [cds_long_md](includes/cds_long_md.md)] ved at gå til [objektet Transaktionsvaluta (valuta).](/powerapps/developer/data-platform/transaction-currency-currency-entity) 

Hvis du vil vide mere om valutaer i [!INCLUDE [prod_short](includes/prod_short.md)], gå til [Valutaer i Business Central](finance-currencies.md).

Hvis du vil tillade forskellige valutaer, skal du sørge for, at du har angivet følgende indstillinger, før du opretter forbindelse:

* Indstillingen for basistransaktionsvaluta i [!INCLUDE [cds_long_md](includes/cds_long_md.md)] har den valutakode, der er angivet på siden **Valutaer** i [!INCLUDE [prod_short](includes/prod_short.md)].
* Der er angivet mindst én valutakurs for valutaen i [!INCLUDE [prod_short](includes/prod_short.md)] på siden **Valutakurser**.

Når du aktiverer forbindelsen til [!INCLUDE [cds_long_md](includes/cds_long_md.md)], tilføjes [!INCLUDE [prod_short](includes/prod_short.md)] dens lokale valuta til **valuta**-objektet i [!INCLUDE [cds_long_md](includes/cds_long_md.md)]. Den lokale valuta bruger valutakursen fra feltet **Valutafaktor** på siden **Valutakurser**.

Da synkronisering af valuta er envejs, fra [!INCLUDE [prod_short](includes/prod_short.md)] til [!INCLUDE [cds_long_md](includes/cds_long_md.md)],konverteres og synkroniseres monetære beløb på følgende måde:

* Beløbene i [!INCLUDE [cds_long_md](includes/cds_long_md.md)]-basisvalutaen konverteres til den [!INCLUDE [prod_short](includes/prod_short.md)] lokale valuta ud fra den seneste valutakurs, der er synkroniseret fra [!INCLUDE [prod_short](includes/prod_short.md)].
* Beløb i den [!INCLUDE [prod_short](includes/prod_short.md)] lokale valuta synkroniseres med den [!INCLUDE [prod_short](includes/prod_short.md)] lokale valuta i en af de andre (ikke-basis) valutaer i [!INCLUDE [cds_long_md](includes/cds_long_md.md)].

## <a name="set-up-a-connection-to-"></a>Konfigurer en forbindelse til [!INCLUDE[cds_long_md](includes/cds_long_md.md)]

For alle andre godkendelsestyper end Microsoft 365-godkendelse kan du konfigurere forbindelse til [!INCLUDE[cds_long_md](includes/cds_long_md.md)] på siden **Konfiguration af Dataverse-forbindelse**. For Microsoft 365-godkendelse anbefaler vi, at du bruger vejledningen **Opsætning af Dataverse-forbindelse** med assisteret opsætning. Denne vejledning gør det nemmere at oprette forbindelsen og angive avancerede funktioner, f.eks. ejerskabsmodel og indledende synkronisering.  

> [!IMPORTANT]
> Under konfigurationen af forbindelsen til [!INCLUDE[cds_long_md](includes/cds_long_md.md)] bliver administratoren bedt om at give følgende tilladelser til det registrerede Azure-program, der hedder [!INCLUDE[prod_short](includes/prod_short.md)]-integration med [!INCLUDE[cds_long_md](includes/cds_long_md.md)]:
>
> * **Få adgang til [!INCLUDE[cds_long_md](includes/cds_long_md.md)] som** nødvendig tilladelse, så du [!INCLUDE[prod_short](includes/prod_short.md)] kan, på vegne af administratoren, automatisk oprette en ikke-licenseret, ikke-interaktiv [!INCLUDE[prod_short](includes/prod_short.md)]-integrationsprogrambruger, tildele sikkerhedsroller til denne bruger og installere [!INCLUDE[prod_short](includes/prod_short.md)]-integrationsløsningen til [!INCLUDE[cds_long_md](includes/cds_long_md.md)]. Denne tilladelse bruges kun én gang under oprettelse af forbindelse til [!INCLUDE[cds_long_md](includes/cds_long_md.md)].  
> * **Fuld adgang til Dynamics 365 [!INCLUDE[prod_short](includes/prod_short.md)]** er en nødvendig tilladelse, så en automatisk oprettet [!INCLUDE[prod_short](includes/prod_short.md)]-integrationsprogrambruger kan få adgang til [!INCLUDE[prod_short](includes/prod_short.md)]-data, der skal synkroniseres.  
> * **Logge på og læse din profil** er en nødvendig tilladelse for at kontrollere, at brugeren, som logger på, faktisk er tildelt Systemadministrator som sikkerhedsrolle i [!INCLUDE[cds_long_md](includes/cds_long_md.md)].  
>
> Ved at give samtykke på vegne af organisationen giver administratoren det registrerede Azure-program, der hedder [!INCLUDE[prod_short](includes/prod_short.md)]-integration til [!INCLUDE[cds_long_md](includes/cds_long_md.md)], ret til at synkronisere data ved hjælp af den automatisk oprettede [!INCLUDE[prod_short](includes/prod_short.md)]-integrationsprogrambrugers legitimationsoplysninger.

### <a name="to-use-the-dataverse-connection-setup-assisted-setup-guide"></a>Sådan bruger du vejledningen Dataverse-forbindelsesopsætning med assisteret opsætning

Dataverse-forbindelsesopsætningsvejledning kan gøre det nemmere at oprette forbindelse til programmerne, og det kan også være en hjælp til at starte en første synkronisering. Hvis du vælger at køre første synkronisering, gennemgår [!INCLUDE[prod_short](includes/prod_short.md)] dataene i begge programmer og giver anbefalinger om, hvordan du skal håndtere den første synkronisering. Den følgende tabel beskriver de forskellige anbefalinger.

|Anbefaling  |Beskrivlse  |
|---------|---------|
|**Fuld synkronisering**|Dataene findes kun i [!INCLUDE[prod_short](includes/prod_short.md)], eller kun i [!INCLUDE[cds_long_md](includes/cds_long_md.md)]. Det anbefales at synkronisere alle data fra den tjeneste, der har den til den anden tjeneste.|
|**Ingen synkronisering**|Dataene findes i begge programmer, og hvis du udfører fuld synkronisering, duplikeres dataene. Det anbefales at koble registreringer.|
|**Afhængighed er ikke opfyldt**|Der findes data i begge programmer, men rækken eller tabellen kan ikke synkroniseres, fordi den afhænger af en række eller en tabel, der ikke har nogen synkroniserings anbefaling. Hvis kunder f.eks. ikke kan synkroniseres, kan data til kontakter, der afhænger af kundedata, ikke synkroniseres.|

> [!IMPORTANT]
> Du bruger som regel kun fuld synkronisering, når du integrerer programmerne første gang, og kun ét program indeholder data. Fuld synkronisering kan være nyttig i et demonstrationsmiljø, da det automatisk opretter og forbinder poster i hvert program, hvilket gør det hurtigere at starte med at arbejde med synkroniserede data. Men du bør kun udføre en fuldstændig synkronisering, hvis du ønsker en række i [!INCLUDE[prod_short](includes/prod_short.md)] for hver række i [!INCLUDE[cds_long_md](includes/cds_long_md.md)] for de givne tabeltilknytninger. Ellers kan resultatet være duplikerede poster.

1. Vælg ![Lightbulb, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, angiv **Assisteret opsætning** og vælg derefter det relaterede link.
2. Vælg **Konfigurer en forbindelse til Microsoft Dataverse** for at starte den assisterede opsætningsvejledning.
3. Udfyld felterne efter behov.

> [!NOTE]
> Hvis du ikke bliver bedt om at logge på med din administratorkonto, skyldes det sandsynligvis, at pop op-vinduer er blokeret. Du kan logge på ved at tillade pop op-vinduer fra `https://login.microsoftonline.com`.

### <a name="to-create-or-maintain-the-connection-manually"></a>Sådan oprettes eller vedligeholdes forbindelsen manuelt

Følgende procedure beskriver, hvordan du kan opsætte forbindelsen manuelt på siden **Dataverse-forbindelsesopsætning**. Siden **Konfiguration af Dataverse-forbindelse** er den side, hvor du administrerer indstillingerne.

1. Vælg ![Lightbulb, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **Dataverse-forbindelseskonfiguration**, og vælg derefter det relaterede link.
2. Indtast følgende oplysninger vedrørende forbindelsen fra [!INCLUDE[prod_short](includes/prod_short.md)] til [!INCLUDE[cds_long_md](includes/cds_long_md.md)].

    |Felt|Beskrivlse|
    |-----|-----|
    |**URL-adresse til miljø**|Hvis du ejer miljøer i [!INCLUDE[cds_long_md](includes/cds_long_md.md)], finder vi dem for dig, når du kører installationsvejledningen. Hvis du vil oprette forbindelse til et andet miljø i en anden lejer, kan du angive administrator-legitimationsoplysninger til miljøet, og dem vil vi registrere. |
    |**Aktiveret**|Begynd at bruge integrationen. Hvis du ikke kan aktivere forbindelse nu, gemmes forbindelsesindstillingerne, men brugerne vil ikke kunne få adgang til [!INCLUDE[cds_long_md](includes/cds_long_md.md)] data fra [!INCLUDE[prod_short](includes/prod_short.md)]. Du kan vende tilbage til denne side og aktivere forbindelsen senere.  |

3. I feltet **Ejerskabsmodel** skal du vælge, om du vil have en teamtabel i [!INCLUDE[cds_long_md](includes/cds_long_md.md)], der skal eje nye poster, eller om der skal være en eller flere bestemte brugere. Hvis du vælger **Person**, skal du angive hver enkelt bruger. Hvis du vælger **Team**, vises standard-koncernvirksomheden i feltet **Sammenkædet koncernvirksomhed**.

    <!--Need to verify the details in this table, are these specific to Sales maybe?  IK: No they are not and no longer relevant 
    Enter the following advanced settings.-->

    <!-- |Field|Description|
    |-----|-----|
    |**[!INCLUDE[prod_short](includes/prod_short.md)] Users Must Map to CDS Users**|If you're using the Person ownership model, specify whether [!INCLUDE[prod_short](includes/prod_short.md)] user accounts must have a matching user accounts in [!INCLUDE[cds_long_md](includes/cds_long_md.md)]. The **Microsoft 365 Authentication Email** of the [!INCLUDE[prod_short](includes/prod_short.md)] user must be the same as the **Primary Email** of the [!INCLUDE[crm_md](includes/crm_md.md)] user.<br /><br /> If you set the value to **Yes**, [!INCLUDE[prod_short](includes/prod_short.md)] users who don't have a matching [!INCLUDE[crm_md](includes/crm_md.md)] user account won't have [!INCLUDE[prod_short](includes/prod_short.md)] integration capabilities in the user interface. Access to [!INCLUDE[crm_md](includes/crm_md.md)] data directly from [!INCLUDE[prod_short](includes/prod_short.md)] is done on behalf of the [!INCLUDE[crm_md](includes/crm_md.md)] user account.<br /><br /> If you set the value to **No**, all [!INCLUDE[prod_short](includes/prod_short.md)] users will have [!INCLUDE[crm_md](includes/crm_md.md)] integration capabilities in the user interface. Access to [!INCLUDE[crm_md](includes/crm_md.md)] data is done on behalf of the [!INCLUDE[crm_md](includes/crm_md.md)] connection (integration) user.|
    |**Current Business Central Salesperson is Mapped to a User**|Indicates whether your user account is mapped to an account in [!INCLUDE[crm_md](includes/crm_md.md)] double check the name of this field|-->
4. Du kan teste forbindelsesindstillingerne ved at vælge **Forbindelse** og derefter **Test forbindelse**.  

    > [!NOTE]  
    > Hvis datakryptering ikke er aktiveret i [!INCLUDE[prod_short](includes/prod_short.md)], bliver du spurgt, om du vil aktivere den. Du aktiverer datakryptering ved at vælge **Ja** og angive de nødvendige oplysninger. Ellers skal du vælge **Nej**. Du kan aktivere datakryptering senere. Du kan finde flere oplysninger i [Kryptere data i Dynamics 365 Business Central](/dynamics365/business-central/dev-itpro/developer/devenv-encrypting-data) i hjælp til udvikleren og administrationen.  
5. Hvis [!INCLUDE[cds_long_md](includes/cds_long_md.md)]-synkronisering ikke allerede er konfigureret, bliver du spurgt, om du vil bruge standardkonfigurationen for synkronisering. Afhængigt af om du vil bevare poster justeret i [!INCLUDE[cds_long_md](includes/cds_long_md.md)] og [!INCLUDE[prod_short](includes/prod_short.md)], skal du vælge **Ja** eller **Nej**.

<!--
## <a name="show-me-the-process"></a>Show Me the Process

The following video shows the steps to connect [!INCLUDE[prod_short](includes/prod_short.md)] and [!INCLUDE[cds_long_md](includes/cds_long_md.md)]. <br>
  
> [!VIDEO https://www.microsoft.com/en-us/videoplayer/embed/RE4ArlP]

-->

## <a name="customize-the-match-based-coupling"></a>Tilpas den matchbaserede sammenkædning

Fra 2021 udgivelsesbølge 2 kan en administrator angive kriterier for at sammenkæde poster baseret på matches. Du kan starte algoritmen til identiske poster kan startes fra følgende placeringer i [!INCLUDE [prod_short](includes/prod_short.md)]:

* Vis sider, der viser poster, som er synkroniseret med [!INCLUDE [cds_long_md](includes/cds_long_md.md)], f. eks. siderne kunder og varer.  

    Vælg flere poster, vælg derefter den **relaterede** handling, Vælg **Dataverse**, vælg **sammenkædning**, og vælg derefter **matchbaseret sammenkædning**.

    Når du starter den match baserede sammenkædningsproces startes fra en Master dataliste, planlægges et sammenkædningsjob, umiddelbart efter at du har valgt sammenkædningskriterierne.  
* Siden **Dataverse Fuld synkroniseringsgennemgang**.  

    Når hele synkroniseringsprocessen registrerer, at du har ikke-sammenkædede poster både i [!INCLUDE [prod_short](includes/prod_short.md)] og i [!INCLUDE [cds_long_md](includes/cds_long_md.md)], vises der et **Vælg sammenkædningskriterie**-link for den relevante integrationstabel.  

    Du kan starte processen **Kør fuld synkronisering** fra siderne **Konfiguration af Dataverse-forbindelse** og **Opsætning af Dynamics 365-forbindelse**. Du kan også starte den i **Konfigurer en forbindelse til Dataverse**-assisteret installationsprogram, når du har fuldført installationen.  

    Når du starter den matchbaserede sammenkædningsproces startes fra siden **Dataverse Fuld synkroniseringsgennemgang**, planlægges et sammenkædningsjob, umiddelbart efter at du har fuldført opsætningen.  
* Listen **Integrationstabelstilknytning**.  

    Vælg en tilknytning, Vælg handlingen **Sammenkædning**, og vælg derefter **Match-baseret sammenkædning**.

    Når du starter den matchbaserede sammenkædningsproces startes fra en integrationstabeltilknytning, køres der et sammenkædningsjob for alle ikke-tilknyttede poster i tilknytningen. Du kan også vælge ikke-koblede poster på listen for at køre kun opgaven for de pågældende poster.

I alle tre tilfælde åbnes siden **Vælg sammenkædningskriterier**, så du kan definere de relevante sammenkædningskriterier. På denne side kan du tilpasse sammenkædningen med følgende opgaver:

* Vælg de felter, der skal bruges til at matche [!INCLUDE [prod_short](includes/prod_short.md)]-poster med [!INCLUDE [cds_long_md](includes/cds_long_md.md)]-enheder. Du kan angive, om der er forskel på store og små bogstaver.  

* Angiv, om du vil synkronisere, når du har koblet posterne. Hvis der bruges tovejs tilknytning af poster, kan du også angive, hvad der sker, hvis konflikter er angivet på siden **Løs Opdateringskonflikter**.  

* Prioritere den rækkefølge, som poster gennemsøges i, ved at angive en *matchprioritet* for de relevante tilknytningsfelter. [!INCLUDE [prod_short](includes/prod_short.md)] søger efter et match i stigende rækkefølge på grundlag af værdien i feltet **Match prioritet**. En tom værdi i feltet **Match prioritet** er lig med prioriteten 0, som er den højeste prioritet. Felter med prioriteten 0 behandles først.  

* Angiv, om der skal oprettes en ny enhedsforekomst i [!INCLUDE [cds_long_md](includes/cds_long_md.md)], hvis der ikke er en entydig, ikke-sammenkoblet match, ved hjælp af søgekriterierne. Hvis du vil aktivere denne funktion, skal du markere afkrydsningsfeltet **Opret ny, hvis der ikke findes en match**-handling.  

### <a name="view-the-results-of-the-coupling-job"></a>Vis resultaterne af sammenkædningssagen

Hvis du vil have vist resultaterne af sammenkædningssagen, skal du åbne siden **integrationstabeltilknytninger**, vælge den relevante tilknytning, vælge **sammenkædningshandlingen** og derefter vælge handlingen foretag tilknytning af **integrationssammenkædningsjob**.  

Hvis der ikke er flere poster, kan du vælge værdien i kolonnen **Mislykkede** for at åbne en liste over fejl, der beskriver, hvorfor det skete.  

Koblingen mislykkes typisk af følgende årsager:

* Der blev ikke defineret overensstemmende kriterier

    Kør den match-baserede sammenkædning igen, men husk at definere sammenkædningskriterierne.

* Der blev ikke fundet noget resultat for de felter, der er angivet i matchkriterier

    Gentag tilkoblingen med forskellige felter.

* Der er fundet flere matches for flere poster, baseret på de felter, der er angivet i matchende kriterier  

    Gentag tilkoblingen med forskellige felter.

* Der blev fundet et match, men posten er allerede kombineret med en post i [!INCLUDE [prod_short](includes/prod_short.md)]  

    Gentag sammenkædningen med andre felter eller undersøg, hvorfor enheden [!INCLUDE [cds_long_md](includes/cds_long_md.md)] er sammenkædet til den pågældende post i [!INCLUDE [prod_short](includes/prod_short.md)].

> [!TIP]
> For at hjælpe dig med at få et overblik over fremdriften i koblingen viser feltet **sammenkoblet til Dataverse**, om en bestemt post er koblet til en [!INCLUDE [cds_long_md](includes/cds_long_md.md)]-enhed. Du kan bruge feltet **Sammenkoblet med Dataverse** til at filtrere listen over poster, som du synkroniserer.

## <a name="upgrade-connections-from-business-central-online-to-use-certificate-based-authentication"></a>Opgradere forbindelser fra Business Central Online for at bruge certifikatbaseret godkendelse

> [!NOTE]
> Dette afsnit er kun relevant for [!INCLUDE[prod_short](includes/prod_short.md)] online-lejere, der er hosted af Microsoft. Online-arkitekturer, der er hosted af ISV'er og lokale installationer, påvirkes ikke.

I april 2022 udfases [!INCLUDE[cds_long_md](includes/cds_long_md.md)] Office365-godkendelsestypen (username/password). Du kan finde flere oplysninger i [Frarådelse af Office365-godkendelsestype](/power-platform/important-changes-coming#deprecation-of-office365-authentication-type-and-organizationserviceproxy-class-for-connecting-to-dataverse). I marts 2022 [!INCLUDE[prod_short](includes/prod_short.md)] udfases desuden brug af klient hemmelig baseret service-to-service-godkendelse til online lejeres. Du skal bruge certifikatbaseret service-til-tjeneste-godkendelse til forbindelser med [!INCLUDE[cds_long_md](includes/cds_long_md.md)]. [!INCLUDE[prod_short](includes/prod_short.md)] online-lejere, der er hosted af ISV'er og lokale installationer, kan fortsætte med at bruge klientens hemmeligheder til godkendelse.

Hvis du vil undgå at afbryde integration, _skal du opgradere_ forbindelsen til at bruge certifikatbaseret godkendelse. Selvom der er planlagt ændringer for marts 2022, anbefaler vi på det kraftigste, at du opgraderer så hurtigt som muligt. Følgende fremgangsmåde beskriver, hvordan du opgraderer til certifikatbaseret godkendelse. 

### <a name="to-upgrade-your-business-central-online-connection-to-use-certificate-based-authentication"></a>Opgradere forbindelser fra Business Central Online til brug certifikatbaseret godkendelse

1. Afhængigt af om du integrerer med Dynamics 365 Sales, skal du benytte en af følgende fremgangsmåder:
   * Hvis du gør det, skal du åbne siden **Microsoft Dynamics 365-forbindelseskonfiguration**.
   * Hvis du ikke gør det, skal du åbne siden **Dataverse-forbindelseskonfiguration**.
2. Vælg **Forbind**, og derefter **Brug certifikatgodkendelse** til at opgradere forbindelsen til at bruge certifikatbaseret godkendelse.
3. Log ind med administratorrettigheder til Dataverse. Det bør tage mindre end et minut at logge på.

> [!NOTE]
> Du skal gentage disse trin i hvert [!INCLUDE[prod_short](includes/prod_short.md)]-miljø, herunder både produktions-og sandkasse miljøer, og i hvert regnskab, du har forbindelse til [!INCLUDE[cds_long_md](includes/cds_long_md.md)].

## <a name="connecting-on-premises-versions"></a>Tilslutning af lokale versioner

Hvis du vil forbinde [!INCLUDE[prod_short](includes/prod_short.md)] i det lokale miljø med [!INCLUDE[cds_long_md](includes/cds_long_md.md)], skal du angive nogle oplysninger på siden **Konfiguration af Dataverse-forbindelse**.

Hvis du vil oprette forbindelse ved hjælp af en Microsoft Entra-konto, skal du registrere et program i Microsoft Entra ID. Du kan også angive program-id, key vault-hemmeligheden og omdirigere den URL-adresse, der skal bruges. URL-adressen til omdirigering er forudindstillet og bør fungere for de fleste installationer. Du skal konfigurere installationen til at bruge HTTPS. Du kan finde flere oplysninger i [Konfigurere SSL for at sikre forbindelsen til Business Central-webklienten](/dynamics365/business-central/dev-itpro/deployment/configure-ssl-web-client-connection). Hvis du konfigurerer serveren, så den har en anden startside, kan du altid ændre URL-adressen. Klientens hemmelighed gemmes som en krypteret streng i din database. 

### <a name="to-register-an-application-in-microsoft-entra-id-for-connecting-from-business-central-to-dataverse"></a>Sådan registrerer du et program i Microsoft Entra ID for at oprette forbindelse fra Business Central til Dataverse

I følgende trin antages det, at du bruger Microsoft Entra ID til at administrere identiteter og adgangsrettigheder. Du kan finde flere oplysninger om registrering af et program i Microsoft Entra ID under [Hurtig start: registrere et program på Microsoft-identitetsplatformen](/azure/active-directory/develop/quickstart-register-app). 

1. Vælg **Godkendelse** under **Administrer** i navigationsruden på Azure-portalen.  
2. Tilføj under **URL-adresse til omdirigering** den URL-adresse til omdirigering, der foreslås på siden til **Konfiguration af Dataverse-forbindelse** i [!INCLUDE[prod_short](includes/prod_short.md)].
3. Vælg **API-tilladelser** under **Administrer**.
4. Vælg **Tilføj en tilladelse** under **Konfigurerede tilladelser**, og tilføj derefter delegerede tilladelser under fanen **Microsoft API'er** på følgende måde:
    * For Business Central skal du tilføje tilladelserne **Financials.ReadWrite.All**.
    * For Dynamics CRM skal du tilføje tilladelserne **user_impersonation**.  

    > [!NOTE]
    > Navnet på Dynamics CRM-API'en ændres muligvis.

5. Vælg **Certifikater og hemmeligheder** under **Administrer**, og opret derefter en ny hemmelighed til din app. Du skal enten bruge hemmeligheden i [!INCLUDE[prod_short](includes/prod_short.md)], i feltet **Klienthemmelighed** på siden til **Konfiguration af Dataverse-forbindelse** eller gemme den i et sikkert lager og angive den i en hændelsesabonnent som beskrevet tidligere i dette emne.
6. Vælg **Oversigt**, og find derefter **Program-id (klient)**-værdien . Dette id er klient-id til programmet. Du skal enten angive det på siden **Konfiguration af Dataverse-forbindelse** i feltet **Klient-id** eller gemme det i et sikkert lager og angive det i en hændelsesabonnent.
7. I [!INCLUDE[prod_short](includes/prod_short.md)] skal du på siden **Konfiguration af Dataverse-forbindelse** i feltet **URL-adresse for miljø** angive URL-adressen til dit [!INCLUDE[cds_long_md](includes/cds_long_md.md)]-miljø.
8. Du skal aktivere forbindelsen til [!INCLUDE[cds_long_md](includes/cds_long_md.md)] ved at slå **Aktiveret** til.
9. Log på med din administratorkonto til Microsoft Entra ID (kontoen skal have en gyldig licens til [!INCLUDE[cds_long_md](includes/cds_long_md.md)] og være administrator i dit [!INCLUDE[cds_long_md](includes/cds_long_md.md)]-miljø). Når du er logget på, bliver du bedt om at tillade, at dit registrerede program logger på [!INCLUDE[cds_long_md](includes/cds_long_md.md)] på vegne af organisationen. Du skal give samtykke for at fuldføre installationen.

   > [!NOTE]
   > Hvis du ikke bliver bedt om at logge på med din administratorkonto, skyldes det sandsynligvis, at pop op-vinduer er blokeret. Du kan logge på ved at tillade pop op-vinduer fra `https://login.microsoftonline.com`.

### <a name="to-disconnect-from-"></a>Sådan afbrydes forbindelsen fra [!INCLUDE[cds_long_md](includes/cds_long_md.md)]

1. Vælg ![Lightbulb, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **Dataverse-forbindelseskonfiguration**, og vælg derefter det relaterede link.
2. På siden **Dataverse-forbindelsesopsætning** skal du slå **Aktiveret** fra.  

## <a name="see-also"></a>Se også

[Se status på en synkronisering](admin-how-to-view-synchronization-status.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
