---
title: "Hent eksempelversionen på nye markeder"
description: "Få mere at vide om at få adgang til eksempelversioner af Business Central."
author: bholtorf
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: preview, trial, sandbox
ms.date: 06/28/2018
ms.author: bholtorf
ms.translationtype: HT
ms.sourcegitcommit: 2286b728a464943841b192031cfea13644441013
ms.openlocfilehash: 0829c825ec0635a20c040fe17cd3e7cfc667ffd7
ms.contentlocale: da-dk
ms.lasthandoff: 06/28/2018

---
# <a name="access-to-the-included365finlongincludesd365finlongmdmd-preview"></a>Adgang til [!INCLUDE[d365fin_long](includes/d365fin_long_md.md)]-eksempelversionen
Startende i foråret 2018 bliver [!INCLUDE[d365fin](includes/d365fin_md.md)] tilgængelig i nye lande. For at sikre, at [!INCLUDE[d365fin](includes/d365fin_md.md)] er den rigtige løsning for kunder, kan vi tilbyde en eksempelversion af tjenesten forud for forårets lancering. Eksempelversionen for Danmark blev tilgængelig i januar, 2018 og yderligere markeder vil hurtigt følge efter.  

## <a name="getting-started-with-previews-and-sandboxes"></a>Introduktion til eksempelversioner og sandkasser
Eksempelversioner og sandkasser er gode måder til at komme i gang med [!INCLUDE[d365fin](includes/d365fin_md.md)]. En forekomst af en eksempelversion indeholder funktioner, der er en tilføjelse til det, som er tilgængeligt i den aktuelle version. Eksempelversioner giver partnere og kunder mulighed for at afprøve og give feedback om funktioner, som vi tænker på at frigive. Selvom eksempelversionerne hovedsageligt er beregnet til partnere, er kunder også velkomne til at bruge dem i en begrænset periode. Den aktuelle eksempelversion af [!INCLUDE[d365fin](includes/d365fin_md.md)] indeholder de fleste af de funktioner, der findes i Dynamics NAV 2018, der typisk kræver lidt hjælp fra en partner at konfigurere.

Hvis du i gang med en eksempelversion, skal du gå til [denne side](https://go.microsoft.com/fwlink/?linkid=866045) og angive din mailadresse på arbejde. Du kan finde yderligere oplysninger om [!INCLUDE[d365fin](includes/d365fin_md.md)] og dets funktioner i dokumentationen på dette websted.

Du kan betragte en sandkasse som et ikke-produktionsmiljø, du kan bruge oven på din produktions- eller eksempelversionsforekomst af [!INCLUDE[d365fin](includes/d365fin_md.md)]. En sandkasse giver dig mulighed for sikkert at opbygge og teste udvidelser og udvikle nye funktioner for at tilpasse tjenesten, uden at det påvirker dataene og indstillingerne i produktions- eller eksempelversionsforekomsterne. I øjeblikket kan alle kunder, der har en produktions- eller eksempelversion, bruge en sandkasse.

Du kan se yderligere oplysninger om at komme i gang med en sandkasse i nedenstående instruktioner.

## <a name="creating-a-sandbox-environment"></a>Oprette et sandkassemiljø
Hvis du vil arbejde i et sandkassemiljø, skal du have et abonnement på [!INCLUDE[d365fin](includes/d365fin_md.md)]. Der må kun være én sandkasse pr. abonnement.

### <a name="advanced-functionality-available-in-a-sandbox-environment"></a>Avancerede funktioner, der er tilgængelige i et sandkassemiljø
Sandkasser indeholder en indbygget Designer-funktion i klienten, hvor du kan designe sider ved hjælp af en træk og slip-grænseflade og bygge udvidelser i selve klienten ved at tilføje eller omarrangere felter.

Der er flere oplysninger i [Anvende designer](https://docs.microsoft.com/en-us/dynamics-nav/developer/devenv-inclient-designer).

### <a name="to-create-a-sandbox-environment"></a>Sådan opretter du et sandkassemiljø
1.  Log ind på din produktions- eller eksempelversionsforekomst af [!INCLUDE[d365fin](includes/d365fin_md.md)].  
2.  Vælg den ![Søg efter side eller rapport](media/ui-search/search_small.png "Ikonet Søg efter side eller rapport"), angiv **Sandkassemiljø**, og vælg derefter det relaterede link.
3.  Vælg **Opret**. Der åbnes en fane, hvor du kan afslutte konfigurationen af din sandkasse.

    > [!Note]
    > Hvis blokering af pop op-vinduer er aktiveret i din webbrowser, kan du ændre denne indstilling, så URL-adresser fra *.businesscentral.dynamics.com*-adressen tillades.  

4.  Når sandkassen er klar, vises siden Velkommen.  
5.  Hvis du vil have yderligere oplysninger om scenarier, som du kan prøve i en sandkasse, f.eks. hvordan du udvikler udvidelser, skal du vælge linket **Få mere at vide**. Ellers kan du vælge **Luk** for at fortsætte til rollecenteret for din [!INCLUDE[d365fin](includes/d365fin_md.md)]-sandkasseforekomst.  
6.  Der vises en meddelelse om, at dette er en sandkasse, øverst i rollecenteret. Du kan også se miljøtypen i titellinjen i klienten.

    > [!Note]
    > Sandkassen indeholder demodata for den fiktive virksomhed CRONUS. Der kopieres ikke eller på anden måde overføres data fra produktionsmiljøet.  

7.  Du kan når som helst vende tilbage til siden Sandkassemiljø og nulstille sandkassen.

    > [!Note]
    > Nulstilling af en sandkasse fjerner den helt, og derefter oprettes den igen med standarddemodata.  

8.  Hvis du vil skifte mellem produktionsmiljøet og sandkassen, skal du bruge Dynamics 365-menuen eller Dynamics-webstedet.

    > [!Note]
    > En administrator eller en anden bruger kan begrænse eller endda blokere brugeradgang til sandkassen ved hjælp af standardsikkerhedsfunktioner i [!INCLUDE[d365fin](includes/d365fin_md.md)], f.eks. brugerkortet, brugergrupper og tilladelsessæt.  

### <a name="building-new-solutions-and-intellectual-property"></a>Oprettelse af nye løsninger og immaterielle rettigheder
[!INCLUDE[d365fin](includes/d365fin_md.md)] indeholder et sæt værktøjer til udvikling og en moderne platform at bygge på, så du kan oprette din egne tilføjelsesapps og integrere løsninger for at forbinde eller udvide [!INCLUDE[d365fin](includes/d365fin_md.md)].

[!INCLUDE[d365fin](includes/d365fin_md.md)] indeholder værktøjer, du kan bruge til at implementere dit eget tilføjelsesprogram og integrere funktioner for at tilføje nye branchespecifikke oplevelser fra slutpunkt til slutpunkt eller integrere løsninger fra tredjepart. Du kan f.eks. bruge et API til at opbygge en forbundet app, der udveksler data mellem [!INCLUDE[d365fin](includes/d365fin_md.md)] og din løn-app. Forbundne apps kan også gør brug af udvidelser til at oprette sider, der skal bruges til installation, konfiguration eller til at understøtte app-specifikke funktioner. Du kan finde flere oplysninger i [Udvikling af apps til [!INCLUDE[d365fin](includes/d365fin_md.md)]](https://aka.ms/getstartedwithapps).

## <a name="see-also"></a>Se også
[Introduktion](product-get-started.md)  
[Arbejde med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)  

