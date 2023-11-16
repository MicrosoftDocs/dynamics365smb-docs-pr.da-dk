---
title: Gennemgang af servicekontrakter for servicevarer
description: 'I denne artikel gennemgås forskellige scenarier, der involverer serviceartikler og kontrakter.'
author: andreipanko
ms.author: andreipa
ms.topic: how-to
ms.date: 05/31/2023
ms.custom: bap-template
---

# Gennemgang af servicekontrakter for servicevarer

Denne gennemgang viser flere centrale processer:

- Oprette serviceartikler via salg
- Oprette og fakturere en servicekontrakt
- Oprette serviceordrer for en servicekontrakt
- Tildele en ressource baseret på færdigheder og zone
- Udfyld tidsregistreringen for serviceordren
- Bogføre og fakturere kontraktserviceordre

## Oprette serviceartikler

### Scenarie  

Susan, der er ordrebehandler, bogfører en salgsordre, der sælger en vare, der er konfigureret til at generere en serviceartikel.  

### Trin

1. Kontroller, at **Serviceartikelgruppe** er valgt for **varen**.
   
    1. Vælg ![Lightbulb, der åbner funktionen Fortæl mig.](../../media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **Varer**, og vælg derefter det relaterede link.  
    2. Vælg varen *S-100*, og åbn den.
    3. Kontroller værdien i feltet **Serviceartikelgruppe**.
       
2. Bogfør **salgsordren** for at oprette serviceartiklen til kunden.  

    1. Vælg ![Lightbulb, der åbner funktionen Fortæl mig.](../../media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **Salgsordrer**, og vælg derefter det relaterede link.  
    2. Vælg ordren til kundenr. 10000. Eksternt Ordrenr. er *SVC-1*.
    3. Vælg handlingen **Bogfør** for at levere varen til kunden.

### Resultater

- Der oprettes en servicevare til Kunde 10000

##  Fakturere en servicekontrakt

### Scenarie

Charles, servicechefen, opretter derefter en servicekontrakt for at fakturere for regelmæssige vedligeholdelsesbesøg.

3. Opret **servicekontrakten** for den nye serviceartikel
    1. Vælg ![Lightbulb, der åbner funktionen Fortæl mig.](../../media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **Servicekontrakter**, og vælg derefter det relaterede link.
    2. Vælg handlingen **Ny**.  
    3. I bekræftelsesdialogboksen skal du vælge **Ja** for at oprette kontrakt ved hjælp af skabelon. 
    4. Vælg *Ikke-forudbetalt Kontrakt - månedligt*.
    5. Skriv **VEDLIGEH.** i oversigtspanelet Service i **serviceordretypen**.
    6. Angiv følgende oplysninger på linjerne:

    |Serviceartikelnr.|Linjeværdi|  
    |----------------|----------|  
    |SV000001|6000|

    7. Hvis du vil underskrive kontrakten, skal du vælge handlingen **Underskriv kontrakt**.
    8. Vælg **Ja** for at bekræfte oprettelsen af en servicefaktura. Du modtager en bekræftelsesmeddelelse med servicefakturanummer.

3. Bogfør servicefakturaen
   1. Vælg ikonet ![Lightbulb, der åbner funktionen Fortæl mig.](../../media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **Servicefakturaer**, og vælg derefter det relaterede link.
   2. Find servicefakturaen, og vælg handlingen **Bogfør**.

### Resultater

- Der oprettes en underskrevet servicekontrakt med finansposter
- Der oprettes en bogført servicefaktura

## Oprette serviceordrer for en servicekontrakt og tildel ressourcer

### Scenarie  

Charles, servicechefen, opretter serviceordrerne for almindelige vedligeholdelsesordrer i henhold til servicekontrakten og gennemser derefter ordreoversigten for at tildele dem.

### Trin

1. Kør de serviceordrer, der skal opfylde forpligtelserne i de aktive servicekontrakter.
   1. Vælg ikonet ![Lightbulb, der åbner funktionen Fortæl mig.](../../media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **Opret kontraktserviceordrer**, og vælg derefter det relaterede link.
   2. Angiv månedens start- og slutdato i felterne Startdato og Slutdato i oversigtspanelet Indstillinger
   3. Vælg **Ja** for at bekræfte oprettelsen af en serviceordre. Du modtager en bekræftelsesmeddelelse med antallet af oprettede serviceordrer.

2. Gennemse de ordrer, der afventer tildeling, via ordreoversigten
   1. Vælg ikonet ![Lightbulb, der åbner funktionen Fortæl mig.](../../media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **Ordreoversigt**, og vælg derefter det relaterede link.
   2. Ordreoversigten viser alle åbne serviceordrer sammen med **antallet af allokeringer** for at vise, om serviceordrerne er tildelt til en ressource.
   3. Vælge handlingen **Vis bilag** for at åbne en serviceordre.  Du kan se, at faktaboksen Serviceartikellinjer viser, hvilke ressourcer der er dygtige til at arbejde med denne artikel.

3. Sådan tildeles en ressource til serviceordren
   1. Fra serviceordren, vælges linjehandlingen **Ressourceallokeringer**
   2. Indtast følgende oplysninger vedrørende ressourceallokering

    |Serviceartikelnr.|Ressourcenr.|Allokeringsdato|Allokerede timer|
    |----------------|------------|---------------|---------------|  
    |SV000001|RESOURCE1|d|1|

    3. Allokeringen ændres til en Status til Aktiv.
    4. Når du opdaterer Ordreoversigt, vises **antallet af allokeringer** ændret fra 0 til 1 for serviceordren.

### Resultater

- Der oprettes serviceordrer for servicekontrakterne
- Serviceordrerne allokeres til en ressource, så arbejdet kan færdiggøres

## Udfyld tidsregistreringen for serviceordren, og bogfør serviceordren

### Scenarie  

Serviceteknikeren registrerer sin tid direkte i forhold til serviceordren og markerer derefter ordren som færdig.

> [!NOTE]
> Tidsregistrering for serviceordrer kan angives via timesedler. For mere information, se [link til timeseddel, hvis denne note giver mening].

### Trin

1. Find serviceordren, og indtast tiden på servicelinjen
   1. Vælg ikonet ![Lightbulb, der åbner funktionen Fortæl mig.](../../media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, angiv **Serviceordre** og vælg derefter det relaterede link.
   2. Find den serviceordre, du vil angive tid for.
   3. Vælg linjehandlingen **Servicelinje**.
   4. Angiv følgende oplysninger

    |Enhedstype|Nr.|Antal|Antal til forbrug|
    |----|---|--------|--------|   
    |Ressource|RESOURCE1|2|2|

2. Bogfør forbrug på serviceordren
   1. Vælg handlingen **Bogfør**, udfyld serviceordren og vælg **Send og forbrug**, og vælg derefter knappen **OK**.

### Resultater

- Der oprettes serviceposter knyttet til serviceartiklen, servicekontrakten og ressourcen

## Se også
