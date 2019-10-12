---
title: Configuration et utilisation d'un flux d'approbation achat | Microsoft Docs
description: Vous pouvez automatiser le processus d'approbation d'enregistrements nouveaux ou modifiés, par exemple de documents, de feuilles et de fiches client, en créant des flux de travail avec des étapes pour les approbations en question. Avant de créer des flux d'approbation, vous devez configurer un approbateur et un approbateur remplaçant pour chaque utilisateur approbation. Vous pouvez également définir les montants maximaux que les approbateurs sont qualifiés à approuver pour les enregistrements de vente et d'achat. Les demandes d'approbation et d'autres notifications peuvent être envoyées par e-mail ou note interne. Pour chaque configuration d'utilisateur d'approbation, vous pouvez également définir à quel moment ils reçoivent les notifications.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/01/2019
ms.author: sgroespe
ms.openlocfilehash: ca97d08166b73f75240203aa9949e4b0aa774ea6
ms.sourcegitcommit: 02e704bc3e01d62072144919774f1244c42827e4
ms.translationtype: HT
ms.contentlocale: fr-CH
ms.lasthandoff: 10/01/2019
ms.locfileid: "2310531"
---
# <a name="walkthrough-setting-up-and-using-a-purchase-approval-workflow"></a>Procédure pas à pas : Configuration et utilisation d'un flux d'approbation achat
Vous pouvez automatiser le processus d'approbation d'enregistrements nouveaux ou modifiés, par exemple de documents, de feuilles et de fiches client, en créant des flux de travail avec des étapes pour les approbations en question. Avant de créer des flux d'approbation, vous devez configurer un approbateur et un approbateur remplaçant pour chaque utilisateur approbation. Vous pouvez également définir les montants maximaux que les approbateurs sont qualifiés à approuver pour les enregistrements de vente et d'achat. Les demandes d'approbation et d'autres notifications peuvent être envoyées par e-mail ou note interne. Pour chaque configuration d'utilisateur d'approbation, vous pouvez également définir à quel moment ils reçoivent les notifications.

> [!NOTE]
> Outre la fonctionnalité de flux de travail dans [!INCLUDE[d365fin](includes/d365fin_md.md)], vous pouvez intégrer à Microsoft Flow pour définir des flux de travail des événements dans [!INCLUDE[d365fin](includes/d365fin_md.md)]. Remarquez que bien qu'ils soient deux systèmes de flux de travail distincts, tous les modèles Flow que vous créez dans Microsoft Flow est ajouté à la liste des modèles de flux de travail dans [!INCLUDE[d365fin](includes/d365fin_md.md)]. Pour plus d'informations, voir [Utilisation de Business Central dans un flux automatisé](across-how-use-financials-data-source-flow.md).   

 Vous pouvez configurer et utiliser des workflows qui connectent des tâches de processus entreprise exécutées par différents utilisateurs. Les tâches du système, telles que la validation automatique, peuvent être incluses comme étapes du workflow, précédées ou suivies des tâches de l'utilisateur. Demander et accorder une approbation pour créer des enregistrements sont des étapes classiques du workflow. Pour plus d'informations, voir [Flux de travail](across-workflow.md).  

## <a name="about-this-walkthrough"></a>À propos de cette procédure pas à pas  
Cette procédure pas à pas présente les tâches suivantes :  

-   Configuration des utilisateurs approbation.  
-   Configuration des notification pour les utilisateurs approbation.  
-   Modification et activation d'un flux d'approbation.  
-   Demande d'approbation d'une commande achat (Alicia).  
-   Réception d'une notification, puis acceptation de la demande (Sean).  

## <a name="prerequisites"></a>Conditions préalables  
Pour effectuer cette procédure pas à pas, vous aurez besoin de la société de démonstration CRONUS International Ltd.

## <a name="story"></a>Scénario  
Sean est un superutilisateur dans CRONUS. Il crée deux utilisateurs d’approbation. Le premier est Alicia, qui représente un agent d'achats. L'autre, c'est lui-même, soit l'approbateur d'Alicia. Ensuite, Sean s'octroie des droits d'approbation pour un montant d'achat illimité et spécifie qu'il recevra les notifications par note interne dès qu'un événement approprié se produira. Enfin, Sean crée le flux d'approbation requis en tant que copie du modèle Flux de travail approbation commande achat existant, laisse toutes les conditions d'événement et options de réponse existantes inchangées, puis active le flux.  

