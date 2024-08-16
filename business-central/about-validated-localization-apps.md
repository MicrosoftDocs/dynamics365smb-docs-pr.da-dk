---
title: Udvikling af validerede lokaliseringsapps
description: Overhold lovmæssige krav i Dynamics 365 Business Central som en valideret lokaliseringsapp.
author: altotovi
ms.date: 06/04/2024
ms.reviewer: bholtorf
ms.topic: conceptual
ms.author: altotovi
---

# Udvikling af validerede lokaliseringsapps

I denne artikel beskrives kravene og retningslinjerne til udvikling af en valideret lokaliseringsapp til [!INCLUDE[prod_short](includes/prod_short.md)].

## Hvad er en valideret lokaliseringsapp?

[!INCLUDE[prod_short](includes/prod_short.md)] er tilgængelig [globalt på 170+ markeder](/dynamics365/business-central/dev-itpro/compliance/apptest-countries-and-translations?toc=/dynamics365/business-central/toc.json). På en række markeder samarbejder Microsoft med ISV-partnere om at lokalisere [!INCLUDE[prod_short](includes/prod_short.md)] via lokaliseringsapps, der er tilgængelige på [Microsoft AppSource](https://go.microsoft.com/fwlink/?linkid=2081646). I disse områder kan lokaliseringer være tilgængelige via foretrukket lokaliseringsappprogram. Programmet Foretrukne lokaliseringsapps genkender de apps, der er bygget i henhold til Microsofts specifikke retningslinjer for kvalitet. ISV-partnere, der overholder disse programkrav og retningslinjer, kan med teknisk og kommerciel fordel betjene deres forhandlere og kunder.  

I de følgende afsnit kan du finde krav og retningslinjer. Du kan kontakte programteamet, hvis du ønsker at deltage i dette program og overholde nedenstående krav, ved at kontakte os via [Microsofts lokaliseringsteam](mailto:d365bcloc@microsoft.com).   

> [!IMPORTANT]
> Initiativet [!INCLUDE[prod_short](includes/prod_short.md)] Validerede lokaliseringsapps er i øjeblikket ved at blive rullet ud som et pilotprogram. Nedenstående krav og fordele kan ændre sig baseret på partnerens og kundens feedback.  

Apps i pilotprogrammet for valideret lokalisering indeholder et sæt funktioner, der imødekommer lokale lovkrav, der falder inden for en af kategorierne på følgende liste.  

- **Lovgivningsmæssige krav** – lokal funktionalitet, der hjælper virksomheder med at opfylde deres juridiske krav, f.eks. skatterapportering, lokale e-faktureringsformater, lokale GAAP og andre lovkrav.
- **Krav til nationale standarder** – lokal funktionalitet, der adresserer lokale standarder, f.eks. adresseformater, nationale bankformater eller lokale fortolkninger af globale standarder.
- **Lokalt sprog** – lokalt sprog i lokaliseringsappen, men også for en basisapp, hvis dette sprog ikke aktuelt er på listen over [understøttede sprog](/dynamics365/business-central/dev-itpro/compliance/apptest-countries-and-translations?toc=/dynamics365/business-central/toc.json).

> [!NOTE]
> Lokale markedsbehov eller branchekrav bør ikke inkluderes i de foretrukne lokaliseringsapps. Hvis apps indeholder disse funktioner, kan apps ikke godkendes som validerede lokaliseringsapps.

> [!NOTE]
> Lokal funktionalitet er gavnlig for produktivitetsforretningsprocesserne i et land og tilføjer dermed værdi til forretningen, men er ikke påkrævet ud fra et lovgivningsmæssigt perspektiv, såsom specifikke bank- og betalingsformater, udgiftsrapporter, HR-funktioner, lønningsliste og lignende mindre eller større, og nice-to-have-funktioner bør isoleres i andre apps. Hvis apps indeholder disse funktioner, godkendes de ikke som validerede lokaliseringsapps.   

## Krav til validerede forretningskrav til lokaliseringsapps  

- Udbyderen af appen Valideret lokalisering overholder alle krav for at være indirekte CSP-udbyder.  
- Udbyderen af appen til valideret lokalisering markedsfører mindst fem lande/områder, som leveres Dynamics 365 Business Central sammen med en valideret lokaliseringsapp. 
- Udbyderen af appen Valideret lokalisering har mindst 10 [!INCLUDE[prod_short](includes/prod_short.md)] onlinekunder med produktionsmiljøer, som aktivt bruger appen Valideret lokalisering. 
- Udbyderen af appen til valideret lokalisering sender årligt en forretningsplan til programmet v-team. Dette omfatter planlagte markedsførings- og parathedsaktiviteter for at promovere det pakkede tilbud med CSP's indirekte forhandlere i relevante lande/områder. Planen kan sendes i starten af hvert kvartal til [Microsofts lokaliseringsteam](mailto:d365bcloc@microsoft.com).  
- Validerede lokaliseringsapps gøres tilgængelige for alle kunder og partnere, der ønsker at drage fordel af dem.     
- Udbyderen af appen til valideret lokalisering deltager i tilbagevendende arbejdsstrømme med Microsoft.

## Funktionelle og tekniske krav til valideret lokaliseringsapp  

### Krav til funktionalitet   

Ud over at opfylde de tekniske krav til den foretrukne lokaliseringsapp er det mindst levedygtige produktomfang for foretrukken lokaliseringsapp:  

- Regionale lovpligtige funktioner:   
  - Lovgivningsmæssige krav.   
  - Officielt obligatoriske funktioner. 
  - Kun horisontale funktioner (ikke branchespecifikke).  
  - Gælder i de fleste virksomheder.  
  - Inden for følgende Blueprint:   
    - Områder med de hyppigste lovændringer. 
    - Allerede sporet som en lokalisering i Microsoft-lokaliseringer. 
    - Funktionsreferencer – sjældent nye.  
    - Ingen leverandør/bankspecifikke formater, løn eller lignende. 
    - Ingen globale funktioner, hvis de ikke er bygget af Microsoft. 
- Oversættelser: 
  - Oversættelse af en lokaliseringsapp til lokale sprog. 
  - Oversættelse af en basisapp til lokale sprog – hvis sprog ikke allerede [understøttes](/dynamics365/business-central/dev-itpro/compliance/apptest-countries-and-translations?toc=/dynamics365/business-central/toc.json).  
  - Oversættelse af en lokaliseringsapp til lokale sprog. 
- Selvom de begge er en del af lokaliseringen, anbefales det, at nationale standardfunktioner (lokal del) bygges som separate apps fra lokale lovgivningsmæssige funktioner. 
- Demodata på det lokale sprog, der gælder for det specifikke marked.   
- Alle funktioner skal være designet til at holde forenklet brugergrænseflade, bemærk at de primært er beregnet til SMB-markedet.  
- Undgå at oprette nye funktioner, hvis de samme eller lignende funktioner allerede findes i basisappen, f.eks. elektronisk fakturering, revisionseksport, momsfunktioner, dataudveksling og andet, hvor de fleste funktioner er fælles for alle lande/områder, men der er nogle lokale regler eller forretningsformater, der er udvidelser af globale strukturer eller formater. I stedet for at bygge nye funktioner, skal du udvide eksisterende.  
- Forbered opsætningsvejledninger (guider) til områder, der er komplekse at konfigurere, for at hjælpe brugerne med at aktivere, opdage og få en god første oplevelse med at bruge din lokaliseringsapp.  
- Partnere skal levere funktionel dokumentation for alle aspekter af deres lokalisering.  

### Tekniske krav  

Det følgende er en kontrolliste over alle de krav, du skal opfylde, før du sender en valideret lokaliseringsapp som udvidelse til validering. Denne liste ændrer ikke [listen over tekniske valideringer](/dynamics365/business-central/dev-itpro/developer/devenv-checklist-submission) og udvider kun kravene derfra.  

- Udbydere af validerede lokaliseringsapps skal bygge appen Valideret lokalisering baseret på W1-basisappen.  
- Udbyderne af validerede lokaliseringsapps skal følge Microsofts livscyklus- og supportpolitikker.   
- Obligatorisk testautomatisering skal dække mindst 80 % af koden, og alle forretningsprocesser, der ændres med appen Valideret lokalisering, skal være dækket af testautomatisering.  
- Udbyderne af validerede lokaliseringsapps skal opdatere og/eller teste appen Valideret lokalisering før den officielle lancering af den nye udgivelse (minimum med RC før ny version) for at bekræfte, at der ikke er nogen problemer. 
- Alle objekter i appkoden til valideret lokalisering skal være på engelsk.   
- Udbyderne af validerede lokaliseringsapps skal følge Microsofts politik for forældede objekter og banebrydende ændringer og bedste fremgangsmåder for udfasning af AL-koden.  
- Udbydere af validerede lokaliseringsapps bør tilføje nye hændelser, hvis markedet (andre implementeringspartnere eller kunder) kræver det, hvis det giver rimelig forretningsmæssig mening i overensstemmelse med Microsofts politik og praksis. Ellers skal de validerede udbydere af lokaliseringsapps besvare sådanne forespørgsler med behørig begrundelse for, hvorfor det ikke giver rimelig forretningsmæssig mening at tilføje. 
- Udbyderen af appen Valideret lokalisering skal levere skriftlige testscenarier på engelsk og give Microsoft mulighed for at udføre manuelle test, hvis Microsoft kræver det.  
- Hvis en valideret lokaliseringsapp udvider [!INCLUDE[prod_short](includes/prod_short.md)] datamodellen med nye tabeller og/eller felter, skal udbyderen af appen Valideret lokalisering angive egenskaben **Dataklassificering** korrekt.

> [!NOTE]  
> Du kan også oprette en integration, hvis du finder det fordelagtigt at have nogle funktioner placeret uden for [!INCLUDE[prod_short](includes/prod_short.md)]-miljøet og i stedet oprette forbindelse til at [!INCLUDE[prod_short](includes/prod_short.md)] bruge for eksempel API'er eller webtjenester.

## Se også

[Teknisk validering](/dynamics365/business-central/dev-itpro/developer/devenv-checklist-submission)  
[Udvikling af en standardlokaliseringsløsning](/dynamics365/business-central/dev-itpro/developer/readiness/readiness-develop-localization)  
[Tilgængelighed i land/område og understøttede sprog](/dynamics365/business-central/dev-itpro/compliance/apptest-countries-and-translations)  
[Hvad er lokal funktionalitet i Dynamics 365 [!INCLUDE[prod_short](includes/prod_short.md)]?](about-localization.md)  
[International tilgængelighed af Microsoft Dynamics 365](/dynamics365/get-started/availability)  
[Oversigt over overholdelse](compliance/compliance-overview.md)  
[Geografisk tilgængelighed for Dynamics 365](https://releaseplans.microsoft.com/availability-reports/?report=productgeoreport/)  
