---
title: Svare på anmodninger om brugerens personlige oplysninger
description: 'Denne artikel viser, hvordan du kan svare på anmodninger om personoplysninger.'
author: brentholtorf
ms.author: bholtorf
ms.reviewer: ivkoleti
ms.topic: conceptual
ms.date: 04/25/2023
ms.custom: bap-template
---

# Svare på anmodninger om brugerens personlige oplysninger

Dataemner kan anmode om flere typer handlinger vedrørende deres personlige oplysninger. I henhold til lovgivning og regler vedrørende databeskyttelse har de ret til at anmode om eksport, sletning og ændring af deres personlige data. Disse anmodninger kaldes *Dataemneanmodninger*. Hvis du har klassificeret følsomheden af dine data og er sikker på, at de er korrekte, kan en administrator reagere på anmodninger ved hjælp af indstillingerne under fanen **Beskyttelse af personlige oplysninger** i rollecenteret **It-chef**. 
<!--
For more information about classifying data and data sensitivity in [!INCLUDE[prod_long](includes/prod_long.md)], go to the following articles:

* [Classifying Data](/dynamics-nav/classifying-data?toc=/dynamics365/business-central/toc.json) 
* [Classifying Data Sensitivity](admin-classifying-data-sensitivity.md)  -->

## Typer af anmodninger

Nedenstående tabel indeholder eksempler på typerne af anmodninger, som administratorer kan reagere på.

> [!Note]
> Selv om vi leverer funktioner til besvarelse af disse typer af anmodning og dermed åbner personlige data, er det dit ansvar at sikre, at personlige og følsomme data er placeret og klassificeret korrekt.

|Anmodningstype|Beskrivelse og foreslåede svar|
|-----|-----|
|Anmodninger om overførsel|Et dataemne kan være en anmodning om datatransport. Du skal eksportere dataemnets personoplysninger fra dine systemer og give dem et struktureret, almindeligt anvendt format. Du kan besvare disse anmodninger ved at bruge **Værktøj til beskyttelse af personlige oplysninger** til at eksportere personlige data til en Excel-fil eller en RapidStart-konfigurationspakke. Ved hjælp af Excel kan du redigere personlige oplysninger og gemme den i et almindeligt anvendt, maskinlæsbart format, f.eks. .csv- eller .xml. Med RapidStart-konfigurationspakker kan du konfigurere masterdatatabeller og deres relaterede tabeller, der indeholder personlige oplysninger. <br><br> **Bemærk:** Når du eksporterer data, angiver du et mindste følsomhedsniveau. Eksporten omfatter minimum og alle niveauer af følsomhed derover. Hvis du f.eks. vil eksportere data, der er klassificeret som personlige, omfatter eksporten også data, der er klassificeret som følsomme. <br><br>Ved eksport af data, der vedrører et dataemne søger **Værktøj til beskyttelse af personlige oplysninger** efter direkte relationer mellem dataemnet og data, der er relateret til emnet. Indirekte relationer mellem data, der er relateret til dataemnet og andre data, eksporteres ikke automatisk af **Værktøj til beskyttelse af personlige oplysninger**. Tabellen Kontakt f.eks. har direkte relaterede data for Svar på kontaktprofil, og tabellen Svar på kontaktprofil er igen relateret til profilspørgsmålsdata. Hvis du også vil eksportere profilspørgsmål, skal du tilføje denne tabel manuelt som en række med de relevante filtre i den konfigurationspakke, som **Værktøj til beskyttelse af personlige oplysninger** opretter.|
|Anmodninger om sletning|Et dataemne kan anmode om, at du sletter deres personlige oplysninger. Der er flere måder at slette personlige oplysninger på ved hjælp af tilpasningsmulighederne, men beslutningen og implementeringen er dit ansvar. I nogle tilfælde kan du vælge at redigere dataene direkte. F.eks. hvis du sletter en kontakt og derefter udfører kørslen Slet annulleret interaktion, slettes interaktioner for kontakten. <br><br> **Bemærk:** Hvis du har angivet en dato i feltet **Tillad sletning af dokument før** på siderne **Opsætning af salg og tilgodehavender** eller **Købsopsætning**, skal du måske ændre datoen, så kan du slette bogførte salgs- og købsdokumenter, der har bogføringsdatoen på eller inden denne dato.|
|Anmodninger om rettelse|Et dataemne kan anmode om, at du retter forkerte personlige oplysninger. Dette kan gøres på flere måder. I nogle tilfælde kan du eksportere lister til Excel til hurtig masseredigering af flere poster og derefter importere de opdaterede data. Du kan finde flere oplysninger i [Eksportere forretningsdata til Excel](about-export-data.md). Du kan også manuelt redigere felter, der indeholder personlige oplysninger, f.eks. redigere oplysninger om en debitor på debitorkortet. Men poster som f.eks. generelle finans-, debitor- og momsposter er vigtige. Hvis du gemmer personlige data i forretningstransaktionsposter, kan du overveje at bruge funktionerne til tilpasning til at ændre disse personlige oplysninger.|

