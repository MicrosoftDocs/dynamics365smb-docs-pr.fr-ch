---
title: "Procédure pas à pas\_: Mise en place d’une campagne de vente"
description: "Cette procédure pas à pas donne un aperçu détaillé de toutes les tâches impliquées dans la conduite d’une campagne de vente dans Business\_Central."
author: brentholtorf
ms.topic: conceptual
ms.devlang: al
ms.search.keywords: null
ms.date: 06/24/2021
ms.author: bholtorf
ms.service: dynamics-365-business-central
---
# <a name="walkthrough-conducting-a-sales-campaign"></a>Procédure pas à pas : Mise en place d’une campagne de vente

Une campagne désigne tout type d’activité impliquant plusieurs contacts. La sélection du public cible de votre campagne représente une étape importante de la configuration. Pour ce faire, dans [!INCLUDE[prod_short](includes/prod_short.md)], créez un segment ou un groupe de contacts à l’aide de filtres.  

 Les fonctionnalités du module Ventes & marketing permet de planifier soigneusement vos activités de marketing et de gérer les interactions avec les contacts et clients. Vous pouvez créer des campagnes et configurer des segments de contacts pour le publipostage et d’autres types d’interactions avec vos contacts et prospects.  

 Les fonctionnalités Campagne et Segment et les processus automatisés associés vous permettent de planifier, d’organiser et de suivre vos activités de marketing. Ainsi, vos chances de gagner de nouveaux clients et de fidéliser les clients existants augmentent.  

## <a name="about-this-walkthrough"></a>À propos de cette procédure pas à pas

 Cette procédure pas à pas répertorie les étapes de suivi d’un salon commercial, ainsi que les étapes de ciblage des clients potentiels (contacts) dans une campagne de suivi.  

 Elle présente la fonctionnalité de gestion des campagnes et segments pour le département Ventes & marketing. Cette procédure pas à pas présente les tâches suivantes :  

- préparation des données ;
- configuration d’une campagne ;  
- sélection du public cible ;  
- exploration de données ;  
- envoi de lettres aux contacts ;  
- enregistrement des réponses de campagne.  

## <a name="roles"></a>Rôles

 Cette procédure pas à pas présente les tâches effectuées par les rôles utilisateur suivants :  

- Directeur marketing ou directeur des ventes  
- Membre de l’équipe marketing  

## <a name="prerequisites"></a>Conditions préalables

 Avant d’exécuter cette procédure pas à pas, veuillez installer [!INCLUDE[prod_short](includes/prod_short.md)].  

## <a name="story"></a>Scénario

 Le directeur marketing du département Ventes de CRONUS est responsable de la planification et de l’exécution des campagnes. Le responsable marketing prend les décisions relatives à la participation ou non de la société à des salons commerciaux et évalue l’évolution des campagnes.  

 Les membres de l’équipe marketing du département Marketing gèrent la production, la distribution, et le placement des supports marketing.  

 La société vient de lancer un nouveau produit appelé Rome Guest Chair. Ce dernier a récemment été exposé au salon Office Futurus. De nombreux clients ont montré un grand intérêt pour le produit et, dans le cadre d’un effort promotionnel, les clients qui ont acheté Rome Guest Chair pendant la période de campagne se sont vus proposer un prix spécial campagne.  

 Après le salon commercial, l’une des tâches des membres de l’équipe marketing consiste à entrer toutes les informations de contact des clients potentiels.  

 Le directeur marketing configure une campagne, crée un segment contenant les nouveaux contacts, puis explore les données de contact pour sélectionner le public cible de la campagne.  

 Les membres de l’équipe marketing aident à l’envoi de lettres de remerciement à tous les contacts qui ont laissé leur carte de visite sur le stand. Le directeur marketing enregistre toutes les réponses reçues de la part des prospects.  

## <a name="setting-up-a-campaign"></a>Configuration d’une campagne

 Dès que les membres de l’équipe ont entré les cartes de visite reçues lors du salon commercial, le directeur marketing configure une fiche campagne visant à gérer les activités associées.  

