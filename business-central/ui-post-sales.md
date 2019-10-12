---
title: Validation de documents vente | Microsoft Docs
description: Découvrez les différentes fonctions de validation pour valider les documents vente et comment mettre à jour les documents validés.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.reviewer: edupont
ms.date: 10/01/2019
ms.author: sgroespe
ms.openlocfilehash: c389a93a71b251b5b0e11f4450251fdf68b64345
ms.sourcegitcommit: 02e704bc3e01d62072144919774f1244c42827e4
ms.translationtype: HT
ms.contentlocale: fr-CH
ms.lasthandoff: 10/01/2019
ms.locfileid: "2310795"
---
# <a name="posting-sales"></a>Validation des ventes
Dans le menu **Validation** sur un document vente, vous pouvez faire votre choix parmi les fonctions de validation suivantes :

* **Valider**
* **Valider et créer**
* **Valider et envoyer**
* **Aperçu compta.**
* **Facture provisoire**
* **Facture pro forma**
* **Impression test**

Lorsque vous avez renseigné toutes les lignes et entré toutes les informations de la commande de vente, vous pouvez la valider. Cela crée une expédition et une facture.

Lorsqu’une commande vente est validée, le compte du client, les écritures comptables et les écritures comptables article sont mis à jour.

Pour chaque commande vente, une écriture vente est créée dans la table **Écriture comptable**. Une écriture est également créée dans le compte client de la table **Écriture comptable client** et une écriture comptable est créée dans le compte client approprié. De plus, la validation de la commande peut avoir pour résultat la création d’une écriture TVA et d’une écriture comptable pour le montant de la remise. La validation d’une écriture pour la remise dépend de la valeur du champ **Comptabilisation remises** de la page **Paramètres ventes**.

Pour chaque ligne commande vente, une écriture comptable article est créée dans la table **Écriture comptable article** (si les lignes vente contiennent des numéros des articles) ou une écriture comptable est créée dans la table **Écriture comptable** (si les lignes vente contiennent un compte général). En outre, les commandes vente sont toujours enregistrées dans les tables **En-tête expédition vente** et **En-tête facture vente**.

> [!IMPORTANT]  
>   Lorsque vous validez une commande, vous pouvez créer une expédition et une facture. Ceci peut être effectué de manière simultanée ou indépendante. Vous pouvez également créer une expédition partielle et une facture partielle en renseignant les champs **Qté à expédier** et **Qté à facturer** sur chaque ligne commande vente avant la validation. Notez que vous ne pouvez pas créer de facture pour un article qui n'est pas expédié. C'est-à-dire que, avant de pouvoir facturer, vous devez avoir validé une expédition, ou vous devez choisir de livrer et de facturer en même temps.

Vous pouvez soit valider, soit valider et imprimer. Si vous choisissez de valider et d’imprimer, un rapport est imprimé lorsque la commande est validée. Vous pouvez aussi choisir la fonction **Valider par lot**, qui vous permet de valider plusieurs commandes en même temps. Pour plus d'informations, voir [Valider plusieurs documents en même temps](ui-batch-posting.md).

Lorsque la validation est terminée, les lignes vente validées sont supprimées de la commande. Un message vous indique lorsque la validation est terminée. Vous pouvez ensuite afficher les écritures validées dans les diverses pages qui contiennent les écritures validées, telles que **Écritures comptables client**, **Écritures comptables**, **Écritures comptables article**, **Expéditions vente enregistrées** et **Factures vente enregistrées**.  

Vous pouvez modifier certains champs dans les documents de vente validés, tels que le champ **N° de suivi du colis**. . Pour plus d'informations, voir [Modifier les documents validés](across-edit-posted-document.md).

## <a name="see-also"></a>Voir aussi
[Ventes](sales-manage-sales.md)  
[Valider plusieurs documents en même temps](ui-batch-posting.md)  
[Valider les documents validés](across-edit-posted-document.md)  
[Envoyer des documents par e-mail](ui-how-send-documents-email.md)  
[Corriger ou annuler des factures vente impayées](sales-how-correct-cancel-sales-invoice.md)  
[Recherche de pages et d'informations avec Tell Me](ui-search.md)  
[Utilisation de [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)
