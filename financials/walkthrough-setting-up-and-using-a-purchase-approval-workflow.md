---
title: "Procédure pas à pas : Configuration et utilisation d'un flux d'approbation achat | Microsoft Docs"
description: "Vous pouvez automatiser le processus d'approbation d'enregistrements nouveaux ou modifiés, par exemple de documents, de feuilles et de fiches client, en créant des flux de travail avec des étapes pour les approbations en question. Avant de créer des flux d'approbation, vous devez configurer un approbateur et un approbateur remplaçant pour chaque utilisateur approbation. Vous pouvez également définir les montants maximaux que les approbateurs sont qualifiés à approuver pour les enregistrements de vente et d'achat. Les demandes d'approbation et d'autres notifications peuvent être envoyées par e-mail ou note interne. Pour chaque configuration d'utilisateur d'approbation, vous pouvez également définir à quel moment ils reçoivent les notifications."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 07/01/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: a49e50213f808fb72b43dfa22a34833b306ef12d
ms.openlocfilehash: 7ce4b45d740e50bba8256e72fcf43c70ea85922c
ms.contentlocale: fr-ch
ms.lasthandoff: 12/14/2017

---
# <a name="walkthrough-setting-up-and-using-a-purchase-approval-workflow"></a>Procédure pas à pas : Configuration et utilisation d'un flux d'approbation achat
Vous pouvez automatiser le processus d'approbation d'enregistrements nouveaux ou modifiés, par exemple de documents, de feuilles et de fiches client, en créant des flux de travail avec des étapes pour les approbations en question. Avant de créer des flux d'approbation, vous devez configurer un approbateur et un approbateur remplaçant pour chaque utilisateur approbation. Vous pouvez également définir les montants maximaux que les approbateurs sont qualifiés à approuver pour les enregistrements de vente et d'achat. Les demandes d'approbation et d'autres notifications peuvent être envoyées par e-mail ou note interne. Pour chaque configuration d'utilisateur d'approbation, vous pouvez également définir à quel moment ils reçoivent les notifications.  

 Vous pouvez configurer et utiliser des workflows qui connectent des tâches de processus entreprise exécutées par différents utilisateurs. Les tâches du système, telles que la validation automatique, peuvent être incluses comme étapes du workflow, précédées ou suivies des tâches de l'utilisateur. Demander et accorder une approbation pour créer des enregistrements sont des étapes classiques du workflow. Pour plus d'informations, voir [Flux de travail](across-workflow.md).  

## <a name="about-this-walkthrough"></a>À propos de cette procédure pas à pas  
Cette procédure pas à pas présente les tâches suivantes :  

-   Configuration des utilisateurs d'approbation (y compris la configuration d'un utilisateur dans Windows et dans [!INCLUDE[d365fin](includes/d365fin_md.md)]).  
-   Configuration des notification pour les utilisateurs approbation.  
-   Modification et activation d'un flux d'approbation.  
-   Démarrage de la file projets qui distribue les notifications.  
-   Demande d'approbation d'une commande achat (Alicia).  
-   Réception d'une notification, puis acceptation de la demande (Sean).  

## <a name="prerequisites"></a>Conditions préalables  
Pour effectuer cette procédure pas à pas, vous aurez besoin de la société de démonstration CRONUS International Ltd.

## <a name="story"></a>Scénario  
Sean est super utilisateur chez CRONUS, sur son propre ordinateur.  

Il crée deux utilisateurs d’approbation. Le premier est Alicia, qui représente un agent d'achats. L'autre, c'est lui-même, soit l'approbateur d'Alicia. Ensuite, Sean s'octroie des droits d'approbation pour un montant d'achat illimité et spécifie qu'il recevra les notifications par note interne dès qu'un événement approprié se produira. Enfin, Sean crée le flux d'approbation requis en tant que copie du modèle Flux de travail approbation commande achat existant, laisse toutes les conditions d'événement et options de réponse existantes inchangées, puis active le flux.  

Pour tester le flux d'approbation, Sean se connecte d'abord à [!INCLUDE[d365fin](includes/d365fin_md.md)] sous l'identité d'Alicia, puis demande l'approbation d'une commande achat. Ensuite, Sean se connecte en tant que lui-même, voit la note dans son Tableau de bord, suit le lien vers la demande d'approbation de la commande achat, et approuve la demande.  

