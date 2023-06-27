---
title: Ændre det årlige beløb på servicekontrakter eller kontrakttilbud
description: 'Du kan ændre det beløb, der vil blive faktureret pr. år på servicekontrakter eller servicekontrakttilbud.'
author: brentholtorf
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: null
ms.date: 04/01/2021
ms.author: bholtorf
---
# <a name="change-the-annual-amount-on-service-contracts-or-contract-quotes" />Ændre det årlige beløb på servicekontrakter eller kontrakttilbud
Du kan ændre det årlige beløb på en servicekontrakt eller et kontrakttilbud til det korrekte beløb, der faktureres årligt.  

## <a name="to-change-the-annual-amount-of-the-service-contract-or-contract-quote" />Sådan ændres det årlige beløb på en servicekontrakt eller et kontrakttilbud

1. Vælg ![Lightbulb, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **Servicekontrakter** eller **Servicekontrakttilbud**, og vælg derefter det relaterede link.  
2. Vælg kontrakten eller kontrakttilbuddet.  
3. Vælg handlingen **Åbn kontrakt** for at åbne kontrakten eller kontrakttilbuddet til redigering.  
4. Marker afkrydsningsfeltet **Tillad beløb, der ikke stemmer**, hvis du vil ændre det årlige beløb og fordele differencen i det årlige beløb manuelt på kontraktlinjerne. Ellers skal du fjerne markeringen i afkrydsningsfeltet for automatisk at fordele differencen i det årlige beløb på kontraktlinjerne, når du har ændret det årlige beløb.  
5. Rediger indholdet i feltet **Årligt beløb**. Du kan ikke underskrive, dvs. konvertere til en servicekontrakt, hvis du arbejder på et kontrakttilbud, eller låse en servicekontrakt, hvis det årlige beløb er negativt. Hvis det årlige beløb angives til nul, skal indholdet af feltet **Faktureringsperiode** angives til **Ingen** ved underskrivning eller låsning af servicekontrakten.  
6. Afhængigt af om afkrydsningsfeltet **Tillad beløb, der ikke stemmer** er markeret, skal du køre enten manuel eller automatisk fordeling af den årlige beløbsdifference. Kontraktlinjerne bliver opdateret, så feltværdien **Årligt. Årlige beløb** er lig med det nye årlige beløb.  

## <a name="distributing-differences-between-new-and-calculated-annual-amounts" />Distribuere forskelle mellem nye og beregnede årlige beløb
Hvis du ændrer det årlige beløb i en servicekontrakt eller et kontrakttilbud, skal du evt. fordele differencen mellem det nye og det beregnede årlige beløb på kontraktlinjerne. Der er tre måder at fordele beløb på:

* Ligelig fordeling  
* Fordeling baseret på linjebeløb  
* Fordeling baseret på avance

### <a name="even-distribution" />Ligelig fordeling
Hvis du ændrer det årlige beløb i servicekontrakten eller kontrakttilbuddet, kan du blive nødt til at fordele differencen mellem det nye og det beregnede årlige beløb på kontraktlinjerne. Ligelig fordeling er en af de automatiske fordelingsmetoder, som kan hjælpe med at fordele differencen mellem det nye og det beregnede beløb ligeligt mellem linjebeløbene på kontraktlinjerne. Følgende procedure beskriver hovedidéen bag denne metode:  

1. Differencen mellem de nye værdier i felterne **Årligt beløb** og **Beregnet årligt beløb** divideres med antallet af kontraktlinjer i servicekontrakten eller kontrakttilbuddet.  
2. Værdien i feltet **Linjebeløb** opdateres ved at lægge resultatet af den tidligere handling til.  
3. Indholdet i felterne **Linjerabatbeløb**, **Linjerabatpct.** og **Avance** opdateres i forhold til den nye værdi i feltet **Linjebeløb** på følgende måde:   
    * Linjerabatbeløb = Linjeværdi - Linjebeløb.  
    * Linjerabatpct. = Linjerabatbeløb / Linjeværdi * 100.  
    * Avance = Linjebeløb - Linjekostpris  

 Trinnene gentages for hver kontraktlinje.  

#### <a name="example" />Eksempel
Afkrydsningsfeltet **Tillad beløb, der ikke stemmer** er ikke markeret i den servicekontrakt, der indeholder tre kontraktlinjer med følgende oplysninger.  

|Vare|Linjekostpris|Linjeværdi|Linjerabatpct.|Linjerabatbeløb|Linjebeløb|Avance|  
|----------|---------------|----------------|---------------------|--------------------------|-----------------|------------|  
|Vare 1|30,00|40,00|0.00|0.00|40,00|10,00|  
|Vare 2|40,00|50.00|10,00|5.00|45.00|5.00|  
|Vare 3|50.00|70.00|10,00|7.00|63.00|13.00|  

Værdien i feltet **Årligt beløb** svarer til indholdet i feltet **Beregnet årligt beløb**, som altid er angivet til summen af linjebeløbene. I dette tilfælde er det lig med følgende: 40 + 45 + 63 = 148.  

Hvis du ændrer **Årligt beløb** til 139, beregnes beløbet, der skal føjes til værdien i feltet **Linjebeløb**. Denne beløb beregnes ved at fratrække **Beregnet årligt beløb** fra den nye feltværdi **Årligt beløb** og dividere resultatet med antallet af kontraktlinjer i servicekontrakten. I dette tilfælde er det lig med følgende: (139 - 148) / 3 = -3. Derefter føjes det sidst beregnede tal til hver **Linjebeløb**-feltværdi, og feltværdierne **Linjerabatpct.**, **Linjerabatbeløb** og **Avance** opdateres ved hjælp af formlerne i den procedure, der er beskrevet ovenfor.  

Kontraktlinjerne indeholder derefter følgende data.  

|Vare|Linjekostpris|Linjeværdi|Linjerabatpct.|Linjerabatbeløb|Linjebeløb|Avance|  
|----------|---------------|----------------|---------------------|--------------------------|-----------------|------------|  
|Vare 1|30,00|40,00|7.50|3.00|37.00|7.00|  
|Vare 2|40,00|50.00|16.00|8.00|42.00|2.00|  
|Vare 3|50.00|70.00|14.29|10.00|60.00|10.00|  

### <a name="distribution-based-on-line-amount" />Fordeling baseret på linjebeløb
Hvis du ændrer det årlige beløb i servicekontrakten eller kontrakttilbuddet, kan du blive nødt til at fordele differencen mellem det nye og det beregnede årlige beløb på kontraktlinjerne. Fordeling baseret på linjebeløb er en automatisk metode, som kan hjælpe med at fordele differencen mellem det nye og det beregnede beløb mellem linjebeløbene på kontraktlinjerne. Fordelingen foretages proportionalt i forhold til andelene af linjebeløbet i det beregnede årlige beløb. Følgende procedure for fordeling for hver kontraktlinje beskriver hovedidéen bag denne metode:  

1. Andelen af linjebeløbprocenten beregnes på følgende måde: Indholdet af feltet **Linjebeløb** divideres med værdierne i feltet **Beregnet årligt beløb** på alle kontraktlinjerne.  
2. Feltet **Linjebeløb** opdateres ved at lægge differencen mellem de nye og de beregnede årlige beløb ganget med den procentvise andel af linjebeløb til feltets værdi.  
3. Indholdet i felterne **Linjerabatbeløb**, **Linjerabatpct.** og **Avance** opdateres i forhold til den nye værdi i feltet **Linjerabatbeløb** på følgende måde:  

    * Linjerabatbeløb = Linjeværdi - Linjebeløb.  
    * Linjerabatprocent = Linjerabatbeløb/Linjeværdi * 100.  
    * Avance = Linjebeløb - Linjekostpris  

Trinnene gentages for hver kontraktlinje.  

#### <a name="example-1" />Eksempel
Afkrydsningsfeltet **Tillad beløb, der ikke stemmer** er ikke markeret i den servicekontrakt, der indeholder tre kontraktlinjer med følgende oplysninger.  

|Vare|Linjekostpris|Linjeværdi|Linjerabatpct.|Linjerabatbeløb|Linjebeløb|Avance|  
|----------|---------------|----------------|---------------------|--------------------------|-----------------|------------|  
|Vare 1|15.00|17.00|3.00|0.51|25.00|1.49|  
|Vare 2|20,00|23.00|Ingen|0.00|55.10|3.00|  
|Vare 3|24.00|27.00|3.00|0.81|112.70|2.19|  

Værdien i feltet **Årligt beløb** svarer til indholdet i feltet **Beregnet årligt beløb**, som altid er angivet til summen af linjebeløbene. I dette tilfælde er det lig med følgende: 16,49 + 23,00 + 26,19 = 65,68.  

Hvis du ændrer **Årligt beløb** til 60, beregnes avanceprocentandelen for hver kontraktlinje:  

* Vare 1-5/(5 + 5,1 +12,7) = 0,2193 %  
* Vare 2 – 5,1/(5 + 5,1 + 12,7) = 0,2237  
* Vare 3-12,7/(5 + 5,1 + 12,7) = 0,557  

Feltværdien **Linjebeløb** opdateres på hver kontraktlinje ved brug af følgende formel: Linjebeløb = linjebeløb + differencen mellem de nye og de beregnede årlige beløb * den procentvise andel. Derefter opdateres feltværdierne **Linjerabatbeløb**, **Linjerabatpct.** og **Avance** ved hjælp af formlerne, der er beskrevet i fremgangsmåden ovenfor.  

Kontraktlinjerne indeholder derefter følgende data.  

|Vare|Linjekostpris|Linjeværdi|Linjerabatpct.|Linjerabatbeløb|Linjebeløb|Avance|  
|----------|---------------|----------------|---------------------|--------------------------|-----------------|------------|  
|Vare 1|15.00|17.00|11.41|1.94|15.06|0.06|  
|Vare 2|20,00|23.00|8.65|1.99|21.01|1.01|  
|Vare 3|24.00|27.00|11.37|3.07|23.93|-0,07|  

### <a name="distribution-based-on-profit" />Fordeling baseret på avance
Hvis du ændrer det årlige beløb i servicekontrakten eller kontrakttilbuddet, kan du blive nødt til at fordele differencen mellem det nye og det beregnede årlige beløb på kontraktlinjerne. Fordeling baseret på avance er en af de automatiske fordelingsmetoder, som kan hjælpe med at fordele differencen mellem det nye og det beregnede beløb mellem linjebeløbene på kontraktlinjerne. Fordelingen foretages proportionelt i forhold til avanceandelene i den samlede avance i kontrakten eller kontrakttilbuddet. Følgende procedure for fordeling for hver kontraktlinje beskriver hovedidéen bag denne metode:  

1. Andelen af avanceprocenten beregnes på følgende måde: Indholdet af feltet **Avance** divideres med summen af værdierne i feltet **Avance** for alle kontraktlinjerne.  
2. Feltet **Linjebeløb** opdateres ved at lægge differencen mellem de nye og de beregnede årlige beløb ganget med andelen af avanceprocenten til feltets værdi.  
3. Indholdet i felterne Linjerabatbeløb, Linjerabatpct. og Avance opdateres i forhold til den nye værdi i feltet **Linjebeløb** på følgende måde:  

    * Linjerabatbeløb = Linjeværdi - Linjebeløb.  
    * Linjerabatprocent = Linjerabatbeløb/Linjeværdi * 100.  
    * Avance = Linjebeløb - Linjekostpris  

#### <a name="example-2" />Eksempel
Afkrydsningsfeltet **Tillad beløb, der ikke stemmer** er ikke markeret i den servicekontrakt, der indeholder tre kontraktlinjer med følgende oplysninger.  

|Vare|Linjekostpris|Linjeværdi|Linjerabatpct.|Linjerabatbeløb|Linjebeløb|Avance|  
|----------|---------------|----------------|---------------------|--------------------------|-----------------|------------|  
|Vare 1|20,00|25.00|0.00|0.00|25.00|5.00|  
|Vare 2|50.00|58.00|5.00|2.90|55.10|5.10|  
|Vare 3|100.00|115.00|2.00|2.30|112.70|12.70|  

Værdien i feltet **Årligt beløb** svarer til indholdet i feltet **Beregnet årligt beløb**, som altid er angivet til summen af linjebeløbene. I dette tilfælde er det lig med følgende: 25,00 + 55,10 + 112,70 = 192,80.  

 Hvis du ændrer **Årligt beløb** til 180, beregnes avanceprocentandelen for hver kontraktlinje:  

* Vare 1 – 5/(5 + 5,1 +1 2,7) = 0,2193 %  
* Vare 2 – 5,1/(5 + 5,1 + 12,7) = 0,2237  
* Vare 3-12,7/(5 + 5,1 + 12,7) = 0,557  

Feltværdien **Linjebeløb** opdateres på hver kontraktlinje ved brug af følgende formel: Linjebeløb = linjebeløb + differencen mellem de nye og de beregnede årlige beløb * den procentvise andel. Derefter opdateres feltværdierne **Linjerabatbeløb**, **Linjerabatpct.** og **Avance** ved hjælp af formlerne i trin 3 i fremgangsmåden ovenfor.  

Kontraktlinjerne indeholder derefter følgende data.  

|Vare|Linjekostpris|Linjeværdi|Linjerabatpct.|Linjerabatbeløb|Linjebeløb|Avance|  
|----------|---------------|----------------|---------------------|--------------------------|-----------------|------------|  
|Vare 1|20,00|25.00|11.24|2.81|22.19|2.19|  
|Vare 2|50.00|58.00|9.93|5.76|52.24|2.24|  
|Vare 3|100.00|115.00|8.20|9.43|105.57|5.57|  

## <a name="see-also" />Se også
[Oprette servicekontrakter og servicekontrakttilbud](service-how-to-create-service-contracts-and-service-contract-quotes.md)  
[Konfigurere Service](service-setup-service.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
