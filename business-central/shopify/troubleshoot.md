---
title: Fejlfinding af Shopify og Business Central-synkronisering
description: 'Få mere at vide om, hvad du skal gøre, hvis noget er galt under synkronisering af data mellem Shopify Business Central.'
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bholtorf
ms.topic: how-to
ms.date: 04/24/2023
ms.custom: bap-template
ms.search.form: '30118, 30119, 30120, 30101, 30102'
ms.service: dynamics-365-business-central
---

# <a name="troubleshooting-the-shopify-and-business-central-synchronization"></a>Fejlfinding af Shopify og Business Central-synkronisering

Du kan køre i situationer, hvor du skal foretage fejlfinding af problemer ved synkronisering af data mellem Shopify og [!INCLUDE[prod_short](../includes/prod_short.md)]. Denne side definerer trin til fejlfinding i forbindelse med typiske scenarier.

## <a name="run-tasks-in-the-foreground"></a>Kør opgaver i forgrunden

1. Vælg ![Lightbulb, der åbner funktionen Fortæl mig 1.](../media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **Shopify Butik**, og vælg det relevante link.
2. Marker den butik, du vil fejlfinde for at åbne siden **Shopify-købskort**.
3. Deaktivér **Tillad baggrundssynkronisering** til/fra.

Når synkroniseringshandlingen udløses, køres opgaven nu i forgrunden. Hvis der opstår en fejl, vises der en fejldialogboks med linket **Kopieringsoplysninger**. Brug linket til at kopiere yderligere oplysninger til en teksteditor til yderligere analyse.

## <a name="logs"></a>Logfiler

Logføringsfunktionerne kan gøre det nemmere at identificere, hvorfor en fejl opstod. På siden **Shopify Køb kort** i feltet **Logføringstilstand** kan du angive det detaljeringsniveau, du vil registrere om fejl. Der er følgende indstillinger til feltet:

- **Deaktiveret** - Log ikke oplysninger om fejl.
- **Kun fejl** - Log kun fejlmeddelelsen uden anmodnings-/svarparrene. Denne indstilling er standardindstillingen for nye butikker.
- **Alle** - Log anmodnings-/svarparrene for alle transaktioner, inklusive dem, der var vellykkede. Logning af alle fejl kan kontinuerligt gøre [!INCLUDE [prod_short](../includes/prod_short.md)] langsommere. Brug denne tilstand, når dataudvekslingen ikke resulterer i fejl, men du ønsker at få mere indsigt i de data, der faktisk blev sendt og modtaget. Bemærk, at nogle data altid logges, uanset om Logfilen er aktiveret. Du kan finde flere oplysninger under [Dataregistrering](#data-capture).

### <a name="to-review-logs"></a>Gennemse logfiler

1. Vælg ![Lightbulb, der åbner funktionen Fortæl mig 1.](../media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **Shopify-logposter**, og vælg det relaterede link.
2. Vælg den relaterede logpost, og åbn derefter siden **Shopify-logpost**.
3. Gennemsynsanmodning, statuskode og beskrivelse og svarværdier.

> [!TIP]
> Hvis du har brug for at kontakte Shopify-support for at få hjælp til fejlfinding, skal du notere oplysningerne i feltet **Anmodnings-id**. Disse oplysninger kan hjælpe med at løse problemet hurtigere.

Du kan hente anmodnings- og svarværdierne som filer i et tekstformat.

### <a name="manage-log-entry-data"></a>Administrere logpostering af data

For at hjælpe med at holde størrelsen på din database under kontrol er logposter inkluderet i en politik for dataopbevaring med navnet **Shopify-logpost**. Opbevaringspolitikker giver dig mulighed for at angive, hvor længe du vil gemme forskellige typer data. Logposter opbevares som standard i Shopify i én måned. Du kan få mere at vide om opbevaringspolitikker i [Definere opbevaringspolitikker](../admin-data-retention-policies.md).

Fra siden **Shopify-logposter** kan du slette alle logposter eller poster, der er ældre end syv dage.

## <a name="data-capture"></a>Dataregistrering

Uanset om Logfilen er aktiveret, registreres nogle Shopify-svar altid. Du kan undersøge eller hente logfilerne fra siden **Dataregistreringsliste**.

Vælg handlingen **Hentet Shopify-data** på en af følgende sider:

- **Shopify-ordre**
- **Shopify-ordrelinje**
- **Shopify-opfyldelser**
- **Shopify-ordreforsendelsesomkostninger**
- **Shopify-ordretransaktioner**
- **Shopify-retur**
- **Shopify-returlinje**
- **Shopify-refusion**
- **Shopify-refusionslinje**
- **Shopify-udbetalinger**
- **Shopify-betalingstransaktioner**
- **Shopify-transaktioner**

## <a name="reset-sync"></a>Nulstil synkronisering

For at opnå optimal ydeevne importerer connectoren kun kunder, produkter og ordrer, der er oprettet eller ændret siden sidste synkronisering. På siden **Shopify-butikskort** er der funktioner, der kan ændres seneste synkroniseringsdato/-tidspunkt eller helt nulstille. Denne funktion sikrer, at alle data synkroniseres og ikke kun ændringerne siden den seneste synkronisering, når synkroniseringen køres.

Denne funktion gælder kun for synkroniseringer fra Shopify til [!INCLUDE[prod_short](../includes/prod_short.md)]. Det kan være nyttigt, hvis du har brug for at gendanne slettede data, f. eks. produkter, kunder eller slettede ordrer.

## <a name="request-the-access-token"></a>Anmode om adgangstoken

Hvis [!INCLUDE[prod_short](../includes/prod_short.md)] ikke kan oprette forbindelse til din Shopify-konto, kan du prøve at nulstille dette adgangstoken fra Shopify. Du skal muligvis anmode om et nyt token, hvis der var ændringer til sikkerhedsnøglerne eller de nødvendige tilladelser (områder).

1. Vælg ![Lightbulb, der åbner funktionen Fortæl mig 1.](../media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **Shopify Butikker**, og vælg det relevante link.
2. Marker den butik, for hvilken du vil have adgangstoken til at åbne siden **Shopify-butikskort**.
3. Vælg handlingen **Anmod om adgang**.
4. Hvis du bliver bedt om det, skal du logge på din Shopify-konto.

Til/fra-knappen **Har AccessKey** er slået til.

## <a name="verify-and-enable-permissions-to-make-http-requests-in-a-non-production-environment"></a>Kontrollere og aktivere tilladelser til at foretage HTTP-anmodninger, når der køres i et ikke-produktionsmiljø

Hvis Shopify-connector-udvidelsen skal fungere korrekt, kræver det, at du har tilladelse til at foretage HTTP-anmodninger. Når der testes i sandkasse, er HTTP-anmodninger forbudt for alle udvidelser.

1. Vælg ![Lightbulb, der åbner funktionen Fortæl mig 1.](../media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **Udvidelsesstyring**, og vælg derefter det relaterede link.
2. Vælg udvidelsens **Shopify Connector**.
3. Vælg handlingen **Konfigurer** for at åbne siden **Udvidelsesindstilling**.
4. Kontroller, at funktionen **Tillad HTTPClient-anmodninger** er aktiveret.

## <a name="rotate-the-shopify-access-token"></a>Rotere Shopify-adgangstoken

Følgende procedurer beskriver, hvordan du kan rotere det adgangstoken, der bruges af Shopify-connector, til at få adgang til dit Shopify online Center.

### <a name="in-shopify"></a>I Shopify

1. Fra din **Shopify Admin** skal du gå til [Apps](https://www.shopify.com/admin/apps).
2. I rækken med **Dynamics 365 Business Central**-appen skal du vælge **Slet**.
3. I meddelelsen, der vises, skal du vælge **Slet**.

### <a name="in-"></a>I [!INCLUDE[prod_short](../includes/prod_short.md)]

1. Vælg ![Lightbulb, der åbner funktionen Fortæl mig 1.](../media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **Shopify-shops**, og vælg derefter det relaterede link.
2. Marker den butik, for hvilken du vil have adgangstoken til at åbne siden **Shopify-butikskort**.
3. Vælg handlingen **Anmod om adgang**.
4. Hvis du bliver bedt om det, skal du logge ind på din Shopify-konto, gennemse personlige oplysninger og tilladelser og derefter vælge knappen **Installer app**.

## <a name="known-issues"></a>Kendte problemer

### <a name="error-the-sales-header-does-not-exist-identification-fields-and-values-document-typequotenoyour-shopify-store"></a>Fejl: Salgshovedet findes ikke. Id-felter og -værdier: Dokumenttype = 'quote',nr. = 'YOUR SHOPIFY STORE'

Hvis du vil beregne den pris, som Shopify Connector opretter midlertidigt salgsdokument (tilbud) til midlertidig kunde (butikskode), og du kan bruge standard pris beregningslogikken til at udføre opgaven. Hvis en tredjepartsudvidelse abonnerer på hændelser i et midlertidigt salgsdokument, er hovedet muligvis ikke tilgængeligt. Det anbefales, at du kontakter udvidelsesudbyderen. Bed dem om at ændre deres kode, så de kan kontrollere, om der er midlertidige poster. I nogle tilfælde er det tilstrækkeligt, at `IsTemporary` tilføjer metoden på det rigtige sted. Du kan få mere at vide om `IsTemporary` ved at gå til [IsTemporary](/dynamics365/business-central/dev-itpro/developer/methods-auto/record/record-istemporary-method). 

Hvis du vil kontrollere, om problemet er forårsaget af et filtypenavn fra tredjepart, skal du bruge linket **Kopier oplysninger til Udklipsholder** i fejlmeddelelsen og kopiere indholdet til tekstredigeringsprogrammet. Oplysningerne indeholder en **AL-kaldestak**, hvor den øverste linje er den linje, hvor fejlen opstod. Det følgende er et eksempel på en AL-kaldestak.

AL-kaldt stak:

```AL
[Object Name]([Object type] [Object Id]).[Function Name] line [XX] - [Extension Name] by [Publisher] 
...
"Sales Line"(Table 37)."No. - OnValidate"(Trigger) line 98 - Base Application by Microsoft
"Shpfy Product Price Calc."(CodeUnit 30182).CalcPrice line 20 - Shopify Connector by Microsoft
"Shpfy Create Product"(CodeUnit 30174).CreateTempProduct line 137 - Shopify Connector by Microsoft
"Shpfy Create Product"(CodeUnit 30174).CreateProduct line 5 - Shopify Connector by Microsoft
"Shpfy Create Product"(CodeUnit 30174).OnRun(Trigger) line 12 - Shopify Connector by Microsoft
"Shpfy Add Item to Shopify"(Report 30106)."Item - OnAfterGetRecord"(Trigger) line 2 - Shopify Connector by Microsoft
"Shpfy Products"(Page 30126)."AddItems - OnAction"(Trigger) line 5 - Shopify Connector by Microsoft
```

Husk at dele oplysninger fra AL-kaldestakken med leverandøren af filtypenavnet.

### <a name="error-gen-bus-posting-group-must-have-a-value-in-customer-your-shopify-store-it-cannot-be-zero-or-empty"></a>Fejl: Gen. Virksomhed-bogføringsgruppe skal have en værdi i Debitor: 'YOUR SHOPIFY STORE'. Den må ikke være nul eller tom

Udfyld feltet **Debitorskabelonkode** på siden **Shopify Butikskort** med den skabelon, som har udfyldt **Virksomhedsbogføringsgruppe**. Debitorskabelonen bruges til at oprette debitorer og til at beregne salgspriser på salgsdokumenter.

### <a name="error-importing-data-to-your-shopify-shop-isnt-enabled-go-to-the-shop-card-to-enable-it"></a>Fejl: Import af data til din Shopify-butik er ikke aktiveret. Gå til butikskortet for at aktivere det

På siden **Shopify-butikskort** skal du slå **Tillad datasynkronisering med Shopify** til. Denne indstilling hjælper med at beskytte onlinebutikken mod at hente demonstrationsdata fra [!INCLUDE[prod_short](../includes/prod_short.md)].

### <a name="error-oauth-error-invalid_request-could-not-find-shopify-api-application-with-api_key"></a>Fejl: Oauth-fejl invalid_request: Kan ikke finde Shopify API-programmet med api_key

Du har evt. brugt [Indlejret app](/dynamics365/business-central/dev-itpro/deployment/embed-app-overview), hvor klientens URL-adresse har formatet: `https://[application name].bc.dynamics.com`. Shopify-connectoren virker ikke for indlejrede apps. Flere oplysninger i [Hvilke Microsoft-produkter er Shopify-connectoren tilgængelige for?](shopify-faq.md#which-microsoft-products-is-the-shopify-connector-available-for).

### <a name="error-internal-error-looks-like-something-went-wrong-on-our-end-request-id-xxxxxxxx-xxxx-xxxx-xxxx-xxxx"></a>Fejl: Intern fejl. Det ser ud til, at noget gik galt. Anmodnings-id: XXXXXXXX-XXXX-XXXX-XXXX-XXXX

Kontakt Shopify support inden for syv dage efter, at du har oplevet fejlen, og Angiv anmodnings-id'et. Du kan få flere oplysninger ved at gå til [Supportmuligheder i Shopify](shopify-faq.md#shopify).

### <a name="error-oauth-error-invalid_request-your-account-does-not-have-permission-to-grant-the-requested-access-for-this-app"></a>Fejl: Oauthfejl invalid_request: Din konto har ikke tilladelse til at give den ønskede adgang til denne app.

Den bruger, der anmodede om adgang, ikke har rettigheder til at administrere apps (mulighed for at administrere og installere apps og kanaler samt potentielt godkende appgebyrer). Du kan muligvis løse dette problem ved at installere appen som kontoejer. Du kan også kontrollere **Apptilladelsen** for brugeren i indstillingerne [**Bruger- og tilladelser**](https://www.shopify.com/admin/settings/account) i din **Shopify administrator**.  

### <a name="messageaccess-denied-for-field-fieldlocationsline0column0pathpathextensionscodeaccess_denieddocumentationhttpsshopifydevapiusageaccess-scopes"></a>[{"meddelelse":"Adgang nægtet for FIELD-feltet.","lokationer":["linje":0,"kolonne":0{],"sti":[}"sti"],"udvidelser":"kode":"ACCESS_DENIED","dokumentation":{https://shopify.dev/api/usage/access-scopes}}]

Anmod om et nyt token, fordi den opdaterede version af connectoren kræver flere tilladelser (programområder). Få mere at vide ved at gå til [Anmod om adgangstoken](#request-the-access-token).

### [API] Ugyldigt API-nøgle eller adgangstoken (ukendt login eller forkert adgangskode)

Anmod om et nyt token, fordi den opdaterede version af connectoren kræver flere tilladelser (programområder). Få mere at vide ved at gå til [Anmod om adgangstoken](#request-the-access-token).

## <a name="see-also"></a>Se også

[Kom i gang med Connectoren til Shopify](get-started.md)
