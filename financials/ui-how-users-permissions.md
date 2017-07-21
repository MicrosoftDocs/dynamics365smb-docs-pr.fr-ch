---
title: "Affecter des autorisations d'utilisateur et créez ou modifiez des ensembles d'autorisations | Microsoft Docs"
description: "Décrit comment ajouter des utilisateurs d'Office 365 à Financials, puis affecte des autorisations, des droits d'accès, et des paramètres de sécurité."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: access, right, security
ms.date: 06/27/2017
ms.author: sgroespe
ms.translationtype: Human Translation
ms.sourcegitcommit: 81636fc2e661bd9b07c54da1cd5d0d27e30d01a2
ms.openlocfilehash: 564ef68a1571611efee32db1cf3759cda6a04c80
ms.contentlocale: fr-ch
ms.lasthandoff: 07/07/2017


---
# <a name="how-to-manage-users-and-permissions"></a>Procédure : gérer les utilisateurs et les autorisations
Pour ajouter des utilisateurs dans [!INCLUDE[d365fin](includes/d365fin_md.md)], l'administrateur Office 365 de votre société doit d'abord créer les utilisateurs dans le centre d’administration Office 365. Pour plus d'informations, voir [Ajouter des utilisateurs à Office 365 for business](https://support.office.com/en-us/article/Add-users-to-Office-365-for-business-435ccec3-09dd-4587-9ebd-2f3cad6bc2bc)

Une fois les utilisateurs créés dans Office 365, ils peuvent être importés dans la fenêtre **Utilisateurs** à l'aide de l'option **Récupérer des utilisateurs à partir d'Office 365**. Des ensembles d'autorisations sont affectés aux utilisateurs selon le plan qui leur est affecté dans Office 365.

Vous pouvez ensuite passer à l'affectation des ensembles d'autorisations aux utilisateurs pour définir à quels objets de base de données, et de ce fait, à quels éléments de l'interface utilisateur, ils ont accès et dans quelles sociétés.

Un ensemble d'autorisations est une collection d'autorisations pour des objets spécifiques de la base de données. Tous les utilisateurs doivent être affectés à une ou plusieurs séries d’autorisations avant de pouvoir accéder à [!INCLUDE[d365fin](includes/d365fin_md.md)]. Plusieurs ensembles d’autorisations prédéfinis sont fournis par défaut. Vous pouvez utiliser ces ensembles d'autorisations tels qu'ils ont été définis, modifier les propres ensembles d'autorisations, ou en créer d'autres.

Vous pouvez ajouter des utilisateurs aux groupes d'utilisateurs. Cela facilite l'affectation des mêmes ensembles d'autorisations à plusieurs utilisateurs.

Les administrateurs peuvent utiliser la fenêtre **Paramètres utilisateur** pour définir les périodes de temps pendant lesquelles les utilisateurs spécifiés peuvent valider, et spécifier également si le système enregistre la durée pendant laquelle les utilisateurs spécifiés ont ouvert une session.

> [!NOTE]  
>   Cette fonctionnalité nécessite que votre expérience soit définie sur Suite. Pour plus d'informations, voir [Personnalisation de votre expérience [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-experiences.md).

## <a name="to-assign-permissions-to-a-user"></a>Pour affecter des autorisations à un utilisateur
1. Choisissez l'icône ![Page ou état pour la recherche](media/ui-search/search_small.png "icône Page ou état pour la recherche"), entrez **Utilisateurs**, puis sélectionnez le lien connexe.
2. Sélectionnez l'utilisateur auquel affecter des autorisations.
Tous les ensembles d’autorisations qui sont affectés à l’utilisateur sont affichés dans le récapitulatif **Ensemble d’autorisations utilisateur**.
3. Sélectionnez l'option **Modifier** pour ouvrir la fenêtre **Fiche utilisateur**.
4. Sur le raccourci **Ensembles d'autorisations utilisateur**, renseignez les champs, le cas échéant sur une nouvelle ligne. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

## <a name="to-group-users-in-user-groups"></a>Pour regrouper des utilisateurs dans des groupes d'utilisateurs
Vous pouvez définir des groupes d'utilisateurs pour vous aider à gérer les ensembles d'autorisations pour des groupes d'utilisateurs de votre société. Vous pouvez utiliser une fonction pour copier tous les ensembles d'autorisations d'un groupe d'utilisateurs existant vers un nouveau groupe d'utilisateurs. Les membres du groupe d'utilisateurs ne sont pas copiés.

