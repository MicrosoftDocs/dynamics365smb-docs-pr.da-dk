---
title: Holde et rapportlayout opdateret | Microsoft Docs
description: "Du har muligvis behov for at opdatere et brugerdefineret rapportlayout, der bruges i en rapport. Dette er påkrævet, når der er sket en designændring af rapportens datasæt, eksempelvis et felt, der bruges i layoutet, er blevet fjernet fra datasættet i rapporten."
services: project-madeira
documentationcenter: 
author: jswymer
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 07/01/2017
ms.author: jswymer
ms.translationtype: HT
ms.sourcegitcommit: bec0619be0a65e3625759e13d2866ac615d7513c
ms.openlocfilehash: 0395cf37d56282684c2a6e4c2066fd9b249f16f0
ms.contentlocale: da-dk
ms.lasthandoff: 03/22/2018

---
# <a name="updating-report-or-document-layouts"></a>Opdatere rapport- eller dokumentlayout
Nogle gange skal du opdatere et brugerdefineret rapportlayout, der bruges i en rapport. Dette er påkrævet, når der er sket en designændring af rapportens datasæt, eksempelvis et felt, der bruges i layoutet, er blevet fjernet fra datasættet i rapporten. Hvis et rapportlayout kræver opdatering, får du en fejlmeddelelse, når du forsøger at se, udskrive eller gemme rapporten.  
  
Du kan automatisk opdatere et rapportlayout fra den fejlmeddelelse, der vises, når du kører rapporten, ved at vælge knappen **Ja** på fejlmeddelelsen. Eller før du kører rapporter, kan du opdatere specifikke rapportlayout eller alle tilpassede rapportlayout, der kunne blive påvirket af datasætændringer.  
  
Du har også mulighed for at kontrollere opdateringer uden at anvende de nødvendige ændringer på brugerdefinerede rapportlayout. Dette gør det muligt for dig at se, hvilke ændringer der anvendes på rapportlayoutet og identificere mulige problemer i processen. Fra resultaterne, kan du åbne de brugerdefinerede rapportlayout direkte til redigering for at løse problemer. Det anbefales at kontrollere kontrolrapportopdateringen, før du anvender opdateringerne.  
  
Ikke alle ændringer af rapportdatasæt kan opdateres automatisk i rapportlayout. Nogle ændringer kræver, at du manuelt redigere rapportlayout. Du kan finde flere oplysninger i [Begrænsninger for den brugerdefinerede rapport layoutopdatering](ui-update-report-layouts.md#UpdateLimitations).  
  
## <a name="to-update-one-or-more-custom-report-layouts"></a>Sådan opdaterer du ét eller flere brugerdefinerede rapportlayout  
  
1.  Vælg ikonet ![Søg efter side eller rapport](media/ui-search/search_small.png "Ikonet Søg efter side eller rapport"), angiv **Rapportlayout**, og vælg derefter det relaterede link.  
  
2.  Hvis du vil opdatere en bestemt rapport, skal du i vinduet **Rapportlayout** vælge layoutet på listen og derefter vælge handlingen **Opdater layout**. Eller hvis du vil opdatere alle brugerdefinerede rapportlayout for virksomheden, skal du vælge handlingen **Opdater alle layout**.  

Hvis der ikke opstår fejl, anvendes opdateringerne på rapportlayout. Hvis der opstår fejl, vises en meddelelse, der indeholder de fejl, der er. Derefter skal du manuelt redigere brugerdefinerede rapportlayout for at rette fejlen. Du kan finde flere oplysninger under [Rettelse af fejl](ui-update-report-layouts.md#FixErrors).  

## <a name="to-test-custom-report-layout-updates"></a>Sådan kontrollerer du opdateringer til brugerdefinerede rapportlayout  
  
1.  Vælg ikonet ![Søg efter side eller rapport](media/ui-search/search_small.png "Ikonet Søg efter side eller rapport"), angiv **Valg af rapportlayout**, og vælg derefter det relaterede link.  
  
2.  I vinduet **Valg af rapportlayout** skal du vælge handlingen **Opdateringer af testlayout**.  
  
 Ændringer til de viste rapportlayout testes, men anvendes ikke på de faktiske rapportlayout. Et **Log over rapportlayoutopdatering** åbnes og viser status for de mulig opdateringer til hver rapportlayout. Hvis der er fejl i et rapportlayout, kan du åbne rapportlayout direkte til redigering fra meddelelsen for at løse problemer. Du kan finde flere oplysninger under [Rettelse af fejl](ui-update-report-layouts.md#FixErrors).  
  
##  <a name="UpdateLimitations"></a> Begrænsninger for den brugerdefinerede rapport layoutopdatering  
 Der er flere typer ændringer, som den automatisk opdatering kan anvende på brugerdefinerede rapportlayout, f.eks. er et felt, der bruges i layoutet, fjernet fra rapportens datasæt. Men den automatisk opdatering kan ikke håndtere følgende ændringer af et rapportdatasæt.  
  
1.  Slettede felter, etiketter eller dataelementer.  
  
2.  Navn på dubletfelter i rapportlayout, når et felt er omdøbt i datasættet. Det skal behandles som en designfejl.  
  
3.  Opgraderingssituationer, hvor der er flere gentagelser af rapportlayout, som bevirker flere omdøbningshandlinger i de samme felter, etiketter eller dataelementer.  
  
 Hvis der registreres et af disse problemer under opdateringen, kan opdateringen ikke anvendes. Du er nødt til at løse problemerne manuelt, f.eks. ved at redigere rapportlayoutet i Word, eller gennem programmering ved at bruge opgraderingskodeenheder.  
  
##  <a name="FixErrors"></a> Rettelse af fejl  
 Hvis du får en fejlmeddelelse, når du opdaterer eller kontrollerer layoutopdateringer, skal du sandsynligvis ændre rapportens layout for at løse problemet. Læs fejlmeddelelsen for at finde årsagen til problemet.  
  
 Det mest almindelige problem opstår, når et felt, der bruges i layoutet, er blevet fjernet fra rapportens datasæt. I dette tilfælde vil du se en linje i den fejlmeddelelse, der angiver, at en vare er blevet fjernet. Du kan løse dette problem ved at ændre layoutet og fjerne det pågældende felt.  
  
 Du kan finde flere oplysninger i [Oprette og ændre et brugerdefineret rapportlayout](ui-how-create-custom-report-layout.md#ModifyCustomLayout).  
  
 Når du ændrer layoutet, kan du prøve at opdatere layoutet igen.  
  
## <a name="see-also"></a>Se også  
 [Administration af rapportlayout](ui-manage-report-layouts.md)  
 [Arbejde med rapporter](ui-work-report.md)  
