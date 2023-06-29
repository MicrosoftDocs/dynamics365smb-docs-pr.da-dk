---
title: Oversigt over opgaver til opsætning af indkøb
description: 'Beskriver de opgaver, der definerer virksomhedens indkøbspolitikker, og som du bruger til at oprette dine indkøbsprocesser.'
author: SorenGP
ms.topic: overview
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 'procurement, supply, vendor order'
ms.search.form: '175, 176, 177, 178, 456, 460, 5727, 5729'
ms.date: 08/30/2022
ms.author: edupont
---
# <a name="setting-up-purchasing"></a><a name="setting-up-purchasing"></a>Opsætning af indkøb

Før du kan administrere købsprocesser, skal du konfigurere de regler og værdier, der definerer virksomhedens købspolitikker.

Du skal angive den generelle opsætning på siden **køb & Købsopsætning**, som typisk gøres én gang ved den første implementering. Få mere at vide i følgende afsnit, [Opsætning af køb og skyldige beløn](#purchases-and-payables-setup).

En særskilt sæt opgaver i forbindelse med registrering af nye kreditorer er at registrere en særlig pris eller rabataftaler, du indgår med hver kreditorer.

Den finansrelaterede købsopsætning, som betalingsmetoder og valutaer, dækkes i afsnittet Konfigurere finans. Flere oplysninger i [Konfigurere finans](finance-setup-finance.md). På samme måde kan du finde lagerrelaterede købsopsætninger, f. eks. enheder og varesporingskoder, i afsnittet [Lageropsætning](inventory-setup-inventory.md).

## <a name="purchases-and-payables-setup"></a><a name="purchases-and-payables-setup"></a>Opsætning af køb og skyldige beløb

Før du arbejder med køb, skal du på siden **Køb og skyldige beløb** angive, hvordan købsværdier bogføres og nummerserierne, der bruges til kreditorer og købsdokumenter.

### <a name="general-settings"></a><a name="general-settings"></a>Generelle indstillinger

I oversigtspanelet **Generelt** angiver du indstillinger for, hvordan der skal beregnes og bogføres rabatter, og om fakturaer skal afrundes. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)].

Nogle felter kræver særlig opmærksomhed, f.eks. feltet **Beregn fakturarabat pr. moms-id**, som angiver, om fakturarabatten beregnes i henhold til moms-id'et eller fakturatotalen. Flere oplysninger [Sådan kombineres momsbogføringsgrupper i momsbogføringsopsætninger](finance-setup-vat.md#combine-vat-posting-groups-in-vat-posting-setups).

På samme måde kan der opstå mindre afrundingsdifferencer i feltet **Udlign. mellem valutaer**, når poster i forskellige valutaer udlignes med hinanden. Flere oplysninger [Aktivere anvendelsen af finansposter i forskellige valutaer](finance-how-enable-application-ledger-entries-different-currencies.md).

Nogle felter ændrer også deres funktionsmåde eller afhænger af, hvordan andre felter er angivet. Funktionen **Kontroller forudbetaling ved bogføring** påvirkes f.eks. af, hvordan feltet **Frekvens for automatisk opdatering af forudbetaling** er indstillet til at kontrollere, om der er ventende forudbetalinger.

