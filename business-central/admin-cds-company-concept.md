---
title: Mappage des sociétés et des centres de profit | Microsoft Docs
description: 'Les sociétés sont des entités à la fois juridiques et commerciales, qui permettent de sécuriser et visualiser les données métier.'
author: brentholtorf
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 'CDS, Dataverse, integration, sync'
ms.date: 04/01/2021
ms.author: bholtorf
---

# <a name="data-ownership-models"></a>Modèles de propriété de données


[!INCLUDE[prod_short](includes/cds_long_md.md)] nécessite que vous indiquiez un propriétaire pour les données que vous stockez. Pour en savoir plus, consultez [Types de tables](/powerapps/maker/data-platform/types-of-entities) dans la documentation Power Apps. Lorsque vous configurez l’intégration entre [!INCLUDE[prod_short](includes/cds_long_md.md)] et [!INCLUDE[prod_short](includes/prod_short.md)], vous devez choisir la propriété **Utilisateur ou équipe** pour les enregistrements synchronisés. Les actions pouvant être effectuées sur ces enregistrements peuvent être contrôlées au niveau de l’utilisateur. <!--We recommend the Team ownership model because it makes it easier to manage ownership for multiple people.NO LONGER TRUE IN DATAVERSE-->

## <a name="team-ownership"></a>Propriété Équipe
Dans [!INCLUDE[prod_short](includes/prod_short.md)], une société est une table juridique et commerciale qui permet de sécuriser et visualiser les données métier. Les utilisateurs travaillent toujours dans le cadre d’une société. L’élément de [!INCLUDE[prod_short](includes/cds_long_md.md)] le plus proche de ce concept est la table Centre de profit, qui n’a aucune implication juridique ou commerciale.

Comme les centres de profit n’ont aucune implication juridique ou commerciale, vous ne pouvez pas forcer un mappage un à un (1:1) pour synchroniser les données entre une société et un centre de profit, que la synchronisation soit unidirectionnelle ou bidirectionnelle. Pour rendre la synchronisation possible, lorsque vous activez la synchronisation pour une société dans [!INCLUDE[prod_short](includes/prod_short.md)], ce qui suit se produit dans [!INCLUDE[prod_short](includes/cds_long_md.md)] :

* Nous créons une table Société équivalente à la table Société dans [!INCLUDE[prod_short](includes/prod_short.md)]. Le nom de la société est suivi de « ID société BC ». Par exemple, Cronus International Ltd. (93555b1a-af3e-ea11-bb35-000d3a492db1).
* Nous créons un centre de profit par défaut qui porte le même nom que la société. Par exemple, Cronus International Ltd. (93555b1a-af3e-ea11-bb35-000d3a492db1).
* Nous créons une équipe propriétaire distincte portant le même nom que la société et l’associons au centre de profit. Le nom de l’équipe est précédé de « BCI - ». Par exemple, BCI - Cronus International Ltd. (93555b1a-af3e-ea11-bb35-000d3a492db1).
* Les enregistrements créés et synchronisés avec [!INCLUDE[prod_short](includes/cds_long_md.md)] sont affectés à l’équipe « Propriétaire BCI » associée au centre de profit.

> [!NOTE]
> Si vous renommez une entreprise en [!INCLUDE[prod_short](includes/prod_short.md)], les noms de l’entreprise, de l’activité commerciale et de l’équipe que nous créons automatiquement dans [!INCLUDE[prod_short](includes/cds_long_md.md)] ne sont pas mis à jour. Étant donné que seul l’ID d’entreprise est utilisé pour l’intégration, cela n’affecte pas la synchronisation. Si vous souhaitez que les noms correspondent, vous devez mettre à jour la société, le centre de profit et l’équipe dans [!INCLUDE[prod_short](includes/cds_long_md.md)].

L’image suivante montre un exemple de cette configuration de données dans [!INCLUDE[prod_short](includes/cds_long_md.md)].

![Le centre de profit racine est en haut, les équipes au centre, puis les sociétés en bas.](media/cds_bu_team_company.png)

Dans cette configuration, les enregistrements associés à la société Cronus US appartiennent à une équipe associée au centre de profit Cronus US dans [!INCLUDE[prod_short](includes/cds_long_md.md)]. Les utilisateurs pouvant accéder à ce centre de profit au moyen d’un rôle de sécurité défini sur la visibilité au niveau du centre de profit dans [!INCLUDE[prod_short](includes/cds_long_md.md)] peuvent maintenant voir ces enregistrements. L’exemple suivant montre comment utiliser des équipes pour fournir l’accès à ces enregistrements.

