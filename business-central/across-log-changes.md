---
title: Audit des modifications| Microsoft Docs
description: Vous pouvez activer un journal utilisateur de sorte que vous avez un historique de toutes les modifications apportées aux données dans les tables suivies. Vous pouvez également suivre les activités avec certains types de journaux d’activité.
author: edupont04
ms.service: dynamics365-business-central
ms.topic: get-started-article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: user log, user activity, tracking
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: 1497051beebd01839dfc4b4fe2dce6b46977eef4
ms.sourcegitcommit: ddbb5cede750df1baba4b3eab8fbed6744b5b9d6
ms.translationtype: HT
ms.contentlocale: fr-CH
ms.lasthandoff: 10/01/2020
ms.locfileid: "3922682"
---
# <a name="auditing-changes-in-business-central"></a>Audit des modifications dans Business Central
Un défi courant dans de nombreuses applications de gestion d’entreprise est d’éviter les modifications indésirables des données. Il peut s’agir d’une simple erreur de numéro de téléphone client comme d’une écriture comptable erronée. Cette rubrique décrit les fonctionnalités permettant de savoir ce qui a changé, qui l’a modifié et quand la modification a été effectuée.

## <a name="about-the-change-log"></a>À propos du journal des modifications 
Le journal des modifications vous permet de suivre toutes les modifications directes apportées par un utilisateur aux données dans la base de données. Vous devez spécifier les opérations que le système doit journaliser, pour chaque table et chaque champ, puis activer le journal modification.  

Le journal des modifications est basé sur les modifications apportées aux données dans les tableaux que vous suivez. Sur la page **Écritures du journal des modifications** , les entrées sont chronologiquement ordonnées et montrent toutes les modifications apportées aux valeurs des champs des tables que vous spécifiez.

> [!Important]
> Les changements s’affichent dans **Écritures journal modification** seulement après le redémarrage de la session de l’utilisateur, ce qui se passe comme suit :
<br />
> * La session a expiré et a été actualisée.
> * L’utilisateur a sélectionné une autre société ou un autre Tableau de bord.
> * L’utilisateur s’est déconnecté et reconnecté.

### <a name="working-with-the-change-log"></a>Utilisation du journal des modifications
Vous devez activer et désactiver le journal des modifications sur la page **Paramètres journal modification** . Lorsqu’un utilisateur active ou désactive le journal des modifications, cette activité est enregistrée, ainsi vous pouvez toujours savoir quel utilisateur est à l’origine de la modification.

Sur la page **Paramètres journal modification** , si vous choisissez l’option **Tables** , vous pouvez spécifier les tables dont vous souhaitez suivre les modifications, et quelles modifications suivre. [!INCLUDE[d365fin](includes/d365fin_md.md)] suit également un nombre de tables système.

