---
title: VIA-metoder til beregning og registrering af projektets fremdrift
description: 'Beskriver de forskellige metoder for igangværende arbejde, du kan bruge til at bogføre, overvåge og beregne finansielle oplysninger for igangværende projekter.'
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bholtorf
ms.topic: conceptual
ms.search.keywords: 'work in process, work in progress, calculate project WIP'
ms.search.form: '1010,'
ms.date: 08/19/2024
ms.service: dynamics-365-business-central
ms.custom: bap-template
---
# Forståelse af VIA-metoder i projektledelse

Efterhånden som status for et projekt ændrer sig, forbruges der materialer, ressourcer og andre udgifter, og disse skal bogføres i projektet. Igangværende arbejde er en funktion, som giver dig mulighed for at estimere den økonomiske værdi af projekter i finansregnskabet under udførelsen af projektet. Du kan i mange tilfælde bogføre udgifterne for et projekt, før projektet faktureres. Når der kun bogføres udgifter, er din regnskabsopgørelse ikke korrekt.

Du kan beregne VIA og bogføre værdien i finansregnskabet for at spore værdien i finansregnskabet. Du kan finde flere oplysninger i [Overvåge projektstatus og -udførelse](projects-how-monitor-progress-performance.md).

Ud af kassen [!INCLUDE[prod_short](includes/prod_short.md)]  understøtter følgende metoder til beregning og registrering af værdien af igangværende arbejde.

| Metode til igangværende arbejde | Beskrivelse | Realiserede omkostninger | Realiseret salg |
| --- | ------- |--- | --- |
| Kostværdi |Registrerer omkostning, når debitoren faktureres. Registrerer salg baseret på det fakturerede salg. |Kostværdi|Kontrakt (fakturapris)|
| Salgsomkostning |Registrerer omkostning, når debitoren faktureres. Registrerer salg baseret på det fakturerede salg.|Salgsomkostning|Kontrakt (faktureret salgsbeløb)|
| Salgsværdi |Registrerer omkostninger, efterhånden som de rapporteres. Registrerer salg proportionalt med de rapporterede omkostninger.|Forbrug (kostbeløb)|Salgsværdi|
| Færdiggørelsesgrad |Registrerer omkostninger, efterhånden som de rapporteres. Registrerer salg proportionalt med de rapporterede omkostninger.|Forbrug (kostbeløb)|Færdiggørelsesgrad|
| Afsluttet kontrakt |Intet salg eller omkostninger indgår i VIA-beregningen. Afsluttet kontrakt registrerer ikke indtægter og omkostninger, før projektet er afsluttet. Denne indstilling er f.eks. nyttig, når der er stor usikkerhed omkring estimaterne for projektets omkostninger og indtægter.|Ved færdiggørelse|Ved færdiggørelse|

