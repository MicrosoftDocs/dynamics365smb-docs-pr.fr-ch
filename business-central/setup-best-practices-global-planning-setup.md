---
title: Pratiques recommandées pour la configuration du planning général | Microsoft Docs
description: Le raccourci Planning de la page Paramètres production comporte plusieurs champs permettant de définir les règles globales pour la planification des approvisionnements.
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: null
ms.date: 04/01/2021
ms.author: edupont
---
# <a name="setup-best-practices-global-planning-setup"></a><a name="setup-best-practices-global-planning-setup"></a>Configurer des recommandations : configuration du planning général
Le raccourci **Planning** de la page **Paramètres production** comporte plusieurs champs permettant de définir les règles globales pour la planification des approvisionnements.  

 Le tableau suivant fournit les meilleures pratiques sur la procédure de configuration de champs paramètres sélectionnés de planification générale. Pour plus d’informations sur un champ donné, sélectionnez le lien correspondant dans la colonne **Configuration d’un champ**.  

|Paramétrage de champ|Meilleure pratique|Commentaire|  
|-----------------|-------------------|-------------|  
|Prévision sur magasin|Indiquez si vous avez des prévisions pour des entrepôts spécifiques.||  
|Mag. composant par déf.|Si les articles ne sont pas définis comme points de stock, sélectionnez le code magasin de l’entrepôt principal.|Cela s’applique également si vous utilisez uniquement la demande achat.|  
|Niveau de dépassement de capacité vide|Sélectionnez **Autoriser calcul par défaut** si vous effectuez une migration de Microsoft Dynamics NAV 5.0 ou d’une version antérieure.|Ne l’utilisez que si vous souhaitez autoriser tout ou partie de vos articles à franchir le point de réapprovisionnement.|  
|Période tampon par défaut|Doit être compris entre 1D et 5D.<br /><br /> Si vous débutez en planification avec [!INCLUDE[prod_short](includes/prod_short.md)], définissez une plus longue période.|Quand les utilisateurs sont plus au fait des différents motifs des messages d’action, raccourcissez la période tampon pour autoriser plus de propositions de modification.|  
|Quantité tampon par défaut (%)|Définissez à entre 5 et 20 % de la taille du lot de l’article.||  

## <a name="see-also"></a><a name="see-also"></a>Voir aussi
 [Pratiques de configuration recommandées : planification de l’approvisionnement](setup-best-practices-supply-planning.md)   
 [Détails de conception : planification de l’approvisionnement](design-details-supply-planning.md)   
 [Configurer des domaines d’application complexes à l’aide des meilleures pratiques](set-up-complex-application-areas-using-best-practices.md)  
 [Utiliser [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]
