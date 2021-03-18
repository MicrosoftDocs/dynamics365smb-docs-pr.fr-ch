---
author: edupont04
ms.service: dynamics365-business-central
ms.topic: include
ms.date: 01/25/2021
ms.author: edupont
ms.openlocfilehash: 539ee2eb2c9e4a71eacfb78d95320870128fb1d9
ms.sourcegitcommit: cb06aa973f5c767df774b0e1e199c6fbe0e85b88
ms.translationtype: HT
ms.contentlocale: fr-CH
ms.lasthandoff: 02/17/2021
ms.locfileid: "5470302"
---
Lorsque tous les articles ont été entrés sur les lignes vente, vous pouvez calculer la remise sur facture pour l’ensemble du document vente en choisissant l’action **Calculer remise facture**.

La remise est calculée en fonction de toutes les lignes du document vente pour les articles et les ressources pour lesquels le champ **Remise facture autorisée** de la ligne commande vente indique **Oui**. C’est la configuration par défaut pour les articles. Les lignes avec des frais annexes, par exemple, ne sont pas incluses dans le calcul de la remise facture. Si vous souhaitez appliquer une remise à ces lignes, vous devez définir le champ **% remise ligne** sur les lignes appropriées.  

> [!TIP]
> Si le champ **Calculer remise facture** est sélectionné dans la page **Paramètres ventes**, la remise facture est calculée automatiquement lorsque vous effectuez l’une des actions suivantes sur un document vente :
>
> * Afficher les statistiques
> * Afficher une impression test
> * Imprimer
> * Comptabilisation

Les conditions de remise facture pour un client sont définies sur la page **Remise facture client** pour le client. Le code devise du document vente est utilisé pour trouver les conditions remise facture de la devise.

Si vous n’avez pas défini de remise facture pour les devises, les conditions de remise facture définies sur la page **Remises facture client** avec des montants dans votre devise locale et le taux de change à la date de comptabilisation du document vente sont utilisés pour calculer la remise facture en devise.
