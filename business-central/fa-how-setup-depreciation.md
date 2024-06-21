---
title: Opsætte anlægsafskrivning
description: Der er forskellige metoder til afskrivning. I Business central defineres afskrivningsmetoden for anlæg på **anlægskort**-siden.
author: brentholtorf
ms.topic: conceptual
ms.search.keywords: write down
ms.date: 06/28/2021
ms.author: bholtorf
ms.service: dynamics-365-business-central
ms.reviewer: bholtorf
---

# Opsætte afskrivning af anlægsaktiv

Du kan bruge forskellige afskrivningsmetoder til forberedelse af årsregnskab og selvangivelse. Mange store virksomheder benytter lineær afskrivning i deres årsregnskab, fordi dette som regel tillader angivelse af højere indkomst. Af skattemæssige årsager bruger mange virksomheder dog en metode til hurtigere afskrivning såsom saldoafskrivning. Du kan definere afskrivningsmetoden for anlægsaktivet med feltet **Afskrivningsmetode** på siden **Anlægskort**. Du kan finde yderligere oplysninger om de forskellige metoder i [Afskrivningsmetoder](fa-depreciation-methods.md).

Du kan konfigurere de afskrivningsprofiler, du definerer de forskellige afskrivninger, skal der beregnes for de forskellige anlægsaktiver. Hver afskrivningsprofil angiver individuelle afskrivningsbetingelser. For en profil kan du f.eks. angive, at anlægsaktivet skal afskrives over 3 år, og i en anden profil over fem år.

Når du har oprettet de relevante afskrivningsprofiler, skal du tildele en eller flere afskrivningsprofiler til hvert anlægsaktiv. En afskrivningsprofil, der er tildelt til et anlægsaktiv, kaldes en anlægsafskrivningsprofil. Du kan opsætte et ubegrænset antal afskrivningsprofiler for et anlæg.  

## Sådan oprettes en afskrivningsprofil

I en anlægsafskrivningsprofil angiver du, hvordan anlægsaktiver skal afskrives. Du kan definere flere afskrivningsprofiler for at tage højde for forskellig slags afskrivningsmetoder.  

