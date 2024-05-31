---
title: Omvurdere anlægsaktiver
description: 'Lær at regulere værdien af anlægsaktiver, registrere nye beløb som nedskrivning eller opskrivning og bogføre andre anskaffelser.'
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bnielse
ms.topic: conceptual
ms.search.form: '5628, 5629, 5633'
ms.date: 02/22/2024
ms.service: dynamics-365-business-central
ms.custom: bap-template
---
# Omvurdere anlægsaktiver

Regulering af anlægsaktiver kan bestå af opskrivninger, nedskrivninger eller generelle værdireguleringer.

Når værdien af et anlægsaktiv stiver, skal du bogføre en kladdelinje med en opskrivning for afskrivningsprofilen. Det nye beløb registreres som en opskrivning ifølge anlægsbogføringsgruppens opsætning.

Når værdien af et anlægsaktiv falder, skal du bogføre en kladdelinje med et lavere beløb, dvs. en nedskrivning, for afskrivningsprofilen. Det nye beløb registreres som en nedskrivning ifølge anlægsbogføringsgruppens opsætning.

Indeksering anvendes til at justere værdien for flere anlæg, f.eks. ifølge generelle prisændringer. Kørslen **Indeksér anlæg** kan bruges til at ændre forskellige beløb, f.eks. nedskrivnings- og opskrivningsbeløb.

## Sådan bogføres en opskrivning fra anlægskassekladden