## <a name="setting-up-the-sample-data"></a>Configuration des exemples de données  
Vous devez créer un nouvel utilisateur sur l'ordinateur local et dans [!INCLUDE[d365fin](includes/d365fin_md.md)] représentant Alicia, que vous sélectionnerez ultérieurement en tant qu'utilisateur d'approbation. Votre propre compte d'utilisateur représentera Sean.  

### <a name="to-add-alicia-as-a-user-on-the-local-computer"></a>Pour ajouter Alicia en tant qu'utilisateur sur l'ordinateur local  

1.  Choisissez **Démarrer**, dans la zone **Rechercher les programmes et fichiers**, saisissez **Modifier les utilisateurs et les groupes locaux**, puis sélectionnez le lien associé.  
2.  Ouvrez le dossier **Utilisateurs**.  
3.  Sous l'onglet **Actions**, choisissez **Nouvel utilisateur**.  
4.  Dans le champ **Nom utilisateur**, entrez Alicia.  
5.  Dans les champs **Mot de passe** et **Confirmer mot de passe**, entrez un mots de passe valide.  
6.  Désactivez la case à cocher **L'utilisateur doit changer le mot de passe à la prochaine ouverture de session**.  
7.  Fermez la fenêtre **Utilisateurs et groupes locaux**.  

### <a name="to-add-alicia-as-a-user-in-included365finincludesd365finmdmd"></a>Pour ajouter Alicia en tant qu'utilisateur dans [!INCLUDE[d365fin](includes/d365fin_md.md)]  
1.  Choisissez l'icône ![Page ou état pour la recherche](media/ui-search/search_small.png "Page ou état pour la recherche"), entrez **Utilisateurs**, puis sélectionnez le lien connexe.  
2.  Dans la fenêtre **Utilisateurs Windows**, sous l'onglet **Accueil**, dans le groupe **Nouveau**, choisissez **Nouveau**.  
3.  Dans la fenêtre **Fiche utilisateur**, dans le champ **Nom utilisateur**, saisissez Alicia.  
4.  Dans le champ **Nom d'utilisateur Windows**, cliquez sur le bouton AssistEdit.  
5.  Dans la fenêtre **Sélectionner un utilisateur ou un groupe**, dans le champ **Entrer les noms d'objet à sélectionner**, entrez Alicia, puis sélectionnez le bouton **Vérifier les noms**.  
6.  Lorsque [ORDINATEUR]ALICIA s'affiche dans le champ, cliquez sur le bouton **OK**.  
7.  Dans le raccourci **Ensembles d'autorisations utilisateur**, dans le champ **Ensemble d'autorisations**, sélectionnez **SUPER**.  
8.  Dans le champ **Société**, sélectionnez **CRONUS International Ltd.**  
9. Cliquez sur le bouton **OK**.  

## <a name="setting-up-approval-users"></a>Configuration des utilisateurs approbation  
À l'aide de l'utilisateur Windows que vous venez de créer, configurez Alicia en tant qu'utilisateur approbation dont vous êtes l'approbateur. Configurez vos droits d'approbation et spécifiez comment et quand être averti des demandes d'approbation.  

### <a name="to-set-up-yourself-and-alicia-as-approval-users"></a>Pour configurer votre propre profil et celui d'Alicia en tant qu'utilisateurs approbation  
1.  Choisissez l'icône ![Page ou état pour la recherche](media/ui-search/search_small.png "Page ou état pour la recherche"), entrez **Paramètres utilisateur approbation**, puis choisissez le lien associé.  
2.  Dans la fenêtre **Paramètres utilisateur approbation**, sous l'onglet **Accueil**, dans le groupe **Nouveau**, choisissez **Nouveau**.  

    > [!NOTE]  
    >  Vous devez configurer un approbateur avant de pouvoir configurer des utilisateurs qui ont besoin de l'approbation de l'approbateur. Par conséquent, vous devez configurer votre propre profil avant de configurer celui d'Alicia.  

3.  Configurez les deux utilisateurs approbation en renseignant les champs comme indiqué dans le tableau suivant.  

    |Code utilisateur|ID approbateur|Montant illimité d'achat autorisé|  
    |-------------|-----------------|---------------------------------|  
    |[ORDINATEUR][VOUS]||Sélectionné|  
    |[ORDINATEUR]ALICIA|[ORDINATEUR][VOUS]||  

## <a name="setting-up-notifications"></a>Configuration de notifications  
Spécifiez comment et quand être averti des demandes d'approbation.  

