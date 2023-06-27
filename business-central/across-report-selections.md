---
title: "Sélection des états dans Business\_Central"
description: "Découvrez comment configurer les états que vous utilisez pour imprimer différents types de documents dans Business\_Central."
author: brentholtorf
ms.topic: conceptual
ms.search.keywords: 'setup, reporting'
ms.search.form: '306, 307, 347, 385, 524, 865, 5932, 7401, 7355, 99000917'
ms.date: 06/09/2022
ms.author: bholtorf
---
# <a name="report-selection-for-documents-in-business-central"></a>Sélection d’état pour les documents dans Business Central

Vous pouvez configurer des états par défaut à utiliser pour imprimer des documents de vente, d’achat et de services, tels que des commandes, des devis et des factures. Par exemple, si vous avez une mise en page spécifique pour les factures vente, vous pouvez spécifier cet état sur la page **Sélection des états - Vente** afin qu’elle soit utilisée pour envoyer ou imprimer les factures vente.  

## <a name="available-report-selections"></a>Sélection des états disponible

Les pages **Sélection des états** spécifient quel état sera imprimé dans différentes situations. [!INCLUDE [prod_short](includes/prod_short.md)] fournit des configurations par défaut, mais vous pouvez les modifier si nécessaire. Vous pouvez également ajouter des états aux pages **Sélection des états** si vous souhaitez imprimer plus qu’un état par type de document, par exemple. 

Le tableau suivant décrit où vous pouvez trouver des informations sur les différentes pages.  

|Zone ou tâche  |En savoir plus|
|--------------|----------|
|Exemple de fonctionnement de la sélection des états (ventes)|[Sélection des états pour les documents de vente](#example-report-selection-for-sales-documents) ci-dessous|
|Mise en page par défaut des e-mails avec des documents vente et achat  |[Configurer des textes et des mises en page d’e-mail réutilisables pour les documents vente et achat](admin-how-setup-email.md#set-up-reusable-email-texts-and-layouts) |
|Définir les mises en page de chèques     |[Sélectionner une mise en page de chèque](finance-how-define-check-layouts.md) |
|Définir des états pour la déclaration de taxe sur la valeur ajoutée (TVA) (Allemagne)|[Paramétrer les déclarations de TVA et les états d’échanges intracomm.](LocalFunctionality/Germany/how-to-set-up-reports-for-vat-and-intrastat.md) |

> [!TIP]
> Votre [!INCLUDE [prod_short](includes/prod_short.md)] peut inclure des pages **Sélection des états** en fonction de votre emplacement et de votre secteur d’activité, par exemple. Pour vérifier votre configuration, sélectionnez l’![icône en forme d’Ampoule qui ouvre la fenêtre de recherche.](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire") entrez **Sélection des états**, puis choisissez le lien approprié.

La version par défaut de [!INCLUDE [prod_short](includes/prod_short.md)] comprend les pages suivantes **Sélection des états** :

* **Sélection des états - Ventes**  
* **Sélection des états - Achats**  
* **Sélection des états - Stocks**  
* **Sélection des états - Trésorerie**  
* **Sélection des états - Entrepôt**  
* **Sélection des états - Compte bancaire**  
* **Sélection des états - Projet**  
* **Sélection des états : Services**

## <a name="example-report-selection-for-sales-documents"></a>Exemple : Sélection des états pour les documents de vente

La page **Sélection des états - Ventes** présente les états par défaut à utiliser dans différents scénarios pour chaque type de document associé. Choisissez un type de document dans le champ **Usage**, puis ajoutez ou examinez la sélection des états. Vous pouvez configurer plusieurs états et l’ordre de séquence dans lequel les états doivent être envoyés ou imprimés.  

[!INCLUDE [tooltip-inline-tip_md](includes/tooltip-inline-tip_md.md)]

Vous ne pouvez pas envoyer tous les types de documents sous forme de pièces jointes à des e-mails. Pour ceux pour lesquels c’est possible, la page **Sélection des états** contient des champs supplémentaires.  

Par exemple, dans les pages **Sélection des états - Ventes** et **Sélection des états -Achat**, les champs suivants vous aident à configurer l’envoi d’e-mails :

|Nom du champ |Désignation  |
|-----------|-------------|
|**Utiliser pour le corps du message**| Insérez des informations résumées, telles que le numéro de facture, la date d’échéance, ou un lien vers un service de paiement, dans un e-mail.        |
|**Utiliser comme pièce jointe**| Joignez le document correspondant à l’e-mail.|
|**Description de la présentation du corps du message e-mail**|Spécifiez la mise en page à utiliser pour le corps du message. En règle générale, la mise en page de l’état est personnalisée. |

## <a name="see-also"></a>Voir aussi

[Configurer des textes et des mises en page d’e-mail réutilisables](admin-how-setup-email.md#set-up-reusable-email-texts-and-layouts)  
[Sélectionner une mise en page de chèque](finance-how-define-check-layouts.md)  
[Paramétrer les déclarations de TVA et les états d’échanges intracomm. (Allemagne)](LocalFunctionality/Germany/how-to-set-up-reports-for-vat-and-intrastat.md)  
[Gestion des présentations d’état et de document](ui-manage-report-layouts.md)  
[Définir des présentations de document pour les clients et les fournisseurs](ui-define-customer-vendor-document-layouts.md)  
[Paramétrage imprimantes](ui-specify-printer-selection-reports.md)  
[États financiers et analyses dans Business Central](finance-reports.md)  
[États comptabilité client et analyses d’immobilisation dans Business Central](receivables-reports.md)  
[États comptabilité fournisseur et analyses d’immobilisation dans Business Central](payables-reports.md)  
[États sur les immobilisations et analyses dans Business Central](fa-reports.md)  
[États de projet et analyses dans Business Central](project-reports.md)  
[États ventes et analyses dans Business Central](sales-reports.md)  
[États achats et analyses dans Business Central](purchase-reports.md)  
[États de stock et d’entrepôt et analyses dans Business Central](inventory-WMS-reports.md)  
[États d’assemblage et analyses dans Business Central](assembly-reports.md)  
[États de production et analyses dans Business Central](production-reports.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
