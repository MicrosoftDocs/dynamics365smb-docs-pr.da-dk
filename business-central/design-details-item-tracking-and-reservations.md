---
title: Designoplysninger - Varesporing og reservationer
description: Dette emne omhandler varesporing og reservationer og beskriver begreberne bag disse to indstillinger.
author: brentholtorf
ms.topic: conceptual
ms.devlang: al
ms.search.keywords: null
ms.date: 06/15/2021
ms.author: bholtorf
ms.service: dynamics-365-business-central
---
# Designoplysninger: Varesporing og reservationer

Samtidig brug af reservation og specifik varesporing er usædvanlig, da de begge skaber en kobling mellem udbud og efterspørgsel. Bortset fra situationer, hvor en kunde eller produktionsplanlægger anmoder om et bestemt lot, giver det sjældent mening at reservere lagervarer, der allerede har varesporingsnumre til bestemt udligning. Selvom det er muligt at reservere varer, der kræver bestemt varesporing, er specielle funktioner nødvendige for at undgå konflikter omkring tilgængelighed mellem ordrebehandlere, der anmoder om de samme varesporede varer.  
  
Konceptet for sen binding sikrer, at en generel reservation af et serienummer eller lotnummer forbliver løst sammenkoblet indtil bogføringen. På bogføringstidspunktet kan reservationssystemet omrokere generelle reservationer for at sikre, at fast udligning er mulig mod det serie- eller lotnummer, der faktisk er plukket. I mellemtiden stilles serienummer eller lotnummer til rådighed for specifik reservation i andre dokumenter, der anmoder om det bestemte serie- eller lotnummer.  
  
En generel reservation er en, hvor det er ligegyldigt for brugeren, hvilken specifik vare der plukkes, og en specifik reservation er en, hvor det ikke er ligegyldigt for brugeren.  
  
> [!NOTE]  
> Funktionen Sen binding vedrører kun varer, der er defineret med specifik varesporing, og den gælder kun for reservation på lager, ikke af indgående forsyningsordrer.  
  
Reservation af varesporingsnumre falder i to kategorier, som vist i følgende tabel.  
  
|Reservation|Beskrivelse|  
|-----------------|---------------------------------------|  
|Bestemt|Du vælger et bestemt serienummer eller lotnummer, når du reserverer lagervaren fra et behov, f.eks. en salgsordre.<br /><br /> Dette er en almindelig reservation. Det er et stift link mellem forsyning og behov, der både bærer serie- og lotnumre. **Bemærk!** Behovet har serie- eller lotnumre. <br /><br /> Du ønsker f.eks. at reservere en dåse blå maling fra Lot A, fordi kunden anmoder om det. En dåse blå maling fra lotnummer A er leveret til kunden.|  
|Ikke-specifik|Du vælger ikke et bestemt serienummer eller lotnummer, når du reserverer lagervaren fra et behov, f.eks. en salgsordre.<br /><br /> Dette er en tilstand, der er pålagt en reservationspost for serie- eller lotnumre, der ikke er specifikt valgt. **Bemærk!** Behovet har ikke serie- eller lotnumre. <br /><br /> Du ønsker f.eks. at reservere en dåse blå maling fra et hvilket som helst lot til din salgsordre. En dåse blå maling fra et vilkårlig serie- eller lotnummer er leveret til kunden.|  
  
Den væsentligste forskel mellem specifik og generel reservation defineres af eksistensen af serie- eller lotnumre på behovssiden, som vist i følgende tabel.  

| Type            | Forsyning                | Behov                   |
|-----------------|-----------------------|--------------------------|
| **Bestemt**    | Serie- eller lotnummer. | Serie- eller lotnummer.    |
| **Ikke-specifik** | Serie- eller lotnummer. | Intet serie- eller lotnummer. |
  
Når du reserverer lagerbeholdningsantal fra en udgående dokumentlinje for en vare, der har varesporingsnumre tildelt og er defineret til specifik varesporing, fører siden **Reservation** dig gennem forskellige arbejdsgange, afhængigt af behovet for serie- eller lotnumre.  
  
## Specifik reservation  
Når du vælger **Reserver** fra den udgående dokumentlinje, vises der en dialogboks, hvor du bliver spurgt, om du vil reservere bestemte serie- eller lotnumre. Hvis du vælger **Ja**, vises en liste med alle serie- eller lotnumre, der er tildelt bilagslinjen. Siden **Reservation** åbnes, når du har valgt et serie- eller lotnummer, og du kan derefter reservere mellem de valgte serie- eller lotnumre på normal vis.  
  
Hvis nogle af de specifikke varesporingsnumre, du forsøger at reservere, opbevares i generelle reservationer, vil en meddelelse nederst i siden **Reservation** informere dig om, hvor mange af det samlede reserverede antal, der holdes i generelle reservationer, og om de stadig er tilgængelige.  
  
