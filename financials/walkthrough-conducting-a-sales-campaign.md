---
title: "Procédure pas à pas : mise en place d'une campagne de vente | Microsoft Docs"
description: "Une campagne désigne tout type d'activité impliquant plusieurs contacts. La sélection du public cible de votre campagne représente une étape importante de la configuration. Pour ce faire, dans Finance and Operations, Business edition, créez un segment ou un groupe de contacts à l'aide de filtres."
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 08/16/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: bec0619be0a65e3625759e13d2866ac615d7513c
ms.openlocfilehash: e933115531f9adb0296ad8983be00da480f11f25
ms.contentlocale: fr-ch
ms.lasthandoff: 03/22/2018

---
# <a name="walkthrough-conducting-a-sales-campaign"></a>Procédure pas à pas : mise en place d'une campagne de vente
Une campagne désigne tout type d'activité impliquant plusieurs contacts. La sélection du public cible de votre campagne représente une étape importante de la configuration. Pour ce faire, dans [!INCLUDE[d365fin](includes/d365fin_md.md)], créez un segment ou un groupe de contacts à l'aide de filtres.  

 Les fonctionnalités du module Ventes & marketing permet de planifier soigneusement vos activités de marketing et de gérer les interactions avec les contacts et clients. Vous pouvez créer des campagnes et configurer des segments de contacts pour le publipostage et d'autres types d'interactions avec vos contacts et prospects.  

 Les fonctionnalités Campagne et Segment et les processus automatisés associés vous permettent de planifier, d'organiser et de suivre vos activités de marketing. Ainsi, vos chances de gagner de nouveaux clients et de fidéliser les clients existants augmentent.  

## <a name="about-this-walkthrough"></a>À propos de cette procédure pas à pas  
 Cette procédure pas à pas répertorie les étapes de suivi d'un salon commercial, ainsi que les étapes de ciblage des clients potentiels (contacts) dans une campagne de suivi.  

 Elle présente la fonctionnalité de gestion des campagnes et segments pour le département Ventes & marketing. Cette procédure pas à pas présente les tâches suivantes :  

-   configuration d'une campagne ;  
-   sélection du public cible ;  
-   exploration de données ;  
-   envoi de lettres aux contacts ;  
-   enregistrement des réponses de campagne.  

## <a name="roles"></a>Rôles  
 Cette procédure pas à pas présente les tâches effectuées par les rôles utilisateur suivants :  

-   Directeur marketing ou directeur des ventes  
-   Membre de l'équipe marketing  

## <a name="prerequisites"></a>Conditions préalables  
 Avant d'exécuter cette procédure pas à pas, veuillez installer [!INCLUDE[d365fin](includes/d365fin_md.md)].  

## <a name="story"></a>Scénario  
 Le directeur marketing du département Ventes de CRONUS est responsable de la planification et de l'exécution des campagnes. Il prend les décisions relatives à la participation ou non de la société à des salons commerciaux et évalue l'évolution des campagnes.  

 Les membres de l'équipe marketing du département Marketing gèrent la production, la distribution, et le placement des supports marketing.  

 La société vient de lancer un nouveau produit appelé Millennium Server. Ce dernier a récemment été exposé au salon informatique Computer Futurus. De nombreux clients ont montré un grand intérêt pour le produit et, dans le cadre d'un effort promotionnel, les clients qui ont acheté Millennium Server pendant la période de campagne se sont vus proposer un prix spécial campagne.  

 Après le salon commercial, l'une des tâches des membres de l'équipe marketing consiste à entrer toutes les informations de contact des clients potentiels.  

 Le directeur marketing configure une campagne, crée un segment contenant les nouveaux contacts, puis explore les données de contact pour sélectionner le public cible de la campagne.  

 Les membres de l'équipe marketing aident à l'envoi de lettres de remerciement à tous les contacts qui ont laissé leur carte de visite sur le stand. Le directeur marketing enregistre toutes les réponses reçues de la part des prospects.  

## <a name="setting-up-a-campaign"></a>Configuration d'une campagne  
 Dès que les membres de l'équipe ont entré les cartes de visite reçues lors du salon commercial, le directeur marketing configure une fiche campagne visant à gérer les activités associées.  

