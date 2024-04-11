---
title: Revaluere finanskontosaldi
description: 'Have mere at vide om, hvordan du justerer saldi på finanskonti, før du udarbejder regnskaber.'
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bnielse
ms.topic: conceptual
ms.date: 03/14/2024
ms.custom: bap-template
ms.search.form: null
ms.service: dynamics-365-business-central
---

# Revaluere finanskontosaldi

Hvis du bruger finanskonti til at registrere balanceposter i udenlandsk valuta, bør du revaluere kontosaldiene, inden du udarbejder årsregnskaber. Valutakurser ændres ofte, og værdiregulering hjælper med at gøre dine regnskaber mere nøjagtige.

## Konfigurer til værdievalueringer

Du definerer hver konto, som du vil medtage i reguleringer på siden **Finanskort**. Du kan vælge, om værdireguleringsreguleringer skal bogføres på realiserede eller urealiserede gevinst-/tabskonti. Bogføring af gevinster og tab under en valutakursregulering følger den normale bogføringsrutine. Du skal f.eks. gøre det for hver opsætning på siden **Valutaer**. Du kan få mere at vide om valutakursreguleringer ved at gå til [Opdater valutakurser](finance-how-update-currencies.md).

For at minimere fejl kan du i feltet **Bogføring af kildevaluta** oprette en validering af de valutaer, som du vil tillade at bogføre på individuelle finanskonti:

* Alle valutaer (tom)
* Flere valutaer
* Samme valuta
* Lokal valuta

## Kør en regulering

Hvis du vil regulere beløbene i udenlandsk valuta i lokal valuta for finanskontosaldi, skal du bruge handlingen **Værdiregulering** af finansvaluta på siden **Kontoplan** til at starte en kørsel. Kørslen opretter reguleringsposter i den kladde, du vælger. Når du bogfører posterne, regulerer du saldoen i den lokale valuta (RV) for kontoen. De finanskonti, der altid vises i RV, afspejler nu ændringer i de valutaer, som posterne er bogført i. Denne værdiregulering giver dig mulighed for at oprette et mere nøjagtigt regnskab med mindre indsats.

Hvis du bruger en ekstra rapporteringsvaluta (EV), har finansværdireguleringsposterne et ACY-beløb. Det beløb, der kun svarer til RV-beløbet på disse poster, ikke ACY-saldoen på finanskontoen. Hvis du regulerer ACY-kurserne, efter du har bogført reguleringerne, skal du udføre valutakursreguleringen én gang til for at regulere alle finansposter.

> [!IMPORTANT]
> Værdiregulering af finanskonti opfylder muligvis ikke alle krav til transaktions- og aktivregistreringer, der kræver værdiregulering. Det kan f.eks. være for finansielle instrumenter, værdipapirer, leasede aktiver, eller hvis du bruger dem til specifikke eller store mængder transaktioner eller aktiver. Vi anbefaler, at du drøfter med din revisor, om du kan bruge funktionen, og i så fald hvordan du skal bruge den. Det kan f.eks. være, om du vil tillade, at valutaer blandes for en konto, eller om du skal have en separat konto for hvert aktiv, du vil spore.

> [!NOTE]
> Værdiregulering giver ikke mulighed for at udligne eller annullere udligning af poster, som du kan med debitor- og kreditorposter. Reguleringer sker på saldo pr. valutabasis.

## Revurdere konti vs. valutakursreguleringer for debitor og kreditor

Værdireguleringen gør det lettere at regulere saldi for finanskonti. Funktionen justerer saldoen pr. valuta pr. finanskonto på samme måde, som du gør ved reguleringer af finanskonti, der er knyttet til bankkonti. Hvis du bruger en finanskonto til at spore flere aktiver, kan du overveje at bruge en kreditor- eller debitorkonto i stedet.

> [!NOTE]
> Værdiregulering af finanskonti opfylder muligvis ikke alle krav til transaktions- og aktivregistreringer, der kræver værdiregulering. Det kan f.eks. være for finansielle instrumenter, værdipapirer, leasede aktiver, eller hvis du bruger dem til specifikke eller store mængder transaktioner eller aktiver. Vi anbefaler, at du drøfter med din revisor, om du kan bruge funktionen, og i så fald hvordan du skal bruge den. Det kan f.eks. være, om du vil tillade, at valutaer blandes for en konto, eller om du skal have en separat konto for hvert aktiv, du vil spore.

Følgende eksempler illustrerer forskellen mellem at bruge en finanskonto og en kreditorkonto til at spore saldoen for to monetære aktiver, der bruger en udenlandsk valuta.

**Brug en finanskonto** Hvis du bruger én finanskonto til at spore enten flere aktiver (f.eks. lån eller anlægsaktiver) i samme valuta eller individuelle deltransaktioner for det samme aktiv, men stadig i samme valuta, foretages der én post pr. værdiregulering for valutaen. Det betyder, at du ikke kan spore reguleringer relateret til individuelle aktiver eller individuelle transaktioner for det samme aktiv.

**Bruge en kreditorkonto** Hvis du opretter flere anlægsaktiver som kreditorer og bogfører transaktioner til dem i enten samme eller forskellige valutaer, får du en regulering pr. valuta pr. kreditor. Eller hvis du slår **Bogføring pr. post** til for opgavekøposten **Reguler valutakurs**, får du en reguleringspost for hver separat kreditorpost.

Denne forskel er vigtig, når du vurderer, om finansværdiregulering er den rigtige funktion for dig i forhold til dine rapporteringsbehov.

> [!TIP]
> Vi anbefaler, at du spørger din revisor eller revisor, hvilken type konto der er bedst for din virksomhed. Der kan også være en app til [!INCLUDE [prod_short](includes/prod_short.md)] i [AppSource](https://appsource.microsoft.com/en-us/marketplace/apps?page=1&product=dynamics-365-business-central) , der passer lige til dine forretningsscenarier.

## Se også

[Gennemse beløb i finanskonti](finance-review-accounts.md)  
[Forstå Finans og Kontoplan](finance-general-ledger.md)  
