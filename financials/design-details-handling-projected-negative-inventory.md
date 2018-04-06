---
title: "Designoplysninger – Håndtering af forventet negativt lager | Microsoft Docs"
description: "Genbestillingspunktet udtrykker det forventede behov under leveringstiden for varen. Når genbestillingspunktet er overskredet, er det tid til at bestille mere. Men den forventede lagerbeholdning skal være stor nok til at dække behovet, indtil den nye ordre er modtaget. I mellemtiden bør sikkerhedslageret tage højde for udsving i behov op til et målrettet serviceniveau."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 07/01/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 2c13559bb3dc44cdb61697f5135c5b931e34d2a8
ms.openlocfilehash: 3436e2a00858a1dbfcbb0a44cb9db32bd7665593
ms.contentlocale: da-dk
ms.lasthandoff: 03/22/2018

---
# <a name="design-details-handling-projected-negative-inventory"></a>Designoplysninger: Håndtering af forventet negativt lager
Genbestillingspunktet udtrykker det forventede behov under leveringstiden for varen. Når genbestillingspunktet er overskredet, er det tid til at bestille mere. Men den forventede lagerbeholdning skal være stor nok til at dække behovet, indtil den nye ordre er modtaget. I mellemtiden bør sikkerhedslageret tage højde for udsving i behov op til et målrettet serviceniveau.  

 Derfor anser planlægningssystemet det for en nødsituation, hvis et fremtidigt behov ikke kan dækkes fra den forventede lagerbeholdning, eller udtrykt på en anden måde, hvis den forventede lagerbeholdning bliver negativ. Systemet håndterer en sådan undtagelse ved at foreslå en ny forsyningsordre for at imødekomme en del af det behov, som ikke kan opfyldes af lagerbeholdningen eller andre forsyninger. Ordrestørrelsen på den nye forsyningsordre vil ikke tage det maksimale lager eller genbestillingsantal i betragtning og vil heller ikke tage ordremodifikatorerne Maks. ordrestørrelse, Min. ordrestørrelse og Oprundingsfaktor i betragtning. I stedet afspejler den nøjagtig mangel.  

 Planlægningslinjen for denne type forsyningsordre viser et Nødsituation-advarselsikon, og yderligere oplysninger kan findes ved opslag for at informere brugeren om situationen.  

 I følgende illustration repræsenterer forsynings-id en akutordre for at justere for negativt lager.  

 ![](media/nav_app_supply_planning_2_negative_inventory.png "NAV_APP_supply_planning_2_negative_inventory")  

1.  Forsyning **A**, oprindeligt planlagte lagerbeholdning, er under genbestillingspunkt.  

2.  En ny ordre, der er planlagt fremad, oprettes (**C**).  

     (Antal = Maks. lagerbeholdning – Forventet lagerbeholdning)  

3.  Forsyning **A** er lukket af behov **B**, som ikke fuldt ud dækkes.  

     (Behov **B** kunne forsøge at planlægge forsyning C, men det vil ikke ske i overensstemmelse med intervalkonceptet).  

4.  Ny forsyning (**D**) er oprettet for at dække det resterende antal efter behov **B**.  

5.  Behov **B** er lukket (oprettelse af en påmindelse til den forventede lagerbeholdning).  

6.  Den nye forsyning **D** er lukket.  

7.  Planlagt lagerbeholdning kontrolleres, og genbestillingspunkt er ikke krydset.  

8.  Forsyning **C** er lukket (der findes ingen yderligere behov).  

9. Sidste kontrol: Der findes ingen udestående påmindelser om lagerniveau.  

> [!NOTE]  
>  Trin 4 afspejler, hvordan systemet reagerer i versioner tidligere end Microsoft Dynamics NAV 2009 SP1.  

 Dette afslutter beskrivelsen af de centrale principper vedrørende lagerplanlægning baseret på genbestillingsmetoder. I følgende afsnit beskrives karakteristika for de fire understøttede genbestillingsmetoder.  

## <a name="see-also"></a>Se også  
 [Designoplysninger: Genbestillingsmetoder](design-details-reordering-policies.md)   
 [Designoplysninger: Planlægningsparametre](design-details-planning-parameters.md)   
 [Designoplysninger: Håndtering af genbestillingsmetoder](design-details-handling-reordering-policies.md)   
 [Designoplysninger: Forsyningsplanlægning](design-details-supply-planning.md)

