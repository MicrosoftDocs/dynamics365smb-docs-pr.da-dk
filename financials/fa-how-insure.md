---
title: "Forsikring af anlægsaktiver | Microsoft Docs"
Description: You can assign a fixed asset to an insurance policy, which is represented by an insurance card.
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: policy, coverage
ms.date: 06/02/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: bec0619be0a65e3625759e13d2866ac615d7513c
ms.openlocfilehash: d5f3ef437e19ec037dc8f81aac6a8d283fc251a5
ms.contentlocale: da-dk
ms.lasthandoff: 03/22/2018

---
# <a name="insure-fixed-assets"></a>Forsikring af anlægsaktiver
En forsikringspolice for et anlægsaktiv repræsenteres af et forsikringskort. Du kan knytte et anlægsaktiv til en forsikringspolice eller flere anlægsaktiver til en forsikringspolice.

Du kan knytte et anlægsaktiv til en forsikringspolice ved at bogføre forsikringsposterne fra vinduet **Forsikringskladde**.

Du kan også knytte et anlægsaktiv til en forsikringspolice og oprette forsikringsposter, når du bogfører anskaffelsesprisen. Dette gøres ved at bogføre en anskaffelsespris fra anlægskladden, hvor feltet **Forsikringsnr.** er udfyldt. Afkrydsningsfeltet **Aut. forsikr.bogføring** i vinduet **Anlægsopsætning** skal være markeret. Du kan finde flere oplysninger i afsnittet "Sådan bogføres anskaffelse af et anlægsaktiv manuelt med anlægskassekladden" i [Anskaffe anlægsaktiver](fa-how-acquire.md).

Hvis afkrydsningsfeltet **Aut. forsikr.bogføring** i vinduet **Anlægsopsætning** ikke er markeret, vil bogføring af anskaffelser fra anlægskladden oprette linjer i vinduet **Forsikringskladde**, som du derefter skal bogføre manuelt.

> [!WARNING]  
>   Hvis du ikke markerer afkrydsningsfeltet **Aut. forsikr.bogføring** i vinduet **Anlægsopsætning**, skal din forsikringskladde være baseret på en kladdetype uden en nummerserie. Det skyldes, at de indsatte dokumentnumre fra anlægskladdelinjen ellers er i konflikt med nummerserien for forsikringskladden. Du kan finde flere oplysninger om kladdetyper og -kørsler i [Angive generelle oplysninger om anlægsaktiver](fa-how-setup-general.md).

Når du har tildelt et anlægsaktiv til en forsikringspolice, er afkrydsningsfeltet **Forsikret** markeret på anlægskortet. Når du sælger anlægsaktivet, fjernes markeringen i afkrydsningsfeltet automatisk.

## <a name="to-create-or-modify-an-insurance-card"></a>Sådan oprettes og redigeres et forsikringskort
En forsikringspolice for et anlægsaktiv skal være repræsenteret af et forsikringskort.

Når du får oplysninger om ændringer i forsikringsbeløbet, skal du angive de nye oplysninger i vinduet **Forsikringskort** for at sikre dig, at du analyserer forsikringsposterne korrekt.  

1. Vælg ikonet ![Søg efter side eller rapport](media/ui-search/search_small.png "Ikonet Søg efter side eller rapport"), angiv **Forsikring**, og vælg derefter det relaterede link.
2. Vælge handlingen **By** for at oprette et nyt kort til en forsikringspolice. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
3. Du kan også vælge den forsikringspolice, du vil ændre, og derefter vælge handlingen **Rediger**.

## <a name="to-assign-a-fixed-asset-to-an-insurance-policy-by-posting-from-the-insurance-journal"></a>Sådan tildeles et anlægsaktiv til en forsikringspolice ved at bogføre forsikringskladden
Du tildeler et anlægsaktiv til en forsikringspolice ved at bogføre det til forsikringsposten.  

Følgende procedure beskriver, hvordan du kan oprette en forsikringskladdelinje manuelt. Hvis afkrydsningsfeltet **Aut. forsikr.bogføring** er markeret i vinduet **Anlægsopsætning**, oprettes forsikringskladdelinjerne automatisk, når du bogfører anskaffelsespriserne. I så fald skal du blot bogføre kladden.  

1. Vælg ikonet ![Søg efter side eller rapport](media/ui-search/search_small.png "Ikonet Søg efter side eller rapport"), angiv **Forsikringskladder**, og vælg derefter det relaterede link.  
2. Åbn den relevante kladde, og udfyld kladdelinjerne efter behov.  
3. Du kan tildele flere anlægsaktiver til én forsikringspolice ved at oprette kladdelinjer med samme værdi i feltet **Forsikringsnr.** og forskellige værdier i feltet **Anlægsnr.**  
4. Vælg handlingen **Bogfør**.  

    > [!NOTE]  
>   Posterne fra en forsikringskladde bogføres kun til forsikringsposterne.  

## <a name="to-update-the-insurance-value-of-a-fixed-asset"></a>Sådan opdateres forsikringsværdien af et anlægsaktiv
Du kan bruge kørslen **Indekser forsikring** til at opdatere værdien af de anlægsaktiver, der er dækket af forsikringen.  

1. Vælg ikonet ![Søg efter side eller rapport](media/ui-search/search_small.png "Ikonet Søg efter side eller rapport"), angiv **Indekser forsikring**, og vælg derefter det relaterede link.
2. Udfyld felterne efter behov.

    > [!NOTE]  
