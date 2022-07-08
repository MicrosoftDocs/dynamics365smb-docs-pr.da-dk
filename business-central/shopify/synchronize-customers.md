---
title: Synkronisere debitorer
description: Importere debitorer fra eller eksportere til Shopify
ms.date: 05/27/2022
ms.topic: article
ms.service: dynamics365-business-central
author: edupont04
ms.author: andreipa
ms.reviewer: solsen
ms.openlocfilehash: c5a77e5258f4d70a35a1751ff01dc210210b3a6e
ms.sourcegitcommit: 00a8acc82cdc90e0d0db9d1a4f98a908944fd50a
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 06/29/2022
ms.locfileid: "9077784"
---
# <a name="synchronize-customers"></a>Synkronisere debitorer

Når en ordre indlæses fra Shopify, er oplysningerne om debitor nødvendig for at kunne behandle dokumentet yderligere i [!INCLUDE[prod_short](../includes/prod_short.md)]. Der findes to hovedindstillinger og deres kombinationer:

* Brug speciel kunde til alle ordrer.
* Importer oplysninger om den aktuelle kunde fra Shopify. Denne indstilling er også tilgængelig, når du eksporterer debitorer til Shopify fra [!INCLUDE[prod_short](../includes/prod_short.md)] først.

## <a name="how-the-connector-chooses-which-customer-to-use"></a>Hvordan connectoren vælger, hvilken kunde der skal bruges

Funktionen *Importer ordre fra Shopify* forsøger at vælge debitoren i følgende rækkefølge:

