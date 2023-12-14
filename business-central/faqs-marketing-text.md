---
title: FAQ sur les suggestions de texte marketing pour les articles
description: "Cette FAQ fournit des informations sur la technologie d’IA utilisée dans Business\_Central, ainsi que des considérations et des détails clés sur la façon dont l’IA est utilisée, comment elle a été testée et évaluée, ainsi que toute limitation spécifique."
ms.date: 10/07/2023
ms.custom:
  - responsible-ai-faqs
ms.topic: article
author: jswymer
ms.author: jswymer
ms.reviewer: jswymer
---

# FAQ relatives aux suggestions de textes marketing avec Copilot

Cette foire aux questions (FAQ) décrit l’impact de la fonctionnalité [!INCLUDE[feature-marketing-text-suggestions](includes/feature-marketing-text-suggestions.md)] sur l’IA dans [!INCLUDE[prod_short](includes/prod_short.md)].

## Que sont les suggestions de texte marketing pour les articles ?

Copilot fournit une aide à la rédaction aux utilisateurs responsables de la rédaction du texte marketing (également appelé copie) sur les articles contenus dans [!INCLUDE[prod_short](includes/prod_short.md)]. Cette fonctionnalité est connue sous le nom de [!INCLUDE[feature-marketing-text-suggestions](includes/feature-marketing-text-suggestions.md)]. La fonctionnalité [!INCLUDE[feature-marketing-text-suggestions](includes/feature-marketing-text-suggestions.md)] fournit une aide à la rédaction aux utilisateurs responsables de la rédaction du texte marketing (également appelé *copie*) sur les articles contenus dans [!INCLUDE[prod_short](includes/prod_short.md)].

La fonctionnalité est disponible sur n’importe quelle fiche d’article dans [!INCLUDE[prod_short](includes/prod_short.md)]. Pour l’utiliser, ouvrez simplement un élément, puis sélectionnez **Texte marketing** > **Rédiger avec Copilot**. Cette action génère automatiquement une suggestion de texte attrayante, créative et spécifique à l’article affiché. Les suggestions sont basées sur diverses entrées, notamment :

- Les attributs, la catégorie et le nom de l’article.
- Préférences de style d’écriture personnelles comme le ton de la voix, la qualité mise en évidence, le format et la longueur.

Vous pouvez modifier la valeur de ces options d’entrée pour influencer le résultat du texte généré par l’IA. Avant d’enregistrer une suggestion, vous pouvez facilement la passer en revue et la modifier pour gagner en précision ou essayer une autre suggestion.

Parmi certains avantages clés de cette fonctionnalité figurent les suivants :

- Diminue le temps consacré à la rédaction, ce qui peut accélérer la mise sur le marché des articles vendus dans les boutiques en ligne.
- Libère la créativité pour fournir des descriptions de produits plus attrayantes.
- Améliore la cohérence du matériel marketing pour les gammes de produits.

## Quelles sont les capacités du système ?

La fonctionnalité [!INCLUDE[feature-marketing-text-suggestions](includes/feature-marketing-text-suggestions.md)] utilise [Azure OpenAI Service de Microsoft](/azure/cognitive-services/openai/overview) pour avoir accès à de puissants modèles de langage qui analysent et génèrent un langage naturel. Ces modèles ont été entraînés sur un large éventail de jeux de données textuelles. En conséquence, Copilot peut générer des suggestions de réponses personnalisées en anglais basées sur une quantité minimale de données d’entrée, telles que les attributs, la catégorie ou la description d’un élément. 

## Quelle est l’utilisation prévue du système ?

Cette fonctionnalité est destinée à aider les utilisateurs à créer un texte marketing pour les articles dans [!INCLUDE[prod_short](includes/prod_short.md)]. Les rédacteurs utilisent cette fonctionnalité pour obtenir rapidement des suggestions de texte convaincantes et attrayantes, qui sont ensuite examinées et modifiées pour gagner en précision. 

