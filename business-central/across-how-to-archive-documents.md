---
title: Arkivere salgs- og købsdokumenter
description: 'Du kan arkivere salgs-og købsordrer, tilbud, returvareordrer og rammeordrer.'
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bholtorf
ms.topic: how-to
ms.date: 08/18/2023
ms.custom: bap-template
ms.search.form: '42, 49, 50, 459, 460, 5159, 5162, 5164, 5167, 6627, 6630, 6644, 9305, 9306, 9346, 9347, 9348, 9349'
---
# <a name="archive-documents"></a>Arkivere dokumenter

Du kan arkivere salgs-og købsordrer, tilbud, returvareordrer og rammeordrer. Du kan arkiverer et salgs- eller købsdokument flere gange og gemme en ny arkiveret version hver gang.

For arkiverede salgsdokumenter, hvor originalen stadig findes og ikke er bogført, kan du bruge funktionen **Gendan**, hvis du vil overskrive det aktuelle dokument med en arkiveret version. Handlingen kan kun bruges til salgsdokumenter.

Du kan kun genbruge indholdet i arkiverede dokumenter, hvis originalen er slettet, ved at kopiere dataene, for eksempel med handlingen **Kopiér fra dokument**.  

## <a name="to-set-up-automatic-document-archiving"></a>Sådan konfigurerer du automatisk dokumentarkivering

Du kan konfigurere automatisk arkivering af salgs- og indkøbsordrer, tilbud, rammeordrer og returordrer. Når automatisk arkivering er aktiveret, oprettes der en ny version af det arkiverede dokument, når nogen udfører følgende opgaver:

* Ændrer eller sletter et dokument.
* Udskriver, henter eller sender et dokument med e-mail.
* Konverterer et tilbud til en ordre eller en faktura.
* Bogfører en ordre.

Nedenstående fremgangsmåde beskriver konfigurationen af automatisk arkivering af salgsdokumenter. Fremgangsmåden er den samme for købsdokumenter.

1. Vælg ![Lightbulb, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, angiv **Salgsopsætning**, og vælg derefter det relaterede link.
2. I oversigtspanelet **arkivering** skal du angive, om der skal slås automatisk arkivering til de forskellige typer salgsdokumenter. [!INCLUDE [tooltip-inline-tip_md](includes/tooltip-inline-tip_md.md)]

I følgende tabel beskrives indstillingerne for feltet **Arkivér tilbud**.

|Indstilling|Beskrivelse|
|------|-----------|
|**Aldrig**| Arkivér aldrig salgstilbud, når de er slettet.|
|**Spørgsmål**|Spørg brugeren om at vælge, om salgstilbud skal arkiveres, når de slettes.|
|**Altid**|Arkivér automatisk salgstilbud, når de slettes.|

## <a name="to-manually-archive-a-sales-order"></a>Sådan arkiveres en salgsordre manuelt

Nedenstående procedure beskriver, hvordan du arkiverer en salgsordre manuelt. Fremgangsmåden er den samme for alle ordrer, rammeordrer, returvareordrer og tilbud.

1. Vælg ![Lightbulb, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **Salgsordrer**, og vælg derefter det relaterede link.  
2. Åbn en salgsordre, som du vil arkivere.  
3. Vælg handlingen **Arkivér bilag**.

Salgsordren arkiveres. Du kan se den på siden **Arkiverede salgsordrer**.

## <a name="to-restore-a-non-posted-sales-order-from-the-archive"></a>Sådan gendannes en ikke-bogført salgsordre fra arkivet

Følgende procedure beskriver, hvordan du gendanner en arkiveret salgsordre tilbage til den oprindelige salgsordre. Gendannelse af et dokument er kun muligt, når det oprindelige dokument ikke er bogført. Fremgangsmåden er den samme for alle ordrer, rammeordrer, returvareordrer og tilbud.

1. Vælg ![Lightbulb, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **Salgsordrearkiver**, og vælg derefter det relaterede link.
2. Vælg den arkiverede salgsordre eller en version af den, som du vil gendanne, og vælg derefter handlingen **Gendan**.  

Oplysningerne i den oprindelige salgsordre erstattes med oplysningerne fra den valgte arkiverede version.

## <a name="to-delete-archived-sales-orders"></a>Sådan sletter du arkiverede salgsordrer

Brug en opbevaringspolitik til at rydde op i arkiverede dokumenter, som du ikke længere har brug for. Opbevaringspolitikker lader administratorer definere, hvor lang tid de vil gemme data. De kan f.eks. oprette en politik, der sletter data efter en udløbsdato. Du kan finde flere oplysninger i [Definere opbevaringspolitikker](admin-data-retention-policies.md).

Der er et par ting, du skal være opmærksom på, når du opretter opbevaringspolitikker for arkiverede dokumenter:

* *Hvis det oprindelige dokument ikke er slettet, sletter Business Central ikke arkiverede versioner. Arkiverede versioner udløber ikke, så længe originalen findes.
* Når du konfigurerer opbevaringspolitikken, kan du angive, at politikken skal slette alle arkiverede versioner af et dokument, undtagen den seneste. Du kan f.eks. have ti versioner af et dokument og vil beholde en kopi af den seneste. 
* Business Central beregner udløbsdatoen for dokumenter baseret på datoen for den senest arkiverede version.

## <a name="see-also"></a>Se også

[Spore bilagslinjer](across-how-to-track-document-lines.md)  
[Salg](sales-manage-sales.md)  
[Generelle forretningsfunktioner](ui-across-business-areas.md)  
[Arbejd med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)

[!INCLUDE[footer-include](includes/footer-banner.md)]
