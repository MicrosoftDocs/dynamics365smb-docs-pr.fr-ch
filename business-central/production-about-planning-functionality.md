---
title: À propos de la fonctionnalité Planification
description: Découvrez comment la planification utilise les données de l’offre et de la demande pour suggérer comment équilibrer l’offre pour répondre à la demande.
author: brentholtorf
ms.author: bholtorf
ms.reviewer: andreipa
ms.topic: conceptual
ms.search.form: '5430,'
ms.date: 09/19/2023
ms.custom: bap-template
ms.service: dynamics-365-business-central
---
# À propos de la fonctionnalité Planification

Le système de planification prend en compte toutes les données d'offre et de demande, ajuste les résultats et génère des suggestions pour l'équilibrage de l'offre en fonction de la demande.  

Pour plus d’informations, voir [Détails de conception : planification de l’approvisionnement](design-details-supply-planning.md).  

> [!NOTE]  
> Pour tous les champs mentionnés dans cette rubrique, lisez l’info-bulles pour comprendre leur fonction. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

## Offre et demande

La planification comporte deux volets : l'offre et la demande. Ceux-ci doivent s’équilibrer pour garantir que la demande est satisfaite.  

- La demande désigne toute sorte de besoin brut, tel qu’une commande vente, une commande service ou un besoin composant pour des ordres d’assemblage ou de fabrication, un transfert sortant, une commande ouverte ou une prévision. En outre, il existe d’autres types techniques de demande, tels qu’un ordre de fabrication ou une commande achat négatif, un stock négatif et un retour achat.  
- Le réapprovisionnement fait référence à toute sorte de réapprovisionnement telle qu’un stock, une commande achat, un ordre d’assemblage, un ordre de fabrication ou un transfert enlogement. Par conséquent, il peut y avoir une commande vente ou une commande service négative, un besoin de composant ou un retour vente négatif – tous représentant aussi l’offre d’une certaine façon.  

Un autre objectif du système de planification est de garantir que le stock ne croisse pas inutilement. En cas de baisse de la demande, le système de planification suggère de reporter, de réduire ou d'annuler des ordres de réapprovisionnement existants.  

## Calcul de planification

