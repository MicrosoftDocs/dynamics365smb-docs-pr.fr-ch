---
title: Paramétrer des feuilles de temps et leur approbation
description: 'Vous paramétrez des feuilles de temps pour suivre le temps consacré aux tâches et aux projets, ce qui vous aide à gérer des projets, à recruter du personnel et à anticiper vos capacités'
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 'project management, capacity, staff, resource, time sheet'
ms.search.form: '977, 462, 76, 77'
ms.date: 12/13/2021
ms.author: edupont
---
# <a name="set-up-time-sheets" />Paramétrer des feuilles de temps

Dans [!INCLUDE[prod_short](includes/prod_short.md)], les feuilles de temps gèrent l’enregistrement des heures sur une base hebdomadaire par incrément de sept jours. Elles permettent de suivre le temps consacré à des projets, et vous pouvez les utiliser pour enregistrer les heures ressource. Avant de pouvoir utiliser les feuilles de temps, vous devez spécifier quels utilisateurs en soumettront et comment vous souhaitez les configurer.  

> [!TIP]
> Dans [!INCLUDE [prod_short](includes/prod_short.md)], les utilisateurs de feuilles de temps sont des *ressources*. De cette façon, vous pouvez utiliser des feuilles de temps pour suivre le travail des personnes qui ne font pas partie des employés, par exemple. Pour suivre le travail de vos propres employés ou pour utiliser des feuilles de temps pour suivre les indisponibilités des employés, vous devez associer des *employés* à des *ressources* dans le guide d’installation.  

Vous pouvez également spécifier si et comment les feuilles de temps sont approuvées. Selon les besoins de votre organisation, vous pouvez désigner :

* un ou plusieurs utilisateurs en tant qu’administrateur et approbateur de feuille de temps pour toutes les feuilles de temps ;
* un approbateur de feuille de temps pour chaque ressource.

Lorsque vous créez des feuilles de temps, vous pouvez en créer pour les ressources, et les ressources peuvent valider les lignes de feuille de temps. Pour pouvez affecter des feuilles de temps à des lignes planning projet. Pour plus d’informations, voir [Utiliser des feuilles de temps](projects-how-use-time-sheets.md).  

## <a name="set-up-time-sheets-with-the-assisted-setup-guide" />Paramétrer des feuilles de temps avec le guide de configuration assistée

[!INCLUDE [2021_releasewave2](includes/2021_releasewave2.md)]

À partir de la deuxième vague de lancement 2021, vous pouvez utiliser un guide de configuration assistée pour faciliter le paramétrage des feuilles de temps.  

