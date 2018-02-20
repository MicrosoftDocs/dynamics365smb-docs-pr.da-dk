---
title: "Designoplysninger – Overvågning af det forventede lagerniveau og genbestillingspunktet | Microsoft Docs"
description: "Få mere at vide, hvordan lagerplanlægningen skelner mellem planlagt beholdning og projekterede tilgængelige lagerniveauer."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: design, supply, inventory, planning
ms.date: 07/01/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 2c13559bb3dc44cdb61697f5135c5b931e34d2a8
ms.openlocfilehash: a0e64d96389739c67a9e9f548958fac12e3aca2a
ms.contentlocale: da-dk
ms.lasthandoff: 12/14/2017

---
# <a name="design-details-monitoring-the-projected-inventory-level-and-the-reorder-point"></a>Designoplysninger: Overvågning af det forventede lagerniveau og genbestillingspunktet
Lageret er en slags forsyning, men for lagerplanlægning skelner planlægningssystemet mellem to lagerniveauer:  

* Planlagt beholdning  
* Forventet disponibel beholdning  

## <a name="projected-inventory"></a>Planlagt beholdning  
Oprindeligt er planlagt lagerbeholdning mængden af bruttolager, herunder forsyning og behov i fortiden, selvom det ikke er bogført, når du starter planlægningsprocessen. I fremtiden bliver det et bevægeligt planlagt lagerniveau, der vedligeholdes af bruttomængder fra fremtidig forsyning og behov, fordi det føres langs tidslinjen (uanset om det er reserveret eller på andre måder tildelt).  

Den planlagte beholdning bruges af systemet til at overvåge genbestillingspunktet og bestemme genbestillingsantallet, når du bruger genbestillingsmetoden Maks. antal.  

## <a name="projected-available-inventory"></a>Forventet disponibel beholdning  
Den forventede disponible beholdning er en del af det planlagte lager, der er tilgængeligt til at opfylde behov på et givet tidspunkt. Den forventede disponible beholdning der bruges af planlægningssystemet ved overvågning af niveauet for sikkerhedslageret.  

Den forventede disponible beholdning bruges i planlægningssystemet til at overvåge niveauet for sikkerhedslageret, da sikkerhedslageret altid skal være tilgængeligt til at afhjælpe uventede behov.  

## <a name="time-buckets"></a>Intervaller  
Det er afgørende at have streng kontrol med den forventede lagerbeholdning for at registrere, når genbestillingspunktet nås eller passeres, og for at beregne det korrekte ordreantal, når du bruger genbestillingsmetoden Maks. antal.  

Som tidligere nævnt beregnes den forventede lagerbeholdning i starten af planlægningsperioden. Det er et bruttoniveau, der ikke medtager reservationer og lignende fordelinger. Systemet overvåger de aggregerede ændringer over en tidsperiode, et interval, for at overvåge dette lagerniveau under planlægningssekvensen. Systemet sikrer, at tidsintervallet er mindst én dag, da det er den mest nøjagtige tidsenhed for en behovs- eller forsyningshændelse.  

## <a name="determining-the-projected-inventory-level"></a>Bestemmelse af det forventede lagerniveau  
Følgende sekvens beskriver, hvordan det planlagte lagerniveau bestemmes:  

* Når en forsyningshændelse, f.eks. en indkøbsordre, er blevet fuldstændig planlagt, øges den projekterede lagerbeholdning på forfaldsdatoen.  
* Når en behovshændelse har opfyldt behovet, formindskes den projekterede lagerbeholdning ikke straks. Der bogføres i stedet en påmindelse om reducering, som er en intern post, der indeholder dato og mængdebidrag til den planlagte lagerbeholdning.  
* Når en efterfølgende forsyningshændelse planlægges og placeres på tidslinjen, undersøges de bogførte reduktionsrykkerne én efter én indtil den planlagte dato for levering, mens den projekterede lagerbeholdning opdateres. Under denne proces kan niveauet for genbestillingspunktet for den interne forøgelse blive nået eller passeret.  
* Hvis der er indført en ny forsyningsordre, kontrollerer systemet, om den er indtastet før den aktuelle forsyning. Hvis det er, bliver den nye forsyning den aktuelle forsyning, og den udlignende procedure starter forfra.  

Nedenstående viser en grafisk illustration af dette princip:  

![](media/nav_app_supply_planning_2_projected_inventory.png "NAV_APP_supply_planning_2_projected_inventory")  

1. Forsyning **Sa** af 4 (faste) lukker behov **Da** af -3.  
2. CloseDemand: Opret en påmindelse om reducering af -3 (ikke vist).  
3. Forsyning **Sa** er lukket med et overskud på 1 (der findes ingen yderligere behov).  

     Dette øger det forventede lagerniveau til +4, mens den forventede **disponible** beholdning bliver -1.  

4. Den næste forsyning **Sb** af 2 (en anden ordre) er allerede placeret på tidslinjen.  
5. Systemet kontrollerer, om der er påmindelse om reducering før **Sb** (det er der ikke, så ingen handling).  
6. Systemet lukker forsyning **Sb** (der findes ingen yderligere behov) – enten A: ved at reducere den til 0 (annullere) eller B: ved at lade den være.  

     Dette øger den projekterede lagerbeholdning (A: +0 => +4 eller B: +2 = +6).  

7. Systemet foretager endelig kontrol: Er der nogen påmindelse om reducering? Ja, der er en på datoen for **Da**.  
8. Systemet føjer reduktionsrykkeren af -3-rykker til det planlagte lagerniveau enten A: +4 -3 = 1 eller B: +6 -3 = +3.  
9. I tilfælde af A opretter systemet en fremad planlagt ordre fra datoen **Da**.  

     Genbestillingspunktet er ikke nået i B, og der oprettes ingen ny ordre.  

## <a name="see-also"></a>Se også  
[Designoplysninger: Genbestillingsmetoder](design-details-reordering-policies.md)   
[Designoplysninger: Planlægningsparametre](design-details-planning-parameters.md)   
[Designoplysninger: Håndtering af genbestillingsmetoder](design-details-handling-reordering-policies.md)   
[Designoplysninger: Forsyningsplanlægning](design-details-supply-planning.md)

