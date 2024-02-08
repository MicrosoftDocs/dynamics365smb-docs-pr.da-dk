---
title: Power BI Ofte stillede spørgsmål
description: Få svar på nogle typiske spørgsmål om arbejde med Power BI og Business Central.
author: jswymer
ms.topic: get-started
ms.devlang: al
ms.search.keywords: 'Power BI, reports, faq, errors'
ms.date: 04/22/2021
ms.author: jswymer
ms.service: dynamics-365-business-central
---
# <a name="power-bi--faq"></a>Power BI Ofte stillede spørgsmål

I denne artikel besvares nogle af de spørgsmål, du kan have om at arbejde med Power BI og [!INCLUDE [prod_short](includes/prod_short.md)].

## [Generelt](#tab/general)
<!-- 26 -->
### <a name="ive-selected-a-report-for-my-role-center-in-business-central-if-i-later-make-changes-to-the-reports-visuals-online-will-the-role-center-automatically-update-to-my-changes"></a>Jeg har valgt en rapport for mit rollecenter i Business Central. Hvis du senere foretager ændringer i rapportens visuelle elementer online, opdateres rollecenter automatisk til mine ændringer?

Ja, da rapporterne er integrerede fra Power BI.

<!-- 3 -->
### <a name="are-the-business-central-apps-for-power-bi-available-in-languages-other-than-english"></a>Er Business Central-apps til Power BI tilgængelige på andre sprog end engelsk?

Nej. Disse apps er i øjeblikket kun tilgængelige på engelsk.

<!-- 24 -->
### <a name="once-a-report-is-published-on-mypowerbicomworkspace-can-i-download-its-pbix"></a>Når en rapport er udgivet på mit powerbi.com arbejdsområde, kan jeg hente dets pbix?

Ja. Du kan finde flere oplysninger i [Hente en rapport fra Power BI-tjenesten til Power BI Desktop](/power-bi/create-reports/service-export-to-pbix).  

<!-- 27 -->
### <a name="can-i-download-the-apps-as-pbix-files"></a>Kan jeg hente apps som pbix-filer?

Nej. I øjeblikket tilbyder vi ikke hentning af pbix-filer til de officielle Power BI-apps, fordi de er udgivet på AppSource.

## [Licens](#tab/license)

<!-- 14 -->
### <a name="do-i-need-a-power-bi-pro-license-to-publish-reports"></a>Skal jeg bruge en Power BI Pro-licens for at udgive rapporter?

