---
title: Oprette et salgstilbud til en kunde | Microsoft Docs
description: Beskriver, hvordan du opretter et salgstilbuds- eller tilbudsanmodningsdokument for at registrere dit tilbud til en kunde om at sælge produkter i henhold til bestemte betingelser.
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: rfq
ms.date: 04/01/2020
ms.author: sgroespe
ms.openlocfilehash: a8db87b7dd365123a21633e4905d56dd13bf7b40
ms.sourcegitcommit: 88e4b30eaf6fa32af0c1452ce2f85ff1111c75e2
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 04/01/2020
ms.locfileid: "3193607"
---
# <a name="make-sales-quotes"></a>Oprette salgstilbud
Du opretter et salgstilbud for at registrere dit tilbud til en debitor om at sælge bestemte produkter på bestemte leverings- og betalingsbetingelser. Du kan sende salgstilbuddet til debitoren for at kommunikere tilbuddet. Du kan sende dokumentet i en mail som en vedhæftet PDF-fil. Du kan også få brødteksten i mailen udfyldt med en oversigt over tilbuddet. Du kan finde flere oplysninger under [Sende dokumenter via mail](ui-how-send-documents-email.md).

Mens du forhandler med debitoren, kan du ændre og gensende salgstilbuddet så meget, som det er nødvendigt. Når debitoren accepterer tilbuddet, kan du konverterer salgstilbuddet til en salgsfaktura eller en salgsordre, hvor du behandler salget. Du kan finde flere oplysninger i [Fakturere salg](sales-how-invoice-sales.md) eller [Sælge produkter](sales-how-sell-products.md).

Du kan udfylde debitorfelter i salgstilbud på to måder, afhængigt af om debitoren allerede er registreret. Se trin 2 og 3 i følgende procedure.

## <a name="to-create-a-sales-quote"></a>Sådan oprettes et salgstilbud
1. Vælg ikonet ![Elpære, der åbner funktionen Fortæl mig](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig"), angiv **Salgstilbud**, og vælg derefter det relaterede link.
2. I feltet **Debitor** skal du indtaste navnet på en eksisterende debitor.

   Andre felter på siden **Salgstilbud** indeholder standardoplysningerne for den valgte debitor. Hvis debitoren ikke er registreret, skal du følge disse trin:
3. I feltet **Debitor** skal du indtaste navnet på den nye debitor.
4. I dialogboksen, hvor du registrerer den nye debitor, skal du trykke på knappen **Ja**.
5. På siden **Vælg en skabelon til en ny debitor** skal du vælge en skabelon, som det nye debitorkort skal baseres på, og derefter vælge knappen **OK**.
6. Et nyt debitorkort viser oplysninger om den valgte debitorskabelon. Udfyld de resterende felter. Du kan finde flere oplysninger i [Registrere nye debitorer](sales-how-register-new-customers.md).  
7. Når du er færdig med debitorkortet, skal du vælge **OK** for at vende tilbage til siden **Salgstilbud**.

   En række af felterne i salgstilbuddet er nu udfyldt med oplysninger, der er angivet på det nye debitorkort.  
8. Udfylde de resterende felter efter behov på siden **Salgstilbud**. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]  

    Du er nu klar til at udfylde salgsordrelinjerne for produkter, du sælger til debitoren, eller til andre transaktioner med debitoren, som du vil registrere i en finanskonto.   

    Hvis du har konfigureret de tilbagevendende salgslinjer for debitoren, f.eks en månedlig genbestillingsordre, kan du indsætte disse linjer i ordren ved at vælge handlingen **Hent tilbagevendende salgslinjer**.  

