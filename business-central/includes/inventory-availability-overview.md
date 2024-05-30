---
author: brentholtorf
ms.topic: include
ms.date: 04/23/2024
ms.author: bholtorf
ms.service: dynamics-365-business-central
---

Øg effektiviteten på lagerstedet med nøjagtige oplysninger i realtid om faktorer, der kan påvirke tilgængelige mængder. Eksempler: 

* Lagerniveauer
* Placeringer
* Forarbejdningsstadier
* Elementer, der er sat i karantæne
* Reservationer

Du kan få adgang til oplysninger om varedisponering fra følgende kildedokumenter:

* Salgsordrer
* Produktionsordrer
* Montageordrer
* Job

Oplysningerne respekterer også andre faktorer, der påvirker tilgængeligheden. For eksempel dedikerede placeringer, låste placeringer og varer, der ikke er tilgængelige til pluk. Varer kan f.eks. være reserveret eller afventer læg-på-lager- eller leveringsoperationer. På siden **Plukoversigt** kan du gennemse de varer, der [!INCLUDE [prod_short](prod_short.md)] ikke fandtes i plukdokumenterne, og udføre de nødvendige handlinger.

> [!NOTE]
> Denne funktion kræver, at du aktiverer til/fra-knappen **Styret læg-på-lager og pluk** for de lokationer, du bruger i plukprocessen.

### <a name="set-up-previews"></a>Konfigurere forhåndsversioner

Hvis du vil have oplysninger om, hvad der plukkes, og hvad der ikke plukkes, skal du aktivere **Vis oversigt (styret læg-på-lager og pluk)** på anmodningssiderne **Lager - kilde - Opret dokument** eller **Lager - leverance - Opret pluk**.

### <a name="determine-the-quantity-you-can-pick"></a>Bestem det antal, du kan plukke

På linjerne på siden **Opret lagerplukoversigt** viser feltet **Håndteringsantal (basis)**, hvilke og hvor mange varer [!INCLUDE [prod_short](prod_short.md)] har forsøgt at plukke. Faktaboksen **Oversigt** indeholder flere oplysninger.

I forbindelse med simple undersøgelser er **Antal, der kan plukkes** kan give dig nok oplysninger. Feltet viser, hvor mange varer der er tilgængelige. Hvis det antal, der kan plukkes, er mindre end forventet, skal du undersøge placeringsindholdet.

Det **Antal, der kan plukkes** er det maksimale antal, [!INCLUDE [prod_short](prod_short.md)] kan tage i betragtning ved plukning. Dette antal består af varer på plukbare placeringer. Antallet omfatter ikke antal, der er på blokerede eller dedikerede placeringer, eller varer, der plukkes i lagerplukdokumenter. Hvis den vare, du vil plukke, kræver varesporing, udelukkes blokerede lot- eller serienumre, der er gemt på plukbare placeringer, fra det antal, der kan plukkes.

Hvis det antal, der kan plukkes, afviger fra antallet på plukbare placeringer, kan der være et problem. Udforsk placeringsindholdet for at finde blokerede placeringer eller antal i aktive dokumenter.

Feltet **Antal på lager** viser det samlede antal, du finder på lagerstedet, hvis du foretager en fysisk optælling. Fra dette felt kan du analysere ned til lagerposterne. Hvis feltet viser et antal, der er mindre end antallet i **Antal i placeringer, der kan plukkes**, er der en forkert justering mellem lager- og lagerantal. Hvis det er tilfældet, skal du bruge handlingen **Beregn lagerregulering** på siden **Varekladde** og derefter oprette lagerplukket igen.

Følgende billede illustrerer det maksimale antal, der tages i betragtning til pluk.

:::image type="content" source="../media/pickable-qty.png" alt-text="Maksimumsantal, der tages i betragtning til plukning.":::

**Forklaring**

