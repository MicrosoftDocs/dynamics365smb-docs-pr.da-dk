---
title: 'Designoplysninger - Reservation, ordresporing og aktionsmeddelelser | Microsoft Docs'
description: Reservationssystemet er omfattende og omfatter indbyrdes relaterede og parallelle funktionerne for ordresporing og aktionsmeddelelser.
author: brentholtorf
ms.topic: conceptual
ms.devlang: al
ms.search.keywords: 'design, replenishment, reordering'
ms.date: 06/08/2021
ms.author: bholtorf
ms.service: dynamics-365-business-central
---
# Designoplysninger: Reservation, ordresporing og aktionsmeddelelser

Reservationssystemet er omfattende og omfatter indbyrdes relaterede og parallelle funktionerne for ordresporing og aktionsmeddelelser.  

I kernen af reservationssystemet er sammenkædningen af en behovspost og en tilsvarende forsyningspost, enten via reservation eller ordresporing. En reservation er et brugergenereret link, og en ordresporingsregistrering et et systemgenereret link. En varemængde, der er angivet i reservationssystemet, er enten reserveret eller ordresporet, men ikke begge dele på samme tid. Hvordan systemerne håndterer en vare, afhænger af, hvordan varen er oprettet.  

Reservationssystemet interagerer med planlægningssystemet ved at oprette aktionsmeddelelser i planlægningslinjer under planlægningskørsler. En aktionsmeddelelse kan betragtes som et appendiks til en ordresporingspost. Aktionsmeddelelser er et praktisk værktøj til effektiv forsyningsplanlægning, uanset om de oprettes dynamisk i ordresporing eller under planlægningskørslen.  

