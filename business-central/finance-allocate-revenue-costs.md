---
title: Allokere indtægter og omkostninger til flere finanskonti
description: 'Lære, hvordan du allokerer omkostninger på en eller flere konti i finansposterne.'
author: brentholtorf
ms.author: bholtorf
ms.date: 09/04/2023
ms.topic: conceptual
ms.search.keywords: 'allocate, allocation, accounts'
ms.search.form: '39, 2673, 2670, 2674,'
ms.custom: bap-template
ms.service: dynamics-365-business-central
ms.reviewer: bholtorf
---

# <a name="allocate-revenue-and-costs-to-multiple-general-ledger-accounts"></a>Allokere indtægter og omkostninger til flere finanskonti

I denne artikel beskrives, hvordan du kan bruge allokeringskonti til at fordele beløb i salgs- og købsdokumenter og finanskladdelinjer til forskellige finanskonti. Du kan allokere beløb via en fast eller variabel fordeling.  

Allokering opdeler en finanskladdelinje i de linjer, der er defineret på siden **Allokeringskonto**. Hvis du f.eks. opdeler en lejeudgift på tre måder ved hjælp af dimensioner, har du tre linjer at bogføre for allokeringen. Derfor har du seks finanslinjer (eller muligvis flere, hvis du bruger moms eller moms). Selvom der derved bogføres flere finansposter, end du måske har brug for, giver det dig mulighed for at tilbageføre individuelle linjer i stedet for at tilbageføre hele allokeringen.

Allokeringskonti arbejder også med udsættelser. Du kan få mere at vide om udsættelser ved at gå til [Udskyde indtægter og udgifter](finance-how-defer-revenue-expenses.md).

Følgende tabel viser de allokeringsmetoder, du kan bruge.

|Allokeringsmetode  |Beskrivelse  |
|---------|---------|
|Løst     | Når du vil opdele udgifterne på en måde, der gentages over en længere periode, kan du bruge en fast allokering. En fast fordeling giver dig mulighed for at definere allokeringsfordelingen. Denne opdeling ændres kun, når du ændrer opsætningen på siden **Allokeringskonto**.        |
|Variabel     | Hvis du vil fordele indtægter eller udgifter baseret på værdier, der ændrer sig over tid, skal du bruge den variable allokeringsmetode. Med variable allokeringer kan du angive de kilder, der skal bruges til at beregne allokeringsprocenterne. Denne metode er f.eks. nyttig, når du vil opdele medarbejderomkostningerne efter forskellige antal medarbejdere i afdelinger eller divisioner. Et andet eksempel er fordelingen af lejeomkostningerne baseret på optagelser fra produktionsgulvet, der kan variere fra produktionslinje til produktionslinje over tid. Variable allokeringer bruger en kombination af dimensioner og statistikkonti til at bestemme, hvordan beløbene fordeler sig i en periode. Du kan få mere at vide om statistiske konti ved at gå til [Analysér data med statistiske konti](bi-use-statistical-accounts.md). Hvis du vil vide mere om dimensioner, skal du gå til [Arbejde med dimensioner](finance-dimensions.md).        |

## <a name="use-a-fixed-share-or-percentage-method-to-allocate-amounts"></a>Bruge en fast andels- eller procentmetode til at allokere beløb

