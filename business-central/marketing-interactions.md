---
title: Administrere interaktioner med dine kontakter | Microsoft Docs
description: Du kan administrere alle typer kommunikation eller interaktioner mellem din virksomhed og dine kontakter, f.eks. kommunikation via brev, telefon, møder osv.
services: project-madeira
documentationcenter: ''
author: jswymer
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: relationship, prospect
ms.date: 10/01/2020
ms.author: jswymer
ms.openlocfilehash: 854970fc2d47110375cf905236df19c90db27e33
ms.sourcegitcommit: ddbb5cede750df1baba4b3eab8fbed6744b5b9d6
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 10/01/2020
ms.locfileid: "3914035"
---
# <a name="record-interactions-with-contacts"></a>Registrere interaktioner med kontakter
Konfiguration af programmet til at registrere interaktioner består af disse opgaver:

* Konfiguration af interaktionsskabeloner  
* Oprettelse af interaktioner i kontakter eller målgrupper  
* Få vist og administrere registrerede interaktioner  

##  <a name="setting-up-interaction-templates"></a>Konfiguration af interaktionsskabeloner
Du skal konfigurere interaktionsskabeloner, før du kan oprette og registrere interaktioner. Når du skal oprette interaktioner, skal du angive de skabeloner, som interaktionerne er baseret på. En interaktionsskabelon en model, der definerer grundlæggende karakteristika for en interaktion.
Du konfigurerer en interaktionsskabelon på siden **Interaktionsskabeloner**.

Når du er færdig med at indtaste oplysninger om skabelonen, kan du oprette en vedhæftet fil, f.eks. et Microsoft Word-dokument. Gentag trinnene for hver interaktionsskabelon, du vil oprette.  

## <a name="creating-interactions"></a>Oprette interaktioner
Interaktioner kan registreres på to måder:

* Du kan oprette interaktioner manuelt, der er knyttet til en enkelt kontakt eller en målgruppe. Du kan finde flere oplysninger i [Oprette interaktioner for kontakter og målgrupper](marketing-how-create-interactions.md).  
* Du kan automatisk registrere interaktioner, når du udfører handlinger i programmet, f.eks. når du udskriver en faktura eller et tilbud. Du kan finde flere oplysninger i [Automatisk registrere interaktioner med kontakter](marketing-auto-record-interactions.md).

## <a name="viewing-and-managing-recorded-interactions"></a>Visning og administration af registrerede interaktioner
Brug siden **Interaktionslogposter** til at se alle de registrerede interaktioner, som ikke er blevet slettet. Du kan åbne siden ved at:

* Bruge ikonet **Søg efter side eller rapport** til at søge på **Interaktionslogposter**.
* Vælge handlingen **Interaktionslogposter** i en kontakt eller en målgruppe.
  Siden **Interaktionslogpost** indeholder både de interaktioner, du opretter manuelt, og dem, som registreres automatisk af programmet.

På denne side kan du:

* Få vist status for interaktioner.
* Markere interaktioner som annulleret.

Du kan slette interaktionslogposter, der er blevet annulleret. For at slette interaktionslogposter skal du vælge ikonet ![Elpære, der åbner funktionen Fortæl mig](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig"), angive **Slet annullerede interaktionslogposter** og derefter vælge det relaterede link og angive oplysningerne.

## <a name="see-also"></a>Se også
[Administrere kontakter](marketing-contacts.md)  
[Administrere salgsleads](marketing-manage-sales-opportunities.md)  
[Arbejde med Business Central](ui-work-product.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]