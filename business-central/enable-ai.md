---
title: Konfigurere marketingtekst med Copilot til AI-styret vare (forhåndsversion)
description: 'I denne artikel forklares det, hvordan du får en CoPilot prøveversion af Business central, og hvordan du aktiverer CoPilot på et miljø'
author: jswymer
ms.author: jswymer
ms.reviewer: jswymer
ms.topic: how-to
ms.date: 03/22/2023
ms.custom: bap-template
---

# Konfigurere marketingtekst med Copilot til AI-styret vare (forhåndsversion)

[!INCLUDE[ai-preview](includes/ai-preview.md)]

I denne artikel forklares det, hvordan du kan styre muligheden for at oprette marketingtekst med CoPilot til virksomheden i forbindelse med AI-styret vare. Denne opgave udføres af en administrator. Der er to krav, som du skal udføre for at gøre funktionen tilgængelig for brugerne:

- Aktivér funktionen **Opret AI-drevet produktbeskrivelser med Copilot**.
- Samtykke til vilkårene og betingelserne i forbindelse med [forhåndsversion](https://dynamics.microsoft.com/legaldocs/supp-dynamics365-preview/) og [Microsoft erklæring om beskyttelse af personlige oplysninger](https://go.microsoft.com/fwlink/?LinkId=521839) på vegne af organisationen.

Hvis et af disse krav ikke er opfyldt, kan funktionen ikke bruges.

## Forudsætninger

Du bruger en [forhåndsversion](ai-preview-getstarted.md) af Business central, som er aktiveret til CoPilot. Aktivering af CoPilot udføres af en administrator. Du kan finde flere oplysninger i [Konfigurere marketingtekst for AI-styret vare med CoPilot](enable-ai.md).

## Aktivér eller deaktivér funktionen "Opret AI-drevet produktbeskrivelser med Copilot"

1. I Business Central skal du søge efter og åbne siden **Funktionsstyring**.
2. Angiv kolonnen **Aktiveret til** for **Forhåndsversion af funktion: Opret AI-drevne produktbeskrivelser med CoPilot**-funktion til **Alle brugere**, så funktionen eller **Ingen** deaktiveres.

   Du kan finde flere oplysninger om funktionsstyring generelt i [Funktionsstyring](/dynamics365/business-central/dev-itpro/administration/feature-management).

## Tilladelse til accept eller afvisning af forhåndsversion og oplysninger om beskyttelse af personlige oplysninger for alle brugere

1. Søg, og åbn siden **Status for meddelelser om beskyttelse af personlige oplysninger** i Business central.
2. Vælg **Azure OpenAI** i kolonnen **Integrationsnavn**, og læs derefter de vilkår og betingelser, der er angivet for dig.
3. Marker afkrydsningsfeltet **Accepter for alle** i **Azure OpenAI**  , eller marker afkrydsningsfeltet **Afvis for alle** for at afvise.

## Næste trin

Når du har et sandkasse- eller et prøvemiljø, er du klar til at afprøve CoPilot om emner i Business central. Gå til [Tilføje marketingtekst for varer](item-marketing-text.md).  

## Se også

[Oversigt over AI-styret varemarketingtekst med Copilot](ai-overview.md)  
[Oprette marketingtekst til varer vha. CoPilot](item-marketing-text.md)  
[AI-drevet varemarketingtekst med Copilot, ofte stillede spørgsmål](ai-faq.md)  