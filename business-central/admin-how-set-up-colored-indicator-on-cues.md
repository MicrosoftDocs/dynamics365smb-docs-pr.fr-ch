---
title: Configurer vos indicateurs colorés personnalisés pour l’activité de piles
description: 'En tant qu’administrateur, vous pouvez définir des piles apparaissant sur les Tableaux de bord des utilisateurs comprenant un indicateur qui modifie la couleur en fonction des valeurs de données dans les piles.'
author: jswymer
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.form: '9701, 9702'
ms.date: 04/01/2021
ms.author: jswymer
---
# <a name="set-up-a-colored-indicator-on-cues-for-the-company-or-individual-users"></a>Configurer un indicateur coloré sur les piles pour la société ou les utilisateurs individuelles

En tant qu’administrateur, vous pouvez définir des piles apparaissant sur les Tableaux de bord des utilisateurs comprenant un indicateur qui modifie la couleur en fonction des valeurs de données dans les piles.  

L’indicateur apparait sous forme d’une barre de couleur le long de la bordure supérieure de la mosaïque Pile. Il offre un signal visuel du statut de l’activité de la pile, ce qui peut indiquer des conditions favorables ou défavorables pour inviter l’utilisateur à prendre des mesures. Par exemple, si une pile affiche les factures vente en cours, vous pouvez définir l’indicateur pour qu’il apparaisse vert (favorable) lorsque le nombre total des factures vente en cours est inférieur à 10, et apparaisse rouge (défavorable) lorsque le total est supérieur à 20.  

Sur la page **Paramètres pile**, vous configurez des indicateurs pour toutes les piles disponibles dans la base de données de la société. Vous pouvez configurer les indicateurs à appliquer à tous les utilisateurs de la société ou à un utilisateur individuel uniquement. Les paramètres d’indicateur sur la page **Paramètres pile** agissent en tant que paramètres d’indicateur par défaut. Si la page **Utilisateur final paramètres pile** est rendue disponible aux utilisateurs, alors ils peuvent personnaliser les paramètres d’indicateurs que vous définissez sur la page **Paramètres pile**.  

Pour configurer l’indicateur, vous pouvez spécifier jusqu’à deux valeurs de seuil qui définissent trois plages de valeurs de données (basse, moyenne et haute) à laquelle vous pouvez appliquer une couleur différente (ou un style différent).  

### <a name="to-set-up-colored-indicators-on-cues"></a>Pour paramétrer des indicateurs colorés sur des piles
1. Sélectionnez l’icône ![Ampoule qui ouvre la fonction Tell Me.](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire") saisissez **Paramètres pile**, puis choisissez le lien associé.  

     La page **Paramètres pile** s’affiche. La page liste les indicateurs actuellement paramétrés sur des piles. Les indicateurs qui s’appliquent à tous les utilisateurs de la société ont le champ **Nom d’utilisateur** vide. Les indicateurs s’appliquant à un utilisateur spécifique incluent le nom d’utilisateur dans le champ **Nom d’utilisateur**.  

    > [!NOTE]  
    >  Si vous avez configuré un indicateur à l’échelle de la société et si un utilisateur modifie l’indicateur ultérieurement, une écriture distincte pour l’indicateur s’affiche dans la liste pour cet utilisateur.  

2. Choisissez l’action **Modifier la liste**.  
3. Pour configurer un indicateur pour une pile qui ne figure pas sur la page, choisissez l’action **Nouveau**, puis renseignez les champs tel que décrit ci-après. Si vous souhaitez modifier un indicateur existant, passez à l’étape suivante.  

    |  Champ  |  Désignation  |    
    |---------|---------------|  
    |**Nom d’utilisateur**|Si vous souhaitez configurer l’indicateur pour tous les utilisateurs, laissez ce champ vide.<br /><br /> Si vous souhaitez configurer l’indicateur pour un utilisateur spécifique, définissez ce champ sur le nom d’utilisateur.|  
    |**Numéro table**|Spécifie l’ID de l’objet de table qui contient la pile. Utilisez la liste déroulante pour trouver la table. La liste déroulante inclut toutes les tables de pile dans la base de données de la société.<br /><br /> Le champ **Nom table** est automatiquement renseigné en fonction de vos choix.|  
    |**N° champ**|Spécifie l’identifiant de la pile sur laquelle vous souhaitez configurer un indicateur. Utilisez la liste déroulante pour trouver la pile que vous voulez. **Remarque** : l’ID pile correspond au numéro du champ qui est affecté à la pile dans la table. <br /><br /> Le champ **Nom de champ** est automatiquement renseigné en fonction de vos choix|  

4. Pour configurer l’indicateur pour une pile, définissez les champs tel que décrit dans le tableau suivant.  

    |  Champ  |  Désignation  |    
    |---------|---------------|  
    |**LowStyle**|Spécifie la couleur de l’indicateur lorsque la valeur de la pile est inférieure à la valeur du champ **Seuil 1**.|  
    |**LowThreshold**|Spécifie la valeur supérieure ou égale à laquelle l’indicateur change de couleur en fonction de celle spécifiée par le champ **Style milieu de gamme**.|  
    |**MiddleStyle**|Spécifie la couleur de l’indicateur lorsque la valeur de la pile est supérieure ou égale à la valeur du champ **Seuil 1** mais inférieure ou égale à la valeur du champ **Seuil 2**.|  
    |**HighThreshold**|Spécifie la valeur supérieure à partir de laquelle l’indicateur change de couleur en fonction de celle spécifiée par le champ **Style haut de gamme**.|  
    |**HighStyle**|Spécifie la couleur à utiliser lorsque la valeur de la pile est supérieure à la valeur du champ **Seuil 2**.|  

     Le tableau suivant répertorie les couleurs correspondant aux options des champs **LowStyle**, **MiddleStyle** et **HighStyle**.  

    |  Option  |  Couleur  |  
    |----------|---------|  
    |**Aucune**|Aucune couleur (même couleur que la mosaïque Pile)|  
    |**Favorable**|Vert|  
    |**Défavorable**|Rouge|  
    |**Ambigu**|Jaune|  
    |**Subordonné**|Gris|  

## <a name="see-also"></a>Voir aussi


[!INCLUDE[footer-include](includes/footer-banner.md)]
