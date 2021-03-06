---
title: Indsende momsrapporter til skattemyndigheder | Microsoft Docs
description: Få at vide, hvordan du udarbejder rapporter over moms fra salg i en periode eller fra salg og indkøb og sender rapporten til en skattemyndighed.
author: bholtorf
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: VAT, tax, report, EC sales list, statement
ms.date: 10/01/2020
ms.author: bholtorf
ms.openlocfilehash: eabb6962dba09e7837e271f3ad2d6b14313941e3
ms.sourcegitcommit: 2e7307fbe1eb3b34d0ad9356226a19409054a402
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 12/17/2020
ms.locfileid: "4746912"
---
# <a name="report-vat-to-tax-authorities"></a>Rapportere moms til skattemyndighederne
Dette emne beskriver rapporterne i [!INCLUDE[prod_short](includes/prod_short.md)], som du kan bruge til at indsende oplysninger om momsbeløb for salg og indkøb til skattemyndigheder i dit område. 

Du kan bruge følgende rapporter:

* Rapportlisterne **Oversigt over EU-salg** fra det Europæiske Fællesskab (EU) viser de momsbeløb, du har indsamlet for salg til momsregistrerede debitorer i EU-lande.  
* Rapporten **Momsangivelse** inkluderer moms for salg og køb til kunder og fra leverandører i alle lande, der bruger moms.

