---
title: 'Oprette projektressourceomkostninger, -priser og -kapacitet'
description: For at bruge ressourcer og lette projektstyring skal du angive omkostninger og priser for individuelle ressourcer eller ressourcegrupper og angive ressourcekapacitet.
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bholtorf
ms.topic: conceptual
ms.search.keywords: 'project management, capacity, staff'
ms.search.form: '72, 76, 77, 203, 204'
ms.date: 08/19/2024
ms.service: dynamics-365-business-central
ms.custom: bap-template
---
# <a name="set-up-resources-for-projects"></a>Konfigurere ressourcer for projekter

For at kunne administrere ressourceaktiviteterne korrekt skal du oprette ressourcerne og de tilhørende omkostninger og priser. De projektrelaterede pris-, rabat- og kostfaktorregler oprettes på projektkortet. Du kan angive omkostninger og priser for individuelle ressourcer, ressourcegrupper eller alle tilgængelige ressourcer i virksomheden.

Når der bruges eller sælges ressourcer i et projekt, hentes de tilhørende priser og omkostninger fra de oplysninger, du har oprettet.

Du kan angive standardbeløbet pr. time, når ressourcen oprettes. Hvis du f.eks. bruger en bestemt maskine i fem timer i et projekt, udregnes projektet ud fra beløbet pr. time.

> [!NOTE]
> Du kan ikke købe eksterne ressourcer til et bestemt projekt. Vi anbefaler, at du bruger elementer af typen Service i stedet.

## <a name="to-set-up-a-resource"></a>Sådan defineres en ressource

Opret et kort for hver ressource, du vil bruge i projekter.

1. Vælg ![Lightbulb, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **Ressourcer**, og vælg derefter det relaterede link.
2. Vælg handlingen **Ny**.
3. Udfyld felterne efter behov. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]  

## <a name="to-set-up-a-resource-group"></a>Sådan oprettes en ressourcegruppe

Du kan samle flere forskellige ressourcer i en ressourcegruppe. Ressourcegruppens kapaciteter og budgetter bliver akkumuleret fra de enkelte ressourcer i gruppen. Du kan også indtaste kapaciteter for ressourcegrupper, enten uafhængigt af de akkumulerede værdier eller som supplement til dem.

