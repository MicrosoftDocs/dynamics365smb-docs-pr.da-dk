---
title: Konfigurere OIOUB-udvidelsen til elektronisk fakturering | Microsoft Docs
description: 'Beskriver, hvad du skal udføre for at blive klar til at sende salgsdokumenter i et OIOUBL-format (Offentlig oplysninger Online - Universal Business Language).'
author: brentholtorf
ms.topic: conceptual
ms.devlang: al
ms.search.keywords: null
ms.date: 04/01/2021
ms.author: bholtorf
ms.service: dynamics-365-business-central
ms.reviewer: bholtorf
---
# <a name="set-up-oioubl"></a>Konfigurere OIOUBL

Du skal angive en placering til lagring af OIOUBL-filer (Offentlig Information Online UBL), når du opretter elektroniske dokumenter som f.eks. fakturaer eller kreditnotaer. Du skal også definere betalingsformer, betalingsbetingelser og varegebyrer, og du skal oprette relevante kunder til OIOUBL.  

* Konfigurere betalingsbetingelser og varegebyrer.  
* Konfigurere kunder til OIOUBL.  

### <a name="about-oioubl-profiles"></a>Om OIOUBL-profiler

OIOUBL-profiler er tilpasninger af forretningsprocesser til forskellige typer transaktioner og afhænger af typerne af og oplysningerne i de dokumenter, der udveksles. I Danmark er de to profiler, der skal bruges, profilerne **Simpel fakturaproces** (Procurement-OrdSim-BilSim-1.0) og **Grundlæggende fakturering** (urn:www.nesubl.eu:profiles:profile5:ver2.0). Profilen Grundlæggende fakturering er baseret på NES (Northern European Subset). Kunden skal kunne modtage dokumenter på én af disse profiler. Hvis du ikke er sikker, skal du spørge kunden om, hvilken profil de kræver. Du kan finde flere oplysninger i emnet om OIOUBL-profiler i afsnittet Ofte stillede spørgsmål på [Digitaliseringsstyrelsen](https://aka.ms/Digitaliseringsstyrelsen).  

Standardprofilen for alle debitorer er profilen Simpel fakturaproces, der er valgt på siden **Opsætning af salg og tilgodehavender**. Du kan angive profilen for en bestemt kunde på kortet **Debitor**. Hvis du vil bruge profilen Grundlæggende fakturering, skal du tilføje den. Det gør du ved på siden **Opsætning af salg og tilgodehavender** at klikke på knappen i feltet **Standardprofilkode** og derefter vælge **Ny**. Angiv et navn for koden, og i feltet **Profil** skal du derefter angive **urn:www.nesubl.eu:profiles:profile5:ver2.0**. Du kan derefter vælge profilen, enten som standardprofilen eller for en eller flere debitorer.

## <a name="to-set-up-payment-terms"></a>Sådan defineres betalingsbetingelser

Hvis du angiver betalingsbetingelserne for debitorer, medtages de elektroniske dokumenter rabatter, som du giver for førtidige betalinger.

1.  Vælg ![Lightbulb, der åbner funktionen Fortæl mig.](../../media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **Betalingsbetingelser**, og vælg derefter det relaterede link.  
2.  I feltet **OIOXML-kode** skal du vælge en kode for hver betalingsbetingelse, du vil bruge til elektroniske fakturaer.  

### <a name="to-set-up-customers-for-oioubl"></a>Sådan konfigureres kunder til OIOUBL

Du kan bruge debitorskabelonen **Offentlig kunde (OIOXML)** til at anvende standardindstillinger for OIOUBL til en ny debitor, eller funktionen **Anvend skabelon**, hvis du vil anvende indstillingerne i skabelonen til en eksisterende kunde. Nedenfor beskrives, hvordan du manuelt kan udfylde de obligatoriske felter til OIOUBL. <!--need to check whether this overwrites anything for existing customers-->

1.  Vælg ![Lightbulb, der åbner funktionen Fortæl mig.](../../media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **Kunder**, og vælg derefter det relaterede link.  
2.  Åbn den kunde, du vil konfigurere aktivere til OIOUBL.  
3.  Angiv debitorens adresse. Sørg for, at du angiver en lande/områdekode og kontaktoplysninger for kundeattentionpersonen.  
4.  I feltet **Dokumentafsendelsesprofil**, skal du vælge profilen **OIOUBL**.
5.  Udfyld felterne i oversigtspanelet **Fakturering** som beskrevet i følgende tabel.  

    > [!Tip]
    > For at få vist alle felterne, skal du måske vælge **Vis mere** i oversigtspanelet **Fakturering**.

    |Felt|Beskrivelse|  
    |---------------------------------|---------------------------------------|
    |**GLN**|Angiv GLN-lokationsnummeret for debitoren. |  
    |**Kontokode**|Angiv kontokoden for kunden.<br /><br /> Kunder i den offentlige sektor angiver en kontokode, når de afgiver en bestilling eller rekvisition. Baseret på værdien i dette felt medtages kontokoden i OIOUBL-dokumenter, du opretter i [!INCLUDE[prod_short](../../includes/prod_short.md)]. Ifølge **Lov om Offentlige Betalinger** og relaterede love har kunden ret til at tilbageholde betaling, indtil der modtages en faktura med den relevante kontokode. |  
    |**Profilkode**|Angiver den profil, som denne kunde kræver for elektroniske dokumenter, hvis den er anderledes end den standardprofil, du har angivet på siden **Salgsopsætning**.|  
    |**Profilkode kræves**|Angiver, om debitoren kræver en profilkode til elektroniske bilag.<br /><br /> **Tip** <br /> Hvis feltet **Profilkode kræves** er markeret, kan du ikke bogføre et salgsdokument for debitoren, medmindre du har angivet en profil.|  

6. I feltet **Betalingsbetingelser**, skal du vælge de betingelser, som du forventer, at kunden skal betale.

Du kan finde flere oplysninger om, hvordan du opretter en debitor i [Registrere nye debitorer](../../sales-how-register-new-customers.md).

## <a name="to-set-up-item-charges"></a>Sådan konfigureres varegebyrer

1.  Vælg ![Lightbulb, der åbner funktionen Fortæl mig.](../../media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **varegebyrer**, og vælg derefter det relaterede link.  
2.  For hvert varegebyr, skal du vælge en kategori i feltet **Gebyrkategori**.  

Endelig skal du angive EAN-numre og kontokoder for de relevante debitorer. Du kan få flere oplysninger i [Konfigurere kunder til OIOUBL](how-to-set-up-customers-for-oioubl.md).  

## <a name="see-also"></a>Se også

[Lokal funktionalitet for Danmark](denmark-local-functionality.md)  
[Oversigt over elektronisk OIOUBL-fakturering](oioubl-electronic-invoicing-overview.md)   
[Konfigurere kunder til OIOUBL](how-to-set-up-customers-for-oioubl.md)   

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
