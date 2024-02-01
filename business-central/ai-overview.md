---
title: Suggestions de textes marketing avec vue d’ensemble de Copilot
description: Obtenez un aperçu des capacités de génération de contenu IA dans Business Central.
author: jswymer
ms.author: jswymer
ms.reviewer: jswymer
ms.topic: overview
ms.date: 10/29/2023
ms.custom: bap-template
ms.collection:
  - bap-ai-copilot
---
# <a name="marketing-text-suggestions-with-copilot-overview"></a>Suggestions de textes marketing avec vue d’ensemble de Copilot

<!--[!INCLUDE[ai-preview](includes/ai-preview.md)]-->

Cet article donne un aperçu de la capacité alimentée par l’IA fournie par Copilot dans Business Central.

## <a name="what-is-ai-powered-item-marketing-text-with-copilot"></a>Qu’est-ce que le Texte marketing article optimisé par l’IA avec Copilot

Copilot fournit une assistance à la rédaction basée sur l’IA pour les utilisateurs de Business Central responsables de la rédaction de textes marketing (descriptions de produits) sur des articles vendus dans des boutiques en ligne, comme Shopify. D’un simple clic, Copilot génère un texte engageant et créatif et met en évidence les attributs clés de l’élément spécifique. Avec un peu de révision et d’édition, il est prêt à être publié.

Copilot utilise le [service Microsoft Azure OpenAI](/azure/cognitive-services/openai/overview) pour accéder à des modèles de langage qui reconnaissent, prédisent et génèrent du texte basé sur des ensembles de données entraînés.

<br><br>  

> [!Video https://www.microsoft.com/en-us/videoplayer/embed/RWZdAr]

*La vidéo ne reflète pas exactement le fonctionnement actuel de la fonctionnalité ou son apparence dans le produit. La fonctionnalité a changé depuis la production de la vidéo. Mais cela vous donne une idée générale de la fonctionnalité et de ce que vous pouvez en faire.*
  
## <a name="where-its-used"></a>Emplacement d’utilisation

Copilot est disponible sur les fiches articles dans Business Central. Dans Business Central, les articles sont comme des produits dans d’autres applications et magasins. Chaque article peut être géré à partir d’une carte où vous entrez des détails sur l’article, comme ses dimensions, son coût ou sa photo. Cette carte comprend également une zone pour saisir du texte marketing. Ce texte marketing peut être publié sur votre boutique en ligne pour promouvoir l’article. C’est là qu’intervient Copilot. En sélectionnant simplement l’action **Rédiger avec Copilot** sur la fiche article, Copilot générera pour vous un brouillon de texte intelligent. Une fois que vous avez obtenu le premier brouillon, vous pouvez exécuter Copilot encore et encore jusqu’à ce que vous obteniez un brouillon que vous aimez. Quand vous avez une suggestion que vous aimez, vous la révisez et la modifiez pour plus de précision, puis enregistrez-la.

Si Business Central est configuré pour se connecter à votre boutique en ligne sur Shopify, vous pouvez pousser ce texte encore plus loin en le publiant avec l’article directement dans votre boutique en sélectionnant **Ajouter à Shopify**.

## <a name="why-and-how-to-use-it"></a>Pourquoi et comment l’utiliser

Le texte généré par l’IA peut vous aider à accélérer la mise sur le marché des produits dans les boutiques en ligne, en limitant le temps consacré à la rédaction. Certains avantages principaux comprennent :

- Aide les utilisateurs à surmonter le blocage de l’écrivain en les incitant à démarrer avec un brouillon intelligent.
- Libère la créativité pour fournir des descriptions de produits plus attrayantes.
- Améliore la cohérence du contenu marketing pour les gammes de produits.

Vous devez considérer le texte généré par l’IA comme un *suggestion seulement*. Les suggestions peuvent, dans certains cas, contenir des erreurs et même du texte inapproprié. Une surveillance et un examen humains sont donc nécessaires. Avant de rendre le texte accessible au public, vous devez en vérifier l’exactitude et apporter les modifications appropriées.

## <a name="current-limitations"></a>Limitations actuelles

Cette section explique les limites actuelles de la fonctionnalité de texte généré par l’IA fournie par Copilot.

- [!INCLUDE[copilot-supported-languages.md](includes/copilot-supported-languages.md)]
- De mauvaises suggestions peuvent se produire quand des noms de produits vagues ou génériques sont utilisés et que des détails sur un article manquent, comme des attributs clés ou une catégorie.
- Copilot est uniquement pris en charge sur Business Central Online ; pas les environnements de cloud privé ou les environnements Business Central sur site.
- Copilot n’est pas pris en charge via les connexions à votre propre ressource de service Azure OpenAI dans votre abonnement Azure.

<!-- Partner extensibility of the AI capability by using AL code isn't supported.-->

## <a name="next-steps"></a>Étapes suivantes

Pour commencer, vous aurez besoin d’un environnement Business Central (v23.1 et version ultérieure) dédiée qui est activée avec Copilot.

- Si vous êtes déjà client de Business Central, l’administrateur Business Central devra configurer pour vous un environnement activé pour les suggestions de texte marketing. Pour plus d’informations, accédez à [Configurer les fonctionnalités Copilot et IA](enable-ai.md).

- Si vous n’êtes pas client de Business Central mais que vous souhaitez l’essayer, inscrivez-vous pour un essai gratuit. Pour plus d’informations, accédez à [S’inscrire à un essai gratuit de Dynamics 365 Business Central](trial-signup.md).

Une fois que vous disposez d’un environnement ou d’un environnement d’évaluation, accédez à [Ajouter un texte marketing aux éléments avec Copilot](item-marketing-text.md).  

## <a name="see-also"></a>Voir aussi

[Configurer les capacités Copilot et IA](enable-ai.md)  
[Ajouter un texte marketing pour les articles avec Copilot](item-marketing-text.md)  
[FAQ sur les suggestions de texte marketing pour les articles](faqs-marketing-text.md)  
[Mise en route avec le connecteur Shopify](shopify/get-started.md)  
