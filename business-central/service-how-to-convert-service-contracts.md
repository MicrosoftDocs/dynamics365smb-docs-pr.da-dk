---
title: "Sådan konverteres servicekontrakter | Microsoft Docs"
description: "Da momssatsændringsværktøjet ikke kan konvertere servicekontrakter, skal disse kontrakter konverteres manuelt. Dette emne beskriver flere alternative metoder, der kan bruges til konvertering af servicekontrakter."
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 10/01/2018
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 33b900f1ac9e295921e7f3d6ea72cc93939d8a1b
ms.openlocfilehash: 3c34f2b456df88b043b7b90a739f363b892dd48d
ms.contentlocale: da-dk
ms.lasthandoff: 11/26/2018

---
# <a name="convert-service-contracts-that-include-vat-amounts"></a>Konvertere servicekontrakter, som omfatter momsbeløb
Da momssatsændringsværktøjet ikke kan konvertere servicekontrakter, skal disse kontrakter konverteres manuelt. Dette emne beskriver flere alternative metoder, der kan bruges til konvertering af servicekontrakter.  

> [!NOTE]  
>  Dette emne giver en overordnet arbejdsproces.  

 Følgende procedure beskriver, hvordan du retter en faktura til en forudbetalt servicekontrakt, der er oprettet et år i forvejen.  

> [!NOTE]  
>  I dette eksempel skal du ændre din arbejdsdato til 01.01.2017.  

### <a name="to-correct-an-invoice-for-a-prepaid-service-contract"></a>Sådan rettes en faktura for en forudbetalt servicekontrakt  
1. Vælg ikonet ![Elpære, der åbner funktionen Fortæl mig](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig"), angiv **Kontraktstyring**, og vælg derefter det relaterede link.  
2. Under **Lister** skal du vælge **Servicekontrakter**.  
3. Opret en ny forudbetalt servicekontrakt. Angiv en startdato til **01.01.2017** og et fakturaperiodeåret for debitor **20000**.  
4. Denne kontrakt skal underskrives. Under fanen **Startside** i gruppen **Behandle** skal du vælge **Underskriv kontakt**.  
5. Opret en servicefaktura.
6. Fakturaen er angivet som en ikke-bogførte servicefaktura. For at se servicefakturaen skal du vælge **Service**, vælge **Kontraktstyring** og derefter vælge **Service fakturaer**.  
7. Bogfør servicefakturaen.  

> [!NOTE]  
>  Ændr ikke den ikke-bogførte servicefaktura. Da serviceposterne oprettes, når fakturaen oprettes, vil en ændring af den ikke-bogførte faktura ikke ændre de allerede oprettede serviceposter. Momsposter oprettes dog, når fakturaen bogføres. Dermed kan du ændre den generelle produktbogføringsgruppe og GSP-produktbogføringsgruppe på den ikke-bogførte servicefaktura.  

### <a name="to-create-a-credit-memo-for-vat-difference"></a>Sådan oprettes en kreditnota for momsdifference  
Følgende procedure beskriver, hvordan du opretter en kreditnota , der kun omfatter momsdifference for den periode, der allerede er fakturerede, startende med **01.07.2017**. I dette eksempel bogføres momsbeløbet kun i modulet Økonomistyring, ikke i modulet Servicestyring. De momsposter, der er knyttet til serviceposten, vil ikke blive rettet.  

1. Oprette en ny finanskonto for momsdifferencen. Denne konto bruges til direkte bogføring af momskorrektionen.  
2. Tilføj en ny linje til momsbogføringsopsætningen.  

### <a name="to-create-contract-expiration-dates-in-contract-lines"></a>Sådan oprettes kontraktudløbsdatoen i kontraktlinjer  
Følgende procedure beskriver, hvordan du opretter nye kontrakter ved at arbejde med kontraktudløbsdatoer i servicekontraktlinjer.  

1. På siden **Servicekontrakt** angives kontraktens udløbsdato til **30.06.2017**.  
2. Vælg handlingen **Opret kreditnota** for automatisk at oprette en kreditnota for juli 2017 til december 2017.  
3. Da kontrakten er udløbet, skal du oprette en ny kontrakt for perioden med den nye momssats for 1 juli 2017 til 31. december 2017.  

### <a name="to-create-a-new-credit-memo"></a>Sådan oprettes en ny kreditnota  
Følgende procedure beskriver, hvordan du opretter en ny kreditnota ved hjælp af batchjobbet **Hent forudbetalte kontraktposter**. Poster, du ikke vil rette fra januar 2017 til juni 2017, vil blive slettet.  

1. Du kan køre momssatsændringsværktøjet på 1 juli 2017. Den generelle produktbogføringsgruppe eller momsproduktbogføringsgruppen ændres. Du kan finde flere oplysninger i [Arbejde med moms af salg og køb](finance-work-with-vat.md).  
2. Når du har kørt momssatsændringsværktøjet skal du angive en kontraktudløbsdato for servicekontrakten. Du kan nu slette servicekontraktlinjen og oprette en ny linje, der er identisk med den gamle.  
3. Opret en ny faktura for perioden januar 2017 til december 2012 ved hjælp af den nye momssats.  
4. For at oprette en anden kreditnota skal du på siden **Servicekreditnotaer** vælge **Ny** for at oprette en ny servicekreditnota.  
5. Vælg handlingen **Hent forudbetalte kontraktposter**.  
6. Når konverteringen er fuldført, vil moms og serviceposter være korrekte.  

## <a name="see-also"></a>Se også  
[Arbejde med servicekontrakter og servicekontrakttilbud](service-how-to-create-service-contracts-and-service-contract-quotes.md)  
[Finans](finance.md)  
[Rapportere moms til skattemyndighederne](finance-how-report-vat.md)  
[Arbejde moms af salg og køb](finance-work-with-vat.md)  

