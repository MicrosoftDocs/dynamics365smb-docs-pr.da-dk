---
title: Designoplysninger – Kostregulering | Microsoft Docs
description: Hovedformålet med kostregulering er at flytte kostprisændringer fremad fra omkostningskilder til modtagerne på basis af en vares kostmetode for at give korrekt lagerværdi.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 06/19/2020
ms.author: sgroespe
ms.openlocfilehash: 686aa7b0e6bae7fa5fbc639f03ef3ac34237d9e8
ms.sourcegitcommit: ec3034640ed10e0fd028568ec45f21c84498d3de
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 06/19/2020
ms.locfileid: "3486417"
---
# <a name="design-details-cost-adjustment"></a>Designoplysninger: Omkostningsregulering

Hovedformålet med kostregulering er at flytte kostprisændringer fremad fra omkostningskilder til modtagerne på basis af en vares kostmetode for at give korrekt lagerværdi.  

En vare kan salgsfaktureres, før den er blevet købsfaktureret, så den registrerede lagerværdi af salget ikke svarer til den faktiske købspris. Omkostningsregulering opdaterer vareforbruget for historiske salgsposter for at sikre, at de svarer til omkostningerne for de indgående transaktioner, som de udlignes med. Du kan finde flere oplysninger i [Designoplysninger: Vareudligning](design-details-item-application.md).  

Følgende er sekundære formål eller funktioner for kostregulering:  

* Fakturer afsluttede produktionsordrer:  

  * Skift status for værdiposter fra **Forventet** til **Faktisk**.  
  * Ryd VIA-kontoer. Du kan finde flere oplysninger i [Designoplysninger: Bogføring af produktionsordre](design-details-production-order-posting.md).  
  * Bogfør afvigelse. Du kan finde flere oplysninger i [Designoplysninger: Afvigelse](design-details-variance.md).  
  * Opdater kostprisen på varekortet.  

Lagerværdien skal reguleres, før de relaterede værdiposter kan afstemmes med finans. Du kan finde flere oplysninger i [Designoplysninger: Afstemning med Finans](design-details-reconciliation-with-the-general-ledger.md).  

## <a name="detecting-the-adjustment"></a>Reguleringsregistrering

Opgaven med at registrere, om der skal ske en omkostningsregulering udføres primært af rutinen Varekladde – Bogfør linje, mens opgaven med at beregne og generere omkostningsreguleringsposter, udføres af kørslen **Juster kostpris - vareposter**.  

For at kunne overføre omkostninger bestemmer registreringsmekanismen, hvilke kilder der er ændret i omkostninger, og til hvilke destinationer disse omkostninger skal overføres. Der findes følgende tre registreringsfunktioner i [!INCLUDE[d365fin](includes/d365fin_md.md)]:  

* Vareudligningspost  
* Gennemsnitlige kostregulerede indførselssteder  
* Ordreniveau  

### <a name="item-application-entry"></a>Vareudligningspost

Denne reguleringsfunktion bruges til varer, der bruger FIFO, LIFO, standardkostmetoder og specifikke kostmetoder, og til faste udligningsscenarier. Funktionen fungerer på følgende måde:  

* Omkostningsregulering registreres ved at markere kildevareposter som *Udlignet post til regulering*, når en varepost eller værdipost bogføres.  
* Omkostninger overføres i henhold til de omkostningskæder, der er registreret i tabellen **Vareudligningspost**.  

### <a name="average-cost-adjustment-entry-point"></a>Gennemsnitlige kostregulerede indførselssteder

Denne registreringsfunktion bruges til varer, der bruger kostmetoden Gennemsnit. Funktionen fungerer på følgende måde:  

* Omkostningsregulering registreres ved at markere en post i tabellen **Indf.sted, regl. gnsn. kostpr.**, når der bogføres en værdipost.  
* Omkostninger overføres ved at anvende omkostningerne på værdiposter med en senere værdiansættelsesdato.  

### <a name="order-level"></a>Ordreniveau

Denne registreringsfunktion bruges i konverteringsscenarier, produktion og montage. Funktionen fungerer på følgende måde:  

* Omkostningsregulering registreres ved at markere ordren, når et materiale eller en ressource bogføres som forbrugt.  
* Omkostninger overføres ved at anvende omkostningerne fra materialet/komponenten på de afgangsposter, der er tilknyttet samme ordre.  

Ordreniveaufunktionen bruges til at registrere justeringer i montagebogføring. I følgende illustration vises reguleringspoststrukturen:  

![Flow af poster i justering af udgifter](media/design_details_assembly_posting_3.png "Flow af poster i justering af udgifter")  

Du kan finde flere oplysninger i [Designoplysninger: Bogføring af montageordre](design-details-assembly-order-posting.md).  

## <a name="manual-versus-automatic-cost-adjustment"></a>Manuel vs. automatisk kostregulering

Omkostningsregulering kan udføres på to måder:  

