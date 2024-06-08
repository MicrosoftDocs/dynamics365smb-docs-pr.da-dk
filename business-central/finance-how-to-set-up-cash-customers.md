---
title: Konfigurere kontantkunder
description: 'I dette emne beskrives de trin, der er nødvendige for at oprette fakturaen med et debitornummer for debitorer, der betaler kontant.'
author: brentholtorf
ms.topic: conceptual
ms.devlang: al
ms.search.form: '21, 22'
ms.date: 06/16/2021
ms.author: bholtorf
ms.service: dynamics-365-business-central
---
# <a name="set-up-cash-customers"></a>Konfigurere kontantkunder

Du kan ikke oprette en faktura uden et debitornummer. Det gælder også, hvis du sælger kontant og ikke har noget at registrere i en kundekonto.  

## <a name="to-set-up-a-cash-customer"></a>Definere en kontantkunde

1. Vælg ![Lightbulb, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **Debitor**, og vælg derefter det relaterede link.  
2. Opret et nyt kort for en **Kunde**. Du kan finde flere oplysninger i [Registrere nye debitorer](sales-how-register-new-customers.md).
3. I feltet **Nummer** skal du f.eks. angive **Kontant**.  
4. Angiv f.eks. **Kontantsalg** i feltet **Navn**.  
5. I oversigtspanelet **Fakturering** skal du udfylde felterne **Debitorbogføringsgruppe** og feltet **Virksomhedsbogføringsgruppe**.  

 Du har nu angivet en debitor, der indeholder tilstrækkelige oplysninger til fakturering.  

> [!NOTE]  
> Du kan vælge en bogføringsgruppe, der også anvendes til indenlandsk kreditsalg. Hvis du vil have separate salgstal for kontantsalg, f.eks. på en særlig salgskonto, kan du angive en ekstra bogføringsgruppe til dette formål.  
>
> Du skal angive et nummer til salgskonto for bogføringsgruppen, også selvom saldoen altid vil være 0, når du har bogført en faktura.  

## <a name="see-also"></a>Se også

[Administrere tilgodehavender](receivables-manage-receivables.md)  
[Registrere nye debitorer](sales-how-register-new-customers.md)
[Finance](finance.md)  



[!INCLUDE[footer-include](includes/footer-banner.md)]
