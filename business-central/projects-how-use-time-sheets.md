---
title: Utiliser des feuilles de temps
description: 'Décrit comment créer une feuille de temps, définir les types de travaux, renseigner la feuille de temps et la soumettre pour approbation.'
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 'project management, capacity, staff, resource, time sheets'
ms.search.form: '950, 951, 973'
ms.date: 03/01/2022
ms.author: edupont
---
# <a name="use-time-sheets"></a><a name="use-time-sheets"></a><a name="use-time-sheets"></a>Utiliser des feuilles de temps

Vous pouvez utiliser des feuilles de temps dans [!INCLUDE [prod_short](includes/prod_short.md)] pour suivre les indisponibilités et pour suivre le temps et les ressources consacrés à un projet. Grâce à la gestion du temps, vous pouvez anticiper les problèmes et éviter les retards ou les surcoûts. Grâce aux feuilles de temps, une ressource peut facilement enregistrer le temps d’utilisation d’une personne ou d’une machine, tandis qu’un administrateur peut facilement consulter l’activité d’une ressource et son affectation. Cet article décrit comment créer une feuille de temps, définir les types de travaux, renseigner la feuille de temps et la soumettre pour approbation.  

Vous pouvez copier et utiliser vos lignes planning projet dans une feuille de temps. Vous n’avez ainsi à entrer les informations qu’à un seul emplacement et les informations de ligne sont toujours correctes.

Une fois que vous avez approuvé les écritures des feuilles de temps d’un projet, vous pouvez les valider dans la feuille ressource ou projet correspondante.

Avant de pouvoir utiliser des feuilles de temps, vous devez définir des informations générales et spécifier un administrateur et un ou plusieurs approbateurs de feuilles de temps. Pour plus d’informations, voir [Paramétrer des feuilles de temps](projects-how-setup-time-sheets.md).  

