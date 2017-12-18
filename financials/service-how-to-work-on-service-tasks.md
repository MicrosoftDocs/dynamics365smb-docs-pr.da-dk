---
title: "Sådan arbejder du med serviceopgaver | Microsoft Docs"
description: "Når du har oprettet en serviceordre eller et servicetilbud, registreret serviceartikellinjer og allokeret ressourcer til serviceartiklerne i ordren eller tilbuddet, kan du begynde at reparere og vedligeholde serviceartiklerne."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 07/01/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 2c13559bb3dc44cdb61697f5135c5b931e34d2a8
ms.openlocfilehash: 32cbc23b24a8a04a62a246dd50eac8d8a721e2e7
ms.contentlocale: da-dk
ms.lasthandoff: 09/22/2017

---
# <a name="how-to-work-on-service-tasks"></a>Fremgangsmåde: Arbejde med serviceopgaver
Når du har oprettet en serviceordre eller et servicetilbud, registreret serviceartikellinjer og allokeret ressourcer til serviceartiklerne i ordren eller tilbuddet, kan du begynde at reparere og vedligeholde serviceartiklerne.  

[!INCLUDE[d365fin](includes/d365fin_md.md)] indeholder vinduet **Serviceopgaver**, der giver et overblik over alle de serviceartikler, der skal behandles. Du betragte dette vindue som dit servicedashboard, hvor du kan se, hvilke ordrer der venter, søge efter og registrere reservedele og holde lageret opdateret.  
  
Hvis du vil spore ændringer og have vist grafiske oversigter over serviceaktiviteterne, kan du bruge statistikværktøjerne i [!INCLUDE[d365fin](includes/d365fin_md.md)] til hurtigt at opstille automatisk genererede diagrammer og analyser.  
  
## <a name="to-work-on-a-service-task"></a>Sådan arbejdes med serviceopgaver  
1. Vælg ikonet ![Søg efter side eller rapport](media/ui-search/search_small.png "Ikonet Søg efter side eller rapport"), angiv **Serviceopgaver**, og vælg derefter det relaterede link. 
2. Hvis du vil se en liste over serviceopgaver, som en bestemt ressource eller ressourcegruppe er allokeret til, skal du udfylde feltet **Ressourcefilter** eller feltet **Ressourcegruppefilter** og trykke på Enter.  
3. Hvis du vil have vist en liste over serviceopgaver, der har en eller flere bestemte svardatoer inden for en bestemt periode, skal du udfylde feltet **Svardatofilter** og trykke på Enter.  
4. Hvis du vil se en liste over serviceopgaver med en bestemt allokeringsstatus eller reparationsstatus, skal du udfylde feltet **Allokeringsstatusfilter** eller feltet **Reparationsstatuskodefilter** og trykke på Enter.  
5. Markér navnet på den serviceopgave, du vil arbejde på. Vælg **Serviceartikelkld.** i gruppen **Serviceopgaver** under fanen **Naviger**. Vinduet **Serviceartikelkladde** åbnes.  
6. Registrer standardtekster, reservedele, ressourcetimer og omkostninger ved hjælp af de tilsvarende indstillinger i feltet **Type**: <Blank>, **Vare**, **Ressource** og **Omkostning**.  
7. Vælg den relevante status i feltet **Reparationsstatus**.  
  
   > [!NOTE]  
   >  Udfyld feltet **Reparationsstatus** med statussen **Færdig** eller **Delvist repareret**, afhængigt af om serviceartiklen er færdigrepareret, eller en anden ressource fortsætter reparationen. Statussen **Færdig** eller **Genallokering nødvendig** angives automatisk for den allokeringspost, der svarer til serviceartiklen.  

## <a name="to-register-service-operations"></a>Sådan registreres servicehandlinger  
Når der udføres service på en serviceordre, kan du registrere detaljerne ved at angive de varer, der er anvendt, de omkostninger, der er påløbet, og den tid, der er medgået. De data, du angiver gemmes i vinduet **Serviceartikelkladde**. Du kan opdatere dataene efter behov. 
   
1. Vælg ikonet ![Søg efter side eller rapport](media/ui-search/search_small.png "Ikonet Søg efter side eller rapport"), angiv **Serviceordrer**, og vælg derefter det relaterede link.  
2. Åbn serviceordren, du vil registrere service for, og vælg varelinjen.  
3. Vælg **Handlinger**, vælg **Linje**, og vælg derefter **Serviceartikelkladde.**  
4. Angiv de varer, der er brugt, de omkostninger, der er påløbet, og den tid, der er forbrugt på servicen, på linjerne.  
  
   > [!NOTE]  
   >  Du kan også registrere service direkte på de servicelinjer, der er knyttet til serviceordren.  
  
## <a name="to-register-spare-parts"></a>Registrere reservedele  
Når du arbejder på serviceartikler i serviceordrer, kan du få brug for reservedele til reparation. Følgende fremgangsmåde viser, hvordan de anvendte reservedele skal registreres i vinduet **Serviceartikelkladde**.  
  
1. Vælg ikonet ![Søg efter side eller rapport](media/ui-search/search_small.png "Ikonet Søg efter side eller rapport"), angiv **Serviceopgaver**, og vælg derefter det relaterede link. 
2. Vælg den linje, der indeholder den relevante serviceartikel, og vælg derefter handlingen **Artikelkladde**.  
3. Indsæt en ny servicelinje.  
4. Vælg **Vare** i feltet **Type**.  
5. I feltet **Nummer** skal du vælge den relevante reservedel.  
6. Angiv, hvor det nødvendige antal varer i feltet **Antal**.  
  
 Du kan bruge en tilsvarende fremgangsmåde til at registrere reservedelene på siden **Servicelinjer**, som du kan åbne fra siden **Serviceordre**.  
  