Du kan få vist en komplet oversigt over momsposter ved hver bogføring, der indebærer moms, hvor der oprettes en post på siden **Momsposter**. Disse poster bruges til at beregne momsafregningsbeløb, f.eks. betaling og refusion, for en bestemt periode. Du kan få vist VAT-poster ved at vælge ikonet ![Elpære, der åbner funktionen Fortæl mig](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") og angive **Momsposter** og derefter vælge det relaterede link.

> [!NOTE]
> Hvert [!INCLUDE[prod_short](includes/prod_short.md)]-miljø skal behandle lovpligtig rapportering i ét enkelt land. Den hollandske version af [!INCLUDE[prod_short](includes/prod_short.md)] håndterer momsrapportering i Holland, men ikke i andre lande. På samme måde håndterer den amerikanske version af [!INCLUDE[prod_short](includes/prod_short.md)] 1099 rapportering i USA og understøtter ikke krav om momsindberetning i andre lande, medmindre de er indført via en udvidelse, der leveres af vores partnerøkosystem eller en kundespecifik kodeændring.

## <a name="about-the-ec-sales-list-report"></a>Om rapporten Oversigt over EU-salg
I Storbritannien skal alle virksomheder, der sælger varer og tjenester til momsregistrerede kunder, herunder kunder i andre EU-lande, sende en elektronisk udgave af rapporten Oversigt over EU-salg i XML-format via HMRC-webstedet (Her Majesty's Revenue and Customs). Rapporten Oversigt over EU-salg kan kun bruges til EU-lande.

Rapporten indeholder én linje for hver type transaktion med kunden og viser det samlede beløb for hver transaktionstype. Rapporten kan indeholde tre typer transaktioner:  

* B2B-varer  
* B2B-tjenester  
* B2B triangulerede varer  

B2B-varer og -tjenesteydelser angiver, om du har solgt en vare eller en tjeneste, og de styres af indstillingen **EU-service** i momsbogføringsopsætningen. B2B-triangulerede varer angiver, om du har drevet handel med tredjepart, og styres af indstillingen **Trekantshandel** i salgsdokumenter, f.eks. salgsordrer, fakturaer, kreditnotaer osv.  

Når skattemyndighederne gennemser rapporten, sender de en e-mail til kontaktpersonen for virksomheden. I [!INCLUDE[prod_short](includes/prod_short.md)] angives kontaktpersonen på siden **Virksomhedsoplysninger**. Før du sender rapporten, skal du kontrollere, at der er valgt en kontaktperson.

## <a name="about-the-vat-return-report"></a>Om rapporten Momsopgørelse
Du kan bruge denne rapport til at sende moms for salgs- og købsdokumenter, f.eks. købs- og salgsordrer, fakturaer og kreditnotaer. Oplysningerne i rapporten er opstillet på samme måde som i listeangivelsen fra SKAT.  

Moms beregnes på basis af momsbogføringsopsætningen og de momsbogføringsgrupper, du har oprettet.

For momsopgørelsen kan du angive, at posterne skal omfatte:

* Send kun åbne transaktioner, eller åbne og lukkede. Dette er f.eks. nyttigt, når du forbereder din endelige årlige momsopgørelse.
* Send kun poster fra de angivne perioder, eller medtag også poster fra tidligere perioder. Dette er nyttigt for at opdatere en momsopgørelse, som du allerede har sendt, f.eks. hvis en leverandør sender dig en forsinket faktura.    

## <a name="to-connect-to-your-tax-authoritys-web-service"></a>Sådan opretter du forbindelse til din skattemyndigheds webtjeneste
[!INCLUDE[prod_short](includes/prod_short.md)] indeholder serviceforbindelser til skattemyndighedernes websteder. Hvis du f.eks. befinder dig i Storbritannien, kan du aktivere serviceforbindelsen **GovTalk** for at sende rapporterne Oversigt over EU-salg og Momsopgørelsen elektronisk. Hvis du vil sende rapporten manuelt, for eksempel ved at indtaste dataene på skattemyndighedens websted, er dette ikke påkrævet.   

Når du vil rapportere moms til en skattemyndighed elektronisk, skal du forbinde [!INCLUDE[prod_short](includes/prod_short.md)] med skattemyndighedens webtjeneste. Dette kræver, at du opretter en konto hos skattemyndighederne. Når du har en konto, kan du aktivere en tjenesteforbindelse, som vi leverer i [!INCLUDE[prod_short](includes/prod_short.md)].

1. Vælg ikonet ![Elpære, der åbner funktionen Fortæl mig](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig"), angiv **Serviceforbindelser**, og vælg derefter det relaterede link.
2. Udfyld de påkrævede felter. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]  

    > [!NOTE]  
    > Det er en god ide at teste forbindelsen. For at gøre dette skal du vælge afkrydsningsfeltet **Testtilstand**. Forbered og send derefter momsrapporten, som beskrevet i afsnittet _Sådan forbereder og sender du en momsrapport_. I Testtilstand kontrollerer tjenesten, om skattemyndighederne kan modtage rapporten, og statussen for rapporten angiver, om testafsendelsen blev udført. Det er vigtigt at huske, at det ikke er en faktisk afsendelse. For at sende rapporten rigtigt skal du fjerne markeringen i afkrydsningsfeltet **Testtilstand** og derefter gentage afsendelsesprocessen.

## <a name="to-set-up-vat-reports-in-prod_short"></a>Sådan opsættes momsrapporter i [!INCLUDE[prod_short](includes/prod_short.md)]
1. Vælg ikonet ![Elpære, der åbner funktionen Fortæl mig](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig"), angiv **Momsrapportkonfiguration**, og vælg derefter det relaterede link.  
2. For at vil lade brugerne ændre rapporten og sende den igen skal du markere afkrydsningsfeltet **Modificer sendte rapporter**.  
3. Vælg den nummerserie, der skal bruges til hver rapport.  

## <a name="to-prepare-and-submit-a-vat-report"></a>Sådan forbereder og sender du en momsrapport
1. Vælg ikonet ![Elpære, der åbner funktionen Fortæl mig](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig"), angiv **Oversigt over EU-salg** eller **Momsopgørelse**, og vælg derefter det relaterede link.  
2. Vælg **Ny**, og udfyld de påkrævede felter. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
3. For at generere oplysningerne i rapporten skal du vælge handlingen **Foreslå linjer**.  

    > [!NOTE]  
    >   For rapporten Oversigt over EU-salg kan du gennemse transaktionerne i rapportlinjerne, inden du sender rapporten. Det gør du ved at vælge linjen og derefter vælge handlingen **Vis momsposter**.  
4. Hvis du vil validere og forberede rapporten til afsendelse, skal du vælge handlingen **Frigiv**.  

    > [!NOTE]  
    > [!INCLUDE[prod_short](includes/prod_short.md)] kontrollerer, om rapporten er konfigureret korrekt. Hvis valideringen ikke lykkes, vises fejlene under **Fejl og advarsler**, så du ved, hvad du skal rette. Hvis meddelelsen typisk drejer sig om en manglende indstilling i [!INCLUDE[prod_short](includes/prod_short.md)], kan du klikke på meddelelsen for at åbne siden med de oplysninger, der skal rettes.  
5. Du sender rapporten ved at vælge handlingen **Send**.  

Når du sender rapporten, overvåger [!INCLUDE[prod_short](includes/prod_short.md)] tjenesten og registrerer din kommunikation. Feltet **Status** angiver, hvor rapporten er i processen. F.eks. når myndighederne behandler rapporten, ændres status for rapporten til **Fuldført**. Hvis skattemyndighederne finder fejl i den rapport, du har sendt, bliver status for rapporten **Mislykkedes**. Du kan se fejlene under **Fejl og advarsler**, rette dem og derefter sende rapporten igen. For at få vist en liste over alle EU-salgslisterapporter, skal du gå til siden **Rapporter over EU-salg**.  

## <a name="viewing-communications-with-your-tax-authority"></a>Visning af kommunikationen med skattemyndighederne
I nogle lande udveksler du meddelelser med skattemyndighederne, når du sender rapporter. Du kan få vist først og sidste meddelelse, du har sendt eller modtaget, ved at vælge handlingerne **Download afsendelsesmeddelelse** og **Download svarmeddelelse**.  

## <a name="submitting-vat-reports-manually"></a>Sende momsrapporter manuelt
Hvis du bruger en anden metode til at sende rapporten, f.eks. ved at eksportere XML-filen og overføre den til en skattemyndighedens websted, kan du vælge **Marker som sendt** for at afslutte rapporteringsperioden. Når du har markeret rapporten som udgivet, kan den ikke redigeres. Hvis du har brug for at ændre rapporten efter, at den er markeret som udgivet, skal du åbne den.

## <a name="vat-settlement"></a>Momsafregning
Du skal med jævne mellemrum betale nettomomsen til skattemyndighederne. Når du skal afregne moms jævnligt, kan du udføre kørslen **Afregn moms** for at lukke de åbne momsposter og overføre købs- og salgsmomsbeløb til momsafregningskontoen.

Når du overfører momsbeløb til afregningskontoen, bliver købsmomskontoen krediteret, og salgsmomskontoen debiteres de beløb, der er beregnet for den angivne periode. Nettobeløbet krediteres eller debiteres momsafregningskontoen, hvis købsmomsbeløbet er større. Du kan bogføre afregningen med det samme eller udskrive en kontrolrapport først.  

> [!Note]
> Når du bruger kørslen **Afregn moms**, hvis du ikke angiver en **Momsvirksomhedsbogf.gruppe** og en **Momsproduktbogf.gruppe**, medtages poster med alle virksomhedsbogføringsgrupper og produktbogføringsgruppekoder.

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

> [!Note]
> Når du opretter kodeenheder til rapporten, skal du være opmærksom på værdien i feltet **Momsrapportversion**. Dette felt skal afspejle versionen af den rapport, der blev/bliver krævet af skattemyndighederne. Du kan f.eks. angive **2017** i feltet for at angive, at rapporten opfylder kravene for dette år. For at finde den aktuelle version skal du kontakte skattemyndighederne.

## <a name="see-related-training-at-microsoft-learn"></a>Se relateret oplæring på [Microsoft Learn](/learn/paths/process-vat-dynamics-365-business-central/)

## <a name="see-also"></a>Se også
[Konfigurere beregnings- og bogføringsmetoder for moms](finance-setup-vat.md)  
[Arbejde med moms af salg og køb](finance-work-with-vat.md)  
[Konfigurere salg](sales-setup-sales.md)  
[Fakturere salg](sales-how-invoice-sales.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]