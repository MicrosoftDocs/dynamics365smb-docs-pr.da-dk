---
title: Sådan konfigureres kunder til OIOUBL | Microsoft Docs
description: 'Hvis du vil oprette OIOUBL-dokumenter (Offentlig Information Online UBL) for debitorer i den offentlige sektor, skal du tilføje OIOUBL-oplysninger for de relevante debitorer.'
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: null
ms.date: 04/01/2021
ms.author: edupont
---
# <a name="set-up-customers-for-oioubl"></a>Konfigurere kunder til OIOUBL
Hvis du vil oprette OIOUBL-dokumenter (Offentlig Information Online UBL) for debitorer i den offentlige sektor, skal du tilføje OIOUBL-oplysninger for de relevante debitorer.  

 I dette emne beskrives kun de felter, der gælder for OIOUBL. Du kan finde flere oplysninger i [Registrere nye debitorer](../../sales-how-register-new-customers.md).  

### <a name="to-set-up-customers-for-oioubl"></a>Sådan konfigureres kunder til OIOUBL

1.  Vælg ![Lightbulb, der åbner funktionen Fortæl mig.](../../media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **Kunder**, og vælg derefter det relaterede link.  
2.  Åbn den kunde, du vil konfigurere aktivere til OIOUBL.  
3.  Udfyld felterne i oversigtspanelet **Fakturering** som beskrevet i følgende tabel.  

    |Felt|Beskrivelse|  
    |---------------------------------|---------------------------------------|  
    |**GLN**|Angiv debitorens GLN-lokationsnummer, der entydigt identificerer faktureringsadressen. Et GLN har en fast længde på 13 cifre. Det omfatter et tildelt præfiks for virksomheden, en placeringsreference og et kontrolciffer.|  
    |**Kontokode**|Angiv kontokoden for kunden.<br /><br /> Kunder i den offentlige sektor angiver en kontokode, når de afgiver en bestilling eller rekvisition. Baseret på værdien i dette felt medtages kontokoden i OIOUBL-dokumenter, du opretter i [!INCLUDE[prod_short](../../includes/prod_short.md)]. Ifølge **Lov om Offentlige Betalinger** og relaterede love har kunden ret til at tilbageholde betaling, indtil der modtages en faktura med den relevante kontokode.|  
    |**OIOUBL-profilkode**|Angiver den profil, som denne kunde kræver for elektroniske dokumenter, hvis den er anderledes end den standardprofil, du har angivet på siden **Salgsopsætning**.|  
    |**OIOUBL-profilkode kræves**|Angiver, om debitoren kræver en profilkode til elektroniske bilag. **Tip:** Hvis feltet **OIOUBL-profilkode kræves** er markeret, kan du ikke bogføre et salgsdokument for debitoren, medmindre du har angivet en profil.|  

 Disse felter er specifikke for OIOUBL. De værdier, der bruges i alle OIOUBL-dokumenter, du opretter for denne kunde. Du kan finde flere oplysninger i [Oversigt over elektronisk OIOUBL-fakturering](oioubl-electronic-invoicing-overview.md).  

## <a name="see-also"></a>Se også
[Lokal funktionalitet for Danmark](denmark-local-functionality.md)  
[Registrere nye debitorer](../../sales-how-register-new-customers.md)   
[Konfigurere OIOUBL](how-to-set-up-oioubl.md)   
[Oprette elektroniske dokumenter ved hjælp af OIOUBL](how-to-create-electronic-documents-by-using-oioubl.md)   
[Oversigt over elektronisk OIOUBL-fakturering](oioubl-electronic-invoicing-overview.md)  


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
