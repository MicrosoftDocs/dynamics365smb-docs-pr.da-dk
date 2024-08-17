---
title: Tabellen Reservationspost – Funktioner til opdatering af tabellen Reservationspost | Microsoft Docs
description: 'Den indeholder en vejledning, der kan hjælpe dig med at forstå og foretage fejlfinding af problemer med datauoverensstemmelser i tabellen Reservationspost.'
author: brentholtorf
ms.topic: conceptual
ms.devlang: al
ms.search.keywords: null
ms.date: 06/26/2024
ms.author: bholtorf
ms.service: dynamics-365-business-central
ms.reviewer: bholtorf
---

# <a name="reservation-entry-table---introduction"></a>Tabellen Reservationspost - Introduktion

Dette tekniske whitepaper indeholder vejledning, der kan hjælpe dig med at forstå og foretage fejlfinding af problemer med datauoverensstemmelser *i tabellen Reservationspost* (tabel 337) i [!INCLUDE[prod_short](includes/prod_short.md)]. Den første del er en introduktion til de funktioner, der genererer eller ændrer data i denne tabel. Den dækker også flere felter i *tabellen Reservationspost*, som det er værd at påpege i forhold til disse funktioner. I anden del demonstreres *det med eksempler, hvordan poster i tabellen Reservationspost* genereres, slettes eller ændres, når overflytningsordrer behandles, eller planlægningsfunktioner udføres.

Tabellen *Reservationspost* bruges til at håndtere og lagre oplysninger vedrørende reservation, varesporing og ordresporing.

Når der håndteres varesporing med delvis bogføring, fungerer tabellen sammen med *tabellen Sporingsspecifikation* (tabel 336). Data, som **brugeren har angivet på siden Varesporingslinjer**, oprettes i en midlertidig version af tabel 336 og overføres til tabel 337 og tabellen med sporingsspecifikation, når siden lukkes.

Generelt afhænger de data, der genereres i *tabellen Reservationspost*, af, hvilke funktioner du bruger, og hvilke parametre du har valgt på varen kort. Det drejer sig bl.a. om:

- Politik for ordresporing
- Regler for reservation
- Planlægningsfunktioner udført
- Genbestillings- og produktionspolitik
- Planlægningsparametre for varen eller lagervaren kort
- Varesporingskode

## <a name="features-that-update-the-reservation-entry-table"></a>Funktioner, der opdaterer tabellen Reservationspost

### <a name="order-tracking-policy"></a>Politik for ordresporing

 **Hvis feltet Ordresporingsmetode** for en vare er angivet til Ingen, [!INCLUDE[prod_short](includes/prod_short.md)]  oprettes der aldrig reservationsposter i *tabellen Reservationspost*, medmindre nettoplanen eller totalplanen, reservationen eller varesporingen udføres. Hvis ordresporing ikke er aktiveret, kan du desuden have reservationsposter, når du bruger politikkerne Produktion til ordre eller Montage til ordre.

Du kan overveje at indstille **ordresporingspolitikken** til Ingen, hvis du ikke har brug for sporing på farten, et behov i forhold til en forsyning eller omvendt. Sporing af forsyning i forhold til et behov håndteres af ordresporingsfunktionen eller planlægningsprogrammet. Vi anbefaler ikke, at du bruger ordresporing sammen med planlægningsfunktioner.

Når du angiver **feltet Ordresporingsmetode** til Kun sporing, [!INCLUDE[prod_short](includes/prod_short.md)]  oprettes der altid poster i tabel 337, hver gang der oprettes en ordre på varen, men **reservationsstatus** i tabel 337 er ikke altid strengt angivet til Sporing. Overvej følgende scenarie:

> [!NOTE]  
> Arbejdsdatoen er angivet til 23-01-2014 (MM/DD/ÅÅÅÅ) for alle eksempler. 
  
1. Opret en vare, hvor **feltet Ordresporingsmetode** er angivet til Kun sporing.  
1. Opret en indkøbsordre. [!INCLUDE[prod_short](includes/prod_short.md)] opretter en reservationspost med **reservationsstatus** som Overskud, da købsordren endnu ikke er allokeret til et behov.
1. Oprette en salgsordre. [!INCLUDE[prod_short](includes/prod_short.md)] vil nu oprette endnu en reservationspost med **reservationsstatus** som sporing.

Den **reservationsstatus**, der blev oprettet i trin 2, opdateres til Sporing; dette håndteres automatisk [!INCLUDE[prod_short](includes/prod_short.md)] . Dette koncept kaldes dynamisk sporing.
Ved at indstille feltet **Ordresporingsmetode** for varen til Kun sporing kan en slutbruger gøre brug af ordresporingsfunktionen til at få et overblik over, hvilken forsyning behovet er allokeret til og omvendt.

> [!NOTE]  
> Sporingsfunktionen erstatter ikke planlægningsfunktionaliteten, hvor alle varer, behov og forsyninger tages i betragtning under ét for at give de optimale planlægningsforslag til optimering af kundeserviceniveauet og afbalancering af lagerniveauerne.

### <a name="reservation-policy"></a>Regler for reservation

En reservation består af et par poster i *tabellen Reservationspost* med reservationsstatussen **Reservation**, som har samme løbenummer. Én post har feltet Positiv aktiveret og peger på forsyningen. Den anden post har feltet **Positiv** ikke aktiveret og peger på behovet. Felterne **Kildetype**, **Kildereferencenr**. og **Kilde-id** fremhæver den reservation, der sammenkæde mellem behov og levering.

Oplysningerne i **feltet Kildetype** er tabellen, reservationens **løbenr.** -feltet er relateret til. Hvis det f.eks. er en (negativ) behovspost, kan det være *tabellen Salgsordre* (tabel 37) eller *planlægningskomponenten*  (tabel 99000829).

Feltet Kilde-id **indeholder** id'et for det dokument i tabellen, der refereres til af Kildetype.

