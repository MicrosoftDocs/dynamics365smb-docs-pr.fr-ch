---
title: Affichage et édition dans Excel depuis Business Central (contient une vidéo)
description: "En savoir plus sur la manière dont vous pouvez ouvrir les pages dans Microsoft Excel à partir de Business\_Central pour une meilleure analyse de données."
author: jswymer
ms.topic: conceptual
ms.devlang: al
ms.search.form: 1480
ms.search.keywords: 'accountant, accounting, financial report'
ms.date: 04/01/2021
ms.author: jswymer
ms.service: dynamics-365-business-central
---
# Affichage et édition dans Excel depuis Business Central

Avec des pages qui affichent une liste d’enregistrements dans des lignes et des colonnes, comme une liste de clients, de commandes client ou de factures, vous pouvez exporter la liste vers Microsoft Excel et l’y afficher. Selon la page, vous avez deux options pour l’affichage dans Excel. Les deux options sont disponibles à partir de l’icône **Partager** ![Partager une page dans une autre application.](media/share-icon.png) en haut d’une page. Vous pouvez sélectionner l’action **Ouvrir dans Excel** ou l’action **Modifier dans Excel** sur la page. Cet article explique les deux actions.

## Ouvrir dans Excel

Avec l’action **Ouvrir dans Excel**, vous pouvez apporter des modifications aux enregistrements dans Excel, mais vous ne pouvez pas publier les modifications dans [!INCLUDE[prod_short](includes/prod_short.md)]. Vous pouvez uniquement enregistrer les modifications dans le fichier Excel, sans affecter les données dans [!INCLUDE[prod_short](includes/prod_short.md)].

- Avec cette action, Excel tient compte de tous les filtres de la page qui limitent les enregistrements affichés. Le classeur Excel contiendra les mêmes lignes et colonnes figurant sur la page dans [!INCLUDE[prod_short](includes/prod_short.md)].

- Cette action fonctionne sur Windows et macOS.
- [!INCLUDE[open-edit-excel](includes/open-and-edit-excel.md)]

> [!IMPORTANT]
> Pour [!INCLUDE[prod_short](includes/prod_short.md)] sur site, l’action **Ouvrir dans Excel** est disponible par défaut. Cependant, si vous configurez [!INCLUDE[prod_short](includes/prod_short.md)] sur site pour la modification de données dans Excel, l’action **Ouvrir dans Excel** est alors remplacée par l’action **Modifier dans Excel**.

[!INCLUDE [send-report-excel](includes/send-report-excel.md)] 

