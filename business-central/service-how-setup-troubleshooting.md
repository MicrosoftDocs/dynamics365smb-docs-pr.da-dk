---
title: Konfigurere fejlfindingsprocesser | Microsoft Docs
description: 'Få at vide, hvordan du konfigurerer processer, som hjælper servicerepræsentanter med at identificere og løse problemer med serviceartikler.'
author: brentholtorf
ms.topic: conceptual
ms.devlang: al
ms.search.keywords: 'service, service item, troubleshoot, repairs, maintenance'
ms.date: 04/01/2021
ms.author: bholtorf
ms.service: dynamics-365-business-central
ms.reviewer: bholtorf
---

# Opsætning af fejlfinding for serviceartikler
Du kan angive fejlfindingsretningslinjer, som hjælper teknikere med at løse problemer, når de yder service. Retningslinjerne kan f.eks. være en række trin, der skal udføres i forbindelse med en reparation, eller en række spørgsmål, der skal stilles om varerne. Når du har konfigureret retningslinjerne for fejlfinding, kan du tildele dem til serviceartikelgrupper, serviceartikler og varer. Der er et nedarvningshierarki for retningslinjer. Hvis du tildeler dem til en serviceartikelgruppe, arver de varer, der indgår i gruppen, retningslinjerne, medmindre du angiver retningslinjer for varerne. Desuden arver serviceartikler retningslinjer fra varer.  

## Definere retningslinjer for fejlfinding
1. Vælg ![Lightbulb, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **Fejlfinding**, og vælg derefter det relaterede link.  
2. Udfyld felterne efter behov. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]  

## Sådan tildeles retningslinjer for fejlfinding til varer, serviceartikler eller serviceartikelgrupper.
1. Vælg ![Lightbulb, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") Skal du angive **Varer** eller **Serviceartikler** eller **Serviceartikelgrupper**, og vælg derefter det relaterede link.  
2. Vælg den relevante enhed, og vælg derefter handlingen **Fejlfinding**.  

## Se også
[Service Management](service-service.md)

[!INCLUDE[footer-include](includes/footer-banner.md)]