---
title: "Behandle indgående bilag | Microsoft Docs"
description: "Når du vil registrere et eksternt bilag, f.eks. en PDF-fil, i Dynamics 365 for Financials, skal du først oprette eller fuldføre en indgående bilagsrecord."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: electronic document, e-invoice, incoming document, OCR, ecommerce, document exchange, import invoice
ms.date: 06/02/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 81636fc2e661bd9b07c54da1cd5d0d27e30d01a2
ms.openlocfilehash: b4d344c52bf6f10d00f2157fbdb45903402f6c55
ms.contentlocale: da-dk
ms.lasthandoff: 09/22/2017

---
# <a name="processing-incoming-documents"></a>Behandle indgående bilag
Når du vil registrere et eksternt dokument i [!INCLUDE[d365fin](includes/d365fin_md.md)], skal du først oprette eller fuldføre en indgående dokumentpost. Du kan gøre dette manuelt, eller du kan tage et billede af det eksterne dokument og derefter oprette den indgående dokumentpost med billedfilen vedhæftet.

Fra PDF-filer eller billedfiler, som du modtager fra dine handelspartnere, kan du få en ekstern OCR-tjeneste (Optical Character Recognition) til at oprette elektroniske dokumenter, der kan konverteres til dokumentposter i [!INCLUDE[d365fin](includes/d365fin_md.md)]. F.eks. når du modtager en faktura i PDF-format fra en leverandør, kan du sende den til tjenesten OCR fra vinduet **Indgående bilag**. Du kan også vælge at sende filen til OCR-tjenesten via mail. Når du får det elektroniske dokument retur, oprettes der automatisk en relateret indgående dokumentpost. Efter nogle sekunder får du filen tilbage fra OCR-tjenesten som en elektronisk faktura, der kan konverteres til en købsfaktura til kreditoren.

| Hvis du vil | Se |
| --- | --- |
| Opret indgående dokumentposter manuelt eller automatisk ved at tage et billede af en papirkvittering, f.eks. |[Fremgangsmåde: Oprette indgående dokumentposter](across-how-create-income-document-records.md) |
| Bruge en OCR-tjeneste til at konvertere PDF- og billedfiler til elektroniske dokumenter, der igen kan konverteres til købsfakturaer i [!INCLUDE[d365fin](includes/d365fin_md.md)] f.eks. Lær OCR-tjenesten at undgå fejl, næste gang lignende data behandles. |[Fremgangsmåde: Bruge OCR til at gøre PDF og filer til elektroniske dokumenter](across-how-use-ocr-pdf-images-files.md) |
| Forbinde eller fjerne indgående dokumentposter for ikke-bogførte salgs- eller købsdokumenter og med enhver debitor-, kreditor- eller finanspost fra dokumentet eller posten. |[Fremgangsmåde: Oprette indgående dokumentposter direkte fra dokumenter og poster](across-how-connect-disconnect-income-document-records.md) |
| Fra vinduerne **Kontoplan** og **Finansposter** skal du bruge en søgefunktionen til at finde finansposter for bogførte dokumenter, som ikke har indgående dokument poster og derefter knytte centralt til eksisterende poster eller oprette nye med vedhæftede dokument filer. |[Fremgangsmåde: Finde bogførte dokumenter uden indgående dokumentposter](across-how-find-posted-documents-without-income-document-records.md) |
| Få et større overblik ved at indstille indgående dokumentposter til Behandlet for at fjerne dem fra standardvisningen. |[Fremgangsmåde: Administrere mange indgående dokumentposter](across-how-manage-many-income-document-records.md) |

## <a name="see-also"></a>Se også
[Indgående bilag](across-income-documents.md)  
[Køb](purchasing-manage-purchasing.md)  
[Arbejde med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

