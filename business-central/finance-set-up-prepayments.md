---
title: Oprette forudbetalinger
description: Lær, hvordan du konfigurerer Business Central til at fakturere og opkræve depositum, der kræves af debitorer eller at sende depositummerne til kreditorer.
author: edupont04
ms.topic: conceptual
ms.search.keyword: prepayment
ms.search.form: 314, 459, 460, 664
ms.date: 10/27/2021
ms.author: edupont
ms.openlocfilehash: 39870723c78bc341ecd32b031503980740151c48
ms.sourcegitcommit: ef80c461713fff1a75998766e7a4ed3a7c6121d0
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 02/15/2022
ms.locfileid: "8128465"
---
# <a name="set-up-prepayments"></a>Oprette forudbetalinger

Hvis det er et krav, at dine kunder skal betale, før du leverer en ordre til dem, eller hvis din leverandør kræver, at du skal betale, før de sender en ordre til dig, kan du bruge forudbetalinger. Forudbetalingsfunktionen sætter dig i stand til at fakturere og opkræve depositum fra debitorer eller at sende depositummerne til kreditorer og til at sikre, at alle delvise betalinger bogføres i forhold til en faktura. Du kan finde flere oplysninger i [Oprette forudbetalingsfakturaer](finance-how-to-create-prepayment-invoices.md).

Inden du kan bogføre forudbetalingsfakturaer, skal du oprette bogføringskonti i finansposterne, og du skal oprette nummerserier for forudbetalingsdokumenterne. Du skal angive en konto til forudbetalinger, der vedrører salg, og en konto til forudbetalinger, der vedrører køb. Du kan angive de samme bogføringskonti, der skal bruges til alle forudbetalinger, der vedrører alle virksomhedsbogføringsgrupper eller generelle produktbogføringsgrupper, eller du kan angive bestemte konti til bestemte bogføringsgrupper til henholdsvis salg og køb. Dette afhænger af virksomhedens krav til sporing af forudbetalinger.  

Du kan definere den procentdel af linjebeløbet, der skal faktureres for forudbetaling - for en debitor eller kreditor, for alle varer eller udvalgte varer. Når du har fuldført opsætningen, kan du generere forudbetalingsfakturaer fra salgs- og købsordrer. Du kan bruge standardprocenterne for hver salgs- eller indkøbslinje, eller du kan ændre beløbene efter behov. Du kan f.eks. angive et samlet beløb for hele ordren.  

> [!NOTE]
> Det anbefales, at du ikke bruger en forudbetalingsprocent på 100 % i følgende tilfælde:
>
> * Hvis du befinder dig i Nordamerika. Grundet beregningsmåden for moms kan en forudbetalingsprocent på 100 % medføre problemer med forudbetalingsfakturaer.
> * I alle områder hvis du manuelt fratrækker en kontantrabat fra fakturaen. Vil en forudbetalingsprocent på 100 % ikke automatisk efterlade et beløb, hvorfra rabatten skal fratrækkes.
>
> Når du bruger en forudbetaling på 100 %, er [!INCLUDE[prod_short](includes/prod_short.md)] det måske nødvendigt at oprette afrundingsposter. Når det sker, skal du vælge en finanskonto i feltet **Fakturaafrundingskonto** på siden **Debitorbogføringsgrupper**. Dette gælder også, hvis du ikke har aktiveret til/fra-feltet **Fakturaafrunding** på siden **Salgsopsætning**. Hvis du ikke angiver en konto, kan du ikke bogføre forudbetalingsfakturaer. 

Eftersom det forudbetalte beløb tilhører køberen, indtil han har modtaget varerne eller tjenesteydelsen, er du nødt til at oprette finanskonti, som forudbetalte beløb kan indsættes på, indtil den endelige faktura bogføres. Salgsforudbetalinger skal registreres på en passivkonto, indtil varerne leveres. Købsforudbetalinger skal registreres på en aktivkonto, indtil varerne modtages. Du skal også oprette en separat finanskonto til hvert moms-id.  

[!INCLUDE[local-func-setup-link](includes/local-func-setup-link.md)]

## <a name="to-add-prepayment-accounts-to-the-general-posting-setup"></a>Sådan føjes forudbetalingskonti til bogføringsopsætning  

