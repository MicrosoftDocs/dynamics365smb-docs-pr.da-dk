---
title: Diagram over bæredygtighedskonti og finans
description: 'Få mere at vide om, hvordan du administrerer bæredygtighedskontoplaner, kategorier og underkategorier og detaljer om bæredygtighedsposter.'
author: altotovi
ms.topic: conceptual
ms.devlang: al
ms.search.keywords: 'Sustainability, ESG, emission, GHG, CSRD, CoA, Chart, Account, Ledger'
ms.search.form: '6210, 6213, 6214, 6220'
ms.date: 04/02/2024
ms.author: altotovi
ms.service: dynamics-365-business-central
---

# Diagram over bæredygtighedskonti og finans 

## Diagram over bæredygtighedskonti  

**Planen for bæredygtighedsregnskaber** (CoSA) udgør den grundlæggende strukturerede liste, der bruges til registrering af alle emissionsdata. Det fungerer som en ramme, der kategoriserer og organiserer bæredygtighedskonti baseret på deres attributter, såsom omfang eller andre grupperinger. Hver konto tildeles typisk en unik kode eller et unikt nummer til nem reference og sporing efter samme struktur som en traditionel **kontoplan**, men tilpasset specifikt til overvågning af bæredygtighedsrelaterede data og målinger i en organisation. 
 
Brugere kan tilføje **kontokategorier** og **underkategorier** for at definere, hvordan systemet opfører sig, vælge dedikerede emissioner til sporing, emissionsfaktorer, formler og lignende konfigurationer.  

>[!NOTE]
>For at blive familariseret med scopes, baseret på GHG (drivhusgasser) standarder, er der tre emissionsomfang:  
>- **Omfang 1-udledninger**: omfatter udledninger, der udsendes fra stationær og mobil forbrænding og fra utilsigtet flygtig udledning. 
>- **Omfang 2-udledninger**: omfatter indirekte udledninger fra den generation af energi, der er købt fra en udbyder af forsyningsudbydere. 
>- **Omfang 3-udledninger**: omfatter et bredt spektrum af emissioner fra købte varer og tjenesteydelser og kapitalgoder, brændstof- og energirelaterede aktiviteter, Upstream- og Downstream-transport, produceret affald, forretningsrejser og medarbejderpendling osv. 

Fra **Diagram over bæredygtighedskonti** (CoSA) kan du gøre ting som at:  

-   Vise rapporter med finansposter for bæredygtighed og saldi. 
-   Åbne **Kort over bæredygtighedskonto** for at tilføje eller ændre indstillinger.  
-   Se kategorien og underkategorien for den pågældende konto.   
-   Se separate saldi for hver af emissionerne for en enkelt konto. 
-   Føj en eller flere **dimensioner** til hver af kontiene, og angiv dimensionsfilter. 
    
Du kan tilføje, ændre eller slette **Bæredygtighedskonti**. For at undgå uoverensstemmelser kan du dog ikke slette en **bæredygtighedskonto**, hvis der er knyttet en eller flere poster til denne konto.  

### Tilføje eller ændre konti  