> [!NOTE]
> Dans Excel, les nombres entiers dans les colonnes auront un symbole décimal à la fin (comme un point `.` ou une virgule `,`) même si le symbole décimal n’est pas affiché dans Business Central. Le symbole décimal dépend des paramètres régionaux de votre appareil. Par exemple, `10` dans Business Central peut apparaître comme `10.` ou `10,` dans Excel. Vous pouvez modifier le format dans Excel en sélectionnant les valeurs, puis en sélectionnant <kbd>Ctrl</kbd>+<kbd>1</kbd>. Pour en savoir plus sur la modification du format des nombres dans Excel, consultez [Format des nombres](https://support.microsoft.com/office/format-numbers-f27f865b-2dc5-4970-b289-5286be8b994a).


## Modifier dans Excel

L’action **Modifier dans Excel** est disponible sur la plupart des listes, mais pas toutes. Avec l’action **Modifier dans Excel**, vous pouvez apporter des modifications aux enregistrements dans Excel, mais vous ne pouvez pas publier les modifications dans [!INCLUDE[prod_short](includes/prod_short.md)]. À l’ouverture d’Excel, vous verrez le volet **Complément Excel** à droite.

- Avec cette action, Excel respecte la plupart des filtres de la page qui limitent les enregistrements affichés, de sorte que le classeur Excel contiendra presque les mêmes enregistrements et colonnes.

- Pour obtenir les dernières données de [!INCLUDE[prod_short](includes/prod_short.md)], choisissez **Actualiser** dans le volet Complément Excel.
- [!INCLUDE[open-edit-excel](includes/open-and-edit-excel.md)]

### Première connexion

L’action **Modifier dans Excel** nécessite que le complément Business Central soit installé dans Excel. Dans certains cas, votre administrateur peut avoir configuré le complément pour qu’il s’installe automatiquement pour vous. Dans ce cas, il vous suffit de vous connecter à Business Central dans le volet **Complément Excel** avec votre nom d’utilisateur et votre mot de passe. Sinon, le volet **Nouveau complément Office** s’ouvre. Pour installer le complément, sélectionnez **Faire confiance à ce complément**, ce qui a pour effet d’installer le complément directement depuis l’Office Store.

Si le complément ne s’installe pas, contactez votre administrateur ou essayez de l’installer manuellement. Pour plus d’informations, consultez [Installer le complément manuellement pour votre propre usage](admin-deploy-excel-addin.md#install).

### Travailler dans plusieurs environnements et sociétés

Vous pouvez changer la société en cours d’utilisation. Pour changer de société, sélectionnez l’icône **Options** ![Options de complément Excel.](media/cogwheel.png "Options du module complémentaire Excel") dans le volet Complément Excel, puis sélectionnez la société dans le champ **Société**.  

> [!IMPORTANT]
> Lors du changement de société, assurez-vous que le champ **Environnement** n’est pas vide. Si tel est le cas, définissez-le sur l’une des options disponibles ; sinon, le module complémentaire ne fonctionnera pas correctement.  

Si vous apportez des modifications au module complémentaire, vous devez le recharger afin de mettre à jour la connexion. Pour recharger, utilisez le ![menu Module complémentaire Excel](media/excel-addin-menu.png "Menu Module complémentaire Excel") dans le coin supérieur droit du module complémentaire. Si vous ne pouvez pas charger le complément, parlez-en à votre administrateur. Si vous êtes l’administrateur, consultez [Obtenir le complément Business Central pour Excel](admin-deploy-excel-addin.md).

> [!NOTE]
> Le complément fonctionne avec Excel pour le Web (en ligne) à partir de n’importe quel appareil, à condition d’utiliser un navigateur pris en charge. Il fonctionne également avec l’application Excel pour Windows (PC), mais pas pour macOS.
>
> Pour [!INCLUDE[prod_short](includes/prod_short.md)] sur site, l’action **Modifier dans Excel** est disponible seulement si le module complémentaire Excel a été configuré par votre administrateur, et uniquement pour le client web. Pour les administrateurs, si vous souhaitez connaître la manière de configurer le module complémentaire Excel, consultez [Configuration du module complémentaire Excel pour modifier des données Business Central](/dynamics365/business-central/dev-itpro/administration/configuring-excel-addin).

### Limites lors de l’utilisation d’Excel pour le Web 

Lorsque vous utilisez **Modifier dans Excel** sur les pages de liste pour les tables comportant de nombreuses colonnes, le classeur résultant peut comporter trop de colonnes pour que le fichier puisse être affiché dans Excel pour le Web. [!INCLUDE[prod_short](includes/prod_short.md)] limite automatiquement le classeur exporté à 100 colonnes lorsque OneDrive est configuré pour les fonctionnalités du système. 

## Voir les différences entre les options
<br><br>  

> [!Video https://go.microsoft.com/fwlink/?linkid=2086039]

## Voir aussi

[Analyse des états financiers dans Microsoft Excel](finance-analyze-excel.md)  
[Utiliser Business Central](ui-work-product.md)  
[Améliorations de l’intégration d’Excel dans la deuxième vague de publication 2019](/dynamics365-release-plan/2019wave2/dynamics365-business-central/enhancements-excel-integration)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
