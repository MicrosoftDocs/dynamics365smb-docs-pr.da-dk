---
title: Designdetaljer - Overførsler i planlægning
description: 'Lær, hvordan overflytningsordrer bruges som en forsyningskilde ved planlægning af lagerniveauer.'
author: brentholtorf
ms.author: bholtorf
ms.reviewer: andreipa
ms.topic: conceptual
ms.date: 02/22/2023
ms.custom: bap-template
ms.search.keywords: 'design, transfer, sku, locations, warehouse'
---
# <a name="design-details-transfers-in-planning"></a><a name="design-details-transfers-in-planning"></a><a name="design-details-transfers-in-planning"></a>Designoplysninger: Overførsler i planlægning

Overflytningsordrer er også en forsyningskilde, når du arbejder på lagervareniveauet. Ved at bruge flere lokationer (lagre) kan lagervaregenbestillingssystemet indstilles til Overførsel, hvilket indebærer, at lokationen genopfyldes ved at overføre varer fra en anden lokation. I en situation med flere lagersteder kan du have en kæde af overflytninger. Lokationen til GRØNi lokation overføres fra GUL, leverance til GUL overføres fra RØD osv. I begyndelsen af kæden er der et genbestillingssystem for **produktionsordre** eller **Indkøb**.  

![Eksempel på overflytningsflow.](media/nav_app_supply_planning_7_transfers1.png "Eksempel på overflytningsflow")  

> [!NOTE]
> [!INCLUDE [locations-cronus](includes/locations-cronus.md)]

Hvis du sammenligner følgende situationer, er det klart, at planlægningsopgaven i sidstnævnte kan blive kompleks:

* En forsyningsordre er direkte over for en efterspørgselsordre
* En salgsordre leveres via en kæde med SKU-overflytninger

Hvis efterspørgslen ændres, kan det medføre en ripple-effekt via kæden. Alle overflytningsordrer plus indkøbs- og produktionsordren i den modsatte ende af kæden skal opdateres for at kunne ændre efterspørgsel og forsyning.  

![Eksempel på overensstemmelse mellem udbud og efterspørgsel i overflytninger.](media/nav_app_supply_planning_7_transfers2.png "Eksempel på overensstemmelse mellem udbud og efterspørgsel i overflytninger")  

## <a name="why-is-a-transfer-a-special-case"></a><a name="why-is-a-transfer-a-special-case"></a><a name="why-is-a-transfer-a-special-case"></a>Hvorfor er overførsel et særligt tilfælde?

Overførselsordrer svarer til andre ordrer, f.eks. købs- og produktionsordrer. I virkeligheden er der dog meget forskelligt.  

En forskel er, at en overflytningslinje repræsenterer både udbud og efterspørgsel. Den udgående del, der er afsendt, er efterspørgsel. Den indgående del, der skal modtages på den nye lokation, er udbud på den pågældende lokation.  

![Indhold af siden Overflytningsordre.](media/nav_app_supply_planning_7_transfers3.png "Indhold af siden Overflytningsordre")  

Det betyder, at når [!INCLUDE [prod_short](includes/prod_short.md)] manipulerer på udbudssiden af overflytningen, så skal der ske en lignende ændring på efterspørgselssiden.  

## <a name="transfers-are-dependent-demand"></a><a name="transfers-are-dependent-demand"></a><a name="transfers-are-dependent-demand"></a>Overflytninger er afhængige af efterspørgsel

Udbuds-og efterspørgselsforholdet svarer til komponenter på produktionsordrelinjer. Forskellen er, at komponenter på produktionsordrelinjer er på det næste planlægningsniveau og har en anden vare. De to dele af overførslen er på samme niveau for den samme vare.  

En vigtig lighed er, at ligesom komponenter og overførsler er afhængige behov. Behov fra en overflytningslinje dikteres af leveringssiden for overførslen. Hvis leveringen ændres, påvirkes behovet direkte.

Medmindre der ingen planlægningsfleksibilitet er, bør en overflytningslinje ikke blive behandlet som et uafhængigt behov i planlægningen.  

I planlægningsproceduren bør behovet for overførslen kun tages i betragtning, når forsyningssiden er blevet behandlet af planlægningssystemet. Før behandlingen sker, er det faktiske behov ikke kendt. Rækkefølgen af ændringer er vigtig for overflytningsordrer.  