### <a name="to-set-up-how-and-when-you-are-notified"></a>Pour spécifier comment et quand recevoir les notifications  
1.  Dans la fenêtre **Paramètres utilisateur approbation**, sélectionnez la ligne correspondant à vous-même, puis sous l'onglet **Accueil**, dans le groupe **Processus**, choisissez **Paramètres de notification**.  
2.  Dans la fenêtre **Paramètres de notification**, dans le champ **Type de notification**, entrez **Approbation**.  
3.  Cliquez sur le champ **Code modèle de notification**, puis sélectionnez le bouton **Avancé**.  
4.  Dans la fenêtre **Modèles de notification**, sous l'onglet **Accueil**, dans le groupe **Gérer**, choisissez **Modifier la liste**.  
5.  Sur la ligne du modèle d'approbation, dans le champ **Mode de notification**, entrez **Note**.  
6.  Cliquez sur le bouton **OK**.  
7.  Dans la fenêtre **Notification Setup**, sous l'onglet **Accueil**, dans le groupe **Processus**, choisissez **Tableau de notification**.  
8.  Dans la fenêtre **Tableau de notification**, dans le champ **Récurrence**, sélectionnez **Immédiatement**.  
9. Cliquez sur le bouton **OK**.  

## <a name="creating-the-approval-workflow"></a>Création d'un flux d'approbation  
 Créez le flux d'approbation de commande d'achat en copiant les étapes du modèle de Flux de travail approbation commande achat. Laissez les étapes existantes du flux inchangées, puis activez le flux.  

### <a name="to-create-and-enable-a-purchase-order-approval-workflow"></a>Pour créer et activer un flux d'approbation de commande d'achat  
1.  Sélectionnez l'icône ![Page ou état pour la recherche](media/ui-search/search_small.png "Page ou état pour la recherche"), entrez **Flux de travail**, puis sélectionnez le lien connexe.  
2.  Dans la fenêtre **Flux de travail**, sous l'onglet **Actions**, dans le groupe **Général**, choisissez **Créer le flux de travail à partir du modèle**.  
3.  Sous l'onglet **Actions**, dans le groupe **Général**, choisissez **Créer le flux de travail à partir du modèle**. La fenêtre **Modèles flux de travail** s'ouvre.  
4.  Sélectionnez le modèle de flux de travail nommé Flux de travail approbation commande achat, puis choisissez le bouton **OK**.  

    La fenêtre **Flux de travail** s'ouvre pour un nouveau flux de travail contenant toutes les informations du modèle sélectionné. La valeur du champ **Code** est étendue avec « -01 » pour indiquer que ce premier flux de travail est créé à partir du modèle Flux de travail approbation commande achat.  
5.  Dans l'en-tête de la fenêtre **Flux de travail**, activez la case à cocher **Activé**.  

## <a name="starting-a-notification-job-queue"></a>Démarrage de la file projets des notifications  
Assurez-vous que la file projets dans votre installation est configurée pour traiter les notifications du workflow.  

### <a name="to-start-the-notify-job-queue"></a>Pour lancer la file projets NOTIFY  
1.  Sélectionnez l'icône ![Page ou état pour la recherche](media/ui-search/search_small.png "Page ou état pour la recherche"), entrez **File d'attente des travaux**, puis sélectionnez le lien connexe.  
2.  Dans la fenêtre **File d'attente des travaux**, sélectionnez la ligne correspondant à la file projets NOTIFY, puis sous l'onglet **Accueil**, dans le groupe **Processus**, choisissez **Démarrer la file projets**.  

## <a name="using-the-approval-workflow"></a>Utilisation du flux d'approbation  
Utilisez le nouveau Flux de travail approbation commande achat en ouvrant une session dans [!INCLUDE[d365fin](includes/d365fin_md.md)] en tant qu'Alicia pour demander l'approbation d'une commande achat. Ensuite, connectez-vous en tant que vous-même, affichez la note dans le Tableau de bord, suivez le lien vers la demande d'approbation, puis approuvez la demande.  

Pour vous connecter à [!INCLUDE[d365fin](includes/d365fin_md.md)] en tant qu'utilisateur différent, utilisez la fonction **Exécuter en tant qu'utilisateur différent**.  

### <a name="to-log-into-included365finincludesd365finmdmd-as-alicia"></a>Pour vous connecter à [!INCLUDE[d365fin](includes/d365fin_md.md)] en tant qu'Alicia  

1.  Pour le client Web [!INCLUDE[d365fin](includes/d365fin_md.md)], sur le bouton de lancement du navigateur Web, appuyez sur Maj + clic droit, puis choisissez **Exécuter en tant qu'utilisateur différent**.  

    Pour le client Windows [!INCLUDE[d365fin](includes/d365fin_md.md)], sur le bouton de lancement du programme, appuyez sur Maj + clic droit, puis choisissez **Exécuter en tant qu'utilisateur différent**.  

