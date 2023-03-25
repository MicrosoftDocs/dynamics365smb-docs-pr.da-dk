---
title: Foreslå kørsel af kreditorbetalinger
description: 'Du kan angive kreditorbetalingsindstillinger for at få vist forslag eller forslag til betalinger, der forfalder snart, eller hvor en rabat er tilgængelig.'
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 'vendor payment, creditor, debt, balance due, AP'
ms.search.form: 256
ms.date: 04/01/2021
ms.author: edupont
---
# Lav forslag

På siden **Udbetalingskladde** kan du bruge kørslen **Lav kreditorbetalingsforslag** til at foreslå betalingslinjer. Linjer til betalinger, som snart forfalder, eller betalinger, hvor en kontantrabat er tilgængelig, foreslås baseret på dine indstillinger.

For at få det fulde udbytte af betalingsforslag skal du først prioritere dine kreditorer. Du kan finde flere oplysninger i [Tildele kreditorer prioritet](purchasing-how-prioritize-vendors.md).  

> [!NOTE]  
> Kreditorposter, der er markeret med **Afvent**, medtages ikke.  

> [!IMPORTANT]  
>   Hvis du vil have fordel af kontantrabatter og har indtastet et disponibelt beløb, bliver beløbet brugt til:  
    * Prioriterede forfaldne kreditorposter først i prioriteret rækkefølge.   
    * Forfaldne kreditorposter, der ikke er prioriteret.  
    * Åbne kreditorposter, hvor der ydes kontantrabat, arrangeret efter kreditornummer.  

## Sådan bruges funktionen Lav kreditorbetalingsforslag

1. Vælg ![Lightbulb, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **Udbetalingskladder**, og vælg derefter det relaterede link.  
2. Åbn den relevante kladde, og vælg derefter handlingen **Lav kreditorbetalingsforslag**.  
3. Udfyld felterne efter behov. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]  
4. Vælg knappen **OK**.  

## Sådan indsættes forfaldsdatoen som bogføringsdato på betalingskladdelinjer

Når du udfører kørslen **Lav kreditorbetalingsforslag** til at oprette betalingslinjer for dine kreditorer, kan du udfylde to særlige felter for at sikre, at de genererede linjer bruger forfaldsdatoen til at beregne bogføringsdatoen. Disse felter er **Beregn bogføringsdato fra forfaldsdato for udligningsbilag** og **Forskydning af forfaldsdato for udligningsbilag**.  

> [!IMPORTANT]  
>   Du kan ikke bruge feltet **Beregn bogføringsdato fra forfaldsdato for udligningsbilag** sammen med **Find kontantrabatter** eller feltet **Sammenfat pr. kreditor**. Hvis bogføringsdatoen er baseret på forfaldsdatoen, beregnes nogle kontantrabatter måske ikke korrekt, da bogføringsdatoen ligger efter kontantrabatdatoen.  

Hvis den beregnede bogføringsdato er i fortiden, bliver bogføringsdatoen desuden flyttet til arbejdsdatoen, og der vises en advarsel.  

Du kan manuelt oprette betalingslinjer ved at bruge forfaldsdatoen til at beregne bogføringsdatoen. Når du udligner kreditorposter, kan du bruge handlingen **Beregn bogføringsdato** til at opdatere bogføringsdatoen på kladdelinjen med forfaldsdatoen for den relaterede købsfaktura. Du kan finde flere oplysninger i [Udligne købstransaktioner manuelt](payables-how-apply-purchase-transactions-manually.md).  

> [!NOTE]  
>   Hvis købsfakturaen er overskredet, bliver bogføringsdatoen indstillet til arbejdsdatoen, og skrifttypen på linjen bliver rød.  

## Se relateret [Microsoft-træning](/training/modules/suggest-vendor-payments-dynamics-365-business-central/)

## Se også

[Administrere skyldige beløb](payables-manage-payables.md)  
[Foretage betaling](payables-make-payments.md)  
[Arbejde med finanskladder](ui-work-general-journals.md)  
[Arbejd med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
