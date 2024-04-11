---
author: brentholtorf
ms.topic: include
ms.date: 03/08/2024
ms.author: bholtorf
ms.service: dynamics-365-business-central
---

> [!NOTE]
> Når du kopierer et regnskab i et miljø, hvor Dataverse eller Sales-integration er aktiveret, rydder [!INCLUDE [prod_short](prod_short.md)] følgende indstillinger, når du kopierer til målregnskabet:
>
> * Dataverse og Dynamics Connection Settings for at sikre, at integrationen genoptages korrekt i målvirksomheden.
> * Integrationsposter for at sikre, at målfirmaet ikke peger på poster, der er sammenkædet i kilderegnskabet.
> * Synkroniseringsjob for integration for at stoppe synkronisering af baggrundsjob.
> * Synkroniseringsfejl, hvis de findes, fordi de peger på fejl i kildefirmaet og bare ville blive betragtet som støj i målfirmaet.