---
title: Introduktion til demonstrationsdata for Contoso Coffee
description: 'Oversigt over scenarier for, hvordan oplysninger om demonstrationsdata for Contoso Coffee kan hjælpe dig med at lære, hvordan du bruger funktionerne i Business central.'
author: brentholtorf
ms.author: bholtorf
ms.reviewer: andreipa
ms.date: 09/20/2023
ms.topic: article
ms.service: dynamics-365-business-central
ms.search.form: '5194,'
ms.custom: bap-template
---

# Introduktion til demonstrationsdata for Contoso Coffee

Contoso Coffee er en fiktiv virksomhed, der producerer forbruger- og kommercielle kaffemaskine. Apps **Contoso Coffee** til [!INCLUDE [prod_short](../includes/prod_short.md)] tilføjer demodata, som du kan bruge til at lære, hvordan du bruger funktionerne i [!INCLUDE [prod_short](../includes/prod_short.md)].  

## Opsætning af Contoso Coffee-data

[!INCLUDE [contoso-coffee-app-install](../includes/contoso-coffee-app-install.md)]

Når apps er installeret, skal du bruge handlingen **Konfigurer** på siden **Contoso-demoværktøj** til at forberede følgende moduler. Du kan vælge at installere alle tilgængelige data, herunder opsætnings- og produktionsdata eller kun opsætningsdata.

 - Det **fælles modul** til forberedelse af generelle indstillinger, som [!INCLUDE [prod_short](../includes/prod_short.md)] kræver. For eksempel ting som nummerserier. Bemærk, at **Fælles modul** kun indeholder supplerende data til scenarierne Lagersted, Produktion, Service. Det anbefales ikke at køre det isoleret.

Følgende tabel beskriver indstillingerne:  

|Felt  |Beskrivelse  |
|---------|---------|
|**Startår** |Angiver det første år, du vil bruge til demonstrationsdataene fra Contoso Coffee. Afhængigt af virksomhedens opsætning er året enten et kalenderår eller et regnskabsår.|
|**Landekode**|Angiver en lande/områdekode for indenlandske debitorer og kreditorer.|
|**Virksomhedstype**    |Angiver, om det aktuelle regnskab skal rapportere moms eller moms. |
|**Prisfaktor**     |Angiver en faktor, der skal omregnes til en pris fra USD/EUR til den lokale valuta. *1* betyder, at prisen er det samme beløb i alle valutaer. Der bruges et højere nummer til at beregne prisen i den lokale valuta. |
|**Nøjagtighed i afrunding**  |Angiver den nøjagtighed i afrunding, som du vil oprette demodataene med.|

 - [Produktionsmodulet](manufacturing/contoso-coffee-manufacturing-intro.md) til forberedelse til brug af [produktionsscenarierne](manufacturing/contoso-coffee-manufacturing-intro.md#scenarios)
 - [Lagerstedsmodulet](warehousing/contoso-coffee-warehousing-intro.md) til forberedelse til brug af [lagerstedsscenarierne](warehousing/contoso-coffee-warehousing-intro.md#scenarios)
 - [Tjenestemodulet](service/contoso-coffee-service-intro.md) til forberedelse til brug af [Tjenestescenarierne](service/contoso-coffee-service-intro.md#scenarios)

Når du har konfigureret de moduler, du vil afprøve, skal du vælge handlingen **Opret** for at oprette demonstrationsdata til dem.

## Se også

[Produktion](../production-manage-manufacturing.md)  
[Lagersted](../warehouse-manage-warehouse.md)  
[Tjeneste](../service-service.md)
<!-- [Projects and Jobs](../projects-manage-projects.md) -->

