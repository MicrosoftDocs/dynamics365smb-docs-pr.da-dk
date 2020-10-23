---
title: Opsætte forudbetalinger | Microsoft Docs
description: Forudbetalinger faktureres og bogføres på en forudbetalingsordre for salg eller køb inden den endelige bogføring. Du kræver måske et depositum, inden du producerer varerne efter ordre, eller du kræver måske betaling, før du leverer varer til en kunde. Forudbetalingsfunktionen sætter dig i stand til at fakturere og opkræve depositum fra debitorer eller at sende depositummerne til kreditorer. På den måde kan du sikre, at alle betalinger bogføres i forhold til en faktura.
author: edupont04
ms.service: dynamics365-business-central
ms.topic: article
ms.search.keywords: prepayment
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: 7f8d0109b42eb75f022bac580c2bef006f311157
ms.sourcegitcommit: ddbb5cede750df1baba4b3eab8fbed6744b5b9d6
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 10/01/2020
ms.locfileid: "3914235"
---
# <a name="set-up-prepayments"></a>Oprette forudbetalinger
Hvis det er et krav, at dine kunder skal betale, før du leverer en ordre til dem, eller hvis din leverandør kræver, at du skal betale, før de sender en ordre til dig, kan du bruge forudbetalinger. Funktionen sætter dig i stand til at fakturere og opkræve depositum fra debitorer eller at sende depositummerne til kreditorer og til at sikre, at alle delvise betalinger bogføres i forhold til en faktura. Du kan finde flere oplysninger i [Oprette forudbetalingsfakturaer](finance-how-to-create-prepayment-invoices.md).

Inden du kan bogføre forudbetalingsfakturaer, skal du oprette bogføringskonti i finansposterne, og du skal oprette nummerserier for forudbetalingsdokumenterne. Du skal angive en konto til forudbetalinger, der vedrører salg, og en konto til forudbetalinger, der vedrører køb. Du kan angive de samme bogføringskonti, der skal bruges til alle forudbetalinger, der vedrører alle virksomhedsbogføringsgrupper eller generelle produktbogføringsgrupper, eller du kan angive bestemte konti til bestemte bogføringsgrupper til henholdsvis salg og køb. Dette afhænger af virksomhedens krav til sporing af forudbetalinger.  

Du kan definere den procentdel af linjebeløbet, der skal faktureres for forudbetaling - for en debitor eller kreditor, for alle varer eller udvalgte varer. Når du har fuldført opsætningen, kan du generere forudbetalingsfakturaer fra salgs- og købsordrer. Du kan bruge standardprocenterne for hver salgs- eller indkøbslinje, eller du kan ændre beløbene efter behov. Du kan f.eks. angive et samlet beløb for hele ordren.  

> [!NOTE]
> Det anbefales, at du ikke bruger en forudbetalingsprocent på 100 % i følgende tilfælde:
> * Hvis du befinder dig i Nordamerika. Grundet beregningsmåden for moms kan en forudbetalingsprocent på 100 % medføre problemer med forudbetalingsfakturaer.
> * I alle områder hvis du manuelt fratrækker en kontantrabat fra fakturaen. Vil en forudbetalingsprocent på 100 % ikke automatisk efterlade et beløb, hvorfra rabatten skal fratrækkes. 

Eftersom det forudbetalte beløb tilhører køberen, indtil han har modtaget varerne eller tjenesteydelsen, er du nødt til at oprette finanskonti, som forudbetalte beløb kan indsættes på, indtil den endelige faktura bogføres. Salgsforudbetalinger skal registreres på en passivkonto, indtil varerne leveres. Købsforudbetalinger skal registreres på en aktivkonto, indtil varerne modtages. Du skal også oprette en separat finanskonto til hvert moms-id.  

[!INCLUDE[local-func-setup-link](includes/local-func-setup-link.md)]

## <a name="to-add-prepayment-accounts-to-the-general-posting-setup"></a>Sådan føjes forudbetalingskonti til bogføringsopsætning  

1. Vælg ikonet ![Elpære, der åbner funktionen Fortæl mig](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig"), angiv **Bogføringsopsætning**, og vælg derefter det relaterede link.
2. På siden **Bogføringsopsætning** skal du udfylde følgende felter:  

    - **Forudbetalingskonto for salg**  
    - **Forudbetalingskonto for køb**  

> [!TIP]
> Hvis du ikke kan se felterne på siden **Bogføringsopsætning**, skal du bruge det vandrette rullepanel nederst på siden til at rulle til højre.  

Hvis du ikke allerede har angivet finanskonti til forudbetalinger, kan du åbne siden **Finanskontooversigt** fra det relevante kontofelt.  

## <a name="to-set-up-number-series-for-prepayment-documents"></a>Sådan oprettes nummerserier til forudbetalingsdokumenter  

1. Vælg ikonet ![Elpære, der åbner funktionen Fortæl mig](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig"), angiv **Salgsopsætning**, og vælg derefter det relaterede link.
2. På siden **Salgsopsætning** skal du udfylde følgende felter:  

   - **Bogførte forudbetalingsfakturanr.**
   - **Bogførte forudbetalingskreditnotanr.**

1. Vælg ikonet ![Elpære, der åbner funktionen Fortæl mig](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig"), angiv **Købsopsætning**, og vælg derefter det relaterede link.
2. På siden **Købsopsætning** skal du udfylde følgende felter:

    - **Bogførte forudbetalingsfakturanr.**
    - **Bogførte forudbetalingskreditnotanr.**

> [!NOTE]  
> Du kan bruge samme nummerserie til forudbetalingsfakturaer som til almindelige fakturaer, eller du kan bruge forskellige serier. Hvis du bruger forskellige serier, må der ikke være ens numre i serierne; dvs. numre, der optræder i begge serier.  

## <a name="to-set-up-prepayment-percentages-for-items-customers-and-vendors"></a>Sådan opretter forudbetalingsprocenter til varer, debitorer og kreditorer  
Hvis du opretter en standardforudbetalingsprocent til en vare, kan den bruges til alle kunder, en bestemt kunde eller en debitorprisgruppe.  

1. Vælg ikonet ![Elpære, der åbner funktionen Fortæl mig](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig"), angiv **Varer**, og vælg derefter det relaterede link.
2. Markér en vare, og vælg derefter handlingen **Forudbetalingsprocenter**.  
3. På siden **Forudbetalingsprocenter - salg** skal du udfylde felter efter behov. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

Til en kunde eller leverandør kan du oprette én standardforudbetalingsprocent, der gælder for alle varer og alle former for salgslinjer. Du angiver dette på debitor- eller kreditorkortet.

1. Vælg ikonet ![Elpære, der åbner funktionen Fortæl mig](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig"), angiv **Debitorer**, og vælg derefter det relaterede link.
2. Åbn kortet for en debitor.
3. Udfyld feltet **Forudbetaling i %**.
4. Gentag trinene for andre debitorer eller for kreditorer.  

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
[Arbejde med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)
