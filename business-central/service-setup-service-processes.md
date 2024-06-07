---
title: Konfigurere Service-processer
description: 'Få at vide, hvordan du konfigurerer processer, der er med til at sikre, at dine kunder er tilfredse med din service.'
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bholtorf
ms.topic: how-to
ms.search.keywords: 'service, number sequences, setup, warnings, fee, contracts, warranties'
ms.date: 02/27/2024
ms.service: dynamics-365-business-central
ms.custom: bap-template
---

# <a name="configure-service-management-processes"></a>Konfigurere Service-processer

Følgende er nogle eksempler på de indstillinger, du kan anvende på Service-processer:  
  
* Generelle indstillinger for forskellige processer, f.eks. advarsler, næste service-beregninger for serviceartikler, startgebyr til vurdering, det fejlrapporteringsniveau, der skal bruges, osv.  
* Typerne af oplysninger, som teknikere angiver i servicedokumenter. Du kan f.eks. kræve, at de angiver ordretypen, start-og/eller slutdatoer for arbejdet, og typen af arbejde, der blev udført.  
* Nogle standardindstillinger for svartider og garantier. Det kan være en standardsvartid for start af tjenesten, rabatprocenter for garantien på reservedele og arbejde og hvor lang tid garantier gælder.  
* Indstillinger for kontrakter, f.eks. det maksimale antal dage, som du kan bruge til kontraktserviceordrer, om der skal bruges årsagskoder, når en kontrakt annulleres, standardtekster til beskrivelser og kontraktværdier.  
* De nummerserier, der skal bruges til servicerelaterede dokumenter og varer.  

## <a name="to-enter-general-and-mandatory-settings"></a>Sådan angives generelle og obligatoriske indstillinger

1. Vælg ![Lightbulb, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, angiv **Serviceopsætning**, og vælg derefter det relaterede link.
2. Udfyld felterne efter behov. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]  

## <a name="set-up-service-invoice-posting-policies-for-users"></a>Konfigurere politikker for bogføring af servicefakturaer for brugere

Virksomheder har ofte forskellige processer til fakturaer og leverancer. Processer kan f.eks. variere fra én person, der bogfører alt på en serviceordre, til flere medarbejdere, der hver især arbejder med deres egne sider.

Du kan bruge bogføringspolitikker til at forhindre brugere i at bogføre servicefakturaer eller til at kræve, at de bogfører fakturaer sammen med den relaterede serviceleverance. Hvis du vil konfigurere en bogføringspolitik, skal du gå til siden **Brugeropsætning**, gå til feltet **Politik til bogføring af servicefaktura** og vælge en af følgende indstillinger:

* **Tilladt** (standard): Bevar den aktuelle funktionsmåde, hvor du kan vælge bogføringsindstillingerne, f.eks. **Lever**, **Fakturer** og **Lever og fakturer**.
* **Forbudt**: Forhindrer brugere i at bogføre servicefakturaer. [!INCLUDE [prod_short](includes/prod_short.md)] viser en bekræftelsesdialogboks, der kun indeholder indstillingen **Lever**.
* **Obligatorisk**: Giver brugere mulighed for at bogføre fakturaer sammen med serviceleverancer. [!INCLUDE [prod_short](includes/prod_short.md)] viser en bekræftelsesdialogboks, der kun indeholder indstillingen **Lever og fakturer**.

Denne indstilling påvirker følgende dokumenter:

* Serviceordrer
* Lagerstedsleverancer
* Servicefakturaer
* Servicekreditnotaer

Den følgende tabel beskriver, hvordan de forskellige dokumenter påvirkes.

|Dokument  |Tillad<br>Viser en række muligheder   |Forhindret<br>Bekræftelsesdialogboks  |Obligatorisk<br>Bekræftelsesdialogboks  |
|---------|---------|---------|---------|
|Serviceordre     | * Lever<br>* Fakturer<br>* Lever og fakturer<br>* Send og forbrug         |* Lever<br>* Send og forbrug  |Skal forsendelsen bogføres og faktureres?         |
|Lagerstedsforsendelse     |* Lever<br>* Lever og fakturer         |Vil du bogføre leveringen?         | Skal forsendelsen bogføres og faktureres?        |
|Servicefaktura     | Vil du bogføre fakturaen?         | Fejl: Du kan ikke bogføre.       |Vil du bogføre fakturaen?         |
|Servicekreditnota     | Vil du bogføre kreditnotaen?         | Fejl: Du kan ikke bogføre.        |Vil du bogføre kreditnotaen?         |

> [!NOTE]
> Når du bogfører servicefakturaer og kreditnotaer, har du ingen bogføringsmuligheder. Dokumenterne bogfører altid fysiske og økonomiske transaktioner samlet. Du kan ikke bogføre servicefakturaer og kreditnotaer delvist.

## <a name="see-also"></a>Se også

[Konfigurere fejlrapportering](service-how-setup-fault-reporting.md)  
[Konfigurere ressourceallokering](service-how-setup-resource-allocation.md)  
[Definere koder for standardservices](service-how-setup-service-coding.md)  
[Konfigurere ekstra omkostninger for tjenester](service-how-setup-service-costs-pricing.md)  
[Konfigurere fejlfinding](service-how-setup-troubleshooting.md)  
[Service Management](service-service.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
