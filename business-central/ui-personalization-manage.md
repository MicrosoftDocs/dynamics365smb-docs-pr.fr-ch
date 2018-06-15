---
title: "Gérer la personnalisation en tant qu'administrateur dans Financials | Microsoft Docs"
description: "Découvrez comment personnaliser l'interface utilisateur pour l'adapter à votre méthode de travail."
services: project-madeira
documentationcenter: 
author: jswymer
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: customize, personalize, personalization, hide columns, remove fields, move fields
ms.date: 07/26/2017
ms.author: jswymer
ms.translationtype: HT
ms.sourcegitcommit: 7c346455a9e27d7274b116754f1d594484b95d67
ms.openlocfilehash: 2d9b45bf21d325e60beadedfc94827d7f3fda075
ms.contentlocale: fr-ch
ms.lasthandoff: 04/18/2018

---
# <a name="managing-personalization-as-an-administrator"></a>Gérer la personnalisation en tant qu'administrateur
<!--NAV in the Web client-->
Les utilisateurs peuvent personnaliser leur espace de travail en fonction de leurs propres préférences. En tant qu'administrateur, vous pouvez contrôler et gérer la personnalisation en désactivant la capacité des utilisateurs à personnaliser des pages et en effaçant toutes les personnalisations de page effectuées par les utilisateurs.

## <a name="disable-personalization-for-a-profile"></a>Désactiver la personnalisation pour un profil
Vous pouvez empêcher tous les utilisateurs appartenant à un profil spécifique de personnaliser leurs pages.
1.  Sélectionnez l'icône ![Page ou état pour la recherche](media/ui-search/search_small.png "Page ou état pour la recherche"), entrez **Profils**, puis sélectionnez le lien connexe.
2.  Sélectionnez dans la liste le profil à modifier.
3. Activez la case à cocher **Désactiver la personnalisation**, puis cliquez sur le bouton **OK**.

## <a name="clear-user-personalizations"></a>Effacer les personnalisations des utilisateurs

L'effacement de la personnalisation de la page rétablit la page à sa disposition d'origine, antérieure à toute personnalisation. Il y a deux méthodes pour effacer les personnalisations de page effectuées par les utilisateurs : en utilisant la page **Supprimer la personnalisation utilisateur** et en utilisant la page **Fiche de personnalisation utilisateur**.

### <a name="clear-user-personalizations-by-using-the-delete-user-personalization-page"></a>Effacer les personnalisations utilisateur à l'aide de la page Supprimer la personnalisation utilisateur

La page **Supprimer la personnalisation utilisateur** permet d'effacer les personnalisations par page et par utilisateur individuellement.

1.  Choisissez l'icône ![Page ou état pour la recherche](media/ui-search/search_small.png "icône Page ou état pour la recherche"), entrez **Supprimer la personnalisation utilisateur**, puis sélectionnez le lien connexe.

    La page répertorie toutes les pages qui ont été personnalisées et l'utilisateur auquel elles appartiennent.

    >[!NOTE]
    > Une coche dans la colonne **Legacy Personalization** indique si la personnalisation a été effectuée dans une ancienne version de [!INCLUDE[d365fin](includes/d365fin_md.md)], qui a traité la personnalisation de manière différente. Les utilisateurs qui essaient de personnaliser ces pages sont empêchés de le faire, à moins qu'ils ne choisissent de déverrouiller la page. Pour plus d'informations, voir [Pourquoi la personnalisation d'une page est bloquée](ui-personalization-locked.md).

2. Sélectionnez l'écriture à supprimer, puis sélectionnez l'action **Supprimer**.

    L'utilisateur les verra les modifications lors de sa prochaine connexion.

### <a name="clear-user-personalizations-by-using-the-user-personalization-card-page"></a>Effacer les personnalisations utilisateur à l'aide de la page Fiche de personnalisation utilisateur

La page **Fiche de personnalisation utilisateur** permet d'effacer la personnalisation de toutes les pages d'un utilisateur spécifique. Cela nécessite l'autorisation d'écriture dans la table 2000000072 **Profil**.

1.  Choisissez l'icône ![Page ou état pour la recherche](media/ui-search/search_small.png "Page ou état pour la recherche"), entrez **Personnalisation utilisateur**, puis sélectionnez le lien connexe.

    La page **Personnalisation utilisateur** répertorie tous les utilisateurs qui ont potentiellement des pages personnalisées. Si vous ne trouvez pas un utilisateur dans la liste, cela signifie qu'ils n'a aucune page personnalisée.

2. Sélectionnez l'utilisateur dans la liste, puis sélectionnez l'action **Modifier**.

3.  Sous l'onglet **Actions**, choisissez **Effacer les pages personnalisées**.

    L'utilisateur les verra les modifications lors de sa prochaine connexion.

## <a name="see-also"></a>Voir aussi
[Personnalisation de votre espace de travail](ui-personalization-user.md)  
[Utilisation de [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)  
[Modification des paramètres de base](ui-change-basic-settings.md)  
[Modification des fonctionnalités affichées](ui-experiences.md)  

