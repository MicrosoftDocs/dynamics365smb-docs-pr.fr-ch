---
title: Pourquoi la personnalisation d’une page est verrouillée
description: Vous ne pouvez pas personnaliser une page. Lisez ici pour savoir ce que vous pouvez faire pour la déverrouiller afin de pouvoir la personnaliser.
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 'customize, personalize, personalization, hide columns, remove fields, move fields'
ms.search.form: null
ms.date: 04/01/2021
ms.author: edupont
---
# Pourquoi la personnalisation d’une page est verrouillée

Deux conditions vous empêchent de personnaliser une page. La page est verrouillée (comme indiqué par l’icône ![Verrouillage de personnalisation.](media/personalization-lock-icon.png "Verrouillage de personnalisation")) ou bloquée (comme indiqué par l’icône ![Personnalisation bloquée.](media/personalization-blocked-icon.png "Personnalisation bloquée") .

## Personnalisation verrouillée

S’il y a une icône ![Verrouillage de personnalisation.](media/personalization-lock-icon.png "Verrouillage de personnalisation") dans la bannière **Personnalisation** lorsque vous ouvrez une page, vous ne pouvez pas apporter d’autres modifications de personnalisation à la page.

<!-- This is because we changed the way personalization works behind the scenes since the last time that you personalized the page. Unfortunately, the old way and new of doing things do not work together.

The page currently includes the last personalization changes that you made. If you want to continue personalizing the page, then you can choose the lock icon and then **Unlock**. Just be aware that if you choose to unlock the page, the current personalization of the page will be cleared, and you will have to start from scratch.
-->

Deux raisons sont possibles :

1. Vous avez personnalisé la page auparavant, mais en utilisant une version antérieure du produit. Nous avons modifié la manière dont la personnalisation fonctionne en arrière-plan depuis votre dernière personnalisation de la page. Malheureusement, l’ancienne méthode et la nouvelle ne sont pas compatibles.

2. Jusqu’ici, vous n’avez utilisé que la version obsolète de [!INCLUDE[nav_windows_md](includes/nav_windows_md.md)] pour personnaliser la page.

### Déverrouillage de la page

Si vous souhaitez déverrouiller une page et poursuivre sa personnalisation, sélectionnez l’icône ![Verrouillage de personnalisation](media/personalization-lock-icon.png "Verrouillage de personnalisation"), puis l’action **Déverrouiller**.  

> [!CAUTION]
> La personnalisation actuelle de la page est désactivée. La page reviendra à sa mise en page d’origine et vous devrez recommencer à zéro.  

## Personnalisation bloquée

S’il y a une icône ![Personnalisation bloquée](media/personalization-blocked-icon.png "Personnalisation bloquée") dans la bannière **Personnalisation**, vous ne pouvez pas apporter de personnalisation à la page.

<!-- Only text is translated, so removing this image for non-English UX reasons.  ![Personalize blocked.](media/personalization-blocked.png "Personalize lock") -->

La raison est que le Tableau de bord ou le rôle actuellement associé à votre compte d’utilisateur modifie cette page, notamment pour votre rôle. Contactez votre administrateur pour obtenir de l’aide. Sinon, essayez de passer à un Tableau de bord qui inclut la personnalisation des rôles pour cette page. Pour plus d’informations, voir [Modifier les paramètres de base](ui-change-basic-settings.md).

## Voir aussi

[Personnaliser votre espace de travail](ui-personalization-user.md)  
[Personnaliser les pages pour les profils](ui-personalization-manage.md)  
[Modifier les paramètres de base](ui-change-basic-settings.md)  
[Modifier les fonctionnalités affichées](ui-experiences.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
