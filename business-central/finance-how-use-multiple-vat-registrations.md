---
title: Flere momsregistreringsnumre
description: Få mere at vide om funktionaliteten for flere (alternative) momsregistreringsnumre.
author: altotovi
ms.topic: conceptual
ms.reviewer: null
ms.search.keywords: 'VAT, multiple, alternative, customer, tax, value-added tax'
ms.search.form: '212, 301,'
ms.date: 08/21/2024
ms.author: altotovi
ms.service: dynamics-365-business-central
---

# <a name="multiple-vat-registration-numbers"></a>Flere momsregistreringsnumre

For virksomheder med lagre i flere EU-lande kan det være en udfordring at administrere moms (moms), da hver lagerlokation kræver et andet momsnummer for at overholde de specifikke regler i hvert land. Denne artikel indeholder oplysninger om dette krav og forklarer funktionaliteten for momsregistreringsnumre. Denne funktion giver brugerne mulighed for at oprette momsregistreringsnumre for kunderne i forskellige lande/områder.  

> [!NOTE]
> Funktionaliteten *Flere momsnumre for debitorer* er kun tilgængelig fra Business Central 2024 udgivelsesbølge 2 (version 25).

## <a name="how-to-set-up-the-alternative-vat-registration-numbers"></a>Sådan defineres alternative momsregistreringsnumre

Hvis du vil konfigurere alternative momsregistreringsnumre for forskellige lande/områder, skal du følge disse trin: 

1. Vælg ![Lightbulb, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") , angiv **Momsregistrering** for alternativ debitor, og vælg derefter de relaterede sammenkæde. 
2. Tilføj debitoren i feltet Debitornr **.** og det land/område, der er relateret til denne momsregistrering, i lande-/områdekoden for **moms**.  
3. Du skal tilføje momsnummeret i SE/CVR-nummeret **.** mark. Du skal holde dig til formatet, når du bruger **Lande-/områdekode**. 
4. Hvis du vil bruge forskellige momsbogføringsgrupper eller generelle bogføringsgrupper, kan du alternativt tilføje dem til opsætningen i felterne **Momsvirksomhedsbogf.gruppe** og **Virksomhedsbogføringsgruppe** . 
5. Luk siden.   

Følg trinnene for at oprette en alternativ adresse til din kunde:  

1. Åbn **Debitor**  kort for den debitor, du vil tilføje ny **leveringsadresse**. 
2. Vælg **Debitor**, og vælg handlingen **Leveringsadresser** .   
3. Siden **Lev.adresseliste** åbnes og vælger **Ny**. 
4. Angiv oplysningerne om kundens leveringsdestination.  
5. Vælg den korrekte **lande-/områdekode**.   
6. Hvis du allerede har konfigureret et nyt **SE/CVR-nr.**  **på den alternative debitormomsregistrering** for dette land eller område, sker der intet. 
7. Men hvis du ikke har konfigureret SE/CVR-nummeret **.** Tidligere i **Alternativ debitormomsregistrering** for dette land eller område, vises følgende meddelelse: **Klik på Tilføj, hvis du vil indsætte den alternative momsregistrering for denne leveringslandekode.** 
8. Der vises en meddelelse som en advarsel om, at du skal tilføje et nyt momsnummer. For at gøre dette skal du vælge handlingen **Tilføj** på meddelelsen, hvorefter **siden Alternativ debitormomsregistrering** åbnes. 
9. På denne side udfyldes dit **debitornummer.** Og lande-/områdekoden **for** moms. Så du skal bare tilføje opsætning, som du vil bruge. 

## <a name="work-with-the-sales-documents"></a>Arbejde med salgsdokumenterne

Du kan oprette en ny [salgsfaktura](sales-how-invoice-sales.md) eller [salgsordre](sales-how-sell-products.md) i [!INCLUDE[prod_short](includes/prod_short.md)]. Hvis du har brug for at bruge en leveringsadresse, der er forskellig fra kundens adresse, og som befinder sig i et andet land, skal du følge trinnene:  

### <a name="alternate-shipping-address"></a>Alternativ leveringsadresse

1. Udvid oversigtspanelet **Levering og fakturering** .   
2. I feltet Levering skal du vælge indstillingen **Alternativ leveringsadresse** . 
3. Siden **Leveringsadresseliste** med tilgængelige alternative adresser vises. 
4. Vælg en af adresserne med en anden **lande-/områdekode**. 
5. Siden **Bekræft alternativ debitormomsregistrering** vises med en liste over felter, som du har ændret på grund af opsætningen af **Alternativ debitormomsregistrering** . 
6. Vælg **OK** for at bekræfte.   

> [!NOTE]
> Hvis du ikke længere vil bekræfte et sådant valg, kan du vælge **feltet Vis ikke igen**, og fremover vil du ikke se denne type meddelelse om ændringer. Men hvis du vil aktivere det igen, kan du gøre det ved at aktivere feltet **Bekræft alternativ momsregistrering** i **momsopsætningen**.  
   
7. Når du har bekræftet, overskrives værdierne med værdierne fra opsætningen af **alternativ debitormomsregistrering** . Du kan se alle momsrelaterede felter i **oversigtspanelet Fakturadetaljer** .  
8. Bogfør dokumentet.  

### <a name="custom-address"></a>Brugerdefineret adresse

Hvis du ikke har konfigureret leveringsadressen, men stadig vil bruge en anden adresse til forsendelse, kan du bruge denne mulighed.  

1. Udvid oversigtspanelet **Levering og fakturering** .   
2. I feltet Levering skal du vælge indstillingen **Brugerdefineret adresse** .  
3. Skift land i feltet **Land/område** .  
4. Når du ændrer lande-/områdekoden, så den **svarer til lande-/områdekoden** for moms i den **alternative debitors momsregistrering**, vises siden Bekræft alternativ debitormomsregistrering **med en liste over felter,** der er blevet ændret. 
5. [!INCLUDE[prod_short](includes/prod_short.md)] vil også ændre alle de momsrelaterede felter, der findes i **oversigtspanelet Fakturadetaljer** .  

### <a name="work-with-no-shipment"></a>Arbejde uden forsendelse

Hvis der ikke er nogen forsendelse som en proces, kan du stadig drage fordel af opsætningen af **alternativ debitormomsregistrering** .

I salgsordren eller fakturaen kan du finde lande-/områdekoden for **moms i** oversigtspanelet Fakturadetaljer **og angive den værdi, der svarer til opsætningen af momsregistrering** for **alternativ** debitor. Og du skal se den samme bekræftelsesdialogside som ovenfor. 

I denne situation kan du bogføre salgsfakturaen med det korrekte **SE/CVR-nr.** for din kunde, selvom du ikke sender varer med dette dokument. 

### <a name="work-with-the-sales-credit-memo"></a>Arbejde med salgskreditnotaen

Når du bogfører fakturaen med en lande-/områdekode for **levering eller** moms, der har forskellige bogføringsdata, henter rettelsen **salgskreditnotaen**  **værdierne fra hovedet Bogført** salgsfaktura **, hvor disse værdier hentes fra** den alternative debitors momsregistrering **, så der kræves ingen andre** handlinger. 

## <a name="see-also"></a>Se også

[Oversigt over momsadministration](finance-manage-vat.md)    
[Oprette moms](finance-setup-vat.md)    
[Arbejde moms af salg og køb](finance-work-with-vat.md)    
[Rapportere moms til en skattemyndighed](finance-how-report-vat.md)    
[Lokal funktionalitet i Business Central](about-localization.md)    


[!INCLUDE[footer-include](includes/footer-banner.md)]
