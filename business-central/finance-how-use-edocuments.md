---
title: Bruge e-dokumenter i salg og køb
description: 'Lære, hvordan du bruger e-dokumentfunktioner, der er relateret til salgs- og købsfakturaer.'
author: altotovi
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 'electronic document, electronic invoice, e-document, e-invoice, sales, purchase'
ms.search.form: '42, 43, 51, 6103, 6133, 6121, 9301, 9305, 9308'
ms.date: 10/03/2023
ms.author: altotovi
---

# Bruge e-dokumenter i salg og køb

Du kan bruge konfigurerede elektroniske dokumenter (e-dokumenter) sammen med salgs- og købsdokumenter.

Du kan bruge følgende dokumenter med e-dokumenters funktioner:  

- Salg: 
    - Salgsfakturaer
    - Salgsordrer
    - Salgskreditnotaer
    - Servicefakturaer
    - Servicekreditnotaer
    - Rentenotaer
    - Rykkere
- Køb: 
    - Købsfakturaer
    - Købsordrer (opret kun nyt dokument)
    - Købskreditnotaer
    - Finanskladder

> [!NOTE]
> I øjeblikket kan en købsordre kun bruges, når du opretter dokumentet fra e-dokumentet fra leverandøren. Du kan dog ikke opdatere det eksisterende dokument med linjer, som du har fået fra kreditoren.  

## E-dokumenter i salg

For at oprette og sende en e-faktura til en kunde skal du oprette og bogføre salgsfakturaen. Du kan få mere at vide om standardprocessen under [Fakturere salg](sales-how-invoice-sales.md).

Når du har bogført salgsdokumentet, skal du åbne siden **Bogført salgsfaktura** for at få adgang til den relaterede side **E-dokument**.

### Vise e-dokumenter

Følg disse trin for at få vist eksisterende e-dokumenter.

1. På siden **Bogført salgsfaktura** skal du vælge **e-dokument** \> **Åbn e-dokument**.
2. På siden **e-dokument** i hovedet kan du få vist grundlæggende oplysninger om den bogførte faktura.
3. Feltet **Post** viser dokumentnummeret på det bogførte salgsfaktura. Vælg linket til at åbne dokumentet.
4. I feltet **Status for elektroniske dokumenter** kan du få vist dokumentets status i realtid og dets placering i procespipelinen. Hvis dokumentet er bogført, er status **Behandlet**.

### Logfiler for e-dokumentstatusser

Du kan finde flere oplysninger om servicestatusniveauet for dit e-dokument i oversigtspanelet **E-dokumentservicestatus**. På linjerne viser systemet en eller flere tjenester, som dokumentet har brugt. I det mest almindelige scenarie bruger hvert dokument kun én tjeneste. Et dokument kan dog bruge flere tjenester.

- Se feltet **E-dokumentservicekode** for at finde ud af, hvilken service der blev brugt.
- Se feltet **Status for e-dokument** for at bestemme den aktuelle servicestatus for dette dokument.
- Hvis du vil have flere oplysninger, skal du vælge feltet **Logfiler** for tjenesten på siden **E-dokumentlogfiler**. Der vises en kronologisk oversigt over de forskellige statusser for dokumentet.
- Tjek **løbenummeret** og **Oprettet den** og andre oplysninger på siden **E-dokumentlogfiler**. I feltet **E-dokumentstatus** er den første status **Eksporteret**, hvilket angiver, at e-dokumentfilen er oprettet. Den næste status er **Sendt**, hvilket angiver, at dokumentet er sendt til tjenesteudbyderen, hvis det er konfigureret.

Du kan få mere indsigt ved at vælge den post, der har statussen **Eksporteret**, og derefter udføre en af følgende handlinger:

- **Åbn tilknytningslogfiler** – Få et overblik over alle eksporterede felter fra kildetabellerne i feltet **Oprindelig værdi**. Hvis du har brugt transformationsregler i eksportprocessen, kan du også hente den endelige værdi i feltet **Ny værdi**.
- **Eksportér fil** – Eksportér XML-filen til manuel gennemgang.

Hvis du vil have vist kommunikationen mellem dig selv og den tjeneste, du sender dokumentet til, skal du bruge feltet **Kommunikationslogfiler**. Åbn siden **E-dokumentkommunikationslogfiler** for at få vist oplysninger om meddelelsen om anmodningen og årsagerne til den pågældende tjeneste.

Hvis der er et problem med tjenesteudbyderen, og dokumentet ikke kan sendes, skal du se efter følgende indikatorer på siden **E-dokument**:

- Feltet **Status for elektronisk dokument** i hovedet viser **Fejlstatus**.
- Feltet **Status for e-dokument** i oversigtspanelet **Status for e-dokumenttjeneste** viser status for **Afsendelsesfejl**.
- Oversigtspanelet **Fejl og advarsler** indeholder en eller flere meddelelser, der angiver årsagen til problemet.

Når problemet er løst, skal du manuelt køre handlingerne **Send dokumenter**. Hvis du har brug for forskellige handlinger, f.eks. **Genoprettede dokument**, **Annuller dokument** eller **Hent godkendelse**, kan du køre dem.

