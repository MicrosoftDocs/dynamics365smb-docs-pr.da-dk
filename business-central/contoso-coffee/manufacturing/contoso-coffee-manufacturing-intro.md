---
title: Introduktion til Contoso Coffee til produktion
description: 'Oversigt over scenarier for, hvordan oplysninger om demonstrationsdata for Contoso Coffee kan hjælpe dig med at lære, hvordan du bruger produktionsfunktionerne i Business central.'
ms.date: 04/01/2023
ms.topic: article
ms.service: dynamics-365-business-central
ms.search.form: '4765,'
author: brentholtorf
ms.author: bholtorf
---

# Introduktion til Contoso Coffee til produktion

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

Produktionsaktiviteterne i alle scenarier bruger *MAIN*-lokationen.  

> [!IMPORTANT]
> Før du udfører et af scenarierne for Contoso Coffee, skal du bogføre alle varekladdelinjer med primosaldi. Du kan finde flere krav i afsnittet [Opsætning af Contoso Coffee-data](#set-up-contoso-coffee-manufacturing-data).

## Opsætning af Contoso Coffee-produktionsdata

[!INCLUDE [contoso-coffee-app-install](../../includes/contoso-coffee-app-install.md)]

|Felt  |Beskrivelse  |
|---------|---------|
|**Produktionssted** |Angiver det lagersted, som du vil bruge til produktionshandlinger. Standardindstillingen er *MAIN*, men du kan ændre den efter behov.|


Når du er færdig, skal du vælge handlingen **Opret demodata**. Det tager nogle få minutter at føje dataene til den underliggende database, men så er du klar til at køre forskellige scenarier.  

## Eksempler

Contoso Coffee-produktionsdemodata understøtter i øjeblikket følgende scenarier for test og træning:

1. [Opret en ny produktionsstykliste og styklisteversion](create-new-production-bom-version.md)  
2. [Opret en ny rute](create-new-routing.md)  
3. [Oprette en ny fastlagt produktionsordre og ændre den](create-firm-planned-production-order-change.md)  
4. [Kombinere automatisk og manuel træk](combine-automatic-manual-flushing.md)  
5. [Bruge Ordreplanlægning til at oprette og reservere levering](order-planning-create-reserve-supply.md)  
6. [Konfigurere og behandle en underleverandør operation](set-up-process-subcontracting-operation.md)  
7. [Opret ny kapacitet](set-up-new-capacity.md)  
8. [Prognosebehov for varevarianter med forskellige styklister tildelt](variants.md)  

Læs trinene for hvert scenarie i den relevante artikel.  

> [!IMPORTANT]
> Denne gennemgang kræver, at brugeroplevelsen er sat til *Premium* på siden **firmaoplysninger**.

## Se også

[Produktion](../../production-manage-manufacturing.md)  
[Produktionsrapporter og analyser i Business Central](../../production-reports.md)  