### <a name="to-set-up-a-campaign"></a>Pour configurer une campagne  

1.  Sélectionnez l'icône ![Page ou état pour la recherche](media/ui-search/search_small.png "Page ou état pour la recherche"), saisissez **Campagnes**, puis sélectionnez le lien connexe.  
2.  Choisissez l'action **Nouveau** pour créer une campagne. Dans la fiche campagne, appuyez sur la touche Entrée pour qu'un numéro de campagne soit automatiquement inséré.  
3.  Dans le champ **Description**, entrez la description de la campagne, par exemple, **Salon FUTURUS**.  
4.  Choisissez le champ **Code statut**, puis sélectionnez un code statut dans la liste qui s'ouvre dans la fenêtre **Statut campagne**.  
5.  Renseignez les champs **Date début** et **Date fin** de la campagne en fonction des besoins.  

## <a name="selecting-the-target-audience"></a>Sélection du public cible  
 Le directeur marketing crée un segment pour sélectionner les contacts avec lesquels il souhaite interagir.  

### <a name="to-create-a-segment-with-the-relevant-contacts"></a>Pour créer un segment avec les contacts appropriés  

1.  Sélectionnez l'action **Segments**.  
2.  Choisissez l'action **Nouveau** pour créer un segment. Dans la fiche segment, appuyez sur la touche Entrée pour qu'un numéro de segment soit automatiquement inséré.  
3.  Sur le raccourci **Général**, dans le champ **Description**, entrez par exemple **Visiteurs du salon commercial FUTURUS**.  

     Après avoir entré les informations générales relatives au segment, sélectionnez les contacts à inclure dans celui-ci.  

     Vous pouvez utiliser différents critères pour sélectionner les contacts, par exemple, vous pouvez sélectionner les contacts de personnes travaillant sur le site ou un prospect responsable des achats pour sa société.  

     Utilisez des filtres pour ajouter des contacts en fonction des critères correspondant le mieux à vos besoins. Par exemple, vous pouvez choisir de filtrer la responsabilité du contact, les relations d'affaires ou le secteur d'activité de la société. Pour cette procédure pas à pas, choisissez le filtre **Responsabilité** pour sélectionner les contacts.  

4.  Dans la fenêtre **Segment**, sélectionnez l'action **Ajouter contacts**pour ouvrir le filtre **Ajouter contacts**.  
5.  Sur le raccourci **Responsabilité**, sélectionnez le filtre **Achat** comme **Code responsabilité**, puis choisissez le bouton **OK**.  

     La fenêtre **Segment** inclut désormais une liste de contacts basée sur le filtre entré. Sur le raccourci **Général**, dans le champ **Nbre de lignes**, vous pouvez visualiser en un clin d'œil le nombre de contacts répondant à ces critères.  

    > [!NOTE]  
    >  Vous pouvez enregistrer vos critères de segmentation pour qu'il soient réutilisés ultérieurement.

    1.  Dans la fenêtre **Segment**, sélectionnez l'action **Segment**, puis l'action **Enregistrer critères**.  
    2.  Dans la fenêtre **Critères segment enregistrés**, entrez un code pour le segment. Dans le champ **Description**, entrez la description des critères segment.
    3.  Cliquez sur le bouton **OK**.  

## <a name="mining-the-data"></a>Exploration de données  
 Le directeur marketing observe attentivement la liste segmentée des contacts et réalise que la liste est bien trop longue. Il décide de la réduire en se basant sur de véritables prospects afin d'être certain de se concentrer sur le bon groupe cible. Ce processus de réduction et de redéfinition des données porte également le nom d'exploration de données.  

### <a name="to-remove-contacts-from-the-segment"></a>Pour supprimer des contacts du segment  

