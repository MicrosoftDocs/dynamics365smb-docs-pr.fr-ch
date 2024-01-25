---
title: Ajouter du texte marketing aux articles
description: Écrire du texte marketing pour les articles dans Business Central
author: jswymer
ms.author: jswymer
ms.reviewer: jswymer
ms.topic: how-to
ms.date: 12/13/2023
ms.custom: bap-template
ms.collection:
  - bap-ai-copilot
---

# <a name="add-marketing-text-to-items"></a>Ajouter du texte marketing aux articles

Pour tous les articles enregistrés dans Business Central, vous pouvez écrire du *texte marketing* sur l’article dans Business Central. Bien que le texte marketing soit une sorte de description, il est différent du champ **Description** d’un article. Le champ **Description** est généralement utilisé comme nom d’affichage concis pour identifier rapidement le produit. Le texte marketing, quant à lui, est un texte plus riche et descriptif. Son objectif est d’ajouter du contenu marketing et promotionnel, également appelé *copie*. Ce texte peut ensuite être publié avec l’article s’il est publié sur une boutique en ligne, comme Shopify, ou collé dans des e-mails ou d’autres communications avec vos clients.

Il existe deux manières de créer du texte marketing. Le moyen le plus simple de commencer est d’utiliser Copilot, qui vous suggère un texte généré par l’IA. L’autre façon est de repartir de zéro. 

## <a name="get-marketing-text-suggestions-with-copilot"></a><a name=copilot></a>Obtenir des suggestions de textes marketing avec Copilot

Avec Copilot, vous obtenez rapidement une suggestion de texte automatiquement générée pour vous. Le texte généré par l’IA est adapté à l’article et constitue un bon point de départ. Le texte repose en partie sur les informations suivantes :

- Attributs définis pour l’article, par exemple, comme la description, la couleur, les dimensions, le matériau, etc. [En savoir plus sur les attributs d’article](inventory-how-work-item-attributes.md).
- Le champ **description** de l’article.
- La catégorie article. [En savoir plus sur Classer les articles](inventory-how-categorize-items.md).
- Préférences de style sélectionnables comme le ton de la voix, le format et la longueur.

Copilot est conçu pour vous faire gagner du temps et vous aider à rédiger des textes créatifs et attrayants qui reflètent votre marque et sont cohérents dans toute votre gamme de produits. Commencez par générer une suggestion, puis modifiez le texte suggéré si nécessaire.

### <a name="prerequisites"></a>Conditions préalables

