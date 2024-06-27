---
title: Opsætte betalingsmetoder
description: 'Du bruger betalingsformer, for eksempel check, bankoverførsel, kontant eller PayPal, til at definere, hvordan salgs- og købsfakturaer er betalt.'
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bholtorf
ms.topic: conceptual
ms.devlang: al
ms.search.keywords: 'check, bank transfer, cash, PayPal'
ms.search.form: '427,'
ms.date: 06/10/2024
ms.service: dynamics-365-business-central
---
# <a name="set-up-payment-methods"></a>Opsætte betalingsmetoder

Betalingsformer definerer, hvordan du foretrækker, at debitorer skal betale dig, og hvordan du foretrækker at betale dine kreditorer. Metoden kan variere for hver debitor eller kreditor. Eksempler på typiske betalingsformer er **bank**, **kontant**, **check** eller **konto**.

Du kan knytte en betalingsmetode til debitorer og kreditorer, så den samme metode altid bruges på de salgs- og købsdokumenter, du opretter til dem. Du kan om nødvendigt ændre metoden på salgs- eller købsdokumentet. F.eks. hvis du vil betale en bestemt købsfaktura kontant og frem for med check. Den betalingsmetode, der som standard er knyttet til kreditoren, ændres ikke.

De samme betalingsmetoder bruges til salgs- og købsdokumenter. En _kontant_-betalingsmetode bruges f.eks. til at udføre indbetalinger og modtage betalinger. [!INCLUDE[prod_short](includes/prod_short.md)] ved, at når du opretter en salgsfaktura, forventer du at modtage betaling, og det modsatte for købsfakturaer.

Kreditnotaer for returneringer er dog undtagelser, fordi pengene flyder den modsatte vej, dvs. fra dig til dine kunder og fra din leverandør til dig. Derfor tildeles der ikke en standardbetalingsmetode til kreditnotaer. Der er dog en løsning. Du kan angive betalingsbetingelser for debitoren eller kreditoren. Selvom feltet **Beregn kont.rabat på kred.notaer** ikke er beregnet til denne løsning, og du markerer afkrydsningsfeltet på siden **Betalingsbetingelser**, tilføjes en standardbetalingsmetode, når du opretter en kreditnota. <br><br>  

> [!Video https://www.microsoft.com/videoplayer/embed/RE476Ys?rel=0]

## <a name="to-set-up-a-payment-method"></a>Sådan defineres en betalingsform

[!INCLUDE[prod_short](includes/prod_short.md)] indeholder et par betalingsmetoder, som virksomheder ofte bruger. Du kan dog tilføje lige så mange, du vil.

1. Vælg ![Lightbulb, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **Betalingsformer**, og vælg derefter det relaterede link.
2. Udfyld felterne efter behov. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

Du kan også tilføje betalingsbetingelser til betalingsmetoden. Du kan finde flere oplysninger i [Oprette betalingsbetingelser](finance-payment-terms.md).  

## <a name="to-assign-a-payment-method-to-a-customer-or-vendor"></a>Sådan tildeles en betalingsmetode til en debitor eller kreditor

1. Vælg ![Lightbulb, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **Debitor** eller **Kreditor**, og vælg derefter det relaterede link.
2. I feltet **Betalingsformkode** skal du vælge metoden, der skal bruges som standard for debitoren eller kreditoren.

## <a name="see-also"></a>Se også

[Registrere nye debitorer](sales-how-register-new-customers.md)  
[Konfigurere betalingsvilkår](finance-payment-terms.md)  
[Finans](finance.md)  
[Arbejd med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