* Manuelt ved at køre kørslen **Juster kostpris - vareposter**. Du kan udføre kørslen for alle varer eller kun for bestemte varer eller varekategorier. Denne kørsel udfører en kostregulering for varerne på lageret, for hvilke en indgående transaktion er foretaget, som f.eks. et køb. For varer, der bruger kostmetoden Gennemsnit, foretager kørslen også en regulering, hvis der oprettes udgående transaktioner.  
* Automatisk, ved at justere omkostninger hver gang du bogfører en lagertransaktion, og når du er færdig med en produktionsordre. Kostregulering køres kun for den eller de specifikke varer, der er berørt af bogføringen. Dette er oprettet, når du vælger afkrydsningsfeltet **Automatisk omkostningsregulering** er markeret på siden **Lageropsætning**.  

Det er en god ide at køre automatisk kostregulering, når du bogfører, da kostpriser ofte opdateres og derfor er mere nøjagtige. Ulempen er, at databasens ydeevne kan påvirkes ved at udføre kostregulering så ofte.  

Da det er vigtigt at holde en vares kostpris opdateret, anbefales det, at du udfører kørslen **Juster kostpris - vareposter** så ofte som muligt uden for normal arbejdstid. Du kan også bruge automatisk kostregulering. Dette sikrer, at kostprisen opdateres dagligt for varer.  

Uanset om du kører omkostningsregulering manuelt eller automatisk, er reguleringsprocessen og følgerne ens. [!INCLUDE[d365fin](includes/d365fin_md.md)]beregner værdien af den indgående overflytning, og sender udgiften til en udgående transaktion, f.eks. salg eller forbrug, som er blevet udlignet med den indgående overflytning. Kostregulering opretter værdiposter, der indeholder reguleringsbeløb og beløb, der kompenserer for afrunding.  

De nye regulerings- og afrundingsværdiposter har bogføringsdatoen for den relaterede faktura. Undtagelserne er, hvis værdiposterne ligger i en lukket regnskabsperiode eller lagerperiode, eller hvis bogføringsdatoen ligger tidligere end datoen i feltet **Bogf. tilladt fra** på siden **Opsætning af Finans**. Hvis dette sker, tildeler kørslen bogføringsdato som den første dato i den næste åbne periode.  

## <a name="adjust-cost---item-entries-batch-job"></a>Kørslen Juster kostpris - vareposter

Når du udfører kørslen **Juster kostpris - vareposter**, har du mulighed for at udføre kørslen for alle varer eller kun for bestemte varer eller kategorier.  

> [!NOTE]  
> Vi anbefaler, at du altid udfører kørslen for alle varer og kun bruger filtreringsindstillingen til at begrænse afviklingstiden for kørslen eller til at rette omkostningerne for et bestemt element.  

### <a name="example"></a>Eksempel

I følgende eksempel vises, hvis du bogfører en købt vare som modtaget og faktureret den 01-01-20. Du bogfører senere den solgte vare som leveret og faktureret den 01-15-20. Derefter skal du køre kørslerne **Juster kostværdi - vareposter** og **Bogfør lagerregulering**. Der oprettes følgende poster.  

#### <a name="value-entries-1"></a>Værdiposter (1) 

|Bogføringsdato|Vareposttype|Kostbeløb (faktisk)|Bogført kostværdi|Faktureret antal|Løbenr.|  
|------------|----------------------|--------------------|------------------|-----------------|---------|  
|01-01-20|Køb|10,00|10,00|1|1|  
|01-15-20|Salg|-10,00|-10,00|-1|2|  

#### <a name="relation-entries-in-the-gl--item-ledger-relation-table-1"></a>Relationsposter i finans – relationstabel for varepost (1)

|Finansløbenr.|Værdiløbenr.|Finansjournalnr.|  
|-------------|---------------|----------------|  
|1|1|1|  
|2|1|1|  
|3|2|1|  
|4|2|1|  

#### <a name="general-ledger-entries-1"></a>Finansposter (1)

|Bogføringsdato|Finanskonto|Kontonummer (En-US Demo)|Beløb|Løbenr.|  
|------------------|------------------|---------------------------------|------------|---------------|  
|01-01-20|[Lagerkonto]|2130|10,00|1|  
|01-01-20|[Tillagte dir. omkost.konto]|7291|-10,00|2|  
|01-15-20|[Lagerkonto]|2130|-10,00|3|  
|01-15-20|[Vareforbrugskonto]|7290|10,00|4|  

Senere skal du bogføre et relateret varekøbsgebyr for 2.00 RV, der er faktureret 10-02-20. Derefter skal du køre kørslerne **Juster kostværdi - vareposter** og **Bogfør lagerregulering**. Kørslen til kostregulering justerer omkostningerne ved salget af -2,00 RV i overensstemmelse hermed, og kørslen **Bogfør lagerregulering** bogfører de nye værdiposter i finans. Resultatet er som følger.  

#### <a name="value-entries-2"></a>Værdiposter (2)  

