---
title: Utiliser des profils pour classer les contacts
description: Découvrez comment configurer des questionnaires de profil pour aider à classer les profils de vos contacts professionnels.
author: edupont04
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 'contacts, profiles'
ms.search.form: '5109, 5110'
ms.author: edupont
ms.date: 05/20/2022
---

# Utiliser des questionnaires profil pour classer les contacts professionnels

Vous pouvez évaluer un prospect afin d’identifier les prospects idéaux sur lesquels axer votre compagne de vente. Vous pouvez configurer des questionnaires profil à utiliser au moment d’entrer des informations sur les profils de vos contacts. Dans chaque questionnaire, vous pouvez configurer les questions à poser à vos contacts. De cette façon, vous pouvez regrouper les contacts afin que vos campagnes soient plus susceptibles de cibler les personnes appropriées en fonction des critères que vous définissez avec les questionnaires.  

Avec les questionnaires adaptés, vous pouvez évaluer vos prospects et les regrouper en catégories. Vous pouvez utiliser des questions et réponses existantes, et les combiner avec de nouvelles pour obtenir la base de votre évaluation. Chaque réponse de l’évaluation correspond à un nombre de points et, selon la plage que vous définissez pour les catégories (*Valeur début* et *Valeur fin*), le système d’évaluation place vos contacts dans les catégories définies. Par exemple, clients *ABC*, fournisseurs à *fidélité élevée/faible* ou prospects *Platinum/Gold/Silver*.  

Vous pouvez également exécuter le questionnaire pour répondre automatiquement à certaines de ces questions en fonction des données contact, client ou fournisseur.  

## Pour ajouter un questionnaire profil

1. Sélectionnez l’icône ![Ampoule qui ouvre la fonction Tell Me.](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire") entrez **Configuration du questionnaire**, puis sélectionnez le lien associé.  
2. Sélectionnez l’action **Nouveau**.  
3. Renseignez les champs selon vos besoins. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]  

## Pour ajouter des questions à un questionnaire profil

1. Choisissez le questionnaire profil approprié, puis sélectionnez l’action **Modifier paramètres questionnaire**.  
2. Sur la première ligne vide, dans le champ **Type**, choisissez **Question**, puis tapez la question dans le champ **Désignation**. Renseignez les autres champs sur cette ligne.  

    Ajoutez éventuellement des détails à la question.

    1. Choisissez la ligne avec la question, puis choisissez le menu **Ligne**, puis choisissez **Questionnaire**.  

    2. Sur le raccourci **Méthode classification** de la fenêtre **Questionnaire profil**, sélectionnez le champ **Classification contact auto**.  

    3. Dans le champ **Champ class. contact**, sélectionnez l’option **Évaluation**.  

    4. Renseignez le champ **% min. questions traitées**. Par défaut, il s’agit de **0**.  

        Ceci indique le nombre de questions (sous forme de pourcentage) devant obtenir une réponse pour que cette évaluation soit calculée.

    5. Sous l’onglet **Actions**, dans le groupe **Page**, choisissez **Points réponse**. Indiquez le nombre de points à attribuer à chaque réponse répertoriée dans la page **Points réponse**.

        Si vous voulez avoir un aperçu des points que vous avez donnés pour chaque réponse, choisissez l’action **Points de réponse**.

    6. Pour exécuter une mise à jour, revenez à la page **Paramètres quest. profil**. Dans le menu **Actions** , dans le groupe **Fonctions**, choisissez **Mettre à jour la classification**.

    Sur la page **Paramètres quest. profil**, le nombre de contacts répondant à ces critères est affiché dans le champ **Nbre contacts**, ainsi que sur la **Fiche contact** de chaque contact.

3. Sur la ligne vide suivante, dans le champ **Type**, choisissez **Réponse**, puis tapez la réponse dans le champ **Désignation**.  
4. Dans le champ **Priorité**, sélectionnez la priorité. Dans les champs **Valeur début** et **Valeur fin**, définissez une plage de points. Les contacts obtenant un nombre de points compris dans la plage définie recevront la réponse.  

Répétez ces étapes pour entrer toutes les questions et réponses du questionnaire profil.

Après avoir créé un questionnaire, vous pouvez l’utiliser pour évaluer et classer vos contacts. Vous pouvez également définir des questions qui sont évaluées automatiquement en fonction des informations de la fiche contact.  

> [!NOTE]
> Si vous entrez une question dont la réponse est automatique, choisissez **Ligne**, puis **Questionnaire** pour entrer les critères de réponse automatique.

## Appliquer des questionnaires aux contacts

Vous pouvez appliquer vos questionnaires aux contacts manuellement. Il vous suffit d’ouvrir la fiche contact appropriée, puis de choisir l’action **Profils**. Ensuite, une fois que vous avez appliqué les questionnaires que vous souhaitez appliquer, vous pouvez commencer à utiliser les catégories dans vos campagnes.  

## Classification automatique des contacts

Vous pouvez configurer le programme pour qu’il classe automatiquement les contacts en fonction des données client, fournisseur et contact. Pour cela, configurez des questions profil à réponse automatique sur la page **Paramètres questionnaires profil**.  

> [!NOTE]
> Vous ne pouvez affecter une classification basée sur les données contact qu’aux contacts enregistrés en tant que clients. De même, seuls les contacts enregistrés en tant que fournisseurs peuvent se voir affecter une classification basée sur les données fournisseur. La classification automatique n’est pas mise à jour automatiquement. Par conséquent, vous pouvez être amené à mettre à jour les questionnaires profil après avoir mis à jour les données client, fournisseur ou contact dont ils dépendent.  

Une fois que vous avez configuré les questions profil à réponse automatique, affectez à un contact le questionnaire profil qui les contient. [!INCLUDE[prod_short](includes/prod_short.md)] répond ensuite automatiquement aux questions.  

## Exemple :

Vous pouvez classer vos contacts en fonction du montant de leurs achats :

|Réponse|Doc. lettrage|
|--- |--- |
|A|contacts ayant effectué des achats pour une somme supérieure ou égale à 500 000 DS|
|B|contacts ayant effectué des achats pour une somme comprise entre 100 000 et 499 999 DS|
|C|contacts ayant effectué des achats pour une somme inférieure ou égale à 99 999 DS|

Pour cela, renseignez la page **Paramètres questionnaires profil** comme suit :

| Type     | Description        | Classification automatique     | Valeur début | Valeur fin |
|----------|--------------------|------------------------------|------------|----------|
| Question | Classification ABC | Cochez la ligne appropriée. |            |          |
| Réponse   | A                  |                              | 500,000    |          |
| Réponse   | B                  |                              | 100,000    | 499,999  |
| Réponse   | C                  |                              |            | 99,999   |

Renseignez ensuite la page **Questionnaire profil** comme suit :

| Champ                         | Valeur         |
|-------------------------------|---------------|
| Champ de classification des clients | Ventes (DS)   |
| Méthode classification         | Valeur définie |

Lorsque vous affectez le questionnaire profil contenant cette question à un contact, l’application insère automatiquement la réponse correspondante dans les lignes profil de la fiche contact.

## Voir aussi

[Création de contacts](marketing-create-contact-companies.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]