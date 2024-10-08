---
title: Fejlfinding og rettelse af dimensioner
description: 'Få mere at vide om, hvordan du foretager fejlfinding af typiske dimensions fejl, og hvordan du retter dimensioner, efter at de er brugt i bogførte transaktioner.'
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bholtorf
ms.topic: conceptual
ms.search.keywords: 'dimension, correction, correct, business intelligence'
ms.search.form: '116, 540, 2588'
ms.date: 08/08/2024
ms.service: dynamics-365-business-central
ms.custom: bap-template
---

# <a name="troubleshoot-and-correct-dimensions"></a>Fejlfinding og rettelse af dimensioner

Regnskabsrapporter og analysevisninger er ofte afhængige af data fra dimensioner. Uanset hvilke sikkerhedsforanstaltninger der er til rådighed, opstår der nogle gange en fejl, som kan medføre unøjagtigheder. I denne artikel beskrives nogle af de typiske fejl, og det forklares, hvordan du retter dimensions tildelinger i bogførte transaktioner, så regnskabsrapporter er nøjagtige.

## <a name="troubleshooting-dimensions-errors"></a>Fejlfinding af dimensionsfejl

Når du bogfører dokumenter eller kladdelinjer, der indeholder dimensioner, kan der opstå forskellige fejl. De er dog typisk relateret til en forkert opsætning eller tildeling af dimensioner.

> [!NOTE]
> På følgende liste over mulige fejlmeddelelser er *%X*-koder pladsholdere for de datavariabler, som findes i den aktuelle meddelelse i brugergrænsefladen afhængig af konteksten. *%1 %2 er f.eks. spærret.* Kan vises i brugergrænsefladen som "Dimensionskode AREA er spærret.".  

|Udsted|Fejlmeddelelse|Mulig løsning|
|-----|-------------|-----------------|
|Spærret dimension|%1 %2 er spærret.|-Find ikke-bogførte bilag, der indeholder dimensionsgruppen med den dimension, der er spærret, og fjern spærringen.<br />– Fjern dimensionsgruppelinjen for den dimension, der er spærret.|
|Slettet dimension|%1 %2 blev ikke fundet.|– Gendan den manglende dimension.<br />-Find ikke-bogførte bilag, der indeholder dimensionsgruppen med den manglende dimension, og tilføj den.<br />– Fjern dimensionsgruppelinjen for den manglende dimension.|
|Spærret dimensionsværdi|%1 %2 - %3 er spærret.|-Find ikke-bogførte bilag, der indeholder dimensionsgruppen med den dimensionsværdi, der er spærret, og fjern spærringen.<br />– Fjern dimensionsgruppelinjen for den dimensionsværdi, der er spærret.|
|Slettet dimensionsværdi|    %1 for %2 mangler.|– Gendan den manglende dimensionsværdi.<br />-Find ikke-bogførte bilag, der indeholder dimensionsgruppen med den manglende dimensionsværdi, og tilføj den.<br />– Fjern dimensionsgruppelinjen for den manglende dimensionsværdi.|
|Forbudt dimensionsværdi|Dimensionsværditypen for %1 %2 - %3 må ikke være %4.|– Ret feltet **Dimensionsværditype** på siden **Dimensionsværdier** til **Standard** eller **Fra-sum**.<br />– Fjern dimensionsgruppelinjen for den dimensionsværdi, der er spærret.|
|Spærret dimensionskombination|Dimensionerne %1 og %2 kan ikke bruges samtidig.|-Find ikke-bogførte bilag, der indeholder dimensionsgruppen med den dimensionskombination, der er spærret, og fjern spærringen.<br />-Ret en af de modstridende linjer i rettighedssæt for dimensionskombinationen.|
|Spærret dimensionsværdikombination|Dimensionskombinationerne %1 - %2 og %3 - %4 kan ikke bruges samtidig.|-Find ikke-bogførte bilag, der indeholder dimensionsgruppen med den dimensionsværdikombination, der er spærret, og fjern spærringen.<br />-Ret en af de modstridende linjer i rettighedssæt for dimensionsværdikombinationen.|
|Tom dimensionsværdikode for standarddimensionen hvor feltet **Værdibogføring** indeholder **Tvungen kode**|– Angiv %1 for %2 %3.<br />– Vælg %1 til %2 %3 for %4 %5.|– Ret feltet **Værdibogføring** på siden **Standarddimension**.<br />-Angiv en ikke-tom dimensionsværdi for den modstridende dimension i dimensionsgruppen.|
|Forkert dimensionsværdikode for standarddimensionen hvor feltet **Værdibogføring** indeholder **Samme kode**|– Vælg %1 %2 til %3 %4.<br />– Vælg %1 %2 til %3 %4 for %5 %6|– Ret feltet **Værdibogføring** på siden **Standarddimension**.<br />– Angiv den krævede dimensionsværdi for den modstridende dimension i dimensionsgruppen.|
|Ikke-tom dimensionsværdikode for tom standarddimension hvor feltet **Værdibogføring** indeholder **Samme kode**|– %1 %2 skal være tom.<br />– %1 %2 skal være tom for %3 %4.|– Ret feltet **Værdibogføring** på siden **Standarddimension**.<br />– Angiv en tom dimensionsværdikode for den modstridende dimension i dimensionsgruppen.|
|Uventet dimensionsværdi for standarddimensionen hvor feltet **Værdibogføring** indeholder **Ingen kode**|– %1 %2 må ikke angives.<br />– %1 %2 må ikke angives for %3 %4|– Ret feltet **Værdibogføring** på siden **Standarddimension**.<br />– Fjern den uoverensstemmende linje fra dimensionsgruppen.|
|En dimensionsrettelse fuldføres ikke korrekt.||-Vælg **Nulstil** for at føre rettelsen tilbage til en kladdetilstand. Derved nulstilles ændringerne, og du kan udføre rettelsen igen.|

