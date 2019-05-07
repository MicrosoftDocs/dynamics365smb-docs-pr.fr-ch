---
title: 'Procédure : calculer des dates promesse livraison | Microsoft Docs'
description: La fonction de configuration des promesses livraison est un outil permettant de calculer la date la plus proche à laquelle un article est disponible pour la livraison ou l'expédition. Cette fonction crée également des lignes demande achat pour les dates que vous acceptez.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/01/2019
ms.author: sgroespe
ms.openlocfilehash: 119c3df2f58f6aeb7ee6614a56b85c42724517c8
ms.sourcegitcommit: bd78a5d990c9e83174da1409076c22df8b35eafd
ms.translationtype: HT
ms.contentlocale: fr-CH
ms.lasthandoff: 03/31/2019
ms.locfileid: "919883"
---
# <a name="calculate-order-promising-dates"></a>Calculer des dates promesse livraison
Une société doit pouvoir informer ses clients des dates de livraison de commande. La page **Lignes promesse de livraison** vous permet d'effectuer cette opération à partir d'une ligne commande vente.  

À partir des dates de disponibilité connues et attendues d'un article, [!INCLUDE[d365fin](includes/d365fin_md.md)] calcule immédiatement les dates d'expédition et de livraison, qui peuvent être communiquées au client.  

Si vous spécifiez une date de livraison demandée sur une ligne commande vente, alors cette date est utilisée comme point de départ du calcul suivant :  

- Date livraison demandée - délai d'expédition = date d'expédition planifiée  
- Date d'expédition + délai désenlogement = date d'expédition planifiée  

Si les articles peuvent être prélevés à la date d'expédition, alors le processus vente peut continuer. Si les articles ne peuvent pas être prélevés à la date d'expédition, alors une alerte rupture de stock est affichée.  

Si vous ne spécifiez aucune date livraison demandée sur une ligne de commande vente ou si la date livraison demandée ne peut pas être respectée, alors la première date à laquelle les articles sont disponibles est calculée. Cette date est ensuite renseignée dans le champ **Date d'expédition** sur la ligne, et la date à laquelle vous prévoyez d'expédier les articles, ainsi que la date à laquelle ces derniers seront livrés au client sont calculées via les calculs suivants :  

- Date d'expédition + délai désenlogement = date d'expédition planifiée  
- Date livraison planifiée - délai d'expédition = date expédition planifiée  

## <a name="about-order-promising"></a>À propos de la promesse de livraison
La fonctionnalité de configuration des promesses livraison vous permet de promettre la livraison ou l'expédition d'une commande à une date donnée. La date à laquelle un article est disponible afin de le promettre ou de pouvoir le promettre est calculée, et des lignes commande sont créées pour les dates que vous acceptez. Cette fonctionnalité calcule la date la plus proche à laquelle un article est disponible pour la livraison ou l'expédition. Elle crée également des lignes demande, dans le cas où les articles doivent d'abord être achetés, pour les dates que vous acceptez.

[!INCLUDE[d365fin](includes/d365fin_md.md)] utilise deux concepts essentiels :  

- Disponible à la vente (DAV)  
- Simulation de délai (SDD)  

### <a name="available-to-promise"></a>Disponible à la vente  
La fonction Disponible à la vente (ATP) calcule les dates sur la base du système de réservation. Elle effectue une vérification de la disponibilité des quantités non réservées en stock vis-à-vis de la production, des achats, des transferts et des retours vente planifiés. En fonction de ces informations, [!INCLUDE[d365fin](includes/d365fin_md.md)] calcule automatiquement la date de livraison de la commande du client dans la mesure où les articles sont disponibles (en stock ou avec entrée planifiée).  

### <a name="capable-to-promise"></a>Simulation de délai  
La fonction Simulation de délai (CTP) considère un scénario basé sur l'hypothèse, qui s'applique uniquement aux quantités d'articles qui ne sont pas en stock ou des commandes planifiées. En fonction de ce scénario, [!INCLUDE[d365fin](includes/d365fin_md.md)] calcule la date la plus proche à laquelle cet article sera disponible s'il doit être produit, acheté ou transféré.

#### <a name="example"></a>Exemple :
S'il y a une commande de 10 pièces, et que 6 pièces sont disponibles en stock ou dans des commandes planifiées, alors le calcul de simulation de délai est basé sur 4 pièces.

### <a name="calculations"></a>Calculs  
Lorsque [!INCLUDE[d365fin](includes/d365fin_md.md)] calcule la date de livraison du client, il effectue deux tâches :  

