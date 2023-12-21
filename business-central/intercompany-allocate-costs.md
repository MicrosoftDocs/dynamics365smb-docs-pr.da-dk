---
title: Allokere omkostninger til IC-partnere | Microsoft-dokumenter
description: 'Få mere at vide om, hvordan momsindstillinger for debitorer og kreditorer styrer om, og hvordan moms beregnes.'
author: brentholtorf
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: incoming document
ms.date: 04/01/2021
ms.author: bholtorf
---
# <a name="allocate-costs-to-intercompany-partners"></a>Allokere omkostninger til IC-partnere
Når du bruger Intercompany-bogføringer til at overføre dokumenter mellem partner firmaer, har momsrelaterede indstillinger (primært den momsvirksomhedsbogføringsgruppe), der er tildelt debitor-eller kreditorkontiene (associeret med IC-partneren), at bestemme, om og hvordan moms skal beregnes og registreres. Du kan også foretage omkostningsfordelinger direkte fra en købsordre til partnervirksomheder. Hvis du f.eks. registrerer en købsfaktura fra en ekstern leverandør, og du vil distribuere nogle eller alle omkostninger til en eller flere IC-partnere.

Du kan allokere omkostninger til en eller flere IC-partnere på følgende måde:

* **IC-finanskladder** – disse kladder er nyttige, når en service købes. F. eks. Når en modervirksomhed betjener en service for at opsætte computersystemer i to datterselskaber. Fakturaen sendes til moderselskabet, men omkostningerne fordeles til partnerne. Du kan finde flere oplysninger i [Arbejde med IC-dokumenter og kladder](intercompany-how-work-documents-journals.md).
* Købsordrer og fakturaer-brug af købsdokumenter er nyttige, når du f.eks. opererer med køb, f.eks. driftsudgifter, er centraliseret i ét regnskab og derefter allokeret til IC-partnerne.

## <a name="to-allocate-costs-using-an-intercompany-general-journal"></a>Sådan allokeres omkostninger vha. en IC-finanskladde
Hvis du vil angive en linje i en IC-finanskladde, skal du følge disse trin. 

1. Vælg ![Lightbulb, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **Koncerninterne finanskladder**, og vælg derefter det relaterede link.
2. Hvis det er nødvendigt, skal du angive **Eksternt bilagsnr.** i feltet på fakturaen fra kreditoren.
3. Marker **Dokumenttype** i feltet og vælg **faktura**.
4. I feltet **Kontotype** skal du vælge **Kreditor**.
5. I feltet **Kontotype** skal du vælge Kreditor.
6. I feltet **Beløb** skal du angive et negativt beløb, der er lig med beløbet på fakturaen.
7. Indtast i feltet **Modkontotype** **Finanskonto**.
8. Få vist en oversigt over de relevante modkontonummer i feltet **Modkonto**.
9. Hvis du vil fordele omkostninger til IC-partnere, skal du følge disse trin:
   1. Opret en ny linje.
   2. Undlad at udfylde feltet **Dokumenttype**, og vælg den indstilling, der lader feltet være tomt.
   3. I feltet **Dokumentnr.** skal du angive et tal, der er forskelligt fra nummeret i feltet **Eksternt dokumentnr.** Omkostningstildelingen betragtes som en anden transaktion.
   4. I feltet **Kontotype** skal du vælge **IC-partner**.
   5. I feltet **Konktonr.** skal du vælge den IC-partner, som omkostningen skal allokeres til.
   6. Indtast i feltet **Modkontotype** **Finanskonto**.
   7. I feltet I **Modkonto** skal du vælge den finanskonto, som du vil bogføre det beløb, du modtager fra IC-partneren.
   1. I feltet **Beløb** skal du angive beløbet på den faktura, der skal fordeles til IC-partneren.
   1. I feltet **IC-partner finanskontonr.** skal du vælge den finanskonto, hvor du vil bogføre beløbet fra IC-partneren. 
   1. Udfyld de resterende felter efter behov. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)] Gentag disse trin for hver IC-partner, der skal dele i omkostningen.
