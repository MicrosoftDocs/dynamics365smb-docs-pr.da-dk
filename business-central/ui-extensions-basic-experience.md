---
title: Basic Experience Extension | Microsoft-dokumenter
description: Denne udvidelse er et nyere alternativ til Microsoft Dynamics C5.
author: brentholtorf
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 'C5, financials, extension'
ms.search.form: '20600,'
ms.date: 04/01/2021
ms.author: bholtorf
---

# <a name="the-basic-experience-extension"></a><a name="the-basic-experience-extension"></a><a name="the-basic-experience-extension"></a>Basic Experience Extension

Hvis du har brugt Microsoft Dynamics C5, kan Microsoft-partnere hjælpe dig med at skifte til en mere moderne løsning, der er baseret på [!INCLUDE[prod_short](includes/prod_short.md)], så du fortsat kan nyde den samme strømlinede funktionalitet som Dynamics C5.

Denne udvidelse henvender sig til mindre virksomheder og kan understøtte op til tre brugere. Hvis du har brug for flere brugere, skal du opgradere til en [!INCLUDE[prod_short](includes/prod_short.md)]-licens og fjerne udvidelsen.

> [!NOTE]
> Denne udvidelse er kun tilgængelig for debitorer i Danmark og Island.

## <a name="whats-available"></a><a name="whats-available"></a><a name="whats-available"></a>Tilgængelige oplysninger

I følgende tabel beskrives de funktioner, der er tilgængelige, hvis du installerer Basic Experience-udvidelsen.

|Område  |Funktion  |
|---------|---------|
|**Finansposter** |Grundlæggende finans, finansrapporter, anlægsaktiver, bankstyring, bankafstemning, betalinger, direkte debitering, dimensioner, flere valutaer, budgetter, arbejdsgang, dokumentstyring/OCR, konsolidering, ubegrænsede firmaer|
|**Aldersfordelte tilgodehavender** |Grundlæggende tilgodehavender, salgsfakturering, salgsrabatter, pris, moms, Kontaktstyring |
|**Kreditorer/indkøb** |Grundlæggende skyldige beløb, købsfakturering |
|**Projektstyring** |Sager, sagsomkostninger, time sedler, tildeling, opgaver, ressourcer |
|**Lagerbeholdning** |Basis lager, erstatningsvare, varereferencer |

## <a name="getting-started"></a><a name="getting-started"></a><a name="getting-started"></a>Introduktion

Dette filtypenavn er lidt anderledes end de fleste, og du har brug for hjælp fra en Microsoft-partner for at kunne installere og konfigurere den. Det betyder, at du ved, hvad du kan forvente, men her er en overordnet oversigt over, hvad Microsoft-partneren skal gøre.

1. Oprette en ny [!INCLUDE[prod_short](includes/prod_short.md)]-lejer. Dette kan enten være en prøveversion eller en version af CSP.
2. Tilføje mindst én bruger, der er tildelt en grundlæggende Experience licens, i din Azure Active Directory-konto.
3. Fjerne alle regnskaber, herunder eksemplet med CRONUS-regnskabet.
4. Oprette en ny virksomhed, der ikke indeholder eksempeldata eller opsætninger.
5. Tilføje **Demo RapidStart**-pakken. <!--what does the package contain?-->
6. Hente og installere Basic Experience-udvidelsen fra AppSource.

## <a name="migrating-data"></a><a name="migrating-data"></a><a name="migrating-data"></a>Dataoverførsel

Bring dine Dynamics C5-data sammen. Når din Microsoft-partner har installeret den grundlæggende oplevelse, har du en tom virksomhed. En nem måde at flytte dine data fra Dynamics C5 il Basic Experience på er at bruge det C5-data overflytnings udvidelse, som findes i [!INCLUDE[prod_short](includes/prod_short.md)]. Udvidelsen overflytter debitorer, kreditorer, varer og finanskonti og deres poster.

## <a name="see-also"></a><a name="see-also"></a><a name="see-also"></a>Se også

[Udvidelsen C5-dataoverførsel](ui-extensions-c5-data-migration.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
