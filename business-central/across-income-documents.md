---
title: Arbejde med indgående bilag
description: 'Du kan administrere indgående eksterne virksomhedsdokumenter, f.eks. betalingskvitteringer eller PDF-filer, styre OCR-opgaver og konvertere filerne til elektroniske dokumenter og poster.'
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 'electronic document, e-invoice, incoming document, OCR, ecommerce, document exchange, import invoice'
ms.date: 06/14/2022
ms.author: edupont
---
# <a name="incoming-documents"></a><a name="incoming-documents"></a><a name="incoming-documents"></a>Indgående bilag

Eksterne forretningsbilag kan komme til din virksomhed som en vedhæftet fil i mail eller som en papirkopi, som du indscanne i en fil. Dette er typisk for køb, hvor sådanne indgående bilagsfiler repræsenterer betalingskvitteringer for udgifter eller mindre køb.

På siden **Indgående bilag** kan du bruge forskellige funktioner til at gennemgå udgiftsbilag, administrere OCR-opgaver og konvertere indgående bilagsfiler, manuelt eller automatisk, til de relevante købs- og salgsdokumenter eller kladdelinjer. Eksterne filer kan tilknyttes i enhver procesfase, herunder til bogførte dokumenter og til de derved oprettede kreditor-, debitor- og finansposter.

## <a name="usage-scenario"></a><a name="usage-scenario"></a><a name="usage-scenario"></a>Brugsscenarie

Du kan registrere filer eller papirkopier, der er modtaget fra samhandelspartnere, i [!INCLUDE[prod_short](includes/prod_short.md)] og oprette en bilagspost. F. eks. en købs-eller salgsfaktura, kreditnota eller en kladdelinje.

Overfør de modtagne filer – eller brug enhedens kamera til at tage et billede – og Opret poster, der repræsenterer de eksterne bilag. Alternativt med PDF-filer eller billedfiler kan du få en ekstern OCR-tjeneste (Optical Character Recognition) til at oprette elektroniske dokumenter, som derefter kan konverteres til dokumentposter i [!INCLUDE[prod_short](includes/prod_short.md)].