Kildehenvisningsnr **.** Indeholder et referencenummer til linjen, som reservationsløbenr **.** er relateret til. Hvis posten vedrører en salgs-, købs-, kladde- eller indkøbskladdelinje, kopieres oplysningerne i dette felt fra feltet Linjenr **.** . Hvis den vedrører en post i *tabellen Varepost* (tabel 32), kopieres oplysningerne i dette felt fra **feltet Løbenr.** i tabellen *Varepost* .

Når du bruger indstillingen Reservationspolitik Altid i kombination med ordresporing, synkroniseres begge normalt normalt. Men når reservationen fjernes, eller leveringsdatoen flyttes længere frem efter behovets forfaldsdato, fjernes ordresporingen. Du kan også støde på en fejlmeddelelse, hvor du bliver spurgt, hvad du [!INCLUDE[prod_short](includes/prod_short.md)] skal gøre med eksisterende reservationer. Dette scenarie illustreres i følgende eksempel:

1. Opret en ny vare med navnet COMP. Angiv følgende felter:
  - **Genbestillingssystem**: Køb
  - **Ordresporingsmetode**: Kun sporing
  - **Reserver**: Altid
2. Opret et andet element kaldet FG. Angiv følgende felter:
  - **Genbestillingssystem**: Prod.ordre
  - **Ordresporingsmetode**: Kun sporing
  - **Reserver**: Altid
3. Opret et andet element kaldet FG. Angiv følgende felter:
  - **Konto**: COMP
  - **Antal pr**.: 1
4. Godkend produktionsstyklistenr. Stykliste FG og tildel mod Vare FG.
5. Opret en indkøbsordre. Angiv følgende felter:
  - **Konto**: COMP
  - **Antal**: 10
  - **Lokationskode**: BLÅ
  - **Forventet modtagelsesdato**: 24-01-2014
6. Oprette en salgsordre. Angiv følgende felter:
  - **Afsendelsesdato**: 14-02-2014
  - **Lokationskode**: BLÅ
  - **Konto**: COMP
  - **Antal**: 10

> [!NOTE]  
> Der er foretaget automatisk reservation mellem købs- og salgsordren. Derudover er der oprettet ordresporing mellem købs- og salgsordrerne.

7. Opret en manuelt frigivet produktionsordre. Angiv følgende felter:
  - **Vare**: 14-02-2014
  - **Antal**: 10
  - **Beliggenhed, sted, område**: BLÅ
  - **Forfaldsdato**: 02/01/2014
8. Under fanen **Hjem** i gruppen Proces skal du vælge **Opdater produktionsordre**.
9. Åbn komponentlisten, og slå Varesammensætning op.

> [!NOTE]  
> Der oprettes ingen reservation eller ordresporing af [!INCLUDE[prod_short](includes/prod_short.md)]. Det skyldes, at der allerede findes en reservation mod den salgsordre, der blev oprettet i trin 6.

Antag, at varen af forretningsmæssige årsager er nødvendig mere presserende på den frigivne produktionsordre, der er oprettet i trin 7. I de følgende trin annullerer vi derfor reservationen fra den salgsordre, der blev oprettet i trin 6, og bemærker, hvordan ordresporing håndteres.

10. Slå salgsordren for Vare COMP op fra trin 6, og annuller reservationen.
11. Åbn købsordren fra trin 5, og bemærk, at der nu er oprettet ordresporing mellem købsordren og den nødvendige komponent fra den frigivne produktionsordre.
12. Genskab reservationen mellem den nødvendige komponent fra den frigivne produktionsordre og forsyningen fra købsordren i trin 5.

> [!NOTE]  
> Reservationen genoprettes ikke, hvilket skal gøres manuelt.

13.  **Ret feltet Forventet modt.dato** i købsordrehovedet på trin 5 fra 24-01-2014 til 05-02-2014.

[!INCLUDE[prod_short](includes/prod_short.md)] vises følgende advarselsmeddelelse:

   Der er forbehold for denne bekendtgørelse. Disse reservationer annulleres, hvis ændringen forårsager en datakonflikt. Vil du fortsætte?

14. Vælg Ja. Slå reservations- og ordresporingsposterne op fra købsordren.

> [!NOTE]  
> Den eksisterende reservation annulleres og skal oprettes igen manuelt. Ordren er imidlertid dynamisk og er blevet genskabt af [!INCLUDE[prod_short](includes/prod_short.md)] at eksistere mellem købsordren og salgsordren. Årsagen er, at behovet i den frigivne produktionsordre (01-02-2014) ligger før den forventede modtagelsesdato for leveringen.

Dermed er demonstrationen af samspillet mellem brug af automatiske reservationer og ordresporing afsluttet. Eksemplerne viser også, hvad der sker, når du ændrer forfaldsdatoer, og den fejlmeddelelse, der udløses, når der er en reservationskonflikt.

### <a name="planning-calculated"></a>Beregnet planlægning

Når planlægningen udføres vha. ordreplanlægningen, indkøbskladden eller planlægningskladden, genereres der poster i *tabellen Reservationspost* med **feltet Reservationsstatus** angivet til Sporing, Reservation eller Overskud. Der skal altid være et matchende par med samme løbenr. af positiv og negativ værdi i feltet **Antal (basis),**  når status er Sporing eller Reservation. Feltet Kildetype **er** behovstypen, dvs. tabel 37 for det negative antal og en planlægningstabel, f.eks. tabel 246, for det positive antal. Feltet Kilde-id **vil** være PLANLÆGNING.

I tilfælde af ikke-allokeret udbud eller behov, [!INCLUDE[prod_short](includes/prod_short.md)]  angives feltet **Reservationsstatus** til Overskud. Du kan f.eks. have reservationsstatussen Overskud, når den eksisterende lagerbeholdning er under sikkerhedslageret, eller behovet er knyttet til forecast.

Tabellen *Ikke-sporet planlægningselement* (tabel 99000855) indeholder oplysninger om ikke-sporede antal, der vises, når brugeren foretager et opslag fra ordresporingssiden for at se ikke-sporede antal eller vælger et advarselsikon i planlægningskladden. Tabellen indeholder poster for ikke-sporet overskud i ordresporingsnetværket.

