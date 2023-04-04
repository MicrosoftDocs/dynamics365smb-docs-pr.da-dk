---
title: Få adgang til Business Central forhåndsversion - CoPilot-version
description: 'Forklarer, hvordan du får et Business Central-miljø med ny AI-muligheden for at generere tekstforslag til vare- og produktbeskrivelser.'
author: jswymer
ms.author: jswymer
ms.reviewer: jswymer
ms.topic: how-to
ms.date: 03/16/2023
ms.custom: bap-template
---

# Kom i gang med en Business central-forhåndsversion - CoPilot-udgave

[!INCLUDE[ai-preview](includes/ai-preview.md)]

Du kan prøve at udføre AI-drevet varemarketingtekst med CoPilot, uanset om du er en eksisterende Business Central-kunde eller en potentiel kunde, dvs. en person, der bare er interesseret i at udforske Business central og afprøve den nye funktion. For at komme i gang skal du have adgang til en forhåndsversionen af Business central, som understøtter den nye funktion. Udfyld den sektion nedenfor, der gælder for dig.

## Organisationen bruger allerede Business Central

Som eksisterende kunde eller partner har du brug for en administrator med adgang til Business Central Administration for at oprette et *Sandkasse*-miljø, der kører forhåndsversionen, der omfatter CoPilot. Når sandkassemiljøet er konfigureret og kører, kan brugerne afprøve den nye funktion.

Hvis du er miljøadministrator, skal du udføre følgende trin:

1. Log på Business Central Administration.
2. Vælg **Miljøer** > **Ny**.
3. I ruden **Opret miljø** skal du angive et navn til et nyt miljø i feltet **Miljønavn**.
4. Indstil **Miljøtype** til **Sandkasse**.
5. Angiv **Land** til **USA**.

   > [!IMPORTANT]
   > Forhåndsversionen er kun tilgængeligt for USA. Organisationer i et hvilket som helst land eller område kan stadig oprette et amerikansk sandkasse-forhåndsversion for at kunne opleve CoPilot.

6. I boksen **Version** vælges en version **22.0.54157.54311 (Forhåndsversion - Copilot-version)**.

   > [!IMPORTANT]
   > Du skal bruge **22.0.54157.54311 (forhåndsversion - CoPilot-version)** for at kunne opleve CoPilot.

7. Vælg **Opret**.  

