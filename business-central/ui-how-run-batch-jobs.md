---
title: Udføre kørsler og XMLporte
description: 'Du kører kørsler for at behandle data og opdatere oplysninger, f.eks. for at foretage periodiske regnskabsaktiviteter eller udføre beregninger.'
author: brentholtorf
ms.topic: conceptual
ms.devlang: al
ms.search.keywords: 'task, process'
ms.search.form: '672, 676, 682'
ms.date: 04/01/2021
ms.author: bholtorf
ms.service: dynamics-365-business-central
---
# Udføre kørsler og XMLporte

En kørsel er en rutine, hvor data behandles i bundter, f.eks. kørslen **Kursreguler valutabeholdninger**. Der findes kørsler, som udfører periodiske regnskabsaktiviteter, som f.eks. opgørelse af resultatopgørelsen ved afslutning af regnskabsåret. Mange kørsler udfører beregninger, som f.eks. beregningen af rentenotaer, kursjusteringer og beregning af salgspriser.

En kørsel minder om en rapport med den undtagelse, at kørslen bruger resultatet af sit arbejde til at opdatere oplysningerne direkte i stedet for at udskrive resultaterne.

Du kan planlægge, hvornår en kørsel skal udføres. Du kan finde flere oplysninger i [Bruge opgavekøer til at planlægge opgaver](admin-job-queues-schedule-tasks.md).

## Sådan foretages en kørsel
1. Hvis du vil åbne anmodningssiden for den relevante kørsel, skal du vælge ![lightbulb, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv navnet på batchjobbet, og vælg derefter det relaterede link.
2. Hvis der er et oversigtspanel med **Indstillinger** for kørslen, skal du udfylde felterne for at angive, hvad kørslen skal gøre.
3. Siden kan indeholde mere end et oversigtspanel med filtre, som du kan bruge til at begrænse de data, der inkluderes i kørslen. Du kan angive kriterier i de foreslåede filtre eller tilføje flere filtre.
4. Vælg **OK** for at starte kørslen.

## Se også
[Sortering af, søgning i og filtrering af lister](ui-enter-criteria-filters.md)  
[Bruge opgavekøer til at planlægge opgaver](admin-job-queues-schedule-tasks.md)  
[Arbejd med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]