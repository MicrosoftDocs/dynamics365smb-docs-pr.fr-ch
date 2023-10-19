---
title: Configurer les centres de charge et les postes de charge
description: 'Les fiches Centre de charge organisent les exigences et les valeurs fixes des ressources de production, et régissent ainsi la production des centres de charge.'
author: brentholtorf
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.form: '99000754, 99000755, 99000756, 99000758, 99000760, 99000761, 99000762'
ms.date: 04/01/2021
ms.author: bholtorf
---
# <a name="set-up-work-centers-and-machine-centers"></a>Configurer les centres de charge et les postes de charge

L’application distingue trois types de capacité. Ces capacités sont ordonnées de façon hiérarchique. Chaque niveau contient les niveaux subordonnés.  

Le premier niveau correspond au groupe centres de charge. Des centres de charge sont affectés aux groupes centres de charge. Chaque centre de charge ne peut appartenir qu’à un seul groupe centres de charge.

Vous pouvez affecter plusieurs postes de charge à chaque centre de charge. Un poste de charge ne peut appartenir qu’à un seul centre de charge.  

La capacité planifiée d’un centre de charge se compose de la disponibilité des postes de charge correspondants et de la disponibilité planifiée du centre de charge. La disponibilité planifiée du groupe centres de charge correspond donc au total de toutes les disponibilités des postes de charge et des centres de charge qui le composent.  

La disponibilité est enregistrée dans les écritures calendrier.  

> [!IMPORTANT]
> Avant de configurer des centres ou postes de charge, vous devez configurer des calendriers usine. Pour plus d’informations, voir [Créer des calendriers usine](production-how-to-create-work-center-calendars.md).

## <a name="to-set-up-a-work-center"></a>Pour configurer un centre de charge

La procédure suivante décrit essentiellement comment configurer un centre de charge. La procédure de configuration d’un calendrier poste de charge est similaire, sauf pour le raccourci **Paramètres gamme**.  

