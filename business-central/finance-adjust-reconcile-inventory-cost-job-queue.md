---
title: Planlæg sager til regulering og afstemning af lageromkostninger
description: 'Få mere at vide om, hvordan du kan bruge opgavekøen til at flytte opgaverne for at regulere lageromkostninger eller afstemme den med finansregnskabet i baggrunden. Hvis din virksomhed f.eks. kører mange opgaver eller behandler mange transaktioner.'
author: brentholtorf
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.reviewer: bholtorf
ms.search.form: 461
ms.date: 09/23/2021
ms.author: bholtorf
---
# Planlæg sager til regulering og afstemning af lageromkostninger med finansmodulet

Hvis du vil optimere oplevelsen, er automatisk kostregulering og bogføring til finansmodulet aktiveret som standard. Men når data akkumuleres over tid, kan det påvirke ydeevnen. Hvis du vil reducere belastningen af programmet, kan det ofte være nyttigt at bruge opgavekøposter til at flytte opgaver, der skal køres i baggrunden.

## Flytte opgaven for regulering af vareomkostningerne til baggrunden ved hjælp af assisteret opsætning

Det kan være vanskeligt at oprette opgavekøposter, selv for en erfaren konsulent, så vi har en assisteret opsætningsvejledning, der letter processen i forbindelse med regulering af vareomkostninger.  

1. Vælg ikonet ![Elpære, der åbner funktionen Fortæl mig](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig"), angiv **Lageropsætning**, og vælg derefter det relaterede link.  
2. På siden **Lageropsætning** skal du slå feltet **Aut. lagerværdibogføring** til og fra eller angive **Aldrig** i feltet **Automatisk kostregulering**.  
3. I den meddelelse, der nu vises øverst på siden, skal du vælge linket **Planlæg indgangspunkt for opgavekø**. Dette åbner opsætningsvejledningen **Planlæg omkostningsregulering og bogføring**.  
4. Angiv den opgave, du vil planlægge.  

  > [!NOTE]
  > Du kan ikke oprette en ny opgavekøpost, hvis der allerede findes en opgavekøpost for den angivne opgave.

5. Vælg feltet **Vis logposterne i sagskøen, når du er færdig** for at gennemgå og justere indstillingerne. Du kan finde flere oplysninger i [Bruge opgavekøer til at planlægge opgaver](admin-job-queues-schedule-tasks.md).  

## Sådan oprettes en opgavekøpost til regulering og afstemning af lageromkostninger manuelt

Du kan også oprette opgavekøposter manuelt. Følgende fremgangsmåde viser, hvordan du angiver **Reguler kostværdi - vareposter** til at blive kørt automatisk hver dag, men de samme trin gælder for kørslen **Bogfør lagerregulering til Finans**.  

1. Vælg ikonet ![Elpære, der åbner funktionen Fortæl mig](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig"), angiv **Opgavekøposter**, og vælg derefter det relaterede link.  
2. Vælg handlingen **Ny**.  
3. I feltet **Objekttype, der skal køres** skal du vælge *Rapport*.  
4. I feltet **Objekt-id, der skal køres** skal du vælge *795*, **Regulere kostværdi - vareposter**.  
5. I feltet **Datoformel for næste kørsel** skal du indtaste *1D*.
6. I feltet **Starttidspunkt** skal du indtaste *02:00*.
7. Vælg handlingen **Angiv status til Klar**.

Nu opdateres lageromkostningen hver nat.  

Hvis du vil planlægge en opgave til afstemning af lageret med finansbogholderiet, skal du vælge kodeenhed 2846 **Bogfør lagerregulering til Finans**.

> [!TIP]
> Hvis du vil undgå låsning, skal du ikke planlægge opgaver for kørslen **Reguler kostværdi - vareposter**, codeunit **Bogfør lagerregulering til Finans** og opgaver til bogføring af salgs- eller indkøbstransaktioner på samme tid. Sørg også for, at de bruger samme opgavekøkategori.

## Se også

[Regulere varepriser](inventory-how-adjust-item-costs.md)  
[Afstemme lageromkostninger med finansregnskabet](finance-how-to-post-inventory-costs-to-the-general-ledger.md)  
[Bruge opgavekøer til at planlægge opgaver](admin-job-queues-schedule-tasks.md)  
[Søge efter sider og oplysninger med Fortæl mig](ui-search.md)  
[Arbejd med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)  
