---
title: Oprette bankkonti (indeholder video)
description: Få mere at vide om, hvordan bankkonti bruges i Business central, og hvordan du kan afstemme beløb med din bank.
author: brentholtorf
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: Yodlee, feed, stream
ms.search.form: 370, 371, 372, 373, 375, 423, 424, 425, 426, 1240, 1280
ms.date: 01/24/2022
ms.author: edupont
ms.openlocfilehash: af48197d84407fc16e103991852f98fa0338bf9e
ms.sourcegitcommit: 00a8acc82cdc90e0d0db9d1a4f98a908944fd50a
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 06/29/2022
ms.locfileid: "9078774"
---
# <a name="set-up-bank-accounts"></a>Sådan oprettes bankkonti

Brug bankkonti i [!INCLUDE[prod_short](includes/prod_short.md)] til at holde styr på dine banktransaktioner. Konti kan være i den lokale valuta eller i fremmed valuta. Når du har oprettet bankkonti, kan du også bruge funktionen til kontrol af udskrevne check. Bankkontiene indeholder ekstra funktionalitet til [afstemning af betaling](receivables-apply-payments-auto-reconcile-bank-accounts.md), [Bankafstemning](bank-how-reconcile-bank-accounts-separately.md) og import og eksport af bankfiler. Bankkonti kan også medtages i transaktioner i finanskladder. Hver bankkonto er knyttet til en konto i kontoplanen via den tildelte Bankbogføringsgruppe. Hvis du bruger en bankkonto i en betalingstransaktion, oprettes der automatisk en post på både bankkontoen og den tilknyttede finanskonto.  

Bank konti fungerer forskelligt, afhængigt af om der er angivet en valutakode:

- Valutakode er tomt

  Alle transaktioner i bankkontoen bliver i lokal valuta (RV) for det aktuelle regnskab. Hvis der foretages en transaktion til kontoen i en anden valuta, bogføres beløbene på kontoen i RV baseret på den relevante valutakurs. Alle checks, der udstedes fra denne konto, skal udstedes i den relevante regnskabsvaluta. Hvis bankkontoen bruges i en kladde, vil kladdelinjen automatisk arve den tomme valutakode.  
- Angiver en valutakode.

  Alle de transaktioner, der foretages på kontoen, skal være i samme valuta som angivet på kontoen. Alle de checks, der udstedes fra denne konto, skal også have denne valuta.  

Du kan spare tid på dataindtastning ved at gøre en bankkonto til den valuta, der er angivet for kontoen. Hvis du gør det, tildeles kontoen til salgs-og servicedokumenter, der bruger valutaen. Hvis kontoen skal være standard for salgs-og servicedokumenter, skal du aktivere funktionen **Brug som standard for valuta** på siden **bankkontokort**. Hvis det er nødvendigt, kan du vælge en anden konto, når du arbejder med et dokument.

En bankkonto er en integreret del af [!INCLUDE[prod_short](includes/prod_short.md)] og spiller en rolle i mange andre muligheder. Følgende illustration viser de vigtigste relationer:

![Illustration af bankkonto relationer.](media/Set-Up-Bank-Accounts/Bank_Account_Relations.png)

Det betyder, at du opretter en bankkonto, gør den tilgængelig på alle de steder, der vises ovenfor, og som er spejlet i for den relevante finanskonto og på siden med **firmaoplysninger**.

En bankkonto overvåges som regel dagligt for at sikre, at alle nye betalinger fra debitorer registreres så hurtigt som muligt. Det er med til at sikre, at den faktiske status for kunderne afspejles i [!INCLUDE[prod_short](includes/prod_short.md)], så sælgere, bogholdere og andre medarbejdere har adgang til relevante og opdaterede oplysninger. På den måde undgår du unødvendige opkald til kunden om forfaldne fakturaer eller forsinkelser i leverancer.  

![Illustration af bankbetaling.](media/Set-Up-Bank-Accounts/Bank-payment-flow.png)

En anden opgave er at importere kreditor valuta betalinger med de realiserede valutakurser for at sikre, at kreditorens faktiske status er opdateret. Den nemmeste måde at sikre, at bankkontoen er opdateret på, er at bruge funktionen til [afstemning af betalinger](receivables-apply-payments-auto-reconcile-bank-accounts.md). I **kladden til afstemning af betaling** kan du indlæse banktransaktioner direkte fra en online bank ansøgning og få dem bogført mere eller mindre automatisk. Kladden identificerer og bogfører automatisk følgende:  