> [!NOTE]
> OCR-funktionen leveres af eksterne udbydere. Vælg en servicepakke, der passer til din organisation og/eller dit land/område. Find tjenester, der er kompatible med [!INCLUDE[prod_short](includes/prod_short.md)], og oplysninger om tilgængelige funktioner på [AppSource.microsoft.com](https://go.microsoft.com/fwlink/?linkid=2081646).

F.eks. når du modtager en faktura i PDF-format fra en leverandør, kan du sende den til tjenesten OCR fra siden **Indgående bilag**. Nogle OCR-udbydere giver også mulighed for at behandle filer, der er videresendt til en dedikeret e-mailadresse, som derefter automatisk opretter en relateret post for indgående bilag. Efter nogle sekunder får du filen tilbage fra OCR-tjenesten som en elektronisk faktura, der kan konverteres til en købsfaktura til kreditoren.

> [!TIP]
> Oprette indgående bilagsposter i [!INCLUDE[prod_short](includes/prod_short.md)] direkte fra e-mails, der er sendt af leverandører ved hjælp af Outlook-tilføjelsesprogrammet. Du kan finde flere oplysninger i [Brug Business Central som din virksomheds Indbakke i Outlook](work-outlook-addin.md).

## <a name="incoming-document-features"></a><a name="incoming-document-features"></a><a name="incoming-document-features"></a>Indgående bilagsfunktioner

Det indgående bilag kan bestå af følgende primære aktiviteter:

* Registrer eksterne dokumenter i [!INCLUDE[prod_short](includes/prod_short.md)] ved at oprette linjer på siden **Indgående bilag** på en af følgende måder:
  * Manuelt fra en pc eller fra en mobilenhed på en af følgende måder:
    * Brug knappen **Opret fra fil**, upload en fil og udfyld derefter de relevante felter på siden **Indgående bilag**.
    * Brug knappen **Ny**, og udfyld derefter de relevante felter på siden **Indgående bilag**, og vedhæft manuelt den relaterede fil.
    * Fra en tablet eller telefon skal du bruge knappen **Opret fra kamera** til at oprette en ny indgående bilagspost ved hjælp af enhedens indbyggede kamera.
  * Automatisk ved at modtage dokumentet fra OCR-tjenesten som et elektronisk dokument, når du har sendt en mail med den relaterede PDF- eller billedfil til OCR-tjenesten. Oversigtspanelet **Finansielle oplysninger** udfyldes automatisk på siden **Indgående bilag**.
* Bruge en ekstern OCR-tjeneste til at omdanne PDF- eller billedfiler til elektroniske dokumenter, der kan konverteres til dokumentposter i [!INCLUDE[prod_short](includes/prod_short.md)].
* Opret nye dokumenter eller finanskladdelinjer for indgående bilagsposter ved at angive oplysninger, mens du læser dem fra indgående bilagsfiler.
* Vedhæfte indgående bilagsfiler for købs- og salgsdokumenter af enhver status, herunder til de kreditor-, debitor- og finansposter, der stammer fra bogføring.
* Få vist indgående bilagsposter og de vedhæftede filer fra ethvert købs- og salgsdokument eller post eller finde alle finansposter uden indgående bilagsposter fra siden **Kontoplan**.

> [!NOTE]
> Filer, der er vedhæftet til kort og bilag på fanen **Vedhæftede filer**, medtages ikke under fanen **Indgående bilag**. Du kan få flere oplysninger i [Administrere vedhæftede filer, links og noter på kort og dokumenter](ui-how-add-link-to-record.md).

| Til | Se |
| --- | --- |
| Konfigurer funktionen **indgående bilag**, og opret OCR tjenesten. |[Opsætning af indgående bilag](across-how-setup-income-documents.md) |
| Opret indgående bilagsposter manuelt eller automatisk ved at tage et billede af en papirkvittering, f.eks. |[Oprette indgående bilagsposter](across-how-create-income-document-records.md) |
| Bruge en OCR-tjeneste til at konvertere PDF- og billedfiler til elektroniske dokumenter, der igen kan konverteres til købsfakturaer i [!INCLUDE[prod_short](includes/prod_short.md)] f.eks. Lær OCR-tjenesten at undgå fejl, næste gang lignende data behandles. |[Bruge OCR til at gøre PDF- og billedfiler til elektroniske dokumenter](across-how-use-ocr-pdf-images-files.md) |
| Forbinde eller fjerne indgående bilagsposter for ikke-bogførte salgs- eller købsdokumenter og med enhver debitor-, kreditor- eller finanspost fra dokumentet eller posten. |[Oprette indgående bilagsposter direkte fra dokumenter og poster](across-how-connect-disconnect-income-document-records.md) |
| Fra siderne **Kontoplan** og **Finansposter** skal du bruge en søgefunktionen til at finde finansposter for bogførte dokumenter, som ikke har indgående bilagsposter og derefter knytte centralt til eksisterende poster eller oprette nye med vedhæftede dokument filer. |[Finde bogførte dokumenter uden indgående bilagsposter](across-how-find-posted-documents-without-income-document-records.md) |
| Få et større overblik ved at indstille indgående bilagsposter til *Behandlet* for at fjerne dem fra standardvisningen. |[Administrere mange indgående bilagsposter](across-how-manage-many-income-document-records.md) |

## <a name="see-related-microsoft-training"></a><a name="see-related-microsoft-training"></a><a name="see-related-microsoft-training"></a>Se relateret [Microsoft-træning](/training/modules/incoming-documents-dynamics-365-business-central/)

## <a name="see-also"></a><a name="see-also"></a><a name="see-also"></a>Se også

[Køb](purchasing-manage-purchasing.md)  
[Redigering af bogførte bilag](across-edit-posted-document.md)  
[Udveksle data elektronisk](across-data-exchange.md)  
[Business Central og OneDrive for Business Integration](across-onedrive-overview.md)  
[Bruge Business Central som din virksomheds Indbakke i Outlook](work-outlook-addin.md)  
[Sende dokumenter og e-mails](ui-how-send-documents-email.md)  
[Arbejd med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
