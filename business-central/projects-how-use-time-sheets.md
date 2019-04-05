---
title: Utilisation de feuilles de temps pour des projets| Microsoft Docs
description: Décrit comment créer une feuille de temps pour un projet, copier des lignes planning dans celle-ci, définir les types de travaux, renseigner la feuille de temps, et la soumettre pour approbation.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: project management, capacity, staff, resource
ms.date: 10/01/2018
ms.author: sgroespe
ms.openlocfilehash: 70d63dcc678a49fa1854b88bc3ca1f9ec8ecc69f
ms.sourcegitcommit: 1bcfaa99ea302e6b84b8361ca02730b135557fc1
ms.translationtype: HT
ms.contentlocale: fr-CH
ms.lasthandoff: 03/08/2019
ms.locfileid: "820582"
---
# <a name="use-time-sheets-for-jobs"></a>Utiliser des feuilles de temps pour des projets
Vous devez utiliser le traitement par lots **Créer des feuilles de temps** pour configurer des feuilles de temps pour un nombre donné de périodes ou de semaines. Vous devez disposer d'autorisations pour pouvoir créer des feuilles de temps.

Vous pouvez copier et utiliser vos lignes planning projet dans une feuille de temps. Vous n'avez ainsi à entrer les informations qu'à un seul emplacement et les informations de ligne sont toujours correctes.

Une fois que vous avez approuvé les écritures des feuilles de temps d'un projet, vous pouvez les valider dans la feuille ressource ou projet correspondante.

Avant de pouvoir utiliser des feuilles de temps, vous devez définir des informations générales et spécifier un administrateur et un ou plusieurs approbateurs de feuilles de temps. Pour plus d'informations, voir [Paramétrer des feuilles de temps](projects-how-setup-time-sheets.md).

## <a name="to-create-a-time-sheet"></a>Pour créer une feuille de temps
Vous pouvez utiliser le traitement par lots **Créer des feuilles de temps** pour configurer des feuilles de temps pour un nombre donné de périodes ou de semaines. Une fois qu'une feuille de temps est créée, son propriétaire peut l'ouvrir et y enregistrer le temps consacré à une tâche.

1. Choisissez l'icône ![Ampoule qui ouvre la fonction Tell Me](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire"), saisissez **Feuilles de temps**, puis choisissez le lien associé.
2. Sur la page **Liste des feuilles de temps**, cliquez sur l'action **Créer des feuilles de temps**.
3. Renseignez les champs selon vos besoins. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

> [!NOTE]  
>   Les champs **Utiliser la feuille de temps** et **ID utilisateur du propriétaire de la feuille de temps** doivent être renseignés sur la fiche de la ressource de la feuille de temps.

1. Choisissez le bouton **OK**.  

Vous pouvez afficher les feuilles de temps que vous avez créées sur la page **Liste des feuilles de temps**.

## <a name="to-copy-job-planning-lines-to-a-time-sheet"></a>Pour copier des lignes planning projet dans une feuille de temps
La procédure suivante indique comment ajouter rapidement des lignes planning projet à une feuille de temps.

1. Choisissez l'icône ![Ampoule qui ouvre la fonction Tell Me](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire"), saisissez **Feuilles de temps**, puis choisissez le lien associé.  
2. Sur la page **Liste des feuilles de temps**, sélectionnez une feuille de temps pour la période de référence, puis cliquez sur **Modifier feuille de temps**.  
3. Cliquez sur **Créer des lignes à partir du planning projet**. Toutes les lignes planning projet de la période de feuille de temps sont copiées dans la feuille de temps de la personne ou du poste du champ **N° ressource** sur la feuille de temps.

## <a name="to-define-work-types-and-add-one-to-a-time-sheet"></a>Pour définir les types de travaux et en ajouter un à une feuille de temps
Vous pouvez définir le type de travail pour toutes les lignes feuille de temps des projets. Vous pouvez ainsi ajouter les informations dont vous avez besoin pour facturer le client en fonction des différents types de travaux.

1. Choisissez l'icône ![Ampoule qui ouvre la fonction Tell Me](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire"), saisissez **Feuilles de temps**, puis choisissez le lien associé.   
2. Ouvrez la feuille de temps correspondante.
3. Choisissez le champ **Description**.  
4. Sur la page **Détails des tâches - ligne feuille de temps**, cliquez sur le champ **Code type travail**, puis sélectionnez un type de travail dans la liste, par exemple **Miles**.  
5. S'il n'existe aucun type de travail, cliquez sur **Nouveau**.
6. Sur la page **Types de travaux**, renseignez les champs selon vos besoins.
7. Répétez l'étape 4 pour affecter le nouveau type de travail à la feuille de temps.

