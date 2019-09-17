---
title: Config. identifiant messagerie | Microsoft Docs
description: Apprenez à transformer les interactions de messagerie entre les vendeurs et les clients en véritables opportunités de vente.
services: project-madeira
documentationcenter: ''
author: bholtorf
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: relationship, prospect, opportunity, email
ms.date: 08/26/2019
ms.author: bholtorf
ms.openlocfilehash: e42618be17ff4f9bfe0d54a88e70d5a1841568c1
ms.sourcegitcommit: 8d9f08304b2f3b5504332bc626383797564ac5e3
ms.translationtype: HT
ms.contentlocale: fr-CH
ms.lasthandoff: 08/26/2019
ms.locfileid: "1920481"
---
# <a name="track-email-message-exchanges-between-salespeople-and-contacts"></a>Suivre les échanges de messages électroniques entre les vendeurs et les contacts
Tirez le meilleur parti des communications entre les vendeurs et vos clients existants ou potentiels en suivant les échanges de courriers électroniques, puis en les transformant en opportunités exploitables. [!INCLUDE[d365fin](includes/d365fin_md.md)] peut utiliser Exchange Online pour conserver un journal des messages entrants et sortants. Vous pouvez afficher et analyser le contenu de chaque message sur la page **Écritures journal interaction**.

> [!VIDEO https://go.microsoft.com/fwlink/?linkid=2085401]

## <a name="setting-up-included365finincludesd365fin_mdmd-to-log-email-messages"></a>Configuration de [!INCLUDE[d365fin](includes/d365fin_md.md)] pour enregistrer les messages électroniques
Commencez avec la connexion à la messagerie en deux étapes :

1. Connectez [!INCLUDE[d365fin](includes/d365fin_md.md)] à Exchange Online pour votre abonnement Office 365. Exchange Online gère vos e-mails. Nous avons facilité cette étape en fournissant un guide de configuration assisté. Vous avez juste besoin de vos identifiants d’administrateur pour votre compte d’administrateur dans Office 365. Pour commencer le guide, accédez à **Configuration assistée**, puis choisissez **Configurer la journalisation des emails**. 
2. Assurez-vous que des adresses électroniques valides ont été entrées dans [!INCLUDE[d365fin](includes/d365fin_md.md)] pour vos commerciaux et vos contacts, selon qu’ils sont des clients potentiels ou existants. Pour ce faire, pour chaque client ou vendeur, ouvrez la fiche **Contact** ou **Vendeur/Acheteur** et regardez le champ **E-mail**.

> [!Tip]
> Une fois les étapes du guide terminées, vous pouvez vérifier si la connexion a réussi. Recherchez **Paramètres marketing**, choisissez **Traiter**, puis **Fonctions** et **Valider la configuration de la connexion à la messagerie**.

## <a name="viewing-email-message-exchanges-in-the-interaction-log"></a>Affichage des échanges de messages électroniques dans le journal des interactions
[!INCLUDE[d365fin](includes/d365fin_md.md)] crée une entrée sur la page **Journal des interactions** chaque fois qu'un vendeur et un contact échangent un message par courrier électronique. Pour afficher le journal des interactions, ouvrez la fiche **Contact** ou **Vendeur/Acheteur** pour la personne, puis choisissez **Naviguer**, **Historique**, puis choisissez **Écritures journal interaction**. Nous pouvons faire certaines choses avec chaque entrée du journal, par exemple :

* Affichez le contenu du message électronique échangé en cliquant sur l'action **Afficher les pièces jointes**.
* Transformez un échange de courrier électronique en opportunité de vente. Si une entrée semble prometteuse, vous pouvez la transformer en opportunité, puis gérer son évolution vers une vente. Pour cela, sélectionnez l'entrée, puis cliquez sur l'action **Créer une opportunité**. Pour plus d'informations, voir [Gérer des opportunités de vente](marketing-manage-sales-opportunities.md).

## <a name="see-also"></a>Voir aussi
[Gestion des relations](marketing-relationship-management.md)

