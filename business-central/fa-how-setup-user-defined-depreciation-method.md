---
title: Définir une méthode d’amortissement paramétrable
description: "Dans Business\_Central, vous pouvez appliquer une méthode d’amortissement définie par l’utilisateur pour définir la méthode d’amortissement de votre immobilisation sur la page Fiche d’immobilisation."
author: jill-kotel-andersson
ms.reviewer: bholtorf
ms.topic: conceptual
ms.search.keywords: user-depreciation
ms.date: 07/05/2021
ms.author: bholtorf
---

# <a name="set-up-fixed-assets-with-user-defined-depreciation-methods"></a>Définir des immobilisations avec des méthodes d’amortissement paramétrables

Vous pouvez utiliser [!INCLUDE[prod_short](includes/prod_short.md)] pour configurer les méthodes d’amortissement paramétrables, comme décrit ici.

Pour chaque méthode paramétrable, vous utilisez la page **Tables d’amortissement** dans laquelle vous devez saisir un pourcentage d’amortissement pour chaque période (mois, trimestre, année ou période comptable). Ensuite, lorsque vous affectez des lois d’amortissement avec une méthode définie par l’utilisateur à une immobilisation, vous devez définir les champs **Date premier amortissement** et **Date début amortissement** sur la page **Plan amortissement** pour l’immobilisation spécifique.  

La formule de calcul des montants d’amortissement est la suivante :  

*Montant de l’amortissement = (% amortissement x nombre de jours d’amortissement x base amortissement)/(100 x 360)*


> [!NOTE]  
> Alors que la date du champ **Date premier amortissement** est utilisée pour déterminer les intervalles de temps, c’est la **Date début amortissement** qui est utilisée pour déterminer le nombre de jours d’amortissement. Si la **Date premier amortissement** est antérieure à la **Date début amortissement**, le pourcentage de la première période de la table amortissement ne sera que partiellement utilisée lorsque le programme calcule le premier amortissement. Cela signifie que l’immobilisation n’est pas totalement amortie au terme de la période précédente.

## <a name="to-assign-a-depreciation-book-to-a-fixed-asset-with-a-user-defined-depreciation-method"></a>Pour affecter une loi d’amortissement à une immobilisation avec une méthode d’amortissement paramétrable

1. Sélectionnez l’icône ![en forme d’ampoule qui ouvre la fonction Tell Me.](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire") saisissez **Immobilisations**, puis choisissez le lien associé.
2. Sélectionnez l’immobilisation pour laquelle vous souhaitez configurer une loi d’amortissement.
3. Sélectionnez l’action **associée**, puis choisissez **Immobilisation**, et enfin **Lois d’amortissement**. Cela ouvre la page **Lois d’amortissement**.

   Par défaut, certains des champs qui doivent être remplis selon les instructions ci-dessous sont masqués, vous devez donc les afficher. Pour cela, vous devez personnaliser la page. Pour plus d’informations, consultez [Commencer à personnaliser une page au moyen de la bannière Personnalisation](ui-personalization-user.md#to-start-personalizing-a-page-through-the-personalizing-banner).
4. Dans le champ **Méthode amortissement**, sélectionnez **Paramétrable**.
5. Dans le champ **Code table amortissement**, sélectionnez la **Table amortissement** vous voulez utiliser.
6. Dans le champ **Date début amortissement**, sélectionnez la date de début du calcul de l’amortissement.
7. Lorsque vous utilisez une méthode définie par l’utilisateur, le champ **Date premier amortissement** doit être défini sur une date identique ou antérieure à la date du champ **Date début amortissement**. Si vous avez sélectionné une valeur dans le champ **Base période** de la table amortissement, la date du champ **Date premier amortissement** doit être la date début d’une période comptable.
8. Remplissez le champ **Nombre années amortissement** ou le champ **Date fin amortissement**. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)] 

## <a name="to-set-up-user-defined-depreciation-methods"></a>Pour définir des méthodes d’amortissement paramétrables

Sur la page **Table amortissement**, vous pouvez configurer des méthodes d’amortissement paramétrables. Par exemple, vous pouvez définir l’amortissement en fonction du nombre d’unités.  

