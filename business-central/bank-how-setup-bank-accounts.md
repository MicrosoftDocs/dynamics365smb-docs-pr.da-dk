---
title: Oprette bankkonti (indeholder video)
description: 'Få mere at vide om, hvordan bankkonti bruges i Business central, og hvordan du kan afstemme beløb med din bank.'
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bnielse
ms.topic: conceptual
ms.search.keywords: 'Yodlee, feed, stream'
ms.search.form: '370, 371, 372, 373, 375, 423, 424, 425, 426, 1240, 1280'
ms.date: 08/03/2023
ms.custom: bap-template
ms.service: dynamics-365-business-central
---
# <a name="set-up-bank-accounts"></a>Sådan oprettes bankkonti

Brug bankkonti i [!INCLUDE[prod_short](includes/prod_short.md)] til at holde styr på dine banktransaktioner. Konti kan være i den lokale valuta eller i fremmed valuta. Når du har oprettet bankkonti, kan du også bruge funktionen til kontrol af udskrevne check. Bankkontiene indeholder ekstra funktionalitet til [afstemning af betaling](receivables-apply-payments-auto-reconcile-bank-accounts.md), [Bankafstemning](bank-how-reconcile-bank-accounts-separately.md) og import og eksport af bankfiler. Bankkonti kan også medtages i transaktioner i finanskladder. Hver bankkonto er knyttet til en konto i kontoplanen via den tildelte Bankbogføringsgruppe. Hvis du bruger en bankkonto i en betalingstransaktion, oprettes der automatisk en post på både bankkontoen og den tilknyttede finanskonto.  

Bank konti fungerer forskelligt, afhængigt af om der er angivet en valutakode:

- Hvis valutakoden er tom

  Alle transaktioner i bankkontoen er i lokal valuta (RV) for det aktuelle regnskab. Hvis der foretages en transaktion til kontoen i en anden valuta, bogføres beløbene på kontoen i RV baseret på den relevante valutakurs. Alle checks, der udstedes fra denne konto, skal udstedes i den lokale valuta. Hvis bankkontoen bruges i en kladde, vil kladdelinjen automatisk arve den tomme valutakode.  
  
- Angiver en valutakode.

  Alle transaktioner til og checks udstedt fra kontoen skal være i samme valuta som angivet på kontoen.

Du kan spare tid på dataindtastning ved at gøre en bankkonto til den valuta, der er angivet for kontoen. Hvis du gør det, tildeles kontoen salgs-og servicedokumenter, der bruger valutaen. Hvis kontoen skal være standard for salgs-og servicedokumenter, skal du aktivere funktionen **Brug som standard for valuta** på siden **bankkontokort**. Hvis det er nødvendigt, kan du vælge en anden konto, når du arbejder med et dokument.

En bankkonto er en integreret del af [!INCLUDE[prod_short](includes/prod_short.md)] og spiller en rolle i mange andre funktioner. Følgende illustration viser de vigtigste relationer:

![Illustration af bankkonto relationer.](media/Set-Up-Bank-Accounts/Bank_Account_Relations.png)

Du kan se, at oprettelse af en bankkonto gør den tilgængelig på alle de steder, der vises ovenfor, og som er afspejlet i den relevante finanskonto og på siden med **Virksomhedsoplysninger**.

En bankkonto overvåges som regel dagligt for at sikre, at alle nye betalinger fra debitorer registreres så hurtigt som muligt. Dermed sikres det, at en kundes faktiske status afspejles i [!INCLUDE[prod_short](includes/prod_short.md)]. Det giver sælgere, bogholdere og andre medarbejdere adgang til de mest relevante og opdaterede oplysninger, så de undgår overflødige opkald til kunden om forfaldne fakturaer eller forsinkelser i leverancerne.  

![Illustration af bankbetaling.](media/Set-Up-Bank-Accounts/Bank-payment-flow.png)

