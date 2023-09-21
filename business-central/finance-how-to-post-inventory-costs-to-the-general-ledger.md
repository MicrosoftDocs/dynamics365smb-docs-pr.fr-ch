---
title: Rapprocher les coûts ajustés avec la comptabilité
description: 'À la fin de la période comptable, une série de tâches de contrôle des coûts et d’audit doivent être effectuées pour déclarer une valeur en stock correcte et équilibrée au département Finances.'
author: brentholtorf
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 'warehouse, stock'
ms.search.form: 9297
ms.date: 06/16/2021
ms.author: bholtorf
---
# <a name="reconcile-inventory-costs-with-the-general-ledger"></a>Rapprocher les coûts ajustés avec la comptabilité

Lorsque vous validez des mouvements de stock, tels que des expéditions vente, des factures achat ou des ajustements de stock, les coûts article modifiés sont enregistrés dans les écritures valeur. Pour refléter ces modifications de la valeur stock dans vos livres financiers, les coûts stocks sont automatiquement validés dans les comptes stock associés dans les écritures comptables. Pour chaque mouvement stock que vous validez, les valeurs appropriées sont validées dans le compte stocks, le compte ajustement et le compte validation stock dans la comptabilité.

La comptabilisation des coûts automatique est définie par le champ **Compta. coûts automatique** sur la page **Paramètres stock**.

Bien que les coûts soient automatiquement validés en comptabilité, il est malgré tout nécessaire de vous assurer que les coûts des biens sont transmis à la transaction de vente sortante associée, notamment dans les situations où vous vendez des biens avant de facturer l’achat. Il s’agit d’un ajustement des coûts. Le coût des articles est ajusté automatiquement lorsque vous validez des transactions article, mais vous pouvez également les ajuster manuellement. Pour en savoir plus, voir [Ajuster coûts article](inventory-how-adjust-item-costs.md).

## <a name="to-post-inventory-costs-manually"></a>Pour valider des coûts ajustés manuellement

