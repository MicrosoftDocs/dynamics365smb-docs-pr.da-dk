---
title: Diagram over bæredygtighedskonti og finans
description: 'Få mere at vide om, hvordan du administrerer bæredygtighedskontoplaner (CoSA), kategorier og underkategorier og detaljer om bæredygtighedsposter.'
author: altotovi
ms.topic: conceptual
ms.devlang: al
ms.search.keywords: 'Sustainability, ESG, emission, GHG, CSRD, CoA, Chart, Account, Ledger'
ms.search.form: '6210, 6213, 6214, 6220'
ms.date: 05/07/2024
ms.author: altotovi
ms.service: dynamics-365-business-central
---

# Diagram over bæredygtighedskonti og finans

## Diagram over bæredygtighedskonti

Planen for bæredygtighedsregnskaber (CoSA) udgør den grundlæggende strukturerede liste, der bruges til registrering af alle emissionsdata. Det fungerer som en ramme, der kategoriserer og organiserer bæredygtighedskonti baseret på deres attributter, såsom omfang eller andre grupperinger. Hver konto tildeles typisk en unik kode eller et unikt nummer for nem reference og sporing. Det har samme struktur som en traditionel kontoplan, men er tilpasset specifikt til at overvåge bæredygtighedsrelaterede data og målinger i en organisation.

Brugere kan tilføje bæredygtighedskontokategorier og underkategorier for bæredygtighedskonti for at definere, hvordan systemet opfører sig. På denne måde kan de vælge dedikerede emissioner til sporing, emissionsfaktorer, formler og lignende konfigurationer.

> [!NOTE]
> Baseret på GHG (drivhusgasser)-standarder, er der tre udledningsomfang:
>
> - **Omfang 1-udledninger** omfatter udledninger, der udsendes fra stationær og mobil forbrænding og fra utilsigtet flygtig udledning.
> - **Omfang 2-udledninger** omfatter indirekte udledninger fra den generation af energi, der er købt fra en udbyder af forsyningsudbydere.
> - **Omfang 3-udledninger** omfatter et bredt spektrum af emissioner fra købte varer og tjenesteydelser og kapitalgoder, brændstof- og energirelaterede aktiviteter, Upstream- og Downstream-transport, produceret affald, forretningsrejser og medarbejderpendling osv.

Fra CoSA kan du gøre ting som:

- Vise rapporter med finansposter for bæredygtighed og saldi.
- Åbne kort over bæredygtighedskonto for at tilføje eller ændre indstillinger.
- Se kategorien og underkategorien for den pågældende konto. 
- Se separate saldi for hver af udledningerne for en enkelt konto.
- Føj en eller flere dimensioner til hver konto, og angiv dimensionsfilter.

Du kan tilføje, ændre eller slette bæredygtighedskonti. For at undgå uoverensstemmelser kan du dog ikke slette en bæredygtighedskonto, hvis der er knyttet en eller flere poster til denne konto.

### Tilføje eller ændre konti

