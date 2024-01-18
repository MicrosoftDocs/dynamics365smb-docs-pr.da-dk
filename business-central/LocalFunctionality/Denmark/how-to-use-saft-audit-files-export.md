---
title: Eksportere SAF-T-overvågnings filformatet i Danmark
description: 'I denne artikel forklares det, hvordan du eksporterer alle nødvendige data ifølge formatet SAF-T i Danmark.'
author: altotovi
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: null
ms.search.form: '5264, 5266, 5267, 5270,'
ms.date: 12/13/2023
ms.author: altotovi
---

# <a name="export-the-saf-t-audit-file-format-in-denmark"></a>Eksportere SAF-T-overvågnings filformatet i Danmark

Du kan eksportere alle obligatoriske data, der er obligatoriske, i overensstemmelse med standardrevisionsfilen til Skatformatet (SAF-T) i Danmark. SAF-T er en international standard for elektronisk udveksling af pålidelige regnskabsdata fra organisationer til nationale skattemyndigheder eller eksterne revisorer. Danske skattemyndigheder bruger organisationen som standardfilformat for økonomisk samarbejde og udvikling (OECD) standard SAF-T som standardfilformat. Der findes imidlertid nogle Danmark-specifikke felter i denne eksportfil.  

## <a name="exporting-audit-files"></a>Eksportere revisionsfiler

Eksport af SAF-T-overvågningsfilformatet i den danske lokalisering er baseret på **Eksport af revisionsfiler** i Microsoft-app. Få flere oplysninger i [Eksport af revisionsfil](../../finance-how-to-export-audit-files.md)  

Du kan finde flere oplysninger i [Danske landespecifikke funktioner](denmark-local-functionality.md).

## <a name="import-audit-files"></a>Importer revisionsfiler

Du kan importere SAF-T fil i dansk lokalisering. Det kan du gøre ved at benytte følgende fremgangsmåde. 

1. Vælg søgeknappen ![Forstørrelsesglas-knappen, der åbner funktionen Fortæl mig.](../../media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig"), angiv **Importer SAF-T-filer**, og vælg derefter det relaterede link. 
2. På siden **Importer SAF-T-filer** skal du vælge **Importer SAF-T-fil**.   
3. På den vedhæftede side uploader du SAF-T-filen ved at bruge træk og slip eller ved at browse til den fil, du vil importere.  

Når du er færdig med at importere de eksterne SAF-T-filer, vises resultatet på **Importer SAF-T-filer**-listesiden. 

Fra siden **Importér SAF-T-filer** kan du finde detaljer om importerede SAF-T-filer med det specifikke navn og datoen, når filen er uploadet. 

> [!NOTE]
> Når du importerer SAF-T-filen, skal du huske på, at der ikke er yderligere handlinger i systemet baseret på disse oplysninger. Dynamics 365 Business Central kan kun beholde listen over uploadede filer. 

## <a name="see-also"></a>Se også
[Økonomistyring](../../finance.md)  
[Forstå Finans og Kontoplan](../../finance-general-ledger.md)  
[Arbejde med dimensioner](../../finance-dimensions.md)  


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
