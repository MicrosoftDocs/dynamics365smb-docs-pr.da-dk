---
title: Overholdelse af bogføringsloven i Danmark
description: Lær hvordan Business Central overholder bogføringsloven i Danmark.
author: altotovi
ms.topic: conceptual
ms.devlang: al
ms.search.keywords: 'bookkeeping, law, compliance, e-vat, e-document, nemhandel, denmark, dk'
ms.search.form: null
ms.date: 01/18/2024
ms.author: altotovi
ms.service: dynamics-365-business-central
ms.reviewer: bholtorf
---
# <a name="compliance-with-the-bookkeeping-act-in-denmark"></a>Overholdelse af bogføringsloven i Danmark
[!INCLUDE[prod_short](../../includes/prod_short.md)] (sky) er registreret som digitalt bogføringssystem i Danmark.  

> [!IMPORTANT]
> Dynamics 365 Business Central er kun registreret som digitalt bogføringssystem som standardløsning uden tilpasninger (som det er). Hvis systemet er tilpasset, er det på partner eller kunde at bevise, at dette system stadig er en standardløsning, da Microsoft ikke kan give mening, hvis tilpasninger bryder dele af et digitalt bogføringssystem DBA certificeret.  

Registreringsattest er baseret på jfr. §4 stk.1 i bekendtgørelse nr. 98 af 26. januar 2023, om anmeldelse og registrering af digitale standardbogføringssystemer, hvorefter det digitale standardbogføringssystem [!INCLUDE[prod_short](../../includes/prod_short.md)] er registreret af Erhvervsstyrelsen den 21. december 2023 med den **registreringsnummer fob467715**.  

> [!NOTE]
> Følgende dokument giver ikke officiel dokumentation i processen med certificering hos DBA. Dette er blot en forklaring på, at Dynamics 365 Business central overholder alle krav og i sidste ende instruktioner til partnere eller kunder, hvis de ønsker at certificere deres løsning uden for Microsoft.  

## <a name="how-does-business-central-comply"></a>Hvordan opfyldes Business central?

For at opnå dette registreringsbevis [!INCLUDE[prod_short](../../includes/prod_short.md)] skulle overholde forskellige krav fra Danske Erhvervsmyndigheder baseret på bekendtgørelse nr. 97.  

## <a name="main-requirements----15-no-1"></a>Hovedkrav - § 15, nr. 1

Understøtte en løbende registrering af virksomhedens transaktioner med angivelse af bilag for hver registrering og sikker opbevaring af registreringer og bilag i fem år.  

### <a name="annex-1-1-a--e"></a>Bilag 1, 1, a – e

Krav: Det almindelige digitale bogføringssystem skal indeholde felter for, at virksomheden kan give oplysninger om følgende forhold ved registrering af hver enkelt transaktion:  

* Transaktionsdato (f.eks. betalingsdato, købsdato osv.)  
* Beløb    
* Kvitteringsnummer  
* Transaktionstekst  
* Valutakurs på transaktionsdagen eller anden omregningsfaktor, hvis registrering sker i anden valuta end DKK. 

Hvordan [!INCLUDE[prod_short](../../includes/prod_short.md)] overholder:  

Alle transaktioner, der er indtastet i [!INCLUDE[prod_short](../../includes/prod_short.md)] indeholder en transaktionsdato, beløb, kvitteringsnummer / dokumentnummer og transaktionstekst / beskrivelse. Alle posteringer i hovedbogsforretninger opbevares udelukkende i DKK. Hvis det originale dokument har anden valuta end DKK, findes disse oplysninger i hovedbog i forbindelse med hovedbogføring. Alle disse oplysninger kan findes på **G/L Register** siden. **G/L Register** siden indeholder detaljer om hver transaktion, herunder registernummeret, oprettelsesdatoen og -tidspunktet, bruger-id'et for, hvem der har oprettet transaktionen, og dens kildekode.  

### <a name="annex-1-2-a--e"></a>Bilag 1, 2, a – e

Krav: Det digitale standard bogføringssystem skal sikre:  