Disse poster genereres i forbindelse med planlægningskørslen og forklarer, hvor det ikke-sporede overskud på ordresporingslinjerne stammer fra. Det ikke-sporede overskud kan stamme fra:

- Produktionsforecast
- Rammeordrer
- Sikkerhedslager
- Genbestillingspunkt
- Maks. lagerbeholdning
- Ordrekvantum
- Maks. ordrestørrelse
- Min. ordrestørrelse
- Oprundingsfaktor
- Aktionsgrænse (% af lotstr.)

 *I tabellen Reservationspost* findes **feltet Planlægningsfleksibilitet** ligesom på købs-, overflytnings- og produktionsordrerne. Denne indstilling angiver, om der tages højde for forsyningen repræsenteret af disse forsyningsordrer i planlægningssystemet, når der beregnes aktionsmeddelelser. Hvis feltet indeholder indstillingen Ubegrænset, medtages linjen i beregningen af aktionsmeddelelser i planlægningssystemet. Hvis feltet viser indstillingen Ingen, er linjen låst og kan ikke ændres, og planlægningssystemet medtager ikke linjen, når aktionsmeddelelsen beregnes. Funktionen administreres i *tabellen Reservationspost* af feltet med samme navn.

### <a name="reordering-and-manufacturing-policy"></a>Genbestillings- og produktionspolitik

Hvis der udføres en planlægningsfunktion for et varesæt, hvor Genbestillingsmetode er angivet til Ordre, [!INCLUDE[prod_short](includes/prod_short.md)]  oprettes der poster i *tabellen Reservationspost* med reservationsstatus af typen Reservation i stedet for Sporing.

Felterne **Kildetype** og **Kilde-id** behandles på samme måde som andre genbestillingspolitikker. I feltet **Binding** i *tabellen*  Reservationspost [!INCLUDE[prod_short](includes/prod_short.md)] står der dog Ordre-til-ordre.

Feltet **Binding** udfyldes for at styre forsyningsordrer, der er knyttet til bestemte behov, f.eks. produktionsordrer, der oprettes direkte ud fra salgsordrer. Ordre-til-ordre vises i feltet, når posten er knyttet specifikt til et behov eller en forsyning (Automatisk reservation). Behovet kan være relateret til salg eller komponentbehov.

### <a name="item-tracking-and-prospect-reservation-entry"></a>Varesporing og post for reservation af kundeemner

Kundeemnereservationsstatus kan oprettes af [!INCLUDE[prod_short](includes/prod_short.md)] i *tabellen Reservationspost*, når du ikke bruger nogen ordrenetværksenheder, dvs. ordresporing. På en forbrugskladdelinje kan du f.eks. tildele varesporing til komponenten. Men hvis varen allerede er ordresporet [!INCLUDE[prod_short](includes/prod_short.md)] , kan der opstå flere kundeemnereservationsposter. Dette er demonstreret i EKSEMPEL 2 vedrørende overflytningsordrer i anden del af dette dokument.

Når du får vist eller ændrer **siden Varesporingslinjer**, vises det samlede indhold i *tabellen Sporingsspecifikation* (tabel 336) og *tabellen Reservationspost* i en midlertidig version af tabel 336. Dette sikrer, at historiske og aktive varesporingsdata kan åbnes som en.

Reservationer falder i to kategorier: Uspecifikke reservationer, hvor lot- og serienumre ikke er angivet på reservationstidspunktet, og Specifikke reservationer, hvor du reserverer specifikke lot- eller serienumre fra lageret.

Ved en uspecifik reservation anses Lotnr **.** eller **serienr.** feltet er tomt i feltet **Løbenr.** i tabel 337, der peger på efterspørgslen (f.eks. salget). På grund af strukturen i reservationslogikken skal [!INCLUDE[prod_short](includes/prod_short.md)] du, når du placerer en uspecifik reservation på en varesporet vare på lageret, [!INCLUDE[prod_short](includes/prod_short.md)]  alligevel vælge specifikke vareposter at reservere mod.

Da vareposterne indeholder varesporingsoplysningerne, reserverer reservationen indirekte bestemte lot- eller serienumre, selvom brugeren ikke havde til hensigt dette. Med Sen binding [!INCLUDE[prod_short](includes/prod_short.md)]  reserveres der dog stadig forbehold for bestemte poster, men der bruges derefter en omrokeringsmekanisme [!INCLUDE[prod_short](includes/prod_short.md)] ved bogføring.

Du kan finde flere oplysninger i de [!INCLUDE[prod_short](includes/prod_short.md)] tekniske hvidbøger, der er angivet i Yderligere ressourcer i slutningen af dette dokument.

### <a name="source-subtype-suppressed-action-msg-action-message-adjustment-and-disallow-cancellation-fields"></a>Felterne Kildeundertype, Undertrykt aktionsmedd., Justering af aktionsmeddelelse og Tillad ikke annullering

Felterne Kildeundertype,Undertrykt **aktionsmedd**. **,** Aktionsmeddelelsesjustering **og** Tillad ikke annullering **i** tabellen Reservationspost *er beskrevet i dette* afsnit. Der opstilles scenarier for at demonstrere brugen af felterne **Undertrykt aktionsmedd.**, **Justering** af aktionsmeddelelse og **Tillad ikke annullering** . Feltet **Aktionsmeddelelsesjustering** bruges til ordresporingspolitikfunktionen Sporing og Aktionsmeddelelse. Feltet **Tillad ikke annullering** bruges til funktionen Montage efter ordre i [!INCLUDE[prod_short](includes/prod_short.md)] 2013.

#### <a name="source-subtype"></a>Kildeundertype

Feltet Kildeundertype **angiver**, hvilken kildeundertype reservationsposten vedrører. Hvis posten vedrører en købs- eller salgslinje, kopieres feltet fra feltet Bilagstype **på** linjen. Hvis posten vedrører en kladdelinje, kopieres feltet fra feltet **Posttype** på kladdelinjen.

