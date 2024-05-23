---
title: Registrer bæredygtighedsposter
description: Sådan kan du registrere drivhusgas (GHG)-udledninger.
author: altotovi
ms.topic: conceptual
ms.devlang: al
ms.search.keywords: 'Sustainability, ESG, emission, GHG, CSRD, journal'
ms.search.form: '6216, 6219, 6220'
ms.date: 05/07/2024
ms.author: altotovi
ms.service: dynamics-365-business-central
---

# Registrer bæredygtighedsposter

I øjeblikket er den eneste måde at registrere drivhusgasudledninger (GHG) til finansposter for bæredygtighed på at bruge bæredygtighedskladder.

## Bæredygtighedskladder

Bæredygtighedskladder er designet til at spore og registrere bæredygtighedsrelaterede aktiviteter ved hjælp af den samme brugeroplevelse som andre kladder i Business Central. Brugere, der har de nødvendige oplysninger, kan manuelt angive udledninger i en kladde. Alternativt, hvis de mangler disse oplysninger, kan de bruge indbyggede formler til nøjagtigt at beregne emissioner baseret på specifikke kendte parametre svarende til forskellige typer kilder og konti.

De oplysninger, du angiver i en kladde, er midlertidige og kan ændres, mens de er i kladden. Når du bogfører kladden, overføres oplysningerne til finansposter for bæredygtighed på individuelle bæredygtighedskonti, hvor de ikke kan ændres. Du kan dog bogføre tilbageførsels- eller rettelsesposter.

### Bruge kladdeskabeloner og -batches

Der er som standard to bæredygtighedskladdetyper, standardskabelonen og den tilbagevendende skabelon.

For hver kladdetype kan du angive din egen private kladde som kladdenavn. For at gøre dette skal du vælge handlingen **Batches** på siden **Skabeloner til bæredygtighedskladde** og oprette den nye **bæredygtighedskladdenavn** på den nye side. Du kan f.eks. definere din egen kladde for hvert emissionsomfang ved hjælp af indstillingen **Udledningsomfang**, hvor du kan vælge mellem tre eksisterende omfang. Du kan også tilføje eller ændre **kildesporet** og **årsagskoden** for hvert af navnene.

> [!TIP]
> Hvis du har mange linjer, kan du reducere risikoen for fejl ved at have en kladdekørsel for hver emissionstype. Alternativt kan du bruge den fælles batch til alle udledningstyper.

### Validering af bæredygtighedskladder

Du kan aktivere en baggrundskontrol på siden **Opsætning af bæredygtighed**, som medvirker til at forhindre forsinkelser ved bogføring. Kontrollen giver dig besked, når der opstår fejl i bæredygtighedskladden, og den vil forhindre, at du arbejder med at bogføre kladden.

Når du aktiverer valideringen, viser faktaboksen **Kladdekontrol** problemer på den aktuelle linje og på hele kørslen. Validering sker, når du indlæser et kladdenavn, og når du vælger en anden kladdelinje. Feltet **Antal i alt** i faktaboksen viser det samlede antal fundne problemer [!INCLUDE [prod_short](includes/prod_short.md)] . Du kan vælge feltet for at åbne en oversigt over problemerne.

### Arbejde med bæredygtighedskladder

Følg disse trin for at begynde at arbejde med bæredygtighedskladder:

