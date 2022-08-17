---
title: Synkronisere og opfylde salgsordrer
description: Konfigurere og køre import og behandling af salgsordre fra Shopify.
ms.date: 05/27/2022
ms.topic: article
ms.service: dynamics365-business-central
author: edupont04
ms.author: andreipa
ms.reviewer: solsen
ms.openlocfilehash: bef02c5fcbc2b6174e8a3f746a97f0e11564dcf6
ms.sourcegitcommit: 902da19b0ab7a3fbc051cd69ab2802f30d0f378f
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 08/01/2022
ms.locfileid: "9213685"
---
# <a name="synchronize-and-fulfill-sales-orders"></a>Synkronisere og opfylde salgsordrer

I denne artikel beskrives de nødvendige indstillinger og trin, du skal fuldføre for at synkronisere og opfylde salgsordrer fra Shopify i [!INCLUDE[prod_short](../includes/prod_short.md)].

## <a name="set-the-import-of-orders-on-the-shopify-shop-card"></a>Angive importen af ordrer på Shopify-butikskortet

En almindelig Shopify-ordre kan indeholder omkostninger ud over subtotalen, f. eks. forsendelsesgebyrer eller, hvis det er aktiveret, tip. Beløbene bogføres direkte på den finanskonto, der skal bruges til bestemte posteringstyper:

