---
title: Configuration du texte marketing article optimisé par l’IA (version préliminaire) avec Copilot
description: Cet article explique comment obtenir une version d’essai Copilot de Business Central et activer Copilot sur un environnement.
author: jswymer
ms.author: jswymer
ms.reviewer: jswymer
ms.topic: how-to
ms.date: 03/22/2023
ms.custom: bap-template
---

# <a name="configure-ai-powered-item-marketing-text-preview-with-copilot"></a><a name="configure-ai-powered-item-marketing-text-preview-with-copilot"></a>Configuration du texte marketing article optimisé par l’IA (version préliminaire) avec Copilot

[!INCLUDE[ai-preview](includes/ai-preview.md)]

Cet article explique comment vous pouvez contrôler la possibilité de créer du texte marketing d’articles alimenté par l’IA avec Copilot pour votre organisation. Cette tâche est effectuée par un administrateur. Vous devez remplir deux conditions pour que la fonctionnalité soit disponible pour les utilisateurs :

- Activez la fonctionnalité **Création de descriptions de produits optimisées par l’IA avec Copilot**.
- Consentement aux termes et conditions de la [version préliminaire](https://dynamics.microsoft.com/legaldocs/supp-dynamics365-preview/) et de la [Déclaration de confidentialité Microsoft](https://go.microsoft.com/fwlink/?LinkId=521839) au nom de l’organisation.

Si l’une de ces conditions n’est pas remplie, la fonctionnalité ne pourra pas être utilisée.

## <a name="prerequisites"></a><a name="prerequisites"></a>Conditions préalables

Vous utilisez une [version préliminaire](ai-preview-getstarted.md) de Business Central qui est activée pour Copilot. L’activation de Copilot est effectuée par un administrateur. Pour plus d’informations, accédez à [Configurer le texte marketing d’un article basé sur l’IA avec Copilot](enable-ai.md).

## <a name="enable-or-disable-create-ai-powered-product-descriptions-with-copilot"></a><a name="enable-or-disable-create-ai-powered-product-descriptions-with-copilot"></a>Activez ou désactivez la fonctionnalité Création de descriptions de produits optimisées par l’IA avec Copilot

1. Dans Business Central, recherchez et ouvrez la page **Gestion des fonctionnalités**.
2. Définissez la colonne **Activé pour** pour **version préliminaire de la fonctionnalité : Créer des descriptions de produits basées sur l’IA avec Copilot** sur **Tous les utilisateurs** pour activer la fonctionnalité ou **Aucun** pour la désactiver.

   Pour plus d’informations sur la gestion des fonctionnalités en général, accédez à [Gestion des fonctionnalités](/dynamics365/business-central/dev-itpro/administration/feature-management).

## <a name="consent-to-or-reject-preview-and-privacy-terms-and-conditions-for-all-users"></a><a name="consent-to-or-reject-preview-and-privacy-terms-and-conditions-for-all-users"></a>Accepter ou rejeter les conditions d’utilisation de la version préliminaire et de confidentialité pour tous les utilisateurs

1. Dans Business Central, recherchez et ouvrez la page **Statut des déclarations de confidentialité**.
2. Dans la colonne **Nom de l’intégration**, sélectionnez **Azure OpenAI**, puis lisez les termes et conditions qui vous êtes présentés.
3. Dans la ligne **Azure OpenAI**, cochez la case **Accepter pour tout le monde** pour consentir ou la case **Pas d’accord pour tout le monde** pour rejeter.

## <a name="next-steps"></a><a name="next-steps"></a>Étapes suivantes

Après avoir activé et accepté la fonctionnalité, vous êtes prêt à essayer Copilot sur des éléments dans Business Central. Accédez à [Ajouter du texte marketing aux articles](item-marketing-text.md).  

## <a name="see-also"></a><a name="see-also"></a>Voir aussi

[Vue d’ensemble du texte marketing article optimisé par l’IA avec Copilot](ai-overview.md)  
[Créer un texte marketing pour les articles à l’aide de Copilot](item-marketing-text.md)  
[FAQ sur le texte marketing article optimisé par l’IA avec Copilot](ai-faq.md)  