## <a name="planning-sequence"></a><a name="planning-sequence"></a><a name="planning-sequence"></a>Planlægningssekvens

Følgende billede viser et eksempel på overførselsrækkefølge.  

![Eksempel på enkle overflytningsflow.](media/nav_app_supply_planning_7_transfers4.png "Eksempel på enkle overflytningsflow")  

I dette eksempel bestiller en kunde varen på lokationen Grøn. Lokationen Grøn leveres via overførsel fra centrallageret Rød. Centrallageret Rød forsynes via overflytning fra produktion på lokationen Blå.  

I dette eksempel starter planlægningssystemet ved kundebehov og arbejder sig baglæns gennem kæden. Behov og forsyninger bliver behandlet ét sted ad gangen.  

![Forsyningsplanlægning med overflytninger.](media/nav_app_supply_planning_7_transfers5.png "Forsyningsplanlægning med overflytninger")  

## <a name="transfer-level-code"></a><a name="transfer-level-code"></a><a name="transfer-level-code"></a>Overflytningsniveaukode

Den rækkefølge, som lokationer behandles i i planlægningssystemet, bestemmes af overflytningsniveaukoden for lagervaren.  

Overførselsniveaukoden er et internt felt. Feltet beregnes og gemmes på SKU, når du opretter eller ændrer SKU. Beregningen udføres på tværs af alle lagervarer for en given kombination af vare og varevariant. I beregningen bruges lokationskoden og Overflyt fra-koden til at bestemme, hvilken rute der skal bruges til lagervarerne. Beregningen sikrer, at alle behov behandles.  

Overflytningsniveaukoden vil være 0 for lagervarer med genbestillingssystem for produktionsordre eller indkøbsordre og vil være -1 for det første overflytningsniveau -2 for det andet osv. I overførselskæden beskrevet ovenfor vil niveauerne derfor være -1 for RØD og -2 for GRØN, som vist i følgende illustration.  

![Indhold af siden Lagerkort.](media/nav_app_supply_planning_7_transfers6.gif "Indhold af siden Lagerkort")  

Når du opdaterer en lagervare, kan planlægningssystemet registrere, om lagervarer med genbestillingssystemet for lagervarer er konfigureret med cirkulære referencer.  

## <a name="planning-transfers-without-sku"></a><a name="planning-transfers-without-sku"></a><a name="planning-transfers-without-sku"></a>Planlægning af overførsler uden lagervare

Hvis du vil have mindre avancerede logistik opsætninger, kan du bruge lokationer og foretage manuelle overførsler mellem lokationer, også selvom du ikke bruger lagervarer. Overflytningen kan f. eks. omfatte en salgsordre på den pågældende lokation. Planlægningssystemet reagerer på ændringer i behov.  

Med henblik på at understøtte manuelle overflytninger analyserer planlægningen eksisterende overflytningsordrer og planlægger derefter den rækkefølge, som lokationerne skal behandles. Planlægningssystemet fungerer internt med midlertidige lagervarer, der transporterer overførselsniveaukoder.  

![Overflytningsniveaukode.](media/nav_app_supply_planning_7_transfers7.png "Overflytningsniveaukode")  

Hvis der findes flere overførsler til en given lokation, vil den første overflytningsordre definere planlægningens retning. Overførsler, der kører i den modsatte retning, annulleres.  

## <a name="changing-quantity-with-reservations"></a><a name="changing-quantity-with-reservations"></a><a name="changing-quantity-with-reservations"></a>Ændring af antal med reservationer

Når du ændrer antallet i en forsyningsmængde, tager planlægningssystemet reservationer i betragtning. Det reserverede antal repræsenterer den nedre grænse for, hvor meget leveringen skal reduceres med.  

Når du ændrer antallet på en overflytningsordrelinje, skal du være opmærksom på den nedre grænse. Den nedre grænse er det højeste reserverede antal på de udgående og indgående overflytningslinjer.

Der reserveres f. eks. en flytteforslagslinje på 117 dele til følgende linjer:

* En salgslinje på 46
* En købslinje på 24

