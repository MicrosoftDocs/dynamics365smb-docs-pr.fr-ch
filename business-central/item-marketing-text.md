---
title: Ajouter du texte marketing aux articles
description: Écrire du texte marketing pour les articles dans Business Central
author: jswymer
ms.author: jswymer
ms.reviewer: jswymer
ms.topic: how-to
ms.date: 03/22/2023
ms.custom: bap-template
---

# Ajouter du texte marketing aux articles

Pour tous les articles enregistrés dans Business Central, vous pouvez écrire du *texte marketing* sur l’article dans Business Central. Bien que le texte marketing soit une sorte de description, il est différent du champ **Description** de l’article. Le champ **Description** est généralement utilisé comme nom d’affichage concis pour identifier rapidement le produit. Le texte marketing, quant à lui, est un texte plus riche et descriptif. Son objectif est d’ajouter du contenu marketing et promotionnel, également appelé *copie*. Ce texte peut ensuite être publié avec l’article s’il est publié sur une boutique en ligne, comme Shopify.

Il existe deux manières de créer du texte marketing. Le moyen le plus simple de commencer est d’utiliser Copilot, qui vous suggère un texte généré par l’IA. L’autre façon est de repartir de zéro. 

## <a name=copilot></a>Créer un texte marketing généré par l’IA (version préliminaire) avec Copilot

[!INCLUDE[ai-preview](includes/ai-preview.md)]

Avec Copilot, vous obtenez rapidement une suggestion de texte automatiquement générée pour vous. Le texte généré par l’IA est adapté à l’article et constitue un bon point de départ. Le texte repose en partie sur les informations suivantes :

- Attributs définis pour l’article, par exemple, comme la description, la couleur, les dimensions, le matériau, etc.
- Préférences de style sélectionnables comme le ton de la voix, le format et la longueur.

Copilot est conçu pour vous faire gagner du temps et vous aider à rédiger des textes créatifs et attrayants qui reflètent votre marque et sont cohérents dans toute votre gamme de produits. Commencez par générer une suggestion, puis modifiez le texte suggéré si nécessaire.

### Conditions préalables

- Vous utilisez une [version préliminaire](ai-preview-getstarted.md) de Business Central qui est activée pour Copilot. L’activation de Copilot est effectuée par un administrateur. Pour plus d’informations, accédez à [Configurer le texte marketing d’un article basé sur l’IA avec Copilot](enable-ai.md).

- Consultez la [FAQ de Copilot](ai-faq.md) pour en savoir plus sur les suggestions de texte générées par l’IA de Copilot et sur la manière de les utiliser.

### Créer un premier brouillon avec Copilot

