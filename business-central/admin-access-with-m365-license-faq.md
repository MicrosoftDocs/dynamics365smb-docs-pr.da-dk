---
title: 'Adgang til Microsoft 365-licenser, ofte stillede spørgsmål'
description: 'Få svar på ofte stillede spørgsmål om, hvordan du får adgang til Business Central med Microsoft 365 licenser.'
author: mikebc
ms.author: mikebc
ms.reviewer: jswymer
ms.service: dynamics-365-business-central
ms.topic: faq
ms.date: 09/28/2023
ms.custom: bap-template
---
# Adgang til Microsoft 365-licenser, ofte stillede spørgsmål

[!INCLUDE[azure-ad-to-microsoft-entra-id](~/../shared-content/shared/azure-ad-to-microsoft-entra-id.md)]

[!INCLUDE [2023rw1-sec-group-short](includes/2023rw1-sec-group-short.md)]

Brugere kan få adgang til Business Central-data Microsoft Teams ved hjælp af deres Microsoft 365 licens. Denne artikel besvarer ofte stillede spørgsmål fra administratorer, konsulenter og andre. Udviklere bør henvise til ofte stillede spørgsmål om udviklere. Hvis du har spørgsmål om integrering af Business central med Microsoft Teams, skal du gå til [ofte stillede spørgsmål i Teams](teams-faq.md).

## [Rettigheder](#tab/permissions) 

### Kan jeg konfigurere forskellige starttilladelser for forskellige brugergrupper?

Ikke på nuværende tidspunkt. Business central giver kun mulighed for at konfigurere én gruppetilladelser, der er tildelt til alle Microsoft 365-brugere, når de logger på Business central første gang.

### Kan jeg proaktivt konfigurere tilladelser, profiler og indstillinger for individuelle brugere, før de logger på?

Ja. Det kan gøres via sikkerhedsgrupper. Ved at anvende en sikkerhedsgruppe i et miljø definerer du det samlede sæt brugere, der har adgang til det pågældende miljø. Denne sikkerhedsgruppe kan omfatte brugere med en Business Central-licens og brugere med en Microsoft 365-licens. Når du opdaterer brugere fra Microsoft 365 på listen **Brugere**, oprettes Microsoft 365-brugerposter. Du kan derefter tildele brugergrupper, tilladelser, profiler og andre indstillinger, før de er logget på.

### Når en bruger logger på, kan jeg så ændre, hvilke objekter de har adgang til?

Ja. Når en bruger har logget på første gang, og deres brugerpost er blevet klargjort, administrerer administratorer disse brugere på samme måde som alle andre Business Central-brugere. Du kan f. eks. tilføje eller fjerne tilladelser til forskellige objekter. Hvis du ændrer de tilladelsessæt, der er tildelt Microsoft 365-licensen på siden licens konfiguration, påvirker ændringen kun de næste brugere, der logger på første gang.

### Hvordan forhindrer jeg adgang til følsomme tabeller?

Business Central tilbyder en stærk og fleksibel tilladelses model, hvor administratorer kan definere tilladelsessæt, der giver adgang til bestemte objekter, forretningsprocesser eller hele roller. Hvis du vil forhindre adgang til følsomme tabeller, kan du oprette brugerdefinerede tilladelsessæt, der udelukker tilladelse til følsomme objekter. Du kan finde flere oplysninger om, hvordan du udelader rettigheder i [Oprette et rettighedssæt](ui-define-granular-permissions.md).  

### Kan jeg tilpasse en brugergruppe i stedet for at tilpasse licenskonfigurationen?

Ja. Tilføjelse af tilladelsessæt til Microsoft Teams-brugergruppen interne brugere i Business central har samme effekt som tilføjelse af tilladelsessæt til Microsoft 365-licensen, så længe Microsoft 365-licensen fortsat knyttes til denne brugergruppe. Denne fremgangsmåde har den ekstra fordel, at tilladelsessæt altid synkroniseres med medlemmerne i gruppen, hver gang du redigerer brugergruppen.

### Når en Business Central-bruger deler en post i Teams, får de nye rettigheder?

Nej. Denne handling er ikke det samme som at dele et link med et SharePoint-dokument, hvor den person, der deler dokumentet, kan vælge at give andre tilladelser. I Business central kan kun administratorer konfigurere og tildele tilladelser. Sammenlignet med at dele SharePoint-dokumenter, svarer det til at vælge indstillingen "dele til personer med eksisterende adgang".

