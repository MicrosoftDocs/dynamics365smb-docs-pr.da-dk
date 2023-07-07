---
title: Konfigurere marketingtekst med Copilot til AI-styret vare (forhåndsversion)
description: 'I denne artikel forklares det, hvordan du får en Copilot prøveversion af Business central, og hvordan du aktiverer Copilot på et miljø.'
author: jswymer
ms.author: jswymer
ms.reviewer: jswymer
ms.topic: how-to
ms.date: 03/22/2023
ms.custom: bap-template
---

# <a name="configure-ai-powered-item-marketing-text-preview-with-copilot"></a>Konfigurere marketingtekst med Copilot til AI-styret vare (forhåndsversion)

[!INCLUDE[ai-preview](includes/ai-preview.md)]

I denne artikel forklares det, hvordan du kan styre muligheden for at oprette marketingtekst med Copilot til virksomheden i forbindelse med AI-styret vare. Denne opgave udføres af en administrator. Der er to krav, som du skal udføre for at gøre funktionen tilgængelig for brugerne:

- Aktivér funktionen **Opret AI-drevet produktbeskrivelser med Copilot**.
- Samtykke til vilkårene og betingelserne i forbindelse med [forhåndsversion](https://dynamics.microsoft.com/legaldocs/supp-dynamics365-preview/) og [Microsoft erklæring om beskyttelse af personlige oplysninger](https://go.microsoft.com/fwlink/?LinkId=521839) på vegne af organisationen.

Hvis et af disse krav ikke er opfyldt, kan funktionen ikke bruges.

## <a name="prerequisites"></a>Forudsætninger

Du bruger en [forhåndsversion](ai-preview-getstarted.md) af Business central, som er aktiveret til Copilot. Aktivering af Copilot udføres af en administrator. Du kan finde flere oplysninger i [Konfigurere marketingtekst for AI-styret vare med Copilot](enable-ai.md).

## <a name="enable-or-disable-create-ai-powered-product-descriptions-with-copilot"></a>Aktivér eller deaktivér Opret AI-drevet produktbeskrivelser med Copilot

1. I Business Central skal du søge efter og åbne siden **Funktionsstyring**.
2. Angiv kolonnen **Aktiveret til** for **Forhåndsversion af funktion: Opret AI-drevne produktbeskrivelser med Copilot** til **Alle brugere**, så funktionen eller **Ingen** deaktiveres.

   Du kan finde flere oplysninger om funktionsstyring generelt i [Funktionsstyring](/dynamics365/business-central/dev-itpro/administration/feature-management).

## <a name="consent-to-or-reject-preview-and-privacy-terms-and-conditions-for-all-users"></a>Tilladelse til accept eller afvisning af forhåndsversion og oplysninger om beskyttelse af personlige oplysninger for alle brugere

1. Søg, og åbn siden **Status for meddelelser om beskyttelse af personlige oplysninger** i Business central.
2. Vælg **Azure OpenAI** i kolonnen **Integrationsnavn**, og læs derefter de vilkår og betingelser, der er angivet for dig.
3. Marker afkrydsningsfeltet **Accepter for alle** i **Azure OpenAI**, eller marker afkrydsningsfeltet **Afvis for alle** for at afvise.

## <a name="next-steps"></a>Næste trin

Når du aktiverer og godkender en funktion, er du klar til at afprøve Copilot om emner i Business central. Gå til [Tilføje marketingtekst for varer](item-marketing-text.md).  

## <a name="see-also"></a>Se også

[Oversigt over AI-styret varemarketingtekst med Copilot](ai-overview.md)  
[Oprette marketingtekst til varer vha. Copilot](item-marketing-text.md)  
[AI-drevet varemarketingtekst med Copilot, ofte stillede spørgsmål](ai-faq.md)  
