---
title: Synkronisere debitorer
description: Importere debitorer fra eller eksportere til Shopify
ms.date: 05/27/2022
ms.topic: article
ms.service: dynamics365-business-central
ms.search.form: 30105, 30106, 30107, 30108, 30109,
author: edupont04
ms.author: andreipa
ms.reviewer: solsen
ms.openlocfilehash: 1a796d1094401cd2ebc0efd54f752211d22bfb12
ms.sourcegitcommit: 5bb13966e9ba8d7a3c2f00dd32f167acccf90b82
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 10/28/2022
ms.locfileid: "9728649"
---
# <a name="synchronize-customers"></a>Synkronisere debitorer

Når en ordre indlæses fra Shopify, er oplysningerne om debitor nødvendig for at kunne behandle dokumentet yderligere i [!INCLUDE[prod_short](../includes/prod_short.md)]. Der findes to hovedindstillinger og deres kombinationer:

* Brug speciel kunde til alle ordrer.
* Importer oplysninger om den aktuelle kunde fra Shopify. Denne indstilling er også tilgængelig, når du eksporterer debitorer til Shopify fra [!INCLUDE[prod_short](../includes/prod_short.md)] først.

## <a name="important-settings-when-importing-customers-from-shopify"></a>Vigtige indstillinger, når du importerer debitorer fra Shopify

Uanset om du masseimporterer debitorer fra Shopify eller sammen med importen af ordrer, men følgende indstillinger giver dig mulighed for at administrere processen:

|Felt|Beskrivelse|
|------|-----------|
|**Debitorimport fra Shopify**|Vælg **Alle debitorer**, hvis du planlægger at masseimportere debitorer Shopify - enten manuelt ved hjælp af **Synkroniser kunder** eller via jobkø for tilbagevendende opdateringer. Uanset valget vil kundeoplysningerne altid blive importeret sammen med ordren. Brugen af disse oplysninger afhænger imidlertid af **Shopify Kundeskabelonerne** og indstillinger i feltet **Debitortilknytningstype**.|
|**Type af debitortilknytning**|Definer, hvordan connectoren tilknytningen skal udføre tilknytningen.<br>- **Via mail/telefon**, hvis du ønsker, at forbindelsen skal knyttes fra den importerede Shopify Debitor til en eksisterende kunde i [!INCLUDE[prod_short](../includes/prod_short.md)] via e-mail og Phone.</br>- **Ved Bill-To oplysninger**, hvis connectoren skal bruge adressen til fakturamodtageren tilknyttet til den importerede Shopify-kunde til en eksisterende debitor i [!INCLUDE[prod_short](../includes/prod_short.md)] ved hjælp af adresseoplysninger for den part, som modtager fakturaen.</br>- Vælg **Brug altid standard debitor**, hvis systemet skal bruge en debitor fra feltet **Debitornr.** . |
|**Shopify kan opdatere debitorer**| Marker dette felt, hvis du vil have connectoren til at opdatere kunder, der er fundet, når indstillingerne **pr. e-mail/telefon** eller **pr. faktureringsoplysninger** er valgt i feltet **Debitortilknytningstype**.|
|**Opret automatisk ukendte debitorer**| Marker dette felt, hvis du vil have connectoren til at oprette manglende kunder, når indstillingerne **pr. e-mail/telefon** eller **pr. faktureringsoplysninger** er valgt i feltet **Debitortilknytningstype**. Der oprettes en ny kunde ved hjælp af de importerede data og **kundeskabelonkoden**, der er defineret på siden med **Shopify butikskort** eller **Shopify debitorskabeloner**. Bemærk, at Shopify-debitor skal have mindst én adresse. Hvis denne indstilling ikke er aktiveret, skal du oprette debitoren manuelt og knytte den til Shopify-kunden. Du kan altid oprette en kunde manuelt fra siden **Shopify Ordrer**.|
|**Debitorskabelonkode**|Dette felt bruges sammen med **automatisk oprettelse af ukendte kunder**.<br>- Vælg den standardskabelon, der skal bruges til automatisk oprettede debitorer. Kontroller, at den valgte skabelon indeholder de obligatoriske felter, f. eks. **Virksomhedsbogføringsgruppe**, **Debitorbogføringsgruppe** og moms- eller skatterelaterede felter.<br>- Du kan definere skabeloner pr. land/område på siden **Shopify debitorskabeloner**, som er nyttige i forbindelse med beregning af den relevante afgift. <br>- Få flere oplysninger [Konfigurere moms](setup-taxes.md).|

### <a name="customer-template-per-country"></a>Debitorskabelon pr. land

