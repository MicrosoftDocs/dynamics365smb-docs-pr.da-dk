---
title: Synkronisere og transaktioner og udbetalinger
description: Konfigurere og køre import af transaktioner og udbetalinger fra Shopify.
ms.date: 05/27/2022
ms.topic: article
ms.service: dynamics365-business-central
ms.search.form: 30124, 30125, 30130, 30131, 30132, 30133, 30134,
author: edupont04
ms.author: andreipa
ms.reviewer: solsen
ms.openlocfilehash: f4833a3fa77cdff587947a9686e61e3255b66a7c
ms.sourcegitcommit: 5bb13966e9ba8d7a3c2f00dd32f167acccf90b82
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 10/28/2022
ms.locfileid: "9728716"
---
# <a name="transactions-and-payouts"></a>Transaktioner og udbetalinger

Når en kunde har færdiggjort check ud i onlinebutikken, gemmes oplysningerne om betalinger som en **transaktion**. Der kan være knyttet flere transaktioner til ordren, f. eks. Når en kunde bruger et gavekort til at betale noget af omkostningerne og derefter bruger et kreditkort eller en PayPal til restbeløbet.

Hvis du bruger Shopify-betaling som betalingsudbyder og derefter ud over oplysninger om de penge, som Betalingsudbyderen har modtaget fra kunden, kan du også få vist udbetalinger fra Shopify til din bankkonto.

## <a name="transactions"></a>Transaktioner

De betalingstransaktioner, der er foretaget i Shopify synkroniseres sammen med ordrerne og kan ses på siden **Shopify-ordrer**.

