---
title: Montere elementer
description: Få mere at vide om montage efter ordre-processer og montage til lager-processer i Business central.
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bholtorf
ms.service: dynamics365-business-central
ms.topic: how-to
ms.date: 11/23/2022
ms.search.keywords: 'kit, kitting'
ms.search.form: '900, 901, 902, 903, 904, 907, 910, 916, 920, 921, 922, 923, 940, 941, 942, 930, 931, 932, 914, 915, 905'
ms.custom: bap-template
---
# <a name="assemble-items"></a>Montere elementer

Hvis feltet **Genbestillingssystem** på varekortet indeholder **Montage**, er standardmetoden til at levere varen at montere den fra definerede komponenter og potentielt af en ressource, der er defineret. Flere oplysninger i [Arbejde med Montagestyklister](assembly-how-work-assembly-boms.md). Du kan finde flere oplysninger om opsætning af et montageelement i [Om montage til ordre eller montage til lager](assembly-assemble-to-order-or-assemble-to-stock.md).

Konfiguration af montageelementer for to forskellige montageprocesser.

|Behandl  |Beskrivelse  |
|---------|---------|
|Montage til lager     | Varer, som du samler og lagrer for fremtidige salg. F. eks. pakker til en kommende salgskampagne. Varerne er endnu ikke relateret til en salgsordre. Disse varer tilpasses typisk ikke til kundeanmodninger.        |
|Montage til ordre     | Varer, som du ikke vil have på lager. Da de er tilpasset på baggrund af kundeordrer eller reducerer omkostningerne ved den disponible lagerbeholdning. |
  
Denne artikel beskriver standardindstillingerne for montage til lagerbeholdning. Der kan være andre metoder, som er mere velegnede til virksomheden. Du kan finde flere oplysninger i [Sælge lagervarer i montage til ordre-flows](assembly-how-to-sell-assemble-to-order-items-and-inventory-items-together.md) og [Sælge montage til ordre-varer og lagervarer sammen](assembly-how-to-sell-assemble-to-order-items-and-inventory-items-together.md).

> [!NOTE]  
> Montagekomponenter håndteres på en særlig måde i grundlæggende lageropsætninger. Flere oplysninger i [Håndtering af montage til ordre-varer med pluk](warehouse-how-to-pick-items-with-inventory-picks.md#handling-assemble-to-order-items-with-inventory-picks).

## <a name="to-assemble-an-item-to-stock"></a>Sådan monteres et element til lager

Udfør trinnene i denne procedure for at samle en vare på lager. Du kan lære mere om montage efter ordre ved at gå til [Sælge varer, der er samlet til ordre](assembly-how-to-sell-items-assembled-to-order.md).

1. Vælg ![Lightbulb, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **Montageordrer**, og vælg derefter det relaterede link.  
2. Vælg handlingen **Ny**. Siden **Ny montageordre** åbnes.  
3. Udfyld felterne efter behov. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
4. Vælg det montageelement, som skal behandles, i feltet **Varenr.**. Du kan vælge varer, der er oprettet til montage og har en montagestykliste, eller varer uden en montagestykliste. Dette er nyttigt i forbindelse med ikke-planlagte samlinger eller scenarier, når du vil bruge vareomposteringer og sporingsomkostninger.  
5. I feltet **Antal** skal du angive, hvor mange enheder af varen, der skal monteres.  

    > [!NOTE]  
    >  Hvis en eller flere komponenter ikke er tilgængelige til at fuldføre mængden på forfaldsdato, åbnes siden **Montagedisponering**. Siden viser, hvor mange montageelementer, der kan monteres på basis af komponenttilgængeligheden. Flere oplysninger i [Vise varedisponering](inventory-how-availability-overview.md). Når du lukker siden, oprettes montageordren med beskeder om tilgængelighed på linjerne for de berørte komponenter.  

    Linjerne indeholder indholdet af montagestyklisten og de angivne antal.  

    > [!NOTE]  
    >  Hvis siden **Montagedisponering** åbnes, når du har udfyldt montageordrehovedet, indeholder hver berørt montageordrelinje et **Ja** i feltet **Disponeringsadvarsel** med et link til yderligere disponeringsoplysninger. <!--check whether this field help is useful For more information, see Check Availability.--> Du kan løse et problem med tilgængeligheden af komponenter ved at:

    > * Udskyde startdatoen.
    > * Udskift komponenten med en anden vare.
    > * Valg af tilgængelig erstatning, hvis der er defineret en.  

6. I feltet **Antal til montage** skal du angive, hvor mange enheder af montageelementet, du vil bogføre som afgang, næste gang du bogfører montageordren. Dette antal kan være lavere end værdien i feltet **Antal** som afspejling af en delvis afgangsbogføring.  

    > [!NOTE]  
    >  For at sikre, at bogføringen af komponentforbruget svarer til bogføringen af montageelementafgangen, reguleres antalsfelterne i montageordrelinjerne automatisk til den værdi, du angiver i feltet **Antal til montage**.  
7. På montageordrelinjer af typen **Vare** eller **Ressource** skal du i feltet **Antal til forbrug** angive, hvor mange enheder du vil bogføre som forbrugte, næste gang du bogfører montageordren.
8. Når du er klar til at bogføre helt eller delvist, kan du vælge handlingen **Bogfør**.  

    > [!NOTE]  
    >  Hvis der stadig findes advarsler i nogen af montageordrelinjerne, kan du ikke gennemføre bogføringen. Der vises en meddelelse om, hvilke komponenter der ikke er på lager.  

Når bogføringen er udført, bogføres montageelementet som afgang til den lokationskode og potentielle placeringskode, der er defineret på montageordren. For manuelt oprettede montageordrer kopieres placeringen evt. fra opsætningsfeltet **Standardlokation for ordrer**. Ved montage efter ordre-forløb kopieres lokationskoden evt. fra salgsordrelinjen.  

## <a name="see-also"></a>Se også

[Montagestyring](assembly-assemble-items.md)  
[Arbejde med montagestyklister](assembly-how-work-assembly-boms.md)  
[Lagerbeholdning](inventory-manage-inventory.md)  
[Warehouse Management-oversigt](design-details-warehouse-management.md)
[Arbejde med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
