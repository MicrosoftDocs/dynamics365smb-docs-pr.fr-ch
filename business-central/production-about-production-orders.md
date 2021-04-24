---
title: À propos des ordres de fabrication | Microsoft Docs
description: Les ordres de fabrication permettent de gérer la conversion de matières achetées en articles fabriqués. La gamme des ordres de fabrication (ordres de fabrication ou de projet) utilise diverses fonctions (centre de charge ou poste de charge) de l'atelier.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/01/2021
ms.author: edupont
ms.openlocfilehash: ecf65fef85d7f7f184ec8cddd8551eeaa990d92d
ms.sourcegitcommit: 766e2840fd16efb901d211d7fa64d96766ac99d9
ms.translationtype: HT
ms.contentlocale: fr-CH
ms.lasthandoff: 03/31/2021
ms.locfileid: "5779447"
---
# <a name="about-production-orders"></a>À propos des ordres de fabrication
Les ordres de fabrication permettent de gérer la conversion de matières achetées en articles fabriqués. La gamme des ordres de fabrication utilise divers centres de charge ou postes de charge de l'atelier.  

Avant de commencer la production, la plupart des sociétés effectuent une planification des approvisionnements, généralement une fois par semaine, pour calculer le nombre d'ordres de fabrication et de commandes achat à exécuter pour répondre à une demande de vente de la semaine en cours. Les commandes achat fournissent les composants requis en fonction de la nomenclature de production pour produire les produits finis.

Les ordres de fabrication sont les composants centraux de la fonctionnalité de fabrication de l'application et contiennent les informations suivantes :  

-   produits planifiés pour fabrication ;  
-   matières requises pour les ordres de fabrication planifiés ;  
-   produits qui viennent d'être fabriqués ;  
-   matières déjà sélectionnées ;  
-   produits fabriqués par le passé ;  
-   matières utilisées dans des opérations de fabrication précédentes.  

Les ordres de fabrication sont les points de départ pour :  

-   le planning de la fabrication future ;  
-   le contrôle de la fabrication en cours ;  
-   la traçabilité de la fabrication terminée.  

## <a name="production-order-creation"></a>Création des ordres de fabrication  
Il est possible de créer des ordres de fabrication un par un manuellement sur la page **Ordre de fabrication** ou de les générer sur les pages **Commande vente Planning** et/ou **Planning commande**. La page **Feuille planning** permet de générer plusieurs ordres.  

Les ordres de fabrication sont créés à l'aide d'informations provenant des éléments suivants :  

- Articles  
- Nomenclatures de production
- Gammes  
- postes de charge ;  
- centres de charge ;  

## <a name="limitations-on-production-order-creation"></a>Limitations de la création d'ordres de fabrication  
Les ordres de fabrication sont automatiquement réservés et tracés sur leur source quand ils sont :  

-   créés dans la fenêtre **Feuille planning** ;  
-   Créés avec la fonction Commande sur la page **Planification commande vente** ;  
-   Créés sur la page **Planification commande** ;  
-   utilisés avec la fonction **Replanification** des ordres de fabrication.  

Pour plus d'informations, voir [Suivre les relations entre l'offre et la demande](production-how-track-demand-supply.md).

Les ordres de fabrication créés par d'autres moyens ne sont pas automatiquement réservés et tracés.   

## <a name="production-order-status"></a>Statut de l'ordre de fabrication  
Le statut de l'ordre de fabrication contrôle la manière dont l'ordre de fabrication se comporte dans l'application. La forme et le contenu de la production sont dictés par le statut de l'ordre. Les ordres de fabrication sont affichés sur différentes pages en fonction de leur statut. Vous ne pouvez pas modifier le statut d'un ordre de fabrication manuellement ; vous devez utiliser la fonction **Modifier statut**.  

### <a name="simulated-production-order"></a>O.F. simulé  
L'ordre de fabrication simulé est unique en raison des caractéristiques suivantes :  