Pour tester le flux d'approbation, Sean se connecte d'abord à [!INCLUDE[d365fin](includes/d365fin_md.md)] sous l'identité d'Alicia, puis demande l'approbation d'une commande achat. Ensuite, Sean se connecte en tant que lui-même, voit la note dans son Tableau de bord, suit le lien vers la demande d'approbation de la commande achat, et approuve la demande.  

## <a name="setting-up-sample-data"></a>Configuration des exemples de données
Pour pouvoir configurer des utilisateurs d'approbation et leur méthode de notification, vous devez vous assurer que deux utilisateurs existent dans [!INCLUDE[d365fin](includes/d365fin_md.md)] : Un utilisateur représente Alicia. L'autre utilisateur, vous-même, représente Sean. Pour en savoir plus, reportez-vous à [Gérer les utilisateurs et les autorisations](ui-how-users-permissions.md).

### <a name="setting-up-approval-users"></a>Configuration des utilisateurs approbation  
Une fois connecté comme vous-même, définissez Alicia en tant qu'utilisateur d'approbation dont l'approbateur est vous-même. Configurez vos droits d'approbation et spécifiez comment et quand être averti des demandes d'approbation.  

#### <a name="to-set-up-yourself-and-alicia-as-approval-users"></a>Pour configurer votre propre profil et celui d'Alicia en tant qu'utilisateurs approbation  
1.  Choisissez l'icône ![Ampoule qui ouvre la fonction Tell Me](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire"), saisissez **Paramètres utilisateur approbation**, puis sélectionnez le lien associé.  
2.  Sur la page **Paramètres utilisateur approbation**, sélectionnez l'action **Nouveau**.  

    > [!NOTE]  
    >  Vous devez configurer un approbateur avant de pouvoir configurer des utilisateurs qui ont besoin de l'approbation de l'approbateur. Par conséquent, vous devez configurer votre propre profil avant de configurer celui d'Alicia.  

3.  Configurez les deux utilisateurs approbation en renseignant les champs comme indiqué dans le tableau suivant.  

    |ID utilisateur|ID approbateur|Montant illimité d'achat autorisé|  
    |-------------|-----------------|---------------------------------|  
    |VOUS||Sélection|  
    |ALICIA|VOUS||  

### <a name="setting-up-notifications"></a>Configuration de notifications  
Dans cette procédure, l'utilisateur est averti par une note interne concernant les demandes d'approbation. La notification d'approbation peut également être par e-mail. Pour plus d'informations, voir [Spécifier quand et comment recevoir des notifications](across-how-to-specify-when-and-how-to-receive-notifications.md). 

#### <a name="to-set-up-how-and-when-you-are-notified"></a>Pour spécifier comment et quand recevoir les notifications  
1.  Sur la page **Paramètres utilisateur approbation**, sélectionnez la ligne pour vous-même, puis sélectionnez l'action **Paramètres de notification**.  
2.  sur la page **Paramètres de notification**, dans le champ **Type de notification**, choisissez **Approbation**.  
3.  Dans le champ **Mode de notification**, choisissez **Note**.  
6.  Sur la page **Paramètres de notification**, cliquez sur l'action **Tableau de notification**.  
7.  Sur la page **Tableau de notification**, dans le champ **Récurrence**, sélectionnez **Immédiatement**.  
8. Choisissez le bouton **OK**.  

## <a name="creating-the-approval-workflow"></a>Création d'un flux d'approbation  
 Créez le flux d'approbation de commande d'achat en copiant les étapes du modèle de Flux de travail approbation commande achat. Laissez les étapes existantes du flux inchangées, puis activez le flux.  

### <a name="to-create-and-enable-a-purchase-order-approval-workflow"></a>Pour créer et activer un flux d'approbation de commande d'achat  
1.  Choisissez l'icône ![Ampoule qui ouvre la fonction Tell Me](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire"), saisissez **Flux de travail**, puis sélectionnez le lien associé.  
2.  Sur la page **Flux de travail**, choisissez l'action **Créer le flux de travail à partir du modèle**.  
3.  Sur la page **Modèles de flux de travail**, sélectionnez le modèle de flux de travail nommé Flux de travail approbation commande achat, puis choisissez le bouton **OK**.  

    La page **Flux de travail** s'ouvre pour un nouveau flux de travail contenant toutes les informations du modèle sélectionné. La valeur du champ **Code** est étendue avec « -01 » pour indiquer que ce premier flux de travail est créé à partir du modèle Flux de travail approbation commande achat.  
