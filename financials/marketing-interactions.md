---
title: Interaktioner | Microsoft Docs
description: Beskriver brug af interaktioner med kontakter i Financials
services: project-madeira
documentationcenter: 
author: jswymer
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: relationship, prospect
ms.date: 03/28/2017
ms.author: jswymer
ms.translationtype: Human Translation
ms.sourcegitcommit: a31be0f9d07e2abb591e26f6bae34c6f6e4dcda6
ms.openlocfilehash: a423f5581f6803b60a0351d0b91f2c08ebafeba7
ms.contentlocale: da-dk
ms.lasthandoff: 05/04/2017


---
# <a name="managing-interactions-with-contacts"></a>Administration af interaktioner med kontakter
I [!INCLUDE[d365fin_long](includes/d365fin_long_md.md)] er interaktioner alle typer kommunikation mellem din virksomhed og dine kontakter. F.eks. kan kommunikation foregå via brev, fax, mail, telefon, møder osv.

I relationsstyringsområdet kan du registrere alle de interaktioner, du har med kontakter. Det sætter dig i stand til at holde styr på de salgs- og marketingstiltag, du har iværksat i forbindelse med kontakterne, og til at forbedre de fremtidige forretningsinteraktioner med dem. Konfiguration af programmet til at registrere interaktioner består af disse opgaver:

* Konfiguration af interaktionsskabeloner  
* Oprettelse af interaktioner i kontakter eller målgrupper  
* Få vist og administrere registrerede interaktioner  

##  <a name="set-up-interaction-templates"></a>Konfigurere interaktionsskabeloner
Du skal konfigurere interaktionsskabeloner, før du kan oprette og registrere interaktioner. Når du skal oprette interaktioner, skal du angive de skabeloner, som interaktionerne er baseret på. En interaktionsskabelon en model, der definerer grundlæggende karakteristika for en interaktion.
Du konfigurerer en interaktionsskabelon i vinduet **Interaktionsskabeloner**.  

## <a name="create-interactions"></a>Oprette interaktioner
Interaktioner kan registreres på to måder:

* Du kan oprette interaktioner manuelt, der er knyttet til en enkelt kontakt eller en målgruppe. Du kan finde flere oplysninger i [Fremgangsmåde: Oprette interaktioner for kontakter og målgrupper](marketing-how-create-interactions.md).  
* Du kan automatisk registrere interaktioner, når du udfører handlinger i programmet, f.eks. når du udskriver en faktura eller et tilbud. Du kan finde flere oplysninger i [Automatisk registrere interaktioner med kontakter](marketing-auto-record-interactions.md).

## <a name="view-and-manage-recorded-interactions"></a>Få vist og administrere registrerede interaktioner
Brug vinduet **Interaktionslogposter** til at se alle de registrerede interaktioner, som ikke er blevet slettet. Du kan åbne vinduet ved at:

* Bruge ikonet **Søg efter side eller rapport** til at søge på **Interaktionslogposter**.
* Vælge handlingen **Interaktionslogposter** i en kontakt eller en målgruppe.
  Vinduet **Interaktionslogpost** indeholder både de interaktioner, du opretter manuelt, og dem, som registreres automatisk af programmet.

I dette vindue kan du:

* Få vist status for interaktioner.
* Markere interaktioner som annulleret.

Du kan slette interaktionslogposter, der er blevet annulleret. For at slette interaktionslogposter skal du i øverste højre hjørne vælge ikonet **Søg efter side eller rapport** ![Søg efter side eller rapport](media/ui-search/search_small.png "Ikonet Søg efter side eller rapport"), angive **Slet annullerede interaktionslogposter** og derefter vælge det relaterede link og angive oplysningerne.

## <a name="see-also"></a>Se også
[Administrere kontakter](marketing-contacts.md)  
[Administrere salgsleads](marketing-manage-sales-opportunities.md)  
[Arbejde med Financials](ui-work-product.md)  