1. Vælg ![Lightbulb, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **Afskrivningsprofiloversigt**, og vælg derefter det relaterede link.
2. På siden **Afskrivningsprofiloversigt** skal du vælge handlingen **Ny**.
3. På siden **Afskrivningsprofilkort** skal du udfylde felterne efter behov. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

    > [!NOTE]  
    > Du kan registrere anlægstransaktioner på siden **Anlægskassekladde** eller på siden **Anlægskladde**, afhængigt af om transaktionerne, der er til finansiel rapportering eller intern administration. Udfør næste trin for at angive, hvilken type kladden der som standard bruges til de forskellige anlægsaktiviteter.
4. På oversigtspanelet **Integration** skal du markere afkrydsningsfeltet for hvert anlægsaktivitet, hvis transaktioner skal bogføres ved hjælp af siden **Anlægskassekladde**.
5. Gentag trin 2 til 4 for hver afskrivningsmetode eller bogføringsmetode, du vil tildele til anlægsaktiver som en afskrivningsprofil.

> [!IMPORTANT]
> Marker feltet **Brug afrunding i per. afskr. afskrivning** for at afrunde de beregnede afskrivningsbeløb til hele tal. Hvis virksomheden f.eks. også anvender fakturaafrunding til hele tal på siden **Regnskabsopsætning**, kan afrunding også indeholder afskrivningsbeløb til hele tal være med til at give gennemsigtighed.

Hvis du f.eks. sælger et anlægsaktiv, hvor afskrivningsprofilen ikke angiver afrunding, men virksomhedens finans opsætning kræver afrunding, vises der en fejlmeddelelse om, at et beløb skal afrundes på en post, når du sælger anlægsaktivet.  

## Sådan tildeles en afskrivningsprofil til et anlægsaktiv

1. Vælg ![Lightbulb, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **Anlægsaktiver**, og vælg derefter det relaterede link.
2. Vælg det anlægsaktiv, som du vil konfigurere en anlægsafskrivningsprofil for.
3. I oversigtspanelet **Afskrivningsprofil** skal du udfylde felterne efter behov.
4. Hvis du vil tildele mere end én afskrivningsprofil til anlægsaktivet, skal du vælge handlingen **Tilføj flere afskrivningsprofiler**.
5. Du kan også vælge handlingen **Afskrivningsprofiler** for at angive en eller flere anlægsafskrivningsprofiler.

    > [!NOTE]  
    >   Når du bruger den manuelle afskrivningsmetode, skal du angive afskrivningen manuelt i anlægskassekladden. Funktionen **Beregn afskrivninger** udelader de anlægsaktiver, som benytter den manuelle afskrivningsmetode. Du kan bruge denne metode til aktiver, der ikke skal afskrives, f.eks. jord.

    > [!NOTE]  
    > Når du bruger den brugerdefinerede afskrivningsmetode, skal du tildele afskrivningsprofilen på en anden måde. Du kan finde flere oplysninger i [konfigurere brugerdefineret afskrivningsmetode](fa-how-setup-user-defined-depreciation-method.md).

## Sådan tildeles en afskrivningsprofil til flere anlægsaktiver med en kørsel

Hvis du vil tildele en afskrivningsprofil til flere anlægsaktiver, kan du bruge kørslen **Opret anlægsafskr.profiler** til at oprette anlægsafskrivningsprofiler.  

1. Vælg ![Lightbulb, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **Anlægsaktiver**, og vælg derefter det relaterede link.
2. Vælg det anlægsaktiv, som du vil tildele en afskrivningsprofil, og vælg derefter handlingen **Rediger**.
3. På siden **Afskrivningsprofilkort** skal du vælge handlingen **Opret anlægsafskr.profiler**.
4. På siden **Opret anlægsafskr.profiler** skal du udfylde feltet **Afskrivningsprofil**.
5. Vælg feltet **Kopier fra anlægsnr.**, og vælg derefter det anlægsnummer, du vil bruge som grundlag for oprettelsen af nye afskrivningsprofiler for anlægsaktiver.

    Hvis du udfylder feltet, får afskrivningsfelterne i de nye anlægsafskrivningsprofiler samme indhold som de tilsvarende felter i den anlægsafkrivningsprofil, du kopierer fra. Lad feltet stå tomt, hvis du vil oprette nye anlægsafskrivningsprofiler med tomme afskrivningsfelter.  
6. I oversigtspanelet **Anlæg** kan du definere et filter for at udvælge de aktiver, som du vil oprette anlægsafskrivningsprofiler for.
7. Vælg knappen **OK**.

## Sådan defineres bogføringstyper for afskrivning

For hver afskrivningsprofil skal du angive, hvordan [!INCLUDE[prod_short](includes/prod_short.md)] skal håndtere forskellige bogføringstyper. For eksempel skal det angives, om bogføringen skal være debet eller kredit, og om bogføringstypen skal medtages i afskrivningsgrundlaget.  

1. Vælg ![Lightbulb, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **Afskrivningsprofiloversigt**, og vælg derefter det relaterede link.  
2. Vælg den afskrivningsprofil, du vil konfigurere, og vælg derefter handlingen **Anlægsbogf.typeopsætning**.
3. Udfyld felterne efter behov på siden **Anlægsbogf.typeopsætning**.

    > [!NOTE]  
    >   Du kan ikke indsætte eller slette linjer på siden **Anlægsbogf.typeopsætning**. Du kan kun rette eksisterende linjer.

Det anbefales dog, at du ikke ændrer opsætningen af afskrivningsprofiler, hvori posteringer allerede er blevet bogført. Ændringer har ikke indflydelse på posteringer, som allerede er bogført, hvilket ville gøre afskrivningsprofilstatistikken misvisende.

## Sådan defineres standardtyper og -kørsler for anlægsafskrivning

For hver afskrivningsprofil skal du definere en standardopsætning med typer og navne. Du bruger disse standarder til at duplikere linjer fra én kladde til en anden, oprette kladdelinjer ved hjælp af kørslen **Beregn afskrivning** eller **Indekser anlæg**, duplikere anskaffelsesomkostninger i forsikringskladden.  

1. Vælg ![Lightbulb, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **Afskrivningsprofiloversigt**, og vælg derefter det relaterede link.  
2. Vælg den afskrivningsprofil, du vil definere standardkladder for, og vælg derefter handlingen **Anlægskladdeopsætning**.  
3. Hvis du vil have en standardopsætning for hver enkelt bruger, skal du vælge feltet **Bruger-id** for at vælge opsætninger på siden **Brugere**.  
4. Vælg den kladdetype eller kørsel i de andre felter, som skal bruges som standard.  

## Feltet Regnskabsår 365 dage afskrivning

Når der beregnes afskrivninger i kørslen Beregn afskrivninger, bruges der normalt et standardår på 360 dage i kørslen, hvor hver af de 12 måneder består af 30 dage.

Hvis du markerer dette felt, anvendes der i stedet et kalenderår på 365 dage i kørslen Beregn afskrivninger, hvor hver måned beregnes med samme antal dage som i kalenderen. Den eneste undtagelse er februar i skudår, som i kørslen behandles, som om der er 28 dage og ikke 29. Pga. det anses alle år, også skudår, for at bestå af 365 dage.

## Se også

[Opsætning af Anlægsaktiver](fa-setup.md)  
[Anlægsaktiver](fa-manage.md)  
[Finans](finance.md)  
[Blive køreklar](ui-get-ready-business.md)  
[Arbejd med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]
