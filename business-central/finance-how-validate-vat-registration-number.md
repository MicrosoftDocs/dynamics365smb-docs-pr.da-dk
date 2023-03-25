---
title: Valider et SE/CVR-nr.
description: 'Lad Business Central validere momsregistreringsnummeret for kontakter, debitorer og kreditorer, baseret på den Europæiske Unions liste momsnummervalideringsservice.'
author: andregu
ms.topic: conceptual
ms.reviewer: edupont
ms.search.keywords: 'VAT, posting, tax, value-added tax'
ms.search.form: '249, 575, 1279'
ms.date: 06/16/2021
ms.author: andregu
---

# Valider et SE/CVR-nr.

Det er vigtigt, at de momsregistreringsnumre, du har for debitorer, kreditorer og kontakter, er gyldige, hvis du anvender [!INCLUDE [prod_short](includes/prod_short.md)] i et land, der bruger moms. F.eks. ændrer virksomheder nogle gange deres status for skattetilsvar, og i visse lande/områder kan skattemyndighederne måske bede dig om at indsende rapporter, f.eks. rapportering af **EU-salg** med de momsnumre, du bruger, når du handler.

Kommissionen har VIES-tjenesten til kontrol af momsnumre på deres websted, som er offentlig og gratis. [!INCLUDE [prod_short](includes/prod_short.md)] kan spare dig for et trin, idet du kan bruge VIES-tjenesten til at validere og spore momsnumre for kunder og andre virksomhedsoplysninger for debitorer, kreditorer og kontakter. Tjenesten i [!INCLUDE [prod_short](includes/prod_short.md)] hedder **Service for validering af SE/CVR-nr. for EU**. Tjenesten findes på siden **Serviceforbindelser**, og du kan begynde at bruge den med det samme. Tjenesteforbindelsen er gratis, og yderligere tilmelding er ikke nødvendig.

## Konfigurere servicen til at kontrollere momsregistreringsnummeret automatisk

Aktivere **Service for validering af SE/CVR-nr. for EU** ved at åbne posten på siden **Serviceforbindelse**. Hvis feltet **Serviceslutpunkt** ikke allerede er udfyldt, skal du bruge funktionen **Angiv standardslutpunkt**. Angiv derefter feltet **Aktiveret**, og så er du klar til at gå i gang.  

> [!IMPORTANT]
> For at aktivere valideringsservice skal du have administratorrettigheder.

Du kan også vælge at konfigurere skabeloner for de typer momsrelaterede data, som servicen også skal kontrollere. Du kan finde flere oplysninger i afsnittet [Valideringsskabeloner](#validation-templates).

Når du bruger tjenesteforbindelsen, registrerer vi en oversigt over momsnumre og kontrol for hver debitor, kreditor eller kontaktperson, i **Log over SE/CVR-nr.**, så du nemt kan spore dem. Loggen er specifik for hver debitor. Eksempelvis er loggen nyttig, hvis du vil bevise, at du har kontrolleret, at det aktuelle momsnummer er korrekt. Når du kontrollerer et momsnummer, afspejler kolonnen **Anmodnings-id** i loggen, at du har udført en handling.

Du kan få vist Log over SE/CVR-nr. på debitor-, kreditor- eller kontaktkort på oversigtspanelet **Fakturering** ved at vælge opslagsknappen i feltet **SE/CVR-nr.**  

Der er et par ting at bemærke om VIES-tjenesten til kontrol af momsnumre:

* Tjenesten bruger HTTP-protokollen, hvilket betyder, at data, der overføres via tjenesten, ikke er krypterede.  
* Du kan opleve nedetid for denne tjeneste, som Microsoft ikke kan holdes ansvarlig for. Tjenesten er en del af et bredt EU-netværk af nationale momsregistre.

> [!IMPORTANT]
> Det er dit ansvar at kontrollere, at dataene er gyldige. Af og til returneres data med fejl af VIES-tjenesten til kontrol af momsregistreringsnumre. Hvis valideringen mislykkes, skal du validere momsregistreringsnummeret på [webstedet](https://ec.europa.eu/taxation_customs/vies/), udskrive resultatet eller gemme det på en fælles placering og derefter tilføje linket til posten for din kunde, leverandør eller kontaktperson. Du kan få flere oplysninger i [Administrere vedhæftede filer, links og noter på kort og dokumenter](ui-how-add-link-to-record.md).

## Valideringsskabeloner

Du kan også kontrollere andre virksomhedsoplysninger, f.eks. adressen, samt se/CVR-nummeret ved hjælp af listetjenesten. Opret i feltet **Se/CVR-nr. Siden validerings skabeloner** en post for hvert land, du vil have valideret nærmere for, og angiv derefter de oplysninger, som du vil have valideret automatisk.  

Tilføj f.eks. en post for Spanien, hvor du vil have valideret navn, adresse, by-og postnummer og derefter en anden post for Tyskland, hvor du kun vil have valideringen af postnummeret. Derefter skal du i feltet **Serviceopsætning for validering af SE/CVR-nr. for EU** du angive standardskabelonen.  

> [!NOTE]
> Kontroller altid, at standardskabelonen passer til dine behov. Du kan ændre standardindstillingen, så den passer til dine behov, f.eks. validering af alle felter eller ingen felter.

Næste gang du angiver et Se/CVR-nummer, validerer service nummeret og de yderligere data, der er fastsat i dine validerings skabeloner. Hvis de angivne værdier er forskellige fra de værdier, der returneres af tjenesten, vises detaljerne på siden **valideringsoplysninger**, hvor du kan acceptere eller nulstille værdierne.  

## Se også

[Konfigurere moms](finance-setup-vat.md)  
[Opsætning af ikke-realiseret moms](finance-setup-unrealized-vat.md)  
[Rapportere moms til skattemyndighederne](finance-how-report-vat.md)  
[Arbejde med moms af salg og køb](finance-work-with-vat.md)  
[Lokal funktionalitet i Business Central](about-localization.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
