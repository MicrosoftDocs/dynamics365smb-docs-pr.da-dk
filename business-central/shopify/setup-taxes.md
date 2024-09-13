---
title: Konfigurere moms for Shopify-forbindelsen
description: Hvordan moms i Shopify og Business Central skal konfigureres.
ms.date: 05/29/2024
ms.topic: article
ms.service: dynamics-365-business-central
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bholtorf
ms.custom: bap-template
---

# Opsætte moms for Shopify-forbindelsen

I denne artikel undersøges det, hvordan forskellige indstillinger i Shopify påvirker priser og moms, der vises for kunden i butikken. Vi gennemgår også, hvordan du konfigurerer [!INCLUDE[prod_short](../includes/prod_short.md)] til at understøtte indstillingerne i Shopify. Denne artikel er ikke tænkt som en udtømmende momsvejledning. Kontakt din lokale skattemyndighed eller revisor for at få mere at vide.  

I artiklen antages det, at du skal betale moms, når du sælger varer lokalt eller internationalt.

## Hvis du sælger indenlandsk

Når du har konfigureret Shopify til at opkræve moms i dit eget land eller område, kan du vælge, hvordan du vil vise priser i din butiksfacade.

Du angiver, om du vil medtage moms i priser ved at slå til/fra for **alle priser inkl. moms** i [**Moms og afgifter**](https://www.shopify.com/admin/settings/taxes)-indstillinger i din **Shopify-administrator**.

Til/fra er aktiveret som regel for følgende lande/områder:

* Australien
* Østrig
* Belgien
* Tjekkiet
* Danmark
* Finland
* Frankrig
* Tyskland
* Island
* Italien
* Nederlandene
* New Zealand
* Norge
* Spanien
* Sverige
* Schweiz
* Storbritannien

På de forskellige markeder, f.eks. en pris på 100 EUR, der er defineret på produkt kortet, indeholder allerede moms. Prisen inklusive moms vises til kunden i butiksfacaden og ved betaling.  

I USA og Canada forventer kunderne ikke at se priser med afgifter, fordi den endelige skat afhænger af, hvor produkterne sendes til. Skat tilføjes ved betaling, så til/fra-knappen **Alle priser inkl. moms** er normalt slået fra. I dette tilfælde er en pris på $100 defineret på produktet kort prisen uden skat. Moms lægges til prisen ved udlevering.

Udfyld følgende felter på siden **Alle priser inkl. moms** er valgt i [!INCLUDE[prod_short](../includes/prod_short.md)], udfyld følgende feter på siden **Shopify-butikskort**:  

1. Aktiver til/fra-feltet **Priser inkl. moms**.  
2. Angiv den bogføringsgruppe, du vil bruge til indenlandske debitorer **Momsvirksomhedsbogføringsgruppe**.  

Nu skal du angive varepriser i feltet **Varekort** eller **Salgsprisliste** med eller uden moms. Når priserne eksporteres til Shopify, [!INCLUDE [prod_short](../includes/prod_short.md)] inkluderer indenlandsk moms i den beregnede pris og viser denne pris i produktkortet i Shopify.

> [!NOTE]
> Disse indstillinger påvirker udførsel af priser. Når du indlæser ordrer fra Shopify, stammer indstillingen for feltet **Priser inkl. moms** fra **Kundeskabelonen** på Shopify-butikskortet eller debitorskabelonen pr. land/område. Selvom du bruger standard debitoren til importerede ordrer, skal du udfylde **kundeskabelonkoden**.

## Hvis du sælger internationalt

I dette afsnit vil vi udforske indstillingerne for scenarier, hvor du skal opkræve moms, når du sælger til et andet land/område, f.eks. andre lande/områder i EU.

Connector til Shopify-connector understøtter aktuelt kun eksport af én pris. Shopify anvender automatisk lokal moms, valuta og afrunding. Funktionen **Alle priser inkl. moms** resulterer i de handlinger, der er beskrevet i følgende undersektioner.

### Alle priser inkl. moms er valgt

|-|Indenlandsk salg|Udland/område, hvor du ikke opkræver moms|Udland/område, hvor du ikke opkræver moms|
|------------------------|--------|--------|--------|
|Pris vist i butiksfacade|1200|1200|1200|
|Momsprocentsats|20|25|0|
|Pris ved kassen|1200|1200|1200|

Pris for kunde forbliver intakt, uanset hvor kunden befinder sig, men din margen påvirkes på grund af momssatser i forskellige lande/områder.

### Alle priser inkl. moms er ikke valgt

|-|Indenlandsk salg|Udland, hvor du opkræver moms|Udland, hvor du ikke opkræver moms|
|------------------------|--------|--------|--------|
|Pris vist i butiksfacade|1000|1000|1000|
|Momsprocentsats|20|25|0|
|Pris ved kassen|1200|1250|1000|

Shopify lægger lokal moms oven på den pris, der er defineret på produktkortet, ud fra hvor varer leveres til.

## Dynamisk pris inkl. moms

Lande/områder har forskellige krav vedrørende moms priser. Hvis priserne automatisk skal inkludere moms, kan du aktivere [Dynamisk moms med priser](https://help.shopify.com/en/manual/markets/pricing/dynamic-tax-inclusive-pricing) i Shopify.

I **Shopify Administration** skal du vælge **Medtag eller udelad moms baseret på kundens land**  i afsnittet **Andre markeder - præferencer** for indstillingerne [**Markeder**](https://www.shopify.com/admin/settings/markets).  

> [!NOTE]
> Denne indstilling har ikke indflydelse på repræsentation af priser på indenlandske markeder, som styres af **Alle priser inkl. moms**.

### Alle priser inkl. moms er valgt

|-|Indenlandsk salg|Udland/område, hvor moms er inkluderet i prisen|Udland/område, hvor moms ikke er inkluderet|
|------------------------|---------------|---------------|--------|
|Pris vist i butiksfacade|1200|1250|1000|
|Momsprocentsats|20|25|10|
|Pris ved kassen|1200|1250|1100|

Prisen for hver kunde ændres afhængigt af kundens opholdssted.

### Alle priser inkl. moms er ikke valgt

|-|Indenlandsk salg|Udland/område, hvor moms er inkluderet i prisen|Udland/område, hvor moms ikke er inkluderet|
|------------------------|--------|--------|--------|
|Pris vist i butiksfacade|1000|1250|1000|
|Momsprocentsats|20|25|10|
|Pris ved kassen|1200|1250|1100|

> [!NOTE]
> Indstillingen **Alle priser inkl. moms** ændrer ikke den måde, priserne vises på for internationale kunder.

## Hvis du sælger til EU-kunder

Forskellige EU-lande/områder har forskellige lokale momssatser. Men hvis du er hjemmehørende i EU og sælger til andre EU-lande/områder, kan du bruge den lokale momssats i nogle tilfælde.  

I **Shopify-administrator** skal du kontrollere afkrydsningsfeltet **Opkræv moms** i sektionen **EU** til [**Moms og afgifter**](https://www.shopify.com/admin/settings/taxes)-indstillingerne.

|Opkræv moms|Momssats|
|-|-|
|Undtagelse for mikrovirksomheder|Brug den indenlandske momssats for al salg i EU|
|One-stop shop eller lande/områdespecifik registrering|Brug momssatsen i kundens land/område|

### Opkræv moms angivet til one-stop shop-registrering

I det følgende eksempel er **Alle priser inkl. moms** aktiveret. Prisen på produktkortet er angivet til *1200*.

|-|Indenlandsk salg|Lande-/områdekode|
|------------------------|--------|--------|
|Pris vist i butiksfacade|1200|1250|
|Momsprocentsats|20|25|
|Pris ved kassen|1200|1250|

Shopify Bruger skatteprocenten i udlandet, når slutpriserne beregnes.

### Opkræv moms angivet til undtagelse for mikrovirksomheder

I det følgende eksempel er **Alle priser inkl. moms** aktiveret. Prisen på produktkortet er angivet til *1200*.

|-|Indenlandsk salg|Udland/område med lokal momssats på 25 procent.|
|------------------------|--------|--------|
|Pris vist i butiksfacade|1200|1200|
|Momsprocentsats|20|20|
|Pris ved kassen|1200|1200|

Shopify bruger den indenlandske momssatsen og ignorerer momssatsen i det andet land/område, når der beregnes slutpriser.

## Import af Shopify-ordrer, der er solgt til internationale kunder

Hvis du opkræver moms fra flere lande/områder, skal du definere en lande/områdespecifik indstilling i [!INCLUDE[prod_short](../includes/prod_short.md)]. Der er en årsag til, at denne indstilling er nødvendig. Når et salgsdokument oprettes i [!INCLUDE[prod_short](../includes/prod_short.md)], [!INCLUDE [prod_short](../includes/prod_short.md)], beregner systemet moms i stedet for at bruge dem, der blev importeret fra Shopify.

Du kan vælge lande/områdespecifikke-indstillinger i vinduet **Shopify-debitorskabelon**. Du kan definere **Standarddebitornr.** eller **Debitorskabelonnr.** I begge tilfælde skal du sørge for, at der er defineret følgende felter i den valgte kunde eller skabelon:

1. **Generel virksomhedsbogføringsgruppe** (bruges til udenlandske debitorer).
2. **Momsvirksomhedsbogføringsgruppe** (bruges til udenlandske debitorer).
3. **Priser inkl. moms** (justeret med indstillingen på Shopify-siden):

* Vælg **Ja**, hvis **Alle priser inkl. moms** er aktiveret, og **Medtag eller udelad moms baseret på kundens land** er deaktiveret.
* Vælg **Nej**, hvis **Alle priser inkl. moms** er deaktiveret, og **Medtag eller udelad moms baseret på kundens land** er deaktiveret.
* Vælg **Ja**, hvis **Medtag eller udelad moms baseret på kundens land** er aktiveret, og landet/området er angivet i [Momsinklusive lande/områder](https://help.shopify.com/en/manual/markets/pricing/dynamic-tax-inclusive-pricing#tax-inclusive-versus-tax-exclusive-countries-and-regions).
* Vælg **Nej**, hvis **Medtag eller udelad moms baseret på kundens land** er aktiveret, og landet/området ikke er angivet i [Momsinklusive lande/områder](https://help.shopify.com/en/manual/markets/pricing/dynamic-tax-inclusive-pricing#tax-inclusive-versus-tax-exclusive-countries-and-regions).

> [!NOTE]
> Indstillingen af **Priser inkl. moms** kommer fra skabelonen, ikke fra den specifikke debitor. Derfor er det vigtigt, at du har defineret debitorskabelonen.

## Andre momskommentarer

Mens den importerede Shopify-ordre viser oplysninger om moms, bliver momsen genberegnet, når du opretter et salgsdokument. Denne genberegning betyder, at det er vigtigt, at momsindstillingerne er korrekte i [!INCLUDE[prod_short](../includes/prod_short.md)].

* Flere produktsatser eller momssatser. Nogle produktkategorier er kan have reducerede momssatser. Du kan bruge funktionen [momstilsidesættelse](https://help.shopify.com/en/manual/taxes/tax-overrides#create-a-manual-collection-for-products-that-need-a-tax-override) i Shopify. Når varer importeres og oprettes i [!INCLUDE[prod_short](../includes/prod_short.md)], bruges momsopsætningen som udfyldt på vareskabelonkoden i Shopify-butikken. Før du importerer ordrer med sådanne varer, skal du opdatere momsproduktbogføringsgruppen.  
* Adresse-afhængige momssatser. Brug feltet **Prioritet af momsområde** sammen med tabellen **Debitorskabeloner** til at overskrive standardlogik, som udfyldes i **Skatteområdekode** i salgsdokumentet. Feltet **Prioritet af momsområde** angiver den prioritet, hvor funktionen skal indeholde oplysninger om land eller område og stat eller provins. Derefter bliver den tilsvarende post i Shopify-debitorskabelonen identificeret, og **Skatteområdekode**, **Momspligtig** og **Momsvirksomheds bogføringsgruppe** bruges, når der oprettes et salgsdokument.  

## Se også

[Kom i gang med Connectoren til Shopify](get-started.md)  