1. Sélectionnez l’icône ![en forme d’ampoule qui ouvre la fonction Tell Me.](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire") saisissez **Tables d’amortissement**, puis choisissez le lien associé.  
2. Sur la page **Liste des tables amortissement**, sélectionnez l’action **Nouveau**.  
3. Sur la page **Fiche table d’amortissement**, renseignez les champs comme nécessaire. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]  

> [!TIP]
> Utilisez la fonction **Créer une table Somme des chiffres** pour définir une table d’amortissement basée sur la méthode *Somme des chiffres*.

Avec la méthode *Somme des chiffres*, si une immobilisation est amortie sur 4 ans, l’amortissement pour chaque année est calculé de la manière suivante :

Somme des chiffres = 1 + 2 + 3 + 4 = 10 Amortissement :

* Année 1 = 4/10  
* Année 2 = 3/10  
* Année 3 = 2/10  
* Année 4 = 1/10  

### <a name="depreciation-based-on-number-of-units"></a>Amortissement basé sur un nombre d’unités

Cette méthode paramétrable peut également être utilisée pour calculer un amortissement sur la base d’un nombre d’unités, par exemple dans le cas de machines de production dont la durée de vie est préétablie. Sur la page **Tables d’amortissement**, vous saisissez le nombre d’unités pouvant être produites au cours de chaque période (mois, trimestre, année ou période comptable).  

### <a name="example---user-defined-depreciation"></a>Exemple - Amortissement défini par l’utilisateur

Vous souhaitez utiliser une méthode d’amortissement vous permettant d’amortir des immobilisations de manière accélérée dans le cadre de l’impôt sur le revenu.  

Pour le calcul de l’impôt, utilisez les taux d’amortissement suivants pour une immobilisation ayant une durée de vie de trois ans :  

* Année 1 : 25 %  
* Année 2 : 38 %  
* Année 3 : 37 %  

Le coût d’acquisition est de 100 000 DS et la durée d’amortissement est de cinq ans. L’amortissement est calculé tous les ans.  

| Date | Type compta. immo. | Jours | Montant | Valeur comptable |
| --- | --- | --- | --- | --- |
| 01/01/20 |Coût acquisition |(Date début amortissement) |100 000,00 |100 000,00 |
| 31/12/20 |Amortissements |360 |-25 000,00 |75,000.00 |
| 31/12/21 |Amortissements |360 |-38 000,00 |37,000.00 |
| 31/12/22 |Amortissements |360 |-37 000,00 |0 |
| 31/12/23 |Amortissements |Aucun |Aucun |0 |
| 31/12/24 |Amortissements |Aucun |Aucun |0 |

Dans l’exemple précédent, les champs **Date premier amortissement** et **Date début amortissement** seraient définis sur 01/01/20 dans la page **Lois d’amortissement immo.** pour l’immobilisation spécifique. Toutefois, en supposant que le champ **Date premier amortissement** contienne la date 01/01/20 et que le champ **Date début amortissement** indique la valeur 01/04/20, le résultat serait le suivant :  

| Date | Type compta. immo. | Jours | Montant | Valeur comptable |
| --- | --- | --- | --- | --- |
| 01/01/20 |Coût acquisition |(Date début amortissement) |100 000,00 |100 000,00 |
| 31/12/20 |Amortissements |270 |-18 750,00 |81,250.00 |
| 31/12/21 |Amortissements |360 |-38 000,00 |42,250.00 |
| 31/12/22 |Amortissements |360 |-37 000,00 |6,250.00 |
| 31/12/23 |Amortissements |90 |-6 250,00 |0 |
| 31/12/24 |Amortissements |Aucun |Aucun |0 |


## <a name="see-also"></a>Voir aussi
[Paramétrage d’immobilisations](fa-setup.md)  
[COMPTES D’IMMOBILISATIONS](fa-manage.md)  
[Configurer un amortissement immobilisation](fa-how-setup-depreciation.md)  
[Méthodes amortissement pour les immobilisations](fa-depreciation-methods.md)

[!INCLUDE[footer-include](includes/footer-banner.md)]