### <a name="to-set-up-a-campaign"></a>Pour configurer une campagne

1. Sélectionnez l’icône ![Ampoule qui ouvre la fonction Tell Me.](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire") entrez **Campagnes**, puis choisissez le lien associé.  
2. Choisissez l’action **Nouveau** pour créer une campagne. Dans la fiche campagne, sélectionnez <kbd>Entrée</kbd> pour qu’un numéro de campagne soit automatiquement inséré.  
3. Dans le champ **Description**, entrez la description de la campagne, par exemple, **Salon Office Futurus**.  
4. Choisir le champ **Code statut** et sélectionnez le code statut « 1-PLAN ». 
5. Renseignez les champs **Date début** et **Date fin** de la campagne en fonction des besoins.  

## <a name="selecting-the-target-audience"></a>Sélection du public cible

 Le directeur marketing crée un segment pour sélectionner les contacts avec lesquels il souhaite interagir.  
 
 Lorsque vous créez un segment, vous pouvez utiliser divers critères pour sélectionner les contacts qui doivent être des cibles pour le segment. Par exemple, vous pouvez sélectionner des personnes travaillant sur le site ou des prospects responsables des achats pour leur société. Utilisez des filtres pour ajouter des contacts en fonction des critères correspondant le mieux à vos besoins. Par exemple, vous pouvez choisir de filtrer la responsabilité du contact, les relations d’affaires ou le secteur d’activité de la société. Pour cette procédure pas à pas, nous choisissons le filtre **Responsabilité** pour sélectionner les contacts.

### <a name="to-create-a-segment-with-the-relevant-contacts"></a>Pour créer un segment avec les contacts appropriés

1. Choisissez l’action **Naviguer**, puis choisissez **Segments**.  
2. Choisissez l’action **Nouveau** pour créer un segment. Dans la fiche segment, sélectionnez **Entrée** pour qu’un numéro de segment soit automatiquement inséré.  
3. Sur le raccourci **Général**, dans le champ **Description**, entrez par exemple *Visiteurs du salon Office Futurus*.
4. Choisissez l’action **Ajouter contacts** pour ouvrir le filtre **Ajouter contacts**.  
5. Faites défiler vers le raccourci **Responsabilité contact**, sélectionnez le filtre **Achat** comme **Code responsabilité**, puis choisissez le bouton **OK**.  

La page **Segment** inclut désormais une liste de contacts basée sur le filtre entré. Sur le raccourci **Général**, dans le champ **Nbre de lignes**, vous pouvez visualiser en un clin d’œil le nombre de contacts répondant à ces critères.  

> [!NOTE]  
> Vous pouvez enregistrer vos critères de segmentation pour qu’il soient réutilisés ultérieurement.

### <a name="to-save-your-segmentation-criteria"></a>Pour enregistrer vos critères de segmentation

1. Sur la page **Segment**, sélectionnez **Actions**.
2. Choisissez **Fonctions**, puis **Segment**, puis choisissez l’action **Enregistrer critères**.  
3. Sur la page **Critères segment enregistrés**, entrez un code pour le segment. Dans le champ **Description**, entrez la description des critères segment.
4. Cliquez sur le bouton **OK**.  

## <a name="mining-the-data"></a>Exploration de données

 Le directeur marketing observe attentivement la liste segmentée des contacts et réalise que la liste est bien trop longue. Il décide de la réduire en se basant sur de véritables prospects afin d’être certain de se concentrer sur le bon groupe cible. Ce processus de réduction et de redéfinition des données porte également le nom d’exploration de données.  

### <a name="to-remove-contacts-from-the-segment"></a>Pour supprimer des contacts du segment

1. Sur la page **Segment**, sélectionnez **Actions**.
2. Dans la barre de menus ci-dessous, choisissez **Fonctions**, **Contacts**, puis **Réduire les contacts**.  

  Vous ouvrez ainsi la boîte de dialogue **Supprimer contacts – Réduire**.  
4. Sur le raccourci **Relation d’affaires contact**, sélectionnez le filtre **CUST** comme **Code relation d’affaires**, puis choisissez le bouton **OK**.

 La page **Segment** inclut désormais une liste réduite de contacts. Dans le champ **Nbre de lignes**, vous pouvez visualiser le nombre de contacts répondant à ces critères.  

 > [!NOTE]  
 > Si vous devez annuler la suppression d’un groupe de contacts, utilisez la fonction **Annuler dernière action**. En d’autres termes, vous pouvez annuler la dernière segmentation.  

### <a name="to-bring-back-the-removed-contacts"></a>Pour rétablir les contacts supprimés

1. Sur la page **Segment**, sélectionnez l’action **Segment**.
2. Sélectionnez l’action **Annuler dernière action**.

Les contacts que vous venez de supprimer sont rajoutés à la liste des contacts.

## <a name="linking-a-segment-to-a-campaign"></a>Association d’un segment à une campagne

Le directeur marketing décide que la liste réduite fera office de liste finale et servira pour la campagne. Pour cela, il associe le segment à la campagne Salon FUTURUS.  

### <a name="to-link-a-segment-to-the-campaign"></a>Pour associer un segment à une campagne

1. Sur la page **Segment**, dans le raccourci **Campagne**, sélectionnez le champ **N° campagne** pour sélectionner la campagne à laquelle vous souhaitez lier le segment, par exemple, **CP0001**.
2. Sélectionnez **Oui**.  
3. Puisque ce segment représente la cible de la campagne, cochez la case **Cible campagne** et choisissez **Oui**.  

## <a name="sending-letters-and-email-messages-to-contacts"></a>Envoi de lettres et de messages électroniques à des contacts

 Les membres de l’équipe marketing aident le directeur marketing à envoyer une correspondance aux prospects, dans laquelle il les remercie de leur visite au salon.

### <a name="to-use-a-segment-to-send-a-letter-to-a-contact"></a>Pour utiliser un segment afin d’envoyer une lettre à un contact :

> [!NOTE]  
> Dans cette procédure, vous devez joindre un document Word. Vous pouvez ajouter des pièces jointes dans n’importe quelle langue.

> [!NOTE]  
> Si besoin, cliquez sur l’icône de crayon **Modifier** pour ouvrir la page en mode édition.

1. Ouvrez la fiche **Segment** correspondant aux **Visiteurs du salon commercial FUTURUS**.  
2. Sur le raccourci **Interaction**, dans le champ **Code modèle interaction**, sélectionnez un modèle de lettre commerciale, code **BUS** et sélectionnez **Oui**.
3. Choisissez le champ **Code langue (par défaut)** pour ouvrir la page **Langues interaction segment**. Sélectionnez un **Code langue** et cliquez sur le bouton **OK**.
4. Assurez-vous que **Type correspondance (par défaut)** est défini sur **Impression**.
5. Dans le champ **Document joint**, cochez la case **Ellipse**. Cela ouvre la boîte de dialogue Importer document.
    1. Sélectionnez le bouton **Choisir** pour choisir votre fichier.
    1. Recherchez le fichier et sélectionnez le bouton **Ouvrir** pour le joindre.
6. Dans le champ **Sujet (par défaut)**, entrez le texte exemple suivant : **Merci de votre visite au salon**. Sélectionnez la touche <kbd>Tab</kbd> pour quitter le champ et sélectionnez le bouton **Oui**.
7. Faites glisser **Envoyer doc Word attachés** sur Activé et sélectionnez le bouton **Oui**.
8. Sélectionnez l’action **Journaliser**. Dans la fenêtre contextuelle Journaliser segment, activez **Créer suivi segment**
9. Cliquez sur le bouton **OK** pour commencer le **Traitement par lots Journaliser segment**.  

Les documents joints sont envoyés. Lorsque le processus est terminé, cliquez sur le bouton **OK** associé au message qui indique que le segment a été journalisé.  

 Les lettres sont automatiquement imprimées et le segment journalisé. Comme le segment a été journalisé, il ne figure plus dans la liste des segments, mais est déplacé dans la liste des segments journalisés. Pour voir cette liste, sélectionnez l’icône ![Ampoule qui ouvre la fonction Fenêtre de recherche.](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire") entrez **Segments journalisés**, puis sélectionnez le lien associé.  

Une fois le segment journalisé, chaque lettre envoyée est enregistrée en tant qu’interaction, que vous pouvez afficher dans le journal.  

Sélectionnez l’icône ![Ampoule qui ouvre la fonction Tell Me.](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire") entrez **Écritures journal interaction**, puis choisissez le lien associé. Chaque lettre envoyée est associée à une entrée.  

### <a name="to-send-an-email-message-to-a-contact"></a>Pour envoyer un message électronique à un contact :

1. Sur le raccourci **Interaction**, dans le champ **Code modèle interaction**, sélectionnez un modèle de lettre commerciale, code **BUS**.  
2. Dans le champ **Sujet (par défaut)**, entrez le texte exemple suivant : **Merci de votre visite au salon**.  
3. Dans le champ **Type correspondance**, sélectionnez **E-mail**.  
4. Spécifiez les paramètres de langue et joignez un document Word, comme dans la procédure précédente.  
5. Sélectionnez l’action **Journal**. La page **Journaliser segment** s’affiche.  
6. Cochez la case **Envoyer les documents joints** pour imprimer les documents joints envoyés par courrier électronique.  
7. Cochez la case **Créer suivi segment**.  
8. Cliquez sur le bouton **OK**.  

 Les lettres sont automatiquement envoyées par courrier électronique et le segment journalisé. Comme le segment a été journalisé, il ne figure plus dans la liste des segments, mais est enregistré dans la liste des segments journalisés. Pour voir cette liste, sélectionnez l’icône ![Ampoule qui ouvre la fonction Tell Me.](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire") entrez **Segments journalisés**, puis sélectionnez le lien associé.  

## <a name="registering-campaign-responses"></a>Enregistrement des réponses de campagne

 Au cours des semaines suivantes, les prospects répondent à la lettre. Le directeur marketing souhaite assurer le suivi des réponses et enregistre ces interactions.  

 Pour cela, configurez un segment pour les contacts ayant répondu à la lettre.  

### <a name="to-register-campaign-responses"></a>Pour enregistrer les réponses de la campagne

1. Sur la page **Segment**, sur le raccourci **Interaction**, choisissez le champ **Code modèle interaction**.  

 Aucun modèle d’interaction n’existe pour l’enregistrement des réponses à la campagne. Par conséquent, créez un nouveau modèle.  

2. Dans la liste déroulante **Modèles interaction**, cliquez sur l’action **Nouveau**.  
3. Dans le champ **Code**, entrez **RESP**. Dans le champ **Description**, entrez **Réponses à la campagne**.  
4. Cliquez sur le bouton **OK**.
5. Choisissez **Oui** pour confirmer que vous souhaitez appliquer ce code de modèle interaction à toutes les lignes de segment.
6. Sur le raccourci **Campagne**, activez le champ **Réponse campagne**. Choisissez **Oui** pour confirmer le message *Vous avez modifié la réponse de campagne*.  
7. Sur la page **Segment**, sélectionnez l’action **journal**.  
8. Sur la page **Journaliser segment**, décochez la case **Envoyer les documents joints**. Choisissez ensuite le bouton **OK** pour confirmer le message indiquant que le segment a été journalisé.  
  
## <a name="see-also"></a>Voir aussi
[Gestion des relations](marketing-relationship-management.md)  
 [Procédures pas à pas liées au processus entreprise](walkthrough-business-process-walkthroughs.md)  
 [Utiliser [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]