* At systemet tildeler en registreringsdato for hver registreret transaktion.  
* At systemet tildeler et fortløbende transaktionsnummer eller ID for hver registreret transaktion.
* At systemet tildeler initialer eller lignende til den person, der har registreret en transaktion.
* At systemet gemmer ændringer i optagelsen, fx ved at forkerte indtastninger skal rettes med nye indtastninger.
* At registrerede transaktioner ikke kan ændres, tilbagedateres eller slettes. 

Hvordan [!INCLUDE[prod_short](../../includes/prod_short.md)] overholder:   

Der oprettes et revisionsspor for hver transaktion (**G/L Register**) ved bogføring, der registrerer **Oprettelsesdatoen** og endda **Creation Time** sammen med **Bruger ID** som en person, der registrerede en transaktion. For hvert revisionsspor - register kan du også se nr. Kolonne, som angiver det systemoprettede nummer på hovedbogsregisteret.  

**Finansregister** og **Hovedbogsposter** og alle underreskontro har unikke systembaserede postnumre, som gør det muligt at definere hver nummersekvens som fortløbende.  

Når først en transaktion er bogført, kan transaktionen ikke redigeres eller slettes efter bogføring. Rettelser til transaktionen skal foretages gennem en tilbageførselsindtastning og derefter en ny indtastning for at registrere ændringerne. Korrektion kan udføres manuelt eller ved at bruge **Omvendt** handling fra **G/L-registret** for at tilbageføre transaktionen fuldstændigt. Men under alle omstændigheder oprettes tilbageførsel af transaktion som en ny transaktion uden at ændre oprindelige værdier. Få mere at vide om brug af [finanskonto og kontoplan](../../finance-general-ledger.md).  

### <a name="annex-1-3-a--b"></a>Bilag 1, 3, a – b

Krav: Det digitale standardbogføringssystem skal understøtte opbevaring af kvitteringer omfattet af § 3, som dokumenterer virksomhedens registrerede købs- og salgstransaktioner:  

* Kvitteringer vedrørende købstransaktioner kan gemmes digitalt i systemet.
* Kvitteringer vedrørende salgstransaktioner genereres enten automatisk i systemet og lagres digitalt eller kan lagres digitalt i systemet, for eksempel som et billede eller en scannet fil.

Hvordan [!INCLUDE[prod_short](../../includes/prod_short.md)] overholder:

[!INCLUDE[prod_short](../../includes/prod_short.md)] understøtter lagring af filer som vedhæftede filer til købs- og salgsfakturaer og enhver anden registrering af en tabel, der er tilgængelig for brugere af [!INCLUDE[prod_short](../../includes/prod_short.md)] via brugergrænsefladen. Men for at understøtte obligatoriske vedhæftede filer til købs- og salgstransaktioner, [!INCLUDE[prod_short](../../includes/prod_short.md)] har en mere standardopsætning for digitale bilag, hvor det kræver obligatorisk vedhæftning til salgs- og købstransaktioner og ikke tillader bogføring af disse dokumenter uden vedhæftede filer. For mere automatisering vil salgstransaktioner automatisk oprette salgsdokumenter og vedhæfte dem til denne transaktion uden brugerinteraktion. Men brugeren kan tilføje flere dokumenter, hvis de vil. Læs mere om [obligatoriske digitale værdibeviser her](how-to-digital-vouchers-dk.md).  

### <a name="annex-1-4-and-1-4-a-d"></a>Bilag 1, 4 og 1, 4, a-d

Krav: Det digitale standardbogføringssystem skal understøtte opbevaring af virksomhedens registrerede transaktioner og kvitteringer, der er omfattet af § 3, i 5 år fra regnskabsårets udløb, som materialet vedrører. Det digitale standard bogføringssystem skal understøtte:

* At registrerede transaktioner bevares, så de ikke kan ændres, tilbagedateres eller slettes af virksomheden.
* At alle registrerede transaktioner opbevares i et struktureret og maskinlæsbart format i fem år fra udgangen af ​​det regnskabsår, den registrerede transaktion vedrører, uanset eventuelle ophør af kundeforhold til selskabet eller selskabets konkurs eller tvangsopløsning.
* At alle kvitteringer omfattet af § 3 opbevares i fem år fra udgangen af ​​det regnskabsår, som kvitteringen vedrører, uanset eventuelle ophør af kundeforhold til virksomheden eller virksomhedens konkurs eller tvangsopløsning.