1. Sélectionnez l’icône ![en forme d’ampoule qui ouvre la fonction Tell Me.](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire") entrez **Centres de charge**, puis choisissez le lien associé.  
2. Sélectionnez l’action **Nouveau**.  
3. Renseignez les champs selon vos besoins. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
4. Dans le champ **Groupe centres de charge**, sélectionnez le regroupement de ressources de niveau supérieur sous lequel le centre de charge est organisé, au besoin. Choisissez l’action **Nouveau** dans la liste déroulante.  
5. Dans le champ **Autre centre de charge**, sélectionnez le Centre de charge à utiliser si ce Centre de charge n’est pas disponible ou quand la demande dépasse sa capacité. L’autre Centre de charge est à titre informatif uniquement et n’est pas automatiquement inclus dans les processus de planification.
6. Sélectionnez le champ **Bloqué** pour empêcher le centre de charge d’être utilisé pour quelque traitement que ce soit. Cela signifie que la production ne peut pas être validée pour un article produit dans le centre de charge. Pour plus d’informations, voir [Valider la production](production-how-to-post-output-quantity.md).
7. Dans le champ **Coût unitaire direct**, entrez le coût de production d’une unité de mesure dans le centre de charge, sans intégrer les autres éléments de coût. Ce coût est souvent appelé *frais de main-d’œuvre directs*.  
8. Dans le champ **% coût indirect**, entrez les coûts opératoires généraux de l’utilisation du centre de charge sous la forme d’un pourcentage du coût unitaire direct. Ce pourcentage est ajouté au coût direct lors du calcul du coût unitaire.  
9. Dans le champ **Frais généraux**, entrez tous les coûts non opératoires, comme les frais de maintenance, du centre de charge sous la forme d’un montant absolu.  

    Le champ **Coût unitaire** affiche le résultat du calcul du coût unitaire de production d’une unité de mesure dans le centre de charge. Tous les éléments de coût sont pris en compte comme suit :  

    Coût unitaire = Coût unitaire direct + (Coût unitaire direct x % coût indirect) + Frais généraux.  

10. Dans le champ **Unité de coût**, indiquez si le calcul ci-dessus doit être basé sur le délai passé : **Heure** ou sur le nombre d’unités produites : **Unités**.  
11. Sélectionnez le champ **Coût unitaire spécifique** pour définir le coût unitaire du centre de charge sur la ligne gamme dans laquelle il est utilisé. Ceci peut s’avérer utile pour les opérations dont les coûts opératoires diffèrent radicalement de ceux normalement traités dans le centre de charge.  
12. Dans le champ **Méthode consommation**, indiquez si la validation de production du centre de charge doit être calculée et validée manuellement ou automatiquement, de l’une des manières suivantes.

    |Option|Description|
    |------|-----------|
    |**Manuel**| Le temps consacré et la quantité de production et de rebut sont validés manuellement dans la feuille production.|
    |**Aval**|La quantité de production est validée automatiquement lorsque l’ordre de fabrication est émis.|
    |**Amont**|La quantité de production est validée automatiquement lorsque l’ordre de fabrication est terminé.|

    > [!NOTE]
    > Si nécessaire, vous pouvez modifier la méthode de consommation sélectionnée ici pour des opérations précises en modifiant le paramétrage des lignes gamme

13. Dans le champ **Code unité**, entrez l’unité de temps utilisée pour le calcul de coût et la planification de capacité du centre de charge.
    Pour contrôler en permanence la consommation, vous devez d’abord définir une méthode de mesure. Les unités que vous saisissez sont des unités de base. Par exemple, la durée de traitement est mesurée en heures et en minutes.

    > [!NOTE]  
    > Si vous choisissez d’utiliser Jours, n’oubliez pas qu’1 jour = 24 heures et non 8 (heures de travail).

14. Dans le champ **Capacité**, indiquez si le centre de charge a plusieurs postes ou personnes travaillant simultanément. Si votre installation de [!INCLUDE[prod_short](includes/prod_short.md)] n’inclut pas la fonctionnalité de poste de charge, la valeur de ce champ doit être **1**.  
15. Dans le champ **Rendement**, entrez le pourcentage de la production standard prévue qui est réalisé par le centre de charge. Si vous entrez **100**, cela signifie que la production réelle du centre de charge est identique à la production standard.  
16. Activez la case à cocher **Calendrier consolidé** si vous utilisez également des postes de charge. Ainsi, les écritures calendrier sont générées à partir des calendriers de poste de charge.  
17. Dans le champ **Code calendrier usine**, sélectionnez un calendrier usine. Pour plus d’informations, voir [Créer des calendriers usine](production-how-to-create-work-center-calendars.md).  
18. Dans le champ **File d’attente**, spécifiez le délai fixe qui doit s’écouler avant que le travail attribué ne commence dans le centre de charge. 

> [!NOTE]
> Utilisez les files d’attente pour fournir un tampon entre le moment où un composant arrive sur une machine ou un centre de travail et le moment où l’opération démarre réellement. Par exemple, une pièce est livrée à un poste de charge à 10h00, mais il faut une heure pour la monter sur la machine de sorte que l’opération ne démarre pas avant 11h00. Pour tenir compte de cette heure, le temps d’attente serait d’une heure. La valeur du champ **File d’attente** sur une fiche poste de charge ou centre de charge spécifique plus la somme des valeurs des champs **Temps de préparation**, **Temps de fonctionnement**, **Temps d’attente** et **Temps de transfert** sur la ligne gamme article se combinent pour donner le délai de fabrication de l’article. Cela permet de fournir des temps de production globaux précis.  

## <a name="considerations-about-capacity"></a>Considérations sur la capacité

La capacité et l’efficacité spécifiées pour un centre de charge et de poste de charge n’affectent pas seulement la capacité disponible. Elles ont également un impact sur le temps de production global qui se compose du temps de préparation et du temps d’exécution, qui sont tous deux définis sur la ligne gamme.  

Lorsqu’une ligne gamme spécifique est affectée à un centre de charge et de poste de charge, le système calcule la capacité nécessaire et le temps nécessaire pour terminer l’opération.  

### <a name="run-time"></a>Temps d’exécution

Pour calculer le temps d’exécution, le système alloue le temps exact qui est défini dans le champ **Durée** de la ligne gamme. Ni l’efficacité ni la capacité n’ont d’impact sur le temps alloué. Par exemple, si le temps d’exécution est défini sur 2 heures, le temps alloué sera de 2 heures, quelles que soient les valeurs des champs d’efficacité et de capacité du Centre de charge.  

> [!NOTE]
> La capacité utilisée dans les calculs est définie comme la valeur minimale entre la capacité définie dans le centre de charge ou de poste de charge et la capacité simultanée définie pour la ligne gamme. Si un Centre de charge a une capacité de 100, mais que la capacité simultanée de la ligne gamme est de 2, alors *2* sera utilisé dans les calculs.

La *durée* d’une opération, au contraire, considère à la fois l’efficacité et la capacité. La durée est calculée comme *Temps d’exécution / Efficacité / Capacité*. La liste suivante montre quelques exemples de calcul de durée pour un même temps d’exécution, qui est défini comme 2 heures pour la ligne gamme :

- Une efficacité de 80 % signifie que vous aurez besoin de 2,5 heures au lieu de deux heures  
- Une efficacité de 200 % signifie que vous pouvez terminer le travail en une heure : vous pouvez creuser le trou deux fois plus vite si vous avez une pelle deux fois plus grande que la plus petite  

    Vous pouvez obtenir le même résultat si vous utilisez deux petites pelles au lieu d’une grande : utilisez *2* comme la capacité et *100 %* comme l’efficacité  

La capacité fractionnelle est délicate, et nous en discuterons plus tard. 

### <a name="setup-time"></a>Temps de préparation

La répartition du temps pour le Temps de préparation dépend de la capacité et est calculée comme *Temps de préparation * Capacité*. Par exemple, si la capacité est définie sur *2*, votre temps de préparation alloué sera doublé, car vous devez configurer deux machines pour l’opération.  

La *Durée* du temps de préparation dépend de l’efficacité et est calculée comme *Temps de préparation / Efficacité*. 

- Une efficacité de 80 % signifie que vous aurez besoin de 2,5 h au lieu de deux heures la préparation  
- Une efficacité de 200 % signifie que vous pouvez terminer la configuration en 1 h au lieu des 2 heures définies dans la ligne gamme  

La capacité fractale n’est pas quelque chose de facile à employer, et elle est utilisée dans des cas très spécifiques.

### <a name="work-center-processing-multiple-orders-simultaneously"></a>Centre de charge traitant plusieurs commandes simultanément

Prenons l’exemple d’une cabine de peinture au pistolet. Elle a la même configuration et le même temps d’exécution pour chaque lot traité. Mais chaque lot peut contenir plusieurs commandes individuelles peintes simultanément.  

Dans ce cas, le temps et le coût alloués aux commandes sont gérés par le temps de préparation et la capacité concurrente. Nous vous recommandons de ne pas utiliser le temps d’exécution dans les lignes gamme.  

Le temps de préparation alloué pour chaque ordre individuel sera dans l’ordre inverse du nombre d’ordres (quantités) qui sont exécutés simultanément. Voici quelques autres exemples de calcul du temps préparation lorsqu’il est défini sur deux heures pour la ligne gamme :

- S’il y a deux ordres, la capacité simultanée dans la ligne gamme doit être définie sur 0,5.

    En conséquence, la capacité allouée pour chacun sera d’une heure, mais la durée de chaque ordre restera de deux heures.
- S’il y a deux ordres avec une quantité de un et quatre, respectivement, la capacité concurrente pour la ligne gamme du premier ordre est de 0,2 et de 0,8 pour la seconde.  

    En conséquence, la capacité allouée pour le premier ordre sera de 24 min et pour la seconde de 96. La durée des deux ordres reste de deux heures.  

Dans les deux cas, le temps total alloué pour tous les ordres est de deux heures.


### <a name="efficient-resource-can-dedicate-only-part-of-their-work-date-to-productive-work"></a>Une ressource efficace ne peut consacrer qu’une partie de sa date de travail à un travail productif

> [!NOTE]
> Ce scénario n’est pas recommandé. Nous vous recommandons d’utiliser plutôt l’efficacité. 

L’un de vos centres de charge représente un collaborateur expérimenté qui travaille avec 100 % d’efficacité sur les tâches. Mais il ne peut consacrer que 50 % de son temps de travail à des tâches, car le reste du temps, il résout des tâches administratives. Bien que ce collaborateur soit capable d’accomplir une tâche de deux heures en deux heures exactement, vous devez en moyenne attendre encore deux heures pendant que la personne s’occupe d’autres tâches.  

Le temps d’exécution alloué est de deux heures et la durée est de quatre heures.  

N’utilisez pas le temps de préparation pour de tels scénarios, car le système n’allouera que 50 % du temps. Si le Temps de préparation est défini sur *2*, le Temps de préparation alloué est d’une heure et la durée est de deux heures.

### <a name="consolidated-calendar"></a>Calendrier consolidé

Lorsque le champ **Calendrier consolidé** est sélectionné, le Centre de charge n’a pas de capacité propre. Au lieu de cela, sa capacité est égale à la somme des capacités de tous les Postes de charge qui sont affectés au Centre de charge.  

> [!NOTE]
>  L’efficacité du Poste de charge est convertie en capacité du Centre de charge.

Par exemple, si vous avez deux Postes de charge avec une efficacité de 80 et 70, respectivement, l’entrée de calendrier consolidé aura une efficacité de 100, une capacité de 1,5 et une capacité totale de 12 heures (huit heures de décalage * capacité de 1,5). 

> [!NOTE]
>  Utilisez le champ **Calendrier consolidé** lorsque vous structurez vos gammes pour planifier les opérations de production au niveau du Poste de charge, et non au niveau du centre de charge. Lorsque vous consolidez le calendrier, la page **Charge centre de charge** et les rapports deviennent une vue d’ensemble de la charge globale dans tous les centres de charge qui sont affectés au Poste de charge.

### <a name="example---different-machine-centers-assigned-to-a-work-center"></a>Exemple - Plusieurs postes de charge sont affectés à un centre de charge

Lors de la configuration des postes et des centres de charge, il convient de planifier les capacités constituant la capacité totale.

Si différents postes de charge (tels que 210 Table d’emballage 1, 310 Cabine de peinture...) sont affectés à un centre de charge, il convient de prendre en compte les capacités de chaque poste de charge, car la panne de l’un de ces postes risque d’interrompre l’ensemble du processus. Vous pouvez saisir les groupes postes en fonction de leur capacité mais vous ne pouvez pas les inclure dans le planning. Lorsque vous désactivez le champ **Calendrier consolidé**, seule la capacité du centre de charge est affectée au planning, pas le poste de charge.

Toutefois, lorsqu’un centre de charge combine des postes de charge identiques (tels que 210 Table d’emballage 1 et 220 Table d’emballage 2), il convient de prendre en compte ce centre de charge en tant que somme des postes de charge affectés. Le centre de charge est donc répertorié avec une capacité zéro. La capacité commune est affectée au centre de charge lorsque vous activez le champ **Calendrier consolidé**.

Lorsque les capacités des centres de charge n’ajoutent en rien à la capacité totale, vous pouvez paramétrer Rendement = 0.

## <a name="to-set-up-a-capacity-constrained-machine-or-work-center"></a>Pour configurer un centre de charge ou un poste de charge à la capacité critique

Vous devez configurer les ressources de production que vous considérez comme critique et de l’accepter comme une charge limitée au lieu de la charge illimitée par défaut que d’autres ressources de production acceptent. Une capacité critique peut être un centre de charge ou un poste de charge que vous avez identifié comme étant un goulot d’étranglement et pour lequel vous souhaitez établir une charge limitée.

[!INCLUDE[prod_short](includes/prod_short.md)] ne prend pas en charge le contrôle détaillé d’atelier. Il prévoit une utilisation des ressources faisable via une planification approximative, mais il ne crée ni ne met à jour automatiquement des plannings détaillés sur la base des priorités ou des règles d’optimisation.

Sur la page **Capacités critiques**, vous pouvez effectuer un paramétrage qui évite la surcharge de ressources spécifiques et permet de s’assurer qu’aucune capacité n’est laissée non affectée si elle peut augmenter le délai d’exécution d’un ordre de fabrication. Dans le champ **Seuil (% capacité totale)**, vous pouvez ajouter un seuil aux ressources afin de réduire la répartition des opérations. Cela permet au système de planifier la charge sur le dernier jour possible en dépassant légèrement le pourcentage de charge critique si ceci peut réduire le nombre d’opérations qui sont divisées.

Lors de la planification avec des ressources avec contraintes de capacité, le système veille à ce qu’aucune ressource ne soit chargée au-dessus de sa capacité définie (charge critique). Ceci est effectué en affectant chaque opération à l’emplacement du temps disponible le plus proche. Si le créneau n’est pas assez long pour effectuer toute l’opération, l’opération est répartie en au moins deux parties placées dans les créneaux disponibles les plus proches.

1. Sélectionnez l’icône ![en forme d’ampoule qui ouvre la fonction Tell Me.](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire") saisissez **Capacités critiques**, puis choisissez le lien associé.
2. Sélectionnez l’action **Nouveau**.
3. Renseignez les champs selon vos besoins.

> [!NOTE]
> Les opérations de postes ou de centres de charge qui sont configurées comme ressources contraintes sont toujours planifiées en série. Cela signifie que même si une ressource contrainte a plusieurs capacités, ces capacités ne peuvent être planifiées que dans l’ordre, pas en parallèle, comme c’est le cas si le poste ou le centre de charge n’a pas été défini en tant que ressource contrainte. Dans une ressource contrainte, le champ Capacité du centre ou du poste de charge est supérieur à 1.

> En cas de répartition des opérations, le temps de préparation n’est affecté qu’une fois car on suppose qu’un certain ajustement manuel est effectué pour optimiser le planning.

## <a name="see-also"></a>Voir aussi

[Créer des calendriers usine](production-how-to-create-work-center-calendars.md)  
[Paramétrage de la production](production-configure-production-processes.md)  
[Production](production-manage-manufacturing.md)  
[Planifié](production-planning.md)  
[Stock](inventory-manage-inventory.md)  
[Achats](purchasing-manage-purchasing.md)  
[Utiliser [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
