---
title: Effectuer le suivi de l'activité utilisateur dans un journal modification| Microsoft Docs
description: Vous pouvez activer un journal utilisateur de sorte que vous avez un historique de toutes les modifications apportées aux données dans les tables suivies.
author: edupont04
ms.service: dynamics365-business-central
ms.topic: get-started-article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: user log, user activity, tracking
ms.date: 04/01/2019
ms.author: edupont
ms.openlocfilehash: fc14d11bf75ea39553c1ed04986273903874a0e1
ms.sourcegitcommit: bd78a5d990c9e83174da1409076c22df8b35eafd
ms.translationtype: HT
ms.contentlocale: fr-CH
ms.lasthandoff: 03/31/2019
ms.locfileid: "915445"
---
# <a name="auditing-changes-in-business-central"></a>Audit des modifications dans Business Central

Vous pouvez activer le journal des modifications dans [!INCLUDE[d365fin](includes/d365fin_md.md)] afin d'avoir un historique des activités. Le journal est basé sur les modifications apportées aux données dans les tableaux que vous suivez. Sur la page **Écritures du journal des modifications**, les entrées sont chronologiquement ordonnées et montrent les modifications apportées aux champs des tables spécifiées. Le journal modification regroupe tous les changements apportés à la table.

> [!Important]
> Les modifications d'un utilisateur ne sont pas visibles dans les **Écritures du journal des modifications** jusqu'à ce que la session utilisateur soit redémarrée, ce qui se produit dans les cas suivants :
<br />
> * La session a expiré et a été actualisée.
> * L'utilisateur a sélectionné une autre société ou un autre Tableau de bord.
> * L'utilisateur s'est déconnecté et reconnecté.

## <a name="working-with-the-change-log"></a>Utilisation du journal des modifications

Dans de nombreux systèmes financiers, il est souvent difficile de trouver l'origine des erreurs ou des modifications de données. Il peut s'agir d'une simple erreur de numéro de téléphone client comme d'une écriture comptable erronée. Le journal des modifications vous permet de suivre toutes les modifications directes apportées par un utilisateur aux données dans la base de données. Vous devez spécifier les opérations que le système doit journaliser, pour chaque table et chaque champ, puis activer le journal modification.  

Vous devez activer et désactiver le journal des modifications sur la page **Paramètres journal modification**. Lorsqu'un utilisateur active ou désactive le journal des modifications, cette activité est enregistrée, ainsi vous pouvez toujours savoir quel utilisateur est à l'origine de la modification.

Sur la page **Paramètres journal modification**, si vous choisissez l'option **Tables**, vous pouvez spécifier les tables dont vous souhaitez suivre les modifications, et quelles modifications suivre. [!INCLUDE[d365fin](includes/d365fin_md.md)] suit également un nombre de tables système.

Une fois que vous avez configuré et activé le journal des modifications et modifié des données, vous pouvez afficher et filtrer les modifications sur la page **Écritures journal modification**. Vous pouvez supprimer des données à partir de la page **Suppr écritures journal modif**, dans laquelle vous pouvez définir des filtres basés sur la date et l'heure.  

## <a name="see-also"></a>Voir aussi
[Modification des paramètres de base](ui-change-basic-settings.md)  
[Tri](ui-sorting.md)  
[Utilisation de la fonction Tell Me pour trouver des fonctions et des informations](ui-search.md)  
[Gestion des utilisateurs et des autorisations](ui-how-users-permissions.md)    
[Utilisation de [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)  
