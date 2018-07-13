---
title: "Svare på anmodninger om personlige oplysninger"
description: Du skal besvare anmodninger fra dataemner.
author: bholtorf
ms.service: dynamics365-business-central
ms.author: bholtorf
ms.custom: na
ms.date: 05/25/2018
ms.reviewer: na
ms.suite: na
ms.tgt_pltfrm: na
ms.topic: article
ms.translationtype: HT
ms.sourcegitcommit: 2286b728a464943841b192031cfea13644441013
ms.openlocfilehash: b90577cbab4167894fe79a3e8e8a0c61ce8c70e9
ms.contentlocale: da-dk
ms.lasthandoff: 06/28/2018

---

# <a name="responding-to-requests-about-personal-data"></a>Svare på anmodninger om personlige oplysninger  
Dataemner kan anmode om flere typer handlinger vedrørende deres personlige oplysninger. I henhold til den generelle forordning om databeskyttelse (GDPR) f.eks. har indbyggere i EU-lande ret til at anmode om eksport, sletning og ændring af deres personlige data. Dette kaldes en *Dataemneanmodning*. Hvis du har klassificeret følsomheden i dine data og er sikker på, at de er korrekte, kan en administrator svare på anmodninger ved hjælp af indstillingerne under **Beskyttelse af personlige oplysninger** i rollecenteret **Administrer brugere, brugergrupper og tilladelser** eller, hvis du bruger Windows-klienten, i rollecenteret **It-chef**. Du kan finde flere oplysninger om at klassificere data og klassificere datafølsomheden i [!INCLUDE[d365fin_long](includes/d365fin_long_md.md)] under [Klassificering af data](/dynamics-nav/classifying-data?toc=/dynamics365/business-central/toc.json) og [Klassificere datafølsomhed](admin-classifying-data-sensitivity.md).  

## <a name="types-of-requests"></a>Typer af anmodninger

Nedenstående tabel indeholder eksempler på typerne af anmodninger, som du kan reagere på.

> [!Note]
> Selv om vi leverer funktioner til besvarelse af disse typer af anmodning og dermed åbner personlige data, er det dit ansvar at sikre, at personlige og følsomme data er placeret og klassificeret korrekt.

|Anmodningstype|Beskrivelse og foreslåede svar|
|-----|-----|
|Anmodninger om overførsel|Et dataemne kan foretage en anmodning om dataoverførsel, hvilket vil sige, at du skal eksportere dataemnets personlige oplysninger fra dine systemer og levere dem i et struktureret, normalt anvendt format. Du kan besvare disse anmodninger ved at bruge **værktøjet til databeskyttelse** til at eksportere personlige data til en Excel-fil eller en RapidStart-konfigurationspakke. Ved hjælp af Excel kan du redigere personlige oplysninger og gemme den i et almindeligt anvendt, maskinlæsbart format, f.eks. .csv- eller .xml. Med RapidStart-konfigurationspakker kan du konfigurere masterdatatabeller og deres relaterede tabeller, der indeholder personlige oplysninger. <br><br> **Bemærk:** Når du eksporterer data, angiver du et mindste følsomhedsniveau. Eksporten omfatter minimum og alle niveauer af følsomhed derover. Hvis du f.eks. vil eksportere data, der er klassificeret som personlige, omfatter eksporten også data, der er klassificeret som følsomme. <br><br>Ved eksport af data, der vedrører et dataemne søger **Værktøj til beskyttelse af personlige oplysninger** efter direkte relationer mellem dataemnet og data, der er relateret til emnet. Indirekte relationer mellem data, der er relateret til dataemnet og andre data, eksporteres ikke automatisk af **Værktøj til beskyttelse af personlige oplysninger**. Tabellen Kontakt f.eks. har direkte relaterede data for Svar på kontaktprofil, og tabellen Svar på kontaktprofil er igen relateret til profilspørgsmålsdata. Hvis du også vil eksportere profilspørgsmål, skal du tilføje denne tabel manuelt som en række med de relevante filtre i den konfigurationspakke, som **Værktøj til beskyttelse af personlige oplysninger** opretter.|
|Anmodninger om sletning|Et dataemne kan anmode om, at du sletter deres personlige oplysninger. Der er flere måder at slette personlige oplysninger på ved hjælp af tilpasningsmulighederne, men beslutningen og implementeringen er dit ansvar. I nogle tilfælde kan vælge du at redigere dataene direkte, f.eks. ved at slette en kontakt og derefter udføre kørslen Slet annulleret interaktion for at slette interaktioner for kontakten. <br><br> **Bemærk:** Hvis du har angivet en dato i feltet **Tillad sletning af dokument før** på siderne **Opsætning af salg og tilgodehavender** eller **Købsopsætning**, skal du måske ændre datoen, så kan du slette bogførte salgs- og købsdokumenter, der er udskrevet, og hvor bogføringsdatoen er på eller inden denne dato.|
|Anmodninger om rettelse|Et dataemne kan anmode om, at du retter forkerte personlige oplysninger. Dette kan gøres på flere måder. I nogle tilfælde kan du eksportere lister til Excel til hurtig masseredigering af flere poster og derefter importere de opdaterede data. Du kan finde flere oplysninger under [Eksportere forretningsdata til Excel](about-export-data.md). Du kan også manuelt redigere felter, der indeholder personlige oplysninger, f.eks. redigere oplysninger om en debitor på debitorkortet. Men transaktionsposter, f.eks. finans-, debitor- og momsposter, er nødvendige for integriteten i ERP-systemet. Hvis du gemmer personlige data i forretningstransaktionsposter, kan du overveje at bruge funktionerne til tilpasning til at ændre disse personlige oplysninger.|