## <a name="changing-dimension-assignments-after-posting"></a>Ændring af dimensionstildelinger efter bogføring

Hvis du opdager, at der er anvendt en ukorrekt dimension på bogførte finansposter, kan du rette dimensionsværdierne og opdatere dine analysevisninger. Rettelsen hjælper med til at sikre, at dine finansrapporter og analyser bliver nøjagtige.

> [!IMPORTANT]
> Funktionerne til korrigering af dimensioner er kun beregnet til at gøre finansiel rapportering præcis. Dimensions korrektioner gælder kun for finansposterne. De dimensioner, der er tildelt til poster i andre finansposter, ændres ikke for den samme transaktion. Der er uoverensstemmelse mellem de dimensioner, der er tildelt i finansbogholderiet og under Finans.

### <a name="set-up-dimension-corrections"></a>Konfigurere dimensionskorrektioner

Du skal overveje to ting, når du opsætter dimensionsrettelser:

* Er der dimensioner, som du ikke vil give brugere tilladelse til at ændre? På siden **Indstillinger for dimensionsrettelser** skal du angive de dimensioner, som du vil spærre for ændringer.
* Hvem kan ændre dimensioner? Hvis du vil tillade, at brugere foretager ændringer, skal du tildele brugerne tilladelsen **D365 DIM CORRECTION**. Med tilladelserne lader du brugerne oprette dimensionsrettelser, køre dem og fortryde dem, hvis det er nødvendigt. De kan også angive spærrede dimensioner. Du kan finde flere oplysninger i [Tildele tilladelser til brugere og grupper](ui-define-granular-permissions.md). 

### <a name="correct-a-dimension"></a>Rette en dimension

Du kan manuelt vælge en eller flere finansposter, eller du kan bruge filtre til at vælge sæt af poster. Hvis det er nødvendigt, kan du også tilføje eller slette dimensioner. 

1. Hvis du vil starte en dimensionsrettelse, skal du bruge én af følgende sider:

    *  **På siden Finansjournaler** skal du vælge en journal og derefter vælge **handlingen Korrekte dimensioner** . Denne handling starter en rettelse af posterne i den valgte journal.
    * Vælg handlingen **Korrekte** dimensioner **på siden Finansposter** . 

2. Angiv oplysninger om ændringen i feltet **Beskrivelse**. Andre brugere kan bruge disse oplysninger senere til at forstå, hvad der er udført.
3. Vælg de relevante poster I oversigtspanelet **Valgte finansposter**.

    > [!IMPORTANT]
    > Når du ændrer en valg, nulstilles værdierne i oversigtspanelet **Ændringer i dimensionsrettelser**. Du skal derfor altid vælge posterne, før du angiver ændringer af dimensionsværdierne.

   Den følgende tabel beskriver indstillingerne.

   |Indstilling  |Description  |
   |---------|---------|
   |Tilføje relaterede poster     |Tilføj finansposter, der er i den samme finansjournal.|   
   |Tilføje efter filter     |Brug filterkriterier, når du tilføjer finansposter.|
   |Manuelt valg     |Vælg specifikke finansposter.         |
   |Tilføje efter dimensioner     |Filtrer finansposter efter dimensioner.         |
   |Fjerne poster     |Fjern markering af finansposter.         |
   |Administrere valgkriterier     |Hold styr på valgprocessen, og fortryd valg, hvis det er nødvendigt.         |

