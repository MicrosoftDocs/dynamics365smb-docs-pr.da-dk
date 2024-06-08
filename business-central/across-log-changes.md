---
title: Overvåge ændringer
description: Du kan aktivere en brugerlog for at få en oversigt over ændringer af data i registrerede tabeller. Du kan også spore aktiviteter med bestemte typer aktivitetslogge.
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bholtorf
ms.topic: conceptual
ms.search.keywords: 'user log, user activity, tracking'
ms.search.form: '592, 593, 594, 595, 710, 1366, 1367, 1368, 1369'
ms.date: 05/03/2024
ms.custom: bap-template
ms.service: dynamics-365-business-central
---
# Overvåge ændringer

En almindelig udfordring i mange forretningsstyringsprogrammer vil undgå uønskede ændringer i data. Det kan være alt fra et forkert kundetelefonnummer til en forkert postering i regnskabet. I denne artikel beskrives mulighederne for at finde ud af, hvad der er ændret, hvem der ændrede det, og hvornår ændringen blev foretaget.

## Om ændringslog

Du kan bruge funktionaliteten i ændringsloggen til at spore alle direkte modifikationer, som en bruger foretager af data i databasen. Du skal for hver tabel og hvert felt angive, hvad der skal registreres i loggen. Derefter skal du aktivere ændringsloggen. Ændringsloggen er baseret på ændringer, der er foretaget i de tabeller, som du sporer. På siden **Ændringslogposter** registreres posterne i kronologisk rækkefølge og viser de ændringer, der er foretaget i værdierne i felterne på de angivne tabeller.

Registrering af ændringer kan påvirke ydeevnen, som kan koste dig tid, og forøge størrelsen på databasen, der kan koste penge. Hvis du vil reducere disse omkostninger, skal du overveje følgende:

- Vær forsigtig, når du vælger tabeller og handlinger.
- Du skal ikke tilføje finansposter og bogførte bilag. Du skal i stedet prioritere systemfelter som f.eks. oprettet af og oprettelsesdato.
- Undlad at bruge sporingstypen **Alle felter**. I stedet skal du vælge **Nogle felter** og kun spore de vigtigste felter.

> [!NOTE]
> Ændringsloggen registrerer ikke ændringer for felter, der bruger `autoIncrement property`. Et eksempel på et felt, der bruger egenskaben, er feltet Heltal i tabellerne Fejlmeddelelser og Momsrapportlinje.

Af hensyn til ydeevnen er ændringsloggen deaktiveret under opgradering af [!INCLUDE [prod_short](includes/prod_short.md)] til næste version. Ud over at gøre opgraderingsprocessen hurtigere kan du også reducere rodet i loggen. Så snart opgraderingen er fuldført, begynder logfilen at registrere ændringer igen.

> [!Important]
> Ændringer i poster i **ændringslogposter** efter brugerens session genstartes først, hvilket sker på følgende måde:
>
> - Sessionen er udløbet og er blevet opdateret.
> - Brugeren har valgt et andet regnskab eller Rollecenter.
> - Bruger har logget af og på igen.

## Indstilling af ændringsloggen

Du aktiverer og deaktiverer ændringsloggen på siden **Opsætning af ændringslog**. Når du gør det, logføres aktiviteten, så du altid kan se, hvem der har foretaget ændringen.

Hvis du på siden **Opsætning af ændringslog** vælger handlingen **Tabeller**, kan du angive, hvilke tabeller du vil spore ændringer for, og hvilke ændringer du vil spore. [!INCLUDE[prod_short](includes/prod_short.md)] sporer også flere systemtabeller.

