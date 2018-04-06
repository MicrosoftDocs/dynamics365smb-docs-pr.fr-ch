---
title: "Configurer des recommandations - Paramètres de planification | Microsoft Docs"
description: "Le raccourci **Planning** de la fiche article est le cœur de la chaîne d'approvisionnement de la société. Définir des paramètres appropriés de planification est très important pour une gestion rentable des stocks et un service client de haute qualité."
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 09/08/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 2c13559bb3dc44cdb61697f5135c5b931e34d2a8
ms.openlocfilehash: a9dfb17b0cbddb3d6b65e8d807dd92990c2ccdc1
ms.contentlocale: fr-ch
ms.lasthandoff: 03/22/2018

---
# <a name="setup-best-practices-planning-parameters"></a>Configurer des recommandations : paramètres de planification
Le raccourci **Planning** de la fiche article est le cœur de la chaîne d'approvisionnement de la société. Définir des paramètres appropriés de planification est très important pour une gestion rentable des stocks et un service client de haute qualité.  

 Le tableau suivant fournit les meilleures pratiques sur la procédure de configuration de champs paramètres sélectionnés de planification. Pour plus d'informations sur un champ donné, sélectionnez le lien correspondant dans la colonne **Configuration d'un champ**.  

|Paramétrage de champ|Meilleure pratique|Commentaire|  
|-----------------|-------------------|-------------|  
|Méthode réapprovisionnement||Pour plus d'informations, voir [Pratiques de configuration recommandées : méthodes de réapprovisionnement](setup-best-practices-reordering-policies.md).|  
|Réserver|Sélectionnez **Jamais** lorsque l'article est planifié en utilisant un point de commande.<br /><br /> À la fabrication, sélectionnez **jamais** pour que le système de planification puisse couvrir toutes les demandes.<br /><br /> Sélectionnez **Facultatif** pour les articles que vous souhaiteriez réserver aux clients prioritaires.<br /><br /> Sélectionnez **toujours** pour les articles non uniques, comme les articles de type divers qui sont entrants pour des besoins spécifiques.|Les réservations contrecarrent généralement l'objectif de la planification, qui est d'équilibrer l'offre et la demande. Par conséquent, qui sont créées pour être planifiés ne doivent généralement pas être réservés.<br /><br /> Si l'utilisateur réserver une quantité en stock pour une demande future, la base de planification est perturbée, et le point de réapprovisionnement ne peut pas être utilisé correctement. Même si le niveau de stock prévisionnel est acceptable par rapport au point de réapprovisionnement, les quantités peuvent ne pas être disponibles en raison de la réservation.|  
|Période tampon|Définir par rapport à la flexibilité du fournisseur.|Si le fournisseur accepte les modifications de dernière minute des commandes, alors utilisez une plus longue période. Si le fournisseur a besoin de planification ferme, raccourcissez votre période autant que possible.<br /><br /> Pour plus d'informations sur la configuration générale, voir [Détails de conception : paramètres de planification](design-details-planning-parameters.md).|  
|Quantité tampon||Pour plus d'informations sur la configuration générale, voir [Détails de conception : paramètres de planification](design-details-planning-parameters.md).|  
|Inclure stock|Sélectionnez toujours lorsque vous utilisez la méthode du lot pour lot.|Ne sélectionnez pas uniquement dans les situations spéciales, par exemple si les articles de stock ne sont pas vendables.|  
|Délai de sécurité|Doit être compris entre 1D et 6D.<br /><br /> Définir un délai de sécurité d'au moins un jour pour vous assurer que les approvisionnements sont disponibles un jour avant qu'ils ne soient nécessaires.<br /><br /> Si vous utilisez un nouveau fournisseur, définissez une plus longue période jusqu'à ce que leur performances de livraison soit connue.<br /><br /> À la fabrication, définissez des délais longs de sécurité pour les composants vitaux.|La livraison prévue par le système pour éviter une rupture de stocks arrivera le jour même où la rupture de stocks intervient. Ceci peut être plusieurs heures trop tard, si, par exemple, la demande est nécessaire le matin et l'approvisionnement arrive dans l'après-midi. **Note :** le champ **Délai de sécurité** utilise le calendrier principal. Par conséquent, 14D ne sont pas nécessairement deux semaines.|  
|Stock de sécurité|Utilisez pour les articles connaissant de grandes fluctuations de demande.<br /><br /> À la fabrication, à utiliser pour des composants critiques.<br /><br /> utiliser pour des articles soumis à des accords de service.|Si le champ **Point de commande** n'est pas renseigné, le stock de sécurité comporte également un point de réapprovisionnent.|  
|Période de groupement de lots|Si vous souhaitez uniquement quelques grandes commandes et acceptez des stock importants, définissez une longue période de groupement de lots.<br /><br /> Si vous souhaitez plusieurs petites commandes et un stock minimal, définir une période de groupement de lots courte.|La période de groupement de lots est généralement la plus longue période pendant laquelle vous conserverez le stock.|  
|Point de commande|Baser le point de réapprovisionnement sur le profil de la demande.|Si les données historique indiquent que la demande moyenne de l'article est 100 unités lors d'un délai de sept jours, le point de réapprovisionnement peut être fixé à au moins 100.<br /><br /> Cela signifie que lorsque le niveau de stock passe en dessous de 100 unités, le système de planification suggère de réapprovisionner car cela prend sept jours pour livrer l'article et qu'il doit y en avoir assez pour répondre à la demande dans les sept jours.|  
|Intervalle de planification|Laissez le champ vide, ce qui signifie que le niveau de stock est contrôlé chaque jour.|Contrôler le niveau de stock chaque jour assure la planification optimale du point de réapprovisionnement. **Note :** une fréquence de vérification de 1 semaine signifie que le niveau de stock peut être inférieur au point de commande pendant une semaine avant qu'une commande d'approvisionnement ne soit suggérée.|  
|Précision arrondi|En cas de fabrication coûteuse, définissez-le sur 0,00001.|De grandes quantités arrondies de rebut ou de consommation matière risquent de faire grimper les coûts ajustés. Il peut donc s'avérer utile de définir la plus petite précision d'arrondi pour réduire autant que possible ce coût éventuel.|  

> [!NOTE]  
>  Les recommandations sur les paramètres de planification sur les fiches article s'appliquent également aux mêmes champs sur les fiches point de stock.  
>   
>  Si des sociétés planifient une demande dans différents magasins, il est alors vivement recommandé de définir des points de stock pour chaque magasin et de créer la demande totale à l'aide d'une valeur dans le champ **Code magasin**. Pour plus d'informations, voir [Détails de conception : demande à un magasin vide.](design-details-demand-at-blank-location.md).  

## <a name="see-also"></a>Voir aussi  
 [Pratiques de configuration recommandées : planification de l'approvisionnement](setup-best-practices-supply-planning.md)   
 [Détails de conception : planification de l'approvisionnement](design-details-supply-planning.md)   
 [Configurer des domaines d'application complexes à l'aide des meilleures pratiques](set-up-complex-application-areas-using-best-practices.md)  
 [Utilisation de [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