1. Hvis du vil bogføre dokumentet og allokere omkostningerne, skal du vælge **Bogfør**.  

## <a name="to-allocate-costs-using-a-purchase-document"></a>Sådan allokeres omkostninger ved hjælp af et købsdokument
Følgende procedure beskriver, hvordan du allokerer omkostninger ved hjælp af en købsfaktura. Fremgangsmåden er den samme for købsordrer.

> [!NOTE]
> Hvis du vil udføre disse trin, skal du tilpasse siden **Købsfaktura** ved at tilføje felterne **IC-partnerkode**, **IC-partner Ref. type** og **IC-partner**. Du kan finde flere oplysninger i [Start af tilpasning af en side gennem det personlige banner](ui-personalization-user.md#start-personalizing-by-using-the-personalization-mode).

1. Vælg ![Lightbulb, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **Bogført købsfaktura**, og vælg derefter det relaterede link.
2. I feltet **Type** skal du vælge **Finanskonto**.
   
   Finanskonto er den eneste mulighed, du kan bruge til at allokere omkostninger.  
1. I feltet **Nummer** I feltet Type skal du vælge Finanskonto.
1. I feltet **IC-partnerkode** skal du vælge den IC-partner, som omkostningen skal allokeres til.
1. I **IC-parter Ref. type** skal du vælge den finanskonto, der skal bruges til tildelingen. Denne konto knytter udgiften til en konto i kontoplanen i intercomany-partneren.
1. I feltet **Antal** skal du angive det antal enheder, der skal faktureres til IC-partneren.
1. I feltet **Købspris Ekskl. moms (eller inkl. moms)** skal du angive den kostpris pr. vare, der skal faktureres til IC-partneren.
1. Udfyld de resterende felter efter behov. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)] 
1. Du kan bogføre købsordren ved at vælge **Bogfør**.

## <a name="to-send-the-allocated-costs-to-intercompany-partners"></a>Send de allokerede omkostninger til IC-partnere
1. Vælg ![Lightbulb, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **IC-udbakketransaktioner**, og vælg derefter det relaterede link.
2. Vælg de linjer, der skal sendes, og vælg derefter handlingen **Send til IC-partner**. 
3. Hvis du vil fordele omkostningerne, skal du vælge handlingen **Fuldfør linjehandlinger**.

## <a name="calculating-vat-for-cost-distributions"></a>Beregne moms for omkostningsfordelinger
Når du bruger et dokument til at fordele omkostninger til IC-partnere, er der to indstillinger for moms, der skal være opmærksom på følgende: 
* Indstillingerne på finanskontoen for udgifter:
   * Hvis virksomheds-eller momsvirksomhedsbogføringsgrupperne er oprettet på finanskontoen, afhænger beregningen af grupperne og produktgrupperne fra dokumentlinjen.
   * Hvis der ikke er angivet virksomheds-eller momsvirksomhedsbogføringsgrupper på finanskontoen, afhænger beregningen af følgende:
* Indstillingerne for bogføringsgruppen på IC-partneren
   * Angiver, om IC-partneren er knyttet til et debitornummer, hvor der ikke er angivet en konto for erhvervs- eller momsvirksomhedsbogføringsgrupper.
   * Der er ikke knyttet et debitornummer til IC-partneren. Derefter er finans-eller momsvirksomhedsbogføringsgrupperne tomme, og linjen i momsbogføringsopsætningen bruges, som regel en gruppe, hvor der er angivet 0 % moms.

> [!NOTE]
> Det er vigtigt at validere både IC-partneropsætningen og finanskontoopsætningen (for den udgiftskonto, der bruges til omkostningsfordelingen), før du allokerer omkostninger til IC-partnere.

## <a name="see-also"></a>Se også
[Konfigurere mellemregning](intercompany-how-setup.md)  
[Administrere Intercompany-transaktioner (IC)](intercompany-manage.md)  
[Finans](finance.md)  
[Konfigurere Finans](finance-setup-finance.md)  
[Arbejde med finanskladder](ui-work-general-journals.md)  
[Arbejd med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)

[!INCLUDE[footer-include](includes/footer-banner.md)]
