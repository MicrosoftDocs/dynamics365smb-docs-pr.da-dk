---
title: Om planlægningsfunktioner | Microsoft Docs
description: Planlægningssystemet tager højde for alle oplysninger om efterspørgsel og udbud, tæller resultaterne sammen og opretter forslag til, hvordan udbuddet kan afstemmes, så det passer til efterspørgslen.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 07/14/2020
ms.author: edupont
ms.openlocfilehash: 541d3842977e7b139877d9a26fcc39b448ef9745
ms.sourcegitcommit: a80afd4e5075018716efad76d82a54e158f1392d
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 09/09/2020
ms.locfileid: "3786967"
---
# <a name="about-planning-functionality"></a>Om planlægningsfunktionen

Planlægningssystemet tager højde for alle oplysninger om efterspørgsel og udbud, tæller resultaterne sammen og opretter forslag til, hvordan udbuddet kan afstemmes, så det passer til efterspørgslen.  

Du kan finde detaljerede oplysninger i [Designoplysninger: Forsyningsplanlægning](design-details-supply-planning.md)  

> [!NOTE]  
> Læs værktøjstippet for alle felter, der er nævnt i dette emne, for at forstå deres funktion. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

## <a name="demand-and-supply"></a>Behov og forsyning

I planlægningen indgår to elementer, udbud og efterspørgsel, som her kaldes behov og forsyning. Der skal opretholdes en balance mellem disse to elementer, så det kan sikres, at behovet imødekommes rettidigt og på en økonomisk fornuftig måde.  

- Behov er fællesbetegnelsen for enhver form for bruttobehov, såsom en salgsordre, serviceordre, komponentbehov fra montage eller produktionsordrer, udgående overflytning, rammeordre eller forecast. Herudover kan programmet håndtere andre tekniske behovstyper - som en negativ produktions- eller købsordre, negativ lagerbeholdning og købsreturvarer.  
- Forsyning er fællesbetegnelsen for enhver form for genanskaffelse som lagerbeholdning, en købsordre, montage eller produktionsordre eller indgående overflytning. Tilsvarende kan der være en negativ salgs- eller serviceordre, et negativt komponentbehov eller salgsreturvarer – som alle på en eller anden måde repræsenterer forsyning.  

Et andet formål med planlægningssystemet er at sikre, at lagerbeholdningen ikke vokser unødvendigt. Hvis behovet falder, kan planlægningssystemet foreslå, at du udskyder eksisterende genbestillingsordrer, angiver mindre antal til dem eller helt annullerer dem.  

## <a name="planning-calculation"></a>Planlægningsberegning

Udgangspunktet for planlægningssystemet er forventet og faktisk efterspørgsel fra kunderne, dvs. kundebehov og forskellige faktorer i forbindelse med genbestilling af varer til lageret. Når planlægningsberegningen køres, foreslås det (i form af aktionsmeddelelser), at der tages bestemte forholdsregler, som f.eks. kan være genbestilling fra leverandører, overflytninger mellem lagersteder eller produktion. Hvis der allerede findes genbestillingsordrer, kan den foreslåede aktivitet f.eks. være at øge eller fremskynde ordrerne for på den måde at imødekomme det ændrede behov.  

Udgangspunktet for selve planlægningen er beregningen fra brutto til netto. Et nettobehov udløser frigivelse af planlagte ordrer, som planlægges på basis af ruteoplysningerne (producerede varer) eller på basis af fremskaffelsestiden på varekortet (købte varer). De antal, der frigives i en planlagt ordre, afhænger af planlægningsberegningen og påvirkes af de parametre, der er angivet på de enkelte varekort.  

## <a name="planning-with-manual-transfer-orders"></a>Planlægge med manuelle overflytningsordrer

Som det fremgår af feltet **Genbestillingssystem** på et lagerkort, kan planlægningssystemet indstilles til at oprette overflytningsordrer, der udjævner udbud og efterspørgsel på tværs af lokationer.  

Ud over disse automatiske overflytningsordrer kan du undertiden have brug for at udføre en almindelig flytning af lagerbeholdning til en anden lokation, uanset det nuværende behov. Til det formål skal du manuelt oprette en overflytningsordre på det antal, der skal flyttes. For at sikre, at planlægningssystemet ikke forsøger at justere den manuelle overflytningsordre, skal du indstille **Planlægningsfleksibilitet** på overflytningslinjerne til Ingen.  