#### <a name="suppressed-action-msg"></a>Undertrykt aktionsmeddelelse

Den **undertrykte aktionsmedd.** registrerer når en eksisterende forsyning allerede er delvist behandlet, f.eks. når en købsordre allerede er delvist modtaget, eller når der bogføres forbrug i en produktionsordre.

Når planlægningen er udført, markeres dette felt, [!INCLUDE[prod_short](includes/prod_short.md)]  og feltet Status for reservationspost **angives** til *Overskud8. Følgende eksempel tjener som illustration:

1. Åbn vare 80001. Angiv følgende felter:
  - **Genbestillingsmetode**: Lot-for-lot
  - **Reservér**: Valgfrit
  - **Ordresporingspolitik**: Ingen
2. Oprette en salgsordre. Angiv følgende felter:
  - **Vare**: 80001
  - **Sted**: Tom/Ingen
  - **Antal**: 10
  - **Afsendelsesdato**: 15-02-2014
3. Åbn indkøbskladden, **og** udfør **kørslen Beregn plan** for vare 80001.
  - **Startdato**: 23-01-2014
  - **Slutdato**: 01-03-2014
4. Der gives et planlægningsforslag om genopfyldning af antal på 10 med ny købsordre og **forfaldsdato** 15-02-2014.
5.  **Under fanen Handlinger** i gruppen Funktioner skal du vælge **Udfør aktionsmeddelelse** for at oprette en købsordre med **forventet modtagelsesdato** 15-02-2014.
6. Åbn købsordren fra trin 5, angiv **Modtag** antal til 2, og bogfør kun Modtagelse.
7. Åbn salgsordren fra trin 2, og rediger **Afsendelsesdato** til 02/10/2014.
8. Åbn indkøbskladden, **og** kør **Beregn plan** for vare 80001
  - **Startdato**: 23-01-2014
  - **Slutdato**: 01-03-2014
9. Der gives et planlægningsforslag om genopfyldning af antal på 8 med ny købsordre og **forfaldsdato** 02-10-2014.

Statusoplysningerne i tabel 337 er vist i følgende illustration.

Løbenr. 28 i tabel 337 har reservationsstatus Sporing, der svarer til den eksisterende lagerbeholdning, der er registreret i varepost 318 for 2 enheder og det udestående behov i salgsordretabel 37. Det efterfølgende løbenummer 29 har også reservationsstatus Sporing og sammenkæder det resterende antal på 8 enheder mellem behovet i salgsordretabel 37 og den foreslåede levering i tabel 246 over indkøbskloneringslinjen.

Løbenr. 30 er den eksisterende købsordre, der er delvist modtaget sammen med antal 2. Som følge heraf **er feltet Reservationsstatus** Overskud, og [!INCLUDE[prod_short](includes/prod_short.md)]  **feltet Antal (basis)**  angives til *8*  (restsaldo) og **meddelelsen Undertrykt handling.** er aktiveret.

#### <a name="action-message-adjustment"></a>Aktionsmeddelelsesjustering

Feltet **Aktionsmeddelelsesjustering** viser ændringen på forsyningssiden i den ordresporing, der finder sted, når du accepterer den relaterede aktionsmeddelelse. Der vises kun en værdi her, når funktionerne for ordresporing og aktionsmeddelelser er aktive (Ordresporingsmetode er angivet til Sporing & aktionsmedd.). Værdien beregnes på basis af data i tabellen *Aktionsmeddelelsespost* (tabel 99000849). Følgende eksempel tjener som illustration:
1. Åbn punkt 80002. Angiv følgende felt:
 - **Ordresporingsmetode**: Sporing og aktionsmedd.
2. Oprette en salgsordre. Angiv følgende felter:
  - **Vare**: 80002
  - **Beliggenhed, sted, område**: BLÅ
  - **Antal**: 100
3. Åbn siden **Ordreplanlægning**, og kør **kørslen Beregn plan** .
4. Vælg salgsordren fra trin 2, og kør **Lav ordrer** .
5. I salgsordren fra trin 2 skal du ændre **feltet Antal** fra 100 til 105.
Statusoplysningerne i tabel 337 er vist i følgende illustration.
6. Løbenr. 34 har feltet **Aktionsmeddelelsesregulering** i tabel 337 aktiveret for 5 enheder med reservationsstatus Overskud. Da salgsordren blev udvidet til trin 5, blev denne reservation oprettet, [!INCLUDE[prod_short](includes/prod_short.md)]  fordi der kræves mere forsyning.
7. Åbn siden **Planlægningskladder,** og **vælg** Hent aktionsmeddelelser i gruppen **Proces under fanen Hjem**  **·**. [!INCLUDE[prod_short](includes/prod_short.md)] vil foreslå, at antallet i indkøbsordren øges fra 100 til 105.

#### <a name="disallow-cancellation"></a>Afvis annullering

Feltet **Tillad ikke annullering** angiver, at reservationsposten repræsenterer sammenkæde mellem en salgsordrelinje og en montageordre. Du kan ikke slette denne reservation, fordi den er nødvendig for at bevare den synkronisering, der sker, når en vare samles på bestilling. Følgende eksempel tjener som illustration:

1. Opret en indkøbsordre. Angiv følgende felter:
  - **Basisenhed**: STK
  - Eventuelle standardbogføringsgrupper
  - **Genbestillingssystem**: Montering
  - **Montagepolitik**: Montage på bestilling
  - **Ordresporingsmetode**: Kun sporing
2. Opret en ny vare med navnet Saml SAMMENSÆTNING. Angiv følgende felter:
  - **Basisenhed**: STK
  - Eventuelle standardbogføringsgrupper
  - **Genbestillingssystem**: Køb
  - **Ordresporingsmetode**: Kun sporing
3. Åbn Saml FG, vælg **Samling i gruppen** Montage/produktion **under fanen Naviger**, **og vælg** derefter **Montagestykliste**. Angiv følgende felter på montagestyklisten:
  - **Type**: Vare
  - **Nr.**: Saml COMP
  - **Antal pr**.: 1 Vælg knappen **OK** .
