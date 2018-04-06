---
title: "Designoplysninger – Overførsler i planlægning | Microsoft Docs"
description: "Dette emne beskriver, hvordan overflytningsordrer bruges som en forsyningskilde ved planlægning af lagerniveauer."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: design, transfer, sku, locations, warehouse
ms.date: 07/01/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: d7fb34e1c9428a64c71ff47be8bcff174649c00d
ms.openlocfilehash: e43a339dad7e9f74e9a0b192f53f4f67e52cf8ab
ms.contentlocale: da-dk
ms.lasthandoff: 03/22/2018

---
# <a name="design-details-transfers-in-planning"></a>Designoplysninger: Overførsler i planlægning
Overflytningsordrer er også en forsyningskilde, når du arbejder på lagervareniveauet. Ved at bruge flere lokationer (lagre) kan lagervaregenbestillingssystemet indstilles til Overførsel, hvilket indebærer, at lokationen genopfyldes ved at overføre varer fra en anden lokation. I en situation med flere lagersteder kan virksomheder have en kæde af overførsler, hvor forsyningen til lokationen GRØN overføres fra GUL, og levering til GUL overføres fra RØD og så videre. I begyndelsen af kæden er der et genbestillingssystem for produktionsordre eller indkøb.  
  
![](media/nav_app_supply_planning_7_transfers1.png "NAV_APP_supply_planning_7_transfers1")  
  
Ved sammenligning af en situation, hvor en forsyningsordre stilles direkte over for en behovsordre, med en situation, hvor salgsordren leveres gennem en kæde af lagervareoverflytninger, er det indlysende, at planlægningsopgaven i den sidstnævnte situation kan blive meget kompleks. Hvis behov ændres, kan det forårsage en effekt gennem kæden, fordi al overførsel af ordrer og indkøb/produktionsordre i den modsatte ende af kæden skal manipuleres for at genoprette balancen mellem behov og forsyning.  
  
![](media/nav_app_supply_planning_7_transfers2.png "NAV_APP_supply_planning_7_transfers2")  
  
## <a name="why-is-transfer-a-special-case"></a>Hvorfor er overførsel et særligt tilfælde?  
En overflytningsordre ligner en hvilken som helst anden ordre i programmet. I virkeligheden er det dog meget anderledes.  
  
Et grundlæggende aspekt, der gør overførsler i planlægning forskellig fra købs-og produktionsordrer, er, at en flytteordrelinje repræsenterer behov og forsyning på samme tid. Den udgående del, som leveres fra den gamle lokation, er behov. Den indgående del, der skal modtages på den nye lokation, er forsyning på den pågældende lokation.  
  
![](media/nav_app_supply_planning_7_transfers3.png "NAV_APP_supply_planning_7_transfers3")  
  
Det betyder, at når systemet manipulerer på forsyningssiden af overflytningen, så skal der ske en lignende ændring på behovssiden.  
  
## <a name="transfers-are-dependent-demand"></a>Overflytninger er afhængige behov  
Relateret behov og forsyning har nogen lighed med komponenter i en produktionsordrelinje, men forskellen er, at komponenterne er på det næste planlægningsniveau og med en anden vare, mens de to dele af overflytningen er på samme niveau for den samme vare.  
  
En vigtig lighed er, at ligesom komponenter er afhængige behov, så er overførselsbehovet det også. Behovet fra en flytteordrelinje afgøres på forsyningssiden i overførslen i den forstand, at hvis forsyningen er ændret, bliver behovet direkte berørt.  
  
Medmindre der ingen planlægningsfleksibilitet er, bør en overflytningslinje aldrig blive behandlet som et uafhængigt behov i planlægningen.  
  
I planlægningsproceduren bør behovet for overførslen kun tages i betragtning, når forsyningssiden er blevet behandlet af planlægningssystemet. Før dette, kendes det faktiske behov ikke. Rækkefølgen af de foretagne ændringer er derfor meget vigtigt, når det drejer sig om overflytningsordrer.  
  
## <a name="planning-sequence"></a>Planlægningssekvens  
Følgende illustration viser, hvordan en række overførsler kunne se ud.  
  
![](media/nav_app_supply_planning_7_transfers4.png "NAV_APP_supply_planning_7_transfers4")  
  
I dette eksempel bestiller en kunde varen på lokationen Grøn. Lokationen Grøn leveres via overførsel fra centrallageret Rød. Centrallageret Rød forsynes via overflytning fra produktion på lokationen Blå.  
  
I dette eksempel starter planlægningssystemet ved kundebehov og arbejder baglæns gennem kæden. Behov og forsyninger bliver behandlet ét sted ad gangen.  
  
![](media/nav_app_supply_planning_7_transfers5.png "NAV_APP_supply_planning_7_transfers5")  
  
## <a name="transfer-level-code"></a>Overflytningsniveaukode  
Den rækkefølge, som lokationer behandles i i planlægningssystemet, bestemmes af overflytningsniveaukoden for lagervaren.  
  
