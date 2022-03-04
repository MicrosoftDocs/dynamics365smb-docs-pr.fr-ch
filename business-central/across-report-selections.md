---
title: Sélection des états dans Business Central
description: Découvrez comment configurer les états que vous utilisez pour imprimer différents types de documents dans Business Central.
author: edupont04
ms.topic: conceptual
ms.search.keywords: setup, reporting
ms.search.form: 306, 307, 347, 385, 524, 865, 5932, 7401, 7355, 99000917
ms.date: 04/01/2021
ms.author: edupont
ms.openlocfilehash: 16ad3480c10da544c7fdd3a6a299dc6d86cfce46
ms.sourcegitcommit: ef80c461713fff1a75998766e7a4ed3a7c6121d0
ms.translationtype: HT
ms.contentlocale: fr-CH
ms.lasthandoff: 02/15/2022
ms.locfileid: "8134085"
---
# <a name="report-selection-in-business-central"></a>Sélection des états dans Business Central

Vous pouvez configurer les états par défaut qui seront utilisés pour imprimer les divers documents vente et achat : commandes, devis, factures et avoirs. Par exemple, si vous avez une mise en page spécifique pour les factures vente, vous pouvez spécifier cet état sur la page **Sélection des états - Vente** afin qu’elle soit utilisée pour envoyer ou imprimer les factures vente.  

Les pages **Sélection des états** spécifient quel état sera imprimé dans différentes situations. [!INCLUDE [prod_short](includes/prod_short.md)] inclut les configurations par défaut, mais vous pouvez modifier ces valeurs par défaut. Vous pouvez également ajouter des états aux pages **Sélection des états** si vous souhaitez imprimer plus qu’un état par type de document, par exemple.  

## <a name="available-report-selections"></a>Sélection des états disponible

[!INCLUDE [prod_short](includes/prod_short.md)] comprend différentes pages **Sélection des états** pour différents domaines. Les tableaux suivants décrivent où vous pouvez trouver des informations sur les différentes pages.  

|Zone ou tâche  |En savoir plus|
|--------------|----------|
|Exemple de fonctionnement de la sélection des états (Sales)|[Sélection des états pour les documents de vente](#example-report-selection-for-sales-documents)|
|Mise en page par défaut des e-mails avec des documents vente et achat  |[Configurer des textes et des mises en page d’e-mail réutilisables pour les documents vente et achat](admin-how-setup-email.md#set-up-reusable-email-texts-and-layouts-for-sales-and-purchase-documents) |
|Définir les mises en page de chèques     |[Sélectionner une mise en page de chèque](finance-how-define-check-layouts.md) |
|Définir des états pour la déclaration de TVA (Allemagne)|[Paramétrer les déclarations de TVA et les états d’échanges intracomm.](LocalFunctionality/Germany/how-to-set-up-reports-for-vat-and-intrastat.md) |

> [!TIP]
> Votre [!INCLUDE [prod_short](includes/prod_short.md)] peut inclure des pages **Sélection des états** en fonction de votre emplacement et de votre secteur d’activité, par exemple. Vous pouvez toujours vérifier votre configuration en choisissant l’icône ![Ampoule qui ouvre la fonction Tell Me.](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire") en saisissant **Sélection des états**, puis choisissez le lien approprié.

La version par défaut de [!INCLUDE [prod_short](includes/prod_short.md)] comprend les pages suivantes **Section des états** :

* **Sélection des états - Ventes**  
* **Sélection des états - Achats**  
* **Sélection des états - Stocks**  
* **Sélection des états - Trésorerie**  
* **Sélection des états - Entrepôt**  
* **Sélection des états - Compte bancaire**  
* **Sélection des états - Rappel/Frais financiers**  

## <a name="example-report-selection-for-sales-documents"></a>Exemple : Sélection des états pour les documents de vente

La page **Sélection des états - Ventes** définit les états par défaut à utiliser dans différents scénarios pour chaque type de document associé. Choisissez un type de document dans le champ **Usage**, puis ajoutez ou examinez la sélection des états. Vous pouvez configurer plusieurs états et l’ordre de séquence dans lequel les états doivent être envoyés ou imprimés.  

[!INCLUDE [tooltip-inline-tip_md](includes/tooltip-inline-tip_md.md)]

Certains types de documents peuvent être envoyés sous forme de pièces jointes à un e-mail, et d’autres non. Chaque page **Sélection des états** affiche des champs supplémentaires si le type de courrier électronique de support est prêt à l’emploi.  

Par exemple, dans les pages **Sélection des états - Ventes** et **Sélection des états -Achat**, les champs suivants vous aident à configurer l’envoi d’e-mails :

|Nom du champ |Description  |
|-----------|-------------|
|**Utiliser pour le corps du message**| Spécifie que les informations résumées, telles que le numéro de facture, la date d’échéance et le lien de service de paiement, vont être insérées dans le corps de l’e-mail que vous envoyez.        |
|**Utiliser comme pièce jointe**| Spécifie que le document associé sera joint à l’e-mail.|
|**Description de la présentation du corps du message e-mail**|Spécifie la mise en page du corps de l’e-mail utilisée, généralement une mise en page d’état personnalisée. |

## <a name="see-also"></a>Voir aussi

[Configurer des textes et des mises en page d’e-mail réutilisables pour les documents vente et achat](admin-how-setup-email.md#set-up-reusable-email-texts-and-layouts-for-sales-and-purchase-documents)  
[Sélectionner une mise en page de chèque](finance-how-define-check-layouts.md)  
[Paramétrer les déclarations de TVA et les états d’échanges intracomm. (Allemagne)](LocalFunctionality/Germany/how-to-set-up-reports-for-vat-and-intrastat.md)  
[Gestion des présentations d’état et de document](ui-manage-report-layouts.md)  
[Définir des présentations de document pour les clients et les fournisseurs](ui-define-customer-vendor-document-layouts.md)  
[Paramétrage imprimantes](ui-specify-printer-selection-reports.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]