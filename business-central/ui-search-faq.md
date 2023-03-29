---
title: Foire aux questions sur la fonction Tell Me
description: Cet article fournit des réponses aux questions que nos partenaires et clients posent souvent sur la fonction Tell Me.
author: brentholtorf
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: find
ms.search.form: TellMe
ms.date: 05/23/2022
ms.author: bholtorf
---
# FAQ Tell Me
Cet article répond aux questions que nos utilisateurs expérimentés posent souvent à propos de la fonctionnalité de fenêtre de recherche (Tell Me).

### Toutes les actions de ma page actuelle sont-elles détectables dans Tell Me ?

Non. Les actions dans les parties, telles que la partie Lignes vente ou Récapitulatifs, ne sont pas affichées dans Tell Me.

### Les résultats dans Tell Me sont-ils filtrés par autorisations ?

Si l’utilisateur n’a pas AccessByPermissions, les actions ne s’affichent pas. Cependant, les pages et les états sont visibles dans les résultats mais nécessitent que l’utilisateur soit autorisé à y accéder. Un message s’affiche si l’utilisateur n’est pas autorisé à afficher l’objet.

### La fonction Tell Me affiche-t-elle le contenu de mes personnalisations ou des extensions tierces installées ?

Les actions, les pages et les états qui proviennent d’extensions sont extraits par la fonctionnalité de fenêtre de recherche (Tell Me). Pour des informations techniques sur la manière rédiger des pages et des états personnalisés détectables, voir [Ajout de pages et d’états à rechercher](/dynamics365/business-central/dev-itpro/developer/devenv-al-menusuite-functionality).

### Quelles sont les différences avec la recherche de page précédente ?

La recherche de page s’est transformée en Tell Me pour vous aider à obtenir rapidement des résultats. La recherche de page pouvait uniquement vous aider à accéder aux pages ou aux états. À un niveau technique, Tell Me n’est plus basé sur le concept MenuSuite hérité.

### J’utilise [!INCLUDE[prod_short](includes/prod_short.md)] local. La fonction Tell Me est-elle incluse ?

Vous pouvez utiliser la fonctionnalité de fenêtre de recherche (Tell Me) dans le client Web local pour trouver des actions, des pages et des états, mais pas les applications et les services de conseils sur AppSource.

### La fonction Tell Me est-elle disponible pour tous les facteurs d’écrans ?

Tell Me est uniquement disponible dans le client Web ou l’application de bureau Windows.

<!-- removed in v20 because of Help pane
### Are the documentation results available in any language?
The help articles display in the language you have specified in **My Settings**, if help is available in that language.
-->

### La fonctionnalité de fenêtre de recherche (Tell Me) m’aide-t-elle à utiliser les pages, les rapports et d’autres éléments ?

Non, mais vous pouvez facilement obtenir ces informations à partir du volet Aide. Sélectionnez simplement l’élément de menu **Aide** (le point d’interrogation dans le coin supérieur droit) ou sélectionnez <kbd>Ctrl</kbd>+<kbd>F1</kbd> sur votre clavier. Pour plus d’informations, voir [Volet Aide](product-help-and-support.md#help-pane).

### Pourquoi ne vois-je pas d’icône de signet pour mes résultats de recherche ?

L’icône de signet ne s’affiche pas dans la fenêtre Tell Me lorsque la personnalisation est désactivée pour un rôle d’utilisateur.


## Voir aussi  
[Enregistrer et personnaliser les vues de liste](ui-views.md)  
[Recherche de pages et d’informations avec la fonction Tell Me](ui-search.md)  
[Recherche de pages avec l’explorateur de rôles](ui-role-explorer.md)  
[Ajouter un signet à une page ou à un état sur votre tableau de bord](ui-bookmarks.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]