---
title: Administrere projektforsyninger
description: Bruges til at beskrive forskellige måder at administrere forsyning og køb af materialer og tjenester til projekter på.
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bholtorf
ms.topic: how-to
ms.search.keywords: 'project management, material, purchase'
ms.search.form: '98, 1020'
ms.date: 02/22/2024
ms.service: dynamics-365-business-central
ms.custom: bap-template
---
# Administrere projektforsyninger

Du skal administrere projektforsyninger i form af varer, tjenester og udgifter som et integreret og vigtigt aspekt for alle projekter. Du kan benytte lagerbeholdningsantal eller oprette projektspecifikke køb vha. købsordrer eller købsfakturaer. Et serviceprojekt på en computer kræver f.eks. en ny disk. Du opretter en købsfaktura for at købe en ny disk og registrerer det projekt, der bruger disken.

Hvis købsprocessen ikke kræver, at du registrerer den fysiske transaktion separat, kan du behandle købet på siden **Projektfinanskladder**. Du kan finde flere oplysninger i [Sådan bogføres en projektrelateret udgift](projects-how-manage-project-supplies.md#to-post-a-project-related-expense).

## Sådan køber du varer eller tjenesteydelser for et projekt

Følgende procedure viser, hvordan du bruger en købsfaktura til at købe produkter for et projekt. Samme fremgangsmåde anvendes, når du anvender en købsordre.  

1. Vælg det ![lyspæreikon, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **Købsfakturaer**, og vælg derefter det relaterede link.  
2. Vælg handlingen **Ny**, og udfyld felterne efter behov. Du kan finde flere oplysninger i [Registrere køb](purchasing-how-record-purchases.md).
3. I feltet **Projektnr.** og **Projektopgavenr.** skal du vælge oplysningerne for det projekt, som du vil købe varer eller tjenester til. Brug tilpasningsværktøjerne, hvis et felt ikke er synligt. Du kan finde flere oplysninger i [Tilpasse dit arbejdsområde](ui-personalization-user.md).

    Den værdi, du har valgt i feltet **Projektlinjetype**, angiver, om der oprettes en planlægningslinje, når du bogfører forbruget af varen. Hvis feltet indeholder **Fakturerbar**, oprettes der projektplanlægningslinjer, som er klar til blive faktureret til kunden. Du kan finde flere oplysninger i [Fakturere projekter](projects-how-invoice-jobs.md).
4. Vælg handlingen **Bogfør**.

## Sådan får du vist værdien for køb for et projekt

1. Vælg ![Lightbulb, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **Projekter**, og vælg derefter det relaterede link.
2. Åbn et relevant projektkort.

    På oversigtspanelet **Opgaver** viser feltet **Udestående ordrer** det samlede udestående beløb i lokal valuta for lagervarer og tjenester på købsdokumenter for projektopgavelinjen.  

    Feltet **Modt. beløb (ufakt.)** viser værdien af de varer, der er leveret på købsdokumenter, men endnu ikke faktureret.  
3. Vælg et af felterne for at åbne siden **Købslinjer**, hvor kan du gennemse oplysninger om de relaterede købsdokumentlinjer, herunder hvilke varer eller tjenesteydelser der er modtaget.

## Sådan bogføres en projektrelateret udgift

Hvis der påløber specielle udgifter eller engangsudgifter for projekter, kan du bruge siden **Projektfinanskladde** til at bogføre dem direkte på den relevante projektkonto.

1. Vælg det ![lyspæreikon, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") , skriv **Projektfinanskladder**, og vælg derefter det relaterede link.  
2. Opret en ny linje, og angiv oplysninger om udgiften, inklusive oplysninger i felterne **Projektnr.** og **Projektopgavenr.**  
3. Når kladden er fuldført, skal du vælge handlingen **Bogfør**.

## Se også

[Projektstyring](projects-manage-projects.md)  
[Finans](finance.md)  
[Køb](purchasing-manage-purchasing.md)  
[Salg](sales-manage-sales.md)  
[Arbejde med Business Central](ui-work-product.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
