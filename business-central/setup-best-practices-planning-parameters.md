---
title: "Configurer des recommandations\_: paramètres de planification"
description: Cette rubrique décrit les bonnes pratiques sur la façon de configurer les champs de paramètres de planification sélectionnés avec le raccourci Planification de la fiche article.
author: brentholtorf
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: null
ms.date: 06/23/2021
ms.author: bholtorf
---
# <a name="setup-best-practices-planning-parameters"></a>Configurer des recommandations : paramètres de planification

Le raccourci **Planning** de la fiche article est le cœur de la chaîne d’approvisionnement de la société. Définir des paramètres appropriés de planification est très important pour une gestion rentable des stocks et un service client de haute qualité.  

 Le tableau suivant fournit les meilleures pratiques sur la procédure de configuration de champs paramètres sélectionnés de planification. Pour plus d’informations sur un champ donné, sélectionnez le lien correspondant dans la colonne **Configuration d’un champ**.  

|Paramétrage de champ|Meilleure pratique|Commentaire|  
|-----------------|-------------------|-------------|  
|Méthode réapprovisionnement||Pour plus d’informations, voir [Pratiques de configuration recommandées : méthodes de réapprovisionnement](setup-best-practices-reordering-policies.md).|  
|Réserver|Sélectionnez **Jamais** lorsque l’article est planifié en utilisant un point de commande.<br /><br /> À la fabrication, sélectionnez **jamais** pour que le système de planification puisse couvrir toutes les demandes.<br /><br /> Sélectionnez **Facultatif** pour les articles que vous souhaiteriez réserver aux clients prioritaires.<br /><br /> Sélectionnez **Toujours** pour les articles uniques (type d’article non standard), comme les articles de type divers qui sont entrants pour des besoins spécifiques.|Les réservations contrecarrent généralement l’objectif de la planification, qui est d’équilibrer l’offre et la demande. Par conséquent, qui sont créées pour être planifiés ne doivent généralement pas être réservés.<br /><br /> Si l’utilisateur réserver une quantité en stock pour une demande future, la base de planification est perturbée, et le point de réapprovisionnement ne peut pas être utilisé correctement. Même si le niveau de stock prévisionnel est acceptable par rapport au point de réapprovisionnement, les quantités peuvent ne pas être disponibles en raison de la réservation.|  
|Période tampon|Définir par rapport à la flexibilité du fournisseur.<br /><br /> Une période plus courte vous permet de réduire le fonds de roulement en évitant un stock excessif, mais entraînera également plus d’actions de rééchelonnement.|Si le fournisseur accepte les modifications de dernière minute des commandes, utilisez une période plus courte, mais prévoyez plus d’actions de replanification. Si le fournisseur a besoin de planification ferme, étendez la période autant que possible.<br /><br /> Pour plus d’informations sur le champ **Période tampon**, voir [Détails de conception : paramètres de planification](design-details-planning-parameters.md).|  
|Inclure stock|Sélectionnez toujours lorsque vous utilisez la méthode du lot pour lot.|Ne sélectionnez pas uniquement dans les situations spéciales, par exemple si les articles de stock ne sont pas vendables.|  
|Délai de sécurité|Doit être compris entre 1D et 6D.<br /><br /> Définir un délai de sécurité d’au moins un jour pour vous assurer que les approvisionnements sont disponibles un jour avant qu’ils ne soient nécessaires.<br /><br /> Si vous utilisez un nouveau fournisseur, définissez une plus longue période jusqu’à ce que leur performances de livraison soit connue.<br /><br /> À la fabrication, définissez des délais longs de sécurité pour les composants vitaux.|La livraison prévue par le système pour éviter une rupture de stocks arrivera le jour même où la rupture de stocks intervient. Ceci peut être plusieurs heures trop tard, si, par exemple, la demande est nécessaire le matin et l’approvisionnement arrive dans l’après-midi. **Note :** le champ **Délai de sécurité** utilise le calendrier principal. Par conséquent, 14D ne sont pas nécessairement deux semaines.|  
|Stock de sécurité|Utilisez pour les articles connaissant de grandes fluctuations de demande.<br /><br /> À la fabrication, à utiliser pour des composants critiques.<br /><br /> utiliser pour des articles soumis à des accords de service.|Si le champ **Point de commande** n’est pas renseigné, le stock de sécurité comporte également un point de réapprovisionnent.|  
|Période de groupement de lots|Si vous souhaitez uniquement quelques grandes commandes et acceptez des stock importants, définissez une longue période de groupement de lots.<br /><br /> Si vous souhaitez plusieurs petites commandes et un stock minimal, définir une période de groupement de lots courte.|La période de groupement de lots est généralement la plus longue période pendant laquelle vous conserverez le stock.|  
|Point de commande|Baser le point de réapprovisionnement sur le profil de la demande.|Si les données historique indiquent que la demande moyenne de l’article est 100 unités lors d’un délai de sept jours, le point de réapprovisionnement peut être fixé à au moins 100.<br /><br /> Cela signifie que lorsque le niveau de stock passe en dessous de 100 unités, le système de planification suggère de réapprovisionner car cela prend sept jours pour livrer l’article et qu’il doit y en avoir assez pour répondre à la demande dans les sept jours.|  
|Intervalle de planification|Laissez le champ vide, ce qui signifie que le niveau de stock est contrôlé chaque jour.|Contrôler le niveau de stock chaque jour assure la planification optimale du point de réapprovisionnement. **Note :** une fréquence de vérification de 1 semaine signifie que le niveau de stock peut être inférieur au point de commande pendant une semaine avant qu’une commande d’approvisionnement ne soit suggérée.|  
|Précision arrondi|En cas de fabrication coûteuse, définissez-le sur 0,00001.|De grandes quantités arrondies de rebut ou de consommation matière risquent de faire grimper les coûts ajustés. Il peut donc s’avérer utile de définir la plus petite précision d’arrondi pour réduire autant que possible ce coût éventuel.|  

> [!NOTE]  
> Les recommandations sur les paramètres de planification sur les fiches article s’appliquent également aux mêmes champs sur les fiches point de stock.  
>
> Si des sociétés planifient une demande dans différents magasins, il est alors vivement recommandé de définir des points de stock pour chaque magasin et de créer la demande totale à l’aide d’une valeur dans le champ **Code magasin**. Learn more at [Détails de conception : Planification avec/sans magasin](production-planning-with-without-locations.md).  

## <a name="see-also"></a>Voir aussi
[Pratiques de configuration recommandées : planification de l’approvisionnement](setup-best-practices-supply-planning.md)  
[Détails de conception : planification de l’approvisionnement](design-details-supply-planning.md)  
[Configurer des domaines d’application complexes à l’aide des meilleures pratiques](set-up-complex-application-areas-using-best-practices.md)  
[Détails de conception : Planification avec/sans magasin](production-planning-with-without-locations.md)  
[Utiliser [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]