|Bogstav  |Beskrivelse  |
|---------|---------|
|P     |Placeringer med indhold af typen Pluk         |
|D     |Placeringer med indhold af typen Pluk markeret som Dedikerede placeringer        |
|T     |Placeringer med indhold af typen Vælg i de aktive dokumenter (f.eks. et andet pluk)       |
|D     |Placeringer med indhold af typen Pluk med varer med blokeret sporing         |
|B     |Placeringer med indhold af typen Pluk med blokeret udgående bevægelse         |
|O     |Andre placeringer         |

### <a name="reservations"></a>Reservationer

Hvis der er forbehold for den vare, der plukkes, fortsætter beregningen. Ideen er, at reserveret behov har højere prioritet end ikke-reserveret, hvilket betyder, at plukning for ikke-reserveret behov ikke bør forhindre plukning for reserveret behov senere.

Du kan kontrollere, om antallet kan dække et behov, ved at sammenligne **Plukbart antal.** i faktaboksen **Oversigt** med værdien i feltet **Håndteringsantal (basis)** på linjerne.

Du kan finde reservationer i feltet **Reserveret antal i alt på lager**. Reserverede antal, der allerede er plukket, og som er klar til levering, brug eller forbrug, påvirker ikke tilgængeligheden. Feltet **Reserveret antal på pluk-/leveringsplaceringer** viser dette antal.

Feltet **Disp. antal undtagen leveranceplacering** viser det antal, der er disponibelt, eksklusive antal, hvor følgende gælder:

* De er allerede plukket til forsendelser.
* De findes i blokerede varepartier eller serienumre.
* De er i blokerede placeringer.
* De er i dedikerede placeringer.

Disse antal er muligvis tilgængelige, men du kan muligvis ikke plukke dem endnu. De kan stadig være i modtagelses-, lager- eller kvalitetssikringsområderne. Du kan flytte dem til plukområdet ved at behandle en læg-på-lager- eller bevægelseskladde.

Forskellen mellem **Disp.antal ekskl. leveranceplacering** og reserveret antal på lagerstedet er den mængde, der er disponibel til pluk, uden at det påvirker det reserverede lager.

Følgende værdi illustrerer fordelingen af den disponible mængde for reserveret kvantitet.

:::image type="content" source="../media/Warehouse_Reservation_Pick.png" alt-text="Maksimalt antal, der tages i betragtning til pluk, når reservationen er involveret.":::

**Forklaring**

|Bogstav  |Beskrivelse  |
|---------|---------|
|P     |Beholdning, der kan plukkes         |
|TR    |Samlet reserveret antal i lagersted.         |
|RS    |Reserverede antal, der allerede er plukket, og som er klar til levering, brug eller forbrug       |
|T     |Disponibelt antal ekskl. forsendelsesplacering         |
|B     |Antal på dedikerede eller blokerede placeringer, blokerede varepartier eller serienumre         |

Selvom der er nok disponibel mængde på lagerstedet til at tilfredsstille plukket fuldstændigt, medfører det, at det samlede reserverede antal allokeres i forhold til mængderne på dedikerede eller blokerede placeringer, hvilket forhindrer pluk til dette behov. Da reserveret behov har højere prioritet, reducerer [!INCLUDE [prod_short](prod_short.md)] det antal, der skal plukkes, for at forhindre negativ indvirkning på reserveret behov, f.eks. manglende evne til at plukke.

### <a name="other-details"></a>Andre detaljer

Hvis varer kræver varesporing, kan du også finde antallet i blokerede lot- eller serienumre, hvilket medfører følgende reduktioner:

* Antal, der kan plukkes
* Disponibelt antal, ekskl. forsendelsesplacering
* Reserveret antal i lagersted 

Hvis du plukker den samme vare til flere kildedokumenter eller -linjer, hvilket også er tilfældet, når du plukker serienumre, vises der også oplysninger om pluk til andre linjer, fordi det reducerede plukbare antal.