### Understøtter denne funktion sikkerhed på rækkeniveau?

Ja. Selvom en person, der åbner en post i grupper med sin Microsoft 365-licens, har de korrekte tilladelser til tabel og sideobjekt, gennemtvinges rækkeniveau-tilladelser, hvis den er implementeret for den pågældende tabel.  

### Hvis jeg konfigurerer tilladelser, der omfatter skriveadgang, kan brugere skrive i Teams?

Hvis du konfigurerer Business central til at tildele et tilladelsessæt, der omfatter indsættelse, ændring eller sletning af adgang til et eller flere objekter, vil brugere med det pågældende tilladelsessæt stadig ikke kunne skrive i teams, når de kun har en Microsoft 365-licens. Business Central-tjeneste håndhæver skrivebeskyttet adgang, uanset hvilken tilladelse du har tildelt.  

Selvom Business central giver dette niveau af beskyttelse, anbefaler vi stadig, at du undgår tilladelses sæt med skriveadgang. Hvis du gør det, er der andre problemer, når brugerne skifter rolle eller henter nye licenser.  

## [Installation og Konfiguration](#tab/setup)

### Hvorfor er indstillingen gør adgangen ikke tilgængelig for mit miljø?

Aktivering af adgang med Microsoft 365-licenser er kun tilgængelig for Business Central-miljøer med platformversion 21.1 eller nyere. Når dit miljø er opgraderet til denne minimum version, bliver indstillingen automatisk tilgængelig. Hvis du vil kontrollere versionen af dit miljø, skal du gå til siden med miljø detaljer for miljøet i Business Central administration. Du kan desuden logge på miljøet og gå til siden **hjælp & support** fra menuen **Hjælp** .

### Kan jeg få adgang til Business Central lokalt med Microsoft 365-licenser?

Nej, det understøttes ikke. Business central viser en fejl, når brugere forsøger at få adgang til Business Central-lokale poster i Teams.

### Hvad er medarbejderprofilen?

Den **medarbejder**-profil, der vises på listesiden **profiler (roller)**, blev introduceret med opdatering 21.1. Det er den standardprofil, der er tildelt brugere, som åbner Business central med Microsoft 365-licensen. Denne profil er beregnet til personer i en virksomhed, som ikke har en bestemt rolle i Business central, og som kun har behov for at få vist data, der er delt med dem.

### Hvad er brugergruppen Teams brugere?

Gruppen med **Microsoft Teams-interne brugere**, der vises på siden **brugergrupper**, blev introduceret med opdatering 21.1. Denne gruppe er den standardbrugergruppe, der er tildelt brugere, som åbner Business central med Microsoft 365-licensen. Brugergruppen henvender sig til personer inden for samme organisation, hvor Business Central er vært for, og som samarbejder om Microsoft Teams.  

### Skal brugere, der kun har en Microsoft 365-licens, vises på listen brugere i Business central?

Ja. Hvis du anvender sikkerhedsgrupper på miljøer, vises disse brugere på listen brugere, efter at du har brugt funktionen Opdater brugere fra Microsoft 365-handling fra listen **Brugere**. Hvis du ikke anvender sikkerhedsgrupper, vises bruger poster på listen brugere, efter at de har åbnet en Business central-post.

### Fungerer denne funktion til Integrer ISV-løsninger?

Ja. Brugere med en Microsoft 365-licens kan også få adgang til poster i miljøer, der kører under *.bc.dynamics.com-domænet.

## [Licenser](#tab/license)

### Kan en kunde bruge denne funktion, hvis de ikke har Business Central?

Adgang til Business central med en Microsoft 365-licens er beregnet til virksomheder, der allerede abonnerer på Business Central, og som driver et eller flere Business Central-miljøer med brugere, der har Business Central-licens. Den har ingen ny funktionalitet eller brugerrettigheder til Microsoft 365-kunder, som ikke har en Business Central-plan.

### Hvordan kan denne hjælp administrere abonnements omkostningerne i min virksomhed?

