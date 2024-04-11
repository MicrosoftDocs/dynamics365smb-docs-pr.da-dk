---
title: Ofte stillede spørgsmål om forslag til salgslinjer med Copilot
description: 'Disse ofte stillede spørgsmål indeholder oplysninger om den AI-teknologi, der bruges i Business Central.'
author: brentholtorf
ms.author: bholtorf
ms.reviewer: andreipa
ms.topic: article
ms.search.form: null
ms.date: 02/02/2024
ms.service: dynamics-365-business-central
ms.collection: bap-ai-copilot
ms.custom: responsible-ai-faqs
---

# Ofte stillede spørgsmål om forslag til salgslinje med Copilot (forhåndsversion)

[!INCLUDE[preview-banner](includes/preview-banner.md)]

Disse ofte stillede spørgsmål beskriver AI-effekten af forslag til salgslinje-funktionen i [!INCLUDE [prod_short](includes/prod_short.md)].

[!INCLUDE[production-ready-preview-dynamics365](includes/production-ready-preview-dynamics365.md)]

## Hvad er forslag til salgslinje med Copilot?

Forslag til salgslinjer med Copilot kan hjælpe med at oprette linjer i salgsdokumenter, f.eks. salgstilbud, ordrer og fakturaer baseret på struktureret input eller naturligt sprog. Funktionen er ikke til generel chat, men en meget specifik og integreret oplevelse, som du kan bruge på salgsdokumenter. Funktionen tilbyder to forskellige færdigheder, der hjælper dig med at finde data om individuelle produkter eller hele dokumenter.

## Hvilke muligheder er der for salgslinjeforslag med Copilot?

* Find produkter

  Oplysninger, der beskriver produkter, gemmes flere steder i [!INCLUDE [prod_short](includes/prod_short.md)]. Varenumre og beskrivelser gemmes f.eks. i tabellen **Vare**, flere stregkoder gemmes i tabellen **Varereference**, og produktegenskaber gemmes i tabellen **Vareattributter**. Selvom du måske beder om *rød cykel*, kan det faktiske produkt være *Crimson tourer*, hvor *cykel* er en produktkategori, og *rød* er en attribut.

* Søg efter et dokument efter reference

  Folk gentager ofte en tidligere ordre eller bruger den i det mindste som udgangspunkt. Men det kan være vanskeligt at finde den rigtige ordre i en bunke af ordrer. Du husker måske noget af ordrens id, som kan være et nummer tildelt af virksomheden eller et referencenummer, der er modtaget fra en kunde. Hvis du bruger prompter som f.eks. *Skal bruge faktura fra april*, kan det hjælpe dig med at finde en ordre hurtigere.

## Hvad er den tilsigtede brug af salgslinjeforslag med Copilot?

* Find produkter

  Beregnet til at besvare brugeropfordringer til at finde produkter baseret på vage, ufuldstændige eller unøjagtige beskrivelser.

  Fordi det gennemsnitlige antal varer (produkter / tjenester) for [!INCLUDE [prod_short](includes/prod_short.md)] kunder er 10.000, kan det være svært at finde de rigtige uden forudgående erfaring eller viden. Den måde, data gemmes på [!INCLUDE [prod_short](includes/prod_short.md)], gør ikke tingene lettere, fordi du skal foretage flere søgninger eller filtreringsøvelser på de forskellige sider, der gemmer produktdata.

  Copilot udtrækker de ønskede produkter og mængder og identificerer de vigtigste søgetermer og attributter, så du hurtigere kan indtaste din prompt. Derefter foretager Copilot en avanceret søgning gennem flere relaterede tabeller, anvender synonymer, retter stavefejl og evaluerer kvaliteten af søgeoutputtet.

