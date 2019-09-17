---
title: Konfigurer maillogføring | Microsoft Docs
description: Få at vide, hvordan du ændrer mailinteraktioner mellem sælgere og kunder til reelle salgs-leads.
services: project-madeira
documentationcenter: ''
author: bholtorf
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: relationship, prospect, opportunity, email
ms.date: 08/26/2019
ms.author: bholtorf
ms.openlocfilehash: e42618be17ff4f9bfe0d54a88e70d5a1841568c1
ms.sourcegitcommit: 8d9f08304b2f3b5504332bc626383797564ac5e3
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 08/26/2019
ms.locfileid: "1920462"
---
# <a name="track-email-message-exchanges-between-salespeople-and-contacts"></a>Spore udveksling af mails mellem sælgere og kontakter
Få mere ud af kommunikationen mellem sælgerne og dine eksisterende eller potentielle kunder ved at spore udveksling af mails og derefter ændre dem til handlingsrettede leads. [!INCLUDE[d365fin](includes/d365fin_md.md)] kan bruges sammen med Exchange Online til at føre en log over indgående og udgående meddelelser. Du kan få vist og analysere indholdet af hver meddelelse på siden **Interaktionslogposter**.

> [!VIDEO https://go.microsoft.com/fwlink/?linkid=2085401]

## <a name="setting-up-included365finincludesd365fin_mdmd-to-log-email-messages"></a>Oprette [!INCLUDE[d365fin](includes/d365fin_md.md)] til logføring af mails
Introduktion til maillogføring i to lette trin:

1. Opret forbindelse mellem [!INCLUDE[d365fin](includes/d365fin_md.md)] og Exchange Online for dit Office 365-abonnement. Exchange Online håndterer dine mails. Vi har gjort dette trin lettilgængeligt med en vejledning til assisteret opsætning. Du skal blot bruge dine administratorrettigheder til din administratorkonto i Office 365. Start vejledningen ved at gå til **Assisteret opsætning**, og vælg derefter **Konfigurer maillogføring**. 
2. Kontrollér, at der er angivet gyldige mailadresser i [!INCLUDE[d365fin](includes/d365fin_md.md)] for dine sælgere og kontakter, afhængigt af om de er potentielle eller eksisterende kunder. Hvis du vil gøre det, skal du for hver debitor eller sælger åbne kortet **Kontakt** eller **Sælger/indkøber** og se feltet **Mailadresse**.

> [!Tip]
> Når du har udført trinnene i programguiden, kan du kontrollere, om forbindelsen er oprettet. Søg efter **Marketingopsætning**, vælg **Proces**, derefter **Funktioner** og derefter **Valider opsætning af maillogføring**.

## <a name="viewing-email-message-exchanges-in-the-interaction-log"></a>Få vist udveksling af mails i interaktionslogposten
[!INCLUDE[d365fin](includes/d365fin_md.md)] opretter en post på siden **Interaktionslog**, hver gang en sælger og en kontakt udveksler en mail. Du kan få vist interaktionsloggen ved at åbne kortet **Kontakt** eller **Sælger/indkøber** for personen, vælge **Naviger**, **Oversigt** og derefter vælge **Interaktionslogposter**. Der er nogle få ting, der kan udføres for hver indtastning i logfilen, f. eks.:

* Få vist indholdet af den mail, der blev udvekslet, ved at klikke på handlingen **Vis vedhæftede filer**.
* Omdanne en mailudveksling til et salgs-lead – hvis en post ser lovende ud, kan du gøre den til en lead og derefter styre forløbet hen imod et salg. Det gør du ved at vælge posten og derefter vælge handlingen **Opret lead**. Du kan finde flere oplysninger under [Administrere salgsleads](marketing-manage-sales-opportunities.md).

## <a name="see-also"></a>Se også
[Styre relationer](marketing-relationship-management.md)