Med henblik på at maksimere produktiviteten og strømline deres transaktioner, køber SMB'er ofte Dynamics 365 Business Central sammen med Microsoft 365. I dette tilfælde modtager de fleste personer en Microsoft 365-licens, men kun bestemte roller eller personer modtager en Business Central-licens. Business central giver licens fleksibilitet, så kunderne kun betaler for, hvad de har behov for:

- Brugere, der har behov for fuld adgang til Business central, får typisk tildelt en Business Central Essentials- eller Business Central Premium-licens. 
- Brugere, der kræver begrænset skriveadgang, tildeles typisk en Business Central-licens til Team-medlemmer.
- Alle andre medarbejdere i organisationen, der kun har behov for at læse forretningsdata, der deles med dem, kan gøre dette, hvis de har en Microsoft 365-licens. De behøver ikke at være tildelt en licens til Team-medlem. Der findes flere licensmuligheder. Du kan finde flere oplysninger ved at hente og læse [Dynamics 365-licensvejledning](https://go.microsoft.com/fwlink/?LinkId=866544).

### Er dette 100 % gratis?
 
Nej. Adgang til Business Central-data i Microsoft Teams kræver, at hver bruger har en Business Central-licens eller en Microsoft 365-licens fra listen over understøttede ordninger.

### Fungerer dette sammen med Microsoft 365- forsøg og Business Central-test?

Ja. Hvis en bruger får tildelt en Microsoft 365-licens fra en prøveversion af en understøttet plan, kan vedkommende også få adgang til Business Central-poster i Teams. Så kan kunderne prøve Microsoft-produktivitets-og virksomheds-apps, der arbejder sammen, og giver partner sælgere og konsulenter mulighed for nemt at demonstrere denne funktion. Partnere kan f. eks. forsyne deres egne Microsoft Entra-lejere fra [https://aka.ms/CDX](https://aka.ms/CDX), der omfatter Microsoft 365-forsøg og Business Central-test til påvisning af Business Central.

### Listen over licenser i Business Central viser en Microsoft 365-licens. Hvad er det?

Siden **Licenskonfiguration** i Business central viser de forskellige typer licenser, der kan give adgang til Business Central-service. I version 21 har Microsoft føjet Microsoft 365 til denne liste som en ny måde at få adgang til Business central på. Denne liste over licenser betyder ikke, at din organisation har købt abonnementer på nogen af disse licenser, eller at din organisation har aktiveret adgang via disse licenser.

### Skal jeg have en ny licenstype Microsoft 365, for at denne funktion kan fungere?  

Microsoft har ikke oprettet nye licenser eller nye planer for at kunne tænde denne funktion. Denne funktion er udelukkende afhængig af eksisterende Microsoft 365-planer og licenser. Hvis du allerede abonnerer på en af de understøttede Microsoft 365-planer, har du allerede denne nye brug af. Hvis du ikke abonnerer på Microsoft 365 i dag, kan du tilmelde Microsoft 365 dig Business Central eller lignende planer her. 

### Hvordan finder jeg ud af, hvilke brugere der kun har en Microsoft 365-licens?

Der er flere måder. I Microsoft 365 Administration skal du gå til listen **Aktive brugere**, og se kolonnen **Licenser** . Gå til listen **Brugere** i Business central, vælg en af brugerne, og se faktaboksen **Licenser** .  

### Hvordan kan jeg filtrere listen Brugere i Business Central for at se de brugere, der kun har en Microsoft 365-licens?

Denne opgave er ikke mulig ved hjælp af et filter eller en listevisning. Du kan dog vælge en bruger på listen og få vist den faktaboks med licenser, der kun skal indeholde Microsoft 365, hvis brugeren kun har en Microsoft 365-licens.

### Hvad med brugere, der har både en Microsoft 365-licens og en Business Central-licens?

Når flere licenser tildeles til en bruger, skal større licens brugsrettigheder vinde over mindre licensbrugsrettigheder, når du får adgang til Business central. I dette tilfælde berettiger Business Central-licens brugeren til flere brugerrettigheder. På den måde kan brugere læse og skrive Business Central-poster i Teams og få adgang til Business Central-webklient i browseren, som f. eks. enhver anden Business Central-licensindehaver. Hvis der er konfigureret specifikke tilladelsessæt for Microsoft 365-licensen, får brugeren vist de konfigurerede tilladelsessæt, der er kombineret med tilladelsessæt fra den Business Central-licens, eller som allerede er tildelt brugeren.

### Er denne licensering relateret til Business Central-licens til Team-medlem?

Der er ingen relation mellem Business central teams-medlem af licenser og adgang til Business central i Microsoft Teams forbindelse med Microsoft 365-licenser. Selvom Microsoft Teams og dennes dokumentation henviser til personer i et team som *teammedlemmer*, er det en fællesbetegnelse for en gruppe af Microsoft Teams- brugere. Det henviser ikke til Business Central-licenser.

### Gennemtvinger Business central alle betingelserne?

Ja, den centrale platform for alle platforms begrænsninger og minimumkrav, herunder licenskrav, gennemtvinges af Business Central. På denne måde får brugere med bestemte fejlmeddelelser mulighed for at udføre fejlfinding af deres opsætning og undgå misbrug. Hvis en bruger, der kun har en Microsoft 365-licens, forsøger at få adgang til Business Central-webklient i browseren, nægtes adgang, og der vises en fejlmeddelelse om, at der oprettes en fejl. 

## [Forbrug](#tab/usage)
 
### Kan jeg få adgang til poster på Teams til iOS og Teams for Android? 

I øjeblikket er det ikke muligt at få adgang til Business Central-data i Teams mobil med kun en Microsoft 365-licens. Microsoft arbejder på at aktivere denne funktion. 

### Hvordan ændrer brugerne deres personlige indstillinger i Mine indstillinger? 

Når en bruger kun får adgang til Business central for første gang, hvor der kun anvendes Microsoft 365-licens, angives brugerindstillinger som f. eks. sprog, tidszone og internationale indstillinger automatisk på basis af deres operativsystem eller indstillinger i browseren. Administratorer kan ændre disse indstillinger fra Business central for hver bruger. 

### Hvad bestemmer valget af sprog, første gang du logger på? 

Det sprog, som du oplever i Business central, er baseret på forskellige faktorer, herunder Teams-klienten, som du har åbnet Business central fra første gang. For Teams PC-app, Teams til iOS og Teams til Android anvendes operativsystemsproget. For Teams til World Wide Web anvendes browsersproget. I alle tilfælde tages Teams-sproget ikke i betragtning. 

### Hvorfor kan jeg ikke aktivere nogle af de farvede links i faner og kort detaljer?

De Handlingslinks, der er nødvendige for Business central-sider, vises ofte som et link med fed skrift, som kan aktiveres til at gå et andet sted eller udføre en handling. På et teknisk niveau er disse links typisk implementeret som feltværdier uden tekst, der udløser en kode, og hvor valget af typografi ofte afspejler tilstanden. Når brugerne får adgang til Business Central-sider med deres Microsoft 365-licens, bruges de som en typografi. Men de kan ikke aktiveres, fordi licensen ikke giver mulighed for at udføre handlinger med brug af rettigheder.  

### Hvorfor kan jeg ikke aktivere handlinger til side beskeder?

Kontekstmeddelelser, der vises på sider, ledsages ofte af Handlingslinks. Når brugere åbner Business Central-sider med deres Microsoft 365-licens, vises disse links, men de kan ikke aktiveres, fordi licensen ikke giver dig tilladelse til at udføre handlinger. På et teknisk niveau implementeres disse links som handlinger.

### Kan Microsoft 365-brugere fjerne faner?

Ja. Alle i chat eller kanal kan fjerne faner, som er oprettet af andre. Fjernelse af en fane vil ikke fjerne eller påvirke data i Business central, men fanen fjernes for alle brugere i chatten eller-kanalen.

### Hvis jeg ikke kan filtrere, vil jeg stadig se en filtreret liste, som andre har oprettet?

Brugere, der får adgang til Business central med deres Microsoft 365-licens, har ikke rettighederne brug til at filtrere ved hjælp af filterruden eller Anvend listevisninger. Men hvis en anden bruger har oprettet en fane med en filtreret listeside, får Microsoft 365-brugere også vist de filtre, der er anvendt på fanen.

---

## Se også

[Oversigt over Business Central-adgang med Microsoft 365-licenser](admin-access-with-m365-license.md#minimum-requirements)  
[Konfigurere adgang til Microsoft 365-licenser](admin-access-with-m365-license-setup.md)  