---
author: brentholtorf
ms.topic: include
ms.date: 09/11/2023
ms.author: bholtorf
ms.service: dynamics-365-business-central
---

Augmentez l’efficacité dans votre entrepôt avec des informations précises et en temps réel sur les facteurs qui peuvent affecter les quantités disponibles. Par exemple : 

* Niveaux d’inventaire
* Emplacements
* Phases de traitement
* Articles en quarantaine
* Réservations

Vous pouvez accéder aux informations sur la disponibilité des articles à partir des documents origine suivants :

* Commandes vente
* Ordres de fabrication
* Ordres d’assemblage
* Projets

Les informations respectent également d’autres facteurs qui affectent la disponibilité. Par exemple, les emplacements réservés, les emplacements verrouillés et les articles qui ne sont pas disponibles pour le prélèvement. Par exemple, les articles peuvent être réservés ou en attente des opérations de rangement ou d’expédition. La page **Résumé prélèvements** vous permet d’examiner les articles que [!INCLUDE [prod_short](prod_short.md)] n’a pas inclus dans les documents de prélèvement, et de prendre les mesures nécessaires.

> [!NOTE]
> Cette fonctionnalité nécessite que vous activiez le bouton bascule **Prélèvement et rangement suggérés** pour les emplacements que vous utilisez dans votre processus de prélèvement.

### Configurer les versions préliminaires

Pour obtenir des détails sur ce qui est en cours de prélèvement et ce qui ne l’est pas, activez le bouton bascule **Afficher le résumé (prélèvement et rangement suggérés)** sur les pages de demande **Entrepôt - Origine - Créer document** ou **Entrepôt - Expédition - Créer prélèvement**.

### Déterminer la quantité que vous pouvez prélever

Sur les lignes de la page **Créer résumé prélèvements entrepôt**, le champ **Qté à traiter (base)** indique quels et combien d’articles [!INCLUDE [prod_short](prod_short.md)] a essayé de prélever. Le récapitulatif **Résumé** fournit plus de détails.

Pour des investigations simples, le champ **Qté disponible pour prélèvement** peut vous fournir suffisamment d’informations. Le champ indique le nombre d’articles disponibles. Si la quantité disponible pour prélèvement est inférieure à celle prévue, explorez le contenu de l’emplacement.

Le champ **Qte disponible pour prélèvement** est la quantité maximale que [!INCLUDE [prod_short](prod_short.md)] peut prendre en compte pour le prélèvement. Cette quantité est constituée d’articles dans des emplacements de prélèvement. Elle exclut les quantités qui se trouvent dans des emplacements bloqués ou réservés, ou les articles en cours de prélèvement dans les documents de prélèvement entrepôt. Si l’article que vous souhaitez prélever nécessite une traçabilité, les numéros de lot ou de série bloqués stockés dans les emplacements de prélèvement sont exclus de la quantité disponible pour prélèvement.

Si la quantité disponible pour prélèvement diffère de la quantité dans les emplacements de prélèvement, il peut y avoir un problème. Explorez le contenu des emplacements pour trouver les emplacements ou les quantités bloqués dans les documents actifs.

Le champ **Quantité dans l’entrepôt** indique la quantité totale disponible dans votre entrepôt si vous effectuez un inventaire physique. Vous pouvez accéder aux écritures comptables de l’entrepôt à partir de ce champ. Si le champ affiche une quantité inférieure à la quantité dans le champ **Quantité dans les emplacements de prélèvement**, il existe un décalage entre les quantités de l’entrepôt et de l’inventaire. Dans ce cas, utilisez l’action **Calculer ajustement entrepôt** sur la page **Feuille article**, puis créez à nouveau le prélèvement entrepôt.

L’image suivante illustre la quantité maximale prise en compte pour le prélèvement.

:::image type="content" source="../media/pickable-qty.png" alt-text="Quantité maximale prise en compte pour le prélèvement.":::

**Légende**

|Lettre  |Description  |
|---------|---------|
|P     |Emplacements avec du contenu de type Prélèvement         |
|J     |Emplacements avec du contenu de type Prélèvement marqués comme emplacements réservés        |
|A     |Emplacements avec du contenu de type Prélèvement dans les documents actifs (comme un autre prélèvement)       |
|T     |Emplacements avec du contenu de type Prélèvement avec des articles dont le suivi est bloqué         |
|B     |Emplacements avec du contenu de type Prélèvement avec mouvement sortant bloqué         |
|O     |Autres emplacements         |

### Réservations

S’il existe des réservations pour l’article en cours de prélèvement, le calcul continue. L’idée est que la demande réservée a une priorité plus élevée que la demande non réservée, ce qui signifie que le prélèvement pour la demande non réservée ne devrait pas empêcher le prélèvement ultérieure pour la demande réservée.

Pour vérifier que votre quantité peut couvrir une demande, comparez la valeur **Qté disponible pour prélèvement** dans le récapitulatif **Résumé** à la valeur du champ **Qté à traiter (base)** sur les lignes.

Vous pouvez trouver des réservations dans la section **Qté totale réservée en entrepôt**. Les quantités réservées qui sont déjà prélevées et prêtes pour l’expédition, l’utilisation ou la consommation n’affectent pas la disponibilité. Le champ **Qté réservée dans emplacements de prélèvement/d’expédition** affiche cette quantité.

Le champ **Qté dispo. à l’exclusion de l’emplacement expédition** affiche la quantité disponible, à l’exclusion des quantités pour lesquelles les conditions suivantes sont vraies :

* Elles sont déjà prélevées pour les expéditions.
* Elles se trouvent dans des numéros de lot ou de série d’articles bloqués.
* Elles se trouvent dans des emplacements bloqués.

Ces quantités peuvent être disponibles, mais vous ne pourrez peut-être pas encore les prélever. Elles peuvent encore se trouver dans les zones de réception, de stockage ou d’assurance qualité. Vous pouvez les déplacer vers la zone de prélèvement en traitant une feuille de calcul rangement ou mouvement.

La différence entre la **Qté dispo. à l’exclusion de l’emplacement expédition** et la quantité réservée dans l’entrepôt est la quantité disponible pour prélèvement sans impacter le stock réservé.

### Autres détails

Si les articles nécessitent une traçabilité, vous pouvez également trouver la quantité dans des numéros de lot ou de série bloqués, ce qui entraîne les réductions suivantes :

* Quantité disponible pour prélèvement
* Quantité disponible à l’exclusion de l’emplacement d’expédition
* Quantité totale réservée en entrepôt 

Si vous prélevez le même article pour plusieurs documents ou lignes d’origine, ce qui est également le cas lorsque vous prélevez des numéros de série, les informations sur les prélèvements pour d’autres lignes s’affichent également car elles réduisent la quantité disponible pour prélèvement.
