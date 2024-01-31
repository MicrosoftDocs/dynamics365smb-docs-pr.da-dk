---
title: Anmeldelse og tilmelding til NemHandelsregisteret i Danmark
description: 'Denne artikel beskriver, hvordan du håndterer anmeldelse og tilmelding til NemHandelsregisteret i Danmark.'
author: altotovi
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 'nemhandel, nemhandelsregisteret, notification, registration, denmark'
ms.search.form: 1
ms.date: 11/17/2023
ms.author: altotovi
ms.service: dynamics-365-business-central
---

# Anmeldelse og tilmelding til NemHandelsregisteret i Danmark

Ifølge dansk bogføringslov skal alle standardsystemer fra januar 2024 give brugerne besked om, at de kan tilmelde sig NemHandelsregisteret. De skal også oplyse om registreringsfunktionaliteten.

Derudover, hvis virksomheden ikke er registreret i NemHandelsregisteret, vises en meddelelse øverst på siden med registreringsinstruktioner.

## Meddelelse om ikke at være tilmeldt

Hvis virksomheden ikke er registreret i NemHandelsregisteret, modtager du følgende meddelelse: "Dit regnskabsprogram er ikke registreret i Nemhandelsregisteret." Du kan gennemføre registreringsprocessen direkte fra meddelelsen ved at vælge enten linket **Tilmeld dig i Nemhandelsregisteret** eller linket **Åben tilmeldingsguide**. Begge links leder dig til det eksterne Nemhandel-indhold.

Hvis virksomheden allerede er registreret, og hvis et gyldigt CVR-nummer (Central Business Register) er indtastet i **Registreringsnr.** feltet på siden **Virksomhedsinformation**, meddelelsen vises ikke.

> [!NOTE]
> En meddelelse vises på siden **Virksomhedsoplysninger** og på følgende rollecentre: Bogholder, Business Manager, Administration af brugere, sikkerhedsgrupper og tilladelser, Salgsordrebehandler og Salg og Forholdsmanager.

## Tilmelding til NemHandelsregisteret 

> [!IMPORTANT]
> Før du begynder registreringen, skal du indtaste et gyldigt CVR-nummer i feltet **Registreringsnr.** på siden **Virksomhedsoplysninger**.

For at starte registreringen skal du vælge linket **Tilmeld dig i Nemhandelsregisteret** i meddelelsen. Inden de eksterne systemopkald foretages, eller før du åbner NemHandelsregisteret tilmeldingsformular, skal du bekræfte dit samtykke.

Efter du har gennemført tilmeldingen til NemHandelsregisteret, forsvinder den eksisterende anmeldelse, fordi Microsoft Dynamics 365 Business Central bekræfter, at virksomhedens CVR-nummer fra feltet **Registreringsnr.** på siden **Virksomhedsoplysninger** er blevet registreret i NemHandelsregisteret gennem API-kaldet. I Business Centrals interne registreringer har virksomheden status som **registreret i NemHandelsregisteret**.

## Andre vigtige fakta

Hvis virksomheden er registreret i NemHandelsregisteret, og hvis den har indstillet felterne **Momsregistreringsnr.** og **Registreringsnr.** på siden **Virksomhedsoplysninger**, kan du ikke slette virksomheden fra siden **Virksomheder**. Denne begrænsning eksisterer, fordi virksomheden er en produktionsvirksomhed i dette tilfælde, og du kan ikke slette produktionstransaktioner.

Derudover, når du vælger **Kopier** på siden **Virksomheder**, oprettes det nye firma, og felterne **Registreret hos Nemhandel** og **Registreringsnr.** efterlades tomme.

> [!NOTE]
> Disse begrænsninger virker kun, hvis miljøet er et produktionsmiljø. I et sandkassemiljø kan du slette virksomheden uden begrænsninger. 
>
> Hvis du ikke indtaster et gyldigt CVR-nummer i feltet **Registreringsnr.**, kan du bruge e-dokumenter i Danmark.

## Se også

[Økonomistyring](../../finance.md)  
[Oversigt over momsstyring](../../finance-manage-vat.md)  
[Oversigt over e-dokumenter](../../finance-edocuments-overview.md)

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
