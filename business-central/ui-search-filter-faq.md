---
title: À propos de la recherche et du filtrage dans Business Central
description: Réponses aux questions posées fréquemment sur la recherche et le filtre.
author: mikebcMSFT
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.reviewer: edupont04
ms.search.keywords: keyboarding, productivity, how do i, filter pane
ms.date: 11/16/2020
ms.author: mikebc
ms.openlocfilehash: debbf621795564344f11609236b2faac397c6762
ms.sourcegitcommit: ff2b55b7e790447e0c1fcd5c2ec7f7610338ebaa
ms.translationtype: HT
ms.contentlocale: fr-CH
ms.lasthandoff: 02/15/2021
ms.locfileid: "5386814"
---
# <a name="searching-and-filtering-faq"></a>FAQ sur la recherche et le filtrage
Cet article répond à des questions courantes que vous pouvez avoir à propos de la recherche et du filtrage.

## <a name="is-there-a-difference-between-searching-and-filtering"></a>Existe-t-il une différence entre la recherche et le filtrage ?
Oui.
- La recherche est simple et large : elle faire correspondre des enregistrements contenant le texte de recherche dans tous les champs visibles de la page, puis ne respecte pas la casse.
- Le filtrage est très flexible et peut être appliqué à des champs spécifiques, notamment ceux qui ne sont pas visibles dans la page : il affiche les enregistrements qui comportent des correspondances exactes et respectant la casse, mais il peut être ajusté avec des symboles, des jetons et des formules de recherche puissants. Pour plus d’informations sur l’utilisation de ces fonctions, voir [Tri, recherche et filtrage](ui-enter-criteria-filters.md).