## <a name="to-register-spare-parts-from-a-service-order"></a>Sådan registreres reservedele fra en serviceordre  
1. Vælg ikonet ![Søg efter side eller rapport](media/ui-search/search_small.png "Ikonet Søg efter side eller rapport"), angiv **Serviceordrer**, og vælg derefter det relaterede link.  
2. Åbn den serviceordre, du vil registrere reservedele for.  
3. Vælg den linje, der indeholder den relevante serviceartikel. Vælg **Handlinger**, vælg **Ordre**, og vælg derefter **Servicelinjer**.  
4. Indsæt en ny servicelinje.  
  
## <a name="to-replace-a-service-item-or-a-service-item-component"></a>Som erstattes en serviceartikel eller en serviceartikelkomponent  
Når du reparerer en serviceartikel, der består af komponenter, kan du blive nødt til at udskifte en fejlbehæftet komponent med en ny. Hver gang du angiver en reservedel for en serviceartikel med komponenter, får du automatisk mulighed for at vælge at udskifte en komponent eller oprette en ny. Den nye vare registreres ikke som en komponent til serviceartiklen, før du bogfører denne servicelinje eller serviceordren. 
    
1. Vælg ikonet ![Søg efter side eller rapport](media/ui-search/search_small.png "Ikonet Søg efter side eller rapport"), angiv **Serviceopgaver**, og vælg derefter det relaterede link. 
2. Vælg den linje, der indeholder serviceartiklen, og vælg derefter handlingen **Artikelkladde**.  
3. Indsæt en ny servicelinje.  
4. Vælg **Vare** i feltet **Type**.  
5. I feltet **Nummer** skal du vælge komponenten, der skal erstattes.  
6. Tryk på **Enter**. Der vises en dialogboks med følgende tre indstillinger: **Udskift komponent**, **Ny komponent** og **Ignorer**. Den følgende tabel beskriver indstillingerne.  
  
    |Indstilling | Description|  
    |----------------------------------|---------------------------------------|  
    |**Udskift komponent**|Ændrer automatisk status for den komponent, du udskifter, til ikke-aktiv, og det ses på oversigten over udskiftede komponenter for serviceartiklen.|  
    |**Ny komponent**|Angiver automatisk den nye komponent på komponentoversigten for serviceartiklen.|  
    |**Ignorer**|Der sker ingenting med serviceartiklens komponentoversigt.|  
  
7. Vælg **Udskift komponent**.  
8. Vælg den komponent, der skal erstattes, og vælg derefter **OK**.  

## <a name="to-change-the-response-time-for-a-service-item-line"></a>Ændre svartiden for en serviceartikellinje  
Når du registrerer en serviceartikellinje i en serviceordre eller et tilbud, angives der automatisk en standardsvartid i timer, og svardatoen og -tidspunktet beregnes i overensstemmelse hermed. Du kan om nødvendigt ændre svartiden i timer samt svardatoen og -tidspunktet.  

1. Vælg ikonet ![Søg efter side eller rapport](media/ui-search/search_small.png "Ikonet Søg efter side eller rapport"), angiv **Serviceordrer** eller **Servicetilbud**, og vælg derefter det relaterede link.  
2. Vælg serviceordren eller servicetilbuddet for at åbne kortet.  
3. På den serviceartikellinje, du vil ændre svartiden for, skal du skrive de nye svartider eller svardatoen og -tidspunktet i feltet **Svartid (timer)** eller i felterne **Svardato** og **Svartidspunkt**.  

## <a name="to-register-faultresolution-codes"></a>Sådan registreres fejl/løsningskoder  
Når du har repareret en serviceartikel, kan du registrere både fejlkoden og løsningskoden for varen ved at vælge en kombination fra de eksisterende fejl/løsningskoderelationer. Fejl- og løsningskoderne vises i de tilsvarende felter i vinduet **Serviceartikelkladde**. Du kan også registrere koderne direkte i dette vindue.  
    
1. Vælg ikonet ![Søg efter side eller rapport](media/ui-search/search_small.png "Ikonet Søg efter side eller rapport"), angiv **Serviceopgaver**, og vælg derefter det relaterede link. 
2. Vælg den linje, der indeholder den relevante serviceartikel, og vælg derefter handlingen **Artikelkladde**.  
3. På siden **Serviceartikelkladde** skal du vælge **Fejl/løsn.koderelationer**. Vinduet **Fejl/løsn.koderelationer** åbner.  
  
  >  [!Note]
  >  Der sættes automatisk filtre på de relationer, der vises i vinduet, fordi serviceartikelgruppen og fejlkoderne kopieres fra vinduet **Serviceartikelkladde**.  
  
4. Udfyld linjen. Vælg kombinationen af fejl- og løsningskoder, og vælg derefter **OK** for at kopiere den til serviceartiklen. Hvis der ikke kan findes en passende kombination, kan du oprette en ny kombination i vinduet.  

## <a name="see-also"></a>Se også  
[Fremgangsmåde: Definere fejlrapportering](service-how-setup-fault-reporting.md)
[Allokeringsstatus og reparationsstatus](service-allocation-status-and-repair-status.md)  
[Bogføring af tjenesten](service-service-posting.md)  


