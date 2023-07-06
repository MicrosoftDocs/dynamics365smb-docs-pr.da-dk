---
title: Dele kontaktpersoner mellem Business Central og Outlook
description: 'Denne tjeneste er tæt integration med Microsoft 365, så du kan dele kontaktpersoner mellem Outlook og Business Central.'
author: brentholtorf
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 'contacts, Microsoft 365'
ms.search.form: '6700, 5320, 5300, 5301, 5302, 5303, 5304, 5305, 5306, 5307, 5308, 5309, 5310, 5311'
ms.date: 03/17/2023
ms.author: bholtorf
---
# <a name="synchronize-contacts-in-business-central-with-contacts-in-microsoft-outlook"></a><a name="synchronize-contacts-in-business-central-with-contacts-in-microsoft-outlook"></a><a name="synchronize-contacts-in-business-central-with-contacts-in-microsoft-outlook"></a>Synkronisere kontaktpersoner i Business Central med kontaktpersoner i Microsoft Outlook

Du kan konfigurere synkronisering af kontaktpersoner, så dine kontakter i [!INCLUDE[prod_short](includes/prod_short.md)] har de samme oplysninger som dine kontakter i Microsoft Outlook. Hvis du f. eks. er en sælger, kan du arbejde i Outlook og [!INCLUDE[prod_short](includes/prod_short.md)] samtidig. Hvis kontakterne er identiske begge steder, gør det dit arbejde mere enkelt.  

Som standard gemmes de kontaktpersoner, du synkroniserer, i en **Business Central**-mappe i dine foretrukne i mapperuden i Outlook. Mappen Business Central gør det nemmere at se, hvilke kontakter der synkroniseres. Du kan angive filtre, der kun skal synkroniseres med bestemte kontakter fra [!INCLUDE[prod_short](includes/prod_short.md)] til Outlook. Når du har oprettet synkroniseringen, kan du synkronisere manuelt eller automatisere processen, så den synkroniseres jævnligt.  

## <a name="prerequisites"></a><a name="prerequisites"></a><a name="prerequisites"></a>Forudsætninger

- Din brugerprofil i [!INCLUDE[prod_short](includes/prod_short.md)] skalangive din Microsoft 365-mailkonto.

  Du kan kontrollere denne indstilling i sektionen **Microsoft 365-godkendelse** i din brugerprofil på listen **Brugere**.
- Med [!INCLUDE[prod_short](includes/prod_short.md)] kan du konfigurere synkronisering af kontaktpersoner som beskrevet i [Konfigurere kontakt-synkronisering med Outlook for Business central lokalt](admin-contact-sync-setup-onprem.md)

## <a name="set-up-synchronization"></a><a name="set-up-synchronization"></a><a name="set-up-synchronization"></a>Konfigurere synkronisering

Du angiver, hvordan du vil synkronisere kontaktpersoner med Outlook på siden **Opsætning af Exchange-synkronisering** i [!INCLUDE[prod_short](includes/prod_short.md)]. 

På siden **Opsætning af Exchange-synkronisering** kan du kontrollere, at forbindelsen til Exchange fungerer, og derefter konfigurere synkroniseringen. Fra **Opsætning af Exchange-synkronisering** kan du åbne synkroniseringen af **Kontakt synkroniseringsopsætning**, og start synkroniseringen. Du kan også angive et filter for at angive, hvilke kontakter der skal synkroniseres. For eksempel kan du angive et filter for navn, type, virksomhed eller lignende. Du kan også ændre standardnavnet på den mappe i Outlook, som kontakterne skal synkroniseres til.  

Hver af dine kolleger kan også oprette deres egen Exchange-synkronisering og angive deres eget filter for, hvilke kontakter der skal synkroniseres.  

Når du har oprettet synkroniseringen, kan du synkronisere ændringerne af kontaktpersonen manuelt, eller du kan automatisere processen ved at oprette en Opgavekøpost. Du kan finde flere oplysninger om automatisering i næste afsnit i denne artikel.

### <a name="automate-synchronization"></a><a name="automate-synchronization"></a><a name="automate-synchronization"></a>Automatisk synkronisering

Du kan oprette en Opgavekøpost, som synkroniserer kontakter i henhold til en tidsplan, som du definerer. Du kan finde flere oplysninger i [Bruge opgavekøer til at planlægge opgaver](admin-job-queues-schedule-tasks.md). 

I følgende tabel vises indstillingerne på **Kort til opgavekøpost**-siden til synkronisering af kontakter:

|Felt|Indstilling for synkronisering af kontaktpersoner|
|-----|-----|
|Objekttype, der skal køres|Codeunit|
|Objekt-id, der skal aktiveres|6700|

## <a name="synchronize-contacts"></a><a name="synchronize-contacts"></a><a name="synchronize-contacts"></a>Synkronisere kontakter

Hvis du plejer at arbejde med kontaktpersoner i [!INCLUDE[prod_short](includes/prod_short.md)], vil du finde det let at starte synkroniseringen manuelt, når det passer dig, fra oversigten **Kontakter**. Du kan synkronisere kontakter på to måder:

* **Synkroniser med Microsoft 365**

  Synkroniser alle ændringer fra [!INCLUDE[prod_short](includes/prod_short.md)] til Microsoft 365, der er foretaget efter den sidste synkronisering, baseret på den seneste ændringsdato. Eventuelle nye kontakter fra Microsoft 365 synkroniseres også tilbage til [!INCLUDE[prod_short](includes/prod_short.md)]. Dette er typisk hurtigere end at foretage en fuld synkronisering. 

* **Komplet synkronisering med Microsoft 365**

  Synkroniser alle kontakter i begge retninger, uanset datoen for sidste synkronisering og datoen for seneste ændring.  

I begge tilfælde synkroniseres kontakter kun fra Outlook, hvis de nødvendige felter er udfyldt. De obligatoriske felter for synkronisering til Microsoft 365 er **Navn**, **E-mailadresse**, og kontakten skal være af typen **Person**. [!INCLUDE[prod_short](includes/prod_short.md)] er kilden til kontaktoplysninger, så kontaktoplysninger fra [!INCLUDE[prod_short](includes/prod_short.md)] gemmes, hvis der er dubletter.  

> [!NOTE]
> Hvis du sletter en kontaktperson i Outlook, men beholder den i [!INCLUDE[prod_short](includes/prod_short.md)], bliver kontaktpersonen gendannet i Outlook, næste gang du synkroniserer. 

## <a name="see-also"></a><a name="see-also"></a><a name="see-also"></a>Se også

[Blive køreklar](ui-get-ready-business.md)  
[Finans](finance.md)  
[Salg](sales-manage-sales.md)  
[Køb](purchasing-manage-purchasing.md)  
[Brug kontaktpersoner (Personer) i Outlook på internettet](https://support.office.com/article/Using-contacts-People-in-Outlook-on-the-web-1e3438c7-26b2-420c-87de-3cea9d31b5cb?appver=OWB150)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
