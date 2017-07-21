---
title: "Metoder til fejlfinding eller løsning af problemer i forbindelse med selvbetjeningstilmelding | Microsoft Docs"
description: "Få mere at vide om de almindeligste årsager til, hvorfor du muligvis ikke kan fuldføre tilmeldingen til Dynamics 365 til Financials, og hvordan du løser problemet."
services: project-madeira
documentationcenter: 
author: SusanneWindfeldPedersen
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.date: 06/02/2017
ms.author: solsen
ms.translationtype: Human Translation
ms.sourcegitcommit: 81636fc2e661bd9b07c54da1cd5d0d27e30d01a2
ms.openlocfilehash: 1bc036d4e57403d903c292a07a8985dfe939b20d
ms.contentlocale: da-dk
ms.lasthandoff: 07/07/2017


---
# <a name="troubleshooting-self-service-sign-up"></a>Fejlfinding af selvbetjeningstilmelding
Tilmelding til [!INCLUDE[d365fin](includes/d365fin_md.md)] er nemt og kan udføres hurtigt. Du kan oprette en gratis konto, selvom du en eksisterende virksomhed. Denne artikel løser problemer, der måtte opstå under tilmeldingen.

## <a name="what-email-address-can-i-use-with-financials"></a>Hvilken mailadresse kan jeg bruge til Financials?
[!INCLUDE[d365fin](includes/d365fin_md.md)] kræver, at du bruger en arbejds- eller skolemailadresse til at tilmelde dig. [!INCLUDE[d365fin](includes/d365fin_md.md)] understøtter ikke mailadresser, som leveres af forbrugermailtjenester eller telekommunikationsudbydere. Dette omfatter outlook.com, hotmail.com, gmail.com og andre.

Hvis du forsøger at tilmelde dig med en privat mailadresse, får du en meddelelse om, at du skal bruge en arbejds- eller skolemailadresse.

## <a name="troubleshooting"></a>Fejlfinding
I mange tilfælde kan registrering til [!INCLUDE[d365fin](includes/d365fin_md.md)] gøres ved at følge tilmeldingsprocessen. Der er flere årsager til, hvorfor du ikke muligvis ikke kan fuldføre selvbetjeningstilmelding. Tabellen nedenfor indeholder en oversigt over nogle af de mest almindelige årsager til, at du ikke kan fuldføre tilmeldingen, og hvordan du kan løsning disse problemer.

| Symptom/fejlmeddelelse | Årsag og løsning |
| --- | --- |
| Ved Office 365-mailadresser, der ikke er registreret i USA, modtager du en meddelelse som den følgende under tilmeldingen:<br /><br />**Det virkede ikke, vi understøtter ikke dit land eller område endnu.** |[!INCLUDE[d365fin](includes/d365fin_md.md)] understøtter aktuelt kun Office 365-mailkonti, der er registreret i USA. |
| Private mailadresser, f.eks nancy@gmail.com, understøttes ikke. Du modtager en meddelelse som den følgende under tilmeldingen:<br /><br />**Du har indtastet en privat mailadresse: Du skal angive din arbejdsmailadresse, så vi kan opbevare virksomhedens data sikkert.**<br> eller <br> **Det ligner en privat mailadresse. Angiv din arbejdsmailadresse, så vi kan oprette forbindelse mellem dig og andre i virksomheden. Og du behøver ikke at bekymre dig. Vi dele ikke din adresse med nogen.** |[!INCLUDE[d365fin](includes/d365fin_md.md)] understøtter ikke mailadresser, som leveres af forbrugermailtjenester eller telekommunikationsudbydere. Prøv igen at bruge en mailadresse, der er tildelt af dit arbejde eller din skole, for at fuldføre tilmeldingen. Hvis du stadig ikke kan tilmelde dig og mener, at du kan udføre en mere avanceret opsætning, kan du registrere dig til et nyt Office 365 prøveabonnement og bruge denne mailadresse til at tilmelde dig. |
| .gov- eller .mil-mailadresser Du modtager en meddelelse som den følgende under tilmeldingen:<br /><br />**[!INCLUDE[d365fin](includes/d365fin_md.md)] er ikke tilgængelig: [!INCLUDE[d365fin](includes/d365fin_md.md)] er ikke tilgængelig for brugere med .gov eller .mil-mailadresser på nuværende tidspunkt. Brug en anden arbejdsmailadresse, eller besøg os igen senere.** <br>eller <br>**Vi kan ikke afslutte din tilmelding. Det ser ud til, at [!INCLUDE[d365fin](includes/d365fin_md.md)] ikke aktuelt er tilgængelig for din skole eller dit arbejde.** |[!INCLUDE[d365fin](includes/d365fin_md.md)] understøtter ikke .gov- eller .mil-adresser på nuværende tidspunkt. |
| Selvbetjeningstilmelding er ikke aktiveret. Du modtager en meddelelse som den følgende under tilmeldingen:<br /><br />**Vi kan ikke afslutte din tilmelding. Din it-afdeling har deaktiveret tilmelding for projekt [!INCLUDE[d365fin](includes/d365fin_md.md)]. Kontakt dem for at fuldføre tilmeldingen.** <br>eller <br> **Det ligner en privat mailadresse. Angiv din arbejdsmailadresse, så vi kan oprette forbindelse mellem dig og andre i virksomheden. Og du behøver ikke at bekymre dig. Vi dele ikke din adresse med nogen.** |Virksomhedens it-administrator har deaktiveret selvbetjeningstilmelding for [!INCLUDE[d365fin](includes/d365fin_md.md)]. For at fuldføre tilmeldingen skal du kontakte it-administratoren og bede ham eller hende om at følge instruktionerne på siden nedenfor for at tillade eksisterende brugere at tilmelde sig [!INCLUDE[d365fin](includes/d365fin_md.md)] og nye brugere at slutte sig til din eksisterende lejer. Problemet kan også forekomme, hvis du har tilmeldt dig Office 365 via en partner. |
| Mailadressen er ikke et Office 365-id. Du modtager en meddelelse som den følgende under tilmeldingen:<br /><br />**Vi finder ikke du i contoso.com. Bruger du et andet id på arbejde eller i skolen? Prøv at logge på med det, og hvis det ikke virker, skal du kontakte it-afdelingen.** |Din organisation bruger id'er til at logge på Office 365 og andre Microsoft-tjenester, der er forskellige fra din mailadresse. For eksempel kan din mailadresse kan være Nancy.Smith@contoso.com, men dit id er nancys@contoso.com. Brug det id, som virksomheden har tilknyttet, til at logge på Office 365 eller andre Microsoft-tjenester. Hvis du ikke kender det, skal du kontakte it-administratoren. Hvis du stadig ikke kan tilmelde dig, men kan udføre en mere avanceret opsætning, kan du registrere dig til et nyt Office 365 prøveabonnement og bruge denne mailadresse til at tilmelde dig. |

## <a name="see-also"></a>Se også
[Velkommen til [!INCLUDE[d365fin](includes/d365fin_long_md.md)]](index.md)  
[Arbejde med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)


