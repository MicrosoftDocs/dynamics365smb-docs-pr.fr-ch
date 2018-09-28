---
title: Familiarisation avec la validation des documents achat | Microsoft Docs
description: "En savoir plus sur les différentes fonctions de validation pour valider des documents achat."
services: project-madeira
documentationcenter: 
author: SusanneWindfeldPedersen
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.date: 10/01/2018
ms.author: solsen
ms.translationtype: HT
ms.sourcegitcommit: d7fb34e1c9428a64c71ff47be8bcff174649c00d
ms.openlocfilehash: d4d1c86f88acfce861a3330ba5457ce3f80c264c
ms.contentlocale: fr-ch
ms.lasthandoff: 03/22/2018

---
# <a name="posting-purchases"></a>Validation des achats
Dans le groupe **Validation** sur un document achat, vous pouvez faire votre choix parmi les fonctions de validation suivantes :

* **Valider**
* **Aperçu compta.**
* **Valider et Imprimer**
* **Impression test**
* **Valider par lot**

Lorsque vous avez renseigné toutes les lignes et saisi toutes les informations de la commande achat, vous pouvez la valider, c'est-à-dire, créer une réception et une facture.

Lorsqu’une commande achat est validée, le compte du fournisseur, les écritures comptables et les écritures comptables article sont mis à jour.

Pour chaque commande achat, une écriture achat est créée dans la table **Ecriture comptable**. Une écriture est également créée dans le compte fournisseur de la table **Ecriture fournisseur** et une autre dans le compte fournisseur approprié. De plus, la validation de la commande peut avoir pour résultat la création d'une écriture TVA et d'une écriture comptable pour le montant de la remise. La validation d'une écriture pour la remise dépend de la valeur du champ **Comptabilisation remise** de la fenêtre **Paramètres achats**.

Pour chaque ligne commande achat, une écriture comptable article est créée dans la table **Écriture comptable article** (si les lignes achat contiennent des numéros d'article) ou une écriture est créée dans la table **Écriture comptable** (si les lignes achat contiennent un compte général). En outre, les commandes achat sont toujours enregistrées dans les tables **En-tête réception achat** et **En-tête facture achat**.

Avant de commencer à valider, vous pouvez effectuer une impression test qui contient toutes les informations de la commande achat et indique les erreurs afférentes. Pour imprimer l’état, sélectionnez **Validation**, puis **Impression test**.

> [!IMPORTANT]  
>   Lorsque vous validez une commande, vous pouvez créer une réception et une facture. Celles-ci peuvent être faites simultanément ou séparément. Vous pouvez également créer une réception partielle et une facture partielle en renseignant les champs **Qté à recevoir** et **Qté à facturer** sur chaque ligne commande achat avant la validation. Remarquez que vous ne pouvez pas créer de facture pour un article qui n'a pas été reçu. C'est-à-dire que, avant de pouvoir facturer, vous devez avoir validé une réception, ou vous devez choisir de réceptionner et de facturer en même temps.

Vous pouvez soit valider, soit valider et imprimer. Si vous choisissez de valider et d’imprimer, un rapport est imprimé lorsque la commande est validée. Vous pouvez aussi choisir la fonction **Valider par lot**, qui vous permet de valider plusieurs commandes en même temps.

Lorsque la validation est terminée, les lignes achat validées sont supprimées de la commande. Un message vous indique lorsque la validation est terminée. Vous pouvez ensuite afficher les écritures validées dans les diverses fenêtres qui contiennent les écritures validées, comme les fenêtres **Écritures comptable fournisseur**, **Écritures comptable**, **Écritures comptable article**, **Réceptions achat enreg.** et **Factures achat enregistrées**.

## <a name="see-also"></a>Voir aussi
[Achats](purchasing-manage-purchasing.md)  
[Valider des documents et des feuilles](ui-post-documents-journals.md)  
[Utilisation de [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)


