---
title: Lager- og lagerstedrapporter og -analyse
description: 'Se, hvilke samling rapporter og analyser der er tilgængelige i standardversionen af Business Central, så du kan holde styr på virksomheden.'
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bholtorf
ms.topic: conceptual
ms.search.keywords: reporting
ms.search.form: 'Report_707, Report_716, Report_813, Report_1001, Report_5807, Report_5808, Report_5809, Report_7313, Report_7319, Report_7320'
ms.date: 03/21/2024
ms.custom: bap-template
ms.service: dynamics-365-business-central
---
# <a name="inventory-and-warehouse-reports-and-analytics"></a>Lager- og lagerstedrapporter og -analyse

Lagerbeholdning og lagerstedsrapportering i [!INCLUDE [prod_short](includes/prod_short.md)] giver lagerbeholdning og ansatte at få indsigt i og hente statistikker om aktuelle og tidligere lagerbeholdning og lagerstedsaktiviteter.  

## <a name="reports"></a>Rapporter

[!INCLUDE [inventory_WMS_reports](includes/inventory-WMS-reports-include.md)]

## <a name="tasks"></a>Opgaver

I følgende artikler beskrives nogle af de vigtigste opgaver i forbindelse med analyse af virksomhedens tilstand:

* [Oprette analyserapporter](bi-how-create-analysis-views-reports.md)  
* [Vise varer, der er disponible](inventory-how-availability-overview.md)

## <a name="print-and-scan-barcodes"></a>Udskriv og scan stregkoder

Brug af stregkoder kan hjælpe med at strømline dine indgående, udgående og interne lagerprocesser. 

[!INCLUDE [barcode-mobile-app](includes/barcode-mobile-app.md)]

Når du har installeret appen, kan du bruge handlingen **Udskriv etiket** til at udskrive 1D- og 2D-stregkoder fra siderne i følgende tabel.

|Side  |Feltværdier stregkoder kan indeholde  |
|---------|---------|
|Varer, varekort     |Varenummer, beskrivelse og GTIN         |
|Varereferenceliste, Varereference     |Varenr., Beskrivelse, Enhed og Referencenr.         |
|Lotnr. Oplysningsoversigt, lotnr. Etiket     |Varenummer, beskrivelse og lotnummer       |
|SN-etiket     |Nummer, beskrivelse og serienummer         |

> [!NOTE]
> Nogle printere og stregkode-/QR-kodeformater kræver en specifik implementering. Du skal muligvis overføre en anden Word-skabelon eller klone rapporten for at oprette din egen tilpassede version.


## <a name="explore-inventory-reports-with-report-explorer"></a>Udforsk lagerrapporter med Stifinder

Hvis du vil have et overblik over de rapporter, der er tilgængelige for lageret, kan du vælge **Alle rapporter** på startsiden. Denne handling åbner Rollestifinder, som filtreres til funktionerne i indstillingen **Rapport og analyse**. Under overskriften **Salg og marketing** skal du vælge **Udforsk**.

:::image type="content" source="media/report-explorer-sales.png" alt-text="Eksempel på rapporter om økonomirollecenteret." lightbox="media/report-explorer-sales.png":::

Flere oplysninger i [Søg efter rapporter med Rollestifinder](ui-role-explorer.md).


## <a name="see-also"></a>Se også

[Ad hoc-analyse af lagerdata](ad-hoc-analysis-inventory.md)  
[Oversigt over lageranalyser](inventory-analytics-overview.md)   
[Opsætning af lagerbeholdning](inventory-setup-inventory.md)  
[Lagerbeholdning](inventory-manage-inventory.md)  
[Sådan konfigureres Warehouse Management](warehouse-setup-warehouse.md)  
[Oversigt over logistik](design-details-warehouse-management.md)

[!INCLUDE[footer-include](includes/footer-banner.md)]
