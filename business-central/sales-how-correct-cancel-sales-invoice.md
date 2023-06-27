---
title: Rette eller annullere en bogført salgsfaktura
description: 'Beskriver, hvordan du kan rette, fortryde eller annullere en bogført salgsfaktura og anvende en salgskreditnota.'
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 'undo, credit memo, return'
ms.date: 06/23/2021
ms.author: edupont
---
# <a name="correct-or-cancel-unpaid-sales-invoices" />Rette eller annullere ubetalte salgsfakturaer

Du kan rette eller annullere en ubetalt bogført salgsfaktura, hvis den ikke er fuldt leveret. Dette er nyttigt, hvis du laver en fejl, eller hvis debitoren anmoder om en ændring før leverancen er fuldført. I alle andre scenarier anbefales det, at du opretter en rettelses salgskreditnota direkte. Du kan finde flere oplysninger i [Sådan oprettes en salgskreditnota på en bogført-salgsfaktura](sales-how-process-sales-returns-cancellations.md#to-create-a-sales-credit-memo-from-a-posted-sales-invoice).  

> [!NOTE]  
> Efter en bogført salgsfaktura er blevet helt eller delvist betalt, kan du ikke rette eller annullere den fra selve den bogførte salgsfaktura. I stedet for skal du manuelt oprette en salgskreditnota for at gøre salget ugyldigt og tilbagebetale debitoren, evt. administreret med en salgsreturvareordre. Du kan finde flere oplysninger i [Behandle salgsreturvarer eller annulleringer](sales-how-process-sales-returns-cancellations.md).

Forskellen mellem at annullere eller rette en bogført salgsfaktura, der ikke er betalt eller afsendt, er beskrevet i følgende tabel.

| Handling | Description |
| --- | --- |
| **Annuller** |Den bogførte salgsfaktura er annulleret. En rettelsessalgskreditnota oprettes og bogføres automatisk for at annullere den oprindelige bogførte salgsfaktura. På den oprindeligt bogførte salgsfaktura er afkrydsningsfelterne **Annulleret** og **Betalt** markeret. |
| **Ret** |Den bogførte salgsfaktura er annulleret. Der oprettes en ny salgsfaktura med samme oplysning, medmindre den bogførte salgsordre er bogført fra en salgsordre. Hvis det er tilfældet, foreslår vi, at du annullerer den bogførte salgsfaktura i stedet for og derefter foretager rettelsen og fortsætter salgsprocessen fra den oprindelige salgsordre. <br/><br/>Den nye salgsfaktura har et andet nummer end den første salgsfaktura. En rettelsessalgskreditnota oprettes og bogføres automatisk for at annullere den oprindelige bogførte salgsfaktura. På den oprindeligt bogførte salgsfaktura er afkrydsningsfelterne **Annulleret** og **Betalt** markeret. |

Når du retter eller annullerer en bogført salgsfaktura, anvendes den rettede salgskreditnota på alle finanskonti og lageropgørelsesposter, der blev oprettet, da den oprindelige salgsfaktura blev bogført. På denne måde tilbageføres den bogførte salgsfaktura i dine finansposter, og rettelsessalgskreditnotaen efterlades til revisionsspor.  

> [!TIP]
> Hvis du har bogført en forudbetalingsfaktura for en salgsfaktura, som du derefter retter eller annullerer, skal du også rette eller annullere forudbetalingen. Du kan finde flere oplysninger i [Rette forudbetalinger](finance-how-to-correct-prepayments.md).

## <a name="to-cancel-a-posted-sales-invoice" />Hvis du vil annullere en bogført salgsfaktura

1. Vælg ![Lightbulb, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **Bogførte salgsfakturaer**, og vælg derefter det relaterede link.  
2. Vælg den bogførte salgsfaktura, som du vil annullere.

    > [!NOTE]  
    >   Hvis afkrydsningsfeltet **Annulleret** er markeret, kan du ikke annullere den bogførte salgsfaktura, da den allerede er rettet eller annulleret.
3. På siden **Bogført salgsfaktura** skal du vælge handlingen **Annuller**.

    En salgskreditnota oprettes og bogføres automatisk for at annullere den oprindelige bogførte salgsfaktura. Feltet **Annulleret** på den første bogførte salgsfaktura ændres til **Ja**.
4. Vælg **Vis rettelseskreditnota** for at få vist den bogførte salgskreditnota, som gør den oprindelige bogførte salgsfaktura ugyldig.

### <a name="partial-invoice-posting-also-supported" />Delvis fakturabogføring understøttes også

Hvis annulleringen vedrører en delvis fakturabogføring, opdateres den oprindelige salgsordrelinje, så den afspejler det annullerede fakturerede antal. Felterne **Fakturer anta** og **Fakt. antal** på den relaterede salgsordrelinje nulstilles til værdierne før den delvise fakturabogføring.

## <a name="to-correct-a-posted-sales-invoice" />Hvis du vil rette en bogført salgsfaktura

1. Vælg ![Lightbulb, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **Bogførte salgsfakturaer**, og vælg derefter det relaterede link.  
2. Vælg den bogførte salgsfaktura, som du vil rette.

    > [!NOTE]  
    >   Hvis afkrydsningsfeltet **Annulleret** er markeret, kan du ikke rette den bogførte salgsfaktura, da den allerede er rettet eller annulleret.
3. På siden **Bogført salgsfaktura** skal du vælge handlingen **Ret**.  

    > [!NOTE]
    > Hvis salgsfakturaen er bogført fra en salgsordre, anbefales det, at du *annullerer* denne salgsfaktura og derefter behandler korrektionen fra den oprindelige salgsordre. Hvis den oprindelige salgsordre er slettet, f.eks. Hvis den er leveret fuldt ud, kan du oprette en ny salgsordre ved hjælp af handlingen **Kopier dokument**. Du kan finde flere oplysninger i [Sådan oprettes en salgskreditnota ved at kopiere en bogført salgsfaktura](sales-how-process-sales-returns-cancellations.md#to-create-a-sales-credit-memo-by-copying-a-posted-sales-invoice).
4. En ny salgsfaktura med de samme oplysninger oprettes, hvor du kan foretage en rettelse. Feltet **Annulleret** på den første bogførte salgsfaktura ændres til **Ja**.

    En salgskreditnota oprettes og bogføres automatisk for at annullere den oprindelige bogførte salgsfaktura.
5. Vælg handlingen **Vis rettelseskreditnota** for at få vist den bogførte salgskreditnota, som gør den oprindelige bogførte salgsfaktura ugyldig.

## <a name="see-related-microsoft-training" />Se relateret [Microsoft-træning](/training/modules/ship-invoice-items-dynamics-365-business-central/)

## <a name="see-also" />Se også

[Salg](sales-manage-sales.md)  
[Konfigurere salg](sales-setup-sales.md)  
[Sende dokumenter som mail](ui-how-send-documents-email.md)  
[Arbejd med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]