1.  Dans la fenêtre **Segment**, sélectionnez l'action **Contacts** ,puis l'action **Réduire les contacts** afin d'ouvrir la fenêtre **Réduire les contacts**.  
2.  Sur le raccourci **Relation d'affaires**, sélectionnez le filtre **PROS** comme **Code relation d'affaires**, puis choisissez le bouton **OK**.  

     La fenêtre **Segment** inclut désormais une liste réduite de contacts. Dans le champ **Nbre de lignes**, vous pouvez visualiser le nombre de contacts répondant à ces critères.  

    > [!NOTE]  
    >  Si vous devez annuler la suppression d'un groupe de contacts, utilisez la fonction **Annuler dernière action**. En d'autres termes, vous pouvez annuler la dernière segmentation.  
    >   
    >  Dans la fenêtre **Segment**, sélectionnez l'action **Segment**, puis l'action **Annuler dernière action**.  
    >   
    >  Les contacts que vous venez de supprimer sont rajoutés à la liste des contacts.  

## <a name="linking-a-segment-to-a-campaign"></a>Association d'un segment à une campagne  
 Le directeur marketing décide que la liste réduite fera office de liste finale et servira pour la campagne. Pour cela, il associe le segment à la campagne Salon FUTURUS.  

### <a name="to-link-a-segment-to-the-campaign"></a>Pour associer un segment à une campagne  

1.  Dans la fenêtre **Segment**, dans le raccourci **Campagne**, sélectionnez le champ **N° campagne** pour sélectionner la campagne à laquelle vous souhaitez lier le segment, par exemple, **CP0001**.  
2.  Puisque ce segment représente la cible de la campagne, sélectionnez la case à cocher **Cible campagne**.  

## <a name="sending-letters-and-email-messages-to-contacts"></a>Envoi de lettres et de messages électroniques à des contacts  
 Les membres de l’équipe marketing aident le directeur marketing à envoyer une correspondance aux prospects, dans laquelle il les remercie de leur visite au salon commercial.  

### <a name="to-use-a-segment-to-send-a-letter-to-a-contact"></a>Pour utiliser un segment afin d’envoyer une lettre à un contact :  

1.  Ouvrez la fiche **Segment** correspondant aux **Visiteurs du salon commercial FUTURUS**.  
2.  Sur le raccourci **Interaction**, dans le champ **Code modèle interaction**, sélectionnez un modèle de lettre commerciale, code **BUS**.  
3.  Dans le champ **Sujet (par défaut)**, entrez le texte exemple suivant : **Merci de votre visite au salon**.  

    > [!NOTE]  
    >  Ce modèle est constitué de plusieurs documents joints, chacun dans une langue différente. Les exemples de langue sont l'anglais et le danois.  

4.  Choisissez le champ **Code langue (par défaut)** pour ouvrir la fenêtre **Langues interaction segment**. Sélectionnez un code langue et cliquez sur le bouton **OK**.  
5.  Vous pouvez afficher le document dans la langue sélectionnée. Choisissez l'action **Document joint**, puis sélectionnez l'action **Ouvrir**.  

     Pour répondre au message demandant l’autorisation de lancer Word, sélectionnez l’option **Autoriser pour cette session client**.  

     Le document Word joint s'ouvre afin que vous puissiez l'inspecter. Vous pouvez également saisir cette opportunité pour éditer et modifier la lettre. Fermez Word lorsque vous avez terminé.  

6.  Entrez le sujet de la lettre dans le champ **Sujet**, dans la langue sélectionnée pour le modèle.  
7.  Sélectionnez l'action **Journal**.
8.  Cochez la case **Envoyer les documents joints** pour imprimer les documents joints.  

    1. Cochez la case **Créer suivi segment**.  
    2. Cliquez sur le bouton **OK** pour commencer le traitement par lots **Journaliser segment**.  

9. Les documents joints sont envoyés. Lorsque le processus est terminé, cliquez sur le bouton **OK** associé au message qui indique que le segment a été journalisé.  

     Les lettres sont automatiquement imprimées et le segment journalisé. Comme le segment a été journalisé, il ne figure plus dans la liste des segments, mais est déplacé dans la liste des segments journalisés. Pour afficher cette liste, choisissez l'icône ![Page ou état pour la recherche](media/ui-search/search_small.png "Page ou état pour la recherche"), entrez **Segments consignés**, puis sélectionnez le lien connexe.  

