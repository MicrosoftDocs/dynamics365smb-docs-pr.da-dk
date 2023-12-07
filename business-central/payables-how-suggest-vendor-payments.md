---
title: Foreslå kørsel af kreditorbetalinger
description: Du kan angive indstillinger for kreditorbetaling for at få forslag til betalinger.
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bnielse
ms.topic: conceptual
ms.search.keywords: 'vendor payment, creditor, debt, balance due, AP'
ms.search.form: '256,'
ms.date: 09/07/2023
ms.custom: bap-template
---
# <a name="suggest-vendor-payments"></a>Lav kreditorbetalingsforslag

På siden **Udbetalingskladde** kan du bruge kørslen **Lav kreditorbetalingsforslag** til at foreslå betalingslinjer. Foreslår ud fra dine indstillinger [!INCLUDE [prod_short](includes/prod_short.md)]-betalingslinjer:

* Betalinger, der snart forfalder
* Betalinger, hvor en kontantrabat er tilgængelig

For at få det fulde udbytte af betalingsforslag skal du først prioritere dine kreditorer. Du kan få mere at vide om prioritering af kreditorer ved at gå til [Prioriter kreditorer](purchasing-how-prioritize-vendors.md).  

> [!NOTE]  
> Kørslen omfatter ikke kreditorposter, der er **Afvent**, eller som allerede er udlignet, og som har en værdi i feltet **Udlignings-id**.  

> [!IMPORTANT]  
> Hvis du vil have fordel af kontantrabatter og har indtastet et disponibelt beløb, bliver beløbet brugt til:  
>
> * Prioriterede forfaldne kreditorposter først i prioriteret rækkefølge.
> * Forfaldne kreditorposter, der ikke er prioriteret.  
> * Åbne kreditorposter, hvor der ydes kontantrabat. Posterne er ordnet efter kreditornummer.  

## <a name="use-the-suggest-vendor-payments-action"></a>Sådan bruges funktionen Lav kreditorbetalingsforslag

1. Vælg ![Lightbulb, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **Udbetalingskladder**, og vælg derefter det relaterede link.  
2. Åbn kladden, og vælg derefter handlingen **Lav kreditorbetalingsforslag**.  
3. Udfyld felterne efter behov. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]  
4. Vælg knappen **OK**.  

## <a name="insert-the-due-date-as-posting-date-on-payment-journal-lines"></a>Sådan indsættes forfaldsdatoen som bogføringsdato på betalingskladdelinjer

Når du udfører kørslen **Lav kreditorbetalingsforslag** til at oprette betalingslinjer for dine kreditorer, kan du udfylde to særlige felter for at sikre, at de genererede linjer bruger forfaldsdatoen til at beregne bogføringsdatoen. Disse felter er **Beregn bogføringsdato fra forfaldsdato for udligningsbilag** og **Forskydning af forfaldsdato for udligningsbilag**.  

> [!IMPORTANT]  
> Du kan ikke bruge feltet **Beregn bogføringsdato fra forfaldsdato for udligningsbilag** sammen med **Find kontantrabatter** eller feltet **Sammenfat pr. kreditor**. Hvis bogføringsdatoen er baseret på forfaldsdatoen, beregnes nogle kontantrabatter måske ikke korrekt, da bogføringsdatoen ligger efter kontantrabatdatoen.  

Hvis den beregnede bogføringsdato er i fortiden, bliver bogføringsdatoen desuden flyttet til arbejdsdatoen, og der vises en advarsel.  

Du kan også manuelt oprette betalingslinjer ved at bruge forfaldsdatoen til at beregne bogføringsdatoen. Når du udligner kreditorposter, kan du bruge handlingen **Beregn bogføringsdato** til at opdatere bogføringsdatoen på kladdelinjen med forfaldsdatoen for den relaterede købsfaktura. Du kan få mere at vide om denne manuelle proces ved at gå til [Udlign købstransaktioner manuelt](payables-how-apply-purchase-transactions-manually.md).  

> [!NOTE]  
> Hvis købsfakturaen er overskredet, bliver bogføringsdatoen indstillet til arbejdsdatoen, og skrifttypen på linjen bliver rød.  

## <a name="see-also"></a>Se også

[Administrere skyldige beløb](payables-manage-payables.md)  
[Foretage betaling](payables-make-payments.md)  
[Arbejde med finanskladder](ui-work-general-journals.md)  
[Arbejd med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
