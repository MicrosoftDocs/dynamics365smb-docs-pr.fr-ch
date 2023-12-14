---
title: Créer des gammes
description: 'Cette rubrique donne une vue d’ensemble des différentes manières de créer des gammes, y compris les conditions préalables requises et comment créer des liens de gamme.'
author: brentholtorf
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.form: '99000764, 99000765, 99000766, 99000767, 99000794, 99000796, 99000798, 99000806, 99000808, 99000810, 99000817, 99000834, 99000835, 99000836, 99000837, 99000840, 99000841, 99000844, 99000845'
ms.date: 06/22/2021
ms.author: bholtorf
---
# <a name="create-routings"></a>Créer des gammes

Les sociétés manufacturières utilisent des gammes pour visualiser et gérer le processus de fabrication.

La gamme est la base de la planification des processus et des capacités, de l’affectation planifiée du matériel en fonction des besoins et des documents de production.  

En ce qui concerne les nomenclatures de production, les gammes sont affectées à l’article fini produit. Une gamme contient les données de base qui capturent les exigences du traitement correspondant à un article produit donné. Après la création d’un ordre de fabrication pour cet article, sa gamme gouvernera le calendrier des opérations tels que représenté sur la page **Gamme O.F.** sous l’ordre de fabrication.  

Pour pouvoir configurer une gamme, les éléments suivants doivent être en place :  

- Des fiches article sont créées pour les articles parents qui participent à la production. Pour plus d’informations, reportez-vous à [Enregistrer de nouveaux articles](inventory-how-register-new-items.md).
- Les ressources de production sont configurées. Pour plus d’informations, voir [Configurer les centres de charge et les postes de charge](production-how-to-set-up-work-and-machine-centers.md).

## <a name="to-create-a-routing"></a>Pour créer une gamme

