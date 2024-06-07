---
title: Oprette rapporter i Power BI Desktop for at vise Business Central-data | Microsoft Docs
description: Gøre dine data tilgængelige som en datakilde i Power BI og opbygge nyttige rapporter over status for din virksomhed.
author: jswymer
ms.topic: conceptual
ms.devlang: al
ms.search.keywords: 'business intelligence, KPI, Odata, Power App, SOAP, analysis'
ms.date: 01/22/2024
ms.author: jswymer
ms.service: dynamics-365-business-central
---

# <a name="building-power-bi-reports-to-display--data"></a>Oprette Power BI-rapporter, der viser [!INCLUDE [prod_long](includes/prod_long.md)]-data

Du kan gøre dine [!INCLUDE[prod_long](includes/prod_long.md)]-data tilgængelige som datakilde i Power BI Desktop og opbygge nyttige rapporter over status for din virksomhed.

Denne artikel beskriver, hvordan du kan komme i gang med at bruge Power BI Desktop til at oprette rapporter, der viser [!INCLUDE[prod_long](includes/prod_long.md)]-data.  Når du har oprettet rapporter, kan du udgive dem til din egen Power BI-tjeneste eller dele dem med andre brugere i din organisation. Når disse rapporter er i Power BI-tjenesten, kan de brugere, der er oprettet til den, se rapporterne i [!INCLUDE[prod_long](includes/prod_long.md)].

## <a name="get-ready"></a>Gør dig klar