- Comme son nom l'indique, il s'agit d'une simulation destinée principalement à l'établissement de devis et d'évaluations, par exemple si le département de recherche et développement souhaite obtenir une estimation de coût d'un article proposé. Un ordre de fabrication simulé fait office d'exemple d'ordre de fabrication.  
- Il n'influence par le planning commande. Le planning (PDP et MRP) ne prend jamais en considération et n'est pas affecté par les ordres de fabrication simulés. De même, un ordre de fabrication simulé ne peut pas être utilisé comme modèle parce qu'il disparaît lorsque vous modifiez son statut.  

### <a name="planned-production-order"></a>O.F. planifié  
L'ordre de fabrication planifié est unique en raison des caractéristiques suivantes :  

- Vous pouvez créer automatiquement un ordre de fabrication planifié à partir d'une commande vente.  
- Les ordres de fabrication planifiés sont comme des ordres de fabrication lancés. Ils contribuent à l'établissement du planning des besoins en capacité en montrant les besoins totaux par centre de charge ou poste de charge.  
- Un ordre de fabrication constitue la meilleure estimation de la charge future du centre de charge ou du poste de charge sur la base des informations disponibles. Généralement, il est généré à partir d'un planning, mais il est également possible de le créer manuellement. Comme il est effacé durant les générations de planning suivantes, la création manuelle n'est pas pratique.  
- Sa génération dans le planning produit un « lancement prévu » suggéré qui inclut une quantité, une date de lancement et une date d'échéance. La logique du système de planning est basée sur le système de réapprovisionnement, les méthodes de réapprovisionnement et les modificateurs d'ordre qu'il rencontre dans le processus de planning des besoins nets.  
- Pour afficher leur impact, examinez la charge de chaque centre de charge ou poste de charge sur la gamme de l'ordre de fabrication planifié.  

### <a name="firm-planned-production-order"></a>O.F. planifié ferme  
L'ordre de fabrication planifié ferme est unique en raison des caractéristiques suivantes :  

- Vous pouvez créer automatiquement un ordre de fabrication planifié ferme à partir d'une commande vente.  
- Un ordre de fabrication planifié ferme agit comme un espace réservé dans le planning pour un futur projet transféré à l'atelier.  
- Vous pouvez générer un ordre de fabrication planifié ferme à partir d'un planning, de commandes vente ou manuellement. Il n'est pas effacé durant le planning ultérieur.  
- Sa génération dans le planning produit un « lancement prévu » suggéré qui inclut une quantité, une date de lancement et une date d'échéance. La logique du système de planning est basée sur le système de réapprovisionnement, les méthodes de réapprovisionnement et les modificateurs d'ordre qu'il rencontre dans le processus de planning des besoins nets.  
- Pour afficher leur impact, examinez la charge de chaque centre de charge ou poste de charge sur la gamme de l'ordre de fabrication planifié ferme.  

### <a name="released-production-order"></a>O.F. lancé  
L'ordre de fabrication lancé est unique en raison des caractéristiques suivantes :  

- Vous pouvez créer automatiquement un ordre de fabrication lancé à partir d'une commande vente.  
- Le fait qu'un ordre de fabrication ait été lancé ne signifie pas nécessairement que les matières ont été prélevées ou que le projet a été déplacé physiquement vers la première opération qui y est associée.  
- Dans un environnement MTO (fabrication à la commande), il n'est pas rare de créer un ordre de fabrication lancé immédiatement après l'entrée de l'ordre de fabrication.  
- Vous pouvez enregistrer la consommation de matières et la production réelles manuellement avec un ordre de fabrication lancé. En outre, la consommation automatique de matières et de production n'intervient que pour les ordres de fabrication lancés.  

### <a name="finished-production-order"></a>O.F. terminé  
L'ordre de fabrication terminé est unique en raison des caractéristiques suivantes :  

- Un ordre de fabrication terminé est généralement un ordre qui a été fabriqué.  
- L'achèvement de l'ordre de fabrication est une tâche importante de l'évaluation du cycle de vie de l'article en cours de production. L'achèvement d'un ordre de fabrication permet d'ajuster et de rapprocher l'évaluation.  
- Les ordres de fabrication terminés sont utilisés pour générer des états statistiques et prendre en charge la possibilité de remonter à d'autres ordres (ventes, production et achat, par exemple). La possibilité de remonter à un ordre de fabrication terminé permet d'examiner l'historique détaillé.  
- Il n'est jamais possible de modifier des ordres de fabrication terminés.  

