---
title: Sous-traiter la production
description: "Cette rubrique donne un aperçu détaillé des fonctionnalités étendues de la sous-traitance dans Business\_Central, y compris les champs de centre de charge et de gamme."
author: brentholtorf
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 99000886
ms.date: 06/22/2021
ms.author: bholtorf
---
# <a name="subcontract-manufacturing"></a>Sous-traiter la production

La sous-traitance des opérations sélectionnées au fournisseur est courante dans de nombreuses sociétés de production. La sous-traitance peut être occasionnelle ou faire partie intégrante des processus de production.

[!INCLUDE[prod_short](includes/prod_short.md)] fournit plusieurs outils pour gérer le travail de sous-traitance :  

- Centre de charge avec fournisseur affecté : cette fonctionnalité permet de configurer un centre de charge associé à un fournisseur (sous-traitant). Il s’agit d’un centre de charge sous-traitant. Vous pouvez spécifier un centre de charge sous-traitant sur une opération de gamme, ce qui permet de traiter aisément l’activité sous-traitée. En outre, le coût de l’opération peut être indiqué au niveau de la gamme ou du centre de charge.  
- Coût du centre de charge basé sur des unités de temps : cette fonctionnalité permet de spécifier si les coûts associés au centre de charge sont basés sur le temps de fabrication ou un coût unitaire. Bien que les sous-traitants utilisent généralement un coût unitaire pour facturer leurs services, l’application peut gérer les deux options (temps de fabrication et coût unitaire).  
- Propositions sous-traitance : cette fonctionnalité vous permet de rechercher les ordres de fabrication dont les matériaux sont prêts pour envoi à un sous-traitant et de créer automatiquement des commandes achat pour sous-traiter des opérations à partir de gammes d’ordre de fabrication. L’application valide automatiquement les frais de commande achat dans l’ordre de fabrication durant la validation de la commande achat. Seuls les ordres de fabrication dont l’état est lancé sont accessibles et utilisables à partir d’une proposition sous-traitance.  

## <a name="subcontract-work-centers"></a>Centres de charge sous-traitants
Les centres de charge sous-traitants sont configurés de la même manière que les centres de charge ordinaires avec des informations supplémentaires. Ils sont affectés à des gammes de la même manière que d’autres centres de charge.  

### <a name="subcontract-work-center-fields"></a>Champs Centres de charge sous-traitants
Le champ **N° sous-traitant** désigne le centre de charge comme centre de charge sous-traitant. Vous pouvez entrer le numéro d’un sous-traitant qui fournit le centre de charge. Ce champ permet d’administrer des centres de charge qui ne sont pas internes mais effectuent un traitement sous contrat.  

Si vous sous-traitez avec le fournisseur à un taux différent pour chaque traitement, sélectionnez le champ **Coût unitaire spécifique**. Cela vous permet de configurer un coût sur chaque ligne gamme et vous évite de devoir saisir à nouveau chaque commande achat. Le coût d’une ligne gamme est utilisé dans le cadre du traitement au lieu du coût des champs de coût du centre de charge. La sélection du champ **Coût unitaire spécifique** permet de calculer des coûts pour le fournisseur par opération de gamme.  

Si vous sous-traitez à un coût unique par fournisseur, laissez le champ **Coût unitaire spécifique** vide. Configurez les coûts en renseignant les champs **Coût unitaire direct**, **% coût indirect** et **Frais généraux**.  

### <a name="routings-that-use-subcontract-work-centers"></a>Gammes qui utilisent des centres de charge sous-traitants
Vous pouvez utiliser des centres de charge sous-traitants pour des opérations de gamme de la même manière que des centres de charge ordinaires.  

Vous pouvez configurer un gamme utilisant un centre de charge externe comme étape opérationnelle standard. Vous pouvez également modifier la gamme pour un ordre de fabrication particulier afin d’inclure une opération externe. Cela peut être nécessaire en cas d’urgence, par exemple pour un serveur défaillant, ou durant une période temporaire de demande accrue, où le travail généralement traité en interne doit être délégué à un sous-traitant.  

Pour plus d’informations, reportez-vous à [Créer des gammes](production-how-to-create-routings.md).  

## <a name="calculate-subcontracting-worksheets-and-create-subcontract-purchase-orders"></a>Calculer des propositions de sous-traitance et créer des commandes achat de sous-traitance
Après le calcul des propositions sous-traitance, le document approprié, en l’occurrence une commande achat, est créé.  