Hvis du vil se alle transaktioner, skal du vælge ![Lightbulb, der åbner funktionen Fortæl mig 1.](../media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **Transaktioner**, og vælg derefter det relaterede link.

Hvis du har konfigureret tilknytning af en betalingsmetode, er der tildelt en betalingsmetode kode i det oprettede salgsdokument. Få mere at vide ved [betalingsmetodetilknytning](#payment-method-mapping).

## <a name="payouts"></a>Udbetalinger

Hvis din butik har Shopify Payments aktiveret, modtager du betalinger via **Shopify-udbetalinger**, når en kunde betaler vha Shopify Payments og accelererede checks.

1. Vælg ![Lightbulb, der åbner funktionen Fortæl mig 1.](../media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **Shopify Shops**, vælg derefter det relaterede link.
2. Marker den butik, som du vil synkronisere udbetalinger til for at åbne siden **Shopify-butikskort**.
3. Vælg handlingen **Synkroniser udbetalinger**.

Hvis du vil se alle udbetalinger, skal du vælge ![Lightbulb, der åbner funktionen Fortæl mig.](../media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **Udbetalinger**, og vælg derefter det relaterede link.

**Udbetalinger** er kun til orientering og påvirker ikke finans-eller bank poster, men de kan være nyttige, når du skal behandle bankkontoudtoget.

## <a name="payment-method-mapping"></a>Tilknytning af betalingsmetode

Hvis du vil udfylde **betalingsmetodekoden** automatisk for salgsdokumenter, der er importeret fra Shopify, skal du konfigurere **tilknytning af betalingsmetode**.

1. Vælg ![Lightbulb, der åbner funktionen Fortæl mig 1.](../media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **Shopify Shops**, vælg derefter det relaterede link.
2. Marker den butik, som du vil definere en tilknytning til for at åbne **Shopify Butikskort**-siden.
3. Vælg handlingen **Tilknytning af betalingsmetode**.
4. Indtast navnet på betalingsmetoden i felterne **Gateway** og **Kreditkortfirma** fra Shopify. Posterne oprettes automatisk, når du importerer Shopify-ordrer.
5. Indtast **Betalingsmetodekoden** med den tilsvarende betalingsmetode i [!INCLUDE[prod_short](../includes/prod_short.md)].
6. Angiv **prioritet** for sager, når debitor bruger flere betalingsmidler. Betalingsmetoden med den højeste prioritet bliver valgt i salgsdokumentet. Hvis begge betalingsmetoder har samme prioritet, bruges betalingsmetoden med det højeste beløb.

> [!NOTE]  
> Hvis den tilsvarende betalingsmetode i [!INCLUDE[prod_short](../includes/prod_short.md)] har **Modkonto type** og **Modkonto** udfyldt, vil fakturasystemet under bogføringen, oprette en modpost af *betaling*-typen og udligne den med *faktura*-typen i debitorposten.

## <a name="use-cases"></a>Bruge sager
  
Parter:

* Køber – person, der køber varer fra Shopify-onlinebutikken.
* Forhandler - din virksomhed.
* Betalingsformidler - virksomhed, der håndterer betaling for dig. Kan være Shopify Payments eller en tredjepart.

### <a name="how-money-flows"></a>Sådan er pengestrømmen

Køberen køber varer i onlinebutikker. Den sidste fase er at gennemføre betaling.

>[!NOTE]
> Dette eksempel dækker ikke sager, hvor betalingen er fuldført uden for Shopify-udlevering, hvilket er gyldigt i B2B-scenarier.
  
Køberen betaler med kreditkort, PayPal eller en lokal betalingsmetode som MobilePay i Danmark. Betalingsformidleren tager det fulde beløb fra køberen. På dette tidspunkt er købernes penge blevet flyttet til betalingsformidleren.

Afhængigt af betalingsformidleren kan forhandleren se disse penge på deres konto hos betalingsformidleren - både modtagne beløb samt fratrukket provision. Betalingsformidlere får ofte en provision fra hver transaktion, og i nogle tilfælde kan de også have et fast gebyr.
  
Afhængigt af betalingsformidleren udløser forhandleren enten en overførsel af pengene til sin bankkonto (udbetaling) manuelt, eller det sker automatisk inden for en defineret periode – én gang pr. dag, én gang om måneden osv.
  
Afhængigt af banken kan forhandleren se den indgående transaktion på deres bankkonto via online bank eller i bankens kontoudtog.

Der er flere indstillinger til håndtering af betalingstransaktioner i [!INCLUDE[prod_short](../includes/prod_short.md)]
  
### <a name="option-1-reconcile-incoming-transfers-to-bank-account-against-original-invoices"></a>Mulighed 1: afstemme indgående overførsler til bankkonto mod oprindelige fakturaer
  
Forhandlerens importerer salgsordre til [!INCLUDE[prod_short](../includes/prod_short.md)] og bogfører levering og faktura.

Resultat: systemet opretter en **Debitorpost** af typen *faktura* med det fulde beløb, feltet **Åben** er angivet til Ja. Det **Resterende beløb** svarer til det fakturerede beløb.

Forhandleren importerer bankkontoudtog vha. betalingsudligningskladde.

Fejl:

1. Kan være vanskelig, hvis der er flere fakturaer (og kreditnotaer), men en udbetaling fra betalingsudbyderen med et engangsbeløb.
2. Beløb stemmer som regel ikke overens med provisionen. Du kan bruge betalingstolerance eller/eller kontantrabat til at håndtere gebyrer.

### <a name="option-2-reconcile-incoming-transfers-to-bank-account-against-interim-account-representing-money-at-the-payment-provider"></a>Mulighed 2: afstemme indgående overflytninger til bankkonto mod mellemkonto, der repræsenterer penge hos betalingsudbyderen
  
Forhandlerens importerer salgsordre til [!INCLUDE[prod_short](../includes/prod_short.md)] og bogfører levering og faktura.
  
Resultat: systemet opretter en debitorpost af typen **Faktura** med det fulde beløb, feltet **Åben** er angivet til Ja. Det **Resterende beløb** svarer til det fakturerede beløb.

Men da salgsordren har en betalingsmetodekode, hvor felterne **Modkontotype** og **Modkontonummer** er udfyldt, oprettes der automatisk en anden debitorpost af typen **Betaling**, og den udlignes med den tidligere oprettede debitorpost.

>[!NOTE]
> Feltet Betalingsmetodekode udfyldes automatisk på grundlag af betalingsmetodetilknytning. Få mere at vide ved [betalingsmetodetilknytning](#payment-method-mapping).
  
Du kan definere modkonti til betalingsmetoder på to måder:

* **Modkontotype** angives som *Bank* og **Modkontonr.** udfylder den særlige bankkonto, der repræsenterer kontoen hos betalingsudbyderen.
* **Modkontotype** angives som *Finanskonto** og **Modkontonr.** udfylder den særlige finanskonto, der repræsenterer kontoen hos betalingsudbyderen.

Det giver mening at bruge en bankkonto, hvis betalingsudbyderen udlæser noget kontoudtog, som du kan indlæse i betalingsafstemningskladden.

Forhandleren importerer bankkontoudtog vha. betalingsudligningskladde. Den indgående betaling kan behandles:

* Som en overførsel fra en anden bank. Hvis overførslen tager nogle få dage eller indebærer valutaveksling, skal du muligvis bruge en midlertidig finanskonto.
* Som en difference på den finanskonto, der repræsenterer din konto hos betalingsudbyderen.
  
Den resterende saldo på den finanskonto eller bankkonto, der repræsenterer din konto hos betalingsudbyderen, kan afskrives som "gebyrer/provision"

Fejl:

1. Du kan oprette flere finanskontonumre eller bankkonti, hvis du har flere betalingsudbydere. Salgsordrer [!INCLUDE[prod_short](../includes/prod_short.md)] understøtter dog kun én betalingsmetodekode, hvilket gør det vanskeligt at håndtere sager, når en kunde bruger flere betalingsmetoder til en ordre.

## <a name="see-also"></a>Se også

[Kom i gang med Connectoren til Shopify](get-started.md)  