4. Åbn en varekladde, og øg lagerbeholdningen af Saml COMP til antal 10 i forhold til lokationen BLÅ, og bogfør kladdelinjen.
5. Oprette en salgsordre. Angiv følgende felter:
  - **Vare**: Saml FG
  - **Beliggenhed, sted, område**: BLÅ
  - **Antal**: 1 Statusoplysningerne i tabel 337 vises i følgende illustration.

Løbenr. 82 har Reservationsstatus Overskud som 9 enheder af samlekompagniet på lager og har intet behov. Løbenr. 84 sporer reservationsposter mellem behovet på samlebåndstabel *901* og dets forsyning på varepost 346.

Indgang nr. 86 har bindende ordre-til-ordre med reservationsstatusreservation.  **Derudover er feltet Tillad ikke annullering** aktiveret, da monteringsmetoden er angivet som Montage efter ordre for varemontage FG.  **Endelig er feltet Planlægningsfleksibilitet angivet til Ingen**, hvilket [!INCLUDE[prod_short](includes/prod_short.md)] ikke tillader planlægningslogikken at slette reservationen.

#### <a name="quantity-available-to-pick-and-reservations"></a>Antal til rådighed til pluk og reservationer

Det **reserverede pick &; send-antal** Feltet i tabel 337, der findes i versioner før [!INCLUDE[prod_short](includes/prod_short.md)] 2013, styrer varedisponeringen på et administreret lagersted. I alle installationer af [!INCLUDE[prod_short](includes/prod_short.md)] lagerstedsstyring findes vareantal både som lagerposter og som vareposter. Disse to posttyper indeholder forskellige oplysninger om, hvor varerne findes, og om de er tilgængelige. Lagerposter definerer en vares tilgængelighed efter placering og placeringstype, samlet kaldet placeringsindhold. Vareposter definerer en varedisponering ved sin reservation til udgående dokumenter. Der er en særlig funktionalitet i plukalgoritmen til beregning af det antal, der er tilgængeligt til pluk, når placeringsindhold kobles sammen med reservationer. Plukalgoritmen fratrækker antal, der er reserveret til andre udgående dokumenter, antal i eksisterende plukdokumenter og antal, der er plukket, men endnu ikke leveret eller forbrugt. Resultatet vises i feltet **Disponibelt antal til pluk** på siden **Plukkladde**, hvor feltet beregnes dynamisk. Værdien beregnes også, når en bruger opretter lagerpluk direkte fra udgående dokumenter, f.eks. salgsordrer, produktionsforbrug eller udgående overflytninger.

*Antal til pluk = antal i plukplaceringer - antal på pluk og bevægelser - (reserveret antal i plukplaceringer + reserveret antal på pluk og bevægelser).*

Følgende eksempel illustrerer, hvordan værdien i det antal, der kan plukkes, beregnes i [!INCLUDE[prod_short](includes/prod_short.md)]:

1. Opret en ny vare med navnet Lagervare. Angiv følgende felter:
  - **Basisenhed**: STK
  - Eventuelle standardbogføringsgrupper
  - **Genbestillingssystem**: Køb
  - **Reservepolitik**: Altid
  - **Ordresporingsmetode**: Kun sporing
2. Opret en købsordre mod kreditor 60000. Angiv følgende felter:
  - **Vare**: Lagervare
  - **Beliggenhed, sted, område**: HVID
  - **Antal**: 100
3. Frigiv købsordren, og opret lagermodtagelsen.
4. Bogfør lagermodtagelsen, og registrer læg-på-lager-aktiviteten for antal 100.
5. Opret endnu en købsordre mod kreditor 60000. Angiv følgende felter:
  - **Vare**: Lagervare
  - **Beliggenhed, sted, område**: HVID
  - **Antal**: 10
6. Frigiv købsordren, og opret lagermodtagelsen.
7. Bogfør KUN lagermodtagelsen. Registrer ikke læg-på-lager-aktiviteten.
8. Oprette en salgsordre. Angiv følgende felter:
  - **Vare**: Lagervare
  - **Beliggenhed, sted, område**: HVID
  - **Antal**: 10 Reserveret antal indstilles automatisk til 10, da reservationspolitikken er indstillet til Altid.
9. Oprette en salgsordre. Angiv følgende felter:
  - **Vare**: Lagervare
  - **Beliggenhed, sted, område**: HVID
  - **Antal**: 100 Reserveret antal indstilles automatisk til 100, da reservepolitikken er angivet til Altid.
10. Frigiv den første salgsordre fra trin 8, og opret en lagerleverance.
11. Frigiv lagerleverancen, og vælg Opret pluk under **fanen Handlinger**  **.**
Følgende fejlmeddelelse vises: *Intet at håndtere.*
  Årsagen er, at det disponible antal til pluk er nul. Dette beregnes på følgende måde: Antal på lager = 110 Antal til pluk = 100

> [!NOTE]  
> Antal på læg-på-lager- eller modtagelsesplacering kan ikke plukkes.
   
   Det samlede antal varer, der er reserveret til salgsordrer, er 110 Antal til pluk = 100 – 110 = nul.

Når læg-på-lager-aktiviteten registreres i trin 7, kan pluklisten oprettes i trin 11. I versioner før [!INCLUDE[prod_short](includes/prod_short.md)] 2013 er det reserverede **pick &; ship-antal** Feltet i tabel 337 udfyldes i forhold til reservationen for antal 10.

Følgende illustration er taget fra [!INCLUDE[prod_short](includes/prod_short.md)] 2009 R2.

## <a name="illustrations-using-transfer-orders-and-planning"></a>Illustrationer af overflytningsordrer og planlægning

### <a name="transfer-orders"></a>Overflytningsordrer

Når du bruger overflytningsordrer, og varen er afsendt, men ikke modtaget fuldt ud, får du vist reservationsstatussen Overskud i *tabellen Reservationspost* . Lokationskoden er Overflyt til-lokationen.

