---
title: 'Fremgangsmåde: Opdele lageraktivitetslinjer'
description: 'Lær, hvordan du opdeler lageraktivitetslinjer, hvis den disponible kapacitet på en foreslået placering ikke er tilstrækkelig.'
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bholtorf
ms.service: dynamics365-business-central
ms.topic: how-to
ms.date: 01/25/2023
ms.custom: bap-template
ms.search.forms: '931, 9314, 9313, 9315, 9330'
---
# <a name="split-warehouse-activity-lines"></a>Opdele lageraktivitetslinjer

I læg-på-lager-aktiviteter, bevægelser eller pluk (logistik) og i læg-på-lager-aktiviteter og pluk (lager) foreslås der automatisk placeringer for varer, der plukkes eller lægges på lager. Den faktiske mængde på den foreslåede placering er muligvis ikke tilstrækkelig, eller at der ikke er nok plads på den foreslåede placering til at lægge den ønskede bestilte mængde på lager. I begge tilfælde skal du opdele linjen, så varerne for én linje enten hentes fra eller anbringes på mere end én placering.  

Følgende fremgangsmåde gælder for følgende lagerdokumenter:

* Læg-på-lager (lager)
* Bevægelser (logistik)
* Pluk (logistik)
* Læg-på-lager-akt. (lager)
* Flytninger (lager)
* Lagerpluk  

## <a name="to-split-warehouse-activity-lines"></a>Sådan opdeles lageraktivitetslinjer

1. Åbn en lageraktivitetslinje, hvor du forsøger at håndtere en utilstrækkelig mængde.  
2. I feltet **Håndteringsantal** skal du angive det reducerede antal, som du er i stand til at håndtere.  
3. I oversigtspanelet **Linjer** skal du vælge handlingen **Handlinger**, vælge handlingen **Funktioner** og derefter vælge handlingen **Opdel linje**. En ny linje vises. Linjen er en kopi af den oprindelige linje, bortset fra at feltet **Håndteringsantal** indeholder det antal, du har fjernet fra den oprindelige linje.  
4. Tildel en placering, og hvis der anvendes styret læg-på-lager og pluk, en zone til denne nye linje, eller fortsæt med at opdele linjen efter behov, indtil du finder de rette placeringer for alle antallene.  

> [!NOTE]  
> Hvis lokationen bruger styret læg-på-lager og pluk, og du opdeler linjerne, skal du være godt kendt med lagerstedet og i stand til at vælge en placering, som passer med opbevaringskravene til varen og opfylder de generelle krav for lagerdokumentet. Det er f.eks. ikke nogen god idé at opdele en linje på et plukdokument og placere nogle af varerne i massevarelageret.  

## <a name="see-also"></a>Se også

[Warehouse Management-oversigt](design-details-warehouse-management.md)
[Lager](inventory-manage-inventory.md)  
[Sådan konfigureres Warehouse Management](warehouse-setup-warehouse.md)  
[Arbejd med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]
