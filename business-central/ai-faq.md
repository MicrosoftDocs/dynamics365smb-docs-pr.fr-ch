---
title: FAQ sur le texte marketing article optimisé par l’IA (version préliminaire) avec Copilot
description: Obtenez des réponses aux questions courantes sur les fonctionnalités de texte généré par l’IA avec Copilot.
ms.author: jswymer
ms.reviewer: jswymer
ms.topic: faq
ms.date: 04/03/2023
ms.custom: bap-template
author: jswymer
ms.service: dynamics365-business-central
---

# <a name="ai-powered-item-marketing-text-preview-with-copilot-faq"></a><a name="ai-powered-item-marketing-text-preview-with-copilot-faq"></a><a name="ai-powered-item-marketing-text-preview-with-copilot-faq"></a>FAQ sur le texte marketing article optimisé par l’IA (version préliminaire) avec Copilot

[!INCLUDE[ai-preview](includes/ai-preview.md)]

Cet article utilise des questions et des réponses pour expliquer des aspects importants de la technologie d’IA derrière Copilot et du texte qu’il génère.

## [Général](#tab/general)

### <a name="what-is-copilot"></a><a name="what-is-copilot"></a><a name="what-is-copilot"></a>Qu’est-ce que Copilot ?

Copilot fournit des suggestions de texte générées par l’IA pour les éléments dans Business Central. Il est destiné aux utilisateurs qui rédigent du texte marketing pour des articles afin de les aider à produire un contenu attrayant et convaincant. Certains avantages principaux comprennent :

- Diminue le temps consacré à la rédaction, ce qui peut accélérer la mise sur le marché des articles vendus dans les boutiques en ligne.
- Libère la créativité pour fournir des descriptions de produits plus attrayantes.
- Améliore la cohérence du matériel marketing pour les gammes de produits.

Les utilisateurs doivent considérer le texte généré par l’IA comme une suggestion qui doit être examinée et modifiée pour plus de précision avant qu’elle ne soit accessible au public.

### <a name="why-isnt-copilot-available-for-marketing-text-on-my-items-in-business-central"></a><a name="why-isnt-copilot-available-for-marketing-text-on-my-items-in-business-central"></a><a name="why-isnt-copilot-available-for-marketing-text-on-my-items-in-business-central"></a>Pourquoi Copilot n’est-il pas disponible pour le texte marketing sur mes articles dans Business Central ?

Pour que Copilot soit disponible, les conditions suivantes doivent être remplies :

