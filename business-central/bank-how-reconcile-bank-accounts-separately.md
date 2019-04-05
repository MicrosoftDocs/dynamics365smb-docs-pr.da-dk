---
title: Afstemme bankkonti separat | Microsoft Docs
description: Beskriver, hvordan dine lagerværdier afstemmes med finansmodulet.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: bank account balance, bank statement
ms.date: 10/01/2018
ms.author: sgroespe
ms.openlocfilehash: feb29e3cee1a55833566657a6a007af8854f98f5
ms.sourcegitcommit: 1bcfaa99ea302e6b84b8361ca02730b135557fc1
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 03/08/2019
ms.locfileid: "792058"
---
# <a name="reconcile-bank-accounts-separately"></a>Afstemme bankkonti separat
Når du vil afstemme bankkonti i [!INCLUDE[d365fin](includes/d365fin_md.md)] med kontoudtog fra banken, skal du begynde med at udfylde den venstre rude på siden **Bankkontoafstemning** med bankkontoudtogoplysninger, som du derefter matcher (afstemmer) med bankkontoposter i højre rude. En smart måde at udfylde bankkontoudtogslinjer er ved at importere en bankkontoudtogsfil eller et -feed.

> [!NOTE]  
> I nordamerikanske versioner kan du også udføre dette arbejde på siden **Bankafstemningskladde**, der er mere velegnet til checks og indskud, men ikke tilbyder import af bankkontoudtogsfiler. Hvis du vil bruge denne side i stedet for siden **Bankkontoafstemning**, skal du fjerne markeringen i feltet **Bankafstemning med automatisk match** på siden **Regnskabsopsætning**. Du kan finde flere oplysninger i afsnittet "Afstemme bankkonti" under Lokal funktionalitet for USA.

> [!TIP]  
> Du kan også afstemme bankkonti på siden **Betalingsudligningskladde**. Eventuelle åbne bankposter vedrørende de udlignede debitor- eller kreditorposter bliver lukket, når du vælger handlingen **Bogfør betalinger og afstem bankkonti**. Det betyder, at bankkontoen automatisk afstemmes for de betalinger, du bogfører, med kladden. Du kan finde flere oplysninger i [Afstemme betalinger ved hjælp af automatisk udligning](receivables-how-reconcile-payments-auto-application.md).

For at gøre det muligt at importere bankkontoudtog som bankfeeds skal du først konfigurere og aktivere tjenesten Envestnet Yodlee Bank Feeds og derefter knytte dine bankkonti til de relaterede onlinebankkonti. Du kan finde flere oplysninger under [Konfigurere tjenesten Envestnet Yodlee Bank Feeds](bank-how-setup-bank-statement-service.md).

Linjerne på siden **Bankkontoafstemning** er opdelt i to ruder. Ruden **Bankkontoudtogslinjer** viser enten importerede banktransaktioner eller poster med udestående betalinger. Ruden **Bankkontoposter** viser finansposterne på bankkontoen.

Aktiviteten med at søge efter og udligne bankposter kaldes *afstemning*. Du kan vælge at udføre tilsvarende afstemning automatisk ved hjælp af funktionen **Afstem automatisk**. Du kan alternativt manuelt markere linjer i begge ruder for at sammenkæde de enkelte bankkontoudtogslinjer med en eller flere relaterede bankposter og derefter bruge funktionen **Afstem manuelt**. Afkrydsningsfeltet **Udlignet** er markeret på linjer, hvor posterne stemmer.

Du kan udfylde ruden **Bankkontoudtogslinjer** på siden **Bankkontoafstemning** på følgende måder:

* Automatisk, ved hjælp af funktionen **Importér bankkontoudtog** for at udfylde linjerne i overensstemmelse med faktiske kontoudtog baseret på en fil fra banken.
* Manuelt ved hjælp af funktionen **Foreslå linjer** for at udfylde linjerne med poster for fakturaer, der har udestående beløb.

Når værdien i feltet **Total balance** i ruden **Bankkontoudtogslinjer** svarer til værdien i feltet **Saldo til afstemning** i feltet **Bankkontoposter**, kan du vælge handlingen **Bogfør** for at afstemme de udlignede bankkontoposter. Alle ikke-udlignede bankposter forbliver på siden. Dette angiver, at betalinger, der er behandlet for bankkontoen, ikke afspejles i det seneste bankudtog eller at nogle betalinger er modtaget på checks.

> [!NOTE]  
>   Hvis bankkontoudtogslinjerne vedrører checkposter, kan du ikke bruge afstemningsfunktionerne. I stedet skal du vælge handlingen **Udlign poster** og derefter vælge den relevante checkpost, som bankkontoudtogslinjen skal afstemmes med.

