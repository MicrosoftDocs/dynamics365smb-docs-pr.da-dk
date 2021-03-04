---
title: Designoplysninger – Tabellen Planlægningsopgave | Microsoft Docs
description: Dette emne indeholder indsigt i, hvad der sker, når du ændrer den måde, du planlægger på for en vare.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: b981fc2d234c2f8c32e0fe10daa1ce20f25bb4f8
ms.sourcegitcommit: ddbb5cede750df1baba4b3eab8fbed6744b5b9d6
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 10/01/2020
ms.locfileid: "3922007"
---
# <a name="design-details-planning-assignment-table"></a>Designoplysninger: Tabellen Planlægningsopgave
Der skal foretages planlægning for alle varer, men der er ingen grund til at beregne en plan for en vare, medmindre der er sket en ændring i mønstret for behov eller forsyning, siden sidst en plan blev beregnet.  

Hvis brugeren har angivet en ny salgsordre eller ændret en eksisterende, er der grund til at genberegne planen. Andre årsager omfatter en ændring i budgettet eller den ønskede mængde sikkerhedslager. Ændring af en stykliste ved at tilføje eller fjerne en komponent ville sandsynligvis angive en ændring, men kun for komponentvaren.  

For flere lokationer finder tildelingen sted på niveauet for vare pr. lokationskombination. Hvis en salgsordre f.eks. er blevet oprettet på kun én lokation, bliver varen tildelt på den pågældende lokation til planlægning.  

Årsagen til at vælge varer til planlægning er et spørgsmål om systemets ydeevne. Hvis der ikke er opstået nogen ændring af en vares behov-forsyningsmønster, foreslår planlægningssystemet ikke nogen handlinger, der skal udføres. Uden planlægningsopgave ville systemet skulle udføre beregningerne for alle varer for at finde ud af, hvad der skal planlægges, og det ville forbruge systemressourcer.  

Tabellen **Planlægningsopgave** overvåger behovs- og forsyningshændelser og tildeler de relevante varer til planlægning. Følgende hændelser overvåges:  

* En ny salgsordre, prognose, komponent, købsordre, produktionsordre, montageordre eller overflytningsordre.  
* Ændring af vare, antal, lokation, variant eller dato på en salgsordre, forecast, komponent, købsordre, produktionsordre, montageordre eller overflytningsordre.  
* Annullering af en salgsordre, forecast, komponent, købsordre, produktionsordre, montageordre eller overflytningsordre.  
* Forbrug af varer udover det planlagte.  
* Afgang af andre varer end de planlagte.  
* Ikke-planlagte ændringer i lageret.  

For disse direkte forsyning-behov-flytninger, vedligeholder ordresporings- og aktionsmeddelelsessystemet tabellen Planlægningsopgave og angiver en planlægningsårsag som en aktionsmeddelelse.  

Følgende ændringer i stamdata kan også forårsage en uligevægt i planlægning:  

* Skift status til Certificeret i produktionsstyklistehovedet (for alle varer, der bruger det pågældende hoved).  
* Slettet linje (underordnet vare).  
* Skift status til Certificeret i rutehovedet (for alle varer, der bruger den rute).  
* Ændringer i følgende felter på varekort.  
* Sikkerhedslagerantal eller sikkerhedstid  
* Leveringstid.  
* Genbestillingspunkt.  
* Produktionsstyklistenr. (og alle underordnede af gammel styklistereference).  
* Rutenr.  
* Genbestillingsmetode.  

I disse tilfælde vil en ny funktion, administration af planlægning, vedligeholde tabellen og angive årsagen til planlægning som Bevægelse.  

Følgende ændringer medfører ikke en planlægningsopgave:  

* Kalendere  
* Andre planlægningsparametre på varekortet  

Ved beregning af en hovedplan eller en MRP gælder følgende begrænsninger:  

* Hovedplan: Planlægningssystemet kontrollerer, at varen har en behovsprognose eller en salgsordre. Hvis ikke, medtages varen ikke i planen.  
* MRP: Hvis planlægningssystemet registrerer, at varen genbestilles af en hovedplans planlægningslinje eller forsyningsordre, udelades varen i planlægningen. Et hvilket som helst behov fra relevante komponenter er imidlertid inkluderet.  

## <a name="see-also"></a>Se også  
[Designoplysninger: Afstemning mellem behov og forsyning](design-details-balancing-demand-and-supply.md)   
[Designoplysninger: Håndtering af genbestillingsmetoder](design-details-handling-reordering-policies.md)   
[Designoplysninger: Overførsler i planlægning](design-details-transfers-in-planning.md)   
[Designoplysninger: Planlægningsparametre](design-details-planning-parameters.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]