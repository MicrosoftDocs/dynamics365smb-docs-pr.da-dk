---
title: Oprette salgstilbud
description: 'Beskriver, hvordan du opretter et salgstilbuds- eller tilbudsanmodningsdokument for at registrere dit tilbud til en kunde om at sælge produkter i henhold til bestemte betingelser.'
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: rfq
ms.search.form: '41, 9300'
ms.date: 07/12/2021
ms.author: edupont
---
# Oprette salgstilbud

Du opretter et salgstilbud for at registrere dit tilbud til en debitor eller et emne om at sælge bestemte produkter på bestemte leverings- og betalingsbetingelser. Du kan sende salgstilbuddet til debitoren for at kommunikere tilbuddet. Du kan sende dokumentet i en mail som en vedhæftet PDF-fil. Du kan også få brødteksten i mailen udfyldt med en oversigt over tilbuddet. Du kan finde flere oplysninger i [Sende dokumenter via mail](ui-how-send-documents-email.md).

Mens du forhandler med debitoren eller om emnet, kan du ændre og gensende salgstilbuddet så meget, som det er nødvendigt. Når debitoren accepterer tilbuddet, kan du konverterer salgstilbuddet til en salgsfaktura eller en salgsordre, hvor du behandler salget. Du kan finde flere oplysninger i [Fakturere salg](sales-how-invoice-sales.md) eller [Sælge produkter](sales-how-sell-products.md).

I de fleste tilfælde sender du salgstilbud til potentielle kunder. Du har ofte en kontaktperson, som du kan forhandle med. Hvis de derefter accepterer tilbuddet, kan du konvertere salgstilbuddet til en ordre og registrere kundeemnet som kunde i [!INCLUDE [prod_short](includes/prod_short.md)]. I følgende procedure fokuseres der på kontakter, men du kan også sende tilbud til eksisterende kunder.  

## Sådan oprettes et salgstilbud

1. Vælg ![Lightbulb, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **Salgstilbud**, og vælg derefter det relaterede link.
2. Angiv den kontakt eller debitor, som du vil sende salgstilbuddet til.

    - Hvis salgstilbuddet vedrører en eksisterende kontakt, skal du angive navnet i feltet **Kontaktnr.** .  

        Hvis salgstilbuddet vedrører en eksisterende debitor, skal du angive debitoren i feltet **Debitor**.
    - Hvis kontakten ikke er registreret, skal du følge disse trin:

        1. I felterne **Kontraktnr.** skal du vælge knappen Rediger :::image type="icon" source="media/assist-edit-icon.png" border="false":::.
        2. Vælg den nye handling i dialogboksen for at vælge kontakten **Ny** og udfyld derefter de relevante felter. [!INCLUDE [tooltip-inline-tip_md](includes/tooltip-inline-tip_md.md)] Du kan finde flere oplysninger i [Oprette kontakter](marketing-create-contact-companies.md).  
        3. Når du har udfyldt kontaktkortet, skal du vælge den nyoprettede kontakt på listen over kontakter og derefter vælge knappen OK for at vende tilbage til salgstilbuddet.

        En række af felterne i salgstilbuddet er nu udfyldt med oplysninger, der er angivet på det nye kontaktkort.

        > [!NOTE]
        > Hvis du vil beregne moms og priser for et tilbud korrekt, skal du vælge den relevante debitorskabelon i feltet **Kundeskabelonkode**. Skabelonen vil blive brugt til at konvertere kontakten til en debitor, når tilbuddet er konverteret til en salgsordre eller en faktura.
    -  Hvis tilbuddet er til en ny kunde, skal du tilføje debitoren. Du kan finde flere oplysninger i [Registrere nye debitorer](sales-how-register-new-customers.md).  

3. Udfylde de resterende felter efter behov på siden **Salgstilbud**. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]  

    Du er nu klar til at udfylde salgsordrelinjerne for produkter, du sælger til debitoren, eller til andre transaktioner med debitoren om emnet, som du vil registrere i en finanskonto.  

    Hvis du har konfigureret de tilbagevendende salgslinjer for debitoren, f.eks en månedlig genbestillingsordre, kan du indsætte disse linjer i ordren ved at vælge handlingen **Hent tilbagevendende salgslinjer**.  

4. I oversigtspanelet **Linjer** i feltet **Type** skal du vælge, hvilken type produkt, gebyr eller transaktion, som du vil bogføre for debitoren med salgslinjen.
5. I feltet **Nummer** skal du vælge en post, der skal bogføres i overensstemmelse med værdien i feltet **Type**.

    Lad feltet **Nummer** være tomt i følgende tilfælde:
    - Hvis der er tale om en kommentar. Skriv bemærkningen i feltet **Beskrivelse**.
    - Hvis der er tale om en katalogvare. Vælg handlingen **Vælg katalogvarer**. Du kan finde flere oplysninger i [Arbejde med katalogvarer](inventory-how-work-nonstock-items.md).