## <a name="production-order-execution"></a>Exécution d'un ordre de fabrication  
Après qu'un ordre de fabrication a été créé et planifié, il doit être lancé à l'atelier pour exécution. Durant l'exécution de l'ordre, vous enregistrez les éléments suivants :  

- matières prélevées et consommées ;  
- temps passé à travailler sur l'ordre ;  
- quantité d'articles parents produite.  

Ces informations peuvent être enregistrées manuellement ou via une génération d'état automatique, en fonction des articles définis dans le champ Méthode consommation.  

### <a name="material-consumption"></a>Consommation matière  
L'application offre une série d'options concernant la manière dont une société manufacturière peut enregistrer une consommation matière. Par exemple, une consommation matière peut être enregistrée manuellement, ce qui peut être souhaitable en cas de remplacements fréquents de composants ou de rebuts plus importants que prévu.  

La consommation de matières peut être traitée via la feuille consommation, mais peut également être enregistrée automatiquement par l'application à l'aide du processus de génération d'état automatique. Les méthodes de génération d'état sont les suivantes :  

-   Manuel  
-   Aval  
-   Amont  

La génération manuelle d'états de consommation utilise la feuille consommation pour spécifier un prélèvement de matière.  

En aval, la génération d'états de consommation est basée sur l'hypothèse que la quantité prévue de toutes les matières nécessaires à la commande entière est consommée au lancement de l'ordre de fabrication, sauf en cas d'utilisation de codes lien gamme. En cas d'utilisation de codes lien gamme, les matières consommées après le début de l'opération sont enregistrées dans la feuille production. Pour consommer en aval l'ordre de fabrication entier, vous devez effectuer les deux opérations suivantes :  

- La consommation en aval doit être activée pour tous les articles de la nomenclature de production de niveau supérieur sur leur fiche article.  
- Tous les codes lien gamme dans la nomenclature de production doivent être supprimés.  

En amont, la génération d'états de consommation enregistre la quantité réelle des matières prélevées ou consommées lorsque le statut d'un ordre de fabrication passe à *Terminé*, sauf en cas d'utilisation de codes lien gamme. En cas d'utilisation de codes lien gamme, les matières sont consommées après qu'une quantité d'articles parents a été enregistrée pour l'opération dans la feuille production.  

Lors de l'actualisation de l'ordre de fabrication, la méthode consommation est copiée à partir de la fiche article. Comme la méthode consommation de chaque ordre de fabrication contrôle le mode et le moment d'enregistrement de la consommation, il est important de noter que vous pouvez modifier la méthode de consommation d'articles spécifiques directement dans l'ordre de fabrication.  

#### <a name="automatic-consumption-posting-flushing"></a>Validation de la consommation automatique (consommation)  
L'avantage de la consommation automatique est qu'elle réduit considérablement la saisie de données. La possibilité de consommer automatiquement une opération permet d'automatiser tout le processus d'enregistrement de la consommation et de la production. L'inconvénient de la consommation automatique est que vous risquez de ne pas enregistrer précisément voire d'omettre les rebuts. Les méthodes de génération d'état automatique sont les suivantes :  

- Consommation en aval de l'ordre entier  
- Consommation en aval par opération  
- Consommation en amont par opération  
- Consommation en amont de l'ordre entier  

#### <a name="automatic-reporting---forward-flush-the-entire-order"></a>Génération d'état automatique - Consommation en aval de l'ordre entier  
Si vous consommez en aval l'ordre de fabrication au début du projet, le comportement l'application est très similaire à une consommation manuelle. La principale différence réside dans le fait que la consommation est effectuée automatiquement.  