Hvis du derimod ønsker, at planlægningssystemet justerer overflytningsordrens antal og datoer i forhold til det nuværende behov, skal du indstille feltet **Planlægningsfleksibilitet** til standardværdien, Ubegrænset.

## <a name="planning-parameters"></a>Planlægningsparametre

Planlægningsparametrene bestemmer, hvornår, hvor meget og hvordan der genbestilles på basis af de forskellige indstillinger på varekortet (eller lagervare) og produktionsopsætningen.  

Der findes følgende planlægningsparametrene på vare- eller lagerkortet:  

- Bufferperiode  
- Buffermængde  
- Genbestillingsmetode  
- Genbestillingspunkt
- Maks. lagerbeholdning  
- Overløbsniveau  
- Interval  
- Akkumuleringsperiode for lot  
- Ændringsperiode  
- Ordrekvantum  
- Sikkerhedstid  
- Sikkerhedslager  
- Montagepolitik  
- Produktionsmetode  

Der findes følgende ordremodifikatorer på vare- eller lagerkortet:  

- Min. ordrestørrelse  
- Maks. ordrestørrelse  
- Oprundingsfaktor  

Globale planlægningsopsætningsfelter på siden **Produktionsopsætning** omfatter:  

- Dynamisk laveste-niveau-kode  
- Aktuel behovsprognose  
- Forecast på lokationer  
- Standardsikkerhedstid  
- Tomt overløbsniveau  
- Komb. hovedplan-/MRP-beregning
- Komponenter på lokation  
- Standardbufferperiode  
- Standardbufferantal  

Du kan finde flere oplysninger i [Designoplysninger: planlægningsparametre](design-details-planning-parameters.md)  

## <a name="other-important-planning-fields"></a>Andre vigtige felter til planlægning

### <a name="planning-flexibility"></a>Planlægningsfleksibilitet

I de fleste forsyningsordrer, f.eks. produktionsordrer, kan du vælge **Ubegrænset** eller **Ingen** i feltet **Planlægningsfleksibilitet** på linjerne.

Det angiver, om der tages højde for forsyningen repræsenteret af produktionsordrelinjen i planlægningssystemet, når der beregnes aktionsmeddelelser.
Hvis feltet viser indstillingen **Ubegrænset**, medtager planlægningssystemet linjen, når aktionsmeddelelsen beregnes. Hvis feltet indeholder indstillingen **Ingen**, er linjen fast og kan ikke ændres, og linjen medtages ikke i beregningen af aktionsmeddelelser.

### <a name="warning"></a>Advarsel

Oplysningsfeltet **Advarsel** på siden **Planlægningskladde** viser eventuelle planlægningslinjer, der er oprettet til en usædvanlig situation med en tekst, som brugeren kan vælge for at få yderligere oplysninger. Der findes følgende advarselstyper:

- Nødsituation
- Undtagelse
- Bemærk!
- Nødsituation

Denne advarsel vises i to tilfælde:

- Når lageret er negativt på den planlagte startdato.
- Når der er antedaterede udbuds- eller efterspørgselshændelser.

Hvis varens lager er negativt på den planlagte startdato, foreslår planlægningssystemet en nødforsyningsordre for den negative mængde, som skal ankomme på den planlagte startdato. Advarslen angiver startdatoen og mængden for nødordren.

Evt. dokumentlinjer med forfaldsdatoer før den planlagte startdato konsolideres i én nødforsyningsordre, så varen kan ankomme på den planlagte startdato.

### <a name="exception"></a>Undtagelse

Advarslen om undtagelsen vises, hvis det forventede disponible lager kommer under sikkerhedslageret.

Planlægningssystemet foreslår en forsyningsordre, der skal opfylde behovet på forfaldsdatoen. Advarslen angiver varemængden på sikkerhedslageret og den dato, hvor den overtrædes.

Overskridelse af niveauet for sikkerhedslageret anses for at være en undtagelse, fordi det ikke bør forekomme, hvis genbestillingspunktet er angivet korrekt.