## Comment le texte marketing de l’article a-t-il été évalué ? Quelles mesures sont utilisées pour évaluer les performances ?

- La fonctionnalité a subi des tests approfondis au cours desquels de nombreux textes dans différentes langues ont été évalués par des experts linguistiques selon divers critères. Les tests étaient basés sur les données de démonstration de [!INCLUDE[prod_short](includes/prod_short.md)] et d’autres catalogues de produits fictifs.
- Cette fonctionnalité est conçue conformément à la Norme IA Responsable de Microsoft. [Découvrez-en davantage sur l’IA responsable auprès de Microsoft](https://aka.ms/RAI).

## Comment Microsoft surveille-t-il la qualité du contenu généré ?

Microsoft a mis en place divers systèmes pour garantir que les capacités de Copilot restent opérationnelles et génèrent un contenu de la plus haute qualité.

- Les utilisateurs ont la possibilité de fournir des commentaires pour signaler un contenu inapproprié et améliorer la fonctionnalité.

  - Si vous rencontrez un contenu généré inapproprié, signalez-le à Microsoft en utilisant ce formulaire de commentaires : [Signaler un abus](https://go.microsoft.com/fwlink/?linkid=2249810). 

    Microsoft peut désactiver les fonctionnalités pilotées par Copilot pour certains clients si un abus de la fonctionnalité est détecté. 

  - Nous suivons les commentaires des utilisateurs sur [!INCLUDE[feature-marketing-text-suggestions](includes/feature-marketing-text-suggestions.md)] pour nous aider à améliorer les suggestions. 

    Vous fournissez des commentaires en utilisant l’icône J’aime (pouce levé) ou Je n’aime pas (pouce vers le bas) sur la page **Copilot** dans [!INCLUDE[prod_short](includes/prod_short.md)]. Nous rassemblons la télémétrie de ces gestes pour chaque sortie IA pour laquelle vous soumettez des commentaires.

    ![Affiche une fiche article avec volet Texte marketing](media/create-with-copilot-window-feedback.svg)

- Le service Azure OpenAI stocke les invites et les réalisations du service pour surveiller les utilisations abusives et pour développer et améliorer la qualité des systèmes de gestion de contenu d’Azure OpenAI. [En savoir plus sur notre gestion et notre filtrage de contenu](/azure/cognitive-services/openai/concepts/content-filter). Les données de votre entreprise ne sont pas utilisées pour entraîner des modèles d’IA dans le service Azure OpenAI.

   Les employés Microsoft autorisés peuvent accéder à vos données d’invite et d’achèvement qui ont déclenché nos systèmes automatisés à des fins d’enquête et de vérification d’abus potentiels ; pour les clients utilisant [!INCLUDE[prod_short](includes/prod_short.md)] dans l’Union européenne, les employés Microsoft autorisés sont situés dans l’Union européenne. Ces données peuvent être utilisées pour améliorer nos systèmes de gestion de contenu. En cas de violation confirmée de la stratégie, nous pouvons vous demander de prendre des mesures immédiates pour résoudre le problème et empêcher de nouveaux abus. Le fait de ne pas résoudre le problème peut entraîner la suspension ou la résiliation de l’accès aux ressources Azure OpenAI.

   Pour plus d’informations, consultez [Données, confidentialité et sécurité pour Azure OpenAI Service](/legal/cognitive-services/openai/data-privacy#abuse-and-harmful-content-generation).

## Existe-t-il un processus de journalisation et de révision humaine dans le cadre d’Azure OpenAI Service, et si oui, puis-je le désactiver ?  

Dans le cadre de la fourniture des versions préliminaires du service Azure OpenAI, Microsoft traitera et stockera les données client soumises au service, ainsi que le contenu de sortie, à des fins de surveillance et prévention des utilisations ou sorties abusives ou nuisibles du service ; et de développement, de test et d’amélioration des capacités conçues pour empêcher l’utilisation abusive ou les sorties nuisibles du service. 

Le personnel autorisé de Microsoft peut examiner les données qui ont déclenché nos systèmes automatisés pour enquêter et vérifier les abus potentiels, et peut s’engager dans un échantillonnage aléatoire limité de termes qui ne sont pas signalés par nos systèmes automatisés pour s’assurer que les systèmes fonctionnent correctement. Le personnel autorisé de Microsoft peut également accéder à ces données et les utiliser pour améliorer nos systèmes qui surveillent et empêchent les utilisations ou sorties abusives ou nuisibles du service. En savoir plus sur [les conditions de la version préliminaire](https://dynamics.microsoft.com/legaldocs/supp-dynamics365-preview/).

Pour que Microsoft puisse protéger le service et ses clients, il n’est pas possible de désactiver les processus de journalisation et d’examen humain.

## Quelles données la fonctionnalité recueille-t-elle ? Comment les données sont-elles utilisées ?

La fonctionnalité de suggestions de textes marketing collecte les données minimales requises par Business Central pour offrir le service. Pour plus d’informations, consultez les [Conditions de Dynamics 365 pour les fonctionnalités basées sur Azure OpenAI](https://go.microsoft.com/fwlink/?linkid=2236010).

Cette fonctionnalité collecte également des données à partir des commentaires que l’utilisateur peut fournir à l’aide des icônes J’aime (pouce levé) ou Je n’aime pas (pouce vers le bas) en haut de la page **Copilot**. Les données sont anonymes et incluent le choix d’aimer ou de ne pas aimer, la raison de l’aversion si elle est fournie et la fonctionnalité Copilot à laquelle les commentaires s’appliquent. Nous utilisons ces données afin d’évaluer et d’améliorer la qualité de la fonctionnalité.

## Quelles sont les limites de [!INCLUDE[feature-marketing-text-suggestions](includes/feature-marketing-text-suggestions.md)] ? Comment les utilisateurs peuvent-ils minimiser l’impact des [!INCLUDE[feature-marketing-text-suggestions](includes/feature-marketing-text-suggestions.md)] limitations lors de l’utilisation du système ?

- Étant donné que la technologie sous-jacente à la fonctionnalité utilise une IA qui a été formée sur un large éventail de sources, le contenu généré n’est pas toujours factuel ou approprié. Certaines suggestions peuvent même inclure du contenu douteux ou inapproprié. Il est de votre responsabilité d’examiner et de modifier les suggestions générées pour vous assurer qu’elles sont exactes et appropriées.
- [!INCLUDE[copilot-supported-languages.md](includes/copilot-supported-languages.md)]

  Des réponses inexactes pourraient être renvoyées si les utilisateurs interagissent avec le système dans les langues prises en charge. En outre, un texte inexact pourrait être généré lorsque la langue de l’utilisateur et la langue principale des données dans la base de données [!INCLUDE[prod_short](includes/prod_short.md)] ne sont pas identiques.


## Quels facteurs et paramètres opérationnels permettent une utilisation efficace et responsable du système ?

Il y a plusieurs choses que vous pouvez faire pour tirer le meilleur parti de la fonctionnalité :

- Ajouter plus d’attributs à un article pour promouvoir les fonctionnalités et caractéristiques spécifiques qui vous intéressent.
- Modifiez les options de ton de voix et d’accentuation de la qualité en fonction de vos préférences personnelles.
- Améliorer la description de l’article.
- Assurez-vous que l’article est attribué à la catégorie la plus appropriée.

Pour en savoir plus, accédez à [Améliorer et personnaliser les suggestions de texte](item-marketing-text.md#improve-and-tailor-text-suggestions).

> [!TIP]
> Vérifiez toujours l’exactitude des suggestions avant de les enregistrer et de les publier pour la consommation publique.


## Voir aussi

- [Suggestions de texte marketing](ai-overview.md)

[!INCLUDE[footer-include](includes/footer-banner.md)]