---
title: Konfigurer synkronisering af kontakt med Outlook til Business Central til det lokale miljø
description: 'Få mere at vide om, hvordan du konfigurerer en Business Central i det lokale miljø til at synkronisere kontakter i Business Central og Outlook.'
author: jswymer
ms.author: jswymer
ms.reviewer: jswymer
ms.service: dynamics365-business-central
ms.topic: how-to
ms.date: 04/04/2023
ms.custom: bap-template
---

# Konfigurer synkronisering af kontakt med Outlook til Business Central til det lokale miljø

I denne artikel kan du få mere at vide om, hvordan du opsætter [!INCLUDE[prod_short](includes/prod_short.md)] lokalt, så der synkroniseres kontakter i [!INCLUDE[prod_short](includes/prod_short.md)] med kontakter i Outlook. Du kan få flere oplysninger ved at gå til [Synkronisere kontakter i Business central med kontakter i Microsoft Outlook](admin-synchronize-outlook-contacts.md).

## Introduktion

Synkronisering af kontaktpersoner kræver brug af OAuth 2.0-protokollen til godkendelse med Exchange Online. Tidligere understøttes basisgodkendelsen også, men det er blevet udfaset og understøttes ikke i Exchange Online. Du kan læse mere om udfasning på [Udfasning af grundlæggende godkendelse i Exchange Online](/exchange/clients-and-mobile-in-exchange-online/deprecation-of-basic-authentication-exchange-online). Denne ændring betyder, at synkronisering af kontaktpersoner i Business Central muligvis er holdt op med at fungere på det lokale miljø. Denne artikel forklarer, hvordan du får den til at fungere igen.

## Forudsætninger

- Exchange Online, enten en enkeltstående version eller via Microsoft 365-plan  
- Adgang til Azure Active Directory (Azure AD)-lejeren, der bruges af Exchange Online
- [!INCLUDE[prod_short](includes/prod_short.md)]-brugere har en Microsoft 365- eller Exchange Online-mailkonto, som tildeles til deres konti i [!INCLUDE[prod_short](includes/prod_short.md)]. Du kan kontrollere denne indstilling i sektionen **Microsoft 365-godkendelse** i din brugerprofil på listen **Brugere**. 

## Konfigurer kontaktsynkronisering

Benyt følgende fremgangsmåde for at konfigurere synkronisering af kontaktpersoner. Hvis du kører [!INCLUDE[prod_short](includes/prod_short.md)] Spring 2019 (v.14), skal du udføre et ekstra trin, der enten ændrer programkode eller opretter forbindelse til Power BI.

1. <a name="registerapp"></a>Registrere en app til Exchange Online API i din Azure AD-lejer.

   I dette trin skal du tilføje en registreret app i Azure AD-lejeren i din Microsoft 365- eller Exchange Online-plan. Ligesom andre Azure-tjenester, der fungerer sammen med Business Central, kræver Exchange Online en appregistrering i Azure AD. Appregistreringen leverer godkendelses- og autorisationstjenester mellem Business Central og Exchange Online.

   Følg den detaljerede vejledning i hjælp til udviklere og it-fagfolk i [Registrere et program i Azure Active Directory](/dynamics365/business-central/dev-itpro/administration/register-app-azure#register-an-application-in-azure-active-directory). Når du gennemgår instruktionerne, skal du huske følgende punkter:

   - Hvis du allerede har registreret et program som en del af integrationen med et andet Microsoft-produkt, f.eks. Power BI, kan du genbruge denne appregistrering. I så fald skal du blot angive appen med Office 365 Exchange Online-tilladelserne, der er beskrevet i næste punkt.

   - Konfigurer den registrerede app med følgende uddelegerede tilladelser til Office 365 Exchange Online-API:

     - Contacts.ReadWrite
     - EWS.AccessAsUser.All

2. Benyt en af følgende fremgangsmåder i forbindelse med [!INCLUDE[prod_short](includes/prod_short.md)] version 14:

   - Rediger side 6700 ved at skifte `FALSE` til `TRUE` i følgende kodelinje i `OnPageOpen`-udløseren:

     ```
     PasswordRequired := AzureADMgt.GetAccessToken(AzureADMgt.GetO365Resource,AzureADMgt.GetO365ResourceName,TRUE) = '';
     ```

   - Opret ny side med følgende kode på OnPageOpen-udløseren:

     ```
     PasswordRequired := AzureADMgt.GetAccessToken(AzureADMgt.GetO365Resource,AzureADMgt.GetO365ResourceName,TRUE) = '';
     ```

   - Konfigurer Power BI ved at følge instruktionerne på [Konfigurere Business Central lokalt til Power BI-integration](admin-powerbi-setup.md#setup).

   Når den løsning, du har valgt, er på plads, skal du bede brugeren enten køre den nye/ændrede side eller [oprette forbindelse til Power BI](across-working-with-powerbi.md#connect). Du behøver kun at udføre dette trin én gang.

## Næste trin

[Synkronisere kontaktpersoner i Business Central med kontaktpersoner i Microsoft Outlook](admin-synchronize-outlook-contacts.md)  
