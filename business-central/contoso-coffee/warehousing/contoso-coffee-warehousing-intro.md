---
title: Introduktion til Contoso Coffee
description: 'Oversigt over scenarier for, hvordan oplysninger om demonstrationsdata for Contoso Coffee kan hjælpe dig med at lære, hvordan du bruger lagerfunktionerne i Business central.'
ms.date: 04/01/2022
ms.topic: article
ms.service: dynamics365-business-central
ms.search.form: 4764
author: brentholtorf
ms.author: bholtorf
---

# <a name="introduction-to-contoso-coffee-warehousing"></a>Introduktion til Contoso Coffee-lagersted

Contoso Coffee er en fiktiv virksomhed, der producerer forbruger- og kommercielle kaffemaskine. Apps **Contoso Coffee** til Business Central tilføjer demodata, som du kan bruge til at lære, hvordan du bruger lagerfunktionerne i Business central. Du kan konfigurere logistikfunktioner på forskellige måder i [oversigten over forskellige konfigurationsindstillinger](../../design-details-warehouse-management.md#overview-of-different-configuration-options).

Appen indeholder tre lokationer, der er optimeret til forskellige scenarier:

- **SØLV**  

  Denne lokation er konfigureret til at bruge placeringer. Den kan nemt konfigureres til at understøtte almindelig eller avanceret. 

- **GUL**  

  Denne lokation bruger den avancerede Lageropsætning, men bruger ikke placeringer. Den kan omkonfigureres til at understøtte grundlæggende konfigurationer.

- **HVID**  

  Denne lokation bruger den avancerede lager konfiguration med styret læg-på-lager og pluk, som gør det muligt at have mere avancerede regler for, hvordan varer bevæger sig på hele lagerstedet.

## <a name="set-up-contoso-coffee-warehousing-data"></a>Opsætning af Contoso Coffee-lagerstedsdata

[!INCLUDE [contoso-coffee-app-install](../contoso-coffee-app-install.md)].

Når de relevante apps er installeret, skal du gå til siden [Contoso-demoværktøj](https://businesscentral.dynamics.com/?page=5194) i [!INCLUDE [prod_short](../../includes/prod_short.md)], vælge linjen *Lagermodul*, og brug handlingen **Konfigurer** til at forberede modulerne. Følgende tabeller beskriver indstillingerne:  

|Felt  |Beskrivelse  |
|---------|---------|
|**Placeringsinterval**  |Placeringen til brug af grundlæggende lokationsscenarier.|
|**Placering avanceret**  |Placeringen til brug af enkle logistikscenarier.|
|**Placeringsstyret læg-på-lager og pluk**  |Placeringen til brug af avancerede logistikscenarier.|
|**Placering i transit**  |Den lokation, der skal bruges til transitlokationsplaceringen i overførselsscenarier.|
|**Debitornr.**  |Den kunde, der skal bruges til de grundlæggende og simple scenarier i salgsoperationer.|
|**Kreditornr. (køb)**  |Den kreditor, der skal bruges til alle scenarier i forbindelse med indkøb.|
|**Varenr. 1**  |Hovedvaren, der skal bruges til alle scenarier.|
|**Varenr. 2**  |Den ekstra vare, der skal bruges til alle scenarier.|
|**Varenr. 3**  |Varen med sporing.|

Når du er færdig, skal du vælge handlingen **Opret demodata**. Det tager nogle få minutter at føje dataene til den underliggende database, men så er du klar til at køre forskellige scenarier.  

> [!IMPORTANT]
> Hvis du kører scenarierne, kan det være en god ide at kontrollere, at brugeren er blevet tilføjet som for bestemte placeringer. Du kan finde flere oplysninger i [Definere lagermedarbejdere](../../warehouse-how-to-set-up-warehouse-employees.md).

## <a name="scenarios"></a>Eksempler

Contoso Coffee-lagerdemodata understøtter i øjeblikket følgende scenarier for test og træning:

1.  [Gennemgang af indgående og udgående flow i grundlæggende opsætning af lagersted](warehouse-basic-flow-putaway-pick.md)
2.  [Gennemgang af indgående og udgående flow i blandet opsætning af lagersted](warehouse-mixed-flow-receive-pick-ship.md)
3.  [Gennemgang af indgående og udgående flow i avanceret opsætning af lagersted med Styret læg-på-lager og pluk](warehouse-directed-flow.md)

Læs trinene for hvert scenarie i den relevante artikel.  

## <a name="see-also"></a>Se også

[Konfigurere lager](../../inventory-setup-inventory.md) 
[Sådan opsættes lokationer](../../inventory-how-setup-locations.md) 
[Lagersted](../../warehouse-manage-warehouse.md) 
[Designdetaljer](../../design-details-warehouse-overview.md) 