## <a name="to-fill-bank-reconciliation-lines-by-importing-a-bank-statement"></a>Sådan udfyldes bankafstemningslinjer ved at importere et bankkontoudtog
1. Vælg ikonet ![Elpære, der åbner funktionen Fortæl mig](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig"), angiv **Bankkontoafstemningsoversigt**, og vælg derefter det relaterede link.
2. Vælg handlingen **Ny**.
3. Vælg den relevante bankkonto i feltet **Bankkontonr.**. Bankkontoposterne, der findes på bankkontoen, vises i ruden **Bankkontoposter**.
4. Angiv datoen for kontoudtoget fra banken i feltet **Kontoudtogsdato**.
5. Angiv saldoen fra kontoudtoget i feltet **Kontoudtogs slutsaldo**.
6. Hvis du har en bankkontoudtogsfil, skal du vælge handlingen **Importér bankkontoudtog**.
7. Find filen, og vælg derefter knappen **Åbn** for at importere banktransaktionerne til linjerne på siden **Bankkontoafstemning**.

## <a name="to-fill-bank-reconciliation-lines-with-the-suggest-lines-function"></a>Sådan udfyldes bankafstemningslinjer med funktionen Foreslå linjer
1. På siden **Bankkontoafstemning** skal du vælge handlingen **Foreslå linjer**.
2. Angiv den tidligste dato for de poster, der skal afstemmes, i feltet **Startdato**.
3. Angiv den seneste dato for de poster, der skal afstemmes, i feltet **Slutdato**.
4. Marker afkrydsningsfeltet **Medtag check**, hvis du vil foreslå checkposter i stedet for de tilsvarende bankkontoposter.
5. Vælg knappen **OK**.

## <a name="to-match-bank-statement-lines-with-bank-account-ledger-entries-automatically"></a>Sådan afstemmes kontoudtogslinjer automatisk med bankposter
Siden indeholder automatisk matchningsfunktionalitet, der anvender betalinger på de relaterede åbne poster baseret på en sammenligning af tekst i en bankkontoudtogslinje (venstre rude) med tekst i en eller flere bankkontoposter (højre rude). Bemærk, at du kan overskrive de foreslåede automatiske udligninger, og du kan vælge slet ikke at bruge automatisk udligning. Der er flere oplysninger i næste procedure.

1. På siden **Bankkontoafstemning** skal du vælge **Match automatisk**. Siden **Afstem bankposter** åbnes.
2. I feltet **Transaktionsdatotolerance (dage)** skal du angive antallet af dage før og efter bankpostens bogføringsdato, hvorimellem funktionen skal søge efter tilsvarende transaktionsdatoer i kontoudtoget.

    Hvis du indtaster 0 eller lader feltet stå tomt, vil funktionen **Afstem automatisk** kun søge efter afstemte transaktionsdatoer på bankpostens bogføringsdato.
3. Vælg knappen **OK**.

    Alle bankkontoudtogslinjer og bankposter, der kan afstemmes, ændrer farve til grøn skrifttype, og afkrydsningsfeltet **Udlignet** markeres.
4. For at fjerne et match skal du markere bankkontoudtogslinjen og derefter vælge handlingen **Fjern match**.

## <a name="to-match-bank-statement-lines-with-bank-account-ledger-entries-manually"></a>Sådan afstemmes bankkontoudtoglinjer manuelt med bankposter
1. På siden **Bankkontoafstemning** skal du vælge en ikke-udlignet linje i ruden **Bankkontoudtogslinjer**:
2. I ruden **Bankkontoposter** skal du vælge en eller flere bankkontoposter, der kan afstemmes med den valgte bankkontoudtogslinje. Hvis du vil vælge flere linjer, skal du trykke på og holde Ctrl-tasten nede.
3. Vælg handlingen **Match manuelt**.

    Den valgte bankkontoudtogslinje og de valgte bankposter ændrer farve til grøn skrifttype, og afkrydsningsfeltet **Udlignet** i højre rude markeres.
4. Gentag trin 1 til 3 for alle kontoudtogslinjer, der ikke er afstemt.
5. For at fjerne et match skal du markere bankkontoudtogslinjen og derefter vælge handlingen **Fjern match**.

## <a name="to-create-missing-ledger-entries-to-match-bank-transactions-with"></a>Sådan oprettes manglende poster, som banktransaktioner skal afstemmes med
Undertiden indeholder bankafstemninger beløb med renter eller gebyrer. Sådanne banktransaktioner kan ikke afstemmes, fordi der ikke findes nogen relaterede finansposter i [!INCLUDE[d365fin](includes/d365fin_md.md)]. Derefter skal du bogføre en kladdelinje for hver transaktion for at oprette en relateret post, som de kan afstemmes med.

1. På siden **Bankkontoafstemning** skal du vælge handlingen **Overfør til finanskladde**.  
2. På siden **Overfør afstemning til fin.kld** skal du angive, hvilken finanskladde du vil bruge, og derefter klikke på knappen **OK**.

    Siden **Finanskladde** åbnes. Det indeholder nye kladdelinjer for alle bankkontoudtogslinje med manglende poster.
3. Udfyld kladdelinjen med de relevante oplysninger som f.eks. modkonto. Du kan finde flere oplysninger under [Arbejde med finanskladder](ui-work-general-journals.md).  
4. For at få vist resultatet af bogføringen, inden du bogfører, skal du vælge handlingen **Kontrollér rapport**. Rapporten **Bankkontoudtog** åbnes og viser de samme felter som hovedet på siden **Bankkontoafstemning**.
4. Vælg handlingen **Bogfør**.

    Når posten er bogført, skal du afstemme banktransaktionen med den.
5. Opdatere eller genåbne siden **Bankkontoafstemning**. Den nye post vises i ruden **Bankkontoposter**.
6. Matche bankkontoudtogslinjen med bankkontoposten, manuelt eller automatisk.

## <a name="see-also"></a>Se også
[Håndtere bankkonti](bank-manage-bank-accounts.md)  
[Konfigurere banktransaktioner](bank-setup-banking.md)  
[Arbejde med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)