* Søg efter et dokument efter reference

  Beregnet til at besvare brugerforespørgsler for at finde eksisterende salgsdokumenter for en bestemt kunde ved hjælp af delvise eller omtrentlige oplysninger.

  I B2B-miljøer håndterer folk ofte tilbagevendende anmodninger, og ordrebehandlere kan få forespørgsler til at gentage et tidligere dokument eller i det mindste bruge det som udgangspunkt. Men det kan være vanskeligt at finde en af flere grunde:

  - Gennem hele livscyklussen kan et salgsdokument udvikle sig fra tilbud til ordre til bogført faktura eller leverance. Dokumenter kan også arkiveres.
  - Du har muligvis et nøjagtigt id, men kan ikke sige, hvad det repræsenterer. Er det f.eks. ordrenummer, fakturanummer eller ekstern reference?
  - Nogle gange har du en dato eller et punktum, men ikke et id for dokumentet.

  Hvis du vil finde et kildedokument manuelt, skal du åbne flere sider og søge og filtrere flere gange. Copilot kan dog forenkle dette i en enkelt, naturlig sprogforespørgsel, der giver dig mulighed for at udtrykke det, du leder efter, på din egen måde. 

  * *Hent produkter fra ordre 103031*
  * *Mangler produkter fra sidste faktura i august*

## Hvordan blev forslag til salgslinje med Copilot evalueret? Hvilke metrikværdier bruges til at måle ydeevnen?

Funktionen gennemgik omfattende test, hvor adskillige prompter på amerikansk engelsk repræsenterer både typisk brug og brug af dårlige skuespillere. Testen var baseret på [!INCLUDE [prod_short](includes/prod_short.md)]-demonstrationsdata og et stort mærket produktkatalog, der var tilgængeligt som open source.

