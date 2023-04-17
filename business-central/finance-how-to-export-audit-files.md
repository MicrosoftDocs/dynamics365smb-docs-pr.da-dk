---
title: Eksport af revisionsfil
description: 'I denne artikel forklares det, hvordan du opretter forskellige eksportformater og derefter bruger dem, baseret på revisions- eller myndighedskrav.'
author: altotovi
ms.service: dynamics365-business-central
ms.topic: how-to
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 'audit, export, SIE, SAF-T, FAC, GDPdU, file export'
ms.search.form: '5260, 5261, 5264, 5266, 5267, 5270'
ms.date: 04/04/2023
ms.author: altotovi
ms.reviewer: null
---

# Eksport af revisionsfil

Udførsel af bogføringsoplysninger fra systemet er en fælles anmodning fra nogle lokale myndigheder eller revisorer. Udførsel af formater og nødvendige oplysninger kan være forskellige. Poster til eksport er som regel finansposter eller momsposter. Der er dog nogle gange brug for andre oplysninger.

**Eksport af revisionsfiler** er en forudinstalleret udvidelse, som du kan bruge til at eksportere forskellige poster, baseret på revisions- eller myndighedskrav. Uanset formattypen eller posterne kan du bruge udvidelsens funktionalitet til at styre dataeksportprocessen. Funktionen har ikke et forudinstalleret filformat til eksport. Du skal derfor enten installere en app, der har et specifikt format (f. eks. SIE, SAF-T eller FAC), eller udvikle din egen.

> [!NOTE]
> I øjeblikket kan du vælge SIE- eller SAF-T som en ekstra app. Partnere kan også udvikle et brugerdefineret format. Antallet af tilgængelige formater øges med tiden.

## Opsætning af eksport af revisionsfil