1. Dans Business Central, ouvrez l’article que vous souhaitez modifier. Pour ouvrir un article, procédez comme suit :

   1. Dans le coin supérieur droit, sélectionnez l’icône ![Ampoule qui ouvre la fonctionnalité de La fenêtre de recherche 22](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire") entrez **Articles**, puis sélectionnez le lien associé pour afficher une liste des articles disponibles.
   2. Pour ouvrir l’article, double-cliquez dessus ou sélectionnez sa valeur dans la colonne **N°** .

   Pour plus d’informations sur la création d’un article, accédez à [Enregistrer de nouveaux éléments](inventory-how-register-new-items.md).

   [![Affiche une fiche article avec volet Texte marketing](media/create-with-copilot.png)](media/create-with-copilot.png#lightbox)

2. À partir de la fiche article, il existe deux manières de commencer à rédiger un texte marketing avec Copilot :

   - Une façon consiste à utiliser le volet **Texte marketing** dans le Récapitulatif sur le côté droit de la page. Procédez comme suit :

      1. Dans le volet **Texte marketing** , sélectionnez **Créer avec Copilot**.

         Le texte suggéré apparaît dans le volet.
      2. Si vous souhaitez une autre suggestion, sélectionnez à nouveau **Créer avec Copilot**. Si vous n’aimez pas une suggestion, sélectionnez **Ignorer** pour effacer le volet.

         Vous pouvez répéter cette étape encore et encore jusqu’à ce que vous obteniez une suggestion qui vous semble être un bon point de départ. Mais gardez à l’esprit que la suggestion actuelle sera écrasée et que vous ne pourrez pas nécessairement la récupérer. Donc, si vous aimez la suggestion actuelle, passez à l’étape suivante. Vous aurez toujours la possibilité d’obtenir plus de suggestions, et même d’améliorer les suggestions, si vous le souhaitez plus tard.
      3. Sélectionnez **Revoir et enregistrer la suggestion** ou **Modifier** pour revoir, modifier et enregistrer le texte.

         Cette étape vous amène à la page **Créer avec Copilot**. Accédez à la section suivante.

         > [!NOTE]
         > Le texte ne sera pas enregistré tant que vous n’aurez pas effectué cette étape.

   - Une autre méthode consiste à sélectionner l’action **Texte marketing** en haut de la page de la fiche article pour accéder directement à la page **Créer avec Copilot**.

     Sur la page **Créer avec Copilot** , sélectionnez **Créer avec Copilot** pour obtenir la première suggestion. Vous pouvez ensuite obtenir plus de suggestions, essayer d’améliorer les suggestions que vous obtenez, modifier le texte, etc. Accédez à [Réviser, modifier et enregistrer](#review-edit-and-save-text) pour plus de détails.

   > [!TIP]
   > [D’où vient la suggestion ?](ai-faq.md#how-does-copilot-work-where-does-the-suggested-text-come-from)

### Vérifier, modifier et enregistrer le texte

Une fois que vous avez le premier brouillon, vous devez le réviser et apporter des modifications au texte pour le préparer à la publication. Ce travail est effectué à partir de la page **Créer avec Copilot**. Le texte actuel est affiché dans la zone **Texte marketing**. La page vous permet d’obtenir plus de suggestions, de modifier les préférences pour influencer les suggestions, d’apporter manuellement des modifications et de styliser le texte.

[![Affiche les fenêtres de création avec Copilot](media/create-with-copilot-window.png)](media/create-with-copilot-window.png#lightbox)

> [!IMPORTANT]
> Le texte généré par l’IA de Copilot n’est qu’une suggestion et il peut contenir des erreurs. Il nécessite une surveillance et un examen humains pour s’assurer qu’il est exact et approprié. Passez en revue tout texte suggéré et modifiez-le si nécessaire avant de l’enregistrer et de le publier pour une utilisation publique.

Utilisez les instructions suivantes pour finaliser et enregistrer le texte marketing.

1. Modifiez le texte directement dans la zone **Texte marketing**. Utilisez la barre d’outils en bas de la zone pour mettre en forme et styliser le texte, ajouter des liens, etc.
2. Pour obtenir une nouvelle suggestion, sélectionnez **Créer un brouillon**.
3. Si vous n’êtes pas satisfait des suggestions, améliorez les suggestions de texte en fonction de vos préférences.

   Sélectionnez **Plus de paramètres**, modifiez les options affichées sous **Choisissez comment Copilot crée des suggestions**, puis sélectionnez **Créez un brouillon** pour obtenir une nouvelle suggestion.

   Pour obtenir des instructions sur l’amélioration des suggestions, accédez à [Améliorer et personnaliser les suggestions de texte](#improve-and-tailor-text-suggestions).

4. Si vous souhaitez revenir à la suggestion précédente, sélectionnez **Annuler**.
5. Examinez attentivement le texte pour en vérifier l’exactitude et la pertinence, puis sélectionnez **OK** pour l’enregistrer.

### Améliorez et personnalisez les suggestions de texte

Vous pouvez effectuer quelques étapes pour améliorer les suggestions de texte et les ajuster en fonction de vos préférences personnelles ou de celles de votre entreprise.

1. Utilisez les options en haut de la page **Créer avec Copilot** pour influencer le résultat du texte généré par l’IA : 

   |Option|Description|
   |-|-|
   |Attributs à inclure|Utilisez cette option pour baser les suggestions, en partie, sur les attributs affectés à l’élément. Choisissez les attributs qui correspondent le mieux aux caractéristiques que vous souhaitez promouvoir. Plus vous incluez d’attributs pertinents, plus le résultat sera riche. Si vous pensez qu’il vous manque des attributs clés, ajoutez-en d’autres. Pour en savoir plus sur les attributs, consultez [Utiliser les attributs d’article](inventory-how-work-item-attributes.md). |
   |Mettre l’accent sur une qualité|Utilisez cette option pour choisir parmi une liste de qualités prédéfinies que vous souhaitez mettre en valeur dans le texte. Choisissez une qualité qui correspond le mieux au type d’article sur lequel vous écrivez. Les qualités ne correspondent pas directement aux attributs, à la description ou à la catégorie de l’article. Par exemple, la **Qualité** pourrait être un bon choix pour un vélo ou un bureau, tandis que la **Vitesse** conviendrait à un vélo, mais pas un bureau.|
   |Ton de la voix|Utilisez cette option pour influencer le type de mots, d’expressions et de ponctuation utilisés pour engager le public cible. Vous pouvez choisir parmi plusieurs tons de voix prédéfinis, allant de **Formel** (ce qui donne un ton plus professionnel parmi les choix) à **Créatif** (ce qui se traduit par un ton plus informel des choix). |
   |Format et longueur|Utilisez cette option pour contrôler la structure générale du texte, qui se compose de trois parties, couvertes par quatre options différentes : <ul><li>**Slogan** – Une expression accrocheuse ou une courte phrase qui identifie l’article ou la marque.</li><li>**Paragraphe** – Un seul paragraphe de texte fluide et détaillé, composé de plusieurs phrases complètes.</li><li>**Slogan + Paragraphe** – Un slogan suivi d’un paragraphe</li><li>**Brève** – Une phrase d’introduction, semblable à un slogan, suivie d’une liste à puces des principaux points d’intérêt.</li></ul> |

2. Améliorez le champ **Description** sur la fiche article.

   Le texte du champ **Description** sera utilisé tel quel à plusieurs endroits dans le texte suggéré. Il est donc important que la description décrive au mieux la manière dont vous souhaitez référencer l’élément dans le texte de commercialisation. 

3. Assurez-vous que le champ **Code catégorie article** sur la fiche article est défini sur une catégorie appropriée.

   Copilot trouvera des mots et des phrases liés à la catégorie et les intégrera au texte suggéré.

## Créer un texte marketing à partir de zéro

1. Dans Business Central, ouvrez l’article que vous souhaitez modifier comme suit :

    1. Dans le coin supérieur droit, sélectionnez l’icône ![Ampoule qui ouvre la fonctionnalité de La fenêtre de recherche 22](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire") entrez **Articles**, puis sélectionnez le lien associé pour afficher une liste des articles disponibles.
    2. Pour ouvrir l’article, double-cliquez dessus ou sélectionnez son numéro dans le champ **N°** .

2. Exécutez l’une des étapes suivantes :

   - Dans le volet **Texte marketing** dans le Récapitulatif sur le côté droit de la page, sélectionnez **Modifier**.
   - Sélectionnez l’action **Texte marketing**.
3. Modifiez le texte directement dans la zone **Texte marketing**. Utilisez la barre d’outils en bas de la zone pour mettre en forme et styliser le texte, ajouter des liens, etc.
4. Sélectionner **OK** quand vous avez terminé pour enregistrer le texte.

## Voir aussi

[Vue d’ensemble du texte marketing article optimisé par l’IA avec Copilot](ai-overview.md)  
[Configuration du texte marketing article optimisé par l’IA avec Copilot](enable-ai.md)  
[FAQ sur le texte marketing article optimisé par l’IA avec Copilot](ai-faq.md)  
[Enregistrer de nouveaux articles](inventory-how-register-new-items.md)  