9. I oversigtspanelet **Linjer** i feltet **Type** skal du vælge, hvilken type produkt, gebyr eller transaktion, som du vil bogføre for debitoren med salgslinjen.
10. I feltet **Nummer** skal du vælge en post, der skal bogføres i overensstemmelse med værdien i feltet **Type**.

    Lad feltet **Nummer** være tomt i følgende tilfælde:
    - Hvis der er tale om en kommentar. Skriv bemærkningen i feltet **Beskrivelse**.
    - Hvis der er tale om en katalogvare. Vælg handlingen **Vælg katalogvarer**. Du kan finde flere oplysninger under [Arbejde med katalogvarer](inventory-how-work-nonstock-items.md).

11. I feltet **Antal** skal du angive, hvor mange enheder af produktet, gebyret eller transaktion, som linjen skal registrere for debitoren.

    > [!NOTE]  
    >  Hvis varen er af typen **Service**, eller hvis feltet **Type** indeholder **Ressource**, er antallet en tidsenhed, f.eks. timer, som angivet i feltet **Enhedskode** på linjen. Du kan finde flere oplysninger i [Oprette vareenheder](inventory-how-setup-units-of-measure.md).

    Værdien i feltet **Linjebeløb** beregnes som *Enhedspris* x *Antal*.  

    Prisen og linjebeløbene er med eller uden moms, afhængigt af hvad du har valgt i feltet **Priser inkl. moms** på debitorkortet.  
12. Hvis du vil give en rabat, skal du angive en procentdel i feltet **Linjerabatpct.**. Værdien i feltet **Linjebeløb** opdateres tilsvarende.  

    Hvis der er konfigureret specialvarepriser i oversigtspanelet **Salgspriser og salgslinjerabatter** på debitor- eller varekortet, opdateres linjerabatprocenten, prisen og beløbet på salgslinjen automatisk, hvis priskriterierne er opfyldt. Du kan finde flere oplysninger under [Registrere salgspris, rabat og betalingsaftaler](sales-how-record-sales-price-discount-payment-agreements.md).  
13. Gentag trin 9 til 12 for hvert produkt, du ønsker at tilbyde debitoren.

    Totalerne under linjerne beregnes automatisk, mens du opretter eller redigerer linjer.  
14. I feltet **Fakturarabatbeløb** skal du indtaste et beløb, der trækkes fra den værdi, der vises i feltet **I alt inkl. moms**.

    Hvis du har konfigureret fakturarabatter til debitoren, indsættes den angivne procentværdi automatisk i feltet **Fakturarabat i %**, hvis kriterierne er opfyldt, og det relaterede beløb indsættes i feltet **Fakturarabat ekskl. moms**. Du kan finde flere oplysninger under [Registrere salgspris, rabat og betalingsaftaler](sales-how-record-sales-price-discount-payment-agreements.md).

    > [!TIP]
    > Feltet **Tilbud gyldigt til dato** kan udfyldes automatisk med et bestemt antal dage efter oprettelsen af tilbuddet, hvis du udfylder feltet **Beregning af tilbuddets gyldighed** på siden **Salg**.

15. Når salgstilbudslinjerne er fuldført, skal du vælge handlingen **Send via mail**.
16. På siden **Send mail** skal du udfylde de resterende felter og gennemse det integrerede salgstilbud. Du kan finde flere oplysninger under [Sende dokumenter via mail](ui-how-send-documents-email.md).
17. Hvis kunden accepterer tilbuddet, skal du vælge handlingen **Opret faktura** eller **Lav ordre**.

Salgstilbuddet fjernes fra databasen. En salgsfaktura eller salgsordre oprettes på grundlag af oplysningerne i salgstilbuddet, hvor du kan behandle salget. I feltet **Tilbudsnr.** på salgsfakturaen eller salgsordren kan du se nummeret på det salgstilbud, den blev oprettet ud fra. Du kan finde flere oplysninger i [Fakturere salg](sales-how-invoice-sales.md) eller [Sælge produkter](sales-how-sell-products.md).

## <a name="see-also"></a>Se også
[Salg](sales-manage-sales.md)  
[Konfigurere salg](sales-setup-sales.md)  
[Sende dokumenter som mail](ui-how-send-documents-email.md)  
[Arbejde med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)
