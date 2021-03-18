---
author: edupont04
ms.service: dynamics365-accountant
ms.topic: include
ms.date: 10/02/2020
ms.author: edupont
ms.openlocfilehash: d58d8d628577f163d36199b8fc5785982aac830a
ms.sourcegitcommit: a9d48272ce61e5d512a30417412b5363e56abf30
ms.translationtype: HT
ms.contentlocale: fr-CH
ms.lasthandoff: 03/04/2021
ms.locfileid: "5493015"
---
Avant de pouvoir configurer la connexion à la messagerie, vous devez préparer votre Exchange Online avec [dossiers publics](/exchange/collaboration/public-folders/public-folders?view=exchserver-2019&preserve-view=true ). Vous pouvez le faire dans le [Centre d’administration Exchange](/Exchange/architecture/client-access/exchange-admin-center?view=exchserver-2019&preserve-view=true ), ou vous pouvez utiliser le [shell de gestion Exchange](/powershell/exchange/exchange-management-shell?view=exchange-ps&preserve-view=true ).  

> [!TIP]
> Si vous souhaitez utiliser le [shell de gestion Exchange](/powershell/exchange/exchange-management-shell?view=exchange-ps&preserve-view=true ), vous pouvez trouver l’inspiration pour configurer votre script dans un exemple de script que nous avons publié sur [le repo BCTech](https://github.com/microsoft/BCTech/tree/master/samples/EmailLogging).

La liste suivante décrit les principales étapes avec des liens pour en savoir plus.  

- Créez un rôle d’administrateur pour les dossiers publics en fonction des informations de la table suivante :

  |Propriété        |Valeur                     |
  |----------------|--------------------------|
  |Name            |Gestion des dossiers publics |
  |Rôles sélectionnés  |Dossiers publics            |
  |Membres sélectionnés|Adresse e-mail du compte d’utilisateur que Business Central utilisera pour exécuter la tâche de connexion à la messagerie|

  Pour en savoir plus, voir [Gérer les groupes de rôles](/exchange/permissions/role-groups?view=exchserver-2019&preserve-view=true).

- Créez une nouvelle boîte aux lettres pour les dossiers publics en fonction des informations de la table suivante :

  |Propriété        |Valeur                     |
  |----------------|--------------------------|
  |Name            |Boîte aux lettres publique            |

  Pour plus d’informations, voir [Créer une boîte aux lettres pour les dossiers publics dans Exchange Server](/exchange/collaboration/public-folders/create-public-folder-mailboxes).  

- Créer de nouveaux dossiers publics

  - Créez un nouveau dossier public avec le nom *Connexion à la messagerie* à la racine afin que le chemin d’accès complet au dossier devienne ```\Email Logging\```
  - Créez deux sous-dossiers afin que le résultat soit les chemins d’accès complets suivants aux dossiers :
    - ```\Email Logging\Queue\```
    - ```\Email Logging\Storage\```

  Pour plus d’informations, voir [Créer un dossier public](/exchange/collaboration/public-folders/create-public-folders?view=exchserver-2019&preserve-view=true).

- Activer la messagerie du dossier public *File d’attente*

  Pour plus d’informations, voir [Activer ou désactiver la messagerie d’un dossier public](/exchange/collaboration/public-folders/mail-enable-or-disable?view=exchserver-2019&preserve-view=true)

- Activer la messagerie pour envoyer des e-mails au dossier public *File d’attente* à l’aide d’Outlook ou du shell de gestion Exchange

  Pour plus d’informations, voir [Autoriser les utilisateurs anonymes à envoyer des e-mails vers un dossier public à messagerie activée](/exchange/collaboration/public-folders/mail-enable-or-disable#allow-anonymous-users-to-send-email-to-a-mail-enabled-public-folder?view=exchserver-2019&preserve-view=true)

- Définissez l’utilisateur de connexion à la messagerie en tant que propriétaire des deux dossiers publics, *File d’attente* et *Stockage*, à l’aide d’Outlook ou du shell de gestion Exchange en fonction des informations de la table suivante :

  |Propriété        |Valeur                     |
  |----------------|--------------------------|
  |Utilisateur            |Adresse e-mail du compte d’utilisateur que Business Central utilisera pour exécuter la tâche de connexion à la messagerie|
  |Niveau d’autorisation|Propriétaire                     |

  Pour plus d’informations, voir [Affecter des autorisations au dossier public](/exchange/collaboration-exo/public-folders/set-up-public-folders#step-3-assign-permissions-to-the-public-folder).

- Créez deux règles de flux de messagerie en fonction des informations de la table suivante :

  |Objet  |Name |Conditions                        |Action                                       |
  |---------|-----|----------------------------------|---------------------------------------------|
  |Une règle pour les e-mails entrants |Consigner les e-mails envoyés à cette organisation|*L’expéditeur* est situé *En dehors de l’organisation*, et *le destinataire* est situé *Au sein de l’organisation*|Cci le compte de messagerie spécifié pour le dossier public *File d’attente*|
  |Une règle pour les e-mails sortants | Consigner les e-mails envoyés à partir de cette organisation |*L’expéditeur* est situé *Au sein de l’organisation*, et *le destinataire* est situé *En dehors de l’organisation*|Cci le compte de messagerie spécifié pour le dossier public *File d’attente*|
  
  Pour plus d’informations, voir [Gérer les règles de flux de messagerie dans Exchange Online](/exchange/security-and-compliance/mail-flow-rules/manage-mail-flow-rules) et [Actions des règles de flux de messagerie dans Exchange Online](/exchange/security-and-compliance/mail-flow-rules/mail-flow-rule-actions).

> [!NOTE]
> Si vous apportez des modifications dans le shell de gestion Exchange, les modifications deviennent visibles dans le centre d’administration Exchange après un certain délai. De plus, les modifications apportées dans Exchange seront disponibles dans [!INCLUDE[prod_short](prod_short.md)] après un délai. Le retard peut être de plusieurs heures.
