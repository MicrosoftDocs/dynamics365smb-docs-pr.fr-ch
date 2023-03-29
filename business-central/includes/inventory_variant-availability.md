---
author: edupont04
ms.topic: include
ms.date: 09/21/2022
ms.author: edupont
---
Lorsque vous ouvrez la page **Dispo. article par variante** à partir d’une ligne document, vous pouvez insérer une variante dans la ligne document en sélectionnant la ligne avec la variante que vous souhaitez insérer, puis en cliquant sur OK. Si vous avez utilisé uniquement la page pour afficher la disponibilité et ne souhaitez pas insérer une variante, vous devez fermer la page sans cliquer sur OK.

La page affiche une ligne pour chaque période. Chaque ligne affiche les chiffres de disponibilité de l’article dans les champs clés suivants :

| Champ | Désignation |
|--|--|
| **Besoin brut**| Indique la somme de la demande totale pour cet article. Le besoin brut est égal à la somme de la *demande dépendante* et de la *demande indépendante*. La *demande indépendante* est issue des commandes vente, des commandes service, des ordres de transfert et des prévisions de production. La *demande dépendante* est issue des composants O.F., des ordres de fabrication planifiés, planifiés fermes et lancés. Elle comprend également des lignes de feuilles planning et demande achat.|
| **Réception planifiée** | Spécifie la somme des articles provenant du réapprovisionnement. Le calcul inclut des ordres de fabrication lancés et planifiés fermes, des commandes achat et des ordres de transfert. |
| **Réception prévue** | Spécifie la somme des articles provenant des ordres de fabrication planifiés. |
| **Stock prévisionnel** | Indique les stocks disponibles calculés. |
| **Lancement prévu** | Spécifie la somme des articles provenant des propositions d’ordres de réapprovisionnement. Le calcul inclut les ordres de fabrication planifiés. Il inclut éqalement les lignes des feuilles planning et demande achat calculées en fonction de la date début (de la feuille planning et de l’ordre de fabrication) ou de la date de commande (de la demande achat). Cette somme n’est pas incluse dans les stocks disponibles prévus. Toutefois, elle indique les quantités qui doivent être converties de réceptions prévues en réceptions planifiées. |
