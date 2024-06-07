---
title: Konfigurere betalingsformer (indeholder video)
description: 'Du bruger betalingsformer, for eksempel check, bankoverførsel, kontant eller PayPal, til at definere, hvordan salgs- og købsfakturaer skal betales.'
author: brentholtorf
ms.topic: conceptual
ms.devlang: al
ms.search.keywords: 'check, bank transfer, cash, PayPal'
ms.search.form: 427
ms.date: 04/01/2021
ms.author: bholtorf
ms.service: dynamics-365-business-central
---
# Konfigurere betalingsmetoder

Betalingsformer definerer, hvordan du foretrækker, at debitorer skal betale dig, og hvordan du foretrækker at betale dine kreditorer. Metoden kan variere for hver debitor eller kreditor. Eksempler på typiske betalingsformer er **bank**, **kontant**, **check** eller **konto**.

Du kan knytte en betalingsmetode til debitorer og kreditorer, så den samme metode altid bruges på de salgs- og købsdokumenter, du opretter til dem. Du kan om nødvendigt ændre metoden på salgs- eller købsdokumentet. F.eks. hvis du vil betale en bestemt købsfaktura kontant og frem for med check. Dette ændrer ikke den betalingsmetode, der som standard er knyttet til kreditoren.

De samme betalingsmetoder bruges til salgs- og købsdokumenter. F.eks. bruges en _kontant_-betalingsmetode både ved indbetalinger, du foretager, og når du modtager betalinger. [!INCLUDE[prod_short](includes/prod_short.md)] ved, at når du opretter en salgsfaktura, forventer du at modtage betaling, og det modsatte for købsfakturaer.

Kreditnotaer for returneringer er dog undtagelser, fordi pengene flyder den modsatte vej, dvs. fra dig til dine kunder og fra din leverandør til dig. Derfor tildeles der ikke en standardbetalingsmetode til kreditnotaer. Der er dog en løsning, hvis du har angivet betalingsbetingelser for debitoren eller kreditoren. Selvom feltet **Beregn kont.rabat på kred.notaer** ikke er beregnet til dette, og du markerer afkrydsningsfeltet på siden **Betalingsbetingelser**, tilføjes en standardbetalingsmetode, når du opretter en kreditnota. <br><br>  

> [!Video https://www.microsoft.com/videoplayer/embed/RE476Ys?rel=0]

## Sådan defineres en betalingsform

[!INCLUDE[prod_short](includes/prod_short.md)] indeholder et par betalingsmetoder, som virksomheder ofte bruger. Du kan dog tilføje lige så mange, du vil.

1. Vælg ![Lightbulb, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **Betalingsformer**, og vælg derefter det relaterede link.
2. Udfyld felterne efter behov. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

Du kan også tilføje betalingsbetingelser til betalingsmetoden. Du kan finde flere oplysninger i [Oprette betalingsbetingelser](finance-payment-terms.md).  

## Sådan tildeles en betalingsmetode til en debitor eller kreditor

1. Vælg ![Lightbulb, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **Debitor** eller **Kreditor**, og vælg derefter det relaterede link.
2. I feltet **Betalingsformkode** skal du vælge metoden, der skal bruges som standard for debitoren eller kreditoren.

## Se også

[Registrere nye debitorer](sales-how-register-new-customers.md)  
[Konfigurere betalingsvilkår](finance-payment-terms.md)  
[Finans](finance.md)  
[Arbejd med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
