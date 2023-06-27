---
title: Behandle salgsreturvarer eller annulleringer
description: Beskriver, hvordan du opretter en salgskreditnota for at behandle en returnering, annullering eller refusion for varer eller tjenester, du har modtaget betaling for.
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: undo, credit memo, return
ms.search.form: 44, 134, 143, 6629, 6630, 6633, 6662, 9302, 9304, Report_6646
ms.date: 09/27/2021
ms.author: edupont
ms.openlocfilehash: a6feeced4c3e0e5286b0acbd264157b5cdab2524
ms.sourcegitcommit: 3acadf94fa34ca57fc137cb2296e644fbabc1a60
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 09/19/2022
ms.locfileid: "9531373"
---
# <a name="process-sales-returns-or-cancellations" /><a name="process-sales-returns-or-cancellations"></a>Behandle salgsreturvarer eller annulleringer

Hvis en debitor ønsker at returnere varer eller få refunderet varer eller serviceydelser, som du har solgt og modtaget betaling for, skal du oprette og bogføre en salgskreditnota, der angiver den ønskede ændring. Hvis du vil medtage de korrekte salgsfakturaoplysninger, kan du gøre følgende:  

- Oprette en salgskreditnota direkte fra en bogført salgsfaktura.
- Opret en ny salgskreditnota med oplysninger om kopieret faktura.

Hvis du ønsker større kontrol over salgsreturvareprocessen, f.eks. med lagerdokumenter til håndtering af varer eller bedre overblik ved modtagelse af varer fra flere salgsdokumenter i én salgsreturnering, kan du oprette salgsreturvareordrer. En salgsreturvareordre udsteder automatisk den relaterede salgskreditnota og andre returvarerelaterede dokumenter, f.eks. en erstatningssalgsordre, hvis det er nødvendigt. Du kan finde flere oplysninger i [Behandle salgsreturordrer](sales-how-process-sales-returns-orders.md).

> [!NOTE]  
> Hvis en bogført salgsfaktura endnu ikke er betalt, kan du bruge funktionen **Ret** eller **Annuller** på den bogførte salgsfaktura, så du tilbagefører transaktionerne. Disse funktioner fungerer kun for ubetalte fakturaer, og de understøtter ikke delvise returneringer eller annulleringer. Du kan finde flere oplysninger i [Rette eller annullere ubetalte salgsfakturaer](sales-how-correct-cancel-sales-invoice.md).

En returnering eller refusion kan vedrøre nogle af varerne eller tjenesteydelserne på den oprindelige salgsfaktura. Det er tilfældet skal du redigere oplysningerne på linjerne i salgskreditnotaen eller salgsreturvareordren. Når du bogfører salgskreditnotaen eller salgsreturvareordren, tilbageføres de salgsdokumenter, der berøres af ændringen, og der kan oprettes en refusionsbetaling til debitoren. Du kan finde flere oplysninger i [Foretage betalinger](payables-make-payments.md).  

Bogføringen af kreditnotaen gendanner også de varegebyrer, der er tildelt det bogførte dokument, så varens værdiposter er de samme, som før varegebyret blev tildelt.

> [!NOTE]
> Bogholderiaspekter af salgsreturvarer, f.eks. betalinger til debitorer som refusion, anses for at være bogholderiarbejde og beskrives ikke her. Du kan finde flere oplysninger i [Administrere skyldige beløb](payables-manage-payables.md).

## <a name="to-create-a-sales-credit-memo-from-a-posted-sales-invoice" /><a name="to-create-a-sales-credit-memo-from-a-posted-sales-invoice"></a>Sådan oprettes en salgskreditnota fra en bogført salgsfaktura

