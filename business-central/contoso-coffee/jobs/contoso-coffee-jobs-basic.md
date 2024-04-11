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
# <a name="walkthrough-of-basic-jobs"></a>Gennemgang af grundlæggende job

Denne gennemgang viser flere centrale processer:

- Føje projektopgaver til projekter
- Registrer tids- og materialeudgifter for et projekt
- Fakturere et projekt

## <a name="adding-a-project-task"></a>Tilføje en projektopgave

### <a name="scenario"></a>Scenarie

Simon, projektlederen, vil gerne bruge rekordtid på at lære kunden, hvordan man bruger espressomaskineproduktet. Simon ønsker at bruge en separat opgave i jobbet til installation af en kommerciel maskine på stedet.

### <a name="steps"></a>Trin

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

### <a name="results"></a>Resultater

 - Nu kan tid og udgifter registreres til den nye projektopgave

## <a name="record-time-and-material-expenses-to-a-project"></a>Registrer tids- og materialeudgifter for et projekt

### <a name="scenario-1"></a>Scenarie

Edgin, den tekniker, der installerer maskinen, skal registrere sin tid og de materialer, der bruges under installationen, til jobbet til fakturering. Edgin har allerede tilføjet rejser og materialer, og nu skal han tilføje tid til lærerpersonalet, hvordan man bruger maskinen.

### <a name="steps-1"></a>Trin

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

### <a name="results-1"></a>Resultater

- Der oprettes projektposter og ressourceposter af typen *Forbrug*.
- Der oprettes vareposter for at justere lagerbeholdningen negativt.
- På projektkortet afspejler omkostnings- og prisområdet i området Opgaver de nye saldi, der venter på at blive faktureret.
- På projektkortet afspejler projektoplysninger-faktaboksen de samlede priser.

## <a name="creating-a-sales-invoice-for-a-project"></a>Oprettelse af en salgsfaktura for et projekt

### <a name="scenario-2"></a>Scenarie

Simon skal oprette og bogføre en faktura, der skal sendes til kunden med hensyn til tid og udgifter fra projektet.

### <a name="steps-2"></a>Trin

1. Opret salgsfakturaen.

    1. Vælg ![Lightbulb, der åbner funktionen Fortæl mig.](../../media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **Projekter**, og vælg derefter det relaterede link.  
    2. Vælg handlingen **Opret projektsalgsfaktura** på listen over sager.
    3. Angiv **projektnummeret** filtrer til *J00010*.
    4. Vælg **OK** for at oprette salgsfakturaen. Du modtager en bekræftelse på, hvor mange fakturaer der genereres.

2. Bogføre tid og udgift.

   1. Vælg ikonet ![Lightbulb, der åbner funktionen Fortæl mig.](../../media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **Salgsfakturaer**, og vælg derefter det relaterede link.  
   2. Vælg den sidste faktura for at åbne den til gennemsyn.
   3. Vælg handlingen **Bogfør**.

### <a name="results-2"></a>Resultater

- Der oprettes projektposter og ressourceposter af typen *Salg*.
- På projektkortet afspejler omkostnings- og prisområdet i området Opgaver de nye fakturerede saldi.
- På projektkortet afspejles projektoplysningerne de samlede priser i området med faktureret pris.