Le système de planification est guidé par la demande prévue et réelle des clients ainsi que par les paramètres de réapprovisionnement de stock. L’exécution du calcul de planification a pour effet que l’application suggère des mesures spécifiques ([messages d’action](production-how-to-run-mps-and-mrp.md#action-messages)) à prendre concernant le réapprovisionnement possible auprès de fournisseurs, les transferts entre entrepôts ou la production. S'il y a déjà des ordres de réapprovisionnement, les mesures suggérées peuvent être d'augmenter ou d'accélérer les commandes pour répondre à l'évolution de la demande.  

La base de la routine de planification réside dans le calcul gros/net. Les besoins nets déterminent les lancements de commandes planifiées, qui sont programmés sur la base des informations de gamme (articles fabriqués) ou du délai de réapprovisionnement de la fiche article (articles achetés). Les quantités de lancement de commandes planifiées sont basées sur le calcul de planification et affectées par les paramètres définis sur les fiches article individuelles.  

> [!TIP]
> Le système de planification dépend de la façon dont votre organisation utilise les magasins. Pour plus d’informations, consultez [Planification avec ou sans magasins](production-planning-with-without-locations.md).

## Planification à l’aide d’ordres de transfert manuels

Dans le champ **Système réappro** d’une fiche point de stock, vous pouvez configurer le système de planification pour créer des ordres de transfert destinés à équilibrer l’offre et la demande dans tous les magasins.  

Outre ce type d'ordre de transfert automatique, vous devrez parfois effectuer un mouvement général des quantités en stock vers un autre magasin, quelle que soit la demande existante. Vous créez pour cela un ordre de transfert manuel correspondant à la quantité à déplacer. Pour être sûr que le système de planification ne tente pas de manipuler cet ordre de transfert manuel, vous devez paramétrer le champ **Flexibilité planification** des lignes transfert sur Aucune.  

À l’inverse, si vous souhaitez que le système de planification ajuste les quantités de l’ordre de transfert et les dates en fonction de la demande existante, vous devez paramétrer le champ **Flexibilité planification** sur la valeur Illimitée.

## Paramètres de planification

Le paramètres de planification déterminent le moment, la quantité et la méthode de réapprovisionnement en fonction des divers paramètres de la fiche article (ou point de stock - SKU) et des paramètres de production.  

Les paramètres de planification suivants existent pour l’article ou la fiche point de stock :  

- Période tampon  
- Quantité tampon  
- Méthode réapprovisionnement  
- Point de commande
- Stock maximum  
- Niveau de dépassement de capacité  
- Intervalle de planification  
- Période de groupement de lots  
- Période de replanification  
- Quantité de réappro.  
- Délai de sécurité  
- Stock de sécurité  
- Stratégie d’assemblage  
- Mode de lancement  

Les modificateurs d’ordre suivants existent pour l’article ou la fiche point de stock :  

- Qté minimum commande  
- Qté maximum commande  
- Commandé par  

Les champs de paramètres de planning figurant sur la page **Paramètres production** sont les suivants :  

- Code plus bas niv. dyn.  
- Prévision de la demande actuelle  
- Prévision sur magasin  
- Délai de sécurité par défaut  
- Niveau de dépassement de capacité vide  
- Calcul PDP/MRP combiné
- Mag. composant par déf.  
- Période tampon par défaut  
- Quantité tampon par défaut  

Pour en savoir plus, consultez [Détails de conception : paramètres de planification](design-details-planning-parameters.md)  

## Autres champs de planification importants

### Flexibilité planification

Dans la plupart des commandes approvisionnement, comme les ordres de fabrication, vous pouvez sélectionner **Illimité** ou **Aucun** dans le champ **Flexibilité planification** des lignes.

Cela spécifie si l’approvisionnement représenté par la ligne O.F. est pris en compte par le système de planification lors du calcul des messages d’action.
Si le champ affiche l’option **Illimitée**, le système de planification inclut la ligne lors du calcul des messages d’action. S’il est paramétré sur **Aucune**, la ligne est ferme et définitive, et le système de planification n’inclut pas la ligne dans le calcul des messages d’action.

### Avertissement

Le champ d’informations **Alerte** sur la page **Feuille planning** vous informe lorsqu’une ligne planning est créée pour une situation inhabituelle avec un texte. L’utilisateur peut cliquer sur ce texte pour lire des informations supplémentaires. Les types d’alerte suivants existent :

- Urgence
- Exception
- Attention
- Urgence

L’avertissement Urgence est affiché dans deux situations :

- Le stock est négatif à la date de début de la planification.
- Des événements d’offre ou de demande rétroactifs existent.

Si le stock d’un article est négatif à la date de début de la planification, le système de planification suggère une commande approvisionnement d’urgence afin que la quantité négative arrive à la date de début de la planification. Le texte d'avertissement indique la date de début et la quantité de la commande d'urgence.

Les lignes document avec une date d'échéance antérieure à la date de début de la planification sont consolidées dans une commande approvisionnement d'urgence pour que l'article arrive à la date de début de la planification.

### Exception

L’avertissement Exception s’affiche si le stock disponible prévu descend en dessous du stock de sécurité.

Le système de planification suggère une commande approvisionnement pour répondre aux besoins à la date d’échéance. Le texte d’avertissement indique la quantité du stock de sécurité et la date à laquelle elle est entamée.

Entamer le stock de sécurité est considéré comme une exception car cela ne doit pas se produire si le point de commande a été correctement défini.

> [!NOTE]
> L’approvisionnement pour les lignes planning avec les alertes Exception n’est normalement pas modifié en fonction des paramètres de planification. Au lieu de cela, le système de planification propose uniquement un approvisionnement pour couvrir la quantité de demande exacte. Cependant, vous pouvez définir l’exécution de la planification pour respecter certains paramètres de planification pour les lignes planning à respecter avec certaines alertes. Pour plus d’informations, consultez la description du champ **Respecter les paramètres de planification pour les avertissements d’exception** de l’article [Exécuter une planification complète et un calcul PDP ou MRP](production-how-to-run-mps-and-mrp.md).

### Attention

L’avertissement Attention s’affiche dans deux situations :

- La date de début de la planification est antérieure à la date de travail.
- La ligne planification suggère de changer une commande achat lancée ou un O.F.

> [!NOTE]
> Dans les lignes planning comportant des avertissements, le champ **Accepter message d’action** n’est pas sélectionné, car le gestionnaire doit poursuivre l’étude de ces lignes avant de mettre en application ce plan.

## Feuilles planning et demandes achat

Comme décrit dans [Planification](production-planning.md), vous pouvez choisir entre deux feuilles pour la plupart des activités de planification : la feuille planning et la demande achat. La plupart des processus sont décrits en fonction de la feuille planning, mais il existe quelques scénarios où la demande achat est recommandée.

[!INCLUDE [edit-in-excel](includes/edit-in-excel.md)]

### Demande achat

La page **Demande achat** répertorie les articles que vous souhaitez commander. Il existe plusieurs méthodes pour saisir des articles dans la feuille :

- Saisissez les articles manuellement dans la feuille et renseignez les champs correspondants.

- Utilisez le traitement par lots **Calculer planning**. Cette opération permet de calculer un plan de réapprovisionnement pour les articles et les points de stock ayant été configurés avec un système de réapprovisionnement **achat** ou **transfert**. Lorsque vous utilisez ce traitement par lots, le programme renseigne automatiquement le champ **Message d'action** en y indiquant une proposition d'action en vue du réapprovisionnement de l'article. Cette opération peut contribuer, par exemple, à augmenter la quantité d'articles d'une commande existante ou à créer une nouvelle commande.

- Si vous avez utilisé le traitement par lots **Calculer planning** à partir de la page **Feuille planning** pour calculer un plan de réapprovisionnement, vous pouvez utiliser le traitement par lots **Traiter messages d’action** pour copier des propositions commande achat et ordre transfert de la feuille planning à la demande achat. Ceci est commode si des utilisateurs séparés sont responsables de la gestion des ordres fabrication et des commandes achat/ordres transfert.

- Vous pouvez utiliser l’action **Livraison directe** pour renseigner les lignes demande achat. Cette action utilise le traitement par lots **Extraire commandes vente** pour déterminer les lignes commande vente que vous souhaitez désigner pour une livraison directe.

- Vous pouvez utiliser l’action **Commande spéciale** pour renseigner les lignes demande achat. Cette action utilise le traitement par lots **Extraire commandes vente** pour déterminer les lignes commande vente que vous souhaitez désigner pour une commande spéciale.

Les lignes demande achat contiennent des informations détaillées sur les articles devant être recommandés. Vous pouvez modifier et supprimer les lignes pour ajuster le plan de réapprovisionnement et poursuivre le traitement des lignes à l'aide du traitement par lots **Traiter messages d'action**. 

Pour plus d’informations sur la planification à l’aide de magasins et de transferts, voir [Planification avec/sans magasin](production-planning-with-without-locations.md).

> [!TIP]
> Lorsque vous travaillez sur les pages **Demande achat** ou **Feuille planning**, vous pouvez organiser les lignes en triant sur un nom de colonne. Ceci est particulièrement utile sur la page Feuille planning, car ils peuvent être utilisés pour les ordres de fabrication à plusieurs niveaux. Par défaut, les lignes sont triées par le champ **Numéro d’article**. Pour regrouper les lignes d’une commande à plusieurs niveaux, triez par **N° ordre de référence** . En outre, les champs **Ordre PDP** et **Niveau de planification** peuvent aider à montrer la hiérarchie des lignes.

## Voir aussi

[Détails de conception : planification de l’approvisionnement](design-details-supply-planning.md)  
[Planifié](production-planning.md)  
[Paramétrage de la production](production-configure-production-processes.md)  
[Production](production-manage-manufacturing.md)  
[Stock](inventory-manage-inventory.md)  
[Achats](purchasing-manage-purchasing.md)  
[Pratiques de configuration recommandées : planification de l’approvisionnement](setup-best-practices-supply-planning.md)  
[Utiliser [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]