En anden opgave er at importere kreditorvalutabetalinger med de realiserede valutakurser for at sikre, at kreditorens faktiske status er opdateret. Det er nemmest at bruge [funktionen til afstemning af betalinger](receivables-apply-payments-auto-reconcile-bank-accounts.md). I **kladden til afstemning af betaling** kan du indlæse banktransaktioner direkte fra en online bank ansøgning og få dem bogført mere eller mindre automatisk. Kladden identificerer og bogfører automatisk følgende:  

- Direkte debetbetalinger fra debitorer  
- Debitorbetalinger af enkelt fakturaer  
- Registrerer engangsbetalinger fra kunder.  
- Debitorbetalinger i udenlandske valutaer  
- Kreditorbetalinger  
- Kreditorbetalinger i udenlandske valutaer  
- Tilbagevendende kreditorbetalinger og abonnementer  
- Bankgebyrer og-interesser  

Betalingsafstemning giver store tidsbesparelser ved bogføring af indgående og udgående betalinger. Men transaktionerne på bankkontoen i [!INCLUDE[prod_short](includes/prod_short.md)] er ikke registreret som 100 % korrekte, før du starter en bankafstemning.  

Bankafstemning er den måde, du sørger for, at bankkontoen [!INCLUDE[prod_short](includes/prod_short.md)] stemmer overens med bankens eksterne konto.  

 ![Illustration af bankkontoafstemning.](media/Set-Up-Bank-Accounts/BankReconciliation.png)

I illustrationen ovenfor repræsenterer venstre side bankkontoen i [!INCLUDE[prod_short](includes/prod_short.md)], og den højre side repræsenterer de transaktioner, der er indlæst fra banken gennem online-bankansøgningen. Diagrammet i midten viser transaktionerne fra begge sider, som er bankafstemningen.

Fra en bankkonto [!INCLUDE[prod_short](includes/prod_short.md)], skal de fleste transaktioner bekendtgøres til den fysiske bank. De få undtagelser omfatter følgende:  

- Rettelser bogført i [!INCLUDE[prod_short](includes/prod_short.md)]  
- Udstedte checks, der endnu ikke er blevet indløst 
- Kreditorbetalinger, som ikke er godkendt af banken  

Transaktioner, der ikke blev identificeret i betalingsudligningskladden, modtages fra den fysiske konto i banken hele tiden, f.eks. følgende:  

- Nye kreditorabonnementer  
- Debitorbetalinger uden beskrivelse
- Bankrente
- Bankgebyrer
- Kreditkortgebyrer, der endnu ikke er rapporteret

Jo bedre du tilknytter oplysninger i betalingsudligningskladden, jo flere transaktioner bogføres automatisk, og jo lettere bliver regelmæssig bankafstemning.

Se i videoen herunder de grundlæggende trin til oprettelse af en bankkonto i [!INCLUDE[prod_short](includes/prod_short.md)].

<br /><br />

