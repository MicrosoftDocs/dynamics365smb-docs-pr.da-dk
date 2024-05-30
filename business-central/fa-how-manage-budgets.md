---
title: Administrere anlægsbudgetter
description: 'Du kan oprette oplysninger om fremtidige investeringer, salg og afskrivning på anlægsaktiver for at forberede budgetter og prognoser.'
author: brentholtorf
ms.topic: conceptual
ms.devlang: al
ms.search.keywords: forecast
ms.search.form: '5610, 5611'
ms.date: 04/01/2021
ms.author: bholtorf
ms.service: dynamics-365-business-central
---
# Administrere budgetter for anlægsaktiver

Du kan konfigurere budgetterede anlægsaktiver. Du kan f.eks. inkludere forventede anskaffelser og salg i rapporterne.  

Hvis du vil forberede din budgetterede resultatopgørelse, balance og kontantbudget, skal du bruge oplysninger om fremtidige investeringer, salg og afskrivning på anlægsaktiver. Du kan få disse oplysninger fra rapporten **Anlæg - forventet værdi**. Inden du udskriver rapporten, skal du have forberedt budgettet.  

## Sådan budgetteres anskaffelsesprisen for et anlægsaktiv

Når du skal forberede et budget, skal du oprette anlægskort for de anlægsaktiver, du har planlagt at købe. De budgetterede anlægsaktiver oprettes som almindelige anlægsaktiver, men de skal være angivet til ikke at blive bogført i finansregnskabet.

Når du bogfører anskaffelsesprisen, skal du angive nummeret på det budgetterede anlægsaktiv i feltet **Budgetanlægsnr.** Dermed bogføres automatisk en anskaffelsespris med modsat fortegn for budgetanlægget. Det betyder, at de samlede anskaffelsesomkostninger for budgetanlægget er forskellen mellem den budgetterede og den faktiske anskaffelsesomkostning.

1. Vælg ![Lightbulb, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **Anlægsaktiver**, og vælg derefter det relaterede link.
2. Vælg handlingen **Ny** for at oprette et nyt anlægskort for det budgetterede anlægsaktiv.
3. Markér afkrydsningsfeltet **Budgetanlæg** for at forhindre bogføring i finansregnskabet.
4. Udfyld resten af felterne, tildel en afskrivningsprofil, og bogfør derefter den første anskaffelsespris for det budgetterede anlægsaktiv, der er angivet i feltet **Budgetanlægsnr.** på kladdelinjen Du kan finde flere oplysninger i [Anskaffe anlægsaktiver](fa-how-acquire.md).

## Sådan budgetteres salget af et anlægsaktiv

Hvis du planlægger at sælge anlæg inden for budgetperioden, kan du angive oplysninger om salgspris og -dato.

1. Vælg ![Lightbulb, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **Anlægsaktiver**, og vælg derefter det relaterede link.
2. Vælg det anlægsaktiv, der skal sælges, og vælg derefter handlingen **Afskrivningsprofiler**.
3. På siden **Anlægsafskrivningsprofiler** skal du udfylde felterne **Forventet salgsdato** og **Forventet salgspris**. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

## Sådan vises forventede salgsværdier

Hvis du vil have vist de forventede salgsværdier og beregne gevinst eller tab, kan du bruge rapporten **Anlæg - forventet værdi**.

1. Vælg ![Lightbulb, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **Anlæg - forventet værdi**, og vælg derefter det relaterede link.
2. Udfyld felterne efter behov.
3. Vælg knappen **Udskriv** eller **Vis udskrift**.

## Sådan budgetteres afskrivning

Du kan bruge rapporten **Anlæg - forventet værdi** til at beregne den fremtidige afskrivning. I rapporten vises bogført værdi og akkumuleret afskrivning i starten af den valgte periode og ved ændringer i løbet af perioden, og den bogførte værdi og den akkumulerede afskrivning vises ved slutningen af den valgte periode.

1. Vælg ![Lightbulb, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **Anlæg - forventet værdi**, og vælg derefter det relaterede link.
2. Udfyld felterne efter behov.
3. Hvis du vil have vist de samlede værdier for alle aktiver, skal du rydde afkrydsningsfeltet **Udskrift pr. anlæg**.
4. Lad oversigtspanelet **Anlæg** stå tomt, hvis alle anlægsaktiver skal inkluderes. I feltet **Budgetanlæg** skal du angive **Nej** for at udelukke budgetanlæg eller **Ja** for kun at få vist budgetanlæg.
5. Vælg knappen **Udskriv** eller **Vis udskrift**.

## Se også

[Anlægsaktiver](fa-manage.md)  
[Oversigt over anlægsaktivsanalyser](fa-analytics-overview.md)   
[Opsætning af Anlægsaktiver](fa-setup.md)  
[Finans](finance.md)  
[Blive køreklar til at foretage handler](ui-get-ready-business.md)  
[Arbejd med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]
