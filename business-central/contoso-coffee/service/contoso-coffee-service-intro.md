---
title: Introduktion til Contoso Coffee-servicestyring
description: Denne artikel introducerer dig til Consoso Coffee demonstrationsdata for servicestyring.
author: andreipanko
ms.author: andreipa
ms.topic: how-to
ms.date: 11/27/2023
ms.custom: bap-template
ms.service: dynamics-365-business-central
---

# <a name="introduction-to-contoso-coffee-service-management"></a>Introduktion til Contoso Coffee-servicestyring

Contoso Coffee er en fiktiv virksomhed, der producerer forbruger- og kommercielle kaffemaskine. Apps **Contoso Coffee** til Business Central tilføjer demodata, som du kan bruge til at lære, hvordan du bruger servicestyringsfunktionerne i Business central.

Denne app indeholder flere elementer, der bruges til de vigtigste gennemgange:

- Ressourcer med tildelte færdigheder
- varer konfigureres til at oprette serviceartikler
- Udlånte varer

> [!IMPORTANT]
> Før du udfører et af scenarierne for Contoso Coffee, skal du bogføre alle varekladdelinjer med primosaldi. Du kan finde flere krav i afsnittet [Opsætning af Contoso Coffee-data](#set-up-contoso-coffee-service-management-data).
>
> 
## <a name="set-up-contoso-coffee-service-management-data"></a>Opsætning af Contoso Coffee-servicestyringsdata

[!INCLUDE [contoso-coffee-app-install](../../includes/contoso-coffee-app-install.md)]

Når de relevante apps er installeret, skal du gå til siden [Contoso-demoværktøj](https://businesscentral.dynamics.com/?page=5194) i [!INCLUDE [prod_short](../../includes/prod_short.md)], vælge linjen *Servicemodul*, og brug handlingen **Konfigurer** til at forberede modulerne. Følgende tabel beskriver indstillingerne:  

|Felt  |Beskrivelse  |
|---------|---------|
|**Debitornr.**  |Kunden, der skal bruge scenarier i forbindelse med salg.|
|**Kreditornr. (køb)**  |Den kreditor, der skal bruges til alle scenarier i forbindelse med indkøb.|
|**Varenr. 1**  |Den vare, der skal bruges til reparations- og vedligeholdelsesscenarier.|
|**Serviceartikel 1 Nr.**  |Elementet af typen service til brug af repear scenario.|
|**Servicevarenr. 2**  |Elementet af typen service til brug af repear scenario.|
|**Ressourcenr. 1**  |Den ressource, der skal bruges til kontraktscenarier.|
|**Ressourcenr. 2**  |Den ressource, der skal bruges til break-fix-scenarier.|
|**Service placering** |Angiver det lagersted, som du vil bruge til servicehandlinger. Standardindstillingen er *MAIN*, men du kan ændre den efter behov.|

Når du er færdig, skal du vælge handlingen **Opret demodata**. Det tager nogle få minutter at føje dataene til den underliggende database, men så er du klar til at køre forskellige scenarier.  

## <a name="scenarios"></a>Eksempler

Contoso Coffee-demodata understøtter i øjeblikket følgende servicescenarier for test og træning:

1. Oprette serviceordre for ad hoc-reparationsanmodninger, placere og modtage udlånsvarer, registrere tid og fakturere kunder med [gennemgang af serviceordrer for serviceartikler](service-basic-flow-order.md)
2. Oprette servicekontrakter, generere serviceordrer, fakturere kontraktgebyrer og allokere ressourcer med [Gennemgang af servicekontrakter for serviceartikler](service-contract-flow.md)

Læs trinene for hvert scenarie i den relevante artikel.  

> [!IMPORTANT]
> Servicegennemgangen kræver, at brugeroplevelsen er sat til **Premium** på siden **Firmaoplysninger**.


## <a name="see-also"></a>Se også

[Tjeneste](../../service-service.md)
