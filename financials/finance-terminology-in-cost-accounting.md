---
title: Terminologi i omkostningsregnskab | Microsoft Docs
description: Dette emne definerer vigtige termer, der anvendes i omkostningsregnskab.
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
ms.openlocfilehash: fa2009d6e8c625efa3918186a1b610a863260d5e
ms.contentlocale: da-dk
ms.lasthandoff: 09/22/2017

---
# <a name="terminology-in-cost-accounting"></a>Terminologi i omkostningsregnskab
Dette emne definerer vigtige termer, der anvendes i omkostningsregnskab.  

## <a name="key-terms"></a>Vigtige termer  
 Følgende tabel viser definitionerne af de vigtigste termer i omkostningsregnskab.  

|**Begreb**|**Definition**|  
|--------------|--------------------|  
|Fordelingsnøgle|Fordelingsnøglen er det grundlag, der bruges til at allokere omkostninger. Det er normalt en mængde, f.eks. antal anvendte kvadratmeter, antallet af medarbejdere eller arbejdstimer, der bruges. For eksempel deler to afdelinger med 20 og 10 medarbejdere kantineomkostninger. Omkostningerne fordeles mellem afdelinger ved hjælp af en fordelingsnøgle, der repræsenterer antallet af medarbejdere. To tredjedele af omkostningerne allokeres til den første afdeling, og en tredjedel af omkostningerne allokeres til den anden afdeling.|  
|Fordelingskilde|Fordelingskilden definerer, hvilke omkostninger, der allokeres. Allokeringer er defineret i tabeller for fordelingskilder og fordelingsmål . Hver allokering, der består af en fordelingskilde og mål for en eller flere fordelinger. For eksempel kan alle omkostninger ved omkostningstypen opvarmning, som er en fordelingskilde, allokeres til workshop, produktion og salgsomkostningssteder, der er tre fordelingsmål.|  
|Fordelingsmål|Fordelingsmålet bestemmer, hvortil omkostningerne allokeres. Allokeringer er defineret i tabeller for fordelingskilder og fordelingsmål . Hver allokering, der består af en fordelingskilde og mål for en eller flere fordelinger. For eksempel kan alle omkostninger ved omkostningstypen opvarmning, som er en fordelingskilde, allokeres til workshop, produktion og salgsomkostningssteder, der er tre fordelingsmål.|  
|Omkostningsregnskab|Faktiske omkostninger i forbindelse med operationer, processer, afdelinger eller produkter registreres i omkostningsregnskab. Disse omkostninger fordeles til omkostningssteder og omkostningsobjekter ved hjælp af forskellige omkostningsfordelingsmetoder. Ledere kan bruge statistikker og rapporter som omkostningsfordelingsark og driftsregnskabsanalyse til at træffe beslutninger og reducere tab. Omkostningsregnskab henter data fra regnskabet, men fungerer uafhængigt. Derfor påvirker transaktioner, der er bogført i omkostningsregnskabet, ikke data i regnskabet.|  
|Pristype|Diagrammet over omkostningstyper har samme funktion som kontoplanen i regnskabet. De er ofte opbygget på samme måde. Det er derfor muligt at overføre finanskontoplanen til diagrammet over omkostningstyper og derefter redigere den. Diagrammet over omkostningstyper kan også oprettes fra bunden.|  
|Omkostningssted|Omkostningssteder er som oftest afdelinger og profitcentre, der primært er ansvarlig for virksomhedens omkostninger og indtægter. Omkostningssteder kan synkroniseres med dimensioner i regnskabet. Det er også muligt at tilføje nye omkostningssteder og definere deres egne sorteringer med subtotaler.|  
|Omkostningsobjekt|Omkostningsobjekter er en virksomheds produkter, produktgrupper eller tjenester, en virksomheds færdige varer, der i sidste ende bærer omkostningerne. Omkostningsobjekter kan synkroniseres med dimensioner i regnskabet. Det er også muligt at tilføje nye omkostningsobjekter og definere deres egne sorteringer med subtotaler.|  
|Omkostningsfordeling|Omkostningsfordeling er en proces for allokering af omkostninger til omkostningssteder eller omkostningsobjekter. For eksempel allokeres lønomkostningerne lastbilschaufføren i salgsafdelingen til salgsafdelingens omkostningssted. Det er ikke nødvendigt at allokere lønomkostningerne til andre omkostningssteder. Et andet eksempel er, at omkostningerne til et dyrt computersystem allokeres til de af virksomhedens produkter, der anvender systemet.|  
|Dynamisk fordeling|Dynamisk allokeringer er afhængige af allokeringsbaser, der kan ændres, f.eks. antallet af medarbejdere i afdelingen eller salgsindtægter fra projektet inden for en bestemt periode. Der findes ni foruddefinerede dynamisk fordelingsbaser, som brugerne kan definere ved hjælp af fem filtre.|  
|Købspris|Direkte omkostninger er omkostninger, som kan direkte allokeres til et omkostningsobjekt, f.eks. materiale, der køber til et bestemt produkt.|  
|Fast omkostning|Faste omkostninger er omkostninger, der ikke er afhængige af niveauet af varer eller tjenesteydelser, der produceres af virksomhed. De er som regel tidsrelaterede, såsom løn eller leje, der betales pr. måned. De står i modsætning til variable omkostninger, som er relateret til mængde og betales pr. producerede mængde.|  
|Indir. omkostninger|Indirekte omkostninger kan ikke direkte konteres til et omkostningsobjekt, såsom en bestemt funktion eller et bestemt produkt. Indirekte omkostninger kan være faste eller variable. Indirekte omkostninger kan være udgifter til skat, administration, personale og sikkerhed og er også kendt som faste omkostninger.|  
|Niveau|Niveau bruges til at definere fordelingsrækkefølge. Niveau er defineret som et tal mellem 1 og 99. Fordelingsbogføringen følger niveauernes rækkefølge. For eksempel sikrer niveau, at administration først allokeres til workshop, før workshop allokeres til køretøj og produktion.|  
|Statisk allokering|Statisk allokeringer er baseret på et fast sæt værdier, for eksempel anvendt antal kvadratmeter eller et etableret fordelingsforhold såsom 5: 2: 4.|  
|Driftsomkostning|Driftsomkostninger er tilbagevendende udgifter, som er relateret til driften af en virksomhed, en enhed eller et komponent.|  
|Indirekte kostpris|Faste omkostninger vedrører løbende udgifter til drift af en virksomhed. De er alle omkostninger på resultatopgørelsen, med undtagelse af direkte arbejdsløn, direkte materialer og direkte udgifter. Faste omkostninger inkluderer regnskabsmæssige gebyrer, reklame, afskrivning, forsikring, renter, juridisk gebyrer, leje, reparationer, forsyninger, skatter, telefonregninger, rejser og forbrugsomkostninger.|  
|Variabelt omkostningstrin|Variable omkostningstrin er omkostninger, der drastisk ændres på visse punkter, da de indebærer store køb, der ikke kan spredes ud over tid. For eksempel kan en medarbejder producere 100 tabeller på en måned. Medarbejderens løn er konstant over et produktionsområde på 1 til 100 tabeller. Hvis virksomheden ønsker at producere 110 tabeller, skal virksomhed bruge to medarbejdere. Dermed fordobles prisen.|  
|Fordeling|Den del, der fordeles blandt omkostningssteder eller omkostningsobjekter.|  
|Statisk vægtning|Omkostninger fordeles i henhold til fordelingsnøgler, som kan ændres ved hjælp af en multiplikator. <br />For eksempel deler to afdelinger med 20 og 10 medarbejdere kantineomkostninger. Omkostningerne fordeles mellem afdelingerne ved hjælp af en fordelingsnøgle, der repræsenterer antallet af medarbejdere, der spiser i kantinen. I den første tjeneste spiser kun 5 medarbejdere i kantinen, så denne afdeling har en multiplikator på 0,25. Grundlag for fordeling er 20 x 0,25 = 5. Det samlede antal medarbejdere, der spiser i kantinen er 15. En tredjedele af omkostningerne allokeres til den første afdeling, og to tredjedel af omkostningerne allokeres til den anden afdeling.|  
|Variabel omkostning|Variable omkostninger er udgifter, der ændres i forhold til en virksomheds aktivitet. Variable omkostninger er summen af marginalomkostninger over alle producerede enheder. Faste omkostninger og variable omkostninger udgør de to komponenter af samlede omkostninger.|  
|Variant|En variant bruges som en valgfri brugerdefineret etiket for tildelinger. Formålet med etiketten er at filtrere grupper af fordelinger.|  

## <a name="see-also"></a>Se også  
 [Om omkostningsregnskab](finance-about-cost-accounting.md)   
 [Regnskab for omkostninger](finance-manage-cost-accounting.md)  
 [Arbejde med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

