---
title: Dele kontaktpersoner mellem Business Central og Outlook | Microsoft Docs
description: Denne tjeneste er tæt integration med Microsoft 365, så du kan dele kontaktpersoner mellem Outlook og Business Central.
author: edupont04
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: contacts, Microsoft 365
ms.date: 04/01/2021
ms.author: edupont
ms.openlocfilehash: 1ccada415d506193e52ac37981252a47e6088971
ms.sourcegitcommit: 766e2840fd16efb901d211d7fa64d96766ac99d9
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 03/31/2021
ms.locfileid: "5777162"
---
# <a name="synchronize-contacts-in-business-central-with-contacts-in-microsoft-outlook"></a>Synkronisere kontaktpersoner i Business Central med kontaktpersoner i Microsoft Outlook
Du kan se de samme kontaktpersoner i [!INCLUDE[prod_short](includes/prod_short.md)] som i Outlook, hvis du har oprettet synkronisering af kontaktpersoner. Hvis du er sælger, udfører du måske noget af dit arbejde i Outlook og noget af dit arbejde i [!INCLUDE[prod_short](includes/prod_short.md)]. Hvis kontakterne er identiske begge steder, gør det dit arbejde mere enkelt.  

En dedikeret mappe i Outlook gør det nemt at finde kontaktpersoner, og du kan indstille et filter til at synkronisere de kontakter fra [!INCLUDE[prod_short](includes/prod_short.md)], som du vil have vist i Outlook. Når kontaktsynkroniseringen er oprettet, kan du starte synkroniseringen manuelt eller oprette en automatisk synkronisering, der regelmæssigt kan sørge for, at kontakterne bliver synkroniseret.  

## <a name="set-up-synchronization"></a>Konfigurere synkronisering
Du angiver, hvordan du vil synkronisere kontaktpersoner med Outlook på siden **Opsætning af Exchange-synkronisering** i [!INCLUDE[prod_short](includes/prod_short.md)]. Som en forudsætning skal din [!INCLUDE[prod_short](includes/prod_short.md)]-mailkonto være angivet i din brugerprofil i Microsoft 365. Du kan kontrollere dette i sektionen **Microsoft 365-godkendelse** i din brugerprofil på listen **Brugere**.  

På siden **Opsætning af Exchange-synkronisering** kan du kontrollere, at forbindelsen til Exchange fungerer, og derefter konfigurere synkroniseringen. Åbn siden **Opsætning af Exchange-synkronisering**, og start synkroniseringen. Du kan også angive et filter for, hvilke kontakter der skal synkroniseres mellem [!INCLUDE[prod_short](includes/prod_short.md)] og Outlook. For eksempel kan du angive et filter for navn, type, virksomhed eller lignende. Du kan også ændre standardnavnet på den mappe, som kontakterne skal synkronisere i Outlook. Standardnavnet er *Business Central*.  

Når synkroniseringen er blevet oprettet, synkroniseres ændringer, som du foretager af kontakten i enten Outlook eller i [!INCLUDE[prod_short](includes/prod_short.md)], med den anden kontaktperson.  

Hver af dine kolleger kan også oprette deres egen Exchange-synkronisering og angive deres eget filter for, hvilke kontakter der skal synkroniseres.  

## <a name="synchronize-contacts"></a>Synkronisere kontakter
Hvis du plejer at arbejde med kontaktpersoner i [!INCLUDE[prod_short](includes/prod_short.md)], vil du finde det let at starte synkroniseringen manuelt, når det passer dig, fra oversigten **Kontakter**. Vælg handlingen **Synkroniser med Microsoft 365**, og afgør, om du vil ændre det filter, du har angivet. Når du klikker på knappen OK, starter synkroniseringen med det samme, og de seneste ændringer anvendes på dine kontakter i Outlook.  

I oversigten **Kontakter** kan du synkronisere kontakter på to måder:

* **Synkroniser med Microsoft 365**

  Denne handling synkroniserer alle ændringer fra [!INCLUDE[prod_short](includes/prod_short.md)] til Microsoft 365 siden den forrige synkronisering baseret på den seneste ændringsdato. Eventuelle nye kontakter fra Microsoft 365 synkroniseres tilbage til [!INCLUDE[prod_short](includes/prod_short.md)] også. Dette er typisk hurtigere end at foretage en fuld synkronisering.  

* **Fuld synkronisering med Microsoft 365**

  Denne handling synkroniserer alle kontakter i begge retninger, uanset datoen for sidste synkronisering og datoen for seneste ændring.  

I begge tilfælde synkroniseres kontakter kun fra Outlook, hvis de nødvendige felter er udfyldt. De obligatoriske felter for synkronisering til Microsoft 365 er **Navn**, **E-mailadresse**, og de skal være af typen Person. [!INCLUDE[prod_short](includes/prod_short.md)] er overordnet med hensyn til kontaktoplysninger, så kontaktoplysninger fra [!INCLUDE[prod_short](includes/prod_short.md)] gemmes i tilfælde af dubletter.  

I Outlook vises kontakter fra [!INCLUDE[prod_short](includes/prod_short.md)] i en mappe under **Andre kontakter** i visningen **Personer**. Hvis du ikke kender visningen Personer i Outlook, kan du gå til den fra indstillingerne for navigation i nederste venstre hjørne af Outlook.  

## <a name="see-also"></a>Se også
[Blive køreklar](ui-get-ready-business.md)  
[Finans](finance.md)  
[Salg](sales-manage-sales.md)  
[Køb](purchasing-manage-purchasing.md)  
[Bruge kontaktpersoner (Personer) i Outlook på internettet](https://support.office.com/article/Using-contacts-People-in-Outlook-on-the-web-1e3438c7-26b2-420c-87de-3cea9d31b5cb?appver=OWB150)  


[!INCLUDE[footer-include](includes/footer-banner.md)]