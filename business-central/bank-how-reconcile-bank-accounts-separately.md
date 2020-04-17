---
title: Afstemme bankkonti | Microsoft Docs
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
ms.date: 04/01/2020
ms.author: sgroespe
ms.openlocfilehash: e53c1f7b0b2af4a94579863197ec7348c9b6ff18
ms.sourcegitcommit: 88e4b30eaf6fa32af0c1452ce2f85ff1111c75e2
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 04/01/2020
ms.locfileid: "3186304"
---
# <a name="reconcile-bank-accounts"></a>Afstemme bankkonti
Du udfører bankafstemning for at sikre, at dine forskellige forretningstransaktioner og udgifter afspejles korrekt i firmaets regnskabsbøger. Det gør du ved at sammenligne og afstemme poster på dine interne bankkonti med banktransaktioner i din bank og derefter bogføre saldi på dine interne bankkonti for at gøre totaler tilgængelige for økonomichefer. Bankafstemning er også en praktisk måde at opdage og løse manglende betalinger og bogføringsfejl på.

I det følgende beskrives, hvordan du udfører bankafstemning med siden  **Bankkontoafstemning**.

> [!TIP]
> Du kan også afstemme bankkonti på siden **Betalingsudligningskladde** i forbindelse med betalingsbehandling. Eventuelle åbne bankposter vedrørende de udlignede debitor- eller kreditorposter bliver lukket, når du vælger handlingen **Bogfør betalinger og afstem bankkonti**. Det betyder, at bankkontoen automatisk afstemmes for de betalinger, du bogfører, med kladden. Du kan finde flere oplysninger under [Udligne betalinger automatisk og afstemme bankkonti](receivables-apply-payments-auto-reconcile-bank-accounts.md).

> [!NOTE]  
> I nordamerikanske versioner kan du også udføre dette arbejde på siden **Bankafstemningskladde**, der er mere velegnet til checks og indskud, men ikke tilbyder import af bankkontoudtogsfiler. Hvis du vil bruge denne side i stedet for siden **Bankkontoafstemning**, skal du fjerne markeringen i feltet **Bankafstemning med automatisk match** på siden **Regnskabsopsætning**. Du kan finde flere oplysninger i afsnittet "Afstemme bankkonti" under Lokal funktionalitet for USA.

Linjerne på siden **Bankkontoafstemning** er opdelt i to ruder. Ruden **Bankkontoudtogslinjer** viser enten importerede banktransaktioner eller poster med udestående betalinger. Ruden **Bankkontoposter** viser finansposterne på en intern bankkonto.

Aktiviteten for afstemning af banktransaktioner med interne bankposter kaldes *afstemning.* Du kan vælge at udføre tilsvarende afstemning automatisk ved hjælp af funktionen **Afstem automatisk**. Du kan alternativt manuelt markere linjer i begge ruder for at sammenkæde de enkelte bankkontoudtogslinjer med en eller flere relaterede bankposter og derefter bruge funktionen **Afstem manuelt**. Afkrydsningsfeltet **Udlignet** er markeret på linjer, hvor posterne stemmer. Du kan finde flere oplysninger i [Konfigurere regler for automatisk udligning af betalinger](receivables-how-set-up-payment-application-rules.md).

> [!NOTE]  
> Hvis bankkontoudtogslinjerne vedrører checkposter, kan du ikke bruge afstemningsfunktionerne. I stedet skal du vælge handlingen **Udlign poster** og derefter vælge den relevante checkpost, som bankkontoudtogslinjen skal afstemmes med.

Når værdien i feltet **Total balance** i ruden **Bankkontoudtogslinjer** svarer til værdien i feltet **Saldo til afstemning** i feltet **Bankkontoposter**, kan du vælge handlingen **Bogfør**. Alle ikke-afstemte bankkontoposter forbliver på siden, hvilket indikerer en uoverensstemmelse, som du skal løse for at afstemme bankkontoen.

Alle linjer, der ikke kan afstemmes, hvilket er angivet med en værdi i feltet **Difference**, forbliver på siden  **Bankkontoafstemning** efter bogføring. De repræsenterer en slags uoverensstemmelse, som du skal løse, før du kan fuldføre afstemningen af bankkontoen. Typiske forretningssituationer, der kan forårsage forskelle:

|Difference|Årsag|Løsning|
|-|-|
|En transaktion i den interne bankkonto er ikke på bankkontoudtoget.|Banktransaktionen blev ikke foretaget, selvom der blev bogført en bogføring i [!INCLUDE[d365fin](includes/d365fin_md.md)].|Foretag den manglende pengetransaktion (eller bed en debitor om at foretage den), og importer derefter bankkontoudtogsfilen igen, eller angiv transaktionen manuelt.|
|En postering på bankkontoudtoget findes ikke som et dokument eller en kladdelinje i [!INCLUDE[d365fin](includes/d365fin_md.md)].|En banktransaktion blev foretaget uden en tilsvarende bogføring [!INCLUDE[d365fin](includes/d365fin_md.md)]i, f.eks. bogføring af en kladdelinje for en udgift.|Opret og bogfør den manglende post. Du finder oplysninger om, hvordan du hurtigt starter dette, under [ Sådan oprettes manglende poster, som banktransaktioner skal afstemmes med](bank-how-reconcile-bank-accounts-separately.md#to-create-missing-ledger-entries-to-match-bank-statement-lines-with).|
|En transaktion på den interne bankkonto svarer til en banktransaktion, men nogle oplysninger er for forskellige til at give et match.|Oplysninger såsom beløbet eller kundenavnet blev angivet forskelligt i forbindelse med banktransaktionen eller den interne bogføring.|Gennemse oplysningerne, og match derefter de to manuelt. Du bør eventuelt rette uoverensstemmelsen mellem oplysningerne.||

Du skal løse forskellene, f.eks. ved at oprette manglende poster og rette oplysninger, der ikke svarer til hinanden, eller ved at foretage manglende pengeposteringer, indtil afstemningen af bankkontoen er fuldført og bogført.

Du kan udfylde ruden **Bankkontoudtogslinjer** på siden **Bankkontoafstemning** på følgende måder:

* Automatisk, ved hjælp af funktionen **Importér bankkontoudtog** for at udfylde ruden **Bankkontoudtogslinjer** med banktransaktioner ifølge en importeret fil eller stream, der er leveret af banken.
* Manuelt ved hjælp af funktionen **Foreslå linjer** for at udfylde ruden **Bankkontoudtogslinjer** ifølge fakturaerne i [!INCLUDE[d365fin](includes/d365fin_md.md)], der har udestående betalinger.

## <a name="to-fill-bank-reconciliation-lines-by-importing-a-bank-statement"></a>Sådan udfyldes bankafstemningslinjer ved at importere et bankkontoudtog
Ruden **Bankkontoudtogslinjer** udfyldes med bankposteringer i henhold til en importeret fil eller strøm, der er leveret af banken.

For at gøre det muligt at importere bankkontoudtog som bankfeeds skal du først konfigurere og aktivere tjenesten Envestnet Yodlee Bank Feeds og derefter knytte dine bankkonti til de relaterede onlinebankkonti. Du kan finde flere oplysninger i [Konfigurere tjenesten Envestnet Yodlee Bank Feeds](bank-how-setup-bank-statement-service.md).

1. Vælg ikonet ![Elpære, der åbner funktionen Fortæl mig](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig"), angiv **Bankkontoa&fstemning**, og vælg derefter det relaterede link.
2. Vælg handlingen **Ny**.
3. Vælg den relevante bankkonto i feltet **Bankkontonr.**. Bankkontoposterne, der findes på bankkontoen, vises i ruden **Bankkontoposter**.
4. Angiv datoen for kontoudtoget fra banken i feltet **Kontoudtogsdato**.
5. Angiv saldoen fra kontoudtoget i feltet **Kontoudtogs slutsaldo**.
6. Hvis du har en bankkontoudtogsfil, skal du vælge handlingen **Importér bankkontoudtog**.
7. Find filen, og vælg derefter knappen **Åbn** for at importere banktransaktionerne til linjerne ind i ruden **Bankkontoudtogslinjer** på siden **Bankkontoafstemning**.

## <a name="to-fill-bank-reconciliation-lines-with-the-suggest-lines-function"></a>Sådan udfyldes bankafstemningslinjer med funktionen Foreslå linjer
Ruden **Bankkontoudtogslinjer** udfyldes i henhold til fakturaer i [!INCLUDE[d365fin](includes/d365fin_md.md)], der har udestående betalinger.  
1. På siden **Bankkontoafstemning** skal du vælge handlingen **Foreslå linjer**.
2. Angiv den tidligste dato for de poster, der skal afstemmes, i feltet **Startdato**.
3. Angiv den seneste dato for de poster, der skal afstemmes, i feltet **Slutdato**.
4. Marker afkrydsningsfeltet **Medtag check**, hvis du vil foreslå checkposter i stedet for de tilsvarende bankkontoposter.
5. Vælg knappen **OK**.

## <a name="to-match-bank-statement-lines-with-bank-account-ledger-entries-automatically"></a>Sådan afstemmes kontoudtogslinjer automatisk med bankposter
Siden **Bankkontoafstemning** indeholder automatisk matchningsfunktionalitet, der er baseret på en sammenligning af tekst i en bankkontoudtogslinje (venstre rude) med tekst i en eller flere bankkontoposter (højre rude). Bemærk, at du kan overskrive den foreslåede automatiske afstemning, og du kan vælge slet ikke at bruge automatisk afstemning. Du kan finde flere oplysninger  [Sådan afstemmes bankkontoudtoglinjer manuelt med bankposter](bank-how-reconcile-bank-accounts-separately.md#to-match-bank-statement-lines-with-bank-account-ledger-entries-manually).

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

## <a name="to-create-missing-ledger-entries-to-match-bank-statement-lines-with"></a>Sådan oprettes manglende poster, som bankkontoudtogslinjer skal afstemmes med
Undertiden indeholder bankafstemninger beløb med renter eller gebyrer. Sådanne bankkontoudtogslinjer kan ikke afstemmes, fordi der ikke findes nogen relaterede finansposter i [!INCLUDE[d365fin](includes/d365fin_md.md)]. Derefter skal du bogføre en kladdelinje for hver transaktion for at oprette en relateret post, som de kan afstemmes med.

1. På siden **Bankkontoafstemning** skal du vælge handlingen **Overfør til finanskladde**.  
2. På siden **Overfør afstemning til fin.kld** skal du angive, hvilken finanskladde du vil bruge, og derefter klikke på knappen **OK**.

    Siden **Finanskladde** åbnes. Det indeholder nye kladdelinjer for alle bankkontoudtogslinje med manglende poster.
3. Udfyld kladdelinjen med de relevante oplysninger som f.eks. modkonto. Du kan finde flere oplysninger under [Arbejde med finanskladder](ui-work-general-journals.md).  
4. For at få vist resultatet af bogføringen, inden du bogfører, skal du vælge handlingen **Kontrollér rapport**. Rapporten **Bankkontoudtog** åbnes og viser de samme felter som hovedet på siden **Bankkontoafstemning**.
4. Vælg handlingen **Bogfør**.

    Når posten er bogført, skal du afstemme bankkontoudtogslinjen med den.
5. Opdatere eller genåbne siden **Bankkontoafstemning**. Den nye post vises i ruden **Bankkontoposter**.
6. Matche bankkontoudtogslinjen med bankkontoposten, manuelt eller automatisk.

## <a name="see-related-training-at-microsoft-learn"></a>Se relateret oplæring på [Microsoft Learn](/learn/modules/bank-reconciliation-dynamics-365-business-central/index)

## <a name="see-also"></a>Se også
[Bankkontoafstemning](bank-manage-bank-accounts.md)  
[Udligne betalinger automatisk og afstemme bankkonti](receivables-apply-payments-auto-reconcile-bank-accounts.md)  
[Konfigurere banktransaktioner](bank-setup-banking.md)  
[Konfigurere regler for automatisk udligning af betalinger](receivables-how-set-up-payment-application-rules.md)  
[Arbejde med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)