Kildehenvisningsnr **.** Feltet beregnes ud fra det sidste linjeløbenummer + linjeløbenummer for varen i den bogførte overflytningsleverance.

Når ordresporing er aktiveret, [!INCLUDE[prod_short](includes/prod_short.md)]  og der ikke er noget behov (salgsordre eller forbrug), oprettes der to poster i tabel 337 med reservationsstatus Overskud. Den ene er imod *overflytningslinjetabel* 5741, og den anden er imod vareposttabel 32.

Dette er demonstreret i det første eksempel.

#### <a name="example-1"></a>Eksempel 1

1. Åbn vare 80003 og 80004, og angiv feltet **Sporingsmetode** til *Kun* sporing. Lad de andre felter være standard.
2. Åbn en varekladde, og øg lagerbeholdningen af disse varer til antal 10 hver mod lokationen RØD, og bogfør kladdelinjerne.
3. Opret en overflytningsordre fra lokationen RØD til BLÅ for disse to varer: Vare 80003 på overflytningsordrelinje 10000 og Vare 80004 på anden linje 20000, begge på 10 enheder.
4. Bogfør kun leveringsdelen af overflytningsordren uden lagerfunktioner.
Den bogførte overflytningsleverance er vist i følgende illustration.
Statusoplysningerne i tabel 337 er vist i følgende illustration.
5. Sammenligne resultaterne på den bogførte overflytningsleverance med posterne i tabel 337.

I følgende tabel beskrives, hvad der sker i bestemte felter i forhold til reservationspost 40.

|Felt|Beskrivelse|  
|---------------------------------|---------------------------------------|  
|**Reservation Status**|Overskud som vare 80003 er oprettet med ordresporing, men der er ikke noget behov.|  
|**Lokationskode**|Overflyt til-kodelokation BLÅ.|  
|**Kildetype**|Overflytningslinje tabel 5741.|  
|**Kilde-id**|Bilagsnr. af overflytningsordren 1011.|
|**Kilde: Ref.nr.**|Linjenr. i alt 20000 + Linjenr. 10000 ud for vare 80003 = 30000.|

Forklaringen på følgende felter mod reservationspost 43 er som følger.

|Felt|Beskrivelse|  
|---------------------------------|---------------------------------------|  
|**Reservation Status**|Overskud som vare 80003 er oprettet med ordresporing, men der er ikke noget behov.|  
|**Lokationskode**|Transitlokationen OWN LOG er den lokation, hvor varen findes.|  
|**Kildetype**|Tabellen Varepost 32.|  
|**Kilde: Ref.nr.**|Det åbne vareløbenummer 322.|

#### <a name="example-2"></a>Eksempel 2

I næste eksempel illustreres det, når en komponent overføres mellem lokationer, men samtidig spores mellem et behovsbehov og en tilgængelig forsyning. Komponenterne overføres fra lokationen RØD til BLÅ, som skal forbruges på en frigivet produktionsordre. Komponenten bruger Ordresporing, Ordreplanlægning og Varesporing.

I eksemplet fremhæves det registrerede flow i tabel 337 i forhold til felterne **Reservationsstatus,Lokationskode,Kildetype,Kilde-id,Kildereferencenr** **·** **·** **·** **·**. og bindingstype. **·**

1.  **På siden Produktionsopsætning** skal du angive feltet **Komponenter på lokation** indstillet til RØD.
2. Opret en ny varekomponent. Angiv følgende felter:
  - **Basisenhed**: STK
  - Eventuelle standardbogføringsgrupper
  - **Genbestillingssystem**: Køb
  - **Produktionsmetode**: Fremstil-til-lager
  - **Ordresporingsmetode**: Kun sporing
  - **Varesporingskode**: LOTALL
3. Brug varekladden til at øge lagerbeholdningen for Varekomponent i forhold til lokationen RØD til 100 enheder. Angiv følgende lotnumre:
  - Lotnummer Lot A, Antal 30
  - Lotnummer Parti B, Antal 70
4. Opret en ny vare Produceret. Angiv følgende felter:
  - **Basisenhed**: STK
  - Eventuelle standardbogføringsgrupper
  - **Genbestillingssystem**: Produktion
  - **Produktionsmetode**: Fremstil-til-lager
  - **Ordresporingsmetode**: Kun sporing
5. Opret **produktionsstykliste** med 1 antal pr. af varekomponenten.
6. Tildel produktionsstyklisten mod Fremstillet vare.
7. Oprette en salgsordre. Angiv følgende felter:
  - **Vare**: Produceret
  - **Beliggenhed, sted, område**: BLÅ
  - **Antal**: 100
8.  **Under fanen Handlinger** i gruppen **Plan** i salgsordren skal du vælge **Planlægning** for at oprette en tilknyttet frigivet produktionsordre i forhold til salgsordren.
9. Åbn behovet for frigivet produktionsordre/komponent, og bemærk, at lokationen er angivet som RØD.
Årsagen er, at komponenterne på lokationen **er** RØD på **produktionsopsætningen**  kort.
Den producerede vare får afgangen i forhold til lokationen BLÅ.

Statusoplysningerne i tabel 337 er vist i følgende illustration.

##### <a name="reservation-entries-with-numbers-55-and-56"></a>Reservationsposter med nummer 55 og 56

For komponentbehovet for henholdsvis lot A og lot B oprettes ordresporingslinks fra behovet i tabel 5407, Prod.ordrekomponent, til leveringen i tabel 32, Varepost. Feltet **Reservationsstatus** indeholder Sporing for alle fire poster for at indikere, at disse dynamiske ordresporing er forbundet mellem udbud og efterspørgsel.

Behovet i tabel 5407, Prod.ordrekomponent, er knyttet til kilde-id'et for den frigivne produktionsordre 101006. Forsyningen i tabel 32, Varepost, er knyttet til Kilderef.nr. Er de varepostnumre 325 og 326, hvor enhederne findes.