1. Vælg ![Lightbulb, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **Bogføringsopsætning**, og vælg derefter det relaterede link.
2. På siden **Bogføringsopsætning** skal du udfylde følgende felter for de relevante linjer:  

    * **Forudbetalingskonto for salg**  
    * **Forudbetalingskonto for køb**  

> [!TIP]
> Hvis du ikke kan se felterne på siden **Bogføringsopsætning**, skal du bruge det vandrette rullepanel nederst på siden til at rulle til højre.  

Hvis du ikke allerede har angivet finanskonti til forudbetalinger, kan du åbne siden **Finanskontooversigt** fra det relevante kontofelt.  

## <a name="to-set-up-number-series-for-prepayment-documents"></a>Sådan oprettes nummerserier til forudbetalingsdokumenter  

1. Vælg ![Lightbulb, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, angiv **Salgsopsætning**, og vælg derefter det relaterede link.
2. Udfyld følgende felter i oversigtspanelet **Nummerserie** på siden **Salgsopsætning**.  

   * **Bogførte forudbetalingsfakturanr.**
   * **Bogførte forudbetalingskreditnotanr.**

3. Vælg ![Lightbulb, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, angiv **Købsopsætning** og derefter vælge det relaterede link.
4. Udfyld følgende felter i oversigtspanelet **Nummerserie** på siden **Købsopsætning**.

    * **Bogførte forudbetalingsfakturanr.**
    * **Bogførte forudbetalingskreditnotanr.**

> [!NOTE]  
> Du kan bruge samme nummerserie til forudbetalingsfakturaer som til almindelige fakturaer, eller du kan bruge forskellige serier. Hvis du bruger forskellige serier, må der ikke være ens numre i serierne; dvs. numre, der optræder i begge serier.  

## <a name="to-set-up-prepayment-percentages-for-items-customers-and-vendors"></a>Sådan opretter forudbetalingsprocenter til varer, debitorer og kreditorer

Hvis du opretter en standardforudbetalingsprocent til en vare, kan den bruges til alle kunder, en bestemt kunde eller en debitorprisgruppe. Hvis du ikke vil anvende den samme forudbetalingsprocent på alle debitorer, skal du angive, hvilke debitorer, eller hvilke debitorprisgrupper forudbetalingsprocenten gælder for.

1. Vælg ![Lightbulb, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **Varer**, og vælg derefter det relaterede link.
2. Markér en vare, og vælg derefter handlingen **Forudbetalingsprocenter**.  
3. På siden **Forudbetalingsprocenter - salg** skal du udfylde felter efter behov. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

Til en kunde eller leverandør kan du oprette én standardforudbetalingsprocent, der gælder for alle varer og alle former for salgslinjer. Du angiver dette på debitor- eller kreditorkortet. Følgende procedure viser, hvordan du angiver en forudbetalingsprocent for en debitor, men lignende trin gælder for kreditorer.  

1. Vælg ikonet ![Lightbulb, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **Kunder**, og vælg derefter det relaterede link.
2. Åbn kortet for en debitor.
3. Udfyld feltet **Forudbetaling i %**.
4. Gentag trinene for andre debitorer eller for kreditorer.  

> [!TIP]
> Du kan også få adgang til siden **Forudbetalingsprocenter - salg** fra debitor-eller kreditorkortet.

### <a name="to-determine-which-prepayment-percentage-has-first-priority"></a>Sådan afgøres det, hvilken forudbetalingsprocent der har højeste prioritet  

I en ordre kan der være én forudbetalingsprocent i salgshovedet og en anden procent for varerne på linjerne. For at afgøre, hvilken forudbetalingsprocent der gælder for hver enkelt salgslinje, søger systemet efter forudbetalingsprocenten i følgende rækkefølge, hvorefter den første standardprocent, der bliver fundet, anvendes:  

1. En forudbetalingsprocent for varen på linjen og for den kunde, som ordren vedrører.  
2. En forudbetalingsprocent for varen på linjen og for den debitorprisgruppe, som kunden tilhører.  
3. En forudbetalingsprocent for varen på linjen for alle kunder.  
4. Forudbetalingsprocenten i salgs- eller købshovedet.  

Med andre ord bruges forudbetalingsprocenten på kundekortet kun, hvis der ikke er oprettet andre forudbetalingsprocenter for varen. Hvis du ændrer indholdet i feltet **Forudbetaling i %** i salgs- eller købshovedet, efter linjerne er oprettet, opdateres forudbetalingsprocenten dog på alle linjer. Det gør det nemt at oprette en ordre med en fast forudbetalingsprocent, uanset hvilken procent der er oprettet for varerne.

## <a name="see-also"></a>Se også  

[Fakturere forudbetalinger](finance-invoice-prepayments.md)  
[Gennemgang: Opsætning og fakturering af salgsforudbetalinger](walkthrough-setting-up-and-invoicing-sales-prepayments.md)  
[Beregne moms af varer og ydelser på forudbetalinger i Australien](LocalFunctionality/Australia/how-to-calculate-goods-and-services-tax-on-prepayments.md)  
[Beregne moms af varer og ydelser på forudbetalinger i New Zealand](LocalFunctionality/NewZealand/how-to-calculate-goods-and-services-tax-on-prepayments.md)  
[Om Finans og kontoplanen](finance-general-ledger.md)  
[Finans](finance.md)  
[Arbejde med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]