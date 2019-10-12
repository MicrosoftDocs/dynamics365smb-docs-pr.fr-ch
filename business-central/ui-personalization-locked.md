---
title: Pourquoi je ne peux pas personnaliser une page | Microsoft Docs
description: Explique pourquoi vous ne pouvez pas personnaliser une page et ce que vous pouvez faire pour la déverrouiller et pouvoir ainsi la personnaliser.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: customize, personalize, personalization, hide columns, remove fields, move fields
ms.date: 10/01/2019
ms.author: sgroespe
ms.openlocfilehash: c77664a1013804de13303c8e1d162c437cf5d6e7
ms.sourcegitcommit: 02e704bc3e01d62072144919774f1244c42827e4
ms.translationtype: HT
ms.contentlocale: fr-CH
ms.lasthandoff: 10/01/2019
ms.locfileid: "2315147"
---
# <a name="why-a-page-is-locked-from-personalization"></a>Pourquoi la personnalisation d'une page est verrouillée

Deux conditions vous empêchent de personnaliser une page. Soit la page est verrouillée (comme indiqué par l'icône ![Verrouillage de personnalisation](media/personalization-lock-icon.png "Verrouillage de personnalisation")) ou soit elle est bloquée (comme indiqué par l'icône ![Personnalisation bloquée](media/personalization-blocked-icon.png "Personnalisation bloquée")).

## <a name="locked-from-personalizing"></a>Personnalisation verrouillée

S'il existe une icône ![Verrouillage de personnalisation](media/personalization-lock-icon.png "Verrouillage de personnalisation") dans la bannière **Personnalisation** lorsque vous ouvrez une page, cela signifie que vous ne pouvez pas apporter d'autres modifications de personnalisation à la page.

<!-- This is because we changed the way personalization works behind the scenes since the last time that you personalized the page. Unfortunately, the old way and new of doing things do not work together.

The page currently includes the last personalization changes that you made. If you want to continue personalizing the page, then you can choose the lock icon and then **Unlock**. Just be aware that if you choose to unlock the page, the current personalization of the page will be cleared, and you will have to start from scratch.
-->

Deux raisons expliquent cela :

1. vous avez personnalisé la page auparavant, mais en utilisant une version antérieure du produit. Nous avons modifié la manière dont la personnalisation fonctionne en arrière-plan depuis votre dernière personnalisation de la page. Malheureusement, l'ancienne méthode et la nouvelle ne sont pas compatibles.

2. jusqu'ici, vous n'avez utilisé que [!INCLUDE[nav_windows_md](includes/nav_windows_md.md)] pour personnaliser la page.

### <a name="unlocking-the-page"></a>Déverrouillage de la page

Si vous souhaitez déverrouiller une page et poursuivre sa personnalisation, sélectionnez l'icône ![Verrouillage de personnalisation](media/personalization-lock-icon.png "Verrouillage de personnalisation"), puis l'action **Déverrouiller**.  

Avant de déverrouiller la page, veillez à ce qui suit :

- La personnalisation actuelle de la page est désactivée. La page reviendra à sa mise en page d'origine et vous devrez recommencer à zéro.

- Dans [!INCLUDE[nav_windows_md](includes/nav_windows_md.md)], la page reste telle quelle et n'est pas affectée par les modifications apportées à la nouvelle personnalisation dans le client Business Central. En outre, la personnalisation dans [!INCLUDE[nav_windows_md](includes/nav_windows_md.md)] et le client Business Central sont entièrement distinctes l'une de l'autre.

## <a name="blocked-from-personalizing"></a>Personnalisation bloquée

S'il y a une icône ![Personnalisation bloquée](media/personalization-blocked-icon.png "Personnalisation bloquée") dans la bannière **Personnalisation**, cela signifie que vous ne pouvez pas apporter de personnalisation à la page.

<!-- Only text is translated, so removing this image for non-English UX reasons.  ![Personalize blocked](media/personalization-blocked.png "Personalize lock") -->

La raison à cela n'est autre que le Tableau de bord ou le rôle actuellement associé à votre compte d'utilisateur modifie cette page notamment pour votre rôle. Contactez votre administrateur pour obtenir de l'aide. Sinon, essayez de passer à un Tableau de bord qui inclut la personnalisation des rôles pour cette page. Pour plus d'informations, voir [Modifier les paramètres de base](ui-change-basic-settings.md).

## <a name="see-also"></a>Voir aussi
[Personnaliser votre espace de travail](ui-personalization-user.md)  
[Personnaliser les pages pour les profils](ui-personalization-manage.md)  
[Modifier les paramètres de base](ui-change-basic-settings.md)  
[Modifier les fonctionnalités affichées](ui-experiences.md)  
