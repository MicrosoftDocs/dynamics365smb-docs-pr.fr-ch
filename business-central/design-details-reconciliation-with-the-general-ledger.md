---
title: Détails de conception - rapprochement de comptabilité | Microsoft Docs
description: 'Cette rubrique décrit le rapprochement de comptabilité lorsque vous validez des mouvements de stock, tels que des expéditions vente, des productions ou des ajustements négatifs.'
author: brentholtorf
ms.topic: conceptual
ms.devlang: al
ms.search.keywords: 'design, reconciliation, general ledger, inventory'
ms.date: 06/08/2021
ms.author: bholtorf
ms.service: dynamics-365-business-central
---
# Détails de conception : rapprochement de comptabilité
Lorsque vous validez des mouvements de stock, tels que des expéditions vente, des productions ou des ajustements négatifs, les modifications de quantité et de valeur des stocks sont enregistrées respectivement dans les écritures comptables article et les écritures valeur. L’étape suivante de ce processus consiste à valider les valeurs de stocks dans les comptes stocks de la comptabilité.  

Il existe deux méthodes pour rapprocher l’écriture inventaire à la comptabilité :  

* Manuellement, en exécutant le traitement par lots **Valider coûts ajustés**.  
* Automatiquement, chaque fois que vous validez un mouvement de stock.  

## Traitement par lots Valider coûts ajustés.  
Lorsque vous lancez le traitement par lots **Valider coûts ajustés**, les écritures comptables sont basées sur les écritures créées valeur. Vous avez le choix de résumer les écritures comptables pour chaque écriture valeur, ou créer des écritures comptables pour chaque combinaison de date comptabilisation, code magasin, groupe de validations de stock, groupe de validations commerciales générales, et groupe de validations produit générales.  

Les dates comptabilisation des écritures comptables sont fixées à la date comptabilisation de l’écriture valeur correspondante, sauf si l’écriture valeur se trouve dans une période comptable clôturée. Dans ce cas, l’écriture valeur est ignorée et, vous devez modifier les paramètres comptabilité ou les paramètres utilisateur pour activer la validation dans la plage de dates.  

Lorsque vous exécutez ce traitement par lots **Valider coûts ajustés**, il se peut que vous receviez des erreurs en raison d’une configuration manquante ou d’une configuration de dimension incompatible. Si le traitement par lots détecte des erreurs dans la configuration de dimension, il les ignore et utilise les dimensions de l’écriture valeur. Pour toute autre erreur, le traitement par lots ignore la validation des écritures valeur et les répertorie à la fin de l’état dans la section intitulée **Écritures ignorées**. Pour valider ces écritures, vous devez d’abord corriger les erreurs. Pour afficher la liste des erreurs avant d’exécuter le traitement par lot de validation, vous pouvez générer l’état **Valider coûts ajust. - Test**. Cet état répertorie toutes les erreurs détectées durant un test de validation. Vous pouvez corriger les erreurs, puis exécuter le traitement par lots de validation des coûts ajustés sans ignorer aucune entrée.  

## Compta. coûts automatique  
Pour configurer l’ajustement des coûts à exécuter automatiquement lorsque vous validez une transaction de stock, activez la case à cocher **Compta. coûts automatique** de la page **Paramètres stock**. La date comptabilisation de l’écriture comptable est identique à la date comptabilisation de l’écriture comptable article.  

## Types de compte  
Lors du rapprochement, les valeurs d’inventaire sont validées sur le compte du stock dans le bilan. Le même montant, mais avec le signe opposé, est validé sur le compte contrepartie approprié. Généralement, le compte d’équilibre est un compte de gestion de revenu. Néanmoins, lorsque vous validez des coûts directs liés à la consommation ou la production, le compte contrepartie est un compte de bilan. Le type de l’écriture comptable article et de l’écriture de valeur détermine sur quel compte général publier.  

Le type d’écriture indique le compte général à valider. Ceci est déterminé par le type de la quantité de l’écriture comptable article ou la quantité évaluée de l’écriture valeur, comme les quantités ont toujours même le signe. Par exemple, une écriture vente avec une quantité positive décrit une sortie de stock due à une vente, et une écriture vente avec une quantité négative décrit une entrée de stock due à un retour vente.  

### Exemple :  
L’exemple suivant présente une chaîne de vélo qui est fabriquée à partir des liens achetés. Cet exemple montre la manière dont les différents types de compte général sont utilisés pour un scénario courant.  

La case à cocher **Compta. coûts prévus** de la page **Paramètres stock** est activée et la configuration suivante est définie.  

Le tableau suivant montre la manière dont le lien est paramétré sur la fiche article.  

