---
title: Vedligeholde anlægsaktiver
description: Du fører en vedligeholdelsespost for reparation og service på et anlægsaktiv for at bevare anlægsaktivets værdi.
author: brentholtorf
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 'repair, service'
ms.search.form: '5642, 5625'
ms.date: 06/15/2021
ms.author: bholtorf
---
# <a name="maintain-fixed-assets"></a>Vedligeholde anlægsaktiver

Reparationsudgifter er periodisk forekommende rutineomkostninger, der afholdes for at bevare anlægsaktivernes værdi. I modsætning til kapitalforbedringer forøges deres værdi ikke.

Du kan registrere og vedligeholde en opdateret fil om anlægsreparation og -service, så du har en nemt tilgængelig og fuldstændig fortegnelse over reparation af et anlæg. Hver gang et anlægsaktiv bliver sendt til service, registrerer du alle relevante oplysninger som f.eks. dato, kreditornummer og reparatørens telefonnummer. Der bliver foretaget reparationsregistrering for hvert enkelt anlægsaktiv fra anlægskortet.

Indeksering anvendes til at justere for ændringer af det generelle prisniveau. Kørslen **Indeksér anlæg** kan bruges til at genberegne reparationsomkostningerne.

## <a name="to-record-maintenance-work-on-a-fixed-asset"></a>Sådan registreres reparationsarbejde på et anlægsaktiv

Hver gang der er udført reparationsopgaver, f.eks. et servicebesøg, kan du registrere det for det pågældende anlægsaktiv på siden **Reparationsregistreringer**.  

1. Vælg ![Lightbulb, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **Anlægsaktiver**, og vælg derefter det relaterede link.  
2. Vælg det anlægsaktiv, du vil registrere vedligeholdelse for, og vælg derefter handlingen **Reparationsregistrering**.
3. På siden **Reparationsregistrering** skal du udfylde felterne efter behov. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]  

## <a name="to-post-maintenance-costs-from-a-fixed-asset-gl-journal"></a>Sådan bogføres reparationsomkostninger fra en anlægskassekladde

1. Vælg ![Lightbulb, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **Afskrivningsprofiloversigt**, og vælg derefter det relaterede link.  
2. Vælg den afskrivningsprofil, der er tildelt anlægsaktivet, og vælg derefter handlingen **Rediger**.
3. På siden **Afskrivningsprofilkort** skal du kontrollere, at afkrydsningsfeltet **Vedligeholdese** ikke er markeret. Dette sikrer, at vedlligeholdelsesomkostninger ikke bogføres i finansregnskabet.
4. Vælg ![Lightbulb, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **Anlægsfinanskladder**, og vælg derefter det relaterede link.  
5. Opret en første kladdelinje, og udfyld felterne efter behov.
6. I feltet **Anlægsbogføringstype** skal du vælge **Reparation**.
7. Vælg handlingen **Indsæt anlægsmodkonto**. Der oprettes en anden kladdelinje til den modkonto, der er oprettet til bogføring af vedligeholdelse.

    > [!NOTE]  
    >   Trin 7 fungerer kun, hvis du har angivet følgende: På siden **Anlægsbogføringsgruppekort** for bogføringsgruppen for anlægsaktivet indeholder feltet **Reparationskonto** finansdebetkontoen og feltet **Reparationsmodkonto** indeholder den finanskonto, hvor du vil bogføre modposter for opskrivning. Du kan finde flere oplysninger i [Sådan oprettes anlægsbogføringsgrupper](fa-how-setup-general.md#to-set-up-fixed-asset-posting-groups).
8. Vælg handlingen **Bogfør**.

## <a name="to-follow-up-on-fixed-assets-service-visits"></a>Sådan følger du op på servicebesøg på anlæg

Du kan udskrive rapporten **Reparation - næste service** for at se, hvilke anlæg der er planlagt servicebesøg for. Du kan også bruge denne rapport, når du opdaterer feltet **Næste servicedato** på anlægskort.  

1. Vælg ![Lightbulb, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, angiv **Reparation - næste service**, og vælg derefter det relaterede link.  
2. Udfyld felterne **Startdato** og **Slutdato**  
3. Vælg knappen **Udskriv** eller **Vis udskrift**.

## <a name="to-monitor-maintenance-costs"></a>Sådan overvåges reparationsomkostningerne

Du kan se reparationsomkostningerne i statistikken for et anlægsaktiv.  

1. Vælg ![Lightbulb, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **Anlægsaktiver**, og vælg derefter det relaterede link.
2. Vælg det anlægsaktiv, du vil have vist reparationsomkostninger for, og vælg derefter handlingen **Afskrivningsprofiler**.
3. På siden **Anlægsafskrivningsprofiler** skal du vælge den relevante anlægsafskrivningsprofil og derefter vælge handlingen **Statistik**.
4. På siden **Anlægsstatistik** skal du vælge feltet **Reparation**.

Siden **Reparationsposter** åbnes med de poster, som indgår i beløbet i feltet **Reparation**.

## <a name="to-view-or-print-maintenance-costs-for-multiple-fixed-assets"></a>Sådan får du vist eller udskriver reparationsomkostninger for flere anlægsaktiver

I rapporten **Reparation - analyse** kan du vælge, om du vil have vist vedligeholdelse ud fra en, to eller tre reparationskoder på en bestemt dato eller i en bestemt periode. Du kan se totalen for alle valgte aktiver eller totalen for hvert enkelt aktiv.

1. Vælg ![Lightbulb, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **Reparationsanalyse**, og vælg derefter det relaterede link.
2. Udfyld felterne efter behov.
3. Vælg knappen **Udskriv** eller **Vis udskrift**.

## <a name="to-view-maintenance-ledger-entries"></a>Sådan får du vist reparationsposter

Du kan også undersøge reparationsomkostningerne ved at se på reparationsposterne.  

1. Vælg ![Lightbulb, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **Anlægsaktiver**, og vælg derefter det relaterede link.
2. Vælg det anlægsaktiv, du vil have vist poster for, og vælg derefter handlingen **Afskrivningsprofiler**.
3. På siden **Anlægsafskrivningsprofiler** skal du vælge den relevante anlægsafskrivningsprofil og derefter vælge handlingen **Reparationsposter**.

## <a name="to-view-or-print-maintenance-ledger-entries-for-multiple-fixed-assets"></a>Sådan får du vist eller udskriver reparationsposter for flere anlægsaktiver

I feltet **Reparationsposter** kan du få vist eller udskrive reparationsposter for et eller flere anlægsaktiver.  

1. Vælg ![Lightbulb, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **Reparationsdetaljer**, og vælg derefter det relaterede link.
2. Udfyld felterne efter behov.
3. Vælg knappen **Udskriv** eller **Vis udskrift**.

## <a name="see-also"></a>Se også

[Anlægsaktiver](fa-manage.md)  
[Opsætning af Anlægsaktiver](fa-setup.md)  
[Finans](finance.md)  
[Blive køreklar](ui-get-ready-business.md)  
[Arbejd med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]
