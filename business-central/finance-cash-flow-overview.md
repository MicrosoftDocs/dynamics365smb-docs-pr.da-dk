---
title: Oversigt over pengestrøm
description: 'En oversigt over indgående og udgående pengestrømme for at hjælpe med at forudsige penge, der skal modtages og udbetales.'
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bholtorf
ms.topic: overview
ms.devlang: al
ms.search.keywords: 'cash flow, money flow, expense and income, liquidity, cash receipts minus cash payments'
ms.search.form: '841, 849, 1818'
ms.date: 07/31/2024
ms.service: dynamics-365-business-central
---

# Oversigt over pengestrøm

Forståelse af pengestrømme og udstrømninger er nøglen til at drive en succesrig virksomhed. Du kan bruge likviditet til nemt for at oprette en kortfristet forecast, der forudsiger, hvordan og hvornår du kan forvente at modtage penge og skal betale penge i din virksomhed. Det er vigtigt at vide, at din virksomhed har nok penge til at betale gæld og udgifter, når de forfalder.

## Definition af likviditet

Betegnelsen *likviditet* bruges til at angive indbetalinger minus kontantbetalinger over en valgt periode. Det er et skøn over det beløb, du forventer, vil flyde ind og ud af din virksomhed, og det omfatter alle de forventede indtægter og udgifter.

## Arbejde med pengestrøm

Følgende illustration viser en oversigt over, hvordan du kan arbejde med likviditet.

![Oversigt over likviditet.](media/finance_cash_flow_overview.png "Oversigt over likviditet")

- Du konfigurerer et likviditetsforecast.  

- Du kan få likviditetsforecastkilder fra følgende områder:  

  - Finans – oplysninger om likvide midler og budgetterede indtægter og udgifter for din virksomhed.  
  - Køb – oplysninger om de aktuelle skyldige beløb og budgetterede fordringer fra åbne købsordrer.  
  - Salg – oplysninger om de aktuelle tilgodehavender og budgetterede indbetalinger fra åbne salgsordrer.  
  - Service – oplysninger om åbne serviceordrer.  
  - Anlægsaktiver – oplysninger om planlagte bortskaffelser og budgetterede køb af anlæg.  
  - Manuelle indtægter og udgifter – administrer manuelle indtægter og udgifter og medtag dem i likviditetsforecastet.  
- Brug en kørsel til at overføre oplysninger fra områderne finans, indkøb, salg, service og faste anlægsaktiver til pengestrømskladden. Du skal bruge kørslen til at lave en pengestrømsprognose.  
- Du kan bruge forskellige sider, rapporter og diagrammer til at analysere og udskrive en likviditetsforecast, der vedrører tilgængelighed og oversigter på tidslinjen.  

## Foretage likviditetsforecast

Baseret på registrerede kladdelinjer kan du med jævne mellemrum foretage en likviditetsforecast. Følgende layout er et ofte anvendt layout for en likviditetsforecast. Layout indeholder tre sektioner:

- Indbetaling kladde  
- Kontante udbetalinger  
- Nettolikviditet eller kontanter i hånden  

Indbetalinger giver oplysninger om den indtægt, som virksomheden modtager.

*indbetalinger i alt* = *tilgodehavender* + *åbne salgsordrer* + *åbne serviceordrer* + *afhændelse af faste anlægsaktiver* + *manuelle indtægter* + *budgetterede indtægter*

> [!NOTE]
> Manuelle indtægter kan være lejeindtægt, renter fra finansielle aktiver eller ny privat kapital. Du kan planlægge manuelle indtægter for et tidsrum og bruge dem til beregning af likviditetsforecast.

Kontante udbetalinger giver oplysninger om betalinger foretaget af virksomheden.

*kontante udbetalinger i alt* = *skyldige beløb* + *åbne købsordrer* + *investering i anlæg* + *manuelle udgifter* + *budgetterede udgifter*

> [!NOTE]
> Manuelle udgifter kan være lønninger, renter på kredit eller privat forbrug. Du kan planlægge manuelle udgifter for et tidsrum og bruge dem til beregning af likviditetsforecast.

Nettolikviditet eller kontanter i hånden beregnes som samlede indtægter minus samlede udbetalinger i slutningen af hver periode.

*nettolikviditet* = *samlede indbetalinger* – *samlede kontante udbetalinger* + *likvide midler*

Du kan bruge budgettet som et internt beslutningsværktøj til ledelsen, som hjælper dig med at planlægge og foretage vigtige strategiske beslutninger om driften af virksomheden.

## Se også

[Opsætning af pengestrømsanalyse](finance-setup-cash-flow-analyses.md)  
[Analysér pengestrøm](finance-analyze-cash-flow.md)  
[Pengestrømsprognose i Dynamics 365 Business Central](/training/modules/forecast-cash-flow-dynamics-365-business-central/index)  
[Konfigurere pengestrømsprognoser vha. Azure AI i Dynamics 365 Business Central](/training/modules/setup-cash-flow-forecasts/)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