1. Vælg ikonet ![Elpære, der åbner funktionen Fortæl mig](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig"), angiv **Tildelingskonto**, og vælg derefter det relaterede link.  
1. På siden **TIldelingskonti** skal du vælge handlingen **Ny**.
1. Udfyld feltet **Nummer**. og **Navn**.
1. I feltet **Kontotype** skal du vælge **Fast**.
1. I feltet **Destinationskontotype** skal du vælge **Finans** eller **Bank.**
1. Vælg den konto, værdien skal bogføres på, i feltet **Destinationskontonummer**.
1. Valgfrit: Vælg handlingen **Dimensioner**, og angiv derefter dimensioner for linjen.
1. I felterne **Del** og **Procent** skal du angive, hvordan beløbene skal fordeles til destinationskontoen.
  
   > [!TIP]
   > Hvis du indtaster det faktiske beløb, der skal allokeres til en fast allokering, i feltet **Del** og **Procent** viser feltet procentdelen af det samlede beløb.
1. Gentag denne proces for hver konto, der skal medtages i allokeringen.

## <a name="use-a-variable-method-to-allocate-amounts"></a>Bruge en variabel metode til at allokere beløb

1. Vælg ikonet ![Elpære, der åbner funktionen Fortæl mig](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig"), angiv **Tildelingskonto**, og vælg derefter det relaterede link.  
1. På siden **TIldelingskonti** skal du vælge handlingen **Ny**.
1. Udfyld feltet **Nummer**. og **Navn**.
1. I feltet **Kontotype** skal du vælge **Variable**.
1. Indtast i feltet **Destinationskontotype** **Finanskonto**.
1. Vælg den konto, værdien skal bogføres på, i feltet **Destinationskontonummer**.
1. Indtast i feltet **Fordelingskontotype** **Finanskonto**.
1. Vælg den periode, beløbene skal fordeles for, i feltet **Beregningsperiode**.
1. Valgfrit: Hvis du vil filtrere på bestemte globale dimensionsværdier, skal du vælge handlingen **Fordelingskontosaldofiltre** og derefter angive filterværdierne.
1. Valgfrit: Vælg handlingen **Dimensioner**, og angiv derefter dimensioner for linjen.

## <a name="allocate-amounts-on-the-fly"></a>Alloker beløb undervejs

Du opretter allokeringskonti for at opdele indtægter og omkostninger for finanskonti og bankkonti. Automatisering af allokering kan spare dig for tid. Hvis du vil bruge allokeringskonti, men ikke vil oprette dem til hver finanskonto, kan du spare endnu mere tid.

Med indstillingen Overfør fra overordnet kan du bruge allokeringskontoen til at opdele beløb for en finanskonto på en linje i et dokument eller en kladde. I feltet **Kontotype** på et dokument eller en kladdelinje skal du vælge en finanskonto og derefter vælge allokeringskontoen i feltet **Allokeringskontonr.**. Beløbet på linjen deles for finanskontoen i overensstemmelse med opsætningen på allokeringskontoen. Det er en mindre gennemsigtig måde at allokere på, men du behøver ikke oprette en allokeringskonto specifikt til finanskontoen.

Ad hoc-allokeringer er nemme at oprette. I stedet for at angive en bank- eller finanskonto i feltet **Destinationskontotype** på siden **Allokeringskonto** skal du vælge indstillingen **Overfør fra overordnet** konto. Lad feltet **Destinationskontonummer** stå tomt. Når du vælger finanskontoen på dokumentet eller kladdelinjen, bruges den til at allokere beløb.

## <a name="verify-that-amounts-distribute-correctly-before-you-post-them"></a>Kontrollere, at beløbene fordeles korrekt, før du bogfører dem

Du kan kontrollere, at beløbene fordeles korrekt, på flere måder:

* På siden **Tildelingskonto** skal du vælge handlingen **Test tildeling**. Brug feltet **Beløb, der skal allokeres** til at kontrollere forskellige beløb.
* På siden **Finanskladder** skal du vælge kladden og derefter bruge handlingen **Bogfør forhåndsversion**.

## <a name="adjust-the-distribution"></a>Juster fordelingen

Hvis du finder noget i en allokering, som du gerne vil ændre, kan du justere allokeringen, før du bogfører den.  

1. Åbn det dokument eller den kladde, der indeholder den allokering, du vil ændre.
1. Vælg linjen med fordelingen og vælg derefter handlingen **Omfordel kontotildelinger**.
1. Foretag justeringen på siden **Ret allokeringer**.

## <a name="post-an-allocation-transaction"></a>Bogføre en allokeringstransaktion

I følgende procedure beskrives, hvordan du bogfører en allokeringstransaktion fra en finanskladde. Trinene er de samme for salgs- og købsdokumenter.

1. Vælg ikonet ![Elpære, der åbner funktionen Fortæl mig](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig"), angiv **Finanskladder**, og vælg derefter det relaterede link.  
1. Opret en ny linje. Udfyld felterne på samme måde som med enhver anden type finanskladde.
1. Hvis du bruger en fast eller variabel allokering, skal du udfylde følgende felter:
    1. Indtast i feltet **Kontotype** **Fordelingskonto**.
    1. Indtast i feltet **Kontonr.** fordelingskontoen.
1. Hvis du bruger en allokering, der bruger indstillingen Overfør fra overordnet, skal du gøre følgende:
    1. Indtast i feltet **Kontotype** **Finanskonto**.
    1. Vælg den finanskonto i feltet **Kontonr.**.
    1. I **Tildelingskontonr.** skal du vælge den allokeringskonto, der er konfigureret til at bruge indstillingen Overfør fra overordnet. 
1. Vælg **Bogfør**.

## <a name="see-also"></a>Se også

[Arbejde med finanskladder](ui-work-general-journals.md)  