- **Konto til forsendelsesomkostninger**
- **Solgt gavekortkonto** – du kan finde flere oplysninger i [Gavekort](synchronize-orders.md#gift-cards)
- **Tips til konto**  

Aktiver **Automatisk oprettelse af ordrer** for at oprette salgsdokumenter automatisk i [!INCLUDE[prod_short](../includes/prod_short.md)], når Shopify-ordren er importeret.
Salgsdokumentet i [!INCLUDE[prod_short](../includes/prod_short.md)] indeholder et link til Shopify-ordren. Hvis du aktiverer feltet **Shopify-ordrenr. på dokumentlinjen**, bliver disse oplysninger gentaget på salgslinjen af typen *Bemærkning*.

I feltet **Momsområdekilde** kan du definere prioritering af, hvordan skatteområdekode eller momsvirksomhedsbogføringsgruppe på grundlag af adresse. Dette trin er relevant for lande med moms og moms. Få mere at vide på [Momsbemærkninger](synchronize-orders.md#tax-remarks).

### <a name="shipment-method-mapping"></a>Tilknytning af forsendelsesmetode

**Leveringskode** for salgsdokumenter, der er indlæst fra Shopify, kan udfyldes automatisk. Du skal konfigurere **tilknytning af leveringsmetode**.

1. Vælg ![Lightbulb, der åbner funktionen Fortæl mig 1.](../media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **Shopify Shops**, og vælg derefter det relaterede link.
2. Marker den butik, som du vil definere tilknytning til for at åbne **Shopify Butikskort**-siden.
3. Vælg handlingen **Tilknytning af forsendelsesmetode**. Posterne for forsendelsesmetoder, der er defineret i [**Forsendelse**](https://www.shopify.com/admin/settings/payments)-indstillingerne i din **Shopify Administrator**, oprettes automatisk.
4. I feltet **Navn** kan du se navnet på leveringsmåden fra Shopify.
5. Indtast **Forsendelsesmetodekoden** med den tilsvarende forsendelsesmetoide i [!INCLUDE[prod_short](../includes/prod_short.md)].

> [!NOTE]  
> Hvis der er knyttet flere forsendelsesgebyrer til en salgsordre. der er kun valgt én som forsendelsesmetode, der er knyttet til salgsdokumentet.

### <a name="payment-method-mapping"></a>Tilknytning af betalingsmetode

Hvis du vil udfylde **betalingsmetodekoden** automatisk for salgsdokumenter, der er importeret fra Shopify, skal du konfigurere **tilknytning af betalingsmetode**.

1. Vælg ![Lightbulb, der åbner funktionen Fortæl mig 1.](../media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **Shopify Shops**, og vælg derefter det relaterede link.
2. Marker den butik, som du vil definere tilknytning til for at åbne **Shopify Butikskort**-siden.
3. Vælg handlingen **Tilknytning af betalingsmetode**.
4. Indtast navnet på betalingsmetoden i felterne **Gateway** og **Kreditkortfirma** fra Shopify. Posterne oprettes automatisk, når du importerer Shopify-ordrer.
5. Indtast **Betalingsmetodekoden** med den tilsvarende betalingsmetode i [!INCLUDE[prod_short](../includes/prod_short.md)].
6. Angiv **prioritet** for sager, når debitor bruger flere betalingsmidler. Betalingsmetoden med den højeste prioritet bliver valgt i salgsdokumentet. Hvis begge betalingsmetoder har samme prioritet, bruges betalingsmetoden med det højeste beløb.

> [!NOTE]  
> Hvis den tilsvarende betalingsmetode i [!INCLUDE[prod_short](../includes/prod_short.md)] har **Modkonto type** og **Modkonto** udfyldt, vil fakturasystemet under bogføringen, oprette en modpost af *betaling*-typen og udligne den med *faktura*-typen i debitorposten.

### <a name="location-mapping"></a>Tilknytning af lokation

Hvis du automatisk vil udfylde **Lokationskoden** for salgsdokumenter, der er importeret fra Shopify, skal du konfigurere **Shopify Butiksplaceringer**.

1. Vælg ![Lightbulb, der åbner funktionen Fortæl mig 1.](../media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **Shopify Shops**, og vælg derefter det relaterede link.
2. Marker den butik, for hvilken du vil konfigurere tilknytning af placering for at åbne siden **Shopify-butikskort**.
3. Vælg handlingen **Lokationer** for at åbne **Shopify Butikslokationer**.
4. Vælg handlingen **Hent Shopify Lokationer** for at importere alle de placeringer, der er defineret i Shopify. Du kan finde dem under [**Lokations**](https://www.shopify.com/admin/settings/locations)-indstillinger i **Shopify Administrator**. Bemærk, at den lokation, der er markeret som *standard*, bruges ved import af ikke-opfyldte Shopify-ordrer.
5. Angiv **standardplaceringskoden** med den tilsvarende lokation i [!INCLUDE[prod_short](../includes/prod_short.md)].

> [!NOTE]  
> Du skal konfigurere lokations tilknytningen, hvis til/fra-feltet **lokation, der er obligatorisk** er aktiveret på **lageropsætningskortet**. Ellers kan du ikke oprette salgsdokumenter.

## <a name="run-the-order-synchronization"></a>Kør ordresynkronisering

Nedenstående procedure beskriver, hvordan du imjporterer og opdaterer salgsordrer.

> [!NOTE]  
> Arkiverede ordrer i Shopify kan ikke importeres. Deaktiver **Automatisk arkivering af ordren** i sektionen **Ordrebehandling** under indstillingerne **Tjek ud** i **Shopify Administration** for at kontrollere, at alle ordrer er importeret til [!INCLUDE[prod_short](../includes/prod_short.md)]. Hvis du har brug for at importere arkiverede ordrer, skal du bruge handlingen **Ikke-arkiverede ordrer** på siden [Ordrer](https://www.shopify.com/admin/orders) til panelet **Shopify-Administration**.

1. Vælg ![Lightbulb, der åbner funktionen Fortæl mig 1.](../media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **Shopify Shops**, og vælg derefter det relaterede link.
2. Marker den butik, som du vil importere ordrer til for at åbne **Shopify Butikskort**-siden.
3. Vælg handlingen **Ordrer**.
4. Vælg handlingen **Synkroniser ordrer fra Shopify**.
5. Definer eventuelt filtre for ordrer. Du kan f. eks. indlæse ordrer, der er fuldt betalt, eller dem, der har lav risiko.
6. Vælg knappen **OK**.

Du kan også søge efter **synkroniseringsordrer fra Shopify** batchjobbet.

Du kan planlægge, at følgende tilbagevendende aktiviteter skal udføres automatisk. Få mere at vide, når du [planlægger tilbagevendende opgaver](background.md#to-schedule-recurring-tasks).

## <a name="review-imported-orders"></a>Gennemgå importerede ordrer

Når importen er fuldført, kan du udforske Shopify-ordren og finde alle relaterede oplysninger, f. eks. betalingstransaktioner, forsendelsesomkostninger, følgerne, risikoniveauet eller opfølgningerne, hvis ordren allerede er opfyldt i Shopify. Du kan også se enhver ordrebekræftelse, der er sendt til debitoren, ved at vælge handlingen **Shopify statusside**.

> [!NOTE]  
> Du kan navigere til vinduet **Shopify Ordrer** direkte, og du kan se ordrer med status *Åben* fra alle butikker. Hvis du vil have vist de færdige ordrer, skal du åbne siden **Shopify Ordrer** fra vinduet specifikt **Shopify Butikskort**-vindue.

## <a name="create-sales-documents-in-business-central"></a>Opret salgsdokument i Business Central

Hvis til/fra-feltet **Automatisk oprettelse af ordrer** er aktiveret på **Shopify Butikskortet**, forsøger [!INCLUDE[prod_short](../includes/prod_short.md)] at oprette et salgsdokument, når ordren er blevet importeret. Hvis processen løber ind i problemer, f. eks. Hvis en kunde eller et produkt mangler, skal du løse problemet ved at oprette salgsordren igen.

### <a name="to-create-sales-documents"></a>Oprette salgsdokumenter

1. Vælg ![Lightbulb, der åbner funktionen Fortæl mig 1.](../media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **Shopify Shops**, og vælg derefter det relaterede link.
2. Marker den butik, som du vil synkronisere ordrer til for at åbne **Shopify Butikskort**-siden.
3. Vælg handlingen **Ordrer**.
4. Vælg den ordre, du vil oprette et salgsdokument for, og vælg handlingen **Opret salgsdokumenter**.
5. Vælg **Ja**.

Hvis Shopify-ordren kræver opfyldelse, oprettes der en **Salgsordre**. For gennemførte Shopify-ordrer, f.eks. ordrer, der kun indeholder et gavekort, eller som allerede er håndteret i Shopify, oprettes **salgsfakturaen**.

Der er nu oprettet et salgsdokument, som kan administreres vha. standard [!INCLUDE[prod_short](../includes/prod_short.md)]-funktionerne.

### <a name="manage-missing-customers"></a>Administrer manglende kunder

Hvis dine indstillinger forhindrer, at der oprettes en kunde automatisk, og der ikke findes en korrekt eksisterende kunde, kan du manuelt tildele en kunde en Shopify-ordre. Dette kan gøres på et par måder:

- Du kan knytte feltet **Sælg til kundenr.** direkte i siden **Shopify-ordrer** ved at vælge en kunde på listen over eksisterende kunder.
- Du kan vælge en debitorskabelonkode, oprette og tildele debitoren via handlingen **Opret ny debitor** på siden **Shopify-ordrer**.
- Du kan knytte en eksisterende debitor til den relaterede **Shopify-kunde** i vinduet **Shopify-kunder** og derefter vælge handlingen **Find tilknytning** på side **Shopify-ordrer**.

### <a name="tax-remarks"></a>Momskommentarer

Den importerede Shopify-ordre viser oplysninger om moms, men momsen bliver genberegnet, når du opretter salgsdokumentet, så det er vigtigt, at indstillingerne for moms/skat er korrekte i [!INCLUDE[prod_short](../includes/prod_short.md)].

- Flere momssatser/momssatser. Nogle produktkategorier er f. eks. ansvarlige for reducerede skatte satser. Disse varer skal findes i [!INCLUDE[prod_short](../includes/prod_short.md)] og knyttes til Shopify-produkterne. Hvis du ikke gør det, bruges momsproduktbogføringsgruppen automatisk med automatisk oprettelse af manglende varer.

- Adresse-afhængige momssatser. Brug feltet **Skatteområdeprioritet** sammen med tabellen **Debitorskabeloner** til at overskrive standardlogik, som udfyldes i **Skatteområdekode** i salgsdokumentet. Feltet **skatteområde-prioritet** angiver den prioritet, hvor funktionen skal indeholde oplysninger om land/område og stat/provins. Derefter bliver den tilsvarende post i Shopify-debitorskabelonen fundet, og **Skatteområdekode**, **Skattepligtig moms** og **Momsvirksomheds bogføringsgruppe** bruges, når der oprettes et salgsdokument.

- Priser inkl. moms. Feltet **Priser inkl. moms**/**Priser ekskl. moms** i det oprettede salgsdokument afhænger ikke af debitoren, men af **kundeskabelonen** fra **Shopify-butikskort** eller debitorskabelonen pr. land.

### <a name="impact-of-order-editing"></a>Indflydelse på redigeringen af ordrer

I Shopify:

|Rediger|Effekt|
|------|-----------|
|Ændre opfyldelsesplaceringen | Den oprindelige placering synkroniseres til [!INCLUDE[prod_short](../includes/prod_short.md)]. |
|Redigere en ordre og ændre antal| Ordrehoved og supplerende tabeller opdateres i [!INCLUDE[prod_short](../includes/prod_short.md)], men linjerne vil ikke. |
|Redigere en ordre og tilføje nyt element | Ordrehovedet opdateres, men linjerne vil ikke blive udtaget. |

I [!INCLUDE[prod_short](../includes/prod_short.md)]:

|Rediger|Effekt|
|------|-----------|
|Ændre lokationen til en anden lokation, der er knyttet til Shopify-lokationerne. Bogfør levering. | Når opfyldning er synkroniseret, opdateres lokationen i Shopify. |
|Ændre lokationen til en anden lokation, der ikke er knyttet til Shopify-lokationerne. Bogfør levering. | Denne opfyldelse synkroniseres ikke med Shopify. |
|Ændre reduktionsantallet. Bogfør levering. | Ordren i Shopify bliver markeret som delvist opfyldt. |
|Tilføj en ny komponent. Bogfør levering. | Ordren i Shopify bliver markeret som opfyldt. Linjer ikke opdateres. |

## <a name="synchronize-shipments-to-shopify"></a>Synkronisere leverancer til Shopify

Når en salgsordre, der er oprettet fra en Shopify-ordre, bliver leveret, kan du synkronisere leverancerne til Shopify.

1. Vælg ![Lightbulb, der åbner funktionen Fortæl mig 1.](../media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **Synkronisere forsendelser til Shopify**, og vælg derefter det relaterede link.
2. Definer eventuelt filtre for forsendelser. Du kan f. eks. opdatere forsendelse, der er bogført på en bestemt dato.
3. Vælg knappen **OK**.

Ordren i Shopify bliver markeret som opfyldt. Kunden modtager automatisk en e-mail med leveringsbemærkninger eller tekstmeddelelse (SMS). Hvis der er angivet en speditør og en sporingskode i leverancen, medtages sporingsoplysningerne i e-mailen.

> [!NOTE]  
> Husk at køre **Synkroniser ordre fra Shopify** for at opdatere opfyldelsesstatus for ordre i [!INCLUDE[prod_short](../includes/prod_short.md)]. Connector-funktionen arkiverer også fuldt indbetalte og befriede ordrer både i Shopify og [!INCLUDE[prod_short](../includes/prod_short.md)], hvis betingelserne er opfyldt.

### <a name="shipping-agents-and-tracking-url"></a>Speditører og sporing af URL-adresse

Hvis det **bogførte salgsleverance**-dokument indeholder **Speditørkode** og/eller **Pakkesporingsnummer**, sendes disse oplysninger til Shopify og frem til slutdebitoren i bekræftelsesmailen.

Sporingsvirksomheden udfyldes på grundlag af speditørposten med følgende prioriteter (fra højeste til laveste):

- **Shopify Sporingsvirksomhed**
- **Navn**
- **Kode**

Hvis feltet **Pakkesporings-URL** er udfyldt for speditørposten, vil levering også indeholde en URL-adresse til sporing.

## <a name="gift-cards"></a>Gavekort

I Shopify-butikken kan du sælge gavekort, som kan bruges til at betale for reelle produkter senere.

Når du håndterer gavekort, er det vigtigt at angive en værdi i feltet **Konto for solgte gavekort** i vinduet **Shopify-butikskort**. Det solgte gavekort synkroniseres sammen med ordrer på linje. Et udlignet gavekort indlæses også sammen med ordren, men nu som en transaktion. Bemærk, at gavekortet ikke reducerer det beløb, der skal faktureres.

Hvis du vil se det udstedte og anvendte gavekort, skal du vælge den ![Lightbulb, der åbner funktionen Fortæl mig.](../media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, angiv **Gavekort**, og vælg derefter det relaterede link.

## <a name="transactions-and-payouts"></a>Transaktioner og udbetalinger

Når en kunde har færdiggjort check ud i onlinebutikken, gemmes oplysningerne om betalinger som en **transaktion**. Der kan være knyttet flere transaktioner til ordren, f. eks. Når en kunde bruger et gavekort til at betale noget af omkostningerne og derefter bruger et kreditkort eller en PayPal til restbeløbet. 

Hvis du bruger Shopify-betaling som betalingsudbyder og derefter ud over oplysninger om de penge, som Betalingsudbyderen har modtaget fra kunden, kan du også få vist udbetalinger fra Shopify til din bankkonto. 

### <a name="transactions"></a>Transaktioner

De betalingstransaktioner, der er foretaget ved, at Shopify synkroniseres sammen med ordrerne og kan ses fra siden *Shopify-ordrer*.

Hvis du vil se alle transaktioner, skal du vælge ![Lightbulb, der åbner funktionen Fortæl mig 1.](../media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **Transaktioner**, og vælg derefter det relaterede link.

Hvis du har konfigureret tilknytning af betalingsmetode, er der tildelt en betalingsmetode kode i det oprettede salgsdokument. Få mere at vide ved [betalingsmetodetilknytning](#payment-method-mapping).

### <a name="payouts"></a>Udbetalinger

Hvis din butik har Shopify Payments aktiveret, modtager du betalinger via *Shopify-udbetalinger*, når en kunde betaler vha Shopify Payments og accelererede checks.

1. Vælg ![Lightbulb, der åbner funktionen Fortæl mig 1.](../media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **Shopify Shops**, og vælg derefter det relaterede link.
2. Marker den butik, som du vil synkronisere udbetalinger til for at åbne siden **Shopify-butikskort**.
3. Vælg handlingen **Synkroniser udbetalinger**.

Hvis du vil se alle udbetalinger, skal du vælge ![Lightbulb, der åbner funktionen Fortæl mig.](../media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **Udbetalinger**, og vælg derefter det relaterede link.

**Udbetalinger** er kun til orientering og påvirker ikke finans-eller bank poster, men de kan være nyttige, når du skal behandle bankkontoudtoget.

## <a name="see-also"></a>Se også

[Kom i gang med Connectoren til Shopify](get-started.md)  