- Le contenu entier de la nomenclature de production est consommé et déduit du stock lors de l'actualisation de l'ordre de fabrication lancé.  
- La quantité consommée est la quantité par assemblage indiquée dans la nomenclature de production, multipliée par le nombre d'articles parents que vous créez.  
- Il est inutile d'enregistrer des informations dans la feuille consommation si tous les articles doivent être consommés.  
- Lors de la consommation d'articles du stock, le moment où ont lieu les entrées de feuille production est sans importance parce que la feuille production n'a pas d'effet sur ce mode de validation de la consommation.  
- Aucun code lien gamme ne peut être défini.  

La consommation en aval d'une commande entière est appropriée dans des environnements de production présentant les caractéristiques suivantes :  

-   petit nombre de défauts ;  
-   petit nombre d'opérations ;  
-   consommation de composants importante dans les opérations précoces.  

#### <a name="automatic-reporting---forward-flushing-by-operation"></a>Génération d'état automatique - Consommation en aval par opération  
La consommation par opération permet de déduire le stock durant une opération spécifique dans la gamme de l'article parent. Les matières sont liées à la gamme à l'aide de codes lien gamme qui correspondent aux codes lien gamme appliqués aux composants dans la nomenclature de production.  

La consommation a lieu au démarrage de l'opération auquel le code lien gamme correspond. Le démarrage intervient quand une certaine activité est enregistrée dans la feuille production pour cette opération. Cette activité peut être simplement l'entrée d'un temps de préparation.  

La quantité consommée est calculée pour la quantité par assemblage sur la nomenclature de production multipliée par le nombre d'articles parents créés (quantité prévue).  

Il est recommandé d'utiliser cette technique lorsqu'il y a de nombreuses opérations et que certains composants ne sont nécessaires que vers la fin de la séquence d'assemblage. En réalité, dans le cadre d'une configuration à flux tendu (Just-in-Time, JIT), il se peut que les articles ne soient pas disponibles au début de la RPO.  

Il est possible de consommer des matières durant les opérations à l'aide de codes lien gamme. Il se peut que certains composants ne soient pas utilisés avant les opérations d'assemblage finales, auquel cas ils ne doivent pas être soustraits du stock auparavant.  

#### <a name="automatic-reporting---back-flushing-by-operation"></a>Génération d'état automatique - Consommation en amont par opération  
La consommation en amont par opération enregistre la consommation après la validation de l'opération dans la feuille production.  

L'avantage de cette méthode est que le nombre de pièces parentes finies dans l'opération est connu.  

Les matières dans la nomenclature de production sont liées aux enregistrements de gamme à l'aide de codes lien gamme. La consommation en amont a lieu lors de la validation d'une opération avec un code lien gamme particulier avec une quantité terminée.  

La quantité consommée est calculée pour la quantité par assemblage sur la nomenclature de production multipliée par le nombre d'articles parents validés comme quantité produite pour cette opération. Cette quantité peut différer de la quantité prévue.  

#### <a name="automatic-reporting---back-flushing-the-entire-order"></a>Génération d'état automatique - Consommation en amont de l'ordre entier  
Cette méthode de génération d'état ne tient pas compte des codes lien gamme.  

Aucun composant n'est prélevé tant que le statut de l'ordre de fabrication lancé n'est pas *Terminé*. La quantité consommée est calculée pour la quantité par assemblage sur la nomenclature de production multipliée par le nombre d'articles parents terminés et introduits dans le stock.  

La consommation en amont de l'ordre de fabrication tout entier requiert la même configuration que pour la consommation en aval : la méthode de génération d'état doit être définie sur amont dans la fiche article de tous les articles de la nomenclature parente pour que l'état soit généré. En outre, tous les codes lien gamme doivent être supprimés de la nomenclature de production.  

### <a name="production-output"></a>Production  
L'application offre la possibilité de suivre le temps consacré à un ordre de fabrication, en plus de l'enregistrement de la quantité produite. Ces informations permettent de déterminer plus précisément les coûts de production. De même, les fabricants utilisant un système d'évaluation standard peuvent souhaiter enregistrer des informations réelles afin de pouvoir développer de meilleures normes.  

La production peut être traitée via la feuille production, mais aussi enregistrée automatiquement par l'application. L'application copie la méthode de consommation de la fiche de poste de charge ou de centre de charge dans la gamme de l'ordre de fabrication lors de l'actualisation. Comme pour la consommation matière, trois méthodes de génération d'état s'appliquent à la production :  

