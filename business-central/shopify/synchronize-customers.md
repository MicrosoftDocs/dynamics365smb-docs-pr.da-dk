---
title: Synkronisere debitorer
description: Importere debitorer fra eller eksportere til Shopify
ms.date: 03/25/2024
ms.topic: article
ms.service: dynamics-365-business-central
ms.search.form: '30105, 30106, 30107, 30108, 30109,'
author: brentholtorf
ms.author: bholtorf
ms.reviewer: andreipa
---

# Synkronisere debitorer og virksomheder

Når en ordre importeres fra Shopify, er oplysningerne om debitor nødvendig for at kunne behandle dokumentet yderligere i [!INCLUDE[prod_short](../includes/prod_short.md)]. Der findes to hovedindstillinger for dette og flere kombinationer:

* Brug speciel kunde til alle ordrer.
* Importer debitoroplysninger fra Shopify. Denne indstilling er også tilgængelig, når du eksporterer debitorer til Shopify fra [!INCLUDE[prod_short](../includes/prod_short.md)].

Shopify giver dig mulighed for at køre din B2B- og DTC-forretning fra ét sted med styrken og letheden i Shopifys alt i en-platform. Shopify-connectoren fungerer også med forskellige varianter af e-handel.

Shopify har to objekter, debitor og virksomhed, men [!INCLUDE[prod_short](../includes/prod_short.md)] har kun kundeobjektet, hvilket påvirker, hvordan synkronisering fungerer.

Når du kører DTC, oprettes køberen i Shopify som debitor. Debitoren importeres derefter til [!INCLUDE[prod_short](../includes/prod_short.md)] som Shopify-debitor og knyttes eller konverteres til en debitor.

Hvis du kører B2B, oprettes køberen i Shopify som en kunde, der er knyttet til en virksomhed. Debitoren importeres til [!INCLUDE[prod_short](../includes/prod_short.md)] som en Shopify-debitor, og virksomheden importeres til [!INCLUDE[prod_short](../includes/prod_short.md)] som en Shopify-virksomhed og knyttes eller konverteres til en debitor.

Hvis du vil eksportere en debitor fra [!INCLUDE[prod_short](../includes/prod_short.md)] til Shopify, er trinnene lidt forskellige, afhængigt af hvad du vil foretage dig:

* Eksportere en debitor som Shopify-debitor til DTC.
* Eksportere en debitor som en virksomhed og et debitorpar til B2B-flowet.

## Vigtige indstillinger, når du importerer DTC-debitorer fra Shopify

Uanset om du masseimporterer debitorer fra Shopify eller importerer ordrer, skal du bruge følgende indstillinger til at administrere processen:

|Felt|Beskrivlse|
|------|-----------|
|**Debitorimport fra Shopify**|Vælg **Alle debitorer**, hvis du planlægger at masseimportere debitorer Shopify - enten manuelt ved hjælp af **Synkroniser kunder** eller via jobkø for tilbagevendende opdateringer. Uanset valget vil kundeoplysningerne altid blive importeret sammen med ordren. Brugen af disse oplysninger afhænger imidlertid af **Shopify Kundeskabelonerne** og indstillinger i feltet **Debitortilknytningstype**.|
|**Type af debitortilknytning**|Definer, hvordan connectoren tilknytningen skal udføre tilknytningen.</br></br>- **Via mail/telefon**, hvis du ønsker, at connectoren skal bruge mailkonto og telefonoplysninger til at knytte den importerede Shopify-debitor til en debitor i Business Central.</br></br>- **Ved faktureringsoplysninger**, hvis connectoren skal bruge adressen til fakturamodtageren til at knytte den importerede Shopify-debitor til en eksisterende debitor i Business Central.</br></br>Vælg **Brug altid standard debitor**, hvis systemet skal bruge en debitor fra feltet **Debitornr.** . |
|**Shopify kan opdatere debitorer**| Marker dette felt, hvis du vil have connectoren til at opdatere kunder, der er fundet, når indstillingerne **pr. e-mail/telefon** eller **pr. faktureringsoplysninger** er valgt i feltet **Debitortilknytningstype**.|
|**Opret automatisk ukendte debitorer**| Marker dette felt, hvis du vil have connectoren til at oprette manglende kunder, når indstillingerne **pr. e-mail/telefon** eller **pr. faktureringsoplysninger** er valgt i feltet **Debitortilknytningstype**. Der oprettes en ny debitor ved hjælp af de importerede data og **kundeskabelonkoden**, der er defineret på siden med **Shopify-butikskort** eller **Shopify-debitorskabeloner**. Bemærk, at Shopify-debitor skal have mindst én adresse. Ordrer, der er oprettet via salgskanalen Shopify POS, mangler ofte adressedetaljer. Hvis denne indstilling ikke er aktiveret, skal du oprette debitoren manuelt og knytte den til Shopify-debitoren.|
|**Skabelonkode for debitor/virksomhed**|Brug dette felt sammen med **Opret automatisk ukendte debitorer**.</br></br> Vælg den standardskabelon, der skal bruges til automatisk oprettede debitorer. Kontroller, at den valgte skabelon indeholder de obligatoriske felter, f.eks. **Virksomhedsbogføringsgruppe**, **Debitorbogføringsgruppe** og moms- eller skatterelaterede felter.</br></br>Du kan definere skabeloner pr. land/område på siden **Shopify-debitorskabeloner**, som er nyttige i forbindelse med beregning af afgifter.</br></br>Få flere oplysninger [Konfigurere moms](setup-taxes.md).|

