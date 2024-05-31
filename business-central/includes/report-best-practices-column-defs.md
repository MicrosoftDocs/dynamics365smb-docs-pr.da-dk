---
author: brentholtorf
ms.topic: include
ms.date: 04/05/2024
ms.author: bholtorf
ms.service: dynamics-365-business-central
---

## <a name="best-practices-for-working-with-column-definitions"></a>Bedste fremgangsmåder for arbejde med kolonnedefinitioner

Kolonnedefinitioner versioneres ikke. Når du ændrer en kolonnedefinition, erstattes den gamle version, når ændringen gemmes i databasen. Følgende liste indeholder nogle anbefalede fremgangsmåder til at arbejde med kolonnedefinitioner.

- Hvis du tilføjer kolonnedefinitioner, skal du vælge en god kode og udfylde feltet Beskrivelse med en meningsfuld tekst, mens du stadig ved, hvad du bruger kolonnedefinitionen til. Disse oplysninger hjælper dine kolleger (og dit fremtidige jeg) med at arbejde med Financial Reporting og måske ændre kolonnedefinitionen.
- Før du ændrer en kolonnedefinition, kan du overveje at tage en kopi af den som sikkerhedskopi, hvis ændringen ikke fungerer som forventet. Du kan enten bare kopiere definitionen (give den et godt navn) eller eksportere den. Hvis du vil lære mere, skal du gå til [Importere eller eksportere kolonnedefinitioner](#import-or-export-financial-report-column-definitions).
- Hvis du har brug for en ny kopi af en definition, som [!INCLUDE [prod_short](prod_short.md)] leverer, er en nem måde at få en på at oprette et nyt regnskab, der kun indeholder opsætningsdata. Du kan derefter eksportere definitionen og importere den i det regnskab, hvor definitionen skal opdateres.