<!-- todo What does " or for every user that consults the published report" mean? fixed -->
Nej. Det er ikke nødvendigt med en Pro-licens for at udgive rapporter? Standard Power BI-licensen er tilstrækkelig. Du kan finde flere oplysninger i [Power BI-licenser](admin-powerbi-setup.md#license).

<!-- 15 -->
### <a name="is-there-anything-i-cant-do-with-the-free-license"></a>Er der noget, jeg ikke kan gøre med den gratis licens?

Du kan ikke dele rapporter eller installere Business central-apps til Power BI. Derudover kan du oprette næsten alle variationer af diagrammer og rapporter i den gratis licens.

<!-- 16 -->
### <a name="if-someone-shares-a-report-with-another-person-then-that-person-needs-a-pro-license-to-see-the-report-are-there-plans-to-make-this-capability-possible-with-the-free-license"></a>Hvis en person deler en rapport med en anden person, skal denne person have en Pro-licens for at få vist rapporten. Er der planer om at gøre denne mulighed tilgængelig med den gratis licens?

Vi har ikke kontrol over dette krav. Dette krav angives af Power BI. Du kan finde flere oplysninger i [Dele Power BI-dashboards og rapporter med kolleger og andre](/power-bi/collaborate-share/service-share-dashboards).  

## [Designer](#tab/designer)

<!-- 7 -->
### <a name="does-the-connector-work-with-api-pages"></a>Fungerer connectoren med API-sider?

Ja. Fra og med juni 2021 understøtter den nye Power BI-connector både Business Central-webtjenester og API-sider. Du kan finde flere oplysninger i [Aktivere Power BI-connector til at arbejde med Business Central-API'er i stedet for kun med webtjenester](/dynamics365-release-plan/2021wave1/smb/dynamics365-business-central/enable-power-bi-connector-work-business-central-apis-instead-web-services-only).

### <a name="can-i-build-a-power-bi-report-using-the-sales-invoice-lines-or-journal-lines-apis"></a>Kan jeg bygge en Power BI-rapport ved at bruge salgsfakturalinjer eller kladdelinjer-API'er?

De mest almindeligt brugte linjeposter er tilgængelige i [Business Central API'er v 2.0](/dynamics365/business-central/dev-itpro/api-reference/v2.0/)). Du kan derfor bruge dem til at oprette rapporter i Power BI ved at vælge dem i **Dynamics 365 Business Central**-connectoren. Men **linje-API'erne** er kun beregnet til at blive brugt med nogle meget specifikke filtre, og de fungerer muligvis ikke i dit scenarie. Du kan få en fejl i stil med "du skal angive et id eller et dokument-id for at hente linjerne". Du kan løse problemet ved at benytte følgende fremgangsmåde, når du henter data fra Business central til rapporten i Power BI Desktop:

1. I stedet for at medtage datakilden for objektet linjer, skal du tilføje den overordnede datakilde. Du kan f. eks. tilføje **salgsfakturaer** i stedet for **salgsfakturalinjer**.
2. Vælg **transformeringsdata** på Power BI Desktop-handlingslinjen.
3. Vælg den forespørgsel, du lige har tilføjet, f. eks. **salgsfakturaer**.
4. Anvende enhver nødvendig filtrering på posterne for at reducere antallet af poster, der indlæses i rapporten.
5. Rul til højre, indtil du finder en kolonne, der kaldes som linjer, f. eks. **SalesInvoiceLines**.
6. Klik på knappen Udvid i kolonneoverskriften ud for kolonnenavnet.

   :::image type="content" source="media/saleinvoicelines.png" alt-text="Viser kolonnen SalesInvoiceLines i Power BI Desktop.":::
<!-- 11 --> 
### <a name="is-it-possible-to-choose-which-business-central-environment-to-get-data-from-for-power-bi-for-example-like-a-sandbox-or-production-environment"></a>Er det muligt at vælge hvilket Business Central-miljø, der skal hentes data fra Power BI, f. eks. et sandkasse- eller produktionsmiljø?

Ja. Det er nemt at vælge det. Når du etablerer forbindelse til Business Central ved hjælp af connectoren, skal du vælge miljø- og virksomhedsnavn.

<!-- 6 --> 
### <a name="can-i-merge-data-from-several-production-environments-of-the-same-tenant"></a>Kan jeg flette data fra flere produktionsmiljøer af samme lejer?

Ja. I Power BI skal du bare køre handlingen Hent data igen og vælge det ønskede miljø.

<!-- 25 -->
### <a name="which-pages-in-business-central-have-the-power-bi-report-part"></a>Hvilke sider i Business Central har Power BI-rapportdelen?

Der er i øjeblikket nogle få markerede sider, som indeholder en faktaboks med en **Power BI Reports**-del, hvor der kan vises en rapport. 

På listesider er **Power BI Reports**-delen filtreret, så den viser rapporter, der vedrører data på listen. Følgende listetype sider indeholder **Power BI Reports**-delen:

|Side-id|Name|
|-------|----|
|22|Debitoroversigt|
|27|Kreditoroversigt|
|31|Vareoversigt|
|9305|Salgsordreoversigt|
|9308|Købsfakturaer|

Her er andre sider, som indeholder en større, ikke-filtreret **Power BI Reports**-del:

|Side-id|Name|
|-------|----|
|1156|Virksomhedsoplysninger|
|4013|Intelligent cloudindsigt |
|9006|Rollecenter for ordrebehandler|
|9008|Regul.plac. Grundlæggende rollecenter|
|9010|Rollecenter for produktionsplanlægger|
|9015|Sag Project Manager RC|
|9016|Rollecent er for servicesender|
|9022|Rollecenter for virksomhedsleder|
|9024|Rollecenter for sikkerhedsadministrator|
|9026|Salgs & relationen Mgr. RC|
|9027|Rollecenteret Regnskabsmedarbejder|

> [!TIP]
> Vi har ikke planer om at føje den til alle listesider i øjeblikket. Du kan dog oprette en simpel side udvidelse, som tilføjer **Power BI Reports**-delen i en faktaboks. Du kan finde flere oplysninger i [Tilføje Power BI Report-dele til sider](/dynamics365/business-central/dev-itpro/developer/devenv-power-bi-report-parts) i hjælp til udviklere og it-eksperter.

<!-- 5 -->
### <a name="is-there-any-way-to-filter-a-dataset-from-business-central-before-i-pull-it-into-power-bi-instead-of-applying-filters-afterwards"></a>Er der nogen metode til at filtrere et datasæt fra Business Central, *før* jeg trækker det ind i Power BI, i stedet for at anvende filtre bagefter?

Hvis du vil filtrere større datasæt, er det nemmest at angive et filter i Power BI-rapporten ved at redigere den direkte Power Query-formlen. De fleste af de filtre, du angiver, vil blive overført til Business Central via forespørgselsfoldning. Se [Trinvis opdatering for datasæt](/power-bi/admin/service-premium-incremental-refresh).

Der er på nuværende tidspunkt ingen mulighed for at angive et filter til webtjeneste dataene fra Business Central. Hvis programmet har brug for at angive et filter fra Business Central, skal du oprette en brugerdefineret business Central-app til dette formål.

<!-- 10 -->
### <a name="from-power-bi-besides-using-a-query-is-there-another-way-to-get-data-from-business-central-tables-that-dont-have-an-associated-page-for-example-like-the-item-attributes-value-mapping-table"></a>Fra Power BI, ud over at bruge en forespørgsel, er der en anden måde, hvorpå du kan få data fra Business Central-tabeller, som ikke har en tilknyttet side? F. eks. kan du lide tabellen *Værditilknytning for vareattributter*.

Nej. Ikke på nuværende tidspunkt.

<!-- 12 --> 
### <a name="are-published-queries-faster-to-use-than-published-pages"></a>Er udgivne forespørgsler hurtigere at bruge end udgivne sider?

Når det drejer sig om webtjenester, er publicerede forespørgsler normalt hurtigere end tilsvarende udgivne sider. Det er årsagen til, at forespørgsler er optimeret til læsning af data og ikke indeholder dyre udløsere som OnAfterGetRecord.

Webtjenester er baseret på sider eller forespørgsler, der er bygget til adgang fra internettet, og som normalt ikke er optimeret til adgang fra eksterne tjenester. Selvom Business Central-connector stadig understøtter hentning af data fra-webtjenester, opfordrer vi dig til at bruge API-sider i stedet for webtjenester, når det er muligt.

<!-- 13 --> 
### <a name="is-there-a-way-for-an-end-user-to-create-a-web-service-with-a-column-thats-in-a-business-central-table-but-not-a-page-or-will-the-developer-have-to-create-a-custom-query"></a>Har slutbrugeren mulighed for at oprette en webtjeneste med en kolonne i en Business Central-tabel, men ikke en side? Eller skal udvikleren oprette en brugerdefineret forespørgsel?

Det er ikke muligt at føje et nyt felt til en webtjeneste i øjeblikket. API-sider giver fuld fleksibilitet på side strukturen, så en udvikler kan oprette en ny API-side for at imødekomme dette krav. 

<!-- 28 --> 
### <a name="can-i-connect-power-bi-to-a-read-only-database-server-of-business-central-online"></a>Kan jeg oprette forbindelse fra Power BI til en skrivebeskyttet database server for Business Central Online?

Denne funktionalitet vil være tilgængelig snart. Fra og med februar 2022 vil nye rapporter, du opretter på basis af Business Central onlinedata, automatisk forsøge at oprette forbindelse til en skrivebeskyttet database-replika. Dette medfører, at dine rapporter opdateres hurtigere og får mindre indvirkning på ydeevnen, hvis du bruger Business central, mens en rapport opdateres. Det anbefales dog, at du planlægger, at dine rapporter skal opdateres uden for normal arbejdstid, når det er muligt.

Hvis du har gamle rapporter baseret på Business Central-data, kan der ikke oprettes forbindelse til den skrivebeskyttede database-replika.

### <a name="ive-tried-the-preview-of-the-new-connector-for-the-february-2022-update-when-i-connect-to-my-custom-business-central-api-page-i-get-the-error-cannot-insert-a-record-current-connection-intent-is-read-only-how-can-i-fix-it"></a><a name="databasemods"></a>Jeg har prøvet forhåndsversionen af den nye connector til opdatering februar 2022. Når jeg opretter forbindelse til min brugerdefinerede Business Central API-side, får jeg fejlmeddelelsen "Der kan ikke indsættes en post. Den aktuelle forbindelsesmåde er skrivebeskyttet." Hvordan kan jeg løse problemet?

Med den nye connector vil nye rapporter, der bruger Business Central-data, som standard oprette en skrivebeskyttet replika af Business Central-database. Denne ændring vil bringe en forbedring af ydeevnen. Men i sjældne tilfælde kan det medføre en fejl. Denne fejl opstår typisk, fordi den brugerdefinerede API foretager ændringer af Business Central-poster, mens Power BI prøver at hente dataene. Det sker især som en del af AL triggers: OnInit, OnOpenPage, OnFindRecord, OnNextRecord, OnAfterGetRecord og OnAfterGetCurrRecord.

Du kan løse dette problem ved at tvinge Business Central-connector til at tillade denne funktionsmåde i [Bygge Power BI-rapporter, så du får vist Business Central Data - løsning af problemer](across-how-use-financials-data-source-powerbi.md#fixing-problems).

<!--
In general, we recommend avoiding any database modifications in API pages when they're opening or loading records, because they cause performance issues and might cause your report refresh to fail. In some cases, you might still need to make a database modification when your custom API page opens or loads records. You can force the Business Central connector to allow this behavior. Do the following steps when getting data from Business Central for the report in Power BI Desktop:

1. Start Power BI Desktop.
2. In the ribbon, select **Get Data** > **Online Services**.
3. In the **Online Services** pane, select **Dynamics 365 Business Central**, then **Connect**.
4. In the **Navigator** window, select the API endpoint that you want to load data from.
5. In the preview pane on the right, you'll see the following error:

   *Dynamics365BusinessCentral: Request failed: The remote server returned an error: (400) Bad Request. (Cannot insert a record. Current connection intent is Read-Only. CorrelationId: [...])".*

6.  Select **Transform Data** instead of **Load** as you might normally do.
7. In **Power Query Editor**, select **Advanced Editor** from the ribbon.
8.  Replace the following line:

   ```
   Source = Dynamics365BusinessCentral.ApiContentsWithOptions(null, null, null, null),
   ```

   with the line:

   ```
   Source = Dynamics365BusinessCentral.ApiContentsWithOptions(null, null, null, [UseReadOnlyReplica = false]),
   ```

9.  Select **Done**.
10. Select **Close & Apply** from the ribbon to save the changes and close Power Query Editor.

-->
### <a name="how-do-i-change-or-clear-the-user-account-im-currently-using-to-connect-to-business-central-from-power-bi-desktop"></a><a name="perms"></a>Hvordan kan jeg ændre eller rydde den konto, jeg bruger for at oprette forbindelse til Business central fra Power BI Desktop?

Gør ét af følgende i Power BI Desktop:

1. Vælg **Indstillinger** > **Datakildeindstillinger** i menuen filer.
2. Vælg **Dynamics Business central** på listen, og vælg derefter **Ryd tilladelser** > **Slet**.

Næste gang du opretter forbindelse til Business central for at hente data, bliver du bedt om at logge på.

## [Ydeevne](#tab/performance)

<!-- 17 -->

### <a name="is-it-faster-to-get-data-using-api-pages-than-using-web-services"></a>Er det hurtigere at hente data ved hjælp af API-sider end ved brug af webtjenester?

Ja. Vores tests angiver, at API-sider fylder op til 25 % mere end webtjenester.

<!-- 18 -->
### <a name="are-there-plans-to-have-a-mirror-on-the-azure-sql-database-instance-which-i-can-connect-to-directly"></a>Har der planer om at have en spejling på Azure SQL-database forekomsten, som jeg kan oprette forbindelse til direkte?

Nej. Ikke på nuværende tidspunkt. Du kan kun kommunikere med API'er (Business central gennem API'er).

<!-- 19 -->
### <a name="loading-data-from-business-central-web-services-seems-slow-is-there-any-way-to-get-data-directly-from-the-sql-database-table"></a>Indlæsning af data fra Business Central-webtjenester virker langsomt. Er der nogen måde at hente data direkte fra SQL-databasetabellen på?

Nej. Direkte adgang til databasen er ikke mulig, men skifter til API-sider (når den nye Connector er tilgængelig) vil være en hjælp for meget.

## [Avanceret](#tab/advanced)
<!-- 1 -->

### <a name="are-there-plans-for-the-power-bi-connector-to-support-the-incremental-refresh-features-in-the-power-bi-service"></a>Skal der være planer for Power BI-connector for at understøtte de trinvise opdateringsfunktioner i Power BI-tjenesten?

Ja. Den er på vores plan.

<!-- 2 -->
### <a name="if-a-business-central-on-premises-solution-doesnt-have-internet-access-can-i-still-use-power-bi"></a>Hvis en lokal Business Central-løsning ikke har adgang til internettet, kan jeg stadig bruge Power BI?
<!-- todo: please explain this one-->

Ja. I dette tilfælde skal du bruge Power BI Desktop lokalt og oprette forbindelse til Business Central lokalt. Når den er oprettet, kan du oprette og få vist rapporter, men du kan ikke udgive dem til Power BI-tjenesten. 
<!-- 20 -->
### <a name="are-there-any-plans-to-make-it-possible-to-replicate-business-central-online-databases-so-theyre-accessible-for-read-only-sql-queries-this-capability-would-support-incremental-refresh-and-be-a-lot-faster-than-apis-or-web-services"></a>Er der planer om at gøre det muligt at replikere Business Central Online databaser, så de er tilgængelige for skrivebeskyttede SQL-forespørgsler? Denne funktion understøtter trinvis opdatering og er meget hurtigere end API- eller webtjenester.

<!-- todo: what does "BC-Saas-DB-replicated DB accessible" mean? fixe-->
Ja. Vi har denne funktion på en langsigtet plan. 

<!-- 21 -->
### <a name="if-i-use-azure-data-factory-to-get-data-from-business-central-and-consume-it-on-power-bi-will-that-help-in-increase-in-performance"></a>Hvis jeg bruger Azure data Factory til at hente data fra Business Central og bruge dem i Power BI, vil denne hjælpe med at øge ydeevnen?

Ja. Dette avancerede scenario vil hjælpe Business Central permanent, da dataadgang vil blive udført via Azure Data Factory.

<!-- 22 -->
### <a name="are-there-any-plans-to-support-power-bi-deployment-pipelines-or-a-way-to-build-deployment-pipelines-for-pbi-reports-similar-to-extensions-or-maybe-even-a-simple-api-in-the-business-admin-center"></a>Er der planer om at understøtte Power BI-installations-pipelines eller oprette installations-pipelines til PBI-rapporter, f. eks. udvidelser? Eller måske endda en simpel API i Business Administration Center?

Vi undersøger denne funktion. Power BI tilbyder omfattende API'er til styring af rapportimplementeringer. Du kan finde flere oplysninger i [Introduktion to installations-pipelines](/power-bi/create-reports/deployment-pipelines-overview).

### <a name="when-i-get-data-from-business-central-to-use-in-my-power-bi-reports-i-see-some-values-like-_x0020_-what-are-these-values"></a>Når jeg henter data fra Business central til brug i mine Power BI-rapporter, vises nogle værdier som f. eks. "_x0020_ ". Hvad er disse værdier?

Nogle API-sider, herunder de fleste API v 2.0-sider, har felter, der er baseret på [AL Enum-objekter](/dynamics365/business-central/dev-itpro/developer/devenv-extensible-enums). Felter, der er baseret på AL enum-objekter, skal have navne, der er ensartede og altid ens, så filtre i rapporten altid fungerer på samme måde – uanset det sprog eller operativsystem, du bruger. Derfor oversættes de felter, der er baseret på AL enum, og de kodes for at undgå specialtegn, inklusive pladsen. Når der er en tom indstilling i AL Enum-objektet, er det især kodet til "_x0020_". Du kan altid anvende en transformation til dine data på Power BI, hvis du vil have vist en anden værdi for disse felter, f. eks. "Empty".

## <a name="see-also"></a>Se også

[Power BI-licenser](admin-powerbi-setup.md#license)  
[Introduktion til Business Central og Power BI](admin-powerbi.md)  
[Power BI Oversigt over integration](admin-powerbi-overview.md)  
[Aktivere Power BI i Business Central](admin-powerbi-setup.md)  
[Arbejde med Power BI-rapporter i Business Central](across-working-with-powerbi.md)  
[Arbejde med Business Central-data i Power BI](across-working-with-business-central-in-powerbi.md)  
[Oprette Power BI Reports til Display Business Central Data](across-how-use-financials-data-source-powerbi.md)  
[Power BI-dokumentation](/power-bi/)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
