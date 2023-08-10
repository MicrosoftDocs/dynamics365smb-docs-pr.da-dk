---
title: Konfigurere og bruge Shopify Connector
description: Forskellige integrationsscenarier til påvisning af arbejdsgange mellem Shopify og Business Central
ms.date: 06/21/2022
ms.topic: article
ms.service: dynamics365-business-central
ms.search.form: '30101, 30102, 30106, 30107, 30113, 30115, 30126'
ms.reviewer: solsen
author: AndreiPanko
ms.author: andreipa
---

# <a name="walkthrough-set-up-and-use-the-shopify-connector"></a>Gennemgang: Konfigurere og bruge Shopify Connector

I dette afsnit beskrives nogle typiske scenarier, og du får gennemgang af de trin, du skal udføre for at teste eller uddanne brugere i den integrerede [!INCLUDE[prod_short](../includes/prod_short.md)] og Shopify-butikken.

## <a name="prerequisites"></a>Forudsætninger

### <a name="shopify"></a>Shopify

Du skal have:

- En Shopify-konto
- En Shopify-onlinebutik

Du kan finde flere oplysninger om, hvordan du opretter Shopify-forsøg og anbefalede indstillinger, ved at gå til [Oprette og konfigurere Shopify-konto](shopify-account.md).

### <a name="business-central"></a>Business Central

Du skal have en [!INCLUDE[prod_short](../includes/prod_short.md)]-konto. 

Du kan f. eks. oprette en demo konto eller starte prøveversionen. Flere oplysninger i [Forberede demonstrationsmiljøer af Dynamics 365 Business Central](/dynamics365/business-central/dev-itpro/administration/demo-environment) og [Tilmelde dig prøveversionen](../trial-signup.md). 

## <a name="connect-business-central-to-the-shopify-shop"></a>Forbinde Business central med Shopify-butikken

Gør ét af følgende i [!INCLUDE[prod_short](../includes/prod_short.md)]:

1. Vælg ![Lightbulb, der åbner funktionen Fortæl mig.](../media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **Shopify Shops**, og vælg derefter det relaterede link.
2. Vælg handlingen **Ny**.
3. Skriv `DEMO1` i feltet **Kode**.
4. Angiv den URL-adresse, du vil oprette forbindelse til, i feltet **Shopify URL**.
5. Slå til/fra-feltet **Aktiveret** til, gennemse og accepter vilkår og betingelser.

Konfigurer Shopify-butikken som beskrevet i følgende trin:

1. Aktivér **Logfil aktiveret**-feltet til/fra.
2. Deaktivér **Tillad baggrundssynkronisering** til/fra.
3. Vælg **Til Shopify** i feltet **Sync vare**.
4. Vælg **Til Shopify** i feltet **Sync varebilleder**.
5. Aktivér til/fra-knappen **Synkroniser vareattributter**.
6. Aktiver **Lager sporet** til/fra.
7. Vælg **Afvis** i feltet **Standardlagerpolitik**.
8. Aktiver **Automatisk oprettelse af ukendte kunder** til/fra.
9. Udfyld feltet **Debitorskabelonkode** med den relevante skabelon.
10. Udfyld feltet **Leveringskonto**, **Konto til drikkepenge** med omsætning. F. eks. kan du i USA bruge `40100`.
11. Aktiver **Automatisk oprettelse af ordrer** til/fra.

Konfigurere tilknytning af lokation:

1. Vælg handlingen **Lokationer** for at åbne **Shopify Butikslokationer**.
2. Vælg handlingen **Hent Shopify-lokationer** for at importere alle de placeringer, der er defineret i Shopify.
3. Angiv `''|EAST|MAIN` i **lokationsfilteret**.
4. Fjern markeringen fra til/fra-feltet **Deaktiveret** for at aktivere lagersynkronisering for udvalgt Shopify-lokation.

## <a name="walkthrough-start-selling-products-online"></a>Gennemgang: Start salg af produkter online

### <a name="scenario"></a>Scenarie

Lad os antage, at du vil prøve Shopify som onlinebutik uden at skulle bruge tid på at indstille tingene, især fordi du allerede har vedligeholdt dine varer i [!INCLUDE[prod_short](../includes/prod_short.md)]. Når du har startet din Shopify-onlinebutik, får du straks nye kunder, der er glade for din produktions- og købserfaring. Derfor beslutter de at efterlade drikkepenge ved kassen.

### <a name="steps"></a>Trin

Gennemgå følgende trin i [!INCLUDE[prod_short](../includes/prod_short.md)]:

1. Vælg ![Lightbulb, der åbner funktionen Fortæl mig.](../media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **Shopify Produkter**, og vælg det relevante link.
2. Vælg handlingen **Tilføj varer**.
3. Skriv *DEMO1* i feltet **Butikskode**.
4. Indstil filteret `CHAIR` i feltet **Varekategorikode** (tilføj filter, hvis det er nødvendigt).
5. Vælg **OK**, og vent, til den første synkronisering af varer og priser er fuldført.
6. Vælg handlingen **Synkroniser produktbilleder**.
7. Vælg handlingen **Synkroniser lager**.

I **Shopify-onlinebutik**
> [!Tip]  
> Åbn **Shopify-admin** ved at navigere til den URL-adresse, der er angivet i feltet **URL-adresse** på siden **Shopify-butikskort**. Derefter skal du vælge øjeikonet ud for salgskanalen **Onlinebutik** i sidepanelet for **Shopify-admin**. 

Åbn produktkataloget. Meddelelse:

* Produkttitler, billeder og priser.
* Disponeringsindikator (udsolgt for produkter, der ikke er på lager).

Vælg et produkt, der f. eks. kan sælges, f.eks. `BERLIN Swivel Chair, yellow`. Bemærk, at beskrivelsen indeholder vareattributter.

Vælg knappen **Køb nu**, og fortsæt til udtjekning.

1. I feltet **E-mail eller mobiltelefonnummer** skal du indtaste `cl@contoso.com` (eller e-mail, hvor du vil modtage ordre og levering).
2. I **Fornavn** og **Efternavn** skal du indtaste `Claudia Lawson`.
3. Angiv den lokale adresse.
4. Marker afkrydsningsfeltet **Gem disse oplysninger til næste gang** .
5. Vælg knappen **Fortsæt til levering**.
6. Bevar `Standard` leveringsmetoden, og vælg derefter **Fortsæt med betaling**.
7. Vælg `10%` drikkepenge.
8. I feltet **kreditkort** skal du angive `1`, hvis du bruger *(til test) Bogus gateway*, eller angive `5555 5555 5555 4444`, hvis du bruger *Shopify payments* i testtilstand.
9. Udfyld feltet **Navn på kort**.
10. Angiv i **Udløbsdato** indeværende måned/år.
11. Skriv `111` i **Sikkerhedskode**.
12. Vælg knappen **Betal nu**.

Gør ét af følgende i [!INCLUDE[prod_short](../includes/prod_short.md)]:

1. Vælg ![Lightbulb, der åbner funktionen Fortæl mig.](../media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **Shopify-ordrer**, og vælg derefter det relaterede link.
2. Vælg handlingen **Synkroniser ordrer fra Shopify**.
3. Vælg **OK**.

Den importerede ordre er klar til behandling.

1. Vælg den importerede ordre for at åbne **Shopify-ordre**-vinduet.
2. Bemærk, at der oprettes en ny kunde- og salgsordre.
3. Udforsk handlingerne **risiko** og **forsendelsesomkostning**.
4. Vælg handlingen **Salgsordre** for at åbne vinduet **Salgsordre**. Salgsordre kan, om nødvendigt, dækkes af montage, produktion eller køb ved hjælp af planlægningsprogrammet. Den understøtter også forskellige lagerekspeditionsprocesser med fuldstændig adskillelse af opgaver.
5. Vælg handlingen **Genåbne**.
6. I feltet **helpdesk-medarbejder** angives `DHL`.
7. I feltet **Pakkesporingsnr.** angives `123456789`.
8. Vælg handlingen **Bogfør**, vælg indstillingen **Lever og fakturer**, og vælg derefter knappen **OK**.

Nu registreres fysiske og økonomiske oplysninger i [!INCLUDE[prod_short](../includes/prod_short.md)]. Det er tid til at give besked til Shopify om ændringerne.

1. Vælg ![Lightbulb, der åbner funktionen Fortæl mig.](../media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **Synkronisere forsendelser til Shopify**, og vælg derefter det relaterede link.
2. Vælg **OK**.

I **Shopify Admin** skal du notere om, ordren nu er markeret som *opfyldt*. Du kan også gennemse leveringsoplysningerne og se, hvordan du registrerer URL-adressen. Hvis du kører **synkroniseringsordrer fra Shopify** igen, vil ordren blive arkiveret på begge systemer.

## <a name="walkthrough-invite-your-customers-to-your-new-online-store"></a>Gennemgang: Inviter dine kunder til din nye onlinebutik

### <a name="scenario-1"></a>Scenarie

Når du hurtigt har startet din nye onlinebutik, vil du have de aktuelle kunder til at besøge og begynde at bestille.

### <a name="steps-1"></a>Trin

Gør ét af følgende i [!INCLUDE[prod_short](../includes/prod_short.md)]:

1. Vælg ![Lightbulb, der åbner funktionen Fortæl mig.](../media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **Shopify-butikker**, og vælg det relevante link.
2. Marker den **DEMO1**-butik, som du vil synkronisere debitorer til for at åbne **Shopify-butikskort**-siden.
3. Vælg handlingen **Synkroniser debitorer**.

I **Shopify Admin** skal du registrere, om kunderne er blevet indlæst. Åbn en af debitorerne, og læg mærke til, at det første og sidste navn på debitoren kommer fra i feltet **kontaktnavn** på **debitorkortet**. Firmanavnet kan findes i den standardadresse, der er knyttet til debitoren. Vælg **Send kontoinvitationen** for at invitere debitoren.

## <a name="walkthrough-fine-tuning-of-item-management"></a>Gennemgang: Finjustering af varestyring

### <a name="scenario-2"></a>Scenarie

Du vil gerne give processerne større fleksibilitet og styring i forbindelse med håndtering af emner. Du vil forbedre produktbeskrivelsen og gerne tilføje flere gennemsynstrin, før produkterne bliver tilgængelige for kunden.

### <a name="steps-2"></a>Trin

Gør ét af følgende i [!INCLUDE[prod_short](../includes/prod_short.md)]:

Klargøre data

1. Vælg ![Lightbulb, der åbner funktionen Fortæl mig.](../media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **Debitorprisgruppe**, og vælg derefter det relaterede link.
2. Tilføj ny prisgruppe. Skriv `SHOPIFY` i feltet **Kode**.
3. Luk vinduet **Debitorprisgrupper**.
4. Vælg ![Lightbulb, der åbner funktionen Fortæl mig.](../media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **Varer**, og vælg det relaterede link.

Vælg vare **1896-S, Athens Desk**, og kør følgende trin.

1. Vælg handlingen **Varianter**, og tilføj derefter to varianter `PREMIUM, Athens Desk, Premium edition` og `ESSENTIAL, Athens Desk, Essential edition`.
2. Vælg **Udvidet tekst**, opret en ny udvidet tekst, der gælder for alle sprogkoder. Angiv `Shopify` i feltet **Beskrivelse**. 
3. Tilføj følgende tekst med HTML-koder: `<b>Simple stylish design</b> blends with any ensemble. <i>Available in two editions.</i>`.
4. Vælg **salgspriser**, og tilføj nye priser som vist i følgende tabel:

  |Linje|**Salgstype**|**Salgskode**|Enhedstype|Kode|Variantkode<br>(tilføj feltet via brugertilpasning)|Enhedspris|
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

6. Vælg **varereferencer** og følgende linjer:

  |Linje|**Referencetype**|**Referencenr.**|Variantkode|
  |------|------------|------------|------------|
  |1|Stregkode|77777777|ESSENTIAL|
  |2|Stregkode|11111111|PREMIUM|


Vælg varen **1920-S, ANTWERP Conference Table**, og udfør følgende trin.

1. Vælg **Juster lager**, og angiv `100` for lokationerne **ØST** og *VEST* i feltet *Nyt lager*. 
2. Vælg **OK**.

Juster indstillinger til synkronisering.

1. Vælg ![Lightbulb, der åbner funktionen Fortæl mig.](../media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **Shopify-butikker**, og vælg det relevante link.
2. Marker den *DEMO1*-butik, som du vil synkronisere varer til for at åbne siden Shopify-købskort.
3. Vælg *SHOPIFY* i feltet **Debitorprisgruppe** .
4. Vælg *DETAIL* i feltet **Debitorrabatgruppe** .
5. Aktiver feltet til **udvidet tekst for synkroniseringselement**.
6. Klik på *Varenr. + variantkode* i feltet **SKU-tilknytning**.
7. Vælg *Kladde* i feltet **status for oprettede produkter** .
8. Vælg *status til arkiveret* i feltet **Handling for fjernet produkt** .

Kør varesynkronisering.

1. Vælg ![Lightbulb, der åbner funktionen Fortæl mig.](../media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **Shopify-butikker**, og vælg det relevante link.
2. Marker den *DEMO1*-butik, som du vil synkronisere varer til for at åbne siden **Shopify-købskort**.
3. Vælg handlingen **Produkter** for at åbne vinduet **Shopify-produkter**.
4. Vælg handlingen **Tilføj varer**.
5. Angiv filteret *TABEL* i feltet **Varekategorikode** .
6. Vælg handlingen **Synkroniser produktbilleder**.
7. Vælg handlingen **Synkroniser lager**.

Produkter tilføjes. Bemærk, at statussen er angivet til *Kladde*, og at varerne ikke kan ses i Shopify-onlinebutikken.

1. Vælg linjen med vare *1920-S, ANTWERP Conference Table*. I **SEO-titel** skal du skrive `Rectangular meeting table Antwerp, 10 seats, black`.
2. Vælg *Aktiv* i feltet **Status**.
3. Marker linjen med vare *1906-S, ATHENS, Mobile Pedestal*, og vælg derefter **Slet**-handlingen.

I **Shopify Admin** skal du bemærke, om alle produkter har forskellige statusser.

* *ANTWERP Conference Table* er *Aktiv*, fordi vi har ændret status i vinduet **Shopify-produkt**.
* *ATHENS Desk* er *kladde*, fordi vi har konfigureret standardstatus for alle tilføjede produkter til *Kladde*.
* *ATHENS Mobile Pedestal* er *arkiveret*, fordi vi har konfigureret, at der automatisk tildeles status som *arkiveret* for slettede produkter.

Bemærk, at lager for ANTWERP Conference Table er 100, fordi vi har konfigureret systemet til kun at bruge lager fra to lokationer HOVED og ØST. Lager på andre lokationer (VEST) ignoreres.

* Åbn *ANTWERP Conference Table*, bemærk felterne **brugerdefineret type**, **Kreditor**, **vægt**, **Kostpris pr. vare** og sektionen **Søgemaskineliste, forhåndsversion**.
* Åbn *Athens Desk*, rul ned til sektionen **Varianter**, og læg mærke til, hvordan **SKU** er udfyldt.
* Klik på **Rediger** for at gennemgå stregkode og priser.
* Skift status for *Athens Desk* til *Aktiv*, og vælg **Forhåndsversion**-handling.

I **Shopify-onlinebutik** skal du åbne produktkataloget og finde *ATHENS Desk*-produktet. Bemærk, at der er forskellige muligheder tilgængelige. Priserne er forskellige for forskellige indstillinger. Vær opmærksom på oplysninger om rabat.

## <a name="walkthrough-import-items-from-shopify"></a>Gennemgang: Indlæs varer fra Shopify

### <a name="scenario-3"></a>Scenarie

Du har allerede en onlinebutik med succes og vil gerne bruge [!INCLUDE[prod_short](../includes/prod_short.md)] som software til erhvervsstyring. Du vil importere så mange data fra Shopify som muligt. 

### <a name="steps-3"></a>Trin

Dette er en fortsættelse af [gennemgang: Start salget af produkter online](walkthrough-setting-up-and-using-shopify.md#walkthrough-start-selling-products-online). Du kan også prøve med dine egne data, f.eks. Shopify-butik eller sandkasse.

Gør ét af følgende i [!INCLUDE[prod_short](../includes/prod_short.md)]:

#### <a name="prepare-data"></a>Klargøre data

1. Skift til en gratis 30-dages prøveversion uden eksempeldata. Du kan finde flere oplysninger i [Tilføje dine egne data til en tom prøveversion](/dynamics365/business-central/dev-itpro/administration/trials-subscriptions#add-your-own-data-to-an-empty-trial-company).
2. Vælg ![Lightbulb, der åbner funktionen Fortæl mig.](../media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **Shopify Shops**, og vælg derefter det relaterede link.
3. Vælg handlingen **Ny**.
4. Skriv `DEMO2` i feltet **Kode**.
5. Angiv den URL-adresse, du vil oprette forbindelse til, i feltet **Shopify URL**.
6. Slå til/fra-feltet **Aktiveret** til, gennemse og accepter vilkår og betingelser.

Konfigurer Shopify-butikken som beskrevet herunder i de følgende trin:

7. Aktivér **Logfil aktiveret** til/fra.
8. Deaktivér **Tillad baggrundssynkronisering** til/fra.
9. Vælg **Fra Shopify** i feltet **Sync vare**.
5. Aktiver **Automatisk oprettelse af ukendte varer** til/fra.
11. Udfyld feltet **Vareskabelonkode** med den relevante skabelon.
12. Vælg **Fra Shopify** i feltet **Sync varebilleder**.
13. Vælg **Alle debitorer** i **Debitorimport fra Shopify**.
14. Aktiver **Automatisk oprettelse af ukendte kunder** til/fra.
15. Udfyld feltet **Debitorskabelonkode** med den relevante skabelon.
16. Udfyld feltet **Konto til forsendelsesgebyr**, **Konto til drikkepenge** med omsætningen. F. eks. kan du i USA bruge `40100`.
17. Aktiver **Automatisk oprettelse af ordrer** til/fra.

#### <a name="run-the-synchronization"></a>Kør varesynkronisering

1. Vælg ![Lightbulb, der åbner funktionen Fortæl mig.](../media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **Shopify-butikker**, og vælg det relevante link.
2. Marker den *DEMO2*-butik, som du vil synkronisere data til for at åbne **Shopify Butikskort**-siden.
3. Vælg handlingen **Synkroniser produkter**.
4. Vælg handlingen **Synkroniser produktbilleder**.
5. Vælg handlingen **Synkroniser debitorer**.

### <a name="results"></a>Resultater

* Shopify-produkter importeres. Kontroller ved at vælge ![Lightbulb, der åbner funktionen Fortæl mig.](../media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **Shopify Produkter**, og vælg det relevante link.
* Elementer med billeder oprettes. Kontroller ved at vælge ![Lightbulb, der åbner funktionen Fortæl mig.](../media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **Vare**, og vælg det relaterede link.
* Shopify Debitorer importeres. Kontroller ved at vælge ![Lightbulb, der åbner funktionen Fortæl mig.](../media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **Shopify-kunder**, og vælg derefter det relaterede link.
* Debitorer oprettes. Kontroller ved at vælge ![Lightbulb, der åbner funktionen Fortæl mig.](../media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **Kunder**, og vælg derefter det relaterede link.


## <a name="see-also"></a>Se også

[Kom i gang med Shopify-connectoren](get-started.md)  
