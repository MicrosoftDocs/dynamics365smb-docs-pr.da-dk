---
title: Introduktion til demonstrationsdata for Contoso Coffee
description: Oversigt over scenarier for, hvordan oplysninger om demonstrationsdata for Contoso Coffee kan hjælpe dig med at lære, hvordan du bruger produktionsfunktionerne i Business central.
ms.date: 04/01/2022
ms.topic: article
ms.service: dynamics365-business-central
ms.search.form: 4760
author: edupont04
ms.author: andreipa
ms.openlocfilehash: 41dac60578399e09b9a67ac5747d48648a872f9c
ms.sourcegitcommit: 9bba11d474e21711cc8e2afefee8efb473170707
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 11/18/2022
ms.locfileid: "9788216"
---
# <a name="introduction-to-contoso-coffee-demo-data"></a>Introduktion til demonstrationsdata for Contoso Coffee

Contoso Coffee er en fiktiv virksomhed, der producerer forbruger- og kommercielle kaffemaskine. Apps **Contoso Coffee** til Business Central tilføjer demodata, som du kan bruge til at lære, hvordan du bruger produktionsfunktionerne i Business central.  

Appen indeholder fire produkter, der er optimeret til forskellige scenarier:

- **SP-SCM1009 Airpot**  

  Dette produkt er en stykliste med a halvfabrikata, **Rute**. Bruges til at demonstrere standardproduktionsflowet. Det er konfigureret med alternative ruter, som du kan bruge til at demonstrere forskellige scenarier, der involverer underleverandører. Omkostningsmetoden er *Standard*.  

- **SP-SCM1011 Airpot Duo**  

  Produktet kræver varesporing og har en komponent, der også kræver varesporing. Omkostningsmetoden er *Specifik*.  

- **SP-SCM1004 Autodrip**  

  Dette produkt er en stykliste med a halvfabrikata, **Rute**. Det anbefales at vise de forskellige trækmetoder til både komponenter og operationer. Omkostningsmetoden er *Standard*.

- **SP-SCM1006 AutoDripLite**

  Produktet har tre varianter og tre styklister, der kan tildeles til lagervarer. Produktet bruger funktionen fantomstykliste begreb. Omkostningsmetoden er *Standard*.

Produktionsaktiviteterne i alle scenarier bruger *NORTH*-lokationen.  

> [!IMPORTANT]
> Før du udfører et af scenarierne for Contoso Coffee, skal du bogføre alle varekladdelinjer med primosaldi. Du kan finde flere krav i afsnittet [Opsætning af Contoso Coffee-data](#set-up-contoso-coffee-data).

## <a name="set-up-contoso-coffee-data"></a>Opsætning af Contoso Coffee-data

Hvis du vil bruge demonstrationsdataene fra Contoso Coffee, skal du installere to apps i det relevante regnskab i [!INCLUDE [prod_short](../includes/prod_short.md)]:  

- **Demonstrationsdata for Contoso Coffee**  

    Denne app leverer demonstrationsdata til basisprogrammet.  
- **Demonstrationsdata for Contoso Coffee (lande-id)**  

    Denne app tilføjer landespecifik indhold oven på basisprogrammet.

Føj apps til et tomt firma i et betalt abonnement eller som en del af et prøveabonnement. Du kan f. eks. oprette en ny virksomhed uden eksempeldata fra guiden **Opret ny virksomhed**, som du kan åbne fra **virksomhedslisten**. Tilføj derefter apps fra [markedspladsen](../ui-extensions-install-uninstall.md#install), hvis de ikke allerede er angivet på siden **Udvidelsesstyring**.  

Når de relevante apps er installeret, skal du gå til [Contoso Coffee-demodata](https://businesscentral.dynamics.com/?page=4760)-siden i [!INCLUDE [prod_short](../includes/prod_short.md)] og ændre standardindstillingerne, så de passer til dine behov. Følgende tabeller beskriver indstillingerne:  

|Felt  |Beskrivlse  |
|---------|---------|
|**Startår** |Angiver det første år, du vil bruge til demonstrationsdataene fra Contoso Coffee. Afhængigt af virksomhedens opsætning er året enten et kalenderår eller et regnskabsår.|
|**Produktionssted** |Angiver det lagersted, som du vil bruge til produktionshandlinger. Standardindstillingen er *NORTH*, men du kan ændre den efter behov.|
|**Virksomhedstype**    |Angiver, om det aktuelle regnskab skal rapportere moms eller moms. |
|**Indlands – Virksomhedsbogføringsgruppe**|Angiver en forretnings kode for indenlandske debitorer og kreditorer. Forretnings koderne bruges, når transaktionerne bogføres. |
|**Kapacitet – generel produktbogføringsgruppe**    |Angiver en kode for varer eller ressourcer, der skal bruges til bogføring af kapacitet.|
|**Detail – Generel produktbogføringsgruppe**    |Angiver en kode for varer eller ressourcer, der skal bruges til bogføring af detail.|
|**Råmaterialer – generel produktbogføringsgruppe**    |Angiver en kode for varer eller ressourcer, der skal bruges til bogføring af råmateriale. |
|**Basis momskode**    |Angiver en eksisterende momsproduktgruppe, der skal bruges til varer.|
|**Færdig kode**    |Angiver en eksisterende momsproduktgruppe, der skal bruges til færdige varer.|
|**Prisfaktor**     |Angiver en faktor, der skal omregnes til en pris fra USD/EUR til den lokale valuta. *1* betyder, at prisen er det samme beløb i alle valutaer. Der bruges et højere nummer til at beregne prisen i den lokale valuta. |
|**Afrundingspræcision**  |Definerer, hvordan beregnede forbrugsmængder skal afrundes, når de indtastes på forbrugskladdelinjer. Mængder under 0,5 nedrundes. Mængder, der er lig med eller større end 0.5 rundes op.|

Når du er færdig, skal du vælge handlingen **Opret demodata**. Det tager nogle få minutter at føje dataene til den underliggende database, men så er du klar til at køre forskellige scenarier.  

## <a name="scenarios"></a>Eksempler

Contoso Coffee-demodata understøtter i øjeblikket følgende scenarier for test og træning:

1. [Opret en ny produktionsstykliste og styklisteversion](create-new-production-bom-version.md)  
2. [Opret en ny rute](create-new-routing.md)  
3. [Opret en ny fastlagt produktionsordre og ændre den](create-firm-planned-production-order-change.md)  
4. [Kombinere automatisk og manuel træk](combine-automatic-manual-flushing.md)  
5. [Bruge Ordreplanlægning til at oprette og reservere levering](order-planning-create-reserve-supply.md)  
6. [Konfigurere og behandle en underleverandør operation](set-up-process-subcontracting-operation.md)  
7. [Opret ny kapacitet](set-up-new-capacity.md)  
8. [Prognosebehov for varevarianter med forskellige styklister tildelt](variants.md)  

Læs trinene for hvert scenarie i den relevante artikel.  

> [!IMPORTANT]
> Denne gennemgang kræver, at brugeroplevelsen er sat til *Premium* på siden **firmaoplysninger**.

## <a name="see-also"></a>Se også

[Produktion](../production-manage-manufacturing.md)  
[Produktionsrapporter og analyser i Business Central](../production-reports.md)  
