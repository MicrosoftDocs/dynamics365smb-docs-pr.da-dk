---
title: Købstransaktioner for tredjeparter i EU
description: 'I denne artikel forklares det, hvordan du konfigurerer og bruger tredjepartskøbstransaktioner i Den Europæiske Union (EU).'
author: altotovi
ms.topic: conceptual
ms.devlang: al
ms.search.form: '50, 51, 52, 187, 317'
ms.search.keywords: 'EU3P, EU 3-P, EU 3-Party'
ms.date: 08/12/2024
ms.author: altotovi
ms.service: dynamics-365-business-central
ms.reviewer: bholtorf
---

# <a name="eu-third-party-purchase-transactions"></a>Købstransaktioner for tredjeparter i EU

Tredjepartshandel inden for EU (EU) forekommer, når du modtager en købsfaktura fra en kunde i ét EU-land/område, og produkterne sendes til et andet EU-land, uden at bopælslandet angives. Transaktionsbeløbet kan identificeres og rapporteres særskilt for at overholde visse EU-landes/områders krav til VAT Information Exchange System (system til udveksling af momsoplysninger). Microsoft Dynamics 365 Business Central gør det muligt at oprette købstransaktioner som EU-tredjepartshandel. Bogførte EU-tredjepartstransaktioner kan filtreres i momsangivelser og udelades fra beløbet i kolonnen **Salg til kunde** i rapporten **Moms – VIES-erklæring til momsgodkendelse**.

Selvom funktionen er forudinstalleret som en udvidelse, er den som standard ikke aktiveret. Følg disse trin for at aktivere funktionen.

1. Vælg ![Lightbulb, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") Vælg ikonet, gå til arbejdsområdet **Funktionsstyring**, og vælg derefter det relaterede link.
2. Vælg og find på listen **Funktionsopdatering: Erstat den eksisterende funktion med EU-tredjepartshandelskøb med den nye udvidelse til EU-tredjepartshandelskøb**.
3. Vælg **Alle brugere** i kolonnen **Aktivér for**.

> [!NOTE]
> Hvis du bruger den tyske eller italienske lokalisering, kan du ikke aktivere denne app, fordi den ikke er kompatibel med visse momsfunktioner i disse lokaliseringer.  

## <a name="enable-eu-third-party-trade-functionality-for-a-purchase"></a>Aktivere handel med EU-tredjepartsfunktioner til et køb

1. Vælg ![Lightbulb, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, angiv **Konfiguration af VAT** og vælg derefter det relaterede link.
2. Marker feltet **Aktiver EU-tredjepartskøbs** på feltet **Momsopsætning**.

## <a name="use-eu-third-party-trade-functionality"></a>Brug af EU-funktionalitet til handel med tredjepart

1. Vælg ![Lightbulb, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") , angiv **Købsfakturaer** (eller et andet købsdokument), og vælg derefter den relaterede sammenkæde.
2. Vælg en eksisterende købsfaktura, eller vælg **Ny** for at oprette en ny.
3. Marker afkrydsningsfeltet **EU-tredjepartshandel** i oversigtspanelet **Fakturadetaljer**.
4. Vælg **OK**.

## <a name="include-or-exclude-eu-third-party-trade-records-on-the-vat-statement"></a>Medtage eller udelukke EU-tredjeparts handelsposter på momsangivelsen

1. Vælg ![Lightbulb, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") Vælg ikon, angiv **Momsangivelser**, og vælg derefter det relaterede link.
2. På siden **Momsangivelse** skal du vælge en af følgende indstillinger for at få vist EU-tredjeparts brancheposter ved hjælp af feltet **EU-tredjepartshandel**.

    | Indstilling | Beskrivelse |
    |--------|-------------|
    | Alle | Vis alle poster, uanset om feltet **EU-tredjepartshandel** i dokumenter er markeret. |
    | EU3 | Vis kun poster, hvor feltet **EU-tredjepartshandel** i dokumenter er markeret. |
    | ikke-EU3 | Vis kun poster, hvor feltet **EU-tredjepartshandel** i dokumenter er markeret. |

## <a name="see-also"></a>Se også
[Økonomistyring](finance.md)    
[Arbejde med Business Central](ui-work-product.md)    

[!INCLUDE[footer-include](includes/footer-banner.md)]
