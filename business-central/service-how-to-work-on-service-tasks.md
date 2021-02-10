---
title: Sådan arbejder du med serviceopgaver | Microsoft Docs
description: Når du har oprettet en serviceordre eller et servicetilbud, registreret serviceartikellinjer og allokeret ressourcer til serviceartiklerne i ordren eller tilbuddet, kan du begynde at reparere og vedligeholde serviceartiklerne.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: 21f4dc7f2f0fa6602f02720fc441d1007d0f6bfe
ms.sourcegitcommit: 2e7307fbe1eb3b34d0ad9356226a19409054a402
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 12/17/2020
ms.locfileid: "4747989"
---
# <a name="work-on-service-tasks"></a>Arbejde med serviceopgaver
Når du har oprettet en serviceordre eller et servicetilbud, registreret serviceartikellinjer og allokeret ressourcer til serviceartiklerne i ordren eller tilbuddet, kan du begynde at reparere og vedligeholde serviceartiklerne.  

[!INCLUDE[prod_short](includes/prod_short.md)] indeholder siden **Serviceopgaver**, der giver et overblik over alle de serviceartikler, der skal behandles. Du betragte dette vindue som dit servicedashboard, hvor du kan se, hvilke ordrer der venter, søge efter og registrere reservedele og holde lageret opdateret.  

Hvis du vil spore ændringer og have vist grafiske oversigter over serviceaktiviteterne, kan du bruge statistikværktøjerne i [!INCLUDE[prod_short](includes/prod_short.md)] til hurtigt at opstille automatisk genererede diagrammer og analyser.  

