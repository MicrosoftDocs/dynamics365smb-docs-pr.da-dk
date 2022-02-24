---
title: Bruge AMC Banking 365 Fundamentals-udvidelsen | Microsoft Docs
description: Du kan let udveksle data med dine banker ved at konvertere dataene til det format, de skal bruge.
author: bholtorf
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms. search.keywords: bank, format, data
ms.date: 10/14/2019
ms.author: bholtorf
ms.openlocfilehash: 9c9d927fb13d68c195bd457eb6bd2cbbfe078ea2
ms.sourcegitcommit: 86498fe4326b9ce26cc31e8645db27570d13bdf9
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 11/06/2019
ms.locfileid: "2767534"
---
# <a name="using-the-amc-banking-365-fundamentals-extension"></a>Bruge AMC Banking 365 Fundamentals-udvidelsen
AMC Banking 365 Fundamentals-udvidelsen gør det nemmere og mere nøjagtigt at sende data til dine banker. Udvidelsen forbinder [!INCLUDE[d365fin](includes/d365fin_md.md)] med AMC Banking 365 Fundamentals med Microsoft Dynamics 365 Business Central-tjenesten, som kan konvertere bankdata [!INCLUDE[d365fin](includes/d365fin_md.md)] til formater, der kræves af mere end 600 banker verden over. Det gør det f.eks. nemmere at overføre betalinger og kreditter til kreditorer ved at angive betalingerne i [!INCLUDE[d365fin](includes/d365fin_md.md)] og derefter overføre dem til din bank. Formaterne kan også forenkle bankafstemningsprocesser. Du kan finde flere oplysninger i [AMC Banking til Microsoft Dynamics 365 Business Central](https://amcbanking.com/landing365bc/help).

> [!Note]
> AMC Banking har oprettet yderligere udvidelser, som fungerer sammen med [!INCLUDE[d365fin](includes/d365fin_md.md)]. I dette emne beskrives kun Fundamental-udvidelsen.

## <a name="using-our-demonstration-account"></a>Bruge vores demonstrationskonto
[!INCLUDE[d365fin](includes/d365fin_md.md)] leveres med en demonstrationskonto, som giver dig mulighed for at prøve AMC Banking 365 Fundamentals-udvidelsen. Vi angiver standardindstillinger for oprettelse af forbindelse til AMC Banking, angivelse af de bankkonti, der skal hentes data fra i [!INCLUDE[d365fin](includes/d365fin_md.md)] samt nogle få dataudvekslingsdefinitioner. Du kan få vist forbindelsesindstillingerne på siden **Konfiguration af AMC Banking**. For bankkonti indsætter udvidelsen værdier i felterne **Banknavn**, **Kreditoverførselsmedd.numre**, **Format til import af bankkontoudtog** og **Format til eksport af betaling** på bankkontokort.

Vi angiver indstillingerne, men hvis du vil afprøve udvidelsen, skal du køre den assisterende opsætningsvejledning for at anvende dem. Hvis du vil køre guiden, skal du vælge handlingen **Assisteret opsætning** på siden **Konfiguration af AMC Banking**.

> [!Note]
> Der er nogle begrænsninger for demonstrationskontoen. Hvis du f.eks. konverterer betalinger, vil beløbet i den konverterede fil ikke svare til det faktiske beløb. I stedet vil beløbet altid være fem enheder af den valuta, som du bruger til betalinger.  

## <a name="setting-up-the-extension"></a>Konfigurere udvidelsen
Introduktionen til udvidelsen omfatter kun nogle få lette trin, og en assisteret opsætningsvejledning opretter forbindelsen og aktiverer udvidelsen. Guiden vil f.eks. installere dataudvekslingsdefinitioner til opsætning af eksport/import af bankkontoudtog og starte den nummerserie, der bruges til meddelelser om kreditoverførsel.  

### <a name="to-set-up-the-required-permission-sets"></a>Sådan angives de nødvendige rettighedssæt
Før brugerne kan bruge denne udvidelse, skal administratoren kopiere følgende rettighedssæt, redigere dem og derefter tildele de nye rettighedssæt til brugerne i stedet for originalen:

* **D365 Basis**
* **D365 Teammedlem**
* **D365 Læs**
* **IntelligentCloudBC**

Du kan finde flere oplysninger i [Sådan kopieres et rettighedssæt](ui-define-granular-permissions.md#to-copy-a-permission-set).

For hvert nyt rettighedssæt skal du kun give **læserettighed** til **AMC Banking-opsætningstabellen (20101).** Du kan finde flere oplysninger i [Sådan oprettes eller redigeres rettigheder manuelt](ui-define-granular-permissions.md#to-create-or-modify-permissions-manually).

### <a name="to-connect-the-extension-to-amc-banking"></a>Hvis du vil knytte udvidelsen til AMC Banking
1. Hent et modul og en serviceplan for AMC Banking. Det kan du gøre ved at besøge siden [AMC-licens](https://license.amcbanking.com/register).
2. I [!INCLUDE[d365fin](includes/d365fin_md.md)] skal du vælge ![ikonet Elpære, der åbner funktionen Fortæl mig](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig"), angive **Konfiguration af AMC Banking** og derefter vælge det relaterede link.  
3. Vælg handlingen **Assisteret opsætning** på siden **Konfiguration af AMC Banking**.
4. Udfør trinnene i guiden til assisteret opsætning.

### <a name="to-connect-bank-accounts-to-the-extension"></a>Knytte bankkonti til udvidelsen
1. Vælg ikonet ![Elpære, der åbner funktionen Fortæl mig](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig"), angiv **Bankkonti**, og vælg derefter det relaterede link.
2. Åbn kortet for den bankkonto, du vil knytte til servicen.
3. I feltet **Banknavn** skal du vælge det format, som din bank kræver.  

   Formaterne filtreres til kun at vise dem, der er relevante for det land/område, der er angivet for bankkontoen.
4. I feltet **Kreditoverførselsmedd.numre** skal du vælge den nummerserie, der skal bruges til de meddelelser, der vedlægges betalinger.
5. I felterne **Format til import af bankkontoudtog** og **Format til eksport af betaling** skal du vælge de dataudvekslingsdefinitioner, som din bank kræver.

## <a name="using-the-extension"></a>Brug af udvidelsen
Brug af denne udvidelse går blot ud på at eksportere data på siden **Udbetalingskladder** og derefter overføre dem til bankens webtjeneste. Du kan finde flere oplysninger i [Foretage indbetalinger med tjenesten til konvertering af bankdata eller SEPA Kreditoverførsel](finance-make-payments-with-bank-data-conversion-service-or-sepa-credit-transfer.md).

> [!Note]
> Du skal udfylde felterne **SWIFT-kode** og **IBAN** for hver bankkonto.

### <a name="to-export-data-and-submit-it-to-your-bank"></a>Eksportere data og sende dem til din bank
> [!CAUTION]  
>  Når du eksporterer data ved hjælp af AMC Banking 365 Fundamentals-udvidelsen, vil nogle af virksomhedens data blive eksponeret for tjenesteudbyderen. Serviceudbyderen, AMC Consult A/S, er ansvarlig for beskyttelsen af disse data. Du kan finde flere oplysninger i [AMC's politik for beskyttelse af personlige oplysninger](https://go.microsoft.com/fwlink/?LinkId=510158).

1. Vælg ikonet ![Elpære, der åbner funktionen Fortæl mig](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig"), angiv **Udbetalingskladder**, og vælg derefter det relaterede link.
2. Opret de kladdelinjer, du vil eksportere.  

   > [!Note]
   > For hver linje skal du huske at vælge **Elektronisk betaling** i feltet **Bankbetalingstype**.
3. Vælg handlingen **Eksportér**.

### <a name="to-import-and-apply-the-converted-file"></a>Sådan importeres og anvendes den konverterede fil
1. Vælg ikonet ![Elpære, der åbner funktionen Fortæl mig](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig"), angiv **Betalingsudligningskladde**, og vælg derefter det relaterede link.
2. Vælg handlingen **Importér banktransaktioner**, og vælg derefter den konverterede fil.  

   [!INCLUDE[d365fin](includes/d365fin_md.md)] opretter en ny betalingsudligningskladde, der indeholder dataene i filen. Du kan finde flere oplysninger under [Udligne betalinger automatisk og afstemme bankkonti](receivables-apply-payments-auto-reconcile-bank-accounts.md).

## <a name="see-also"></a>Se også
[Tilpasse [!INCLUDE[d365fin](includes/d365fin_md.md)] ved hjælp af udvidelser](ui-extensions.md)  
[Introduktion](product-get-started.md)