> [!NOTE]  
> Reserverede mængder ignoreres af planlægningssystemet, så det hårde link, der er foretaget mellem udbud og efterspørgsel, kan ikke ændres via planlægning.  

 Reservationssystemet udgør også det strukturelle grundlag for varesporingssystemet. Du kan finde flere oplysninger i [Designoplysninger: varesporing](design-details-item-tracking.md).  

 <!--For more detailed information about how the reservation system works, see the _Reservation Entry Table_ white paper on [PartnerSource](https://go.microsoft.com/fwlink/?LinkId=258348).  -->

> [!NOTE]
> [!INCLUDE [locations-cronus](includes/locations-cronus.md)]

## Reservation  

 En reservation er et fast link, der forbinder et bestemt behov og en bestemt forsyning med hinanden. Denne tilknytning påvirker den efterfølgende lagertransaktion direkte og sikrer en korrekt udligning af vareposter i forbindelse med kostberegning. En reservation tilsidesætter standardomkostningsmetoden for en vare. Du kan finde flere oplysninger i [Designoplysninger: varesporing](design-details-item-tracking.md).  

 Siden **Reservation** er tilgængeligt fra alle ordrelinjer for både behovs- og forsyningstyper. På denne side kan brugeren angive den behovs- og forsyningspost, der skal oprettes en reservationskæde til. Reservationen består af et sæt af poster, der deler samme løbenummer. Én post har et negativt fortegn og peger på behovet. Den anden post har et positivt tegn og peger på forsyningen. Disse poster lagres i tabellen **Reservationspost** med statusværdien **Reservation**. Brugeren kan se alle reservationer på siden **Reservationsposter**.  

### Modregning i reservationer  

 Reservationer foretages af antal tilgængelige varer. Varedisponering beregnes på følgende grundlæggende måde :  

 disponibelt antal = lagerbeholdning + fastlagte tilgange – bruttobehov  

 Følgende tabel viser oplysninger om ordrenetværksenheder, der er en del af disponeringsberegningen.  

||Felt i T27|Kildetabel|Tabelfilter|Kildefelt|  
|-|------------------|------------------|------------------|------------------|  
|**Lagerbeholdning**|Lagerbeholdning|Varepost|I/R|Antal|  
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

Når en bruger bevidst opretter en reservation, får brugeren fuld ejendomsret til og ansvar for disse varer. Det betyder, at brugeren også manuelt skal ændre eller annullere en reservation. Disse manuelle ændringer kan medføre automatiske ændringer af de involverede reservationer.  

I følgende tabel vises hvornår, og hvilke ændringer der kan opstå:  

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

 Desuden reserveres varer automatisk ved forskellige planlægningsfunktioner for at holde et behov knyttet til en bestemt forsyning. Ordresporingsposter for sådanne planlægningskæder indeholder **Reservation** i feltet **Reservationsstatus** i tabellen **Reservationspost**. Der oprettes automatiske reservationer i følgende situationer:  

- En produktionsordre med flere niveauer, hvor feltet **Produktionsmetode** af de involverede overordnede og underordnede elementer er indstillet til **Fremstil-til-ordre**. Planlægningssystemet opretter reservationer mellem den overordnede produktionsordre og de underliggende produktionsordrer for at sikre, at de behandles sammen. Sådan en reservationsbinding tilsidesætter varens standardkostmetode og udligningsmetode.  

- En produktion, montage eller købsordre, hvor feltet **Genbestillingsmetode** på den pågældende vare er angivet til **Ordre**. Planlægningssystemet opretter en reservation mellem behovet og den planlagte forsyning for at sikre, at den specifikke forsyning oprettes. Du kan finde flere oplysninger i [Ordre](design-details-handling-reordering-policies.md#order).  

- En produktionsordre, der er oprettet ud fra en salgsordre med funktionen **Salgsordreplanlægning**, knyttes til salgsordren med en automatisk reservation.  

- En montageordre, der er oprettet automatisk for en salgsordrelinje til at opfylde antallet i feltet **($ T_37_900 Qty. to Assemble to Order $)**. Denne automatiske reservation sammenkæder salgsbehovet og montageforsyningen, så salgsordrebehandlere kan tilpasse og love at levere montageelementet direkte til kunden. Desuden kæder reservationen montageafgangen til salgsordrelinjen via leveringsaktiviteten, der opfylder kundens ordre.  

Ved forsyning og behov, der ikke er allokeret, tildeler planlægningssystemet automatisk en reservationsstatus af typen **Overskud**. Dette kunne opstå fra behov, som skyldes forecastantallet eller brugerindtastede planlægningsparametre. Dette er ægte overskud, som systemet genkender, og det giver ikke en forøgelse af aktionsmeddelelser. Overskud kan også være ægte, overskydende forsyning eller behov, som forbliver ikke-sporet. Dette er en angivelse af en ubalance i ordrenetværket, der får systemet til at udstede aktionsmeddelelser. Bemærk, at en aktionsmeddelelse, der foreslår en ændring i antal, altid henviser til typen **Overskud**. Hvis du ønsker yderligere oplysninger, kan du se afsnittet "Eksempel: Ordresporing i Salg, Produktion og Overførsler" i dette emne.  

Automatiske reservationer, der oprettes under planlægningskørslen, håndteres på følgende måder:  

- De anvendes mod vareantal, der er en del af disponeringsberegningen, ligesom manuelle reservationer. Du kan finde flere oplysninger i afsnittet "Modregning i reservationer" i dette afsnit.  

- De er inkluderet og kan være ændret i efterfølgende planlægningskørsler i modsætning til manuelt reserverede varer.  

## Ordresporing  

Ordresporing hjælper med at vedligeholde en gyldig forsyningsplan ved at give et overblik over modregning mellem behov og forsyning i ordrenetværket. Ordresporingsposter fungerer som grundlag for oprettelse af dynamiske aktionsmeddelelser og planlægningslinjeforslag under planlægningskørsler.  

> [!NOTE]  
> Ordresporingssystemet udligner tilgængeligt lager, når ordrer indsættes i ordrenetværket. Dette indebærer, at systemet ikke prioriterer ordrer, der kan haste mere i forhold til deres forfaldsdato. Det er derfor op til logikken i planlægningssystemet eller visdom hos planlæggeren at arrangere disse prioriteter på en meningsfuld måde.  

> [!NOTE]  
> Ordresporingspolitik og funktionen Hent aktionsmeddelelser er ikke integreret med sager. Det betyder, at efterspørgsel, der er knyttet til et projekt, ikke spores automatisk. Da det ikke registreres, kan det forårsage brugen af en eksisterende genbestilling med projektoplysninger, der kan spores til et andet behov, for eksempel en salgsordre. Derfor kan der opstå den situation, hvor oplysningerne om lagerbeholdningen ikke er synkroniseret.  

### Ordrenetværket  

Ordresporingssystemet er baseret på princippet om, at ordrenetværket altid skal være i en tilstand af balance, hvor hvert behov, der indsættes i systemet, udlignes af en tilsvarende forsyning og omvendt. Systemet leverer dette ved at identificere de logiske forbindelser mellem alle behovs- og forsyningsposter i ordrenetværket.  

Princippet angiver, at en ændring i behov medfører en tilsvarende ubalance på forsyningssiden af ordrenetværket. Omvendt medfører en ændring i forsyning en tilsvarende ubalance på behovssiden af ordrenetværket. I virkeligheden er ordrenetværket i en tilstand af konstant strømmen, når brugere indtaster, ændrer og sletter ordrer. Ordresporing behandler ordrer dynamisk, reagerer på hver enkelt ændring på det tidspunkt, det kommer ind i systemet og bliver en del af ordrenetværket. Så snart der er oprettet nye poster til ordresporing, er ordrenetværket afstemt, men kun indtil næste ændring forekommer.  

Siden **Ikke-sporede planlægningselementer** viser ikke-sporede mængder for at øge gennemsigtigheden af beregninger i planlægningssystemet. Dette repræsenterer forskellen i antallet mellem kendt behov og foreslået forsyning. Hver linje på siden refererer til årsagen til det overskydende antal, som f.eks. **Rammeordre**, **Niveau for sikkerhedslager**, **Fast genbestil.antal**, **Min. ordreantal**, **Afrunding** eller **Aktionsgrænse**.  

### Modregning i ordresporing  

I modsætning til reservationer, som kun kan foretages mod tilgængelige vareantal, er ordresporing mulig i forhold til alle ordrenetværksenheder, der indgår i beregningen af planlægningssystemets nettobehov. Nettobehovet beregnes på følgende måde:  

*nettobehov = bruttobehov + genbestillingspunkt - fastlagt tilgang - planlagt tilgang - planlagt disponibel balance  

> [!NOTE]  
> Behov, der er relateret til forecasts eller planlægningsparametre, ordrespores ikke.  

### Eksempel: Ordresporing i Salg, Produktion og Overførsler  

Følgende scenario viser, hvilke ordresporingsposter der oprettes i tabellen **Reservationspost** som et resultat af forskellige ændringer i ordrenetværk.  

Forestil dig følgende data for to varer, der er defineret til ordresporing.  

|Vare 1|Name|"Komponent"|
|-|-|-|
||Disponering|100 enheder på lokationen WEST<br /><br />- 30 enheder LOTA<br />- 70 enheder LOTB|  
|Vare 2|Name|"Produceret vare"|
||Produktionsstykliste|1 antal pr. "Komponent"|  
||Behov|Salg til 100 enheder på lokationen EAST|  
||Forsyning|Frigivet produktionsordre (oprettet med funktonen **Salgsordreplanlægning** for salg af 100 enheder)|  

På siden **Produktionsopsætning** er feltet **Komponenter på lokation** indstillet til **RØD**.

Følgende ordresporingsposter findes i tabellen **Reservationspost** på basis af data i tabellen.  

 ![Første eksempel på ordresporingsposter i tabellen Reservationspost.](media/supply_planning_RTAM_1.png "forsyningsplanlægning_RTAM_1")  

### Løbenumre 8 og 9  

For komponentbehovet for henholdsvis LOTA og LOTB oprettes der ordresporingslinks fra behovet i tabel 5407, **Prod.ordrekomponent**, til forsyningen i tabel 32 **Varepost**. Feltet **Reservationsstatus** indeholder **Sporing** for at angive, at disse poster er dynamiske ordresporingsbindinger mellem forsyning og behov.  

> [!NOTE]  
> Feltet **Lotnr.** er tomt på behovslinjer, fordi der ikke er angivet lotnumre på komponentlinjerne i den frigivne produktionsordre.  

### Løbenummer 10  

Fra salgsbehovet i tabel 37, **Salgslinje**, oprettes der et ordresporingslink til forsyningen i tabel 5406, **Prod.ordrelinje**. Feltet **Reservationsstatus** indeholder **Reservation**, og feltet **Binding** indeholder **Ordre-til-ordre**. Dette skyldes, at den frigivne produktionsordre blev oprettet specielt til salgsordren og skal forblive sammenkædet i modsætning til ordresporingsbindinger med reservationsstatussen **Sporing**, som oprettes og ændres dynamisk. Du kan finde flere oplysninger i afsnittet "Automatiske reservationer" i dette afsnit.  

 På dette tidspunkt i scenariet overføres 100 enheder af LOTA og LOTB til lokationen EAST af en overflytningsordre.  

> [!NOTE]  
> Kun overflytningsordrens leverance bogføres på dette tidspunkt, ikke modtagelsen.  

 Nu findes følgende ordresporingsposter i tabellen **Reservationspost**.  

 ![Andet eksempel på ordresporingsposter i tabellen Reservationspost.](media/supply_planning_RTAM_2.png "forsyningsplanlægning_RTAM_2")  

### Løbenumre 8 og 9  

Ordresporingsposter til de to lotter af den komponent, der afspejler behovet i tabel 5407, ændres fra en reservationsstatus **Sporing** til **Overskud**. Årsagen er, at de forsyninger, som de var knyttet til tidligere, i tabel 32, er anvendt af overflytningsordren ved leverancen.  

Ægte overskud, som i dette tilfælde, afspejler overskydende forsyning eller behov, som forbliver ikke-sporet. Det er en indikation af ubalance i ordrenetværket, der genererer en aktionsmeddelelse i planlægningssystemet, medmindre den er løst dynamisk.  

### Løbenumre 12 og 16  

Da de to lot'er af komponenten bogføres på overflytningsordren som leveret, men ikke modtaget, er alle relaterede positive ordresporingsposter af reservationstypen **Overskud**, hvilket angiver, at de ikke er allokeret til nogen behov. For hvert lotnummer relateres én post til tabel 5741, **Overflytningslinje**, og én post relateres til vareposten på den transitlokation, hvor varerne findes nu.  

På dette tidspunkt i scenariet er overflytningsordren af komponenterne fra EAST til WEST lokation bogført som modtaget.  

Nu findes følgende ordresporingsposter i tabellen **Reservationspost**.  

 ![Tredje eksempel på ordresporingsposter i tabellen Reservationspost.](media/supply_planning_RTAM_3.png "forsyningsplanlægning_RTAM_3")  

Ordresporingsposterne svarer nu til det første punkt i scenariet, før overflytningsordren blev bogført som kun leveret, bortset fra at komponentens poster nu har reservationsstatussen **Overskud**. Dette skyldes, at komponenten stadig er på lokation WEST, som er et tegn på, at feltet **Lokationskode** på produktionsordrekomponentlinjen indeholder **WEST** som angivet i opsætningsfeltet **Komponenter på lokation**. Den forsyning, der er allokeret til dette behov tidligere, er blevet overført til lokationen EAST og kan nu ikke fuldt spores, medmindre komponentbehov på produktionsordrelinjen ændres til lokationen EAST.  

På dette tidspunkt i scenariet, er **lokationskoden** på produktionsordren indstillet til **EAST**. Desuden bruges siden **Varesporingslinjer** til at tildele produktionsordrelinjen 30 enheder af LOTA og 70 enheder af LOTB.  

Nu findes følgende ordresporingsposter i tabellen **Reservationspost**.  

 ![Fjerde eksempel på ordresporingsposter i tabellen Reservationspost.](media/supply_planning_RTAM_4.png "forsyningsplanlægning_RTAM_4")  

### Løbenumre 21 og 22  

Eftersom komponentbehovet er blevet ændret til lokationen EAST, og leveringen er tilgængelig som vareposter på lokationen EAST, er alle ordresporingsposter til de to lotnumre nu fuldt registreret, angivet ved reservationsstatus **Sporing**.  

Feltet **Lotnr.** er nu udfyldt i ordresporingsposten for tabel 5407, fordi lotnumrene blev tildelt på produktionsordrelinjerne.  

## Aktionsmeddelelser  

Når ordresporingssystemet registrerer en ubalance i ordrenetværket, oprettes der automatisk en aktionsmeddelelse for at give brugeren besked. Aktionsmeddelelser er systemgenererede kald til brugerhandling, som angiver detaljerne omkring ubalancen, og forslagene til, hvordan der genoprettes balance i ordrenetværket. De vises som planlægningslinjer på siden **Planlægningskladde**, når du vælger **Hent aktionsmeddelelser**. Desuden vises der aktionsmeddelelser i planlægningslinjer, der er oprettet af kørslen for at afspejle planlægningssystemets forslag om at gendanne balance i ordrenetværket. I begge tilfælde køres forslagene på ordrenetværk, når du vælger **Udfør aktionsmeddelelse**.  

En aktionsmeddelelse vedrører ét styklisteniveau ad gangen. Hvis brugeren accepterer aktionsmeddelelsen, kan dette give anledning til yderligere meddelelser på det næste niveau for styklisten.  

Følgende tabel viser de aktionsmeddelelser, der findes.  

|Aktionsmeddelelse|Beskrivelse|  
|--------------------|---------------------------------------|  
|**Ret antal**|Ændrer antallet på en eksisterende forsyningsordre til at dække et ændret eller nyt behov.|  
|**Omplanlæg**|Ændrer forfaldsdatoen for en eksisterende ordre.|  
|**Omplanlæg & ret antal**|Ændrer forfaldsdatoen og antallet for en eksisterende ordre.|  
|**Ny**|Opretter en ny ordre, hvis behov ikke kan opfyldes af en af de tidligere aktionsmeddelelser.|  
|**Annuller**|Annullerer en eksisterende ordre.|  

Ordresporingssystemet vil altid forsøge at løse en ubalance i det eksisterende ordrenetværk. Hvis dette ikke er muligt, udstedes en aktionsmeddelelse om at oprette en ny ordre. Nedenfor vises den prioriterede liste, der anvendes af ordresporingssystemet, når det skal besluttes, hvordan der skal genoprettes balance. Hvis et yderligere behov er angivet i ordrenetværket, forsøger systemet på varesporing via følgende kontroller:  

1. Kontroller for eventuel overskydende forsyning i den eksisterende ordresporingpost for dette behov.  
2. Kontroller for fastlagte og planlagte modtagelser efter modtagelsesdato. Den senest mulige dato er valgt.  
3. Kontroller for disponibelt lager.  
4. Kontroller, om der findes en forsyningsordre i den aktuelle ordresporingspost. I så fald udstedes en aktionsmeddelelse af typen **ændring** til at øge ordren.  
5. Kontroller, at der ikke findes en forsyningsordre i den aktuelle ordresporingspost. I så fald udstedes en aktionsmeddelelse af typen **Ny** til at oprette en ny ordre.  

Et åbent behov passerer gennem listen og udligner den disponible forsyning for hvert punkt. Alle resterende behov dækkes altid af check 4 eller 5.  

Hvis der sker en reducering af behovsantal, forsøger ordresporingssystemet at løse ubalancen ved at udføre de forrige kontroller i omvendt rækkefølge. Det betyder, at eksisterende aktionsmeddelelser kan redigeres eller endda slettes, hvis det er nødvendigt. Ordresporingssystemet viser altid resultatet af dets beregninger for brugeren.  

## Ordresporing og planlægning  

Når planlægningssystemet kører, sletter det alle eksisterende ordresporingsposter og poster for aktionsmeddelelser og genopretter dem som planlægningslinjeforslag i henhold til forsyning/behov-par og prioriteter. Når den planlagte kørsel er færdig, er ordrenetværket i afstemt.  

### Planlægningssystemet kontra ordresporing og aktionsmeddelelser  

 Følgende sammenligning viser forskelle mellem de metoder, der bruges af planlægningssystemet til at oprette planlægningslinjer, og de metoder, der bruges af ordresporingssystemet til at oprette ordresporingsposter og aktionsmeddelelser.  

- Planlægningssystemet vedrører hele forsynings- og behovsmønstret for en bestemt vare, hvorimod ordresporing beskæftiger sig med den ordre, der aktiverede den.  

- Planlægningssystemet håndterer alle niveauer i styklistehierarkiet, hvorimod ordresporing beskæftiger sig med ét styklisteniveau ad gangen.  

- Planlægningssystemet opretter links mellem behov og forsyning i henhold til den prioriterede forfaldsdato. Ordresporing etablerer forbindelser mellem behov og forsyning i henhold til ordrepostsekvensen.  

- Planlægningssystemet tager planlægningsparametre i betragtning, hvorimod ordresporing ikke gør det.  

- Planlægningssystemet opretter links i en brugeraktiveret batchtilstand, når det afstemmer behov og forsyning, hvorimod ordresporing opretter links automatisk og dynamisk, efterhånden som brugeren indtaster ordrer.  

## Se også  

[Designoplysninger: Centrale begreber i planlægningssystemet](design-details-central-concepts-of-the-planning-system.md)  
[Designoplysninger: Forsyningsplanlægning](design-details-supply-planning.md)

[!INCLUDE[footer-include](includes/footer-banner.md)]
