---
title: Gérer le stockage en supprimant des documents ou en compressant des données
description: Découvrez comment conserver vos données historiques en compressant les écritures comptables ou en les supprimant.
author: edupont04
ms.service: dynamics365-business-central
ms.topic: article
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: f0d713f57345c312ddbfe6b5462f2623b1088dfc
ms.sourcegitcommit: 2e7307fbe1eb3b34d0ad9356226a19409054a402
ms.translationtype: HT
ms.contentlocale: fr-CH
ms.lasthandoff: 12/17/2020
ms.locfileid: "4753882"
---
# <a name="manage-storage-by-deleting-documents-or-compressing-data"></a>Gérer le stockage en supprimant des documents ou en compressant des données

Un rôle central, par exemple un administrateur d’application, doit régulièrement gérer les documents accumulés au fil du temps en les supprimant ou en les compressant.  

> [!TIP]
> Pour plus d’informations sur les autres moyens de réduire la quantité de données stockées dans une base de données, voir [Réduction des données stockées dans les bases de données Business Central](/dynamics365/business-central/dev-itpro/administration/database-reduce-data) dans l’aide dédiée à l’équipe IT et aux développeurs.

## <a name="delete-documents"></a>Supprimer documents

Dans certains cas, vous pouvez souhaiter supprimer des commandes achat facturées qui n’ont pas été supprimées. [!INCLUDE[prod_short](includes/prod_short.md)] vérifie que vous avez entièrement facturé les commandes achat supprimées. Vous ne pouvez pas supprimer de commandes qui n’ont pas été entièrement facturées et reçues.  

Les retours sont généralement supprimés après leur facturation. Lorsque vous validez une facture, elle est transférée vers la page **Avoir achat enregistré**. Si vous avez activé la case à cocher **Expédition retour sur avoir** sur la page **Paramètres achats**, la facture est transférée vers la page **Expédition retour enregistrée**. Vous pouvez supprimer les documents à l’aide du traitement par lots **Supprimer les retours achat facturés**. Avant de procéder à la suppression, le traitement par lots vérifie que les retours achat ont été entièrement livrés et facturés.  

Les commandes ouvertes achat ne sont pas supprimées une fois que toutes les commandes achat associées ont été traitées et facturées. Vous pouvez supprimer les commandes ouvertes à l’aide du traitement par lots **Supprimer commandes ouvertes achat facturées**.  

Les commandes service facturées sont habituellement supprimées automatiquement après avoir été entièrement facturées. Lors de la validation d’une facture, une écriture correspondante est générée sur la page **Factures service enreg.**. Vous pouvez afficher le document validé sur la page **Facture service enreg.**.  

Le programme ne supprime pas la commande service automatiquement cependant, si la quantité totale sur la commande a été validée, non pas à partir de la commande service proprement dite, mais à partir de la page **Facture service**. Ensuite, il se peut que vous deviez supprimer des commandes facturées qui n’ont pas été supprimées. Pour ce faire, exécutez le traitement par lots **Supprimer commandes service facturées**.  

## <a name="compress-data-with-date-compression"></a>Compresser les données avec la compression selon la date

Vous pouvez compresser les données dans [!INCLUDE [prod_short](includes/prod_short.md)] afin d’économiser de l’espace dans la base de données, qui dans [!INCLUDE [prod_short](includes/prod_short.md)] en ligne peut même vous faire économiser de l’argent. La compression est basée sur les dates et s’effectue en combinant plusieurs anciennes écritures en une nouvelle écriture. Vous pouvez uniquement compresser des écritures d’exercices comptables clôturés, et seulement les écritures comptables fournisseur dont le champ **Ouvert** indique *Non*.  

Par exemple, les écritures comptables fournisseur d’exercices précédents peuvent être compressées de façon à ce qu’il ne reste qu’une écriture créditrice et une écriture débitrice par compte et par mois. Le montant de la nouvelle écriture est la somme de toutes les écritures compressées. La date affectée est la date de début de la période qui est compressée, par exemple le premier jour du mois (si les écritures sont compressées par mois). Après la compression, vous pouvez encore afficher le solde période de chaque compte de l’exercice précédent.

Le nombre d’écritures qui résultent d’un traitement par lots de compression dépend du nombre filtres que vous définissez, des champs qui sont combinés et de la durée de la période que vous choisissez. Il y aura toujours au moins une écriture. Lorsque le traitement par lots est terminé, le résultat s’affiche dans la page **Historique des compressions**.

Vous pouvez compresser les types de données suivants dans [!INCLUDE [prod_short](includes/prod_short.md)] à l’aide de traitements par lots :

