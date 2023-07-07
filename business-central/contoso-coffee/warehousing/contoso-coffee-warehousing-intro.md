---
title: Introduktion til Contoso Coffee
description: 'Oversigt over scenarier for, hvordan oplysninger om demonstrationsdata for Contoso Coffee kan hjælpe dig med at lære, hvordan du bruger lagerfunktionerne i Business central.'
ms.date: 04/01/2022
ms.topic: article
ms.service: dynamics365-business-central
ms.search.form: 4760
author: edupont04
ms.author: andreipa
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

Hvis du vil bruge demonstrationsdataene fra Contoso Coffee-lagersted, skal du installere to apps i det relevante regnskab i [!INCLUDE [prod_short](../../includes/prod_short.md)]:  

- **Demonstrationsdata for Contoso Coffee**  

    Denne app leverer demonstrationsdata til basisprogrammet.  
- **Demonstrationsdata for Contoso Coffee (lande-id)**  

    Denne app tilføjer landespecifik indhold oven på basisprogrammet.

Føj apps til et tomt firma i et betalt abonnement eller som en del af et prøveabonnement. Du kan f. eks. oprette en ny virksomhed uden eksempeldata fra guiden **Opret ny virksomhed**, som du kan åbne fra **virksomhedslisten**. Tilføj derefter apps fra [markedspladsen](../../ui-extensions-install-uninstall.md#install), hvis de ikke allerede er angivet på siden **Udvidelsesstyring**.  

Når de relevante apps er installeret, skal du gå til [Contoso Coffee-lagerstedsdemodata](https://businesscentral.dynamics.com/?page=4761)-siden i [!INCLUDE [prod_short](../../includes/prod_short.md)] og ændre standardindstillingerne, så de passer til dine behov. Følgende tabel beskriver indstillingerne:  

|Felt  |Beskrivlse  |
|---------|---------|
|**Startår** |Angiver det første år, du vil bruge til demonstrationsdataene fra Contoso Coffee. Afhængigt af virksomhedens opsætning er året enten et kalenderår eller et regnskabsår.|
|**Placeringsinterval**  |Placeringen til brug af grundlæggende lokationsscenarier.|
|**Lokationsavanceret logistik**  |Placeringen til brug af enkle logistikscenarier.|
|**Placeringsstyret læg-på-lager og pluk**  |Placeringen til brug af avancerede logistikscenarier.|
|**Placering i transit**  |Den lokation, der skal bruges til transitlokationsplaceringen i overførselsscenarier.|
|**Debitornr.**  |Den kunde, der skal bruges til de grundlæggende og simple scenarier i salgsoperationer.|
|**Kreditornr. (køb)**  |Den kreditor, der skal bruges til alle scenarier i forbindelse med indkøb.|
|**Hovedvarenr.**  |Den vare, der skal bruges til alle scenarier i forbindelse med salg.|
|**Varenr. 1**  |Hovedvaren, der skal bruges til alle scenarier.|
|**Varenr. 2**  |Den ekstra vare, der skal bruges til alle scenarier.|
|**Debitorbogføringsgruppe**|Angiver en forretningskode for indenlandske debitorer. Forretnings koderne bruges, når transaktionerne bogføres. |
|**Kunde Generel virksomhedsbogføringsgruppe**|Angiver en forretningskode for indenlandske debitorer. Forretnings koderne bruges, når transaktionerne bogføres. |
|**Kreditorbogføringsgruppe**|Angiver en forretnings kode for indenlandske debitorer og kreditorer. Forretnings koderne bruges, når transaktionerne bogføres. |
|**Kreditor Generel virksomhedsbogføringsgruppe**|Angiver en forretnings kode for indenlandske debitorer og kreditorer. Forretnings koderne bruges, når transaktionerne bogføres. |
|**Indlands – Momsvirksomhedsbogføringsgruppe**|Angiver en momsvirksomhedskode til debitorer og kreditorer til bogføring af moms, hvis moms er aktiveret.|
|**Videresalg – Varebogføringsgruppe**    |Angiver en kode for varer, der skal bruges til bogføringsvideresalg.|
|**Detail – Generel produktbogføringsgruppe**    |Angiver en kode for varer, der skal bruges til bogføringsdetail.|
|**Momsproduktbogf.gruppe**    |Angiver en momsproduktkode til varer til bogføring af moms, hvis moms er aktiveret.|
|**Prisfaktor**     |Angiver en faktor, der skal omregnes til en pris fra USD/EUR til den lokale valuta. *1* betyder, at prisen er det samme beløb i alle valutaer. Der bruges et højere nummer til at beregne prisen i den lokale valuta. |
|**Afrundingspræcision**  |Definerer, hvordan beregnede forbrugsmængder skal afrundes, når de indtastes på forbrugskladdelinjer. Mængder under 0,5 nedrundes. Mængder, der er lig med eller større end 0.5 rundes op.|

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