>   I feltet **Indekstal** kan du f.eks. angive en reduktion på 5 % som 95, mens du angiver en stigning på 2 % som 102.  
3. Vælg knappen **OK**.  

   Ved kørslen beregnes det nye beløb som en procent af den samlede forsikringsværdi ifølge vinduet **Forsikringsstatistik**, og derefter oprettes der en linje i forsikringskladden.  
4. Vælg ikonet ![Søg efter side eller rapport](media/ui-search/search_small.png "Ikonet Søg efter side eller rapport"), angiv **Forsikringskladder**, og vælg derefter det relaterede link.  
5. Åbn den relevante forsikringskladde, gennemse de oprettede værdier, og bogfør dem til forsikringsposterne.  

## <a name="to-monitor-insurance-coverage"></a>Sådan overvåges forsikringsdækning
[!INCLUDE[d365fin](includes/d365fin_md.md)] indeholder dedikerede rapporter og statistikvinduer, så du kan analysere forsikringspolicerne og om anlægsaktiverne er over- eller underforsikrede.  

### <a name="overview-of-insurance-policies"></a>Oversigt over forsikringspolicer
Hvis du vil have et overblik over dine forsikringspolicer, skal du åbne en eksempelvisning af rapporten **Forsikring - stamoplysninger** eller udskrive rapporten. Rapporten indeholder alle policer og de vigtigste felter fra forsikringskortene.  

### <a name="insurance-coverage"></a>Forsikringsposter
Hvis du vil have vist, hvilke forsikringspolicer der dækker det enkelte anlægsaktiv og med hvilket beløb, kan du få vist eller udskrive rapporten **Forsikring - forsikret i alt**.  

### <a name="overunder-coverage"></a>Over/underforsikring
Du kan kontrollere, om anlægsaktiver er over- eller underforsikrede på følgende måder:  

* Vinduet **Forsikringsstatistik**. Et positivt beløb i feltet **Over/underforsikret** betyder, at anlægsaktivet er overforsikret. Et negativt beløb betyder, at det er underforsikret.  
* Vinduet **Anlægsstatistik**. Vælg feltet **Forsikret i alt** for at få vist vinduet **Forsikringsposter**.  
* Rapporten **Over/underforsikring**.  
* Rapporten **Forsikringsanalyse**.  

### <a name="uninsured-fixed-assets"></a>Ikke-forsikrede anlægsaktiver
Hvis du vil kontrollere, om du har glemt at knytte et anlægsaktiv til en forsikringspolice, kan du udskrive eller se rapporten **Forsikring - ikke-fors. anlæg**. Rapporten viser de anlægsaktiver, hvor ingen beløb er bogført til forsikringsposten.  

## <a name="to-view-insurance-coverage-ledger-entries"></a>Sådan får du vist forsikringsposter
Du kan få vist de forsikringsposter, du har oprettet i forsikringsposterne.  

1. Vælg ikonet ![Søg efter side eller rapport](media/ui-search/search_small.png "Ikonet Søg efter side eller rapport"), angiv **Forsikring**, og vælg derefter det relaterede link.  
2. Vælg den relevante forsikringspolice, og vælg derefter handlingen **Forsikringsposter**.  

## <a name="to-view-the-total-insurance-value-of-fixed-assets"></a>Sådan får du vist den samlede forsikringsværdi for anlægsaktiver
Et dedikeret matrixvindue viser de forsikringsværdier, der er registreret for hver forsikringspolice for de enkelt anlægsaktiver, som resultat af de forsikringsrelaterede beløb, du har bogført.  

1. Vælg ikonet ![Søg efter side eller rapport](media/ui-search/search_small.png "Ikonet Søg efter side eller rapport"), angiv **Forsikring**, og vælg derefter det relaterede link.  
2. Vælg den relevante forsikringspolice, og vælg derefter handlingen **Forsikringssummer pr. anlæg**.  
3. Udfyld felterne efter behov.  
4. Vælg handlingen **Vis matrix**.  
5. Hvis du vil se de underliggende forsikringsposter, skal du vælge en værdi i matrixen.  

## <a name="to-correct-insurance-coverage-entries"></a>Sådan rettes forsikringsposter
Hvis et anlægsaktiv er knyttet til den forkerte forsikringspolice, kan du rette det ved at oprette to omposteringsposterne fra forsikringskladden.  

1. Vælg ikonet ![Søg efter side eller rapport](media/ui-search/search_small.png "Ikonet Søg efter side eller rapport"), angiv **Forsikringskladder**, og vælg derefter det relaterede link.  
2. Opret en kladdelinje for anlægsaktivet og den korrekte forsikringspolice, hvor værdien i feltet **Beløb** er positivt.  
3. Opret en anden kladdelinje for anlægsaktivet og den forkerte forsikringspolice, hvor værdien i feltet **Beløb** er negativt.  
4. Vælg handlingen **Bogfør**.  

Anlægsaktivet vil blive skilt fra den forkerte forsikringspolice på den anden linje og knyttet til den rette forsikringspolice på den første linje.  

## <a name="see-also"></a>Se også
[Anlægsaktiver](fa-manage.md)  
[Opsætning af anlægsaktiver](fa-setup.md)  
[Finans](finance.md)  
[Arbejde med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)  