- Calcule la première date de livraison possible lorsque le client n'a pas demandé une date de livraison spécifique.  
- Vérifie si la date de livraison demandée par le client ou confirmée au client est réaliste.  

Si le client ne demande pas de date de livraison spécifique, la date d'expédition est configurée comme la date de travail, et la disponibilité est ensuite basée sur la date. Si l'article est en stock, [!INCLUDE[d365fin](includes/d365fin_md.md)] calcule à l'avance pour déterminer quand la commande peut être livrée. Ceci est accompli par les formules suivantes :  

- Date d'expédition + Délai traitement entrepôt sortant = Date de livraison planifiée  
- Date d'expédition planifiée + délai d'expédition = date livraison planifiée  

Ensuite, [!INCLUDE[d365fin](includes/d365fin_md.md)] vérifie si la date de livraison calculée est réaliste en calculant en amont dans le temps, pour déterminer quand l'article doit être disponible pour respecter la date confirmée. Ceci est accompli par les formules suivantes :  

- Date livraison planifiée - délai d'expédition = date expédition planifiée  
- Date d'expédition planifiée - Délai traitement entrepôt sortant = Date de livraison  

La date d'expédition est utilisée pour effectuer la vérification de disponibilité. Si l'article est disponible à cette date, [!INCLUDE[d365fin](includes/d365fin_md.md)] confirme que la livraison demandée/promise peut être respectée en configurant la date de livraison planifiée à la date de livraison demandée/confirmée. Si l'article n'est pas disponible, il renvoie une date vide et le préparateur de commandes peut alors utiliser la fonctionnalité CTP.  

Sur la base des nouvelles dates et heures, toutes les dates liées sont calculées en fonction des formules répertoriées précédemment dans cette section. Le calcul CTP prend plus de temps, mais donne une date précise à laquelle le client peut attendre la livraison de l'article. Les dates qui sont calculées à partir de la SDD sont présentées dans les champs **Date livraison planifiée** et **Date d'expédition au plus tôt** sur la page **Lignes promesse de livraison**.  

Le préparateur de commandes finit le processus CTP en acceptant les dates. Cela signifie qu'une ligne de planning et une écriture de réservation sont créées pour l'article avant les dates calculées pour assurer que la commande est satisfaite.  

En plus de la promesse de livraison externe que vous pouvez effectuer sur la page **Lignes promesse de livraison**, vous pouvez également promettre des dates de livraison internes ou externes pour les articles de nomenclature. Pour plus d'informations, voir [Voir la disponibilité des articles](inventory-how-availability-overview.md).

## <a name="to-set-up-order-promising"></a>Pour configurer une promesse livraison  
1. Choisissez l'icône ![Ampoule qui ouvre la fonction Tell Me](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire"), saisissez **Paramètres promesses livraison**, puis sélectionnez le lien associé.  
2. Entrez un numéro et un code unité de temps dans le champ **Décalage (durée)**. Sélectionnez l'une des options suivantes.  

    |Code|Désignation|  
    |----------|-----------------|  
    |**j**|Jour du calendrier|  
    |**t**|Semaine|  
    |**m**|Mois|  
    |**t**|Trimestre|  
    |**a**|Année|  

    Par exemple, « 3S » indique que le décalage est de trois semaines. Pour indiquer la période en cours, utilisez le préfixe « c » devant l'un de ces codes. Par exemple, si vous souhaitez que le décalage porte sur le mois en cours, entrez **mc**.  
3. Entrez une souche de numéros dans le champ **N° promesse de livraison** en sélectionnant une ligne dans la liste de la page **Souches de n°**.  
4. Entrez un modèle promesse de livraison dans le champ **Modèle promesse de livraison** en sélectionnant une ligne de la liste de la page **Liste des modèles demande achat**.  
5. Entrez une demande achat dans le champ **Feuille promesse de livraison** en sélectionnant une ligne de la liste de la page **Noms demandes achat**.

### <a name="to-enter-inbound-warehouse-handling-time-in-the-inventory-setup-page"></a>Pour entrer un délai d'enlogement sur la page Paramètres stocks  
Si vous le souhaitez, vous pouvez inclure un délai entrepôt par défaut pour votre stock ou pour votre magasin dans le calcul de la promesse de livraison sur la ligne achat.    
1. Choisissez l'icône ![Ampoule qui ouvre la fonction Tell Me](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire"), saisissez **Paramètres stock**, puis sélectionnez le lien associé.  
2. Sur le raccourci **Général**, dans le champ **Délai enlogement**, indiquez le nombre de jours que vous souhaitez inclure dans le calcul de la promesse de livraison.  