## <a name="exactly-which-fields-are-matched-when-searching"></a>Quels champs correspondent exactement lors de la recherche ?
[!INCLUDE[prod_short](includes/prod_short.md)] applique les critères de recherche à tous les champs visibles sur la page. Si un champ a été masqué, par exemple en utilisant la personnalisation, la recherche ne tiendra pas compte de ce champ. Les critères de recherche sont appliqués aux champs uniquement si leur type de données correspond à celui des critères de recherche. Par exemple, rechercher le terme *aujourd’hui* recherchera dans tous les champs de texte et de code la valeur littérale « aujourd’hui », ainsi que dans tous les champs de date où *aujourd’hui* est évalué comme une expression pour la date actuelle, mais ne recherche dans aucun champ numérique. Pour plus d’informations sur les critères de filtre, voir [Tri, recherche et filtrage](ui-enter-criteria-filters.md#-filter-criteria-and-operators).

## <a name="is-there-a-keyboard-experience-for-search-and-filter"></a>Existe-t-il une expérience clavier pour la recherche et le filtre ?
La recherche et le filtre ont été fortement optimisés pour les utilisateurs qui préfèrent l’interaction sans souris pour utiliser efficacement leurs données. Il existe un grand choix de touches de raccourci qui peuvent être utilisées dans l’ordre pour travailler à grande vitesse. Pour plus d’informations, reportez-vous à [Raccourcis clavier](keyboard-shortcuts.md#KeyboardFilter).

## <a name="is-the-filter-pane-available-on-all-lists"></a>Le volet Filtre est-il disponible sur toutes les listes ?
Le volet Filtre est disponible sur les pages où la liste est le principal contenu sur la page, tels que des feuilles de calcul et des pages de liste, y compris les listes accessibles depuis la barre de navigation. Le volet Filtre n’est pas encore disponible pour les listes qui s’affichent sous forme de parties, telles que les Récapitulatifs ou les parties du tableau de bord, ou pour les listes affichées sous forme de boîtes de dialogue, comme dans les recherches. Lorsqu’une liste est intégrée sur une page, comme des lignes vente dans une commande vente, le volet Filtre est disponible lorsque vous vous focalisez sur cette liste à l’aide du bouton Mode focalisation. Pour en savoir plus, reportez-vous à la rubrique [Concentration sur les articles de ligne](ui-enter-data.md#Focus).

## <a name="how-can-i-save-my-filters"></a>Comment enregistrer mes filtres ?
Vos filtres et ajustements des filtres prédéfinis sont enregistrés tout au long de la session (lorsque vous restez connecté), même si vous quittez la page. Vous pouvez enregistrer les filtres de manière permanente en tant que vue nommée de la liste en choisissant l’icône ![Enregistrer la vue](media/save_view_icon.png "Enregistrer la vue") dans le volet Filtre. Pour plus d’informations, voir [FAQ sur les vues de liste](ui-views-faq.md). Notez que, contrairement aux filtres, le texte de recherche n’est pas mémorisé lorsque vous quittez une page et n’est pas enregistré lorsque vous enregistrez une vue.

Sur les pages de demande de rapport, vous pouvez également enregistrer des filtres ou utiliser des filtres prédéfinis. Pour plus d’informations, voir [Utilisation des paramètres enregistrés](ui-work-report.md#SavedSettings).

## <a name="is-this-the-same-as-advanced-filters-and-limit-totals-in-microsoft-dynamics-nav"></a>Est-ce pareil qu’avec les filtres avancés et les totaux de limite dans Microsoft Dynamics NAV ?
[!INCLUDE[prod_short](includes/prod_short.md)] s’appuie sur ces fonctions populaires et présente une expérience moderne et extrêmement utilisable pour rechercher et analyser vos données. Avec plus de raccourcis clavier et l’introduction de la recherche, [!INCLUDE[prod_short](includes/prod_short.md)] surpasse la fonctionnalité fournie dans Dynamics NAV.  

## <a name="can-i-search-and-filter-using-the-companion-apps-and-add-ins-for-microsoft-365"></a>Puis-je rechercher et filtrer à l’aide des applications complémentaires pour Microsoft 365 ?
Sur différentes cibles d’affichage, telles que des appareils mobiles ou dans Outlook, vous pouvez rechercher dans les listes mais ne pouvez pas filtrer sur les différents champs dans la plupart des cas. Dans l’application [!INCLUDE[prod_short](includes/prod_short.md)] pour Microsoft Teams, la recherche et le filtre sont disponibles sur les listes.

## <a name="how-do-i-view-how-my-search-terms-have-been-applied-to-fields-in-the-list"></a>Comment voir comment mes termes de recherche ont été appliqués aux champs de la liste ?
Après avoir saisi les termes de recherche dans la zone de recherche, vous pouvez afficher les critères de recherche exacts et les champs auxquels ils ont été appliqués en ouvrant le volet d’inspection de page (**Ctrl + Alt + F1**) et en choisissant l’onglet **Filtres de page**.

## <a name="can-i-do-anything-about-the-searching-for-rows-is-taking-too-long-message"></a>Puis-je faire quelque chose concernant le message « La recherche de lignes prend trop de temps » ?

Il existe une limite de temps concernant une opération de recherche. Premièrement, essayez de modifier les critères de recherche et recherchez à nouveau. Si vous utilisez [!INCLUDE[prod_short](includes/prod_short.md)] local, contactez votre administrateur système, parce qu’un administrateur peut augmenter le délai des recherches.

En tant qu’administrateur local, vous développez le délai des recherches en modifiant le paramètre **Expiration de la recherche** du serveur [!INCLUDE[prod_short](includes/prod_short.md)]. Pour plus d’informations, voir [Configuration de Business Central Server](/dynamics365/business-central/dev-itpro/administration/configure-server-instance?#Database) dans l’Aide destinée aux développeurs et aux professionnels de l’informatique Business Central.

## <a name="will-microsoft-extend-the-filter-pane-experience"></a>Microsoft étendra-il l’expérience du volet Filtre ?
Chez Microsoft, nous écoutons constamment les commentaires de notre communauté diverse d’utilisateurs et prenons les mesures nécessaires pour agir sur les principales propositions de la communauté. Si vous souhaitez étendre le volet Filtre à plus de facteurs d’écrans et plus de types de listes et d’états, ou que vous avez une excellente idée pour l’améliorer, ajoutez une idée ou votez pour les idées existantes à l’adresse [aka.ms/BusinessCentralIdeas](https://aka.ms/businesscentralideas).

## <a name="see-also"></a>Voir aussi
[Tri, recherche et filtrage](ui-enter-criteria-filters.md)  
[Recherche de pages et d’informations avec Tell Me](ui-search.md)  
[Recherche de pages avec l’explorateur de rôles](ui-role-explorer.md)  
[Mise en route](product-get-started.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]