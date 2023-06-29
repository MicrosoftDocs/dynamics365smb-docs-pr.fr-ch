---
title: Variantes
description: Procédure pas à pas pour savoir comment mettre à jour la prévision de la demande pour chaque variante d’un produit dans Business Central.
ms.date: 04/01/2022
ms.topic: article
ms.service: dynamics365-business-central
author: edupont04
ms.author: andreipa
---

# <a name="walkthrough-variants"></a><a name="walkthrough-variants"></a>Procédure pas à pas : variantes

Dans cet article, nous vous expliquons comment utiliser les données de démonstration de Contoso Coffee pour en savoir plus sur les variantes.

## <a name="scenario"></a><a name="scenario"></a>Scénario

Vous êtes planificateur de production chez Contoso Coffee. Vous devez mettre à jour la prévision de la demande pour chaque variante de l’article SP-SCM1006, AutoDripLite. Comme les couleurs sont différentes, vous devez vous assurer que la bonne nomenclature (BOM) est utilisée pour chaque variante. Exécutez la feuille planning pour calculer l’approvisionnement.  

## <a name="steps"></a><a name="steps"></a>Étapes

1. Configurez les unités de gestion des stocks pour l’article SP-SCM1006, AutoDripLite. Attribuez une nomenclature pour SKU avec les variantes ROUGE et BLANC.

    1. Sélectionnez ![l’icône en forme d’Ampoule qui ouvre la fenêtre de recherche](../../media/ui-search/search_small.png "Dites-moi ce que vous voulez faire"), entrez *articles*, puis choisissez le lien associé.  

    2. Ouvrez l’élément **SP-SCM1006, AutoDripLite**.

    3. Choisissez l’action **Créer point de stock**.  

    4. Définissez le champ **Créer par** sur *Magasin et variante*.

    5. Définissez un filtre pour le magasin sur *Nord*, puis cliquez sur le bouton **OK**.

    6. Choisissez l’action **Unités de gestion des stocks**.  

    7. Mettez à jour les nomenclatures de production pour les unités de stockage suivantes :

        1. ROUGE sur NORD, définissez SP-SCM1006-RED  

        2. BLANC sur NORD, définissez SP-SCM1006-WHITE  

        3. Gardez le numéro de nomenclature de production vide pour NOIR sur NORD  

2. Mettez à jour les paramètres production et respectez les prévisions de demande sur les magasins et les variantes.  

    1. Sélectionnez ![l’icône en forme d’Ampoule qui ouvre la fenêtre de recherche](../../media/ui-search/search_small.png "Dites-moi ce que vous voulez faire"), saisissez *Paramètres production*, puis choisissez le lien associé.  

    2. Activez le champ **Prévision sur magasin**.

    3. Activez le champ **Utiliser prévisions sur variantes**.

    4. Fermez la fenêtre **Paramètres production**.

3. Créez une prévision de la demande mensuelle, *AUTODRIP*. Filtrez-la par l’article SP-SCM1006 et le magasin NORD. Définissez la demande pour Mai pour chaque variante. 

    1. Sélectionnez ![l’icône en forme d’Ampoule qui ouvre la fenêtre de recherche](../../media/ui-search/search_small.png "Dites-moi ce que vous voulez faire"), entrez *Prévision de la demande*, puis sélectionnez le lien associé.

    2. Créez une prévision de la demande et nommez-la *AUTODRIP*.

    3. Choisissez l’action **Modifier la prévision de la demande**.

    4. Dans le champ **Afficher par**, sélectionnez *Mois*.

    5. Dans le champ **Filtre article**, sélectionnez *SP-SCM1006*

    6. Activez le champ **Prévision sur magasin**.

    7. Dans le champ **Filtre magasin**, sélectionnez *NORD*

    8. Activez le champ **Utiliser prévisions sur variantes**.

    9. Pour chaque ligne, les valeurs sont mises à jour dans la colonne Mai

        1. ROUGE sur NORD, défini sur 100

        2. BLANC sur NORD, défini sur 200

        3. NOIR sur NORD, défini sur 300

    10. Fermer les fenêtres de prévision de la demande

4. Exécutez le plan MPS en mai pour les prévisions de demande créées. Examinez les composants pour vérifier que la couleur de l’article correspond à la variante.

    1. Sélectionnez ![l’icône en forme d’Ampoule qui ouvre la fenêtre de recherche](../../media/ui-search/search_small.png "Dites-moi ce que vous voulez faire"), entrez *Feuille planning*, puis choisissez le lien associé.

    2. Choisissez l’action **Calculer planning régénératif**.

    3. Activez le champ **MPS**.

    4. Désactivez le champ **MPS**.

    5. Dans le **Date de début**, sélectionnez *1er mai*

    6. Dans le **Date de fin**, sélectionnez *31 mai*

    7. Dans le champ **Utiliser prévisions**, sélectionnez *AUTODRIP*

    8. Sélectionnez l’action **OK**.

    9. Pour chaque ligne créée, choisissez l’action **Composants** et vérifiez quelle couleur est utilisée.  

## <a name="see-also"></a><a name="see-also"></a>Voir aussi

[Introduction aux données de démonstration Contoso Coffee](../contoso-coffee-intro.md)  
