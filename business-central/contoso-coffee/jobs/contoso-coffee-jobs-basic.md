---
title: Gennemgang af grundlæggende job
description: Denne artikel guider dig gennem flere kerneprocesser inden for projektledelse.
author: andreipanko
ms.author: andreipa
ms.topic: how-to
ms.date: 05/31/2023
ms.custom: bap-template
ms.service: dynamics-365-business-central
---
# Gennemgang af grundlæggende job

Denne gennemgang viser flere centrale processer:

- Føje sagsopgaver til sager
- Registrere tids- og materialeudgifter for en sag
- Fakturering af en sag

## Føje en sagsopgave til en sag

### Scenarie  

Simon, projektlederen, ønsker at registrere den tid, der bruges på at uddanne kunden i brugen af espressomaskineprodukter til en separat opgave i jobbet med at installere en kommerciel maskine på stedet.

### Trin

1. Oprette sagsopgaven  

    1. Vælg ![Lightbulb, der åbner funktionen Fortæl mig.](../../media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **Sager**, og vælg derefter det relaterede link.  
    2. Vælg jobbet *J00010*.
    3. I området **Tasks** vælges handlingen **Ny linje**.  Angiv følgende værdier:
 
    |Sagsopgavenr.|Beskrivelse|Sagsopgavetype|
    |------------|-----------|-------------|  
    |220|Kundetræning|Bogfører|

2. Indrykker sagsopgaverne
   1. I området Opgaver skal du finde handlingen **Indryk sagsopgaver**
   2. Bekræft, at du vil indrykke opgaver ved at vælge **Ja**.

### Resultater

 - Nu kan tid og udgifter registreres til den nye sagsopgave

## Registrer tids- og materialeudgifter for en sag

### Scenarie  

Edgin, den tekniker, der installerer maskinen, skal registrere sin tid og de materialer, der bruges under installationen, til jobbet til fakturering.  Han har allerede tilføjet rejser og materialer, og nu skal han tilføje tid til lærerpersonalet, hvordan man bruger maskinen.

### Trin

1. Opret yderligere sagskladdelinjer

    1. Vælg ![Lightbulb, der åbner funktionen Fortæl mig.](../../media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **Sagskladder**, og vælg derefter det relaterede link.  
    2. Vælg batchen *CONTOSO.*  Du får vist flere linjer med ressource- og varetyper, der afspejler den anvendte tid (for teknikeren og køretøjet) og materialerne (maskinen og forsyningerne).
    3. Opret en ny linje. Angiv følgende værdier:
 
    |Sagsnr.|Sagsopgavenr.|Enhedstype|Nr.|Beskrivelse|Antal|
    |-------|------------|----|---|-----------|--------|  
    |J00010|220|Ressource|EDGIN|Kundetræning|1|

2. Bogføre tid og udgift
   1. Vælg handlingen **Bogfør**
   2. Bekræft, at du vil indrykke linjerne ved at vælge **Ja**.

### Resultater

 - Der oprettes sagsposter og ressourceposter af typen *Forbrug* 
 - Der oprettes vareposter for at justere lagerbeholdningen negativt
 - På jobkortet afspejler omkostnings- og prisområdet i området Opgaver de nye saldi, der venter på at blive faktureret
 - Faktaboksen Sagsoplysninger på jobkortet afspejler de samlede priser

## Oprettelse af en salgsfaktura for en sag

### Scenarie  
Simon skal oprette og bogføre en faktura, der skal sendes til kunden med hensyn til tid og udgifter fra sagen.

### Trin
1. Opret salgsfaktura

    1. Vælg ![Lightbulb, der åbner funktionen Fortæl mig.](../../media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **Sager**, og vælg derefter det relaterede link.  
    2. Vælg handlingen **Opret sagssalgsfaktura** på listen over sager.
    3. Angiv **sagsnummer**-filter til *J00010*.
    4. Vælg **OK** for at oprette salgsfaktura.  Du modtager en bekræftelse på, hvor mange fakturaer der genereres

2. Bogføre tid og udgift
   1. Vælg ikonet ![Lightbulb, der åbner funktionen Fortæl mig.](../../media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **Salgsfakturaer**, og vælg derefter det relaterede link.  
   2. Vælg den sidste faktura for at åbne den til gennemsyn.
   3. Vælg handlingen **Bogfør**.

### Resultater

 - Der oprettes sagsposter og ressourceposter af typen *Salg*
 - På jobkortet afspejler omkostnings- og prisområdet i området Opgaver de nye fakturasaldi
 - Faktaboksen Sagsoplysninger på jobkortet afspejler de samlede priser i området med faktureret pris
