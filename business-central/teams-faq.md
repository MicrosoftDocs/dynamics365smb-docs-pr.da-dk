---
title: 'Teams, ofte stillede spørgsmål'
description: Få svar på nogle typiske spørgsmål om arbejde med Teams og Business Central.
author: jswymer
ms.author: jswymer
ms.topic: faq
ms.search.keywords: 'Teams, MS Teams, Microsoft Teams, Skype, Link, Microsoft 365, collaborate, collaboration, teamwork, faq, errors'
ms.date: 09/28/2022
ms.custom: bap-template
---
# Teams, ofte stillede spørgsmål

[!INCLUDE [online_only](includes/online_only.md)]

I denne artikel besvares nogle af de spørgsmål, du kan have om at arbejde med Microsoft Teams og [!INCLUDE [prod_short](includes/prod_short.md)].

## [Generelt](#tab/general)

### Hvordan logger jeg på [!INCLUDE [prod_short.md](includes/prod_short.md)]-appen i Teams?

Når du har installeret appen, bliver du bedt om at logge på, første gang du bruger appen, indsætte et link til [!INCLUDE [prod_short.md](includes/prod_short.md)] i Teams-chatten eller vælge handlingen **Detaljer** på et kort i Teams. Afhængigt af Teams-klienten skal du muligvis angive dine legitimationsoplysninger, som du bruger til at få adgang til [!INCLUDE [prod_short.md](includes/prod_short.md)].

### Hvordan logger jeg ud fra [!INCLUDE [prod_short.md](includes/prod_short.md)]-appen i Teams?

Hvis du vil logge ud af den nuværende brugeridentitet i Teams, som bruges til at oprette forbindelse til [!INCLUDE [prod_short.md](includes/prod_short.md)], skal du gå til en vilkårlig chatboks og vælge ikonet for [!INCLUDE [prod_short.md](includes/prod_short.md)] nedenfor og vælge **Indstillinger**. Når vinduet vises, skal du kontrollere den identitet, der er logget på i øjeblikket, og derefter vælge **Log af**.

### Er appen for Teams tilsluttet [!INCLUDE [prod_short.md](includes/prod_short.md)] på stedet? 

Nej [!INCLUDE [prod_short.md](includes/prod_short.md)]-appen for Teams fungerer kun sammen med [!INCLUDE [prod_short.md](includes/prod_short.md)] online. Der er ingen planer om at understøtte [!INCLUDE [prod_short.md](includes/prod_short.md)]-installationstyper&mdash;f.eks. i det lokale miljø, hybrid-sky eller privat sky&mdash;som Microsoft hverken er vært for eller administrerer direkte.

### Fungerer appen med flere virksomheder og miljøer? 

Ja. Hvis du vil søge efter kontakter i et andet regnskab, skal du gå til [Indstillinger](across-teams-settings.md). Når [!INCLUDE [prod_short.md](includes/prod_short.md)]-appen udvider et link til et kort, skal tilknytningen indeholde miljø- og firmanavnene for appen for at matche posten i den rigtige virksomhed. Du kan indsætte links til virksomheder og miljøer, som du har adgang til i virksomheden og fra den [!INCLUDE [prod_short.md](includes/prod_short.md)]-konto, du har brugt til at logge på. Deltagerne i chatten vil se kortet. Men de kan ikke se kortdetaljerne, medmindre de har tilladelse til det firma eller -miljø, hvor denne post er gemt.

### I hvilke lande eller områder er [!INCLUDE [prod_short.md](includes/prod_short.md)]-appen tilgængelig? 

[!INCLUDE [prod_short.md](includes/prod_short.md)]-appen til Teams er ikke begrænset af land eller område. Appen er tilgængelig på alle markeder, der aktuelt understøttes af markedspladsen Teams. 

### Kan [!INCLUDE [prod_short.md](includes/prod_short.md)]-appen fungere med enhver lokalisering af [!INCLUDE [prod_short.md](includes/prod_short.md)]? 

Ja. Appen er beregnet til at fungere sammen med enhver lokalisering af [!INCLUDE [prod_short.md](includes/prod_short.md)], om denne lokalisering tilbydes direkte fra Microsoft eller fra en partner. Flere oplysninger i [Tilgængelighed i land/område og understøttede sprog](/dynamics365/business-central/dev-itpro/compliance/apptest-countries-and-translations?toc=/dynamics365/business-central/toc.json).

### <a name="language"></a>Hvilke sprog [!INCLUDE [prod_short.md](includes/prod_short.md)] understøtter app'en?

To ting bestemmer det sprog, der bruges til kort- og kort detaljer i Teams:

1. Dit sprog i Teams, som du kan se fra kontoindstillingerne i Teams. 
2. Dit sprog i [!INCLUDE [prod_short.md](includes/prod_short.md)], som du kan se [!INCLUDE [prod_short.md](includes/prod_short.md)]-webklienten med (Se [Skift af grundlæggende indstilling - sprog](ui-change-basic-settings.md#language)).

I følgende tabel forklares det, hvordan oplevelsen adskiller sig fra meddelelses forfattere og-modtagere, afhængigt af sprogindstillingerne og tilgængeligheden af sprog.

|Hvem|Kort|Kortdetaljer |
|-|----|--------------| 
|Meddelelsesforfatter |Vises på det sprog, der er angivet for dig i Teams. Hvis [!INCLUDE [prod_short.md](includes/prod_short.md)] ikke tilbyder det samme sprog, vises kortet på engelsk. |Vises på det sprog, der er angivet for dig i [!INCLUDE [prod_short.md](includes/prod_short.md)], hvilket kan omfatte sprog fra apps, som er leveret af partnere. |
|Meddelelsesmodtager |Vises på sproget for meddelelsens forfatter. |Vises på det sprog, der er angivet for dig i [!INCLUDE [prod_short.md](includes/prod_short.md)]. |

Du kan finde en liste over understøttede sprog til [!INCLUDE [prod_short.md](includes/prod_short.md)] i [Understøttede sprog](/dynamics365/business-central/dev-itpro/compliance/apptest-countries-and-translations?toc=/dynamics365/business-central/toc.json#supported-languages).

### Samarbejder appen [!INCLUDE [prod_short.md](includes/prod_short.md)] med andre brancheløsninger?

Ja. Det er imidlertid kun nogle funktioner i appen, der fungerer med [Integrer apps](/dynamics365/business-central/dev-itpro/deployment/embed-app-overview):

- Appen fungerer sammen med links, der er baseret på mønsteret for **\*.bc.dynamics.com**, som typisk bruges sammen med Integrer apps.
- Kontaktsøgning er ikke tilgængelig for Integrer apps, som erstatter basisprogrammet fra Microsoft.

### Arbejder [!INCLUDE [prod_short.md](includes/prod_short.md)] med Teams mobilapp?

Ja. Appen [!INCLUDE [prod_short.md](includes/prod_short.md)] kan installeres fra den Teams desktopappen eller browseren - eller af en administrator for alle brugere. Når [!INCLUDE [prod_short.md](includes/prod_short.md)]-appen er installeret, er den automatisk tilgængelig i Teams til iOS og Android. På mobilenheder kan du kun få vist kort, der er sendt af andre, få adgang til oplysninger, eller du kan få vist kortet i sin helhed i [!INCLUDE [prod_short.md](includes/prod_short.md)]-mobilappen. Du kan dog ikke indsætte links, som kan udvides til kort, når du opretter meddelelser eller søger efter kontakter. Flere oplysninger om minimumskrav til mobil under [Minimumskrav til brug af Business Central](product-requirements.md).

### Er [!INCLUDE [prod_short.md](includes/prod_short.md)]-appen til Teams den samme som [!INCLUDE [prod_short.md](includes/prod_short.md)]-appen til iOS og Android?

Nej Appen til Teams er et tilføjelsesprogram til Microsoft Teams og er udelukkende beregnet til samarbejde i Teams. På den anden side giver [!INCLUDE [prod_short.md](includes/prod_short.md)]-mobilappen en omfattende oplevelse, så du kan arbejde med [!INCLUDE [prod_short.md](includes/prod_short.md)]-data på dine mobilenheder.

Mobilbrugere opfordres til at installere både mobilappen og appen til Teams for at få mest muligt ud af [!INCLUDE [prod_short.md](includes/prod_short.md)]. Når begge er installeret, kan du vælge **Pop op**-handlingen på et kort i Teams for at åbne kortdetaljerne i [!INCLUDE [prod_short.md](includes/prod_short.md)]-mobilappen. Flere oplysninger om installation af [!INCLUDE [prod_short.md](includes/prod_short.md)] og Teams mobilapps på:

- [Hent Business Central til din mobilenhed](install-mobile-app.md)
- [Hent Teams mobilappen](https://support.microsoft.com/office/download-the-mobile-app-for-teams-5940ebdc-0082-4fb1-83c4-751edc23dcb5) på Microsoft Support

### Fungerer [!INCLUDE [prod_short.md](includes/prod_short.md)]-appen i alle Teams-klienter?

Nej Appen [!INCLUDE [prod_short.md](includes/prod_short.md)] til Teams understøttes ikke, når den installeres som en pakke til macOS eller Linux. På disse platforme kan du få adgang til Teams ved hjælp af en understøttet webbrowser i stedet.

Du kan se minimumskrav til [!INCLUDE [prod_short.md](includes/prod_short.md)] i [Minimumskrav til brug af Business Central](product-requirements.md#teams).

Der er flere oplysninger om, hvordan du vælger Teams-klienter, og hvordan du installerer dem, i [Hent klienter til Microsoft Teams](/microsoftteams/get-clients)-dokumentationen til Teams.

### Hvilke Teams-klienter er bedst til [!INCLUDE [prod_short.md](includes/prod_short.md)]?

Der er kun mindre forskelle og begrænsninger mellem Teams-klienter, som kan påvirke din oplevelse med [!INCLUDE [prod_short.md](includes/prod_short.md)]-appen til Teams. Når du vælger en Teams-klient, skal du overveje:

- Du kan ikke få adgang til kameraet og lokationen i oplysningsvinduet i computerappen for Teams.
- Telefonnumre kan ikke aktiveres fra oplysningsvinduet i Teams til iOS, Team til iOS, Android eller Teams i browseren.
- Bruger du Microsoft Edge sammen med Teams i browseren, kan du nemt arbejde på tværs af flere identiteter og konti ved at logge på Teams fra forskellige profiler. Du kan lære mere om brugen af profiler i Microsoft Edge under [Log på og opret flere profiler i Microsoft Edge](https://support.microsoft.com/office/sign-in-and-create-multiple-profiles-in-microsoft-edge-df94e622-2061-49ae-ad1d-6f0e43ce6435) i Microsoft Support.

### Hvordan kan jeg bedst demonstrere [!INCLUDE [prod_short.md](includes/prod_short.md)] og Microsoft Teams til mulige kunder?

Hvis du er en forhandlingspartner, kan det være en god idé at have et miljø, som du kan vise som del af salgsdemonstrationer. Hvis du vil undgå at påvirke Microsoft Teams i din organisation, kan du få en Microsoft 365-demokonto på [https://aka.ms/CDX](https://aka.ms/CDX). Denne konto giver dig fuld kontrol over en uafhængig Azure-organisation, der omfatter Microsoft Teams og [!INCLUDE [prod_short.md](includes/prod_short.md)]. Du kan finde flere oplysninger i [Forberede demonstrationsmiljøer i Dynamics 365 Business Central](/dynamics365/business-central/dev-itpro/administration/demo-environment).

### Passer [!INCLUDE [prod_short.md](includes/prod_short.md)]-appen til Teams til min opsætning og brugertilpasning?

[!INCLUDE [prod_short.md](includes/prod_short.md)]-appen til Teams kan vise kort for links til kundesider og tabeller i [!INCLUDE [prod_short.md](includes/prod_short.md)], f.eks. de sider og tabeller, der stammer fra dine egne brugerdefinerede udvidelser eller fra AppSource.

De felter, der vises på et kort i Teams, kan også være påvirket af de [!INCLUDE [prod_short.md](includes/prod_short.md)]-tilpasninger, der er installeret i organisationen. Kort overvejer ikke rollespecifikke tilpasninger eller brugertilpasninger. I vinduet kortoplysninger vises dog postoplysninger, som du kan se dem i [!INCLUDE [prod_short.md](includes/prod_short.md)], herunder alle udvidelser, rolle tilpasninger og brugertilpasninger.

Når du søger efter kontakter, påvirkes de felter, der er tilknyttet i tabellen **Kontakter**, og de felter, der vises i søgeresultaterne, påvirkes ikke af tilpasninger eller personlige indstillinger.

### Hvordan påvirker de tilladelser, der kræves af app'en, mine personlige oplysninger?

Før du installerer [!INCLUDE [prod_short.md](includes/prod_short.md)]-appen for Team, kan du gennemse de tilladelser, der som minimum kræves, for at appen kan fungere. Når du installerer app'en, accepterer du, at appen har tilladelse til at modtage meddelelser og data, som du angiver, og Teams har tilladelse til at gemme og behandle disse meddelelser.

Nogle [!INCLUDE [prod_short.md](includes/prod_short.md)]-funktioner kræver også åbning af eksterne hyperlinks eller adgang til kameraet eller geografisk placering. Antag, at du vil tage et billede af en købsfaktura for at blive behandlet. Denne [!INCLUDE [prod_short.md](includes/prod_short.md)]-app bruger ikke disse muligheder uden din tilladelse, og de bruges kun af bestemte funktioner i vinduet **Detaljer**. Når du bruger en af disse funktioner første gang, vises der en dialogboks, hvor du bliver spurgt, om du vil give adgang til de nødvendige enhedsegenskaber.

- På skrivebordet for grupper gennemgås og tilpasses App-tilladelser fra vinduet **Indstillinger**. Vælg et profilbillede øverst i app'en, vælg **indstillinger** > **Tilladelser**, og vælg derefter [!INCLUDE [prod_short.md](includes/prod_short.md)]-appen.

- For Teams i browseren og Teams til iOS eller Android kan du gennemse eller ændre tilladelser fra browseren eller enhedens indstillinger.

> [!NOTE]
> Nøjagtigt, hvilke [!INCLUDE [prod_short.md](includes/prod_short.md)]-funktioner der beder dig om tilladelser, afhænger af de tilføjelsesprogrammer og tilpasninger [!INCLUDE [prod_short.md](includes/prod_short.md)], som du opretter forbindelse til.

### Hvor kan jeg se mere om mine personlige oplysninger? 

Du kan få mere at vide om, hvordan Microsoft håndterer dine data i [Microsofts erklæring om beskyttelse af personlige oplysninger](https://go.microsoft.com/fwlink/?linkid=2030602). 

Kontakt administratoren for at få mere at vide om, hvordan virksomheden håndterer beskyttelsen af dine data.

### Hvordan afinstallerer jeg [!INCLUDE [prod_short.md](includes/prod_short.md)]-appen i Teams?

Hvis du vil fjerne den app, du har installeret til dig selv, skal du gå til en vilkårlig chatboks, finde ikonet for [!INCLUDE [prod_short.md](includes/prod_short.md)] nedenfor, højreklikke på ikonet og vælge **Fjern**.  

### Fortsætter Microsoft med at forbedre [!INCLUDE [prod_short.md](includes/prod_short.md)]-appen for Teams?

Hos Microsoft lytter vi hele tiden til feedback fra vores forskellige grupper af brugere og handler på de mest interessante forslag. Du kan finde flere oplysninger om kommende nyheder for appen [!INCLUDE [prod_short.md](includes/prod_short.md)] til Teams, i [Dynamics 365-udgivelsesplaner](/dynamics365-release-plan/2021wave1/).

Hvis du vil deltage i forbedringen af appen til Teams eller har en god ide til at forenkle dit arbejde eller dine samarbejdsoplevelser i Teams, kan du tilføje en idé eller tilslutte dig eksisterende ideer på [https://aka.ms/BusinessCentralIdeas](https://aka.ms/BusinessCentralIdeas).

### Hvor kan jeg finde Teams-integrationen i Business Central-webklienten? 

Flere oplysninger om funktioner i den webklient, der er sammenkædet med grupper, kan du se i [Links til deling af poster og side i Microsoft Teams](across-working-with-teams.md#share-link).

## [Business Central-faner](#tab/tabs)

### <a name="who-can-view"></a>Hvem kan se indholdet af en fane?

En person i chat eller kanal, som har:

1. Business Central-appen til Teams installeret.
2. Enten en Business Central-licens eller har fået adgangstilladelse til Business Central ved hjælp af Microsoft 365-licensen.
3. Tilladelse til at få vist dataene på siden.

### <a name=#recommended-content></a>Hvor kommer det anbefalede indhold fra?

Det anbefalede indhold, som du kan vælge mellem under **fane-indhold** på en fane, er baseret på dit rollecenter. Anbefalet indhold omfatter kun listesider, f. eks. kunder, salgsordrer og leverandører - ikke individuel kortside for en bestemt kunde eller leverandør.

Særligt, anbefalet indhold omfatter:

- Handlinger i den øverste navigationsmenu i Rollecenter
- Alle listesider, du har givet et bogmærke.
- Hvis en listeside indeholder forskellige visninger, herunder alle visninger, du har oprettet, kan du også vælge mellem disse visninger

Du kan føje listesider til det anbefalede indhold ved at tilføje bogmærker. Du kan også fjerne anbefalet indhold ved at slette bogmærker. Du kan finde flere oplysninger om, hvordan du tilføjer eller sletter bogmærker, i [Bogmærke på en side eller i en rapport i dit rollecenter](ui-bookmarks.md).

Hvis du skifter miljø eller regnskab under fanen fane, ændres det anbefalede indhold, der er baseret på rollecenteret og bogmærker for det miljø og den virksomhed, som du skifter til.

### Når jeg opretter en fane, giver den tilladelse til personerne i kanalen eller chatten?

Nej Oprettelse af tabulatorer påvirker ikke tilladelser, og brugere skal allerede have tilladelse til disse data, når de åbner fanen.

### Kan jeg chatte ved siden af en fane?

Ja. Start samtalen ved hjælp af ikonet chat. Derefter knyttes denne chattråd til fanen. 

### Er alle Business Central-data slettet, hvis jeg fjerner en fane fra en chat eller kanal?

Nej

### Kan jeg omdøbe en fane sikkert?

Ja. Indholdet under fanen er ikke relateret til fanens faktiske navn. Omdøb ved vilje! 

### Jeg har brug for at arbejde på tværs af opgaver i forskellige vinduer. Kan jeg gøre dette?

Ja. Du kan få vist fanen med sit eget browservindue, så du kan se Business Central-webklient. 

### Kan jeg tilføje eller fastgøre faner i Teams-møder?

Nej Business central-app'en for Teams understøtter ikke faner i møder.

### Der kan ikke tilføjes en fane, hvis der bruges ISV-URL-adresser som *. bc.dynamics.com (men de kan fastgøres)

Ikke understøttet.

### Når jeg gør noget under fanen, f.eks. navigere, sortere igen, anvende et filter eller søge, kan andre se mine ændringer?

Nej Kun feltændringer eller kørselshandlinger påvirker, hvordan andre ser indholdet under fanen.

### Opdateres faneindholdet automatisk? Hvis ikke, hvordan foretager jeg en opdatering?

Indholdet opdateres ikke automatisk, og der er ingen automatiske opdateringsknapper. Den bedste måde at opdatere indholdet på for at sikre, at det er op til data, skal du forlade fanen og derefter vende tilbage. 

### Vises og registreres der poster fra mine tilpasninger og tilføjelsesprogrammer?

Ja. 

### Når jeg tilføjer en fane, kan de ses på mit sprog?

Nej Hver bruger får en visning af faneindholdet i indstillingerne sprog, område og tidszone fra Business central. 

### Kan jeg have flere faner, der peger på andet indhold?

Ja.

### Kan jeg også tilføje faner til chat med en enkelt person?

Ja, så længe chatten ikke er en kladde (dvs. en meddelelse er ikke blevet sendt til at starte denne chat), og den anden person har installeret Business Central-appen.

### Kan jeg skifte virksomhed under en fane?

Nej 

### Er dette anderledes end brugen af Teams generiske mulighed for at oprette en fane, der fungerer som vært for et websted?

Ja. Det anbefales, at du ikke bruger visningen. I mange tilfælde fungerer det ikke for Business central.

## [Søg efter kontakter](#tab/contacts)

### Hvilke tabeller søger appen i?

Når du søger efter kontakter fra appen [!INCLUDE [prod_short.md](includes/prod_short.md)] til Teams, bliver dine søgeord sammenlignet med poster i tabellen **Kontakter** i [!INCLUDE [prod_short.md](includes/prod_short.md)]. 

### Hvilke felter i tabellen over kontakter kan jeg søge i?

Når du skriver dine søgeord i søgefeltet, sammenlignes udtrykkene med de fleste felter i tabellen **Kontakter**. Disse felter omfatter f.eks. **Nummer**, **Navn**, **Adresse**, **Telefonnr.** eller felterne **Mobilnr.** og **Mail**. 

Søgeord matches ikke med brugerdefinerede felter, der er føjet til tabellen **Kontaktpersoner** af apps og udvidelser.

### Omfatter søgeresultater virksomheder og personer?

Ja. I [!INCLUDE [prod_short.md](includes/prod_short.md)] kan kontakter være af typen **Virksomhed** eller **Person**, hvor en eller flere personer kan være knyttet til en virksomhed. I søgeresultaterne kan virksomheder og personer have forskellige ikoner.

### Vises kontakterne for en forretningsrelation i resultaterne?

Ja. Nogle kontakter kan repræsentere debitorer eller kreditorer eller begge dele. Andre kontakter uden defineret forretningsforbindelse repræsenterer typisk potentielle kunder. Kontakter med andre forretningsforbindelser, herunder de brugerdefinerede relationer, du har konfigureret i [!INCLUDE [prod_short.md](includes/prod_short.md)], vises også i søgeresultaterne.

### Kan jeg søge efter kontaktoplysninger under møder?

Ja. Du kan søge efter kontaktoplysninger, interaktionshistorik og relaterede dokumenter for debitoren eller kreditoren i løbet af et Teams-møde eller et opkald, mens mødet afholdes, uden at forlade Teams.

Du kan faktisk søge efter kontaktoplysninger fra ethvert sted i Teams ved hjælp af kommandoboksen. Du kan f.eks. søge efter kontaktoplysninger fra kalenderen i Teams, så du lettere kan arrangere møder.

### Hvordan får jeg vist mine sidste interaktioner med en kontakt?

Detaljevinduet for en kontakt viser interaktionslogposter. Interaktionslogposter giver en oversigt over de interaktioner, som organisationen har haft med den specifikke kontakt. Interaktionerne kan omfatte mails, som du har udvekslet, opkald, du har modtaget, eller dokumenter, du har sendt.

For de interaktioner, der skal vises, skal [!INCLUDE [prod_short.md](includes/prod_short.md)] være konfigureret til at spore interaktioner. Du kan lære mere om logføring af interaktioner i [Registrere interaktioner med kontakter](marketing-interactions.md).

### Hvordan kan jeg registrere et Teams-opkald eller -møde som en interaktion?

Find handlingen **Opret interaktion** i detaljevinduet for en kontakt, og vælg mellem indgående og udgående opkald som interaktionsskabeloner. Du kan også oprette dine egne brugerdefinerede interaktionsskabeloner, som er specielt beregnet til brug sammen med Teams-samtaler.

### Kan jeg ringe til en kontakt fra appen [!INCLUDE [prod_short.md](includes/prod_short.md)] til Teams?

Integrationen af [!INCLUDE [prod_short.md](includes/prod_short.md)] med opkaldsfunktionerne i Teams er begrænsede. Det er ikke muligt at starte et VOIP-opkald direkte fra vinduet for kontaktkort eller kontaktoplysninger. Når du får vist kontaktoplysninger i appen Teams til pc, kan du imidlertid vælge feltet for telefonnummer for at ringe nummeret op, hvis Teams er konfigureret som standardopkaldsapp på din enhed. Hvis du vil ringe til fastnet- eller mobiltelefonnumre ved hjælp af PSTN, det traditionelle telefonsystem, kræver det, at du har appen Microsoft 365 Business Voice. Du kan få mere at vide i [Hvad er Microsoft 365 Business Voice?](/MicrosoftTeams/business-voice/whats-business-voice).

### Hvordan kan jeg få vist de seneste dokumenter for en debitor eller kreditor?

[!INCLUDE [prod_short.md](includes/prod_short.md)] knytter typisk en kontakt til en debitor- eller kreditorpost, som igen er tilknyttet poster for forretningstransaktioner som f.eks. salgstilbud eller købsfakturaer. Hvis du vil have vist de tilknyttede dokumenter for en kontakt, skal du gå til detaljevinduet for kontakten, vælge værdien i feltet **Forretningsrelation** eller bruge handlingerne til at navigere til den tilknyttede debitor eller kreditor. På siden for debitoren eller kreditoren skal du udvide faktaboksruden for at få vist statistik for forskellige dokumenter, som du kan dykke ned i. Din oplevelse kan variere afhængigt af dine tilpasninger og personlige indstillinger.

### Hvordan søger jeg efter kontakter ved hjælp af specialtegn?

Du kan indtaste søgekriterier med stort set alle Unicode-tegn. [!INCLUDE [prod_short.md](includes/prod_short.md)] har imidlertid reserveret følgende tegn til andre formål: **=**, **.**, **\*** og **@**. Hvis du bruger disse tegn i søgeordene, returneres de forventede resultater muligvis ikke. Hvis du ikke kan se de forventede resultater, skal du sætte apostroffer omkring tegnene i søgeordene, f.eks. **Contoso'='2**.

### Hvordan kan jeg søge efter kontakter, der findes i et andet regnskab?

Appen [!INCLUDE [prod_short.md](includes/prod_short.md)] til Teams kan søge efter debitorer, kreditorer og andre kontakter i ét regnskab ad gangen.  
Hvis du vil søge efter kontakter, der findes i et andet [!INCLUDE [prod_short.md](includes/prod_short.md)]-regnskab, skal du åbne [Indstillinger](across-teams-settings.md)og derefter skifte miljøet og regnskabet derfra.

### Er kontakterne i [!INCLUDE [prod_short.md](includes/prod_short.md)] forskellige fra dem i skærmbilledet for kontakter i Teams?

Ja. Kontakter i [!INCLUDE [prod_short.md](includes/prod_short.md)] repræsenterer de forretningskontakter, der er tilgængelige for din organisation. Disse kontakter har en etableret og veldefineret forretningsrelation, eller er kontakter, der repræsenterer potentielle kunder. Disse kontakter er typisk eksterne kontakter. Til sammenligning er kontakterne på kontaktlisten for Teams-opkald dine egne kontakter. Disse kontaktpersoner deles ikke nødvendigvis med andre i din organisation, og de repræsenterer typisk kontakter, der er interne i organisationen.

### Synkroniserer [!INCLUDE [prod_short.md](includes/prod_short.md)] kontakter med Teams?

Nej. Kontaktpersoner i [!INCLUDE [prod_short.md](includes/prod_short.md)] forbliver adskilte fra kontakter, der er gemt i Teams.
Der er i øjeblikket ingen planer om at synkronisere de to lister.

### Hvad er minimumversionen af [!INCLUDE [prod_short.md](includes/prod_short.md)] med henblik på søgning efter kontakter?

Søgning efter kontakter kræver, at du har installeret appen [!INCLUDE [prod_short.md](includes/prod_short.md)] til Teams version 1.0.4 eller nyere, og at du har oprettet forbindelse til [!INCLUDE [prod_short.md](includes/prod_short.md)]-miljøer i version 18 eller nyere.

### Kan jeg søge fra min mobilenhed?

På dette tidspunkt er søgning efter kontakter fra Teams til iOS og Teams til Android ikke tilgængelig.

### Hvilke tilladelser skal jeg bruge til søgning efter kontakter?

Hvis du vil søge efter kontakter, skal du have tilladelse på det relevante objektniveau til tabellen **Kontakter** i det [!INCLUDE [prod_short.md](includes/prod_short.md)]-regnskab, du søger i. Hvis du vil have vist detaljevinduet for en kontakt, skal du som minimum have læsetilladelse til siden **Kontakt** i [!INCLUDE [prod_short.md](includes/prod_short.md)]-regnskabet og alle andre relaterede objekter.

### Kan jeg søge efter kontakter, hvis jeg er en delegeret administrator?

Ja. Du kan også søge efter kontakter og kontaktoplysninger, hvis du har rollen som delegeret administrator i en organisation.

### Er søgning efter kontakter omfattet af API-begrænsninger?

Ja. Søgning efter kontakter fra Teams er baseret på [!INCLUDE [prod_short.md](includes/prod_short.md)] v 2.0-API'er og underlagt eventuelle API-grænser for brugen. Du kan få mere at vide om grænserne for de [Aktuelle API-grænser](/dynamics-nav/api-reference/v2.0/dynamics-current-limits).

### Hvorfor bliver jeg nogle gange bedt mig om at konfigurere appen?

Når du logger på appen [!INCLUDE [prod_short.md](includes/prod_short.md)] til Teams første gang, vil appen forsøge at fastlægge dit foretrukne regnskab i [!INCLUDE [prod_short.md](includes/prod_short.md)]. Hvis appen ikke kan bestemme det foretrukne regnskab, kan det være nødvendigt at gå til **Indstillinger** og vælge det regnskab, du vil søge i. Dette sker f.eks., hvis du har adgang til flere regnskaber på tværs af miljøerne i din organisation. I så fald skal du vælge et regnskab, før du kan begynde at søge.  

Appen beder dig muligvis også om at kontrollere **Indstillinger**, hvis du tilsyneladende ikke har et [!INCLUDE [prod_short.md](includes/prod_short.md)]-abonnement, et [!INCLUDE [prod_short.md](includes/prod_short.md)]-miljø eller en [!INCLUDE [prod_short.md](includes/prod_short.md)]-licens for din konto.

### Jeg vil søge efter varer eller poster fra andre tabeller. Kan jeg gøre det fra Teams?

Det er ikke muligt at søge i andre tabeller på nuværende tidspunkt. Appen [!INCLUDE [prod_short.md](includes/prod_short.md)] til Teams søger kun i kontaktlisten for [!INCLUDE [prod_short.md](includes/prod_short.md)], som kan omfatte kreditorer, debitorer og andre kontakter.

Hvis du ønsker, at søgefunktionerne kan inkludere andre tabeller, opfordrer vi brugere af vores forum tilføje en idé eller tilslutte sig eksisterende ideer på https://aka.ms/BusinessCentralIdeas.

## [Arbejde med kort](#tab/cards)

### Hvilke typer links understøtter appen?

[!INCLUDE [prod_short.md](includes/prod_short.md)]-appen til Teams reagerer på de fleste [!INCLUDE [prod_short.md](includes/prod_short.md)]-webklientlinks. Når hyperlinket henviser til en enkelt post på en side, vises der felter for den pågældende post på kortet. De understøttede sidetyper omfatter: 

- Kortsider, f.eks. varekortet
- Dokumentsider, f.eks. salgsordredokumentet
- ListPlus-sider, der repræsenterer en enkelt post, der består af andre poster, f.eks. en bankkontoafstemningskonto
- Simple listesider, hvor en post ikke giver mulighed for at rulle ned på en separat side med oplysninger, f.eks. listen over postnumre

Når du indsætter et hyperlink til URL-adressen til webklienten for rodwebstedet, f.eks. https://businesscentral.dynamics.com, viser kortet i stedet oplysninger, der kan hjælpe nye brugere med at få adgang til [!INCLUDE [prod_short.md](includes/prod_short.md)].

### Hvordan sletter jeg et kort, jeg har sendt til en chat?

Du kan ikke slette et kort, som du allerede har sendt til chat. Men du kan slette hele den meddelelse, som kortet er en del af.

Som meddelelsesforfatter kan du slette alle de meddelelser, du har sendt til chat med en person, gruppe eller kanal&mdash;medmindre administratoren har angivet politikker, der forhindrer sletning af meddelelser. Hvis du tilpasser en kanal som kanalejer, kan administratoren også have givet dig tilladelse til at slette alle meddelelser i kanalen, herunder de meddelelser, som andre brugere har sendt.

Hvis du sletter en meddelelse, der indeholder et kort, slettes eller påvirkes data ikke [!INCLUDE [prod_short.md](includes/prod_short.md)].

### Viser kort altid opdaterede oplysninger?

Nej. Feltværdierne på et kort i Teams, herunder alle billeder, er baseret på de data, der er tilgængelige, da kortet blev sendt til chatten. [!INCLUDE [prod_short.md](includes/prod_short.md)]-kort opdateres ikke automatisk i Teams. 

### Hvorfor viser kort ikke flere oplysninger i stedet for blot knappen sidenavn og detaljer?

En administrator kan have konfigureret Teams-integrationen, så kortene ikke viser data om poster. Du kan finde flere oplysninger i [Vise eller skjule postdata på kort](admin-teams-integration.md#show-or-hide-record-data-on-cards).

### Vil andre se mit kort, hvis de ikke har [!INCLUDE [prod_short.md](includes/prod_short.md)]-appen til Teams? 

Når du skriver og sender en meddelelse til chatten, som indeholder et kort, vil alle brugere kunne se kortet&mdash;selvom de ikke har installeret appen [!INCLUDE [prod_short.md](includes/prod_short.md)] til Teams.

### Hvordan finder jeg ud af, hvilket firma et kort i Teams tilhører?

Hvis du arbejder på tværs af [!INCLUDE [prod_short.md](includes/prod_short.md)]-firmaer, skal du kontakte administratoren for at få aktiveret et virksomhedskort for hvert regnskab. Når dette tip er aktiveret, vises dette iøjnefaldende i alle oplysnings vinduer i Teams, og det firma og miljø, som posten tilhører, vises. Du kan lære mere om, hvordan du konfigurerer virksomhedskort, i [Vis en virksomheds badge ](admin-company-information.md#badge).

## [Arbejde med kortdetaljer](#tab/carddetails)

### Hvor er knappen til gem i vinduet detaljer i Teams?

[!INCLUDE [prod_short.md](includes/prod_short.md)] gemmer automatisk de ændringer, du foretager i et felt, så snart du forlader feltet. Hvis du vil bevare et felt, skal du klikke eller trykke et vilkårligt sted uden for feltet eller bruge tabulatortasten til at flytte til næste felt. Når der vises data i en dialogboks i detaljevinduet, skal du muligvis klikke på knappen **OK** for at [!INCLUDE [prod_short.md](includes/prod_short.md)] gemme ændringerne.

### Hvis jeg vælger at få vist detaljer om et kort, får andre brugere vist vinduet mine oplysninger?

Nej. Mens alle i chatten eller mødet kan se selve kortet, vises vinduet med oplysninger kun for dig på din enhed, når du vælger **Detaljer**. Andre brugere skal vælge **Detaljer**, hvis de vil have vist detaljevinduet på deres enhed.

### Kan jeg starte et Teams-opkald fra vinduet detaljer i Teams?

Ja. Hvis du bruger appen Teams til pc, skal du starte et opkald ved at vælge det tilknyttede nummer i feltet for telefonnummer, f.eks. **Mobilnr.** felt på kortet **Konktakt**. Teams skal være din angivne opkalds-app.

Hvis du vil ringe til lokale eller internationale fastnetnumre og mobiltelefoner, kræver Teams, at du har en Business Voice-licens til virksomhedsopkald. Du skal også konfigurere Teams som opkaldsløsning. Du kan finde flere oplysninger i [Planlægning af stemmeløsning i Teams](/microsoftteams/cloud-voice-landing-page) i dokumentationen til Teams.

### Kan jeg udskrive dokumenter fra vinduet med detaljer i Teams?

Ja. Du udskriver rapporter og andre dokumenter med standardudskrivningsfunktioner for [!INCLUDE [prod_short.md](includes/prod_short.md)] og enhver skybaseret printer, der er konfigureret på siden **Printerstyring** i [!INCLUDE [prod_short.md](includes/prod_short.md)]. Du kan ikke udskrive fra Teams til lokale printere, der kender din klientenhed, f.eks. printere, som du typisk udskriver fra browseren. Du kan derfor ikke udskrive fra vinduet Vis rapport, men kun fra hovedrapportens anmodningsside, direkte til dine Cloud-printere.

Du kan finde flere oplysninger om oprettelse af Cloud-printere i [Konfiguration af printere](ui-specify-printer-selection-reports.md).

### Kan jeg få adgang til kameraet fra detalje vinduet i Teams?

Ja. Alle [!INCLUDE [prod_short.md](includes/prod_short.md)]-funktioner i vinduet detaljer, som bruger kameraet, er tilgængelige på alle Teams-klienter.

### <a name="location"></a>Kan jeg få adgang til min lokation fra detaljevinduet i Teams?

Hvis du bruger funktioner i [!INCLUDE [prod_short.md](includes/prod_short.md)], der får adgang til dine aktuelle placeringskoordinater, f.eks. med Maps, skal du bruge Teams i browseren eller Teams mobil-app. Placeringen er ikke tilgængelig, når appen Teams desktop bruges.

### Hvordan åbnes detaljerne i et nyt vindue?

Det er nyttigt at bruge vinduet med detaljer som et separat vindue til multitasking eller til at arbejde med forretningsdata, samtidig med at Teams chat og andre Teams funktioner stadig kan bruges. Hvis du vil åbne detaljer i et separat vindue, skal du vælge **Åbne i browser** menuen ellipse (**...**) i øverste højre hjørne af vinduet.

## [Samarbejde med gæster](#tab/collaborating)

### Kan jeg dele kort med brugere uden for organisationen?

Ja. Når du skriver og sender en meddelelse, der indeholder et kort, vil alle modtagere i chatten kunne se kortet&mdash;selvom de er gæster eller eksterne i forhold til organisationen. Gæster kan også åbne vinduet detaljer, hvis de har tilladelse til at få adgang til de pågældende data i [!INCLUDE [prod_short.md](includes/prod_short.md)].

### Er der en anden oplevelse hos brugere, som er gæster?

Ja. Hvis du inviterer gæstebrugere fra uden for organisationen til at deltage i chat eller en kanal, får de tilsvarende, men ikke identiske, sammenlignet med brugere inden for organisationen. Når en gæst modtager en meddelelse, der indeholder et kort, kan de se det. Gæster kan også åbne vinduet detaljer, hvis de har tilladelse til at få adgang til de pågældende data i [!INCLUDE [prod_short.md](includes/prod_short.md)] og har fået tildelt en [!INCLUDE [prod_short.md](includes/prod_short.md)]-licens inden for organisationen.

Hvis du vælger hyperlinket detaljer på et hvilket som helst Business Central-kort, logger du på det miljø, kortet er delt fra, hvis du har tilladelse til miljøet.

Gæstebrugere har ikke tilladelse til at bruge Kontaktsøgning, fordi den er bundet til den oprindelige lejer, og vi understøtter i øjeblikket ikke et sådant uddelegeret scenarie.

Når en gæst skriver en meddelelse, vil links til gæstens eller din [!INCLUDE [prod_short.md](includes/prod_short.md)] ikke blive udvidet til kort.

Hvis du vil have oplysninger om andre lighedspunkter og forskelle mellem gæster og teammedlemmer, skal du se [Gæsteerfaringer i Teams](/MicrosoftTeams/guest-experience) i dokumentationen til Teams.

### Hvordan installeres en gæstebruger [!INCLUDE [prod_short.md](includes/prod_short.md)]? 

Gæster har ikke adgang til app-markedspladsen for at installere apps selv. Appen kan imidlertid installeres automatisk på basis af virksomhedens politikker. En anden måde, en gæstebruger kan installere [!INCLUDE [prod_short.md](includes/prod_short.md)]-appen på er, når de modtager en chatmeddelelse, der indeholder et [!INCLUDE [prod_short.md](includes/prod_short.md)]-kort. I dette tilfælde vælger brugeren knappen **Detaljer** eller menuen på kortet og installerer derefter [!INCLUDE [prod_short.md](includes/prod_short.md)]-appen til brug sammen med organisationen. Når appen er installeret, modtager brugeren ikke automatisk tilladelse til at få adgang til data fra din [!INCLUDE [prod_short.md](includes/prod_short.md)].

## [Del på Teams](#tab/share)

### Kan Del på Teams sende et kompakt kort? 

Ja. Hyperlinket udvides automatisk til et kort, hvis du har installeret Business central app til teams. 

### Vil modtagerne modtage meddelelsen fra mig eller fra en Business Central-tjenestekonto? 

Når du bruger Del på Teams, sendes meddelelsen til en person, gruppe eller kanal, som ligner, om du selv har sendt meddelelsen fra Microsoft Teams. Modtagere får vist meddelelsen fra dig på deres foretrukne Teams-klient og kan reagere og svare, som de plejer, i en e-mail. 

### Er Del på Teams tilgængelig i Business Central lokalt? 

Nej. På samme måde som [!INCLUDE [prod_short.md](includes/prod_short.md)]-appen for Teams kan denne funktion kun vælges til webklienten [!INCLUDE [prod_short.md](includes/prod_short.md)] online. Der er ingen planer om at understøtte [!INCLUDE [prod_short.md](includes/prod_short.md)]-installationstyper&mdash;f.eks. i det lokale miljø, hybrid-sky eller privat sky&mdash;som Microsoft hverken er vært for eller administrerer direkte.

### Kan Del på Teams give tilladelser til modtagerne? 

Nej. Når du deler med en person, en gruppe eller en kanal, påvirkes tilladelserne ikke. Brugere, der allerede har tilladelse til at få vist siden og de data, som er målrettet af hyperlinket, kan gøre det. Brugere, som ikke har tilladelse til at få vist denne side og disse data eller ikke har en [!INCLUDE [prod_short.md](includes/prod_short.md)]-licens, vises som en fejlmeddelelse. 
 
### Skal jeg have Teams Desktop-app installeret for at kunne bruge Del på Teams? 

Nej. Det eneste, du behøver, er en gyldig konto, der har adgang til Microsoft Teams. 

### Er Del på Teams tilgængelig i alle Business Central-klienter? 

På nuværende tidspunkt er dele med Teams tilgængelig på desktop-webklienten, i vinduet med detaljer i Teams og ved åbning af en side i et nyt vindue fra Outlook-tilføjelsesprogrammet.

### Hvor kan jeg finde Del på Teams i Business central? 

Handlingen **Del på Teams** kan findes i menuen **Del** på alle sider, f. eks. kort og dokumentsider, liste-eller regnearks sider, herunder brugerdefinerede sider. Handlingen er ikke tilgængelig i dialogbokse eller sider, der vises som dialogbokse, f. eks. opslagssider eller guider.

---
## Se også

[[!INCLUDE [prod_short](includes/prod_short.md)] og Microsoft Teams Oversigt over integration](across-teams-overview.md)  
[Installere appen [!INCLUDE [prod_short](includes/prod_short.md)] til Microsoft Teams](across-install-app-for-teams.md)  
[Søgning efter debitorer, kreditorer og andre kontakter fra Microsoft Teams](across-search-contacts-teams.md)  
[Dele poster i Microsoft Teams](across-working-with-teams.md)  
[Fejlfinding i Teams](admin-teams-troubleshooting.md)  
[Ændring af virksomhed og andre indstillinger i Teams](across-teams-settings.md)  
[Udvikling af Teams-integration](/dynamics365/business-central/dev-itpro/developer/devenv-develop-for-teams)  

## [!INCLUDE[d365fin](includes/free_trial_md.md)]  


[!INCLUDE[footer-include](includes/footer-banner.md)]