Selvom den indgående side kan have overført levering, kan du ikke reducere overførselslinjen under 46.  

![Reservationer i overflytningsplanlægning.](media/nav_app_supply_planning_7_transfers8.png "Reservationer i overflytningsplanlægning")  

## <a name="changing-quantity-in-a-transfer-chain"></a><a name="changing-quantity-in-a-transfer-chain"></a><a name="changing-quantity-in-a-transfer-chain"></a>Ændring af antal i en overførselskæde

Her er et eksempel på, hvad der sker, når du ændrer et antal i en overflytningsændring.

Udgangspunktet er en afbalanceret situation med en overførselskæde, der leverer en salgsordre på 27 på lokationen RØD. Der findes en tilsvarende købsordre på lokationen BLÅ. Begge overførsler gennemgås lokationen PINK. Der er to overflytningsordrer, BLÅ-PINK og PINK-RØD.  

![Ændre antallet i overflytningsplanlægning 1.](media/nav_app_supply_planning_7_transfers9.png "Ændre antallet i overflytningsplanlægning 1")  

Nu vælger planlæggeren PINK lokation til at reservere købet.  

![Ændre antallet i overflytningsplanlægning 2.](media/nav_app_supply_planning_7_transfers10.png "Ændre antallet i overflytningsplanlægning 2")  

Det betyder normalt, at planlægningssystemet ignorerer købsordren og overførselsbehovet. Så længe de stemmer, er der ikke noget problem. Men hvad sker der, når RØD lokation ændrer rækkefølgen fra 27 til 22?  

![Ændre antallet i overflytningsplanlægning 3.](media/nav_app_supply_planning_7_transfers11.png "Ændre antallet i overflytningsplanlægning 3")  

Når planlægningssystemet kører igen, skal det slippe af med overskydende forsyning. Reservationen vil dog låse købet og overførslen til et antal af 27.  

![Ændre antallet i overflytningsplanlægning 4.](media/nav_app_supply_planning_7_transfers12.png "Ændre antallet i overflytningsplanlægning 4")  

PINK-RØD overflytning er blevet reduceret til 22. Den indgående del af den BLÅ-PINK overførsel er ikke reserveret, men den udgående del er. Reservationen betyder, at du ikke kan reducere antallet under 27.  

## <a name="lead-time-calculation"></a><a name="lead-time-calculation"></a><a name="lead-time-calculation"></a>Beregning af leveringstid

Ved beregning af forfaldsdatoen for en overflytningsordre skal der tages forskellige former for leveringstid med i betragtning.  

Følgende leveringstider er aktive, når du planlægger en overflytningsordre:  

* Udgående lagerstedsekspeditionstid  
* Transporttid  
* Indgående lagerstedsekspeditionstid  

Følgende felter bruges på planlægningslinjen til at give oplysninger om beregningen:  

* Afsendelsesdato for overflytning  
* Startdato  
* Afslutningsdato  
* Forfaldsdato  

Afsendelsesdatoen på overflytningslinjen vises i feltet **Overflytningsleverancedato**. Afsendelsesdatoen på overflytningslinjen vises i feltet **Forfaldsdato**.  

Start-og slutdatoer beskriver den faktiske transportperiode.  

Følgende illustration viser fortolkning af startdato og -tidspunkt og slutdato og -tidspunkt på planlægningslinjer, der er relateret til flytteordrer.  

![Centrale datoer og klokkeslæt i overflytningsplanlægning.](media/nav_app_supply_planning_7_transfers13.png "Centrale datoer og klokkeslæt i overflytningsplanlægning")  

Eksemplet viser følgende beregninger:  

* Afsendelsesdato + Udgående håndtering = Startdato  
* Startdato + Transporttid = Slutdato  
* Slutdato + Indgående ekspedition = Modtagelsesdato  

## <a name="safety-lead-time"></a><a name="safety-lead-time"></a><a name="safety-lead-time"></a>Gennemløbstid for sikkerhed

Feltet **Standardsikkerhedstid** på siden **Produktionsopsætning** og det relaterede felt **Sikkerhedstid** på **varekortet** skal ikke tages i betragtning ved beregningen af en overflytningsordre. Sikkerhedstiden har dog indflydelse på den samlede plan. Sikkerhedstid påvirker genbestillingsordren (indkøb eller produktion) i begyndelsen af overflytningskæden. Det sted, hvor varerne blev placeret på den lokation, de skal overføres fra.  