## <a name="to-work-on-a-service-task"></a>Sådan arbejdes med serviceopgaver  
1. Vælg ikonet ![Elpære, der åbner funktionen Fortæl mig](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig"), angiv **Serviceopgaver**, og vælg derefter det relaterede link.
2. Hvis du vil se en liste over serviceopgaver, som en bestemt ressource eller ressourcegruppe er allokeret til, skal du udfylde feltet **Ressourcefilter** eller feltet **Ressourcegruppefilter** og trykke på Enter.  
3. Hvis du vil have vist en liste over serviceopgaver, der har en eller flere bestemte svardatoer inden for en bestemt periode, skal du udfylde feltet **Svardatofilter** og trykke på Enter.  
4. Hvis du vil se en liste over serviceopgaver med en bestemt allokeringsstatus eller reparationsstatus, skal du udfylde feltet **Allokeringsstatusfilter** eller feltet **Reparationsstatuskodefilter** og trykke på Enter.  
5. Markér navnet på den serviceopgave, du vil arbejde på. Vælg handlingen **Varekladde**. Siden **Serviceartikelkladde** åbnes.  
6. Registrer standardtekster, reservedele, ressourcetimer og omkostninger ved hjælp af de tilsvarende indstillinger i feltet **Type**: <Blank>, **Vare**, **Ressource** og **Omkostning**.  
7. Vælg den relevante status i feltet **Reparationsstatus**.  

   > [!NOTE]  
   >  Udfyld feltet **Reparationsstatus** med statussen **Færdig** eller **Delvist repareret**, afhængigt af om serviceartiklen er færdigrepareret, eller en anden ressource fortsætter reparationen. Statussen **Færdig** eller **Genallokering nødvendig** angives automatisk for den allokeringspost, der svarer til serviceartiklen.  

## <a name="to-register-service-operations"></a>Sådan registreres servicehandlinger  
Når der udføres service på en serviceordre, kan du registrere detaljerne ved at angive de varer, der er anvendt, de omkostninger, der er påløbet, og den tid, der er medgået. De data, du angiver gemmes på siden **Serviceartikelkladde**. Du kan opdatere dataene efter behov.

1. Vælg ikonet ![Elpære, der åbner funktionen Fortæl mig](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig"), angiv **Serviceordrer**, og vælg derefter det relaterede link.  
2. Åbn serviceordren, du vil registrere service for, og vælg varelinjen.  
3. Vælg handlingen **Serviceartikelkladde**  
4. Angiv de varer, der er brugt, de omkostninger, der er påløbet, og den tid, der er forbrugt på servicen, på linjerne.  

   > [!NOTE]  
   >  Du kan også registrere service direkte på de servicelinjer, der er knyttet til serviceordren.  

## <a name="to-register-spare-parts"></a>Registrere reservedele  
Når du arbejder på serviceartikler i serviceordrer, kan du få brug for reservedele til reparation. Følgende fremgangsmåde viser, hvordan de anvendte reservedele skal registreres på siden **Serviceartikelkladde**.  

1. Vælg ikonet ![Elpære, der åbner funktionen Fortæl mig](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig"), angiv **Serviceopgaver**, og vælg derefter det relaterede link.
2. Vælg den linje, der indeholder den relevante serviceartikel, og vælg derefter handlingen **Artikelkladde**.  
3. Indsæt en ny servicelinje.  
4. Vælg **Vare** i feltet **Type**.  
5. I feltet **Nummer** skal du vælge den relevante reservedel.  
6. Angiv, hvor det nødvendige antal varer i feltet **Antal**.  

 Du kan bruge en tilsvarende fremgangsmåde til at registrere reservedelene på siden **Servicelinjer**, som du kan åbne fra siden **Serviceordre**.  

## <a name="to-register-spare-parts-from-a-service-order"></a>Sådan registreres reservedele fra en serviceordre  
1. Vælg ikonet ![Elpære, der åbner funktionen Fortæl mig](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig"), angiv **Serviceordrer**, og vælg derefter det relaterede link.  
2. Åbn den serviceordre, du vil registrere reservedele for.  
3. Vælg den linje, der indeholder den relevante serviceartikel. Vælg **Handlinger**, vælg **Ordre**, og vælg derefter **Servicelinjer**.  
4. Indsæt en ny servicelinje.  

## <a name="to-replace-a-service-item-or-a-service-item-component"></a>Som erstattes en serviceartikel eller en serviceartikelkomponent  
Når du reparerer en serviceartikel, der består af komponenter, kan du blive nødt til at udskifte en fejlbehæftet komponent med en ny. Hver gang du angiver en reservedel for en serviceartikel med komponenter, får du automatisk mulighed for at vælge at udskifte en komponent eller oprette en ny. Den nye vare registreres ikke som en komponent til serviceartiklen, før du bogfører denne servicelinje eller serviceordren.

1. Vælg ikonet ![Elpære, der åbner funktionen Fortæl mig](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig"), angiv **Serviceopgaver**, og vælg derefter det relaterede link.
2. Vælg den linje, der indeholder serviceartiklen, og vælg derefter handlingen **Artikelkladde**.  
3. Indsæt en ny servicelinje.  
4. Vælg **Vare** i feltet **Type**.  
5. I feltet **Nummer** skal du vælge komponenten, der skal erstattes.  
6. Tryk på **Enter**. Der vises en dialogboks med følgende tre indstillinger: **Udskift komponent**, **Ny komponent** og **Ignorer**. Den følgende tabel beskriver indstillingerne.  

    |Indstilling | Beskrivelse|  
    |----------------------------------|---------------------------------------|  
    |**Udskift komponent**|Ændrer automatisk status for den komponent, du udskifter, til ikke-aktiv, og det ses på oversigten over udskiftede komponenter for serviceartiklen.|  
    |**Ny komponent**|Angiver automatisk den nye komponent på komponentoversigten for serviceartiklen.|  
    |**Ignorer**|Der sker ingenting med serviceartiklens komponentoversigt.|  

7. Vælg **Udskift komponent**.  
8. Vælg den komponent, der skal erstattes, og vælg derefter **OK**.  

## <a name="to-change-the-response-time-for-a-service-item-line"></a>Ændre svartiden for en serviceartikellinje  
Når du registrerer en serviceartikellinje i en serviceordre eller et tilbud, angives der automatisk en standardsvartid i timer, og svardatoen og -tidspunktet beregnes i overensstemmelse hermed. Du kan om nødvendigt ændre svartiden i timer samt svardatoen og -tidspunktet.  

1. Vælg ikonet ![Elpære, der åbner funktionen Fortæl mig](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig"), angiv **Serviceordrer** eller **Servicetilbud**, og vælg derefter det relaterede link.  
2. Vælg serviceordren eller servicetilbuddet for at åbne kortet.  
3. På den serviceartikellinje, du vil ændre svartiden for, skal du skrive de nye svartider eller svardatoen og -tidspunktet i feltet **Svartid (timer)** eller i felterne **Svardato** og **Svartidspunkt**.  

## <a name="to-register-faultresolution-codes"></a>Sådan registreres fejl/løsningskoder  
Når du har repareret en serviceartikel, kan du registrere både fejlkoden og løsningskoden for varen ved at vælge en kombination fra de eksisterende fejl/løsningskoderelationer. Fejl- og løsningskoderne vises i de tilsvarende felter på siden **Serviceartikelkladde**. Du kan også registrere koderne direkte på denne side.  

1. Vælg ikonet ![Elpære, der åbner funktionen Fortæl mig](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig"), angiv **Serviceopgaver**, og vælg derefter det relaterede link.
2. Vælg den linje, der indeholder den relevante serviceartikel, og vælg derefter handlingen **Artikelkladde**.  
3. På siden **Serviceartikelkladde** skal du vælge **Fejl/løsn.koderelationer**. Siden **Fejl/løsn.koderelationer** åbner.  

  >  [!NOTE]
  >  Der sættes automatisk filtre på de relationer, der vises på siden, fordi serviceartikelgruppen og fejlkoderne kopieres fra siden **Serviceartikelkladde**.  

4. Udfyld linjen. Vælg kombinationen af fejl- og løsningskoder, og vælg derefter **OK** for at kopiere den til serviceartiklen. Hvis der ikke kan findes en passende kombination, kan du oprette en ny kombination på siden.  

## <a name="see-also"></a>Se også  
[Definere fejlrapportering](service-how-setup-fault-reporting.md)
[Allokeringsstatus og reparationsstatus](service-allocation-status-and-repair-status.md)  
[Bogføring af tjenesten](service-service-posting.md)  
