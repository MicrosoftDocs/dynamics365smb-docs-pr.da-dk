---
title: Valider et SE/CVR-nr.
description: Lad Business Central bruge liste tjenesten til at validere momsregistreringsnummeret automatisk.
author: kielkenny
ms.service: dynamics365-business-central
ms.topic: article
ms.reviewer: edupont
ms.search.keywords: VAT, posting, tax, value-added tax
ms.date: 10/01/2020
ms.author: andregu
ms.openlocfilehash: 80e955e96a64c5a0bd91d0a72297b32d67ff4ab6
ms.sourcegitcommit: 2e7307fbe1eb3b34d0ad9356226a19409054a402
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 12/17/2020
ms.locfileid: "4750552"
---
# <a name="validate-vat-registration-numbers"></a>Valider et SE/CVR-nr.

Det er vigtigt, at de momsregistreringsnumre, du har for debitorer, kreditorer og kontakter, er gyldige. F.eks. ændrer virksomheder nogle gange deres status for skattetilsvar, og i visse lande/områder kan skattemyndighederne måske bede dig om at indsende rapporter, f.eks. rapportering af EU-salg med de momsnumre, du bruger, når du handler.

Kommissionen har VIES-tjenesten til kontrol af momsnumre på deres websted, som er offentlig og gratis. [!INCLUDE[prod_short](includes/prod_short.md)] kan spare dig for et trin, idet du kan bruge VIES-tjenesten til at validere og spore momsnumre for kunder, leverandører og kontakter direkte fra debitor-, kreditor- og kontaktkort. Tjenesten i [!INCLUDE[prod_short](includes/prod_short.md)] hedder **Service for validering af SE/CVR-nr. for EU**. Tjenesten findes på siden **Serviceforbindelser**, og du kan begynde at bruge den med det samme. Tjenesteforbindelsen er gratis, og tilmelding er ikke nødvendig.

## <a name="to-verify-vat-registration-numbers"></a>Sådan kontrollere SE/CVR-numre

For at kunne aktivere **Service for validering af SE/CVR-nr. for EU** skal du åbne posten på siden **Serviceforbindelse**. Feltet **Slutpunkt for tjeneste** skal allerede være udfyldt. Hvis ikke, kan du bruge handlingen **Angiv standardslutpunkt**. Angiv derefter feltet **Aktiveret**, og så er du klar til at gå i gang.

> [!NOTE]
> For at aktivere service for validering af SE/CVR-nr. for EU skal du have administratorrettigheder.

Når du bruger tjenesteforbindelsen, registrerer vi en oversigt over momsnumre og kontrol for hver debitor, kreditor eller kontaktperson, i **Log over SE/CVR-nr.**, så du nemt kan spore dem. Loggen er specifik for hver debitor. Eksempelvis er loggen nyttig, hvis du vil bevise, at du har kontrolleret, at det aktuelle momsnummer er korrekt. Når du kontrollerer et momsnummer, afspejler kolonnen **Anmodnings-id** i loggen, at du har udført en handling.

Du kan få vist Log over SE/CVR-nr. på debitor-, kreditor- eller kontaktkort på oversigtspanelet **Fakturering** ved at vælge opslagsknappen i feltet **SE/CVR-nr.**  

Tjenesten kan også spare dig tid, når du opretter en debitor eller kreditor. Hvis du kender debitorens momsnummer, kan du angive det i feltet **SE/CVR-nr.** på debitor- eller kreditorkortene, og vi vil udfylde debitornavnet for dig. Nogle lande/områder angiver også virksomhedsadresser i et struktureret format. I disse lande/områder udfylder vi også adressen.  

Der er et par ting at bemærke om VIES-tjenesten til kontrol af momsnumre:

* Tjenesten bruger HTTP-protokollen, hvilket betyder, at data, der overføres via tjenesten, ikke er krypterede.  
* Du kan opleve nedetid for denne tjeneste, som Microsoft ikke kan holdes ansvarlig for. Tjenesten er en del af et bredt EU-netværk af nationale momsregistre.

> [!IMPORTANT]
> Det er dit ansvar at kontrollere, at dataene er gyldige. Af og til returneres data med fejl af VIES-tjenesten til kontrol af momsregistreringsnumre. Hvis valideringen mislykkes, skal du validere momsregistreringsnummeret på [webstedet](https://ec.europa.eu/taxation_customs/vies/), udskrive resultatet eller gemme det på en fælles placering og derefter tilføje linket til posten for din kunde, leverandør eller kontaktperson. Du kan få flere oplysninger i [Administrere vedhæftede filer, links og noter på kort og dokumenter](ui-how-add-link-to-record.md).

## <a name="see-also"></a>Se også

[Konfigurere moms](finance-setup-vat.md)  
[Opsætning af ikke-realiseret moms](finance-setup-unrealized-vat.md)  
[Rapportere moms til skattemyndighederne](finance-how-report-vat.md)  
[Arbejde med moms af salg og køb](finance-work-with-vat.md)  
[Lokal funktionalitet i Business Central](about-localization.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]