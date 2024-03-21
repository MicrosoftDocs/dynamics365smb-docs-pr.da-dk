---
title: Konfigurere anlægsforsikring
description: 'Når du vil administrere forsikringsdækning for anlægsaktiver, skal du konfigurere et forsikringskort og nogle generelle forsikringsoplysninger pr. police.'
author: brentholtorf
ms.topic: conceptual
ms.devlang: al
ms.search.keywords: 'policy, coverage'
ms.search.form: '5607, 5648, 5644, 5651'
ms.date: 04/01/2021
ms.author: bholtorf
ms.service: dynamics-365-business-central
---
# Definere anlægsforsikring

Hvis du vil administrere forsikringsdækning for anlægsaktiver, skal du først angive nogle generelle forsikringsoplysninger og forsikringskort pr. police.

## Sådan angives generelle forsikringsoplysninger

Du skal angive nogle generelle forsikringsoplysninger for at bruge forsikringsfunktionerne i [!INCLUDE[prod_short](includes/prod_short.md)].  

1. Vælg ![Lightbulb, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **Anlægsaktiver**, og vælg derefter det relaterede link.  
2. Udfyld felterne efter behov. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]  

## Sådan defineres forsikringstyper

Du kan gruppere forsikringspolicer i kategorier, som f.eks. forsikring mod tyveri eller brand. Forsikringstyperne bruges på forsikringskortet.

1. Vælg ![Lightbulb, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **Forsikringstyper**, og vælg derefter det relaterede link.  
2. Udfyld felterne efter behov.

## Sådan defineres forsikringskort

Du kan samle oplysninger om hver enkelt forsikringspolice på forsikringskortet.  

1. Vælg ![Lightbulb, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **Forsikring**, og vælg derefter det relaterede link.  
2. På siden **Forsikring** skal du vælge handlingen **Ny** for at oprette et forsikringskort.  
3. Udfyld felterne efter behov.

## Sådan defineres forsikringskladdetyper

Første gang du åbner siden **Forsikringskladde** i [!INCLUDE[prod_short](includes/prod_short.md)], oprettes der automatisk en forsikringskladdetype, men du kan oprette flere kladdetyper. Du kan finde flere oplysninger i [Arbejde med finanskladder](ui-work-general-journals.md).  

1. Vælg ![Lightbulb, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **Forsikringskladdetyper**, og vælg derefter det relaterede link.  
2. Udfyld felterne efter behov.

## Sådan defineres forsikringskladdenavne

Du kan definere navne i en forsikringskladdetype. Værdierne i kladdenavnet bruges som standardværdier, hvis felterne ikke er udfyldt på kladdelinjerne. Du kan finde flere oplysninger i [Arbejde med finanskladder](ui-work-general-journals.md).  

1. Vælg ![Lightbulb, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **Forsikringskladdetyper**, og vælg derefter det relaterede link.  
2. Markér en forsikringskladdetype, og vælg derefter handlingen **Navne**.
3. På siden **Forsikringskladdenavne** skal du udfylde felterne efter behov.

> [!NOTE]  
>   Tallene har en særlig funktion i kladdenavne. Hvis et kladdetypenavn eller et kladdenavn indeholder et tal, vil tallet automatisk forøges med 1, hver gang kladden bogføres. Hvis du f.eks. angiver HH1 i feltet **Navn**, ændres kladdenavnet til HH2, når kladden HH1 er blevet bogført.

## Se også

[Opsætning af Anlægsaktiver](fa-setup.md)  
[Anlægsaktiver](fa-manage.md)  
[Finans](finance.md)  
[Blive køreklar](ui-get-ready-business.md)  
[Arbejd med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]