> [!Video https://www.microsoft.com/videoplayer/embed/RE3Vhpl?rel=0]

> [!WARNING]
> Nogle felter kan indeholde følsomme data, f. eks. **Bankforgreningsnr.**, **bankkontonummer**, **SWIFT-kode** og **IBAN-kode**. Flere oplysninger i [Overvåge følsomme felter](across-log-changes.md#monitor-sensitive-fields).

## <a name="to-set-up-bank-accounts"></a>Sådan oprettes bankkonti

1. Vælg ![Lightbulb, der åbner funktionen Fortæl mig 1.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **Bankkonti**, vælg derefter det relaterede link.
2. På siden **Bankkonti** skal du vælge handlingen **Ny**.
3. Udfyld felterne efter behov. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

    F.eks. forbindes feltet **Bogføringsgruppe til bankkonto** med bankkontoen til den underliggende finanskonto i balancen. Flere oplysninger i [Konfigurere bogføringsgrupper](finance-posting-groups.md).

> [!TIP]
> Nogle felter er skjult, indtil du vælger handlingen **Vis flere**, typisk fordi de bruges sjældent. Andre skal tilføjes via brugertilpasning. Flere oplysninger i [Tilpasse dit arbejdsområde](ui-personalization-user.md).

Du kan oprette et ubegrænset antal bankkonti til virksomheden. For hver bankkonto skal du angive oplysninger, der gør bankkontoen entydig identificerbar. Disse oplysninger omfatter bankens geografiske adresse, nummerserie for forskellige typer transaktioner, f. eks. direkte debet-og kreditoverførsler, den valuta, som beløbene er angivet i, og oplysninger, der bruges til at indlæse bankkontoudtog. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
<!--
The following table explains key fields.

|Field|Description|  
|---------------------------------|---------------------------------------|  
|**General FastTab**||
|No.|Specifies the number of the bank account, according to the specified number series. If the number series allow manual numbering, any alphanumeric code up to 20 characters can be used.|
|Name|The Name of the bank holding the account.|
|Bank Branch No.|Typically used to identify the bank branch in domestic payments, it's very often considered a sensitive field. Learn more at [Monitoring Sensitive Fields](across-log-changes.md#monitoring-sensitive-fields).|
|Bank Account No.|Typically used to identify the bank account number in domestic payments, it's very often considered a sensitive field. Learn more at [Monitoring Sensitive Fields](across-log-changes.md#monitoring-sensitive-fields).|
|Balance|Shows the bank account balance in the account currency.|
|Balance (LCY)|Shows the bank account balance in the local currency (LCY).|
|Our Contact Code|Specifies a code to identify the employee responsible for this bank account. The employee must be created in the **Salesperson/Purchaser** table.|
|Blocked|Specifies the related record is blocked from being posted in transactions, for example the account is obsolete after a bank change.|
|SEPA Direct Debit Exp. Format|Specifies the single euro payments area (SEPA) format of the bank file to be exported when you choose **Create Direct Debit File** on the **Direct Debit Collect. Entries** page. Learn more at [SEPA Direct Debit in Business Central](finance-collect-payments-with-sepa-direct-debit.md).|
|Credit Transfer Msg. Nos.|Specifies the number series for bank instruction messages created with the export file you create from the **Direct Debit Collect. Entries** page. Learn more at [SEPA Direct Debit in Business Central](finance-collect-payments-with-sepa-direct-debit.md).|
|Direct Debit Msg. Nos.|Specifies the number series to be used on the direct debit file you export for a direct debit collection entry on the **Direct Debit Collect. Entries** page. Learn more at [SEPA Direct Debit in Business Central](finance-collect-payments-with-sepa-direct-debit.md).|
|Creditor No.|Specifies your company as the creditor in connection with payment collection from customers using SEPA direct debit. Learn more at [SEPA Direct Debit in Business Central](finance-collect-payments-with-sepa-direct-debit.md).|
|Bank Clearing Standard|The national bank names register used for the sender bank account.|
|Bank Clearing Code|Specifies the code for bank clearing required according to the format standard you selected in the **Bank Clearing Standard** field. The bank clearing code can be used as an alternative to SWIFT and IBAN to identify your bank as the sender of a bank transfer.|
|Last Date Modified|Date of the latest modification of the bank account.|
|**Payment Matching**||
|Disable Automatic Payment Matching|Specifies whether or not to disable automatic payment matching after importing bank transactions for this bank account. Learn more at [Payment Reconciliation](receivables-apply-payments-auto-reconcile-bank-accounts.md).|
|**Payment Match Tolerance**||
|Match Tolerance Type|Specifies the tolerance the automatic payment application function will use to apply the *Amount Incl. Tolerance Matched* rule for this bank account. Read more in [Payment Reconciliation](receivables-apply-payments-auto-reconcile-bank-accounts.md).|
|Match Tolerance Value|Specifies if the automatic payment application function will apply the *Amount Incl. Tolerance Matched* rule by percentage or amount. Learn more at [Payment Reconciliation](receivables-apply-payments-auto-reconcile-bank-accounts.md).|
|**Hidden Fields**||
|Search Name|Specifies an alternate name you can use to search for the record in question when you can't remember the value in the **Name** field.|
|Min. Balance|Specifies a minimum balance for the bank account. This field is for information purposes only.|
|Positive Pay Export Code|Specifies a code for the data exchange definition managing the export of positive-pay files. Learn more at [Export Positive Pay Files](finance-how-positive-pay.md).|
|**Communication FastTab**||
|Address|The address of the bank branch.|
|Address 2|An additional address field for the bank branch.|
|Post Code|The post code of the bank branch.|
|City|The city of the bank branch.|
|Country/Region Code|The country/region code of the bank branch.|
|Phone No.|The phone number of the bank branch.|
|Mobile Phone No.|The mobile phone number of the bank branch.|
|Contact|The main contact in the bank branch. Additional contacts can be created in the **Contacts** module.|
|Fax No.|The fax number of the bank branch.|
|Email|The email address of the bank branch.|
|Home Page|The home page address of the bank branch website.|
|**Posting FastTab**||
|Currency Code|Specifies the relevant currency code for the bank account. Applying a currency code to a bank account limits all transactions to only using the applied currency code. Leaving the currency code blank allows transactions in all currencies, however, the amount will eventually be converted to the LCY using the applied currency rate. Checks issued from this account follow the same rules.|
|Last Check No.|The number of the latest check issued from this account.|
|Transit No.|Specifies a bank identification number of your own choice.|
|Last Statement No.|The number of the latest bank reconciliation posted to this account. Learn more at [Reconcile Bank Accounts](bank-how-reconcile-bank-accounts-separately.md).|
|Last Payment Statement No.|The number of the latest payment reconciliation posted to this account. Learn more at [Payment Reconciliation](receivables-apply-payments-auto-reconcile-bank-accounts.md).|
|Last Bank Statement|The ending balance of the last bank statement. Learn more at [Reconcile Bank Accounts](bank-how-reconcile-bank-accounts-separately.md).|
|Bank Acc. Posting Group|Specifies a code for the bank account's posting group. The **Bank Acc. Posting Group** connects the bank account to the G/L account in the balance sheet.|
|**Transfer**||
|Transit No.|Specifies a bank identification number of your own choice.|
|SWIFT Code|Specifies the international bank identifier (SWIFT) code of the bank in which you have account. The SWIFT code is very often considered a sensitive field. Learn more at [Monitoring Sensitive Fields](across-log-changes.md#monitoring-sensitive-fields).|
|IBAN|Specifies the bank account's international bank account number (IBAN). The IBAN code is very often considered a sensitive field. Learn more at [Monitoring Sensitive Fields](across-log-changes.md#monitoring-sensitive-fields).|
|Bank Statement Import Format|Specifies the format of the bank statement file imported into this bank account. This format is used in both the payment reconciliation journals and bank account reconciliations.|
|Payment Export Format|Specifies the format of the bank file that is exported when you choose **Export Payments to File** on the **Payment Journal** page.|
-->

## <a name="to-enter-an-opening-balance"></a>Sådan angiver du en primosaldo

For at udfylde feltet **Saldo** med en primosaldo, skal du bogføre en bankkontopost med det pågældende beløb. Du kan gøre dette ved at udføre en afstemning af bankkontoen. Få mere at vide i [Afstemme bankkonti](bank-how-reconcile-bank-accounts-separately.md).  
>
> Du kan også implementere primosaldoen som en del af oprettelse af generelle oplysninger i nye virksomheder ved hjælp af den assisterede opsætningsvejledning **Overflyt virksomhedsdata** . Flere oplysninger i [Blive køreklar](ui-get-ready-business.md).  

> [!IMPORTANT]
> Du må ikke bogføre primosaldoen direkte i finansregnskabet. Hvis der er poster i finanskontoen, der er bogført direkte til den, betyder det typisk, at du ikke kan afstemme bankkontoen. På bankkonti i udenlandsk valuta medfører en sådan metode, at der akkumuleres differencer, når du bogfører flere bankafstemninger. Du bogfører normalt primosaldoen direkte på bankkontoen, og beløbet havner derefter på finanskontoen. Alternativt kan du tilbageføre den senere fra den finanskonto, som du har brugt til at afstemme primosaldoen med finansbalancen. I begge tilfælde skal du udligne en direkte bogføring til finanskontoen, før du starter din første bankafstemning, og især hvis bankkontoen er i udenlandsk valuta.

## <a name="to-set-up-your-bank-account-for-import-or-export-of-bank-files"></a>Sådan oprettes bankkontoen for import eller eksport af bankfiler

Felterne er relateret til indlæsning og udlæsning af bankfeeds og -filer i oversigtspanelet **Overførsel** på siden **Bankkontokort**. Du kan finde flere oplysninger i [Bruge AMC Banking 365 Fundamentals-udvidelsen](ui-extensions-amc-banking.md) og [Konfigurere tjenesten Envestnet Yodlee Bank Feeds](bank-how-setup-bank-statement-service.md).

1. Vælg ![Lightbulb, der åbner funktionen Fortæl mig 2.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, angiv **Bankkonti**, vælg derefter det relaterede link.
2. Åbn kortet for den bankkonto, du vil eksportere eller importere bankfiler for.
3. Udfyld felterne efter behov i oversigtspanelet **Overførsel**. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

> [!NOTE]  
> Andre fileksporttjenester og deres formater kræver andre konfigurationsværdier på siden **Bankkontokort**. Du får information om forkerte eller manglende konfigurationsværdier, når du eksporterer filen. Læs omhyggeligt korte beskrivelser af felterne, eller se de relaterede emner med fremgangsmåder. Eksport af en betalingsfil med f.eks. nordamerikansk elektronisk pengeoverførsel (EFT) kræver, at både feltet **Sidste remitteringsadvisnr.** og **Transitnr.** er udfyldt. Flere oplysninger i [Eksportere betalinger til en bankfil](finance-make-payments-with-bank-data-conversion-service-or-sepa-credit-transfer.md#exporting-payments-to-a-bank-file).

Felterne i oversigtspanelet **Transit** på bankkontoen tjener forskellige formål, afhængigt af om betalingen er indadgående eller udadgående.

I illustrationen nedenfor vises ruten for indgående betalinger (tallene i beskrivelsen svarer til dem på illustrationen):

:::row:::
    :::column:::

1. Transaktionerne udlæses fra bankkontoen i enten et personligt læsbart. csv-format eller bankens eget format.
2. *Dataudvekslingsdefinition* knytter oplysningerne i filen til felterne i [!INCLUDE[prod_short](includes/prod_short.md)]. Flere oplysninger i [Opsætning af dataudveksling](across-set-up-data-exchange.md)
3. I *opsætningen af dataeksport/import* defineres eksporten eller importen og links til dataudvekslingsdefinitionen.
4. *Bankkontoudtogsimportformat* knytter importopsætningen til bankkontoen.
5. Betalingerne indlæses via **kladden til afstemning af betaling** eller **Bankkontoafstemning**.

  :::column-end:::
  :::column:::

        ![Illustration af betalinger, der er modtaget fra banken til bankkonti.](media/Set-Up-Bank-Accounts/payments-in-and-out-1.png)

  :::column-end:::
:::row-end:::

Indgående betalinger indlæses altid via **Betalingsudligningskladde** eller direkte på siden **Bankkontoafstemning**. Udgående betalinger kan derimod stamme fra enhver betalingskladde. Den eneste forudsætning er, at feltet **Tillad kontant eksport** i den relevante Udbetalingskladde navn skal markeres.

I illustrationen nedenfor vises ruten for udgående betalinger (tallene i beskrivelsen svarer til dem på illustrationen):

:::row:::
    :::column:::

6. Transaktionerne udfyldes i en udbetalingskladde, som er blevet forberedt til eksport af betalinger til fil.
7. *Bankkontoudtogsimportformat* knytter importopsætningen til bankkontoen.
8. I *opsætningen af dataeksport/import* defineres eksporten eller importen og links til dataudvekslingsdefinitionen.
9. *Dataudvekslingsdefinition* knytter oplysningerne i filen til felterne i [!INCLUDE[prod_short](includes/prod_short.md)]. Flere oplysninger i [Opsætning af dataudveksling](across-set-up-data-exchange.md)
10. Betalingerne udlæses fra udbetalingskladden og indlæses på bankkontoen.

  :::column-end:::
  :::column:::

        ![Illustration af betalinger, der er modtaget fra banken til bankkonti.](media/Set-Up-Bank-Accounts/payments-in-and-out-2.png)

  :::column-end:::
:::row-end:::

## <a name="to-set-up-vendor-bank-accounts-for-export-of-bank-files"></a>Sådan konfigureres kreditorbankkonti til eksport af bankfiler

Felter i oversigtspanelet **Overførsel** på siden **Kreditors bankkontokort** er relateret til udlæsning af bankfeeds og -filer. Du kan finde flere oplysninger i [Bruge AMC Banking 365 Fundamentals-udvidelsen](ui-extensions-amc-banking.md) og [Eksportere betalinger til en bankfil](finance-make-payments-with-bank-data-conversion-service-or-sepa-credit-transfer.md#exporting-payments-to-a-bank-file).

[!INCLUDE[purchase-vendor-bank-account](includes/purchase-vendor-bank-account.md)]

## <a name="changing-your-bank-account"></a>Ændre din bankkonto

Hvis du vil bruge en anden bankkonto til din virksomhed, skal du oprette den nye bankkonto i [!INCLUDE[prod_short](includes/prod_short.md)]. Det anbefales, at du ikke blot erstatter oplysninger om den konto, du bruger i øjeblikket, da det kan medføre forkerte data. Primosaldoen kan f. eks. være forkert, eller din bank-feed fungerer muligvis ikke korrekt. Det er vigtigt, at du holder de aktuelle og nye firmaer adskilt.

Når du har oprettet den nye bankkonto, skal du også oprette en ny Bankbogføringsgruppe og knytte den til en ny finanskonto. Du kan genbruge en eksisterende Bankbogføringsgruppe, og bank transaktionerne bogføres til samme finanskonti som de andre bankkonti, der deler denne bankbogføringsgruppe. Det anbefales dog, at du opretter en ny Bankbogføringsgruppe og finanskonto, så det er nemmere at foretage afstemningen.

> [!NOTE]
> Bemærk, at bankkontooplysningerne på åbne salgsfakturaer stadig viser den oprindelige bankkonto. Derfor bogføres betalinger stadig på denne konto. Det anbefales, at du holder begge konti aktive i en periode efter ændringen.

Hvis du vil have en mere kompakt oversigt over dine kontantkonti i financial reporting, skal du bruge kontiene **Fra-sum** og **Til-sum** i din kontoplan, rækkerne **Sammentælling** i finansrapporter eller finanskontoarter. Du kan finde flere oplysninger i afsnittet om [Business Intelligence og Financial Reporting](bi.md).

## <a name="see-also"></a>Se også

[Konfigurere banktransaktioner](bank-setup-banking.md)  
[Konfigurere bogføringsgrupper](finance-posting-groups.md)  
[Bankkontoafstemning](bank-manage-bank-accounts.md)  
[Konfigurere tjenesten Envestnet Yodlee Bank Feeds](bank-how-setup-bank-statement-service.md)  
[SEPA-direkte debitering i Business Central](finance-collect-payments-with-sepa-direct-debit.md)  
[Sådan konfigureres din bankkonto til SEPA-Direct Debit](finance-collect-payments-with-sepa-direct-debit.md#to-set-up-your-bank-account-for-sepa-direct-debit)  
[Sådan opsættes en konto til SEPA-kreditoverførsler](finance-make-payments-with-bank-data-conversion-service-or-sepa-credit-transfer.md#to-set-up-a-bank-account-for-sepa-credit-transfer)  
[Foretage betalinger med AMC Banking 365 Fundamentals-udvidelsen eller SEPA-kreditoverførsel](finance-make-payments-with-bank-data-conversion-service-or-sepa-credit-transfer.md)  
[Betalingsafstemning](receivables-apply-payments-auto-reconcile-bank-accounts.md)  
[Om Finans og kontoplanen](finance-general-ledger.md)  
[Arbejd med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)

[!INCLUDE[footer-include](includes/footer-banner.md)]