- La langue que vous utilisez dans Business Central doit être l’anglais. Tous les paramètres régionaux anglais disponibles fonctionneront, comme l’anglais (États-Unis), l’anglais (Royaume-Uni) ou l’anglais (Afrique du Sud).

  Pour modifier la langue, dans le coin supérieur droit, sélectionnez l’icône **Paramètres** ![Paramètres](media/ui-experience/settings_icon_small.png "Icône Paramètres du tableau de bord") > **Mes paramètres** > **Langue**. Pour plus d’informations, consultez [Modifier les paramètres de base](ui-change-basic-settings.md#language).
- Vous devez utiliser la version 22 ou ultérieure de Business Central Online (si vous êtes déjà client) ou une version d’évaluation.  <!--**22.0.54157.54311 (Preview - Copilot edition)**-->

   Pour vérifier la version, sélectionnez le point d’interrogation dans le coin supérieur droit, puis sélectionnez **Aide et support**. Sous **Résolution des problèmes**, recherchez la version de l’application. Pour plus d’informations sur la façon d’obtenir la bonne version préliminaire, accédez à [Commencer par une version préliminaire de Business Central](ai-preview-getstarted.md).
- La fonctionnalité **Créer des descriptions de produits optimisées par l’IA avec Copilot** doit être activée.

   Pour plus d’informations, accédez à [Activer ou désactiver la fonctionnalité "Créer des descriptions de produits basées sur l’IA avec Copilot"](enable-ai.md#enable-or-disable-create-ai-powered-product-descriptions-with-copilot).
- Un administrateur a accepté les termes et conditions.

   Pour plus d’informations, accédez à [Accepter ou rejeter les conditions d’utilisation de la version préliminaire et de confidentialité pour tous les utilisateurs](enable-ai.md#consent-to-or-reject-preview-and-privacy-terms-and-conditions-for-all-users).

### <a name="is-copilot-available-for-preview-in-business-central-on-premises"></a><a name="is-copilot-available-for-preview-in-business-central-on-premises"></a><a name="is-copilot-available-for-preview-in-business-central-on-premises"></a>Est-ce que Copilot est disponible en version préliminaire dans Business Central sur site ?

Non, il n’est actuellement pas pris en charge dans Business Central sur site.

### <a name="how-does-copilot-work-where-does-the-suggested-text-come-from"></a><a name="how-does-copilot-work-where-does-the-suggested-text-come-from"></a><a name="how-does-copilot-work-where-does-the-suggested-text-come-from"></a>Comment fonctionne Copilot, d’où vient le texte suggéré ?

Copilot utilise [le service Azure OpenAI de Microsoft](/azure/cognitive-services/openai/overview) pour accéder à de puissants modèles de langage qui analysent et génèrent du langage naturel. Ces modèles ont été entraînés sur un large éventail de jeux de données textuelles. En conséquence, Copilot peut générer des suggestions de réponses personnalisées en anglais basées sur une quantité minimale de données d’entrée, telles que les attributs, la catégorie ou la description d’un élément. 

### <a name="whats-the-quality-of-the-text-suggested-by-copilot"></a><a name="whats-the-quality-of-the-text-suggested-by-copilot"></a><a name="whats-the-quality-of-the-text-suggested-by-copilot"></a>Quelle est la qualité du texte proposé par Copilot ?

Étant donné que la technologie sous-jacente de Copilot utilise une IA qui a été formée sur un large éventail de sources, le contenu généré n’est pas toujours factuel ou approprié. Certaines suggestions peuvent même inclure du contenu douteux ou inapproprié. Il est de votre responsabilité d’examiner et de modifier les suggestions générées pour vous assurer qu’elles sont exactes et appropriées.

Pour plus d’informations sur les suggestions inappropriées, consultez [Que fait-on à propos des suggestions de texte abusives et nuisibles ?](/dynamics365/business-central/ai-faq?&tabs=oversight#whats-done-about-abusive-and-harmful-text-suggestions).

### <a name="how-can-i-improve-the-suggestions-i-get-from-copilot"></a><a name="how-can-i-improve-the-suggestions-i-get-from-copilot"></a><a name="how-can-i-improve-the-suggestions-i-get-from-copilot"></a>Comment puis-je améliorer les suggestions que je reçois de Copilot ?

Il y a plusieurs choses que vous pouvez faire pour tirer le meilleur parti des suggestions de Copilot :

- Ajouter plus d’attributs à un article pour promouvoir les fonctionnalités et caractéristiques spécifiques qui vous intéressent.
- Modifiez les options de ton de voix et d’accentuation de la qualité en fonction de vos préférences personnelles.
- Améliorer la description de l’article.
- Assurez-vous que l’article est attribué à la catégorie la plus appropriée.

Pour en savoir plus, accédez à [Améliorer et personnaliser les suggestions de texte](item-marketing-text.md#improve-and-tailor-text-suggestions).

### <a name="what-if-im-not-satisfied-with-the-generated-text"></a><a name="what-if-im-not-satisfied-with-the-generated-text"></a><a name="what-if-im-not-satisfied-with-the-generated-text"></a>Que faire si je ne suis pas satisfait du texte généré ?

Pour nous aider à améliorer le texte, sélectionnez **Est-ce une bonne suggestion ?** sur la page **Créer avec Copilot**, qui vous pouvez répondre avec un pouce vers le haut (j’aime ça) ou vers le bas (besoin d’amélioration).

![Affiche une fiche article avec volet Texte marketing](media/create-with-copilot-window-feedback.png)

### <a name="can-admins-disable-copilot-if-so-how"></a><a name="can-admins-disable-copilot-if-so-how"></a><a name="can-admins-disable-copilot-if-so-how"></a>Les administrateurs peuvent-ils désactiver Copilot ? Si oui, comment ?

Business Central propose aux administrateurs deux manières de désactiver Copilot dans la version préliminaire :

- N’acceptez pas l’avis de confidentialité d’Azure OpenAI pour tous les utilisateurs.

  ou

- Désactivez la fonctionnalité **Créer des descriptions de produits basées sur l’IA avec Copilot** sur la page **Gestion des fonctionnalités**.

Pour en savoir plus, accédez à [Configurer le texte marketing d’un article basé sur l’IA (version préliminaire) avec Copilot en tant qu’administrateur](enable-ai.md).

## [Équité](#tab/fairness)

### <a name="does-copilot-work-with-languages-other-than-english"></a><a name="does-copilot-work-with-languages-other-than-english"></a><a name="does-copilot-work-with-languages-other-than-english"></a>Copilot fonctionne-t-il avec des langues autres que l’anglais ?

Actuellement, Copilot ne prend en charge que l’anglais. Des réponses inexactes peuvent être renvoyées quand les utilisateurs conversent avec le système dans des langues autres que l’anglais.

## [Surveillance humaine](#tab/oversight)

### <a name="whats-done-about-abusive-and-harmful-text-suggestions"></a><a name="whats-done-about-abusive-and-harmful-text-suggestions"></a><a name="whats-done-about-abusive-and-harmful-text-suggestions"></a>Que fait-on des suggestions de texte abusives et préjudiciables ?

Le service Azure OpenAI stocke les invites et les réalisations du service pour surveiller les utilisations abusives et pour développer et améliorer la qualité des systèmes de gestion de contenu d’Azure OpenAI. [En savoir plus sur notre gestion et notre filtrage de contenu](/azure/cognitive-services/openai/concepts/content-filter)

Les employés Microsoft autorisés peuvent accéder à vos données d’invite et d’achèvement qui ont déclenché nos systèmes automatisés à des fins d’enquête et de vérification d’abus potentiels ; pour les clients qui ont déployé Azure OpenAI Service dans l’Union européenne, les employés Microsoft autorisés seront situés dans l’Union européenne. Ces données peuvent être utilisées pour améliorer nos systèmes de gestion de contenu. En cas de violation confirmée de la stratégie, nous pouvons vous demander de prendre des mesures immédiates pour résoudre le problème et empêcher de nouveaux abus. Le fait de ne pas résoudre le problème peut entraîner la suspension ou la résiliation de l’accès aux ressources Azure OpenAI.

Pour plus d’informations, consultez [Données, confidentialité et sécurité pour Azure OpenAI Service](/legal/cognitive-services/openai/data-privacy#abuse-and-harmful-content-generation).

### <a name="can-i-opt-out-of-the-logging-and-human-review-process"></a><a name="can-i-opt-out-of-the-logging-and-human-review-process"></a><a name="can-i-opt-out-of-the-logging-and-human-review-process"></a>Puis-je désactiver le processus de journalisation et d’examen humain ?

Dans le cadre de la fourniture des versions préliminaires d’Azure OpenAI, Microsoft traitera et stockera les données client soumises au service, ainsi que le contenu de sortie, à des fins de (1) surveillance et prévention des utilisations ou sorties abusives ou nuisibles du service ; et (2) développer, tester et améliorer les capacités conçues pour empêcher l’utilisation abusive ou les sorties nuisibles du service. 

Le personnel autorisé de Microsoft peut examiner les données qui ont déclenché nos systèmes automatisés pour enquêter et vérifier les abus potentiels, et peut s’engager dans un échantillonnage aléatoire limité de termes qui ne sont pas signalés par nos systèmes automatisés pour s’assurer que les systèmes fonctionnent correctement. Le personnel autorisé de Microsoft peut également accéder à ces données et les utiliser pour améliorer nos systèmes qui surveillent et empêchent les utilisations ou sorties abusives ou nuisibles du service. En savoir plus sur [les conditions de la version préliminaire](https://dynamics.microsoft.com/legaldocs/supp-dynamics365-preview/).

## [Confidentialité](#tab/privacy)

### <a name="what-data-does-the-capability-collect-how-is-the-data-used"></a><a name="what-data-does-the-capability-collect-how-is-the-data-used"></a><a name="what-data-does-the-capability-collect-how-is-the-data-used"></a>Quelles données la fonctionnalité recueille-t-elle ? Comment les données sont-elles utilisées ?

La capacité collecte vos réponses à la question **Est-ce une bonne suggestion ?** sur la page **Créer avec Copilot**, qui vous pouvez répondre avec un pouce vers le haut (j’aime ça) ou vers le bas (besoin d’amélioration).

Nous utilisons ces données afin d’évaluer et d’améliorer la qualité de la fonctionnalité. En savoir plus sur les données recueillies : consultez les [conditions de la version préliminaire](https://dynamics.microsoft.com/legaldocs/supp-dynamics365-preview/).

![Affiche une fiche article avec volet Texte marketing](media/create-with-copilot-window-feedback.png)

---

## <a name="see-also"></a><a name="see-also"></a><a name="see-also"></a>Voir aussi

[Vue d’ensemble du texte marketing article optimisé par l’IA avec Copilot](ai-overview.md)  
[Configuration du texte marketing article optimisé par l’IA avec Copilot en tant qu’administrateur](enable-ai.md)  
[Créer un texte marketing pour les articles à l’aide de Copilot](item-marketing-text.md)  

