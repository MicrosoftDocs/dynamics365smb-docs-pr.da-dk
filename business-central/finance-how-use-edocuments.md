---
title: Brug e-dokumenter i salg
description: 'Lære, hvordan du bruger e-dokumentfunktioner, der er relateret til salg.'
author: altotovi
ms.topic: conceptual
ms.devlang: al
ms.search.keywords: 'electronic document, electronic invoice, e-document, e-invoice, sales, deliver'
ms.search.form: '42, 43, 132, 6103, 6133, 6121, 9301, 9305'
ms.date: 04/10/2024
ms.author: altotovi
ms.service: dynamics-365-business-central
ms.reviewer: bholtorf
---

# Bruge e-dokumenter i salgsprocessen

Du kan bruge konfigurerede elektroniske dokumenter (e-dokumenter) sammen med salgsdokumenter.

Du kan bruge følgende salgsdokumenter med e-dokumenters funktioner:  

- Salgsfakturaer
- Salgsordrer
- Salgskreditnotaer
- Servicefakturaer
- Servicekreditnotaer
- Rentenotaer
- Rykkere

## E-dokumenter i salg  

For at oprette og sende en e-faktura til en kunde skal du oprette og bogføre salgsfakturaen. Du kan få mere at vide om standardprocessen under [Fakturere salg](sales-how-invoice-sales.md).

Når du har bogført salgsdokumentet, skal du åbne siden **Bogførte salgsfakturaer** for at få adgang til den relaterede side **E-dokumenter**.

### Vise e-dokumenter   

Følg disse trin for at få vist eksisterende e-dokumenter.

1. På siden **Bogførte salgsfakturaer** skal du vælge **E-dokument** og derefter **Åbn E-dokument**.
2. På siden **E-dokumenter** kan du på sidehovedet få vist grundlæggende oplysninger om den bogførte faktura.
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

Hvis der er et problem med tjenesteudbyderen, og dokumentet ikke kan sendes, skal du se efter følgende indikatorer på siden **E-dokumenter**:

- Feltet **Status for elektronisk dokument** i hovedet viser **Fejlstatus**.
- Feltet **Status for e-dokument** i oversigtspanelet **Status for e-dokumenttjeneste** viser status for **Afsendelsesfejl**.
- Oversigtspanelet **Fejl og advarsler** indeholder en eller flere meddelelser, der angiver årsagen til problemet.

Når problemet er løst, skal du manuelt køre handlingerne **Send dokumenter**. Hvis du har brug for forskellige handlinger, f.eks. **Genoprettede dokument**, **Annuller dokument** eller **Hent godkendelse**, kan du køre dem.

## Oversigt over e-dokumentstatusser

Hvis du vil have et bedre overblik over alle e-dokumenter i regnskabet, kan du vælge rollecenteret **Bogholder**, hvor der findes e-dokumentstatusser. Der kan du finde e-dokumentaktiviteter, der har følgende statusser:

- **Udgående e-dokumenter:**

    - Behandlet
    - Igangværende
    - Fejl


## Se også

[Sådan kan du opsætte e-dokumenter i [!INCLUDE[prod_short](includes/prod_short.md)]](finance-how-setup-edocuments.md)    
[Sådan bruges e-dokumenter i køb](finance-how-use-edocuments-purchase.md)  
[Sådan udvides e-dokumenter i [!INCLUDE[prod_short](includes/prod_short.md)]](/dynamics365/business-central/dev-itpro/developer/devenv-extend-edocuments)    
[Økonomistyring](finance.md)    
[Fakturere salg](sales-how-invoice-sales.md)    
[Registrere køb med købsfakturaer og ordrer](purchasing-how-record-purchases.md)    
[Arbejd med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
