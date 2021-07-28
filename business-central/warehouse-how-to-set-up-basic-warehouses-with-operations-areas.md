---
title: Oprette grundlæggende lagersteder med handlingsområder
description: Definere lageroperationsområder og bruge lagerbevægelser, pluk og læg-på-lager-aktiviteter til at flytte varer mellem dem.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 06/25/2021
ms.author: edupont
ms.openlocfilehash: 35482dca465da05be01c4eed86e93d30a75e6dcf
ms.sourcegitcommit: a7cb0be8eae6ece95f5259d7de7a48b385c9cfeb
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 07/08/2021
ms.locfileid: "6441393"
---
# <a name="set-up-basic-warehouses-with-operations-areas"></a>Oprette grundlæggende lagersteder med handlingsområder
Hvis der findes interne operationsområder, såsom produktion eller montage i grundlæggende lageropsætninger, hvor lokationer bruger opsætningsfeltet **Tvungen placering** og muligvis opsætningsfelterne **Kræv pluk** og **Kræv læg-på-lager**, kan du derefter bruge følgende grundlæggende lagerdokumenter til at registrere dine lageraktiviteter for interne operationsområder:  

- Siden **Liste flytning (lager)**.  
- Siden **Plukliste (lager)**.  
- Siden **Læg-på-lager (lager)**.

> [!NOTE]
> Selv om indstillingerne kaldes **Kræv pluk** og **Kræv læg-på-lager**, kan du bogføre modtagelser og leverancer direkte fra kildeforretningsdokumenterne på lokationer, hvor du kan markerer disse afkrydsningsfelter.  

Hvis du vil bruge disse sider med interne operationer, f.eks til at plukke og flytte komponenter til produktion, skal du foretage nogle eller alle følgende konfigurationstrin, afhængigt af hvor meget kontrol du har behov for:  

- Aktivér lagerpluk-, flytte- og læg-på-lager-dokumenter.  
- Definer standardplaceringsstrukturer for komponenter og færdigvarer, der cirkulerer til og fra operationsressourcer.  
- Opret til- og fra-placeringer, der er dedikeret til specifikke operationsressourcer, for at forhindre, at varerne plukkes til udgående dokumenter.

