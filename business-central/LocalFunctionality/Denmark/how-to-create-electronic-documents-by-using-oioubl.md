---
title: Oprette elektroniske dokumenter i et OIOUBL-format
description: Når du sælger varer eller tjenesteydelser til en kunde i den offentlige sektor i Danmark, skal du sende dokumenter elektronisk.
author: bholtorf
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 06/18/2021
ms.author: bholtorf
ms.openlocfilehash: f285671ee62b558e7ffa27c3e546602a2224a437
ms.sourcegitcommit: a7cb0be8eae6ece95f5259d7de7a48b385c9cfeb
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 07/08/2021
ms.locfileid: "6444094"
---
# <a name="create-electronic-documents-by-using-oioubl"></a>Oprette elektroniske dokumenter ved hjælp af OIOUBL
Når du sælger varer eller tjenesteydelser til en kunde i den offentlige sektor, skal du sende dokumenter elektronisk. I [!INCLUDE[prod_short](../../includes/prod_short.md)], kan du oprette elektroniske dokumenter til fakturaer, kreditnotaer, rykkere og rentenotaer. Før du kan oprette elektroniske dokumenter, skal du have angivet filplaceringer og oplysninger om kunderne. Du kan få flere oplysninger i [Konfigurere kunder til OIOUBL](how-to-set-up-customers-for-oioubl.md).  

Du kan oprette et elektronisk dokument, når du har bogført et salgs- eller servicedokument. I følgende afsnit beskrives, hvordan du bogfører en salgsfaktura med de nødvendige oplysninger og derefter opretter en elektronisk salgsfaktura, men samme fremgangsmåde gælder for salgs-og servicekreditnotaer og rykkere.  

## <a name="to-post-a-sales-invoice"></a>Sådan bogføres en salgsfaktura  
1.  Vælg ![Lightbulb, der åbner funktionen Fortæl mig.](../../media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **Salgsfakturaer**, og vælg derefter det relaterede link.  
2.  Åbn den salgsfaktura, som du vil bogføre.  
3.  Kontrollér, at feltet **Eksternt bilagsnr.** indeholder nummeret på det dokument, kunden har leveret. Elektroniske OIOUBL-dokumenter kræver dette nummer.

    > [!Note]  
    > For servicedokumenter skal du udfylde feltet **Din reference**.  

4.  I oversigtspanelet **Fakturering** skal du udfylde felterne **GLN** og **OIOUB-kontokode**.  

    Til rykkere og rentenotaer findes felterne i oversigtspanelet **Bogføring**.  

5.  Bogfør fakturaen.  

## <a name="to-create-an-electronic-sales-invoice"></a>Sådan oprettes en elektronisk salgsfaktura  
Når du har bogført et dokument, kan du oprette en elektronisk faktura i OIOUBL-format. Nedenfor beskrives processen for bogførte salgsfakturaer, men proceduren er den samme for andre dokumenter.

1.  Vælg ![Lightbulb, der åbner funktionen Fortæl mig.](../../media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **Bogførte salgsfakturaer**, og vælg derefter det relaterede link.  
2.  Åbn den relevante bogførte salgsfaktura.  
3.  Vælg handlingen **Opret elektronisk <*dokumenttype*>**.  
4.  På siden **Opret elektronisk<*dokumenttype*>** kan du angive yderligere filtre og derefter vælge knappen **OK**.  

Derved oprettes en XML-fil, der gemmes på standardplaceringen for hentning på din enhed.


> [!Note]
> Med onlineversionen af Business Central oprettes XML-filen automatisk i mappen med overførsler på pc'en.

## <a name="see-also"></a>Se også  
[Lokal funktionalitet for Danmark](denmark-local-functionality.md)  
 [Konfigurere OIOUBL](how-to-set-up-oioubl.md)   
 [Konfigurere kunder til OIOUBL](how-to-set-up-customers-for-oioubl.md)   
 [Oversigt over elektronisk OIOUBL-fakturering](oioubl-electronic-invoicing-overview.md)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]