1. Sélectionnez l’icône ![Ampoule qui ouvre la fonction Tell Me.](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire") saisissez **Valider coûts ajustés**, puis choisissez le lien associé.
2. Validez les coûts ajustés dans la comptabilité manuellement en exécutant le traitement par lots. Lorsque vous exécutez ce dernier, des écritures comptables sont créées, basées sur des écritures valeur. Vous pouvez valider les écritures de façon à ce qu’elles soient récapitulées par groupe comptabilisation.

> [!NOTE]  
> Lorsque vous exécutez ce traitement par lots, il se peut que vous rencontriez des erreurs en relation avec une configuration manquante ou une configuration de dimension incompatible. Si le traitement par lots détecte des erreurs dans la configuration de dimension, il les ignore et utilise les dimensions de l’écriture valeur. Pour toute autre erreur, le traitement par lots ignore la validation des écritures valeur et les répertorie à la fin de l’état dans la section intitulée « Écritures ignorées ». Pour valider ces écritures, vous devez corriger les erreurs.

Pour afficher la liste des erreurs avant d’exécuter le traitement par lot de validation, vous pouvez générer l’état **Valider coûts ajust. - Test**. L’impression test répertorie toutes les erreurs détectées durant le test de validation. Vous pouvez ensuite corriger les erreurs et exécuter le traitement par lots de validation des coûts ajustés sans ignorer aucune entrée.

Si vous voulez simplement afficher un aperçu des valeurs qui pourraient être validées dans la comptabilité sans réellement effectuer la validation, vous pouvez exécuter le traitement par lots **Valider coûts ajustés** sans réellement valider les valeurs dans la comptabilité. Pour ce faire, désactivez le champ **Valider** sur la page de sélection. De cette manière, lorsque vous exécutez le traitement par lots, l’état est produit, indiquant les valeurs prêtes pour imputation dans la comptabilité, mais elles ne sont pas validées.

## <a name="to-audit-the-reconciliation-between-the-inventory-ledger-and-the-general-ledger"></a>Pour vérifier le rapprochement de l’écriture inventaire et de la comptabilité
La page **Stocks - Rapprochement compta.** fournit ce qui suit :

- présente les différences de rapprochement en comparant ce qui est enregistré dans la comptabilité et dans l’écriture inventaire (écritures valeur) ;
- affiche les montants coût non rapprochés des écritures valeur dans l’écriture inventaire comme s’ils étaient mappés aux comptes en relation avec le stock correspondants dans la comptabilité, et les compare aux totaux réellement enregistrés dans ces mêmes comptes ;
- Reflète la structure à double écriture de la comptabilité en présentant graphiquement les données en tant que telles. Par exemple, une écriture CMV est associée à une écriture stock.
- permet aux utilisateurs de consulter et de visualiser les écritures qui constituent le montant coût ;
- inclut des filtres qui permettent d’affiner l’analyse par date, article et magasin ;
- explique les motifs des différences de rapprochement dans des messages à caractère informatif.


La colonne **Nom** située à gauche de la grille répertorie les différents types de compte général associés au stock.

Les colonnes **Stock**, **Stocks (attente)** et **Stock en-cours** indiquent les totaux facturés, non facturés (en attente) et de stock en cours pour chaque type de compte général. Ceux-ci sont calculés sur la base des écritures valeur, c’est-à-dire qu’ils sont projetés sur les types de compte général définitifs lorsqu’ils sont validés dans la comptabilité.

La colonne **Total** indique la somme (en gras) des montants des écritures valeur dans les trois colonnes de stock.

La colonne **Total comptabilité** indique les montants (en gras) pour chaque type de compte général existant dans la comptabilité. Ils sont calculés sur la base des écritures comptables, c’est-à-dire qu’ils représentent des coûts déjà validés dans la comptabilité.

La colonne **Différence** représente la différence entre la valeur des champs **Total compta.** et **Total**.

En haut de la page **Stocks - Rapprochement compta.**, vous pouvez appliquer des filtres pour limiter, par exemple, la période sur laquelle vous voulez obtenir des informations.

Si vous sélectionnez la case à cocher **Afficher avertissement** et s’il y a des différences entre les totaux généraux et ceux du stock, l’application affiche des messages dans le champ **Alerte** de la grille, qui expliquent la différence. Si vous cliquez sur le champ Alerte, l’application fournit des informations supplémentaires sur la signification de l’alerte.

Après avoir entré tous les filtres appropriés, choisissez l’action **Afficher la matrice**. Les données sont calculées et la page de la matrice s’affiche.

La colonne de gauche de la grille affiche les différents types de compte général associés aux stocks. La grille affiche ensuite les totaux facturés, non facturés (en attente) et de stock en cours pour chacun de ces types de compte. Ces totaux sont calculés à partir des écritures valeur.

Les colonnes suivantes affichent les totaux pour les mêmes types de compte, calculés à partir des écritures comptables.

Choisissez le montant dans l’un des champs de Total pour afficher les écritures état stock utilisées pour calculer les totaux. Pour les totaux en stock, les écritures état stock sont les sommes des écritures valeur pour les articles. Pour les totaux généraux, les écritures état stock sont les sommes des écritures comptables.

## <a name="reporting-costs-and-reconciling-with-the-general-ledger"></a>Génération des coûts et rapprochement en comptabilité
D’autres rapports, des fonctions de traçage et un outil de rapprochement spécial sont à la disposition de l’auditeur ou du contrôleur chargé de rendre compte d’une valeur d’inventaire correcte et équilibrée au service financier.

Le tableau suivant décrit les valeurs.    

|**Pour**|**Voir**|  
|------------|-------------|  
|Afficher la valeur en stock des articles sélectionnés, y compris les informations sur les quantités et les valeurs des augmentations et des diminutions sur une période donnée.|**État Évaluation du stock**|  
|Afficher la valeur en stock des ordres de fabrication sélectionnés dans votre stock d’en-cours, telle que les quantités et valeurs de consommation, d’utilisation des capacités et de production dans les ordres de fabrication en cours.|**Évaluation du stock - État des travaux en cours**|  
|Afficher la valeur en stock des articles sélectionnés, y compris leur coût réel et prévu à la date spécifiée.|**Éval. stock - Composante coût**|  
|Utiliser un état pour analyser les raisons des écarts de coûts ou pour obtenir un aperçu du coût des marchandises vendues (CMV).|État **Analyse des coûts**|  

## <a name="see-also"></a>Voir aussi
[Gestion des coûts ajustés](finance-manage-inventory-costs.md)  
[Achats](purchasing-manage-purchasing.md)  
[Ventes](sales-manage-sales.md)    
[Utiliser [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  
[Fonctionnalités marché](ui-across-business-areas.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]