- Direkte debetbetalinger fra debitorer  
- Debitorbetalinger af enkelt fakturaer  
- Registrerer engangsbetalinger fra kunder.  
- Debitorbetalinger i udenlandske valutaer  
- Kreditorbetalinger  
- Kreditorbetalinger i udenlandske valutaer  
- Tilbagevendende kreditorbetalinger og abonnementer  
- Bankgebyrer og-interesser  

Betalingsafstemning giver enorme tidsbesparelser ved bogføring af indgående og udgående betalinger. Men transaktionerne på bankkontoen i [!INCLUDE[prod_short](includes/prod_short.md)] er ikke registreret som 100 % korrekte, før du starter en bankafstemning.  

Bankafstemning er den måde, du sørger for, at bankkontoen [!INCLUDE[prod_short](includes/prod_short.md)] stemmer overens med bankens eksterne konto.  

 ![Illustration af bankkontoafstemning.](media/Set-Up-Bank-Accounts/BankReconciliation.png)

I illustrationen ovenfor repræsenterer venstre side bankkontoen i [!INCLUDE[prod_short](includes/prod_short.md)], og den højre side repræsenterer de transaktioner, der er indlæst fra banken gennem online-bankansøgningen. Diagrammet i midten viser transaktionerne fra begge sider, som er bankafstemningen.

Fra en bankkonto [!INCLUDE[prod_short](includes/prod_short.md)], skal de fleste transaktioner bekendtgøres til den fysiske bank. De eneste undtagelser omfatter følgende:  

- Rettelser bogført i [!INCLUDE[prod_short](includes/prod_short.md)]  
- Udstedte checks, der endnu ikke er blevet kontanter  
- Kreditorbetalinger, som ikke er godkendt af banken  

Ukendte transaktioner, der ikke blev identificeret i betalings afstemningskladden, modtages fra den fysiske konto i banken hele tiden, f. eks. følgende:  

- Nye kreditorabonnementer  
- Debitorbetalinger uden beskrivelse
- Bankinteresser
- Bankafgifter
- Kreditkortgebyrer, der endnu ikke er rapporteret

De bedre tilknytningsoplysninger, du foretager i betalings afstemningskladden, bogføres flere transaktioner automatisk, og den letteste bankafstemning bliver.

<br><br>