5.  Dans l'en-tête de la page **Flux de travail**, activez la case à cocher **Activé**.  

## <a name="using-the-approval-workflow"></a>Utilisation du flux d'approbation  
Utilisez le nouveau Flux de travail approbation commande achat en ouvrant une session dans [!INCLUDE[d365fin](includes/d365fin_md.md)] en tant qu'Alicia pour demander l'approbation d'une commande achat. Ensuite, connectez-vous en tant que vous-même, affichez la note dans le Tableau de bord, suivez le lien vers la demande d'approbation, puis approuvez la demande.  

### <a name="to-request-approval-of-a-purchase-order-as-alicia"></a>Pour demander l'approbation d'une commande achat en tant qu'Alicia  
1. Connectez-vous en tant qu'Alicia.
2.  Choisissez l'icône ![Ampoule qui ouvre la fonction Tell Me](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire"), saisissez **Commandes achat**, puis sélectionnez le lien associé.  
3.  Sélectionnez la ligne de la commande achat ouverte 104001, puis choisissez l'action **Modifier**.  
4.  Sur la page **Commande achat**, choisissez l'action **Envoyer demande d'approbation**.  

Notez que la valeur du champ **Statut** est passée à **Approbation en attente**.  

### <a name="to-approve-the-purchase-order-as-sean"></a>Pour approuver la commande achat en tant que Sean  
1. Connectez-vous en tant que Sean.
2.  Dans le Tableau de bord, sur la page **Mes notifications**, recherchez une nouvelle note d'Alicia.  
3.  Lorsque la note s'affiche sur la page **Mes notifications**, sélectionnez la valeur **Écriture approbation : XX, XX** dans le champ **Page**. La page **Demandes à approuver** s'ouvre avec la demande de commande d'achat d'Alicia en surbrillance.  
4.  Sur la page **Demandes à approuver**, choisissez l'action **Approuver**.  

    La valeur du champ **Statut** de la commande d'achat d'Alicia passe à **Lancé**.  

Vous venez de configurer et tester un flux de travail d'approbation simple incluant les deux premières étapes du Flux de travail approbation commande achat. Vous pouvez facilement étendre ce flux pour valider automatiquement la commande d'achat d'Alicia lorsque c'est Sean qui l'approuve. Pour cela, vous devez activer le Flux de travail facture achat, dans lequel la réponse à une facture d'achat lancée est de la valider. Vous devez d'abord modifier la condition d'événement de la première étape du flux (achat) en remplaçant **Facturer** par **Commander**.  

La version générique de [!INCLUDE[d365fin](includes/d365fin_md.md)] inclut un certain nombre de modèles de flux de travail pour les scénarios pris en charge par le code d'application. La plupart concernent des flux d'approbation.  

Définissez les variations des flux de travail en renseignant les champs des lignes à partir des listes fixes de valeurs d'événement et de réponse qui sont les scénarios pris en charge par le code d'application. Pour plus d'informations, voir [Créer des flux de travail](across-how-to-create-workflows.md).  

Si un scénario d'entreprise requiert un événement ou une réponse de workflow qui n'est pas pris en charge, un partenaire Microsoft doit l'implémenter en personnalisant le code de l'application. Pour plus d'informations, voir [Procédure pas à pas : implémentation de nouveaux événements et réponses de flux de travail](/dynamics-nav/Walkthrough--Implementing-New-Workflow-Events-and-Responses) dans l'Aide destinée aux développeurs et aux professionnels de l'informatique.  

## <a name="see-also"></a>Voir aussi  
[Configurer des utilisateurs d'approbation](across-how-to-set-up-approval-users.md)   
[Configuration de notifications de flux de travail](across-setting-up-workflow-notifications.md)   
[Créer des workflows](across-how-to-create-workflows.md)   
[Utilisation des flux d'approbation](across-how-use-approval-workflows.md)   
[Flux de travail](across-workflow.md)  
[Utilisation de Business Central dans un flux automatisé](across-how-use-financials-data-source-flow.md)
