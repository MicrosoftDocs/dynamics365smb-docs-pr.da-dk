---
title: Gennemgang af grundlæggende job
description: Denne artikel guider dig gennem flere kerneprocesser inden for projektledelse.
author: andreipanko
ms.author: andreipa
ms.topic: how-to
ms.date: 05/31/2023
ms.custom: bap-template
ms.service: dynamics-365-business-central
ms.reviewer: bholtorf
---
# Gennemgang af grundlæggende job

Denne gennemgang viser flere centrale processer:

- Føje projektopgaver til projekter
- Registrer tids- og materialeudgifter for et projekt
- Fakturere et projekt

## Tilføje en projektopgave

### Scenarie  

Simon, projektlederen, vil gerne bruge rekordtid på at lære kunden, hvordan man bruger espressomaskineproduktet. Simon ønsker at bruge en separat opgave i jobbet til installation af en kommerciel maskine på stedet.

### Trin

1. Oprette projektopgaven.

    1. Vælg ![Lightbulb, der åbner funktionen Fortæl mig.](../../media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **Projekter**, og vælg derefter det relaterede link.  
    2. Vælg jobbet *J00010*.
    3. I handlingen **Opgaver** skal du vælge handlingen **Ny linje** og derefter angive følgende værdier:
 
    |Projektopgavenr.|Beskrivelse|Projektopgavetype|
    |------------|-----------|-------------|  
    |220|Kundetræning|Bogfører|

2. Indryk projektopgaverne.
   1. I området Opgaver skal du finde handlingen **Indryk projektopgaver**.
   2. Bekræft, at du vil indrykke opgaver ved at vælge **Ja**.

### Resultater

 - Nu kan tid og udgifter registreres til den nye projektopgave

## Registrer tids- og materialeudgifter for et projekt

### Scenarie  

Edgin, den tekniker, der installerer maskinen, skal registrere sin tid og de materialer, der bruges under installationen, til jobbet til fakturering. Edgin har allerede tilføjet rejser og materialer, og nu skal han tilføje tid til lærerpersonalet, hvordan man bruger maskinen.

### Trin

1. Opret ekstra projektkladdelinjer.

    1. Vælg ![Lightbulb, der åbner funktionen Fortæl mig.](../../media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") , skriv **Projektkladder**, og vælg derefter det relaterede link.  
    2. Vælg batchen *CONTOSO.* Du får vist flere linjer med ressource- og varetyper, der afspejler den anvendte tid (for teknikeren og køretøjet) og materialerne (maskinen og forsyningerne).
    3. Opret en ny linje, og angiv derefter følgende værdier:
 
    |Projektnr.|Projektopgavenr.|Enhedstype|Nr.|Beskrivelse|Antal|
    |-------|------------|----|---|-----------|--------|  
    |J00010|220|Ressource|EDGIN|Kundetræning|1|

2. Bogføre tid og udgift.
   1. Vælg handlingen **Bogfør**.
   2. Bekræft, at du vil indrykke linjerne ved at vælge **Ja**.

### Resultater

- Der oprettes projektposter og ressourceposter af typen *Forbrug*.
- Der oprettes vareposter for at justere lagerbeholdningen negativt.
- På projektkortet afspejler omkostnings- og prisområdet i området Opgaver de nye saldi, der venter på at blive faktureret.
- På projektkortet afspejler projektoplysninger-faktaboksen de samlede priser.

## Oprettelse af en salgsfaktura for et projekt

### Scenarie  

Simon skal oprette og bogføre en faktura, der skal sendes til kunden med hensyn til tid og udgifter fra projektet.

### Trin

1. Opret salgsfakturaen.

    1. Vælg ![Lightbulb, der åbner funktionen Fortæl mig.](../../media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **Projekter**, og vælg derefter det relaterede link.  
    2. Vælg handlingen **Opret projektsalgsfaktura** på listen over sager.
    3. Angiv **projektnummeret** filtrer til *J00010*.
    4. Vælg **OK** for at oprette salgsfakturaen. Du modtager en bekræftelse på, hvor mange fakturaer der genereres.

2. Bogføre tid og udgift.

   1. Vælg ikonet ![Lightbulb, der åbner funktionen Fortæl mig.](../../media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **Salgsfakturaer**, og vælg derefter det relaterede link.  
   2. Vælg den sidste faktura for at åbne den til gennemsyn.
   3. Vælg handlingen **Bogfør**.

### Resultater

- Der oprettes projektposter og ressourceposter af typen *Salg*.
- På projektkortet afspejler omkostnings- og prisområdet i området Opgaver de nye fakturerede saldi.
- På projektkortet afspejles projektoplysningerne de samlede priser i området med faktureret pris.