> [!Video https://www.microsoft.com/videoplayer/embed/RE3Vhpl?rel=0]

<br><br>

> [!WARNING]
> Nogle felter kan indeholde følsomme data, f. eks. **Bankforgreningsnr.**, **bankkontonummer**, **SWIFT-kode** og **IBAN-kode**. Du kan finde flere oplysninger i [Overvågning af følsomme felter](across-log-changes.md#monitoring-sensitive-fields).

## <a name="to-set-up-bank-accounts"></a>Sådan oprettes bankkonti

1. Vælg ![Lightbulb, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **Bankkonti**, og vælg derefter det relaterede link.
2. På siden **Bankkonti** skal du vælge handlingen **Ny**.
3. Udfyld felterne efter behov. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

    F.eks. forbindes feltet **Bankbogføringsgruppe** med bankkontoen til den underliggende finanskonto i balancen. Du kan finde flere oplysninger i [Opsætning af bogføringsgrupper](finance-posting-groups.md).

> [!TIP]
> Nogle felter er skjult, indtil du vælger handlingen **Vis flere**, typisk fordi de bruges sjældent. Andre skal tilføjes via brugertilpasning. Du kan finde flere oplysninger i [Tilpasse dit arbejdsområde](ui-personalization-user.md).

Du kan oprette et ubegrænset antal bankkonti til virksomheden. For hver bankkonto skal du angive oplysninger, der gør bankkontoen entydig identificerbar. Disse oplysninger omfatter bankens geografiske adresse, nummerserie for forskellige typer transaktioner, f. eks. direkte debet-og kreditoverførsler, den valuta, som beløbene er angivet i, og oplysninger, der bruges til at indlæse bankkontoudtog. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
<!--
The following table explains key fields.

|Field|Description|  
|---------------------------------|---------------------------------------|  
|**General FastTab**||
|No.|Specifies the number of the bank account, according to the specified number series. If the number series allow manual numbering, any alphanumeric code up to 20 characters can be used.|
|Name|The Name of the bank holding the bank account.|
|Bank Branch No.|The Bank Branch No. is usually used to identify the bank branch in domestic payments. The Bank Branch No. is very often considered a sensitive field. Read more about [Monitoring Sensitive Fields](across-log-changes.md#monitoring-sensitive-fields).|
|Bank Account No.|Bank Account No. is usually used to identify the bank account no. in domestic payments. The Bank Account No. is very often considered a sensitive field. Read more about [Monitoring Sensitive Fields](across-log-changes.md#monitoring-sensitive-fields).|
|Balance|Shows the Balance of the bank account in the account currency.|
|Balance (LCY)|Shows the Balance of the bank account in the local currency (LCY).|
|Our Contact Code|Specifies a code to specify the employee who is responsible for this bank account. The employee must be created in the **Salesperson/Purchaser** table.|
|Blocked|Specifies that the related record is blocked from being posted in transactions, for example the account is obsolete after a bank change.|
|SEPA Direct Debit Exp. Format|Specifies the SEPA format of the bank file that will be exported when you choose the **Create Direct Debit File** button in the **Direct Debit Collect. Entries** window. Read more in [SEPA Direct Debit in Business Central](finance-collect-payments-with-sepa-direct-debit.md).|
|Credit Transfer Msg. Nos.|Specifies the number series for bank instruction messages that are created with the export file that you create from the Direct Debit Collect. Entries window. Read more in [SEPA Direct Debit in Business Central](finance-collect-payments-with-sepa-direct-debit.md).|
|Direct Debit Msg. Nos.|Specifies the number series that will be used on the direct debit file that you export for a direct-debit collection entry in the Direct Debit Collect. Entries window. Read more in [SEPA Direct Debit in Business Central](finance-collect-payments-with-sepa-direct-debit.md).|
|Creditor No.|Specifies your company as the creditor in connection with payment collection from customers using SEPA Direct Debit. Read more in [SEPA Direct Debit in Business Central](finance-collect-payments-with-sepa-direct-debit.md).|
|Bank Clearing Standard|The national bank names register used for the sender bank account.|
|Bank Clearing Code|Specifies the code for bank clearing that is required according to the format standard that you selected in the Bank Clearing Standard field. The bank clearing code can be used as an alternative to SWIFT and IBAN to identify your bank as sender of a bank transfer.|
|Last Date Modified|Date of the latest modification of the bank account.|
|**Payment Matching**||
|Disable Automatic Payment Matching|Specifies whether to disable automatic payment matching after importing bank transactions for this bank account. Read more in [Payment Reconciliation](receivables-apply-payments-auto-reconcile-bank-accounts.md).|
|**Payment Match Tolerance**||
|Match Tolerance Type|Specifies by which tolerance the automatic payment application function will apply the Amount Incl. Tolerance Matched rule for this bank account. Read more in [Payment Reconciliation](receivables-apply-payments-auto-reconcile-bank-accounts.md).|
|Match Tolerance Value|Specifies if the automatic payment application function will apply the Amount Incl. Tolerance Matched rule by Percentage or Amount. Read more in [Payment Reconciliation](receivables-apply-payments-auto-reconcile-bank-accounts.md).|
|**Hidden Fields**||
|Search Name|Specifies an alternate name that you can use to search for the record in question when you cannot remember the value in the Name field.|
|Min. Balance|Specifies a minimum balance for the bank account. This field is for information purposes only.|
|Positive Pay Export Code|Specifies a code for the data exchange definition that manages the export of positive-pay files. Read more in [Export Positive Pay Files](finance-how-positive-pay.md).|
|**Communication FastTab**||
|Address|The address of the bank branch.|
|Address 2|An additional address field for the bank branch.|
|Post Code|The post code of the bank branch.|
|City|The city of the bank branch.|
|Country/Region Code|The Country/Region Code of the bank branch.|
|Phone No.|The Phone No. of the bank branch.|
|Mobile Phone No.|The Mobile Phone No. of the bank branch.|
|Contact|The main contact in the bank branch. Additional contacts can be created in the Contacts module.|
|Fax No.|The Fax No. of the bank branch.|
|Email|The Email of the bank branch.|
|Home Page|The Home Page of the bank branch.|
|**Posting FastTab**||
|Currency Code|Specifies the relevant currency code for the bank account. Applying a currency code to a bank account will limit all transactions to only use the applied currency code. Leaving the currency code blank will allow transactions in all currencies, however, the amount will be converted to the local currency (LCY) using the applied currency rate. Checks issued from this account will also follow the same rules.|
|Last Check No.|The number of the latest check issued from this account.|
|Transit No.|Specifies a bank identification number of your own choice.|
|Last Statement No.|The number of the latest bank reconciliation posted to this account. Read more in [Reconcile Bank Accounts](bank-how-reconcile-bank-accounts-separately.md).|
|Last Payment Statement No.|The number of the latest payment reconciliation posted to this account. Read more in [Payment Reconciliation](receivables-apply-payments-auto-reconcile-bank-accounts.md).|
|Last Bank Statement|The ending-balance of the last bank statement. Read more in [Reconcile Bank Accounts](bank-how-reconcile-bank-accounts-separately.md).|
|Bank Acc. Posting Group|Specifies a code for the bank account posting group for the bank account. The Bank Acc. Posting Group connects the bank account to the G/L Account in the balance sheet.|
|**Transfer**||
|Transit No.|Specifies a bank identification number of your own choice.|
|SWIFT Code|Specifies the international bank identifier code (SWIFT) of the bank where you have the account. The SWIFT Code is very often considered a sensitive field. Read more about [Monitoring Sensitive Fields](across-log-changes.md#monitoring-sensitive-fields).|
|IBAN|Specifies the bank account's international bank account number. The IBAN Code is very often considered a sensitive field. Read more about [Monitoring Sensitive Fields](across-log-changes.md#monitoring-sensitive-fields).|
|Bank Statement Import Format|Specifies the format of the bank statement file that can be imported into this bank account. The format is being used in both the payment reconciliation journals and the bank account reconciliations.|
|Payment Export Format|Specifies the format of the bank file that will be exported when you choose the Export Payments to File button in the Payment Journal window.|
-->

## <a name="entering-an-opening-balance"></a>Angive en primosaldo

For at udfylde feltet **Saldo** med en startsaldo, skal du bogføre en bankkontopost med det pågældende beløb. Du kan gøre dette ved at udføre en afstemning af bankkontoen. Du kan finde flere oplysninger i [Afstemme bankkonti](bank-how-reconcile-bank-accounts-separately.md).  
>
> Du kan også implementere primosaldoen som en del af oprettelse af generelle oplysninger i nye virksomheder ved hjælp af den assisterede opsætningsvejledning **Overflyt virksomhedsdata** . Du kan finde flere oplysninger i [Blive køreklar](ui-get-ready-business.md).  

> [!IMPORTANT]
> Det er vigtigt, at du ikke bogfører primosaldoen direkte i finansregnskabet. Hvis der er poster i finanskontoen, som bogføres direkte på finanskontoen, betyder det som regel, at du ikke kan afstemme bankkontoen, eller, hvis der er tale om bankkonti for udenlandsk valuta, samles differencer, når du bogfører flere bankkontoafstemninger. Du bogfører ofte primosaldoen direkte på bankkontoen, og beløbet ophører derefter med finanskontoen. Alternativt kan du tilbageføre den senere til en angivet finanskonto, som du har brugt til at afstemme primosaldoen med finansbalancen. I begge tilfælde skal du udligne en direkte bogføring til finanskontoen, før du starter din første bankafstemning, og især hvis bankkontoen er i udenlandsk valuta.

## <a name="to-set-up-your-bank-account-for-import-or-export-of-bank-files"></a>Sådan oprettes bankkontoen for import eller eksport af bankfiler

Felterne er relateret til indlæsning og udlæsning af bankfeeds og -filer i oversigtspanelet **Overførsel** på siden **Bankkontokort**. Du kan finde flere oplysninger i [Bruge AMC Banking 365 Fundamentals-udvidelsen](ui-extensions-amc-banking.md) og [Konfigurere tjenesten Envestnet Yodlee Bank Feeds](bank-how-setup-bank-statement-service.md).

1. Vælg ![Lightbulb, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **Bankkonti**, og vælg derefter det relaterede link.
2. Åbn kortet for en bankkonto, du vil eksportere eller importere bankfiler for.
3. Udfyld felterne efter behov i oversigtspanelet **Overførsel**. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

> [!NOTE]  
> Andre fileksporttjenester og deres formater kræver andre konfigurationsværdier på siden **Bankkontokort**. Du får information om forkerte eller manglende konfigurationsværdier, når du prøver at eksportere filen. Læs omhyggeligt korte beskrivelser af felterne, eller se de relaterede emner med fremgangsmåder. Eksport af en betalingsfil med f.eks. nordamerikansk elektronisk pengeoverførsel (EFT) kræver, at både **Sidste remitteringsadvisnr.** og **Transitnr.** er udfyldt. Du kan finde flere oplysninger i [Eksportere betalinger til en bankfil](finance-make-payments-with-bank-data-conversion-service-or-sepa-credit-transfer.md#exporting-payments-to-a-bank-file).

Felterne i oversigtspanelet **Transit** på bankkontoen tjener forskellige formål, afhængigt af om betalingen er indadgående eller udadgående.

Illustrationen viser ruten af indgående betalinger:

:::row:::
    :::column:::
        1. Transaktionerne udlæses fra bankkontoen i enten et personligt læsbart. csv-format eller bankens eget format.
        <br><br>
2. *Dataudvekslingsdefinition* knytter oplysningerne i filen til felterne i [!INCLUDE[prod_short](includes/prod_short.md)]. Du kan finde flere oplysninger i [Konfigurere dataudveksling](across-set-up-data-exchange.md)
<br><br>
3. I *opsætningen af dataeksport/import* defineres eksporten eller importen, og den er kædet sammen med data udvekslingsdefinitionen.
<br><br>
4. *Bankkontoudtogsimportformat* knytter importopsætningen til bankkontoen.
<br><br>
5. Betalingerne indlæses via **kladden til afstemning af betaling** eller **Bankkontoafstemning**.
    :::column-end:::
    :::column:::
        ![Illustration af betalinger, der er modtaget fra banken til bankkonti.](media/Set-Up-Bank-Accounts/payments-in-and-out-1.png)
    :::column-end:::
:::row-end:::

Indgående betalinger indlæses altid via **kladden til afstemning af betaling** eller direkte i **Bankkontoafstemning**. Udgående betalinger kan derimod stamme fra enhver betalingskladde. Den eneste forudsætning er, at feltet **Tillad kontant eksport** i den relevante Udbetalingskladde navn skal markeres.

Illustrationen viser ruten af udgående betalinger:

:::row:::
    :::column:::
        6. De transaktioner, der er udfyldt i en Udbetalingskladde, som er blevet forberedt på udlæsning af betalinger til fil.
        <br><br>
        7. *Bankkontoudtogsimportformat* knytter importopsætningen til bankkontoen.
        <br><br>
        8. I *opsætningen af dataeksport/import* defineres eksporten eller importen og links, og den er kædet sammen med data udvekslingsdefinitionen.
        <br><br>
        9. *Dataudvekslingsdefinition* knytter oplysningerne i filen til felterne i [!INCLUDE[prod_short](includes/prod_short.md)]. Du kan finde flere oplysninger i [Konfigurere dataudveksling](across-set-up-data-exchange.md)
        <br><br>
        10. Betalingerne udlæses fra udbetalingskladden og indlæses på bankkontoen
    :::column-end:::
    :::column:::
        ![Illustration af betalinger, der er modtaget fra banken til bankkonti.](media/Set-Up-Bank-Accounts/payments-in-and-out-2.png)
    :::column-end:::
:::row-end:::

## <a name="to-set-up-vendor-bank-accounts-for-export-of-bank-files"></a>Sådan konfigureres kreditorbankkonti til eksport af bankfiler

Felter i oversigtspanelet **Overførsel** på siden **Kreditors bankkontokort** er relateret til udlæsning af bankfeeds og -filer. Du kan finde flere oplysninger i [Brug AMC Banking 365 Fundamentals-udvidelsen](ui-extensions-amc-banking.md) og [Eksportere betalinger til en bankfil](finance-make-payments-with-bank-data-conversion-service-or-sepa-credit-transfer.md#exporting-payments-to-a-bank-file).

1. Vælg ![Lightbulb, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **Leverandører**, og vælg derefter det relaterede link.
2. Åbn kortet for en kreditor, hvis bankkonto du vil eksportere betalingsbankfiler til.
3. Vælg handlingen **Bankkonti**.
4. Vælg den relevante bankkonto på listen **Kreditorbankkonti**, eller tilføj en ny bankkonto.  
5. Udfyld felterne efter behov på siden **Kreditors bankkontokort** i oversigtspanelet **Overførsel**. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

> [!WARNING]
> Nogle felter på leverandørkontoen kan indeholde følsomme data, f. eks. **Bankforgreningsnr.**, **bankkontonummer**, **SWIFT-kode** og **IBAN-kode**. Du kan finde flere oplysninger i [Overvågning af følsomme felter](across-log-changes.md#monitoring-sensitive-fields).

## <a name="changing-your-bank-account"></a>Ændre din bankkonto

Hvis du vil bruge en anden bankkonto til din virksomhed, skal du oprette den nye bankkonto i [!INCLUDE[prod_short](includes/prod_short.md)]. Det anbefales, at du ikke blot erstatter oplysninger om den konto, du bruger i øjeblikket, da det kan medføre forkerte data. Primosaldoen kan f. eks. være forkert, eller din bank-feed fungerer muligvis ikke korrekt. Det er vigtigt, at du holder de aktuelle og nye firmaer adskilt.

Når du har oprettet den nye bankkonto, skal du også oprette en ny Bankbogføringsgruppe og knytte den til en ny finanskonto. Du kan genbruge en eksisterende Bankbogføringsgruppe, og bank transaktionerne bogføres til samme finanskonti som de andre bankkonti, der deler bank bogføringsgruppen. Det anbefales dog, at du opretter en ny Bankbogføringsgruppe og finanskonto, så det er nemmere at foretage afstemningen.

> [!NOTE]
> Bemærk, at bankkontooplysningerne på åbne salgsfakturaer stadig viser den oprindelige bankkonto. Derfor bogføres betalinger stadig på denne konto. Det anbefales, at du holder begge konti aktive i en periode efter ændringen.

Hvis du vil have en mere kompakt oversigt over dine kontantkonti i financial reporting, skal du bruge kontien **fra-sum** og **til-sum** i din kontoplan, **sammentælling af rækker** i kontoskemaer eller finanskontoarter. Du kan finde flere oplysninger i afsnittet om [Business Intelligence og financial reporting](bi.md).

## <a name="see-related-training-at-microsoft-learn"></a>Se relateret træning på [Microsoft Learn](/learn/modules/cash-management-dynamics-365-business-central/)

## <a name="see-also"></a>Se også

[Konfigurere banktransaktioner](bank-setup-banking.md)  
[Konfigurere bogføringsgrupper](finance-posting-groups.md)  
[Bankkontoafstemning](bank-manage-bank-accounts.md)  
[Konfigurere tjenesten Envestnet Yodlee Bank Feeds](bank-how-setup-bank-statement-service.md)  
[SEPA-direkte debitering i Business Central](finance-collect-payments-with-sepa-direct-debit.md)  
[Sådan konfigureres din bankkonto til SEPA-Direct Debit](finance-collect-payments-with-sepa-direct-debit.md#to-set-up-your-bank-account-for-sepa-direct-debit)  
[Sådan opsættes en konto til SEPA-kreditoverførsler](finance-make-payments-with-bank-data-conversion-service-or-sepa-credit-transfer.md#to-set-up-a-bank-account-for-sepa-credit-transfer)  
[Foretage betalinger med AMC Banking 365 Fundamentals -udvidelsen eller SEPA-kreditoverførsel](finance-make-payments-with-bank-data-conversion-service-or-sepa-credit-transfer.md)  
[Betalingsafstemning](receivables-apply-payments-auto-reconcile-bank-accounts.md)  
[Om Finans og kontoplanen](finance-general-ledger.md)  
[Arbejd med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]
