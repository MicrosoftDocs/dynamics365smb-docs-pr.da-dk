---
title: Behandle indgående bilag | Microsoft Docs
description: Når du vil registrere et eksternt dokument, f.eks. en PDF, i Business Central, skal du først oprette eller fuldføre en indgående bilagspost.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: electronic document, e-invoice, incoming document, OCR, ecommerce, document exchange, import invoice
ms.date: 10/01/2019
ms.author: sgroespe
ms.openlocfilehash: 90bcc95fd6aaf70302caa79f6ba0a265fe92a7a9
ms.sourcegitcommit: 02e704bc3e01d62072144919774f1244c42827e4
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 10/01/2019
ms.locfileid: "2308424"
---
# <a name="processing-incoming-documents"></a>Behandle indgående bilag
Når du vil registrere et eksternt dokument i [!INCLUDE[d365fin](includes/d365fin_md.md)], skal du først oprette eller fuldføre en indgående bilagspost. Du kan gøre dette manuelt, eller du kan tage et billede af det eksterne dokument og derefter oprette den indgående bilagspost med billedfilen vedhæftet.

Fra PDF-filer eller billedfiler, som du modtager fra dine handelspartnere, kan du få en ekstern OCR-tjeneste (Optical Character Recognition) til at oprette elektroniske dokumenter, der kan konverteres til dokumentposter i [!INCLUDE[d365fin](includes/d365fin_md.md)]. F.eks. når du modtager en faktura i PDF-format fra en leverandør, kan du sende den til tjenesten OCR fra siden **Indgående bilag**. Du kan også vælge at sende filen til OCR-tjenesten via mail. Når du får det elektroniske dokument retur, oprettes der automatisk en relateret indgående bilagspost. Efter nogle sekunder får du filen tilbage fra OCR-tjenesten som en elektronisk faktura, der kan konverteres til en købsfaktura til kreditoren.

| Hvis du vil | Se |
| --- | --- |
| Opret indgående bilagsposter manuelt eller automatisk ved at tage et billede af en papirkvittering, f.eks. |[Oprette indgående bilagsposter](across-how-create-income-document-records.md) |
| Bruge en OCR-tjeneste til at konvertere PDF- og billedfiler til elektroniske dokumenter, der igen kan konverteres til købsfakturaer i [!INCLUDE[d365fin](includes/d365fin_md.md)] f.eks. Lær OCR-tjenesten at undgå fejl, næste gang lignende data behandles. |[Bruge OCR til at gøre PDF- og billedfiler til elektroniske dokumenter](across-how-use-ocr-pdf-images-files.md) |
| Forbinde eller fjerne indgående bilagsposter for ikke-bogførte salgs- eller købsdokumenter og med enhver debitor-, kreditor- eller finanspost fra dokumentet eller posten. |[Oprette indgående bilagsposter direkte fra dokumenter og poster](across-how-connect-disconnect-income-document-records.md) |
| Fra siderne **Kontoplan** og **Finansposter** skal du bruge en søgefunktionen til at finde finansposter for bogførte dokumenter, som ikke har indgående bilagsposter og derefter knytte centralt til eksisterende poster eller oprette nye med vedhæftede dokument filer. |[Finde bogførte dokumenter uden indgående bilagsposter](across-how-find-posted-documents-without-income-document-records.md) |
| Få et større overblik ved at indstille indgående bilagsposter til Behandlet for at fjerne dem fra standardvisningen. |[Administrere mange indgående bilagsposter](across-how-manage-many-income-document-records.md) |

## <a name="see-also"></a>Se også
[Indgående bilag](across-income-documents.md)  
[Køb](purchasing-manage-purchasing.md)  
[Arbejde med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)