- Manuel  
- Aval  
- Amont  

La méthode manuel utilise la feuille production pour spécifier le temps consommé et la quantité produite.  

En aval, cette méthode enregistre la production prévue (et le temps), qui est automatiquement enregistrée lors du lancement d'un ordre de fabrication. Les codes lien gamme n'interviennent pas comme facteurs dans la consommation en aval de la production.  

En amont, cette méthode enregistre la production prévue (et le temps), qui est automatiquement enregistrée à la fin d'un ordre de fabrication. Les codes lien gamme n'interviennent pas comme facteurs dans la consommation en amont de la production.  

### <a name="posting-consumption-and-output"></a>Validation de la consommation et de la production  
Vous pouvez utiliser toute combinaison d'informations de consommation automatique et enregistrées manuellement tant pour la consommation que pour la production. Par exemple, vous pouvez consommer automatiquement en aval des composants, tout en utilisant la feuille consommation pour enregistrer les rebuts. De même, vous pouvez enregistrer automatiquement la production tout en utilisant la feuille production pour enregistrer les rebuts de l'article parent ou le temps supplémentaire consacré au traitement de l'ordre.  

Enfin, si vous entrez une consommation et une production manuellement, vous devez déterminer l'ordre dans lequel vous allez enregistrer ces informations. Vous pouvez commencer par enregistrer une consommation, puis utiliser une méthode de raccourci pour entrer les informations, basée sur une quantité de production prévue. Vous pouvez également commencer par entrer une production en utilisant la fonction **Éclater gamme**. Vous enregistrez ensuite une consommation sur la base de la quantité de production réelle.  

### <a name="production-journal"></a>Feuille production  
La feuille production combine les fonctions de la feuille consommation et des feuilles production dans une seule feuille, directement accessible depuis l'ordre de fabrication lancé.  

La feuille production a pour fonction de fournir une interface unique pour l'enregistrement de la consommation et de la production à partir d'un ordre de fabrication.  

La feuille production présente une vue simple et offre les possibilités suivantes :  

- enregistrement aisé de la production et de la consommation en relation avec un ordre de fabrication ;  
- mise en relation de composants et d'opérations ;  
- mise en relation de données d'opération réelles avec les estimations standard des lignes de composant et de gamme d'ordre de fabrication ;  
- validation et impression d'un aperçu des données d'opération enregistrées pour l'ordre de fabrication.  

La feuille production exécute un grand nombre des fonctions des feuilles consommation et production. Les dimensions, la traçabilité et le contenu emplacement sont gérés de la même manière sur les feuilles consommation et production.  

Toutefois, la feuille production diffère des feuilles production et consommation sur les plans suivants :  

- Elle est appelée directement depuis une ligne O.F. lancé et prédéfinie avec les données appropriées.  
- Elle permet de définir les types de composants à gérer sur la base du filtre de méthode de consommation de la feuille.  
- Les quantités et les heures déjà validées pour l'ordre s'affichent au bas de la feuille comme des écritures réelles.  
- Les champs dont les données ne sont pas pertinentes sont vides et non modifiables.  
- L'utilisateur peut configurer la manière dont les quantités de production sont prédéfinies dans la feuille &#8211 ; par exemple, que la quantité de production de la dernière opération doit être zéro.  
- Si vous fermez la feuille involontairement sans valider les modifications, un message de demande s'affiche pour vous proposer de ne pas fermer la feuille.  
- Elle affiche les opérations et composants dans une structure logique qui donne un aperçu du processus de production.  

Dans la feuille production, les quantités consommées sont validées comme écritures comptables article négatives, les quantités produites sont validées comme écritures comptables article positives et les heures sont validées comme écritures comptables capacité.  

## <a name="see-also"></a>Voir aussi
[Production](production-manage-manufacturing.md)    
[Paramétrage de la production](production-configure-production-processes.md)  
[Planifié](production-planning.md)      
[STOCKS ET EN-COURS](inventory-manage-inventory.md)  
[Achats](purchasing-manage-purchasing.md)  
[Utilisation de [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]