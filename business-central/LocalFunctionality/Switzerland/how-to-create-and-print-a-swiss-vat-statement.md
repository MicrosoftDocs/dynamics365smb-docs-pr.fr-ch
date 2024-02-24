---
title: 'Créer et imprimer une déclaration de TVA suisse [CH]'
description: Cet article explique la procédure de création et d'impression d'une déclaration de TVA suisse basée sur les informations spécifiées sur la page Paramètres comptabilisation TVA.
author: brentholtorf
ms.topic: conceptual
ms.devlang: al
ms.search.keywords: null
ms.search.form: '11023, 11024'
ms.date: 02/08/2024
ms.author: bholtorf
ms.service: dynamics-365-business-central
---
# <a name="create-and-print-a-swiss-vat-statement-in-the-swiss-version"></a>Créer et imprimer une déclaration de TVA suisse dans la version suisse
Selon les informations spécifiées dans la page **Paramètres compta. TVA**, [!INCLUDE[prod_short](../../includes/prod_short.md)] peut créer automatiquement une nouvelle configuration de relevé de TVA pour le report TVA réalisé. Avant de continuer avec les procédures de cet article, assurez-vous que vous avez configuré les paramètres comptabilisation TVA ayant des valeurs spécifiées pour les champs de chiffre d'affaires ventes et achats.  

>[!NOTE]
> À partir de janvier 2024, la déclaration de TVA de la société Cronus a été actualisée pour inclure les nouveaux chiffres 303 et 383.  

## <a name="to-set-up-a-swiss-vat-statement-template"></a>Pour configurer un modèle de déclaration de TVA suisse

1.  Choisissez l'icône d'![Ampoule qui ouvre la fonction Tell Me.](../../media/ui-search/search_small.png "Dites-moi ce que vous voulez faire") , entrez **Mettre à jour modèle déclaration TVA**, puis sélectionnez le lien associé.  
2.  Sélectionnez un modèle dans le champ **Nom modèle déclaration de TVA**.
3.  Cliquez sur le bouton **OK**. Cliquez sur **Oui** pour confirmer que vous souhaitez créer un modèle.  
4.  Vérifiez la déclaration TVA qui en résulte et ajustez-la autant que nécessaire.  

     La page de déclaration TVA indique le champ **Chiffre de déclaration TVA**, qui indique dans quelle zone de la déclaration le résultat sera imprimé. Ce champ est automatiquement renseigné par le traitement par lots selon les informations de la page **Paramètres compta. TVA**. Le champ peut être modifié, si nécessaire.  

## <a name="to-print-the-swiss-vat-statement"></a>Pour imprimer la déclaration TVA suisse

1.  Choisissez l'icône d'![Ampoule qui ouvre la fonction Tell Me.](../../media/ui-search/search_small.png "Dites-moi ce que vous voulez faire") , entrez **Déclaration de TVA suisse**, puis sélectionnez le lien associé.  
2.  Sous le raccourci **Options**, renseignez les champs comme indiqué dans le tableau ci-dessous.  

    |Champ|Description|  
    |---------------------------------|---------------------------------------|  
    |**Type date période**|Spécifie le type de date utilisé pour la période à partir de laquelle les écritures TVA sont traitées par le traitement par lots.|
    |**Date début**|Saisissez la date à laquelle vous souhaitez que l'intervalle de temps des lignes déclaration de TVA figurant sur l'état commence.|  
    |**Date fin**|Saisissez la date à laquelle vous souhaitez que l'intervalle de temps des lignes déclaration de TVA figurant sur l'état se termine.|  
    |**Clôture avec n° de déclaration de TVA**|Sélectionnez le registre de TVA qui contient la source de comptabilisation des écritures d'ajustement de la TVA. Cette option évalue les périodes comptables qui ont déjà établies. Lorsque vous choisissez cette option, vous ne spécifiez pas les options dans les champs **Inclure écritures TVA** suivants.|  
    |**Inclure écritures TVA**|Sélectionnez l'une des options disponibles.|  
    |**Inclure écritures TVA**|Sélectionnez l'une des options disponibles.|  
    |**% taux normal**|Entrez le taux de TVA standard s'appliquant à la période.|  
    |**% taux réduit**|Saisissez la taxe de TVA réduite pour certains biens et services.|  
    |**% taux hôtel**|Entrez le taux de TVA pour l'hébergement s'appliquant à la période.|  
    |**% normal (autre taux)**|Saisissez un taux TVA secondaire pour des transactions standard s'appliquant à certaines transactions au cours de la période.|  
    |**% réduit (autre taux)**|Saisissez un taux TVA secondaire pour d'autres transactions s'appliquant à certaines transactions au cours de la période.|  
    |**% Hôtel (Autre taux)**|Saisissez un taux TVA secondaire pour l'hébergement s'appliquant à certaines transactions au cours de la période.|  
    |**Afficher montants en devise report**|Choisissez d'afficher les montants dans une devise de report supplémentaire.|  

## <a name="see-also"></a>Voir aussi
 [Taxe sur la valeur ajoutée suisse](swiss-value-added-tax.md)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
