---
title: Tilbagevendende standardsalgslinjer
description: 'Du kan oprette ofte brugte salgslinjer og indsætte dem i salgsdokumenter, som du hurtigt kan udfylde linjerne med standardoplysninger.'
author: brentholtorf
ms.topic: conceptual
ms.devlang: al
ms.search.keywords: 'trade, sell, replenishment'
ms.search.form: 172
ms.date: 07/06/2022
ms.author: bholtorf
ms.service: dynamics-365-business-central
---
# Opret tilbagevendende salg

Hvis du ofte har brug at oprette salgslinjer med næsten ens oplysninger, kan du oprette standardlinjer, som du derefter kan indsætte i tilbagevendende salgsdokumenter, f.eks. for tilbagevendende genbestillingsordrer.  

## Konfigurer gentagne salgslinjer

1. Vælg ![Lightbulb, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **Tilbagevendende salgslinjer**, og vælg derefter det relaterede link.  
2. På siden **Gentagne salgslinjer** skal du vælge **Ny**.  
3. Udfyld felterne efter behov i oversigtspanelet **Generelt**. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]  
4. I oversigtspanelet **Linjer** skal du angive oplysninger i felterne for at forberede salgslinjer, der afspejler de standardlinjer, du forventer at bruge som tilbagevendende linjerne på salgsdokumenter.  

> [!NOTE]
> Du kan ikke definere priser på gentagne salgslinjer, fordi priser, rabatter osv. beregnes ud fra de faktiske salgsdokumenter, når du har indsat de gentagne salgslinjer.

[!INCLUDE [line-no-info](includes/line-no-info.md)]

## Tildel gentagne salgslinjer til en debitor

Tildele en eller flere gentagne salgslinjer til en debitor, så de kan indsættes i salgsdokumenter for den pågældende debitor.

1. Vælg ![Lightbulb, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **Kunder**, og vælg derefter det relaterede link.
2. Åbn jobkortet for den relevante debitor.
3. Vælg handlingen **Tilbagevendende salgslinjer**.
4. På siden **Tilbagevendende salgslinjer** skal du vælge koder for de gentagne salgslinjer, som du vil kunne indsætte i salgsdokumenter for kunden.
5. Udfyld de andre felter for at definere, hvornår, hvordan og hvor de gentagne salgslinjer skal bruges.  

    Hvis du vil bruge de tilbagevendende salgslinjer, der er indstillet, sammen med kørslen **Opret tilbagevendende salgsfakturaer**, skal du også udfylde felterne **Datoen Gyldig fra** og **Datoen Gyldig til** for at begrænse, hvornår tilbagevendende salgslinjer bruges til oprettelse af fakturaer. Du kan finde flere oplysninger i [Opret flere salgsfakturaer baseret på standardsalgslinjer](sales-how-work-standard-lines.md#create-multiple-sales-invoices-based-on-recurring-sales-lines).

    Du kan også angive en Direct Debit-betalingsform og Direct Debit-betalingsaftale. Salgsfakturaer, der er oprettet med kørslen **Opret tilbagevendende salgsfakturaer**, vil derefter indeholde oplysninger, der skal bruges til at opkræve betaling for salgsfakturaer med SEPA-Direct Debit. Du kan finde flere oplysninger i [Indhente betalinger med SEPA Direct Debit](finance-collect-payments-with-sepa-direct-debit.md).

6. I de fire felter hvor du vælger, hvordan linjerne indsættes på fire dokumenttyper, skal du vælge en af følgende indstillinger:

|Indstilling|Beskrivelse|
|------|-----------|
|**Manuelt**|Du skal manuelt søge efter og indsætte en gentaget salgslinje, som findes for debitoren.|
|**Automatisk**|Hvis der findes flere gentagne salgslinjer for debitoren, får du en notifikation om, hvorfra du kan vælge den, der skal indsættes. Hvis der kun findes én gentagen salgslinje, indsættes den automatisk.<br /><br />Dette kun fungerer, hvis det nye dokument blev oprettet fra en bilagsliste, f.eks. ved at vælge handlingen **Ny** på siden **Salgsordrer**. Det fungerer ikke, hvis dokumentet blev oprettet på f.eks. et debitorkort.|
|**Spørg altid**|Der vises en meddelelse, og alle eksisterende tilbagevendende salgslinjer vises, så du kan vælge én af dem.

## Indsæt tilbagevendende salgslinjer i en salgsfaktura

Hvis der findes gentagne salgslinjerne for debitoren, kan du indsætte dem eller få dem indsat i alle typer salgsdokumenter, f.eks. en salgsfaktura. Hvis du har aktiveret indstillingen **Spørg altid**, når du tildeler gentagne salgslinjer til debitorer, får du besked, hvis der findes gentagne salgslinjer.

1. Vælg ![Lightbulb, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **Salgsfakturaer**, og vælg derefter det relaterede link.
2. Åbn den salgsfaktura, som du vil indsætte en eller flere standardsalgslinjer i.
3. Vælg handlingen **Hent tilbagevendende salgslinjer**.
4. På siden **Tilbagevendende salgslinjer** skal du vælge på opslagsknappen i feltet **Kode** og derefter vælge en række standardsalgslinjer.
5. Vælg knappen **OK** for at indsætte standardsalgslinjerne på fakturaen, hvor du kan genbruge dem eller redigere oplysningerne.

## Opret flere salgsfakturaer baseret på tilbagevendende salgslinjer

Du kan bruge kørslen **Opret tilbagevendende salgsfakturaer** til at oprette salgsfakturaer i overensstemmelse med standardsalgslinjer, som er knyttet til kunderne og med bogføringsdatoer inden for de gyldige fra- og til-datoer, som du angiver i standardsalgslinjerne.

1. Vælg ![Lightbulb, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **Opret tilbagevendende salgsfakturaer**, og vælg derefter det relaterede link.
2. Udfyld felterne efter behov på siden **Opret tilbagevendende salgsfakturaer**.
3. I filterfeltet **Kode** skal du angive den kode for standardsalgslinjer, der er knyttet til en debitor, som du vil oprette salgsfakturaer for.
4. Vælg knappen **OK**.

Salgsfakturaer oprettes for kunder med den angivne standarddebitorsalgskode og eventuelle angivne oplysninger om direkte debitering for bogføring på den angivne dato.

## Se også

[Salg](sales-manage-sales.md)  
[Konfigurere salg](sales-setup-sales.md)  
[Oprette tilbagevendende købslinjer](purchasing-how-work-recurring-purchase-lines.md)  
[Arbejd med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