10. Une fois le segment enregistré, chaque lettre envoyée est enregistrée en tant qu’interaction, que vous pouvez afficher dans le journal.  

     Choisissez l'icône ![Page ou état pour la recherche](media/ui-search/search_small.png "Page ou état pour la recherche"), entrez **Écritures journal interaction**, puis sélectionnez le lien connexe. Chaque lettre envoyée est associée à une entrée.  

### <a name="to-send-an-email-message-to-a-contact"></a>Pour envoyer un message électronique à un contact :  

1.  Sur le raccourci **Interaction**, dans le champ **Code modèle interaction**, sélectionnez un modèle de lettre commerciale, code **BUS**.  
2.  Dans le champ **Sujet (par défaut)**, entrez le texte exemple suivant : **Merci de votre visite au salon**.  
3.  Dans le champ **Type correspondance**, sélectionnez **E-mail**.  
4.  Spécifiez les paramètres de langue, comme dans la procédure précédente.  
5.  Sélectionnez l'action **Journal**. La fenêtre **Journaliser segment** s’affiche.  
6.  Cochez la case **Envoyer les documents joints** pour imprimer les documents joints envoyés par courrier électronique.  
7.  Cochez la case **Créer suivi segment**.  
8.  Cliquez sur le bouton **OK**.  

     Les lettres sont automatiquement envoyées par courrier électronique et le segment journalisé. Comme le segment a été journalisé, il ne figure plus dans la liste des segments, mais est enregistré dans la liste des segments journalisés. Pour afficher cette liste, choisissez l'icône ![Page ou état pour la recherche](media/ui-search/search_small.png "Page ou état pour la recherche"), entrez **Segments consignés**, puis sélectionnez le lien connexe.  

## <a name="registering-campaign-responses"></a>Enregistrement des réponses de campagne  
 Au cours des semaines suivantes, les prospects répondent à la lettre. Le directeur marketing souhaite assurer le suivi des réponses et enregistre ces interactions.  

 Pour cela, configurez un segment pour les contacts ayant répondu à la lettre.  

### <a name="to-register-campaign-responses"></a>Pour enregistrer les réponses de la campagne  

1.  Dans la fenêtre **Segment**, affichez le raccourci **Interaction**.  
2.  Cliquez sur le champ **Code modèle interaction** .  

     Aucun modèle d'interaction n'existe pour l'enregistrement des réponses à la campagne. Par conséquent, créez un nouveau modèle.  

3.  Dans la fenêtre **Modèles d'interaction**, cliquez sur l'action **Nouveau**.  
4.  Dans le champ **Code**, entrez **RESP**. Dans le champ **Description**, entrez **Réponses à la campagne**.  
5.  Cliquez sur le bouton **OK**.  
6.  Sélectionnez ce modèle d'interaction dans le champ **Code modèle interaction**, puis confirmez le message demandant si vous souhaitez mettre à jour les lignes segment associées au même code modèle interaction.  

     Spécifiez à présent que ces contacts ont répondu à la campagne :  
7.  Dans le raccourci **Campagne**, dans le champ **N° campagne** , sélectionnez votre campagne.  
8.  Ne modifiez pas le champ **N° campagne** et acceptez le message vous demandant si vous souhaitez mettre à jour les lignes segment associées au même Code modèle interaction.  
9. Sélectionnez le champ **Réponse campagne** et acceptez le message qui s'affiche.  

     Journalisez le segment pour vous assurer que les interactions sont enregistrées.  
10. Dans la fenêtre **Segment**, sélectionnez l'action **journal**.  
11. Dans la fenêtre **Journaliser segment**, désactivez la case à cocher **Envoyer les documents joints**, puis choisissez le bouton **OK** et acceptez le message qui s'affiche.  

     Une fois le segment journalisé, une écriture pour la campagne est automatiquement créée pour enregistrer cette action dans la fenêtre **Ecritures campagne**.  

## <a name="see-also"></a>Voir aussi  
[Gestion des relations](marketing-relationship-management.md)  
 [Procédures pas à pas liées au processus entreprise](walkthrough-business-process-walkthroughs.md)  
 [Utilisation de [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