At krypterede bogføringsdata kan dekrypteres til et struktureret og maskinlæsbart format, og at krypterede kvitteringer omfattet af § 3 kan dekrypteres til et læsbart format.

Hvordan [!INCLUDE[prod_short](../../includes/prod_short.md)] overholder:

[!INCLUDE[prod_short](../../includes/prod_short.md)] understøtter opbevaring af virksomhedens registrerede transaktioner og digitale bilag. Transaktionsposter, når de først er oprettet, kan ikke slettes eller ændres via brugergrænsefladen til [!INCLUDE[prod_short](../../includes/prod_short.md)], og **Selskab** kan heller ikke slettes fra det øjeblik, hvor virksomheden er udråbt som produktionsselskab og registreret hos Nemhandel. [!INCLUDE[prod_short](../../includes/prod_short.md)] forhindrer også tilbagedatering af den registrerede transaktion, hvilket betyder, at den bogførte transaktionsdato ikke kan redigeres og ændres. Standard funktionalitet af [!INCLUDE[prod_short](../../includes/prod_short.md)] giver brugerne mulighed for at bogføre transaktioner dateret i den seneste periode (dato, uge, måned siden), men i denne situation er der information om **Oprettet dato** og **Oprettet tid** af en post.  

[!INCLUDE[prod_short](../../includes/prod_short.md)] understøtter også lagring af filer som vedhæftede filer (kvitteringer eller digitale bilag) til købs- og salgsfakturaer og enhver anden registrering af en tabel, der er tilgængelig for brugere af [!INCLUDE[prod_short](../../includes/prod_short.md)] via brugergrænsefladen. Alle vedhæftede dokumenter er gemt i databasen, så database backup vil også beholde vedhæftede filer. Disse slags vedhæftede filer ([obligatoriske digitale værdibeviser her](how-to-digital-vouchers-dk.md)) kan ikke slettes én gang, når bilaget bogføres, og der oprettes hovedbogsposter.  

I løbet af systemets brug kan myndighederne få adgang til alle transaktioner og digitale bilag direkte via brugergrænsefladen fra brugerne, da databasen altid er aktiv og tilgængelig. Men selv i tilfælde af, at brugeren ikke ønsker at give adgang til transaktionsregistrene, eller endda i tilfælde af opsigelse af kundeforhold med Microsoft eller virksomhedens konkurs eller tvangsopløsning, kan Microsoft give transaktionsmæssige og digitale værdikuponer detaljer.   

Alle disse transaktionsdata og de originale dokumenter, der findes i regnskabssystemet, bruges som en kilde til daglig dataeksport i det kontobeskyttede Azure-lagermiljø, hvor de ikke kan ændres, tilbagedateres eller slettes af virksomheden, da denne proces er på platformsniveau uden brugeradgang. Lagerkontolegitimationsoplysninger opbevares i Azure Key Vault, og dataene i lageret vil være beskyttet mod potentiel manipulation. Læs mere om, hvordan Microsoft opbevarer [data påkrævet af danske myndigheder i fem år her](how-to-keep-data-5years.md).   

## <a name="main-requirements----15-no-2"></a>Hovedkrav - § 15, nr. 2

Mød anerkendte standarder for it-sikkerhed, herunder for bruger- og adgangsstyring, og sørg for automatisk backup af registreringer og bilag.  

### <a name="-8-par-4-no-1---7"></a>§ 8, par. 4, nr. 1 - 7

Krav: Netværkssikkerhed, Adgangsstyring, Leverandørstyring, Backup, Logning, Beredskab og genetablering samt Databeskyttelse.  

Hvordan [!INCLUDE[prod_short](../../includes/prod_short.md)] overholder: Microsoft har leveret følgende dokumenter: _**Certifikat for registrering for Information Security Management System - ISO/IEC 27001:2022**_ og _**Microsoft-produkter og -tjenester Databeskyttelsestillæg**_. Disse dokumenter bekræfter, at systemet har et højt it-sikkerhedsniveau, og at sikkerhedsniveauet er baseret på en risikovurdering.   