- Tilmeld dig Power BI-tjenesten.

  Hvis du ikke allerede har tilmeldt dig, skal du gå til [https://powerbi.microsoft.com](https://powerbi.microsoft.com). Når du tilmelder dig, skal du bruge din mailadresse og adgangskode.

- Download [Power BI Desktop](https://powerbi.microsoft.com/desktop/).

  Power BI Desktop er et gratis program, du installerer på din lokale computer. Du kan finde flere oplysninger i [Hurtig start: Opret forbindelse til data i Power BI Desktop](/power-bi/desktop-quickstart-connect-to-data).

- Sørg for, at de data, du vil bruge i rapporten, er tilgængelige som en API-side eller udgivet som en webtjeneste.

  Du kan finde flere oplysninger i [Vise data ved hjælp af API-sider eller OData-webtjenester](admin-powerbi-setup.md#exposedata).

<!--- For [!INCLUDE[prod_short](includes/prod_short.md)] on-premises, get the following information:

  - The OData URL for [!INCLUDE[prod_short](includes/prod_short.md)].
  
    Typically, this URL has the format `http[s]://[computer]:[port]/[serverinstance]/ODataV4`, for example, `https://localhost:7048/BC190/ODataV4`. If you have a multi-tenant deployment, include the tenant in the URL, for example, `https://localhost:7048/BC190/ODataV4?tenant=tenant1`.
  - A user name and web service access key of a [!INCLUDE[prod_short](includes/prod_short.md)] account.

    To get data from [!INCLUDE[prod_short](includes/prod_short.md)], Power BI uses basic authentication. So, you'll need a user name and web service access key to connect. The account might be your own user account, or your organization may have specific account for this purpose.-->

- Download [!INCLUDE [prod_short](includes/prod_short.md)]-rapporttemaet (valgfrit).

  Du kan finde flere oplysninger i [Brug [!INCLUDE [prod_short](includes/prod_short.md)]-rapporttemaet](#theme) i denne artikel.

[!INCLUDE[note-multicompany-reports](includes/note-multicompany-reports.md)]

## <a name="add--as-a-data-source-in-power-bi-desktop"></a><a name="getdata"></a>Tilføje [!INCLUDE[prod_short](includes/prod_short.md)] som en datakilde i Power BI Desktop

Den første opgave i oprettelsen af rapporter er at tilføje [!INCLUDE[prod_short](includes/prod_short.md)] som en datakilde i Power BI Desktop. Når forbindelsen er oprettet, kan du starte med at generere rapporten.

1. Start Power BI Desktop.
2. Vælg **Hent data**.

    Hvis du ikke kan se **Hent data**, skal du vælge menuen **Filer** og derefter **Hent data**.
3. Vælg **Onlinetjenester** på siden **Hent data**.
4. Benyt en af følgende fremgangsmåder i ruden **Onlinetjenester**:

    - Hvis du vil oprette forbindelse til [!INCLUDE [prod_short](includes/prod_short.md)] online, skal du vælge **Dynamics 365 Business Central**, og derefter **oprette forbindelse**.
    <!--- To connect to  [!INCLUDE [prod_short](includes/prod_short.md)] on-premises, select **Dynamics 365 Business Central (on-premises)**, then **Connect**.-->

5. Log på [!INCLUDE [prod_short](includes/prod_short.md)] (kun én gang).

    Hvis du ikke har logget ind [!INCLUDE [prod_short](includes/prod_short.md)] fra Power BI desktop før, bliver du bedt om at logge på.

    - For [!INCLUDE [prod_short](includes/prod_short.md)] online, vælg **Log på**, og vælg derefter den relevante konto. Brug den samme konto, som du bruger til at logge på [!INCLUDE [prod_short](includes/prod_short.md)]. Vælg **Tilslut**, når du er færdig.

    <!--- For [!INCLUDE [prod_short](includes/prod_short.md)] on-premises, first enter the OData URL for [!INCLUDE[prod_short](includes/prod_short.md)], then select **OK**. When prompted, enter the user name and password of the account to use for connecting to [!INCLUDE[prod_short](includes/prod_short.md)]. In the **Password** box, enter the web service access key. When done, select **Connect**.-->

    > [!NOTE]  
    > Når du har oprettet forbindelse til [!INCLUDE[prod_short](includes/prod_short.md)], bliver du ikke bedt om at logge på igen. [Hvordan kan jeg ændre eller rydde den konto, jeg bruger for at oprette forbindelse til Business central fra Power BI Desktop?](/dynamics365/business-central/power-bi-faq?tabs=designer#perms)

6. Når forbindelsen er oprettet, kontakter Power BI til Business Central-service. **Navigations**-vinduerne vises, og der vises tilgængelige datakilder til oprettelse af rapporter. Vælg en mappe for at udvide den og få vist de tilgængelige datakilder. 

   Disse datakilder repræsenterer de webtjenester og API'er, som du har publiceret fra for [!INCLUDE [prod_short](includes/prod_short.md)]. Datakilderne er inddelt i Business Central-miljøer og firmaer. Med Business central online har **Navigator** følgende struktur:

    - **Miljønavn**
      - **Navn på virksomhed**
        - **Avancerede API'er**

          Denne mappe indeholder avancerede API-sider, der er udgivet af Microsoft, ligesom [Business Central-automatiserings API'er](/dynamics365/business-central/dev-itpro/administration/itpro-introduction-to-automation-apis) og [brugerdefinerede API-sider til Business Central](/dynamics365/business-central/dev-itpro/developer/devenv-develop-custom-api). Brugerdefinerede API-sider grupperes yderligere i mapper efter [APIPublisher](/dynamics365/business-central/dev-itpro/developer/properties/devenv-apipublisher-property)/[APIGroup](/dynamics365/business-central/dev-itpro/developer/properties/devenv-apigroup-property)-egenskaber for API-sidens kildekode.

        - **Standard-API'er v 2.0**

          Denne mappe viser de API-sider, der udsættes af [Business Central API v 2.0](/dynamics365/business-central/dev-itpro/api-reference/v2.0/).

        - **Webtjenester \(ældre)**

          Denne mappe viser sider, codeunits og forespørgsler, der er udgivet som webtjenester i Business central.

    <!--
    > [!NOTE]
    > The structure for Business Central on-premises is different because it doesn't support API pages.-->

7. Angiv de datakilder, du vil føje til dine datamodel, og vælg derefter knappen **Indlæsning**.
8. Hvis du senere vil tilføje flere Business Central-data, kan du gentage de forrige trin.

Når dataene er indlæst, kan du se dem i den højre navigation på siden. Nu har du oprettet forbindelse til dine [!INCLUDE[prod_short](includes/prod_short.md)]-data og er klar til at begynde at oprette din Power BI-rapport.  

> [!TIP]
> Du kan finde flere oplysninger om brugen af Power BI Desktop under [Introduktion til Power BI Desktop](/power-bi/fundamentals/desktop-getting-started).

## <a name="creating-accessible-reports"></a>Oprette tilgængelige rapporter

Det er vigtigt, at du gør dine rapporter brugbare for så mange personer som muligt. Prøv at designe rapporter, så de ikke kræver særlig tilpasning for at imødekomme specifikke behov hos forskellige brugere. Sørg for, at designet gør det muligt for brugere at udnytte standard hjælpeteknologier som f. eks. skærmlæsere. Power BI indeholder forskellige funktioner til hjælp til handicappede, værktøjer og retningslinjer, som kan hjælpe dig med at opnå dette mål. Du kan finde flere oplysninger i [Designe Power BI-rapporter for tilgængelighed](/power-bi/create-reports/desktop-accessibility-creating-reports) i Power BI-dokumentationen.

## <a name="creating-reports-to-display-data-associated-with-a-list"></a>Oprette rapporter for at vise data, der er knyttet til en liste

Du kan oprette rapporter, der vises i en faktaboks på en [!INCLUDE [prod_short](includes/prod_short.md)]-listeside. Rapporterne kan indeholde data om den post, der er valgt på listen. Oprettelse af disse rapporter minder om andre rapporter, men der er nogle ting, du skal gøre for at sikre, at rapporterne vises som forventet. Du kan finde flere oplysninger i [Oprette Power BI-rapporter til visning af listedata i [!INCLUDE[prod_short](includes/prod_short.md)]](across-how-use-powerbi-reports-factbox.md).

## <a name="using-the--report-theme-optional"></a><a name="theme"></a>Brug af [!INCLUDE [prod_short](includes/prod_short.md)]-rapporttemaet (valgfrit)

Før du opretter rapporten, anbefales det, at du downloader og importerer [!INCLUDE [prod_short](includes/prod_short.md)]-temafilen. Temafilen opretter en farvepalet, så du kan oprette rapporter med de samme farvenuancer som [!INCLUDE [prod_short](includes/prod_short.md)]-apps, uden at du skal definere brugerdefinerede farver til hvert visuelle element.

> [!NOTE]
> Denne opgave er valgfri. Du kan altid oprette dine rapporter og derefter downloade og anvende typografiskabelonen senere.

### <a name="download-the-theme"></a>Downloade temaet

Temafilen er tilgængelig som en json-fil i Microsoft Power BI Community-temagalleriet. Benyt følgende fremgangsmåde for at downloade temafilen:

1. Gå til [Microsoft Power BI Community-temagalleriet til Microsoft Dynamics 365 Business Central](https://community.powerbi.com/t5/Themes-Gallery/Microsoft-Dynamics-365-Business-Central/m-p/385875).
2. Vælg den vedhæftede fil **Microsoft Dynamics Business Central.json**.

### <a name="import-the-theme-on-a-report"></a>Indlæse temaet i en rapport

Når du har downloadet [!INCLUDE [prod_short](includes/prod_short.md)]-rapporttemaet, kan du indlæse det i rapporterne. Hvis du vil indlæse temaet, skal du vælge **Vis** > **Temaer** > **Søg efter temaer**. Du kan finde flere oplysninger i [Power BI Desktop - Indlæse brugerdefinerede rapporttemaer](/power-bi/create-reports/desktop-report-themes#import-custom-report-theme-files).

## <a name="publish-reports"></a>Udgive rapporter

Når du har oprettet eller redigeret en rapport, kan du udgive rapporten til Power BI-tjenesten og dele den med andre i din organisation. Når den er udgivet, kan du se rapporten i Power BI. Rapporterne kan derefter også vælges i [!INCLUDE[prod_short](includes/prod_short.md)].

Hvis du vil udgive en rapport, skal du vælge **Udgiv** på fanen **Startside** på båndet eller i menuen **Filer**. Hvis du er logget på Power BI-tjenesten, udgives rapporten til denne tjeneste. Ellers bliver du bedt om at logge på. 

## <a name="distribute-or-share-a-report"></a>Distribuere eller dele en rapport

Du kan få rapporter ud til dine kolleger og andre på flere måder:

- Distribuer rapporter som .pbix-filer.

    Rapporter gemmes på din computer som .pbix-filer. Du kan distribuere rapportfilen .pbix til brugere ligesom andre filer. Derefter kan brugerne overføre filen til deres Power BI-tjeneste. Se [Overføre rapporter fra filer](across-working-with-powerbi.md#upload).

    > [!NOTE]
    > Hvis du distribuerer rapporter på denne måde, betyder det, at opdatering af data til rapporter udføres individuelt af hver bruger. Denne situation kan have indflydelse på ydeevnen af [!INCLUDE[prod_short](includes/prod_short.md)].

- Dele rapporter fra Power BI-tjenesten

    Hvis du har en Power BI Pro-licens, kan du dele rapporten med andre direkte fra Power BI-servicen. Du kan finde flere oplysninger i [Power BI - Dele et dashboard eller en rapport](/power-bi/collaborate-share/service-share-dashboards#share-a-dashboard-or-report).

## <a name="fixing-problems"></a>Løsning af problemer

### <a name="cant-insert-a-record-current-connection-intent-is-read-only-error-connecting-to-custom-api-page"></a>"Kan ikke indsætte en post. Den aktuelle forbindelsesmåde er skrivebeskyttet." Fejl ved oprettelse af forbindelse til brugerdefineret API-side

> **GÆLDER FOR:** Business Central online

Fra og med februar 2022 vil nye rapporter, der bruger Business Central-data, som standard oprette en skrivebeskyttet replika af Business Central-database. I sjældne tilfælde får du vist en fejlmeddelelse, når du forsøger at oprette forbindelse til og hente data fra siden, afhængigt af side designet.

1. Start Power BI Desktop.
2. På båndet vælges **Hent data** > **Onlinetjenester**.
3. I ruden **online tjenester** vælges **Dynamics 365 Business Central**, og klik derefter på **Opret forbindelse**.
4. Vælg det API-slutpunkt, du vil indlæse data fra, i vinduet **Navigator**.
5. I indholdsruden til højre vises følgende fejlmeddelelse:

   *Dynamics365BusinessCentral: Anmodningen mislykkedes: Fjernserveren returnerede en fejl: (400) forkert anmodning. (Kan ikke indsætte en post. Den aktuelle forbindelsesmåde er skrivebeskyttet. Korrelations-id: [...])".*

6. Vælg **transformeringsdata** i stedet for **Indlæs** som, som du ellers kan gøre.
7. Vælg **Avanceret Editor** på båndet i **Power Query Editor**.
8. Erstat følgende tekst på den linje, der starter med **source =**:

   ```
   Dynamics365BusinessCentral.ApiContentsWithOptions(null, null, null, null)
   ```

   med:

   ```
   Dynamics365BusinessCentral.ApiContentsWithOptions(null, null, null, [UseReadOnlyReplica = false])
   ```

9. Vælg **Udført**.
10. Vælg **Luk og Anvend** på båndet for at gemme ændringerne og lukke Power Query-editoren.

## <a name="see-also"></a>Se også

[Aktivering af dine virksomhedsdata for Power BI](admin-powerbi-setup.md)  
[Business Intelligence](bi.md)  
[Blive køreklar](ui-get-ready-business.md)  
[Importer virksomhedsdata fra andre økonomisystemer](across-import-data-configuration-packages.md)  
[Opsætning af [!INCLUDE[prod_short](includes/prod_short.md)]](setup.md)  
[Finans](finance.md)  
[Hurtig start: Opret forbindelse til data i Power BI Desktop](/power-bi/desktop-quickstart-connect-to-data)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
