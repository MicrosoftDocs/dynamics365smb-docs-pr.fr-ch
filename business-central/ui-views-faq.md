---
title: Foire aux questions sur les vues de liste
description: Informations détaillées sur l’enregistrement des filtres en tant que vues de liste.
author: mikebcMSFT
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: list, filter, pane, views
ms.date: 10/01/2020
ms.author: mikebc
ms.openlocfilehash: 17d7c909865bc077097ba4299e07ed2dd9cedb22
ms.sourcegitcommit: ff2b55b7e790447e0c1fcd5c2ec7f7610338ebaa
ms.translationtype: HT
ms.contentlocale: fr-CH
ms.lasthandoff: 02/15/2021
ms.locfileid: "5392489"
---
# <a name="list-views-faq"></a>FAQ sur les vues de liste
Cet article répond aux questions fréquemment posées par nos utilisateurs expérimentés sur l’utilisation des vues de liste et la sauvegarde des filtres.  

### <a name="how-do-views-handle-expressions"></a>Comment les vues gèrent-elles les expressions ?

Lorsque vous enregistrez une vue qui inclut des filtres avec des expressions, telles que des plages de dates, des opérateurs, des mots-clés ou des jetons de filtre, l’expression est enregistrée, mais pas les valeurs obtenues. Par exemple, le fait d’enregistrer une vue qui filtre sur le champ **Date de création** avec l’expression `-1W..today` trouvera toujours les enregistrements relatifs à la date du jour, même lors de l’accès à la vue le mois prochain.

### <a name="where-are-list-views-saved"></a>Où les vues de liste sont-elles enregistrées ?

De la même manière que pour masquer un champ ou réorganiser votre menu de navigation, les vues de liste font partie de la personnalisation de l’utilisateur et sont stockées dans la base de données. Si vous effacez toutes les personnalisations d’une liste, vos vues personnelles seront également définitivement supprimées, de même que toute personnalisation supplémentaire telle que la réorganisation des vues. Pour plus d’informations, voir [Personnaliser votre espace de travail](ui-personalization-user.md).

### <a name="why-dont-i-have-a-save-icon"></a><a name="save"></a>Pourquoi n’ai-je pas d’icône Enregistrer ?

Il y a plusieurs raisons pour lesquelles vous pourriez ne pas voir l’icône Enregistrer et le menu d’options à côté des vues dans le volet de filtre.

L’une des raisons pourrait être que la personnalisation n’est pas activée pour votre rôle d’utilisateur. Dans ce cas, vous avez toujours accès aux vues système qui font partie intégrante des pages. Vous pouvez modifier ces vues, comme changer ou ajouter des filtres. Vous ne pouvez tout simplement pas enregistrer les modifications. Une autre raison pourrait être que la page que vous consultez est une page de type *feuille de travail*&mdash; pas une liste.

### <a name="on-which-page-types-can-i-use-list-views"></a>Sur quels types de page puis-je utiliser les vues de liste ?

Les vues ne sont disponibles que sur les pages de liste.

### <a name="how-do-i-know-whether-im-on-list-type-page"></a>Comment savoir si je suis sur une page de type liste ?

Utilisez l’inspection des pages. Pour ouvrir l’inspection des pages, appuyez sur Ctrl + Alt + F1. Puis, dans le champ **Page**, cherchez le mot **Liste** entre parenthèses à la fin.

### <a name="are-views-also-available-on-other-form-factors"></a>Les vues sont-elles également disponibles sur d’autres facteurs de forme ?

Oui. Toutes les vues que vous enregistrez sur votre navigateur ou application de bureau seront également disponibles sur votre tablette ou votre smartphone. Vous ne pouvez pas modifier ou personnaliser les vues sur les appareils mobiles.

### <a name="are-my-personal-views-always-accessible"></a>Mes vues personnelles sont-elles toujours accessibles ?

Vos vues sont disponibles sur une page de liste si vous y accédez depuis le menu de navigation, via la fenêtre **Rechercher** ou via un lien URL. Les vues ne sont pas disponibles dans les parties de liste, les recherches ou chaque fois qu’une page de liste est affichée sous forme de boîte de dialogue.