1. Vælg ![Lightbulb, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **Ressourcegrupper**, og vælg derefter det relaterede link.
2. Vælg handlingen **Ny**.
3. Udfyld felterne efter behov.

## <a name="to-set-capacity-for-a-resource"></a>Sådan angives kapaciteten for en ressource

For at beregne, hvor lang tid en ressource kan bruge på projekter, skal ressourcernes kapacitet først angives som disponibel tid pr. periode i arbejdskalenderen. Denne opsætning anvendes, når du udfylder projektplanlægningslinjer, som indeholder ressourcen. Du kan finde flere oplysninger i [Oprette projekter](projects-how-create-jobs.md).

1. Vælg det ![lyspæreikon, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **Ressourcer**, og vælg derefter det relaterede link.
2. Åbn det relevante ressourcekort, og vælg derefter handlingen **Ressourcekapacitet**.
3. På siden **Ressourcekapacitet** feltet **Vis efter** skal du angive periodens længde, f.eks **Dag**, som vises i kolonnerne på oversigtspanelet **Matrix for ressourcekapacitet**.
4. For hver ressource på en linje skal du for hver periode i kolonnerne angive det antal timer, hvor ressourcen er tilgængelig.
5. Du kan også angive ressourcens ugentlige kapacitet med en startdato og en slutdato ved at vælge handlingen **Angiv kapacitet**.
6. På siden **Ressourcekap.indstillinger** skal du udfylde felterne efter behov.
7. Vælg handlingen **Opdater kapacitet**. Siden **Ressourcekapacitet** opdateres med den angivne kapacitet.
8. Luk siden.

## <a name="to-set-up-alternate-resource-costs"></a>Sådan angives ressourcekostpriser

Udover de omkostninger, der er angivet på ressourcekortet, kan du oprette alternative omkostninger for hver ressource. Hvis en medarbejder f.eks. har en højere timesats for overarbejde, kan du i denne tabel oprette en ressourcekostpris for overtidsbetalingen. Den alternative kostpris, du angiver for ressourcen, tilsidesætter kostprisen på ressourcekortet, når du bruger ressourcen i ressourcekladden.

1. Vælg ![Lightbulb, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **Ressourcer**, og vælg derefter det relaterede link.  
2. Vælg ressource, som du vil angive en eller flere alternative omkostninger for, og vælg derefter handlingen **Kostpriser**.  
3. På siden **Ressourcekostpriser** skal du udfylde felterne på en linje efter behov.  
4. Gentag trin 3 for hver alternativ ressourcekostpris, du vil oprette.

> [!NOTE]
> Hvis du vil angive ressourcekostpriser, der gælder for alle ressourcer og ressourcegrupper, skal du åbne siden **Ressourcekostpriser** og udfylde felterne.

## <a name="to-set-up-alternate-resource-prices"></a>Sådan angives ressourcepriser

Udover den pris, der er angivet på ressourcekortet, kan du oprette alternative priser for hver ressource. Alternative priser kan være betingede. De kan være betinget af, om ressourcen anvendes med et bestemt projekt eller en bestemt arbejdstype.

1. Vælg ikonet ![Lightbulb, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **Ressourcer**, og vælg derefter det relaterede link.
2. Vælg ressource, som du vil angive en eller flere alternative priser for, og vælg derefter handlingen **Priser**.
3. På siden **Ressourcesalgspriser** skal du udfylde felterne på en linje efter behov.
4. Gentag trin 3 for hver alternativ ressourcepris, du vil oprette.

## <a name="to-adjust-resource-prices"></a>Sådan reguleres ressourcepriser

Hvis du vil ændre kost- eller salgspriser for et større antal ressourcer, kan du anvende en kørsel.  

1. Vælg ikonet ![Lightbulb, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **Reguler ressourcepriser**, og vælg derefter det relaterede link.
2. Udfyld felterne på linjen efter behov, og vælg derefter knappen **OK**.

> [!NOTE]  
> Denne kørsel kan ikke bruges til at ændre eller oprette alternative salgs- eller købspriser for ressourcer. Den ændrer kun indholdet af feltet på ressourcekortet for feltet **Reguler felt**, som du har markeret i kørslen. Reguleringen træder i kraft med det samme for ressourcen, så du bør kontrollere reguleringsfaktorerne før kørslen.

## <a name="to-get-resource-price-change-suggestions-based-on-existing-alternate-prices"></a>Sådan hentes forslag til ændring af ressourcepriser ud fra eksisterende alternative priser

Hvis du allerede har angivet alternative ressourcepriser for nogle ressourcer, kan du bruge en kørsel til at angive flere alternative ressourcepriser.

1. Vælg ![Lightbulb, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **Ressourceprisforslag**, og vælg derefter det relaterede link.
2. Vælg handlingen **Foreslå ress.salgspris (pris)**, og udfyld derefter felterne efter behov.
3. Vælg knappen **OK**.  
4. Siden **Ressourceprisforslag** viser resultatet af kørslen, når den er færdig.

## <a name="to-get-resource-price-change-suggestions-based-on-standard-prices"></a>Sådan henter du forslag til ændring af ressourcepriser ud fra standardpriser

Hvis du vil angive flere alternative ressourcepriser ud fra standardpriserne på ressourcekortet, kan du anvende en kørsel.  

1. Vælg ![Lightbulb, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **Ressourceprisforslag**, og vælg derefter det relaterede link.
2. Vælg handlingen **Foreslå ress.salgspris (ress.)**, og udfyld derefter felterne efter behov.  
3. Vælg knappen **OK**.  
4. Åbn siden **Ressourceprisforslag** for at se resultatet af kørslen, når den er færdig.

## <a name="see-also"></a>Se også

[Konfigurere projektstyring](projects-setup-projects.md)  
[Projektstyring](projects-manage-projects.md)  
[Finans](finance.md)  
[Køb](purchasing-manage-purchasing.md)  
[Salg](sales-manage-sales.md)  
[Arbejd med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