4. Vælg den dimension, du vil ændre i feltet **Dimensionskode** i oversigtspanelet **Ændringer i dimensionsrettelser**, og vælg den nye værdi i feltet **Ny dimensionsværdikode**.
5. Hvis du vil validere rettelsen, skal du vælge **Valider dimensionsændringer**. Du kan finde flere oplysninger i [Validering af dimensionsrettelser](finance-troubleshooting-correcting-dimensions.md#validating-dimension-corrections).
6. Vælg **Kør**.

### <a name="validate-dimension-corrections"></a>Validere dimensionsrettelser

Før du foretager en rettelse, er det en god ide at validere den først. Validering kontrollerer, om der er begrænsninger for værdibogføring på finanskonti, begrænsninger for dimensioner, og om dimensionsværdierne er spærrede. Under valideringen angives status for rettelsen til **Validering i gang**. Når du validerer en rettelse, vises resultatet i feltet **Valideringsstatus**. Hvis der er fundet fejl, kan du bruge handlingen **Vis fejl** for at undersøge dem nærmere. Når du har rettet en fejl, skal du bruge handlingen **Genåbn** for at udføre rettelsen eller en ny validering.

Du kan enten udføre en rettelse med det samme eller planlægge, at den skal udføres senere. Hvis du udfører rettelser i et stort datasæt, anbefales det, at du planlægger at udføre dem uden for normal arbejdstid. Du kan finde flere oplysninger i [Dimensionsrettelser i store datasæt](finance-troubleshooting-correcting-dimensions.md#dimension-corrections-on-large-data-sets).

### <a name="undo-a-correction"></a>Fortryde en rettelse

Når du har rettet en dimension, kan du bruge handlingen **Fortryd** til at nulstille den tidligere værdi, hvis du ikke bryder dig om, hvad du ser. Du kan dog kun annullere den seneste rettelse. Før du annullerer en rettelse, kan du validere de ændringer, som annulleringen foretager. validering er f.eks. nyttigt, hvis dimensionsbegrænsningerne er blevet ændret efter udførelsen af rettelsen.

Hvis handlingen Fortryd ikke er tilgængelig, f.eks. fordi du har udført mange rettelser, kan du bruge handlingen **Kopier til kladde** for at starte en ny rettelse i de samme poster.

### <a name="dimension-corrections-on-large-data-sets"></a>Dimensionsrettelser i store datasæt

Vær forsigtig, når du retter store sæt poster, f.eks. et sæt, der indeholder mere end 10.000 poster. Hvis du kan, anbefales det, at du bruger filtrene til at udføre rettelserne på mindre sæt af data. Det er også en god ide at udføre rettelser uden for normal åbningstid. 

### <a name="use-analysis-views-with-dimension-corrections"></a>Brug af analysevisninger med dimensionsrettelser

Hvis **Opdatering af bogføring** er aktiveret for en analysevisning, kan [!INCLUDE[prod_short](includes/prod_short.md)] opdatere visning af, hvornår dokumenter og kladder er bogført. Du kan også opdatere visninger med resultater af dimensionsrettelser, når denne indstilling er aktiveret. Hvis du vil gøre det, skal du slå til/fra-knappen for **Opdater analysevisninger** til. Hvis du opdaterer analysevisninger, kan det påvirke ydeevnen, især for store datasæt. Derfor anbefales det, at du kun opdaterer analysevisninger for små datasæt.  

### <a name="view-historical-dimension-corrections"></a>Få vist historiske dimensionsrettelser

Hvis en finanspost var rettet, kan du undersøge ændringen ved at bruge handlingen **Oversigt over dimensionsrettelser**.

### <a name="handle-incomplete-corrections"></a>Håndter ufuldstændige rettelser

Hvis en rettelse ikke fuldføres, vises der en advarsel på rettelseskortet. Hvis det sker, kan du bruge handlingen **Nulstil** til at annullere rettelsen til en kladdestatus og annullere ændringerne. Derefter kan du udføre rettelsen igen.

> [!NOTE]
> Nulstilling af en ufuldstændig rettelse påvirker ikke opdateringer af analysevisninger, fordi de sker i slutningen af rettelsesprocessen.

### <a name="use-cost-accounting-with-corrected-gl-entries"></a>Brug af omkostningsregnskab med rettede finansposter

Når du har rettet dimensionerne vil dine data til omkostningsregnskabet ikke være synkroniserede. Omkostningsregnskabet bruger dimensioner til at samle beløb for omkostningssteder og omkostningsemner og udføre omkostningsfordelinger. Ændring af dimensioner for finansposter vil det sandsynligvis betyde, at du skal køre dine omkostningsregnskabsmodeller igen. Afhængigt af de data, der blev opdateret, og hvordan funktionerne i omkostningsberegningen er konfigureret, skal du muligvis:

* Slet nogle få omkostningsjournaler, og kør allokeringer igen.
* Slet alt, og kør alle dine modeller igen.

Du skal manuelt identificere hvor dimensionsrettelser påvirker omkostningsregnskabet, og hvor opdateringer er nødvendige. I øjeblikket kan [!INCLUDE[prod_short](includes/prod_short.md)] ikke udføre denne proces automatisk.

## <a name="see-also"></a>Se også

[Arbejde med dimensioner](finance-dimensions.md)    
[Analysere data efter dimensioner](bi-how-analyze-data-dimension.md)    

[!INCLUDE[footer-include](includes/footer-banner.md)]
