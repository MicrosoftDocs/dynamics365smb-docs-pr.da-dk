---
title: Administration af OneDrive-integration med Business Central
description: 'Få mere at vide om, hvad du kan gøre for at administrere en integration mellem Business Central og OneDrive for Business.'
author: jswymer
ms.topic: conceptual
ms.devlang: al
ms.search.keywords: 'OneDrive, share, browser'
ms.date: 02/28/2022
ms.author: jswymer
ms.service: dynamics-365-business-central
---
# <a name="managing-onedrive-integration-with-business-central"></a>Administration af OneDrive-integration med Business Central

Denne artikel giver en oversigt over, hvad en administrator kan gøre for at kontrollere OneDrive for Business-integration med [!INCLUDE[prod_short](includes/prod_short.md)]. [!INCLUDE[prod_short](includes/prod_short.md)]-onlinekunder drager fordel af automatisk integration, uden at der kræves ekstra opsætning for at bruge funktionerne til åbning og deling i OneDrive. Med vejledningen til assisteret opsætning af **OneDrive** kan du give brugere adgang til endnu flere OneDrive-funktioner, f.eks. at åbne Excel-filer i OneDrive eller endda slå alle funktioner fra.  

## <a name="configure-onedrive-for-integration-with-business-central"></a>Konfigurere OneDrive til integration med Business Central

I dette afsnit forklares krav, der skal opfyldes i OneDrive for Business for at kunne konfigurere integrationen med Business Central og opgaver, du kan udføre for at administrere integrationen.

### <a name="minimum-requirements"></a>Minimumkrav

* Hver bruger skal have en licens til [!INCLUDE[prod_short](includes/prod_short.md)] og OneDrive som en del af en Microsoft 365-plan.
* OneDrive skal konfigureres for hver bruger.

### <a name="managing-privacy"></a>Administration af beskyttelse af personlige oplysninger

> [!IMPORTANT]
> Hvis du har valgt at installere Business Central og OneDrive til forskellige lande eller områder, kan de filer, der oprettes af Business Central og placeres i OneDrive, ligge på tværs af dataopbevaringsgrænser. Sørg for at bekræfte din organisations politikker og de offentlige overholdelseskrav for dataopbevaring, før du aktiverer forbindelsen til OneDrive.