1. Vælg ![Lightbulb, der åbner funktionen Fortæl mig 3.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **Diagram over bæredygtighedskonti**, og derefter vælge det relaterede link.
2. På siden **Diagram over bæredygtighedskonti** kan du åbne hver bæredygtighedskonto og derefter tilføje eller ændre indstillinger. Placer markøren over et felt for at se en kort beskrivelse.

For kontoer af typen **I alt** skal du udfylde feltet **Sammentælling**.

For kontoer af typen **Til-sum** udfyldes feltet **Sammentælling** automatisk af funktionen Indryk. Når du har oprettet alle kontiene, skal du vælge handlingen **Indryk bæredygtighedskonto** for at køre indrykningsfunktionen og angive feltet **Sammentælling**.

> [!IMPORTANT]
> Indrykningsfunktionen overskriver værdien af alle felter for konti af typen **Til-sum**. Hvis du har angivet definitioner i felterne **Sammentælling** for **Til-sum**-omkostningssteder, før du kører indrykningsfunktionen, skal du angive dem igen.

### Slet konti

Du kan slette en bæredygtighedskonto. Du skal dog først kontrollere, at der ikke er knyttet nogen poster til den. Business Central forhindrer dig i at slette en bæredygtighedskonto, hvis der er knyttet en eller flere poster til denne konto.

## Kontokategorier

Brugere kan tilføje bæredygtighedskontokategorier og underkategorier for bæredygtighedskonti for at definere, hvordan systemet opfører sig. På denne måde kan de vælge dedikerede udledninger til sporing, udledningsfaktorer, formler og lignende konfigurationer.

Følg trinnene for at gennemgå kategorier for bæredygtighedskonti:

1. Vælg ![Lightbulb, der åbner funktionen Fortæl mig 3.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **Kategorier af bæredygtighedskonti**, og derefter vælge det relaterede link.
2. På siden **Bæredygtighedskontokategorier** kan du redigere den eksisterende liste eller oprette en ny kategori. For at oprette en ny kategori skal du vælge handlingen **Ny**.
3. Udfyld felterne **Kode** og **Beskrivelse**.
4. Angiv feltet **Udledningsomfang** ved at vælge en af indstillingerne for omfanget.
5. Vælg de drivhusgasudledninger, du vil spore. I øjeblikket kan du bruge følgende muligheder: **CO2**, **CH4** og **N2O**. Du kan vælge en hvilken som helst kombination, du vil spore, men du skal have mindst én udledning til sporing.
6. I feltet **Beregningsgrundlag** kan du vælge det beregningsgrundlag (formel), der skal bruges til udledningsberegninger, hvis du ikke kender den nøjagtige udledningsmængde. Du kan vælge en af følgende indstillinger: **Brændstof/elektricitet**, **Afstand**, **Installation** eller **Brugerdefineret**.

    > [!NOTE]
    > Hvis dette sæt tilbudte formler i feltet **Beregningsgrundlag** ikke er nok, kan du udvide dette felt og føje flere beregninger til systemet, der skal bruges i Bæredygtighedskladder.

7. Hvis du valgte **Brugerdefineret** i feltet **Beregningsgrundlag** , kan du konfigurere en brugerdefineret beskrivelse i feltet **Brugerdefineret værdi** .

Hvis du angiver feltet **Beregningsgrundlag** , forklares det i følgende tabel, hvordan systemet beregner emissioner baseret på den indstilling, du har valgt. (I denne tabel, repræsenterer *EF* den **udledningsfaktorværdi** , som du kan konfigurere på siden **Underkategori for bæredygtighedskonto**).

| Udledningstype | Beregningsgrundlag | Formel | Kommentar |
|---------------|------------------------|---------|---------|
| **Omfang 1** | | | |
| Stationær forbrænding | Brændstof/elektricitet | *Udledning* = *Brændstof* &times; *EF* | *Brændstof* = mængde af brændstof, der bruges til kedler, varmeapparater, termiske oxidationsmidler og lign. |
| Mobil forbrænding | Brændstof/elektricitet | *Udledning* = *Brændstof* &times; *EF* | *Brændstof* = mængde brændstof, der bruges til vejgående eller ikke-vejgående køretøjer, jernbane og lign. |
| | | *Udledning* = *Afstand* &times; *EF* | *Afstand* = Milleage af on-road eller ikke-vejgående køretøjer, jernbane og lign. |
| Flygtige udledninger | Installation | *Udledning* = *Installationsmultiplikator* &times; *Brugerdefineret mængde* &divide; 100 &times; *Tidsfaktor* | *Brugerdefineret beløb* = montagetab, årlig lækagehastighed og lign. |
| **Omfang 2** | | | |
| Forsyningsudbydere | Brændstof/elektricitet | *Udledning* = *Elektricitet* &times; *EF* | *Brændstof/elektricitet* = Elektricitetsmængde, dampmængde, varmeenhed og så videre |
| | Brugerdefineret | *Udledning* = *Brugerdefineret mængde* &times; *EF* | *Brugerdefineret mængde* = Termisk enhed, ton-time og så videre |
| **Omfang 3** | | | |
| Købte varer og tjenesteydelser samt investeringsgoder | Brugerdefineret | *Udledning* = *Brugerdefineret mængde* &times; *EF* | *Brugerdefineret beløb* = Omkostninger (GL) og så videre |
| Upstream-transport og distribution | Afstand | *Udledning* = *Afstand* &times; *EF* | |
| | Afstand | *Udledning* = *Afstand* &times; *Multiplikator* &times; *EF* | *Multiplikator* = Tons af last |
| Downstream-transport og distribution | Afstand | *Udledning* = *Afstand* &times; *EF* | |
| | Afstand | *Udledning* = *Afstand* &times; *Multiplikator* &times; *EF* | *Multiplikator* = Tons af last |
| Affald genereret ved drift og bortskaffelse af solgte produkter | Brugerdefineret | *Udledning* = *Brugerdefineret mængde* &times; *EF* | *Brugerdefineret beløb* = Affald |
| Forretningsrejser og medarbejderpendling | Afstand | *Udledning* = *Afstand* &times; *EF* | *Afstand* = Milleage af den brugte firmabil, udlejningsbil, tog, fly og så videre |
| | Brugerdefineret | *Udledning* = *Brugerdefineret mængde* &times; *EF* | *Brugerdefineret beløb* = Hotelophold |
| | Brændstof/elektricitet | *Udledning* = *Brændstof* &times; *EF* | *Brændstof* = Mængde brændstof brugt i firmabilen, lejebilen og så videre |

## Kontoens underkategorier

Brugere kan tilføje bæredygtighedskonto-underkategori for hver bæredygtighedskonto. Denne underkategori definerer de emissionsfaktorer, der bruges i formlerne, baseret på valget af emissionssporing i kategorien bæredygtighedskonto.

Følg trinnene for at gennemgå underkategorier for bæredygtighedskonto:

1. Vælg ![Lightbulb, der åbner funktionen Fortæl mig 3.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **Underkategorier af bæredygtighedskonti**, og derefter vælge det relaterede link. 
2. På siden **Underkategorier af bæredygtighedskonti** kan du redigere den eksisterende liste eller oprette en ny kategori. For at oprette en ny kategori skal du vælge handlingen **Ny**.
3. Udfyld felterne **Kode** og **Beskrivelse**.
4. Baseret på de drivhusgasudledninger, du vil spore i kategorien bæredygtighedskonto og knytte denne underkategori til, kan du også udfylde en eller flere udledningsfaktorer: 

    - **Udledningsfaktor CO2** – Udledningsfaktoren for udledning af kuldioxid (CO<sub>2</sub>).
    - **Udledningsfaktor CH4** - Angiver en udledningsfaktor for metan (CH<sub>4</sub>)-udledning.
    - **Udledningsfaktor N2O** – Udledningsfaktoren for udledning af kvælstofsoxid (N<sub>2</sub>O).

5. Hvis denne underkategori er relateret til vedvarende energi, skal du vælge feltet **Vedvarende energi**.

> [!NOTE]
> Felterne **Importer data** og **Importer fra** er beregnet til potentiel integration med eksterne systemer, der bruges til at indsamle udledningsfaktorer. I **udgivelsesbølge 1 i 2024** kan disse felter dog ikke bruges som en funktion som standard.

## Finansposter for bæredygtighed

Bæredygtighedsposten gemmer historikken over alle bogførte bæredygtighedstransaktioner og organiserer alle emissionsdata i henhold til Diagram over bæredygtighedskonti. Når en bruger bogfører bæredygtighedskladden, registreres alle vigtige data der. Alle aktive rapporter genereres på baggrund af bæredygtighedsposterne.

Hvis du vil åbne denne finanspost for en bestemt konto, skal du bruge handlingen **Poster** på siden **Bæredygtighedskontoplan**. Du kan åbne sagsposter ved at vælge den ![lightbulb, der åbner funktionen Fortæl mig 3.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, indtast **Finansposter for bæredygtighed**, og vælg derefter det relaterede link. Placer markøren over et felt for at se en kort beskrivelse.

> [!IMPORTANT]
> Når du først har bogført dine data i bæredygtighedsregnskabet, kan du ikke slette dem. Hvis du har lavet en fejl, kan du bogføre den omvendte transaktion ved hjælp af de samme detaljer, men ved hjælp af det negative tegn for beløb.

## Se også

[Finans](finance.md)  
[Oversigt over Ledelse af bæredygtighed](finance-manage-sustainability.md)  
[Opsætning af bæredygtighed](finance-sustainability-setup.md)  
[Sådan kan du registrere udledninger](finance-sustainability-journal.md)  
[Arbejd med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
