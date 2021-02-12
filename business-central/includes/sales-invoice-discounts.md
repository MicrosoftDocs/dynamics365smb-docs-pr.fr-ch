---
author: edupont04
ms.service: dynamics365-business-central
ms.topic: include
ms.date: 01/20/2021
ms.author: edupont
ms.openlocfilehash: 718845561c1a18701d20b93ebdc8339308ce7ac8
ms.sourcegitcommit: adf1a87a677b8197c68bb28c44b7a58250d6fc51
ms.translationtype: HT
ms.contentlocale: fr-CH
ms.lasthandoff: 01/21/2021
ms.locfileid: "5035815"
---
Lorsque tous les articles ont été entrés sur les lignes commande vente, vous pouvez calculer la remise sur facture pour l’ensemble du document vente en choisissant l’action **Calculer remise facture**.

Si le champ **Calculer remise facture** est sélectionné dans la fenêtre **Paramètres ventes**, la remise facture est calculée automatiquement lorsque vous effectuez l’une des actions suivantes sur un document vente :

* Afficher les statistiques
* Afficher une impression test
* Imprimer
* Comptabilisation

La remise est répartie sur toutes les lignes du document vente pour les articles et les ressources pour lesquels le champ **Remise facture autorisée** de la ligne commande vente indique **Oui**. C’est la configuration par défaut pour les articles.

Les conditions de remise facture sont définies sur la page **Remise facture client** pour calculer la remise facture. Le code devise du document vente est utilisé pour trouver les conditions remise facture de la devise.

Si vous n’avez pas défini de remise facture pour les devises, les conditions de remise facture définies sur la page **Remises facture client** avec des montants dans votre devise locale et le taux de change à la date de comptabilisation du document vente sont utilisés pour calculer la remise facture en devise.