1. Sélectionnez l’icône ![Ampoule qui ouvre la fonction Tell Me.](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire") saisissez **Gammes**, puis sélectionnez le lien associé.  
2. Sélectionnez l’action **Nouveau**.  
3. Renseignez les champs selon vos besoins. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
4. Dans le champ **Type**, sélectionnez **Série** pour calculer la gamme de fabrication en fonction de la valeur de **N° opération** . .  
    Sélectionnez **Parallèle** pour calculer les opérations en fonction de la valeur de **Numéro de l’opération suivante**. .  
5. Pour modifier la gamme, définissez le champ **Statut** sur **Création en cours** ou sur **Modification en cours**. Pour l’activer, définissez le champ **Statut** sur **Validée**.  

    Renseignez les lignes gamme.
6. Dans le champ **N° opération**, entrez le numéro de la première opération \(par exemple, **10**\).  
7. Dans le champ **Type**, sélectionnez le type de ressource utilisé, par exemple, **Centre de charge**.  
8. Dans le champ **N°**, sélectionnez la ressource à utiliser, ou entrez\-la.  
9. Dans le champ **Code lien gamme**, vous pouvez entrer un code permettant de lier le composant à une opération spécifique. Pour plus d’informations, reportez-vous à [Pour créer des liens gamme](production-how-to-create-routings.md#to-create-routing-links).
10. Dans les champs **Temps d’exécution** et **Temps de préparation**, entrez les temps opératoires nécessaires pour exécuter l’opération.

     > [!NOTE]
     > Le temps de préparation est calculé par O.F., tandis que le temps d’exécution est calculé par article produit.  

11. Dans le champ **Capacités simultanées** , indiquez combien d’unités de la ressource sélectionnée sont utilisées pour exécuter l’opération. Par exemple, deux personnes affectées à une opération de livraison diviseront par deux le temps d’exécution.  
12. Poursuivez le remplissage des lignes pour toutes les opérations intervenant dans la production de l’article en question.  
13. Pour copier des lignes à partir d’une gamme existante, choisissez l’action **Copier gamme** pour sélectionner des lignes existantes.  
14. Certifiez la gamme.  
15. Vous pouvez désormais lier la nouvelle gamme à la fiche de l’article produit concerné en renseignant le champ **N° gamme**. Pour plus d’informations, reportez vous à [Enregistrer de nouveaux articles](inventory-how-register-new-items.md).  

> [!NOTE]  
> N’oubliez pas également de recalculer le coût standard de l’article de la fiche **Article** : choisissez l’action **Production**, sélectionnez l’action **Calculer coût standard**, puis sélectionnez l’action **Tous niveaux**.  

## <a name="to-create-routing-links"></a>Pour créer des liens gamme

Vous pouvez créer des liens gamme pour lier des composants à des opérations spécifiques afin de conserver leur relation, même si la nomenclature de production ou la gamme sont modifiées. Cela simplifie également la consommation automatique juste-à-temps des composants, à savoir lorsque l’opération liée commence, et non quand l’ordre de fabrication complet est lancé. Pour plus d’informations, voir [Consommer en aval des composants en fonction de la production réalisée](production-how-to-flush-components-according-to-operation-output.md).  

Les composants et opérations liés apparaissent dans une structure opératoire logique lorsque vous utilisez la page **Feuille production** pour la validation production et consommation, ce qui constitue un autre avantage majeur.  

1. Sélectionnez l’icône ![Ampoule qui ouvre la fonction Tell Me.](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire") saisissez **Gammes**, puis sélectionnez le lien associé.  
2. Ouvrez la gamme contenant les opérations que vous voulez lier.  

    Vérifiez que le statut de la gamme est **Modification en cours**.  

3. Sur la ligne gamme appropriée, dans le champ **Code lien gamme** , sélectionnez un code.  
4. Ajoutez ensuite plusieurs codes lien gamme à d’autres opérations de la gamme, si nécessaire.  

    > [!NOTE]  
    > Vous ne devez pas utiliser le même code lien gamme dans plusieurs opérations d’une gamme, car vous risquez de lier de manière incorrecte un même composant à deux opérations différentes et, de ce fait, de le consommer deux fois.  
    >
    > Il peut être judicieux de nommer le code lien gamme au terme de l’opération pour garantir que les liens gamme soient propres à chaque opération.

5. Définissez le statut de la gamme sur **Validé**.  

    Les codes lien gamme sont désormais affectés aux opérations. Ensuite, vous devez créer le lien réel en attribuant les mêmes codes à des composants spécifiques de la nomenclature de production appropriée.  

6. Ouvrez la **Nomenclature de production** qui contient les composants à lier aux opérations ci-dessus. Pour plus d’informations, reportez-vous à [Créer des nomenclatures de production](production-how-to-create-production-boms.md).
7. Vérifiez que le statut de la nomenclature est **Modification en cours**.  
8. Sur la ligne appropriée de nomenclature de production, dans le champ **Code lien gamme**, sélectionnez le code que vous venez d’affecter à l’opération correspondante.  
9. Ajoutez ensuite des codes lien gamme à d’autres composants, selon les opérations uniques pour lesquelles ils sont utilisés.  
10. Définissez le statut de la nomenclature de production sur **Validé**.  

    > [!NOTE]  
    > Pour activer les liens gamme d’un ordre de fabrication existant, vous devez actualiser l’ordre de fabrication. Pour plus d’informations, voir [Créer des ordres de fabrication](production-how-to-create-production-orders.md).  

Les composants sélectionnés seront liés aux opérations sélectionnées lorsque vous créerez ou actualiserez un ordre de fabrication à l’aide de la nomenclature de production et de la gamme concernées. Ceci est visible sur la page **Composants O.F.** sous l’ordre de fabrication. Ici, vous pouvez également ajouter ou supprimer à tout moment les codes lien gamme définis.

## <a name="to-assign-personnel-tools-and-quality-measures-to-routing-operations"></a>Pour affecter des qualifications, des outils et des contrôles qualité à des opérations gamme

Si vous avez besoin de personnes ayant des qualifications, un savoir-faire particulier, ou bénéficiant d’une autorisation spéciale pour une opération, vous pouvez affecter ces personnes à l’opération. En outre, vous pouvez affecter des outils et des exigences de qualité à l’opération. Cette procédure décrit l’affectation de qualifications. Les étapes sont similaires pour d’autres types d’informations sur l’opération.

1. Sélectionnez l’icône ![Ampoule qui ouvre la fonction Tell Me.](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire") saisissez **Gammes**, puis sélectionnez le lien associé.  
2. Ouvrez la gamme appropriée.  
3. Sur le raccourci **Lignes**, sélectionnez la ligne à traiter, choisissez l’action **Opérations**, puis choisissez l’action **Qualifications**.  
4. Renseignez les champs de la page **Qualifications gamme**.  
5. Cliquez sur le bouton **OK** pour quitter la page. Les valeurs saisies sont copiées et affectées à l’opération.  

## <a name="to-create-a-new-versions-of-a-routing"></a>Pour créer une nouvelle version d’une gamme

Le principe de la version permet de gérer différentes versions d’une gamme. La structure d’une version de gamme correspond à la structure de la gamme composée d’un en-tête et de lignes version de gamme. La différence de base est définie par la date début.  

1. Sélectionnez l’icône ![Ampoule qui ouvre la fonction Tell Me.](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire") saisissez **Gammes**, puis sélectionnez le lien associé.  
2. Sélectionnez la gamme à copier, puis choisissez l’action **Versions**.  
3. Sur la page **Versions de gamme**, sélectionnez l’action **Nouveau**.
4. Renseignez les champs selon vos besoins.
5. Dans le champ **Code version**, saisissez le numéro d’identification unique de la version. Ce champ admet n’importe quelle combinaison de chiffres et de lettres.  

    Le statut **Nouveau** est automatiquement affecté à la version que vous venez de créer.  
6. Pour créer des lignes opération, sélectionnez la première ligne vide, puis renseignez le champ **N° opération** en fonction de la séquence des opérations.

    Les lignes opération sont triées par ordre croissant, en fonction du numéro des opérations. Afin de faciliter les modifications ultérieures, optez pour des incréments de taille adéquate. Le champ **N° opération suivante** se réfère à l’opération suivante. Vous pouvez y entrer directement le numéro de l’opération.

7. Lorsque la version de gamme est terminée, définissez le champ **Statut** sur **Validé**.

La validité de la version est définie par le champ **Date début**.  

## <a name="see-also"></a>Voir aussi

[Créer des nomenclatures de production](production-how-to-create-production-boms.md)  
[Paramétrage de la production](production-configure-production-processes.md)  
[Production](production-manage-manufacturing.md)  
[Planifié](production-planning.md)  
[Stock](inventory-manage-inventory.md)  
[Achats](purchasing-manage-purchasing.md)  
[Utiliser [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