> [!NOTE]
> Vous pouvez surveiller des champs spécifiques pour les changements, tels que les champs qui contiennent des données sensibles, en configurant la surveillance de champ. Si vous le faites, pour éviter la redondance, la table qui contient le champ ne sera pas disponible pour la configuration du journal des modifications. Pour plus d’informations, voir [Surveillance des champs sensibles](across-log-changes.md#monitoring-sensitive-fields).

Une fois que vous avez configuré et activé le journal des modifications et modifié des données, vous pouvez afficher et filtrer les modifications sur la page **Écritures journal modification** . Vous pouvez supprimer des données à partir de la page **Suppr écritures journal modif** , dans laquelle vous pouvez définir des filtres basés sur la date et l’heure.  

## <a name="about-activity-logs"></a>À propos des journaux d’activité
À partir des pages [!INCLUDE [prodshort](includes/prodshort.md)], vous pouvez afficher un journal d’activités indiquant l’état et les erreurs éventuelles des fichiers que vous exportez ou importez dans [!INCLUDE [prodshort](includes/prodshort.md)].  

### <a name="working-with-activity-logs"></a>Utilisation des journaux d’activité
Les informations sont affichées dans la page **Journal des activités** , en fonction du contexte d’ouverture. Par exemple, vous pouvez ouvrir la page depuis les pages **Paramètres du service d’échange de documents** , **Document entrant** , **Facture vente validée** et **Avoir vente enregistré** , par exemple. Vous pouvez vider la liste des entrées du journal ou simplement effacer la liste des entrées de plus de sept jours.  

## <a name="monitoring-sensitive-fields"></a>Surveillance des champs sensibles
La protection et la confidentialité des données sensibles est au cœur des préoccupations de la plupart des entreprises. Pour ajouter une couche de sécurité, vous pouvez surveiller les champs importants et être averti par e-mail lorsque quelqu’un change une valeur. Par exemple, vous souhaiterez peut-être être averti si quelqu’un change le numéro IBAN de votre entreprise.

> [!NOTE]
> Pour envoyer des notifications par e-mail, vous devez configurer la fonction e-mail dans [!INCLUDE[prodshort](includes/prodshort.md)]. Pour plus d’informations, voir [Configurer la messagerie](admin-how-setup-email.md).

### <a name="setting-up-field-monitoring"></a>Configuration de la surveillance des champs
Vous pouvez utiliser le guide de configuration assistée **Surveiller la configuration du changement de champ** pour spécifier les champs que vous souhaitez surveiller en fonction de critères de filtre, tels que la classification de sensibilité des données pour les champs. Pour plus d’informations, voir [Classification de la sensibilité des données](admin-classifying-data-sensitivity.md). Le guide vous permet également de spécifier la personne qui recevra une notification par e-mail en cas de modification et le compte de messagerie qui enverra l’e-mail de notification. Vous devez spécifier à la fois la notification de l’utilisateur et le compte à partir duquel envoyer la notification. Une fois le guide terminé, vous pouvez gérer les paramètres de surveillance des champs sur la page **Configuration de la surveillance des champs** . 

Au fil du temps, la liste des entrées sur la page **Entrées du journal des champs surveillés** grandira. Pour réduire le nombre d’entrées, vous pouvez créer une stratégie de rétention qui supprimera les entrées après une période de temps spécifiée. Pour plus d’informations, voir [Définir les stratégies de rétention](admin-data-retention-policies.md).

Lorsque vous configurez la surveillance des champs ou modifiez quelque chose dans la configuration, des entrées sont créées pour vos modifications. Vous pouvez spécifier si vous souhaitez afficher les entrées liées à la configuration de la surveillance en les affichant ou en les masquant. 

Vous pouvez gérer les paramètres de surveillance des champs, par exemple envoyer une notification par e-mail ou simplement consigner la modification, pour chaque champ sur la page **Feuille de calcul Champs surveillés** . La page est également l’endroit où vous pouvez ajouter ou supprimer des champs à surveiller.

> [!NOTE]
> Après avoir ajouté un ou plusieurs champs et commencé la surveillance, déconnectez-vous de [!INCLUDE[prodshort](includes/prodshort.md)] et reconnectez-vous pour appliquer vos paramètres.

### <a name="working-with-field-monitoring"></a>Utilisation de la surveillance des champs
Les entrées de toutes les valeurs modifiées des champs surveillés sont disponibles sur la page **Entrées du journal des champs surveillés** . Par exemple, les entrées contiennent des informations, telles que le champ pour lequel la valeur a été modifiée, les valeurs d’origine et les nouvelles valeurs, qui a effectué la modification et à quel moment. Pour étudier plus en détail une modification, choisissez une valeur pour ouvrir la page sur laquelle elle a été effectuée. Pour afficher une liste de toutes les entrées, choisissez **Écritures de modification de champ** .

## <a name="defining-retention-policies"></a>Définition des stratégies de rétention
Vous pouvez créer des stratégies de rétention pour supprimer les données inutiles dans les journaux après une période de temps que vous spécifiez. Par exemple, au fil du temps, le nombre d’entrées dans un journal peut augmenter. En nettoyant les anciennes entrées, vous pouvez vous concentrer plus facilement sur des entrées plus récentes et probablement plus pertinentes. Pour plus d’informations, voir [Définir les stratégies de rétention](admin-data-retention-policies.md).

## <a name="see-also"></a>Voir aussi
[Modifier les paramètres de base](ui-change-basic-settings.md)  
[Tri, recherche et filtrage](ui-enter-criteria-filters.md)  
[Recherche de pages et d’informations avec la fonction Tell Me](ui-search.md)  
[Attribuer des autorisations aux utilisateurs et aux groupes](ui-define-granular-permissions.md)    
[Utilisation de [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)  
[Définir des stratégies de rétention](admin-data-retention-policies.md)  