---
author: brentholtorf
ms.topic: include
ms.date: 09/21/2023
ms.author: bholtorf
ms.service: dynamics-365-business-central
---

Les employés de l’entrepôt peuvent expédier et recevoir des articles hors inventaire ainsi que des marchandises physiques dans les commandes vente et achat. Les articles hors inventaire sont des biens incorporels, tels que l’assurance ou les coûts supplémentaires.

Les commandes vente et achat ont souvent différents types d’éléments sur leurs lignes. Par exemple, les commandes peuvent inclure des articles de la comptabilité, des comptes et des immobilisations. Si vous utilisez des documents entrepôt pour gérer des articles physiques, vous pouvez également valider certains types d’articles hors inventaire. Voici des exemples de documents entrepôt :

* Rangements stock
* Réceptions entrepôt
* Prélèvements stock
* Expéditions entrepôt

Pour permettre aux magasiniers d’expédier et de recevoir des articles hors inventaire, complétez le champ **Valider automatiquement les articles hors inventaire via l’entrepôt** sur les pages **Paramètres ventes** et **Paramètres achats**. Le champ fournit les options suivantes :

|Option  |Désignation  |
|---------|---------|
|Aucune     |N’expédiez ni ne recevez des articles hors inventaire.         |
|Attaché/affecté     | Validez les frais article et autres lignes article hors inventaire qui sont attribués ou joints aux articles physiques. Pour joindre des lignes hors inventaire aux articles physiques, utilisez l’action **Joindre à la ligne inventaire**.        |
|Tout     | Validez toutes les lignes hors inventaire dans le document origine dès qu’au moins un article est validé par le document entrepôt.        |

> [!NOTE]
> L’option **Terminé** dans le champ **Avis d’expédition** de la commande client a la priorité sur la sélection dans le champ **Valider automatiquement les articles hors inventaire via l’entrepôt** de la page **Paramètres ventes**.