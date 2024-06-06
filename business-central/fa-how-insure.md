---
title: Forsikre anlægsaktiver
description: Du kan knytte et eller flere anlægsaktiver til en forsikringspolice ved at bogføre forsikringsposterne fra siden **Forsikringskladde**.
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bholtorf
ms.topic: conceptual
ms.search.keywords: 'policy, coverage'
ms.search.form: '5647, 5644, 5653, 5651, 5655, 5652, 5645, 5656, 5646, 5648, 9275'
ms.date: 05/15/2024
ms.service: dynamics-365-business-central
ms.custom: bap-template
---
# Forsikre anlægsaktiver

Brug siden **Forsikringskort** til at oprette en forsikringspolice, der dækker et eller flere anlægsaktiver. Du kan knytte ét anlægsaktiv til én forsikringspolice eller flere anlægsaktiver til én forsikringspolice.

Du kan knytte et anlægsaktiv til en forsikringspolice ved at bogføre forsikringsposterne fra siden **Forsikringskladde**.

Du kan også knytte et anlægsaktiv til en forsikringspolice og oprette forsikringsposter, når du bogfører anskaffelsesprisen. Du bogfører en anskaffelsesomkostning fra anlægskladden med forsikringsnummeret **.** udfyldt. Du skal slå til/fra-knappen **Aut. forsik** . bogføring til på siden **Anlægsopsætning** . Yderligere oplysninger finder du i [Erhverve et anlægsaktiv ved hjælp af en anlægskassekladde](fa-how-acquire.md#acquire-a-fixed-asset-by-using-a-fixed-asset-gl-journal).

 **Hvis til/fra-knappen** Aut. forsik **. bogføring på siden Anlægsopsætning** ikke er slået til, oprettes der linjer på siden Forsikringskladde ved bogføring af anskaffelser fra **anlægskladden** . Du skal bogføre linjerne manuelt.

> [!WARNING]  
> Hvis du ikke slår Aut. forsik. bogføring **til** på **siden Anlægsopsætning**, bør forsikringskladden være baseret på en kladdetype uden en nummerserie. Det skyldes, at de indsatte dokumentnumre fra anlægskladdelinjen ellers er i konflikt med nummerserien for forsikringskladden. Du kan finde flere oplysninger om kladdetyper og -kørsler i [Angive generelle oplysninger om anlægsaktiver](fa-how-setup-general.md).

Når du har knyttet et anlægsaktiv til en forsikringspolice, står **·**  der **Ja i feltet Forsikret** på anlægskortet. Når du sælger anlægsaktivet, deaktiveres til/fra-knappen automatisk.

## Sådan oprettes og redigeres et forsikringskort

Når du får oplysninger om ændringer i forsikringsbeløbet, kan du angive de nye oplysninger på siden **Forsikringskort** for at sikre dig, at du analyserer forsikringsposterne korrekt.  

1. Vælg ![Lightbulb, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **Forsikring**, og vælg derefter det relaterede link.
2. Vælge handlingen **By** for at oprette et nyt kort til en forsikringspolice. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
3. Du kan også vælge den forsikringspolice, du vil ændre, og derefter vælge handlingen **Rediger**.

## Sådan tildeles et anlægsaktiv til en forsikringspolice ved at bogføre forsikringskladden

Du tildeler et anlægsaktiv til en forsikringspolice ved at bogføre det til forsikringsposten.  

Følgende procedure beskriver, hvordan du kan oprette en forsikringskladdelinje manuelt. Hvis til/fra-knappen **Aut. forsik. bogføring** er slået til **på siden Anlægsopsætning**, oprettes der automatisk forsikringskladdelinjer, når du bogfører anskaffelser. I så fald skal du blot bogføre kladden.  

1. Vælg ![Lightbulb, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **Forsikringskladder**, og vælg derefter det relaterede link.  
2. Åbn den relevante kladde, og udfyld kladdelinjerne efter behov.  
3. Du kan tildele flere anlægsaktiver til én forsikringspolice ved at oprette kladdelinjer med samme værdi i feltet **Forsikringsnr.** og forskellige værdier i feltet **Anlægsnr.**  
4. Vælg handlingen **Bogfør**.  

    > [!NOTE]  
    > Posterne fra en forsikringskladde bogføres kun til forsikringsposterne.  

## Sådan opdateres forsikringsværdien af et anlægsaktiv

Du kan bruge kørslen **Indekser forsikring** til at opdatere værdien af de anlægsaktiver, der er dækket af forsikringen.  

1. Vælg ![Lightbulb, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **Indekser forsikring**, og vælg derefter det relaterede link.
2. Udfyld felterne efter behov.

    > [!NOTE]  
    >   I feltet **Indekstal** kan du f.eks. angive en reduktion på 5 % som 95, mens du angiver en stigning på 2 % som 102.  
3. Vælg knappen **OK**.  

   Ved kørslen beregnes det nye beløb som en procent af den samlede forsikringsværdi ifølge siden **Forsikringsstatistik**, og derefter oprettes der en linje i forsikringskladden.  
4. Vælg ![Lightbulb, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **Forsikringskladder**, og vælg derefter det relaterede link.  
5. Åbn den relevante forsikringskladde, gennemse de oprettede værdier, og bogfør dem til forsikringsposterne.  

## Sådan overvåges forsikringsdækning

[!INCLUDE[prod_short](includes/prod_short.md)] indeholder dedikerede rapporter og statistiksider, så du kan analysere forsikringspolicerne og om anlægsaktiverne er over- eller underforsikrede.  

### Oversigt over forsikringspolicer

Hvis du vil have et overblik over dine forsikringspolicer, skal du åbne en eksempelvisning af rapporten **Forsikring - stamoplysninger** eller udskrive rapporten. Rapporten indeholder alle policer og de vigtigste felter fra forsikringskortene.  

### Forsikringsdækning

Hvis du vil have vist, hvilke forsikringspolicer der dækker det enkelte anlægsaktiv og med hvilket beløb, kan du få vist eller udskrive rapporten **Forsikring - forsikret i alt**.  

#### Over/underforsikring

Du kan kontrollere, om anlægsaktiverne er over- eller underforsikrede på følgende måder:  

* Siden **Forsikringsstatistik**. Et positivt beløb i feltet **Over/underforsikret** betyder, at anlægsaktivet er overforsikret. Et negativt beløb betyder, at aktivet er underforsikret.  
* Siden **Anlægsstatistik**. Vælg feltet **Forsikret i alt** for at få vist siden **Forsikringsposter**.  
* Rapporten **Over/underforsikring**.  
* Rapporten **Forsikringsanalyse**.  

### Ikke-forsikrede anlægsaktiver

Hvis du vil kontrollere, om du har glemt at knytte et anlægsaktiv til en forsikringspolice, kan du udskrive eller få vist rapporten **Forsikring - ikke-fors. anlæg** . Denne rapport viser anlægsaktiver, som ikke bogfører beløb for til forsikringsposterne.  

## Sådan får du vist forsikringsposter

Du kan få vist de forsikringsposter, du har oprettet.  

1. Vælg ikonet ![Lightbulb, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **Forsikring**, og vælg derefter det relaterede link.  
2. Vælg den relevante forsikringspolice, og vælg derefter handlingen **Forsikringsposter**.  

## Sådan får du vist den samlede forsikringsværdi for anlægsaktiver

En matrixside viser de forsikringsværdier, der er registreret for hver forsikringspolice for hvert anlægsaktiv, og som stammer fra bogførte forsikringsrelaterede beløb.  

1. Vælg ikonet ![Lightbulb, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **Forsikring**, og vælg derefter det relaterede link.  
2. Vælg den relevante forsikringspolice, og vælg derefter handlingen **Forsikringssummer pr. anlæg**.  
3. Udfyld felterne efter behov.  
4. Vælg handlingen **Vis matrix**.  
5. Hvis du vil se de underliggende forsikringsposter, skal du vælge en værdi i matrixen.  

## Sådan rettes forsikringsposter

Hvis et anlægsaktiv er knyttet til en forkert forsikringspolice, kan du rette det ved at oprette to omposteringsposter fra forsikringskladden.  

1. Vælg ![Lightbulb, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **Forsikringskladder**, og vælg derefter det relaterede link.  
2. Opret en kladdelinje for anlægsaktivet og den korrekte forsikringspolice, hvor værdien i feltet **Beløb** er positivt.  
3. Opret en anden kladdelinje for anlægsaktivet og den forkerte forsikringspolice, hvor værdien i feltet **Beløb** er negativt.  
4. Vælg handlingen **Bogfør**.  

Anlægsaktivet fjernes fra den forkerte forsikringspolice på anden linje. Aktivet knyttes til den korrekte forsikringspolice på første linje i kladden.  

## Se også

[Anlægsaktiver](fa-manage.md)  
[Opsætning af Anlægsaktiver](fa-setup.md)  
[Finans](finance.md)  
[Arbejd med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]