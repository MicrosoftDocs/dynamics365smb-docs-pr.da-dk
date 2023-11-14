---
title: Få Business Central-tilføjelsesprogram til Outlook
description: 'Få mere at vide om, hvordan du installerer Business Central-tilføjelsesprogrammet til Outlook til virksomheden eller eget brug.'
author: jswymer
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 'SMTP, mail, Microsoft 365, Outlook'
ms.search.form: '1831, 1832'
ms.date: 04/27/2022
ms.author: jswymer
---
# Få Business Central-tilføjelsesprogram til Outlook

Med [!INCLUDE[prod_short](includes/prod_short.md)] kan du administrere forretningsinteraktioner med dine kunder og leverandører direkte i Microsoft Outlook. Med [!INCLUDE[prod_short](includes/prod_short.md)] Outlook-tilføjelsesprogrammet kan du se økonomiske oplysninger om debitorer og kreditorer. Du kan også oprette og sende regnskabsdokumenter, f. eks. tilbud og fakturaer.  

Der er to måder at få installeret et Business Central-tilføjelsesprogram til Outlook på, afhængigt af din rolle i organisationen:

- Som Microsoft 365-administrator kan du bruge *Centraliseret installation* til at installere tilføjelsesprogrammet automatisk for hele organisationen, grupper eller specifikke brugere.

- Som enhver bruger kan du installere tilføjelsesprogrammet til eget brug, hvis din administrator ikke allerede har implementeret det for dig.

## Om Business Central-tilføjelsesprogram til Outlook

Tilføjelsesprogrammet Business Central til Outlook består af to mindre tilføjelsesprogrammer:

- Kontaktoplysninger

    Dette tilføjelsesprogram giver brugerne [!INCLUDE[prod_short](includes/prod_short.md)]-oplysninger om kunde eller leverandør i Outlook-mails og-aftaler. Du kan også oprette og sende [!INCLUDE[prod_short](includes/prod_short.md)]-forretningsdokumenter, f. eks. salgstilbud og fakturaer til en kontakt. <!--To support these task, the add-in adds actions to the Outlook ribbon, in the **Business Central** group. --> 

- Dokumentvisning

    Når en e-mail henviser til et forretningsdokumentnummer i e-mailens brødtekst, indeholder dette tilføjelsesprogrammet et direkte, integreret link fra e-mail-brødteksten til det aktuelle forretningsdokument i [!INCLUDE[prod_short](includes/prod_short.md)].

Du kan finde flere oplysninger om, hvad du gør med tilføjelsesprogrammerne, i [Brug Business Central som indbakke i Outlook](work-outlook-addin.md).

Hvert tilføjelsesprogrammet findes som en XML-fil, der kaldes et *manifest*, som skal installeres i Outlook af alle, som vil have denne funktionalitet. Disse filer beskriver, hvordan du aktiverer tilføjelsesprogrammer og opretter forbindelse til Business central, når de bruges i Outlook. En administrator kan typisk arbejde med disse filer. Som normalt behøver du ikke at håndtere filerne direkte i de fleste tilfælde. Administratoren indstiller enten tilføjelsesprogrammet til at blive installeret automatisk, eller du skal bruge den indbyggede assisterede opsætning til at håndtere installationen.

> [!IMPORTANT]
> Arbejde med forskellige miljøer? Tilføjelsesprogrammet Business Central til Outlook er beregnet til at fungere sammen med et enkelt Business Central-miljø. Når tilføjelsesprogrammet er installeret, er navnet på miljøet medtaget i tilføjelsesprogrammets manifest. Denne konfiguration betyder, at tilføjelsesprogrammet kun vil oprette forbindelse til det miljø, hvor det blev installeret. Hvis du vil bruge tilføjelsesprogrammet sammen med et andet miljø, skal du åbne miljøet og installere tilføjelsesprogrammet igen.

## Installere tilføjelsesprogrammet ved hjælp af centraliseret installation som administrator