> [!NOTE]  
> Feltet **Lotnr.** er tomt på behovslinjer, fordi der ikke er angivet lotnumre på komponentlinjerne i den frigivne produktionsordre.

##### <a name="reservation-entry-with-number-57"></a>Reservationspost med nummer 57

Fra salgsbehovet i tabel 37, Salgslinje, oprettes der en ordresporing sammenkæde til forsyningen i tabel 5406, Prod.ordrelinje. Feltet **Reservationsstatus** indeholder Reservation, og feltet **Binding** indeholder Ordre-til-ordre. Det skyldes, at den frigivne produktionsordre blev oprettet specifikt til salgsordren og skal forblive tilknyttet i modsætning til ordresporingslinks med reservationsstatus Sporing, der oprettes og ændres dynamisk.

> [!NOTE]  
> Feltet **Binding** kan også indeholde *Ordre-til-ordre*, når Fremstil-til-ordre bruges som produktionspolitik og/eller Ordre som genbestillingsmetode.

10. På dette tidspunkt i scenariet overføres komponentens 100 enheder fra lokationen RØD til lokationen BLÅ ved hjælp af en overflytningsordre.

Vælg Parti A og Parti B for leverancen.

Bogfør det samlede udestående antal som KUN leveret.

> [!NOTE]  
> Komponenter kan forbruges på lokationen RØD, men for at illustrere flowet af reservationsposter overføres enhederne manuelt til lokationen BLÅ.

Statusoplysningerne i tabel 337 er vist i følgende illustration.

##### <a name="reservation-entries-with-number-55-and-56"></a>Reservationsposter med nummer 55 og 56

Ordresporingsposterne for de to partier af komponenten, der afspejler behovet i tabel 5407, ændres fra reservationsstatussen Sporing til Overskud. Årsagen er, at de forsyninger, som de var knyttet til tidligere, i tabel 32, er anvendt af overflytningsordren ved leverancen. Ægte overskud, som i dette tilfælde, afspejler overskydende forsyning eller behov, som forbliver ikke-sporet. Det er en indikation af ubalance i ordrenetværket, som genererer en aktionsmeddelelse fra planlægningssystemet, medmindre den løses dynamisk.

##### <a name="reservation-entry-numbers-59-to-63"></a>Reservationsløbenummer 59 til 63

Da de to partier af komponenten er bogført på overflytningsordren som leveret, men ikke modtaget, er alle relaterede positive ordresporingsposter af reservationstypen Overskud, hvilket indikerer, at de ikke er allokeret til nogen behov. For hvert lotnummer vedrører én post tabel 5741, Overflytningslinje, og én post vedrører vareposten på det transitsted, hvor varerne nu findes.

Tabel 5741, **Overflytningslinje**, er kildetypen. **Kilde-id** er overflytningsordredokumentnummer 1012 og **kildereferencenr.** Er 20000 = 10000 + 10000 som beskrevet i eksempel 1. Lokationen angives som BLÅ for overflyt til-lokationskoden.

De resterende to poster med **Reserveringsstatus** – Overskud har tabel 32,Varepost **·**, som Kildetype og **Kildereferencenr.** 328 og 330, herunder deres lotnumre, der på nuværende tidspunkt befinder sig på transitstedet OUT LOG.

11. Bogføre den udestående overflytningsordre som Modtaget.

Statusoplysningerne i tabel 337 er vist i følgende illustration.

Ordresporingsposterne ligner nu det første punkt i scenariet, hvor overflytningsordren før kun blev bogført som leveret, bortset fra at posterne for komponenten nu har reservationsstatus Overskud i stedet for Sporing. Dette skyldes, at komponentbehovet stadig er på lokationen RØD, hvilket afspejler, at **feltet Lokationskode** på produktionsordrekomponentlinjen indeholder RØD som angivet i **feltet Komponenter på lokationsopsætning** .

Den forsyning, der tidligere blev allokeret til dette behov, er blevet overført til lokationen BLÅ og kan nu ikke spores fuldt ud, medmindre behovet for komponenter på produktionsordrelinjen ændres til lokationen BLÅ. Dette registreres i de sidste to reservationsposter, hvor lotnumrene er udfyldt, **idet feltet Kildetype** er Tabel 32 og **Kildereferencenr.** Vareposterne 333 og 334.

12. På komponentlisten, der er tildelt den frigivne produktionsordre, skal du ændre lokationen til BLÅ for komponenten.

12. Åbn **forbrugskladden**  **, og kør kørslen Beregn forbrug** .
Tildel parti A-antal 30 og parti B-antal 70.

Luk formen Varesporing.

Statusoplysningerne i tabel 337 er vist i følgende illustration.

##### <a name="reservation-entries-with-numbers-68-and-69"></a>Reservationsposter med nummer 68 og 69

Da komponentbehovet er ændret til lokation BLÅ, og forsyningen er tilgængelig som vareposter på lokationen BLÅ, er alle ordresporingsposter for de to lotnumre nu fuldt sporet, hvilket indikeres af reservationsstatus Sporing. Lotnumrene udfyldes ikke på lotnummeret **.** i forhold til behovet i tabel 5406,Prod.ordrelinje **·**, da vi ikke har angivet lotnumre for komponenten på den frigivne produktionsordre.

##### <a name="reservation-entries-with-numbers-70-and-71"></a>Reservationsposter med numrene 70 og 71

Posterne med reservationsstatussen Lead genereres i tabel 337. Årsagen er, at begge lotnumre er knyttet til komponenten i forbrugskladden, men kladden er ikke blevet bogført.

Dermed er dette afsnit færdigt, hvordan ordresporingsposter i **tabellen Reservationspost** genereres, ændres og slettes, når der bruges flere funktioner i kombination med overflytningsordrer.

### <a name="planning-calculated-1"></a>Beregnet planlægning

