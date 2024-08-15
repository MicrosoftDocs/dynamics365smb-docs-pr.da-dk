---
title: 'Designoplysninger – reservation, ordresporing og aktionsmeddelelser | Microsoft Docs'
description: Reservationssystemet er omfattende og omfatter indbyrdes relaterede og parallelle funktionerne for ordresporing og aktionsmeddelelser.
author: brentholtorf
ms.topic: conceptual
ms.devlang: al
ms.search.keywords: 'design, replenishment, reordering'
ms.date: 07/23/2024
ms.author: bholtorf
ms.service: dynamics-365-business-central
ms.reviewer: bholtorf
---
# Designoplysninger: Reservation, ordresporing og aktionsmeddelelser

Reservationssystemet er omfattende og omfatter indbyrdes relaterede og parallelle funktionerne for ordresporing og aktionsmeddelelser.  

Kernen i reservationssystemet er sammenkædningen af en behovspost og en tilsvarende forsyningspost, enten via reservation eller ordresporing. En reservation er et brugergenereret link, og en ordresporingsregistrering et et systemgenereret link. En varemængde, der er angivet i reservationssystemet, er enten reserveret eller ordresporet, men ikke begge dele på samme tid. Hvordan systemerne håndterer en vare afhænger af, hvordan varen er sat op.  

Reservationssystemet interagerer med planlægningssystemet ved at oprette aktionsmeddelelser i planlægningslinjer under planlægningskørsler. En aktionsmeddelelse kan betragtes som et appendiks til en ordresporingspost. Aktionsmeddelelser er et praktisk værktøj til effektiv forsyningsplanlægning, uanset om de oprettes dynamisk i ordresporing eller under planlægningskørslen.  

