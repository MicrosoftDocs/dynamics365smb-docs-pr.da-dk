---
title: "Svare på anmodninger om personlige oplysninger"
description: Du skal besvare anmodninger fra dataemner.
author: bholtorf
ms.author: bholtorf
ms.custom: na
ms.date: 03/13/2018
ms.reviewer: na
ms.suite: na
ms.tgt_pltfrm: na
ms.topic: article
ms.translationtype: HT
ms.sourcegitcommit: d7fb34e1c9428a64c71ff47be8bcff174649c00d
ms.openlocfilehash: 89f53f24f74401ce384b54d04fbeb473aedad96d
ms.contentlocale: da-dk
ms.lasthandoff: 03/22/2018

---

# <a name="responding-to-requests-about-personal-data"></a>Svare på anmodninger om personlige oplysninger  
Dataemner kan anmode om flere typer handlinger vedrørende deres personlige oplysninger. Hvis du har klassificeret følsomheden i dine data og er sikker på, at de er korrekte, kan en administrator svare på anmodninger ved hjælp af regnearket Klassificering af data i rollecenteret **Administrer brugere, brugergrupper og tilladelser** eller, hvis du bruger Windows-klienten, i rollecenteret **It-chef**. Du kan finde flere oplysninger om at klassificere data og klassificere datafølsomheden i [Klassificering af data](/dynamics-nav/classifying-data) og [Klassificere datafølsomhed](admin-classifying-data-sensitivity.md).

Nedenstående tabel indeholder eksempler på typerne af anmodninger, som du kan reagere på.

> [!Note]
> Selv om vi leverer funktioner til besvarelse af disse typer af anmodning og dermed åbner personlige data, er det dit ansvar at sikre, at personlige og følsomme data er placeret og klassificeret korrekt.

|Anmodningstype|Beskrivelse og foreslåede svar|
|-----|-----|
|Anmodninger om overførsel|Et dataemne kan foretage en anmodning om dataoverførsel, hvilket vil sige, at du skal eksportere dataemnets personlige oplysninger fra dine systemer og levere dem i et struktureret, normalt anvendt format. Til at besvare disse anmodninger, skal du bruge værktøjet til databeskyttelse til at eksportere personlige data til en Excel-fil. Ved hjælp af Excel kan du redigere personlige oplysninger og gemme den i et almindeligt anvendt, maskinlæsbart format, f.eks. .csv- eller .xml. Administratorer kan også eksportere data ved hjælp af Rapid Start-konfigurationspakker og derefter konfigurere masterdatatabeller og deres relaterede tabeller, der indeholder personlige oplysninger. |
|Anmodninger om sletning|Et dataemne kan anmode om, at du sletter deres personlige oplysninger. Der er flere måder at slette personlige oplysninger på ved hjælp af tilpasningsmulighederne, men beslutningen og implementeringen er dit ansvar. I nogle tilfælde kan vælge du at redigere dataene direkte, f.eks. ved at slette en kontakt og derefter udføre kørslen Slet annulleret interaktion for at slette interaktioner for kontakten. <br><br> **Bemærk:** Hvis du har angivet en dato i feltet **Tillad sletning af dokument før** på siderne **Opsætning af salg og tilgodehavender** eller **Købsopsætning**, skal du måske ændre datoen, så kan du slette bogførte salgs- og købsdokumenter, der er udskrevet, og hvor bogføringsdatoen er på eller inden denne dato.|
|Anmodninger om rettelse|Et dataemne kan anmode om, at du retter forkerte personlige oplysninger. Dette kan gøres på flere måder. I nogle tilfælde kan du eksportere lister til Excel til hurtig masseredigering af flere poster og derefter importere de opdaterede data. Du kan finde flere oplysninger under [Eksportere forretningsdata til Excel](https://docs.microsoft.com/en-us/dynamics-nav-app/about-export-data). Du kan også manuelt redigere felter, der indeholder personlige oplysninger, f.eks. redigere oplysninger om en debitor på debitorkortet. Men transaktionsposter, f.eks. finans-, debitor- og momsposter, er nødvendige for integriteten i ERP-systemet. Hvis du gemmer personlige data i forretningstransaktionsposter, kan du overveje at bruge funktionerne til tilpasning til at ændre disse personlige oplysninger.|

## <a name="restrict-data-processing-for-a-data-subject"></a>Begrænse databehandling af et dataemne
Et dataemne kan anmode om, at du midlertidigt stopper behandlingen af deres personlige oplysninger. Du kan imødekomme sådanne anmodninger ved at markere posten som spærret på grund af beskyttelse af personlige oplysninger, så behandlingen af deres data stoppes. Når en post er markeret som spærret, kan du ikke oprette nye posteringer, der bruger denne post. Du kan f.eks. ikke du oprette en ny faktura for en debitor, når enten kunden eller sælgeren er blokeret. Åbn kortet for et dataemne, f.eks. kortene Debitor, Leverandør eller Kontakt, hvis du vil markere et dataemne som spærret, og markér afkrydsningsfeltet **Beskyttelse af personlige oplysninger spærret**. Du skal måske vælge **Vis mere** for at få vist feltet.

## <a name="handling-data-about-minors"></a>Håndtering af data om mindreårige
Hvis en kontakts alder er under myndighedsalderen i henhold til lovgivningen i dit område, kan du angive dette, ved at markere afkrydsningsfeltet **Mindreårig** på kortet **Kontakt**. Når du gør dette, markeres afkrydsningsfeltet **Beskyttelse af personlige oplysninger spærret** automatisk. Når du modtager samtykke fra den mindreåriges forældre eller værge, kan du markere afkrydsningsfeltet **Forældresamtykke modtaget** for at fjerne spærringen af kontakten. Selvom du kan behandle personlige oplysninger for mindreårige, kan du ikke bruge profileringsfunktionen i Microsoft Dynamics 365 for Sales.

> [!Note]
> Ændringsloggen kan f.eks. registrere oplysninger om, hvornår og af hvem afkrydsningsfeltet **Forældresamtykke modtaget** blevet markeret. En administrator kan oprette dette ved hjælp af guiden **Opsætning af ændringslog** guide og også markere afkrydsningsfeltet **Logfør ændring af Forældresamtykke modtaget** på kortet **Kontakt**. Du kan finde flere oplysninger i [Logføre ændringer](/dynamics-nav-app/across-log-changes).  

## <a name="see-also"></a>Se også
[Klassificering af Data](https://docs.microsoft.com/en-us/dynamics-nav/classifying-data)  
[Klassificere datafølsomhed](admin-classifying-data-sensitivity.md)  
[Eksportere forretningsdata til Excel](https://docs.microsoft.com/en-us/dynamics-nav-app/about-export-data)  