1. Vælg ![Lightbulb, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **Bogførte salgsfakturaer**, og vælg derefter det relaterede link.  
2. På siden **Bogf. salgsfakturaer** skal du vælge den bogførte salgsfaktura, der skal tilbageføres, og derefter vælge handlingen **Annuller** og **Opret rettelseskreditnota**.

    Salgskreditnotahovedet indeholder nogle oplysninger fra den bogførte salgsfaktura. Du kan redigere disse oplysninger f.eks med nye oplysninger, der afspejler returneringsaftalen.  
3. Rediger oplysningerne på linjerne i overensstemmelse med aftalen, f.eks antallet af returnerede varer eller beløbet, der skal refunderes.
4. Vælg handlingen **Forbered**, og vælg derefter handlingen **Udlign**.
5. På siden **Udlign debitorposter** skal du vælge linjen med det bogførte salgsdokument, du vil udligne salgskreditnotaen til, og vælg derefter handlingen **Udlignings-id**.

    Salgskreditnotaens id vises i feltet **Udlignings-id**.
6. I feltet **Beløb, der skal udlignes** skal du indtaste det beløb, som du vil udligne, hvis det er mindre end det oprindelige beløb.  

    Nederst på siden **Udlign debitorposter** kan du se det samlede beløb, der skal udlignes for at tilbageføre alle involverede poster, dvs. når værdien i feltet **Saldo** er nul.
7. Vælg knappen **OK**. Når du bogfører salgskreditnotaen, bliver den udlignet til de bogførte salgsdokumenter.

    Når du har oprettet eller redigeret de ønskede salgskreditnotalinjer, og anvendelse på enkelt eller flere er angivet, kan du bogføre salgskreditnotaen.  
8. Vælg handlingen **Bogføring**, og vælg derefter handlingen **Bogfør og send**.  

Dialogboksen **Bekræftelse af bogfør og send** åbnes og viser den foretrukne afsendelsesmetode til kunden. Du kan ændre afsendelsesmetoden ved at vælge opslagsknappen for feltet **Send bilag til**. Du kan finde flere oplysninger i [Konfigurere dokumentafsendelsesprofiler](sales-how-setup-document-send-profiles.md).  

De bogførte salgsdokumenter, som du tilknytter kreditnotaen, tilbageføres nu, og der kan oprettes en refusionsbetaling til debitoren. Salgskreditnotaen fjernes og erstattes med et nyt bilag i oversigten over bogførte salgskreditnotaer.

## <a name="to-create-a-sales-credit-memo-by-copying-a-posted-sales-invoice" /><a name="to-create-a-sales-credit-memo-by-copying-a-posted-sales-invoice"></a>Sådan oprettes en salgskreditnota ved at kopiere en bogført salgsfaktura

1. Vælg ![Lightbulb, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **Salgskreditnotaer**, og vælg derefter det relaterede link.
2. Vælg handlingen **Ny** for at åbne en ny tom salgskreditnota.
3. I feltet **Debitornavn** skal du indtaste navnet på en eksisterende debitor.
4. Vælg handlingen **Forbered**, og vælg derefter handlingen **Kopiér dokument**.
5. På siden **Kopier salgsdokument** skal du vælge **Bogført faktura** i feltet **Dokumenttype**.
6. Vælg feltet **Bilagsnr.** for at åbne siden **Bogf. salgsfakturaer**, og vælg derefter den bogførte salgsfaktura, der indeholder poster, som du vil tilbageføre.
7. Marker afkrydsningsfeltet **Genberegn linjer**, hvis du vil opdatere de kopierede bogførte salgsfakturalinjer med eventuelle ændringer i varepris og kostpris, siden fakturaen blev bogført.
8. Vælg knappen **OK**. De kopierede fakturalinjer skal indsættes i salgskreditnotaen.
9. Udfyld salgskreditnotaen, som beskrevet i [Sådan oprettes en salgskreditnota fra en bogført salgsfaktura](sales-how-process-sales-returns-cancellations.md#to-create-a-sales-credit-memo-from-a-posted-sales-invoice).

## <a name="to-create-a-sales-allowance" /><a name="to-create-a-sales-allowance"></a>Sådan oprettes et salgsnedslag
Du kan have brug for at sende en kunde en kreditnota med en prisreduktion, hvis kunden har modtaget en let beskadiget vare eller modtaget varerne for sent.  
Du kan bogføre den reducerede pris som et varegebyr i en kreditnota eller returvareordre og tildele den til den bogførte levering. Nedenfor beskrives dette for en salgskreditnota, men samme fremgangsmåde anvendes ved en salgsreturvareordre.

1. Vælg ![Lightbulb, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **Salgskreditnotaer**, og vælg derefter det relaterede link.
2. Vælg handlingen **Ny** for at åbne en ny tom salgskreditnota.
3. Udfyld hovedet på kreditnotaen med de relevante oplysninger om den kunde, som du vil give salgsdekorten til.  
4. Marker **Gebyr (vare)** i feltet **Type** på oversigtspanelet **Linjer**.  
5. I feltet **Nummer** skal du markere det relevante varegebyrværdi.  
     Du skal evt. oprette en særligt varegebyrnummer, der dækker salgsdekorten.  
6. Angiv **1** i feltet **Antal**.  
7. Angiv beløbet på salgsdekorten i feltet **Salgspris ekskl. moms**.  
8. Tildel salgsnedslaget som et varegebyr på varerne i den bogførte leverance. Du kan finde flere oplysninger i [Bruge varegebyrer til at angive ekstra handelsomkostninger](payables-how-assign-item-charges.md). Vend derefter tilbage til siden **Salgskreditnota**.  

Når du bogfører salgsreturvareordren, føjes salgsnedslaget til den relevante salgspost. Det gør det muligt at opretholde en præcis lagerværdi.

## <a name="to-combine-return-receipts" /><a name="to-combine-return-receipts"></a>Sådan samles returvaremodtagelser
Du kan kombinere returvaremodtagelser, hvis en kunde returnerer varer, som stammer fra forskellige salgsreturvareordrer.  

Når du modtager varerne på lagerstedet, skal du bogføre salgsreturvareordrerne som modtaget. Dette opretter bogførte returvaremodtagelser.  

Når du skal fakturere kunden, kan du i stedet for at fakturere hver salgsreturvareordre særskilt oprette en salgskreditnota og automatisk kopiere de bogførte returvaremodtagelseslinjer til dokumentet. Derefter kan du bogføre salgskreditnotaen og spare tid ved at fakturere alle de åbne salgsreturvareordrer samtidigt.  

Hvis du vil kombinere returvaremodtagelser skal afkrydsningsfeltet **Tillad samlefaktura** være markeret på siden **Debitorkort**.  

### <a name="to-manually-combine-return-receipts" /><a name="to-manually-combine-return-receipts"></a>Sådan samles returvaremodtagelser manuelt

1. Vælg ![Lightbulb, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **Salgskreditnotaer**, og vælg derefter det relaterede link.  
2. Vælg handlingen **Ny**.
3. Udfyld felterne efter behov i oversigtspanelet **Generelt**.  
4. Vælg handlingen **Hent returvaremodt.linjer**.  
5. Markér de returvarelinjer, der skal indgå i kreditnotaen:  

    - Hvis alle linjer skal indsættes, skal du markere samtlige linjer og derefter vælge knappen **OK**.  

    - Hvis specifikke linjer skal indsættes, skal du markere linjerne og derefter vælge knappen **OK**.  
6.  Hvis du kommer til at vælge en forkert modtagelseslinje eller vil begynde forfra, skal du bare slette linjerne på kreditnotaen og bruge funktionen **Hent returvaremodt.linjer** igen.  
7.  Bogfør fakturaen.  

### <a name="to-automatically-combine-return-receipts" /><a name="to-automatically-combine-return-receipts"></a>Sådan samles returvaremodtagelser automatisk

Du kan samle returvaremodtagelser automatisk og også vælge at bogføre kreditnotaerne automatisk med funktionen **Saml returvarekvit**.  

1. Vælg ikonet ![Lightbulb, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **Saml returvarekvit.**, og vælg derefter det relaterede link.
2. På siden **Saml returvarekvit** skal du udfylde felterne for at vælge de relevante returvaremodtagelser.
3. Markér afkrydsningsfeltet **Bogfør kreditnotaer**. Hvis ikke, skal du manuelt bogføre de købskreditnotaer, der oprettes.
4. Vælg knappen **OK**.  

### <a name="to-remove-a-received-and-invoiced-return-order" /><a name="to-remove-a-received-and-invoiced-return-order"></a>Sådan fjernes en modtaget og faktureret returvareordre

Når du fakturerer returvaremodtagelser på denne måde, findes returvareordrerne, som returvaremodtagelserne er bogført fra, stadig, selvom de er modtaget og faktureret i fuldt omfang.  

Når returvaremodtagelser samles på en kreditnota og bogføres, oprettes der en bogført salgskreditnota for de krediterede linjer. Feltet **Faktureret (antal)** på den oprindelige salgsreturvareordre opdateres på basis af det fakturerede antal.  

1. Vælg ![Lightbulb, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **Slet fakturerede salgsreturvareordrer**, og vælg derefter det relaterede link.  
2. I feltet **Nummer** skal du angive, hvilke returvareordrer der skal slettes.  
3. Vælg knappen **OK**.  

Du kan også slette individuelle salgsreturordrer manuelt.  

## <a name="inventory-costing" /><a name="inventory-costing"></a>Lagerkostmetode

Hvis du vil bevare korrekt lagerværdi, skal du typisk placere returnerede varer tilbage i lagerbeholdningen med den kostpris, som de blev solgt til, og ikke til deres aktuelle kostpris. Dette omtales som præcis kostprisudligning.

Der findes to funktioner til at tildele præcis kostprisudligning automatisk:  

|Funktion|Beskrivlse|  
|------------------|---------------------------------------|  
|Funktionen **Hent bogførte bilagslinjer, der skal tilbageføres** på siden **Salgsreturvareordre**|Kopierer linjer for et eller flere bogførte bilag, der skal tilbageføres, til salgsreturvareordren. Yderligere oplysninger finder du i [Oprette en salgsreturvareordre baseret på et eller flere bogførte salgsdokumenter](sales-how-process-sales-returns-orders.md#create-a-sales-return-order-based-on-one-or-more-posted-sales-documents).|  
|Funktionen **Kopiér dokument** på siderne **Salgskreditnota** og **Salgsreturvareordre**|Kopierer både sidehoved og linjerne i et og samme bogførte dokument, der skal tilbageføres.<br /><br /> Kræver, at afkrydsningsfeltet **Obl. beløbstilbageførsel** er markeret på siden **Salgsopsætning**.|

Hvis du vil tildele præcis kostprisudligning manuelt, skal du vælge feltet **Udlign-fra varepost** på en vilkårlig type returdokumentlinje, og derefter vælge nummeret på den oprindelige salgspost. På den måde knyttes salgskreditnotaen eller salgsreturvareordren til den oprindelige salgspost, og varen værdiansættes til den oprindelige kostpris.

Du kan finde flere oplysninger i [Designoplysninger: Lagerkostmetode](design-details-inventory-costing.md).

## <a name="see-related-microsoft-training" /><a name="see-related-microsoft-training"></a>Se relateret [Microsoft-træning](/training/paths/return-items-dynamics-365-business-central/)

## <a name="see-also" /><a name="see-also"></a>Se også

[Salg](sales-manage-sales.md)  
[Konfigurere salg](sales-setup-sales.md)  
[Administrere skyldige beløb](payables-manage-payables.md)  
[Sende dokumenter som mail](ui-how-send-documents-email.md)  
[Behandle købsreturvarer eller annulleringer](purchasing-how-process-purchase-returns-cancellations.md)  
[Arbejd med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]
