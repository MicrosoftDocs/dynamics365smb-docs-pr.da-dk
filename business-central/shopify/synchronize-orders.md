---
title: Synkronisere og opfylde salgsordrer
description: Konfigurere og køre import og behandling af salgsordrer fra Shopify.
ms.date: 03/25/2024
ms.topic: article
ms.service: dynamics-365-business-central
ms.search.form: '30110, 30111, 30112, 30113, 30114, 30115, 30121, 30122, 30123, 30128, 30129, 30150, 30151, 30145, 30147'
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bholtorf
---

# Synkronisere og opfylde salgsordrer

I denne artikel beskrives de nødvendige indstillinger og trin, du skal fuldføre for at synkronisere og opfylde salgsordrer fra Shopify i [!INCLUDE[prod_short](../includes/prod_short.md)].

## Angive importen af ordrer på Shopify-butikskortet

Husk at angive en **Valutakode**, hvis din online-butik bruger en anden valuta end den relevante regnskabsvaluta. Der skal være konfigureret valutakurser for den angivne valuta. Hvis dit onlineindkøb bruger samme valuta som [!INCLUDE[prod_short](../includes/prod_short.md)], skal du lade feltet stå tomt. 

Du kan få adgang til lagervalutaen i [indstillingerne for butiksdetaljer](https://www.shopify.com/admin/settings/general) i din Shopify-administrator. Shopify kan konfigureres til at acceptere forskellige valutaer, men importerede ordrer til butiksvaluta. Importerede ordrer bruges i [!INCLUDE[prod_short](../includes/prod_short.md)] butiksvaluta.

En almindelig Shopify-ordre kan indeholder omkostninger ud over subtotalen, f. eks. forsendelsesgebyrer eller, hvis det er aktiveret, tip. Beløbene bogføres direkte på den finanskonto, der skal bruges til bestemte posteringstyper:

* **Konto til forsendelsesgebyr**
* **Solgt gavekortkonto** – du kan finde flere oplysninger i [Gavekort](synchronize-orders.md#gift-cards)
* **Tips til konto**  

Aktiver **Automatisk oprettelse af ordrer** for at oprette salgsdokumenter automatisk i [!INCLUDE[prod_short](../includes/prod_short.md)], når Shopify-ordren er importeret.

Hvis du automatisk vil frigive et salgsdokument, skal du aktivere funktionen **Frigiv salgsordrer automatisk**.

Hvis du ikke vil sende automatiske leveringsbekræftelser til kunder, skal du slå **Send leveringsbekræftelse** fra. Det kan være nyttigt at slå til/fra-knappen fra, hvis du sælger digitale varer eller vil bruge en anden meddelelsesmekanisme.

Hvis du vælger feltet **Shopify -ordrenr. på dokumentlinjen**, indsætter [!INCLUDE [prod_short](../includes/prod_short.md)] salgslinjer af typen **Bemærkning** med ordrenummeret Shopify.

> [!NOTE]
> Salgsdokumentet i [!INCLUDE[prod_short](../includes/prod_short.md)] linker til Shopify-ordren, og du kan tilføje **Shopify-ordrenr.** feltet til liste- eller kortsider for salgsordrer, fakturaer og leveringer. Hvis du vil vide mere om tilføjelse af et felt, skal du gå til [Start tilpasning ved hjælp af tilpasningstilstand](../ui-personalization-user.md#start-personalizing-by-using-the-personalization-mode). 

I feltet **Momsområdeprioritet** kan du prioriterer, hvordan du vil vælge skatteområdekode for adresser på ordrer. Den importerede Shopify-ordre viser oplysninger om moms. Momsen genberegnes, når du opretter salgsdokumenter, så det er vigtigt, at moms- eller skatteindstillingerne er korrekte i [!INCLUDE[prod_short](../includes/prod_short.md)]. Du kan finde flere oplysninger om moms i [Konfigurere moms for Shopify-forbindelsen](setup-taxes.md).

Angiv, hvordan returvarer og refusioner skal behandles:

* **Tom** angiver, at du ikke importerer og behandler returvarer og refusioner.
* **Kun import** angiver, at du importerer oplysninger, men du skal oprette den tilsvarende kreditnota manuelt.
* **Opret automatisk kreditnota** angiver, at du importerer oplysninger og [!INCLUDE[prod_short](../includes/prod_short.md)] opretter automatisk kreditnotaerne. Denne indstilling kræver, at du slår **Auto oprettelse af salgsordrer** til og fra.

Angive en lokation til returneringer og finanskonti til refusion af varer og andre refusioner.

* **Refusionskonto til ikke-genopfyldte varer** angiver et finanskontonr. for varer, hvor du ikke vil have en lagerrettelse.
* **Refusionskonto** angiver et finanskontonr. for differencen i feltet Total refunderet beløb og det samlede beløb for varerne.

Få mere at vide på [Returneringer og refusion](synchronize-orders.md#returns-and-refunds)

### Tilknytning af forsendelsesmetode

**Leveringskode** for salgsdokumenter, der er indlæst fra Shopify, kan udfyldes automatisk. Du skal konfigurere **tilknytning af leveringsmetode**.

1. Vælg ![Lightbulb, der åbner funktionen Fortæl mig 1.](../media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **Shopify Shops**, vælg derefter det relaterede link.
2. Marker den butik, som du vil definere en tilknytning til for at åbne **Shopify Butikskort**-siden.
3. Vælg handlingen **Tilknytning af forsendelsesmetode**. Posterne for forsendelsesmetoder, der er defineret i [**Forsendelse**](https://www.shopify.com/admin/settings/payments)-indstillingerne i din **Shopify Administrator**, oprettes automatisk.
4. I feltet **Navn** kan du se navnet på leveringsmåden fra Shopify.
5. Indtast **Forsendelsesmetodekoden** med den tilsvarende forsendelsesmetoide i [!INCLUDE[prod_short](../includes/prod_short.md)].

> [!NOTE]  
> Hvis der er knyttet flere forsendelsesgebyrer til en salgsordre. der er kun valgt én som forsendelsesmetode, der er knyttet til salgsdokumentet.

### Tilknytning af lokation

Lokationskoden er nødvendig for at udfylde **lokationskoden** for salgsdokumentlinjer, der er indlæst fra Shopify. Det er vigtigt, når til/fra-feltet **lokation, der er obligatorisk** er aktiveret på **lageropsætningskortet**. Ellers kan du ikke oprette salgsdokumenter.

1. Vælg ![Lightbulb, der åbner funktionen Fortæl mig 1.](../media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **Shopify Shops**, vælg derefter det relaterede link.
2. Marker den butik, for hvilken du vil konfigurere tilknytning af placering for at åbne siden **Shopify-butikskort**.
3. Vælg handlingen **Lokationer** for at åbne **Shopify Butikslokationer**.
4. Vælg handlingen **Hent Shopify Lokationer** for at importere alle de placeringer, der er defineret i Shopify. Du kan finde dem under [**Lokations**](https://www.shopify.com/admin/settings/locations)-indstillinger i **Shopify Administrator**. 
5. Angiv **standardplaceringskoden** med den tilsvarende lokation i [!INCLUDE[prod_short](../includes/prod_short.md)].

> [!NOTE]  
> Placeringskortlægning bruges også til at synkronisere lagerbeholdning. Hvis du vil vide mere, skal du gå til [Synkronisere lagervarer til Shopify](synchronize-items.md#sync-inventory-to-shopify).
  
## Kør ordresynkronisering

Nedenstående procedure beskriver, hvordan du imjporterer og opdaterer salgsordrer.

> [!NOTE]  
> Arkiverede ordrer i Shopify kan ikke importeres. Hvis du har brug for at kontrollere ordrestatussen, skal du åbne ordren fra [ordresiden i](https://www.shopify.com/admin/orders) adminpanelet **Shopify og gennemgå ordreoplysninger**.
> 
> Deaktiver **Automatisk arkivering af ordren** i sektionen **Ordrebehandling** under indstillingerne **Tjek ud** i **Shopify Administration** for at kontrollere, at alle ordrer er importeret til [!INCLUDE[prod_short](../includes/prod_short.md)]. Hvis du har brug for at importere arkiverede ordrer, skal du bruge handlingen **Ikke-arkiverede ordrer** på siden [Ordrer](https://www.shopify.com/admin/orders) til panelet **Shopify-Administration**. 

1. Vælg ![Lightbulb, der åbner funktionen Fortæl mig 1.](../media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **Shopify Shops**, vælg derefter det relaterede link.
2. Marker den butik, som du vil importere ordrer til for at åbne **Shopify Butikskort**-siden.
3. Vælg handlingen **Ordrer**.
4. Vælg handlingen **Synkroniser ordrer fra Shopify**.
5. Definer eventuelt filtre for ordrer. Du kan f. eks. indlæse ordrer, der er fuldt betalt, eller dem, der har lav risiko.

   > [!NOTE]  
   > Når du filtrerer efter kode, skal du bruge filtertoken `@` og `*`. Hvis du f. eks. vil importere ordrer, der indeholder *tag1*, skal du bruge `@*tag1*`. `@` sikrer, at resultatet ikke skelner mellem store og små bogstaver, mens `*` finder ordrer med flere koder.

6. Vælg knappen **OK**.

Du kan også søge efter **synkroniseringsordrer fra Shopify** batchjobbet.

Du kan planlægge, at opgaven skal udføres automatisk. Få mere at vide, når du [planlægger tilbagevendende opgaver](background.md#to-schedule-recurring-tasks).

### Under toppen

Shopify Connector importerer ordrer i to trin:

1. Den importerer ordrehoveder til **Shopify-ordrer, der skal importeres**, når de svarer til bestemte betingelser:

   * De arkiveres ikke. Det betyder, at du kan inkludere eller ekskludere ordrer fra synkronisering ved at arkivere eller fjerne arkiveringen af dem i Shopify-administratoren.
   * De blev oprettet eller ændret efter sidste synkronisering. Det betyder, at du kan gennemtvinge genimport af en bestemt ordre, hvis du ændrer den, f.eks. ved at tilføje **Noter** eller **Tag**.

2. Den indlæser Shopify-ordrer og supplerende oplysninger.

   * Shopify Connector behandler alle poster i tabellen **Shopify-ordrer, der skal importeres**, som opfylder de filterkriterier, du har defineret i **Synkroniser ordrer fra Shopify**-anmodningssiden. F.eks. tags, kanal eller opfyldelsesstatus. Hvis du ikke har angivet nogen filtre, behandler den alle poster.
   * Når der importeres en Shopify-ordre, anmoder Shopify Connector om yderligere oplysninger fra Shopify:

     * Ordrehoved
     * Ordrelinjer
     * Oplysninger om forsendelse og opfyldelse
     * Transaktioner
     * Returvarer og refusioner, hvis det er konfigureret

Siden **Shopify-ordre, der skal importeres**, er nyttig til fejlfinding af import ordrer. Du kan vurdere de ordrer, der er tilgængelige, og tage de næste trin:

* Undersøg, om en fejl har blokeret for importen af en bestemt ordre, og se nærmere oplysninger om fejlen. Se feltet **Indeholder fejl**.
* Behandl kun bestemte ordrer. Du skal udfylde feltet **Butikskode**, vælge en eller flere ordrer og derefter vælge handlingen **Indlæs markerede ordrer**.
* Slet ordrer fra **Shopify-ordren for at importere** siden for at udelukke dem fra synkroniseringen.

## Gennemgå importerede ordrer

Når importen er fuldført, kan du udforske Shopify-ordren og finde alle relaterede oplysninger, f. eks. betalingstransaktioner, forsendelsesomkostninger, følgerne, risikoniveauet, ordreattributter og koder eller opfølgningerne, hvis ordren allerede er opfyldt i Shopify. Du kan også se enhver ordrebekræftelse, der er sendt til debitoren, ved at vælge handlingen **Shopify statusside**.

> [!NOTE]  
> Du kan navigere til vinduet **Shopify Ordrer** direkte, og du kan se ordrer med status *Åben* fra alle butikker. Hvis du vil have vist de færdige ordrer, skal du åbne siden **Shopify-ordrer** fra den specifikke **Shopify Butikskort**-side.

Før der oprettes salgsdokumenter i [!INCLUDE[prod_short](../includes/prod_short.md)], kan du bruge handlingen **Synkroniseret ordre fra Shopify** på siden **Shopify-ordre** til at importere bestemte ordrer igen.

Du kan også markere en ordre som betalt, hvilket er nyttigt i et B2B-scenarie, hvor betalinger behandles uden for Shopify-kassen. Vælg handlingen **Marker som betalt** på siden **Shopify-ordre**. Du kan også markere en ordre som annulleret for at starte refusionsflowet i Shopify. Vælg handlingen **Annuller ordre** på siden **Shopify-ordre**, udfylde felterne efter behov på siden **Shopify Annuller ordre** og trykke på **OK**. Du skal køre ordresynkronisering for at importere opdateringerne til [!INCLUDE[prod_short](../includes/prod_short.md)].

## Opret salgsdokument i Business Central

Hvis til/fra-feltet **Automatisk oprettelse af ordrer** er aktiveret på **Shopify Butikskortet**, forsøger [!INCLUDE[prod_short](../includes/prod_short.md)] at oprette et salgsdokument, når ordren er blevet importeret. Hvis processen løber ind i problemer, f. eks. Hvis en kunde eller et produkt mangler, skal du løse problemet ved at oprette salgsordren igen.

### Oprette salgsdokumenter

1. Vælg ![Lightbulb, der åbner funktionen Fortæl mig 1.](../media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **Shopify Shops**, vælg derefter det relaterede link.
2. Marker den butik, som du vil synkronisere ordrer til for at åbne **Shopify Butikskort**-siden.
3. Vælg handlingen **Ordrer**.
4. Vælg den ordre, du vil oprette et salgsdokument for, og vælg handlingen **Opret salgsdokumenter**.
5. Vælg **Ja**.

Hvis Shopify-ordren kræver opfyldelse, oprettes der en **Salgsordre**. For gennemførte Shopify-ordrer, f.eks. ordrer, der kun indeholder et gavekort, eller som allerede er håndteret i Shopify, oprettes **salgsfakturaen**.

Der oprettes et salgsdokument, som kan administreres vha. standard [!INCLUDE[prod_short](../includes/prod_short.md)]-funktionerne.

Hvis du vil genskabe salgsdokumentet, kan du bruge handlingen **Fjern sammenkædning af behandlede dokumenter** på siden **Shopify-ordre**. Bemærk, at denne handling ikke sletter det allerede oprettede salgsdokument. Du skal behandle det manuelt.

### Administrer manglende kunder

Hvis dine indstillinger forhindrer, at der oprettes en kunde automatisk, og der ikke findes en matchende kunde, kan du manuelt tildele en kunde en Shopify-ordre. Du kan knytte kunder til ordrer på flere måder:

* Tildel **Kundenr.** og **Faktureres til kundenr.** direkte i siden **Shopify-ordrer** ved at vælge en kunde på listen over eksisterende kunder.
* Vælg en debitorskabelon, og opret og tildel derefter debitoren via handlingen **Opret ny debitor** på siden **Shopify-ordrer**. Shopify-debitoren skal have mindst én adresse. Ordrer, du opretter via salgskanalen Shopify POS, mangler ofte adressedetaljer.
* Knyt en eksisterende debitor til den relaterede **Shopify-kunde** på siden **Shopify-kunder**, og vælg derefter handlingen **Find tilknytning** på siden **Shopify-ordrer**.

### Hvordan connectoren vælger, hvilken kunde der skal bruges

Funktionen *Importer ordre fra Shopify* forsøger at vælge debitorer i følgende rækkefølge:

1. Hvis **Standarddebitornr.** feltet er defineret i **Debitorskabelonen for Shopify** for **Send-til Lande/områdekode** og derefter **Standarddebitornr.** uanset indstillingerne i felterne **Debitorimport fra Shopify** og **Debitortilknytningstype**. Flere oplysninger i [Debitorskabelon pr. land](synchronize-customers.md#customer-template-per-countryregion).
2. Hvis **Debitorimport fra Shopify** er indstillet til *Ingen* og **Standarddebitornr.** er defineret på siden **Shopify Butikskort** skal **Standarddebitornr.** .

Næste trin afhænger af **Debitortilknytningstype**.

* Hvis det er **Hent altid standardkunden**, og connectoren bruger derefter kunden, som er defineret i feltet **Standarddebitornr.** feltet på siden **Shopify Køb kort**.
* Hvis det er **Via mail/telefon** forsøger connectoren først at finde eksisterende kunder efter id, derefter pr. e-mail og derefter pr. telefon. Hvis debitoren ikke findes-connectoren opretter en ny kunde.
* Hvis det er **Ved faktureringsoplysninger** forsøger connectoren først at finde den eksisterende debitor efter id og derefter efter faktureringsadresseoplysninger. Hvis debitoren ikke findes-connectoren opretter en ny kunde.

> [!NOTE]  
> Connectoren bruger oplysninger fra faktureringsadressen og opretter en faktureringskunden i [!INCLUDE[prod_short](../includes/prod_short.md)]. Kunden skal være den samme som den kunde, der faktureres.

For B2B-ordrer er flowet det samme, men connectoren bruger felterne **Standardvirksomhedsnr.**, **Virksomhedsindlæsning fra Shopify**, **Type af virksomhedstilknytning** på siden **Shopify-butikskort**. Bemærk, at der ikke er noget **standardvirksomhedsnummer** i **Shopify-kundeskabelon**, da for B2B forventes det at have navngivne kunder.

### Forskellige behandlingsregler for ordrer

Det kan være en god idé at behandle ordrer forskelligt, afhængigt af en regel. F. eks. bør ordrer fra en bestemt salgskanal, som f. eks. POS, bruge standard debitoren, men du vil gerne have, at din onlinebutik skal have reelle oplysninger om kunden.

En måde at løse dette krav på er at oprette et yderligere Shopify-produktions kort og bruge filtre i **Synkroniseringsrækkefølgen fra Shopify**-anmodningssiden.

Eksempel: Du har en onlinebutik samt en Shopify POS. Til din POS, skal du bruge en fast kunde, men til din onlinebutik, som du vil oprette debitorer i [!INCLUDE[prod_short](../includes/prod_short.md)]. Følgende fremgangsmåde viser de overordnede trin. Hvis du vil vide mere, skal du gå til de tilsvarende artikler i hjælp.

1. Opret et firma med navnet Shopify *STORE*, og Opret en kæde til din Shopify-konto.
1. Konfigurer synkronisering af varer/produkter, så denne butik administrerer produktoplysninger.
1. Angiv, at debitorer indlæses med ordrer. Connectoren bør finde kunder ved at lede efter deres e-mail-adresse. Hvis der ikke findes en adresse, bruges kundeskabelonen til at oprette en ny debitor.
1. Opret et Shopify-butik kaldet *POS*, og opret en kæde til din Shopify-konto.
1. Sørg for, at elementet/produktsynkroniseringen er deaktiveret.
1. Vælg den Connector, der bruger standarddebitoren.
1. Opret en tilbagevendende opgavekøpost for Rapport 30104 **Synkronisere ordrer fra Shopify**. Vælg **STORE** i feltet **Shopify-butikskode**, og brug filtre til at fastholde alle ordrer med undtagelse af dem, som POS-salgskanalen opretter. F.eks. **<>Point of Sale**
1. Opret en tilbagevendende opgavekøpost for Rapport 30104 **Synkronisere ordrer fra Shopify**. Marker **POS** i feltet **Shopify-butikskode**, og brug filtre til at hente ordrer, der er oprettet af salgskanalen POS. F.eks. **<>Point of Sale**.

Hver opgavekø importerer og behandler ordrer inden for de angivne filtre og bruger reglerne fra det tilsvarende Shopify-butikskort. Der oprettes f.eks. POS-ordrer for standarddebitoren.

> [!Important]
> Hvis du vil undgå konflikter, når der behandles ordrer, skal du bruge den samme jobkø kategori for opgavekøer.

### Indflydelse på redigeringen af ordrer

I Shopify:

|Rediger|Indvirkning på Shopify-ordrer, der endnu ikke er behandlet i [!INCLUDE[prod_short](../includes/prod_short.md)] | Indvirkning på Shopify-ordrer, der allerede er behandlet i [!INCLUDE[prod_short](../includes/prod_short.md)] |
|------|-----------|-----------|
|Ændre opfyldelsesplaceringen | Opfyldelse af placering synkroniseres til [!INCLUDE[prod_short](../includes/prod_short.md)]. | Opfyldelse af placering synkroniseres til [!INCLUDE[prod_short](../includes/prod_short.md)].|
|Redigere en ordre og øge antallet|Den importerede ordre vil bruge et nyt antal.| Connectoren registrerer ændringer og markerer ordrer. |
|Redigere en ordre og reducere antallet|Den importerede ordre vil bruge et nyt antal. Shopify-refusion med 0 beløb importeres og ikke kan konverteres til kreditnota.| Connectoren registrerer ændringer og markerer ordrer. |
|Redigere en ordre og fjerne en eksisterende vare |Det fjernede element importeres ikke. Shopify-refusion med 0 beløb importeres og ikke kan konverteres til kreditnota.| Connectoren registrerer ændringer og markerer ordrer. |
|Redigere en ordre og tilføje nyt element | Oprindelige og tilføjede varer vil blive importeret. | Connectoren registrerer ændringer og markerer ordrer. |
|Procesrækkefølge: indfri, opdater betalingsoplysninger | Ordrehovedet opdateres. |Ordrehovedet opdateres. Denne opfyldelse synkroniseres ikke med Shopify.|
|Annuller betalt ordre | Ordrehovedet opdateres, så det behandles separat |Connectoren registrerer ændringer og markerer ordrer. |
|Annuller ubetalt ordre | Det fjernede element importeres ikke. Shopify-refusion med 0 beløb importeres og ikke kan konverteres til kreditnota. |Connectoren registrerer ændringer og markerer ordrer. |

Hvis ordren allerede er behandlet i [!INCLUDE[prod_short](../includes/prod_short.md)], viser connectoren følgende fejlmeddelelse: *Ordren er allerede behandlet i Business Central, men der er modtaget en udgave fra Shopify. Ændringer blev ikke overført til den behandlede ordre i Business Central. Opdater de behandlede dokumenter, så de matcher de modtagne data fra Shopify. Hvis du vil gennemtvinge synkroniseringen, skal du bruge handlingen "Synkroniser ordre fra Shopify" på siden Shopify-ordrekort.*

Afhængigt af status for det oprettede salgsdokument kan du udføre følgende handlinger:

1. Slette oprettede salgsdokumenter
2. Vælg handlingen **Fjern sammenkædning af behandlede dokumenter** for at nulstille indikatoren **Behandlet**.
3. Vælg handlingen **Synkroniseret ordre fra Shopify** for at opdatere den individuelle ordre med de seneste data fra Shopify.

I [!INCLUDE[prod_short](../includes/prod_short.md)]:

|Rediger|Indvirkning|
|------|-----------|
|Skift placering til en anden placering. Bogfør levering. | Ordre markeres som opfyldt. Opfyldelseslokation fra Shopify vil blive brugt. |
|Reducere antallet. Bogfør levering. | Ordren i Shopify bliver markeret som delvist opfyldt. |
|Øge antallet. Bogfør levering. | Denne opfyldelse synkroniseres ikke med Shopify. Det samme gælder, hvis opfyldelsen blev opdelt i Shopify, men behandlet som én linje i [!INCLUDE[prod_short](../includes/prod_short.md)]. |
|Tilføj en ny komponent. Bogfør levering. | Ordren i Shopify bliver markeret som opfyldt. Nye linjer tilføjes ikke. |

## Synkronisere leverancer til Shopify

Når en salgsordre, der er oprettet fra en Shopify-ordre, bliver leveret, kan du synkronisere leverancerne til Shopify.

1. Vælg ![Lightbulb, der åbner funktionen Fortæl mig 1.](../media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **Synkronisere forsendelser til Shopify**, vælg derefter det relaterede link.
2. Definer eventuelt filtre for forsendelser. Du kan f. eks. opdatere forsendelse, der er bogført på en bestemt dato.
3. Vælg **OK**.

Ordren i Shopify bliver markeret som opfyldt. Kunden modtager automatisk en e-mail med leveringsbemærkninger eller tekstmeddelelse (SMS). Hvis der er angivet en speditør og en sporingskode i leverancen, medtages sporingsoplysningerne i e-mailen.

Du kan også bruge handlingen **Synkroniser leverancer** på siderne Shopify-salgsordrer eller Shopify-butik.

Du kan planlægge, at følgende tilbagevendende aktiviteter skal udføres automatisk. Få mere at vide, når du [planlægger tilbagevendende opgaver](background.md#to-schedule-recurring-tasks).

> [!Important]
> Lokationen, herunder tom lokation, der er defineret på den bogførte leverancelinje, skal have en tilsvarende post på Shopify-lokationen. Ellers sendes denne linje ikke tilbage til Shopify. Flere oplysninger [Lokationstilknytning](synchronize-orders.md#location-mapping).

Husk at køre **Synkroniser ordre fra Shopify** for at opdatere opfyldelsesstatus for ordre i [!INCLUDE[prod_short](../includes/prod_short.md)]. Connector-funktionen arkiverer også fuldt indbetalte og befriede ordrer både i Shopify og [!INCLUDE[prod_short](../includes/prod_short.md)], hvis betingelserne er opfyldt. 

### Speditører og sporing af URL-adresse

Hvis det **bogførte salgsleverance**-dokument indeholder **Speditørkode** og/eller **Pakkesporingsnummer**, sendes disse oplysninger til Shopify og frem til slutdebitoren i bekræftelsesmailen.

Sporingsvirksomheden udfyldes på grundlag af speditørposten med følgende prioriteter (fra højeste til laveste):

1. **Shopify Sporingsvirksomhed**
1. **Navn**
1. **Kode**

Hvis feltet **Pakkesporings-URL** er udfyldt for speditørposten, vil levering også indeholde en URL-adresse til sporing.

## Returneringer og refusioner

I en integration mellem Shopify og [!INCLUDE[prod_short](../includes/prod_short.md)] er det vigtigt, at du kan synkronisere så mange virksomhedsdata som muligt. Det gør det nemmere at holde finans-og lagerniveauer opdaterede i [!INCLUDE[prod_short](../includes/prod_short.md)]. De data, som du kan synkronisere, indeholder returvarer og refusioner, der er registreret i Shopify Administration eller Shopify POS.

Returvarer og refusioner importeres med tilhørende ordrer, hvis du har aktiveret behandlingstypen på Shopify-butikskortet.

Returvarer importeres til oplysningsformål alene. Der er ingen tilknyttet behandlingslogik.

Økonomisk og om nødvendigt lagertransaktioner behandles via refusion. Refusion kan omfatte produkter eller blot beløb, f.eks. hvis en handlende har besluttet at kompensere leveringsgebyrer eller et andet beløb.

Du kan oprette salgskreditnotaer til refusioner. Kreditnotaerne kan have følgende linjetyper:

|Enhedstype|Nej|Kommentar|
|-|-|-|
|Finanskonto|Konto til solgte gavekort| Bruges til refusioner i forbindelse med gavekort.|
|Finanskonto|Refusionskonto til ikke-genopfyldte varer | Bruges til at udføre refusioner i forbindelse med produkter, som ikke er blevet lagerførte. |
|Artikel |Varenr.| Bruges til at udføre refusioner i forbindelse med produkter, som ikke er blevet lagerførte. Gælder for direkte refusioner eller refusioner, der er knyttet til refusioner. Den lokationskode, der er på kreditlinjen, angives på grundlag af den værdi, der er valgt for returlokationen.|
|Finanskonto| Refusionskonto | Bruges til andre refusionsbeløb, der ikke er relateret til produkter eller gavekort. F.eks. tips, eller hvis du manuelt har angivet et beløb til refusion i Shopify. |

> [!Note]
> Returlokationer, herunder tomme lokationer, der er defineret i **Shopify-butikskortet** bruges på den oprettede kreditnota. De oprindelige lokationer ignoreres fra ordrer eller leverancer.

## Gavekort

I Shopify-butikken kan du sælge gavekort, som kan bruges til at betale for reelle produkter senere.

Når du håndterer gavekort, er det vigtigt at angive en værdi i feltet **Konto for solgte gavekort** i vinduet **Shopify-butikskort**. Det solgte gavekort synkroniseres sammen med ordrer på linje. Et udlignet gavekort indlæses også sammen med ordren, men nu som en transaktion. Bemærk, at gavekortet ikke reducerer det beløb, der skal faktureres.

Hvis du vil se det udstedte og anvendte gavekort, skal du vælge den ![Lightbulb, der åbner funktionen Fortæl mig.](../media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, angiv **Gavekort**, og vælg derefter det relaterede link.

## Se også

[Kom i gang med Shopify Connector](get-started.md)  