1. Vælg ![Lightbulb, der åbner funktionen Fortæl mig 3.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **Bæredygtighedskladde**, og vælg derefter det relaterede link.
2. På siden **Bæredygtighedskladde** kan du indtaste lige så mange linjer, som du planlægger at bogføre med samme batch.
3. Du kan lade feltet **Bilagstype** være tomt, eller du kan vælge **Faktura** eller **Kreditnota**.
4. I feltet **Kontonr.** kan du kun vælge ikke-blokerede bæredygtighedskonti med feltet **Direkte bogføring** markeret, og hvor feltet **Bogføringstype** er angivet til **Bogfører**. Konti skal også være konfigureret med en kategori og en underkategori.

    > [!NOTE]
    > Hvis du bruger det batch, hvor udledningsomfanget er konfigureret, skal **Udledningsomfanget** i bæredygtighedskontoen svare til **Udledningsomfanget** i anvendte batch.

5. Du kan enten bogføre beløbene manuelt eller bruge formler.

    - Hvis du har nøjagtige oplysninger om emissionen, du vil bogføre den (dvs. hvis du har den på den modtagne faktura), skal du markere feltet **Manuel indtastning** for at angive, at mængderne skal indtastes manuelt. I dette tilfælde kan du ikke udfylde dine data direkte i felterne **Brændstof/elektricitet**, **Afstand**, **Brugerdefineret antal**, **Installationsmultiplikator** og **Tidsfaktor**, da de bliver ikke-redigerbare. Men felterne **Udledning af CO2**, **Udledning af CH4** og **Udledning af N2O** kan redigeres, og du kan udfylde dine data direkte der.
    - Hvis du ikke har nøjagtigt kendskab til emissionen og skal beregne den, skal du ikke vælge feltet **Manuel indtastning**. I dette tilfælde kan felterne **Udledning CO2**, **Udledning CH4** og **Udledning N2O** ikke redigeres. Du kan dog angive dine beregningsoplysninger baseret på den formel, du bruger. Du kan finde mere om de anvendte formler, der er defineret i kategorien **bæredygtighedskonto** i [Diagram over bæredygtighedskonti og hovedbøger](finance-sustainability-accounts-ledger.md#account-categories).

6. Vælg handlingen **Bogfør** for at bogføre kladden. Når der bogføres i en bæredygtighedskladde, genereres poster på bæredygtighedsposten.

Hvis din formel er baseret på indstillingen **Beregn fra finans** i kategorien bæredygtighedskonto, skal du bruge handlingen **Indsaml beløb fra finansposter**, før du bogfører kladden, for at beregne udledninger baseret på denne datakilde. Hvis du har foretaget nogle ændringer i udledningsfaktorerne, efter at du har udfyldt kladdelinjerne, skal du desuden vælge handlingen **Genberegn** for at få den korrekte mængde i kladden.

### Gentagelseskladder

En gentagelseskladde er en bæredygtighedskladde med særlige felter til styring af transaktioner, som bogføres ofte med få eller ingen ændringer. For eksempel bæredygtighedstransaktioner som el, varme eller andre lignende transaktioner. Du kan bruge gentagelseskladder til at bogføre faste og variable beløb.

Når du bruger en gentagelseskladder kan du oprette de poster, der bogføres regelmæssigt, én gang. Oplysninger som f.eks. konti, dimensioner og dimensionsværdier forbliver i kladden efter bogføringen. Hvis det er nødvendigt at foretage ændringer, kan du gøre det, hver gang du bogfører.

Feltet **Gentagelsesmetode** er vigtigt. Dette felt bestemmer, hvordan beløbet på kladdelinjen bliver behandlet efter bogføringen. Hvis du f.eks. bogfører det samme beløb, hver gang du bogfører linjen, kan du lade beløbet stå, og i så fald skal du bruge **F Fast** som en mulighed. Eller du kan vælge at lade det slette, fordi konti og tekst i linjen kan genbruges ved hver bogføring, men beløbet hver gang varierer, og i dette tilfælde vil du vælge indstillingen **V Variabel**.

Feltet **Gentagelsesinterval** er også vigtigt og skal indstilles. Dette datoformel angiver, hvor ofte posten på kladdelinjen skal bogføres, og det skal udfyldes. Flere oplysninger i [Bruge datoformler](ui-enter-date-ranges.md#use-date-formulas).

Feltet **Udløbsdato** bestemmer, når linjen bliver bogført for sidste gang. Linjen bogføres ikke efter denne dato. Fordelen ved at bruge feltet **Udløbsdato** er, at linjen ikke slettes fra kladden med det samme. Du kan angive en senere dato, så du kan bruge linjen i fremtiden. Hvis feltet er tomt, bogføres linjen, hver gang du bogfører, indtil den slettes fra kladden.

## Se også

[Finans](finance.md)  
[Oversigt over Ledelse af bæredygtighed](finance-manage-sustainability.md)  
[Opsætning af bæredygtighed](finance-sustainability-setup.md)  
[Diagram over bæredygtighedskonti og finans](finance-sustainability-accounts-ledger.md)  
[Arbejd med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