## <a name="restrict-data-processing-for-a-data-subject"></a>Begrænse databehandling af et dataemne
Et dataemne kan anmode om, at du midlertidigt stopper behandlingen af deres personlige oplysninger. Du kan imødekomme sådanne anmodninger ved at markere posten som spærret på grund af beskyttelse af personlige oplysninger, så behandlingen af deres data stoppes. Når en post er markeret som spærret, kan du ikke oprette nye posteringer, der bruger denne post. Du kan f.eks. ikke du oprette en ny faktura for en debitor, når enten kunden eller sælgeren er blokeret. Åbn kortet for et dataemne, f.eks. kortene Debitor, Leverandør eller Kontakt, hvis du vil markere et dataemne som spærret, og markér afkrydsningsfeltet **Beskyttelse af personlige oplysninger spærret**. Du skal måske vælge **Vis mere** for at få vist feltet.  

## <a name="handling-data-subject-requests-while-in-trial"></a>Håndtering af dataemneanmodninger i prøveversion
Bestemte typer personlige oplysninger er en del af din Office 365-konto, og det kræver administratorrettigheder til at eksportere dem, hvis du modtager en dataemneanmodning fra en bruger om denne type personlige data i henhold til den generelle forordning om databeskyttelse (GDPR). Processen til håndtering af dataemneanmodninger er forskellige afhængigt af [!INCLUDE[d365fin](includes/d365fin_md.md)]-lejertypen.  

Hvis du har et betalt abonnement på [!INCLUDE[d365fin](includes/d365fin_md.md)], skal du kontakte organisationens lejeradministrator for at sende en dataemneanmodning. Administratoren har administratorrettigheder og -værktøjer til at imødekomme anmodningen.  

Hvis du er tilmeldt til [!INCLUDE[d365fin](includes/d365fin_md.md)] fra siden med [prøveversioner](https://trials.dynamics.com/), og din organisations administrator ikke har valgt at gå fra denne prøveoplevelse til et betalt abonnement, kan du udfylde din egen dataemneanmodning på [Siden om beskyttelse af personlige oplysninger for arbejde og skole på Azure-portalen](https://portal.azure.com#blade/Microsoft_AAD_IAM/GDPRViralBlade). Her kan du eksportere og hente dine personlige data.

Du kan også lukke din konto på denne side. Vi anbefaler dog, at du kontrollerer, at du har eksporteret og slettet alle data først, for når du sletter din konto betyder det, at du mister adgangen til [!INCLUDE[d365fin](includes/d365fin_md.md)].  

Du kan stadig markere personer som spærret af hensyn til beskyttelse af personlige oplysninger og eksportere, redigere eller slette transaktioner, som beskrevet andetsteds i denne artikel.  

## <a name="exporting-data-from-tables-not-classified-by-data-subject"></a>Eksportere data fra tabeller, der ikke er klassificeret af dataemnet
Hvis du har en situation, hvor du skal eksportere data, der ikke er klassificeret på en sådan måde, så de bliver eksporteret automatisk, f.eks. data fra tabellen Profilsvar, skal du gøre følgende: 
-   Hvis du reelt ønsker eller er nødt til at eksportere disse supplerende data, der ikke vedrører kontakten, hvilket vil sige, at det ikke er nogen direkte relation til den 
-   Føje denne tabel og relation manuelt til Rapid Start-pakken og eksportere dem direkte fra Rapid Start-pakken – det er derfor vi generere en Rapid Start-pakke, så du kan ændre den i situationer som denne.

## <a name="handling-data-about-minors"></a>Håndtering af data om mindreårige
Hvis en kontakts alder er under myndighedsalderen i henhold til lovgivningen i dit område, kan du angive dette, ved at markere afkrydsningsfeltet **Mindreårig** på kortet **Kontakt**. Når du gør dette, markeres afkrydsningsfeltet **Beskyttelse af personlige oplysninger spærret** automatisk. Når du modtager samtykke fra den mindreåriges forældre eller værge, kan du markere afkrydsningsfeltet **Forældresamtykke modtaget** for at fjerne spærringen af kontakten. Selvom du kan behandle personlige oplysninger for mindreårige, kan du ikke bruge profileringsfunktionen i Microsoft Dynamics 365 for Sales.

> [!Note]
> Ændringsloggen kan f.eks. registrere oplysninger om, hvornår og af hvem afkrydsningsfeltet **Forældresamtykke modtaget** blevet markeret. En administrator kan oprette dette ved hjælp af guiden **Opsætning af ændringslog** guide og også markere afkrydsningsfeltet **Logfør ændring af Forældresamtykke modtaget** på kortet **Kontakt**. Du kan finde flere oplysninger i [Logføre ændringer](across-log-changes.md).  

## <a name="see-also"></a>Se også
[Klassificering af Data](/dynamics-nav/classifying-data?toc=/dynamics365/business-central/toc.json)  
[Klassificere datafølsomhed](admin-classifying-data-sensitivity.md)  
[Eksportere forretningsdata til Excel](about-export-data.md)  
[Logføre ændringer](across-log-changes.md)  
[Dataemneanmodninger for GDPR](/microsoft-365/compliance/gdpr-data-subject-requests)  

