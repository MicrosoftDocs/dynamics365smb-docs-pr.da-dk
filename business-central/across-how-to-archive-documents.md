---
title: Arkivere salgs- og købsdokumenter
description: 'Du kan arkivere salgs-og købsordrer, tilbud, returvareordrer og rammeordrer.'
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bholtorf
ms.topic: how-to
ms.date: 02/26/2024
ms.custom: bap-template
ms.search.form: '42, 49, 50, 459, 460, 5159, 5162, 5164, 5167, 6627, 6630, 6644, 9305, 9306, 9346, 9347, 9348, 9349'
ms.service: dynamics-365-business-central
---
# <a name="archive-documents"></a>Arkivere dokumenter

Du kan arkivere salgs-og købsordrer, tilbud, returvareordrer og rammeordrer. Hvis du bruger projektstyringsfunktioner, kan du også arkivere dine projekter. Du kan arkiverer dokumenter og projekter flere gange samt gemme en ny arkiveret version hver gang.

For salgsdokumenter, hvor originalen stadig findes og ikke er bogført, kan du bruge funktionen **Gendan**, hvis du vil overskrive det med en arkiveret version. 

> [!NOTE]
> Du kan kun gendanne salgsdokumenter og projekter. Handlingen er ikke tilgængelig for arkiverede købsdokumenter.

Du kan genbruge indholdet i arkiverede dokumenter, hvis originalen er slettet, ved at kopiere dataene, for eksempel med handlingen **Kopiér fra dokument**.  

## <a name="to-set-up-automatic-document-archiving"></a>Sådan konfigurerer du automatisk dokumentarkivering

Du kan automatisere arkivering for at oprette en ny version af det arkiverede dokument, når nogen udfører følgende opgaver:

* Ændrer eller sletter et dokument eller et projekt.
* Udskriver, henter eller sender et dokument med e-mail.
* Konverterer et tilbud til en ordre eller en faktura.
* Bogfører en ordre.

I følgende procedure beskrives, hvordan du konfigurerer automatisk arkivering af salgsdokumenter fra siden **Salgsopsætning**. Trinene er de samme for alle købsdokumenter og projekter. Hvis du har købt dokumenter, skal du bruge siden **Køb og Gæld**. For projekter skal du bruge siden **Projektopsætning**.

1. Vælg det ![lyspæreikon, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, angiv **Salgsopsætning**, og vælg derefter det relaterede link.
2. I oversigtspanelet **arkivering** skal du angive, om der skal slås automatisk arkivering til de forskellige typer salgsdokumenter. [!INCLUDE [tooltip-inline-tip_md](includes/tooltip-inline-tip_md.md)]

I følgende tabel beskrives indstillingerne for feltet **Arkivér tilbud**.

|Indstilling|Beskrivelse|
|------|-----------|
|**Aldrig**| Arkivér aldrig salgstilbud, når de er slettet.|
|**Spørgsmål**|Spørg brugeren om at vælge, om salgstilbud skal arkiveres, når de slettes.|
|**Altid**|Arkivér automatisk salgstilbud, når de slettes.|

## <a name="to-manually-archive-a-sales-order"></a>Sådan arkiveres en salgsordre manuelt

Nedenstående procedure beskriver, hvordan du arkiverer en salgsordre manuelt. Trinene er de samme for alle de dokumenter og projekter, du kan arkivere.

1. Vælg ![Lightbulb, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **Salgsordrer**, og vælg derefter det relaterede link.  
2. Åbn en salgsordre, som du vil arkivere.  
3. Vælg handlingen **Arkivér bilag**.

Salgsordren arkiveres. Du kan se den på siden **Arkiverede salgsordrer**.

## <a name="to-restore-a-non-posted-sales-document-or-a-project-from-the-archive"></a>Sådan gendannes et ikke-bogført dokument eller projekt fra arkivet

Følgende procedure beskriver, hvordan du gendanner en arkiveret salgsordre tilbage til den oprindelige salgsordre. Gendannelse af et dokument er kun muligt, når det oprindelige dokument ikke er bogført. Fremgangsmåden er den samme for alle ordrer, rammeordrer, returvareordrer og tilbud samt for projekter.

1. Vælg det ![lyspæreikon, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **Salgsordrearkiver**, og vælg derefter det relaterede link.
2. Vælg den arkiverede salgsordre eller en version af den, som du vil gendanne, og vælg derefter handlingen **Gendan**.  

Oplysningerne i den oprindelige salgsordre eller projekter erstattes med oplysningerne fra den valgte arkiverede version.

## <a name="to-delete-archived-versions"></a>Slette arkiverede versioner

Brug en opbevaringspolitik til at rydde op i arkiverede versioner, som du ikke længere har brug for. Opbevaringspolitikker lader administratorer definere, hvor lang tid de vil gemme data. De kan f.eks. oprette en politik, der sletter data efter en udløbsdato. Du kan få mere at vide i [Definere opbevaringspolitikker](admin-data-retention-policies.md).

Der er et par ting, du skal være opmærksom på, når du opretter opbevaringspolitikker for arkiverede dokumenter og projekter:

* Hvis det oprindelige dokument ikke er slettet, sletter [!INCLUDE [prod_short](includes/prod_short.md)] ikke arkiverede versioner. Arkiverede versioner udløber ikke, så længe originalen findes.
* Når du konfigurerer opbevaringspolitikken, kan du angive, at politikken skal slette alle arkiverede versioner, undtagen den seneste. Du kan f.eks. have 10 versioner og vil beholde en kopi af den seneste. 
* [!INCLUDE [prod_short](includes/prod_short.md)] beregner udløbsdatoen for dokumenter baseret på datoen for den senest arkiverede version.

## <a name="see-also"></a>Se også

[Spore bilagslinjer](across-how-to-track-document-lines.md)  
[Salg](sales-manage-sales.md)  
[Generelle forretningsfunktioner](ui-across-business-areas.md)  
[Arbejd med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)

[!INCLUDE[footer-include](includes/footer-banner.md)]