> [!TIP]
> À partir de la deuxième vague de lancement 2021, vous pouvez gérer les feuilles de temps attribuées sur un appareil mobile. Toutefois, il est possible que votre administrateur doive activer la fonctionnalité **Mise à jour des fonctionnalités : nouvelle expérience de feuille de temps** dans la page [Gestion des fonctionnalités](https://businesscentral.dynamics.com/?page=2610) pour utiliser cette fonctionnalité. Pour plus d’informations, voir [Paramétrer des feuilles de temps](projects-how-setup-time-sheets.md).

## <a name="to-create-time-sheets"></a><a name="to-create-time-sheets"></a><a name="to-create-time-sheets"></a>Pour créer des feuilles de temps

Vous pouvez utiliser le traitement par lots **Créer des feuilles de temps** pour configurer des feuilles de temps pour un nombre donné de périodes ou de semaines. Une fois qu’une feuille de temps est créée, son propriétaire peut l’ouvrir et y enregistrer le temps consacré à une tâche. Vous pouvez également [planifier le traitement par lots pour une exécution automatique](ui-work-report.md#ScheduleReport).  

> [!IMPORTANT]
> Vous devez disposer d’autorisations pour pouvoir créer des feuilles de temps. Pour plus d’informations, voir [Paramétrer des feuilles de temps](projects-how-setup-time-sheets.md).

1. Sélectionnez ![l’icône en forme d’ampoule qui ouvre la fonction Tell Me.](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire") entrez **Feuilles de temps**, puis choisissez le lien associé.
2. Sur la page **Feuilles de temps**, choisissez l’action **Créer des feuilles de temps**.
3. Renseignez les champs selon vos besoins. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

    > [!NOTE]  
    > Les champs **Utiliser la feuille de temps** et **ID utilisateur du propriétaire de la feuille de temps** doivent être renseignés sur la fiche de la ressource de la feuille de temps.

    Si vous le souhaitez, vous pouvez choisir l’action **Planifier** afin de spécifier la fréquence à laquelle vous souhaitez que la tâche s’exécute automatiquement. Par exemple, pour configurer la tâche de façon à ce qu’elle s’exécute chaque semaine pendant quatre semaines, sur la page **Planifier un état – Créer des feuilles de temps**, définissez le champ **Formule de date de la prochaine exécution** sur *4W*. Pour en savoir plus, consultez [Planifier un état à exécuter](ui-work-report.md#ScheduleReport)  
4. Cliquez sur le bouton **OK**.  

Vous pouvez afficher les feuilles de temps que vous avez créées sur la page **Feuilles de temps**. Chaque feuille de temps se compose d’une ou plusieurs lignes qui définissent l’heure à laquelle vous souhaitez soumettre pour approbation. Le tableau suivant décrit les types de lignes que vous pouvez ajouter à la feuille de temps.

| **Champ** | **Description** |
|---|---|
| | Permet d’ajouter une note ou un marqueur dans le champ **Description** de la ligne feuille de temps. Par exemple, vous pouvez utiliser ce champ pour classer des écritures de la feuille de temps par catégorie. Si vous laissez le champ **Type** vide pour une ligne feuille de temps, vous ne pouvez pas entrer les valeurs de temps dans les champs de jour de la semaine pour cette ligne. |
| Indisponibilité | Permet d’enregistrer la durée de votre indisponibilité au cours d’une semaine de travail. Pour compléter les informations de la ligne, spécifiez le type d’indisponibilité dans le champ **Code motif indisponibilité**. |
| Ordre d’assemblage | Permet d’enregistrer la durée des ordres d’assemblage. Une ligne feuille de temps de ce type est créée lors de la validation des lignes d’ordre d’assemblage pour lesquelles la ressource est configurée afin d’utiliser des feuilles de temps. Vous ne pouvez pas sélectionner manuellement une ligne de ce type. |
| Projet | Permet d’enregistrer le temps d’utilisation d’un projet. Pour compléter les informations de la ligne, spécifiez le numéro de projet et le numéro de la tâche projet pour lesquels vous souhaitez enregistrer la durée. Vous pouvez enregistrer la durée pour des lignes que vous n’avez pas planifiées.|
| Ressource | Permet d’enregistrer le temps d’utilisation d’une ressource. Pour compléter les informations de la ligne, entrez une description de la tâche. |
| Service | Permet d’enregistrer le temps d’utilisation d’une commande service ou d’un avoir service. |

Par exemple, pour soumettre une feuille de temps pour une semaine de travail pendant laquelle vous avez travaillé sur des tâches de nettoyage la plupart du temps, mais pendant laquelle vous pris un jour de congé afin de vous rendre à des rendez-vous médicaux, vous devez ajouter des lignes comme illustré dans le tableau suivant.

| Type | Description | Code type travail | Code de type indisponibilité |
|--|--|--|--|
| Ressource | Heures de travail | Nettoyage |  |
| Indisponibilité | Absence |  | Santé |
|  | J’ai dû poser un congé le mardi en raison d’un rendez-vous médical. |  |  |

Dans cet exemple, vous devriez ensuite enregistrer les heures appropriées pour les jours appropriés dans les champs pour chaque jour de la semaine.  

> [!TIP]
> Dans la plupart des cas, votre entreprise proposera des types de travail prédéfinis pour les différents types de lignes. Dans ces cas, vous choisissez simplement le type de travail approprié dans la liste, puis vous ajoutez votre propre description.  
>
> Choisissez le type de travail en choisissant le bouton :::image type="icon" source="media/assist-edit-icon.png" border="false"::: dans le champ **Description**, en choisissant l’action **Détails de l’activité**, puis en la spécifiant dans la page qui s’ouvre, ou en la choisissant dans le champ **Code type travail** ou dans le champ **Code type indisponibilité**, respectivement. Dans ce cas, vous pouvez ignorer la section [Pour définir les types de travaux et en ajouter un à une feuille de temps](#to-define-work-types-and-add-one-to-a-time-sheet).  

## <a name="to-reuse-time-sheet-lines-in-other-time-sheets"></a><a name="to-reuse-time-sheet-lines-in-other-time-sheets"></a><a name="to-reuse-time-sheet-lines-in-other-time-sheets"></a>Pour réutiliser des lignes feuille de temps dans d’autres feuilles de temps par la suite

Si les informations de votre feuille de temps ne changent pas d’une période à une autre, vous pouvez gagner du temps en copiant les lignes de la période précédente. Il vous suffit ensuite d’entrer votre temps d’utilisation pour la nouvelle période.

1. Sélectionnez ![l’icône en forme d’ampoule qui ouvre la fonction Tell Me.](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire") entrez **Feuilles de temps**, puis choisissez le lien associé.  
2. Ouvrez la feuille de temps pour une période ultérieure à la période d’une feuille de temps existante avec des lignes.  
3. Cliquez sur **Copier les lignes de la feuille de temps précédente**.

Les lignes sont copiées, y compris les détails comme le type et la description. Par exemple, si la ligne est associée à un projet, le **N° projet** est copié. Toutes les lignes copiées ont le statut **En cours**. Vous pouvez à présent modifier les lignes selon vos besoins.

## <a name="to-copy-job-planning-lines-to-a-time-sheet"></a><a name="to-copy-job-planning-lines-to-a-time-sheet"></a><a name="to-copy-job-planning-lines-to-a-time-sheet"></a>Pour copier des lignes planning projet dans une feuille de temps
La procédure suivante indique comment ajouter rapidement des lignes planning projet à une feuille de temps.

1. Sélectionnez l’icône ![en forme d’ampoule qui ouvre la fonction Tell Me.](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire") entrez **Feuilles de temps**, puis choisissez le lien associé.  
2. Sur la page **Feuilles de temps**, sélectionnez une feuille de temps pour la période de référence.  
3. Cliquez sur **Créer des lignes à partir du planning projet**. Toutes les lignes planning projet de la période de feuille de temps sont copiées dans la feuille de temps de la personne ou du poste du champ **N° ressource** sur la feuille de temps.

## <a name="to-define-work-types-and-add-one-to-a-time-sheet"></a><a name="to-define-work-types-and-add-one-to-a-time-sheet"></a><a name="to-define-work-types-and-add-one-to-a-time-sheet"></a>Pour définir les types de travaux et en ajouter un à une feuille de temps

Vous pouvez définir le type de travail de toutes les lignes feuille de temps pour les commandes service, les ordres de travail et les ressources. Vous pouvez ainsi ajouter les informations dont vous avez besoin pour facturer le client en fonction des différents types de travaux.  

1. Sur la page **Feuilles de temps**, choisissez la feuille de temps appropriée.
2. Sur la première ligne de la section **Lignes**, choisissez le champ **Type**, puis choisissez le type approprié, par exemple *Ressource*.  
3. Choisissez le champ **Description**, puis, sur la page **Détail de la ressource de la ligne feuille de temps**, renseignez les champs. [!INCLUDE [tooltip-inline-tip_md](includes/tooltip-inline-tip_md.md)]  
    1. S’il n’existe aucun type de travail, cliquez sur **Nouveau**.
    2. Sur la page **Types de travail**, renseignez les champs selon vos besoins, puis revenez à la feuille de temps.
4. Renseignez les autres champs de la feuille de temps. Pour plus d’informations, consultez la section [Pour renseigner des lignes d’une feuille de temps et les envoyer pour approbation](#to-fill-in-time-sheet-lines-and-submit-for-approval).  

> [!TIP]
> Des étapes similaires s’appliquent à la définition des codes d’indisponibilité.

## <a name="to-fill-in-time-sheet-lines-and-submit-for-approval"></a><a name="to-fill-in-time-sheet-lines-and-submit-for-approval"></a><a name="to-fill-in-time-sheet-lines-and-submit-for-approval"></a>Pour renseigner des lignes d’une feuille de temps et les envoyer pour approbation

L’enregistrement des feuilles de temps est assuré en heures, qui est l’unité de mesure standard pour les ressources. Par défaut, une feuille de temps indique les jours de travail ouvrés du lundi au vendredi.  

1. Sélectionnez l’icône ![en forme d’ampoule qui ouvre la fonction Tell Me.](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire") entrez **Feuilles de temps**, puis choisissez le lien associé.  
2. Sélectionnez une feuille de temps pour la période concernée.
3. Renseignez les champs d’une ligne selon vos besoins. Saisissez le nombre d’heures utilisées par la ressource chaque jour de la semaine.  

    Dans la plupart des cas, pour suivre le travail, vous ajoutez une ligne de type *Ressource*, puis vous enregistrez les heures passées chaque jour. Si vous souhaitez enregistrer une indisponibilité, vous ajoutez une ligne de type *Indisponibilité*.  

    > [!TIP]  
    > Vous pouvez consulter dans le récapitulatif **Totalisation réelle/budgétée** la somme des heures des feuilles de temps que vous avez entrées.  
4. Répétez l’étape 3 pour d’autres types de travaux que la ressource effectue.  

    Ensuite, vous devez décider si vous souhaitez soumettre toutes les lignes de la feuille de temps ou si vous souhaitez soumettre des lignes individuelles.  

    * Pour soumettre la feuille de temps pour une ou plusieurs lignes, choisissez la ligne appropriée, puis choisissez l’action **Soumettre**.

        Dans la page des soumissions, choisissez l’option **Lignes sélectionnées uniquement**. L’état de la ligne passe de *Ouvert* à *Soumis*.
    * Pour soumettre la feuille de temps pour toutes les lignes ouvertes, choisissez l’action **Soumettre** en haut de la page **Feuille de temps**.  

        Vous devrez confirmer que vous souhaitez soumettre toutes les lignes ouvertes sur la feuille de temps actuelle.  

    > [!NOTE]  
    > Vous ne pouvez toutefois soumettre que des lignes pour lesquelles vous avez entré du temps.  
5. Pour modifier les informations d’une ligne qui a pour valeur **Soumis**, sélectionnez la ligne en question, puis cliquez sur **Rouvrir**.

    > [!NOTE]  
    >   Un administrateur peut rejeter une ligne feuille de temps qui est envoyée pour approbation. Si une ligne a le statut **Rejeté**, vous pouvez modifier cette ligne et choisir de nouveau **Envoyer**.  
6. Cliquez sur le bouton **OK**.

## <a name="to-approve-or-reject-a-time-sheet"></a><a name="to-approve-or-reject-a-time-sheet"></a><a name="to-approve-or-reject-a-time-sheet"></a>Pour approuver ou rejeter une feuille de temps
Une feuille de temps doit être soumise pour approbation avant de pouvoir être utilisée. Vous pouvez approuver et rejeter chacune des lignes d’une feuille de temps ou les renvoyer à la personne à l’origine de leur soumission pour qu’elle effectue d’autres actions. Une feuille de temps peut être approuvée de deux manières :

* Un administrateur de feuille de temps peut approuver n’importe quelle feuille de temps.
* La personne qui est indiquée dans le champ **ID utilisateur de l’approbateur de la feuille de temps** d’une fiche ressource peut approuver les feuilles de temps de cette ressource. Pour plus d’informations, voir [Paramétrer des feuilles de temps](projects-how-setup-time-sheets.md).

1. Sélectionnez l’icône ![en forme d’ampoule qui ouvre la fonction Tell Me.](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire") entrez **Feuilles de temps administrateur**, puis choisissez le lien associé.
2. Sélectionnez une feuille de temps dans la liste.  
3. Sur la page **Feuille de temps**, 
    1. Choisissez l’action **Traiter**, puis l’action **Approuver**.
    2. Cliquez sur **Toutes les lignes envoyées** pour approuver toutes les lignes ou sur **Ligne(s) sélectionnée(s) uniquement** pour approuver uniquement les lignes qui sont sélectionnées sur la page **Feuille de temps**.
4. Choisissez le bouton **OK**.  
5. Sinon, cliquez sur **Rejeter** et suivez les étapes 4 à 5.  

> [!TIP]  
>   Utilisez les récapitulatifs **Statut feuille de temps** et **Totalisation réelle/budgétée** pour obtenir un aperçu des informations des feuilles de temps.

Une fois qu’une feuille de temps est approuvée ou rejetée, elle ne peut plus être modifiée à moins d’être rouverte au préalable. La procédure suivante explique comment rouvrir une feuille de temps approuvée ou rejetée.

## <a name="to-reopen-a-time-sheet"></a><a name="to-reopen-a-time-sheet"></a><a name="to-reopen-a-time-sheet"></a>Pour rouvrir une feuille de temps
1. Sélectionnez l’icône ![en forme d’ampoule qui ouvre la fonction Tell Me.](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire") entrez **Feuilles de temps administrateur** ou **Feuilles de temps**, puis choisissez le lien associé.
2. Ouvrez une feuille de temps à partir de la liste.  

    > [!NOTE]  
    >   Vous ne pouvez rouvrir que les lignes dont le statut est **Approuvé**. Vous ne pouvez pas rouvrir les lignes dont le statut est **Rejeté**. Vous ne pouvez pas rouvrir une feuille de temps qui a été validée.  
3. Sur la page **Feuille de temps**, cliquez sur **Rouvrir**, puis sur **Toutes les lignes soumises** pour rouvrir toutes les lignes ou sur **Ligne(s) sélectionnée(s) uniquement** pour rouvrir uniquement les lignes sélectionnées sur la page **Feuille de temps**.
4. Choisissez le bouton **OK**. Le statut de la ou des lignes des feuilles de temps devient **Soumis**.  

## <a name="to-view-and-approve-time-sheets-by-job"></a><a name="to-view-and-approve-time-sheets-by-job"></a><a name="to-view-and-approve-time-sheets-by-job"></a>Pour afficher et approuver des feuilles de temps par tâche

Dans le cadre d’une tâche, vous pouvez indiquer une personne qui soit chargée de celle-ci. Ces informations sont liées aux lignes feuille de temps et elles peuvent être utilisés pour dresser la liste des feuilles de temps qu’un chef de projet doit consulter et approuver. Par exemple, le chef de projet équipe peut être chargé de certaines tâches dans votre société. Dans ce cas, le responsable doit figurer en tant que **Responsable** sur la fiche projet. Dans cette vue des informations des feuilles de temps, vous pouvez afficher les tâches projet associées à un projet, ainsi que le nombre d’heures utilisées.

> [!NOTE]
> Pour pouvoir approuver des feuilles de temps dans la fenêtre **Feuille de temps administrateur par projet**, vous devez d’abord sélectionner une option **Feuille de temps par approbation de projet** dans la fenêtre **Paramètres ressources**. Pour plus d’informations, reportez-vous à [Configuration de ressources](projects-how-setup-resources.md).

### <a name="to-approve-or-reject-a-time-sheet-by-job"></a><a name="to-approve-or-reject-a-time-sheet-by-job"></a><a name="to-approve-or-reject-a-time-sheet-by-job"></a>Pour approuver ou rejeter une feuille de temps par projet

1. Dans la zone **Rechercher**, entrez **Feuille de temps administrateur par projet**, puis sélectionnez le lien associé. [!INCLUDE[prod_short](includes/prod_short.md)] affiche une liste des lignes feuille de temps associées aux projets dont vous êtes responsable.
2. Cliquez sur **Approuver**, puis sur **Toutes les lignes envoyées** pour approuver toutes les lignes ou sur **Ligne(s) sélectionnée(s) uniquement** pour approuver uniquement les lignes qui sont sélectionnées sur la page **Feuille de temps**.

    > [!NOTE]
    > Vous ne pouvez approuver que les feuilles de temps dont le statut est **Soumis**.

3. Pour fournir des informations supplémentaires sur l’approbation ou le rejet, sélectionnez **Association**, **Commentaires**, puis **Commentaires de ligne** et saisissez des commentaires.
4. Cliquez sur le bouton **OK**.

> [!NOTE]
> Une fois une ligne feuille de temps par projet approuvée ou rejetée, elle ne peut plus être modifiée ni rouverte dans la fenêtre **Feuille de temps**.

## <a name="to-post-time-sheet-lines-in-a-resource-journal"></a><a name="to-post-time-sheet-lines-in-a-resource-journal"></a><a name="to-post-time-sheet-lines-in-a-resource-journal"></a>Pour valider des lignes feuille de temps dans une feuille ressource
Une fois que vous avez approuvé les écritures des feuilles de temps d’une ressource, vous pouvez les valider dans la feuille ressource correspondante.

1. Sélectionnez l’icône ![en forme d’ampoule qui ouvre la fonction Tell Me.](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire") saisissez **Feuilles ressource**, puis choisissez le lien associé.  
2. Cliquez sur **Proposer des lignes à partir des feuilles de temps**.  
3. Sur la page **Proposer lignes feuille ressources**, renseignez les champs selon vos besoins.  
4. Cliquez sur le bouton **OK**. Les écritures de l’activité sont créées dans la feuille ressource, dans laquelle vous pouvez modifier les informations selon vos besoins.  
5. Sélectionnez l’action **Valider**.  
6. Pour vérifier la validation, cliquez sur **Écritures comptables**. La page **Écritures comptables ressource** s’ouvre et affiche le résultat de la validation de la feuille ressource.

## <a name="to-post-time-sheet-lines-in-a-job-journal"></a><a name="to-post-time-sheet-lines-in-a-job-journal"></a><a name="to-post-time-sheet-lines-in-a-job-journal"></a>Pour valider des lignes feuille de temps dans une feuille projet
Une fois que vous avez approuvé les écritures des feuilles de temps d’un projet, vous pouvez les valider dans la feuille projet correspondante.

1. Sélectionnez l’icône ![Ampoule qui ouvre la fonction Tell Me](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire"), entrez **Feuilles projet**, puis choisissez le lien associé.  
2. Cliquez sur **Proposer des lignes à partir des feuilles de temps**.  
3. Sur la page **Proposer lignes feuille projet**, renseignez les champs selon vos besoins.  
4. Cliquez sur le bouton **OK**. Les écritures de l’activité sont créées dans la feuille projet, dans laquelle vous pouvez modifier les informations selon vos besoins.  

    > [!NOTE]  
    >   Les informations sur le type de travail et la facturabilité du travail sont copiées à partir de la ligne feuille de temps. Si nécessaire, vous pouvez réduire le nombre d’heures et procéder à une validation partielle. Si vous réduisez la quantité, la prochaine fois que vous cliquerez sur **Proposer des lignes à partir des feuilles de temps**, la ligne qui sera créée contiendra la quantité d’heures restante.  
5. Sélectionnez l’action **Valider**.  
6. Pour vérifier la validation, cliquez sur **Écritures comptables**. La page **Écritures comptables projet** s’ouvre et affiche le résultat de la validation de la feuille ressource.

## <a name="to-archive-time-sheets"></a><a name="to-archive-time-sheets"></a><a name="to-archive-time-sheets"></a>Pour archiver des feuilles de temps
Une fois les feuilles de temps validées, vous pouvez les archiver pour vous y référer par la suite. Toutes les lignes des feuilles de temps doivent être validées avant qu’une feuille de temps puisse être archivée.

> [!NOTE]  
>   Lorsque vous archivez une feuille de temps, elle est supprimée des listes de la page **Feuilles de temps** et **Feuilles de temps administrateur**.

1. Sélectionnez l’icône ![Ampoule qui ouvre la fonction Tell Me.](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire") entrez **Feuilles de temps**, puis choisissez le lien associé.
2. Sélectionnez **Déplacer les feuilles de temps vers l’archive**.  
3. Sur la page **Déplacer les feuilles de temps vers l’archive**, renseignez les champs selon vos besoins, puis cliquez sur le bouton **OK**.  
4. Pour examiner les feuilles de temps archivées, sélectionnez l’icône ![Ampoule qui ouvre la fonction Tell Me.](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire") entrez **Archives des feuilles de temps** ou **Archives des feuilles de temps administrateur**, puis choisissez le lien associé.

## <a name="see-also"></a><a name="see-also"></a><a name="see-also"></a>Voir aussi
[Gestion de projets](projects-manage-projects.md)  
[Configuration de la gestion de projets](projects-setup-projects.md)  
[Finances](finance.md)  
[Achats](purchasing-manage-purchasing.md)  
[Ventes](sales-manage-sales.md)  
[Utiliser [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
