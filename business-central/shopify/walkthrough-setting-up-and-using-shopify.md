---
title: Konfigurere og bruge Shopify Connector
description: Forskellige integrationsscenarier til påvisning af arbejdsgange mellem Shopify og Business Central
ms.date: 08/30/2024
ms.topic: article
ms.service: dynamics-365-business-central
ms.search.form: '30101, 30102, 30106, 30107, 30113, 30115, 30126, 30156, 30157'
ms.reviewer: bholtorf
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
3. Skriv **DEMO1** i feltet **Kode**.
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
8. Udfyld feltet **Debitor/Firmaskabelonkode** med den relevante skabelon.
9. Udfyld feltet **Leveringskonto**, **Konto til drikkepenge** med omsætning. I USA skal du f.eks. bruge **40210**.
10. Aktiver **Automatisk oprettelse af ordrer** til/fra.
11. Deaktivér **Automatisk frigivelse af salgsordrer**.

Konfigurere tilknytning af lokation:

1. Vælg handlingen **Lokationer** for at åbne **Shopify Butikslokationer**.
2. Vælg handlingen **Hent Shopify-lokationer** for at importere alle de placeringer, der er defineret i Shopify. Vælg post med Til/fra-knappen **Er primær** er valgt.
3. I lokationsfilteret **skal** du indtaste **''|ØST|VIGTIGSTE**.
4. Hvis du vil aktivere lagersynkronisering for en valgt Shopify lokation, skal du **i feltet Lagerberegning** vælge **Forventet disponibel balance til dags dato**.

## Gennemgang: Start salg af produkter online

### Scenarie

Lad os antage, at du vil prøve Shopify som onlinebutik uden at skulle bruge tid på indstilling, især fordi du allerede har vedligeholdt dine varer i [!INCLUDE[prod_short](../includes/prod_short.md)]. Når du har startet din Shopify-onlinebutik, får du straks nye kunder, der er glade for din produktions- og købserfaring. Derfor beslutter de at efterlade drikkepenge ved kassen.

### Trin

Følg disse trin i [!INCLUDE[prod_short](../includes/prod_short.md)]:

1. Vælg ![Lightbulb, der åbner funktionen Fortæl mig.](../media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **Shopify-produkter**, og vælg derefter det relaterede link.
2. Vælg **Tilføj elementer**.
3. Angiv **DEMO1**  i feltet **Produktionskode**.
4.  **I feltet Varekategorikode** skal du angive filteret **CHAIR.**
5. Aktivér til/fra-knappen **Synkroniser produktbilleder**.
6. Aktiver til/fra-knappen **Synkronisér lager**.
7. Vælg **OK**, og vent, indtil den første synkronisering af varer, priser, billeder og lagerbeholdning er fuldført.

I **Shopify-onlinebutik**:
> [!Tip]  
> Åbn **Shopify-admin** ved at navigere til den URL-adresse, der er angivet i feltet **URL-adresse** på siden **Shopify-butikskort**. Vælg øjeikonet ud for salgskanalen **Onlinebutik** i sidepanelet for **Shopify-admin**. 

Åbn produktkataloget. Meddelelse:

* Produkttitler, billeder og priser.
* Disponeringsindikator (udsolgt for produkter, der ikke er på lager).

Vælg ethvert produkt, der kan sælges. For eksempel BERLIN drejestol, **gul**. Bemærk, at beskrivelsen indeholder vareattributter.

Vælg **Køb nu**, og fortsæt til udtjekning.

1. I feltet **E-mail eller mobiltelefonnummer** skal du indtaste **cl@contoso.com**  (eller en e-mail-adresse, hvor du vil modtage ordre- og forsendelsesbekræftelser).
2. I felterne **Fornavn** og **Efternavn** skal du skrive **Claudia** og **Lawson**.
3. Angiv den lokale adresse.
4. Vælg afkrydsningsfeltet **Gem disse oplysninger til næste gang**.
6. Hold *Standard* som forsendelsesmetode.
8.  **I feltet Kredit kort nummer** skal du angive **1**, hvis du bruger **(til test) Bogus Gateway**, eller angive **5555 5555 5555 4444**, hvis du bruger **Shopify betalinger** i testtilstand.
9. Udfyld feltet **Navn på kort**.
10. Angiv i **Udløbsdato** indeværende måned/år.
11. Indtast 111 **i sikkerhedskoden.** **·**
12. Valgfrit: Vælg **10 %** tip.
13. Vælg **Betal nu**.

Gør ét af følgende i [!INCLUDE[prod_short](../includes/prod_short.md)]:

1. Vælg ![Lightbulb, der åbner funktionen Fortæl mig.](../media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **Shopify-ordrer**, og vælg derefter det relaterede link.
2. Vælg handlingen **Synkroniser ordrer fra Shopify**.
3. Vælg **OK**.

Den importerede ordre er klar til behandling.

1. Vælg den importerede ordre for at åbne **Shopify-ordre**-vinduet.
2. Bemærk, at der oprettes ny kunde- og salgsordrer.
3. Udforsk handlingerne **Risici** og **Forsendelsesomkostninger** .
4. Vælg **Salgsordre** for at åbne vinduet **Salgsordre**. Salgsordre kan, om nødvendigt, dækkes af montage, produktion eller køb ved hjælp af planlægningsprogrammet. Den understøtter også forskellige lagerekspeditionsprocesser med fuldstændig adskillelse af opgaver.
6. Indtast DHL **i** feltet **Agent**. Åbn ordren igen, hvis det er nødvendigt, ved at vælge handlingen **Åbn igen**.
7. I feltet **Pakkesporingsnr.** skal du indtaste **123456789**.
8. Vælg handlingen **Bogfør**, vælg indstillingen **Lever og fakturer**, og vælg derefter knappen **OK**.

Nu registreres fysiske og økonomiske oplysninger i [!INCLUDE[prod_short](../includes/prod_short.md)]. Det er tid til at give besked til Shopify om ændringerne.

1. Vælg ![Lightbulb, der åbner funktionen Fortæl mig.](../media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **Synkronisere forsendelser til Shopify**, og vælg derefter det relaterede link.
2. Vælg **OK**.

I **Shopify Admin** skal du notere om, ordren nu er markeret som *opfyldt*. Du kan også gennemse leveringsoplysningerne og se, hvordan du registrerer URL-adressen. Hvis du kører **synkroniseringsordrer fra Shopify** igen, vil ordren blive arkiveret på begge systemer.

## Gennemgang: Tilføj dine kunder til din nye onlinebutik

### Scenarie

Når du hurtigt har startet din nye onlinebutik, vil du have de aktuelle kunder til at besøge og begynde at bestille. Afhængigt af din Shopify plan og proces kan du prøve B2B- og DTC-flows.

### DTC Trin

I [!INCLUDE[prod_short](../includes/prod_short.md)] skal du gøre følgende:

1. Vælg ![Lightbulb, der åbner funktionen Fortæl mig.](../media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **Shopify-kunder**, og vælg derefter det relaterede link.
2. Vælg **Tilføj kunder**.
3. Angiv **DEMO1**  i feltet **Produktionskode**.
4. I feltet **Nummer** Skal du angive filteret **20000**.
5. Vælg **OK**, og vent, til den første synkronisering af kunder er fuldført.

I **Shopify Admin** skal du registrere, om kunderne er blevet indlæst. Åbn debitorerne, og læg mærke til, at det første og sidste navn på debitoren kommer fra i feltet **kontaktnavn** på **debitorkortet**. Firmanavnet kan findes i den standardadresse, der er knyttet til debitoren. Hvis du bruger **Classic-kundekonti**, kan du vælge **Send kontoinvitation** for at invitere kunden. Med **Nye kundekonti** kræves der ikke en adgangskode, for at kunderne kan logge på.  Shopify I stedet kan dine kunder logge ind ved hjælp af en engangs, 6-cifret bekræftelseskode, der sendes via e-mail. 

### B2B trin

[!INCLUDE [shopify-preview](../includes/shopify-preview.md)]

I [!INCLUDE[prod_short](../includes/prod_short.md)] skal du gøre følgende:

1. Vælg ![Lightbulb, der åbner funktionen Fortæl mig.](../media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **Shopify Virksomheder**, og vælg derefter det relaterede link.
2. Vælg **Tilføj virksomhed**.
3. Angiv DEMO1 **i feltet Produktionskode.**  **·**
4. Indstil filteret **30000** på **Nej.** .
5. Vælg **OK**, og vent, til den første synkronisering af kunder er fuldført.

Bemærk **Shopify , at både firmaet og kunden blev importeret i Administrator**. Åbn debitorerne, og bemærk, at firmafaktaboksen indeholder links til firmaet, lokationen og de tildelte tilladelser.
Hvis du vil invitere kunden, skal du vælge **[...]**  **i faktaboksen Virksomhed**, og vælg **derefter Send B2B-adgangsmail**.

## Gennemgang: Finjustering af varestyring

### Scenarie 

Du vil gerne give processerne større fleksibilitet og styring i forbindelse med håndtering af emner. Du vil forbedre produktbeskrivelser og tilføje flere gennemsynstrin, før produkterne bliver tilgængelige alle kunder.

### Trin

I [!INCLUDE[prod_short](../includes/prod_short.md)] skal du gøre følgende:

Klargøre data

1. Vælg ![Lightbulb, der åbner funktionen Fortæl mig.](../media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **Debitorprisgruppe**, og vælg det relaterede link.
2. Tilføj en ny prisgruppe. I feltet **Kode** skal du skrive **SHOPIFY.**
3. Luk vinduet **Debitorprisgrupper**.
4. Vælg ![Lightbulb, der åbner funktionen Fortæl mig.](../media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **Varer**, og vælg derefter det relaterede link.
5. Vælg vare **1896-S, Athen Desk**, og følg derefter disse trin:

6. Vælg handlingen **Varianter**, og tilføj derefter to varianter: **PREMIUM, Athens Desk, Premium Edition** og **ESSENTIAL, Athens Desk, Essential edition**.
7. Vælg handlingen **Marketingtekst**, og brug **Kladde med Copilot**  til at få en kreativ og engagerende tekst. Hvis forslag til marketingtekst ikke er aktiveret, skal du blot indtaste: "**Enkelt, stilfuldt design** passer ind i ethvert ensemble. *Fås i to udgaver.*.
8. Vælg **salgspriser**, og tilføj nye priser som vist i følgende tabel:

   |Linje|Salgstype|Salgskode|Enhedstype|Kode|Variantkode<br>(tilføj feltet via brugertilpasning)|Enhedspris|
   |------|------------|------------|------------|----------------|------------|------------|
   |1|Debitorprisgruppe|SHOPIFY|Artikel|1896-S|ESSENTIAL|700|
   |2|Debitorprisgruppe|SHOPIFY|Artikel|1896-S|PREMIUM|1000|

9. Vælg **salgsrabatter**, og tilføj en ny rabat:

   * **Salgstype** *Debitorrabatgruppe*
   * **Salgskode** *DETAIL*
   * **Type** *Vare*
   * **Kode** *1896-S*
   * **Enhedskode** *PCS*
   * **Linjerabat %** *10*

10. Vælg handlingen **Varereferencer**, og tilføj følgende linjer:

   |Linje|Referencetype|Referencenr.|Variantkode|
   |------|------------|------------|------------|
   |1|Stregkode|77777777|ESSENTIAL|
   |2|Stregkode|11111111|PREMIUM|

11. Vælg varen **1920-S, ANTWERP Conference Table**, og udfør følgende trin.
12. Vælg **Reguler lagerbeholdning**, **og indtast** 100 **i feltet Ny lagerbeholdning** for lokationerne **ØST** og **VEST**.
13. Vælg **OK**.

Juster indstillinger til synkronisering.

1. Vælg ![Lightbulb, der åbner funktionen Fortæl mig.](../media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **Shopify-butikker**, og vælg det relevante link.
2. Vælg den DEMO1-butik **·**, du vil synkronisere varer for, for at åbne **Shopify siden Shop kort** .
3. Aktiver feltet **Synkronisér marketingtekst**.
4.  **Vælg** Varenr.+ Variantkode i feltet tilknytning **lagervare.**
5. I feltet **Standardlagerpolitik** skal du vælge **Fortsæt**.
6. I feltet **Status for oprettede produkter** skal du vælge **Kladde**.
7. I feltet **Handling for fjernet produkt** skal du vælge **Status til arkiveret**.
8. Vælg SHOPIFY i feltet **Debitorprisgruppe**  **.**
9. I feltet **Debitorrabatgruppe** skal du vælge **DETAIL.**

Kør varesynkronisering.

1. Vælg ![Lightbulb, der åbner funktionen Fortæl mig.](../media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **Shopify-butikker**, og vælg det relevante link.
2. Vælg den DEMO1-butik **·**, du vil synkronisere varer for, for at åbne **Shopify siden Shop kort** .
3. Vælg **Produkter** for at åbne siden **Shopify Produkter** .
4. Vælg handlingen **Tilføj varer**.
5. Indstil filteret **TABEL|DESK** i feltet **Varekategorikode** .
6. Aktivér til/fra-knappen **Synkroniser produktbilleder**.
7. Aktiver til/fra-knappen **Synkronisér lager**.
8. Vælg **OK**, og vent, indtil den første synkronisering af varer, priser, billeder og lagerbeholdning er fuldført.

Produkter tilføjes. Bemærk, at status er angivet til **Kladde**, og at varerne derfor ikke er synlige i webshoppen Shopify .

1. Vælg linjen med punkt **1920-S, ANTWERPEN Conference Table**.  **I SEO-titlen** skal du indtaste **rektangulært mødebord Antwerpen, 10 pladser, sort**.
2. Vælg Aktiv i **feltet Status**  **.**
3. Vælg linjen med vare **1906-S, ATHENS, Mobil piedestal**, og vælg **derefter Slet**.

I **Shopify Admin** skal du bemærke, om alle produkter har forskellige statusser.

* *ANTWERP Conference Table* er *aktiv*, **Shopify fordi vi har ændret dens status på produktsiden** .
* *ATHENS Desk* er *kladde*, fordi vi har konfigureret standardstatus for alle tilføjede produkter til *Kladde*.
* *ATHENS Mobile Pedestal* er *arkiveret*, fordi vi har konfigureret, at der automatisk tildeles status som *arkiveret* for slettede produkter.

Bemærk, at lagerbeholdningen for ANTWERP Conference Table er 100, fordi vi konfigurerede systemet til kun at bruge lagerbeholdning fra to lokationer, MAIN og EAST. Lager på en anden lokation (VEST) ignoreres.

* Åbn *ANTWERP Conference Table*, bemærk felterne **Brugerdefineret type**, **Kreditor**, **Vægt** og **Kostpris pr. vare** og sektionen **Søgemaskineliste, forhåndsversion**.
* Åbn *Athens Desk*, rul ned til sektionen **Varianter**, og læg mærke til, hvordan **SKU** er udfyldt.
* Hvis du vil gennemse stregkoder og priser, skal du vælge **Rediger**.
* Skift status for **Athens Desk** til **Aktiv**, og vælg **forhåndsversion**.

 Shopify I onlinebutikken skal du åbne produktkataloget og finde ATHENS Desk-produktet **·** . Bemærk, at der er forskellige muligheder tilgængelige. Priserne er forskellige for forskellige indstillinger. Vær opmærksom på oplysninger om rabat.

### Yderligere trin til B2B

[!INCLUDE [shopify-preview](../includes/shopify-preview.md)]

Du kan konfigurere connectoren til automatisk at oprette og tildele katalog til eksporterede virksomheder. Nedenstående trin er nyttige, hvis du vil have mere præcis kontrol over, hvad der er tilgængeligt for B2B-kunder.

Opret og tildel et katalog i **Shopify Administrator**.

1. Vælg **Produkter** og derefter **Kataloger** i sidebjælken i **Shopify admin**.
2. Opret et katalog til specifikke produkter. Giv det titlen 'B2B'. 
3. Vælg Administrer **og derefter** Administrer **produkter og priser**.
4. Vælg filteret **Ekskluderet**, find **ATHEN Desk**, og vælg **Medtag i katalog**.
5. Vælg **Kunder** og derefter **Virksomheder** i sidebjælken i **Shopify admin**.
6. Vælg **School of Fine Art**, vælg **[...]**, og derefter **Tilføj kataloger**, og tilføj det B2B-katalog **, der** blev oprettet tidligere.

I [!INCLUDE[prod_short](../includes/prod_short.md)] skal du gøre følgende:

Klargøre data

1. Vælg ![Lightbulb, der åbner funktionen Fortæl mig.](../media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **Varer**, og vælg derefter det relaterede link.
2. Vælg vare **1896-S, Athen Desk**, og følg derefter disse trin:
3. Vælg **salgsrabatter**, og tilføj en ny rabat:

   * **Salgstype** *Debitorrabatgruppe*
   * **Salgskode** *LARGE ACC*
   * **Type** *Vare*
   * **Kode** *1896-S*
   * **Enhedskode** *PCS*
   * **Linjerabat %** *25*

4. Vælg ![Lightbulb, der åbner funktionen Fortæl mig.](../media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **Shopify-kataloger**, og vælg derefter det relaterede link.
5. Vælg **Hent kataloger**.
6. Angiv **DEMO1**  i feltet **Produktionskode**.
7. Vælg posten med det B2B-katalog *·*, du vil synkronisere priser for.
8. Aktivér til/fra-knappen **Synkroniser priser**.
9. Vælg SHOPIFY i feltet **Debitorprisgruppe**  **.**
10. I feltet **Debitorrabatgruppe** skal du vælge **STOR ACC**.
11. Vælg **Synkronisér priser**, og vent, til den første synkronisering af varer og priser er fuldført.

Udforsk priserne for B2B-kataloget **Shopify** i **Administrator** .

I **Shopify-onlinebutik** skal du åbne produktkataloget og finde *ATHENS Desk*-produktet. Bemærk pris- og rabatoplysningerne.

## Gennemgang: Synkronisering af udtjekning og bestilling for den enkelte indkøber og virksomhedsrepræsentant

Dette er en fortsættelse af [gennemgang: Start salget af produkter online](walkthrough-setting-up-and-using-shopify.md#walkthrough-start-selling-products-online). Du kan også prøve med dine egne data, f.eks. ved hjælp af din Shopify butik eller sandkasse.

Individuel køber

1. I **Shopify-onlinebutik**. Vælg ikonet **Konto**-ikon. Aktivér den e-mail, du har adgang til.
2. Log ind ved hjælp af en engangs 6-cifret bekræftelseskode sendt via e-mail, du indtastede.
3. Udforsk produktkataloget, så skal du kunne se alle produkter med detailpriser.
4. Vælg Essential-variant, vælg **Køb den nu**, og fortsæt til kassen.
5. Udfyld felterne **Fornavn** og **Efternavn**.
6. Angiv den lokale adresse.
7. Hold *Standard* som forsendelsesmetode.
8.  **I feltet Kredit kort nummer** skal du indtaste **1**, hvis du bruger **(til test) Bogus Gateway**, eller indtaste **5555 5555 5555 4444**, hvis du bruger **Shopify betalinger** i testtilstand.
9. Angiv i **Udløbsdato** indeværende måned/år.
10. Indtast 111 **i sikkerhedskoden.** **·**
11. Udfyld feltet **Navn på kort**.
12. Vælg **Betal nu**.

Virksomhedsrepræsentant

[!INCLUDE [shopify-preview](../includes/shopify-preview.md)]

1. I **Shopify Administrator**.
2. Vælg **Debitorer** og derefter **Virksomheder** i sidebjælken i **Shopify admin**.
3. åbn posten *School of Fine Art*.
4. Vælg **[...]**  **i faktaboksen Kunstskole**, rediger **betalingsbetingelser**, og vælg **derefter Forfalder på opfyldelse**.
5. Vælg **[...]**  **i faktaboksen Kunder**, derefter **Tilføj kunde**, og tilføj derefter faktaboksen med den mail, du brugte til at logge på butikken tidligere.
6. I **Shopify-onlinebutik**. Vælg ikonet **Konto**-ikon. Aktivér den e-mail, du har adgang til.
7. Log ind ved hjælp af en engangs 6-cifret bekræftelseskode sendt via e-mail, du indtastede.
8. Udforsk produktkataloget, bør du kun kunne se produkter, der er føjet til B2B-kataloget med specialpriser i detailhandlen.
9. Vælg den vigtige variant, vælg **Køb den nu**, og fortsæt til kassen.
10. Bemærk, at konto, Send til og betalingsmetode er udfyldt.
11. Udfyld feltet **PO-nummer** med **PO-12345**.
12. Vælg **Send ordre**.

Gør ét af følgende i [!INCLUDE[prod_short](../includes/prod_short.md)]:

1. Vælg ![Lightbulb, der åbner funktionen Fortæl mig.](../media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **Shopify-ordrer**, og vælg derefter det relaterede link.
2. Vælg handlingen **Synkroniser ordrer fra Shopify**.
3. Vælg **OK**.

Den importerede ordre er klar til behandling.

1. Vælg den importerede ordre for at åbne siden **Shopify Ordre** .
2. Bemærk, at begge ordrer blev sendt af samme person, de er knyttet til to forskellige kunder.
3. I den ordre, der er afgivet på virksomhedens vegne, kan du se værdien i **feltet Købsordrenr** ., som også overføres til feltet Eksternt bilagsnr **.** for det oprettede salgsdokument.
4. Da vi konfigurerede B2B-virksomheden til at håndtere betalinger uden for Shopify, er den **økonomiske status** angivet til **Afventende**. Når du har modtaget betalingen, skal du vælge handlingen **Markér som betalt** . Den økonomiske status opdateres i Shopify.

## Gennemgang: Indlæs varer, debitorer, virksomheder fra Shopify

### Scenarie 

Du har allerede en onlinebutik med succes og vil gerne bruge [!INCLUDE[prod_short](../includes/prod_short.md)] som software til erhvervsstyring. Du vil importere så mange data fra Shopify som muligt.

### Trin

Dette er en fortsættelse af [Gennemgang: Begynd at sælge produkter online](walkthrough-setting-up-and-using-shopify.md#walkthrough-start-selling-products-online) og [Gennemgang: Føj dine kunder til din nye webshop](walkthrough-setting-up-and-using-shopify.md#walkthrough-add-your-customers-to-your-new-online-store). Du kan også prøve med dine egne data, f.eks. ved hjælp af din Shopify butik eller sandkasse.

I [!INCLUDE[prod_short](../includes/prod_short.md)] skal du følge nedenstående trin.

#### Klargøre data

1. Skift til en gratis 30-dages prøveversion uden eksempeldata. Du kan finde flere oplysninger i [Tilføje dine egne data til en tom prøveversion](/dynamics365/business-central/dev-itpro/administration/trials-subscriptions#add-your-own-data-to-an-empty-trial-company).
2. Vælg ![Lightbulb, der åbner funktionen Fortæl mig.](../media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **Shopify-Shops**, og vælg derefter det relaterede link.
3. Vælg **Ny**.
4. Skriv **DEMO2** i feltet **Kode**.
5. Angiv den URL-adresse, du vil oprette forbindelse til, i feltet **Shopify URL**.
6. Slå til/fra-feltet **Aktiveret** til, gennemse og accepter vilkår og betingelser.

Konfigurer Shopify butikken som beskrevet her:

1. Deaktivér **Tillad baggrundssynkronisering** til/fra.
2. I feltet **Synkroniser element** skal du vælge **Fra Shopify**.
3. Aktivér til/fra-knappen **Opret automatisk ukendte elementer** .
4. Udfyld feltet **Vareskabelonkode** med den relevante skabelon.
5. I feltet **Synkroniser varebilleder** skal du vælge **Fra Shopify**.
6.  **Vælg** Varenr.+ Variantkode i feltet tilknytning **lagervare.**
7. I **feltet Debitorimport fra Shopify** skal du vælge **Alle debitorer**.
8. Aktiver **Automatisk oprettelse af ukendte kunder** til/fra.
9. Udfyld feltet **Debitor/Firmaskabelonkode** med den relevante skabelon.
10. I feltet **Firmaimport fra Shopify** skal du vælge **Alle debitorer**.
11. Slå til/fra-knappen **Opret ukendt firma** automatisk.

#### Kør varesynkronisering

1. Vælg ![Lightbulb, der åbner funktionen Fortæl mig.](../media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **Shopify-butikker**, og vælg det relevante link.
2. Marker den *DEMO2*-butik, som du vil synkronisere data til for at åbne **Shopify Butikskort**-siden.
3. Vælg **Synkroniser produkter**.
4. Vælg **Synkroniser produktbilleder**.
5. Vælg **Synkroniser kunder**.
6. Vælg **Synkroniser kunder**

### Resultater

* Shopify-produkter importeres. Kontroller ved at vælge ![Lightbulb, der åbner funktionen Fortæl mig.](../media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **Shopify-produkter**, og vælg derefter det relaterede link.
* Elementer med billeder oprettes. Kontroller ved at vælge ![Lightbulb, der åbner funktionen Fortæl mig.](../media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **Vare**, og vælg derefter det relaterede link.
* Shopify Kunderne importeres. Kontroller ved at vælge ![Lightbulb, der åbner funktionen Fortæl mig.](../media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **Shopify-kunder**, og vælg derefter det relaterede link.
* Shopify virksomheder importeres. Kontroller ved at vælge ![Lightbulb, der åbner funktionen Fortæl mig.](../media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **Shopify Virksomheder**, og vælg derefter det relaterede link.
* Debitorer oprettes. Kontroller ved at vælge ![Lightbulb, der åbner funktionen Fortæl mig.](../media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **Kunder**, og vælg derefter det relaterede link.

## Se også

[Kom i gang med Shopify-connectoren](get-started.md)  
