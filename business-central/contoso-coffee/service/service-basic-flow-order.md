---
title: Gennemgang af serviceordrer for serviceartikler
description: 'I denne artikel gennemgås flere kerneprocesser, der omfatter serviceordrer og varer.'
author: andreipa
ms.author: andreipa
ms.reviewer: andreipa
ms.topic: how-to
ms.date: 05/31/2023
ms.custom: bap-template
ms.service: dynamics-365-business-central
---

# Gennemgang af serviceordrer for serviceartikler

Denne gennemgang viser flere centrale processer:

- Oprette en ad hoc-serviceordre og registrere reparation af varen
- Levere en udlånsvare til kunden for en reparationstid
- Bogføre og fakturere serviceordrer
    
## Sådan oprettes en serviceordre

### Scenarie  

Charles, servicechefen, opretter en serviceordre til et reparationsscenarie og låner en udlånsvare ud til kunden på reparationstidspunktet.

### Trin

1. Oprette serviceordren manuelt for den vare, der skal repareres.
   1. Vælg ![Lightbulb, der åbner funktionen Fortæl mig.](../../media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") Ikon, angiv **Serviceordrer**
   2. Vælg handlingen **Ny**.
   3. Angiv **10000** i feltet Debitornr. felt
   4. Vælg **REPARATION** i feltet **Serviceordretype**.
   5. Vælg **S-100** som **varenr.** på Linjer.
2. Valgfri
   1. Vælg linjehandlingen **Fejlfinding** for at kontrollere mulige løsninger.
   2. Vælg linjehandlingen **Fejl/Løsn. Koder Relationer**
   3. Vælg *STØJ* som **symptomkode**
   4. Vælg *5-2 Høj støj under brygning* som **Fejlkode**, og luk siden. Fejlkode, løsningskoder opdateres i linjer.
3. Lån en erstatning, mens varen repareres
   1. Vælg **UDLÅNER1** som udlånernr. på linjerne. Bekræft udlånsvarens udstedelse ved at vælge **Ja** for at låne udlånsvaren ud. 
   2. Vælg funktionshandlingen **Hent std.servicekoder**, vælg standardkode, der er tilknyttet servicegruppen, og vælg **OK**.
   
### Resultater

- Der oprettes en serviceordre for varen
- Servicedokumentets log over serviceordren viser udlånsaktiviteterne.
- Udlånsvaren vil have en finanspost, der afspejler udlånet.
   

## Registrer udførte arbejde, markér udlåner som returneret.

### Scenarie  

Serviceteknikeren markerer udlånsvarer som returneret, registrerer udført arbejde.

### Trin

1. Finde serviceopgaven og registrere tid 
   1. Vælg ![Lightbulb, der åbner funktionen Fortæl mig.](../../media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, angiv **Serviceopgaver** og vælg derefter det relaterede link.
   2. Find den serviceordre, du vil angive tid for.
   3. Vælg handlingen **Varekladde**.
   4. Angiv følgende oplysninger

    |Enhedstype|Nej|Antal|
    |----|---|--------|  
    |Artikel|SER102|2|

   4. Vælg *UDFØRT* i feltet **Reparationsstatuskode**
    
2. Markér udlånsvare som returneret
   1. Vælg ![Lightbulb, der åbner funktionen Fortæl mig.](../../media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **Udlånsvarer**, og vælg derefter det relaterede link.
   2. Find udlånsvaren, der skal markeres som returneret.
   3. Vælg handlingen **Modtag** 
   4. Bekræft udlåners returnering ved at vælge **Ja** for at udlånsreturnering.
      
### Resultater

- Servicedokumentets **Log over serviceordren** viser udlånsaktiviteterne.
- Udlånsvaren har en finanspost, der afspejler kvitteringen.


### Scenarie  

Charles, servicechefen, bogfører den færdige serviceordre.

1. Find serviceordren 
   1. Vælg ikonet ![Lightbulb, der åbner funktionen Fortæl mig.](../../media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, angiv **Serviceordre** og vælg derefter det relaterede link.
   2. Find den serviceordre, som du vil bogføre.

2. Bogføre fakturaen på serviceordren
   1. Vælg handlingen **Bogfør**, udfyld serviceordren og vælg **Send og fakturer**, og vælg derefter knappen **OK**.
   2. Bekræft åbningen af den bogførte faktura ved at vælge **Ja**. 
### Resultater

- Åbn **Bogført servicefaktura** er oprettet.
- De **Serviceposter**, der tilknyttes til varen og ressourcen, oprettes

## Se også
[Gennemgang af servicekontrakter for servicevarer](service-contract-flow.md)  
[Tjeneste](../../service-service.md)