|Bogføringsdato|Vareposttype|Kostbeløb (faktisk)|Bogført kostværdi|Faktureret antal|Regulering|Løbenr.|  
|------------|----------------------|--------------------|------------------|-----------------|----------|---------|  
|02-10-20|Køb|2.00|2.00|0|Nej|3|  
|01-15-20|Salg|-2,00|-2,00|0|Ja|4|  

#### <a name="relation-entries-in-the-gl--item-ledger-relation-table-2"></a>Relationsposter i finans – relationstabel for varepost (2)

|Finansløbenr.|Værdiløbenr.|Finansjournalnr.|  
|-------------|---------------|----------------|  
|5|3|2|  
|6|3|2|  
|7|4|2|  
|8|4|2|  

#### <a name="general-ledger-entries-2"></a>Finansposter (2)

|Bogføringsdato|Finanskonto|Kontonummer (En-US Demo)|Beløb|Løbenr.|  
|------------|-----------|------------------------|------|---------|  
|02-10-20|[Lagerkonto]|2130|2.00|5|  
|02-10-20|[Tillagte dir. omkost.konto]|7291|-2,00|6|  
|01-15-20|[Lagerkonto]|2130|-2,00|7|  
|01-15-20|[Vareforbrugskonto]|7290|2.00|8|  

## <a name="automatic-cost-adjustment"></a>Automatisk kostregulering

Hvis du vil konfigurere omkostningsregulering til at køre automatisk, når du bogfører en lagertransaktion, skal du bruge feltet **Automatisk omkostningsregulering** på siden **Opsætning af Lager**. Dette felt gør det muligt for dig at vælge, hvor langt tilbage i tiden fra den aktuelle arbejdsdato, du ønsker, at automatisk kostregulering skal udføres. Der findes følgende indstillinger.  

|Indstilling|Beskrivelse|
|------|-----------|
|Aldrig|Kostpriser reguleres ikke, når du bogfører.|  
|Dag|Kostpriser reguleres, hvis bogføringen foretages senest én dag fra arbejdsdatoen.|  
|Uge|Kostpriser reguleres, hvis bogføringen foretages senest én uge fra arbejdsdatoen.|  
|Måned|Kostpriser reguleres, hvis bogføringen foretages senest én måned fra arbejdsdatoen.|  
|Kvartal|Kostpriser reguleres, hvis bogføringen foretages senest ét kvartal fra arbejdsdatoen.|  
|År|Kostpriser reguleres, hvis bogføringen foretages senest ét år fra arbejdsdatoen.|  
|Altid|Kostpriser reguleres altid, når du bogfører, uanset bogføringsdatoen.|  

De valg, som du foretager i feltet **Automatisk omkostningsregulering**, er vigtige for ydeevne og nøjagtigheden af dine omkostninger. Kortere tidsperioder, som **Dag** eller **Uge**, påvirker systemets ydeevne mindre, fordi de giver de strengere krav, som kun omkostninger, der er bogført i det sidste døgn eller den sidste uge, kan justeres automatisk. Det betyder, at den automatiske kostregulering ikke kører så ofte, og derfor påvirkes systemets ydeevne mindre. Det betyder også, at kostpriser kan være mindre nøjagtige.  

### <a name="example"></a>Eksempel

Følgende eksempel viser et scenario for automatisk justering af kostpris:  

* Den 10 januar bogfører du en købt vare som modtaget og faktureret.  
* Du bogfører en salgsordre for varen som leveret og faktureret den 15. januar.
* Du modtager en faktura for fragttillæg på det oprindelige køb den 5. februar. Du bogfører dette fragtgebyr, udligner det på den oprindelige købsfaktura, hvilket forøger omkostningerne på det oprindelige køb.  

Hvis du har oprettet den automatiske kostregulering for posteringer, der forekommer inden for en måned eller et kvartal fra den aktuelle arbejdsdato, kører automatisk kostregulering, og omkostningerne ved købet videresendes til salg.  

Hvis du har oprettet den automatiske kostregulering for posteringer, der forekommer inden for en dag eller en uge fra den aktuelle arbejdsdato, kører automatisk kostregulering ikke, og omkostningerne ved købet videresendes ikke til salg, før du kører kørslen **Juster kostpris - vareposter**.  

## <a name="see-also"></a>Se også

[Regulere varepriser](inventory-how-adjust-item-costs.md)  
[Designoplysninger: Lagerkostmetode](design-details-inventory-costing.md)  
[Designoplysninger: Afstemning med Finans](design-details-reconciliation-with-the-general-ledger.md)  
[Designoplysninger: Varekladde](design-details-inventory-posting.md)  
[Designoplysninger: Afvigelse](design-details-variance.md)  
[Designoplysninger: Bogføring af montageordre](design-details-assembly-order-posting.md)  
[Designoplysninger: Bogføring af produktionsordre](design-details-production-order-posting.md)  
[Administrere lageromkostninger](finance-manage-inventory-costs.md)  
[Finans](finance.md)  
[Arbejde med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)  