Du kan finde flere oplysninger om, hvordan du opretter sandkassemiljøer, ved at gå til [Opret et miljø](/dynamics365/business-central/dev-itpro/administration/tenant-admin-center-environments#create-a-new-environment).

> [!IMPORTANT]
> Sandkasserne i forhåndsversion er kun tilgængelige indtil 01 maj 2023. Efter denne dato skal du klargøre et nyt miljø eller opgradere alle andre miljøer til version 22.0 eller nyere for at fortsætte med at prøve forhåndsversionen på AI-drevet varemarketingtekst.

## Organisationen bruger ikke Business Central

Hvis du ikke er Business Central-kunde, men gerne vil prøve AI-funktionerne, kan du tilmelde dig og få en gratis forhåndsversion. Enkel tilmelding til prøveversion. Du kommer til at lede efter et par trin, hvor du skal angive nogle oplysninger, f. eks. din e-mailadresse, telefonnummer og navn. Hvis du vil have prøveversionen, skal du fuldføre følgende trin:

1. Gå til [dette prøvewebsted](https://go.microsoft.com/fwlink/?linkid=2227167) for at komme i gang med tilmeldingsprocessen.
2. Følg instruktionerne på skærmen.

   Du bliver bedt om at angive oplysninger som din e-mailadresse, dit navn og dit telefonnummer. Den nøjagtige oplevelse kan variere, afhængigt af hvilke oplysninger du angiver. Men her er et par vigtige punkter, du skal være opmærksom på, når du gennemgår tilmeldingsprocessen:

   - Brug din mail på arbejdet eller i skolen til din e-mailadresse. Vi opretter en prøveversion af din organisationskonto. Du kan ikke bruge e-mail-adresser fra forbruger-e-mail-udbydere eller telekommunikationsudbydere, f. eks. outlook.com, hotmail.com, gmail.com og andre.
   - Når du kommer til indstillingen for **Land eller område**, skal du sørge for at indstille dette **USA**.

      > [!IMPORTANT]
      > Du skal angive **Land/område** til **USA**. I modsat fald vil AI-drevet varemarketingtekst i forbindelse med CoPilot ikke være tilgængelig i Business Central.  
3. Når du kommer til trinnet **Bekræftelsesoplysninger**, er du klar til at starte prøveversionen.

   - Hvis du vil gå direkte til Business Central, skal du vælge **Spring over og gå til Dynamics 365 Business Central** > **Introduktion**.
   - Du har også mulighed for at invitere andre i organisationen til den gratis prøveversion. Indtast blot e-mailadresserne på hver person, og vælg derefter **Send invitationer**. Vælg **Introduktion** for at gå til Business central.  

   Du bliver omdirigeret til din prøveversion på [https://businesscentral.dynamics.com/](https://businesscentral.dynamics.com/). Det kan vare flere minutter at få prøveversionen klar, første gang du logger på.

<!--
1. On the **Let's get you started** step, enter your work or school email address, then select **Next**.

   Use your work or school email address. We'll establish your trial on your organization's account. You can't use email addresses provided by consumer email services or telecommunication providers, such as outlook.com, hotmail.com, gmail.com, and others.
3. When asked what kind of email you have, select **I got it from my organization** > **Next**.
4. On the **Create your account** step, you provide information that will help use set up a trial version of Business Central that you can sign in to.

   1. Provide a telephone number that we can use to send you a verification code. Enter a country code and number that isn't VoIP or toll free.
   2. Choose how you want us to send the verification code:
      - Select **Text me** to get the verification code in a text message.
      - Select **Call me** to get the code in a voice message.
   3. Select **Send verification code**. 
   4. When you get the code, type it in the **Enter your verification code** box, then select **Verify**.

      Once you're verified, we'll send you an email with another verification code that you'll use in the next step to complete creating your account.
   5. Fill in your first and last name.
   6. Set **Country or region** to **United States**.

      > [!IMPORTANT]
      > You must set **Country or region** to **United States**; otherwise the AI-powered item marketing text with Copilot won't be available in Business Central.  

   7. Enter a valid phone umber in the **Business telephone number** box.
   8. In the **Create password** and **Confirm password** boxes, enter a password that you want to use to sign in to Business Central. The password must at least eight characters and include at least one number, an uppercase letter, and a lower case letter.
   9. In the **Verification code** box, enter the verification code we sent you in an email, then select **Next**.
   10. When you get a prompt that your account is successfully created, select **Sign in**.
-->

4. Når du er logget på, kan du se hjemmesiden for Business Central, kaldet rollecenter, som ligner følgende:

   [![Viser Business Central-rollecenter og kontrollisten til CoPilot](media/copilot-checklist.png)](media/copilot-checklist.png#lightbox)

5. Hvis du vil have en introduktion til oprettelse af AI-drevet marketingtekst med CoPilot under **Din kontrolliste** øverst på siden skal du vælge **Opret med Copilot** > **Start præsentation**. Derefter skal du følge vejledningen på skærmen.

   > [!TIP]
   > Hvis du ikke kan se **Din kontrolliste**, skal du vælge knappen **Vis demonstrationspræsentation** først.

## Næste trin

Egenskaberne for AI, som leveres af CoPilot, skal aktiveres, før du eller andre kan bruge CoPilot. Hvis du vil aktivere AI-funktionerne, skal en administrator godkende vilkårene og betingelserne i [forhåndsversion](https://dynamics.microsoft.com/legaldocs/supp-dynamics365-preview/) og [Microsoft erklæring om beskyttelse af personlige oplysninger](https://go.microsoft.com/fwlink/?LinkId=521839) på vegne af organisationen.

> [!NOTE]
> Hvis du bruger en prøveversion, er du administrator. Hvis du har inviteret andre personer i virksomheden til prøveversionen under tilmeldingen, kan de ikke bruge CoPilot, før du har aftalt vilkårene og betingelserne.

Der er to måder at godkende som administrator:

- Den nemmeste måde at bruge CoPilot på. Første gang du bruger CoPilot som administrator, bliver du bedt om at gennemgå vilkår og betingelser og derefter acceptere eller blive uenig. Sådan kan du lære, hvordan du bruger CoPilot, ved at gå til [Tilføje marketingtekst til varer](item-marketing-text.md).  

- Den anden måde er at bruge siden **Status for meddelelser om beskyttelse af personlige oplysninger** i Business central og accepterer **Azure OpenAI**-integration for alle brugere. Hvis du vil vide mere, skal du gå til [Bekræftelse til Vilkår og betingelser](enable-ai.md#consent-to-or-reject-the-preview-and-privacy-terms-and-conditions-for-all-users).

## Se også

[Oversigt over AI-styret varemarketingtekst med Copilot](ai-overview.md)  
[Konfigurere marketingtekst med Copilot til AI-styret vare som administrator](enable-ai.md)  
[Oprette marketingtekst til varer vha. CoPilot](item-marketing-text.md)  
[AI-styret marketingtekst med element (forhåndsversion) med Copilot Ofte stillede spørgsmål](ai-faq.md)  