Overflytningsniveaukoden er et internt felt, som automatisk beregnes og lagres på lagervaren, når denne oprettes eller ændres. Beregningen kører på tværs af alle lagervarer for en given kombination af vare/variant og bruger lokationskoden og overflyt fra-koden til at fastlægge den rute, der skal bruges i planlægningen, når den gennemkører lagervarerne for at sikre, at alle behov behandles.  
  
Overflytningsniveaukoden vil være 0 for lagervarer med genbestillingssystem for produktionsordre eller indkøbsordre og vil være -1 for det første overflytningsniveau -2 for det andet osv. I overførselskæden beskrevet ovenfor vil niveauerne derfor være -1 for rød og -2 for grøn, som vist i følgende illustration.  
  
![](media/nav_app_supply_planning_7_transfers6.gif "NAV_APP_supply_planning_7_transfers6")  
  
Når du opdaterer en lagervare, kan planlægningssystemet registrere, om lagervarer med genbestillingssystemet Overførsel er konfigureret med cirkulære referencer.  
  
## <a name="planning-transfers-without-sku"></a>Planlægning af overførsler uden lagervare  
  
Selvom lagervarefunktionen ikke bruges, er det muligt at bruge lokationer og foretage manuelle overførsler mellem lokationer. For virksomheder med mindre avanceret lageropsætning, understøtter planlægningssystemet scenarier, hvor eksisterende lager overføres manuelt til en anden lokation, for eksempel for at dække en salgsordre på den pågældende lokation. Samtidigt skal planlægningssystemet reagere på ændringer i behov.  
  
Med henblik på at understøtte manuelle overflytninger analyserer planlægningen eksisterende overflytningsordrer og planlægger derefter den rækkefølge, som lokationerne skal behandles. Planlægningssystemet fungerer internt med midlertidige lagervarer, der transporterer overførselsniveaukoder.  
  
![](media/nav_app_supply_planning_7_transfers7.png "NAV_APP_supply_planning_7_transfers7")  
  
Hvis der findes flere overførsler til en given lokation, vil den første overflytningsordre definere planlægningens retning. Overførsler, der kører i den modsatte retning, annulleres.  
  
## <a name="changing-quantity-with-reservations"></a>Ændring af antal med reservationer  
Når du ændrer antallet i eksisterende forsyning, tager planlægningssystemet reservationer med i betragtning, forstået på den måde, at det reserverede antal repræsenterer den nedre grænse for, hvor meget forsyningen kan reduceres.  
  
Når du ændrer antallet på en eksisterende overflytningsordrelinje, skal du huske på, at den nedre grænse defineres som det højeste reserverede antal på linjen for udgående og indgående overflytning.  
  
Hvis f.eks. en overflytningsordrelinje af 117 stykker reserveres mod en salgslinje på 46 og en købslinje på 24, er det ikke muligt at reducere overflytningslinjen under 46 stykker, selvom det kan repræsentere overskydende forsyning på den indgående side.  
  
![](media/nav_app_supply_planning_7_transfers8.png "NAV_APP_supply_planning_7_transfers8")  
  
## <a name="changing-quantity-in-a-transfer-chain"></a>Ændring af antal i en overførselskæde  
I følgende eksempel er udgangspunktet en afbalanceret situation med en overførselskæde, der leverer en salgsordre på 27 på lokation Rød med en tilsvarende indkøbsordre på lokation Blå, overført via lokation Pink. Der er derfor, udover køb og salg, to overflytningsordrer: BLÅ-PINK og PINK-RØD.  
  
![](media/nav_app_supply_planning_7_transfers9.png "NAV_APP_supply_planning_7_transfers9")  
  
Nu vælger planlæggeren Pink lokation til at reservere købet.  
  
![](media/nav_app_supply_planning_7_transfers10.png "NAV_APP_supply_planning_7_transfers10")  
  
Det betyder normalt, at planlægningssystemet ignorerer købsordren og overførselsbehovet. Så længe de stemmer, er der ikke noget problem. Men hvad sker der, når kunden på lokationen RØD delvist fortryder sin bestilling og ændrer den til 22?  
  
![](media/nav_app_supply_planning_7_transfers11.png "NAV_APP_supply_planning_7_transfers11")  
  
Når planlægningssystemet kører igen, skal det slippe af med overskydende forsyning. Reservationen vil dog låse købet og overførslen til et antal af 27.  
  
![](media/nav_app_supply_planning_7_transfers12.png "NAV_APP_supply_planning_7_transfers12")  
  
PINK-RØD overflytning er blevet reduceret til 22. Den indgående del af BLÅ-PINK overflytning er ikke reserveret, men da den udgående del er reserveret, er det ikke muligt at reducere antallet under 27.  
  
## <a name="lead-time-calculation"></a>Leveringstid  
Ved beregning af forfaldsdatoen for en overflytningsordre skal der tages forskellige former for leveringstid med i betragtning.  
  
De leveringstider, der er aktive, når du planlægger en overflytningsordre, er:  
  
