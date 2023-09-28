---
title: 'Sælge varer, der er monteret til ordre'
description: 'Sådan sælger du en vare, der er samlet til ordre.'
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bholtorf
ms.service: dynamics365-business-central
ms.topic: how-to
ms.date: 11/23/2022
ms.search.keywords: 'kit, kitting, substitute items'
ms.search.form: '900, 901, 902, 903, 904, 907, 910, 916, 920, 921, 922, 923, 940, 941, 942, 930, 931, 932, 914, 915, 905'
ms.custom: bap-template
---
# <a name="sell-items-assembled-to-order"></a>Sælge varer, der er monteret til ordre

Varer, der er konfigureret til montage til ordre, forventes varen derefter ikke at være på lager, og den skal samles specifikt til en salgsordre. En vare, der er konfigureret til montage efter ordre, når feltet **montagepolitik** på varekortet indeholder **montage efter ordre**. Når du indtaster varen på en salgsordrelinje, bliver der automatisk oprettet en montageordre, hvorefter den knyttes til salgsordren.  

> [!NOTE]  
> Hvis montage efter ordre-elementer allerede findes i lageret, kan de fratrække mængden fra montageordre og reservere den fra lageret. Flere oplysninger i [Sælge lagervarer i montage til ordre-forløb](assembly-how-to-sell-assemble-to-order-items-and-inventory-items-together.md).  

I denne procedure behandler du salg af et element, der skal samles i henhold til specifikationer, der er anmodet af debitor. Trinnene er følgende: 

* Oprette en salgsordrelinje.
* Tilpasning af montageelementet ved at redigere dets komponenter og ressourcer.
* Kontrollere tilgængelighed for at oprette en leveringsdato.
* Frigivelse af salgsordren til montage og afsendt med det samme.  

> [!NOTE]  
> Følgende procedure omfatter ikke trinnene til oprettelse af standardsalgsordre før det trin, hvor du indtaster montage efter ordre-elementer på en salgsordrelinje. Få mere at vide om oprettelse af salgsordrer i [Salg af produkter med en kundesalgsordre](sales-how-sell-products.md).  

## <a name="to-sell-an-item-that-is-assembled-to-order"></a>Sådan sælger du en vare, der er samlet til ordre

1. Vælg ![Lightbulb, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **Salgsordrer**, og vælg derefter det relaterede link.  
2. Oprette en salgsordre. 
3. I feltet **Nummer** skal du angive en vare, der er indstillet til at samles til ordre.  
4. I feltet **Lokationskode** skal du definere, hvilken lokation varen sælges fra. Montageprocessen vil forekomme på denne placering.  
5. I feltet **Antal** skal du angive, hvor mange enheder, der skal sælges.  

    > [!NOTE]  
    >  Hvis en eller flere komponenter af antallet af anmodede montageelementer ikke er tilgængelige, åbnes en side med en detaljeret tilgængelighedsadvarsel. <!-- Check whether the field help would be useful. For more information, see Assembly Availability.  -->

    Der oprettes nu en montageordre med tilknytning til salgsordrelinjen. Forfaldsdato for montageordren er afsendelsesdatoen for salgsordrelinjen.  

    Antal, der skal sælges, kopieres til feltet **Antal til montage efter ordre**, som angiver, at vareopsætningen forventer, at hele mængden på salgslinjen skal samles til ordren. Du kan reducere antallet til montage efter ordre, hvis du f.eks ved, at nogle elementer allerede er tilgængelige. Flere oplysninger i [Sælge lagervarer i montage til ordre-forløb](assembly-how-to-sell-inventory-items-in-assemble-to-order-flows.md).  

6. Hvis en debitor ønsker yderligere et element i en pakke, skal du på oversigtspanelet **Linjer** vælge handlingen **Linje**, vælge handlingen **Montage til ordre** og derefter vælge handlingen **Montage til ordre-linjer** for at få vist og ændret standardmontagekomponenterne. Du kan også vælge feltet **Antal til montage efter ordre**.  
7. På siden **Montage efter ordre-linjer** oprettes en ny linje af typen **Element** for det ekstra montagekomponent.  

    Du kan også tilpasse rækkefølgen ved at øge antallet af ét standardelement i pakken. Du kan gøre dette ved at forøge værdien i feltet **Mængde pr.** på den pågældende montageordrelinje.  

    > [!NOTE]  
    >  Siden **Montage efter ordre-linjer** indeholder kun de vigtigste felt til tilpasning af komponentoversigten, med tilføjelse af varesporingsnumre eller løsning af problemer med komponent-tilgængelighed. Hvis du vil tilføje flere montageordreoplysninger, f.eks. montageordrens startdato, skal du vælge handlingen **Vis dokumenter**. Dette åbner en komplet visning af den montageordre, der er tilknyttet salgsordrelinjen. Du kan ikke ændre indholdet i de fleste felter i montageordrehovedet, og du kan ikke bogføre montageoutput fra den. Du skal bogføre leveringen af salgsordrelinjen.  
    >
    >  I tilknyttede montageordrer er det kun feltet **Startdato**, der kan ændres. Hvis du ændrer startdatoen, angiver det, at montagearbejdere skal starte montagen tidligere end forfaldsdatoen. Alle felter på linjerne i den tilknyttede montageordre kan ændres, så lagermedarbejdere kan indtaste tallene for forbrug under processen.  

8. Gennemse eller reager på problemer med tilgængeligheden af komponenter. Vælg f. eks. et erstatningselement.  
9. Luk siden **Montage efter ordre-linjer**. Den tilknyttede montageordre er nu klar til at begynde samling af de tilpassede elementer.  
10. På salgsordren skal du vælge handlingen **Frigiv** for at advisere montageafdelingen om, at montageprocessen kan startes. Flere oplysninger i [Montage af varer](assembly-how-to-assemble-items.md).  

> [!NOTE]  
> Erstatningsvarer erstatter ikke automatisk en vare med en anden vare, f.eks. når der oprettes en salgsordre eller en stykliste. I stedet bliver du advaret om, at der er en erstatningsvare tilgængelig.

## <a name="see-also"></a>Se også

[Montagestyring](assembly-assemble-items.md)  
[Arbejde med montagestyklister](assembly-how-work-assembly-boms.md)  
[Registrere nye varer](inventory-how-register-new-items.md)  
[Lagerbeholdning](inventory-manage-inventory.md)  
[Warehouse Management-oversigt](design-details-warehouse-management.md)
[Arbejde med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
