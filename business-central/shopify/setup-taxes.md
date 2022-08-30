---
title: Konfigurere moms for Shopify-forbindelsen
description: Hvordan moms i Shopify og Business Central skal konfigureres.
ms.date: 05/27/2022
ms.topic: article
ms.service: dynamics365-business-central
author: AndreiPanko
ms.author: andreipa
ms.openlocfilehash: 0070d583752002cc34ebff74dee2906c289b7136
ms.sourcegitcommit: b353f06e0c91aa6e725d59600f90329774847ece
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 08/19/2022
ms.locfileid: "9317486"
---
# <a name="set-up-taxes-for-the-shopify-connection"></a>Konfigurere moms for Shopify-forbindelsen

I denne artikel undersøges det, hvordan forskellige indstillinger i Shopify påvirker priser og moms, der vises for kunden i butikken. Vi gennemgår også, hvordan du konfigurerer [!INCLUDE[prod_short](../includes/prod_short.md)] til at understøtte indstillingerne i Shopify. Denne artikel er ikke tænkt som en udtømmende momsvejledning. Kontakt din lokale skattemyndighed eller revisor for at få mere at vide.  

I artiklen antages det, at du skal betale moms, når du sælger varer lokalt eller internationalt.

## <a name="if-you-sell-domestically"></a>Hvis du sælger indenlandsk 

