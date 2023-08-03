---
title: Synkronisere debitorer
description: Importere debitorer fra eller eksportere til Shopify
ms.date: 06/06/2023
ms.topic: article
ms.service: dynamics365-business-central
ms.search.form: '30105, 30106, 30107, 30108, 30109,'
author: andreipa
ms.author: andreipa
ms.reviewer: bholtorf
---

# <a name="synchronize-customers"></a>Synkronisere debitorer

Når en ordre importeres fra Shopify, er oplysningerne om debitor nødvendig for at kunne behandle dokumentet yderligere i [!INCLUDE[prod_short](../includes/prod_short.md)]. Der findes to hovedindstillinger for dette og flere kombinationer:

* Brug speciel kunde til alle ordrer.
* Importer oplysninger om den aktuelle kunde fra Shopify. Denne indstilling er også tilgængelig, når du eksporterer debitorer til Shopify fra [!INCLUDE[prod_short](../includes/prod_short.md)] først.

## <a name="important-settings-when-importing-customers-from-shopify"></a>Vigtige indstillinger, når du importerer debitorer fra Shopify

Uanset om du masseimporterer debitorer fra Shopify eller importerer ordrer, skal du bruge følgende indstillinger til at administrere processen:

|Felt|Beskrivlse|
|------|-----------|
|**Debitorimport fra Shopify**|Vælg **Alle debitorer**, hvis du planlægger at masseimportere debitorer Shopify - enten manuelt ved hjælp af **Synkroniser kunder** eller via jobkø for tilbagevendende opdateringer. Uanset valget vil kundeoplysningerne altid blive importeret sammen med ordren. Brugen af disse oplysninger afhænger imidlertid af **Shopify Kundeskabelonerne** og indstillinger i feltet **Debitortilknytningstype**.|
|**Type af debitortilknytning**|Definer, hvordan connectoren tilknytningen skal udføre tilknytningen.<br>- **Via mail/telefon**, hvis du ønsker, at forbindelsen skal knyttes fra den importerede Shopify Debitor til en eksisterende kunde i [!INCLUDE[prod_short](../includes/prod_short.md)] via e-mail og Phone.</br>- **Ved Bill-To oplysninger**, hvis connectoren skal bruge adressen til fakturamodtageren tilknyttet til den importerede Shopify-kunde til en eksisterende debitor i [!INCLUDE[prod_short](../includes/prod_short.md)] ved hjælp af adresseoplysninger for den part, som modtager fakturaen.</br>- Vælg **Brug altid standard debitor**, hvis systemet skal bruge en debitor fra feltet **Debitornr.** . |
|**Shopify kan opdatere debitorer**| Marker dette felt, hvis du vil have connectoren til at opdatere kunder, der er fundet, når indstillingerne **pr. e-mail/telefon** eller **pr. faktureringsoplysninger** er valgt i feltet **Debitortilknytningstype**.|
|**Opret automatisk ukendte debitorer**| Marker dette felt, hvis du vil have connectoren til at oprette manglende kunder, når indstillingerne **pr. e-mail/telefon** eller **pr. faktureringsoplysninger** er valgt i feltet **Debitortilknytningstype**. Der oprettes en ny kunde ved hjælp af de importerede data og **kundeskabelonkoden**, der er defineret på siden med **Shopify butikskort** eller **Shopify debitorskabeloner**. Bemærk, at Shopify-debitor skal have mindst én adresse. Ordrer, der er oprettet via salgskanalen Shopify POS, mangler ofte adressedetaljer. Hvis denne indstilling ikke er aktiveret, skal du oprette debitoren manuelt og knytte den til Shopify-kunden.|
|**Debitorskabelonkode**|Dette felt bruges sammen med **automatisk oprettelse af ukendte kunder**.<br>- Vælg den standardskabelon, der skal bruges til automatisk oprettede debitorer. Kontroller, at den valgte skabelon indeholder de obligatoriske felter, f. eks. **Virksomhedsbogføringsgruppe**, **Debitorbogføringsgruppe** og moms- eller skatterelaterede felter.<br>- Du kan definere skabeloner pr. land/område på siden **Shopify debitorskabeloner**, som er nyttige i forbindelse med beregning af den relevante afgift. <br>- Få flere oplysninger [Konfigurere moms](setup-taxes.md).|

### <a name="customer-template-per-countryregion"></a>Debitorskabelon pr. land/område

