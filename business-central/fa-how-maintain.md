---
title: Vedligeholde anlægsaktiver
description: Registrere vedligeholdelser og service på et anlægsaktiv for at bevare dets værdi.
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bholtorf
ms.topic: conceptual
ms.search.keywords: 'repair, service'
ms.search.form: '5642, 5625'
ms.date: 05/22/2024
ms.service: dynamics-365-business-central
ms.custom: bap-template
---
# Vedligeholde anlægsaktiver

Reparationsomkostninger er driftsudgifter til de ting, du gør for at bevare anlægsaktivernes tilstand. I modsætning til kapitalforbedringer øger vedligeholdelse ikke værdien af dine aktiver.

Hver gang du sender et anlægsaktiv til service, registrerer du alle relevante oplysninger som f.eks. servicedato, kreditoren, som udførte arbejdet, samt reparatørens telefonnummer. Du angiver vedligeholdelsesoplysninger på flere sider:

* Anlægskort
* Købsordre
* Købsfaktura
* Anlægskassekladde

Indeksering anvendes til at justere for ændringer af det generelle prisniveau. Brug handlingen **Indeksér anlæg** til at genberegne vedligeholdelsesomkostningerne.

## Registrer et vedligeholdelsesarbejde direkte på et anlægsaktiv

Hver gang en vedligeholdelse udføres for et aktiv, f.eks. et servicebesøg, kan du registrere det for det pågældende anlægsaktiv på siden **Vedligeholdelsesregistreringer**.  

1. Vælg det ![lyspæreikon, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **Anlægsaktiver**, og vælg derefter det relaterede link.  
2. Vælg det anlægsaktiv, du vil registrere vedligeholdelse for, og vælg derefter handlingen **Reparationsregistrering**.
3. På siden **Reparationsregistrering** skal du udfylde felterne efter behov. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]  

## Bogfør vedligeholdelsesomkostninger fra en anlægskassekladde

1. Vælg ![Lightbulb, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **Afskrivningsprofiloversigt**, og vælg derefter det relaterede link.  
2. Vælg den afskrivningsprofil, der er tildelt anlægsaktivet, og vælg derefter handlingen **Rediger**.
3. På siden **Afskrivningsprofilkort** skal du kontrollere, at afkrydsningsfeltet **Vedligeholdelse** ikke er markeret, så du ikke bogfører vedligeholdelsesomkostninger i finansposterne.
4. Vælg det ![lyspæreikon, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **Anlægsfinanskladder**, og vælg derefter det relaterede link.  
5. Opret en første kladdelinje, og udfyld felterne efter behov.
6. I feltet **Anlægsbogføringstype** skal du vælge **Reparation**.
7. Vælg handlingen **Indsæt anlægsmodkonto**. Der oprettes en anden kladdelinje til den modkonto, der er oprettet til bogføring af vedligeholdelse.

    > [!NOTE]  
    > Trin 7 fungerer kun, hvis du har angivet følgende: På siden **Anlægsbogføringsgruppekort** for bogføringsgruppen for anlægsaktivet indeholder feltet **Reparationskonto** finansdebetkontoen og feltet **Reparationsmodkonto** indeholder den finanskonto, hvor du vil bogføre modposter for opskrivning. Du kan finde flere oplysninger i [Sådan oprettes anlægsbogføringsgrupper](fa-how-setup-general.md#to-set-up-fixed-asset-posting-groups).
8. Vælg handlingen **Bogfør**.

## Registrere vedligeholdelsesomkostninger fra en købsfaktura

I det følgende beskrives, hvordan du registrerer vedligeholdelsesomkostninger for et anlægsaktiv fra en købsfaktura. Fremgangsmåden er den samme for købsordrer.

1. Vælg ikonet ![Lightbulb, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **Bogført købsfaktura**, og vælg derefter det relaterede link.
2. Udfyld felterne efter behov i oversigtspanelet **Generelt**. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
3. Vælg **Anlægsaktiv** i feltet **Type** på oversigtspanelet **Linjer**.
4. I feltet **Nummer** , vælg aktivet, og angiv derefter antal og pris.
5. I feltet **Anlægsbogføringstype** skal du vælge **Reparation**.
6. Bogført købsfakturaen.

## Følg op på servicebesøg

Du kan udskrive rapporten **Reparation - næste service** for at se, hvilke aktiver der er planlagt servicebesøg for. Du kan også bruge denne rapport, når du vil opdatere feltet **Næste servicedato** på anlægskort.  

1. Vælg ikonet ![Lightbulb, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, angiv **Reparation - næste service**, og vælg derefter det relaterede link.  
2. Udfyld felterne **Startdato** og **Slutdato**  
3. Vælg knappen **Udskriv** eller **Vis udskrift**.

## Overvåge reparationsomkostninger

Du kan få vist statistikker for at overvåge vedligeholdelsesomkostningerne.  

1. Vælg ikonet ![Lightbulb, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **Anlægsaktiver**, og vælg derefter det relaterede link.
2. Vælg det anlægsaktiv, du vil have vist reparationsomkostninger for, og vælg derefter handlingen **Afskrivningsprofiler**.
3. På siden **Anlægsafskrivningsprofiler** skal du vælge den relevante anlægsafskrivningsprofil og derefter vælge handlingen **Statistik**.
4. På siden **Anlægsstatistik** skal du vælge feltet **Reparation**.

Brug siden **Vedligeholdelsesposter** til at få vist de poster, som indgår i beløbet i feltet **Vedligeholdelse**.

## Få du vist eller udskriver vedligeholdelsesomkostninger for flere anlægsaktiver

I rapporten **Vedligeholdelse - analyse** kan du vælge, om du vil have vist vedligeholdelse ud fra en, to eller tre Vedligeholdelseskoder på en bestemt dato eller i en bestemt periode. Rapporten kan vise totalen for alle valgte aktiver eller totalen for hvert enkelt aktiv.

1. Vælg ![Lightbulb, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **Reparationsanalyse**, og vælg derefter det relaterede link.
2. Udfyld felterne efter behov.
3. Vælg knappen **Udskriv** eller **Vis udskrift**.

## Få vist vedligeholdelsesposter

Du kan også undersøge vedligeholdelsesomkostningerne ved at se på vedligeholdelsesposterne.  

1. Vælg ![Lightbulb, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **Anlægsaktiver**, og vælg derefter det relaterede link.
2. Vælg det anlægsaktiv, du vil have vist poster for, og vælg derefter handlingen **Afskrivningsprofiler**.
3. På siden **Anlægsafskrivningsprofiler** skal du vælge den relevante anlægsafskrivningsprofil og derefter vælge handlingen **Reparationsposter**.

## Få du vist eller udskrive vedligeholdelsesposter for flere anlægsaktiver

I feltet **Reparationsposter** kan du få vist eller udskrive reparationsposter for et eller flere anlægsaktiver.  

1. Vælg ![Lightbulb, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **Reparationsdetaljer**, og vælg derefter det relaterede link.
2. Udfyld felterne efter behov.
3. Vælg knappen **Udskriv** eller **Vis udskrift**.

## Se også

[Anlægsaktiver](fa-manage.md)  
[Opsætning af Anlægsaktiver](fa-setup.md)  
[Finans](finance.md)  
[Blive køreklar](ui-get-ready-business.md)  
[Arbejd med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]
