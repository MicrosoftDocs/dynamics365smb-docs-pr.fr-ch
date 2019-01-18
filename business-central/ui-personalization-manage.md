---
title: "Gérer la personnalisation en tant qu'administrateur dans Business Central | Microsoft Docs"
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
ms.date: 10/01/2018
ms.author: jswymer
ms.translationtype: HT
ms.sourcegitcommit: caf7cf5afe370af0c4294c794c0ff9bc8ff4c31c
ms.openlocfilehash: 15d7e4aac7989f95f7becc8aa8ed96381a7dc2de
ms.contentlocale: fr-ch
ms.lasthandoff: 11/22/2018

---
# <a name="managing-personalization-as-an-administrator"></a>Gérer la personnalisation en tant qu'administrateur
<!--NAV in the Web client--> Les utilisateurs peuvent personnaliser leur espace de travail en fonction de leurs propres préférences. En tant qu'administrateur, vous pouvez contrôler et gérer la personnalisation en désactivant la capacité des utilisateurs à personnaliser des pages et en effaçant toutes les personnalisations de page effectuées par les utilisateurs.

## <a name="disable-personalization-for-a-profile"></a>Désactiver la personnalisation pour un profil
Vous pouvez empêcher tous les utilisateurs appartenant à un profil spécifique de personnaliser leurs pages.
1.  Choisissez l'icône ![Ampoule qui ouvre la fonction Tell Me](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire"), saisissez **Profils**, puis sélectionnez le lien associé.
2.  Sélectionnez dans la liste le profil à modifier.
3. Activez la case à cocher **Désactiver la personnalisation**, puis cliquez sur le bouton **OK**.

## <a name="clear-user-personalizations"></a>Effacer les personnalisations des utilisateurs

L'effacement de la personnalisation de la page rétablit la page à sa disposition d'origine, antérieure à toute personnalisation. Il y a deux méthodes pour effacer les personnalisations de page effectuées par les utilisateurs : en utilisant la page **Supprimer la personnalisation utilisateur** et en utilisant la page **Fiche de personnalisation utilisateur**.

### <a name="clear-user-personalizations-by-using-the-delete-user-personalization-page"></a>Effacer les personnalisations utilisateur à l'aide de la page Supprimer la personnalisation utilisateur

La page **Supprimer la personnalisation utilisateur** permet d'effacer les personnalisations par page et par utilisateur individuellement.

1.  Choisissez l'icône ![Ampoule qui ouvre la fonction Tell Me](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire"), saisissez **Supprimer la personnalisation utilisateur**, puis sélectionnez le lien associé.

    La page répertorie toutes les pages qui ont été personnalisées et l'utilisateur auquel elles appartiennent.

    >[!NOTE]
    > Une coche dans la colonne **Legacy Personalization** indique si la personnalisation a été effectuée dans une ancienne version de [!INCLUDE[d365fin](includes/d365fin_md.md)], qui a traité la personnalisation de manière différente. Les utilisateurs qui essaient de personnaliser ces pages sont empêchés de le faire, à moins qu'ils ne choisissent de déverrouiller la page. Pour plus d'informations, voir [Pourquoi la personnalisation d'une page est bloquée](ui-personalization-locked.md).

2. Sélectionnez l'écriture à supprimer, puis sélectionnez l'action **Supprimer**.

    L'utilisateur les verra les modifications lors de sa prochaine connexion.

### <a name="clear-user-personalizations-by-using-the-user-personalization-card-page"></a>Effacer les personnalisations utilisateur à l'aide de la page Fiche de personnalisation utilisateur

La page **Fiche de personnalisation utilisateur** permet d'effacer la personnalisation de toutes les pages d'un utilisateur spécifique. Cela nécessite l'autorisation d'écriture dans la table 2000000072 **Profil**.

1.  Choisissez l'icône ![Ampoule qui ouvre la fonction Tell Me](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire"), saisissez **Personnalisation utilisateur**, puis sélectionnez le lien associé.

    La page **Personnalisation utilisateur** répertorie tous les utilisateurs qui ont potentiellement des pages personnalisées. Si vous ne trouvez pas un utilisateur dans la liste, cela signifie qu'ils n'a aucune page personnalisée.

2. Sélectionnez l'utilisateur dans la liste, puis sélectionnez l'action **Modifier**.

3.  Sous l'onglet **Actions**, choisissez **Effacer les pages personnalisées**.

    L'utilisateur les verra les modifications lors de sa prochaine connexion.

## <a name="see-also"></a>Voir aussi
[Personnalisation de votre espace de travail](ui-personalization-user.md)  
[Utilisation de [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)  
[Modification des paramètres de base](ui-change-basic-settings.md)  
[Modification des fonctionnalités affichées](ui-experiences.md)  