Denne funktion er bygget i overensstemmelse med ansvarlig brug af AI-standard i Microsoft. [Få mere at vide om ansvarlig AI fra Microsoft](https://aka.ms/RAI).

## Hvad er begrænsningerne for salgslinjeforslag med Copilot? Hvordan kan brugerne minimere virkningen af salgslinjeforslag med Copilot, når de bruger systemet?

* Find produkter
  
  Find produkter fungerer bedst på engelsk. Selvom du kan bruge denne funktion på alle de sprog, som [!INCLUDE [prod_short](includes/prod_short.md)] understøtter, kan elementsøgninger på andre sprog være mindre nøjagtige.

Hvis din branche eller dit domæne overlapper med det, Microsoft betragter som følsomme emner (f.eks. stoffer, vold, voksenunderholdning osv.), kan Copilot bøje sig for neutrale, organiserede svar eller give unøjagtige svar.

Forslag til salgslinjer udfylder kun felterne **Type** som **Vare**, **Nummer** og **Antal** som beskrevet. Andre felter, herunder **Enhed**, **Salgspris** og **Lokation** , bruger den aktuelle logik og udfyldes enten baseret på vareindstillinger eller på nedarvede værdier fra dokumenthovedet.

**Variantkoden** understøttes ikke i øjeblikket. Hvis du f.eks. kan sende et produkt i to forskellige farver, finder Copilot det nødvendige produkt, men lader feltet **Variantkode** være tomt. Du skal udfylde feltet manuelt.

Den måde, du navngiver dine produkter på, kan påvirke outputtet. For eksempel kan brug af kryptiske forkortelser versus venlige navne reducere outputkvaliteten.

For produkter viser følgende tabel de tabeller og felter, som Copilot søger i.

|Sortbord  |Felter  |
|---------|---------|
|**Varer**     |  * Nr.<br>* Beskrivelse<br>* Beskrivelse 2<br>* Søgebeskrivelse<br>* GTIN<br>* Kreditors varenr.       |
|**Varevariant**     | * Kode<br>* Beskrivelse<br>* Beskrivelse 2          |
|**Varereference**     | * Referencenr.<br>* Beskrivelse<br>* Beskrivelse 2        |
|**Vareattributter**     | * Navn<br>* Værdi        |
|**Varekategori**     |  * Kode<br>* Beskrivelse<br>* Overordnet kategori - 1 Niveau           |
|**Varetekst**     | * Sprog<br>* Beskrivelse<br>* Beskrivelse 2          |
|**Vare-id**     |  * Kode       |
|**Udvidet tekstlinje**     |  * Tekst      |

* Søg efter dokumenter efter reference

  I øjeblikket kan du starte forslag til salgslinjer fra salgsordrer, fakturaer og tilbud og søge i følgende dokumenter:

  * Salgsordrer
  * Salgskvoter
  * Salgsfakturaer
  * Bogførte salgsfakturaer
  * Bogførte salgsleverancer

  Copilot søger i følgende felter

  * Dokumentnr.
  * Eksternt dokumentnr.
  * Din reference
  * Tilbudsnr.
  * Dokumentdato
  * Sælg-til-kundenr.

  Copilot returnerer ikke alle linjer af varetypen. Det er kun varenumre, variantkoder og antal, der overføres. Antallet fra kildedokumentet konverteres til **salgsenheden**.

## I hvilke geografiske områder og på hvilke sprog er salgslinjeforslag tilgængelig?

Med undtagelse af Canada er denne funktion tilgængelig for alle miljølande-/områdelokaliseringer og på alle understøttede sprog. På grund af begrænset sprogunderstøttelse vil funktionen i første omgang ikke være tilgængelig for canadiske kunder på grund af overholdelse af lovgivningsmæssige sprog. For denne funktion, der er tilgængelig for kundemiljøer, der er placeret i lande/områder, hvor Azure OpenAI-tjenesten ikke er udrullet, skal administratorer først give samtykke til, at data flyttes på tværs af grænser for [!INCLUDE [prod_short](includes/prod_short.md)] for at oprette forbindelse til Azure OpenAI-tjenesten, og for at denne funktion er tilgængelig.  

## Hvilke driftsmæssige faktorer og indstillinger gør det muligt at bruge funktionen på en effektiv og ansvarlig måde?

AI-drevne matches og forslag kan nogle gange være forkerte eller ufuldstændige. Du bør altid gennemgå nøjagtigheden af Copilots forslag, før du vælger, om du vil beholde dem. Copilots matches og forslag gemmes ikke i [!INCLUDE [prod_short](includes/prod_short.md)]-databasen, før du vælger knappen **Behold den** og forlader Copilot-vinduet. Du kan redigere og rette eventuelle forslag, før du vælger at beholde dem, eller efter at de er indsat i et salgsdokument.

### Hvad forventes der af administratorer og slutbrugere, når du bruger salgslinjeforslag?

Hver enkelt bruger vælger, om der skal bruges **salgslinjeforslag**. Selv når funktionen er aktiveret af administratorer og tilgængelig, kan du vælge at bruge den altid, nogle gange eller aldrig.  

Administratorer træffer den overordnede beslutning om, hvorvidt Copilot-funktionerne skal bruges i [!INCLUDE [prod_short](includes/prod_short.md)]. Hvis administratorer aktiverer Copilot, skal de sørge for at give adgang til de relevante brugere.   

> [BEMÆRK!]
> - Vi understøtter ikke denne funktion i [!INCLUDE [prod_short](includes/prod_short.md)] det lokale miljø eller private cloudmiljø.
> - Partnere kan ikke udvide denne funktion. Det betyder, at partnerudviklere ikke kan ændre, erstatte eller udvide den.

## Er Copilot den eneste måde at oprette salgslinjer på?  

Nej, brug af Copilot er valgfrit. [!INCLUDE [prod_short](includes/prod_short.md)] tilbyder ikke-AI-drevne måder at indsætte salgslinjer eller kopiere dokumenter på. Organisationer kan bruge begge metoder på samme tid.  

## Hvordan giver jeg feedback om AI-genereret indhold?  

Hver gang Copilot giver matches eller forslag, kan du give feedback til Microsoft direkte fra Copilot-vinduet ved hjælp af knapperne Synes godt om og Afvis. Dit feedback forbliver anonymt, og vi bruger disse data til at evaluere og forbedre kvaliteten af tjenesten.  

## Se også

[Foreslå linjer på salgsordrer med Copilot](sales-suggest-sales-lines-with-copilot.md)  
[Konfigurere Copilot- og AI-funktioner](enable-ai.md)  
[Ofte stillede spørgsmål om ansvarlig brug af AI til Dynamics 365 Business Central](responsible-ai-overview.md)  
