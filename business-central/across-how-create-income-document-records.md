---
title: Oprette poster for indgående bilag | Microsoft Docs
description: Du kan oprette poster for indgående bilag, f.eks. e-fakturaer, og administrere OCR-opgaver eCommerce og dokumentudveksling.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: electronic document, e-invoice, incoming document, OCR, ecommerce, document exchange, import invoice
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: 722e69389413dc06db4f2b7fd2f8447d9033d030
ms.sourcegitcommit: 2e7307fbe1eb3b34d0ad9356226a19409054a402
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 12/17/2020
ms.locfileid: "4753288"
---
# <a name="create-incoming-document-records"></a>Oprette indgående bilagsposter
På siden **Indgående bilag** kan du bruge forskellige funktioner til at gennemgå udgiftsbilag, administrere OCR-opgaver og konvertere indgående bilagsfiler, manuelt eller automatisk, til de relevante købs- og salgsdokumenter eller kladdelinjer. Eksterne filer kan tilknyttes i enhver procesfase, herunder til bogførte dokumenter og til de derved oprettede kreditor-, debitor- og finansposter.

Når du vil registrere et eksternt dokument i [!INCLUDE[prod_short](includes/prod_short.md)], skal du først oprette eller fuldføre en indgående bilagspost. Du kan gøre dette manuelt, eller du kan tage et billede af det eksterne bilag og derefter oprette den indgående bilagspost med billedfilen vedhæftet.

Før du kan bruge funktionen Indgående bilag, skal du foretage den nødvendige opsætning. Du kan finde flere oplysninger under [Konfigurere indgående bilag](across-how-setup-income-documents.md).

## <a name="to-approve-or-reject-an-incoming-document"></a>Sådan godkendes eller afvises et indgående bilag
Hvis du vil tillade brugere at oprette fakturaer eller finanskladdelinjer fra indgående bilagsposter, medmindre de er godkendt, kan du angive godkendere, der skal godkende posterne, før de kan behandles.

1. Vælg ikonet ![Elpære, der åbner funktionen Fortæl mig](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig"), angiv **Indgående bilag**, og vælg derefter det relaterede link.
2. Marker linjen i det dokument, du vil godkende eller afvise, og vælg derefter handlingen **Godkend** eller **Afvis**.

Hvis du godkender den indgående bilagspost, markeres afkrydsningsfeltet **Frigivet** på den indgående bilagslinje. Brugeren, der har ansvaret for at godkende, f.eks, købsfakturaer, kan fortsætte med at behandle posten.

## <a name="to-create-an-incoming-document-record-by-taking-a-photo"></a>Sådan opretter du en indgående bilagspost ved at tage et billede
> [!NOTE]  
>   Følgende procedure gælder kun for [!INCLUDE[prod_short](includes/prod_short.md)] tablet- og telefonklienter.

1. På applinjen skal du vælge feltet **Opret indgående bilag fra kamera** og derefter gå til trin 4.
2. Du kan også vælge alternativknappen på applinjen, vælge **Indgående bilag** og derefter vælge **Alle**.
3. På siden **Indgående bilag** skal du vælge ellipseknappen og derefter vælge **Opret fra kamera**. Kameraet på tabletten eller telefonen aktiveres.
4. Tag et billede af et dokument, f.eks en købsleverance, som du vil behandle som et indgående bilag, og vælg derefter knappen **OK**.

    Der oprettes en ny indgående bilagspost med billedet vedhæftet.

## <a name="to-attach-an-image-to-an-incoming-document-record-by-taking-a-photo"></a>Sådan vedhæfter du et billede til en indgående bilagspost ved at tage et billede
> [!NOTE]  
>   Følgende procedure gælder kun for [!INCLUDE[prod_short](includes/prod_short.md)] tablet- og telefonklienter.

1. På applinjen skal du vælge alternativknappen, vælg **Indgående bilag** og vælg derefter **Alle**.
2. Åbn kortet for en eksisterende indgående bilagspost.
3. På siden **Indgående bilag** skal du vælge ellipseknappen og derefter vælge **Vedhæft billede fra kamera**. Kameraet på tabletten eller telefonen aktiveres.
4. Tag et billede af et bilag, f.eks en købsleverance, som du vil behandle som et indgående bilag, og vælg derefter knappen **OK**.

    Billedet vedhæftes til den indgående bilagspost.

## <a name="to-create-an-incoming-document-record-manually"></a>Sådan oprettes en indgående bilagspost manuelt
1. Vælg ikonet ![Elpære, der åbner funktionen Fortæl mig](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig"), angiv **Indgående bilag**, og vælg derefter det relaterede link.
2. Vælg handlingen **Opret fra fil**.  
3. På siden **Indsæt fil** skal du vælge en fil og derefter klikke på **Åbn**. Filen vedhæftes automatisk.
4. Du kan også vælge handlingen **Ny**.
5. Du kan vedhæfte en fil ved at vælge handlingen **Vedhæft fil**.
6. På siden **Indsæt fil** , skal du vælge den fil, der repræsenterer det pågældende indgående bilag og derefter vælge knappen **Åbn**.
7. På siden **Indgående bilag** skal du udfylde felterne efter behov. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

## <a name="see-also"></a>Se også
[Behandle indgående bilag](across-process-income-documents.md)  
[Indgående bilag](across-income-documents.md)  
[Køb](purchasing-manage-purchasing.md)  
[Arbejde med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]