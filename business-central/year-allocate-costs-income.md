---
title: Aperçu des tâches de ventilation des coûts et des revenus
description: Décrit les tâches pour ventiler une écriture d’une feuille abonnement dans différents comptes lorsque vous validez la feuille.
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bnielse
ms.topic: overview
ms.devlang: al
ms.search.form: '283, 5629'
ms.date: 02/05/2024
ms.custom: bap-template
ms.service: dynamics-365-business-central
---
# <a name="allocate-recurring-costs-and-income"></a>Ventilation des coûts et des bénéfices récurrents

Vous pouvez ventiler une écriture d’une feuille abonnement dans différents comptes lorsque vous validez la feuille. Pour en savoir plus sur les feuilles abonnement, consultez [Utiliser des feuilles abonnement](ui-work-general-journals.md#work-with-recurring-journals). 

La ventilation peut être effectuée de trois manières différentes :

* Quantité
* Pourcentage (%)
* Montant

Les fonctions de ventilation fonctionnent avec les feuilles récurrentes et dans les feuilles immobilisation.
<!--You can also distribute the cost or revenue of a line to an intercompany partner when you post a sales or purchase document. When you post the document, a line will be posted in your general journal, and a corresponding line will be created in the intercompany outbox.-->

Les procédures suivantes décrivent comment se préparer à affecter des coûts dans une feuille abonnement en définissant des clés de ventilation. Lorsque des clés de ventilation sont définies, vous renseignez et validez la feuille comme toute autre feuille abonnement. Pour en savoir plus, voir [Utiliser des feuilles comptabilité](ui-work-general-journals.md).

## <a name="to-set-up-allocation-keys"></a>Pour définir des clés de ventilation

Vous pouvez ventiler une écriture dans une feuille abonnement dans différents comptes lorsque vous validez la feuille. La ventilation peut être effectuée par quantité, pourcentage ou montant.  

1. Sélectionnez l’icône ![Ampoule qui ouvre la fonction Tell Me.](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire") entrez **Feuille récurrente**, puis sélectionnez le lien associé.
2. Sélectionnez le champ **Nom de la feuille** pour ouvrir la page **Noms feuilles comptabilité**.
3. Vous pouvez soit modifier les ventilations sur un lot existant dans la liste ou créer un lot avec des ventilations.
   * Pour créer un lot, sélectionnez l’action **Nouveau**, et passez à l’étape suivante.
   * Pour modifier les ventilations à partir d’une feuille existante, sélectionnez la feuille et passez à l’étape 7.    
4. Dans le champ **Nom**, saisissez le nom du lot, par exemple NETTOYAGE. Dans le champ **Description**, saisissez une description, par exemple Feuille frais de nettoyage.
5. Fermez la page lorsque vous avez terminé. Une nouvelle feuille récurrente vide s’ouvre.
6. Renseignez les champs de la ligne.
7. Sélectionnez l’action **Ventilations**.
8. Ajoutez une ligne pour chaque ventilation. Vous devez renseigner le champ **% ventilation**, **Quantité imputée** ou **Montant**. Vous devez également renseigner le champ **N° compte** et, si vous affectez la transaction à des axes principaux, les champs de ces axes principaux.
9. Si vous saisissez un pourcentage dans une ligne, le montant du champ **Montant** est calculé automatiquement. Ces montants sont dotés du signe opposé à celui du montant total figurant dans le champ **Montant** de la feuille récurrente.
10. Après avoir saisi les lignes de ventilation, cliquez sur **OK** pour revenir à la page **Feuille abonnement**. Le champ **Montant imputé DS** est renseigné et correspond au champ **Montant**.
11. Validez la feuille.

## <a name="to-change-an-allocation-key-that-has-already-been-set-up"></a>Pour modifier une clé de ventilation déjà configurée

1. Sélectionnez l’icône ![Ampoule qui ouvre la fonction Tell Me.](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire") entrez **Feuille récurrente**, puis sélectionnez le lien associé.
2. Sur la page **Feuille récurrente**, sélectionnez la feuille contenant la ventilation.
3. Sélectionnez la ligne de la ventilation, puis choisissez l’action **Ventilations**.
4. Modifiez les champs appropriés, puis choisissez **OK**.

## <a name="see-also"></a>Voir aussi

[Clôture des exercices et des périodes](year-close-years-periods.md)  
[Utilisation des feuilles comptabilité](ui-work-general-journals.md)    
[Validation des documents et des feuilles](ui-post-documents-journals.md)    
[Utiliser [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]