### <a name="how-do-i-return-a-view-to-its-original-filters-after-modifying-them"></a>Comment restaurer les filtres originaux d’une vue après les avoir modifiés ?

Au bas du volet Filtre, choisissez l’action **Réinitialiser les filtres** permettant d’effacer les modifications de filtre apportées à la vue et de revenir aux champs et critères de filtre d’origine.

### <a name="what-is-the-difference-between-hiding-and-removing-views"></a>Quelle est la différence entre masquer et supprimer des vues ?

Le fait de supprimer une vue supprime définitivement cette vue. Le fait de masquer une vue vous permet de la masquer temporairement dans le volet Filtre, mais vous pouvez la réafficher ultérieurement en choisissant l’action **Afficher**.

### <a name="how-can-i-share-my-views-with-others"></a>Comment puis-je partager mes vues avec d’autres ?

[!INCLUDE[prod_short](includes/prod_short.md)] ne fournit pas un moyen de partager la vue de liste précise. Mais vous pouvez partager vos filtres actuels afin que les autres utilisateurs puissent voir une liste similaire d’enregistrements. Dans le navigateur de votre ordinateur de bureau, copiez simplement l’URL et partagez-la avec vos collègues. Le partage des filtres ne garantit pas au destinataire un ensemble de filtres identique à celui que vous voyez dans votre navigateur.

### <a name="can-i-search-for-views-in-the-tell-me-window"></a>Puis-je rechercher des vues dans la fenêtre Tell Me ?

Non. La fenêtre **Rechercher** n’affiche que les résultats de la recherche pour la page, mais il ne vous reste plus qu’à accéder à votre vue préférée une fois que vous avez accédé à la page.

### <a name="what-is-shared-layout"></a>Qu’est-ce qu’une disposition partagée ?

Toutes les vues d’une page de liste partagent une disposition de colonne commune. La mise en page inclut les colonnes affichées, leur séquence, leur largeur, le volet figé et les paramètres de saisie rapide. La personnalisation de la disposition des colonnes affectera également les autres vues partageant la même disposition sur la page de liste.

Certaines vues système peuvent avoir des présentations uniques des colonnes de la liste. Par exemple, elles peuvent réorganiser les colonnes pour n’afficher que celles qui sont les plus pertinentes pour cette vue. Vous pouvez identifier les vues ayant des présentations uniques en choisissant l’icône ![Afficher plus d’options](media/show-more-options-icon.png "Afficher plus d’options") et en vérifiant que la case à cocher **Disposition partagée** n’est pas sélectionnée. En tant qu’utilisateur, vous pouvez personnaliser la disposition des colonnes pour une vue avec une disposition unique sans que cela affecte les autres vues de la page de liste. Seuls les développeurs peuvent définir une disposition de colonne unique pour une vue qui a initialement une disposition partagée.

### <a name="what-does-the-show-system-filters-link-do"></a>Que fait le lien Afficher filtres système ?

Sur certaines pages de liste, le volet Filtre affiche **Afficher filtres système** en bas, notamment lorsque la page comprend des filtres spécifiés par le système. Ces filtres spéciaux sont généralement utilisés pour afficher les enregistrements en fonction du contexte actuel. Un exemple serait lorsqu’une liste de commandes doit être filtrée pour un client spécifique.

Les filtres système sont définis par les développeurs d’application, qu’ils définissent en utilisant le groupe de filtres 0. Pour plus de détails sur les filtres système, voir [Méthode de groupe de filtres](/dynamics365/business-central/dev-itpro/developer/methods-auto/record/record-filtergroup-method).

### <a name="i-see-multiple-views-on-my-page-but-i-didnt-create-them-where-did-they-come-from"></a>Je vois plusieurs vues sur ma page, mais je ne les ai pas créées. D’où viennent-ils ?

Les vues que vous voyez sur une liste sont une combinaison de vos vues personnelles avec des vues système. Les vues système peuvent provenir de l’application métier, des extensions ou être spécifiques à un rôle si la liste a été personnalisée pour votre rôle.

### <a name="why-do-some-views-provide-fewer-options"></a>Pourquoi certaines vues offrent-elles moins d’options ?

