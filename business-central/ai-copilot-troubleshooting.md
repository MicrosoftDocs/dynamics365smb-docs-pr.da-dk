---
title: Fejlfinde Copilot- og AI-funktioner
description: 'Lær, hvordan du løser almindelige problemer, som du kan støde på, mens du arbejder med Copilot- og AI-funktioner i Business Central.'
author: jswymer
ms.author: jswymer
ms.reviewer: jswymer
ms.topic: troubleshooting
ms.collection:
  - bap-ai-copilot
ms.date: 02/01/2024
ms.custom: bap-template
ms.service: dynamics-365-business-central
---
# <a name="troubleshoot-copilot-and-ai-capabilities"></a>Fejlfinde Copilot- og AI-funktioner

Copilot er en AI-drevet funktionalitet i Business Central, der hjælper med forskellige opgaver som at udarbejde marketingtekst og afstemme bankkonti. Hvis du oplever problemer med Copilot eller andre AI-funktioner, kan denne artikel hjælpe dig med at identificere og løse almindelige problemer.

## <a name="copilot-doesnt-appear-on-pages"></a>Copilot vises ikke på siderne

Hvis Copilot-funktionalitet, såsom **Kladde med Copilot** handlingen til markedsføringstekstforslag eller **Afstem med Copilot** handlingen for hjælp til bankkontoafstemning, vises ikke på en side som forventet, tjek følgende:

- Hvis funktionen styres under Funktionsstyring, skal du sørge for, at den er aktiveret. [Få mere at vide om funktionsstyring](admin-feature-management.md).

- Sørg for, at funktionaliteten ikke er skjult af personalisering. [Få mere at vide mere om tilpasning](ui-personalization-user.md).

## <a name="copilot-appears-on-pages-but-you-get-an-error-that-its-not-activated"></a>Copilot vises på siderne, men du får en fejlmeddelelse om, at den ikke er aktiveret

Når du prøver at bruge Copilot, og du får en fejl svarende til **Beklager, Copilot er ikke aktiveret for \[funktion\]**, er der et par ting at tjekke :

- Først skal du kontrollere, at funktionen er aktiveret på siden **Copilot- og AI-funktioner**. [Få mere at vide om aktivering af Copilot- og AI-funktioner](enable-ai.md#activate-features). 
- Dernæst skal du sørge for, at erklæringen om beskyttelse af personlige oplysninger for Azure OpenAI-integration ikke er indstillet til **Uenig for alle**. Hvis det er det, skal du ændre det til **Enig for alle**. [Få mere at vide om fortrolighedserklæringer](privacy-notices-status.md).

## <a name="copilot-capabilities-from-microsoft-not-listed-on-copilot--ai-capabilities-page"></a>Copilot-funktioner fra Microsoft er ikke angivet på siden Copilot- og AI-funktioner

Hvis ingen af AI-funktionerne fra Microsoft vises på siden **Copilot- og AI-funktioner**, skyldes det sandsynligvis, at du har en eller flere integreringsapps installeret i dit miljø. Integreringsapps kan tilbyde deres egne Copilot-funktioner, men funktioner, der udgives af Microsoft, er ikke kompatible med miljøer, der har integrerede apps.

## <a name="see-also"></a>Se også

[Konfigurere Copilot- og AI-funktioner](enable-ai.md)  
[Marketing-tekstforslag med Copilot](ai-overview.md)  
[Afstemme bankkonti med Copilot](bank-reconciliation-with-copilot.md)  