1. Vælg ![Lightbulb, der åbner funktionen Fortæl mig 3.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **Diagram over bæredygtighedskonti**, og derefter vælge det relaterede link. 
2. På siden **Diagram over bæredygtighedskonti** (CoSA) kan du åbne hver **Bæredygtighedskonto** og derefter tilføje eller ændre indstillinger. Placer markøren over et felt for at se en kort beskrivelse. 

For kontoer af typen **I alt** skal du udfylde feltet **Sammentælling**. For kontoer af typen **Til-sum** udfyldes feltet automatisk af funktionen Indryk. Når du har oprettet kontiene, skal du vælge handlingen **Indryk diagram over bæredygtighedskonti** for at gøre det.  

>[!IMPORTANT]
>Hvis du har angivet definitioner i felterne **I alt** for konti med **Til-sum**, før du anvender indrykningsfunktionen, skal du angive dem igen bagefter, fordi funktionen overskriver værdierne i alle felter med **Til-sum**.  

### Slet konti  

Du kan slette en **Bæredygtighedskonto**. Før du sletter den, skal du dog sikre dig, at der er en eller flere poster knyttet til denne konto, da Business Central forhindrer dig i at slette en **Bæredygtighedskonto** i denne situation.  

## Kontokategorier   

Brugere skal tilføje **Bæredygtighedskontokategorien** til hver af **Bæredygtighedskontiene** for at definere, hvordan systemet opfører sig, vælge emissionsomfang, dedikerede emissioner til sporing, formler og lignende konfigurationer.  

Følg trinnene for at gennemgå **Kategorier for bæredygtighedskonti**: 

1.  Vælg ![Lightbulb, der åbner funktionen Fortæl mig 3.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **Kategorier af bæredygtighedskonti**, og derefter vælge det relaterede link. 
2.  På siden **Bæredygtighedskontokategorier** kan du redigere den eksisterende liste eller oprette en ny kategori. For at oprette en ny kategori skal du vælge handlingen **Ny**.  
3.  Udfyld felterne **Kode** og **Beskrivelse**.   
4.  Angiv feltet **Udledningsomfang** ved at vælge en af indstillingerne for omfanget.  
5.  Vælg de drivhusgasudledninger, du vil spore. I øjeblikket kan du bruge en af mulighederne: **CO2**, **CH4** eller **N2O**. Du kan vælge en hvilken som helst kombination, du vil spore, men du skal have mindst én emission til sporing.  
6.  I feltet **Beregningsgrundlag** kan du vælge en hvilken som helst af de formler, du vil bruge, hvis du ikke kender den nøjagtige emissionsmængde. Her kan du angive beregningsgrundlaget (formlen) for udledningsberegningen. Du kan vælge en af følgende indstillinger: **Brændstof/elektricitet**, **Afstand**, **Installation** eller **Brugerdefineret**. 
7.  Hvis du vælger **Brugerdefineret** formel, kan du konfigurere brugerdefineret beskrivelse i feltet **Brugerdefineret værdi**.  

>[!NOTE]
>Hvis dette sæt tilbudte formler i feltet **Beregningsgrundlag** ikke er nok, kan du udvide dette felt og føje flere beregninger til systemet, der skal bruges i **Bæredygtighedskladder**.  

Hvis du bruger **Beregningsgrundlaget** (formler), er der en forklaring på, hvordan systemet beregner baseret på den indstilling, du har valgt (**EF** er den **Udledningsfaktor**, du kan konfigurere på siden **Underkategori for bæredygtighedskonto**): 

|  Udledningstype  |  Beregningsgrundlag  |  Formel         | Kommentar      |
|------------|--------------|------------------------------|---------------------------------|
| **OMFANG 1**  |
| Stationær forbrænding | Brændstof/elektricitet | Udledning = Brændstof * EF | _dvs. brændstof = mængde af brændstof, der bruges til kedler, varmeapparater, termiske oxidationsmidler..._ |
| Mobil forbrænding | Brændstof/elektricitet | Udledning = Brændstof * EF | _dvs. brændstof = mængde brændstof, der bruges til vejgående eller ikke-vejgående køretøjer, jernbane ..._ |
|  |  |  Udledning = Afstand * EF | _dvs. afstand = Milleage af on-road eller ikke-vejgående køretøjer, jernbane..._ |
| Flygtige udledninger | Installation | Udledning = Installationsmultiplikator * Brugerdefineret mængde / 100 * Tidsfaktor | _dvs. brugerdefineret beløb = monteringstab, årlig lækagehastighed..._ |
| **OMFANG 2**  |
| Forsyningsudbydere | Brændstof/elektricitet | Udledning = Elektricitet * EF | _dvs. brændstof/elektricitet = elektricitetsmængde, dampmængde, varmeenhed..._ |
|  | Brugerdefineret | Udledning = Brugerdefineret mængde * EF | _dvs. brugerdefineret mængde = termisk enhed, ton-time ..._ |
| **OMFANG 3**  |
| Købte varer og tjenesteydelser samt investeringsgoder | Brugerdefineret | Udledning = Brugerdefineret mængde * EF | _dvs. brugerdefineret beløb = omkostninger (GL)..._ |
| Upstream-transport og distribution | Afstand | Udledning = Afstand * EF |  |
|  | Afstand | Udledning = Afstand * Multiplier * EF | _Multiplikator = Toins af last_ |
| Downstream-transport og distribution | Afstand | Udledning = Afstand * EF |  |
|  | Afstand | Udledning = Afstand * Multiplier * EF | _Multiplikator = Toins af last_ |
| Affald genereret ved drift og bortskaffelse af solgte produkter | Brugerdefineret | Udledning = Brugerdefineret mængde * EF | _dvs. brugerdefineret beløb = Affald_ |
| Forretningsrejser og medarbejderpendling | Afstand | Udledning = Afstand * EF | _dvs. afstand = Milleage af den brugte firmabil, udlejningsbil, tog, fly..._ |
|  | Brugerdefineret | Udledning = Brugerdefineret mængde * EF | _i.e. brugerdefineret beløb = hotelophold..._ |
|  | Brændstof/elektricitet | Udledning = Brændstof * EF | _dvs. brændstof = Mængde brændstof brugt i firmabilen, lejebilen..._ |

## Kontoens underkategorier  

Brugere skal føje **Bæredygtighedskonto-underkategorien** til hver af **Bæredygtighedskonti** for at definere udledningsfaktorer, der skal bruges i formlerne, men den er baseret på valget af udledningssporing i **kategorien Bæredygtighedskonto**.  

Følg trinnene for at gennemgå **Underkategorier for bæredygtighedskonto**:  

1.  Vælg ![Lightbulb, der åbner funktionen Fortæl mig 3.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **Underkategorier af bæredygtighedskonti**, og derefter vælge det relaterede link. 
2.  På siden **Underkategorier af bæredygtighedskonti** kan du redigere den eksisterende liste eller oprette en ny kategori. For at oprette en ny kategori skal du vælge handlingen **Ny**.  
3.  Udfyld felterne **Kode** og **Beskrivelse**.   
4.  Baseret på de drivhusgasudledninger, du vil spore i **kategorien Bæredygtighedskonto** og knytte denne underkategori til, kan du også udfylde en eller flere udledningsfaktorer: 

   - **Udledningsfaktor CO2** - Angiver en udledningsfaktor for CO2-udledning.  
   - **Udledningsfaktor CH4** - Angiver en udledningsfaktor for CH4-udledning. 
   - **Udledningsfaktor N2O** - Angiver en udledningsfaktor for N2O-udledning.  

5.  Hvis denne underkategori er relateret til vedvarende energi, skal du vælge feltet **Vedvarende energi**.   

>[!NOTE]
>Felterne **Importér data** og **Importer fra** er beregnet til potentiel integration med eksterne systemer, der bruges til indsamling af udledningsfaktorer, men i **2024 udgivelsesbølge 1** kan de som standard ikke bruges som en funktion.  

## Finansposter for bæredygtighed  

**Bæredygtighedsposten** gemmer historikken over alle bogførte bæredygtighedstransaktioner og organiserer alle emissionsdata i henhold til **Diagram over bæredygtighedskonti**. Når en bruger bogfører **Bæredygtighedskladden**, registreres alle vigtige data der. Alle aktive rapporter genereres på baggrund af **Bæredygtighedsposterne**.   

Brugeren kan åbne denne finanspost for en bestemt konto ved hjælp af handlingen **Vareposter** fra siden **Bæredygtighedskontoplan**, eller hvis du vil åbne alle posterne, skal du vælge den ![pære, der åbner funktionen Fortæl mig, 3.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, indtast **Finansposter for bæredygtighed**, og vælg derefter det relaterede link. Placer markøren over et felt for at se en kort beskrivelse.  

>[!IMPORTANT]
>Når du først har bogført dine data i bæredygtighedsregnskabet, kan du ikke slette dem. Hvis du har lavet en fejl, kan du bogføre den omvendte transaktion ved hjælp af de samme detaljer, men ved hjælp af det negative tegn for beløb.  

## Se også  
[Finance](finance.md)    
[Oversigt over styring af bæredygtighed](finance-manage-sustainability.md)
[Opsætning af bæredygtighed](finance-sustainability-setup.md)
[Sådan kan du registrere udledninger](finance-sustainability-journal.md)
[Arbejde med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]
