---
title: Mappage des sociétés et des centres de profit | Microsoft Docs
description: Les sociétés sont des entités à la fois juridiques et commerciales, qui permettent de sécuriser et visualiser les données métier.
author: bholtorf
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: CDS, Common Data Service, integration, sync
ms.date: 01/17/2020
ms.author: bholtorf
ms.openlocfilehash: 795656cd5b4ad8d40c48a2edf327cffb56ad6906
ms.sourcegitcommit: 7d54d8abe52e0546378cf760f5082f46e8441b90
ms.translationtype: HT
ms.contentlocale: fr-CH
ms.lasthandoff: 04/30/2020
ms.locfileid: "3324069"
---
# <a name="data-ownership-models"></a>Modèles de propriété de données
[!INCLUDE[d365fin](includes/cds_long_md.md)] nécessite que vous indiquiez un propriétaire pour les données que vous stockez. Pour en savoir plus, consultez [Propriété d'entité](https://docs.microsoft.com/powerapps/maker/common-data-service/types-of-entities#entity-ownership) dans la documentation Power Apps. Lorsque vous configurez l'intégration entre [!INCLUDE[d365fin](includes/cds_long_md.md)] et [!INCLUDE[d365fin](includes/d365fin_md.md)], vous devez choisir l'un des deux modèles de propriété pour les enregistrements synchronisés :

* Équipe 
* Personne (utilisateur)

Les actions pouvant être effectuées sur ces enregistrements peuvent être contrôlées au niveau de l'utilisateur. Pour en savoir plus, consultez [Entités Utilisateur et Équipe](https://docs.microsoft.com/powerapps/developer/common-data-service/user-team-entities). Nous vous recommandons le modèle de propriété Équipe, car il facilite la gestion de la propriété pour plusieurs personnes.

## <a name="team-ownership"></a>Propriété Équipe
Dans [!INCLUDE[d365fin](includes/d365fin_md.md)], une société est une entité juridique et commerciale qui permet de sécuriser et visualiser les données métier. Les utilisateurs travaillent toujours dans le cadre d'une société. L'élément de [!INCLUDE[d365fin](includes/cds_long_md.md)] le plus proche de ce concept est l'entité Centre de profit, qui n'a aucune implication juridique ou commerciale.

Comme les centres de profit n'ont aucune implication juridique ou commerciale, vous ne pouvez pas forcer un mappage un à un (1:1) pour synchroniser les données entre une société et un centre de profit, que la synchronisation soit unidirectionnelle ou bidirectionnelle. Pour rendre la synchronisation possible, lorsque vous activez la synchronisation pour une société dans [!INCLUDE[d365fin](includes/d365fin_md.md)], ce qui suit se produit dans [!INCLUDE[d365fin](includes/cds_long_md.md)] :

* Nous créons une entité Société équivalente à l'entité Société dans [!INCLUDE[d365fin](includes/d365fin_md.md)]. Le nom de la société est suivi de « ID société BC ». Par exemple, Cronus International Ltd. (93555b1a-af3e-ea11-bb35-000d3a492db1).
* Nous créons un centre de profit par défaut qui porte le même nom que la société. Par exemple, Cronus International Ltd. (93555b1a-af3e-ea11-bb35-000d3a492db1).
* Nous créons une équipe propriétaire distincte portant le même nom que la société et l'associons au centre de profit. Le nom de l'équipe est précédé de « BCI - ». Par exemple, BCI - Cronus International Ltd. (93555b1a-af3e-ea11-bb35-000d3a492db1).
* Les enregistrements créés et synchronisés avec [!INCLUDE[d365fin](includes/cds_long_md.md)] sont affectés à l'équipe « Propriétaire BCI » associée au centre de profit.

> [!NOTE]
> Si vous renommez une entreprise en [!INCLUDE[d365fin](includes/d365fin_md.md)], les noms de l'entreprise, de l'activité commerciale et de l'équipe que nous créons automatiquement dans [!INCLUDE[d365fin](includes/cds_long_md.md)] ne sont pas mis à jour. Étant donné que seul l'ID d'entreprise est utilisé pour l'intégration, cela n'affecte pas la synchronisation. Si vous souhaitez que les noms correspondent, vous devez mettre à jour la société, le centre de profit et l'équipe dans [!INCLUDE[d365fin](includes/cds_long_md.md)].

L'image suivante montre un exemple de cette configuration de données dans [!INCLUDE[d365fin](includes/cds_long_md.md)].

![Le centre de profit racine est en haut, les équipes au centre, puis les sociétés en bas.](media/cds_bu_team_company.png)

Dans cette configuration, les enregistrements associés à la société Cronus US appartiennent à une équipe associée au centre de profit Cronus US <ID> dans [!INCLUDE[d365fin](includes/cds_long_md.md)]. Les utilisateurs pouvant accéder à ce centre de profit au moyen d'un rôle de sécurité défini sur la visibilité au niveau du centre de profit dans [!INCLUDE[d365fin](includes/cds_long_md.md)] peuvent maintenant voir ces enregistrements. L'exemple suivant montre comment utiliser des équipes pour fournir l'accès à ces enregistrements.

* Le rôle de responsable commercial est attribué aux membres de l'équipe commerciale de Cronus US.
* Les utilisateurs ayant le rôle de responsable commercial peuvent accéder aux enregistrements de compte pour les membres du même centre de profit.
* L'équipe commerciale de Cronus US est associée au centre de profit de Cronus US mentionné précédemment. Les membres de l'équipe commerciale de Cronus US peuvent voir tout compte appartenant à l'utilisateur Cronus US <ID>, qui proviendrait de l'entité Société Cronus US dans [!INCLUDE[d365fin](includes/d365fin_md.md)].

Cependant, le mappage 1:1 entre le centre de profit, la société et l'équipe n'est qu'un point de départ, comme le montre l'image suivante.

![Le rôle de sécurité contrôle la visibilité des données.](media/cds_bu_team_company_2.png)

Dans cet exemple, un nouveau centre de profit racine EUR (Europe) est créé dans [!INCLUDE[d365fin](includes/cds_long_md.md)] en tant que parent pour Cronus DE (Allemagne) et Cronus ES (Espagne). Le centre de profit EUR n'est pas associé à la synchronisation. Cependant, il peut donner aux membres de l'équipe commerciale EUR l'accès aux données de compte dans Cronus DE et Cronus ES en définissant la visibilité des données sur **Centre de profit parent/enfant** sur le rôle de sécurité associé dans [!INCLUDE[d365fin](includes/cds_long_md.md)].

La synchronisation détermine l'équipe devant posséder les enregistrements. Ceci est contrôlé par le champ **Équipe propriétaire par défaut** sur l'enregistrement BCI - <ID>. Lorsqu'un enregistrement BCI - <ID> est activé pour la synchronisation, nous créons automatiquement le centre de profit associé et l'équipe propriétaire (si elle n'existe pas déjà), et définissons le champ **Équipe propriétaire par défaut**. Lorsque la synchronisation est activée pour une entité, les administrateurs peuvent changer d'équipe propriétaire, mais une équipe doit toujours être affectée.

> [!NOTE]
> Les enregistrements passent en lecture seule après l'ajout et la sauvegarde d'une société. Veillez donc à choisir la société adéquate.

## <a name="choosing-a-different-business-unit"></a>Choix d'un autre centre de profit
Vous pouvez modifier la sélection du centre de profit si vous utilisez le modèle de propriété Teams. Si vous utilisez le modèle de propriété Personne, le centre de profit par défaut est toujours sélectionnée. 

Si vous choisissez un autre centre, par exemple un que vous avez créé précédemment dans [!INCLUDE[d365fin](includes/cds_long_md.md)], il conserve son nom initial. Autrement dit, il n'est pas suivi de l'ID société. Nous allons créer une équipe qui utilise la convention de nommage.

Lorsque vous modifiez un centre de profit, vous ne pouvez choisir que les centres de profit situés un niveau en dessous du centre de profit racine.

## <a name="person-ownership"></a>Propriété Personne
Si vous choisissez le modèle de propriété Personne, vous devez indiquer chaque vendeur qui possédera de nouveaux enregistrements. Le centre de profit et l'équipe sont créés comme décrit dans la section [Propriété Équipe](admin-cds-company-concept.md#team-ownership).

Le centre de profit par défaut est utilisé lorsque le modèle de propriété Personne est choisi et que vous ne pouvez pas choisir un autre centre de profit. L'équipe associée au centre de profit par défaut détiendra des enregistrements pour des entités communes, telles que l'entité Produit, qui ne sont pas liées à des vendeurs spécifiques.

## <a name="see-also"></a>Voir aussi
[À propos de [!INCLUDE[d365fin](includes/cds_long_md.md)]](admin-common-data-service.md)