* Le rôle de responsable commercial est attribué aux membres de l’équipe commerciale de Cronus US.
* Les utilisateurs ayant le rôle de responsable commercial peuvent accéder aux enregistrements de compte pour les membres du même centre de profit.
* L’équipe commerciale de Cronus US est associée au centre de profit de Cronus US mentionné précédemment. Les membres de l’équipe commerciale de Cronus US peuvent voir tout compte appartenant à l’utilisateur Cronus US, qui proviendrait de la table Société Cronus US dans [!INCLUDE[prod_short](includes/prod_short.md)].

Cependant, le mappage 1:1 entre le centre de profit, la société et l’équipe n’est qu’un point de départ, comme le montre l’image suivante.

![Le rôle de sécurité contrôle la visibilité des données.](media/cds_bu_team_company_2.png)

Dans cet exemple, un nouveau centre de profit racine EUR (Europe) est créé dans [!INCLUDE[prod_short](includes/cds_long_md.md)] en tant que parent pour Cronus DE (Allemagne) et Cronus ES (Espagne). Le centre de profit EUR n’est pas associé à la synchronisation. Cependant, il peut donner aux membres de l’équipe commerciale EUR l’accès aux données de compte dans Cronus DE et Cronus ES en définissant la visibilité des données sur **Centre de profit parent/enfant** sur le rôle de sécurité associé dans [!INCLUDE[prod_short](includes/cds_long_md.md)].

La synchronisation détermine l’équipe devant posséder les enregistrements. Ceci est contrôlé par le champ **Équipe propriétaire par défaut** sur la ligne BCI. Lorsqu’un enregistrement BCI est activé pour la synchronisation, nous créons automatiquement le centre de profit associé et l’équipe propriétaire (si elle n’existe pas déjà), et définissons le champ **Équipe propriétaire par défaut**. Lorsque la synchronisation est activée pour une table, les administrateurs peuvent changer d’équipe propriétaire, mais une équipe doit toujours être affectée.

> [!NOTE]
> Les enregistrements passent en lecture seule après l’ajout et la sauvegarde d’une société. Veillez donc à choisir la société adéquate.

## <a name="choosing-a-different-business-unit"></a>Choix d’un autre centre de profit
Vous pouvez modifier la sélection du centre de profit si vous utilisez le modèle de propriété Teams. Si vous utilisez le modèle de propriété Personne, le centre de profit par défaut est toujours sélectionnée. 

Si vous choisissez un autre centre, par exemple un que vous avez créé précédemment dans [!INCLUDE[prod_short](includes/cds_long_md.md)], il conserve son nom initial. Autrement dit, il n’est pas suivi de l’ID société. Nous allons créer une équipe qui utilise la convention de nommage.

Lorsque vous modifiez un centre de profit, vous ne pouvez choisir que les centres de profit situés un niveau en dessous du centre de profit racine.

## <a name="person-ownership"></a>Propriété Personne
Si vous choisissez le modèle de propriété Personne, vous devez indiquer chaque vendeur qui possédera de nouveaux enregistrements. Le centre de profit et l’équipe sont créés comme décrit dans la section [Propriété Équipe](admin-cds-company-concept.md#team-ownership).

Le centre de profit par défaut est utilisé lorsque le modèle de propriété Personne est choisi et que vous ne pouvez pas choisir un autre centre de profit. L’équipe associée au centre de profit par défaut détiendra des enregistrements pour des tables communes, telles que la table Produit, qui ne sont pas liées à des vendeurs spécifiques.

Lorsque vous associez des vendeurs [!INCLUDE[prod_short](includes/prod_short.md)] aux utilisateurs de [!INCLUDE[prod_short](includes/cds_long_md.md)], [!INCLUDE[prod_short](includes/prod_short.md)] ajoute l’utilisateur à l’équipe par défaut dans [!INCLUDE[prod_short](includes/cds_long_md.md)]. Vous pouvez vérifier que les utilisateurs sont ajoutés en consultant la colonne **Membre de l’équipe par défaut** sur la page **Utilisateurs – Common Data Service**. Si l’utilisateur n’est pas ajouté, vous pouvez l’ajouter manuellement en utilisant l’action **Ajouter des utilisateurs couplés à l’équipe**. Pour plus d’informations, voir [Synchronisation des données dans Business Central avec Dataverse](admin-synchronizing-business-central-and-sales.md).

## <a name="see-also"></a>Voir aussi
[À propos de [!INCLUDE[prod_short](includes/cds_long_md.md)]](admin-common-data-service.md)

[!INCLUDE[footer-include](includes/footer-banner.md)]
