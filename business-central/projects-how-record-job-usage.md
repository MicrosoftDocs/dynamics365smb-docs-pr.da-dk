---
title: Registrere forbrug eller brug af projektressourcer og varer
description: 'Denne artikel beskriver, hvordan du registrerer forbrug af varer eller ressourcer på projekter for at gøre projektstyringen nemmere.'
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bholtorf
ms.service: dynamics-365-business-central
ms.topic: how-to
ms.date: 02/22/2024
ms.custom: bap-template
---
# Registrere forbrug eller brug til projekter

Fra siden **Projektkort** kan du åbne siden **Projektplanlægningslinjer** for at gennemgå og registrere brugen af forskellige dele af projektet. Disse oplysninger opdateres automatisk, når du ændrer og overfører oplysninger mellem projekter og projektkladder eller projektfakturaer. Dette kræver, at du slår til/fra-knappen **Anvend anvendelseslink som standard** til på siden **Projektopsætning**. Flere oplysninger [Konfigurere projekter](projects-how-setup-jobs.md).  

F.eks. kan du angive antallet af en ressource, og hvilken mængde, der skal overføres til projektkladden, for planlægningslinjer af typen **Budget**. Hvis planlægningslinjens type er **Fakturerbar**, kan du angive antallet af ressourcen, og angive hvilket antal, der skal overføres til en faktura. Yderligere oplysninger om fakturering af debitor finder du i [Fakturaprojekter](projects-how-invoice-jobs.md). Ved at sammenligne den oprindelige mængde, restantal eller bogført antal kan du hurtigt gennemgå oplysninger om forbrug. Du kan finde oplysninger om vurdering af budgetterede værdier under planlægning under [Administrere projektbudgetter](projects-how-manage-budgets.md).  

Følgende procedurer beskrives, hvordan du kan registrere faktiske (fakturerbare) mængder eller udgifter ved projektkladde. Du kan også bruge købsdokumenter til at registrere indkøb for et projekt. Få mere at vide i [Administrere projektforsyninger](projects-how-manage-project-supplies.md).

## Sådan registreres forbrug for en projektplanlægningslinje af typen Budget

