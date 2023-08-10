---
title: Créer une gamme
description: Procédure pas à pas pour apprendre à saisir manuellement toutes les informations relatives à une nouvelle gamme dans Business Central.
ms.date: 04/01/2022
ms.topic: article
ms.service: dynamics365-business-central
author: edupont04
ms.author: andreipa
---
# <a name="walkthrough-create-a-new-routing"></a>Procédure pas à pas : Créer une gamme

Dans cet article, nous vous expliquons comment utiliser les données de démonstration Contoso Coffee pour configurer manuellement une nouvelle gamme de production dans [!INCLUDE [prod_short](../../includes/prod_short.md)].  

## <a name="scenario"></a>Scénario

Oscar, l’ingénieur de processus chez Contoso Coffee, décide de créer une gamme nommée *Nouveau chemin*. Étant donné que cette gamme ne ressemble à aucune autre chez Contoso Coffee, Oscar doit saisir manuellement toutes les informations relatives à la gamme.  

## <a name="steps"></a>Étapes

1. Créez l’en-tête de la gamme.  

    1. Sélectionnez ![l’icône en forme d’Ampoule qui ouvre la fenêtre de recherche](../../media/ui-search/search_small.png "Dites-moi ce que vous voulez faire"), saisissez **gammes**, puis sélectionnez le lien associé.  

    2. Cliquez sur l’action **Nouveau**, puis renseignez les champs comme indiqué dans le tableau suivant.  

        |Champ  |Valeur  |
        |---------|---------|
        |**N°** |1099|
        |**Description** |Nouveau chemin|
2. Créer les lignes de la gamme.

    1. Dans le raccourci **Lignes**, ajoutez une nouvelle ligne, puis renseignez les champs comme indiqué dans le tableau suivant.  

        |Champ  |Valeur  |
        |---------|---------|
        |**N° opération** |10|
        |**Type** |Centre de charge|
        |**N°** |100|
        |**Temps de préparation** |20|
        |**Temps d’exécution** |15|

    2. Ajoutez une nouvelle ligne, puis renseignez les champs comme indiqué dans le tableau suivant.  

        |Champ  |Valeur  |
        |---------|---------|
        |**N° opération** |20|
        |**Type** |Centre de charge|
        |**N°** |200|
        |**Temps de préparation** |30|
        |**Temps d’exécution** |5|
3. Certifiez la gamme.

    1.Dans le champ **Statut**, choisissez *Validé*.  

La nouvelle gamme est maintenant configurée.  

## <a name="see-also"></a>Voir aussi

[Introduction aux données de démonstration Contoso Coffee](../contoso-coffee-intro.md)  
