---
title: Betalingspraksisrapport
description: 'Få flere oplysninger om, hvordan du nemt kan oprette rapporten Betalingsmetoder for kreditorer og debitorer.'
author: altotovi
ms.topic: conceptual
ms.devlang: al
ms.search.keywords: 'payment, practices, vendor, customer, report'
ms.search.form: '686, 687, 689'
ms.date: 04/23/2024
ms.author: altotovi
ms.reviewer: bholtorf
--- 

# Betalingspraksisrapport  

Nogle lande/områder kræver, at virksomheder rapporterer betalingstider for deres kreditorer som defineret af de lokale myndigheder. Denne rapportering kan være baseret på forskellige kilder og kan sortere kreditorer baseret på deres størrelse eller definerede betalingsbetingelser, så der kan leveres rapportering til kreditorer for følgende efter behov fra lokale myndigheder:  

- Gennemsnitlig aftalt betalingsperiode  
- Gennemsnitlig faktisk betalingsperiode   
- Andelen af fakturaer, der er betalt efter udløbet af den aftalte betalingsperiode. 

Brugere kan vælge den periode, de vil køre en beregning for, og finde detaljer baseret på en gruppering, du vælger. For hver af disse grupperinger kan du finde kildeposter. 

> [!NOTE]
> Denne rapportering er indtil videre påkrævet i nogle lande, men dette er en global funktion og kan bruges overalt. I øjeblikket skal svenske virksomheder med 250 og flere ansatte hvert år rapportere til det svenske selskabsregister, hvilke betalingstider de har for køb fra virksomheder, der er mindre end dem selv. Lignende handlinger findes i Storbritannien, Australien og New Zealand.  

## Opret rapporten 

Benyt følgende fremgangsmåde for at køre rapporten **Betalingspraksis**:

1. Vælg ![Lightbulb, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **Betalingspraksis**, og vælg derefter det relaterede link. 
2. Vælg **Ny**.
3. Udfyld værdierne i følgende felter i oversigtspanelet **Generelt**.

   | Felt | Beskrivelse |
   |---------|-----------------------------------|
   | Nej | Angiver antallet af posten eller recorden for rapporten. |
   | Summeringstype | Angiv, hvordan data aggregeres. Hvis du vælger indstillingen **Perioderapport** vil være baseret på forskellige perioder, men hvis du vælger indstillingen **Firmastørrelse**, oprettes rapporten baseret på de virksomhedsstørrelser, der er konfigureret i feltet **Firmastørrelseskode** på **kreditorkortet**. |
   | Overskriftstype | Angiver kilden til poster i betalingspraksis, og du kan vælge Kreditorer, Debitorer eller begge dele. |
   | Startdato | Angiver startdatoen for betalingspraksis. |
   | Afslutningsdato | Angiver slutdato for betalingspraksis. |

> [!NOTE]
> Hvis du beslutter dig for at bruge indstillingen **Firmastørrelse**, skal du først oprette poster på siden **Firmastørrelser** og føje dem til alle kreditorer, du vil spore ved hjælp af denne metode.

4. Når du én gang udfylder alle felter i hovedet, skal du køre handlingen **Generer** for at generere data i linjerne og statistikkerne for den valgte type rapportering.
5. Baseret på **Agregationstypen** får du forskellige linjer. Du kan ændre nogle af værdierne manuelt, men i så fald markeres hver af de ændrede linjer og hele rapporten som **Ændret manuelt**.
6. Fra alle beregnede felter kan du gå dybere for at se, hvordan dette resultat er blevet beregnet, ved at åbne siden **Dataliste over betalingspraksis**.
7. Hvis du vil udskrive dokumentet, kan du gøre det ved at køre handlingen **Udskriv**.

## Se også

[Finansrapporter](finance-reports.md)  
[Analysere regnskaber i Microsoft Excel](finance-analyze-excel.md)  
[Rapporter og analyser for debitor](receivables-reports.md)  
[Rapporter og analyser for skyldige beløb](payables-reports.md)  
[Konfigurere Finans](finance-setup-finance.md)  
[Finans](finance.md)  
[Oversigt over lokal funktionalitet](about-localization.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