* Udgående lagerekspeditionstid  
* Transporttid  
* Indgående lagerekspeditionstid  
* Følgende felter bruges på planlægningslinjen til at give oplysninger om beregningen.  
* Afsendelsesdato for overflytning  
* Startdato  
* Slutdato  
* Forfaldsdato  
  
Afsendelsesdatoen på overflytningslinjen vises i feltet Afsendelsesdato for overflytning, og modtagelsesdatoen på overflytningslinjen vises i feltet Forfaldsdato.  
  
Start-og slutdatoer bruges til at beskrive den faktiske transportperiode.  
  
Følgende illustration viser fortolkning af startdato og -tidspunkt og slutdato og -tidspunkt på planlægningslinjer, der er relateret til flytteordrer.  
  
![](media/nav_app_supply_planning_7_transfers13.png "NAV_APP_supply_planning_7_transfers13")  
  
I dette eksempel betyder det, at:  
  
* Afsendelsesdato + Udgående håndtering = Startdato  
* Startdato + Transporttid = Slutdato  
* Slutdato + Indgående ekspedition = Modtagelsesdato  
  
## <a name="safety-lead-time"></a>Sikkerhedstid  
Feltet Standardsikkerhedstid i vinduet Produktionsopsætning og det relaterede felt Sikkerhedstid på varekortet skal ikke tages i betragtning ved beregningen af en overflytningsordre. Sikkerhedstiden kan imidlertid stadig påvirke den samlede plan, ligesom den påvirker genbestillingsordren (køb eller produktion) i begyndelsen af overførselskæden, når varerne lægges på den placering, hvorfra de kan overføres.  
  
![](media/nav_app_supply_planning_7_transfers14.png "NAV_APP_supply_planning_7_transfers14")  
  
På produktionsordrelinjen: Slutdato + Sikkerhedstid + Indgående lagerekspeditionstid = Forfaldsdato.  
  
På købsordrelinjen: Planlagt modtagelsesdato + Sikkerhedstid + Indgående lagerekspeditionstid = Forventet modt.dato.  
  
## <a name="reschedule"></a>Omplanlæg  
Ved planlægning af en eksisterende overflytningslinje skal planlægningssystemet slå den udgående del op og ændre dato og klokkeslæt på denne. Det er vigtigt at bemærke, at hvis leveringstiden er defineret, vil der være et mellemrum mellem forsendelsen og modtagelsen. Som nævnt kan leveringstiden bestå af flere elementer, f.eks. transporttiden og lagerekspeditionstiden. På en tidslinje flyttes planlægningssystemet tilbage i tid, mens det afstemmer elementerne.  
  
![](media/nav_app_supply_planning_7_transfers15.png "NAV_APP_supply_planning_7_transfers15")  
  
Når du ændrer forfaldsdatoen på en overflytningslinje, skal der derfor beregnes leveringstid for at opdatere den udgående side af overførslen.  
  
## <a name="seriallot-numbers-in-transfer-chains"></a>Serienumre/lotnumre i overførselskæder  
Hvis behovet er underlagt serienumre/lotnumre, og planlægningsprogrammet køres, giver det anledning til nogle direkte oprettede overflytningsordrer. Hvis du ønsker yderligere oplysninger om dette koncept, kan du se Vareattributter. Hvis serienumre/lotnumre derimod fjernes fra behovet, vil flytteordrerne, der er oprettet i kæden, stadig have serienumre/lotnumre og ignoreres derfor ved planlægning (ikke slettet).  
  
## <a name="order-to-order-links"></a>Ordre-til-ordre-links  
I dette eksempel er Blå lagervare sat op til ordrens genbestillingsmetode, mens Pink og Rød bruger Lot-for-Lot. Når der oprettes en salgsordre på 27 på lokationen RØD, vil det føre til en kæde af overflytninger med det sidste led på lokationen BLÅ, der er reserveret med binding. I dette eksempel er reservationerne ikke hårde reservationer, der er oprettet af planlæggeren ved Pink-lokation, men bindinger, der er oprettet af planlægningssystemet. Den vigtige forskel er, at planlægningssystemet kan ændre sidstnævnte.  
  
![](media/nav_app_supply_planning_7_transfers16.png "NAV_APP_supply_planning_7_transfers16")  
  
Hvis behovet er ændret fra 27 til 22, sænker systemet antallet ned gennem kæden, og den bindende reservation reduceres også.  
  
## <a name="see-also"></a>Se også  
[Designoplysninger: Planlægningsparametre](design-details-planning-parameters.md)   
[Designoplysninger: Tabellen Planlægningsopgave](design-details-planning-assignment-table.md)   
[Designoplysninger: Håndtering af genbestillingsmetoder](design-details-handling-reordering-policies.md)   
[Designoplysninger: Behov på lokationen TOM](design-details-demand-at-blank-location.md)   
[Designoplysninger: Centrale begreber i planlægningssystemet](design-details-central-concepts-of-the-planning-system.md)   
[Designoplysninger: Afstemning mellem behov og forsyning](design-details-balancing-demand-and-supply.md)   
[Designoplysninger: Forsyningsplanlægning](design-details-supply-planning.md)