## E-dokumenter i køb

Modtagelse af elektroniske købsfakturaer i Dynamics 365 Business Central kan udføres som en kørsel eller manuelt.

### Kør batchjobbet

> [!NOTE]
> Dette batchjob bruges til automatisk opkrævning af indgående fakturaer. Det kan kun fungere i et land eller område, hvor funktionaliteten findes.

Hver gang der køres en opgavekø, og den eksterne tjeneste har indgående fakturaer, der er sendt fra din leverandør, indsamler og importerer systemet disse fakturaer. Udfør disse trin for at fuldføre processen.

1. Når kørslen er færdig, vises de nyligt importerede fakturaer på siden **E-dokumenter** sammen med deres grundlæggende detaljerede oplysninger.
2. Hvis du vil se flere detaljer, skal du åbne et bestemt e-dokument.
3. Hvis der ikke var nogen fejl eller problemer i e-dokumentet, og det er tilknyttet, viser feltet **Post** bilagsnummeret på den købsfaktura, som systemet oprettede automatisk. Vælg linket til at åbne dokumentet. Dette systemoprettede dokument er ikke det bogførte dokument.
4. Hvis du vil gå direkte til købsdokumentet, skal du markere feltet **Post**. Kontroller dokumentet, når du har åbnet siden **Købsfaktura**. Derefter, hvis alt er korrekt, skal du bogføre dokumentet.
5. Når du bogfører købsdokumentet, opdateres feltet **Post** på **E-dokumentet** fra **Faktura** til **Købsfaktura** og nummeret på det bogførte købsdokument er tilgængeligt. Du kan vælge nummeret til at åbne den bogførte købsfaktura.

Oplysningerne om logfiler er de samme som i salgsprocessen for e-dokumenter.

Da fejl i salgsprocessen for det meste er relateret til tilgængeligheden af tjenesten, kan det indgående bilag indeholde flere årsager. Den mest almindelige årsag til en fejl er, at systemet ikke kan genkende linjerne på det e-dokument, du har fået fra leverandøren. Derfor kan det ikke indsætte linjer på din købsfaktura.

Der er to almindelige fejl:

- Hvis du vil bruge denne specifikke linje fra kreditorfakturaen, som blev bogført direkte på finanskontoen, skal du have konfigureret værdien for **Tilknyttet tekst** korrekt. Hvis du vil tilsidesætte denne fejl, hvis du vil bruge finanskonti, skal du vælge **Knyt tekst til konto** for at oprette en specifik tilknytning af værdien **Tilknyttet tekst** med den **Debetkontonr.**-værdi, som du vil bruge.
- Hvis du vil spore lagerbeholdningen og bruge linjer fra kreditorfakturaen til at udfylde varer på dokumentlinjerne, skal du have konfigureret **Varereferencenr.** korrekt værdi. Hvis du vil omgå denne fejl, skal du knytte den eksterne vare til dine varenumre ved hjælp af varereferenceoversigten. Du kan finde flere oplysninger i [Bruge varereferencer](inventory-how-use-item-cross-refs.md).

Når du har rettet fejlene og advarslerne, kan du manuelt angive, hvornår systemet skal oprette en købsfaktura baseret på din opsætning, ved at vælge **Opret dokument**.

### Importer fakturaer manuelt

Følg disse trin for manuelt at importere eksterne e-dokumenter.

1. Vælg ![Lightbulb, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **e-dokumenttjeneste**, og vælg derefter det relaterede link.
2. Vælg den aktive tjeneste på siden **E-dokumenttjeneste**. 
3. Vælg **Modtag**, og overfør den e-dokumentfil, du fik fra kreditoren.
4. Hvis der vises en fejlmeddelelse, skal du åbne e-dokumentet for at løse problemerne.
5. Når du er færdig med at løse problemerne, skal du vælge **Opret dokument** i gruppen **Importér manuelt**.
6. Når dokumentet er oprettet i Business Central, kan du få det vist på samme måde, som hvis du bruger et batchjob.

## Oversigt over e-dokumentstatusser

Hvis du vil have et bedre overblik over alle e-dokumenter i regnskabet, kan du vælge rollecenteret **Bogholder**, hvor der findes e-dokumentstatusser. Der kan du finde e-dokumentaktiviteter, der har følgende statusser:

- **Udgående e-dokumenter:**

    - Behandlet
    - Igangværende
    - Fejl

- **Indgående e-dokumenter:**

    - Behandlet
    - Igangværende
    - Fejl

## Se også

[Sådan konfigureres e-dokumenter i Business Central](finance-how-setup-edocuments.md)  
[Sådan udvides e-dokumenter i Business Central](/dynamics365/business-central/dev-itpro/developer/devenv-extend-edocuments)  
[Økonomistyring](finance.md)  
[Fakturasalg](sales-how-invoice-sales.md)  
[Registrere køb med købsfakturaer og ordrer](purchasing-how-record-purchases.md)  
[Arbejd med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)

[!INCLUDE[footer-include](includes/footer-banner.md)]