![Elementer i forfaldsdatoen for overflytningen.](media/nav_app_supply_planning_7_transfers14.png "Elementer i forfaldsdatoen for overflytningen")  

På produktionsordrelinjen: Slutdato + Sikkerhedstid + Indgående lagerekspeditionstid = Forfaldsdato.  

På købsordrelinjen: Planlagt modtagelsesdato + Sikkerhedstid + Indgående lagerekspeditionstid = Forventet modt.dato.  

## <a name="reschedule"></a><a name="reschedule"></a><a name="reschedule"></a>Omplanlæg

Ved planlægning af en overflytningslinje skal planlægningssystemet slå den udgående del op og ændre dato og klokkeslæt på denne.

> [!NOTE]
> Det er vigtigt at bemærke, at hvis leveringstiden er defineret, vil der være et mellemrum mellem forsendelsen og modtagelsen. Som nævnt kan leveringstiden bestå af flere elementer, f.eks. transporttiden og lagerekspeditionstiden. På en tidslinje flyttes planlægningssystemet tilbage i tid, mens det afstemmer elementerne.  

![Ændring af forfaldsdatoen i overflytningsplanlægning.](media/nav_app_supply_planning_7_transfers15.png "Ændring af forfaldsdatoen i overflytningsplanlægning")  

Når du ændrer forfaldsdatoen på en overflytningslinje, skal der derfor beregnes leveringstid for at opdatere den udgående side af overførslen.  

## <a name="serial-and-lot-numbers-in-transfer-chains"></a><a name="serial-and-lot-numbers-in-transfer-chains"></a><a name="serial-and-lot-numbers-in-transfer-chains"></a>Serienumre/lotnumre i overførselskæder

Hvis behovet er underlagt serienumre/lotnumre, og planlægningsprogrammet køres, giver det anledning til nogle direkte oprettede overflytningsordrer. Hvis du ønsker yderligere oplysninger om dette koncept, kan du se Vareattributter. Hvis serienumre/lotnumre derimod fjernes fra behovet, vil flytteordrerne, der er oprettet i kæden, stadig have serienumre/lotnumre og ignoreres derfor ved planlægning (ikke slettet).  

## <a name="order-to-order-links"></a><a name="order-to-order-links"></a><a name="order-to-order-links"></a>Ordre-til-ordre-links

I dette eksempel oprettes den BLÅ SKU med en **ordre**-genbestillingsmetode. De PINK og RØDE varenumre har genbestillingsmetoden **Lot-for-Lot**. Oprettelse af en salgsordre på 27 på lokationen RØD fører til kædeoverflytninger. Den seneste overførsel er på lokationen BLÅ, og den er reserveret med binding. I dette eksempel er reservationerne ikke hårde reservationer, der er oprettet af planlæggeren ved PINK-lokation. Planlægningssystemet opretter bindingerne. Den vigtige forskel er, at planlægningssystemet kan ændre sidstnævnte.  

![Ordre-til-ordre-links i overflytningsplanlægning.](media/nav_app_supply_planning_7_transfers16.png "Ordre-til-ordre-links i overflytningsplanlægning")  

Hvis behovet er ændret fra 27 til 22, sænker systemet antallet ned gennem kæden. Bindingen bliver reduceret.  

## <a name="see-also"></a><a name="see-also"></a><a name="see-also"></a>Se også

[Designoplysninger: Planlægningsparametre](design-details-planning-parameters.md)   
[Designoplysninger: Tabellen Planlægningsopgave](design-details-planning-assignment-table.md)   
[Designoplysninger: Håndtering af genbestillingsmetoder](design-details-handling-reordering-policies.md)   
[Designdetaljer: Planlægning med eller uden lokationer](production-planning-with-without-locations.md)   
[Designoplysninger: Centrale begreber i planlægningssystemet](design-details-central-concepts-of-the-planning-system.md)   
[Designoplysninger: Afstemning af behov og efterspørgsel](design-details-balancing-demand-and-supply.md)   
[Designoplysninger: Forsyningsplanlægning](design-details-supply-planning.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]