1. Choisissez l'icône ![Page ou état pour la recherche](media/ui-search/search_small.png "icône Page ou état pour la recherche"), entrez **Utilisateurs**, puis sélectionnez le lien connexe.
2. Sinon, dans la fenêtre **Utilisateurs**, sélectionnez l'option **Groupes d'utilisateurs**.
3. Dans la fenêtre **Groupes d'utilisateurs**, sélectionnez un groupe d'utilisateurs existant à copier, puis sélectionnez l'option **Copier groupe d'utilisateurs**.
4. Dans le champ **Nouveau code du groupe d'utilisateurs**, spécifiez le nom du nouveau groupe d'utilisateurs, puis cliquez sur le bouton **OK**.

    Au lieu de copier, vous pouvez aussi choisir l'option Nouveau pour créer une ligne pour un groupe d'utilisateurs vide, que vous renseignez ensuite manuellement.
5. Pour ajouter de nouveaux utilisateurs ou des utilisateurs supplémentaires , dans la fenêtre **Groupe d'utilisateurs**, cliquez sur **Membres du groupe d'utilisateurs**.
6. Dans la fenêtre **Membres du groupe d'utilisateurs**, dans une nouvelle ligne, renseignez les champs selon vos besoins en sélectionnant des utilisateurs existants.
7. Pour ajouter de nouveaux ensembles d'autorisations ou des ensembles d'autorisations supplémentaires , dans la fenêtre **Groupe d'utilisateurs**, cliquez sur **Ensembles d'autorisations groupe d'utilisateurs**.
8. Dans la fenêtre **Ensembles d'autorisations groupe d'utilisateurs**, dans une nouvelle ligne, renseignez les champs selon vos besoins en sélectionnant parmi des ensembles d’autorisations existants.

## <a name="to-create-or-modify-permission-sets"></a>Pour créer ou modifier des ensembles d'autorisations
Si les ensembles d’autorisations qui sont fournis par défaut avec [!INCLUDE[d365fin](includes/d365fin_md.md)] ne sont pas suffisants ou ne sont pas applicables à votre organisation, vous pouvez créer des ensembles d’autorisations. Et si les différentes autorisations d'objet qui définissent un ensemble d'autorisations ne sont pas appropriées, vous pouvez modifier un ensemble d'autorisations. Vous pouvez créer un ensemble d'autorisations manuellement, ou vous pouvez utiliser une fonction d'enregistrements qui stocke vos actions lorsque vous naviguez dans un scénario, puis génère l'ensemble d'autorisations requis.

### <a name="to-create-or-modify-permission-sets-manually"></a>Pour créer ou modifier des ensembles d'autorisations manuellement
1. Choisissez l'icône ![Page ou état pour la recherche](media/ui-search/search_small.png "icône Page ou état pour la recherche"), entrez **Utilisateurs**, puis sélectionnez le lien connexe.
2. Dans la fenêtre **Utilisateurs**, cliquez sur l'option **Ensembles d'autorisations**.
3. Dans la fenêtre **Ensembles d'autorisations**, cliquez sur l'option **Nouveau**.
4. Sur une nouvelle ligne, renseignez les champs selon vos besoins.
5. Sélectionnez l'option **Autorisations**.
6. Dans la fenêtre **Autorisations**, renseignez les champs de l'en-tête selon vos besoins.
7. Sur une nouvelle ligne, renseignez les cinq champs pour les différents types d'autorisation comme indiqué dans le tableau suivant.

    |Option|Désignation|
    |------|-----------|
    |Vide|Indique que le type d'autorisation n'est pas accordé pour l'objet.|
    |**Oui**|Indique que le type d'autorisation n'est pas accordé avec un accès direct à l'objet.|
    |**Indirect**|Indique que le type d'autorisation est accordé avec un accès indirect à l'objet.|

    L'autorisation indirecte à une table signifie que vous ne pouvez pas ouvrir la table et lire directement à partir de celle-ci, mais vous pouvez afficher les données de la table via un autre objet, par exemple une page, à laquelle vous avez un accès direct. Pour plus d'informations, voir la section « Exemple - Autorisation indirecte » de cette rubrique.

8. Dans le champ **Filtre sécurité**, entrez un filtre auquel vous souhaitez appliquer l'autorisation en sélectionnant le champ sur lequel vous souhaitez limiter l'accès utilisateur.

    Par exemple, si vous souhaitez créer un filtre de sécurité afin qu'un utilisateur puisse afficher uniquement les ventes ayant un code vendeur spécifique, sélectionnez le numéro de champ pour le champ **Code vendeur**. Ensuite, dans le champ **Filtre champ**, saisissez la valeur à utiliser pour limiter l'accès. Par exemple, pour qu'un utilisateur puisse uniquement accéder aux ventes d'Angela Barbariol, entrez AB.
9. Répétez les étapes 7 et 8 pour ajouter des autorisations pour d'autres objets de l'ensemble d'autorisations.