6. I feltet **Antal** skal du angive, hvor mange enheder af produktet, gebyret eller transaktion, som linjen skal registrere for debitoren.

    > [!NOTE]  
    >  Hvis varen er af typen **Service**, eller hvis feltet **Type** indeholder **Ressource**, er antallet en tidsenhed, f.eks. timer, som angivet i feltet **Enhedskode** på linjen. Du kan finde flere oplysninger i [Oprette vareenheder](inventory-how-setup-units-of-measure.md).

    Værdien i feltet **Linjebeløb** beregnes som *Enhedspris* x *Antal*.  

    Prisen og linjebeløbene er med eller uden moms, afhængigt af hvad du har valgt i feltet **Priser inkl. moms** på debitorkortet.  
7. Hvis du vil give en rabat, skal du angive en procentdel i feltet **Linjerabatpct.**. Værdien i feltet **Linjebeløb** opdateres tilsvarende.  

    Hvis der er konfigureret specialvarepriser i oversigtspanelet **Salgspriser og salgslinjerabatter** på debitor- eller varekortet, opdateres linjerabatprocenten, prisen og beløbet på salgslinjen automatisk, hvis priskriterierne er opfyldt. Du kan finde flere oplysninger i [Registrere salgspris, rabat og betalingsaftaler](sales-how-record-sales-price-discount-payment-agreements.md).  
8. Gentag trin 4 til 7 for hvert produkt, du ønsker at tilbyde kontakten.

    Totalerne under linjerne beregnes automatisk, mens du opretter eller redigerer linjer.  
9. I feltet **Fakturarabatbeløb** skal du indtaste et beløb, der trækkes fra den værdi, der vises i feltet **I alt inkl. moms**.

    Hvis du har konfigureret fakturarabatter til debitoren, indsættes den angivne procentværdi automatisk i feltet **Fakturarabat i %**, hvis kriterierne er opfyldt, og det relaterede beløb indsættes i feltet **Fakturarabat ekskl. moms**. Du kan finde flere oplysninger i [Registrere salgspris, rabat og betalingsaftaler](sales-how-record-sales-price-discount-payment-agreements.md).

    > [!TIP]
    > Feltet **Tilbud gyldigt til dato** kan udfyldes automatisk med et bestemt antal dage efter oprettelsen af tilbuddet, hvis du udfylder feltet **Beregning af tilbuddets gyldighed** på siden **Salg**.

10. Når salgstilbudslinjerne er fuldført, skal du vælge handlingen **Send via mail**.
11. På siden **Send mail** skal du udfylde de resterende felter og gennemse det integrerede salgstilbud. Du kan finde flere oplysninger i [Sende dokumenter via mail](ui-how-send-documents-email.md).
12. Hvis kontaktpersonen accepterer tilbuddet, skal du vælge **Lav ordre**-handlingen.  

    Hvis organisationen foretrækker denne proces, skal du vælge handlingen **Opret faktura**.  
    > [!NOTE]
    > Hvis du har tilføjet en kunde i trin 2, bliver du bedt om at bekræfte konverteringen af tilbuddet til en ordre.  
    >
    > Hvis du har føjet en kontaktperson fra en mulig kunde i trin 2, bliver du bedt om at gøre følgende:
    >
    >  - Konvertere kontaktpersonen eller kundeemnet til en kunde ved at vælge en af skabeloner til konvertering af kontaktpersoner. Du kan finde flere oplysninger i [Sådan oprettes en debitor-, kreditor-, medarbejder- eller bankkonto fra en kontakt](marketing-create-contact-companies.md#to-create-a-customer-vendor-employee-or-bank-account-from-a-contact).  
    > - Bekræft konverteringen af tilbuddet til en ordre.

Konverteringen fjerner salgstilbuddet fra databasen. En salgsfaktura eller salgsordre oprettes på grundlag af oplysningerne i salgstilbuddet, hvor du kan behandle salget. I feltet **Tilbudsnr.** på salgsfakturaen eller salgsordren kan du se nummeret på det salgstilbud, den blev oprettet ud fra. Du kan finde flere oplysninger i [Fakturere salg](sales-how-invoice-sales.md) eller [Sælge produkter](sales-how-sell-products.md).  

## Eksterne bilagsnumre

[!INCLUDE [ext-doc-no-sales](includes/ext-doc-no-sales.md)]

## Se relateret [Microsoft-træning](/training/modules/create-sales-documents-dynamics-365-business-central/)

## Se også

[Salg](sales-manage-sales.md)  
[Konfigurere salg](sales-setup-sales.md)  
[Sende dokumenter som mail](ui-how-send-documents-email.md)  
[Arkivere dokumenter](across-how-to-archive-documents.md)  
[Arbejd med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
