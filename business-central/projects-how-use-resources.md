---
title: Registrere og regulere ressourceforbrug og priser
description: 'Beskriver, hvordan du kan registrere ressourceforbrug eller forbrug, der er knyttet til et projekt, for at holde styr på og styre omkostninger, priser, og arbejdstyper.'
author: brentholtorf
ms.topic: how-to
ms.search.keywords: 'project management, capacity, staff'
ms.search.form: '201,206, 207, 271, 493'
ms.date: 02/22/2024
ms.author: bholtorf
ms.service: dynamics-365-business-central
ms.custom: bap-template
---
# <a name="use-resources-for-projects"></a>Bruge ressourcer til projekter

Du registrerer forbruget af ressourcer i projektkladden, for at holde styr på omkostninger, priser og de arbejdstyper, der er knyttet til projekter. Du kan finde flere oplysninger i [Registrere forbrug for projekter](projects-how-record-job-usage.md).

> [!NOTE]
> Du kan også købe eksterne ressourcer, f.eks. for at fakturere en kreditor for udført arbejde. Du kan finde flere oplysninger i [Registrere køb](purchasing-how-record-purchases.md).

Du kan også bogføre forbruget af en ressource i en ressourcekladde. Posteringer i en ressourcekladde har ingen indflydelse på finanskontiene.

## <a name="to-assign-resources-to-projects"></a>Sådan tildeles ressourcer til projekter

Du kan tildele ressourcer til projekter ved at oprette projektplanlægningslinjer for projektet. Du kan finde flere oplysninger i [Oprette projekter](projects-how-create-jobs.md).

## <a name="to-record-resource-usage-for-a-project"></a>Sådan registreres ressourceforbrug for et projekt

1. Vælg ![Lightbulb, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") , skriv **Projektkladder**, og vælg derefter det relaterede link.
2. Åbn en relevant projektkladde, og udfyld felterne efter behov. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
3. Når kladden er fuldført, skal du vælge handlingen **Bogfør**.

    [!INCLUDE [preview-posting-inventory](includes/preview-posting-inventory.md)]

## <a name="to-adjust-resource-prices"></a>Sådan reguleres ressourcepriser

Hvis du vil ændre kost- eller salgspriser for et større antal ressourcer, kan du anvende en kørsel.  

1. Vælg ![Lightbulb, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **Reguler ressourcepriser**, og vælg derefter det relaterede link.
2. Udfyld felterne på linjen efter behov, og vælg derefter knappen **OK**.

> [!NOTE]  
> Denne kørsel kan ikke bruges til at ændre eller oprette alternative salgs- eller købspriser for ressourcer. Den ændrer kun indholdet af feltet på ressourcekortet for feltet **Reguler felt**, som du har markeret i kørslen. Reguleringen træder i kraft med det samme for ressourcen, så du bør kontrollere reguleringsfaktorerne før kørslen.

## <a name="to-get-resource-price-change-suggestions-based-on-existing-alternate-prices"></a>Sådan hentes forslag til ændring af ressourcepriser ud fra eksisterende alternative priser

Hvis du allerede har angivet en alternativ ressourcepris for nogle ressourcer, kan du bruge en kørsel til at angive flere alternative ressourcepriser.

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

## <a name="to-get-resource-price-change-suggestions-based-on-alternate-prices"></a>Sådan henter du forslag til ændring af ressourcepriser ud fra standardpriser

Hvis du allerede har angivet en alternativ ressourcepris for nogle ressourcer, kan du bruge en kørsel til at angive flere alternative ressourcepriser.

1. Vælg ![Lightbulb, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **Foreslå ress.salgspris (pris)**, og vælg derefter det relaterede link.  
2. Udfyld felterne efter behov.
3. Vælg knappen **OK**.  
4. Åbn siden **Ressourceprisforslag** for at se resultatet af kørslen, når den er færdig.

## <a name="see-also"></a>Se også

[Projektstyring](projects-manage-projects.md)  
[Finans](finance.md)  
[Køb](purchasing-manage-purchasing.md)         
[Salg](sales-manage-sales.md)     
[Arbejd med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