Centraliseret installation er en funktion i Microsoft 365 Administration, som du bruger til automatisk at installere tilføjelsesprogrammer i brugernes Office-apps, f.eks. Outlook. Det er den anbefalede måde, hvorpå administratorer kan installere til Office-tilføjelsesprogrammer til brugere og grupper i organisationen.

> [!NOTE]
> Du kan finde flere oplysninger om Business Central-lokalt i [Konfigurere tilføjelsesprogrammet til Outlook-integration med Business Central-lokalt](/dynamics365/business-central/dev-itpro/administration/setting-up-office-add-ins-outlook-inbox) i administrationsindholdet (kun på engelsk).

### Forudsætninger

- Et Microsoft 365-abonnement  
- Brugere får tildelt en Microsoft 365-licens  
- Din Microsoft 365-konto har rollen som *Global administrator* eller *Exchange-administrator*

### Anvende tilføjelsesprogrammet

1. I Business Central kan du vælge den ![Lightbulb, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, angiv **Assisteret opsætning** og vælg derefter det relaterede link.
2. Vælg **Centraliseret installation af Outlook-tilføjelsesprogrammet** for at starte vejledningen til installation af support.
3. Gennemse den første side, og vælg **Næste** for at åbne siden til hentning af tilføjelsesprogrammerne.
4. Marker afkrydsningsfeltet for de tilføjelsesprogrammer, du vil installere, i kolonnen **Installer**, og vælg derefter **Hent og Fortsæt**.

    En fil med navnet *OutlookAddins.zip* overføres til enheden.

5. På dette tidspunkt er du færdig med det arbejde, du skal udføre i Business central, så du kan vælge **udført**.

   >[!TIP]
   > Før du vælger **næste**, skal du vælge **Gå til Microsoft 365 (åbnes i et nyt vindue)** for at åbne og logge på Microsoft 365 Administrationscenter i et nyt browservindue. Du skal alligevel gå til Microsoft 365 Administration Center senere.

6. Gå til den mappe, hvor filen OutlookAddins. zip blev hentet, og Pak filerne **Contact Insights.xml** og **Document View. XML** fra. zip-filen ud til en mappe, du vælger.

    Du kan få flere oplysninger i [Pakke og pakke filer og mapper ud](https://support.microsoft.com/en-us/windows/zip-and-unzip-files-8d28fa72-f2f9-712f-67df-f80cf89fd4e5).
7. Log på Microsoft 365 Administration, og gå til [Integrerede apps](https://go.microsoft.com/fwlink/?linkid=2163967).

8. Vælg **Overfør brugerdefinerede apps**.
9. På siden **Overfør apps til installation** vælge **Overfør manifest-fil (.xml) fra enhed** > **Vælg fil**.
10. Vælg en af de tilføjelsesfiler, du har trukket tidligere, f. eks **Contact Insights.xml**.
11. Følg instruktionerne for at tildele brugere og installere tilføjelsesprogrammet.
12. Gentag trin 9 til 11 for den anden tilføjelsesprogramfil, hvis du vil.

> [!IMPORTANT]
> Der vises en grøn markering, når tilføjelsesprogrammet er installeret i Administrationscenter. Det kan tage op til 24 timer, før brugerne af tilføjelsesprogrammet installeres automatisk i Outlook af brugere. Det kan også være nødvendigt at genstarte Outlook.

Når du er færdig, kan du altid ændre installationen i Microsoft 365 Administration, f.eks. ved at tildele flere brugere. Du kan finde flere oplysninger om installation af tilføjelsesprogrammer i Administration under [Installer tilføjelsesprogrammer i Administration](/microsoft-365/admin/manage/centralized-deployment-faq?view=o365-worldwide#how-do-you-target-add-in-user-assignments-with-centralized-deployment-&preserve-view=true).

## <a name="install"></a>Installere tilføjelsesprogrammet til eget brug

Hvis organisationen tillader det, kan du selv installere det Business Central-tilføjelsesprogram til virksomheden. Kontakt din administrator, hvis du ikke er sikker.

1. I Business Central skal du gå til ![Lightbulb, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikonet, skal du skrive **Hent Outlook-tilføjelsesprogrammet** og derefter vælge det relaterede link.
2. Læs siden, og vælg **Næste**, når du er klar.
3. Hvis du vil modtage en velkomstmeddelelse fra Business central med oversigt over brugen af tilføjelsesprogrammet, skal du aktivere **Send eksempel på e-mail**.
4. Vælg **Afslut** for at fuldføre installationen.

Business Central opretter forbindelse til e-mail-serveren og installerer tilføjelsesprogrammet i din Outlook. Det tager ikke lang tid. Du er nu klar til at begynde at bruge tilføjelsesprogrammet i Outlook.

### <a name="onprem"></a>Til Business Central i det lokale miljø

Hvis du bruger Business Central lokalt, kan det være en smule anderledes at installere tilføjelsesprogrammet.

1. I Business Central skal du gå til ![Lightbulb, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikonet, skal du skrive **Hent Outlook-tilføjelsesprogrammet** og derefter vælge det relaterede link.
2. Læs siden, og vælg **Næste**, når du er klar.
3. Benyt en af følgende fremgangsmåder, afhængigt af den side der vises:

    - Hvis du får vist knappen **Installer på min Outlook**, skal du vælge den, og du er færdig.
    - Hvis knappen **Næste** vises, skal du vælge den. På næste side skal du, hvis du vil modtage en velkomstmeddelelse fra Business central med oversigt over brugen af tilføjelsesprogrammet, aktivere **Send eksempel på e-mail**. Derefter skal du vælge **Udfør**, og du er færdig.
    - Hvis du får vist knappen **Hent tilføjelsesprogram**, skal du vælge det og derefter gå til næste trin.
4. Når du vælger **download-tilføjelsesprogram**, overføres en fil med navnet *OutlookAddins. zip* til din enhed. Filen vises øverst i browseren.

   Gå til den mappe, hvor filen OutlookAddins.zip blev hentet, og Pak filen **Contact Insights.xml** og **Document View.XML** fra zip-filen ud til en mappe, du vælger. Du kan finde flere oplysninger om, hvordan du pakker filer ud, i [pakke og pakke filer og mapper ud](https://support.microsoft.com/en-us/windows/zip-and-unzip-files-8d28fa72-f2f9-712f-67df-f80cf89fd4e5).

5. Åbn Outlook, og vælg **Hent tilføjelsesprogrammer** på båndet. Hvis du bruger Outlook på internettet, skal du vælge rullemenuen i en ny eller eksisterende e-mailmeddelelse og derefter vælge **Hent tilføjelsesprogrammer**.
6. Vælg **Mine tilføjelsesprogrammer** > **Tilføj et brugerdefineret tilføjelsesprogram** > **Tilføj fra en fil**.
7. Vælg en af de .xml-filer, som du har pakket ud, f.eks. **Contact Insights.xml**, og vælg derefter **Åbn** > **installation**.
8. Gentag trin 6 og 7 for den anden .xml-fil, hvis du har hentet den.

Du er nu klar til at begynde at bruge tilføjelsesprogrammet i Outlook.

## Se også

[Blive køreklar](ui-get-ready-business.md)  
[Få Business Central på min mobilenhed](install-mobile-app.md)  
[Sende dokumenter som mail](ui-how-send-documents-email.md)  
[Finans](finance.md)  
[Salg](sales-manage-sales.md)  
[Køb](purchasing-manage-purchasing.md)  
[Minimumkrav til Outlook](product-requirements.md#outlook)  
[Brug tilføjelsesprogrammer i Outlook på internettet](https://support.office.com/article/Using-Add-ins-in-Outlook-on-the-web-8f2ce816-5df4-44a5-958c-f7f9d6dabdce?appver=OWB150)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