> [!NOTE]  
> Reserverede mængder ignoreres af planlægningssystemet, så det hårde link, der er foretaget mellem udbud og efterspørgsel, kan ikke ændres via planlægning.  

 Reservationssystemet udgør også det strukturelle grundlag for varesporingssystemet. Du kan finde flere oplysninger i [Designoplysninger: varesporing](design-details-item-tracking.md).  

 <!--For more detailed information about how the reservation system works, see the _Reservation Entry Table_ white paper on [PartnerSource](https://go.microsoft.com/fwlink/?LinkId=258348).  -->
<!--
> [!NOTE]
> [!INCLUDE [locations-cronus](includes/locations-cronus.md)]
-->

## Reservation  

 En reservation er et fast link, der forbinder et bestemt behov og en bestemt forsyning med hinanden. Denne tilknytning påvirker den efterfølgende lagertransaktion direkte og sikrer en korrekt udligning af vareposter i forbindelse med kostberegning. En reservation tilsidesætter standardomkostningsmetoden for en vare. Du kan finde flere oplysninger i [Designoplysninger: varesporing](design-details-item-tracking.md).  

 Siden **Reservation** er tilgængeligt fra alle ordrelinjer for både behovs- og forsyningstyper. På denne side kan brugeren angive den behovs- og forsyningspost, der skal oprettes en reservationskæde til. Reservationen består af et sæt af poster, der deler samme løbenummer. Én post har et negativt fortegn og peger på behovet. Den anden post har et positivt tegn og peger på forsyningen. Disse poster gemmes i *tabellen Reservationspost* med statusværdien *Reservation*. Brugeren kan se alle reservationer på siden **Reservationsposter**.  

### Modregning i reservationer  

 Reservationer foretages af antal tilgængelige varer. Varedisponering beregnes på følgende grundlæggende måde :  

 `available quantity = inventory + scheduled receipts - gross requirements`

 Følgende tabel viser oplysninger om ordrenetværksenheder, der er en del af disponeringsberegningen.  

||Felt i T27-vare|Kildetabel|Tabelfilter|Kildefelt|  
|-|------------------|------------------|------------------|------------------|  
|**Lagerbeholdning**|Lager|Varepost|I/R|Antal|  
|**Fastlagt tilgang**|Fastlagt ordretilgang (antal)|Prod.ordrelinje|=Fastlagt|Restantal (basis)|  
|**Fastlagt tilgang**|Frigivet ordretilgang (antal)|Prod.ordrelinje|=Frigivet|Restantal (basis)|  
|**Fastlagt tilgang**|Antal i montageordre|Montagehoved|=Ordre|Restantal (basis)|  
|**Fastlagt tilgang**|Antal i købsordre|Købslinje|=Ordre|Udestående antal (basis)|  
|**Fastlagt tilgang**|Overfly.ordremodt. (antal)|Overflytningslinje|I/R|Udestående antal|  
|**Bruttobehov**|Antal i salgsordre|Salgslinje|=Ordre|Udestående antal (basis)|  
|**Bruttobehov**|Planlagt behov (antal)|Prod.ordrekomponent|<>Simuleret|Restantal (basis)|  
|**Bruttobehov**|Mgd. på montagekomponent|Montagelinje|=Ordre|Restantal (basis)|  
|**Bruttobehov**|Overfly.ordrelev. (antal)|Overflytningslinje|I/R|Udestående antal|  

 Du kan finde flere oplysninger i [Designoplysninger: Tilgængelighed i lageret](design-details-availability-in-the-warehouse.md).  

### Manuel reservation  

Når en bruger bevidst opretter en reservation, får brugeren fuld ejendomsret til og ansvar for disse varer. Det betyder, at brugeren også manuelt skal ændre eller annullere en reservation. Sådanne manuelle ændringer kan medføre automatisk ændring af de involverede reservationer.  

Følgende tabel viser, hvornår og hvilke ændringer der kan forekomme:  

|Brugerhandling|Systemets reaktion|  
|-----------------|---------------------|  
|Reducering af det reserverede antal.|Relaterede mængdefelter opdateres.|  
|Ændring af datofelter|Relaterede datofelter opdateres.<br /><br /> **Bemærk:** Hvis forfaldsdatoen på et behov ændres for at stå foran leveringsdatoen eller forfaldsdatoen for forsyningen, annulleres reservationen.|  
|Sletning af ordren.|Reservationen annulleres.|  
|Ændring af lokation, placering, variant, serienummer eller lotnummer|Reservationen annulleres.|  

> [!NOTE]  
> Funktionen Sen binding kan også ændre reservationer uden at underrette brugeren via reshuffling af generelle reservationer af serie- eller lotnumre. Hvis du ønsker yderligere oplysninger, kan du se [Designoplysninger: Varesporing og reservationer](design-details-item-tracking-and-reservations.md).  

### Automatiske reservationer  

 Varekortet kan konfigureres til altid at være automatisk reserveret fra behov, f.eks. salgsordrer I så fald reserveres på lager, indkøbsordrer, montageordrer og produktionsordrer. Der advares, hvis forsyning er utilstrækkelig.  

 Desuden reserveres varer automatisk ved forskellige planlægningsfunktioner for at holde et behov knyttet til en bestemt forsyning. Ordresporingsposterne for sådanne planlægningslinks indeholder **Reservation** i **feltet Reservationsstatus** i tabellen *Reservationspost* . Der oprettes automatiske reservationer i følgende situationer:  

- En produktionsordre med flere niveauer, hvor feltet **Produktionsmetode** af de involverede overordnede og underordnede elementer er indstillet til **Fremstil-til-ordre**. Planlægningssystemet opretter reservationer mellem den overordnet produktionsordre og de underliggende produktionsordrer for at sikre, at de behandles samlet. Sådan en reservationsbinding tilsidesætter varens standardkostmetode og udligningsmetode.  

- En produktion, montage eller købsordre, hvor feltet **Genbestillingsmetode** på den pågældende vare er angivet til **Ordre**. Planlægningssystemet opretter en reservation mellem behovet og den planlagte forsyning for at sikre, at den specifikke forsyning oprettes. Du kan finde flere oplysninger i [Ordre](design-details-handling-reordering-policies.md#order).  

- En produktionsordre, der er oprettet ud fra en salgsordre med funktionen **Salgsordreplanlægning**, knyttes til salgsordren med en automatisk reservation.  

- En montageordre, der oprettes automatisk for en salgsordrelinje for at opfylde antallet i feltet Antal, der skal **samles til ordre** . Denne automatiske reservation sammenkæder salgsbehovet og montageforsyningen, så salgsordrebehandlere kan tilpasse og love at levere montageelementet direkte til kunden. Desuden kæder reservationen montageafgangen til salgsordrelinjen via leveringsaktiviteten, der opfylder kundens ordre.  

Hvis der ikke er allokeret forsyning eller behov, tildeler planlægningssystemet automatisk reservationsstatus af typen **Overskud**. Dette kunne opstå fra behov, som skyldes forecastantallet eller brugerindtastede planlægningsparametre. Dette er legitimt overskud, som systemet anerkender, og det giver ikke anledning til aktionsmeddelelser. Overskud kan også være ægte, overskydende forsyning eller behov, som forbliver ikke-sporet. Dette er en angivelse af en ubalance i ordrenetværket, der får systemet til at udstede aktionsmeddelelser. Bemærk, at en aktionsmeddelelse, der foreslår en ændring i antal, altid henviser til typen **Overskud**. Du kan finde flere oplysninger i afsnittet [Eksempel: Ordresporing i salg, produktion og overførsler](#example-order-tracking-in-sales-production-and-transfers) i denne artikel.  

Automatiske reservationer, der oprettes under planlægningskørslen, håndteres på følgende måder:  

- De anvendes på vareantal, der er en del af tilgængelighedsberegningen, ligesom manuelle reservationer. Du kan finde flere oplysninger i afsnittet "Modregning i reservationer" i denne artikel.  

- De medtages og kan ændres i efterfølgende planlægningskørsler i modsætning til manuelt reserverede varer.  

## Ordresporing  

Ordresporing hjælper med at vedligeholde en gyldig forsyningsplan ved at give et overblik over modregning mellem behov og forsyning i ordrenetværket. Ordresporingsposter fungerer som grundlag for oprettelse af dynamiske aktionsmeddelelser og planlægningslinjeforslag under planlægningskørsler.  

> [!NOTE]  
> Ordresporingssystemet udligner tilgængeligt lager, når ordrer indsættes i ordrenetværket. Dette indebærer, at systemet ikke prioriterer ordrer, der kan haste mere i forhold til deres forfaldsdato. Det er derfor op til logikken i planlægningssystemet eller visdom hos planlæggeren at arrangere disse prioriteter på en meningsfuld måde.  

> [!NOTE]  
> Ordresporingspolitikken og funktionen Hent aktionsmeddelelser er ikke integreret med projekter. Det betyder, at efterspørgsel, der er knyttet til et projekt, ikke spores automatisk. Da det ikke registreres, kan det forårsage brugen af en eksisterende genbestilling med projektoplysninger, der kan spores til et andet behov, for eksempel en salgsordre. Derfor kan der opstå den situation, hvor oplysningerne om lagerbeholdningen ikke er synkroniseret.  

### Ordrenetværket  

Ordresporingssystemet er baseret på princippet om, at ordrenetværket altid skal være i en tilstand af balance, hvor hvert behov, der indsættes i systemet, udlignes af en tilsvarende forsyning og omvendt. Systemet leverer dette ved at identificere de logiske forbindelser mellem alle behovs- og forsyningsposter i ordrenetværket.  

Princippet angiver, at en ændring i behov medfører en tilsvarende ubalance på forsyningssiden af ordrenetværket. Omvendt medfører en ændring i forsyning en tilsvarende ubalance på behovssiden af ordrenetværket. I virkeligheden er ordrenetværket i en tilstand af konstant strømmen, når brugere indtaster, ændrer og sletter ordrer. Ordresporing behandler ordrer dynamisk, reagerer på hver enkelt ændring på det tidspunkt, det kommer ind i systemet og bliver en del af ordrenetværket. Så snart der er oprettet nye poster til ordresporing, er ordrenetværket afstemt, men kun indtil næste ændring forekommer.  

Siden **Ikke-sporede planlægningselementer** viser ikke-sporede mængder for at øge gennemsigtigheden af beregninger i planlægningssystemet. Dette repræsenterer forskellen i antallet mellem kendt behov og foreslået forsyning. Hver linje på siden refererer til årsagen til det overskydende antal, som f.eks. **Rammeordre**, **Niveau for sikkerhedslager**, **Fast genbestil.antal**, **Min. ordreantal**, **Afrunding** eller **Aktionsgrænse**.  

### Modregning i ordresporing  

I modsætning til reservationer, som kun kan foretages mod tilgængelige vareantal, er ordresporing mulig i forhold til alle ordrenetværksenheder, der indgår i beregningen af planlægningssystemets nettobehov. Nettobehovet beregnes på følgende måde:  

`net requirements = gross requirements + reorder point - scheduled receipts - planned receipts - projected available balance`  

> [!NOTE]  
> Behov, der er relateret til forecasts eller planlægningsparametre, ordrespores ikke.  

### Eksempel: Ordresporing i Salg, Produktion og Overførsler  

Følgende scenarie viser, hvilke ordresporingsposter der oprettes i *tabellen Reservationspost* som resultat af forskellige ændringer i ordrenetværket.  

Forestil dig følgende data for to varer, der er defineret til ordresporing.  

|Artikel|Parameter|Detaljer|
|-|-|-|
|Vare 1|Navn|Komponent|
||Tilgængelighed|100 enheder på lokationen EAST<br /><br />- 30 enheder LOTA<br />- 70 enheder LOTB|  
|Vare 2|Navn|Produceret vare|
||Produktionsstykliste|1 antal pr. komponent|  
||Efterspørgsel|Salg til 100 enheder på lokationen WEST|  
||Forsyning|Frigivet produktionsordre (oprettet med *funktionen Salgsordreplanlægning* ved salg af 100 enheder)|  

På siden **Produktionsopsætning** **er feltet Komponenter på lokation** angivet til *ØST.*

Der findes følgende ordresporingsposter i tabellen *Reservationspost*, som er baseret på dataene i tabellen.  

<!--![First example of order tracking entries in Reservation Entry table.](media/supply_planning_RTAM_1.png "supply_planning_RTAM_1")  -->
**Reservationsposter**

|Postnr.|Positiv|Varenr.|Lokationskode|Antal|Reservationsstatus|Beskrivelse|Partinr.|Kildetype|Kilde-id|Binding|  
|--------|--------|--------|-------------|--------|------------------|-----------|-------|-----------|---------|-------| 
|8|-|KOMPONENT|ØST|-70|Sporing|Komponent|-|5407|101004|-|
|8|Ja|KOMPONENT|ØST|70|Sporing|Komponent|LOTB|32|-|-| 
|9|-|KOMPONENT|ØST|-30|Sporing|Komponent|-|5407|1001004|-| 
|9|Ja|KOMPONENT|ØST|30|Sporing|Komponent|LOTA|32|-|-| 
|10|-|PRODUCERET VARE|VEST|-100|Reservation|Produceret vare|-|37|1001|Ordre-til-ordre|
|10|Ja|PRODUCERET VARE|VEST|100|Reservation|Produceret vare|-|5406|101004|Ordre-til-ordre|


#### Løbenumre 8 og 9  

For komponentbehovet for henholdsvis LOTA og LOTB oprettes ordresporingslinks fra behovet i tabel 5407,Prod.ordrekomponent *·*, til leveringen i tabel 32,Varepost *·*. Feltet **Reservationsstatus** indeholder *Sporing*, der angiver, at disse poster er dynamiske ordresporingsforbindelser mellem udbud og efterspørgsel.  

> [!NOTE]  
> Feltet **Lotnr.** er tomt på behovslinjer, fordi der ikke er angivet lotnumre på komponentlinjerne i den frigivne produktionsordre.  

#### Løbenummer 10  

Fra salgsbehovet i tabel 37,Salgslinjer *·*, oprettes en ordresporing sammenkæde til leveringen i tabel 5406,Prod.ordrelinje *·*. Feltet **Reservationsstatus** indeholder *Reservation*, og feltet **Binding** indeholder *Ordre-til-ordre*. Det skyldes, at den frigivne produktionsordre blev oprettet specifikt til salgsordren og skal forblive tilknyttet i modsætning til ordresporingslinks med reservationsstatus Sporing, som oprettes og ændres dynamisk. Du kan finde flere oplysninger i afsnittet Automatiske reservationer [i](#automatic-reservations) denne artikel.  

 På dette tidspunkt i scenariet overføres 100 enheder af LOTA og LOTB til lokationen WEST af en overflytningsordre.  

> [!NOTE]  
> Kun overflytningsordrens leverance bogføres på dette tidspunkt, ikke modtagelsen.  

 Følgende ordresporingsposter findes nu i tabellen *Reservationspost* .  

<!-- ![Second example of order tracking entries in Reservation Entry table.](media/supply_planning_RTAM_2.png "supply_planning_RTAM_2")  -->
**Reservationsposter**

|Postnr.|Positiv|Varenr.|Lokationskode|Antal|Reservationsstatus|Beskrivelse|Partinr.|Kildetype|Kilde-id|Binding|  
|---------|--------|--------|-------------|--------|------------------|-----------|-------|-----------|---------|-------| 
|9|-|KOMPONENT|ØST|-30|Overskud|Komponent|-|5407|1001004|-| 
|10|-|PRODUCERET VARE|VEST|-100|Reservation|Produceret vare|-|37|1001|Ordre-til-ordre|
|10|Ja|PRODUCERET VARE|VEST|100|Reservation|Produceret vare|-|5406|101004|Ordre-til-ordre|
|12|Ja|KOMPONENT|VEST|70|Overskud|Komponent|LOTB|5741|1011|-| 
|14|Ja|KOMPONENT|VEST|30|Overskud|Komponent|LOTA|5741|1011|-| 
|15|Ja|KOMPONENT|UD. LOG.|70|Overskud|Komponent|LOTB|32|-|-| 
|16|Ja|KOMPONENT|UD. LOG.|30|Overskud|Komponent|LOTA|32|-|-| 

#### Løbenumre 8 og 9  

Ordresporingsposterne for de to partier af komponenten, der afspejler behovet i tabel 5407, ændres fra reservationsstatussen *Sporing* til *Overskud*. Årsagen er, at de forsyninger, som de var knyttet til tidligere, i tabel 32, er anvendt af overflytningsordren ved leverancen.  

Ægte overskud, som i dette tilfælde, afspejler overskydende forsyning eller behov, som forbliver ikke-sporet. Det er en indikation af ubalance i ordrenetværket, som genererer en aktionsmeddelelse fra planlægningssystemet, medmindre den løses dynamisk.  

#### Løbenumre 12 og 16  

Da de to partier af komponenten er bogført på overflytningsordren som leveret, men ikke modtaget, er alle relaterede positive ordresporingsposter af reservationstypen *Overskud*, hvilket indikerer, at de ikke er allokeret til nogen behov. For hvert lotnummer er én post relateret til tabel 5741, *Overflytningslinje*, og én post relation til vareposten på det transitsted, hvor varerne nu findes.  

På dette tidspunkt i scenariet bogføres overflytningsordren for komponenter fra *lokationen ØST* til *VEST* som modtaget.  

Følgende ordresporingsposter findes nu i tabellen *Reservationspost* .  

<!-- ![Third example of order tracking entries in Reservation Entry table.](media/supply_planning_RTAM_3.png "supply_planning_RTAM_3") -->
 **Reservationsposter**

|Postnr.|Positiv|Varenr.|Lokationskode|Antal|Reservationsstatus|Beskrivelse|Partinr.|Kildetype|Kilde-id|Binding|  
|---------|--------|--------|-------------|--------|------------------|-----------|-------|-----------|---------|-------| 
|8|-|KOMPONENT|ØST|-70|Overskud|Komponent|-|5407|101004|-| 
|9|-|KOMPONENT|ØST|-30|Overskud|Komponent|-|5407|1001004|-|
|10|-|PRODUCERET VARE|VEST|-100|Reservation|Produceret vare|-|37|1001|Ordre-til-ordre|
|10|Ja|PRODUCERET VARE|VEST|100|Reservation|Produceret vare|-|5406|101004|Ordre-til-ordre|
|17|Ja|KOMPONENT|VEST|70|Overskud|Komponent|LOTB|32|-|-| 
|18|Ja|KOMPONENT|VEST|30|Overskud|Komponent|LOTA|32|-|-| 

Ordresporingsposterne ligner nu det første punkt i scenariet, hvor overflytningsordren før kun blev bogført som leveret, bortset fra at posterne for komponenten nu har reservationsstatus *Overskud*. Dette skyldes, at komponentbehovet stadig er på lokation *ØST*, hvilket afspejler, at **feltet Lokationskode** på produktionsordrekomponentlinjen indeholder *ØST* som opsætning i **feltet Komponenter på lokation** . Den forsyning, der tidligere blev allokeret til dette behov, er blevet overført til *lokationen Vest* og kan nu ikke spores helt, medmindre komponentbehovet på produktionsordrelinjen ændres til *lokation Vest* .  

På dette tidspunkt i scenariet er lokationskoden **på** produktionsordrekomponentlinjen angivet til *VEST*. På siden **Varesporingslinjer** er de 30 enheder LOTA og de 70 enheder LOTB desuden knyttet til produktionsordrekomponentlinjen.  

Følgende ordresporingsposter findes nu i tabellen *Reservationspost* .  

<!-- ![Fourth example of order tracking entries in Reservation Entry table.](media/supply_planning_RTAM_4.png "supply_planning_RTAM_4")   -->
 **Reservationsposter**

|Postnr.|Positiv|Varenr.|Lokationskode|Antal|Reservationsstatus|Beskrivelse|Partinr.|Kildetype|Kilde-id|Binding|  
|---------|--------|--------|-------------|--------|------------------|-----------|-------|-----------|---------|-------| 
|10|-|PRODUCERET VARE|VEST|-100|Reservation|Produceret vare|-|37|1001|Ordre-til-ordre|
|10|Ja|PRODUCERET VARE|VEST|100|Reservation|Produceret vare|-|5406|101004|Ordre-til-ordre|
|21|-|KOMPONENT|VEST|-70|Sporing|Komponent|LOTB|5407|101004|-| 
|21|Ja|KOMPONENT|VEST|70|Sporing|Komponent|LOTB|32|-|-| 
|22|-|KOMPONENT|VEST|-30|Sporing|Komponent|LOTA|5407|1001004|-| 
|22|Ja|KOMPONENT|VEST|30|Sporing|Komponent|LOTA|32|-|-| 

#### Løbenumre 21 og 22  

Da behovet for komponenter er ændret til lokation Vest, og forsyningen er tilgængelig som vareposter på *lokationen Vest*, er alle ordresporingsposter for de to lotnumre nu fuldt sporet, hvilket indikeres af reservationsstatus *Sporing* . *·*  

Feltet **Lotnr.** er nu udfyldt i ordresporingsposten for tabel 5407, fordi lotnumrene blev tildelt på produktionsordrelinjerne.  

## Aktionsmeddelelser  

Når ordresporingssystemet registrerer en ubalance i ordrenetværket, oprettes der automatisk en aktionsmeddelelse for at give brugeren besked. Aktionsmeddelelser er systemgenererede kald til brugerhandling, som angiver detaljerne omkring ubalancen, og forslagene til, hvordan der genoprettes balance i ordrenetværket. De vises som planlægningslinjer på **siden Planlægningskladder,** når du vælger **Hent aktionsmeddelelser** . Desuden vises der aktionsmeddelelser i planlægningslinjer, der er oprettet af kørslen for at afspejle planlægningssystemets forslag om at gendanne balance i ordrenetværket. I begge tilfælde køres forslagene på ordrenetværket, når du vælger **Udfør aktionsmeddelelse** .  

En aktionsmeddelelse vedrører ét styklisteniveau ad gangen. Hvis brugeren accepterer aktionsmeddelelsen, kan dette give anledning til yderligere meddelelser på det næste niveau for styklisten.  

Følgende tabel viser de aktionsmeddelelser, der findes.  

|Aktionsmeddelelse|Beskrivelse|  
|--------------------|---------------------------------------|  
|**Ret antal**|Ændrer antallet på en eksisterende forsyningsordre til at dække et ændret eller nyt behov.|  
|**Omplanlæg**|Ændrer forfaldsdatoen for en eksisterende ordre.|  
|**Omplanlæg & ret antal**|Ændrer forfaldsdatoen og antallet for en eksisterende ordre.|  
|**Nyt**|Opretter en ny ordre, hvis behovet ikke kan opfyldes af nogen af de foregående aktionsmeddelelser.|  
|**Annuller**|Annullerer en eksisterende ordre.|  

Ordresporingssystemet vil altid forsøge at løse en ubalance i det eksisterende ordrenetværk. Hvis dette ikke er muligt, sendes der en aktionsmeddelelse for at oprette en ny ordre. Nedenfor vises den prioriterede liste, der anvendes af ordresporingssystemet, når det skal besluttes, hvordan der skal genoprettes balance. Hvis et yderligere behov er angivet i ordrenetværket, forsøger systemet på varesporing via følgende kontroller:  

1. Kontroller for eventuel overskydende forsyning i den eksisterende ordresporingpost for dette behov.  
2. Kontroller for fastlagte og planlagte modtagelser efter modtagelsesdato. Den senest mulige dato er valgt.  
3. Kontroller for disponibelt lager.  
4. Kontroller, om der findes en forsyningsordre i den aktuelle ordresporingspost. Hvis det er tilfældet, udsender systemet en aktionsmeddelelse af typen *Skift* for at øge ordren.  
5. Kontroller, at der ikke findes en forsyningsordre i den aktuelle ordresporingspost. Hvis det er tilfældet, udsender systemet en aktionsmeddelelse af typen *Ny* for at oprette en ny ordre.  

Et åbent behov passerer gennem listen og udligner den disponible forsyning for hvert punkt. Alle resterende behov dækkes altid af check 4 eller 5.  

Hvis der sker en reducering af behovsantal, forsøger ordresporingssystemet at løse ubalancen ved at udføre de forrige kontroller i omvendt rækkefølge. Det betyder, at eksisterende aktionsmeddelelser kan redigeres eller endda slettes, hvis det er nødvendigt. Ordresporingssystemet viser altid resultatet af dets beregninger for brugeren.  

## Ordresporing og planlægning  

Når planlægningssystemet kører, sletter det alle eksisterende ordresporingsposter og poster for aktionsmeddelelser og genopretter dem som planlægningslinjeforslag i henhold til forsyning/behov-par og prioriteter. Når den planlagte kørsel er færdig, er ordrenetværket i afstemt.  

### Planlægningssystemet kontra ordresporing og aktionsmeddelelser  

 Følgende sammenligning viser forskelle mellem de metoder, der bruges af planlægningssystemet til at oprette planlægningslinjer, og de metoder, der bruges af ordresporingssystemet til at oprette ordresporingsposter og aktionsmeddelelser.  

- Planlægningssystemet vedrører hele forsynings- og behovsmønstret for en bestemt vare, hvorimod ordresporing beskæftiger sig med den ordre, der aktiverede den.  

- Planlægningssystemet håndterer alle niveauer i styklistehierarkiet, hvorimod ordresporing beskæftiger sig med ét styklisteniveau ad gangen.  

- Planlægningssystemet opretter links mellem behov og forsyning i henhold til den prioriterede forfaldsdato. Ordresporing etablerer forbindelser mellem behov og forsyning i henhold til ordrepostsekvensen.  

- Planlægningssystemet tager højde for planlægningsparametre, mens ordresporing ikke gør det.  

- Planlægningssystemet opretter links i en brugeraktiveret batchtilstand, når det afstemmer behov og forsyning, hvorimod ordresporing opretter links automatisk og dynamisk, efterhånden som brugeren indtaster ordrer.  

## Se også  

[Designoplysninger: Centrale begreber i planlægningssystemet](design-details-central-concepts-of-the-planning-system.md)  
[Designoplysninger: Forsyningsplanlægning](design-details-supply-planning.md)

[!INCLUDE[footer-include](includes/footer-banner.md)]
