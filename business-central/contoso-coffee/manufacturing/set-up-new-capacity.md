---
title: Configurer une nouvelle capacité
description: Procédure pas à pas pour apprendre à configurer un nouveau centre de charge avec un calendrier de capacité pour un seul quart de travail dans Business Central.
ms.date: 04/01/2022
ms.topic: article
ms.service: dynamics365-business-central
author: edupont04
ms.author: andreipa
---

# <a name="walkthrough-set-up-new-capacity"></a><a name="walkthrough-set-up-new-capacity"></a><a name="walkthrough-set-up-new-capacity"></a>Procédure pas-à-pas : Configurer une nouvelle capacité

Dans cet article, nous vous expliquons comment utiliser les données de démonstration de Contoso Coffee pour gérer les capacités.  

## <a name="scenario"></a><a name="scenario"></a><a name="scenario"></a>Scénario

Vous êtes planificateur de production chez Contoso Coffee. En réponse à des changements dans l’atelier, vous devez créer un nouveau centre de charge, un département de test. Le nouveau centre de charge dispose d’un poste de charge pour effectuer des tests. Le nouveau poste doit avoir un calendrier de capacité pour un seul quart de travail de 8 h 00 à 16 h 00, du lundi au vendredi.  

## <a name="steps"></a><a name="steps"></a><a name="steps"></a>Étapes

1. Configurez le centre de charge.

    1. Sélectionnez ![l’icône en forme d’Ampoule qui ouvre la fenêtre de recherche](../../media/ui-search/search_small.png "Dites-moi ce que vous voulez faire"), entrez **Centres de charge**, puis choisissez le lien associé.  

    2. Cliquez sur l’action **Nouveau**, puis renseignez les champs comme indiqué dans le tableau suivant.  

        |Champ  |Valeur  |
        |---------|---------|
        |**N°** |700|
        |**Nom** |Département de test|
        |**Code groupe centres de charge** |1, Département production|
        |**Coût unitaire direct**|3,25|
        |**Calcul du coût unitaire**|Heure|
        |**Méthode consommation**|Manuel|
        |**Groupe compta. produit**|SANS TVA</br></br>Notez que cette sélection dépend de la configuration de la comptabilité et de votre pays.|
        |**Code unité** |MINUTES|
        |**Capacité** |1|
        |**Rendement** |90|
        |**Code calendrier usine** |1|

        Dans le champ **Code calendrier usine**, 1 désigne une équipe du lundi au vendredi.

    3. Fermez la fiche de centre de charge.

2. Configurez le poste de charge.

    1. Sélectionnez ![l’icône en forme d’Ampoule qui ouvre la fenêtre de recherche](../../media/ui-search/search_small.png "Dites-moi ce que vous voulez faire"), entrez **postes de charge**, puis choisissez le lien associé.  

    2. Cliquez sur l’action **Nouveau**, puis renseignez les champs comme indiqué dans le tableau suivant.  

        |Champ  |Valeur  |
        |---------|---------|
        |**N°** |760|
        |**Nom** |Test|
        |**N° centre de charge** |700, département des tests|
        |**Coût unitaire direct**|3,25|
        |**Méthode consommation**|Manuel|
        |**Groupe compta. produit**|SANS TVA</br></br>Notez que cette sélection dépend de la configuration de la comptabilité et de votre pays.|
        |**Capacité** |1|
        |**Rendement** |90|
    3. Développez le raccourci **Paramètres gamme**, puis, dans le champ **Temps de préparation**, entrez *10*.  

3. Calculez le calendrier de capacité du poste de charge.  

    1. Sélectionnez l’action **Calendrier**.  

    2. Dans la page **Calendrier poste de charge**, sur le raccourci **Options matrice**, définissez le champ **Afficher par** sur *Mois*.  

    3. Choisissez l’action **Afficher matrice**.  

    4. Sur la page **Matrice Calendrier poste de charge**, choisissez l’action **Calculer**.  

    5. Dans la page **Calculer calendrier poste ch.**, sur le raccourci **Options**, définissez le champ **Date de début** sur *1er janvier*.  

    6. Définissez le champ **Date de fin** sur 31 décembre.  

    7. Sur le raccourci **Poste de charge**, dans le champ à filtrer **N°**. sélectionnez *760, Tests*.  

    8. Cliquez sur le bouton **OK**. Une fois le traitement par lots terminé, vous revenez sur la page **Matrice Calendrier poste de charge**.  

    9. Sélectionnez l’action **Actualiser**.  

    10. Sur la ligne du Poste de charge 760, Tests, accédez à la valeur de la colonne de janvier.  

Sur la page **Écritures calendrier**, les écritures de capacité journalière du champ **Capacité (totale)** sont de 480 minutes. Cela correspond à un quart de travail de huit heures pour chaque journée de travail. De plus , le champ **Capacité (réelle)** indique 432 minutes. Cela reflète le taux d’efficacité de 90 % que vous avez attribué au poste de charge.  

## <a name="see-also"></a><a name="see-also"></a><a name="see-also"></a>Voir aussi

[Introduction aux données de démonstration Contoso Coffee](../contoso-coffee-intro.md)  