De nøjagtige formler og finanstransaktioner defineres ved udvælgelsen i felterne [**Registreret kostpris**](#recognized-cost) og [**Realiseret salg**](#recognized-sales) .

## Oprette en projektmetode for igangværende arbejde

Opret et projekt med igangværende arbejde-metode, der afspejler behovet i organisationen og angiver det som standard.  

> [!NOTE]
> Når du har brugt en metode til at oprette VIA-poster, kan du ikke ændre eller slette metoden.  

1. Vælg det ![lyspæreikon, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") Ikon, angiv **VIA-metoder** i Project, og vælg derefter den relaterede sammenkæde.  
2. Vælg handlingen **Ny**, vælg de relevante værdier for felterne **Registreret omkostning** og **Registreret salg**, og udfyld derefter de andre felter efter behov. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]  
3. Luk siden.
4. Hvis du vil gøre denne metode til standard, skal du vælge den ![pære, der åbner funktionen Fortæl mig det.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") , angiv **Opsætning af projekter**, og vælg derefter den relaterede sammenkæde.  
5. I feltet **Standard-VIA-metode** skal du vælge metoden fra listen.

### Registreret omkostning

| Registreret omkostning | Formel til beregning af realiseret kostpris | Finansposter |
| --- | --- | ---------- |
|Ved færdiggørelse|0 (nul)|Konto **til realiserede DT-omkostninger** Cr **konto til VIA-omkostninger** </br>Beløb: Realiseret omkostning </br></br>Dt **VIA-omkostningskonto** Konto til **projektomkostninger** </br>Beløb: MAX[Realiseret omkostning; Faktisk (kostbeløb)]|
|Salgsomkostning|Faktisk (kostbeløb) - Budget (kostbeløb) x faktureringspct., hvor:</br></br> Faktureringspct. = Faktureret (salgsbeløb) / Fakturerbar (salgsbeløb)</br></br>**Bemærk:**  Denne beregning kræver, at Fakturerbar (Salgsbeløb) og Budget (Kostbeløb) er angivet korrekt for hele projektet.|Konto **til realiserede DT-omkostninger** Cr **konto til VIA-omkostninger** </br>Beløb: Realiseret omkostning </br></br>Dt **VIA-omkostningskonto** Konto til **projektomkostninger** </br>Beløb: MAX[Realiseret omkostning; Faktisk (kostbeløb)] </br></br>Konto **til justering af DT-projektomkostninger Konto**  **til justering af VIA-omkostninger** </br>Beløb: Realiserede omkostninger – Faktisk (kostbeløb), Hvis realiseretOmkostning > Faktisk (kostbeløb)|
|Kostværdi|Faktisk (kostbeløb) – [Færdiggørelse% – Faktureret%] * Fakturerbar (samlet pris) * BudgetCostPriceRatio, hvor: </br></br> BudgetCostPriceRatio = Budget(Kostbeløb) / Budget (Salgsbeløb)</br>Faktureringspct. = Faktureret (salgsbeløb) / Fakturerbar (salgsbeløb)</br>Færdiggørelsesgrad = Faktisk (kostbeløb)/budget (kostbeløb)</br></br>**Bemærk:**  Denne beregning kræver, at Fakturerbar (Salgsbeløb), Budget (Salgsbeløb) og Budget (Kostbeløb) angives korrekt for hele projektet.|Konto **til realiserede DT-omkostninger** Cr **konto til VIA-omkostninger** </br>Beløb: Realiseret omkostning</br></br>Dt **VIA-omkostningskonto** Konto til **projektomkostninger** </br>Beløb: MAX[Realiseret omkostning; Faktisk (kostbeløb)] </br></br>Konto **til justering af DT-projektomkostninger Konto**  **til justering af VIA-omkostninger** </br>Beløb: Realiserede omkostninger – Faktisk (kostbeløb), Hvis realiseretOmkostning > Faktisk (kostbeløb)|
|Kontrakt (faktureret omkostning)|Faktureret (kostbeløb i alt) |Konto **til realiserede DT-omkostninger** Cr **konto til VIA-omkostninger** </br>Beløb: Realiseret omkostning </br></br> Dt **VIA-omkostningskonto** Konto til **projektomkostninger** </br>Beløb: MAX[Realiseret omkostning; Faktisk (kostbeløb)] </br></br>Konto **til justering af DT-projektomkostninger Konto**  **til justering af VIA-omkostninger** </br>Beløb: Realiserede omkostninger – Faktisk (kostbeløb), Hvis realiseretOmkostning > Faktisk (kostbeløb)|
|Forbrug (kostbeløb)|Faktisk (samlet omkostning) |Konto **til realiserede DT-omkostninger** Cr **konto til VIA-omkostninger** </br>Beløb: Realiseret omkostning </br></br>Dt **VIA-omkostningskonto** Konto til **projektomkostninger** </br>Beløb: MAX[Realiseret omkostning; Faktisk (kostbeløb)]|

Når projektets status ændres til Fuldført, tilbagefører opgaven Beregn VIA **VIA-transaktionen** og bogføres i stedet.

Konto **til realiserede omkostninger** Konto **til projektomkostninger**, Beløb: **Faktisk (kostbeløb)**

> [!NOTE]
> Afhængigt af valget i **feltet Anvendt** VIA-bogføringsmetode kan Varekostpris-anvendt konto **,** Ressourceomkostningsudlignet **konto** eller **Finansomkostningsanvendt konto** bruges i stedet for **Projektomkostningsanvendt konto**. Du kan finde flere oplysninger i [Projektbogføringsgrupper](projects-how-setup-jobs.md#to-set-general-information-for-projects).

### Registreret salg

| Realiseret salg | Formel til beregning af realiseret salg | Finansposter |
| --- | --- | ---------- |
|Ved færdiggørelse|0 (nul)|Dt **VIA-faktureret salgskonto** Konto **til realiseret salg** </br>Beløb: Realiseret salg</br></br>Dt **Projektsalg anvendt konto** Cr **VIA faktureret salgskonto** </br>Beløb: Faktureret (salgsbeløb)|
|Kontrakt (faktureret salgsbeløb)|Faktureret (samlet pris)|Dt **VIA-faktureret salgskonto** Konto **til realiseret salg** </br>Beløb: Realiseret salg</br></br>Dt **Projektsalg anvendt konto** Cr **VIA faktureret salgskonto** </br>Beløb: Faktureret (salgsbeløb)|
|Forbrug (kostbeløb)|Faktisk (samlet omkostning)|Dt **VIA-faktureret salgskonto** Konto **til realiseret salg** </br>Beløb: Realiseret salg</br></br>Dt **Projektsalg anvendt konto** Cr **VIA faktureret salgskonto** </br>Beløb: Faktureret (salgsbeløb)
|Færdiggørelsesgrad|MIN[Fakturerbar (samlet pris) x færdiggørelsesgrad Fakturerbar (samlet pris)], hvor:</br></br>Færdiggørelsesgrad = Faktisk (kostbeløb)/budget (kostbeløb)</br></br>**Bemærk:**  Denne beregning kræver, at Fakturerbar (Salgsbeløb) og Budget (Kostbeløb) er angivet korrekt for hele projektet.|Dt **VIA-konto for periodisk salg** Konto **til registreret salg** </br>Beløb: Realiseret salg</br></br>Dt **Projektsalg anvendt konto** Cr **VIA faktureret salgskonto** </br>Beløb: Faktureret (salgsbeløb)|
|Forbrug (salgsbeløb)|Faktisk (samlet pris)|Dt **VIA-faktureret salgskonto** Konto **til realiseret salg** </br>Beløb: Realiseret salg </br></br>Dt **Projektsalg anvendt konto** Cr **VIA faktureret salgskonto** </br>Beløb: MAX[RecognizedSales; Faktureret (salgsbeløb)]</br></br>Dt **VIA-konto for periodisk salg** Cr-projektsalgsjusteringskonto **·** </br>Beløb: MAX[RecognizedSales; Faktureret (salgsbeløb)] – Faktureret (salgsbeløb)|
|Salgsværdi| Faktisk (salgsbeløb) x Fakturerbar (salgsbeløb)/budget (salgsbeløb)</br></br>**Bemærk:**  Denne beregning kræver, at Fakturerbar (Salgsbeløb) og Budget (Salgsbeløb) er angivet korrekt for hele projektet.|Dt **VIA-faktureret salgskonto** Konto **til realiseret salg** </br>Beløb: Realiseret salg</br></br>Dt **Projektsalg anvendt konto** Cr **VIA faktureret salgskonto** </br>Beløb: MAX[RecognizedSales; Faktureret (salgsbeløb)]</br></br>Dt **VIA-konto for periodisk salg** Cr-projektsalgsjusteringskonto **·** </br>Beløb: MAX[RecognizedSales; Faktureret (salgsbeløb)] – Faktureret (salgsbeløb)|

Når projektets status ændres til Afsluttet, tilbagefører opgaven Beregn VIA **VIA-transaktionen** og bogføres i stedet.

Dt **projektsalg anvendt konto** Cr **Realiseret salgskonto**, Beløb: **Faktureret (samlet pris)**

## Se også

[Projektstyring](projects-manage-projects.md)  
[Finans](finance.md)  
[Køb](purchasing-manage-purchasing.md)  
[Salg](sales-manage-sales.md)  
[Arbejd med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