|Paramétrage de champ|Valeur|  
|-----------------|-----------|  
|**Mode évaluation stock**|Standard|  
|**Coût standard**|1,00 DS|  
|**Frais généraux**|0,02 DS|  

Le tableau suivant montre la manière dont la chaîne est paramétrée sur la fiche article.  

|Paramétrage de champ|Valeur|  
|-----------------|-----------|  
|**Mode évaluation stock**|Standard|  
|**Coût standard**|150,00 DS|  
|**Frais généraux**|25,00 DS|  

Le tableau suivant montre la manière dont le centre de charge est paramétré sur la fiche centre de charge.  

|Paramétrage de champ|Valeur|  
|-----------------|-----------|  
|**Coût unitaire direct**|2,00 DS|  
|**Pourcentage coût indirect**|10|  

##### Scénario  
1. L’utilisateur achète 150 liens et valide la commande achat comme reçue. (Achat)  
2. L’utilisateur valide la commande achat comme facturée. Cela crée une quantité supplémentaire de 3,00 LCY à affecter à une quantité d’écart de 18,00 LCY. (Achat)  

    1. Les comptes d’attente sont supprimés. (Achat)  
    2. Le coût direct est validé. (Achat)  
    3. Le coût indirect est calculé et validé. (Achat)  
    4. L’écart achat est calculé et validé (uniquement pour les articles de coût standard). (Achat)  
3. L’utilisateur vend une chaîne et valide la commande vente comme expédiée. (Vente)  
4. L’utilisateur valide la commande vente comme facturée. (Vente)  

    1. Les comptes d’attente sont supprimés. (Vente)  
    2. Le coût des biens vendus (COGS) est validé. (Vente)  

        ![Résultats de la validation des ventes sur les comptes généraux.](media/design_details_inventory_costing_3_gl_posting_sales.png "Résultats de la validation des ventes sur les comptes généraux")  
5. L’utilisateur valide la consommation de 150 liens, qui est le nombre de liens utilisés pour produire une chaîne. (Consommation, Matière)  

    ![Résultats de la validation des matières sur les comptes généraux.](media/design_details_inventory_costing_3_gl_posting_material.png "Résultats de la validation des matières sur les comptes généraux")  
6. Le centre de charge est utilisé 60 minutes pour produire la chaîne. L’utilisateur valide le coût de conversion. (Consommation, Capacité)  

    1. Les coûts directs sont validés. (Consommation, Capacité)  
    2. Les coûts indirects sont calculés et validés. (Consommation, Capacité)  

        ![Résultats de la validation de la capacité sur les comptes généraux.](media/design_details_inventory_costing_3_gl_posting_capacity.png "Résultats de la validation de la capacité sur les comptes généraux")  
7. L’utilisateur valide le coût prévu d’une chaîne. (Production)  
8. L’utilisateur termine l’ordre de fabrication et exécute le traitement par lots **Ajuster coûts - Écr. article**. (Production)  

    1. Les comptes d’attente sont supprimés. (Production)  
    2. Le coût direct est transféré du compte TEC vers le compte stock. (Production)  
    3. Le coût indirect (frais généraux) est transféré du compte des coûts indirects vers le compte stock. (Production)  
    4. Cela a pour résultat une quantité d’écart de 157,00 LCY. Les écarts sont uniquement calculés pour les articles de coût standard. (Production)  

        ![Résultats de la validation de la production sur les comptes généraux.](media/design_details_inventory_costing_3_gl_posting_output.png "Résultats de la validation de la production sur les comptes généraux")  

        > [!NOTE]  
        >  Pour des raisons de simplicité, un seul compte écart est affiché. En réalité, cinq comptes différents existent :  
        >   
        >  * Écart matière  
        >  * Écart opératoire  
        >  * Écart frais gén. opératoires  
        >  * Écart sous-traitance  
        >  * Écart frais généraux production  

9. L’utilisateur réévalue la chaîne de 150,00 LCY à 140,00 LCY. (Ajustement/Réévaluation/Arrondi/Transfert)  

    ![Résultats de la validation de l’ajustement sur les comptes généraux.](media/design_details_inventory_costing_3_gl_posting_adjustment.png "Résultats de la validation de l’ajustement sur les comptes généraux")  

Pour plus d’informations sur les relations entre les types de compte et les différents types d’écritures valeur, voir [Détails de conception : comptes de la comptabilité](design-details-accounts-in-the-general-ledger.md).  

## Voir aussi  
[Détails de conception : évaluation stock](design-details-inventory-costing.md)   
[Détails de conception : validation du coût prévu](design-details-expected-cost-posting.md)   
[Détails de conception : ajustement des coûts](design-details-cost-adjustment.md)
[Gestion des coûts ajustés](finance-manage-inventory-costs.md)  
[Finances](finance.md)  
[Utiliser [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]