Nogle indstillinger kan defineres på lande/regionalt niveau eller på niveauet stat/provins. Indstillingerne kan konfigureres i [Forsendelse og levering](https://www.shopify.com/admin/settings/shipping) på Shopify.

Du kan gøre følgende for hver kunde ved hjælp af **Shopify -kundeskabelonen**:

1. Angiv **Standardkundenr.**, som har højere prioritet end det, du har valgt i felterne **Debitorimport fra Shopify** og **Debitortilknytningstype**. Den bruges i den importerede salgsordre.
2. Definer den **debitorskabelonkode**, der bruges til at oprette manglende kunder, hvis **Automatisk oprettelse af ukendte debitorer** er aktiveret. Hvis **debitorskabelonkode** er tom, bruger funktionen den **debitorskabelonkode**, der er defineret på **Shopify butikskortet**.
3. Angiv, om priser er inkl. moms for importerede ordrer.
4. I nogle tilfælde er den **debitorskabelonkode**, der er defineret for et land, ikke nok til at sikre, at moms beregnes korrekt (f. eks. lande med moms). I dette tilfælde kan **skatteområderne** være nyttige.

> [!NOTE]  
> Landekoderne er ISO 3166-1 Alfa-2-landekoder. Flere oplysninger om [Landekode](https://help.shopify.com/en/api/custom-storefronts/storefront-api/reference/enum/countrycode).

## <a name="export-customers-to-shopify"></a>Eksportér debitorer til Shopify

Eksisterende kunder kan masseeksporteres til Shopify. I hvert tilfælde oprettes der en kunde og en standardadresse. Du kan bruge følgende indstillinger til at administrere processen:

|Felt|Beskrivelse|
|------|-----------|
|**Eksportér debitorer til Shopify**|Vælg, om du vil masseeksportere alle debitorer fra [!INCLUDE[prod_short](../includes/prod_short.md)] til Shopify. Du kan enten gøre det manuelt ved at bruge handlingen **Synkroniser debitorer** eller automatisk ved hjælp af en opgavekø til tilbagevendende opdateringer.<br> Når du eksporterer kunder med adresser, der omfatter provinser/stater, skal du sørge for, at **ISO-kode** er angivet for lande/områder.|
|**Kan opdatere Shopify debitorer**|Bruges sammen med indstillingen **Eksporter debitorer til Shopify**. Aktiver den, hvis du vil oprette opdateringer senere fra [!INCLUDE[prod_short](../includes/prod_short.md)] til debitorer, der allerede findes i Shopify.|

Der er følgende krav til eksport af en debitor:

* Kunden skal have en gyldig e-mailadresse.
* Et land/område er valgt på debitorkortet, for lokale debitorer, med et tomt land/område det land/område, der er angivet på siden **firmaoplysninger**, skal have en defineret ISO-kode.
* Hvis debitoren har et telefonnummer, skal nummeret være entydigt, da Shopify ikke accepterer en anden kunde med det samme telefonnummer.
* Hvis kunden har et telefonnummer, skal det være i formatet E.164. Forskellige formater understøttes, hvis de repræsenterer et nummer, der kan ringes op fra et vilkårligt sted i verden. Følgende formater er mulige:
  * xxxxxxxxxx
  * +xxxxxxxxxxx
  * (xxx)xxx-xxxx
  * +x xxx-xxx-xxxx

Når du har oprettet debitorerne i Shopify, kan du sende dem direkte til mødeindkaldelser for at give dem mulighed for at aktivere deres konti.

### <a name="populate-customer-information-in-shopify"></a>Udfyld kundeoplysninger i Shopify

En kunde i Shopify har fornavn, efternavn, mail og/eller telefonnummer. Du kan udfylde fornavn og efternavn baseret på dataene fra debitorkortet i [!INCLUDE[prod_short](../includes/prod_short.md)].

|Prioritet|Felt i debitorkortet|Beskrivelse|
|------|------|-----------|
|1|**Kontaktnavn**|Højeste prioritet, hvis feltet **kontaktnavn** er udfyldt, og feltet **kontaktkilde** på **Shopify produktionskortet** indeholder *Fornavn og efternavn* eller *Efternavn og fornavn*, der definerer, hvordan værdierne skal opdeles.|
|2|**Navn 2**|Hvis feltet **Navn 2** er udfyldt, og feltet **Navn 2-kilde** på **Shopify produktionskortet** indeholder *Fornavn og efternavn* eller *Efternavn og fornavn*, defineres hvordan værdierne skal opdeles.|
|3|**Navn**|Laveste prioritet, hvis feltet **kontaktnavn** er udfyldt, og feltet **Navnekilde** på **Shopify produktionskortet** indeholder *Fornavn og efternavn* eller *Efternavn og fornavn*, der definerer, hvordan værdierne skal opdeles.|

En kunde i Shopify har også en standardadresse, som ud over fornavn, efter navn, e-mail-adresse og/eller telefon kan indeholde firma og adresse. Feltet **Firma** kan udfyldes på basis af data fra debitorkortet i [!INCLUDE[prod_short](../includes/prod_short.md)].

|Prioritet|Felt i debitorkortet|Beskrivelse|
|------|------|-----------|
|1|**Navn**|Højeste prioritet, hvis feltet **Navnekilde** på **Shopify Produktionskortet** indeholder *Firmanavn*.|
|2|**Navn 2**|Laveste prioritet, hvis feltet **Navn 2-kilde** i **Shopify Produktionskortet** indeholder *Firmanavn*.|

I forbindelse med adresser, hvor lande/provins anvendes, skal du vælge *Kode* eller *Navn* i feltet **Landekilde** i **Shopify Butikskort**. Dette angiver den type data, der er gemt i [!INCLUDE[prod_short](../includes/prod_short.md)] i feltet **Land**.

## <a name="sync-customers"></a>Synkronisere debitorer

1. Vælg ![Lightbulb, der åbner funktionen Fortæl mig 1.](../media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **Shopify butik**, og vælg derefter det relaterede link.
2. Marker den butik, som du vil synkronisere debitorer til.
3. Vælg handlingen **Synkroniser debitorer**.

Du kan også bruge handlingen **Start debitorsynkronisering** i vinduet **Shopify Debitorer** eller Søg efter **Synkroniseringsdebitorer**.

Du kan planlægge, at følgende tilbagevendende aktiviteter skal udføres automatisk. Få mere at vide, når du [planlægger tilbagevendende opgaver](background.md#to-schedule-recurring-tasks).

## <a name="see-also"></a>Se også

[Kom i gang med Connectoren til Shopify](get-started.md)  
