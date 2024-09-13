---
title: Bæredygtighed ømme kort og mål
description: 'Få mere at vide om, hvordan du opsætter og bruger scorecards og mål for bæredygtighed.'
author: altotovi
ms.topic: conceptual
ms.devlang: al
ms.search.keywords: 'Sustainability, ESG, emission, GHG, CSRD, scorecard, goal, forecast, budget'
ms.search.form: null
ms.date: 08/19/2024
ms.author: altotovi
ms.service: dynamics-365-business-central
ms.reviewer: solsen
---

# Oversigt over scorekort og mål for bæredygtighed

Denne artikel indeholder vejledning i, hvordan du opretter scorekort og mål, og hvordan du opdaterer status for mål. Scorecards og mål giver organisationer mulighed for at kuratere bæredygtighedsmålinger og spore dem mod vigtige forretningsmål. Mål kan oprettes baseret på aktuelle værdier og målværdier, så brugerne kan holde styr på fremskridtene for aktuelle emissioner sammenlignet med tidligere perioder.  

## Oprette et scorecard  

Følg trinnene for at oprette et *nyt resultatkort* for bæredygtighed:

1. Vælg ![Lightbulb, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") , angiv **Scorecards** for bæredygtighed, og vælg derefter den relaterede sammenkæde. 
2. På siden Resultatkort **for** bæredygtighed skal du vælge **Ny** for at oprette et nyt scorecard.  
3. Angiv Nej **.** Og felterne **Navn** **i oversigtspanelet Generelt** og derefter tilføje **Ejer**. 

> [BEMÆRK!] I feltet **Ejer** kan du kun vælge brugere, der har valgt **feltet Bæredygtighedschef** i tabellen **Brugeropsætning** . 

## Opret mål  

Følg trinnene for at oprette et *nyt bæredygtighedsmål*:

1. Vælg ![Lightbulb, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") , angiv **Scorecards** for bæredygtighed, og vælg derefter den relaterede sammenkæde.
2.  **Vælg handlingen Mål** for at oprette et nyt **bæredygtighedsmål** for det valgte scorecard.  
3. Vælg **Ny** for at begynde at oprette et nyt mål.
4. Scorekortets **nr.** Tilføjes automatisk baseret på værdien fra det tilknyttede **Sustainability Scorecard**, og brugeren vil ikke kunne redigere dette felt. Systemet konfigurerer **også feltet Enhed** baseret på **emissionsenhedskoden** på **siden Bæredygtighedsopsætning** .  
5. Du skal udfylde **Nummer.** og **navnet på** det nye **bæredygtighedsmål**. Feltet **Ejer** udfyldes automatisk baseret på værdien fra det tilknyttede **resultatkort** for bæredygtighed.   
6. Brugere kan vælge at oprette *bæredygtighedsmål* for hele virksomheden, et bestemt land/område eller en facilitet. Hvis brugerne vil oprette et bestemt mål, skal de vælge landet eller området i **feltet Lande-/områdekode** eller faciliteten i **feltet Ansvarscenter** .  
7. Vælg felterne **Startdato** og **Slutdato** for at konfigurere en dedikeret periode til sporing af aktuelle værdier. Denne konfiguration bestemmer værdierne i følgende felter: **Aktuel værdi for CO2**, **Aktuel værdi for CH4** og **Aktuel værdi for N2O**. 
8. Vælg felterne Startdato **for oprindelig plan og** Oprindelig slutdato **for at angive en dedikeret oprindelig periode til sammenligning af** aktuelle værdier. Denne konfiguration bestemmer værdierne i følgende felter: **Referencescenarie for CO2**, **Referencescenarie for CH4** og **Referenceværdi for N2O**.
9. Brugere kan også tilføje målværdier i det valgte **enhedsfelt** for den aktuelle periode ved hjælp af følgende felter: **Målværdi for CO2**, **Målværdi for CH4** og **Målværdi for N2O**.   
10. Et af disse mål kan vælges som et **hovedmål**. Værdier fra hovedmålet bruges i rollecenteret **Bæredygtighedschef** .  

Hvis du har mange mål på siden, kan du bruge **handlingen Vis mine mål** til kun at vise dig dine mål, og hvis du vil vise alle, skal du køre handlingen **Vis alle mål** .  

> [!NOTE]
> *Bæredygtighedsmål* kan kun oprettes for et bestemt *resultatkort* for bæredygtighed, og du kan ikke oprette mål, der ikke er relateret til scorecardet, men du kan oprette flere mål for ét scorecard. Du kan kun have ét **bæredygtighedsmål** markeret som **hovedmål**.

> [!NOTE]
> Brugere kan oprette forskellige kombinationer af mål for hele virksomheden, specifikke lande eller regioner og et ansvarscenter for et *resultatkort for bæredygtighed*. Brugere kan også bruge forskellige perioder til den samme sporingsmodel. 

## Se også

[Opsætning af bæredygtighed](finance-sustainability-setup.md)    
[Diagram over bæredygtighedskonti og finans](finance-sustainability-accounts-ledger.md)    
[Sådan registrerer du bæredygtighedsposter](finance-sustainability-journal.md)    
[Ad hoc-analyse af bæredygtighedsdata](ad-hoc-analysis-sustainability.md)    
[Bæredygtighedsrapporter og -analyser i Business Central](sustainability-reports.md)   
[Bæredygtigheds-API](/dynamics365/business-central/dev-itpro/api-sustainability/sustainability-api?toc=/dynamics365/business-central/toc.json)    
[Finance](finance.md)    
[Arbejd med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)    

[!INCLUDE[footer-include](includes/footer-banner.md)]
