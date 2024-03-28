---
title: Tilbagevendende standardkøbslinjer
description: 'Du kan oprette ofte brugte købslinjer og købslinjer og indsætte dem i købsdokumenter, som du hurtigt kan udfylde linjerne med standardoplysninger.'
author: brentholtorf
ms.topic: conceptual
ms.devlang: al
ms.search.keywords: 'trade, purchase, replenishment'
ms.search.form: 177
ms.date: 07/06/2022
ms.author: bholtorf
ms.service: dynamics-365-business-central
---
# <a name="create-recurring-purchase-lines"></a>Opret tilbagevendende købslinjer

Hvis du ofte har brug at oprette købslinjer med næsten ens oplysninger, kan du oprette standardlinjer, som du derefter kan indsætte i tilbagevendende købsdokumenter, f.eks. for tilbagevendende genbestillingsordrer.

## <a name="set-up-recurring-purchase-lines"></a>Konfigurer gentagne købslinjer

1. Vælg ![Lightbulb, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **Tilbagevendende købslinjer**, og vælg derefter det relaterede link.
2. På siden **Gentagne købslinjer** skal du vælge **Ny**.
3. Udfyld felterne efter behov i oversigtspanelet **Generelt**. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
4. I oversigtspanelet **Linjer** skal du angive oplysninger i felterne for at forberede salgslinjer, der afspejler de standardlinjer, du forventer at bruge som tilbagevendende linjerne på købsdokumenter.

> [!NOTE]
> Du kan ikke definere priser på gentagne købslinjer, fordi priser, rabatter osv. beregnes ud fra de faktiske købsdokumenter, når du har indsat de gentagne købslinjer.

[!INCLUDE [line-no-info](includes/line-no-info.md)]

## <a name="assign-recurring-purchase-lines-to-a-vendor"></a>Tildele tilbagevendende købslinjer til en kreditor

Tildele en eller flere gentagne købslinjer til en kreditor, så de kan indsættes i købsdokumenter for den pågældende kreditor.

1. Vælg ![Lightbulb, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **Leverandører**, og vælg derefter det relaterede link.
2. Åbn kortet for den relevante kreditor.
3. Vælg handlingen **Tilbagevendende købslinjer**.
4. På siden **Tilbagevendende købslinjer** skal du vælge koder for de gentagne købslinjer, som du vil kunne indsætte i købsdokumenter for kreditor.
5. Udfyld de andre felter for at definere, hvornår, hvordan og hvor de gentagne købslinjer skal bruges.
6. I de fire felter hvor du vælger, hvordan linjerne indsættes på hver dokumenttype, skal du vælge en af følgende indstillinger:

|Indstilling|Beskrivelse|
|------|-----------|
|**Manuelt**|Du skal manuelt søge efter og indsætte en gentaget købslinje, som findes for kreditor.|
|**Automatisk**|Hvis der findes flere gentagne købslinjer for kreditoren, får du en notifikation om, hvorfra du kan vælge den, der skal indsættes. Hvis der kun findes én gentagen købslinje, indsættes den automatisk.<br /><br />Dette fungerer kun, hvis det nye dokument blev oprettet fra en bilagsliste, f.eks. ved at vælge handlingen **Ny** på siden **Købsordrer**. Det fungerer ikke, hvis dokumentet blev oprettet på f.eks. et kreditorkort.|
|**Spørg altid**|Der vises en meddelelse, og alle eksisterende tilbagevendende købslinjer vises, så du kan vælge én af dem.

## <a name="insert-recurring-purchase-lines-on-a-purchase-invoice"></a>Indsæt gentagne købslinjer på en købsfaktura

Hvis der findes gentagne købslinjerne for kreditoren, kan du indsætte dem eller få dem automatisk indsat i alle typer købsdokumenter, f.eks. en købsfaktura. Hvis du har aktiveret indstillingen **Spørg altid**, når du tildeler gentagne købslinjer til kreditorer, får du besked, hvis der findes gentagne købslinjer.

1. Vælg ![Lightbulb, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **Købsfakturaer**, og vælg derefter det relaterede link.
2. Åbn den købsfaktura, som du vil indsætte en eller flere standardkøbslinjer i.
3. Vælg handlingen **Hent tilbagevendende købslinjer**.
4. På siden **Tilbagevendende købslinjer** skal du vælge på opslagsknappen i feltet **Kode** og derefter vælge en række standardkøbslinjer.
5. Vælg knappen **OK** for at indsætte standardkøbslinjerne på fakturaen, hvor du kan genbruge dem eller redigere oplysningerne.

## <a name="see-also"></a>Se også

[Køb](purchasing-manage-purchasing.md)  
[Konfigurere indkøb](purchasing-setup-purchasing.md)  
[Opret tilbagevendende salg](sales-how-work-standard-lines.md)  
[Arbejd med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