- La fonctionnalité de suggestions de texte marketing est activée et activée sur votre environnement. Cette tâche est généralement effectuée par un administrateur. Pour plus d’informations, accédez à [Configurer Copilot et les capacités IA](enable-ai.md).
- Vous utilisez l’une des langues actuellement prises en charge par les suggestions de texte marketing.

  [!INCLUDE[copilot-supported-languages.md](includes/copilot-supported-languages.md)]

  Pour modifier la langue, dans le coin supérieur droit, sélectionnez l’icône **Paramètres** ![Paramètres](media/ui-experience/settings_icon_small.png "Icône Paramètres du tableau de bord") > **Mes paramètres** > **Langue**. Pour plus d’informations, consultez [Modifier les paramètres de base](ui-change-basic-settings.md#language).
- Consultez la [FAQ sur les suggestions de textes marketing](faqs-marketing-text.md) pour découvrir comment l’IA est appliquée.

### <a name="create-first-draft-with-copilot"></a>Créer un premier brouillon avec Copilot

Procédez comme suit pour ajouter un texte marketing à un article existant. Pour savoir comment créer un article, accédez à [Enregistrer de nouveaux articles](inventory-how-register-new-items.md).

1. Dans Business Central, ouvrez l’article que vous souhaitez modifier en procédant suit :

   - Dans le coin supérieur droit, sélectionnez l’icône ![Ampoule qui ouvre la fonctionnalité de La fenêtre de recherche 22](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire") entrez **Articles**, puis sélectionnez le lien associé pour afficher une liste des articles disponibles.

   - Double-cliquez sur l’article ou sélectionnez sa valeur dans la colonne **N°** .

   [![Affiche une fiche article avec volet Texte marketing](media/create-with-copilot.svg)](media/create-with-copilot.svg#lightbox)

2. À partir de la fiche article, il existe deux manières de commencer à rédiger un texte marketing avec Copilot. Exécutez l’une des étapes suivantes :

   - Dans le volet **Texte marketing** dans le volet Récapitulatif sur le côté droit de la page, sélectionnez **Rédiger avec Copilot**. 
   
     Copilot commence à rédiger le texte marketing. 

   - En haut de la page, sélectionnez l’action **Texte marketing** , puis sélectionnez **Rédiger avec Copilot** sur la fenêtre **Modifier le texte marketing**.  La fenêtre **Rédiger un texte marketing avec Copilot** s’affiche et répertorie tous les attributs disponibles pour l’article.
   
     ![Affiche la fenêtre Modifier le texte marketing](media/marketing-text-copilot-attributes.svg)

     Sélectionnez les attributs sur lesquels vous souhaitez que Copilot base les suggestions, puis sélectionnez **Générer**. Vous pourrez modifier les attributs sélectionnés et d’autres options ultérieurement. Copilot commence à rédiger le texte marketing. 
     
3. Quand Copilot termine le brouillon, le texte s’affiche dans la fenêtre de l’éditeur Copilot pour révision et modification. 

   [![Affiche les fenêtres de création avec Copilot](media/create-with-copilot-window.svg)](media/create-with-copilot-window.svg#lightbox)

   Vous pouvez désormais obtenir plus de suggestions, essayer d’améliorer les suggestions que vous obtenez, modifier le texte, etc. Accédez à [Réviser, modifier et enregistrer](#review-edit-and-save-text) pour plus de détails.


### <a name="review-edit-and-save-text"></a>Vérifier, modifier et enregistrer le texte

Une fois que vous avez le premier brouillon, vous devez le réviser et apporter des modifications au texte pour le préparer à la publication. Ce travail se fait depuis l’éditeur Copilot, qui vous permet d’obtenir plus de suggestions, de modifier les préférences pour influencer les suggestions, d’apporter manuellement des modifications et de styliser le texte.

> [!IMPORTANT]
> Le texte généré par l’IA de Copilot n’est qu’une suggestion et il peut contenir des erreurs. Il nécessite une surveillance et un examen humains pour s’assurer qu’il est exact et approprié. Passez en revue tout texte suggéré et modifiez-le si nécessaire avant de l’enregistrer et de le publier pour une utilisation publique.

Utilisez les instructions suivantes pour finaliser et enregistrer le texte marketing.

1. Modifiez le texte directement dans la zone de texte. Utilisez la barre d’outils en bas de la zone pour mettre en forme et styliser le texte, ajouter des liens, etc.
2. Pour obtenir une nouvelle suggestion, sélectionnez **Regénérer**.
3. Si vous n’êtes pas satisfait des suggestions, améliorez les suggestions de texte à l’aide des options de préférence **Ton**, **Format**, et **Accent**.

   <!--Select **More Settings**, change the options that are shown under **Choose how Copilot creates suggestions**, then select **Create draft** to get a new suggestion.-->

   Pour obtenir des instructions sur l’amélioration des suggestions, accédez à [Améliorer et personnaliser les suggestions de texte](#improve-and-tailor-text-suggestions).

4. Pour parcourir les suggestions, utilisez les liens précédent et suivant en haut de la page (*X* **sur** *Y*). <!-- or select the **...** (More formatting options) along the bottom of the window, then select **Undo**. Select **Redo** to go back.-->
5. Examinez attentivement le texte pour en vérifier l’exactitude et la pertinence :

   - Si vous souhaitez enregistrer le texte, sélectionnez **Conserver**. 
   - Si vous ne souhaitez pas enregistrer, sélectionnez le bouton Ignorer (corbeille) ![Affiche l’icône de la corbeille pour supprimer toutes les propositions Copilot pour le rapprochement des comptes bancaires](media/copilot-delete-trash-can.png).

### <a name="improve-and-tailor-text-suggestions"></a>Améliorez et personnalisez les suggestions de texte

Vous pouvez effectuer quelques étapes pour améliorer les suggestions de texte et les ajuster en fonction de vos préférences personnelles ou de celles de votre entreprise.

1. Modifiez les attributs d’article utilisés par Copilot.

   Les suggestions Copilot sont basées en partie sur les attributs affectés à l’article. Pour afficher les attributs disponibles et les paramètres actuels, sélectionnez l’icône Modifier ![Affiche l’icône de modification dans la fenêtre Copilot pour modifier les attributs](media/edit-pencil.png) dans le coin supérieur gauche. Sur la page **Attributs d’article**, choisissez les attributs qui correspondent le mieux aux caractéristiques que vous souhaitez promouvoir. Plus vous incluez d’attributs pertinents, plus le résultat est riche. Si vous pensez qu’il vous manque des attributs clés, ajoutez-en d’autres. Pour en savoir plus sur les attributs, consultez [Utiliser les attributs d’article](inventory-how-work-item-attributes.md).
1. Modifiez vos paramètres de préférences pour les options **Ton**, **Format** et **Accent**.

   |Option|Désignation|
   |-|-|
   |Ton |Utilisez cette option pour influencer le type de mots, d’expressions et de ponctuation utilisés pour engager le public cible. Vous pouvez choisir parmi plusieurs tons de voix prédéfinis, allant de **Formel** (ce qui donne un ton professionnel) à **Créatif** (ce qui se traduit par un ton informel). |
   |Format et longueur|Utilisez cette option pour contrôler la structure générale du texte, qui se compose de trois parties, couvertes par quatre options différentes : <ul><li>**Slogan** – Une expression accrocheuse ou une courte phrase qui identifie l’article ou la marque.</li><li>**Paragraphe** – Un seul paragraphe de texte fluide et détaillé, composé de plusieurs phrases complètes.</li><li>**Slogan + Paragraphe** – Un slogan suivi d’un paragraphe</li><li>**Brève** – Une phrase d’introduction, semblable à un slogan, suivie d’une liste à puces des principaux points d’intérêt.</li></ul> |
   |Accentuation|Utilisez cette option pour choisir parmi une liste de qualités prédéfinies que vous souhaitez mettre en valeur dans le texte. Choisissez une qualité qui correspond le mieux au type d’article sur lequel vous écrivez. Les qualités ne correspondent pas directement aux attributs, à la description ou à la catégorie de l’article. Par exemple, la **Qualité** pourrait être un bon choix pour un vélo ou un bureau, tandis que la **Vitesse** conviendrait à un vélo, mais pas un bureau.|

1. Améliorez le champ **Description** sur la fiche article.

   Le texte du champ **Description** est utilisé tel quel à plusieurs endroits dans le texte suggéré. Il est donc important que la description décrive au mieux la manière dont vous souhaitez référencer l’élément dans le texte de commercialisation. 

1. Assurez-vous que le champ **Code catégorie article** sur la fiche article est défini sur une catégorie appropriée.

   Copilot trouve des mots et des phrases liés à la catégorie et les intégrera au texte suggéré.

### <a name="working-with-multiple-languages"></a>Travailler avec plusieurs Langues

Le texte est toujours généré dans la langue définie par vos [paramètres utilisateur](ui-change-basic-settings.md#language). Si votre organisation exploite et saisit des données dans Business Central dans une langue différente, ou si Business Central est connecté à votre boutique en ligne, par exemple avec Shopify, cela peut entraîner la publication d’un contenu qui ne correspond pas à un contenu marketing similaire.

## <a name="create-text-from-scratch"></a>Créer un texte à partir de zéro

1. Dans Business Central, ouvrez l’article que vous souhaitez modifier comme suit :

    1. Dans le coin supérieur droit, sélectionnez l’icône ![Ampoule qui ouvre la fonctionnalité de La fenêtre de recherche 22](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire") entrez **Articles**, puis sélectionnez le lien associé pour afficher une liste des articles disponibles.
    2. Pour ouvrir l’article, double-cliquez dessus ou sélectionnez son numéro dans le champ **N°** .

2. Exécutez l’une des étapes suivantes :

   - Dans le volet **Texte marketing** dans le Récapitulatif sur le côté droit de la page, sélectionnez **Modifier**.
   - Sélectionnez l’action **Texte marketing**.
3. Modifiez le texte directement dans la zone **Texte marketing**. Utilisez la barre d’outils en bas de la zone pour mettre en forme et styliser le texte, ajouter des liens, etc.
4. Sélectionner **OK** quand vous avez terminé pour enregistrer le texte.

## <a name="see-also"></a>Voir aussi

[Vue d’ensemble des suggestions de texte marketing](ai-overview.md)  
[Résoudre les problèmes des fonctionnalités de Copilot et d’IA](ai-copilot-troubleshooting.md)  
[FAQ sur les suggestions de texte marketing pour les articles](faqs-marketing-text.md)  
[Configuration des fonctionnalités de Copilot et d’IA](enable-ai.md)  
[Enregistrement des nouveaux articles](inventory-how-register-new-items.md)  