> [!NOTE]
> Efterspørgsel på planlægningslinjer med undtagelsesadvarsler modificeres normalt ikke i henhold til planlægningsparametre. Planlægningssystemet foreslår i stedet for kun en forsyning til at dække det nøjagtige behovsantal. Du kan dog konfigurere planlægningskørslen til at overholde bestemte planlægningsparametre for planlægningslinjer med visse advarsler. Du kan finde flere oplysninger i beskrivelsen af feltet **Respekter advarsler om undtagelser for planlægningsparametre** i artiklen [Kør fuld planlægning, MPS eller MRP](production-how-to-run-mps-and-mrp.md).

### <a name="attention"></a>Bemærk

Denne advarsel vises i to tilfælde:

- Når den planlagte startdato ligger før arbejdsdatoen.
- Når planlægningslinjen foreslår at ændre en frigivet købs- eller produktionsordre.

> [!NOTE]
> På planlægningslinjer med advarsler er feltet **Accepter aktionsmeddelelse** ikke markeret, fordi planlæggeren forventes at undersøge disse linjer nærmere, før planen udføres.

## <a name="planning-worksheets-and-requisition-worksheets"></a>Planlægningskladder og indkøbskladder

Som beskrevet under [Planlægning](production-planning.md) kan du vælge mellem to kladder til de fleste planlægningsaktiviteter, planlægningskladden og indkøbskladden. De fleste processer beskrives på basis af planlægningskladden, men der er et par scenarier, hvor indkøbskladden foretrækkes.

### <a name="requisition-worksheet"></a>Indkøbskladde

Siden **Indkøbskladde** viser de varer, du vil bestille. Du kan indsætte varer i kladden på følgende måder:

- Indsæt varerne manuelt i kladden, og udfyld de relevante felter.

- Brug kørslen **Beregn plan**. Herved opstilles en genbestillingsplan for varer og enheder, der er oprettet med et genbestillingssystem, der er sat til **Køb** eller **Overførsel**. Når du udfører denne kørsel, udfyldes feltet **Aktionsmeddelelse** automatisk med en foreslået handling, som du kan udføre for at genbestille varen. Det kan f.eks. være at øge vareantallet på en eksisterende ordre eller oprette en ny ordre.

- Hvis du har brugt kørslen **Beregn plan** fra siden **Planlægningskladde** til at opstille en genbestillingsplan, kan du bruge kørslen **Udfør aktionsmeddelelse** til at kopiere forslag til købs- og overflytningsordrer fra planlægningskladden til indkøbskladden. Dette er praktisk, hvis forskellige brugere er ansvarlige for at håndtere produktionsordrer og købs- eller overflytningsordrer.

- Du kan bruge handlingen **Direkte levering** til at udfylde linjerne i indkøbskladden. Denne handling bruger kørslen **Hent salgsordrer** til at finde de salgsordrelinjer, som du vil ekspedere i en direkte levering.

- Du kan bruge handlingen **Specialordre** til at udfylde linjerne i indkøbskladden. Denne handling bruger kørslen **Hent salgsordrer** til at finde de salgsordrelinjer, som du vil ekspedere i en specialordre.

Linjerne i indkøbskladden indeholder detaljerede oplysninger om de varer, der skal genbestilles. Du kan redigere og slette linjerne for at regulere genbestillingsplanen, og du kan viderebehandle linjerne ved hjælp af kørslen **Udfør aktionsmeddelelse**.

Du kan finde flere oplysninger om planlægning med lokationer og overflytninger under [Planlægning med eller uden lokationer](production-planning-with-without-locations.md).

## <a name="see-also"></a>Se også

[Designoplysninger: Forsyningsplanlægning](design-details-supply-planning.md)  
[Skabelon](production-planning.md)  
[Konfigurere produktion](production-configure-production-processes.md)  
[Produktion](production-manage-manufacturing.md)  
[Lagerbeholdning](inventory-manage-inventory.md)  
[Køb](purchasing-manage-purchasing.md)  
[Konfigurere bedste fremgangsmåder: Forsyningsplanlægning](setup-best-practices-supply-planning.md)  
[Arbejde med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)
