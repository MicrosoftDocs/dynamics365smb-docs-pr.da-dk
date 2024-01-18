---
title: Introduktion til Contoso Coffee til Projektstyring
description: Denne artikel introducerer dig til Consoso Coffee demonstrationsdata for job og projektledelse.
author: andreipanko
ms.author: andreipa
ms.topic: how-to
ms.date: 05/31/2023
ms.custom: bap-template
---

# Introduktion til Contoso Coffee-jobs og Projektstyring

Contoso Coffee er en fiktiv virksomhed, der producerer forbruger- og kommercielle kaffemaskine. Apps **Contoso Coffee** til Business Central tilføjer demodata, som du kan bruge til at lære, hvordan du bruger funktionerne i jobs og projektstyring i Business central.

Denne app indeholder flere elementer, der bruges til de vigtigste gennemgange:

- Ressourcer med tildelte færdigheder og zoner
- varer konfigureres til at oprette serviceartikler

> [!IMPORTANT]
> Før du udfører et af scenarierne for Contoso Coffee, skal du bogføre alle varekladdelinjer med primosaldi. Du kan finde flere krav i afsnittet [Opsætning af Contoso Coffee-data](#set-up-contoso-coffee-jobs-and-project-management-data).
>
> 
## Konkfigurere Contoso Coffee-jobs og Projektstyringsdata

[!INCLUDE [contoso-coffee-app-install](../../includes/contoso-coffee-app-install.md)]

Når de relevante apps er installeret, skal du gå til [Contoso Coffee-jobs - demodata](https://businesscentral.dynamics.com/?page=4767)-siden i [!INCLUDE [prod_short](../../includes/prod_short.md)] og ændre standardindstillingerne, så de passer til dine behov. Følgende tabeller beskriver indstillingerne:  

|Felt  |Beskrivlse  |
|---------|---------|
|**Startår** |Angiver det første år, du vil bruge til demonstrationsdataene fra Contoso Coffee. Afhængigt af virksomhedens opsætning er året enten et kalenderår eller et regnskabsår.|
|**Debitornr.**  |Kunden, der skal bruge scenarier i forbindelse med salg.|
|**Varenr. 1**  |Den vare, der skal bruges til kontraktscenarier.|
|**Varenr. 2**  |Den vare, der skal bruges til breakfix-scenarier.|
|**Ressource-lokal 1 nr.**  |Den ressource, der skal bruges til kontraktscenarier.|
|**Ekstern ressource 1 nr.**  |Den ressource, der skal bruges til breakfix-scenarier.|
|**Debitorbogføringsgruppe**|Angiver en forretningskode for indenlandske debitorer. Forretnings koderne bruges, når transaktionerne bogføres. |
|**Kunde Generel virksomhedsbogføringsgruppe**|Angiver en forretningskode for indenlandske debitorer. Forretnings koderne bruges, når transaktionerne bogføres. |
|**Indlands – Virksomhedsbogføringsgruppe**|Angiver en forretnings kode for indenlandske debitorer og kreditorer. Forretnings koderne bruges, når transaktionerne bogføres. |
|**Videresalg – Varebogføringsgruppe**    |Angiver en kode for varer, der skal bruges til bogføringsvideresalg.|
|**Detail – Generel produktbogføringsgruppe**    |Angiver en kode for varer, der skal bruges til bogføringsdetail.|
|**Momsproduktbogf.gruppe**    |Angiver en momsproduktkode til varer til bogføring af moms, hvis moms er aktiveret.|
|**Prisfaktor**     |Angiver en faktor, der skal omregnes til en pris fra USD/EUR til den lokale valuta. *1* betyder, at prisen er det samme beløb i alle valutaer. Der bruges et højere nummer til at beregne prisen i den lokale valuta. |
|**Afrundingspræcision**  |Definerer, hvordan beregnede forbrugsmængder skal afrundes, når de indtastes på forbrugskladdelinjer. Mængder under 0,5 nedrundes. Mængder, der er lig med eller større end 0.5 rundes op.|

Når du er færdig, skal du vælge handlingen **Opret demodata**. Det tager nogle få minutter at føje dataene til den underliggende database, men så er du klar til at køre forskellige scenarier.  

## Se også
