---
title: Oprette læg-på-lager-skabeloner
description: Brug læg-på-lager-skabeloner for at få foreslået de mest velegnede placeringer til dig på et hvilket som helst tidspunkt.
author: brentholtorf
ms.topic: conceptual
ms.devlang: al
ms.search.form: '7312, 7313, 7314, 7321, 7322, 7323, 7329'
ms.date: 10/04/2023
ms.author: bholtorf
ms.service: dynamics-365-business-central
---
# <a name="set-up-put-away-templates"></a>Oprette læg-på-lager-skabeloner

Hvis du benytter styret læg-på-lager og pluk, foreslås den til enhver tid mest velegnede placering til varer ifølge den læg-på-lager-skabelon, du har defineret til lagerstedet, de placeringsniveauer, du har tildelt placeringerne, og de minimum- og maksimumantal, du har angivet for faste placeringer.  

Du kan oprette en række læg-på-lager-skabeloner og vælge en af som standardskabelon for læg-på-lager-aktiviteter. Du kan også vælge en bestemt skabelon til en vare eller lagervare, som der er specielle krav til i forbindelse med læg-på-lager-aktiviteter.  

## <a name="to-set-up-put-away-templates"></a>Sådan oprettes læg-på-lager-skabeloner

1. Vælg ![Lightbulb, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **Læg-på-lager-skabeloner**, og vælg derefter det relaterede link.  
2. Vælg handlingen **Ny**.  
3. Indtast en kode som entydig id for skabelonen.  
4. Indtast evt. en kort beskrivelse.  
5. Brug den første linje til at angive de krav til placeringer, som du ønsker, først og fremmest skal være overholdt, når der foreslås en læg-på-lager-aktivitet.

    Hvis standardmetoden for læg-på-lager f.eks. skal baseres på faste placeringer, skal du vælge feltet **Find fast placering**. [!INCLUDE[tooltip-inline-tip_md](includes/tooltip-inline-tip_md.md)]  
6. Brug den anden linje til at angive de sekundære krav til placeringer, som skal overholdes, når der skal findes en placering for en læg-på-lager-aktivitet. Den anden linje bruges kun, hvis en placering, der overholder kravene på den første linje, ikke kan findes.  
7. Fortsæt med at udfylde linjerne, indtil du har beskrevet alle de acceptable placeringer, som du vil bruge til læg-på-lager-aktiviteter.  
8. Marker afkrydsningsfeltet **Find løs placering** på den nederste linje i skabelonen.  

Du kan oprette en række læg-på-lager-skabeloner og bruge dem efter behov. Den læg-på-lager-skabelon, som du har valgt til varen eller lagervaren, hvis en sådan er oprettet, benyttes først. Hvis felterne her ikke er udfyldt, anvendes den læg-på-lager-skabelon, du har valgt til lagerstedet i oversigtspanelet **Placeringsmetode** på lokationskortet.  

## <a name="see-also"></a>Se også

[Warehouse Management-oversigt](design-details-warehouse-management.md)
[Lager](inventory-manage-inventory.md)                                
[Sådan konfigureres Warehouse Management](warehouse-setup-warehouse.md)  
[Arbejd med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