## <a name="to-reuse-time-sheet-lines-in-other-time-sheets"></a>Pour réutiliser des lignes feuille de temps dans d'autres feuilles de temps par la suite
Si les informations de votre feuille de temps ne changent pas d'une période à une autre, vous pouvez gagner du temps en copiant les lignes de la période précédente. Il vous suffit ensuite d'entrer votre temps d'utilisation pour la nouvelle période.

1. Choisissez l'icône ![Ampoule qui ouvre la fonction Tell Me](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire"), saisissez **Feuilles de temps**, puis choisissez le lien associé.  
2. Ouvrez la feuille de temps pour une période ultérieure à la période d'une feuille de temps existante avec des lignes.  
3. Cliquez sur **Copier les lignes de la feuille de temps précédente**.

Les lignes sont copiées, y compris les détails comme le type et la description. Par exemple, si la ligne est associée à un projet, le **N° projet** est copié. Toutes les lignes copiées ont le statut **En cours**. Vous pouvez à présent modifier les lignes selon vos besoins.

## <a name="to-fill-in-a-time-sheet-lines-and-submit-for-approval"></a>Pour renseigner les lignes d'une feuille de temps lignes et l'envoyer pour approbation
L'enregistrement des feuilles de temps est assuré en heures, qui est l'unité de mesure standard pour les ressources. Par défaut, une feuille de temps indique les jours de travail ouvrés du lundi au vendredi.

1. Choisissez l'icône ![Ampoule qui ouvre la fonction Tell Me](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire"), saisissez **Feuilles de temps**, puis choisissez le lien associé.  
2. Sélectionnez une feuille de temps pour la période de référence, puis cliquez sur **Modifier feuille de temps**.  
3. Renseignez les champs d'une ligne selon vos besoins. Saisissez le nombre d'heures utilisées par la ressource chaque jour de la semaine.

    > [!TIP]  
    >   Vous pouvez consulter dans le récapitulatif **Totalisation réelle/budgétée** la somme des heures des feuilles de temps que vous avez entrées.  
4. Répétez l'étape 3 pour d'autres types de travaux que la ressource effectue.
5. Cliquez sur **Envoyer**, puis sur **Toutes les lignes ouvertes** pour envoyer toutes les lignes ou sur **Ligne(s) sélectionnée(s) uniquement** pour envoyer uniquement les lignes qui sont sélectionnées sur la page **Feuille de temps**.  

    > [!NOTE]  
    >   Vous ne pouvez toutefois soumettre que des lignes pour lesquelles vous avez entré du temps.  
6. Pour modifier les informations d'une ligne qui a pour valeur **Soumis**, sélectionnez la ligne en question, puis cliquez sur **Rouvrir**.

    > [!NOTE]  
    >   Un administrateur peut rejeter une ligne feuille de temps qui est envoyée pour approbation. Si une ligne a le statut **Rejeté**, vous pouvez modifier cette ligne et choisir de nouveau **Soumettre**.  
7. Cliquez sur le bouton **OK**.

## <a name="to-approve-or-reject-a-time-sheet"></a>Pour approuver ou rejeter une feuille de temps
Une feuille de temps doit être soumise pour approbation avant de pouvoir être utilisée. Vous pouvez approuver et rejeter chacune des lignes d'une feuille de temps ou les renvoyer à la personne à l'origine de leur soumission pour qu'elle effectue d'autres actions. Une feuille de temps peut être approuvée de deux manières :

* Un administrateur de feuille de temps peut approuver n'importe quelle feuille de temps.
* La personne qui est indiquée dans le champ **ID utilisateur de l'approbateur de la feuille de temps** d'une fiche ressource peut approuver les feuilles de temps de cette ressource. Pour plus d'informations, voir [Paramétrer des feuilles de temps](projects-how-setup-time-sheets.md).

1. Choisissez l'icône ![Ampoule qui ouvre la fonction Tell Me](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire"), saisissez **Feuilles de temps administrateur**, puis choisissez le lien associé.
2. Sélectionnez une feuille de temps dans la liste.  
3. Sur la page **Feuille de temps**, cliquez sur **Approuver**, puis sur **Toutes les lignes soumises** pour approuver toutes les lignes ou sur **Ligne(s) sélectionnée(s) uniquement** pour envoyer uniquement les lignes qui sont sélectionnées sur la page **Feuille de temps**.
4. Choisissez le bouton **OK**.  
5. Sinon, cliquez sur **Rejeter** et suivez les étapes 4 à 5.  

> [!TIP]  
>   Utilisez les récapitulatifs **Statut feuille de temps** et **Totalisation réelle/budgétée** pour obtenir un aperçu des informations des feuilles de temps.

Une fois qu'une feuille de temps est approuvée ou rejetée, elle ne peut plus être modifiée à moins d'être rouverte au préalable. La procédure suivante explique comment rouvrir une feuille de temps approuvée ou rejetée.