2.  Dans la fenêtre **Sécurité Windows**, entrez [ORDINATEUR]ALICIA et le mot de passe requis.  

### <a name="to-request-approval-of-a-purchase-order-as-alicia"></a>Pour demander l'approbation d'une commande achat en tant qu'Alicia  

1.  Sélectionnez l'icône ![Page ou état pour la recherche](media/ui-search/search_small.png "Page ou état pour la recherche"), entrez **Commandes achat**, puis sélectionnez le lien connexe.  
2.  Sélectionnez la ligne pour ouvrir la commande d'achat 104001, puis sous l'onglet **Accueil**, dans le groupe **Gestion**, choisissez **Modifier**.  
3.  Dans la fenêtre **Commande achat**, sous l'onglet **Actions**, dans le groupe **Approbation**, choisissez **Envoyer demande d'approbation**.  

    Notez que la valeur du champ **Statut** est passée à **Approbation en attente**.  

4.  Fermez [!INCLUDE[d365fin](includes/d365fin_md.md)].  

### <a name="to-approve-the-purchase-order-as-sean"></a>Pour approuver la commande achat en tant que Sean  

1.  Ouvrez [!INCLUDE[d365fin](includes/d365fin_md.md)] normalement. Le programme s'ouvre avec vous-même en tant qu'utilisateur.  
2.  Dans le Tableau de bord, dans la fenêtre **Mes notifications**, recherchez une nouvelle note d'Alicia.  

    > [!NOTE]  
    >  Bien que la récurrence de notification soit définie sur **Immédiatement**, la note arrivera environ une minute après l'envoi de la demande d'approbation par Alicia. Ceci est dû à la fréquence de récurrence par défaut de la fonctionnalité file projets.  

3.  Lorsque la note s'affiche dans la fenêtre **Mes notifications**, sélectionnez la valeur **Écriture approbation : XX, XX** dans le champ **Page**. La fenêtre **Demandes à approuver** s'ouvre avec la demande de commande d'achat d'Alicia en surbrillance.  
4.  Dans le fenêtre **Demandes à approuver**, sous l'onglet **Accueil**, dans le groupe **Traitement**, choisissez **Approuver**.  

    La valeur du champ **Statut** de la commande d'achat d'Alicia passe à **Lancé**.  

Vous venez de configurer et tester un flux de travail d'approbation simple incluant les deux premières étapes du Flux de travail approbation commande achat. Vous pouvez facilement étendre ce flux pour valider automatiquement la commande d'achat d'Alicia lorsque c'est Sean qui l'approuve. Pour cela, vous devez activer le Flux de travail facture achat, dans lequel la réponse à une facture d'achat lancée est de la valider. Vous devez d'abord modifier la condition d'événement de la première étape du flux (achat) en remplaçant **Facturer** par **Commander**.  

La version [!INCLUDE[d365fin](includes/d365fin_md.md)] générique inclut un certain nombre de modèles de flux de travail pour les scénarios pris en charge par le code d'application. La plupart concernent des flux d'approbation. Pour plus d'informations, voir Modèles flux de travail.  

Définissez les variations des flux de travail en renseignant les champs des lignes à partir des listes fixes de valeurs d'événement et de réponse qui sont les scénarios pris en charge par le code d'application. Pour plus d'informations, reportez\-vous à [Procédure : créer des flux de travail](across-how-to-create-workflows.md).  

Si un scénario d'entreprise requiert un événement ou une réponse de workflow qui n'est pas pris en charge, un partenaire Microsoft doit l'implémenter en personnalisant le code de l'application. Pour plus d'informations, voir [Procédure pas à pas : implémentation de nouveaux événements et réponses de flux de travail](/dynamics-nav/Walkthrough--Implementing-New-Workflow-Events-and-Responses) dans l'Aide destinée aux développeurs et aux professionnels de l'informatique.  

## <a name="see-also"></a>Voir aussi  
[Procédure : configurer des utilisateurs d'approbation](across-how-to-set-up-approval-users.md)   
[Configuration de notifications de workflow](across-setting-up-workflow-notifications.md)   
[Procédure : créer des workflows](across-how-to-create-workflows.md)   
[Procédure : utilisation des flux d'approbation](across-how-use-approval-workflows.md)   
[Flux de travail](across-workflow.md)

