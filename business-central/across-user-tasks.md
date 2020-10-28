---
title: Tildele og administrere opgaver | Microsoft Docs
description: Få at vide, hvordan du kan tildele opgaver til brugere, herunder din bogholder, i Business Central
author: edupont04
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: tasks, work
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: c76751726f5cd680fafc0887fc57a1464d0ac3ca
ms.sourcegitcommit: ddbb5cede750df1baba4b3eab8fbed6744b5b9d6
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 10/01/2020
ms.locfileid: "3922613"
---
# <a name="define-user-tasks"></a>Definere brugeropgaver

I [!INCLUDE[d365fin](includes/d365fin_md.md)] kan du oprette opgaver for at minde dig om arbejde, der skal udføres. Du kan oprette opgaver til dig selv, men du kan også tildele opgaver til andre eller få tildelt en opgave af en anden i organisationen.  

## <a name="managing-user-tasks"></a>Administrere brugeropgaver

Siden **Brugeropgaver** viser alle opgaver, og du kan nemt oprette og tildele nye opgaver. Når du opretter en opgave, kan du angive start- og forfaldsdato, og du kan føje et link til siden eller rapporten i [!INCLUDE[d365fin](includes/d365fin_md.md)], hvor brugeren skal udføre arbejdet.  

Du kan f.eks. oprette en opgave til dig selv eller en kollega for at få vist alle bogførte salgsfakturaer. I så fald skal knytte du opgaven til side 143, **Bogf. salgsfakturaer**. På følgende skærmbillede oprettes der en opgave for MeganB for at gennemgå de bogførte salgsfakturaer.  

:::image type="content" source="media/across-user-tasks/sample-user-task.png" alt-text="Eksempel på en brugeropgave":::

> [!TIP]  
> Brug opslaget i feltet **Side**, og brug derefter feltet **Søg** til at finde den ønskede side.  
>
> Du kan oprette et link til enhver side, men du kan ikke oprette en link til enkelte poster, så du skal bruge beskrivelsen så eksplicit som muligt, f.eks. skrive &quot;Kig nærmere på Kundenr." 10000, og sørg for, at der ikke er forfaldne betalinger".

### <a name="picking-up-user-tasks"></a>Hente brugeropgaver

I rollecentrene Virksomhedsleder, Bogholder og Regnskabsmedarbejder viser et felt ventende opgaver, der er knyttet til den pågældende bruger. For at hente en opgave skal du blot vælge den på listen over ventende brugeropgaver. På båndet åbner linket **Gå til opgaveelementet** den side, hvor du kan udføre arbejdet.  

Når du har udført en opgave, skal du blot markeres som fuldført.  

### <a name="deleting-user-tasks"></a>Slette brugeropgaver

Hvis du vil masseslette alle eller nogle brugeropgaver, kan du bruge rapporten **Slet brugeropgaver**. På anmodningssiden kan du angive filtre, der bestemmer, hvilke opgaver der skal slettes.  

## <a name="see-also"></a>Se også

[Søge efter en side eller rapport](ui-search.md)  
[Revisoroplevelser i [!INCLUDE[d365fin](includes/d365fin_md.md)]](finance-accounting.md)  