## <a name="main-requirements----15-no-3"></a>Hovedkrav - § 15, nr. 3

Understøtte automatisering af administrative processer, herunder automatisk afsendelse og modtagelse af e-fakturaer og mulighed for indtastning i henhold til en offentlig standardkontoplan i registrerede regnskabssystemer. 

### <a name="annex-2-1-a--e-and-2-2-a--f"></a>Bilag 2, 1, a – e og 2, 2, a – f

Krav: Det digitale standard bogføringssystem understøtter automatisk afsendelse og modtagelse af e-fakturaer via Nemhandel i OIOUBL-format på følgende måde:

* Kunden kan sende elektroniske fakturaer i OIOUBL-format.
* Kunden kan modtage elektroniske fakturaer i OIOUBL-format.
* Kunden kan sende elektroniske kreditnotaer i OIOUBL-format.
* Kunden kan modtage elektroniske kreditnotaer i OIOUBL-format.
* Kunden kan sende et ansøgningssvar ved modtagelse af en elektronisk faktura.

Det digitale standard bogføringssystem understøtter automatisk afsendelse og modtagelse af e-fakturaer via Nemhandel i Peppol BIS-format på følgende måde:

* Kunden kan sende elektroniske fakturaer i Peppol BIS-format.
* Kunden kan modtage elektroniske fakturaer i Peppol BIS-format.
* Kunden kan sende elektroniske kreditnotaer i Peppol BIS-format.
* Kunden kan modtage elektroniske kreditnotaer i Peppol BIS-format.
* Kunden kan sende et svar på meddelelsesniveau ved modtagelse af en elektronisk faktura.
* Kunden kan sende et fakturasvar ved modtagelse af en elektronisk faktura.

Hvordan [!INCLUDE[prod_short](../../includes/prod_short.md)] overholder:

[Elektronisk faktureringsfunktion](../../finance-edocuments-overview.md) i [!INCLUDE[prod_short](../../includes/prod_short.md)] giver mulighed for at generere elektroniske analoger af forretningsdokumenter (kundefakturaer eller kundekreditnota) i krævede formater (OUOUBL og Peppol BIS) og udføre efterbehandling af genererede elektroniske dokumenter, for eksempel, sende det til forskellige destinationer, samt at importere leverandør elektroniske dokumenter (leverandørfakturaer eller kreditnota) til systemet fra forskellige eksterne kilder. Da brugere skal sende elektroniske dokumenter direkte, kan de gøre det via Access Point-tjenesteudbydere, hvor [!INCLUDE[prod_short](../../includes/prod_short.md)] fungerer som transportlag for afsendelse af oprettede PEPPOL- og OIOUBL-standard-kompatible XML e-fakturaer samt modtagelse, parsing, og import af XML modtaget i førnævnte formater som krævet af loven. I dette scenarie fungerer [!INCLUDE[prod_short](../../includes/prod_short.md)] e-dokumentudvekslingsfunktionaliteten efter 4-hjørnemodellen.  

Beskeder er baseret på en kombination af synkron og asynkron API-kommunikation med en Access Point Service Provider. Alle typer informationer vedrørende evnen til at behandle indgående fakturaer og forretningsbrugeres meddelelser om godkendelse eller afvisning af dokumenter, arbejder baseret på foruddefineret korrekt meddelelsesbehandling. Du kan læse mere om [Dansk Elektronisk fakturering med NemHandel](how-to-edocuments-nemhadel.md) her.  

### <a name="annex-2-3-a"></a>Bilag 2, 3, a

Krav: Det digitale standardbogføringssystem understøtter muligheden for at afstemme virksomhedens bogføring med virksomhedens bankkonto ved at importere en CSV-fil med bankposteringer i bogføringssystemet. 

Hvordan [!INCLUDE[prod_short](../../includes/prod_short.md)] overholder:

[!INCLUDE[prod_short](../../includes/prod_short.md)] leverer en omfattende løsning, der imødekommer kravene fra det digitale standardbogføringssystem og understøtter muligheden for at afstemme virksomhedens bogføring med virksomhedens bankkonto. Den understøtter avanceret bankafstemning, så du kan importere elektroniske kontoudtog i forskellige formater, herunder CSV, og automatisk afstemme dem med banktransaktioner i systemet. Du kan læse flere detaljer om [Udvidelsen Betalinger og afstemninger (DK)](../../ui-extensions-payments-reconciliation-formats-dk.md) og [FIK-detaljer i betalingsafstemningsjournalen](fik-details-in-the-payment-reconciliation-journal.md) i Danmark.   

### <a name="annex-2-3-2-a-b"></a>Bilag 2, 3, 2. a– b

Krav: Bogføringssystemet understøtter, udover tidligere krav, muligheden for at afstemme virksomhedens bogføring med virksomhedens bankkonto ved:

* Bogføringssystemet sikrer, at bankkontoen er repræsenteret i kontoplanen, og at den kan afstemmes med de indlæste bankposter. 
* Der vises en klar forskel i bogføringssystemet, hvis poster indtastet fra banken ikke er afstemt.  

Hvordan [!INCLUDE[prod_short](../../includes/prod_short.md)] overholder:

Brugere kan bruge bankkonti i [!INCLUDE[prod_short](../../includes/prod_short.md)] til at holde styr på deres banktransaktioner. Konti kan være i den lokale valuta (DKK) eller i fremmed valuta. Hver bankkonto er knyttet til en konto i kontoplanen via den tildelte Bankbogføringsgruppe. Hvis du bruger en bankkonto i en betalingstransaktion, oprettes der automatisk en post på både bankkontoen og den tilknyttede finanskonto.  

Bankafstemning er den måde, brugere sørger for, at bankkontoen [!INCLUDE[prod_short](../../includes/prod_short.md)] stemmer overens med bankens eksterne konto. Bankkontoafstemning sammenligner og matcher poster på de bankkonti, brugere har oprettet i [!INCLUDE[prod_short](../../includes/prod_short.md)], med banktransaktioner i deres bank. Derefter kan du bogføre saldiene på deres bankkonti i [!INCLUDE[prod_short](../../includes/prod_short.md)] for at gøre dem tilgængelige for økonomicheferne. Bankafstemning er også en praktisk måde at opdage og løse manglende betalinger og bogføringsfejl på. 

Hvis brugere opdager en fejl i en bogført bankafstemning, kan de bruge handlingen **Fortryd** på siden **Bankkontoudtogsliste** til at rette den. Når de fortryder en bogført bankafstemning, flyttes posterne til siden **Bankafstemning** og markeres som **Åbne**, hvilket betyder, at de ikke er afstemt. De kan derefter rette bankafstemningen og bogføre den igen.   

Der vises en klar forskel i bogføringssystemet, hvis poster indtastet fra banken ikke er afstemt.   

Læs mere om afstemningsprocessen i [!INCLUDE[prod_short](../../includes/prod_short.md)]:

* [Afstemme betalinger ved hjælp af automatisk udligning](../../receivables-how-reconcile-payments-auto-application.md)   
* [Afstemme betalinger, der ikke kan udlignes automatisk](../../receivables-how-reconcile-payments-cannot-apply-auto.md)  
* [Afstemme debitorbetalinger på en liste over ubetalte salgsdokumenter](../../receivables-how-reconcile-customer-payments-list-unpaid-sales-documents.md) 

### <a name="annex-2-4-a--c"></a>Bilag 2, 4, a – c

Krav: Det digitale standard bogføringssystem understøtter muligheden for at bruge en offentlig standard kontoplan:

* Virksomheden anvender den offentlige standardkontoplan direkte i bogføringssystemet.
* Kortlægning af bogføringssystemets standardkontoplan til den offentlige standardkontoplan.
* Bogføringssystemet giver et værktøj, der gør kunden i stand til på en enkel måde at kortlægge sin egen kontoplan til den fælles offentlige standardkontoplan.

Hvordan [!INCLUDE[prod_short](../../includes/prod_short.md)] overholder:

I [!INCLUDE[prod_short](../../includes/prod_short.md)] kan en virksomhed kun bruge én **Oversigt over konti** til opslag i **Hovedbogsposteringer**. Brugere kan konfigurere **Oversigt over konti** til at være det samme som dansk offentlig standard kontoplan manuelt eller under initialiseringen af ​​SAF-T app'en.  

