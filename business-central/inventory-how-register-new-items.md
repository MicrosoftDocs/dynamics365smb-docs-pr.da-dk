---
title: Oprette kort for varer eller tjenesteydelser (indeholder video)
description: 'Du kan oprette varekort til de servicer, du sælger som timer og fysiske produkter. Montageelementer og færdigvarer, som du sælger fra lagerbeholdningen.'
author: brentholtorf
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 'item, finished good, component, raw material, assembly item, item substitution'
ms.search.form: '30, 5717, 31, 32, 346, 9091, 5718, 5716, 5720, 1384, 1383, 35, 5404, 1378, 5719'
ms.date: 09/26/2022
ms.author: bholtorf
---
# Registrere nye varer

Varer er, blandt andre produkter, grundlaget for din virksomhed og de varer eller tjenester, som du handler med. Hver vare skal registreres som et varekort.

Varekort indeholder de oplysninger, der kræves for at købe, opbevare, sælge, levere og føre regnskab med varer.

Varekortet kan være af typen **Lager**, **Service** eller **Ikke-lager** for at angive, om varekortet repræsenterer en fysisk lagerenhed, en arbejdstidsenhed eller en fysisk enhed, der ikke spores på lageret. Du kan finde flere oplysninger i [Om varetyper](inventory-about-item-types.md).

En vare kan struktureres som en overordnet vare med underliggende underordnede varer på en stykliste. Få mere at vide om montagestyklister og produktionsstyklister på [arbejde med styklister ](inventory-how-work-BOMs.md).

Hvis du køber den samme vare fra flere forskellige leverandører, kan du forbinde disse leverandører på varekortet. Leverandørerne vises derefter på siden **Vare/leverandører**, så du nemt kan vælge en anden leverandør.

*Katalogvarer*, som du tilbyder til dine kunder, men som du ikke vil administrere i dit system, før du begynder at sælge dem, kan oprettes som katalogvarer. Katalogvarer må ikke forveksles med almindelige varer af typen **Ikke-lager**. Flere oplysninger i [Arbejde med katalogvarer](inventory-how-work-nonstock-items.md).  

> [!NOTE]  
> Hvis der er en vareskabelon til forskellige varetyper, vises der en side, når du opretter et nyt varekort, hvorfra du kan vælge en passende skabelon. Hvis der kun er én vareskabelon, bruger nye varekort altid denne skabelon.

Følgende fremgangsmåde beskriver, hvordan du opretter et varekort fra bunden. Du kan også oprette nye varekort ved at kopiere eksisterende kort. Du kan finde flere oplysninger i [Kopiere eksisterende elementer for at oprette nye varer](inventory-how-copy-items.md).  

<br />