1. Vælg søgeknappen ![Forstørrelsesglas-knappen, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig"), angiv **Opsætning af eksport af revisionsfil**, og vælg derefter det relaterede link.
2. Følg disse trin på siden **Opsætning af eksport af revisionsfil**:

    1. I oversigtspanelet **Generelt** i feltet **Formatkode til eksport af revisionsfiler** skal du angive standardformatkoden for eksporten af revisionsfilen. Kun de formater, der blev aktiveret, da et bestemt filformat blev installeret fra funktionsstyring, og dem, der blev tilføjet som brugerdefinerede formater, er tilgængelige.
    2. I oversigtspanelet **Datakvalitet** skal du markere afkrydsningsfeltet **Kontroller firmaoplysninger** for at få besked om felter med virksomhedsoplysninger, der ikke er konfigureret korrekt.
    3. Vælg afkrydsningsfeltet **Tjek debitor** for at få besked om felter, der ikke er konfigureret korrekt for specifikke debitorer.
    4. Vælg afkrydsningsfeltet **Tjek kreditor** for at få besked om felter, der ikke er konfigureret korrekt for specifikke kreditorer.
    5. Vælg afkrydsningsfeltet **Tjek bankkonto** for at få besked om felter, der ikke er konfigureret korrekt for specifikke bankkonti.
    6. Marker afkrydsningsfeltet **Tjek postnummer** for at få besked om et postnummer, der ikke er konfigureret korrekt.
    7. Marker afkrydsningsfeltet **Kontroller adresse** for at få besked, når en adresse ikke er konfigureret korrekt.
    8. I feltet **Standardpostnummer** skal du angive det postnummer, der skal bruges, hvis der ikke er angivet et postnummer på debitor- eller kreditorkortet.

3. Vælg søgeknappen ![Forstørrelsesglas-knappen, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig"), angiv **Formatopsætning af eksport af revisionsfil**, og vælg derefter det relaterede link.
4. Følg disse trin på siden **Formatopsætning af eksport af revisionsfil**:

    1. Vælg det format for revisionsfil til eksport, der skal bruges til konfigurationen. Kun de formater, der blev aktiveret, da et bestemt filformat blev installeret fra funktionsstyring, og dem, der blev tilføjet som brugerdefinerede formater, er tilgængelige.
    2. I feltet **Revisionsfilnavn** skal du angive standardfilnavnet eller skabelonen til filnavnet til den revisionsfil, du vil eksportere.
    3. Marker afkrydsningsfeltet **Arkiver til Zip** for automatisk at zippe eksporterede filer.

## Angiv finanskontotilknytningen for eksport af revisionsfiler

De fleste formater, der kræves af myndighederne i finanskonti, kræver en bestemt standardkontoplan. Når du har konfigureret finanskontiene, bliver den eksporterede fil derfor baseret på tilknytningerne. Du kan bruge flere tilknytninger i systemet.

Følg disse trin for at angive finanskontotilknytningen for eksport af revisionsfiler.

1. Vælg søgeknappen ![Forstørrelsesglas-knappen, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig"), angiv **Tilknytning af finanskonto**, og vælg derefter det relaterede link.
2. Vælg **Ny** på siden **Finanstilknytning** for at oprette en tilknytning.
3. I feltet **Kode** angives den tilknytningskode, der repræsenterer rapporteringsperioden.
4. Vælg den relevante finanskonto i feltet **Standardkontotype**.
5. I feltet **Format til eksport af revisionsfiler** skal du angive det eksportformat for overvågningsfilen, som standardfinanskontiene er tilknyttet.
6. I feltet **Periodetype** angiver systemet en regnskabsperiode eller en brugerdefineret periodetype, der har en fleksibel startdato og et fleksibelt tidspunkt baseret på dit valg. Hvis du vælger en bestemt regnskabsperiode, angives feltet til **Regnskabsperiode**. Ellers vil den blive sat til **Dataområde**.
7. Angiv startdatoen for den regnskabsperiode, der skal bruges som rapporteringsperiode, i feltet **Regnskabsperiode**, hvis de skal være ens.
8. Hvis du angiver feltet **Regnskabsperiode**, angives felterne **Startdato** og **Slutdato** automatisk på grundlag af den periode, du har angivet. Hvis du ikke gør det, kan du manuelt angive start- og slutdatoen for rapporteringen.
9. Hvis du allerede har tilføjet en standardkontoplan, skal du følge disse trin:

    1. I **Standardkontokategorinr.** felt, angiv kategorien af den standardkonto eller gruppekode, der bruges til tilknytning.
    2. I feltet **Standardkontonr.** skal du angive den standardkontokode eller gruppekode, der bruges til tilknytning.

10. Vælg afkrydsningsfeltet **Medtag indgående saldo** for at overveje, om den indgående saldo på finanskontoen af typen **Statuskonto** skal tages i betragtning ved tilknytning i stedet for rapporteringsperiodens nettoændring.
11. Start tilknytning ved at følge disse trin:

    1. Generer linjerne på siden **Tilknytning af finanskonto** baseret på en eksisterende kontoplan, ved at vælge **Initialiser kilde til tilknytning**. Hvis du vil kopiere finanskontotilknytningen fra en anden tilknytningskode, skal du vælge **Kopier fra en anden tilknytning**. Når du er færdig med at oprette linjer, vil alle finanskonti med bogførte poster blive markeret med grønt.
    2. Hvis du kun vil markere finanskonti med poster, skal du vælge **Opdater finansposttilgængelighed**. Hvis indstillingen **Medtag indgående saldo** er aktiveret, indgår alle bogførte finansposter med henblik på beregning. Ellers er det kun finansposter i rapporteringsperioden, der tages i betragtning.

## Eksporter revisionsfil

1. Vælg søgeknappen ![Forstørrelsesglas-knappen, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig"), angiv **Dokumenter til eksport af revisionsfiler**, og vælg derefter det relaterede link.
2. Vælg **Ny** på siden **Dokumenter til eksport af revisionsfiler**.
3. Benyt følgende fremgangsmåde i oversigtspanelet **Generelt**:

    1. I feltet **Format til eksport af revisionsfiler** skal du vælge det format, der bruges til at eksportere revisionsfilen.
    2. I feltet **Finanskontotilknytningskode** skal du vælge finanskontoens tilknytningskode til rapporteringsperioden.
    3. Marker afkrydsningsfeltet **Opdelt efter måned**, hvis der skal oprettes flere overvågningsfiler pr. måned.
    4. Marker afkrydsningsfeltet **Opdelt efter dato**, hvis der skal oprettes flere overvågningsfiler pr. dag.
    5. Skriv den bemærkning, der skal medtages i sidehovedet i revisionsfilen, i feltet **Sidehovedbemærkning** .
    6. Angiver den kontakt, der eksporteres til overskriften i revisionsfilen i feltet **Kontakt**.
    7. Marker afkrydsningsfeltet **Opret flere zip-filer** for at oprette flere zip-filer.

        > [!IMPORTANT]
        > Du skal kun markere dette afkrydsningsfelt, hvis du tidligere har installeret nogle af apps apps eller oprettet et brugerdefineret. Installation af et eller flere af de specifikke formater vil sandsynligvis føje felter og funktioner til **Eksport af revisionsfiler**-funktionen, baseret på formatkravene.

4. Benyt følgende fremgangsmåde i oversigtspanelet **Behandling**:

    1. Marker afkrydsningsfeltet **Parallel behandling**, hvis du vil behandle overvågning af parallelle baggrundsjob med parallelle job. Fjern markeringen i afkrydsningsfeltet for at eksportere data i den aktuelle session.
    2. Hvis du har markeret afkrydsningsfeltet **Parallel behandling** i feltet **Maks. antal sager** skal du angive det maksimale antal baggrundsjob, der kan køres samtidigt.
    3. Angiv Tidligste dato og tidligste klokkeslæt, hvor baggrundsjobbet skal køres, i feltet **tidligste start dato/tidspunkt**. Hvis du kører processen ved at vælge **Start**, kan du spore status for oversigtspanelerne **Behandling** og **Linjer**.

5. Når du er færdig, skal du vælge **Indlæs som fil** for at hente revisionsfilen til den valgte linje.

> [!IMPORTANT]
> Hvis du har flere poster, der skal eksporteres, anbefales det, at du eksporterer dem i den aktuelle session pga. mulige problemer med ydeevnen. I stedet anbefales det, at du bruger parallel behandling i ikke-arbejdsdage eller timer.

## Se også

[Økonomistyring](finance.md)  
[Forstå Finans og Kontoplan](finance-general-ledger.md)  
[Arbejde med dimensioner](finance-dimensions.md)  
[Arbejd med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)

[!INCLUDE[footer-include](includes/footer-banner.md)]
