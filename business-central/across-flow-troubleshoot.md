---
title: Problemen met uw geautomatiseerde werkstromen oplossen
description: Meer informatie over het oplossen van problemen tussen Business Central en Power Automate wanneer u een geautomatiseerde workflow maakt.
author: jswymer
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 'workflow, OData, Power App, SOAP, Entity set not found, workflowWebhookSubscriptions, Power Automate,'
ms.date: 08/04/2022
ms.author: edupont
---

# Problemen met uw geautomatiseerde [!INCLUDE[prod_short](includes/prod_short.md)]-werkstromen oplossen

Wanneer u [!INCLUDE [prod_short](includes/prod_short.md)] verbindt met Power Automate om geautomatiseerde werkstromen te maken, kunt u foutmeldingen tegenkomen. Dit artikel biedt voorgestelde oplossingen voor vaak terugkerende problemen.

## Stroom wordt niet uitgevoerd op alle records die zijn gemaakt of gewijzigd

### Probleem

Als een gebeurtenis veel records maakt of wijzigt, wordt de stroom niet uitgevoerd voor sommige of alle records.

### Mogelijke oorzaak

Momenteel is er een limiet voor het aantal records dat een stroom kan verwerken. Als er binnen 30 seconden meer dan 100 records worden gemaakt of gewijzigd, wordt de stroom niet geactiveerd.

> [!NOTE]
> Voor ontwikkelaars wordt de stroomtriggering gedaan via webhook-berichten en deze beperking is te wijten aan de manier waarop de Business Central-connector omgaat met `collection`-berichten. Zie voor meer informatie [Werken met webhooks in Dynamics 365 Business Central](/dynamics365/business-central/dev-itpro/api-reference/v2.0/dynamics-subscriptions#notes-for-power-automate-flows) in de Help voor ontwikkelaars en beheerders.

## Fout "Entiteitset niet gevonden"

### Probleem

Bij het aanmaken van een nieuwe Power Automate-stroom met een [!INCLUDE[prod_short](includes/prod_short.md)]-goedkeuringstrigger, zoals *Wanneer goedkeuring van een inkoopdocument wordt aangevraagd*, kunt u een foutmelding krijgen die lijkt op:

`Entity set not found: \<name\>`

De plaatshouder `\<name\>` is de servicenaam van de ontbrekende webservice, zoals *workflowWebhookSubscriptions* of *workflowPurchaseDocumentLines*.

### Mogelijke oorzaak

Gebruik van Power Automate voor uw goedkeuringen vereist dat bepaalde pagina- en codeunit-objecten worden gepubliceerd als webservices. Standaard worden de meeste vereiste objecten gepubliceerd als webservices. Maar in sommige gevallen is uw omgeving mogelijk aangepast zodat deze objecten niet langer worden gepubliceerd.

### Corrigeren

Ga naar de pagina **Webservices** en zorg ervoor dat de volgende objecten worden gepubliceerd als webservices. Er moet een item in de lijst zijn voor elk object, met het selectievakje **Gepubliceerd** geselecteerd.  

| Objecttype | Object-id | Objectnaam | Servicenaam |
|--|--|--|--|
| Codeunit | 1544 | WorkflowWebhookSubscription | WorkflowActionResponse |
| Pagina | 6408 | workflowCustomers | workflowCustomers |
| Pagina | 6406 | workflowGenJournalBatches | workflowGenJournalBatches |
| Pagina | 6407 | workflowGenJournalLines | workflowGenJournalLines |
| Pagina | 6409 | workflowItems | workflowItems |
| Pagina | 6405 | Entiteit inkoopdocumentregel | workflowPurchaseDocumentLines |
| Pagina | 6404 | workflowPurchaseDocuments | workflowPurchaseDocuments |
| Pagina | 6403 | Entiteit verkoopdocumentregel | workflowSalesDocumentLines |
| Pagina | 6402 | workflowSalesDocuments | workflowSalesDocuments |
| Pagina | 6410 | workflowVendors | workflowVendors |
| Pagina | 831 | workflowWebhookSubscriptions | workflowWebhookSubscriptions |

> [!NOTE]
> De waarde van **Servicenaam** moet precies zijn zoals weergegeven in de tabel. Wijzig of vertaal de servicenaam niet.

Zie [Een webservice publiceren](across-how-publish-web-service.md) voor meer informatie over het publiceren van webservices.

## Zie gerelateerde training op [Microsoft Learn](/learn/modules/use-power-automate/).

## Zie ook

[Power Automate-stromen gebruiken in [!INCLUDE[prod_short](includes/prod_short.md)]](across-how-use-financials-data-source-flow.md)  
[Werkstroom](across-workflow.md)  
[Geautomatiseerde werkstromen instellen](/dynamics365/business-central/dev-itpro/powerplatform/automate-workflows)  
[Directe stromen inschakelen](/dynamics365/business-central/dev-itpro/powerplatform/instant-flows)  
[Power Automate-stromen beheren](/dynamics365/business-central/dev-itpro/powerplatform/manage-power-automate-flows)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
