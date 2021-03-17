---
title: Fejlfinding i virksomhedens hub
description: Få mere at vide om, hvordan du kan løse problemer, når du arbejder i virksomheden i Dynamics 365 Business Central for at administrere arbejde på tværs af flere firmaer.
author: edupont04
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: accountant, accounting, troubleshoot
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: d75c6ceb27c7e1ee101b23bbc18f3eac0db4ced7
ms.sourcegitcommit: ff2b55b7e790447e0c1fcd5c2ec7f7610338ebaa
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 02/15/2021
ms.locfileid: "5389120"
---
# <a name="troubleshooting-your-company-hub"></a>Fejlfinding i virksomhedens hub

Det er nemt at føje virksomheder til virksomhedshubben, og denne artikel vedrører problemer, der eventuelt opstår undervejs.  

## <a name="check-errors"></a>Kontrollér fejl

Brug handlingen **Kontroller fejl** til at få vist en liste over de seneste fejl. Du kan få vist flere oplysninger om hver fejl, og du kan rydde op i loggen ved at slette gamle poster.  

## <a name="connection-failed"></a>Der kunne ikke oprettes forbindelse

Der kan være nogle årsager til, at du ikke kan oprette forbindelse til en virksomhed, herunder følgende:

- URL-adressen i feltet **Miljølink** er ikke gyldig  

  Gå til siden **Miljølinks**, åbn det miljø, du ikke kan oprette forbindelse til, og vælg derefter handlingen **Test forbindelse**.  
- Kundens virksomhed er offline, f.eks. hvis den er ved at blive opgraderet

  På dashboardet skal du vælge menupunktet **Værktøjer** og derefter vælge **Kontroller fejl**. Dermed åbnes en liste med tekniske oplysninger, så du skal måske kontakte systemadministratoren, hvis du får vist fejl. Meddelelsen "*Serveren har afvist kundens legitimationsoplysninger*" angiver f.eks., at du ikke har adgang.  
- Du har ikke adgang til alle regnskaber i miljøet, som du forsøger at oprette forbindelse til.

  I [!INCLUDE [prod_short](includes/prod_short.md)] kan en organisation have flere forretningsenheder kaldet virksomheder, og du har muligvis ikke adgang til alle virksomheder. Arbejd sammen med administratoren for at sikre, at du har adgang til de virksomheder, som du ønsker at arbejde i.  

## <a name="data-does-not-refresh"></a>Data opdateres ikke

Når du tilføjer en virksomhed eller anmoder om en opdatering af dataene, henter [!INCLUDE [prod_short](includes/prod_short.md)] dataene. Men du skal selv opdatere siden, f.eks. ved at vælge handlingen **Genindlæs alle virksomheder**, opdatere browsersiden, navigere væk fra dashboardet og derefter tilbage igen eller noget lignende.  

Hvis du har tilføjet et regnskab, men det ikke vises på listen, kan du også bruge handlingen **Genindlæs alle virksomheder** for at opdatere listen.

## <a name="see-also"></a>Se også

[Administrere arbejde på tværs af flere regnskaber i virksomhedshub](company-hub.md)  
[Tilføj firmaer til virksomhedens hub](company-hub-add-company.md)  
[Revisoroplevelser i Business Central](finance-accounting.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]