---
title: Partage de données
description: Découvrez les différentes façons de partager des données métier à partir de Business Central.
author: jswymer
ms.topic: conceptual
ms.workload: na
ms.search.keywords: null
ms.date: 09/21/2022
ms.author: jswymer
---
# <a name="sharing-business-data-from-business-central"></a>Partage de données métier à partir de Business Central

La collaboration entre les personnes à l’intérieur et à l’extérieur d’une organisation fait partie intégrante de la plupart des entreprises. [!INCLUDE[prod_short](includes/prod_short.md)] offre plusieurs fonctionnalités pour partager des données métier, comme une liste d’enregistrements, des enregistrements spécifiques ou des documents. <!--, with others&mdash;even those people who don't have a Business Central license in some cases.-->

Avec toutes ces fonctionnalités, l’accès aux données est protégé par la licence et les autorisations de Business Central.

## <a name="copying-a-link"></a>Copie d’un lien

![Prise en charge](media/check.png) Business Central Online ![Prise en charge](media/check.png) Business Central sur site

À partir de n’importe quelle page, vous pouvez copier l’URL de la page, puis la coller et la distribuer dans d’autres formes de médias comme des e-mails, des discussions Teams ou des messages texte. Le moyen le plus simple de copier un lien consiste à sélectionner **Partager** > **Copier le lien** en haut de la page. Une autre méthode consiste à copier l’URL directement à partir de la zone d’adresse du navigateur.

Lorsque vous collez l’URL dans un éditeur de texte enrichi, comme Word, Outlook ou Teams, au lieu d’afficher l’URL complète, le lien reçoit un nom plus lisible qui indique clairement le contexte de la cible. Le nom et le modèle varient en fonction de la page vers laquelle vous créez un lien. Prenez en compte les exemples suivants :

|Modèle|Exemple de page|Nom du lien|
|-|-|-|
|Pages de liste|Page de liste **Articles** | **Articles**|
|Vue de liste| **Ouvrir** la vue filtrée dans la liste **Commandes vente**|**Commandes vente - Ouvertes**|
| Enregistrement unique|Fiche article affichant un enregistrement unique|« Fiche article - 1896 ∙ Bureau ATHÈNES »|
|Brouillons d’enregistrements| Nouvelle fiche client|**Nouveau - Fiche client**|
|Entreprise qui utilise un badge|Page de liste **Articles** pour l’entreprise avec un badge **CRONUS**| **Articles (CRONUS)**|

> [!TIP]
> Une convention d’affectation de noms similaire est utilisée dans les onglets du navigateur.

### <a name="share-data-analysis"></a>Partager l’analyse des données
Si vous affichez une page ou une requête en mode d’analyse des données, vous pouvez partager un onglet d’analyse spécifique en sélectionnant la pointe de la flèche vers le bas dans l’onglet, puis en sélectionnant **Copier le lien**. [En savoir plus sur le mode d’analyse des données](analysis-mode.md). 

### <a name="modify-the-page-link"></a>Modifier le lien de la page

Après avoir copié un lien, avant de l’envoyer, vous pouvez modifier l’URL pour manipuler ce qui s’affiche lorsque la page s’ouvre. Vous pouvez, par exemple, ajouter des filtres ou spécifier une autre société.

[En savoir plus sur l’URL du client Web](/dynamics365/business-central/dev-itpro/developer/devenv-web-client-urls).

### <a name="about-filtered-lists"></a>À propos des listes filtrées

À l’aide du volet Filtre sur les pages de liste, vous pouvez appliquer des filtres pour affiner les enregistrements affichés dans la liste. Si vous utilisez l"action **Copier le lien** ou copiez l’URL à partir du navigateur, le lien de la page n’inclura pas les modifications apportées au filtre. Les utilisateurs qui ouvrent le lien voient la collection complète. La façon de conserver le filtrage sur un lien de page de collection consiste à d’abord enregistrer la page filtrée en tant que **Vue**. Ensuite, ouvrez la vue et copiez le lien à partir de là.

[En savoir plus sur le tri, la recherche et le filtrage](ui-enter-criteria-filters.md).

## <a name="sharing-to-teams"></a>Partage dans Teams

![Prise en charge](media/check.png) Business Central Online ![Non pris en charge](media/x-icon.png) Business Central sur site

Directement à partir de la plupart des pages de collection et de détails, vous pouvez envoyer un lien vers la page à des personnes, des discussions de groupe ou des canaux. Par exemple, partagez un lien vers une vue filtrée de vos enregistrements. Si vous avez installé l’application [!INCLUDE[prod_short](includes/prod_short.md)] pour Teams, le lien se développera automatiquement en une fiche compacte que vous pourrez inclure dans votre message. Les destinataires sélectionnent ensuite le lien ou la fiche pour ouvrir la page dans Business Central.

[En savoir plus sur le partage d’enregistrements et de liens de page dans Teams](across-working-with-teams.md).

## <a name="sharing-through-onedrive"></a>Partage dans OneDrive

![Prise en charge](media/check.png) Business Central Online ![Prise en charge](media/check.png) Business Central sur site

Business Central facilite le stockage, la gestion et le partage de fichiers avec d’autres personnes via OneDrive Entreprise. Sur la plupart des pages où les fichiers sont disponibles, comme la Boîte de réception état ou les fichiers joints à des enregistrements, vous trouverez les actions **Ouvrir dans OneDrive** et **Partager**. Les deux actions enregistrent une copie d’un fichier dans OneDrive. Une fois dans OneDrive, vous pouvez utiliser ses fonctionnalités de partage et de contribution sur le fichier. Voici la différence entre les deux actions : **Ouvrir dans OneDrive** ouvre le fichier dans OneDrive. **Partager** ouvre une page qui vous permet de sélectionner les personnes avec qui vous souhaitez partager le fichier. Les destinataires reçoivent un e-mail de notification pour accéder au fichier depuis votre OneDrive.

[En savoir plus sur le partage de fichiers dans OneDrive](across-share-onedrive.md).

## <a name="opening-in-excel"></a>Ouverture dans Excel

![Prise en charge](media/check.png) Business Central Online ![Prise en charge](media/check.png) Business Central sur site

Pour les pages de liste et les listes intégrées à une page, vous pouvez utiliser l’action **Ouvrir dans Excel**. Cette action exporte la liste des enregistrements vers un classeur Excel (fichier .xlsx), que vous pouvez partager avec d’autres personnes. Dans le classeur, vous pouvez également utiliser la fonctionnalité Partager qui fait partie d’Excel.

[En savoir plus sur l’affichage et la modification dans Excel](across-work-with-excel.md).

## <a name="sharing-rows-or-tables"></a>Partage de lignes ou de tableaux

![Prise en charge](media/check.png) Business Central Online ![Prise en charge](media/check.png) Business Central sur site

Vous pouvez partager un ou plusieurs enregistrements dans une liste. Sélectionnez simplement le raccourci clavier <kbd>Ctrl</kbd>+<kbd>C</kbd> pour copier dans votre presse-papiers. Collez ensuite ce que vous avez copié dans une autre application en appuyant sur <kbd>Ctrl</kbd>+<kbd>V</kbd>. Par exemple, copier trois bons de commande et les coller dans un e-mail affichera les commandes dans un tableau bien formaté.

[En savoir plus sur la copie et le collage dans la FAQ](faq-copy-paste.yml).

## <a name="see-also"></a>Voir aussi

[Intégration de Business Central et OneDrive](across-onedrive-overview.md)  
[Gestion de l’intégration de OneDrive avec Business Central](admin-onedrive-integration.md)  
[FAQ sur OneDrive](admin-onedrive-faq.md)
