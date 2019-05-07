---
title: Definere omkostningssteder og omkostningsemner for kontoplanen | Microsoft Docs
description: Du kan automatisk overføre posterne udgifter og indtægter fra regnskabet til omkostningsregnskab, enten for hver bogføring til regnskab eller med et batchjob. Når du foretager overførslen, overfører systemet kun de poster, der allerede er knyttet til et omkostningssted eller et omkostningsobjekt. For at oprette en relevant overførsel skal du sikre omkostningssteder og omkostningsobjekter er korrekt defineret.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/01/2019
ms.author: sgroespe
redirect_url: finance-set-up-cost-accounting
ms.openlocfilehash: 00c0ac4a37476c2ab21ddc850e80e7abeb5eda18
ms.sourcegitcommit: bd78a5d990c9e83174da1409076c22df8b35eafd
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 03/31/2019
ms.locfileid: "923318"
---
# <a name="defining-cost-centers-and-cost-objects-for-chart-of-accounts"></a>Definition af omkostningssteder og omkostningsobjekter for kontoplanen
Du kan automatisk overføre posterne udgifter og indtægter fra regnskabet til omkostningsregnskab, enten for hver bogføring til regnskab eller med et batchjob. Når du foretager overførslen, overfører [!INCLUDE[d365fin](includes/d365fin_md.md)] kun de poster, der allerede er knyttet til et omkostningssted eller et omkostningsobjekt. For at oprette en relevant overførsel skal du sikre omkostningssteder og omkostningsobjekter er korrekt defineret.  

## <a name="defining-default-dimension-values-for-general-ledger-accounts"></a>Definere standarddimensionsværdier for finanskonti  
For hver enkelt finanskonto kan du definere standarddimensionsværdier i tabellen **Standarddimension**. Følgende eksempel viser, hvordan du definerer, at der altid skal være et omkostningssted DEPARTMENT, men aldrig et omkostningsobjekt PROJECT, når du bogfører til en finanskonto.  

|**Dimensionskode**|**Værdibogføring**|  
|------------------------------------------|-----------------------------------------|  
|Afdeling|Tvungen kode|  
|Projekt|Ingen kode|  

## <a name="defining-dimension-values-for-overhead-costs-and-direct-costs"></a>Definition af dimensionsværdier for faste og direkte omkostninger  
 Du kan overføre faste omkostninger til et omkostningssted og direkte omkostninger til et omkostningsobjekt. Følgende tabel viser den optimale kombination af dimensionsopsætningsværdierne.  

|Kopiér til|Omkostningsstedbogføring|Omkostningsobjektbogføring|  
|-----------------|-------------------------|-------------------------|  
|Omkostningssted|Tvungen kode|Ingen kode|  
|Omkostningsobjekt|Ingen kode|Tvungen kode|  

> [!NOTE]  
>  For at sikre, at det foruddefinerede omkostningssted og omkostningsemne, du har oprettet i regnskabet, automatisk overføres til omkostningsregnskab, skal du markere afkrydsningsfeltet **Kontroller finansbogføringer** på siden Konfiguration af omkostningsregnskab.  

## <a name="see-also"></a>Se også  
[Regnskab for omkostninger](finance-manage-cost-accounting.md)  
[Konfigurere omkostningsregnskab](finance-set-up-cost-accounting.md)  
[Arbejde med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)
