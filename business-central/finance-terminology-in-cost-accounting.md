---
title: Terminologi i omkostningsberegning
description: 'I denne artikel defineres de nøglebegreber, der bruges i omkostningsregnskaber, f.eks. allokeringsnøgle og allokeringskilde.'
author: brentholtorf
ms.topic: conceptual
ms.devlang: al
ms.search.keywords: null
ms.search.form: 1123
ms.date: 07/25/2024
ms.author: bholtorf
ms.service: dynamics-365-business-central
ms.reviewer: bholtorf
---

# Terminologi i omkostningsberegning

I denne artikel defineres de nøglebegreber, der bruges i omkostningsberegning.  

## Vigtige begreber

 Følgende tabel viser definitionerne af de vigtigste termer i omkostningsregnskab.  

|**Begreb**|**Definition**|  
|--------------|--------------------|  
|Fordelingsnøgle|Fordelingsnøglen er det grundlag, der bruges til at allokere omkostninger. Det er typisk en mængde, såsom kvadratmeter optaget, antal medarbejdere eller anvendte arbejdstimer. For eksempel deler to afdelinger med 20 og 10 medarbejdere kantineomkostninger. Omkostningerne fordeles mellem afdelinger ved hjælp af en fordelingsnøgle, der repræsenterer antallet af medarbejdere. To tredjedele af omkostningerne allokeres til den første afdeling, og en tredjedel af omkostningerne allokeres til den anden afdeling.|  
|Fordelingskilde|Fordelingskilden definerer, hvilke omkostninger, der allokeres. Allokeringer er defineret i tabeller for fordelingskilder og fordelingsmål . Hver allokering, der består af en fordelingskilde og mål for en eller flere fordelinger. For eksempel kan alle omkostninger ved omkostningstypen opvarmning, som er en fordelingskilde, allokeres til workshop, produktion og salgsomkostningssteder, der er tre fordelingsmål.|  
|Fordelingsmål|Fordelingsmålet bestemmer, hvortil omkostningerne allokeres. Allokeringer er defineret i tabeller for fordelingskilder og fordelingsmål . Hver allokering, der består af en fordelingskilde og mål for en eller flere fordelinger. For eksempel kan alle omkostninger ved omkostningstypen opvarmning, som er en fordelingskilde, allokeres til workshop, produktion og salgsomkostningssteder, der er tre fordelingsmål.|  
|Omkostningsregnskab|Faktiske omkostninger i forbindelse med operationer, processer, afdelinger eller produkter registreres i omkostningsregnskab. Disse omkostninger fordeles til omkostningssteder og omkostningsobjekter ved hjælp af forskellige omkostningsfordelingsmetoder. Ledere kan bruge statistikker og rapporter som omkostningsfordelingsark og driftsregnskabsanalyse til at træffe beslutninger og reducere tab. Omkostningsregnskab henter data fra regnskabet, men fungerer uafhængigt. Derfor påvirker transaktioner, der bogføres i omkostningsberegningen, ikke dataene i finansmodulet.|  
|Omkostningstype|Diagrammet over omkostningstyper har samme funktion som kontoplanen i regnskabet. De er ofte struktureret på samme måde. Det er derfor muligt at overføre finanskontoplanen til diagrammet over omkostningstyper og derefter ændre den. Diagrammet over omkostningstyper kan også oprettes fra bunden.|  
|Omkostningssted|Omkostningssteder er som oftest afdelinger og profitcentre, der primært er ansvarlig for virksomhedens omkostninger og indtægter. Omkostningssteder kan synkroniseres med dimensioner i regnskabet. Det er også muligt at tilføje nye bærere og definere deres egen sortering med subtotaler.|  
|Omkostningsobjekt|Omkostningsobjekter er produkter, produktgrupper eller tjenester fra en virksomhed, en virksomheds færdige varer, der i sidste ende bærer omkostningerne. Omkostningsobjekter kan synkroniseres med dimensioner i regnskabet. Det er også muligt at tilføje nye omkostningsobjekter og definere deres egen sortering med subtotaler.|  
|Omkostningsfordeling|Omkostningsfordeling er en proces for allokering af omkostninger til omkostningssteder eller omkostningsobjekter. For eksempel allokeres lønomkostningerne lastbilschaufføren i salgsafdelingen til salgsafdelingens omkostningssted. Det er ikke nødvendigt at allokere lønomkostningerne til andre bærere. Et andet eksempel er, at omkostningerne til et dyrt computersystem allokeres til de af virksomhedens produkter, der anvender systemet.|  
|Dynamisk fordeling|Dynamisk allokeringer er afhængige af allokeringsbaser, der kan ændres, f.eks. antallet af medarbejdere i afdelingen eller salgsindtægter fra projektet inden for en bestemt periode. Der findes ni foruddefinerede dynamisk fordelingsbaser, som brugerne kan definere ved hjælp af fem filtre.|  
|Købspris|Direkte omkostninger er omkostninger, som kan direkte allokeres til et omkostningsobjekt, f.eks. materiale, der køber til et bestemt produkt.|  
|Fast omkostning|Faste omkostninger er de omkostninger, der ikke afhænger af niveauet af varer eller tjenester, der produceres af virksomheden. De er som regel tidsrelaterede, såsom løn eller leje, der betales pr. måned. De står i modsætning til variable omkostninger, som er relateret til mængde og betales pr. producerede mængde.|  
|Indir. omkostninger|Indirekte omkostninger er ikke direkte ansvarlige over for et omkostningsobjekt, f.eks. en bestemt funktion eller et bestemt produkt. Indirekte omkostninger kan være faste eller variable. Indirekte omkostninger kan være udgifter til skat, administration, personale og sikkerhed og er også kendt som faste omkostninger.|  
|Niveau|Niveau bruges til at definere fordelingsrækkefølge. Niveau er defineret som et tal mellem 1 og 99. Fordelingsbogføringen følger niveauernes rækkefølge. For eksempel sikrer niveau, at administration først allokeres til workshop, før workshop allokeres til køretøj og produktion.|  
|Statisk allokering|Statisk allokeringer er baseret på et fast sæt værdier, for eksempel anvendt antal kvadratmeter eller et etableret fordelingsforhold såsom 5: 2: 4.|  
|Driftsomkostning|Driftsomkostninger er de tilbagevendende udgifter, der er relateret til driften af en virksomhed, en enhed og en komponent.|  
|Indirekte kostpris|Faste omkostninger vedrører løbende udgifter til drift af en virksomhed. De er alle omkostninger på resultatopgørelsen undtagen direkte arbejdskraft, direkte materialer og direkte udgifter. Faste omkostninger inkluderer regnskabsmæssige gebyrer, reklame, afskrivning, forsikring, renter, juridisk gebyrer, leje, reparationer, forsyninger, skatter, telefonregninger, rejser og forbrugsomkostninger.|  
|Variabelt omkostningstrin|Trin variable omkostninger er omkostninger, der ændrer sig dramatisk på visse punkter, fordi de involverer store køb, der ikke kan spredes over tid. For eksempel kan en medarbejder producere 100 tabeller på en måned. Medarbejderens løn er konstant over et produktionsområde på 1 til 100 tabeller. Hvis virksomheden ønsker at producere 110 tabeller, skal virksomhed bruge to medarbejdere. Dermed fordobles prisen.|  
|Fordeling|Den del, der fordeles blandt omkostningssteder eller omkostningsobjekter.|  
|Statisk vægtning|Omkostninger fordeles i henhold til fordelingsnøgler, som kan ændres ved hjælp af en multiplikator. <br />For eksempel deler to afdelinger med 20 og 10 medarbejdere kantineomkostninger. Omkostningerne fordeles mellem afdelingerne ved hjælp af en fordelingsnøgle, der repræsenterer antallet af medarbejdere, der spiser i kantinen. I den første afdeling spiser kun fem medarbejdere i kantinen, så denne afdeling har en multiplikator på 0,25. Grundlag for fordeling er 20 x 0,25 = 5. Det samlede antal medarbejdere, der spiser i kantinen er 15. En tredjedele af omkostningerne allokeres til den første afdeling, og to tredjedel af omkostningerne allokeres til den anden afdeling.|  
|Variabel omkostning|Variable omkostninger er udgifter, der ændres i forhold til en virksomheds aktivitet. Variable omkostninger er summen af marginalomkostninger over alle producerede enheder. Faste omkostninger og variable omkostninger udgør de to komponenter af samlede omkostninger.|  
|Variant|En variant bruges som en valgfri brugerdefineret etiket for tildelinger. Formålet med etiketten er at filtrere grupper af fordelinger.|  

## Se også

 [Om omkostningsregnskab](finance-about-cost-accounting.md)  
 [Regnskab for omkostninger](finance-manage-cost-accounting.md)  
 [Arbejd med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]
