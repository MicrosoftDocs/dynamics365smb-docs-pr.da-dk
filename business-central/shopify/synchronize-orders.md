---
title: Synkronisere og opfylde salgsordrer
description: Konfigurere og køre import og behandling af salgsordre fra Shopify.
ms.date: 05/27/2022
ms.topic: article
ms.service: dynamics365-business-central
author: edupont04
ms.author: andreipa
ms.reviewer: solsen
ms.openlocfilehash: 4e8d640f6de61d642037a55fdfeb09e32f197a96
ms.sourcegitcommit: fb43bc843be4ea9c0c674a14945df727974d9bb9
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 05/27/2022
ms.locfileid: "8809009"
---
# <a name="synchronize-and-fulfill-sales-orders"></a>Synkronisere og opfylde salgsordrer

I denne artikel beskrives de nødvendige indstillinger og trin, du skal udføre for at synkronisere og opfylde salgsordrer.

## <a name="set-import-of-orders-on-the-shopify-shop-card"></a>Angive import af ordrer på Shopify-butikskortet

En almindelig Shopify-ordre kan have ekstra mængder øverst, f. eks. forsendelsesgebyrer eller, hvis det er aktiveret, tip. Beløbene bogføres direkte på finanskonti. Vælg den finanskonto, der skal bruges til bestemte transaktioner:

- **Konto til forsendelsesomkostninger**
- **Solgt gavekortkonto** – du kan finde flere oplysninger i [Gavekort](synchronize-orders.md#gift-cards).
- **Tips til konto**  

Aktiver **Automatisk oprettelse af ordrer**  for at oprette salgsdokumenter automatisk i [!INCLUDE[prod_short](../includes/prod_short.md)], når Shopify-ordren er importeret.
Salgsdokumentet i [!INCLUDE[prod_short](../includes/prod_short.md)] indeholder et link til Shopify-ordren. Hvis du aktiverer feltet **Shopify-ordrenr. på dokumentlinjen**, bliver disse oplysninger gentaget på salgslinjen af typen *Bemærkning*.

I feltet **Momsområdekilde** kan du definere prioritering af, hvordan skatteområdekode eller momsvirksomhedsbogføringsgruppe på grundlag af adresse. Dette trin er relevant for lande med moms, men kan bruges til moms lande. Du kan finde flere oplysninger i [Momskommentarer](synchronize-orders.md#tax-remarks).

### <a name="shipment-method-mapping"></a>Tilknytning af forsendelsesmetode

**Leveringskode** for salgsdokumenter, der er indlæst fra Shopify, kan udfyldes automatisk. Du skal konfigurere **tilknytning af leveringsmetode**.

1. Gå til søgning ![Lightbulb, der åbner funktionen Fortæl mig.](../media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **Shopify Butik**, og vælg det relevante link.
2. Marker den butik, som du vil definere tilknytning til for at åbne **Shopify Butikskort**-siden.
3. Vælg handlingen **Tilknytning af forsendelsesmetode**. Posterne for forsendelsesmetoder, der er defineret i [**Forsendelse**](https://www.shopify.com/admin/settings/payments)-indstillingerne i din **Shopify Administrator**, oprettes automatisk.
4. I feltet **Navn** kan du se navnet på leveringsmåden Shopify.
5. Indtast **Forsendelsesmetodekoden** med den tilsvarende forsendelsesmetoide i [!INCLUDE[prod_short](../includes/prod_short.md)].

> [!NOTE]  
> Hvis der er knyttet flere forsendelsesgebyrer til en salgsordre. der er kun valgt én som forsendelsesmetode, der er knyttet til salgsdokumentet.

### <a name="payment-method-mapping"></a>Tilknytning af betalingsmetode

Hvis du vil udfylde **betalingsmetodekoden** automatisk for salgsdokumenter, der er importeret fra Shopify, skal du konfigurere **tilknytning af betalingsmetode**.

1. Gå til søgning søg ![Lightbulb, der åbner funktionen Fortæl mig.](../media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **Shopify Butik**, og vælg det relevante link.
2. Marker den butik, som du vil definere tilknytning til for at åbne **Shopify Butikskort**-siden.
3. Vælg handlingen **Tilknytning af betalingsmetode**.
4. Indtast navnet på betalingsmetoden i felterne **Gateway** og **Kreditkortfirma** fra Shopify. Posterne oprettes automatisk, når du importerer Shopify-ordrer.
5. Indtast **Betalingsmetodekoden** med den tilsvarende betalingsmetode i [!INCLUDE[prod_short](../includes/prod_short.md)].
6. Angiv **prioritet** for sager, når debitor bruger flere betalingsmidler. Betalingsmetoden med den højeste prioritet bliver valgt i salgsdokumentet. Hvis begge betalingsmetoder har samme prioritet, bruges betalingsmetoden med det højeste beløb.

## <a name="run-order-synchronization"></a>Kør ordresynkronisering

Nedenstående procedure beskriver, hvordan du imjporterer og opdaterer salgsordrer.

> [!NOTE]  
> Arkiverede ordrer i Shopify kan ikke importeres. Deaktiver **Automatisk arkivering af ordren** i sektionen **Ordrebehandling** under indstillingerne **Tjek ud** i **Shopify Administration** for at kontrollere, at alle ordrer er importeret til [!INCLUDE[prod_short](../includes/prod_short.md)]. Hvis du har brug for at importere arkiverede ordrer, skal du bruge handlingen **Ikke-arkiverede ordrer** på siden [Ordrer](https://www.shopify.com/admin/orders) o Shopify Admin.

1. Gå til søgning ![Lightbulb, der åbner funktionen Fortæl mig.](../media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **Shopify Butik**, og vælg det relevante link.
2. Marker den butik, som du vil importere ordrer til for at åbne **Shopify Butikskort**-siden.
3. Vælg handlingen **Ordrer**.
4. Vælg handlingen **Synkroniser ordrer fra Shopify**.
5. Definer eventuelt filtre for ordrer. Du kan f. eks. indlæse ordrer, der er fuldt betalt, eller dem, der har lav risiko.
6. Vælg knappen **OK**.

Du kan også søge efter **synkroniseringsordrer fra Shopify** batchjobbet.

Du kan planlægge, at følgende tilbagevendende aktiviteter skal udføres automatisk. Du kan finde flere oplysninger i [Planlægge gentagne opgaver](background.md#to-schedule-recurring-tasks).

## <a name="review-imported-orders"></a>Gennemgå importerede ordrer

Når importen er fuldført, kan du udforske Shopify-ordren og finde alle relaterede oplysninger. F.eks. kan du finde betalingstransaktioner, leveringsomkostninger, risiko niveauer eller providere, hvis ordren allerede er blevet opfyldt i Shopify. Du kan også se enhver ordrebekræftelse, der er sendt til debitoren, ved at vælge handlingen **Shopify statusside**.

> [!NOTE]  
> Du kan navigere til vinduet **Shopify Ordrer** direkte, og du kan se ordrer med status *Åben* fra alle butikker. Hvis du vil have vist de færdige ordrer, skal du åbne siden **Shopify Ordrer** fra vinduet specifikt **Shopify Butikskort**-vindue.

## <a name="create-sales-documents-in-business-central"></a>Opret salgsdokument i Business Central

Hvis til/fra-feltet **Automatisk oprettelse af ordrer** er aktiveret på **Shopify Butikskortet**, forsøger [!INCLUDE[prod_short](../includes/prod_short.md)] at oprette et salgsdokument, når ordren er blevet importeret. Hvis processen løber ind i problemer, f. eks. Hvis en kunde eller et produkt mangler, skal du løse problemet. Derefter kan du forsøge at oprette salgsordren igen.

### <a name="to-create-sales-documents"></a>Oprette salgsdokumenter

1. Gå til søgning ![Lightbulb, der åbner funktionen Fortæl mig.](../media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **Shopify Butik**, og vælg det relevante link.
2. Marker den butik, som du vil synkronisere ordrer til for at åbne **Shopify Butikskort**-siden.
3. Vælg handlingen **Ordrer**.
4. Vælg den ordre, du vil oprette et salgsdokument for, og vælg handlingen **Opret salgsdokumenter**.
5. Vælg **Ja**.

Hvis Shopify-ordren kræver opfyldelse, oprettes der en **Salgsordre**. For helt gennemførte Shopify-ordrer, f.eks. ordrer, der kun indeholder et gavekort, eller som allerede er håndteret i Shopify, oprettes **salgsfakturaen**.

Der er nu oprettet et salgsdokument, som kan administreres vha. standard [!INCLUDE[prod_short](../includes/prod_short.md)]-funktionerne.

### <a name="manage-missing-customers"></a>Administrer manglende kunder

Hvis dine indstillinger forhindrer, at der oprettes en kunde automatisk, og der ikke findes en korrekt eksisterende kunde, kan du manuelt tildele en kunde en Shopify-ordre. Der er et par indstillinger:

- Du kan knytte feltet **Sælg til kundenr.** direkte i **Shopify-ordren** ved at vælge en kunde på listen over eksisterende kunder.
- Du kan vælge en debitorskabelonkode, oprette og tildele debitoren via handlingen **Opret ny debitor** i **Shopify-ordren**.
- Du kan knytte en eksisterende debitor til den relaterede **Shopify-kunde** i vinduet **Shopify-kunder** og derefter vælge handlingen **Find tilknytning** i **Shopify-ordren**.

### <a name="tax-remarks"></a>Momskommentarer

Mens den importerede Shopify-ordre viser oplysninger om moms, bliver momsen genberegnet, når du opretter et salgsdokument. Det er derfor vigtigt, at moms- og skatteindstillingerne er korrekte i [!INCLUDE[prod_short](../includes/prod_short.md)].

- Flere momssatser/momssatser. Nogle produktkategorier er f. eks. ansvarlige for reducerede skatte satser. Disse varer skal findes i [!INCLUDE[prod_short](../includes/prod_short.md)] og knyttes til Shopify-produkterne. Hvis du ikke gør det, bruges momsproduktbogføringsgruppen automatisk med automatisk oprettelse af manglende varer.

- Adresse-afhængige momssatser. Brug feltet **Skatteområdeprioritet** sammen med tabellen **Debitorskabeloner** til at overskrive standardlogik, som udfyldes i **Skatteområdekode** i salgsdokumentet. Feltet **skatteområde-prioritet** angiver den prioritet, hvor funktionen skal indeholde oplysninger om land/område og stat/provins. Derefter bliver den tilsvarende post i Shopify-debitorskabelonen fundet, og **Skatteområdekode**, **Skattepligtig moms** og **Momsvirksomheds bogføringsgruppe** bruges, når der oprettes et salgsdokument.

## <a name="synchronize-shipments-to-shopify"></a>Synkronisere leverancer til Shopify

Når en salgsordre, der er oprettet fra en Shopify-ordre, bliver leveret, kan du synkronisere leverancerne til Shopify.

1. Gå til søgning ![Lightbulb, der åbner funktionen Fortæl mig.](../media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **Synkronisere forsendelser til Shopify**, og vælg derefter det relaterede link.
2. Definer eventuelt filtre for forsendelser. Du kan f. eks. opdatere forsendelse, der er bogført på en bestemt dato.
3. Vælg knappen **OK**.

Ordren i Shopify bliver markeret som opfyldt. Kunden modtager automatisk en e-mail med leveringsbemærkninger eller tekstmeddelelse (SMS). Hvis der er angivet en speditør og en sporingskode i leverancen, medtages sporingsoplysningerne i e-mailen.

> [!NOTE]  
> Husk at køre **Synkroniser ordre fra Shopify** for at opdatere opfyldelses status for ordre i [!INCLUDE[prod_short](../includes/prod_short.md)]. Connector-funktionen arkiverer også fuldt indbetalte og befriede ordrer både i Shopify og [!INCLUDE[prod_short](../includes/prod_short.md)], hvis betingelserne er opfyldt.

### <a name="shipping-agents-and-tracking-url"></a>Speditører og sporing af URL-adresse

Hvis det **bogførte salgsleverance**-dokument indeholder **Speditørkode** og/eller **Pakkesporingsnummer**, sendes disse oplysninger til Shopify og frem til slutdebitoren i bekræftelsesmailen.

Opfølgningsregnskab udfyldes på grundlag af speditørposten med følgende prioriteter (fra højeste til laveste):

- **Shopify Sporingsvirksomhed**
- **Navn**
- **Kode**

Hvis feltet **Pakkesporings-URL** er udfyldt for speditørposten, vil levering også indeholde en URL-adresse til sporing.

## <a name="gift-cards"></a>Gavekort

I Shopify-butikken kan du sælge gavekort, som kan bruges til at betale for reelle produkter senere.

Når du håndterer gavekort, er det vigtigt at angive en værdi i feltet **Konto for solgte gavekort** i vinduet **Shopify-butikskort**. Det solgte gavekort synkroniseres sammen med ordrer på linje. Et udlignet gavekort indlæses også sammen med ordren, men nu som en transaktion. Bemærk, at gavekortet ikke reducerer det beløb, der skal faktureres.

Hvis du vil se det udstedte og anvendte gavekort, skal du vælge den ![Lightbulb, der åbner funktionen Fortæl mig.](../media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, angiv **Gavekort**, og vælg derefter det relaterede link.

## <a name="transactions"></a>Transaktioner

De betalingstransaktioner, der er foretaget ved Shopify, synkroniseres sammen med ordrerne og kan ses fra *Shopify-ordren*.

Hvis du vil se alle transaktioner, skal du vælge søg ![Lightbulb, der åbner funktionen Fortæl mig.](../media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **Transaktioner**, og vælg derefter det relaterede link.

## <a name="payouts"></a>Udbetalinger

Hvis din butik har Shopify Payments aktiveret, modtager du betalinger via *Shopify-udbetalinger*, når en kunde betaler vha Shopify Payments og accelererede checks.

1. Gå til søgning ![Lightbulb, der åbner funktionen Fortæl mig.](../media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **Shopify Butik**, og vælg det relevante link.
2. Marker den butik, som du vil synkronisere udbetalinger til for at åbne siden **Shopify-butikskort**.
3. Vælg handlingen **Synkroniser udbetalinger**.

Hvis du vil se alle udbetalinger, skal du vælge ![Lightbulb, der åbner funktionen Fortæl mig.](../media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **Udbetalinger**, og vælg derefter det relaterede link.

## <a name="see-also"></a>Se også

[Kom i gang med Connectoren til Shopify](get-started.md)  