## Begrænse databehandling for et dataemne

Et dataemne kan anmode om, at du midlertidigt stopper behandlingen af deres personlige oplysninger. Du kan imødekomme sådanne anmodninger ved at markere posten som spærret på grund af beskyttelse af personlige oplysninger, så behandlingen af deres data stoppes. Når en post er markeret som spærret, kan du ikke oprette nye posteringer, der bruger denne post. Du kan f.eks. ikke du oprette en ny faktura for en debitor, når enten kunden eller sælgeren er blokeret. Åbn kortet for et dataemne, f.eks. kortene Debitor, Leverandør eller Kontakt, hvis du vil markere et dataemne som spærret, og markér afkrydsningsfeltet **Beskyttelse af personlige oplysninger spærret**. Du skal måske vælge **Vis mere** for at få vist feltet.  

## Håndtering af dataemneanmodninger i prøveversion

Visse typer personoplysninger er en del af en Microsoft 365-konto, og det er kun administratorer, der kan eksportere dataene. Processen til håndtering af dataemneanmodninger er forskellige afhængigt af [!INCLUDE[prod_short](includes/prod_short.md)]-lejertypen.

Hvis du har et betalt abonnement på [!INCLUDE[prod_short](includes/prod_short.md)], skal brugere kontakte deres organisations lejeradministrator for at sende en dataemneanmodning. Administratorer har administratorrettigheder og -værktøjer til at imødekomme anmodninger om dataemner.

Hvis du har tilmeldt dig [!INCLUDE[prod_short](includes/prod_short.md)] fra siden [Prøve](https://trials.dynamics.com/), og du stadig bruger prøveversionen, kan brugere hente og eksportere deres egne data i på [siden om beskyttelse af arbejde og skole i Azure-portalen](https://portal.azure.com#blade/Microsoft_AAD_IAM/GDPRViralBlade).

Du kan også lukke din konto på denne side. Det anbefales dog, at du først eksporterer og sletter alle data. Hvis du sletter kontoen, betyder det, at du har mistet adgangen til [!INCLUDE[prod_short](includes/prod_short.md)].

Du kan stadig markere personer som spærret af hensyn til beskyttelse af personlige oplysninger og eksportere, redigere eller slette transaktioner, som beskrevet andetsteds i denne artikel.  

## Eksportere data fra tabeller, der ikke er klassificeret af dataemnet

Hvis du skal eksportere data, der ikke er klassificeret på en sådan måde, så de bliver eksporteret automatisk, f.eks. data fra tabellen Profilsvar, skal du gøre følgende:

* Overvej, om du skal eksportere supplerende data, der ikke er direkte relateret til kontakten.
* Føj tabellen og relationen til manuelt start pakken, og eksporter den direkte fra den hurtige startpakke. Vi opretter en hurtig startpakke til dig, så du kan ændre den i sådanne situationer.

## Håndtering af data om mindreårige

Hvis en kontakts alder er under myndighedsalderen i henhold til lovgivningen i dit område, kan du angive dette, ved at markere afkrydsningsfeltet **Mindreårig** på kortet **Kontakt**. Når du gør dette, markeres afkrydsningsfeltet **Beskyttelse af personlige oplysninger spærret** automatisk. Når du modtager samtykke fra den mindreåriges forældre eller værge, kan du markere afkrydsningsfeltet **Forældresamtykke modtaget** for at fjerne spærringen af kontakten. Selvom du kan behandle personlige oplysninger for mindreårige, kan du ikke bruge profileringsfunktionen i Dynamics 365 Sales.

> [!Note]
> Ændringsloggen kan f.eks. registrere oplysninger om, hvornår og af hvem afkrydsningsfeltet **Forældresamtykke modtaget** blevet markeret. En administrator kan oprette dette ved hjælp af guiden **Opsætning af ændringslog** guide og også markere afkrydsningsfeltet **Logfør ændring af Forældresamtykke modtaget** på kortet **Kontakt**. Du kan finde flere oplysninger i [Logføre ændringer](across-log-changes.md).  

### Se også

<!-- [Classifying Data](/dynamics-nav/classifying-data?toc=/dynamics365/business-central/toc.json)  
[Classifying Data Sensitivity](admin-classifying-data-sensitivity.md)  -->
[Eksportere forretningsdata til Excel](about-export-data.md)  
[Logføre ændringer](across-log-changes.md)  
[Anmodninger vedrørende dataemner](/microsoft-365/compliance/gdpr-data-subject-requests)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