Administratorer og slutbrugere styrer det indhold, der er gemt i OneDrive, og disse data ejes udelukkende af organisationen. Du kan finde flere oplysninger under [Sådan beskytter SharePoint og OneDrive dine data i skyen](/sharepoint/safeguarding-your-data). Du kan også besøge vores [Microsoft Erklæring om beskyttelse af personlige oplysninger fra](https://privacy.microsoft.com/en-us/privacystatement), som forklarer de data, som Microsoft behandler, hvordan Microsoft behandler dem, og til hvilke formål.

Ved at aktivere denne serviceforbindelse accepterer du:

(a) at dele data fra Dynamics 365 Business Central med serviceudbyderen, som bruger dem i henhold til sine regler og oplysninger om beskyttelse af personlige oplysninger. (b) serviceudbyderens overholdelsesniveau kan være anderledes end Dynamics 365 Business Central, og (c) Microsoft må dele dine kontaktoplysninger med denne serviceudbyder, hvis det er nødvendigt, for at den kan fungere og der kan foretages fejlfinding af tjenesten.

## <a name="configure-business-central"></a>Konfigurer Business Central

Med Business Central Online er forbindelsen mellem Business Central og OneDrive automatisk konfigureret for dig, og OneDrive-funktionerne er som standard tilgængelige for brugerne. Hvis du vil slå nogle eller alle funktioner fra, kan du bruge **Opsætning af OneDrive**-vejledningen med assisteret opsætning i Business Central-klienten.

Konfiguration af Business Central on-premises er anderledes, fordi forbindelsen mellem Business Central og OneDrive ikke er konfigureret for dig. Du skal gøre dette manuelt. Du kan finde flere oplysninger i [Konfigurere OneDrive-integration med Business Central On-premises](admin-onedrive-integration-onpremises.md).

### <a name="about-multiple-environments"></a>Om flere miljøer

OneDrive-integration er konfigureret pr. miljø, så dine indstillinger vil gælde for alle firmaer i dette miljø. Hvis organisationen har mere end ét miljø, skal du konfigurere OneDrive-integration for hver af dem.

### <a name="prerequisites"></a>Forudsætninger

- Indirekte, redigere- og slette-tilladelse på tabellen **Dokumentservicescenarie** som minimum

### <a name="configure-onedrive-using-onedrive-setup"></a>Konfigurere OneDrive ved hjælp af OneDrive-konfiguration

1. Vælg ![Lightbulb, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, angiv **OneDrive-konfiguration**, og vælg derefter det relaterede link. 
2. Første gang du kører den assisterede opsætning, kan du se **Dine personlige oplysninger**. Læs siden, og hvis du kan acceptere vilkårene, skal du vælge **Acceptér** for at fortsætte.
3. På siden **Konfigurer filhåndtering** kan du vælge mellem følgende indstillinger:

   [!INCLUDE[onedrive-feature-options](includes/onedrive-feature-options.md)]
4. Vælg **Næste**>**Udført**.

### <a name="switching-to-new-onedrive-integration-after-upgrade"></a>Skifte til ny OneDrive-integration efter opgradering

Den assisterede opsætning af **OneDrive** blev introduceret i 2022 udgivelsesbølge 2, version 21.0. Tidligere brugte OneDrive-integrationen **Opsætning af SharePoint-forbindelse**, som er udfaset og vil blive fjernet i 2023 udgivelsesbølge 2, version 23.0. Når du har opgraderet til version 21, fungerer OneDrive stadig som før. Men det anbefales, at du skifter til den nye OneDrive-integration. Hvis du foretager dette skifte nu, bliver det nemmere, når **Opsætning af SharePoint-forbindelse** bliver fjernet. Desuden giver det dig mulighed for at bruge assisteret opsætning af **OneDrive** til at administrere de OneDrive-funktioner, som brugerne har adgang til. Den assisterede opsætning af **OneDrive** gør overgangen fra den ældre SharePoint-installation nem og problemfri.

Hvis du vil skifte, skal du blot åbne og køre assisteret opsætning af **OneDrive** direkte, eller åbne siden **Opsætning af SharePoint-forbindelse** og vælge **Gå til ny OneDrive-konfiguration** i meddelelsen øverst på siden. Følg opsætningsvejledningen som beskrevet i det foregående afsnit.

## <a name="restoring-onedrive-and-"></a>Gendannelse af OneDrive og [!INCLUDE[prod_short](includes/prod_short.md)]

Som en del af en øvelse i genoprettelse efter nedbrud skal administratorer muligvis gendanne et [!INCLUDE[prod_short](includes/prod_short.md)]-onlinemiljø til en sikkerhedskopi fra et tidspunkt tidligere og synkronisere OneDrive-lageret til det samme tidspunkt. OneDrive indeholder forskellige gendannelsesværktøjer, f.eks. gendannelse af en brugers OneDrive til en tidligere tidsperiode, gendannelse af en tidligere version af en enkelt fil eller gendannelse af slettede filer. Du kan finde flere oplysninger i følgende artikler:

* For [!INCLUDE[prod_short](includes/prod_short.md)], se [Gendanne et miljø i Administration](/dynamics365/business-central/dev-itpro/administration/tenant-admin-center-backup-restore).
* For OneDrive, se [Gendanne din OneDrive](https://support.microsoft.com/en-us/office/restore-your-onedrive-fa231298-759d-41cf-bcd0-25ac53eb8a15?ui=en-us&rs=en-us&ad=us)

## <a name="governance"></a>Styreformer

SharePoint Administrationen giver omfattende kontrol over politikker, der styrer brugen af OneDrive i hele organisationen. Globale administratorer eller brugere, der har SharePoint-rollen Administrator, kan konfigurere politikker, der bestemmer, hvem der kan få adgang til OneDrive, hvor data er placeret, indholdslivscyklussen og meget mere. Følgende links indeholder oplysninger om ofte anvendte funktioner og indstillinger, der kan forbedre integrationen med [!INCLUDE[prod_short](includes/prod_short.md)]. 

* [Administrere delingsindstillinger](/sharepoint/turn-external-sharing-on-or-off)
* [Brug informationsbarrierer med SharePoint](/sharepoint/information-barriers)
* [Få mere at vide om forhindring af datatab](/microsoft-365/compliance/dlp-learn-about-dlp)
* [Angive standardlagerplads for OneDrive-brugere](/onedrive/set-default-storage-space)
* [Tilføje og fjerne administratorer for en brugers OneDrive](/sharepoint/manage-user-profiles#add-and-remove-admins-for-a-users-onedrive)
* [Deaktiver OneDrive-oprettelse for nogle brugere](/sharepoint/manage-user-profiles#disable-onedrive-creation-for-some-users)
* [Multi-Geo-funktioner i OneDrive og SharePoint-online](/microsoft-365/enterprise/multi-geo-capabilities-in-onedrive-and-sharepoint-online-in-microsoft-365)

> [!NOTE]
> Nogle funktioner er muligvis kun tilgængelige for bestemte planer.

## <a name="see-also"></a>Se også

[Business Central og OneDrive for Business Integration](across-onedrive-overview.md)  
[Åbner Business Central-filer i OneDrive](across-share-onedrive.md)  
[OneDrive Ofte stillede spørgsmål](admin-onedrive-faq.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
