---
title: Administrere interaktioner med dine kontakter | Microsoft Docs
description: "Du kan administrere alle typer kommunikation eller interaktioner mellem din virksomhed og dine kontakter, f.eks. kommunikation via brev, telefon, møder osv."
services: project-madeira
documentationcenter: 
author: jswymer
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: relationship, prospect
ms.date: 06/06/2017
ms.author: jswymer
ms.translationtype: HT
ms.sourcegitcommit: bec0619be0a65e3625759e13d2866ac615d7513c
ms.openlocfilehash: 761502b8c8e4c2b9b1b864e7316ea1130a940bb0
ms.contentlocale: da-dk
ms.lasthandoff: 03/22/2018

---
# <a name="managing-interactions-with-contacts"></a>Administration af interaktioner med kontakter
I [!INCLUDE[d365fin](includes/d365fin_md.md)] er interaktioner alle typer kommunikation mellem din virksomhed og dine kontakter. F.eks. kan kommunikation foregå via brev, fax, mail, telefon, møder osv.

I relationsstyringsområdet kan du registrere alle de interaktioner, du har med kontakter. Det sætter dig i stand til at holde styr på de salgs- og marketingstiltag, du har iværksat i forbindelse med kontakterne, og til at forbedre de fremtidige forretningsinteraktioner med dem. Konfiguration af programmet til at registrere interaktioner består af disse opgaver:

* Konfiguration af interaktionsskabeloner  
* Oprettelse af interaktioner i kontakter eller målgrupper  
* Få vist og administrere registrerede interaktioner  

##  <a name="setting-up-interaction-templates"></a>Konfiguration af interaktionsskabeloner
Du skal konfigurere interaktionsskabeloner, før du kan oprette og registrere interaktioner. Når du skal oprette interaktioner, skal du angive de skabeloner, som interaktionerne er baseret på. En interaktionsskabelon en model, der definerer grundlæggende karakteristika for en interaktion.
Du konfigurerer en interaktionsskabelon i vinduet **Interaktionsskabeloner**.  

## <a name="creating-interactions"></a>Oprette interaktioner
Interaktioner kan registreres på to måder:

* Du kan oprette interaktioner manuelt, der er knyttet til en enkelt kontakt eller en målgruppe. Du kan finde flere oplysninger i [Oprette interaktioner for kontakter og målgrupper](marketing-how-create-interactions.md).  
* Du kan automatisk registrere interaktioner, når du udfører handlinger i programmet, f.eks. når du udskriver en faktura eller et tilbud. Du kan finde flere oplysninger i [Automatisk registrere interaktioner med kontakter](marketing-auto-record-interactions.md).

## <a name="viewing-and-managing-recorded-interactions"></a>Visning og administration af registrerede interaktioner
Brug vinduet **Interaktionslogposter** til at se alle de registrerede interaktioner, som ikke er blevet slettet. Du kan åbne vinduet ved at:

* Bruge ikonet **Søg efter side eller rapport** til at søge på **Interaktionslogposter**.
* Vælge handlingen **Interaktionslogposter** i en kontakt eller en målgruppe.
  Vinduet **Interaktionslogpost** indeholder både de interaktioner, du opretter manuelt, og dem, som registreres automatisk af programmet.

I dette vindue kan du:

* Få vist status for interaktioner.
* Markere interaktioner som annulleret.

Du kan slette interaktionslogposter, der er blevet annulleret. For at slette interaktionslogposter skal du vælge ikonet ![Søg efter side eller rapport](media/ui-search/search_small.png "Ikonet Søg efter side eller rapport"), angive **Slet annullerede interaktionslogposter** og derefter vælge det relaterede link og angive oplysningerne.

## <a name="see-also"></a>Se også
[Administrere kontakter](marketing-contacts.md)  
[Administrere salgsleads](marketing-manage-sales-opportunities.md)  
[Arbejde med Financials](ui-work-product.md)  

