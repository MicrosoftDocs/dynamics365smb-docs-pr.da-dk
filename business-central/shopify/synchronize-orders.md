---
title: Synkronisere og opfylde salgsordrer
description: Konfigurere og køre import og behandling af salgsordre fra Shopify.
ms.date: 05/27/2022
ms.topic: article
ms.service: dynamics365-business-central
ms.search.form: '30110, 30111, 30112, 30113, 30114, 30115, 30121, 30122, 30123, 30128, 30129,'
author: edupont04
ms.author: andreipa
ms.reviewer: solsen
---

# Synkronisere og opfylde salgsordrer

I denne artikel beskrives de nødvendige indstillinger og trin, du skal fuldføre for at synkronisere og opfylde salgsordrer fra Shopify i [!INCLUDE[prod_short](../includes/prod_short.md)].

## Angive importen af ordrer på Shopify-butikskortet

Husk at angive en **Valutakode**, hvis din online-butik bruger en anden valuta end den relevante regnskabsvaluta. Der skal være konfigureret valutakurser for den angivne valuta. Hvis dit onlineindkøb bruger samme valuta som [!INCLUDE[prod_short](../includes/prod_short.md)], skal du lade feltet stå tomt. 

Du kan se lager valutaen i indstillingerne for [butiksdetaljer](https://www.shopify.com/admin/settings/general) i din Shopify-administrator. Shopify kan konfigureres til at acceptere forskellige valutaer, men importerede ordrer til [!INCLUDE[prod_short](../includes/prod_short.md)] butiksvaluta.

En almindelig Shopify-ordre kan indeholder omkostninger ud over subtotalen, f. eks. forsendelsesgebyrer eller, hvis det er aktiveret, tip. Beløbene bogføres direkte på den finanskonto, der skal bruges til bestemte posteringstyper:

* **Konto til forsendelsesgebyr**
* **Solgt gavekortkonto** – du kan finde flere oplysninger i [Gavekort](synchronize-orders.md#gift-cards)
* **Tips til konto**  

Aktiver **Automatisk oprettelse af ordrer** for at oprette salgsdokumenter automatisk i [!INCLUDE[prod_short](../includes/prod_short.md)], når Shopify-ordren er importeret.

Salgsdokumentet i [!INCLUDE[prod_short](../includes/prod_short.md)] indeholder et link til Shopify-ordren. Hvis du aktiverer feltet **Shopify-ordrenr. på dokumentlinjen**, bliver disse oplysninger gentaget på salgslinjen af typen *Bemærkning*.

I feltet **Momsområdekilde** kan du definere prioritering af, hvordan skatteområdekode eller momsvirksomhedsbogføringsgruppe på grundlag af adresse. Den importerede Shopify-ordre viser oplysninger om moms, men momsen bliver genberegnet, når du opretter salgsdokumentet, så det er vigtigt, at indstillingerne for moms/skat er korrekte i [!INCLUDE[prod_short](../includes/prod_short.md)]. Du kan finde flere oplysninger om moms i [Konfigurere moms for Shopify-forbindelsen](setup-taxes.md).

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

Lokationstilknytningen kræves i tre henseender:

* Du kan finde flere oplysninger i [synkronisere lager til Shopify](synchronize-items.md#sync-inventory-to-shopify)
* Sådan udfyldes **lokationskoden** for salgsdokumenter, der indlæses fra Shopify. Det er vigtigt, når til/fra-feltet **lokation, der er obligatorisk** er aktiveret på **lageropsætningskortet**. Ellers kan du ikke oprette salgsdokumenter.
* Opdatere Shopify-ordren med oplysningerne om opfyldelsen på siden **Bogført salgsleverance**.

1. Vælg ![Lightbulb, der åbner funktionen Fortæl mig 1.](../media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **Shopify Shops**, vælg derefter det relaterede link.
2. Marker den butik, for hvilken du vil konfigurere tilknytning af placering for at åbne siden **Shopify-butikskort**.
3. Vælg handlingen **Lokationer** for at åbne **Shopify Butikslokationer**.
4. Vælg handlingen **Hent Shopify Lokationer** for at importere alle de placeringer, der er defineret i Shopify. Du kan finde dem under [**Lokations**](https://www.shopify.com/admin/settings/locations)-indstillinger i **Shopify Administrator**. Bemærk, at den lokation, der er markeret som *standard*, bruges ved import af ikke-opfyldte Shopify-ordrer.
5. Angiv **standardplaceringskoden** med den tilsvarende lokation i [!INCLUDE[prod_short](../includes/prod_short.md)].

## Kør ordresynkronisering

Nedenstående procedure beskriver, hvordan du imjporterer og opdaterer salgsordrer.

> [!NOTE]  
> Arkiverede ordrer i Shopify kan ikke importeres. Deaktiver **Automatisk arkivering af ordren** i sektionen **Ordrebehandling** under indstillingerne **Tjek ud** i **Shopify Administration** for at kontrollere, at alle ordrer er importeret til [!INCLUDE[prod_short](../includes/prod_short.md)]. Hvis du har brug for at importere arkiverede ordrer, skal du bruge handlingen **Ikke-arkiverede ordrer** på siden [Ordrer](https://www.shopify.com/admin/orders) til panelet **Shopify-Administration**.

1. Vælg ![Lightbulb, der åbner funktionen Fortæl mig 1.](../media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **Shopify Shops**, vælg derefter det relaterede link.
2. Marker den butik, som du vil importere ordrer til for at åbne **Shopify Butikskort**-siden.
3. Vælg handlingen **Ordrer**.
4. Vælg handlingen **Synkroniser ordrer fra Shopify**.
5. Definer eventuelt filtre for ordrer. Du kan f. eks. indlæse ordrer, der er fuldt betalt, eller dem, der har lav risiko.

> [!NOTE]  
> Når du filtrerer efter kode, skal du bruge filtertoken `@` og `*`. Hvis du f. eks. vil importere ordrer, der indeholder *tag1*, skal du bruge `@*tag1*`. `@` sikrer, at der ikke skelnes mellem store og små bogstaver i resultatet, mens `*` finder ordrer med flere koder.

7. Vælg knappen **OK**.

Du kan også søge efter **synkroniseringsordrer fra Shopify** batchjobbet.

Du kan planlægge, at følgende tilbagevendende aktiviteter skal udføres automatisk. Få mere at vide, når du [planlægger tilbagevendende opgaver](background.md#to-schedule-recurring-tasks).

## Gennemgå importerede ordrer

Når importen er fuldført, kan du udforske Shopify-ordren og finde alle relaterede oplysninger, f. eks. betalingstransaktioner, forsendelsesomkostninger, følgerne, risikoniveauet, ordreattributter og koder eller opfølgningerne, hvis ordren allerede er opfyldt i Shopify. Du kan også se enhver ordrebekræftelse, der er sendt til debitoren, ved at vælge handlingen **Shopify statusside**.

> [!NOTE]  
> Du kan navigere til vinduet **Shopify Ordrer** direkte, og du kan se ordrer med status *Åben* fra alle butikker. Hvis du vil have vist de færdige ordrer, skal du åbne siden **Shopify Ordrer** fra vinduet specifikt **Shopify Butikskort**-vindue.

## Opret salgsdokument i Business Central

Hvis til/fra-feltet **Automatisk oprettelse af ordrer** er aktiveret på **Shopify Butikskortet**, forsøger [!INCLUDE[prod_short](../includes/prod_short.md)] at oprette et salgsdokument, når ordren er blevet importeret. Hvis processen løber ind i problemer, f. eks. Hvis en kunde eller et produkt mangler, skal du løse problemet ved at oprette salgsordren igen.

### Oprette salgsdokumenter

1. Vælg ![Lightbulb, der åbner funktionen Fortæl mig 1.](../media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **Shopify Shops**, vælg derefter det relaterede link.
2. Marker den butik, som du vil synkronisere ordrer til for at åbne **Shopify Butikskort**-siden.
3. Vælg handlingen **Ordrer**.
4. Vælg den ordre, du vil oprette et salgsdokument for, og vælg handlingen **Opret salgsdokumenter**.
5. Vælg **Ja**.

Hvis Shopify-ordren kræver opfyldelse, oprettes der en **Salgsordre**. For gennemførte Shopify-ordrer, f.eks. ordrer, der kun indeholder et gavekort, eller som allerede er håndteret i Shopify, oprettes **salgsfakturaen**.

Der er nu oprettet et salgsdokument, som kan administreres vha. standard [!INCLUDE[prod_short](../includes/prod_short.md)]-funktionerne.

### Administrer manglende kunder

Hvis dine indstillinger forhindrer, at der oprettes en kunde automatisk, og der ikke findes en korrekt eksisterende kunde, kan du manuelt tildele en kunde en Shopify-ordre. Dette kan gøres på et par måder:

* Du kan knytte feltet **Sælg til kundenr.** og **Faktureres til kundenr.** direkte i siden **Shopify-ordrer** ved at vælge en kunde på listen over eksisterende kunder.
* Du kan vælge en debitorskabelonkode, oprette og tildele debitoren via handlingen **Opret ny debitor** på siden **Shopify-ordrer**. Bemærk, at Shopify-debitor skal have mindst én adresse. Ordrer, der er oprettet via salgskanalen Shopify POS, mangler ofte adressedetaljer.
* Du kan knytte en eksisterende debitor til den relaterede **Shopify-kunde** i vinduet **Shopify-kunder** og derefter vælge handlingen **Find tilknytning** på siden **Shopify-ordrer**.

### Hvordan connectoren vælger, hvilken kunde der skal bruges

Funktionen *Importer ordre fra Shopify* forsøger at vælge debitorer i følgende rækkefølge:

1. Hvis **Standarddebitornr.** feltet er defineret i **Shopify Debitorskabelonen** for det tilsvarende land, så anvendes **Standarddebitornr.** uanset indstillingerne i felterne **Debitorimport fra Shopify** og **Debitortilknytningstype**. Flere oplysninger i [Debitorskabelon pr. land](synchronize-customers.md#customer-template-per-country).
2. Hvis **Debitorimport fra Shopify** er indstillet til *Ingen* og **Standarddebitornr.** er defineret på siden **Shopify Butikskort** skal **Standarddebitornr.** .

Næste trin afhænger af **Debitortilknytningstype**.

* Hvis det er **Hent altid standardkunden**, og connectoren bruger derefter kunden, som er defineret i feltet **Standarddebitornr.** feltet på siden **Shopify Køb kort**.
* Hvis det er **Via mail/telefon** forsøger connectoren først at finde eksisterende kunder efter id, derefter pr. e-mail og derefter pr. telefon. Hvis debitoren ikke findes-connectoren opretter en ny kunde.
* Hvis det er **Ved faktureringsoplysninger** forsøger connectoren først at finde den eksisterende debitor efter id og derefter efter faktureringsadresseoplysninger. Hvis debitoren ikke findes-connectoren opretter en ny kunde.

> [!NOTE]  
> Connectoren bruger oplysninger fra faktureringsadressen og opretter en faktureringskunden i [!INCLUDE[prod_short](../includes/prod_short.md)]. Kunden skal være den samme som den kunde, der faktureres.

### Indflydelse på redigeringen af ordrer

I Shopify:

|Rediger|Effekt|
|------|-----------|
|Ændre opfyldelsesplaceringen | Den oprindelige placering synkroniseres til [!INCLUDE[prod_short](../includes/prod_short.md)]. |
|Ændre opfyldelsesplacering og registrere opfyldelse i Shopify| Hvis ordren allerede er blevet importeret, opdateres linjerne ikke. I det andet tilfælde, hvor ordren er importeret, bruges opfyldelsesplaceringen. |
|Redigere en ordre og ændre antal| Ordrehoved og supplerende tabeller opdateres i [!INCLUDE[prod_short](../includes/prod_short.md)], men linjerne vil ikke. |
|Redigere en ordre og tilføje nyt element | Ordrehovedet opdateres, men linjerne vil ikke blive udtaget. |

I [!INCLUDE[prod_short](../includes/prod_short.md)]:

|Rediger|Effekt|
|------|-----------|
|Ændre lokationen til en anden lokation, der er knyttet til Shopify-lokationerne. Bogfør levering. | Når opfyldning er synkroniseret, opdateres lokationen i Shopify. |
|Ændre lokationen til en anden lokation, der ikke er knyttet til Shopify-lokationerne. Bogfør levering. | Denne opfyldelse synkroniseres ikke med Shopify. |
|Ændre reduktionsantallet. Bogfør levering. | Ordren i Shopify bliver markeret som delvist opfyldt. |
|Tilføj en ny komponent. Bogfør levering. | Ordren i Shopify bliver markeret som opfyldt. Linjer ikke opdateres. |

## Synkronisere leverancer til Shopify

Når en salgsordre, der er oprettet fra en Shopify-ordre, bliver leveret, kan du synkronisere leverancerne til Shopify.

1. Vælg ![Lightbulb, der åbner funktionen Fortæl mig 1.](../media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **Synkronisere forsendelser til Shopify**, vælg derefter det relaterede link.
2. Definer eventuelt filtre for forsendelser. Du kan f. eks. opdatere forsendelse, der er bogført på en bestemt dato.
3. Vælg knappen **OK**.

Ordren i Shopify bliver markeret som opfyldt. Kunden modtager automatisk en e-mail med leveringsbemærkninger eller tekstmeddelelse (SMS). Hvis der er angivet en speditør og en sporingskode i leverancen, medtages sporingsoplysningerne i e-mailen.

Du kan også bruge handlingen **Synkroniser leverancer** på siderne Shopify-salgsordrer eller Shopify-butik.

Du kan planlægge, at følgende tilbagevendende aktiviteter skal udføres automatisk. Få mere at vide, når du [planlægger tilbagevendende opgaver](background.md#to-schedule-recurring-tasks).

>[Vigtigt] Lokationen, herunder tom lokation, der er defineret på den bogførte leverancelinje, skal have en tilsvarende post på Shopify-lokationen. Ellers sendes denne linje ikke tilbage til Shopify. Flere oplysninger [Lokationstilknytning](synchronize-orders.md#location-mapping).

Husk at køre **Synkroniser ordre fra Shopify** for at opdatere opfyldelsesstatus for ordre i [!INCLUDE[prod_short](../includes/prod_short.md)]. Connector-funktionen arkiverer også fuldt indbetalte og befriede ordrer både i Shopify og [!INCLUDE[prod_short](../includes/prod_short.md)], hvis betingelserne er opfyldt.

### Speditører og sporing af URL-adresse

Hvis det **bogførte salgsleverance**-dokument indeholder **Speditørkode** og/eller **Pakkesporingsnummer**, sendes disse oplysninger til Shopify og frem til slutdebitoren i bekræftelsesmailen.

Sporingsvirksomheden udfyldes på grundlag af speditørposten med følgende prioriteter (fra højeste til laveste):

* **Shopify Sporingsvirksomhed**
* **Navn**
* **Kode**

Hvis feltet **Pakkesporings-URL** er udfyldt for speditørposten, vil levering også indeholde en URL-adresse til sporing.

## Gavekort

I Shopify-butikken kan du sælge gavekort, som kan bruges til at betale for reelle produkter senere.

Når du håndterer gavekort, er det vigtigt at angive en værdi i feltet **Konto for solgte gavekort** i vinduet **Shopify-butikskort**. Det solgte gavekort synkroniseres sammen med ordrer på linje. Et udlignet gavekort indlæses også sammen med ordren, men nu som en transaktion. Bemærk, at gavekortet ikke reducerer det beløb, der skal faktureres.

Hvis du vil se det udstedte og anvendte gavekort, skal du vælge den ![Lightbulb, der åbner funktionen Fortæl mig.](../media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, angiv **Gavekort**, og vælg derefter det relaterede link.

## Se også

[Kom i gang med Connectoren til Shopify](get-started.md)  