1. Hvis **Standarddebitornr.** feltet er defineret i **Shopify Debitorskabelonen** for det tilsvarende land, så anvendes **Standarddebitornr.** uanset indstillingerne i felterne **Debitorimport fra Shopify** og **Debitortilknytningstype**. Du kan finde flere oplysninger i afsnittet [Debitorskabelon pr. land](synchronize-customers.md#customer-template-per-country).
2. Hvis **Debitorimport fra Shopify** er indstillet til *Ingen* og **Standarddebitornr.** er defineret i **Shopify Butikskort** skal **Standarddebitornr.** .

Næste trin afhænger af **Debitortilknytningstype**.

* **Hent altid standardkunden**, og connectoren bruger derefter kunden, som er defineret i feltet **Standarddebitornr.** feltet på siden **Shopify Køb kort**.
* **Via mail/telefon** forsøger connectoren først at finde eksisterende kunder efter id, derefter pr. e-mail og derefter pr. telefon. Hvis debitoren ikke findes-connectoren opretter en ny kunde.
* **Ved faktureringsoplysninger** forsøger connectoren først at finde den eksisterende debitor efter id og derefter efter faktureringsadresseoplysninger. Hvis den ikke findes-connectoren opretter en ny kunde.

> [!NOTE]  
> Connectoren bruger oplysninger fra faktureringsadressen og opretter en faktureringskunden i [!INCLUDE[prod_short](../includes/prod_short.md)]. Kunden er lig med faktureres til kunde.

## <a name="important-settings-when-importing-customers-from-shopify"></a>Vigtige indstillinger, når du importerer debitorer fra Shopify

Du kan enten masseimportere debitorer fra Shopify eller sammen med importen af ordrer, men følgende indstillinger giver dig mulighed for at administrere processen:

|Felt|Beskrivelse|
|------|-----------|
|**Debitorimport fra Shopify**|Vælg **Alle debitorer**, hvis du planlægger at masseimportere debitorer Shopify - enten manuelt ved hjælp af **Synkroniser kunder** eller via jobkø for tilbagevendende opdateringer. Uanset valget vil kundeoplysningerne altid blive importeret sammen med ordren. Brugen af disse oplysninger afhænger imidlertid af **Shopify Kundeskabelonerne** og indstillinger i feltet **Debitortilknytningstype**.|
|**Type af debitortilknytning**|Definer, hvordan connectoren tilknytningen skal udføre tilknytningen.<br>- **Via mail/telefon**, hvis du ønsker, at forbindelsen skal knyttes fra den importerede Shopify Debitor til en eksisterende kunde i [!INCLUDE[prod_short](../includes/prod_short.md)] via e-mail og Phone.</br>- **Ved Bill-To oplysninger**, hvis du vil knytte den importerede Shopify Kunde til en eksisterende debitor i [!INCLUDE[prod_short](../includes/prod_short.md)] ved hjælp af adresseoplysninger for den part, som modtager fakturaen.</br>Vælg **Brug altid standard debitor**, hvis systemet skal bruge en debitor fra feltet **Debitornr.** . |
|**Shopify kan opdatere debitorer**| Marker dette felt, hvis du vil have connectoren til at opdatere kunder, der er fundet, når indstillingerne **pr. e-mail/telefon** eller **pr. faktureringsoplysninger** er valgt i feltet **Debitortilknytningstype**.|
|**Opret automatisk ukendte debitorer**| Marker dette felt, hvis du vil have connectoren til at oprette manglende kunder, når indstillingerne **pr. e-mail/telefon** eller **pr. faktureringsoplysninger** er valgt i feltet **Debitortilknytningstype**. Der oprettes en ny kunde ved hjælp af de importerede data og **kundeskabelonkoden**, der er defineret på siden med **Shopify butikskort** eller **Shopify debitorskabeloner**. Bemærk, at Shopify-debitor skal have mindst én adresse. Hvis denne indstilling ikke er aktiveret, skal du oprette debitoren manuelt og knytte den til Shopify-kunden. Du kan altid oprette en kunde manuelt fra siden **Shopify Ordrer**.|
|**Debitorskabelonkode**|Bruges sammen med **automatisk oprettelse af ukendte kunder**.<br> Vælg den standardskabelon, der skal bruges til automatisk oprettede debitorer. Kontroller, at den valgte skabelon indeholder de obligatoriske felter, f. eks. **Virksomhedsbogføringsgruppe**, **Debitorbogføringsgruppe**, moms eller skatterelaterede felter.<br> Du kan definere skabeloner pr. land/område på siden **Shopify debitorskabeloner**, som er nyttige i forbindelse med beregning af den relevante afgift. Du kan finde flere oplysninger i [Momskommentarer](synchronize-orders.md#tax-remarks).|

### <a name="customer-template-per-country"></a>Debitorskabelon pr. land

Nogle indstillinger kan defineres på land/regionalt niveau eller på niveauet stat/provins. Indstillingerne kan konfigureres i [Forsendelse og levering](https://www.shopify.com/admin/settings/shipping) på Shopify.

Med **Shopify kundeskabelonen** kan du gøre følgende for hvert land:

1. Angiv **Standardkundenr.**, som har højere prioritet end det, du har valgt i felterne **Debitorimport fra Shopify** og **Debitortilknytningstype**. Den bruges i den importerede salgsordre.
2. Definer den **debitorskabelonkode**, der bruges til at oprette manglende kunder, hvis **Automatisk oprettelse af ukendte debitorer** er aktiveret. Hvis **debitorskabelonkode** er tom, bruger funktionen den **debitorskabelonkode**, der er defineret på **Shopify butikskortet**.
3. I nogle tilfælde er **Kundeskabelonkode** defineret for land ikke nok til at sikre, at skat beregnes direkte. F. eks. for lande med moms. I dette tilfælde kan **skatteområderne** være nyttige.

> [!NOTE]  
> Landekoderne er ISO 3166-1 Alfa-2-landekoder. Du kan finde flere oplysninger på [Landekode](https://help.shopify.com/en/api/custom-storefronts/storefront-api/reference/enum/countrycode).

## <a name="export-customers-to-shopify"></a>Eksportér debitorer til Shopify

Eksisterende kunder kan masseeksporteres til Shopify. Det betyder, at der oprettes en kunde og en standardadresse. Du kan administrere processen ved hjælp af følgende indstillinger:

|Felt|Beskrivelse|
|------|-----------|
|**Eksportér debitorer til Shopify**|Vælg, hvis du planlægger at masseeksportere alle debitorer med en gyldig e-mailadresse fra [!INCLUDE[prod_short](../includes/prod_short.md)] til Shopify ved hjælp af **Synkroniser debitorer** eller via en jobkø til tilbagevendende opdateringer.|
|**Kan opdatere Shopify debitorer**|Bruges sammen med indstillingen **Eksporter debitorer til Shopify**. Aktiver den, hvis du vil oprette opdateringer senere fra [!INCLUDE[prod_short](../includes/prod_short.md)] til debitorer, der allerede findes i Shopify.|

> [!NOTE]  
> Når du har oprettet debitorer i Shopify, kan du sende direkte mødeindkaldelser til kunderne. Den opfordrer dem til at aktivere deres konto.

### <a name="populate-customer-information-in-shopify"></a>Udfyld kundeoplysninger i Shopify

En kunde i Shopify har fornavn, efternavn, mail og/eller telefonnummer. Du kan udfylde fornavn og efter navn baseret på dataene fra debitorkortet i [!INCLUDE[prod_short](../includes/prod_short.md)].

|Prioritet|Felt i Debitorkort|Beskrivelse|
|------|------|-----------|
|1|**Kontaktnavn**|Højeste prioritet, hvis feltet **kontaktnavn** er udfyldt, og feltet **kontaktkilde** på **Shopify produktionskortet** indeholder *Fornavn og efternavn* eller *Efternavn og fornavn*, der definerer, hvordan værdierne skal opdeles.|
|2|**Navn 2**|Hvis feltet **Navn 2** er udfyldt, og feltet **Navn 2-kilde** på **Shopify produktionskortet** indeholder *Fornavn og efternavn* eller *Efternavn og fornavn*, defineres hvordan værdierne skal opdeles.|
|3|**Navn**|Laveste prioritet, hvis feltet **kontaktnavn** er udfyldt, og feltet **Navnekilde** på **Shopify produktionskortet** indeholder *Fornavn og efternavn* eller *Efternavn og fornavn*, der definerer, hvordan værdierne skal opdeles.|

En kunde i Shopify har også en standardadresse, som ud over fornavn, efter navn, e-mail-adresse og/eller telefon kan indeholde firma og adresse. feltet **Firma** kan udfyldes på basis af data fra debitorkortet i [!INCLUDE[prod_short](../includes/prod_short.md)].

|Prioritet|Felt i Debitorkort|Beskrivelse|
|------|------|-----------|
|1|**Navn**|Højeste prioritet, hvis feltet **Navnekilde** på **Shopify Produktionskortet** indeholder *Firmanavn*.|
|2|**Navn 2**|Laveste prioritet, hvis feltet **Navn 2-kilde** i **Shopify Produktionskortet** indeholder *Firmanavn*.|

I forbindelse med adresser, hvor lande/provins anvendes, skal du vælge *Kode* eller *Navn* i feltet **Landekilde** på **Shopify Produktionskortet** for at angive, hvilken type data der skal gemmes [!INCLUDE[prod_short](../includes/prod_short.md)] i feltet **Land**.

## <a name="sync-customers"></a>Synkronisere debitorer

1. Vælg ![Lightbulb, der åbner funktionen Fortæl mig 1.](../media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **Shopify Shop**, og vælg derefter det relaterede link.
2. Marker den butik, som du vil synkronisere debitorer til for at åbne **Shopify Shop-kort**-siden.
3. Vælg handlingen **Synkroniser debitorer**.

Du kan også bruge handlingen **Start debitorsynkronisering** i vinduet **Shopify Debitorer** eller Søg efter **Synkroniseringsdebitorer**.

Du kan planlægge, at følgende tilbagevendende aktiviteter skal udføres automatisk. Du kan finde flere oplysninger i [Planlægge gentagne opgaver](background.md#to-schedule-recurring-tasks).

## <a name="see-also"></a>Se også

[Kom i gang med Connectoren til Shopify](get-started.md)  