1. Vælg det ![lyspæreikon, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **Projekter**, og vælg derefter det relaterede link.  
2. Markér det relevante projekt, og vælg derefter handlingen **Projektplanlægningslinjer**. 
3. Vælg en projektplanlægningslinje af typen **Budget** eller **Både budget og fakturerbar**, som du vil registrere forbruget for.   

    > [!NOTE]
    > Du kan også registrere forbrug for en projektplanlægningslinje af typen **Fakturerbar**. I dette tilfælde skal du typisk bruge disse linjer til at oprette fakturaer, men du kan også overføre det til en kladde. Flere oplysninger i [Fakturere projekter](projects-how-invoice-jobs.md) 

4. I feltet **Antal, der skal overføres til kladde** skal du angive det nummer, du vil overføre. Standardantallet er den værdi, du angiver i feltet **Antal**.

    Feltet **Restantal** viser det antal, der mangler for at afslutte projektet og blive overført til kladden.
5. Vælg handlingen **Opret projektkladdelinjer**.

    > [!TIP]
    > Hvis du vil tilføje flere projektplanlægningslinjer for dette projekt, skal du vente med dette trin, indtil du har tilføjet alle projektplanlægningslinjer.
6. På siden **Kopier projekt til projektplanlægningslinje** skal du udfylde felterne efter behov og derefter vælge knappen **OK**. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
7. Vælg handlingen **Åbn projektkladde**.  
8. På siden **Projektkladde** skal du markere den relevante linje og derefter vælge handlingen **Bogfør**.

    [!INCLUDE [preview-posting-inventory](includes/preview-posting-inventory.md)]

9. På siden **Projektplanlægningslinjer** skal du gennemgå det registrerede forbrug ved at holde øje felterne **Antal**, **Restantal** og **Antal, der skal overføres til kladde**.  
10. Gentag trin 3 til 8 for at registrere ekstra forbrug.  

## Sådan oprettes projektkladdelinjer manuelt

1. Vælg ![Lightbulb, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") , skriv **Projektkladder**, og vælg derefter det relaterede link.  
2. I feltet **Kladdenavn** skal du vælge et relevant projektkladdenavn.  
3. På en ny linje skal du angive bilagsnummer, projektnummer, projektopgavenummer, type og mængde af den type, der forbruges.  
4. Når projektkladdelinjerne er fuldført, skal du vælge handlingen **Bogfør**.  

    [!INCLUDE [preview-posting-inventory](includes/preview-posting-inventory.md)]

## Sådan vises projektforbrugsestimater og bogføringsopdateringer

Du kan få vist projektforbruget op til færdiggørelsen af et projekt i ét trin. Hvis du vil gøre det, skal du bruge kørslen **Beregn resterende forbrug for projekt** for alle sagerne op til og inklusive afslutningen af et projekt.  

På denne måde kan du holde styr på og sammenligne dine oprindelige estimater med de faktiske resultater og foretage ændringer eller oprette nye poster efter behov. Du kan f.eks. have anslået, at et projekt krævede 10 timer, og at det frem til nu har taget 15 timer. Du kan føje de ekstra fem timer til den eksisterende kladdelinje eller oprette en ny kladdelinje for at rapportere disse fem timer som overtid, hvilket er en anden arbejdstype. Den korrekte omkostning og pris beregnes, og du kan derefter bogføre den til kladden.  

> [!NOTE]  
> Vareposter opretter vareposter til finans og reducerer antallet af varer på lager. Kørslen **Bogfør lagerregulering** overfører omkostningen fra lager til finans. Ressourceposter opretter ressourceposter til finans.  

1. Vælg det ![lyspæreikon, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") , skriv **Projektkladder**, og vælg derefter det relaterede link.  
2. Vælg en relevant projektkladde, og vælg derefter handlingen **Beregn resterede forbrug**.  
3. På siden **Beregn resterende forbrug for projekt** skal du angive dokumentnummeret og bogføringsdatoen, der skal indsættes i kladden, og derefter vælge knappen **OK**.  
4. Opdater kladden med eventuelle nødvendige ændringer.  
5. Vælg **Bogfør**.

## Opret lagerbeholdnings- lagersteds-plukdokumenter for et projekt

Brug handlingerne **Opret pluk (lager)** og **Opret lager (logistik)** på siden **Projektkort**. Hvis du vil oprette eller registrere et plukdokument, skal du bruge **Læg-på-lager/pluk-linjer/bevægelseslinjer** eller **registrerede pluklinjer**. Flere oplysninger i [Flows for produktion, montage og projekter](design-details-internal-warehouse-flows.md).

Du kan bruge handlingerne under følgende betingelser:

* Projektets **status** er **åben**.
* **Linjetypen** for projektplanlægningslinjen er **Budget** eller **Både budget og fakturerbart**.
* **Typen** for projektplanlægningslinjen er **Vare**.
* **Kræv pluk** er aktiveret for den relaterede lokation.
* **Styret læg-på-lager og pluk** er deaktiveret.

> [!NOTE] 
> Selvom indstillingen kaldes **Kræver pluk**, kan du stadig bogføre forbrug direkte fra projektkladdelinjen for lokationen. Hvis lokationen er sat op til at kræve pluk, men ikke leverance, skal du bruge dokumentet **Pluk (lager)** til at organisere og udskrive plukaktiviteten. Du kan også bruge siden til at angive og bogføre resultatet af plukket, som igen bogfører forbruget af varer. 
> 
> Hvis lokationen er indstillet til at kræve både pluk og leverance, dvs. at du har markeret både feltet **Kræv pluk** og feltet **Kræv leverance** på **lokationskortet**, kan du bruge siden **Pluk (logistik)** til at håndtere plukningen. Lagerpluk svarer til pluk (lager). Forskellen er, at i stedet for at bogføre plukoplysninger, registrerer du plukket. Denne registrering bogfører ikke forbrug, den gør blot varerne disponible til bogføring. Som lagerchef kan du bruge en plukkladde til at organisere plukoplysningerne, før du opretter de enkelte plukinstruktioner (logistik)

## Sådan gennemgås planlægningslinjerne for en projektpost

Når du har bogført projektkladdelinjer, kan du se de planlægningslinjer, der er knyttet til posterne i projektkladden, der er blevet bogført.

> [!NOTE]  
> Dette kræver, at afkrydsningsfeltet **Anvend anvendelseslink** er markeret for projektet. Du kan finde flere oplysninger i [Oprette projekter](projects-how-setup-jobs.md).  

1. Vælg ikonet ![Lightbulb, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") , skriv **Projektkladder**, og vælg derefter det relaterede link.  
2. Vælg en relevant projektkladde, og vælg derefter handlingen **Poster**.  
3. På siden **Projektposter** skal du vælge handlingen **Vis tilknyttede projektplanlægningslinjer**.

## Se også

[Projektstyring](projects-manage-projects.md)  
[Finans](finance.md)  
[Køb](purchasing-manage-purchasing.md)  
[Salg](sales-manage-sales.md)  
[Arbejd med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
