---
title: Fejlfinding af problemer med selvbetjeningstilmelding | Microsoft Docs
description: 'Få mere at vide om de almindeligste årsager til, hvorfor du muligvis ikke kan fuldføre tilmeldingen til Business Central, og hvordan du løser problemet.'
author: brentholtorf
ms.topic: conceptual
ms.devlang: al
ms.date: 04/01/2021
ms.author: bholtorf
ms.service: dynamics-365-business-central
ms.reviewer: bholtorf
---
# Fejlfinding af selvbetjeningstilmelding
Tilmelding til [!INCLUDE[prod_short](includes/prod_short.md)] er nemt og kan udføres hurtigt. Du kan oprette en gratis konto, selvom du en eksisterende virksomhed. Denne artikel løser problemer, der måtte opstå under tilmeldingen.

## Hvilken mailadresse kan jeg bruge til Business Central?
[!INCLUDE[prod_short](includes/prod_short.md)] kræver, at du bruger en arbejds- eller skolemailadresse til at tilmelde dig. [!INCLUDE[prod_short](includes/prod_short.md)] understøtter ikke mailadresser, som leveres af forbrugermailtjenester eller telekommunikationsudbydere. Dette omfatter outlook.com, hotmail.com, gmail.com og andre.

Hvis du forsøger at tilmelde dig med en privat mailadresse, får du en meddelelse om, at du skal bruge en arbejds- eller skolemailadresse.

## Fejlfinding
I mange tilfælde kan registrering til [!INCLUDE[prod_short](includes/prod_short.md)] gøres ved at følge tilmeldingsprocessen. Der er flere årsager til, hvorfor du ikke muligvis ikke kan fuldføre selvbetjeningstilmelding. Tabellen nedenfor indeholder en oversigt over nogle af de mest almindelige årsager til, at du ikke kan fuldføre tilmeldingen, og hvordan du kan løsning disse problemer.