## Ikke-specifik reservation  
Hvis du vælger **Nej** i den dialogboks, der vises, åbnes siden **Reservation**, så du kan reservere blandt alle serienumre eller lotnumre på lageret.  
  
Når du foretager en generel reservation af en varesporet vare, skal systemet vælge bestemte vareposter, at reservere mod på grund af strukturen i reservationssystemet. Da vareposterne er markeret med varesporingsnumrene, reserverer reservationen indirekte specifikke serie- eller lotnumre, selvom det ikke var din hensigt. Reservationssystemet forsøger at omrokere ikke-specifikke reservationsposter inden bogføring for at håndtere denne situation.  
  
Systemet reserverer faktisk stadig mod bestemte poster, men derefter bruger det en omrokeringsmekanisme, når der er bestemt behov for lot- eller serienummeret i den generelle reservationen. Dette kan være tilfældet, når du bogfører en transaktion, f.eks. en salgsordre, forbrugskladde eller overflytningsordre for serie- eller lotnummeret, eller når du forsøger specifikt at reservere serie- eller lotnummeret. Systemet omrokerer reservationerne for at gøre lot- eller serienumrene tilgængelige for behovet eller for den specifikke reservation og dermed placere et andet lot- eller serienummer i den generelle reservation. Hvis der er utilstrækkelig mængde på lageret, vil systemet reshuffle så meget som muligt, og du modtager en fejlmeddelelse om tilgængelighed, hvis der stadig er utilstrækkelig mængde på tidspunktet for bogføringen.  
  
> [!NOTE]  
>  På en generel reservation er feltet med lotnummer eller serienummer tomt i reservationsposten, der peger på behov, f.eks. salg.  
  
## Omrokering  
Når en bruger sender et udgående dokument efter at have valgt forkert serie- eller lotnummer, omrokeres andre generelle reservationer, så de afspejler det faktiske serie- eller lotnummer, der er plukket. Dette opfylder bogføringsprogrammet med en fast udligning mellem forsyning og behov.  
  
For alle understøttede virksomhedsscenarier er omrokering kun mulig mod positive vareposter med reservationsnummer og serie- eller lotnumre, men uden definerede serie- eller lotnumre på behovssiden.  
  
## Understøttede virksomhedsscenarier  
Funktionen Sen binding understøtter følgende virksomhedsscenarier:  
  
* Angivelse af et bestemt serienummer eller lotnummer på et udgående dokument med generel reservation af et forkert serienummer eller lotnummer.  
* Reservere et bestemt serie- eller lotnummer.  
* Bogføring af et udgående dokument med generel reservation af et serie- eller lotnummer.  
  
### Angivelse af serie- eller lotnumre på et udgående dokument med forkert generel reservation  
Dette er det mest almindelige af de tre understøttede scenarier. I dette tilfælde sikrer sen bindingsfunktionalitet, at en bruger kan indtaste et serienummer eller lotnummer, der rent faktisk plukkes, på et udgående dokument, der allerede har en generel reservation af et andet serie- eller lotnummer.  
  
Behovet opstår for eksempel, når en ordrebehandler først har foretaget en generel reservation af et hvilket som helst serienummer eller lotnummer. Senere, når varen faktisk plukkes fra lager, skal plukket serie- eller lotnummer angives på ordren, før den bogføres. Den ikke-specifikke reservation omrokeres på bogføringtidspunktet for at sikre, at det plukkede serie- eller lotnummer kan angives uden at miste reservationen og for at sikre, at det plukkede serie- eller lotnummer fuldt ud kan anvendes og bogføres.  
  
### Reservere bestemte serienumre eller lotnumre  
Sen bindingsfunktionalitet sikrer, at en bruger, der forsøger at reservere et bestemt serienummer eller lotnummer, der er reserveret generelt i øjeblikket, kan gøre det i dette virksomhedsscenario. En generel reservation omrokeres på tidspunktet for reservationen for at frigøre serie- eller lotnummeret for den specifikke anmodning.  
  
Omrokering sker automatisk, men integreret Hjælp vises nederst på siden **Reservation** og viser følgende tekst:  
  
**XX af det samlede reserverede antal er ikke specifikt og kan være tilgængeligt.**  
  
Derudover viser feltet **Ikke-specifikt reserveret antal**, hvor mange reservationsposter der er generelle. Dette felt er som standard ikke synligt for brugerne.  
  
### Bogføring af et udgående dokument med generel reservation af serie- eller lotnumre  
Dette forretningsscenarie understøttes med funktionaliteten Sen Binding, der muliggør fast udligning og udgående bogføring af, hvad der faktisk er plukket, ved at omrokere en anden generel reservation af et serie- eller lotnummer. Hvis reshuffling ikke er mulig, vises følgende standardfejlmeddelelse, når brugeren forsøger at postere leveringen:  
  
**XX-element kan ikke anvendes fuldt ud.**  
  
## Se også  
[Designoplysninger: Varesporing](design-details-item-tracking.md)

[!INCLUDE[footer-include](includes/footer-banner.md)]