Certaines vues offrent uniquement la possibilité d’enregistrer une copie de la vue, tandis que d’autres n’autorisent pas l’enregistrement des modifications apportées à la vue. Comment le mode de création de la vue détermine-il les options disponibles pour cette vue , Les vues peuvent être créées de plusieurs manières :

- Vues personnelles que vous avez enregistrées
- Les vues système qui font partie de l’application métier ou qui sont ajoutées par des extensions ou des vues spécifiques à un rôle. Contrairement aux vues personnelles, vous ne pouvez pas enregistrer les modifications apportées aux filtres dans cette vue système.
- Les vues système héritées faisant partie de l’application métier mais ayant été créées à l’aide de versions antérieures de [!INCLUDE[prod_short](includes/prod_short.md)]. Ces vues offrent moins d’options. Vous ne pouvez les enregistrer que dans une nouvelle vue et vous ne pouvez pas non plus les masquer ou les réorganiser. Les vues système héritées seront supprimées lors d’une prochaine mise à jour [!INCLUDE[prod_short](includes/prod_short.md)].

### <a name="how-do-i-convert-legacy-system-views"></a>Comment convertir des vues système héritées ?

Les vues système héritées sont des vues de liste créées par les développeurs d’anciennes versions de [!INCLUDE[prod_short](includes/prod_short.md)] en les plaçant sur la page Tableau de bord. Ces vues sont maintenant affichées directement sur la page de liste, mais elles offrent une expérience plus mauvaise et moins d’options. Vous pouvez convertir une vue système héritée en une vue personnelle entièrement personnalisable, simplement en enregistrant cette vue héritée en tant que nouvelle vue. De même, les administrateurs peuvent choisir de convertir les vues système héritées spécifiques à un rôle en personnalisant le rôle d’utilisateur et en enregistrant la vue héritée en tant que nouvelle vue spécifique à un rôle.

Les vues système héritées seront supprimées lors d’une prochaine mise à jour [!INCLUDE[prod_short](includes/prod_short.md)].

### <a name="others-in-my-organization-need-similar-list-views-as-standard-what-can-i-do"></a>D’autres membres de mon organisation ont besoin de vues de liste similaires en standard. Que puis-je faire ?

Le fait d’utiliser des vues personnelles est rapide et efficace, mais [!INCLUDE[prod_short](includes/prod_short.md)] fournit des outils supplémentaires pour définir les vues de liste nécessaires à des rôles d’utilisateur spécifiques ou à tous les utilisateurs de l’organisation.
 - Les développeurs peuvent personnaliser l’environnement et créer des vues de liste dans des extensions pour tous les utilisateurs de l’organisation.
 - Les non-codeurs, tels que les administrateurs ou les chefs de service, peuvent créer des vues de liste spécifiques à un rôle lors de la personnalisation d’un rôle à partir de la page **Profils (rôles)**.

### <a name="i-work-with-multiple-languages-how-do-i-translate-the-name-of-the-view"></a>Je travaille avec plusieurs langues : comment traduire le nom de la vue ?

Lorsque vous enregistrez une nouvelle vue ou renommez une vue existante, vous devez entrer un nom reconnaissable et significatif pour cette vue. Le nom est enregistré pour votre langue actuelle et sera également affiché lorsque vous ou d’autres utilisateurs utiliserez [!INCLUDE[prod_short](includes/prod_short.md)] dans différentes langues. Pour fournir des noms de vue traduits, changez de langue à l’aide de la page **Mes paramètres**. Renommez ensuite la vue, qui stockera le nom traduit dans la nouvelle langue.

### <a name="do-views-with-expressions-work-in-all-languages"></a>Les vues avec des expressions fonctionnent-elles dans toutes les langues ?

Les expressions n’utilisant que des symboles, tels que `|` ou `..`, sont considérés comme sûrs pour les utilisateurs dans toutes les langues. Toutes les vues contenant des expressions comprenant des lettres, des mots-clés ou des jetons de filtre ne fonctionneront que pour la langue dans laquelle elles ont été créées.

### <a name="see-also"></a>Voir aussi

[Enregistrer et personnaliser les vues de liste](ui-views.md)  
[Recherche de fonctions et d'informations](ui-search.md)  
[Tri, recherche et filtrage](ui-enter-criteria-filters.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]