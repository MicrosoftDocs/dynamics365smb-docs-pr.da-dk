---
title: Administrere momsrapportering til skattemyndigheder | Microsoft Docs
description: "Få at vide, hvordan du udarbejder en rapport over moms fra salg i en periode, og sender rapporten til en skattemyndighed."
services: project-madeira
documentationcenter: 
author: bholtorf
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: VAT, tax, report, EC sales list, statement
ms.date: 06/02/2017
ms.author: bholtorf
ms.translationtype: Human Translation
ms.sourcegitcommit: 81636fc2e661bd9b07c54da1cd5d0d27e30d01a2
ms.openlocfilehash: 9b0db56fc08881a94b1f80bafed32d7bcbc24fd8
ms.contentlocale: da-dk
ms.lasthandoff: 07/07/2017


---

# <a name="how-to-report-vat-to-tax-authorities"></a>Fremgangsmåde: Rapportere moms til skattemyndighederne
Rapportlisterne i salgsoversigten fra Det Europæiske Fællesskab (EU) indeholder momsbeløb, som du har indsamlet for salg inden for EU, så du kan sende momsbeløbene til en skattemyndigheds webtjeneste.

> [!NOTE]  
>   I Storbritannien skal alle virksomheder, der sælger mere end en bestemt værdi hvert år til kunder i EU-medlemsstater, sende en elektronisk version af deres EU-salgslisterapport i XML-format via HMRC-webstedet (Her Majesty's Revenue and Customs).

EU-salgslisterapporten kan kun bruges til EU-lande. F.eks. omfatter den ikke moms på salg til lande som Kina eller USA.

Når du vil rapportere moms til en skattemyndighed elektronisk, skal du forbinde [!INCLUDE[d365fin](includes/d365fin_md.md)] med skattemyndighedens webtjeneste. Dette kræver, at du opretter en konto hos skattemyndighederne. Når du har en konto, kan du aktivere en tjenesteforbindelse, som vi leverer i [!INCLUDE[d365fin](includes/d365fin_md.md)]. F.eks. kan du i Storbritannien bruge **GovTalk**-tjenesteforbindelsen.

Rapporten indeholder én linje for hver type transaktion med kunden og viser det samlede beløb for hver transaktionstype. Rapporten kan indeholde tre typer transaktioner:  
  
* B2B-varer  
* B2B-tjenester  
* B2B triangulerede varer  
  
B2B-varer og -tjenesteydelser angiver, om du har solgt en vare eller en tjeneste, og de styres af indstillingen **EU-service** i momsbogføringsopsætningen. B2B-triangulerede varer angiver, om du har drevet handel med tredjepart. Det styres af indstillingen **Trekantshandel** i salgsdokumenter, f.eks. salgsordrer, fakturaer, kreditnotaer osv.  
  
Når du sender rapporten, overvåger [!INCLUDE[d365fin](includes/d365fin_md.md)] tjenesten og registrerer din kommunikation. Feltet **Status** angiver, hvor rapporten er i processen. F.eks. når myndighederne behandler rapporten, ændres status for rapporten til **Fuldført**. Hvis skattemyndighederne finder fejl i den rapport, du har sendt, bliver status for rapporten **Mislykkedes**. Du kan se fejlene under **Fejl og advarsler**, rette dem og derefter sende rapporten igen. For at få vist en liste over alle EU-salgslisterapporter, skal du gå til siden **Rapporter over EU-salg**.  
  
> [!NOTE]  
>   Hvis du bruger en anden metode til at sende rapporten, f.eks. ved at eksportere XML-filen og overføre den til en skattemyndighedens websted, kan du vælge **Marker som sendt** for at afslutte rapporteringsperioden. Når du har markeret rapporten som udgivet, kan den ikke redigeres. Hvis du har brug for at ændre rapporten efter, at den er markeret som udgivet, skal du åbne den. 
  
Når skattemyndighederne gennemser rapporten, sender de en e-mail til kontaktpersonen for virksomheden. I [!INCLUDE[d365fin](includes/d365fin_md.md)] angives kontaktpersonen på siden **Virksomhedsoplysninger**. Før du sender rapporten, skal du kontrollere, at der er valgt en kontaktperson.

<!--> [!NOTE]  
>   EU-salgslisterapporten kan indeholde op til 1000 linjer. Hvis du har flere linjer, skal du sende en anden rapport. -->

## <a name="to-connect-to-your-tax-authoritys-web-service"></a>Sådan opretter du forbindelse til din skattemyndigheds webtjeneste
[!INCLUDE[d365fin](includes/d365fin_md.md)] indeholder tjenester, der har forbindelse til skattemyndighedernes websteder. F.eks. hvis du er i Storbritannien skal du aktivere **GovTalk**-tjenesteforbindelsen.  

1. I feltet **Søg efter sider eller rapporter** skal du angive **Tjenesteforbindelser** og derefter vælge relevante link. <!-- remember to get the updated text for this-->  
2. Udfyld de påkrævede felter.  

## <a name="to-set-up-the-ec-sales-list-report"></a>Sådan defineres EU-salgslisterapporten
1. I feltet **Søg efter sider eller rapporter** skal du angive **Momsrapportopsætning** og derefter vælge det relaterede link.  
2. Hvis du vil lade brugerne ændre rapporten og sende den igen, skal du markere afkrydsningsfeltet **Modificer sendte rapporter**.  
3. Angiv den nummerserie, der skal bruges til EU-salgslisterapporter.  

## <a name="to-prepare-and-submit-the-ec-sales-list-report"></a>Udarbejde og sende EU-salgslisterapporten
1. I feltet **Søg efter sider eller rapporter** skal du angive **Oversigt over EU-salg** og derefter vælge det relaterede link.  
2. Vælg **Ny**, og udfyld de påkrævede felter.  
3. For at generere oplysningerne i rapporten skal du vælge handlingen **Foreslå linjer**.  

    > [!NOTE]  
>   Du kan se de transaktioner, der indgår på linjen, inden du sender rapporten. Det gør du ved at vælge linjen og derefter vælge handlingen **Vis momsposter**.  
4. Du gør klar til at sende rapporten ved at vælge handlingen **Frigiv**.  
5. Du sender rapporten ved at vælge handlingen **Send**.  
  
[!INCLUDE[d365fin](includes/d365fin_md.md)] kontrollerer, om rapporten er konfigureret korrekt. Hvis valideringen ikke lykkes, vises fejlene under **Fejl og advarsler**, så du kan foretage de nødvendige ændringer.

## <a name="viewing-communications-with-your-tax-authority"></a>Visning af kommunikationen med skattemyndighederne
I nogle lande udveksler du meddelelser med skattemyndighederne, når du sender rapporter. Du kan få vist først og sidste meddelelse, du har sendt eller modtaget, ved at vælge handlingerne **Download afsendelsesmeddelelse** og **Download svarmeddelelse**.  

## <a name="configuring-your-own-vat-reports"></a>Konfigurere dine egne momsrapporter
Du kan bruge standard-EU-salgslisterapporten, men du kan også oprette dine egne rapporter. Dette kræver, at du opretter et par kodeenheder. Hvis du har brug for hjælp til dette, skal du kontakte en Microsoft-partner.  
    
I følgende tabel beskrives kodeenheder, du skal oprette til rapporten.

| Codeunit | Dette skal den gøre |
|----|-----|
|Foreslå linjer| Hente oplysninger fra tabellen Momsposter og vise dem i linjerne i momsrapporten.|
|Indhold | Kontrollere rapportens format. F.eks. om det er XML eller JSON. Formatet afhænger af kravene i din skattemyndigheds webtjeneste. |
|Afsendelse | Styre, hvordan og hvornår du sender rapporten ud fra skattemyndighedernes krav. |
|Svarhandler | Håndtere skattemyndighedernes returnering. Der kan f.eks. blive sendt en e-mail til kontaktpersonen i din virksomhed. |
|Annuller | Sende en annullering af en momsrapport, der tidligere blev sendt til skattemyndighederne. |

> [!NOTE]  
>   Når du opretter kodeenheder til rapporten, skal du være opmærksom på værdien i feltet **Momsrapportversion**. Dette felt skal afspejle versionen af den rapport, der blev/bliver krævet af skattemyndighederne. Du kan f.eks. angive **2017** i feltet for at angive, at rapporten opfylder kravene for dette år. For at finde den aktuelle version skal du kontakte skattemyndighederne.  

## <a name="see-also"></a>Se også
[Angive indstillinger for moms](finance-setup-vat.md)  
[Konfigurere salg](sales-setup-sales.md)  
[Fremgangsmåde: Fakturere salg](sales-setup-sales.md)  