Når du har konfigureret Shopify til at opkræve moms i dit eget land eller område, kan du vælge, hvordan du vil vise priser i din butiksfacade. Du kan styre dette ved at aktivere eller deaktivere **Alle priser inkl. moms** i indstillingerne for [**Moms og afgifter**](https://www.shopify.com/admin/settings/taxes) i din **Shopify-administration**.

Det er almindeligt at aktivere dette for lande som Australien, Østrig, Belgien, Den Tjekkiske Republik, Danmark, Finland, Frankrig, Tyskland, Island, Italien, Nederlandene, New Zealand, Norge, Spanien, Sverige, Schweiz og Storbritannien. På markeder som disse, vil prisen *100 EUR*, som er defineret i produktkortet, allerede indeholde moms, og den samme pris vises for kunden på butiksfacaden og ved kassen.  

I USA og Canada forventer kunderne at få vist produktpriser uden moms, som tilføjes ved kassen. Feltet **Alle priser inkl. moms** er som regel ikke markeret. I dette tilfælde repræsenterer prisen *$100*, der er defineret på produktkortet, prisen uden moms. Moms lægges til prisen for at beregne totalen ved kassen.

For at understøtte det scenario, hvor **Alle priser inkl. moms** er valgt på siden [!INCLUDE[prod_short](../includes/prod_short.md)], skal du udfylde feltet **Debitorskabelonkode** på siden **Shopify-butikskort** for at få adgang til skabelonen med følgende felter defineret:  
<!--I changed that last part of the sentence above because it didn't track logically. Just wanted to let you know in case I introduced an inaccuracy.-->

1. **Generel virksomhedsbogføringsgruppe** bruges til indenlandske debitorer.  
2. **Momsvirksomhedsbogføringsgruppe** bruges til indenlandske debitorer.  
3. **Priser inkl. moms** angivet til *Ja*.  

Nu skal du angive varepriser i feltet **Varekort** eller **Salgsprisliste** med eller uden moms. Når priserne eksporteres til Shopify, beregnes prisen automatisk til at medtage indenlandsk moms for at vise denne pris i produktkortet i Shopify.

> [!NOTE]
> Hvis du har konfigureret Shopify-connectoren til automatisk at oprette debitorer, kan du have brug for flere felter i din skabelon, f.eks. **Debitorbogføringsgruppe**. Hvis du bruger standarddebitoren til importerede ordrer, skal du kontrollere, at debitoren har fået udfyldt de samme felter. Du skal stadig udfylde **Kundeskabelonkode** som angivet ovenfor, da feltet **Priser inkl. moms**/**Priser ekskl. moms** i det oprettede salgsdokument afhænger ikke af debitoren, men af **Debitorskabelon** fra Shopify-butikskortet eller -debitorskabelonen pr. land/område.

## <a name="if-you-sell-internationally"></a>Hvis du sælger internationalt

I dette afsnit vil vi udforske indstillingerne for scenarier, hvor du skal opkræve moms, når du sælger til et andet land, f.eks. andre lande i EU. 

Connector til **Shopify**-udvidelsen understøtter aktuelt kun eksport af én pris. Shopify anvender automatisk lokal moms, valuta og afrunding. Funktionen **Alle priser inkl. moms** resulterer i de handlinger, der er beskrevet i følgende undersektioner.

### <a name="all-prices-include-tax-is-selected"></a>*Alle priser inkl. moms* er valgt

||Indenlandsk salg|Udland, hvor du opkræver moms|Udland, hvor du ikke opkræver moms|
|------------------------|--------|--------|--------|
|Pris vist i butiksfacade|1200|1200|1200|
|Momsprocentsats|20|25|0|
|Pris ved kassen|1200|1200|1200|

Pris for kunde forbliver intakt, uanset hvor kunden befinder sig, men din margen påvirkes på grund af momssatser i forskellige lande.

### <a name="all-prices-include-tax-is-not-selected"></a>*Alle priser inkl. moms* er ikke valgt

||Indenlandsk salg|Udland, hvor du opkræver moms|Udland, hvor du ikke opkræver moms|
|------------------------|--------|--------|--------|
|Pris vist i butiksfacade|1000|1000|1000|
|Momsprocentsats|20|25|0|
|Pris ved kassen|1200|1250|1000|

Shopify lægger lokal moms oven på den pris, der er defineret på produktkortet, ud fra hvor varer leveres til.

## <a name="dynamic-tax-inclusive-pricing"></a>Dynamisk pris inkl. moms

Da forskellige lande har forskellige krav, der afhænger af, om du inkluderer moms i den viste pris eller ej, kan du slå [dynamiske priser inkl moms](https://help.shopify.com/en/manual/markets/pricing/dynamic-tax-inclusive-pricing) til i Shopify. Derved automatiseres momsmedtagelsesfunktionen. 
<!--I added the last sentence to complete the thought. I hope that's okay.-->

Vælg **Medtag eller udelad moms baseret på kundens land** i afsnittet **Andre markeder - præferencer** for indstillingerne [**Markeder**](https://www.shopify.com/admin/settings/markets) i din **Shopify-administration**.  

> [!NOTE]
> Denne indstilling har ikke indflydelse på repræsentation af priser på indenlandske markeder, som styres af **Alle priser inkl. moms**.

### <a name="all-prices-include-tax-is-selected"></a>*Alle priser inkl. moms* er valgt

||Indenlandsk salg|Udland, hvor moms er inkluderet i prisen|Udland, hvor moms ikke er inkluderet|
|------------------------|--------|--------|--------|
|Pris vist i butiksfacade|1200|1250|1000|
|Momsprocentsats|20|25|10|
|Pris ved kassen|1200|1250|1100|

Prisen for hver kunde ændres afhængigt af kundens opholdssted.

### <a name="all-prices-include-tax-is-not-selected"></a>*Alle priser inkl. moms* er ikke valgt

||Indenlandsk salg|Udland, hvor moms er inkluderet i prisen|Udland, hvor moms ikke er inkluderet|
|------------------------|--------|--------|--------|
|Pris vist i butiksfacade|1000|1250|1000|
|Momsprocentsats|20|25|10|
|Pris ved kassen|1200|1250|1100|

> [!NOTE]
> Indstillingen **Alle priser inkl. moms** ændrer ikke den måde, priserne vises på for internationale kunder.

## <a name="if-you-sell-to-eu-customers"></a>Hvis du sælger til EU-kunder

Forskellige EU-lande har forskellige lokale momssatser. Men hvis du er hjemmehørende i EU og sælger til andre EU-lande, kan du bruge den lokale momssats i nogle tilfælde.  

Markér afkrydsningsfeltet **Opkræv moms** i afsnittet **EU** for indstillingerne [**Moms og afgifter**](https://www.shopify.com/admin/settings/taxes) i din **Shopify-administration**.

|Opkræv moms|Momssats|
|-|-|
|Undtagelse for mikrovirksomheder|Brug den indenlandske momssats for al salg i EU|
|One-stop shop eller landespecifik registrering|Brug momssatsen i kundens land|


### <a name="collect-vat-set-to-one-stop-shop-registration"></a>Opkræv moms angivet til one-stop shop-registrering

I det følgende eksempel er **Alle priser inkl. moms** aktiveret. Prisen på produktkortet er angivet til *1200*. 
        
|-|Indenlandsk salg|Udland|
|------------------------|--------|--------|
|Pris vist i butiksfacade|1200|1250|
|Momsprocentsats|20|25|
|Pris ved kassen|1200|1250|       
        
### <a name="collect-vat-set-to-micro-business-exemption"></a>Opkræv moms angivet til undtagelse for mikrovirksomheder

I det følgende eksempel er **Alle priser inkl. moms** aktiveret. Prisen på produktkortet er angivet til *1200*. 
        
|-|Indenlandsk salg|Udland med lokal momssats på 25 procent.|
|------------------------|--------|--------|
|Pris vist i butiksfacade|1200|1200|
|Momsprocentsats|20|20|
|Pris ved kassen|1200|1200|           
    
Shopify ignorerer momssatsen i det andet land, når der beregnes slutpriser, og der bruges en indenlandsk momssats.

## <a name="importing-shopify-orders-sold-to-international-customers"></a>Import af Shopify-ordrer, der er solgt til internationale kunder

Hvis du opkræver moms fra flere lande, skal du højst sandsynligt definere en landespecifik indstilling i [!INCLUDE[prod_short](../includes/prod_short.md)]. Det er nødvendigt, for når der oprettes et salgsdokument i [!INCLUDE[prod_short](../includes/prod_short.md)], beregner systemet moms i stedet for at bruge dem, der blev importeret fra Shopify.

Du kan vælge lande/områdespecifikke indstillinger i vinduet **Shopify-debitorskabelon**.
<!--Should this be "window" or "page"? I haven't been seeing "window" is use elsewhere, but I don't know what the interface looks like for this action.--> Der kan du definere **Standarddebitornr.** eller **Debitorskabelonnr.** I begge tilfælde skal du sørge for, at der er defineret følgende felter i den valgte kunde eller skabelon:

1. **Generel virksomhedsbogføringsgruppe** (bruges til udenlandske debitorer).
2. **Momsvirksomhedsbogføringsgruppe** (bruges til udenlandske debitorer).
3. **Priser inkl. moms** (justeret med indstillingen på Shopify-siden):
* Vælg *Ja*, hvis **Alle priser inkl. moms** er aktiveret, og **Medtag eller udelad moms baseret på kundens land** er deaktiveret.
* Vælg *Nej*, hvis **Alle priser inkl. moms** er deaktiveret, og **Medtag eller udelad moms baseret på kundens land** er deaktiveret.
* Vælg *Ja*, hvis **Medtag eller udelad moms baseret på kundens land** er aktiveret, og landet/området er angivet i [Momsinklusive lande/områder](https://help.shopify.com/en/manual/markets/pricing/dynamic-tax-inclusive-pricing#tax-inclusive-versus-tax-exclusive-countries-and-regions).
* Vælg *Nej*, hvis **Medtag eller udelad moms baseret på kundens land** er aktiveret, og landet/området ikke er angivet i [Momsinklusive lande/områder](https://help.shopify.com/en/manual/markets/pricing/dynamic-tax-inclusive-pricing#tax-inclusive-versus-tax-exclusive-countries-and-regions).
<!--I changed "Set" to "Choose" since "Set" really isn't an instruction we use. if they're toggling, we then would say "Toggle" as in "Toggle *No* if...."-->
> 
[!Note]
> Indstillingen af **Priser inkl. moms** kommer fra skabelonen, ikke fra den specifikke debitor. Derfor er det vigtigt, at du har defineret debitorskabelonen.

## <a name="other-tax-remarks"></a>Andre momskommentarer

Mens den importerede Shopify-ordre viser oplysninger om moms, bliver momsen genberegnet, når du opretter et salgsdokument. Denne genberegning betyder, at det er vigtigt, at momsindstillingerne er korrekte i [!INCLUDE[prod_short](../includes/prod_short.md)].

- Flere produktsatser eller momssatser. Nogle produktkategorier er kan have reducerede momssatser. Du kan bruge funktionen [momstilsidesættelse](https://help.shopify.com/en/manual/taxes/tax-overrides#create-a-manual-collection-for-products-that-need-a-tax-override) i Shopify. Når varer importeres og oprettes i [!INCLUDE[prod_short](../includes/prod_short.md)], bruges momsopsætningen som udfyldt på vareskabelonkoden i Shopify-butikken. Før du importerer ordrer med sådanne varer, skal du opdatere momsproduktbogføringsgruppen.  

- Adresse-afhængige momssatser. Brug feltet **Prioritet af momsområde** sammen med tabellen **Debitorskabeloner** til at overskrive standardlogik, som udfyldes i **Skatteområdekode** i salgsdokumentet. Feltet **Prioritet af momsområde** angiver den prioritet, hvor funktionen skal indeholde oplysninger om land eller område og stat eller provins. Derefter bliver den tilsvarende post i Shopify-debitorskabelonen identificeret, og **Skatteområdekode**, **Momspligtig** og **Momsvirksomheds bogføringsgruppe** bruges, når der oprettes et salgsdokument.  

## <a name="see-also"></a>Se også

[Kom i gang med Connectoren til Shopify](get-started.md)  