Nogle indstillinger kan defineres på lande/regionalt niveau eller på niveauet stat/provins. Indstillingerne kan konfigureres i [Forsendelse og levering](https://www.shopify.com/admin/settings/shipping) på Shopify.

Du kan gøre følgende for hver kunde ved hjælp af **Shopify -kundeskabelonen**:

1. Angiv **Standardkundenr.**, som har højere prioritet end det, du har valgt i felterne **Debitorimport fra Shopify** og **Debitortilknytningstype**. Den bruges i den importerede salgsordre.
2. Definer den **debitorskabelonkode**, der bruges til at oprette manglende kunder, hvis **Automatisk oprettelse af ukendte debitorer** er aktiveret. Hvis **debitorskabelonkode** er tom, bruger funktionen den **debitorskabelonkode**, der er defineret på **Shopify butikskortet**. Systemet prøver først at finde en skabelon til **lande-/områdekoden** for standardadressen. Hvis der ikke findes en skabelon, bruges den første adresse.
3. I nogle tilfælde er den **debitorskabelonkode**, der er defineret for et land/område, ikke nok til at sikre, at moms beregnes korrekt (f. eks. lande/områder med moms). I dette tilfælde kan **momsområderne** være nyttige.
4. Feltet **skatteområde** indeholder også en **landekode** og et **Navn på region**. Dette par er praktisk, når forbindelsen skal konvertere en kode til et navn, eller omvendt.

> [!NOTE]  
> Landekoderne er ISO 3166-1 Alfa-2-landekoder. Flere oplysninger om [Landekode](https://help.shopify.com/en/api/custom-storefronts/storefront-api/reference/enum/countrycode).

## <a name="export-customers-to-shopify"></a>Eksportér debitorer til Shopify

Eksisterende kunder kan masseeksporteres til Shopify. I hvert tilfælde oprettes der en kunde og en standardadresse. Du kan bruge følgende indstillinger til at administrere processen:

|Felt|Beskrivlse|
|------|-----------|
|**Eksportér debitorer til Shopify**|Vælg, om du vil masseeksportere alle debitorer fra [!INCLUDE[prod_short](../includes/prod_short.md)] til Shopify. Du kan enten gøre det manuelt ved at bruge handlingen **Synkroniser debitorer** eller automatisk ved hjælp af en opgavekø til tilbagevendende opdateringer.<br> Når du eksporterer kunder med adresser, der omfatter provinser/stater, skal du sørge for, at **ISO-kode** er angivet for lande/områder.|
|**Kan opdatere Shopify debitorer**|Denne indstilling bruges sammen med indstillingen **Eksporter debitorer til Shopify**. Aktiver den, hvis du vil oprette opdateringer senere fra [!INCLUDE[prod_short](../includes/prod_short.md)] til debitorer, der allerede findes i Shopify.|

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

En debitor i Shopify har et fornavn, et efternavn, en mailadresse og/eller et telefonnummer. Du kan udfylde fornavn og efternavn baseret på dataene fra debitorkortet i [!INCLUDE[prod_short](../includes/prod_short.md)].

|Prioritet|Felt i debitorkortet|Beskrivelse|
|------|------|-----------|
|1|**Kontaktnavn**|Højeste prioritet, hvis feltet **kontaktnavn** er udfyldt, og feltet **kontaktkilde** på **Shopify produktionskortet** indeholder *Fornavn og efternavn* eller *Efternavn og fornavn*, der definerer, hvordan værdierne skal opdeles.|
|2|**Navn 2**|Hvis feltet **Navn 2** er udfyldt, og feltet **Navn 2-kilde** på **Shopify-butikskort** indeholder indstillingen *Fornavn og efternavn* eller *Efternavn og fornavn*, defineres det hvordan værdierne skal opdeles.|
|3|**Navn**|Laveste prioritet, hvis feltet **kontaktnavn** er udfyldt, og feltet **Navnekilde** på **Shopify produktionskortet** indeholder *Fornavn og efternavn* eller *Efternavn og fornavn*, der definerer, hvordan værdierne skal opdeles.|

En debitor i Shopify har også en standardadresse. Ud over fornavn, efternavn, mailadresse og/eller telefonnummer kan adressen indeholde et firma og en adresse. Feltet **Firma** kan udfyldes på basis af data fra debitorkortet i [!INCLUDE[prod_short](../includes/prod_short.md)].

|Prioritet|Felt i debitorkortet|Beskrivelse|
|------|------|-----------|
|1|**Navn**|Højeste prioritet, hvis feltet **Navnekilde** på **Shopify Produktionskortet** indeholder *Firmanavn*.|
|2|**Navn 2**|Laveste prioritet, hvis feltet **Navn 2-kilde** i **Shopify Produktionskortet** indeholder *Firmanavn*.|

I forbindelse med adresser, hvor land/provins anvendes, skal du vælge **Kode** eller **Navn** i feltet **Navn på amt** på siden **Shopify Butikskort**. Koden eller navnet angiver den type data, der er gemt i [!INCLUDE[prod_short](../includes/prod_short.md)] i feltet **Land**. Husk at initialisere kundeskabeloner pr. land/område, så lande/områdekode/navnetilknytning er klar. 


## <a name="sync-customers"></a>Synkronisere debitorer

1. Vælg ![Lightbulb, der åbner funktionen Fortæl mig 1.](../media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **Shopify butik**, og vælg derefter det relaterede link.
2. Marker den butik, som du vil synkronisere debitorer til.
3. Vælg handlingen **Synkroniser debitorer**.

Du kan også bruge handlingen **Start debitorsynkronisering** i vinduet **Shopify Debitorer** eller Søg efter **Synkroniseringsdebitorer**.

Du kan planlægge, at følgende tilbagevendende aktiviteter skal udføres automatisk. Få mere at vide, når du [planlægger tilbagevendende opgaver](background.md#to-schedule-recurring-tasks).

## <a name="see-also"></a>Se også

[Kom i gang med Connectoren til Shopify](get-started.md)  