### Debitorskabelon pr. land/område

Nogle indstillinger kan defineres på lande/regionalt niveau eller på niveauet stat/provins. Indstillingerne kan konfigureres i [Forsendelse og levering](https://www.shopify.com/admin/settings/shipping) på Shopify.

Du kan gøre følgende for hver kunde ved hjælp af **Shopify -kundeskabelonen**:

1. Angiv **Standardkundenr.**, som har højere prioritet end det, du har valgt i felterne **Debitorimport fra Shopify** og **Debitortilknytningstype**. Den bruges i den importerede salgsordre.
2. Definer den **debitorskabelonkode**, der bruges til at oprette manglende kunder, hvis **Automatisk oprettelse af ukendte debitorer** er aktiveret. Hvis **debitorskabelonkode** er tom, bruger funktionen den **debitorskabelonkode**, der er defineret på **Shopify butikskortet**. Systemet prøver først at finde en skabelon til **lande-/områdekoden** for standardadressen. Hvis der ikke findes en skabelon, bruges den første adresse.
3. I nogle tilfælde er den **debitorskabelonkode**, der er defineret for et land/område, ikke nok til at sikre, at moms beregnes korrekt (f. eks. lande/områder med moms). I dette tilfælde kan **momsområderne** være nyttige.
4. Feltet **skatteområde** indeholder også en **landekode** og et **Navn på region**. Dette par er praktisk, når forbindelsen skal konvertere en kode til et navn, eller omvendt.

> [!NOTE]  
> Landekoderne er ISO 3166-1 Alfa-2-landekoder. Flere oplysninger om [Landekode](https://help.shopify.com/en/api/custom-storefronts/storefront-api/reference/enum/countrycode).

## Vigtige indstillinger, når du eksporterer DTC-debitorer til Shopify

Eksisterende kunder kan masseeksporteres til Shopify. I hvert tilfælde oprettes der en kunde og en standardadresse. Du kan bruge følgende indstillinger til at administrere processen:

|Felt|Beskrivelse|
|------|-----------|
|**Kan opdatere Shopify debitorer**| Aktiver den, hvis du vil oprette opdateringer senere fra Business Central for debitorer, der allerede findes i Shopify.|

Der er følgende krav til eksport af en debitor:

* Kunden skal have en gyldig e-mailadresse.
* Når du eksporterer kunder med adresser, der omfatter provinser/stater, skal du sørge for, at **ISO-kode** er angivet for lande/områder.|
* Du skal sørge for, at **ISO-kode** er valgt for land/område på debitorkortet. For lokale kunder med tomt land/område bruger Shopify-connectoren det land/område, der er angivet i **Virksomhedsoplysninger**.
* Hvis debitoren har et telefonnummer, skal nummeret være entydigt, da Shopify ikke accepterer en anden kunde med det samme telefonnummer.
* Hvis kunden har et telefonnummer, skal det være i formatet E.164. Forskellige formater understøttes, hvis de repræsenterer et nummer, der kan ringes op fra et vilkårligt sted i verden. Følgende formater er mulige:

  * xxxxxxxxxx
  * +xxxxxxxxxxx
  * (xxx)xxx-xxxx
  * +x xxx-xxx-xxxx

Når du har oprettet debitorerne i Shopify, kan du sende dem direkte invitationer for at opfordre dem til at aktivere deres konti.

### Udfyld kundeoplysninger i Shopify

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

## Eksportere DTC-debitorer til Shopify

### Oprindelig synkronisering af debitorer fra Business Central til Shopify

1. Gå til søgning ![Lightbulb, der åbner funktionen Fortæl mig.](../media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **Shopify-kunder**, og vælg derefter det relaterede link.
2. Vælg handlingen **Tilføj debitor**.
3. Angiv koden i feltet **Butikskode**. Hvis du åbner vinduet **Shopify-debitorer** fra vinduet **Butikskort**, er butikskoden automatisk udfyldt.
4. Angiv filtre for debitor efter behov. Du kan f.eks. filtrere efter lande-/områdekode.
5. Vælg **OK**.

De resulterende debitorer oprettes automatisk i Shopify med adresser.

> [!NOTE]  
> Indledende synkronisering af debitorer fra [!INCLUDE[prod_short](../includes/prod_short.md)] til Shopify anvender ikke indstillingen **Kan opdatere Shopify-debitorer**.

### Synkronisere debitorer

1. Vælg ![Lightbulb, der åbner funktionen Fortæl mig 1.](../media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **Shopify butik**, og vælg derefter det relaterede link.
2. Marker den butik, som du vil synkronisere debitorer til.
3. Vælg handlingen **Synkroniser debitorer**.

Du kan også bruge handlingen **Start debitorsynkronisering** i vinduet **Shopify Debitorer** eller Søg efter **Synkroniseringsdebitorer**.

Du kan planlægge, at følgende tilbagevendende aktiviteter skal udføres automatisk. Få mere at vide, når du [planlægger tilbagevendende opgaver](background.md#to-schedule-recurring-tasks).

## B2B-virksomheder

Hvis du bruger B2B i Shopify, kan du ud over debitorer også oprette virksomheder. Du kan knytte en eller flere individuelle debitorer til en virksomhed. Du kan også definere betalingsbetingelser, lokationer og kataloger.

## Vigtige indstillinger, når du importerer B2B-virksomheder fra Shopify

Uanset om du masseimporterer virksomheder fra Shopify eller importerer ordrer, skal du bruge indstillinger i følgende tabel til at administrere processen.

|Felt|Beskrivelse|
|------|-----------|
|**Virksomhedsindlæsning fra Shopify**|Vælg **Alle virksomheder**, hvis du planlægger at masseimportere debitorer fra Shopify, enten manuelt ved hjælp af **Synkroniser virksomheder** eller via jobkøen for tilbagevendende opdateringer. Uanset valget vil debitoroplysningerne altid blive importeret sammen med ordren. Brugen af disse oplysninger afhænger imidlertid af **Shopify-virksomhedsskabelonerne** og indstillinger i feltet **Type af virksomhedstilknytning**.|
|**Type af virksomhedstilknytning**|Definer, hvordan connectoren skal udføre tilknytningen.</br></br>- **Via mail/telefon**, hvis du ønsker, at connectoren skal knytte de importerede Shopify-virksomheder til en eksisterende debitor i Business Central via e-mail og telefon fra den primære kontakt.</br></br>- Vælg **Brug altid standardvirksomheden**, hvis systemet skal bruge en virksomheden i feltet **Standardvirksomhedsnr.** . |
|**Shopify kan opdatere virksomheder**| Markér dette felt, hvis du vil have connectoren til at opdatere debitorer, den finder, når indstillingen **Via mail/telefon** er valgt i feltet **Type af virksomhedstilknytning**.|
|**Opret automatisk ukendte virksomheder**| Markér dette felt, hvis du vil have connectoren til at oprette nye debitorer, når indstillingen **Via mail/telefon** er valgt i feltet **Type af virksomhedstilknytning**. Der oprettes en ny debitor ved hjælp af de importerede data og den **kunde-/virksomhedsskabelonkode**, der er defineret på siden **Shopify-butikskort** eller **Shopify-debitorskabeloner**.|
|**Skabelonkode for debitor/virksomhed**|Brug dette felt sammen med **Opret automatisk ukendte virksomheder**.</br></br>- Vælg den standardskabelon, der skal bruges til automatisk oprettede debitorer. Kontroller, at de obligatoriske felter er udfyldt i skabelonen, f.eks. **Virksomhedsbogføringsgruppe**, **Debitorbogføringsgruppe** og **Moms** eller andre skatterelaterede felter.</br></br>- Du kan definere skabeloner pr. land/område på siden **Shopify debitorskabeloner**, som er nyttige i forbindelse med beregning af den relevante afgift.</br></br>Få flere oplysninger i [Konfigurere moms](setup-taxes.md).|

> [!NOTE]  
> Virksomheden skal have en primær kontakt. Ellers går connectoren videre til virksomheden.
> Der importeres kun én ældste lokation.
> Kun den primære kontakten importeres.

## Vigtige indstillinger, når du eksporterer B2B-virksomheder til Shopify

Eksisterende debitorer kan masseeksporteres til Shopify som en virksomhed. I hvert tilfælde oprettes der en virksomhed og én standardlokation og en primær kontakt. Det er også muligt at oprette et katalog.

|Felt|Beskrivelse|
|------|-----------|
|**Kan opdatere Shopify-virksomheder**| Aktivér denne indstilling, hvis du vil oprette opdateringer senere fra Business Central for virksomheder, der allerede findes i Shopify.|
|**Standardkontakttilladelser**| Angiv, hvilke tilladelser der skal tildeles den primære kontakt. Du kan vælge mellem **Ingen**, **Kun bestilling** og **Placeringsadministrator**.|
|**Opret katalog automatisk**| Aktivér denne indstilling, hvis du vil oprette et katalog, der omfatter alle produkter. Der oprettes et katalog for hver eksporteret virksomhed.|

## Eksportere B2B-virksomhed til Shopify

### Oprindelig synkronisering af B2B-virksomheder fra Business Central til Shopify

1. Gå til søgning ![Lightbulb, der åbner funktionen Fortæl mig.](../media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") , skriv **Shopify-virksomhed**, og vælg det relevante link.
2. Vælg handlingen **Tilføj virksomhed**.
3. Angiv koden i feltet **Butikskode**. Hvis du åbner vinduet **Shopify-virksomhed** fra vinduet **Butikskort**, er butikskoden automatisk udfyldt.
4. Angiv filtre for debitor efter behov. Du kan f.eks. filtrere efter lande-/områdekode.
5. Vælg **OK**.

De resulterende virksomheder og debitorer oprettes automatisk i Shopify.

> [!NOTE]  
> Indledende synkronisering af virksomheder fra [!INCLUDE[prod_short](../includes/prod_short.md)] til Shopify anvender ikke indstillingen **Kan opdatere Shopify-virksomheder**.

### Synkronisere B2B-virksomhed

1. Vælg ![Lightbulb, der åbner funktionen Fortæl mig 1.](../media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **Shopify butik**, og vælg derefter det relaterede link.
2. Marker den butik, som du vil synkronisere debitorer til.
3. Vælg handlingen **Synkroniser virksomhed**.

Du kan også bruge handlingen **Start synkronisering af virksomhed** på siden **Shopify-virksomhed** eller søge efter batchjobbet **Synkroniser virksomhed**.

Du kan planlægge, at opgaven skal udføres automatisk. Få mere at vide, når du [planlægger tilbagevendende opgaver](background.md#to-schedule-recurring-tasks).

## Se også

[Kom i gang med Connectoren til Shopify](get-started.md)  