Men hvis brugere allerede har oprettet en hovedkontoplan, der er forskellig fra den offentlige standardkontoplan, eller de ønsker at bruge en, der er anderledes end andre årsager, kan de altid have kortlagt kontoplan med den offentlige standardkontoplan. dansk [offentlig standard kontoplan initialiseres som standard i systemet på siden **Standardkonti**](how-to-set-up-standard-coa.md). 

### <a name="annex-2-4-2-a"></a>Bilag 2, 4, 2. a

Krav: Bogføringssystemet giver et værktøj, der gør kunden i stand til på en enkel måde at kortlægge til standardmomskoder. 

Hvordan [!INCLUDE[prod_short](../../includes/prod_short.md)] overholder:

[!INCLUDE[prod_short](../../includes/prod_short.md)] giver brugergrænseflade til at kortlægge momskoder brugt i skattetransaktioner til offentlige standardmomskoder (offentlig standardmomskontoplan) på en enkel måde til indberetning af Standard Audit File for Tax (SAF-T). For at bruge denne funktion på siden **Opsætning af momsbogføring SAF-T** tilknytter du en opsætning af momsbogføringsgruppe med **Indberetningskode for salgsmoms** og **Købsmomsindberetningskode**.  

### <a name="annex-2-5-a--c"></a>Bilag 2, 5, a – c

Krav: Det digitale standard bogføringssystem understøtter korrekt bogføring gennem bogføringsvejledningen eller regnskabsvejledningen: 

* En bogføringsguide/assistent er blevet indarbejdet i bogføringssystemet for at hjælpe virksomheden med at registrere.  
* Bogføringssystemet indeholder regnskabsinstrukser og/eller link/henvisning til regnskabsinstrukser/vejledninger fra tredjemand. 
* Bogføringssystemet skal understøtte funktionen, at brugerne kan indtaste en regnskabsvejledning for den enkelte konto. 

Hvordan [!INCLUDE[prod_short](../../includes/prod_short.md)] overholder:

[!INCLUDE[prod_short](../../includes/prod_short.md)] har udgivet bogføringsvejledning på sit officielle Learning-websted med en oversigt over bogføringsprocesser, herunder regler, procedurer og andre retningslinjer i [!INCLUDE[prod_short](../../includes/prod_short.md)]: [Regnskab og bogføring](../../learn-accounting-bookkeeping-guide.md).  

Men vigtigere er det [!INCLUDE[prod_short](../../includes/prod_short.md)] har en kontekstbaseret assistent indbygget i produktet. Denne assistent indeholder links til oplysninger, der er relateret til den aktuelle side og instruktioner til at arbejde med den relevante proces.  

Et nøgleelement i at uddanne brugere om [!INCLUDE[prod_short](../../includes/prod_short.md)] sider og koncepter er rundvisningen. En rundvisning er en sekvens af undervisningstips. Undervisningstip kan defineres på sideniveau, sideundervisningstip, og efterfølges af undervisningstip på kontrolniveau, kontrolundervisningstip. 

Det er også muligt at forbinde systemet med fællesskabets support og instruktioner ved at bruge linket til **Fællesskab** i **Hjælp**-ruden. Det er også muligt at tilføje mere indhold gennem brugernes eller partnerens indhold, men denne udvidelse kræver en anden konfiguration.   

### <a name="annex-2-6-a--c"></a>Bilag 2, 6, a – c

Krav: Det digitale standard bogføringssystem understøtter deling af virksomhedens bogføringsdata ved at: 

* Bogføringssystemet gør det muligt at generere en standardfil, som er defineret af myndighederne.   
* Bogføringssystemet eksporterer en standardfil, som defineret af myndighederne, til en anden udbyder af bogføringssystemer.  
* Bogføringssystemet kan indlæse oplysningerne i en standardfil, som er defineret af myndighederne, så den er tilgængelig for kunden. 

Hvordan [!INCLUDE[prod_short](../../includes/prod_short.md)] overholder:

[!INCLUDE[prod_short](../../includes/prod_short.md)] understøtter generering af Standard Audit File for Tax (SAF-T) i XML-format indført ved bogføringsloven i juli 2022 i henhold til skema defineret af "_Danske SAF-T Finansielle data, version 1.0_", udgivet af Erhvervsstyrelsen, 11/2022. [!INCLUDE[prod_short](../../includes/prod_short.md)] kan også indlæse eksisterende SAF-T-filer hentet fra eksterne systemer og holde inde i databasen som en fil. Flere detaljer om denne funktion i [Eksporter SAF-T revisionsfilformatet i Danmark](how-to-use-saft-audit-files-export.md).   

### <a name="annex-2-7-a"></a>Bilag 2, 7, a

Krav: Bogføringssystemet opretter en CSV-fil med virksomhedernes bogføringsdata til Regnskab Basis. 

Hvordan [!INCLUDE[prod_short](../../includes/prod_short.md)] overholder:

[!INCLUDE[prod_short](../../includes/prod_short.md)] understøtter generering af CSV-fil med virksomhedens bogføringsdata i henhold til "Vejledning til upload af regnskabsfil I Regnskab Basis". Du kan forstå detaljer om [Eksport af regnskabsdata til Regnskab Basis i Danmark her](how-to-use-regnskabbasis-export.md)  

### <a name="annex-2-7-b"></a>Bilag 2, 7, b

Krav: Bogføringssystemet kan understøtte indberetning af moms via Skattestyrelsens VAT API. 

Hvordan [!INCLUDE[prod_short](../../includes/prod_short.md)] opfylder: [!INCLUDE[prod_short](../../includes/prod_short.md)] understøtter indberetning af momsangivelse via Skattestyrelsens VAT API og opdatering af statusser givet af myndigheder, men muliggør også download af svarbeskeder. Læs mere hvordan du [Indsender momsangivelser elektronisk](how-to-evat-statement-dk.md).  

### <a name="annex-2-8--9"></a>Bilag 2, 8 - 9

Krav: Besked om registrering i Nemhandelsregistrere og Registreringsfunktionalitet til Nemhandelsregistrere:  

* Det digitale standardbogføringssystem skal efter tilmelding af systemet i Erhvervsstyrelsen og ved tilmelding af nye kunder i systemet give besked til systemets eksisterende kunder, der gør dem opmærksom på muligheden for at blive registreret i NemHandelsregisteret. 
* Ved opsætning af systemet eller ved direkte besked til systemets eksisterende kunder skal det digitale standardbogføringssystem kunne vise information om og registreringsfunktionalitet for NemHandelsregisteret. Kunder skal kunne tilkendegive, at de ønsker at blive registreret i NemHandelsregisteret og give samtykke hertil og dermed blive registreret heri. Det godkendte bogføringssystem skal herefter varetage registreringen af ​​systemets kunder i NemHandelsregisteret ud fra de til enhver tid gældende standardfunktioner og krav i NemHandel.

Hvordan [!INCLUDE[prod_short](../../includes/prod_short.md)] overholder:

Hvis virksomheden ikke er registreret i NemHandelsregisteret, vises en meddelelse øverst på siden med registreringsinstruktioner. Hvis virksomheden er registreret, vil [!INCLUDE[prod_short](../../includes/prod_short.md)] tjekke om CVR-nummeret på siden Virksomhedsoplysninger findes som registreret i NemHandelsregisteret, og hvis det findes, vil beskeden ikke fremkomme, og denne virksomhed vil blive markeret som ' registreret i NemHandelsregisteret'. 

For at starte registreringen skal brugeren vælge linket Tilmeld dig i NemHandelsregisteret i meddelelsen. Når brugeren har afsluttet registreringen i NemHandelsregisteret, forsvinder meddelelsen. Flere oplysninger om [anmeldelse og tilmelding til NemHandelsregisteret i Danmark](how-to-nemhandel-register.md).   


## <a name="see-also"></a>Se også

[Lokal funktionalitet for Danmark](denmark-local-functionality.md)  
[Arbejd med [!INCLUDE[prod_short](../../includes/prod_short.md)]](../../ui-work-product.md)  

## [!INCLUDE[prod_short](../../includes/free_trial_md.md)]

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