> [!TIP]
> Vous devez activer la fonctionnalité **Mise à jour des fonctionnalités : nouvelle expérience de feuille de temps** dans la page [Gestion des fonctionnalités](https://businesscentral.dynamics.com/?page=2610) pour utiliser cette fonctionnalité.
>
> La même fonctionnalité facilite également la gestion des feuilles de temps sur un appareil mobile.

Ouvrez le guide de configuration assistée **Paramétrer des feuilles de temps** sur la page [Configuration assistée](https://businesscentral.dynamics.com/?page=1801).

Le guide de configuration assistée vous guide à travers les étapes suivantes :

1. Configurer les participants aux processus de feuille de temps

    La première page du guide vous indique le nombre d’utilisateurs de votre [!INCLUDE [prod_short](includes/prod_short.md)]. Elle indique également d’autres informations obligatoires et facultatives.  
2. Spécifier le premier jour d’une semaine de travail dans cette organisation

    Le premier jour d’une semaine de travail sera le premier jour par défaut pour toutes les feuilles de temps.
3. Spécifier la personne qui administre les feuilles de temps

    Cette personne peut modifier et supprimer toutes les feuilles de temps. Vous pouvez éventuellement ajouter le même rôle à d’autres personnes dans la page **Paramètres utilisateur**.
4. Configurer les ressources qui utiliseront les feuilles de temps et les personnes qui approuveront les feuilles de temps

À la fin de la configuration guidée, vous pouvez choisir de laisser [!INCLUDE [prod_short](includes/prod_short.md)] créer des feuilles de temps en fonction de votre configuration. Consultez les nouvelles feuilles de temps sur la page **Feuilles de temps** que vous pouvez ouvrir [ici](https://businesscentral.dynamics.com/?page=951). Vous pouvez également exécuter à nouveau le guide de configuration assistée ou terminer la configuration manuellement.  

## <a name="set-up-time-sheets-manually" />Paramétrer des feuilles de temps manuellement

Les sections suivantes décrivent comment configurer des feuilles de temps si vous n’utilisez pas le guide de configuration assistée **Paramétrer des feuilles de temps**.  

### <a name="to-set-up-general-information-for-time-sheets-manually" />Pour configurer manuellement des informations générales pour les feuilles de temps

1. Sélectionnez l’icône en forme ![d’Ampoule qui ouvre la fenêtre de recherche.](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire") saisissez **Configuration des ressources.**, puis choisissez le lien associé.  
2. Renseignez les champs selon vos besoins. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
3. Sélectionnez l’une des options suivantes pour le champ **Feuille de temps par approbation de projet**.

| Option | Désignation |
| --- | --- |
| **Jamais** |L’utilisateur du champ **ID utilisateur de l’approbateur de la feuille de temps** de la fiche ressource approuve la feuille de temps. |
| **Toujours** |L’utilisateur du champ **Responsable** de la fiche projet approuve la feuille de temps. |
| **Poste uniquement** |Si la feuille de temps poste est liée à un projet, alors l’utilisateur du champ **Responsable** spécifié sur la fiche projet approuve la feuille de temps. Si la feuille de temps poste est liée à une ressource, alors l’utilisateur du champ **ID utilisateur de l’approbateur de la feuille de temps** spécifié sur la fiche ressource approuve la feuille de temps. |

### <a name="to-assign-a-time-sheet-administrator-manually" />Pour affecter manuellement un administrateur de feuille de temps

1. Sélectionnez l’icône en forme ![d’Ampoule qui ouvre la fenêtre de recherche.](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire") saisissez **Paramètres utilisateur**, puis choisissez le lien associé.  
2. Ajoutez un nouvel utilisateur (si la personne que vous souhaitez désigner en tant qu’administrateur de feuille de temps ne figure pas dans la liste des utilisateurs). Pour en savoir plus, voir [Attribuer des autorisations aux utilisateurs et aux groupes](ui-define-granular-permissions.md).
3. Sélectionnez l’utilisateur qui deviendra l’administrateur de feuille de temps et sélectionnez la case à cocher **Admin. feuille de temps**.  

> [!TIP]  
> Il est recommandé de ne désigner qu’un seul utilisateur en tant qu’administrateur de feuille de temps dans une société. Dans la procédure suivante, vous devez configurer un propriétaire et un approbateur de feuille de temps et affecter l’approbateur à chaque ressource.  

### <a name="to-assign-a-time-sheets-owner-and-approver-manually" />Pour affecter manuellement un propriétaire et un approbateur de feuille de temps

1. Sélectionnez l’icône en forme ![d’Ampoule qui ouvre la fenêtre de recherche.](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire") saisissez **Ressources**, puis choisissez le lien associé.
2. Sélectionnez la ressource pour laquelle vous souhaitez configurer la capacité d’utiliser des feuilles de temps, puis sélectionnez la case à cocher **Utiliser la feuille de temps**.  
3. Entrez l’ID du propriétaire de la feuille de temps dans le champ **ID utilisateur du propriétaire de la feuille de temps**. Le propriétaire peut entrer le temps d’utilisation dans une feuille de temps et la soumettre pour approbation. En règle générale, lorsque la ressource est une personne, cette personne est également le propriétaire.  
4. Entrez l’ID de l’approbateur de la feuille de temps dans le champ **ID utilisateur de l’approbateur de la feuille de temps**. L’approbateur peut approuver, rejeter ou rouvrir une feuille de temps.  

> [!NOTE]  
> Vous ne pouvez pas modifier l’ID de l’approbateur de feuille de temps s’il existe des feuilles de temps qui n’ont pas encore été traitées et dont le statut est **Soumis** ou **En cours**.

## <a name="see-related-microsoft-trainingtrainingpathsset-up-jobs-resources" />Voir la [formation Microsoft](/training/paths/set-up-jobs-resources/) associée

## <a name="see-also" />Voir aussi

[Utiliser des feuilles de temps pour des projets](projects-how-use-time-sheets.md)  
[Procédure : créer des feuilles de temps](projects-how-use-time-sheets.md#to-create-time-sheets)  
[Enregistrer la consommation ou l′utilisation pour les projets](projects-how-record-job-usage.md)  
[Configuration de la gestion de projets](projects-setup-projects.md)  
[Gestion de projets](projects-manage-projects.md)  
[Finances](finance.md)  
[Achats](purchasing-manage-purchasing.md)  
[Ventes](sales-manage-sales.md)  
[Utiliser [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