Læse oplysninger om feltet [**Eksternt bilagsnr. obl.**](#external-document-number) og præcise beløb til feltet [**Obl. præcis kostprisudligning**](#exact-cost-reversing) herunder.

### <a name="number-series-settings"></a><a name="number-series-settings"></a>Indstillinger for nummerserier

I oversigtspanelet **Nummerserier** angiver du den de entydige identifikationskoder, som skal bruges til kreditorer, fakturaer og andre købsdokumenter. Nummereringen er ikke kun vigtig ved interne processer, men det kan også være nødvendigt at følge lokale forskrifter. Det kan være værd at overveje at oprette serier på siden **Nummerserie** i stedet for at oprette nye fra **Købsopsætning**. Flere oplysninger i [Oprette nummerserie](ui-create-number-series.md).

## <a name="external-document-number"></a><a name="external-document-number"></a>Eksterne bilagsnumre

[!INCLUDE [ext-doc-no-purch](includes/ext-doc-no-purch.md)]

## <a name="exact-cost-reversing"></a><a name="exact-cost-reversing"></a>Præcis kostprisudligning

Den **præcise funktion til tilbageførsel af kostpris** hjælper med at sikre, at returvarer værdiansættes til den samme omkostning, som da de oprindeligt blev trukket fra lageret ved hjælp af en fast udligning i stedet for en kostmetode for FIFO eller første, første og anden. Få mere at vide i sektionen [Designdetaljer: fast udligning](design-details-item-application.md#fixed-application). Hvis der senere føjes en supplerende pris til det oprindelige køb, opdateres værdien af købsreturvaren tilsvarende automatisk.

Med funktionen aktiveret kan returtransaktionen kun bogføres med angivelse af varepostnummeret i feltet **Udl.varepostløbenr.** på ordrelinjen for købsreturvaren. Feltet vises ikke som standard på oversigtspanelet **Linjer**. Få mere at vide om, hvordan du føjer felter til sider i sektionen [Tilpasning af arbejdsområde](ui-personalization-user.md#to-start-personalizing-a-page-through-the-personalizing-banner).

[!INCLUDE[local-functionality](includes/local-functionality.md)]

## <a name="more-purchasing-setups"></a><a name="more-purchasing-setups"></a>Flere indkøbsopsætninger

| Til | Se |
| --- | --- |
| Opret et kreditorkort for hver kreditor, du køber fra. |[Registrere nye kreditorer](purchasing-how-register-new-vendors.md) |
| Prioritere kreditorer. |[Tildele kreditorer prioritet](purchasing-how-prioritize-vendors.md) |
| Indtaste bankkontooplysninger, herunder IBAN-og SWIFT-koder, på kreditorkortet. | [Konfigurere kreditorbankkonti](purchasing-how-set-up-vendors-bank-accounts.md) |
| Oprette indkøbere, tildele dem kreditorer og koder til sporingsstatistik. |[Oprette indkøbere](purchasing-how-setup-purchasers.md) |
| Angiv de forskellige rabatter og specialpriser, som kreditorer yder dig, afhængigt af vare, antal og/eller dato. |[Registrer købspris, rabat og betalingsaftaler](purchasing-how-record-purchase-price-discount-payment-agreements.md) |
| Definere, hvad du betaler for varer og tjenester, som købes af din virksomhed.  | [Konfigurere priser og rabatter](across-prices-and-discounts.md) |
| Opret standardlinjer, der skal indsættes i gentagende købsdokumenter. | [Konfigurer gentagne købslinjer](purchasing-how-work-recurring-purchase-lines.md) |
| Opret sekvens af opgaver for at forbinde processer, der udføres af forskellige brugere, f. eks. anmodning om og godkendelse af købsordrer. | [Konfigurer købsgodkendelsesworkflows](across-set-up-workflows.md) |
| Administrere forretningsaktiviteter med dine leverandører, importere modtagne fakturadokumenter og registrere nye leverandører ved hjælp af Outlook-e-mailklienten. | [Konfigurer Business Central-tilføjelsesprogram til Outlook](admin-outlook.md) |
| Gennemgå udgifts kvitteringer, konverter papir og elektroniske dokumenter til kladdelinjer, og digitalize papir fakturaer fra kreditorer. | [Opsætning af indgående bilag](across-how-setup-income-documents.md) |
| Angiv standardrapporter, der skal bruges til forskellige dokumenttyper. |[Rapportvalg i Business Central](across-report-selections.md)|
|Angive, om brugere må bogføre købsfakturaer, og om de skal bogføre dem sammen med en forsendelse. |[Definere politik til bogføring af faktura for brugere](admin-setup-invoice-posting-policy.md)|

## <a name="see-related-training-at-microsoft-learn"></a><a name="see-related-training-at-microsoft-learn"></a>Se relateret træning på [Microsoft Learn](/learn/paths/trade-get-started-dynamics-365-business-central/).

## <a name="see-also"></a><a name="see-also"></a>Se også

[Køb](purchasing-manage-purchasing.md)  
[Konfigurer oversigt](setup.md)  
[Arbejd med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)

[!INCLUDE[footer-include](includes/footer-banner.md)]
