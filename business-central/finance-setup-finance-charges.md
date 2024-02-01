---
title: Konfiguration af Rentebetingelser
description: 'Se her, hvordan du konfigurerer Business Central, så du kan underrette debitorerne om tilføjede gebyrer ved at sende rentenotaer.'
author: brentholtorf
ms.topic: conceptual
ms.devlang: al
ms.search.keywords: 'payment due, debt, overdue, fee, charge'
ms.search.form: '6, 494'
ms.date: 04/01/2021
ms.author: bholtorf
ms.service: dynamics-365-business-central
---
# Konfiguration af Rentebetingelser

Når en debitor ikke betaler til forfaldsdatoen, kan du automatisk få en rentenota beregnet og føje den til de forfaldne beløb på debitorens konto. Du kan underrette debitor om de tilføjede gebyrer ved at sende rentenotaen. Først skal du definere en kode, der repræsenterer for hver renteberegningsmetode. Du kan så angive denne kode i feltet Rentebetingelseskode på debitorkortene.  

## Rentebetingelser

Du skal definere rentebetingelser for hver renteberegning og derefter knytte betingelserne til debitoren i feltet **Rentebetingelseskode** på siden **Debitor**.

Rentenotaer kan beregnes efter kreditkronedage- eller saldorentemetoder.

* Gennemsnitlig daglig saldo  
  
  Der tages hensyn til det antal dage, betalingsfristen er overskredet med:  
  *Metoden Kreditkronedage* - *Rente* = *Forfalden saldo* x *(Kreditdage/Renteperiode)* x *(Rentesats/100)*

* Forf. beløb  
  
  Rentegebyret er blot en procentdel af den forfaldne saldo:  
  *Saldorenteprincippet* - *Rente* = *Forfalden saldo* x *(Rentesats/100)*

Hver kode i tabellen Rentebetingelser er desuden kædet sammen med en undertabel, nemlig tabellen Rentenotatekst. Til hver rentebetingelse kan du definere en starttekst og/eller en sluttekst, som skal vises på rentenotaen.

### Sådan konfigurerer du rentebetingelser

1. Vælg ![Lightbulb, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **Rentebetingelser**, og vælg derefter det relaterede link.  
2. Udfyld felterne efter behov.
3. Hvis du vil bruge mere end én kombination af rentebetingelser, kan du angive en kode for hver enkelt.

    For hver rentebetingelse kan du angive individuelle betingelser, som kan omfatte ekstra gebyrer i både lokal og udenlandsk valuta. Du kan definere adskillige opkrævningsgebyrer i udenlandsk valuta for hver kode på siden **Rentebetingelser**.
4. Vælg handlingen **Valutaer**.
5. På siden **Valutaer til rentebetingelser** skal du for hver periode angive en valutakode og et opkrævningsgebyr.

    > [!NOTE]  
    > Når du beregner renter i en udenlandsk valuta, bruges de betingelser for udenlandsk valuta, som du angiver her, til at oprette rentenotaer. Hvis der ikke er defineret rentebetingelser i udenlandske valutaer, bruges rentebetingelserne i den regnskabsvaluta, der er angivet på siden **Rentebetingelser**, og de konverteres derefter til den relevante valuta.

    For hver rentebetingelse kan du angive tekst, der udskrives før (**Starttekst**) eller efter (**Sluttekst**) på posterne i rentenotaen.  
6. Vælg henholdsvis handlingen **Starttekst** eller **Sluttekst**, og udfyld siden **Rentenotatekst**.
7. Hvis du vil indsætte relaterede værdier i den resulterende rentenotatekst automatisk, skal du angive følgende pladsholdere i feltet **Tekst**.

|Pladsholder|Værdi|  
|-----------------|-----------|  
|%1|Indholdet af feltet **Bilagsdato** på rentenotahovedet|  
|%2|Indholdet af feltet **Forfaldsdato** på rentenotahovedet|  
|%3|Indholdet af feltet **Rentesats** på de relaterede rentebetingelser|  
|%4|Indholdet af feltet **Restbeløb** i rentenotahovedet|  
|%5|Indholdet af feltet **Rentebeløb** i rentenotahovedet|  
|%6|Indholdet af feltet **Opkrævningsgebyr** i rentenotahovedet|  
|%7|Rykkerens totalbeløb|  
|%8|Indholdet af feltet **Valutadato** på rentenotahovedet|  
|%9|Indholdet af feltet **Bogføringsdato** i rentenotahovedet|  

## Se også

[Indhente udestående beløb](receivables-collect-outstanding-balances.md)  
[Konfiguration af rykkerbetingelser og -niveauer](finance-setup-reminders.md)  
[Konfigurere Finans](finance-setup-finance.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