La page **Proposition sous-traitance** fonctionne comme la **Feuille planning** en calculant les approvisionnements nécessaires \(dans ce cas, les commandes achat\) que vous vérifiez dans la feuille puis créez à l’aide de la fonction **Traiter messages d’action**.  

> [!NOTE]  
>  Seuls les ordres de fabrication dont l’état est **Lancé** sont accessibles et utilisables à partir d’une proposition sous-traitance.  

### <a name="to-calculate-the-subcontracting-worksheet"></a>Pour calculer des propositions sous-traitance
1.  Sélectionnez l’icône ![Ampoule qui ouvre la fonction Tell Me.](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire") entrez **Propositions sous-traitance**, puis sélectionnez le lien associé.  
2.  Pour calculer la feuille, choisissez l’action **Générer sous-traitances**.  
3.  Sur la page **Générer sous-traitances**, définissez des filtres pour les opérations de sous-traitance, ou les centres de charge où celles-ci sont effectuées, pour ne calculer que les ordres de fabrication appropriés.  
4.  Choisissez le bouton **OK**.  

    Examinez les lignes de la page **Propositions sous-traitance**. Les informations de cette feuille proviennent des lignes de l’ordre de fabrication et de la gamme de l’ordre de fabrication et sont insérées dans la commande achat lors de la création de ce document. Vous pouvez supprimer une ligne de la feuille sans toucher aux informations d’origine, tout comme vous pouvez le faire avec les autres feuilles. Les informations réapparaissent à la prochaine exécution de la fonction **Générer sous-traitances**.  

### <a name="to-create-the-subcontract-purchase-order"></a>Pour créer la commande achat sous-traitance
1.  Sélectionnez l’icône ![Ampoule qui ouvre la fonction Tell Me.](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire") entrez **Propositions sous-traitance**, puis sélectionnez le lien associé.  
2.  Choisissez l’action **Traiter message d’action**.  
3.  Sélectionnez le champ **Imprimer commandes** pour imprimer la commande achat lors de sa création.  
4.  Cliquez sur le bouton **OK**.  

Si toutes les opérations de sous-traitance sont adressées au même magasin fournisseur, alors une seule commande achat est créée.  

La ligne proposition transformée en commande achat est supprimée de la feuille. Une fois qu’une commande achat est créée, elle n’apparaît pas de nouveau dans la feuille.  

## <a name="posting-subcontract-purchase-orders"></a>Validation de commandes achat de sous-traitance
Une fois les commandes achat de sous-traitant créées, il est possible de les valider. La réception de la commande valide une écriture comptable capacité dans l’ordre de fabrication et la facturation de ce dernier valide le coût direct de la commande achat dans l’ordre de fabrication.  

## <a name="to-post-a-subcontract-purchase-order"></a>Pour valider une commande achat sous-traitance
1.  Sélectionnez l’icône ![Ampoule qui ouvre la fonction Tell Me.](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire") entrez **Commandes achat**, puis sélectionnez le lien associé.  
2.  Ouvrez une commande achat créée à partir de la proposition de sous-traitance.  

    Sur les lignes commande achat, vous pouvez visualiser les mêmes informations qui étaient dans la feuille. Les champs **N° ordre de fabrication**, **N° ligne O.F.**, **N° opération** et **N° centre de charge** sont renseignés avec les informations de l’ordre de fabrication source.  

3.  Sélectionnez l’action **Valider**.  

Lorsque l’achat est validé comme reçu, une écriture feuille production est automatiquement validée pour l’ordre de fabrication. Cela s’applique uniquement si l’opération de sous-traitance est la dernière opération sur la gamme de l’ordre de fabrication.  

> [!CAUTION]  
>  La validation automatique de la production pour un ordre de fabrication en cours lorsque des articles sous-traités peut ne pas être souhaitée. Les raisons à cela peuvent être une différence entre la quantité produite prévue validée et la quantité réelle, et l"inexactitude de la date validation de la production automatique.  
>   
>  Pour éviter que la production prévue d’un ordre de fabrication ne soit validée lorsque les achats de sous-traitance sont réceptionnés, veillez à ce que l’opération sous-traitée ne soit pas la dernière. Sinon, insérez une dernière opération pour la quantité produite finale.  

Lorsque la commande achat est validée comme facturée, son coût direct est validé dans l’ordre de fabrication.  

## <a name="see-also"></a>Voir aussi
[Production](production-manage-manufacturing.md)    
[Paramétrage de la production](production-configure-production-processes.md)  
[Planifié](production-planning.md)      
[Stock](inventory-manage-inventory.md)  
[Achats](purchasing-manage-purchasing.md)  
[Utiliser [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]