* Écritures comptables compte bancaire

  Après la compression, l’option **Conserver champs** vous permet de conserver la valeur des champs **N° document, Notre contact**, **Code axe principal 1** et **Code axe principal 2**.
* Écritures comptables fournisseur

  Après la compression, le contenu des champs suivants sera toujours conservé : **Date comptabilisation**, **N° fournisseur**, **Type de document**, **Code devise**, **Groupe comptabilisation**, **Montant**, **Montant ouvert**, **Montant initial DS**, **Montant ouvert DS**, **Montant DS**, **Achat DS**, **Remises facture DS**, **Escompte accordé DS** et **Escompte ouvert possible**.

  Avec l’option **Conserver champs**, vous pouvez également conserver la valeur de ces champs supplémentaires : **N° document**, **N° fournisseur**, **Code acheteur**, **Code axe principal 1** et **Code axe principal 2**.

> [!NOTE]
> Après avoir exécuté la compression des dates, tous les comptes du grand livre sont verrouillés. Par exemple, vous ne pouvez pas désappliquer les écritures du fournisseur ou du grand livre bancaire pour les comptes au cours de la période pour laquelle les dates sont compressées.

<!--* General ledger entries
* Customer ledger entries-->
<!--* Fixed asset ledger entries
* G/L budget entries
* VAT entries

  After the compression the contents of the following fields are always retained: **Posting Date**, **Type**, **Closed**, **Gen. Bus. Posting Group**, **Gen. Prod. Posting Group**, **VAT Calculation Type**, **Base**, and **Amount**.

  With the **Retain Field Contents** facility, you can also retain the contents of the following additional fields: **Document No.**, **Bill-to/Pay-to No.**, **EU 3-Party Trade**, **Country/Region Code**, and **Internal Ref. No.**.
* Insurance ledger entries
* Maintenance ledger entries
* Resource ledger entries

  After the compression, the contents of the following fields are retained: **Posting Date**, **Resource No.**, **Resource Group No.**, **Entry Type**, **Quantity**, **Total Cost**, **Total Price**, and **Chargeable**.

  With the **Retain Field Contents** facility, you can also retain the contents of the following additional fields: **Document No.**, **Work Type Code**, **Job No.**, **Unit of Measure Code**, **Source Type**, **Source No.**. **Chargeable**, **
* Warehouse entries

  After the compression the contents of the following fields are always retained: **Registering Date**, **Location Code**, **Zone Code**, **Bin Code**, **Item No.**, **Quantity**, **Qty. (Base)**, **Bin Type Code**, **Entry Type**, **Variant Code**, **Qty. per Unit of Measure**, **Unit of Measure Code**, **Warranty Date**, **Expiration Date**, **Cubage**, and **Weight**.

  With the **Retain Field Contents** facility, you can also retain the contents of the **Serial No.** and **Lot No.** fields. -->

Le nombre d’écritures qui résultent d’un traitement par lots de compression dépend du nombre filtres que vous définissez, des champs qui sont combinés et de la durée de la période que vous choisissez. Il y aura toujours au moins une écriture. 

> [!WARNING]
> La compression selon la date supprime des écritures ; vous devez donc toujours faire une sauvegarde de la base de données avant de lancer le traitement par lots.

Le tableau suivant répertorie les champs du raccourci **Options** disponibles sur tous les traitements par lots. La section **Conserver le contenu du champ** comprend des champs supplémentaires qui sont décrits ci-dessus.

|Champ  |Description  |
|-------|-------------|
|Date de début     |Saisissez la première date à inclure dans la compression. La compression affecte toutes les écritures comprises entre cette date et la date fin.|
|Date de fin     |Saisissez la dernière date à inclure dans la compression. La compression affecte toutes les écritures comprises entre la date début et cette date.|
|Base période |Sélectionnez la durée de la période pendant laquelle les écritures vont être combinées. Pour visualiser les options, cliquez sur le champ. Si vous sélectionnez la longueur de la période *Trimestre*, *Mois* ou *Semaine*, seules les écritures ayant une période comptable commune sont compressées.|
|Conserver champs     |Activez les champs si vous souhaitez conserver la valeur de certains champs bien que les écritures soient compressées. Plus vous choisissez de champs à conserver, plus les écritures compressées sont détaillées. Si vous ne sélectionnez aucun champ, le traitement par lots crée une écriture par jour, par semaine, ou pour une autre période, selon la période sélectionnée dans le champ **Base période**. |

## <a name="see-also"></a>Voir aussi

[Administration](admin-setup-and-administration.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]