> [!NOTE]  
>  Si vous avez renseigné le champ **Délai enlogement** dans la **fiche magasin** pour votre magasin, ce champ est utilisé en tant que délai d'enlogement par défaut.  

### <a name="to-enter-inbound-warehouse-handling-time-on-location-cards"></a>Pour entrer des délais d'enlogement dans les fiches magasin  
1. Choisissez l'icône ![Ampoule qui ouvre la fonction Tell Me](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire"), saisissez **Magasin**, puis choisissez le lien associé.  
2.  Ouvrez la fiche magasin appropriée.  
3.  Sur le raccourci **Entrepôt**, dans le champ **Délai enlogement**, indiquez le nombre de jours que vous souhaitez inclure dans le calcul de la promesse de livraison.  

> [!NOTE]  
>  Si vous laissez le champ **Délai enlogement** vide, le calcul utilise la valeur de la page **Paramètres stock**.

### <a name="to-enter-outbound-warehouse-handling-time-in-the-inventory-setup-page"></a>Pour entrer un délai de désenlogement sur la page Paramètres stocks  
Vous pouvez configurer un délai de désenlogement par défaut pour le stock, à inclure dans le calcul des promesses de livraison dans les lignes vente.

1. Choisissez l'icône ![Ampoule qui ouvre la fonction Tell Me](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire"), saisissez **Paramètres stock**, puis sélectionnez le lien associé.  
2. Sur le raccourci **Général**, dans le champ **Délai enlogement sortant**, indiquez le nombre de jours que vous souhaitez inclure dans le calcul de la promesse de livraison.  

> [!NOTE]  
>  Si vous avez renseigné le champ **Délai enlogement sortant** dans la fiche magasin pour votre magasin, ce champ est utilisé en tant que délai d'enlogement sortant par défaut.  

### <a name="to-enter-outbound-warehouse-handling-time-on-location-cards"></a>Pour entrer un délai de désenlogement sortant dans les fiches magasin  
1.  Choisissez l'icône ![Ampoule qui ouvre la fonction Tell Me](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire"), saisissez **Magasins**, puis choisissez le lien associé.  
2.  Ouvrez la fiche magasin appropriée.  
3.  Sur le raccourci **Entrepôt**, dans le champ **Délai enlogement sortant**, indiquez le nombre de jours que vous souhaitez inclure dans le calcul de la promesse de livraison.  

> [!NOTE]  
>  Si vous laissez le champ **Délai désenlogement** vide, le calcul utilise la valeur de la page **Paramètres stock**.

## <a name="to-make-an-item-critical"></a>Pour affecter le statut critique à un article  
Avant qu'un article puisse être inclus dans le calcul de la promesse de livraison, il doit être signalé comme critique. Cette configuration garantit que les articles non critiques ne génèrent pas de calculs inutiles de promesse de livraison.   
1.  Choisissez l'icône ![Ampoule qui ouvre la fonction Tell Me](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire"), saisissez **Articles**, puis sélectionnez le lien associé.  
2.  Ouvrez la fiche article appropriée.  
3.  Sur le raccourci **Planifié**, sélectionnez le champ **Critique**.  

## <a name="to-calculate-an-order-promising-date"></a>Pour calculer une date promesse livraison  
1.  Choisissez l'icône ![Ampoule qui ouvre la fonction Tell Me](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire"), saisissez **Commande vente**, puis sélectionnez le lien associé.  
2.  Ouvrez la commande vente appropriée et sélectionnez les lignes de commande vente que vous souhaitez que le programme calcule.  
3.  Choisissez l'action **Promesse de livraison**, puis sélectionnez l'action **Lignes promesse de livraison**.  
4.  Sélectionnez une ligne, puis l'une des options suivantes :  

    - Choisissez **Disponible à la vente** si vous souhaitez calculer la date la plus proche à laquelle l'article sera disponible pour ce qui est du stock, des réceptions planifiées, et des besoins bruts.  
    - Choisissez **Simulation de délai** si vous savez que l'article est actuellement en rupture de stock et que vous souhaitez calculer la date la plus proche à laquelle cet article sera disponible grâce à l'émission de demandes de réapprovisionnement.  
5.  Cliquez sur le bouton **Accepter** pour accepter la date d'expédition disponible la plus proche.  

## <a name="see-also"></a>Voir aussi  
[Ventes](sales-manage-sales.md)  
[Calcul de la date des achats](purchasing-date-calculation-for-purchases.md)  
[Utilisation de [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)