De placeringskoder, der er angivet på lokationskort, definerer en standardlagerstrøm for visse aktiviteter, som komponenter i en montageafdeling. Der findes yderligere funktioner for at sikre, at varer, der placeres i en bestemt placering, ikke kan flyttes eller plukkes til andre aktiviteter. Du kan finde flere oplysninger i [Sådan oprettes dedikerede komponentplaceringer](warehouse-how-to-set-up-basic-warehouses-with-operations-areas.md#to-create-dedicated-component-bins).

Følgende procedurer er baseret på oprettelse af grundlæggende lageraktiviteter omkring et produktionsområde. Trinene er de samme for andre operationsområder, f.eks. montage, servicestyring og sager.  

> [!NOTE]  
>  I følgende procedure er feltet **Tvungen placering** på lokationskort markeret som en forudsætning, fordi dette betragtes som grundlaget for ethvert logistikniveau.  

## <a name="to-enable-inventory-documents-for-internal-operation-activities"></a>Aktivere lagerdokumenter til interne operationsaktiviteter  
1.  Vælg ![Lightbulb, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **Lokationer**, og vælg derefter det relaterede link.
2. Åbn det lokationskort, du vil konfigurere.  
3.  Markér afkrydsningsfeltet **Kræv læg-på-lager** i oversigtspanelet **Lagersted** for at angive, at når der frigives et indgående eller internt kildedokument med en placeringskode, så kan der oprettes et læg-på-lager-dokument eller et flytning (lager)-dokument.  
4.  Markér afkrydsningsfeltet **Kræv pluk** for at angive, at når der oprettes et udgående eller internt kildedokument med en placeringskode, så skal der oprettes et lagerplukdokument eller et flytning (lager)-dokument.  

## <a name="to-define-a-default-bin-structure-in-the-production-area"></a>Definere en standardplaceringsstruktur i produktionsområdet  
1.  Vælg ![Lightbulb, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **Lokationer**, og vælg derefter det relaterede link.
2. Åbn det lokationskort, du vil konfigurere.  
3.  Indtast i feltet **Åben prod.placeringskode** i oversigtspanelet **Placeringer** koden for placeringen i produktionsområdet med masser af komponenter, som maskinoperatøren kan forbruge fra uden at anmode om en lageraktivitet for at bringe dem til placeringen. Varer, der er placeret på denne placering, er normalt angivet til automatisk bogføring eller træk. Dette betyder, at feltet **Trækmetode** indeholder **Forlæns** eller **Baglæns**.  
4. I feltet **Til-produktionsplaceringskode** skal du indtaste koden for den placering i produktionsområdet, hvor de komponenter, der kan plukkes til produktion på lokationen placeres som standard, før de kan forbruges. Varer, der er placeret på denne placering, er normalt angivet til manuel forbrugsbogføring. Dette betyder, at feltet **Trækmetode** indeholder **Manuelt** eller **Pluk + Forlæns** eller **Pluk + Baglæns** for lagerpluk og flytninger (lager).  

    > [!NOTE]  
    >  Når du bruger pluk fra lager definerer feltet **Placeringskode** på en produktionsordrekomponentlinje den *hente*-placering, som komponenter tages fra, når forbruget posteres. Når du bruger lagerbevægelser, definerer feltet **Placeringskode** på produktionsordrekomponentlinjerne den *område*-placering i handlingsområdet, hvor lagermedarbejderen skal placere komponenterne.  

5. Indtast i feltet **Kode for placering til færdigproducerede varer** i oversigtspanelet **Placeringer** koden på den placering i produktionsområde, hvor færdigproducerede tages fra som standard, når processen involverer en lageraktivitet. I grundlæggende lageropsætninger registreres aktiviteten som en læg-på-lager-aktivitet eller en flytning (lager).  

Nu kræver produktionsordrekomponentlinjerne med standardplaceringskoden, at komponenter, der trækkes forlæns, placeres der. Indtil der forbruges komponenter fra placeringen, kan andre komponentbehov plukke eller forbruge fra placeringen, da de stadig betragtes som tilgængelige placeringsindhold. For at sikre at placeringsindholdet kun er tilgængeligt for komponentbehov, der bruger produktionsplacering, skal du vælge feltet **Dedikeret** på linjen for placeringskoden på siden **Placeringer**, der åbnes fra lokationskortet.

Dette flow-diagram viser, hvordan feltet **Placeringskode** i produktionsordrekomponenter udfyldes i henhold til din konfiguration.  

![Placeringsrutediagram.](media/binflow.png "BinFlow")    

## <a name="to-define-a-default-bin-structure-in-the-assembly-area"></a>Definere en standardplaceringsstruktur i montageområdet
Komponenter til montageordrer kan ikke plukkes eller bogføres med pluk. Brug i stedet siden **Flytning (lager)**. Du kan finde flere oplysninger i [Flytte komponenter til et handlingsområde i basislogistik](warehouse-how-to-move-components-to-an-operation-area-in-basic-warehousing.md).

Når du plukker og leverer salgslinjemængder, der er monteret til ordren, skal du følge visse regler, når du opretter lagerpluklinjerne. Du kan finde flere oplysninger i afsnittet "Håndtere montage til ordre-varer i Pluk (lager)" i [Plukke varer med Pluk fra lager](warehouse-how-to-pick-items-with-inventory-picks.md).

Du kan finde flere oplysninger i [Montagestyring](assembly-assemble-items.md).

### <a name="to-set-up-that-an-inventory-movement-is-automatically-created-when-the-inventory-pick-for-the-assembly-item-is-created"></a>Sådan angiver du, at en flytning (lager) automatisk skal oprettes, når lagerpluk for montageelementet oprettes
1. Vælg ![Lightbulb, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, angiv **Montagekonfiguration**, og vælg derefter det relaterede link.
2. Markér afkrydsningsfeltet **Opret bevægelser automatisk**.

### <a name="to-set-up-the-bin-in-the-assembly-area-where-components-are-placed-by-default-before-they-can-be-consumed-in-assembly"></a>Sådan angiver du placeringen i montageområdet, hvor komponenter placeres som standard, før de kan forbruges i montagen
Værdien i dette felt indsættes automatisk i feltet **Placeringskode** på montageordrelinjer, når denne lokation indsættes i feltet **Lokationskode** på montageordrelinjen.

1. Vælg ![Lightbulb, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **Lokationer**, og vælg derefter det relaterede link.
2. Åbn den lokation, du vil konfigurere.
3. Udfyld feltet **Placeringskode til til-montage**.

### <a name="to-set-up-the-bin-in-the-assembly-area-where-finished-assembly-items-are-posted-to-when-they-are-assembled-to-stock"></a>Sådan angiver du den placering i montageområdet, som færdige montageelementer bogføres på, når de monteres til lager
Værdien i dette felt indsættes automatisk i feltet **Placeringskode** på montageordrehoveder, når denne lokationskode indsættes i feltet **Lokationskode** på montageordrehovedet.

De placeringskoder, der er angivet på lokationskort, definerer en standardlagerstrøm for specifikke lageraktiviteter, såsom forbrug af komponenter på et montageområde. Der findes yderligere funktioner for at sikre, at varer, der placeres i en standardplacering, ikke kan flyttes eller plukkes til andre aktiviteter.

> [!NOTE]
> Denne opsætning er kun mulig for lokationer, hvor feltet Tvungen placering er valgt.

1. Vælg ![Lightbulb, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **Lokationer**, og vælg derefter det relaterede link.
2. Åbn den lokation, du vil konfigurere.
3. Udfyld feltet **Placeringskode til fra-montage**.

### <a name="to-set-up-the-bin-where-finished-assembly-items-are-posted-to-when-they-are-assembled-to-a-linked-sales-order"></a>Sådan angives den placering, som færdige montageelementer bogføres på, når de monteres til en tilknyttet salgsordre
Fra denne placering leveres montageelementer med det samme via et lagerpluk for at opfylde salgsordre.

> [!NOTE]
> Feltet kan ikke bruges, hvis lokationen er sat op til at bruge styret pluk og læg-på-lager.

Placeringskoden kopieres fra salgsordrelinjen til montageordrehovedet for at kommunikere til montagearbejdere, hvor outputtet skal placeres, før det leveres. Den kopieres også til lagerpluklinjen for at kommunikere til lagerarbejderne, hvor det skal tages fra til levering.

> [!NOTE]
> Montage efter ordre-leveranceplaceringen er altid tom. Når du bogfører en montage efter ordre-salgslinje, justeres placeringsindholdet først positive med montageoutputtet. Straks derefter justeres det negative med den leverede mængde.

Værdien i dette felt indsættes automatisk i feltet Placeringskode på salgsordrelinjer, der indeholder en mængde i feltet **Mgd. til montage til ordre**, eller hvis varen, der skal sælges, har **Montage efter ordre** i feltet **Genbestillingssystem**.

Hvis **Pla.kode til ordremontagelev.** er tomt, bruges feltet **Placeringskode til fra-montage** i stedet. Hvis begge opsætningsfelter er tomme, bruges den sidst brugte placering med indhold i feltet **Placeringskode** på salgsordrelinjer.

Den samme placeringskode kopieres igen fra feltet **Placeringskode** på lagerpluklinjen, der administrerer leverancen af montage efter ordre-antallet. Du kan finde flere oplysninger i afsnittet "Håndtere montage til ordre-varer i Pluk (lager)" i [Plukke varer med Pluk fra lager](warehouse-how-to-pick-items-with-inventory-picks.md).

1. Vælg ![Lightbulb, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **Lokationer**, og vælg derefter det relaterede link.
2. Åbn den lokation, du vil konfigurere.
3. Udfyld feltet **Pla.kode til ordremontagelev.**.

## <a name="to-create-dedicated-component-bins"></a>Sådan oprettes dedikerede komponentplaceringer
Du kan angive, at antallet i en placering skal beskyttes mod pluk til andre formål end det aktuelle.

Mængderne i dedikerede placeringer kan stadig reserveres. På samme måde medtages mængderne i dedikerede placeringer i feltet **Beholdning i alt** på siden **Reservation**.

F.eks. konfigureres et arbejdscenter med en placeringskode i feltet **Til-produktionsplaceringskode**. Produktionsordrekomponentlinjerne med den placeringskode kræver, at der anbringes komponenter, der trækkes forlæns, der. Indtil der forbruges komponenter fra placeringen, kan andre komponentbehov plukke eller forbruge fra placeringen, da de stadig betragtes som tilgængelige placeringsindhold. For at sikre at placeringsindholdet kun er tilgængeligt for komponentbehov, der bruger produktionsplacering, skal du vælge feltet **Dedikeret** på linjen for placeringskoden på siden **Placeringer**, der åbnes fra lokationskortet.

Hvis du gør en placering dedikeret, giver den samme funktion som brug af placeringstyper, der kun er tilgængeligt i avanceret logistik. Der er flere oplysninger i [Konfigurere placeringer](warehouse-how-to-set-up-bin-types.md).

> [!Caution]
> Varer på dedikerede placeringer er ikke beskyttet, når de plukkes og forbruges som produktionskomponenter på siden Pluk.

1.  Vælg ![Lightbulb, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **Lokationer**, og vælg derefter det relaterede link. Markér den placering, du vil opdatere.  
2.  Vælg handlingen **Placeringer**.  
3.  Markér feltet **Dedikeret** for hver placering, du vil bruge udelukkende til bestemte interne operationer, og som du ønsker at reservere mængder for til den pågældende interne operation, når de er placeret der.  

> [!NOTE]  
>  Placeringen skal være tom, før du kan markere eller fjerne markeringen i feltet **Dedikeret**.

## <a name="see-also"></a>Se også  
[Logistik](warehouse-manage-warehouse.md)  
[Lagerbeholdning](inventory-manage-inventory.md)  
[Sådan konfigureres Warehouse Management](warehouse-setup-warehouse.md)     
[Montagestyring](assembly-assemble-items.md)    
[Designoplysninger: Warehouse Management](design-details-warehouse-management.md)  
[Arbejde med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]