## <a name="to-reopen-a-time-sheet"></a>Pour rouvrir une feuille de temps
1. Choisissez l'icône ![Ampoule qui ouvre la fonction Tell Me](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire"), saisissez **Feuilles de temps administrateur** ou **Feuilles de temps**, puis choisissez le lien associé.
2. Ouvrez une feuille de temps à partir de la liste.  

    > [!NOTE]  
    >   Vous ne pouvez rouvrir que les lignes dont le statut est **Approuvé**. Vous ne pouvez pas rouvrir les lignes dont le statut est **Rejeté**. Vous ne pouvez pas rouvrir une feuille de temps qui a été validée.  
3. Sur la page **Feuille de temps**, cliquez sur **Rouvrir**, puis sur **Toutes les lignes soumises** pour rouvrir toutes les lignes ou sur **Ligne(s) sélectionnée(s) uniquement** pour rouvrir uniquement les lignes sélectionnées sur la page **Feuille de temps**.
4. Choisissez le bouton **OK**. Le statut de la ou des lignes des feuilles de temps devient **Soumis**.  

## <a name="to-post-time-sheet-lines-in-a-resource-journal"></a>Pour valider des lignes feuille de temps dans une feuille ressource
Une fois que vous avez approuvé les écritures des feuilles de temps d'une ressource, vous pouvez les valider dans la feuille ressource correspondante.

1. Choisissez l'icône ![Ampoule qui ouvre la fonction Tell Me](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire"), saisissez **Feuille ressource**, puis sélectionnez le lien associé.  
2. Cliquez sur **Proposer des lignes à partir des feuilles de temps**.  
3. Renseignez les champs selon vos besoins.  
4. Cliquez sur le bouton **OK**. Les écritures de l'activité sont créées dans la feuille ressource, dans laquelle vous pouvez modifier les informations selon vos besoins.  
5. Sélectionnez l'action **Valider**.  
6. Pour vérifier la validation, cliquez sur **Écritures comptables**. La page **Écritures comptables ressource** s'ouvre et affiche le résultat de la validation de la feuille ressource.

## <a name="to-post-time-sheet-lines-in-a-job-journal"></a>Pour valider des lignes feuille de temps dans une feuille projet
Une fois que vous avez approuvé les écritures des feuilles de temps d'un projet, vous pouvez les valider dans la feuille projet correspondante.

1. Choisissez l'icône ![Ampoule qui ouvre la fonction Tell Me](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire"), saisissez **Feuille projet**, puis sélectionnez le lien associé.  
2. Cliquez sur **Proposer des lignes à partir des feuilles de temps**.  
3. Renseignez les champs selon vos besoins.  
4. Cliquez sur le bouton **OK**. Les écritures de l'activité sont créées dans la feuille projet, dans laquelle vous pouvez modifier les informations selon vos besoins.  

    > [!NOTE]  
    >   Les informations sur le type de travail et la facturabilité du travail sont copiées à partir de la ligne feuille de temps. Si nécessaire, vous pouvez réduire le nombre d'heures et procéder à une validation partielle. Si vous réduisez la quantité, la prochaine fois que vous cliquerez sur **Proposer des lignes à partir des feuilles de temps**, la ligne qui sera créée contiendra la quantité d'heures restante.  
5. Sélectionnez l'action **Valider**.  
6. Pour vérifier la validation, cliquez sur **Écritures comptables**. La page **Écritures comptables projet** s'ouvre et affiche le résultat de la validation de la feuille ressource.

## <a name="to-archive-time-sheets"></a>Pour archiver des feuilles de temps
Une fois les feuilles de temps validées, vous pouvez les archiver pour vous y référer par la suite. Toutes les lignes des feuilles de temps doivent être validées avant qu'une feuille de temps puisse être archivée.

> [!NOTE]  
>   Lorsque vous archivez une feuille de temps, elle est supprimée des listes de la page **Feuilles de temps** et **Feuilles de temps administrateur**.

1. Choisissez l'icône ![Ampoule qui ouvre la fonction Tell Me](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire"), saisissez **Feuilles de temps de transfert vers archive**, puis choisissez le lien associé.  
2. Renseignez les champs selon vos besoins, puis cliquez sur le bouton **OK**.  
3. Pour vérifier les feuilles de temps archivées, choisissez l'icône ![Ampoule qui ouvre la fonction Tell Me](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire"), saisissez **Archives des feuilles de temps** ou **Archives des feuilles de temps administrateur**, puis choisissez le lien associé.

## <a name="see-also"></a>Voir aussi
[Gestion de projets](projects-manage-projects.md)  
[Configuration de la gestion de projet](projects-setup-projects.md)    
[Finances](finance.md)  
[Achats](purchasing-manage-purchasing.md)         
[Ventes](sales-manage-sales.md)     
[Utilisation de [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)  