> [!NOTE]
> Du kan overvåge bestemte felter for ændringer, f.eks. felter, der indeholder følsomme data, ved at oprette felt overvågning. Hvis du vil undgå redundans, vil tabellen med feltet ikke være tilgængelig for opsætningen af ændringslog. Du kan finde flere oplysninger i [Overvåge følsomme felter](across-log-changes.md#monitor-sensitive-fields).

Når du har konfigureret ændringsloggen, aktiveret den og ændret data, kan du få vist og filtrere ændringerne på siden **Ændringslogposter**. Hvis du vil slette poster, skal du oprette en opbevaringspolitik, hvor du kan angive filtre, der er baseret på datoer og klokkeslæt. Du kan få mere at vide om opbevaringspolitikker i [Definere opbevaringspolitikker](admin-data-retention-policies.md).  

## Analysere data i ændringsloggen

Du kan bruge funktionen **Dataanalyse** til at analysere data i ændringsloggen fra siden [Ændringslogposter](https://businesscentral.dynamics.com/?page=595). Du behøver ikke at køre en rapport eller åbne et andet program, f.eks. Excel. Funktionen indeholder en interaktiv og alsidig måde at beregne, opsummere og gennemgå data på. I stedet for at køre rapporter med indstillinger og filtre kan du tilføje flere faner, der repræsenterer forskellige opgaver eller visninger på dataene. Nogle eksempler er "Hvem ændrede hvilke data og hvornår" eller "Data ændres efter tabel/felt" eller enhver anden visning, du kan forestille dig. Du kan få mere at vide om, hvordan du bruger funktionen **Dataanalyse** ved at gå til [Analysér liste og forespørge på data med analysetilstand](analysis-mode.md).

### Ændre log ad hoc-analysescenarier

Følgende afsnit indeholder eksempler på scenarier, hvor analyse af ændringsloggen kan hjælpe dig med at overvåge og registrere vigtige ændringer.

| Område | Til... | Åbn denne side i analysetilstand | Brug af disse felter |
| ---- | ----- | ------------------------------- |------------------- |
| [Hvem ændrede hvilke data og hvornår](#example-who-changed-what-data-and-when) | Se, hvem ændrede hvilke data. | [Ændringslogposter](https://businesscentral.dynamics.com/?page=595) | **Bruger-id**, **Dato og klokkeslæt**, **Tabeltitel**, **Felttekst**, **Primær nøgleværdi 2**, **Primær nøgleværdi 3**, **Ændringstype**, **Gammel værdi** og **Ny værdi**. |
| [Dataændringer efter tabel/felt](#example-data-changes-by-tablefield) | Se dataændringer efter tabel/felt, og hvem der har foretaget ændringen. | [Ændringslogposter](https://businesscentral.dynamics.com/?page=595) | **Tabeltitel**, **Felttitel**, **Bruger-id**, **Dato og klokkeslæt**, **Primær nøgleværdi 2**, **Primær nøgleværdi 3**, **Ændringstype**, **Gammel værdi** og **Ny værdi**. |

### Eksempel: Hvem ændrede hvilke data og hvornår

Følg disse trin for at analysere, hvem der har ændret hvilke data hvornår:

1. Åbn [Ændre logposter](https://businesscentral.dynamics.com/?page=595)-listen, og vælg :::image type="content" source="media/analysis-mode-icon.png" alt-text="Aktivér analysetilstand."::: ikon for at tænde for analysetilstand.
1. Fjern alle kolonner i menuen **Kolonner** (markér feltet ud for feltet **Søg** i højre side).
1. Træk feltet **Bruger-id** (hvem gjorde det) til området **Rækkegrupper**.
1. Vælg nu følgende felter:
   - Hvis du vil vise, hvornår det skete, skal du vælge **Dato og klokkeslæt**.
   - Hvis du vil vise tabellen, hvor det skete, skal du vælge **Tabeltekst**. 
   - Hvis du vil have vist dette felt, skal du vælge **Felttekst**.
   - Hvis du vil have vist feltkoden, skal du vælge **Primær nøgleværdi 2**. 
   - Hvis du vil have vist virksomhedsnavnet, skal du vælge **Primær nøgleværdi 3**.
   - Hvis du vil vise, om ændringen var en indsættelses-, opdaterings- eller slettehandling, skal du vælge **Ændringstype**.
   - Hvis du vil have vist ændringen, skal du vælge **Gammel værdi** og **Ny værdi**.
1. Omdøb din analysefane til **Hvem ændrede hvilke data og hvornår** eller noget, der beskriver denne analyse.

Følgende billede viser resultatet af disse trin.

:::image type="content" source=" media/data-analysis-change-log-entries-Who-changed-What-data-When.png" alt-text="Eksempel på, hvordan du udfører dataanalyse på siden Ændringslogposter (Hvem har ændret hvilke data hvornår)." lightbox="media/data-analysis-change-log-entries-Who-changed-What-data-When.png":::

### Eksempel: dataændringer efter tabel/felt

Følg disse trin for at analysere dataændringer efter tabel/felt:

1. Åbn [Ændre logposter](https://businesscentral.dynamics.com/?page=595)-listen, og vælg :::image type="content" source="media/analysis-mode-icon.png" alt-text="Aktivér analysetilstand."::: ikon for at tænde for analysetilstand.
1. Fjern alle kolonner i menuen **Kolonner** (markér feltet ud for feltet **Søg** i højre side).
1. Træk felterne **Tabeltekst** (i hvilken tabel) og **Felttekst** (på hvilket felt) til **området Rækkegrupper**.
1. Vælg nu følgende felter:
   - Hvis du vil vise, hvornår det skete, skal du vælge **Dato og klokkeslæt**
   - Hvis du vil vise, hvem der har foretaget ændringen, skal du vælge **Bruger-id**.
   - Hvis du vil have vist feltkoden, skal du vælge **Primær nøgleværdi 2**.
   - Hvis du vil have vist virksomhedsnavnet, skal du vælge **Primær nøgleværdi 3** (typisk virksomhedsnavn), 
   - Hvis du vil vise, om ændringen var en indsættelses-, opdaterings- eller slettehandling, skal du vælge **Ændringstype**.
   - Hvis du vil have vist ændringen, skal du vælge **Gammel værdi** og **Ny værdi**.
1. Omdøb din analysefane til **Dataændringer efter tabel + felt** eller noget, der beskriver denne analyse.

Følgende billede viser resultatet af disse trin.

:::image type="content" source=" media/data-analysis-change-log-entries-data-changes-by-table-field.png" alt-text="Eksempel på, hvordan du udfører dataanalyse på siden Ændringslogposter (dataændringer efter tabel/felt)." lightbox="media/data-analysis-change-log-entries-data-changes-by-table-field.png":::

## Om aktivitetslogfiler

Fra nogle sider i [!INCLUDE [prod_short](includes/prod_short.md)] kan du få vist en aktivitetslog, der viser status og eventuelle fejl i filer, som du eksporterer fra eller importerer til [!INCLUDE [prod_short](includes/prod_short.md)].  

### Arbejde med aktivitetslogfiler

Oplysningerne vises på siden **Aktivitetslog** i overensstemmelse med den kontekst, de åbnes fra. Du kan f.eks. åbne siden fra siderne **Opsætning af dokumentudvekslingstjeneste**, **Indgående bilag**, **Bogført salgsfaktura** og **Bogført salgskreditnota**. Du kan tømme listen med logposter eller blot rydde oversigten over poster, der er ældre end syv dage.  

## Overvåge følsomme felter

Det er vigtigt for de fleste virksomheder at holde følsomme data sikre og private. Hvis du vil tilføje et sikkerhedslag, kan du overvåge vigtige felter og få besked pr. e-mail, når nogen ændrer en værdi. Du kan f.eks. få besked, hvis nogen ændrer virksomhedens IBAN-nummer.

> [!NOTE]
> Hvis du sender meddelelser via e-mail, kræver det, at du konfigurerer e-mail-funktionen i [!INCLUDE[prod_short](includes/prod_short.md)]. Du kan finde flere oplysninger i [Konfigurer mail](admin-how-setup-email.md).

### Konfigurer feltovervågning

Du kan bruge installationsprogrammet **Overvågning af klargøring af feltovervågning** til at angive de felter, der skal overvåges, på basis af filterkriterier, f.eks. klassificeringen af data følsomhed for felterne. Du kan finde flere oplysninger i [Klassificere datafølsomhed](admin-classifying-data-sensitivity.md). Du kan også bruge vejledningen til at angive den person, der skal modtage en e-mail-notifikation, når der sker ændringer, og den e-mail-konto, der sender besked-e-mailen. Angiv både brugermeddelelsen og den konto, som du vil sende notifikationen fra. Når du er færdig med guiden, kan du administrere indstillingerne for feltovervågning på siden **Opsætning af feltovervågning**.

> [!NOTE]
> Når du angiver den e-mail-konto, der skal sendes beskeder fra, skal du tilføje enten kontotyperne **Microsoft 365** eller **SMTP**. Meddelelser skal sendes fra en konto, der ikke er knyttet til en aktuel bruger. Du kan derfor ikke vælge kontotypen **Aktuel bruger**. Hvis du gør det, sendes der ikke beskeder.

Over tid vil listen over poster på siden **Overvågning af feltlogposter** vokse. Hvis du vil reducere antallet af poster, kan du oprette en opbevaringspolitik, der sletter poster efter en angivet periode. Du kan finde flere oplysninger i [Definere opbevaringspolitikker](admin-data-retention-policies.md).

Når du opretter feltovervågning, eller du ændrer noget i opsætningen, oprettes der en post for ændringerne. Du kan angive, om du vil have vist poster, der er relateret til overvågningsopsætningen, ved at vise eller skjule dem.

Du kan administrere indstillingerne for felt overvågning, f.eks. om der skal sendes en e-mail-besked eller kun skal logge af ændringen, for hvert felt på siden **Kladde over overvågede felter**. Siden er også det sted, hvor du kan tilføje eller fjerne felter, der skal overvåges.

> [!NOTE]
> Når du har tilføjet et eller flere felter og startet overvågning, skal du logge af [!INCLUDE[prod_short](includes/prod_short.md)] og logge på igen for at anvende dine indstillinger.

### Arbejde med feltovervågning

Alle ændrede værdier for overvågede felter er tilgængelige på siden over **Overvågning af feltlogposter**. Indtast følgende oplysninger til dette eksempel:

- Feltet, værdien er ændret for.
- De oprindelige og nye værdier.
- Hvem der foretog ændringen, og hvornår de gjorde det.

Hvis du vil undersøge en ændring, skal du vælge en værdi for at åbne den side, hvor den blev oprettet. Hvis du vil have vist en liste over alle poster, skal du vælge **Feltændringsposter**.

### Vise feltovervågningstelemetri

Du kan konfigurere [!INCLUDE[prod_short](includes/prod_short.md)] til at sende feltovervågningsaktivitet til en Application Insights-ressource i Microsoft Azure. Derefter kan du bruge Azure Monitor til at oprette rapporter og konfigurere påmindelser i de indsamlede data. Du kan finde flere oplysninger i følgende artikler i [!INCLUDE[prod_short](includes/prod_short.md)] hjælp til udviklere og it-eksperter:

- [Overvåge og analysere telemetri - aktivere Application Insights](/dynamics365/business-central/dev-itpro/administration/telemetry-overview?toc=/dynamics365/business-central/toc.json#enable)
- [Analysere feltovervågningstelemetri](/dynamics365/business-central/dev-itpro/administration/telemetry-field-monitoring-trace?toc=/dynamics365/business-central/toc.json)

## Definere opbevaringspolitikker

Du kan oprette opbevaringspolitikker for at slette unødvendige data i loggen efter en bestemt periode, du har angivet. Du kan f.eks. overskride antallet af poster i en log. Ved at rydde op i gamle poster kan du gøre det nemmere at fokusere på mere end nylig og dermed mere relevante poster. Du kan få mere at vide om opbevaringspolitikker i [Definere opbevaringspolitikker](admin-data-retention-policies.md).

## Se også

[Overvåge følsomme felter](across-log-changes.md#monitor-sensitive-fields)  
[Analysere feltovervågningstelemetri](/dynamics365/business-central/dev-itpro/administration/telemetry-field-monitoring-trace?toc=/dynamics365/business-central/toc.json)  
[Definere opbevaringspolitikker](admin-data-retention-policies.md)  
[Ændre grundlæggende indstillinger](ui-change-basic-settings.md)  
[Sortere, søge og filtrere](ui-enter-criteria-filters.md)  
[Søge efter sider og oplysninger med Fortæl mig](ui-search.md)  
[Tildele tilladelser til brugere og grupper](ui-define-granular-permissions.md)  
[Arbejd med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