> [!Video https://www.microsoft.com/videoplayer/embed/RE47eLx?rel=0]

## Sådan oprettes et nyt varekort

[!INCLUDE[create_new_item](includes/create_new_item.md)]

> [!NOTE]
> I feltet **Kostmetode** skal du angive, hvordan varens kostpris beregnes på baggrund af antagelser om gennemstrømningen af fysiske varer i virksomheden. Fem kostmetoder er tilgængelige, afhængigt af varetypen. Du kan finde flere oplysninger i [Designoplysninger: Kostmetoder](design-details-costing-methods.md).
>
> Hvis du vælger **Gennemsnit**, beregnes en vares kostpris som den gennemsnitlige kostpris på hvert enkelt tidspunkt efter et køb. Lager værdiansættes ud fra den forudsætning, at alle lagerbeholdninger sælges samtidig. Med denne indstilling kan du vælge feltet **Kostpris** på siden **Oversigt over beregning af gns. kostpris** for at få vist en oversigt over transaktioner, som den gennemsnitlige kostpris beregnes ud fra.

Du kan se eller redigere specialpriser eller rabatter, som du tildeler til varen, eller som din leverandør giver dig, hvis bestemte kriterier opfyldes, f.eks. debitor, mindste ordrestørrelse eller slutdato. Det gør du ved at vælge handlingerne **Angiv særlige priser** eller **Angiv særlig rabat**. Hver række på eksempelvis siden **Salgspriser** repræsenterer en særlig pris. Hver kolonne repræsenterer et kriterium, der skal gælde for at tildele en debitor den specielle pris, som du angiver i feltet **Enhedspris** på siden **Salgspriser**. Du kan finde flere oplysninger i [Registrere salgspris, rabat og betalingsaftaler](sales-how-record-sales-price-discount-payment-agreements.md) eller [Registrere særlige købspriser og rabatter](purchasing-how-record-purchase-price-discount-payment-agreements.md).

Varen er nu registreret, og varekortet er klar til at blive brugt i købs- og salgsdokumenter.

Hvis du vil bruge dette varekort som skabelon, når du opretter nye varekort, kan du gemme det som en skabelon. Du kan finde flere oplysninger i følgende afsnit.  

### Sådan gemmes varekortet som en skabelon

1. På siden **Varekort** skal du vælge handlingen **Gem som skabelon**. Siden **Vareskabelon** åbnes med varekortet som skabelon.
2. Udfyld felterne efter behov. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
3. Hvis du vil genbruge dimensioner i kladder, skal du vælge handlingen **Dimensioner**. Siden **Skabeloner til dimensioner** åbnes med alle dimensionsværdikoder, der er konfigureret for varen.
4. Rediger eller angiv dimensionskoder, der skal gælde for nye debitorkort, oprettes ved hjælp af skabelonen.
5. Når du har fuldført skabelonen for den nye vare, skal du vælge knappen **OK**.

Vareskabelonen føjes til listen over vareskabeloner, så du kan bruge den til at oprette nye varekort.

### Varer, der bruges i produktionsordrer

Hvis du vil registrere varer, der derefter bruges i produktionsordrer, skal du angive genbestillingssystemet som *Prod.ordre* i oversigtspanelet **Genbestilling**. Du kan finde flere oplysninger i [Om produktionsordrer](production-about-production-orders.md).  

## Sådan oprettes flere leverandører af en vare

Hvis du køber den samme vare fra flere forskellige leverandører, skal du angive oplysninger om hver vareleverandør, f.eks. priser, leveringstid og rabatter.  

1. Vælg ![Lightbulb, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **Varer**, og vælg derefter det relaterede link.  
2. Markér den relevante vare, og vælg derefter handlingen **Rediger**.  
3. Vælg handlingen **Leverandører**.  
4. Vælg feltet **Kreditornr.**, og vælg derefter den kreditor, du vil konfigurere for varen.  
5. Det er valgfrit, om du vil udfylde de resterende felterne.  
6. Gentag trin 2 til 5 for hver leverandør, du ønsker at købe varen fra.

Leverandørerne vises nu på siden **Vare/leverandører**, som du åbner fra varekortet, så du nemt kan vælge en anden leverandør.

## Konfigurere erstatningsvarer

Du kan definere, at varer skal have erstatningsvarer, f. eks. andre varer, der kan bruges i stedet for den oprindelige vare.

### Sådan gør du en vare en erstatning

1. Vælg ![Lightbulb, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **Varer**, og vælg derefter det relaterede link.  
2. Find den relevante vare, og vælg derefter på **Varenr.** for at åbne varekortet.  
3. Vælg den **relaterede** handling, vælg **vare**, og klik derefter på **erstatninger** for at åbne siden **Erstatningsvarepost** .  
4. Vælg feltet **Erstatningsnr.** feltet , og vælg derefter erstatningsvaren på listen.
5. Udfylde eller ændre felterne på siden efter behov.

Når antallet af efterspurgte varer overstiger den mængde, der er tilgængelig på lageret, og der vises en meddelelse til at oplyse, at erstatningsvarer findes.

> [!NOTE]  
> Vær opmærksom på, at erstatningsvarer ikke automatisk medfører, at en vare erstattes af en anden vare, f. eks. når der oprettes en salgsordre eller en stykliste. I stedet bliver du advaret om, at der er en erstatningsvare tilgængelig.

## Kategorier, attributter og varianter

[!INCLUDE[inventory_variant](includes/inventory_variant.md)]

Få mere at vide om varianter på [Administrer produktvarianter](inventory-item-variants.md).  

## Sletning af varekort

Hvis du har bogført en postering for en vare, kan du ikke slette kortet, da posterne muligvis er nødvendige med henblik på værdiansættelse eller revision af lageret. Hvis du vil slette varekort med poster, skal du kontakte Microsoft-partneren for at gøre dette via kode.  

## Administration af lager på lagersteder

Når du registrerer en ny vare, kan du se de felter, der er relateret til lagerstedsstyringen, især i oversigtspanelet **Lagersted**. Hvis organisationen ikke bruger warehouse management capabilities i [!INCLUDE [prod_short](includes/prod_short.md)], kan du ignorere disse felter.  

Hvis organisationen på et senere tidspunkt opsætter logistik, anbefales det, at du sikrer dig, at hver eksisterende vare har de rette oplysninger i de forskellige felter. På den måde kan lagerprocesserne køre som forventet. Oplysningerne kan omfatte felter som **Lagerklassekode** eller **Læg på lager-skabelonkode**. Der er flere oplysninger under [Konfigurere lokalitetsstyring](warehouse-setup-warehouse.md).  

## Skabelon

Når din virksomhed bruger forsynings planlægnings processerne i [!INCLUDE [prod_short](includes/prod_short.md)], skal du udfylde de relevante felter i oversigtspanelet **Planlægning** . Du kan finde en introduktion til planlægnings området i [design oplysninger: centrale begreber i planlægningssystemet](design-details-central-concepts-of-the-planning-system.md).  

Du kan finde eksempler på, hvordan du kan bruge felterne i oversigtspanelet **Planlægning**, under [konfigurere bedste fremgangsmåder: planlægningsparametre](setup-best-practices-planning-parameters.md).  

## Se relateret [Microsoft-træning](/training/modules/create-items/)

## Se også

[Lagerbeholdning](inventory-manage-inventory.md)  
[Oprette måleenheder](inventory-how-setup-units-of-measure.md)  
[Administrere produktvarianter](inventory-item-variants.md)  
[Oprette Intrastat-rapportering](finance-how-setup-report-intrastat.md#other-intrastat-configurations)  
[Afstemme lageromkostninger med finansregnskabet](finance-how-to-post-inventory-costs-to-the-general-ledger.md)  
[Oprette nummerserie](ui-create-number-series.md)  
[Konfigurere bogføringsgrupper](finance-posting-groups.md)  
[Køb](purchasing-manage-purchasing.md)  
[Salg](sales-manage-sales.md)  
[Om planlægningsfunktionen](production-about-planning-functionality.md)  
[Oprette bedste fremgangsmåder: Planlægningsparametre](setup-best-practices-planning-parameters.md)  
[Konfigurere bedste fremgangsmåder: Forsyningsplanlægning](setup-best-practices-supply-planning.md)  
[Designoplysninger: Centrale begreber i planlægningssystemet](design-details-central-concepts-of-the-planning-system.md)  
[Designoplysninger: Afstemning mellem behov og forsyning](design-details-balancing-demand-and-supply.md)  
[Designoplysninger: Planlægningsparametre](design-details-planning-parameters.md)  
[Arbejd med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
