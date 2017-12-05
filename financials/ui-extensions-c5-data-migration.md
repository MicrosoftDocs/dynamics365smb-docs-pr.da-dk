---
title: "Bruge udvidelsen C5-dataoverførsel | Microsoft Docs"
description: "Du kan bruge denne udvidelse til at overføre debitorer, kreditorer, varer og omkostninger på finanskonti fra Microsoft Dynamics C5 2012 til Financials."
services: project-madeira
documentationcenter: 
author: bholtorf
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms. search.keywords: extension, migrate, data, C5, import
ms.date: 09/26/2017
ms.author: bholtorf
ms.translationtype: HT
ms.sourcegitcommit: ba26b354d235981bd7291f9ac6402779f554ac7a
ms.openlocfilehash: 2d7d533662936116ffa40ded07b68e845fed810b
ms.contentlocale: da-dk
ms.lasthandoff: 11/10/2017

---

# <a name="the-c5-data-migration-extension-for-dynamics-365-for-finance-and-operations-business-edition"></a>Udvidelsen C5-dataoverførsel til Dynamics 365 for Finance and Operations, Business Edition
Denne udvidelse gør det let at overføre debitorer, kreditorer, varer og finanskonti fra Microsoft Dynamics C5 2012 til [!INCLUDE[d365fin](includes/d365fin_md.md)].  
  
> [!Note] 
> Virksomheden i [!INCLUDE[d365fin](includes/d365fin_md.md)] må ikke indeholde data. Når du starter en overførsel, må du desuden ikke oprette debitorer, kreditorer, varer eller konti, før overflytningen er afsluttet.

## <a name="to-migrate-data"></a>Sådan overføres data
Der er nogle få trin til at eksportere data fra C5 og indlæse dem i [!INCLUDE[d365fin](includes/d365fin_md.md)]:  
  
1. I C5 skal du bruge funktionen **Eksportér databasen** til at eksportere dataene. Send derefter eksportmappen til en komprimeret (zippet) mappe.  
2. I [!INCLUDE[d365fin](includes/d365fin_md.md)] skal du vælge ikonet ![Søg efter side eller rapport](media/ui-search/search_small.png "Ikonet Søg efter side eller rapport"), angive **Dataoverførsel** og derefter vælg **Dataoverførsel**.  
3. Udfør trinnene i guiden til assisteret opsætning. Sørg for at vælge **Indlæs fra Microsoft Dynamcis C5 2012** som datakilde.  

> [!Note] 
> Virksomheder tilføje ofte felter for at tilpasse C5 til deres specifikke branche. [!INCLUDE[d365fin](includes/d365fin_md.md)] overflytter ikke data fra brugerdefinerede felter. Overførslen mislykkes også, hvis du har mere end 10 brugerdefinerede felter. 

## <a name="viewing-the-status-of-the-migration"></a>Få vist status for overførslen
Brug siden **Dataoverførselsoversigt** til at overvåge status for overførslen. Siden viser oplysninger, f.eks. antallet af enheder overførslen skal medtage, status for overførslen, og antallet af elementer, der er blevet overført, og om de var vellykket. Den viser også antallet af fejl, giver dig mulighed for at finde ud af, hvad der gik galt, og gør det, hvis det er muligt, nemt at gå til enheden for at løse problemerne. Du kan finde flere oplysninger i næste afsnit i dette emne. 

> [!Note] 
> Mens du venter på resultaterne af overførslen, skal du opdatere siden for at få vist resultaterne.

## <a name="correcting-errors"></a>Rette fejl
Hvis noget går galt, og der opstår en fejl, viser feltet **Status** teksten **Udført med fejl**, og feltet **Antal fejl** viser hvor mange. For at få vist en liste over fejlene, kan du åbne siden **Dataoverførselsfejl** side ved at vælge:

* Nummeret i feltet **Antal fejl** for enheden. 
* Enheden og derefter handlingen **Vis fejl**. 

På siden **Dataoverførselsfejl** kan du for at rette en fejl vælge en fejlmeddelelse, og derefter vælge **Rediger post** for at åbne en side, der viser de overførte data for objektet. Når du retter en eller flere fejl, kan du vælge **Overfør** for kun at overføre de enheder, du rettede, uden at genstarte hele overførslen.  

> [!Tip]
> Hvis du har rettet mere end én fejl, kan du bruge funktionen **Markér flere** til at markere flere linjer, der skal overføres. Hvis der omvendt er fejl, det ikke er vigtigt at løse, kan du vælge dem og derefter vælge **Spring valg over**.

> [!Note]
> Hvis du har varer, der indgår i en stykliste, kan du være nødt til at overføre mere end én gang, hvis den oprindelige vare ikke er oprettet før de varianter, der refererer til den. Hvis en varevariant oprettes først, kan det medføre, at referencen til den oprindelige vare giver en fejlmeddelelse.  

## <a name="verifying-data-after-migrating"></a>Kontrol af data efter overførsel 
Hvis du vil kontrollere, at dine data overføres korrekt, kan du se de følgende sider i C5 og [!INCLUDE[d365fin](includes/d365fin_md.md)].

|Microsoft Dynamics C5 2012 | [!INCLUDE[d365fin](includes/d365fin_md.md)]|
|-----|-----|
|Debitorposter| Finanskladder|
|Kreditorposter| Finanskladder|
|Vareposter| Varekladder|

I [!INCLUDE[d365fin](includes/d365fin_md.md)] hedder batchen for de overførte data **C5MIGRATE**. 

## <a name="stopping-data-migration"></a>Stoppe dataoverførslen
Du kan stoppe overførslen af data ved at vælge **Stop alle overførsler**. Hvis du gør det, stoppes alle ventende overførsler også.

## <a name="see-also"></a>Se også
[Tilpasse [!INCLUDE[d365fin](includes/d365fin_md.md)] ved hjælp af udvidelser](ui-extensions.md)  
[Velkommen til [!INCLUDE[d365fin](includes/d365fin_md.md)]](index.md)  