| Symptom/fejlmeddelelse | Årsag og løsning |
| --------------------- | -------------------- |
| Ved Microsoft 365-mailadresser, der ikke er registreret i et understøttet land, modtager du en meddelelse som den følgende under tilmeldingen:<br /><br />**Det virkede ikke, vi understøtter ikke dit land eller område endnu.** |[!INCLUDE[prod_short](includes/prod_short.md)] understøtter aktuelt kun Microsoft 365-mailkonti, der er registreret i et begrænset antal markeder. Du kan finde flere oplysninger i [Tilgængelighed i område](#regional-availability) |
| Private mailadresser, f.eks nancy@gmail.com, understøttes ikke. Du modtager en meddelelse som den følgende under tilmeldingen:<br /><br />**Du har indtastet en privat mailadresse: Du skal angive din arbejdsmailadresse, så vi kan opbevare virksomhedens data sikkert.**<br> eller <br> **Det ligner en privat mailadresse. Angiv din arbejdsmailadresse, så vi kan oprette forbindelse mellem dig og andre i virksomheden. Og du behøver ikke at bekymre dig. Vi dele ikke din adresse med nogen.** |[!INCLUDE[prod_short](includes/prod_short.md)] understøtter ikke mailadresser, som leveres af forbrugermailtjenester eller telekommunikationsudbydere. Prøv igen at bruge en mailadresse, der er tildelt af dit arbejde eller din skole, for at fuldføre tilmeldingen. Hvis du stadig ikke kan tilmelde dig og mener, at du kan udføre en mere avanceret opsætning, kan du registrere dig til et nyt Microsoft 365-prøveabonnement og bruge denne mailadresse til at tilmelde dig. |
| .gov- eller .mil-mailadresser Du modtager en meddelelse som den følgende under tilmeldingen:<br /><br />**[!INCLUDE[prod_short](includes/prod_short.md)] er ikke tilgængelig: [!INCLUDE[prod_short](includes/prod_short.md)] er ikke tilgængelig for brugere med .gov eller .mil-mailadresser på nuværende tidspunkt. Brug en anden arbejdsmailadresse, eller besøg os igen senere.** <br>eller <br>**Vi kan ikke afslutte din tilmelding. Det ser ud til, at [!INCLUDE[prod_short](includes/prod_short.md)] ikke aktuelt er tilgængelig for din skole eller dit arbejde.** |[!INCLUDE[prod_short](includes/prod_short.md)] understøtter ikke .gov- eller .mil-adresser på nuværende tidspunkt. |
| Selvbetjeningstilmelding er ikke aktiveret. Du modtager en meddelelse som den følgende under tilmeldingen:<br /><br />**Vi kan ikke afslutte din tilmelding. Din it-afdeling har deaktiveret tilmelding for projekt [!INCLUDE[prod_short](includes/prod_short.md)]. Kontakt dem for at fuldføre tilmeldingen.** <br>eller <br> **Det ligner en privat mailadresse. Angiv din arbejdsmailadresse, så vi kan oprette forbindelse mellem dig og andre i virksomheden. Og du behøver ikke at bekymre dig. Vi dele ikke din adresse med nogen.** |Virksomhedens it-administrator har deaktiveret selvbetjeningstilmelding for [!INCLUDE[prod_short](includes/prod_short.md)]. For at fuldføre tilmeldingen skal du bede it-administratoren om at følge instruktionerne på [denne side](/dynamics365/business-central/dev-itpro/developer/devenv-business-central-manage-selfservice-signups) for at tillade eksisterende brugere at tilmelde sig [!INCLUDE[prod_short](includes/prod_short.md)] og nye brugere at slutte sig til din eksisterende lejer. Problemet kan også forekomme, hvis du har tilmeldt dig Microsoft 365 via en partner. |
| Mailadressen er ikke et Microsoft 365-id. Du modtager en meddelelse som den følgende under tilmeldingen:<br /><br />**Vi finder ikke du i contoso.com. Bruger du et andet id på arbejde eller i skolen? Prøv at logge på med det, og hvis det ikke virker, skal du kontakte it-afdelingen.** |Din organisation bruger id'er til at logge på Microsoft 365 og andre Microsoft-tjenester, der er forskellige fra din mailadresse. For eksempel kan din mailadresse kan være Nancy.Smith@contoso.com, men dit id er nancys@contoso.com. Brug det id, som virksomheden har tilknyttet, til at logge på Microsoft 365 eller andre Microsoft-tjenester. Hvis du ikke kender det, skal du kontakte it-administratoren. Hvis du stadig ikke kan tilmelde dig og kan udføre en mere avanceret opsætning, kan du registrere dig til et nyt Microsoft 365-prøveabonnement og bruge denne mailadresse til at tilmelde dig. |
| Hvis din Microsoft 365-konto er registreret i et understøttet land, og du tilmelder dig til [!INCLUDE[prod_short](includes/prod_short.md)], mens du er i et andet land, modtager du en meddelelse som følgende under tilmeldingen:<br /><br />**Det virkede ikke, vi understøtter ikke dit land eller område endnu.**| Virksomhedens Microsoft 365-abonnement er registreret til et bestemt land i Microsoft 365-administrationsportalen. Tilmeldingsoplevelsen for [!INCLUDE[prod_short](includes/prod_short.md)] bruger det sprog og den landekode, som din aktuelle webbrowser bruger, og derfor du kan få en fejlmeddelelse, selvom du befinder dig i et understøttet land. Bed administratoren om at kontrollere det land, der er angivet i organisationsprofilen i den [Microsoft 365-administrationsportalen](https://portal.office.com/adminportal/home#/companyprofile). Du skal muligvis bruge en anden konto til [!INCLUDE[prod_short](includes/prod_short.md)].|

## Tilgængelighed i område

[!INCLUDE[prod_short](includes/prod_short.md)] fås i en række lande eller områder med lokalisering fra Microsoft eller en godkendt lokaliseringspartner. Du kan finde en komplet liste over de aktuelt understøttede lande og områder under [Tilgængelighed i land/område og understøttede oversættelser](/dynamics365/business-central/dev-itpro/compliance/apptest-countries-and-translations?toc=/dynamics365/business-central/toc.json).  

Du kan finde en oversigt over aktuelt understøttede markeder for hele Dynamics 365 under [International tilgængelighed af Microsoft Dynamics 365](/dynamics365/get-started/availability). Du kan finde en oversigt over lokal funktionalitet i [!INCLUDE[prod_short](includes/prod_short.md)] på startsiden [Lokal funktionalitet](about-localization.md).  

## Se også

[Tilmeld dig for at få en gratis Dynamics 365 Business Central-prøveversion](trial-signup.md)  
[Dynamics 365 Business Central-prøveversion, ofte stillede spørgsmål](trial-faq.md)  
[Velkommen til [!INCLUDE[prod_short](includes/prod_long.md)]](welcome.md)  
[Arbejd med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  
[Lokal funktionalitet](about-localization.md)  
[Tilgængelighed i land/område og understøttede oversættelser](/dynamics365/business-central/dev-itpro/compliance/apptest-countries-and-translations?toc=/dynamics365/business-central/toc.json)  
[International tilgængelighed af Microsoft Dynamics 365](/dynamics365/get-started/availability)  


[!INCLUDE[footer-include](includes/footer-banner.md)]