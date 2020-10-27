---
title: Config. identifiant messagerie | Microsoft Docs
description: Apprenez à transformer les interactions de messagerie entre les vendeurs et les clients en véritables opportunités de vente.
author: bholtorf
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: relationship, prospect, opportunity, email
ms.date: 10/01/2020
ms.author: bholtorf
ms.openlocfilehash: f02e78e0b5c7d7f6d3c22cd12e37bdaf74f4b90f
ms.sourcegitcommit: ddbb5cede750df1baba4b3eab8fbed6744b5b9d6
ms.translationtype: HT
ms.contentlocale: fr-CH
ms.lasthandoff: 10/01/2020
ms.locfileid: "3923635"
---
# <a name="track-email-message-exchanges-between-salespeople-and-contacts"></a>Suivre les échanges de messages électroniques entre les vendeurs et les contacts

Tirez le meilleur parti des communications entre les vendeurs et vos clients existants ou potentiels en suivant les échanges de courriers électroniques, puis en les transformant en opportunités exploitables. [!INCLUDE[d365fin](includes/d365fin_md.md)] peut utiliser Exchange Online pour conserver un journal des messages entrants et sortants. Vous pouvez afficher et analyser le contenu de chaque message sur la page **Écritures journal interaction** .

## <a name="set-up-public-folders-and-rules-for-email-logging-in-exchange-online"></a>Configurer les dossiers publics et les règles de connexion à la messagerie dans Exchange Online

[!INCLUDE[admin-setup-email-public-folder](includes/admin-setup-email-public-folder.md)]

Ensuite, vous connectez [!INCLUDE[prodshort](includes/prodshort.md)] à Exchange Online.

## <a name="setting-up-d365fin-to-log-email-messages"></a>Configuration de [!INCLUDE[d365fin](includes/d365fin_md.md)] pour enregistrer les messages électroniques

Commencez avec la connexion à la messagerie en deux étapes :

1. Connectez [!INCLUDE[d365fin](includes/d365fin_md.md)] à Exchange Online pour votre abonnement Microsoft 365. Exchange Online gère vos e-mails. Nous avons facilité cette étape en fournissant un guide de configuration assisté. Vous avez juste besoin de vos identifiants d’administrateur pour votre compte d’administrateur dans Microsoft 365. Pour commencer le guide, accédez à **Configuration assistée** , puis choisissez **Configurer la journalisation des emails** .  

2. Assurez-vous que des adresses électroniques valides ont été entrées dans [!INCLUDE[d365fin](includes/d365fin_md.md)] pour vos commerciaux et vos contacts, selon qu’ils sont des clients potentiels ou existants. Pour ce faire, pour chaque client ou vendeur, ouvrez la fiche **Contact** ou **Vendeur/Acheteur** et regardez le champ **E-mail** .

> [!Tip]
> Une fois les étapes du guide terminées, vous pouvez vérifier si la connexion a réussi. Recherchez **Paramètres marketing** , choisissez **Traiter** , puis **Fonctions** et **Valider la configuration de la connexion à la messagerie** .

## <a name="viewing-email-message-exchanges-in-the-interaction-log"></a>Affichage des échanges de messages électroniques dans le journal des interactions

[!INCLUDE[d365fin](includes/d365fin_md.md)] crée une entrée sur la page **Journal des interactions** chaque fois qu’un vendeur et un contact échangent un message par courrier électronique. Pour afficher le journal des interactions, ouvrez la fiche **Contact** ou **Vendeur/Acheteur** pour la personne, puis choisissez **Historique** , et **Écritures journal interaction** . Nous pouvons faire certaines choses avec chaque entrée du journal, par exemple :

- Affichez le contenu du message électronique échangé en cliquant sur l’action **Afficher les pièces jointes** .
- Transformez un échange de courrier électronique en opportunité de vente. Si une entrée semble prometteuse, vous pouvez la transformer en opportunité, puis gérer son évolution vers une vente. Pour cela, sélectionnez l’entrée, puis cliquez sur l’action **Créer une opportunité** . Pour plus d’informations, voir [Gérer des opportunités de vente](marketing-manage-sales-opportunities.md).

## <a name="see-also"></a>Voir aussi
[Gestion des relations](marketing-relationship-management.md)