Hvis du bruger planlægningsfunktioner, dvs. indkøbskladden, planlægningskladden **eller** **ordreplanlægningen**, kan reservationsposterne i **reservationsposttabel** 337 blive ændret eller tilføjet, afhængigt af det planlægningsforslag, der er angivet i logikken i **.**  [!INCLUDE[prod_short](includes/prod_short.md)] I eksempel 3 bruges **Genbestillingspolitikordre** sammen med **Fremstil-til-ordre for produktionsmetode** for en produceret vare. Komponenten bruger **Genbestillingsmetode** Fast genbestil.antal.

#### <a name="example-3"></a>Eksempel 3

1. I **Produktionsopsætning**  kort **er Komponent på lokation** RØD fra det forrige eksempel.
2. Opret nye overordnet Vare 70061. Angiv følgende felter:
  - **Basisenhed**: STK
  - Eventuelle standardbogføringsgrupper
  - **Genbestillingssystem**: Prod.ordre
  - **Produktionsmetode**: Fremstil-til-ordre
  - **Genbestillingsmetode**: Ordre
  - **Reservepolitik**: Valgfrit
  - **Ordresporing**: Ingen
3. Opret ny komponentvare 70062. Angiv følgende felter:
  - **Basisenhed**: STK
  - Eventuelle standardbogføringsgrupper
  - **Genbestillingssystem**: Køb
  - **Genbestillingsmetode**: Fast genbestil.antal
  - **Reservepolitik**: Valgfrit
  - **Ordresporingspolitik**: Ingen
  - **Sikkerhedslager**: 10
  - **Genbestillingspunkt**: 25
  - **Genbestil antal**: 50
4. Opret en ny produktionsstykliste, og angiv komponentvare 70062 med antal pr. 1.
Tildel produktionsstyklisten til overordnet vare 70061.
5. Oprette en salgsordre. Angiv følgende felter:
  - **Vare**: Fast genbestil.antal
  - **Beliggenhed, sted, område**: RØD
  - **Antal**: 40
  - **Afsendelsesdato**: 15-02-2014
6. Åbn siden **Planlægningskladder**, og kør **kørslen Beregn totalplan** .
  - **Hovedplan/MRP:** aktiveret
  - **Startdato**: 23-01-2014
  - **Slutdato**: 01-03-2014
  - Filtrere på vare 70061 og 70062
  - Ingen prognose

Der gives følgende planlægningsforslag.

Det første planlægningsforslag går ud på at oprette en ny planlagt produktionsordre for at dække det udestående behov i salgsordren for antal 40 i den overordnet vare 70061. Gennemse ordresporingen og [!INCLUDE[prod_short](includes/prod_short.md)] vil vise den udestående salgsordre. Ordresporing aktiveres, når den oprettes af planlægningsprogrammet.

Den anden linje er at placere lagerbeholdningen over genbestillingspunktet (25). Så under hensyntagen til Genbestil antal (50) foreslås et antal på 50 enheder af planlægningslogikken. Den tredje linje er at bringe lagerbeholdningen op på sikkerhedslagerniveau (10).

Den fjerde linje er at genopfylde lagerbeholdningen, når salgsordren leveres. På det tidspunkt er lagerbeholdningen 20 og deromkring under Genbestillingspunkt. Som følge heraf foreslår planlægningsprogrammet at købe 50 ekstra komponenter under hensyntagen til Genbestil antal. Dette er Ikke-sporet antal, så i *reservationsposttabel* 337 markeres dette med reservationsstatus Overskud.

Statusoplysningerne i tabel 337 er vist i følgende illustration.

Feltet **Reservationsstatus** er Reservation, og der oprettes en ordre-til-ordre-binding. Årsagen er, at vareproduktionspolitikken er Fremstil-til-ordre, og genbestillingspolitikken er angivet som Ordre. Hvis en af de to er angivet til Ordre, vil reservationsstatus være Reservation i stedet for Sporing, og Binding er angivet til Ordre-til-ordre.

Behovet på 40 enheder i forhold til feltet **Kilde-id** er salgsordrenummeret 1005, og Kildetype er *Salgslinjetabel* 37. Reservationsposten er i overensstemmelse med planlægningsforslaget, Kilderef.nr. 10000, Kilde-id er PLANLÆGNING, og Kildetype er *Indkøbskladdelinjetabel* 246. Der er altså en balance mellem behovet fra salgsordren og det udbud, der foreslås af planlægningsprogrammet.

##### <a name="reservation-entry-numbers-73-and-74"></a>Reservationsløbenummer 73 og 74

Når kørslen Beregn plan udføres, genereres de næste fire poster med reservationsstatussen Sporing på grund af indstillingen af genbestillingsmetoden Fast genbestil.antal for komponenten. Den nødvendige forsyning til komponentvare 70062 genopfyldes med de givne planlægningsforslag, Kilderef.nr. 20000 og 30000, med Kilde-id angivet til PLANLÆGNING og Kildetype fra *indkøbskladdelinjen* tabel 246. Komponentbehovet oprettes for at opfylde behovet for den overordnet vare 70061 for det samlede antal (basis) 40. Som følge af dette behov er feltet **Kildeproduktordrelinje** 10000, mens Kildetype er *tabellen Komponentbehov* 99000829.

Reservationsstatus er ikke Overskud, da ordresporing eksisterer mellem behovet for overordnet vare 70061 og leveringen af komponentvare 70062.

##### <a name="reservation-entry-numbers-75-and-76"></a>Reservationsløbenummer 75 og 76

De sidste to poster har reservationsstatus Overskud, da der er tale om ikke-sporede antal, der er genereret i planlægningskladden i forbindelse med genbestillingsparametrene Genbestillingspunkt og Genbestil antal.

## <a name="see-also"></a>Se også
[Designoplysninger: Design af varesporing](design-details-item-tracking-design.md)  
[Designoplysninger: Afstemning mellem udbud og efterspørgsel](design-details-balancing-demand-and-supply.md)  
[Designoplysninger: Reservation, ordresporing og aktionsmeddelelser](design-details-reservation-order-tracking-and-action-messaging.md)   
[Designoplysninger: Forsyningsplanlægning](design-details-supply-planning.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
