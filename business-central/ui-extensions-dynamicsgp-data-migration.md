---
title: Overførsel af data fra Dynamics GP med udvidelsen Dataoverførsel | Microsoft Docs
description: Du kan bruge udvidelsen Dataoverførsel i Dynamics GP til at overføre debitorer, kreditorer, lagervarer, finanskonti, åbne transaktioner for tilgodehavender og skyldige beløb fra Dynamics GP til Business Central.
documentationcenter: ''
author: edupont04
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms. search.keywords: app, add-in, manifest, customize, import, implement
ms.date: 04/01/2020
ms.author: edupont
ms.openlocfilehash: 89611f41192820e03ee055ce171aa55738809195
ms.sourcegitcommit: 88e4b30eaf6fa32af0c1452ce2f85ff1111c75e2
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 04/01/2020
ms.locfileid: "3194255"
---
# <a name="the-dynamics-gp-data-migration-extension"></a>Udvidelsen Overførsel af data med Dynamics GP 
Udvidelsen gør det nemt at overføre debitorer, kreditorer, lagervarer, finanskonti, åbne transaktioner for tilgodehavender og skyldige beløb fra Dynamics GP til [!INCLUDE[prodshort](includes/prodshort.md)]. Hvis din virksomhed bruger Dynamics GP i dag, kan du eksportere de relevante poster og derefter åbne en assisteret opsætningsvejledning for at tilføje dataene i [!INCLUDE[prodshort](includes/prodshort.md)]. Udvidelsen til overførsel fungerer på alle understøttede versioner af Microsoft Dynamics GP. Du kan finde flere oplysninger under [Importere virksomhedsdata fra andre økonomisystemer](across-import-data-configuration-packages.md).

> [!NOTE]
>  Udvidelsen udfases i 15.3-opdateringen. Det anbefales, at brugere, der vil overflytte fra Dynamics GP, begynder at bruge guiden **Skymigrering** i stedet. **Skymigrering**-udvidelsen har mere robust funktionalitet og henter flere data til Business Central fra Dynamics GP.

## <a name="exporting-data-from-dynamics-gp"></a>Eksportere data fra Dynamics GP
Du skal have eksporteret nogle af eller alle dine eksisterende debitorer, kreditorer, lagervarer og finanskonti ved hjælp af funktionen til dataeksport i Dynamics GP. Når du vælger de data, der skal eksporteres, kan du vælge følgende typer:

* Konto  
* Kunde  
* Vare  
* Kreditor  

Når udlæsningsfilen er oprettet, har du en zip-fil, der indeholder flere txt-filer, der afhænger af, hvad du har valgt under processen til eksport af data.  Der vil også være ekstra txt-filer, der bliver oprettet og indeholder supplerende oplysninger, der er nødvendige ved installationen i den nye [!INCLUDE[prodshort](includes/prodshort.md)]-virksomhed.

Udvidelsen til overførsel af data til Dynamics GP tilknyttes automatisk de udlæste data, så dataene hurtigt er tilgængelige i det nye regnskab i [!INCLUDE[prodshort](includes/prodshort.md)].

## <a name="whats-new-in-the-october-2018-release"></a>Nyheder i oktober 2018-udgivelsen

I denne version vi har udvidet mængden af data, vi leverer til [!INCLUDE[prodshort](includes/prodshort.md)] fra Dynamics GP.

I guiden Dataoverflytning kan du nu vælge, hvordan du vil overføre Dynamics GP-kontoplanen. Du kan overføre den eksisterende kontoplan, eller du kan oprette en ny kontoplan, der er baseret på de eksisterende kontoplaner.  

Hvis du vil bruge den eksisterende kontoplan, oprettes kontiene som hovedkontosegmentet fra Dynamics GP, og de ekstra segmenter oprettes som dimensioner i [!INCLUDE[prodshort](includes/prodshort.md)].  

Hvis du vil oprette en ny kontoplan, får du en ekstra kontooplysningsside i guiden, så du kan hente projektmappen, foretage de relevante ændringer og derefter importere projektmappen igen for at ændre dine konti.  

Du skal hente Excel-projektmappen og knytte et nyt kontonummer til hvert kontonummer i Excel-regnearket. Hver konto skal have sit eget nummer, ellers mislykkes overførslen. Når du har oprettet tilknytningen, kan du fortsætte gennem overflytningsguiden ved at importere den Excel-projektmappe, du lige har opdateret. Guiden validerer, at hver række har et entydigt kontonummer, og at ingen rækker har et tomt nyt kontonummer.  

Med ændringen af tilknytning af kontoindstillingerne for kontoplanen kan du også se en ændring af den type data, der overføres til finanskladden for kontonumrene.  

- Hvis du vælger at bruge de eksisterende kontonumre, overfører vi primosaldoen for den primære hovedsegmentet (nyt kontonummer)som en summering af hovedkontonummeret på tidspunktet for overflytningen.  
- Hvis du vælger at oprette nye kontonumre, leverer vi oversigtsoplysninger for det, der tilsvarer to regnskabsår baseret på de regnskabsperioder, du har angivet i Dynamics GP.

I tidligere versioner af [!INCLUDE[prodshort](includes/prodshort.md)] overflyttede guiden en summeringspostering for debitor-/kreditorsaldoen i Dynamics GP. Nu leverer vi detaljerede åbne posteringer for debitorer og kreditorer på tidspunktet for overflytningen. Hvad indebærer dette? Hvis kunden har 3 udestående transaktioner, der er registreret i modulet Debitor, viser guiden disse transaktioner i [!INCLUDE[prodshort](includes/prodshort.md)] med det udestående beløb, som dokumentbeløbet. Dette er den samme for modulet Kreditor for kreditorer.  

Lagervarer indlæses sammen med den omkostningsevalueringsmetoden, der blev valgt, da virksomhedens installationsguiden blev kørt. Serviceartikler tildeles automatisk FIFO-værdiansættelsesmetoden. Aktuelt leverer vi Antal på lager for varer på tidspunktet for overflytning.  Dette antal kan vises på den tomme lokation.  

Den sidste indstilling, der vises i guiden Dataoverførsel til Dynamics GP er muligheden for at angive dine bogføringsindstilling. Denne indstilling angiver, om du automatisk vil bogføre alle transaktioner i finanskladden, så snart overførslen flytter data i [!INCLUDE[prodshort](includes/prodshort.md)], eller om du vil bogføre manuelt, så alle transaktioner placeres i batches på siden Finanskladde, så du kan kontrollere oplysningerne, før du bogfører. Denne indstilling kan ses på siden Kontoplan.


## <a name="see-also"></a>Se også
[Importere virksomhedsdata fra andre økonomisystemer](across-import-data-configuration-packages.md)  
[Tilpasse [!INCLUDE[prodshort](includes/prodshort.md)] ved hjælp af udvidelser](ui-extensions.md)  