### <a name="to-create-or-modify-permission-sets-by-recording-your-actions"></a>Pour créer ou modifier des ensembles d'autorisations en enregistrant vos actions
1. Choisissez l'icône ![Page ou état pour la recherche](media/ui-search/search_small.png "icône Page ou état pour la recherche"), entrez **Utilisateurs**, puis sélectionnez le lien connexe.
2. Dans la fenêtre **Utilisateurs**, cliquez sur l'option **Ensembles d'autorisations**.
3. Dans la fenêtre **Ensembles d'autorisations**, cliquez sur l'option **Nouveau**.
4. Sur une nouvelle ligne, renseignez les champs selon vos besoins.
5. Sélectionnez l'option **Autorisations**.
6. Dans la fenêtre **Autorisations**, cliquez sur l'option **Démarrer**.

    Un processus d'enregistrement commence à capturer toutes vos actions dans l'interface utilisateur.
7. Accédez aux différentes fenêtres et activités dans [!INCLUDE[d365fin](includes/d365fin_md.md)] auxquelles vous voulez que les utilisateurs avec cet ensemble d'autorisations puissent accéder. Vous devez exécuter les tâches pour lesquelles vous souhaitez enregistrer des autorisations.
8. Lorsque vous souhaitez terminer l'enregistrement, revenez dans la fenêtre **Autorisations** et choisissez l'option **Arrêter**.
9. Cliquez sur le bouton **Oui** pour ajouter les autorisations enregistrées au nouvel ensemble d'autorisations.
10. Pour chaque objet de la liste enregistrée, indiquez si les utilisateurs peuvent insérer, modifier ou supprimer des enregistrements dans les tables enregistrées. Voir l'étape 7 de la section « Pour créer ou modifier des ensembles d'autorisations manuellement ».

### <a name="example---indirect-permission"></a>Exemple- Autorisation indirecte
L'autorisation indirecte vous permet d'utiliser un objet uniquement au travers d'un autre objet.
Par exemple, un utilisateur peut être autorisé à exécuter le codeunit 80 **Ventes-Valider**. Le codeunit **Ventes-Valider** effectue de nombreuses tâches, parmi lesquelles modifier la table 37 (**Ligne vente**). Lorsque l'utilisateur valide un document vente, le codeunit **Ventes-Valider**, [!INCLUDE[d365fin](includes/d365fin_md.md)] vérifie si l'utilisateur est autorisé à modifier la table **Ligne vente**. S'il n'est pas autorisé à le faire, le codeunit ne peut pas effectuer ses tâches et l'utilisateur reçoit un message d'erreur. S'il est autorisé à le faire, le codeunit s'exécute.

L'utilisateur n'a toutefois pas besoin d'avoir entièrement accès à la table **Ligne vente** pour exécuter le codeunit. Si une autorisation indirecte a été accordée à l'utilisateur pour la table **Ligne vente**, alors le codeunit **Ventes-Valider** s'exécute. Lorsqu'une autorisation indirecte est accordée à un utilisateur, celui-ci peut uniquement modifier la table **Ligne vente** en exécutant le codeunit **Ventes-Valider** ou un autre objet autorisé à modifier la table **Ligne vente**. L'utilisateur peut uniquement modifier la table **Ligne vente** lorsqu'il procède à partir des modules pris en charge. L'utilisateur ne peut pas exécuter cette fonctionnalité par inadvertance ou par malveillance en suivant d'autres méthodes.

## <a name="to-set-up-user-time-constraints"></a>Pour configurer des contraintes de temps utilisateur
Les administrateurs peuvent définir les périodes de temps pendant lesquelles les utilisateurs spécifiés peuvent valider, et spécifier également si le système enregistre la durée pendant laquelle les utilisateurs spécifiés ont ouvert une session. Les administrateurs peuvent également affecter des centres de gestion à des utilisateurs.

1. Choisissez l'icône ![Page ou état pour la recherche](media/ui-search/search_small.png "icône Page ou état pour la recherche"), entrez **Paramètres utilisateur**, puis choisissez le lien associé.
2. Dans la fenêtre **Paramètres utilisateur**, sélectionnez l'action **Nouveau**.
3. Dans le champ **ID utilisateur**, entrez l'ID d'un utilisateur, ou cliquez sur le champ pour visualiser tous les utilisateurs Windows actuels dans le système.
4. Renseignez les champs selon vos besoins.

## <a name="see-also"></a>Voir aussi
[Préparation aux activités commerciales](ui-get-ready-business.md)  
[Bienvenue dans [!INCLUDE[d365fin](includes/d365fin_md.md)]](index.md)  
[Utilisation de [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)  

