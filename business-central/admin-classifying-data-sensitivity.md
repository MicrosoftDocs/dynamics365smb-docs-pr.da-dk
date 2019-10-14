---
title: Klassificere datafølsomhed
description: Du skal angive, hvilken type data du gemmer om personer, så du kan besvare anmodninger fra dataemnet.
author: bholtorf
ms.author: bholtorf
ms.custom: na
ms.reviewer: na
ms.service: dynamics365-business-central
ms.topic: article
ms.date: 10/01/2019
ms.openlocfilehash: f2b5e3ded5c89f241d0c49ee8c6f9d196c6bae43
ms.sourcegitcommit: 02e704bc3e01d62072144919774f1244c42827e4
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 10/01/2019
ms.locfileid: "2308208"
---
# <a name="classifying-data-sensitivity"></a>Klassificere datafølsomhed
For at klassificere de felter, der indeholder følsomme eller personlige data, kan en Microsoft-partner angive egenskaben ```DataClassification``` på felter. Dette kræver adgang til databasetabellerne, enten via udviklingsmiljøet eller ved at køre et Windows PowerShell-script. Du kan finde flere oplysninger i [Klassificere data](https://docs.microsoft.com/en-us/dynamics-nav/classifying-data).  

Du kan tilføje et andet niveau i klassificering som en kunde ved at angive følsomhedsniveauer for de data, du gemmer i standardfelter og brugerdefinerede felter. Klassificeringen af datafølsomhed hjælper med til at sikre, at du ved, hvor du opbevarer personlige data i systemet, og gør det nemmere at besvare anmodninger fra registrerede. Hvis en kontakt eller kunde f.eks. beder dig om at eksportere deres personlige data. Du kan finde flere oplysninger i [Besvare anmodninger om personlige oplysninger](admin-responding-to-requests-about-personal-data.md).

> [!Important]
> Microsoft stiller kun denne funktion til klassificering af datafølsomhed til rådighed for at gøre tingene nemmere for dig. Det er dit ansvar at klassificere data korrekt og i overensstemmelse med de love og regler, der gælder for dig. Microsoft fraskriver sig ethvert ansvar i forbindelse med krav vedrørende din klassificering af dataene.  

I nedenstående tabel beskrives de datafølsomhedsniveauer, du kan tildele.

|Følsomhed|Beskrivelse|
|----|----|
|Følsomme | Oplysninger om en registrets racemæssig eller etnisk baggrund, politiske meninger, religiøs overbevisning, engagement i fagforeninger, fysiske eller mentale sundhed, seksualitet eller oplysninger om forbrydelser. |
|Personlig | Oplysninger, der kan bruges til at identificere en registreret, enten direkte eller sammen med andre data eller oplysninger.|
|Fortroligt | Forretningsdata, som du bruger til bogholderi eller andre forretningsformål, og ikke ønske at vise til andre enheder. Det kan f.eks. omfatter poster.|
|Normal | Generelle data, der ikke hører til i nogen andre kategorier.|

## <a name="how-do-i-classify-my-data"></a>Hvordan kan jeg klassificere dataene?
Klassificering af følsomheden i et stort antal felter ét ad gangen vil tage lang tid. Som en hjælp til at gøre det hurtigere leverer vi værktøjer, som du kan bruge til at klassificere følsomheden af felter i bundter og derefter finjustere klassificeringen for bestemte felter. Du kan finde værktøjer i regnearket Klassificering af data, som er tilgængelig i rollecentrene Administration af brugere, brugergrupper og tilladelser. Du skal være systemadministrator for at kunne bruge regnearket.

> [!Important]
> Når du åbner regnearket Klassificering af data for første gang, vil det være tomt. Du skal køre guiden Dataklassificering for at oprette listen over felter. Du kan starte guiden ved at vælge handlingen **Konfigurer dataklassificeringer**.

Med regnearket Klassificering af data kan du f.eks. gøre følgende:  

* Brug guiden Dataklassificering til at eksportere dine felter til et Excel-regneark, hvor du kan klassificere felterne i bundter. Det er især nyttigt at bruge Excel-regnearket, hvis du arbejder sammen med en Microsoft-partner. Når du opdaterer regnearket, kan du bruge guiden til at indlæse og anvende klassificeringerne. Du kan også bruge guiden til at klassificere felter manuelt.  
* Vælg et felt, og filtrer derefter oversigten for at finde lignende felter, der sandsynligvis tilhører den samme klassificering som det felt, du har baseret søgningen på.  
* Undersøge et felt ved at få vist dets indhold.  

> [!Tip]
> Vi har defineret prøvefølsomhedsklassificeringer for tabellerne og felterne i demoregnskabet Cronus. Du kan bruge disse klassificeringer som inspiration, når du klassificerer dine egne tabeller og felter.

## <a name="see-also"></a>Se også
[Klassificering af Data](https://docs.microsoft.com/en-us/dynamics-nav/classifying-data)  