1. Vælg det ![lyspæreikon, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **Anlægsfinanskladder**, og vælg derefter det relaterede link.  
2. Opret en første kladdelinje, og udfyld felterne efter behov.
3. I feltet **Anlægsbogføringstype** skal du vælge **Regulering**.
4. Vælg handlingen **Indsæt anlægsmodkonto**. Der oprettes en anden kladdelinje til den modkonto, der er oprettet til bogføring af opskrivning.

    > [!NOTE]  
    >   Trin 4 fungerer kun, hvis du har angivet følgende: På siden **Anlægsbogføringsgruppekort** for bogføringsgruppen for anlægsaktivet indeholder feltet **Opskrivningskonto** finansdebetkontoen og feltet **Opskrivningsmodkonto** indeholder den finanskonto, hvor du vil bogføre modposter for opskrivning. Du kan finde flere oplysninger i [Sådan oprettes anlægsbogføringsgrupper](fa-how-setup-general.md#to-set-up-fixed-asset-posting-groups).  
5. Vælg handlingen **Bogfør**.

## Sådan bogføres en nedskrivning fra anlægskassekladden

1. Vælg ![Lightbulb, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **Anlægsfinanskladder**, og vælg derefter det relaterede link.  
2. Opret en første kladdelinje, og udfyld felterne efter behov.
3. I feltet **Anlægsbogføringstype** skal du vælge **Nedskrivning**.
4. Vælg handlingen **Indsæt anlægsmodkonto**. Der oprettes en anden kladdelinje til den modkonto, der er oprettet til bogføring af nedskrivning.

    > [!NOTE]  
    >   Trin 4 fungerer kun, hvis du har angivet følgende: På siden **Anlægsbogføringsgruppekort** for bogføringsgruppen for anlægsaktivet indeholder feltet **Nedskrivningskonto** finansdebetkontoen og feltet **Nedskrivningsmodkonto** indeholder den finanskonto, hvor du vil bogføre modposter for nedskrivning. Du kan finde flere oplysninger i [Sådan oprettes anlægsbogføringsgrupper](fa-how-setup-general.md#to-set-up-fixed-asset-posting-groups).
5. Vælg handlingen **Bogfør**.

## Sådan udføres generel værdiregulering af anlægsaktiver

Indeksering anvendes til at justere værdien for flere anlæg, f.eks. ifølge generelle prisændringer. Kørslen **Indeksér anlæg** kan bruges til at ændre forskellige beløb, f.eks. nedskrivnings- og opskrivningsbeløb. Afkrydsningsfeltet **Tillad indeksering** på siden **Afskrivningsprofil** skal være markeret.

1. Vælg ![Lightbulb, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **Indeksér anlæg**, og vælg derefter det relaterede link.  
2. Udfyld felterne efter behov.
3. Vælg knappen **OK**.

    Der oprettes værdireguleringslinjer ud fra dine indstillinger i trin 2. Linjerne er oprettet i anlægskladden eller anlægskassekladden, afhængigt af skabelonen og kørselsopsætningen på siden **Anlægskladdeopsætning**. Du kan finde flere oplysninger i [Angive generelle oplysninger om anlægsaktiver](fa-how-setup-general.md).
4. Vælg ![Lightbulb, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **Anlægsfinanskladder**, og vælg derefter det relaterede link.  
5. Vælg kladden med de anlægsaktiver, du vil regulere værdien for, og vælg derefter handlingen **Poster**.  
6. Kontroller de oprettede poster, og vælg derefter handlingen **Bogfør** for at bogføre kladden.

    > [!TIP]  
    >   Hvis indekstallene kun skal bruges til simulering, kan du oprette en særlig afskrivningsprofil, hvor de kan opbevares. Derefter kan disse poster ikke indvirke på de øvrige afskrivningsprofiler.

## Sådan bogføres øvrige anskaffelser

Du bogfører prisen for ekstraanskaffelse af et anlægsaktiv fra en købsfaktura eller fra en anlægskladde på samme måde som du bogfører den oprindelige anskaffelsespris. Du kan finde flere oplysninger i [Anskaffe anlægsaktiver](fa-how-acquire.md).  

Hvis der allerede er beregnet afskrivning for anlægsaktivet, skal du markere afkrydsningsfeltet **Afskriv anskaffelse**, for at den ekstra anskaffelsespris minus skrapværdien afskrives i forhold til det beløb, hvormed det tidligere anskaffede anlægsaktiv i forvejen er blevet afskrevet. Denne metode sikrer, at afskrivningsperioden ikke ændres.  

Afskrivningsprocenten beregnes som:  

*P = (samlet afskrivning x 100) / afskrivningsgrundlag*

*Afskrivningsbeløb = (P/100) x (ekstra anskaffelse - skrapværdi)*  

Husk at markere afkrydsningsfeltet **Afskriv til bogføringsdato for anlæg** på fakturaen, anlægskassekladden eller anlægskladdelinjerne for at sikre, at afskrivningen beregnes fra den sidste bogføringsdato for anlæg til bogføringsdatoen for den ekstra anskaffelsespris.

### Eksempel - bogføring af øvrige anskaffelser

En maskine købes 1. august 2000. Anskaffelsesprisen er 4.800. Afskrivningsmetoden er lineær over fire år.

Den 31. august 2000 udføres kørslen **Beregn afskrivninger**. Afskrivningen beregnes som:

*bogført værdi x antal afskrivningsdage / samlet antal afskrivningsdage = 4800 x 30 / 1440 = 100*  

Den 15. september 2000 bogføres en faktura for maling af maskinen. Fakturabeløbet er 480.

Hvis du har markeret afkrydsningsfeltet **Afskriv til bogføringsdato for anlæg** på fakturaen inden bogføringen, foretages følgende beregning:  

15 dages afskrivning (fra 01-09-00 til 15-09-00) beregnes som:

*bogført værdi x antal afskrivningsdage / resterende antal afskrivningsdage = (4800 - 100) x 15 / 1410 = 50*

Hvis du har markeret afkrydsningsfeltet **Afskriv anskaffelse** på fakturaen inden bogføringen, foretages følgende beregning:  

*Den anden anskaffelsespris afskrives som ((150 x 100) / 4800) / 100 x 480 = 15*

Afskrivningsgrundlaget er nu *5280 = (4800 + 480)*, og den akkumulerede afskrivning er *165 = (100 + 50 + 15)*, hvilket svarer til 45 dages afskrivning på den samlede anskaffelsespris. Denne beregning betyder, at aktivet bliver helt afskrevet inden for den anslåede levetid på fire år.  

Når kørslen **Beregn afskrivninger** udføres den 30-09-00, foretages følgende beregning:  

*Resterende afskrivningsliv er 3 år, 10 måneder og 15 dage = 1395 dage*  

*Bogført værdi er (5280 - 165) = 5115*  

*Afskrivningsbeløb for september 2000: 5115 x 15 / 1395 = 55,00*  

*Samlet afskrivning = 165 + 55 = 220*  

Hvis du ikke har markeret afkrydsningsfeltet **Afskriv til bogføringsdato for anlæg**, mister aktivet 15 dages afskrivning, fordi kørslen **Beregn afskrivninger**, der udføres den 30-09-00, vil beregne afskrivningen fra 15-09-00 til 30-09-00. Det betyder, at når kørslen **Beregn afskrivninger** udføres den 30-09-00, anvendes følgende beregningsmetode:  

*Resterende levetid er 3 år, 10 måneder og 15 dage = 1395 dage*  

*Bogført værdi er (4800 + 480 - 100 - 15) = 5165*

*Afskrivningsbeløb for september 2000: 5165 x 15 / 1395 = 55,54*  

*Samlet afskrivning = 100 + 15 + 55,54 = 170,54*

## Se også

[Anlægsaktiver](fa-manage.md)  
[Opsætning af Anlægsaktiver](fa-setup.md)  
[Finans](finance.md)  
[Blive køreklar](ui-get-ready-business.md)  
[Arbejd med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]
