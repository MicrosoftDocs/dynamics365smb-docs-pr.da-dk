---
title: Eksportér regnskabsdata til Regnskab Basis i Danmark
description: 'Denne artikel beskriver, hvordan du overfører en CSV-fil (kommasepareret), der indeholder regnskabsdata til Regnskab Basis i Danmark.'
author: altotovi
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: null
ms.search.form: '5264, 5266, 5267, 5270,'
ms.date: 08/23/2023
ms.author: altotovi
ms.service: dynamics-365-business-central
---

# Eksportér regnskabsdata til Regnskab Basis i Danmark

Integration af Microsoft Dynamics 365 Business Central med CSV-filer (kommaseparerede værdier) kræves af den danske bogholderilovgivning Regnskab Basis og markerer en pivotal avance i Økonomistyring. Denne strømlinede proces gør det muligt for din virksomhed at importere store datasæt uden problemer og dermed øge præcisionen og effektiviteten.

I denne artikel forklares den problemfri CSV-overførselsproces i Regnskab Basis og dens indflydelse på Danmarks økonomi. Du kan eksportere alle påkrævede data som en CSV-fil i henhold til de danske krav til Regnskab Basis. Før du begynder, skal du installere Microsoft-app'en **Udvidelse af revisionsfiler** og tilknytte finanskonti (GL) med standardkontoplanen. Du kan finde flere oplysninger om denne proces i [Standardkontoplan i Danmark](how-to-set-up-standard-coa.md).

## Eksportér regnskabsdata til Regnskab Basis 

1. Vælg søgeknappen ![Forstørrelsesglas-knappen, der åbner funktionen Fortæl mig.](../../media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig"), angiv **RB-regnskabsfil**, og vælg derefter det relaterede link.
2. På siden **RB-regnskabsfil** i oversigtspanelet **Tilknytningsheader** skal du i feltet **Vælg tilknytningsheader, der skal bruges til eksport**, angive koden for tilknytningen til den standardkontoplan, du vil bruge.
3. På oversigtspanelet **Periode for eksport af regnskabsfil** angiver systemet standardværdier i felterne **Startdato** og **Slutdato**, afhængigt af den tilknytning, du bruger. Du kan opdatere værdierne efter behov.
4. I feltet **Resultatopgørelsesbeløb** skal du angive den beløbstype, du vil bruge. Standardværdien er **Netto ændring**.
5. I feltet **Balancebeløb** skal du angive den beløbstype, du vil bruge. Standardværdien er **Saldo til dato**.
6. Vælg **Generer fil**, når du er færdig med opsætningen. Der genereres en. csv-fil for **Beløb ved hjælp af beregningsmetoder**, **finanskonti, der er tilknyttet** og **Start-og slutdatoer**.
7. Når filen er genereret, skal den overføres til den officielle tjeneste manuelt.

Du kan finde flere oplysninger i [Danske landespecifikke funktioner](denmark-local-functionality.md).

## Se også

[Økonomistyring](../../finance.md)  
[Forstå Finans og Kontoplan](../../finance-general-ledger.md)  
[Arbejde med dimensioner](../../finance-dimensions.md)  

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
