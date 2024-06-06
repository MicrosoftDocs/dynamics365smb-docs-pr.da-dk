---
title: Administrere adgang til Business Central
description: Administratorer bruger en lagdelt tilgang til at styre adgangen til Business central og dens muligheder.
author: brentholtorf
ms.author: bholtorf
ms.reviewer: jswymer
ms.topic: overview
ms.date: 04/04/2023
ms.custom: bap-template
ms.service: dynamics-365-business-central
---

# <a name="manage-access-to-business-central"></a>Administrere adgang til Business Central

[!INCLUDE[azure-ad-to-microsoft-entra-id](~/../shared-content/shared/azure-ad-to-microsoft-entra-id.md)]

Denne artikel giver administratorer og programudviklere en højt oversigt over, hvordan man styrer adgangen til [!INCLUDE [prod_short](includes/prod_short.md)] og dets funktioner. Brug linkene til at gå til andre artikler, hvor du kan finde flere oplysninger om emnerne.

## <a name="layered-access"></a>Lagdelt adgang

[!INCLUDE [prod_short](includes/prod_short.md)] bruger en lagdelt tilgang til programsikkerhed som beskrevet i følgende diagram. Hvis du vil vide mere om hvert lag, skal du gå til [Application Security i Business Central](/dynamics365/business-central/dev-itpro/security/security-application).

:::image type="content" source="media/security-overview.png" alt-text="Lagdelt programsikkerhed i Business Central.":::

## <a name="licenses"></a>Licenser

Tildel [!INCLUDE [prod_short](includes/prod_short.md)]-brugere til en **Dynamics 365 Business Central**-licens, som giver dem mulighed for at få vist, ændre og behandle forretningsdata fra enhver brugergrænseflade. Hvis du vil vide mere om licenser, skal du gå til [Licensering i Dynamics 365 Business Central](/dynamics365/business-central/dev-itpro/deployment/licensing).

Men brugere, der lejlighedsvis har brug for skrivebeskyttet adgang til oplysninger i [!INCLUDE [prod_short](includes/prod_short.md)], kan bruge en **Microsoft 365**-licens. Hvis du vil vide mere om begrænset adgang, skal du gå til [Business Central-adgang med Microsoft 365-licenser](admin-access-with-m365-license.md).

Du kan finde flere oplysninger om de forskellige typer licenser, og hvordan licenser fungerer i [!INCLUDE[prod_short](includes/prod_short.md)] ved at hente [Licensvejledning til Dynamics 365](https://go.microsoft.com/fwlink/?LinkId=866544).

## <a name="business-central-administrator-tasks"></a>Administrative opgaver i Business Central

I følgende tabel vises, hvordan administratorer kan kontrollere adgangen til [!INCLUDE [prod_short](includes/prod_short.md)], og hvilke funktioner personer bruger. Nogle af opgaverne hjælper også at holde Access-indstillingerne opdaterede.

|Opgave| Lær mere |
|--|--|--|
|Hver person skal have en brugerkonto, før de kan logge på [!INCLUDE [prod_short](includes/prod_short.md)]. Den nemmeste måde at konfigurere brugere på er at tilføje dem én ad gangen i [Microsoft 365 Administration](https://go.microsoft.com/fwlink/p/?linkid=2024339). |[Tilføje brugere og tildele licenser på én gang](/microsoft-365/admin/add-users/add-users)|
|Administrere adgangen for alle brugere på miljøniveau. Opret en Microsoft Entra-sikkerhedsgruppe, og tildel den til miljøet.<br><br> Du kan også bruge sikkerhedsgrupper til at administrere adgangen for bestemte brugergrupper. | [Administrere adgang til miljøer](/dynamics365/business-central/dev-itpro/administration/tenant-admin-center-manage-access)<br><br>[Kontrollere adgangen til Business central ved brug af sikkerhedsgrupper](ui-security-groups.md) |
|Oprette brugere i [!INCLUDE [prod_short](includes/prod_short.md)] og definere, hvem der kan logge på. | [Oprette brugere i henhold til licenser](ui-how-users-permissions.md) |
|I kombination med brugerlicenser definerer tilladelser de objekter, som en bruger kan få adgang til inden for hver database eller miljø. Angiv, om man kan læse, ændre eller indtaste data i de databaseobjekter. |[Tildele tilladelser til brugere og grupper](ui-define-granular-permissions.md)|
|Hvis en ekstern bogholder administrerer regnskaberne og Financial Reporting, skal du invitere dem til din [!INCLUDE [prod_short](includes/prod_short.md)]. De vil kunne arbejde mere tæt med dig på dine regnskabsdata.|[Revisoroplevelser i [!INCLUDE[prod_long](includes/prod_long.md)]](finance-accounting.md)|
|Hvis du er en [!INCLUDE [prod_short](includes/prod_short.md)]-videresalgspartner, kan du sende en e-mail til en kunde for at anmode om en forhandlers relation. Du kan medtage delegerede administrationsrettigheder til Microsoft Entra ID og Microsoft 365 i mailen.| [Delegeret administratoradgang til Business Central Online](/dynamics365/business-central/dev-itpro/administration/delegated-admin)|
|En Azure-servicekode repræsenterer en gruppe IP-adresser, som trafik til en tjeneste kan komme fra eller gå til. Brug servicekoder til at oprette firewalls for at tillade trafik fra bestemte tjenester. Med **Dynamics365BusinessCentral**-koden kan du bruge firewall og regler i netværkssikkerhedsgruppen til at begrænse trafikken til og fra [!INCLUDE [prod_short](includes/prod_short.md)].| [Azure-sikkerhedstjenestemærker](/dynamics365/business-central/dev-itpro/security/security-service-tags)|
|Når du bruger Microsoft Entra-godkendelse til [!INCLUDE [prod_short](includes/prod_short.md)], anbefales det, at du drager fordel af [Microsoft Entra ID Multi-Factor Authentication (MFA)](/azure/active-directory/authentication/concept-mfa-howitworks). MFA sikrer yderligere adgang til programmet og dataene.|[Multifaktorgodkendelse for Dynamics 365 Business Central](/dynamics365/business-central/dev-itpro/security/multifactor-authentication)|

## <a name="business-central-developer-tasks"></a>Business Central-udvikleropgaver

Der er også en udviklertekst til at styre adgangen til [!INCLUDE [prod_short](includes/prod_short.md)]. Udviklere og administratorer kan f.eks. bygge og forbinde programmer til [!INCLUDE [prod_short](includes/prod_short.md)], der drager fordel af virksomheden:  

* Strømline forretningsprocesser
* Forbedre kundeinteraktioner
* Træffe bedre beslutninger, hurtigere

Følgende tabel indeholder oplysninger om, hvordan du giver apps og udvidelser adgang til [!INCLUDE [prod_short](includes/prod_short.md)]-data.

| Opgave | Lær mere |
|--|--|
|De to vigtigste begreber for at definere adgang til funktioner er rettigheder og tilladelser. Rettigheder giver almen adgang til objekter i henhold til licenser og Microsoft Entra-roller. Tilladelser og tilladelsessæt giver dig mulighed for at finjustere adgangen til objekter. |[Oversigt over rettigheds- og tilladelsessæt](/dynamics365/business-central/dev-itpro/developer/devenv-entitlements-and-permissionsets-overview)|

## <a name="see-also"></a>Se også

[Sikkerhed i Business Central](/dynamics365/business-central/dev-itpro/security/security-and-protection)
