---
title: Konfigurere og bruge Shopify Connector
description: Forskellige integrationsscenarier til påvisning af arbejdsgange mellem Shopify og Business Central
ms.date: 06/21/2022
ms.topic: article
ms.service: dynamics-365-business-central
ms.search.form: '30101, 30102, 30106, 30107, 30113, 30115, 30126'
ms.reviewer: solsen
author: brentholtorf
ms.author: bholtorf
---

# Gennemgang: Konfigurere og bruge Shopify Connector

I dette afsnit beskrives nogle typiske scenarier, og du får gennemgang af de trin, du skal udføre for at teste eller uddanne brugere i den integrerede [!INCLUDE[prod_short](../includes/prod_short.md)] og Shopify-butikken.

## Forudsætninger 

### Shopify

Du skal have:

- En Shopify-konto
- En Shopify-onlinebutik

Du kan finde flere oplysninger om, hvordan du opretter Shopify-prøveversioner og anbefalede indstillinger på [Opret og konfigurer Shopify-konto](shopify-account.md).

### Business Central

Du skal have en [!INCLUDE[prod_short](../includes/prod_short.md)]-konto. 

Du kan f. eks. oprette en demokonto eller starte en prøveversion. Flere oplysninger i [Forberede demonstrationsmiljøer af Dynamics 365 Business Central](/dynamics365/business-central/dev-itpro/administration/demo-environment) og [Tilmelde dig prøveversionen](../trial-signup.md). 

## Forbinde Business central med Shopify-butikken

I [!INCLUDE[prod_short](../includes/prod_short.md)] skal du gøre følgende:

1. Vælg ![Lightbulb, der åbner funktionen Fortæl mig.](../media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **Shopify-Shops**, og vælg derefter det relaterede link.
2. Vælg handlingen **Ny**.
3. Skriv `DEMO1` i feltet **Kode**.
4. Angiv URL-adressen for den online-shop, du vil oprette forbindelse til, i feltet **Shopify URL**.
5. Slå til/fra-feltet **Aktiveret** til, gennemse og accepter vilkår og betingelser.

Benyt følgende fremgangsmåde for at konfigurere Shopify-shops:

1. Deaktivér **Tillad baggrundssynkronisering** til/fra.
2. Vælg *Til Shopify* i feltet **Sync vare**.
3. Vælg *Til Shopify* i feltet **Sync varebilleder**.
4. Aktivér til/fra-knappen **Synkroniser vareattributter**.
5. Aktiver **Lager sporet** til/fra.
6. Vælg *Afvis* i feltet **Standardlagerpolitik**.
7. Aktiver **Automatisk oprettelse af ukendte kunder** til/fra.
8. Udfyld feltet **Debitorskabelonkode** med den relevante skabelon.
9. Udfyld feltet **Leveringskonto**, **Konto til drikkepenge** med omsætning. F. eks. kan du i USA bruge `40210`.
10. Aktiver **Automatisk oprettelse af ordrer** til/fra.

Konfigurere tilknytning af lokation:

1. Vælg handlingen **Lokationer** for at åbne **Shopify Butikslokationer**.
2. Vælg handlingen **Hent Shopify-lokationer** for at importere alle de placeringer, der er defineret i Shopify. Vælg din standardplacering i Shopify.
3. Angiv `''|EAST|MAIN` i **lokationsfilteret**.
4. Slå til/fra-knappen **Standardproduktplacering** til.
5. Vælg *Forventet disponibel saldo ved dags dato* i feltet **Lagerberegning** for at aktivere en lagersynkronisering for en valgt Shopify-lokation.

## Gennemgang: Start salg af produkter online

### Scenarie

Lad os antage, at du vil prøve Shopify som onlinebutik uden at skulle bruge tid på indstilling, især fordi du allerede har vedligeholdt dine varer i [!INCLUDE[prod_short](../includes/prod_short.md)]. Når du har startet din Shopify-onlinebutik, får du straks nye kunder, der er glade for din produktions- og købserfaring. Derfor beslutter de at efterlade drikkepenge ved kassen.

### Trin

Følg disse trin i [!INCLUDE[prod_short](../includes/prod_short.md)]:

1. Vælg ![Lightbulb, der åbner funktionen Fortæl mig.](../media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **Shopify-produkter**, og vælg derefter det relaterede link.
2. Vælg **Tilføj elementer**.
3. Skriv *DEMO1* i feltet **Butikskode**.
4. Indstil filteret `CHAIR` i feltet **Varekategorikode** (tilføj filter, hvis det er nødvendigt).
5. Vælg **OK**, og vent, til den første synkronisering af varer og priser er fuldført.
6. Vælg **Synkroniser produktbilleder**.
7. Vælg **Synkroniser lager**.

I **Shopify-onlinebutik**:
> [!Tip]  
> Åbn **Shopify-admin** ved at navigere til den URL-adresse, der er angivet i feltet **URL-adresse** på siden **Shopify-butikskort**. Vælg øjeikonet ud for salgskanalen **Onlinebutik** i sidepanelet for **Shopify-admin**. 

Åbn produktkataloget. Meddelelse:

* Produkttitler, billeder og priser.
* Disponeringsindikator (udsolgt for produkter, der ikke er på lager).

Vælg et produkt, der f. eks. kan sælges, f.eks. `BERLIN Swivel Chair, yellow`. Bemærk, at beskrivelsen indeholder vareattributter.

Vælg **Køb nu**, og fortsæt til udtjekning.

1. I feltet **E-mail eller mobiltelefonnummer** skal du indtaste `cl@contoso.com` (eller e-mail, hvor du vil modtage ordre og levering).
2. I felterne **Fornavn** og **Efternavn** skal du indtaste `Claudia Lawson`.
3. Angiv den lokale adresse.
4. Vælg afkrydsningsfeltet **Gem disse oplysninger til næste gang**.
5. Vælg **Fortsæt til levering**.
6. Bevar `Standard` som leveringsmetoden, og vælg derefter **Fortsæt med betaling**.
7. Vælg `10%` drikkepenge.
8. I feltet **kreditkort** skal du angive `1`, hvis du bruger *(til test) Bogus gateway*, eller angive `5555 5555 5555 4444`, hvis du bruger *Shopify payments* i testtilstand.
9. Udfyld feltet **Navn på kort**.
10. Angiv i **Udløbsdato** indeværende måned/år.
11. Skriv `111` i **Sikkerhedskode**.
12. Vælg **Betal nu**.

Gør ét af følgende i [!INCLUDE[prod_short](../includes/prod_short.md)]:

1. Vælg ![Lightbulb, der åbner funktionen Fortæl mig.](../media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **Shopify-ordrer**, og vælg derefter det relaterede link.
2. Vælg handlingen **Synkroniser ordrer fra Shopify**.
3. Vælg **OK**.

Den importerede ordre er klar til behandling.

1. Vælg den importerede ordre for at åbne **Shopify-ordre**-vinduet.
2. Bemærk, at der oprettes ny kunde- og salgsordrer.
3. Udforsk handlingerne **risiko** og **forsendelsesomkostning**.
4. Vælg **Salgsordre** for at åbne vinduet **Salgsordre**. Salgsordre kan, om nødvendigt, dækkes af montage, produktion eller køb ved hjælp af planlægningsprogrammet. Den understøtter også forskellige lagerekspeditionsprocesser med fuldstændig adskillelse af opgaver.
5. Vælg handlingen **Genåbne**.
6. I feltet **helpdesk-medarbejder** angives `DHL`.
7. I feltet **Pakkesporingsnr.** angives `123456789`.
8. Vælg handlingen **Bogfør**, vælg indstillingen **Lever og fakturer**, og vælg derefter knappen **OK**.

Nu registreres fysiske og økonomiske oplysninger i [!INCLUDE[prod_short](../includes/prod_short.md)]. Det er tid til at give besked til Shopify om ændringerne.

1. Vælg ![Lightbulb, der åbner funktionen Fortæl mig.](../media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **Synkronisere forsendelser til Shopify**, og vælg derefter det relaterede link.
2. Vælg **OK**.

I **Shopify Admin** skal du notere om, ordren nu er markeret som *opfyldt*. Du kan også gennemse leveringsoplysningerne og se, hvordan du registrerer URL-adressen. Hvis du kører **synkroniseringsordrer fra Shopify** igen, vil ordren blive arkiveret på begge systemer.

## Gennemgang: Inviter dine kunder til din nye onlinebutik

### Scenarie

Når du hurtigt har startet din nye onlinebutik, vil du have de aktuelle kunder til at besøge og begynde at bestille.

### Trin

I [!INCLUDE[prod_short](../includes/prod_short.md)] skal du gøre følgende:

1. Vælg ![Lightbulb, der åbner funktionen Fortæl mig.](../media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **Shopify-butikker**, og vælg det relevante link.
2. Marker den **DEMO1**-butik, som du vil synkronisere debitorer til for at åbne **Shopify-butikskort**-siden.
3. Vælg **Synkroniser kunder**.

I **Shopify Admin** skal du registrere, om kunderne er blevet indlæst. Åbn en af debitorerne, og læg mærke til, at det første og sidste navn på debitoren kommer fra i feltet **kontaktnavn** på **debitorkortet**. Firmanavnet kan findes i den standardadresse, der er knyttet til debitoren. Vælg **Send kontoinvitationen** for at invitere debitoren.

## Gennemgang: Finjustering af varestyring

### Scenarie 

Du vil gerne give processerne større fleksibilitet og styring i forbindelse med håndtering af emner. Du vil forbedre produktbeskrivelser og tilføje flere gennemsynstrin, før produkterne bliver tilgængelige for kunderne.

### Trin

I [!INCLUDE[prod_short](../includes/prod_short.md)] skal du gøre følgende:

Klargøre data

1. Vælg ![Lightbulb, der åbner funktionen Fortæl mig.](../media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **Debitorprisgruppe**, og vælg det relaterede link.
2. Tilføj en ny prisgruppe. Skriv `SHOPIFY` i feltet **Kode**.
3. Luk vinduet **Debitorprisgrupper**.
4. Vælg ![Lightbulb, der åbner funktionen Fortæl mig.](../media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **Varer**, og vælg derefter det relaterede link.

Vælg vare **1896-S, Athens Desk**, og følg disse trin:

1. Vælg handlingen **Varianter**, og tilføj derefter to varianter: `PREMIUM, Athens Desk, Premium edition` og `ESSENTIAL, Athens Desk, Essential edition`.
2. Vælg **Udvidet tekst**, og opret en ny udvidet tekst, der gælder for alle sprogkoder. Angiv `Shopify` i feltet **Beskrivelse**. 
3. Tilføj følgende tekst med HTML-koder: `<b>Simple stylish design</b> blends with any ensemble. <i>Available in two editions.</i>`. Luk siden **Udvidet tekst**, og vend tilbage til varekortet.
4. Vælg **salgspriser**, og tilføj nye priser som vist i følgende tabel:

   |Linje|Salgstype|Salgskode|Enhedstype|Kode|Variantkode<br>(tilføj feltet via brugertilpasning)|Enhedspris|
   |------|------------|------------|------------|------------|------------|------------|
   |1|Debitorprisgruppe|SHOPIFY|Artikel|1896-S|ESSENTIAL|700|
   |2|Debitorprisgruppe|SHOPIFY|Artikel|1896-S|PREMIUM|1000|

5. Vælg **salgsrabatter**, og tilføj en ny rabat:

   * **Salgstype** *Debitorrabatgruppe*
   * **Salgskode** *DETAIL*
   * **Type** *Vare*
   * **Kode** *1896-S*
   * **Enhedskode** *PCS*
   * **Linjerabat %** *10*

6. Vælg **Varereferencer** og følgende linjer:

   |Linje|Referencetype|Referencenr.|Variantkode|
   |------|------------|------------|------------|
   |1|Stregkode|77777777|ESSENTIAL|
   |2|Stregkode|11111111|PREMIUM|


Vælg varen **1920-S, ANTWERP Conference Table**, og udfør følgende trin.

1. Vælg **Juster lager**, og angiv `100` for lokationerne **ØST** og *VEST* i feltet *Nyt lager*. 
2. Vælg **OK**.

Juster indstillinger til synkronisering.

1. Vælg ![Lightbulb, der åbner funktionen Fortæl mig.](../media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **Shopify-butikker**, og vælg det relevante link.
2. Marker den *DEMO1*-butik, som du vil synkronisere varer til for at åbne siden **Shopify-købskort**.
3. Vælg *SHOPIFY* i feltet **Debitorprisgruppe**.
4. Vælg *DETAIL* i feltet **Debitorrabatgruppe**.
5. Aktiver feltet til **udvidet tekst for synkroniseringselement**.
6. Klik på *Varenr. + variantkode* i feltet **SKU-tilknytning**.
7. Vælg *Kladde* i feltet **status for oprettede produkter**.
8. Vælg *status til arkiveret* i feltet **Handling for fjernet produkt**.

Kør varesynkronisering.

1. Vælg ![Lightbulb, der åbner funktionen Fortæl mig.](../media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **Shopify-butikker**, og vælg det relevante link.
2. Marker den *DEMO1*-butik, som du vil synkronisere varer til for at åbne siden **Shopify-købskort**.
3. Vælg **Produkter** for at åbne vinduet **Shopify-produkter**.
4. Vælg handlingen **Tilføj varer**.
5. Angiv filteret *TABEL|DESK* i feltet **Varekategorikode**.
6. Vælg **Synkroniser produktbilleder**.
7. Vælg **Synkroniser lager**.

Produkter tilføjes. Bemærk, at statussen er angivet til *Kladde*, og at varerne ikke kan ses i Shopify-onlinebutikken.

1. Vælg linjen med vare *1920-S, ANTWERP Conference Table*. I **SEO-titel** skal du skrive `Rectangular meeting table Antwerp, 10 seats, black`.
2. Vælg *Aktiv* i feltet **Status**.
3. Marker linjen med vare *1906-S, ATHENS, Mobile Pedestal*, og vælg derefter **Slet**.

I **Shopify Admin** skal du bemærke, om alle produkter har forskellige statusser.

* *ANTWERP Conference Table* er *Aktiv*, fordi vi har ændret status i vinduet **Shopify-produkt**.
* *ATHENS Desk* er *kladde*, fordi vi har konfigureret standardstatus for alle tilføjede produkter til *Kladde*.
* *ATHENS Mobile Pedestal* er *arkiveret*, fordi vi har konfigureret, at der automatisk tildeles status som *arkiveret* for slettede produkter.

Bemærk, at lager for ANTWERP Conference Table er 100, fordi vi har konfigureret systemet til kun at bruge lager fra to lokationer HOVED og ØST. Lager på en anden lokation (VEST) ignoreres.

* Åbn *ANTWERP Conference Table*, bemærk felterne **Brugerdefineret type**, **Kreditor**, **Vægt** og **Kostpris pr. vare** og sektionen **Søgemaskineliste, forhåndsversion**.
* Åbn *Athens Desk*, rul ned til sektionen **Varianter**, og læg mærke til, hvordan **SKU** er udfyldt.
* Vælg **Rediger** for at gennemgå stregkode og priser.
* Skift status for *Athens Desk* til *Aktiv*, og vælg **Forhåndsversion**.

I **Shopify-onlinebutik** skal du åbne produktkataloget og finde *ATHENS Desk*-produktet. Bemærk, at der er forskellige muligheder tilgængelige. Priserne er forskellige for forskellige indstillinger. Vær opmærksom på oplysninger om rabat.

## Gennemgang: Indlæs varer fra Shopify

### Scenarie 

Du har allerede en onlinebutik med succes og vil gerne bruge [!INCLUDE[prod_short](../includes/prod_short.md)] som software til erhvervsstyring. Du vil importere så mange data fra Shopify som muligt. 

### Trin

Dette er en fortsættelse af [gennemgang: Start salget af produkter online](walkthrough-setting-up-and-using-shopify.md#walkthrough-start-selling-products-online). Du kan også prøve med dine egne data, f.eks. Shopify-butik eller sandkasse.

I [!INCLUDE[prod_short](../includes/prod_short.md)] skal du følge nedenstående trin.

#### Klargøre data

1. Skift til en gratis 30-dages prøveversion uden eksempeldata. Du kan finde flere oplysninger i [Tilføje dine egne data til en tom prøveversion](/dynamics365/business-central/dev-itpro/administration/trials-subscriptions#add-your-own-data-to-an-empty-trial-company).
2. Vælg ![Lightbulb, der åbner funktionen Fortæl mig.](../media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **Shopify-Shops**, og vælg derefter det relaterede link.
3. Vælg **Ny**.
4. Skriv `DEMO2` i feltet **Kode**.
5. Angiv den URL-adresse, du vil oprette forbindelse til, i feltet **Shopify URL**.
6. Slå til/fra-feltet **Aktiveret** til, gennemse og accepter vilkår og betingelser.

Konfigurer Shopify butikken som beskrevet her:

1. Deaktivér **Tillad baggrundssynkronisering** til/fra.
1. Vælg *Fra Shopify* i feltet **Sync vare**.
1. Aktiver **Automatisk oprettelse af ukendte varer** til/fra.
1. Udfyld feltet **Vareskabelonkode** med den relevante skabelon.
1. Vælg *Fra Shopify* i feltet **Sync varebilleder**.
1. Vælg *Alle debitorer* i **Debitorimport fra Shopify**.
1. Aktiver **Automatisk oprettelse af ukendte kunder** til/fra.

#### Kør varesynkronisering

1. Vælg ![Lightbulb, der åbner funktionen Fortæl mig.](../media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **Shopify-butikker**, og vælg det relevante link.
2. Marker den *DEMO2*-butik, som du vil synkronisere data til for at åbne **Shopify Butikskort**-siden.
3. Vælg **Synkroniser produkter**.
4. Vælg **Synkroniser produktbilleder**.
5. Vælg **Synkroniser kunder**.

### Resultater

* Shopify-produkter importeres. Kontroller ved at vælge ![Lightbulb, der åbner funktionen Fortæl mig.](../media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **Shopify-produkter**, og vælg derefter det relaterede link.
* Elementer med billeder oprettes. Kontroller ved at vælge ![Lightbulb, der åbner funktionen Fortæl mig.](../media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **Vare**, og vælg derefter det relaterede link.
* Shopify Debitorer importeres. Kontroller ved at vælge ![Lightbulb, der åbner funktionen Fortæl mig.](../media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **Shopify-kunder**, og vælg derefter det relaterede link.
* Debitorer oprettes. Kontroller ved at vælge ![Lightbulb, der åbner funktionen Fortæl mig.](../media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **Kunder**, og vælg derefter det relaterede link.


## Se også

[Kom i gang med Shopify-connectoren](get-started.md)  
