---
title: Créer une nomenclature de production et une version de nomenclature
description: Procédure pas à pas pour apprendre à ajouter une autre cafetière à la gamme de produits de Contoso Coffee dans Business Central.
ms.date: 04/01/2022
ms.topic: article
ms.service: dynamics365-business-central
author: edupont04
ms.author: andreipa
---
# <a name="walkthrough-create-a-new-production-bom-and-bom-version"></a>Procédure pas à pas : Créer une nomenclature de production et une version de nomenclature

Dans cet article, nous vous expliquons comment utiliser les données de démonstration Contoso Coffee pour les nomenclatures dans les processus de production.  

## <a name="scenario"></a>Scénario

Contoso Coffee a décidé d’ajouter une autre cafetière à sa gamme de produits : **SP-SCM1008 Airpot Lite**. Cette cafetière est identique à l’article existant **SP-SCM1009 Airpot**, sauf qu’elle ne comporte pas la plaque chauffante, **SP-BOM1104**. Dans une étape distincte, le voyant marche/arrêt, **SP-BOM1106** est supprimé pour une version de la nomenclature Airpot Lite.

Oscar, l’ingénieur de processus chez Contoso Coffee, doit configurer une nouvelle nomenclature de production pour définir les exigences initiales en matière de composants pour le modèle Airpot Lite. Oscar doit ensuite mettre en place une nouvelle version de la nomenclature, avec une date de début au 1er juillet, pour s’aligner sur les plans ultérieurs de lancement d’une autre édition.

## <a name="steps"></a>Étapes

1. Créez une nomenclature de production pour le modèle Airpot Lite.

    1. Sélectionnez ![l’icône en forme d’Ampoule qui ouvre la fenêtre de recherche](../../media/ui-search/search_small.png "Dites-moi ce que vous voulez faire"), saisissez **Nomenclature de production**, puis choisissez le lien associé.  

    2. Cliquez sur l’action **Nouveau**, puis renseignez les champs comme indiqué dans le tableau suivant.  

        |Champ  |Valeur  |
        |---------|---------|
        |**N°** |SP-SCM1008|
        |**Description** |Airpot Lite|
        |**Code unité**|PCS  |

2. Copiez les composants de la nomenclature à partir de la nomenclature de production **SP-SCM1009**.

    1. Choisissez l’action **Copier nomenclature**.

    2. Sur la page **Nomenclatures de production**, choisissez la ligne pour **SP-SCM1009, Airpot**, puis choisissez le bouton **OK**.

3. Modifiez les composants de la nouvelle nomenclature de production comme décrit dans le scénario.

    1. Dans le raccourci **Lignes**, sélectionnez la ligne de l’article **SP-BOM1104**, puis choisissez l’action **Supprimer la ligne**.  

4. Validez la nouvelle nomenclature.  

    1. Dans le champ **Statut**, choisissez *Validé*.  

5. Créez une version de nomenclature de production pour le modèle Airpot Lite.

    1. Sélectionnez l’action **Versions**.

    2. Sur la page **Liste versions nomenclature**, choisissez l’action **Nouveau**, puis renseignez les champs comme indiqué dans le tableau suivant.  

        |Champ  |Valeur  |
        |---------|---------|
        |**Code versions** |02|
        |**Description** |Airpot Lite, v2|
        |**Code unité**|PCS  |  
        |**Date début**|1er juillet  |  

6. Copiez les lignes composant de la nomenclature de production dans la nouvelle version de la nomenclature.

    1. Choisissez l’action **Copier nomenclature**, puis choisissez le bouton **Oui** pour copier les composants de la nomenclature de production d’origine.

7. Supprimez l’article **SP-BOM1106, Voyant marche/arrêt** des composants de la version.

8. Validez la nouvelle version de la nomenclature.

    1. Dans le champ **Statut**, choisissez *Validé*.  

    2. Fermez la version de la nomenclature.

La nouvelle cafetière est désormais configurée en tant que nomenclature de production avec une version.  

## <a name="see-also"></a>Voir aussi

[Introduction aux données de démonstration Contoso Coffee](../contoso-coffee-intro.md)  
