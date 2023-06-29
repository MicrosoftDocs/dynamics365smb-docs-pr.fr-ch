---
author: edupont04
ms.topic: include
ms.date: 02/15/2022
ms.author: edupont
---

> [!NOTE]
> Les sections suivantes supposent que vous disposez d’un accès administrateur pour Exchange Online.

Avant de pouvoir configurer la connexion à la messagerie, vous devez préparer les [dossiers publics](/exchange/collaboration-exo/public-folders/public-folders) Office 365. Vous pouvez le faire dans le [Centre d’administration Exchange](/exchange/exchange-admin-center?preserve-view=true), ou vous pouvez utiliser le [PowerShell Exchange Online](/powershell/exchange/exchange-online-powershell?view=exchange-ps&?preserve-view=true).

> [!TIP]
> Si vous souhaitez utiliser [PowerShell Exchange Online](/powershell/exchange/exchange-online-powershell?view=exchange-ps&preserve-view=true), vous pouvez trouver l’inspiration pour configurer votre script dans un exemple de script que nous avons publié dans le [référentiel BCTech](https://github.com/microsoft/BCTech/tree/master/samples/EmailLogging).

Suivez les étapes ci-dessous pour configurer Exchange Online, avec des liens vers où vous pouvez en savoir plus.

### <a name="create-an-admin-role-group"></a><a name="create-an-admin-role-group"></a>Créer un groupe de rôles d’administrateur

Créez un groupe de rôles d’administrateur pour les dossiers publics en fonction des informations de la table suivante :

|Propriété        |Valeur                     |
|----------------|--------------------------|
|Name            |Gestion des dossiers publics |
|Rôles sélectionnés  |Dossiers publics            |
|Utilisateurs sélectionnés  |Adresse e-mail du compte d’utilisateur que Business Central utilisera pour exécuter la tâche de connexion à la messagerie|

Pour en savoir plus, voir [Gérer les groupes de rôles dans Exchange Online](/exchange/permissions-exo/role-groups).

### <a name="create-a-new-public-folder-mailbox"></a><a name="create-a-new-public-folder-mailbox"></a>Créer une boîte aux lettres de dossiers publics

Créez une nouvelle boîte aux lettres pour les dossiers publics en fonction des informations de la table suivante :

|Propriété        |Valeur                     |
|----------------|--------------------------|
|Name            |Boîte aux lettres publique            |

Pour plus d’informations, voir [Créer une boîte aux lettres de dossiers publics](/exchange/collaboration-exo/public-folders/create-public-folder-mailbox).

### <a name="create-new-public-folders"></a><a name="create-new-public-folders"></a>Créer de nouveaux dossiers publics

1. Créez un dossier public avec le nom **Connexion à la messagerie** à la racine afin que le chemin d’accès complet au dossier devienne `\Email Logging\`.
2. Créez deux sous-dossiers afin que le résultat soit les chemins d’accès complets suivants aux dossiers :

    - `\Email Logging\Queue\`
    - `\Email Logging\Storage\`

Pour plus d’informations, voir [Créer un dossier public](/exchange/collaboration-exo/public-folders/create-public-folder).

### <a name="set-public-folder-ownership"></a><a name="set-public-folder-ownership"></a>Définir la propriété des dossiers publics

Définissez l’utilisateur de la connexion à la messagerie en tant que propriétaire des deux dossiers publics, *File d’attente* et *Espace de stockage*.

Pour plus d’informations, voir [Affecter des autorisations au dossier public](/exchange/collaboration-exo/public-folders/set-up-public-folders#step-3-assign-permissions-to-the-public-folder).

### <a name="mail-enable-the-queue-public-folder"></a><a name="mail-enable-the-queue-public-folder"></a>Activer la messagerie du dossier public *File d’attente*

  Pour plus d’informations, voir [Activer ou désactiver la messagerie d’un dossier public](/exchange/collaboration-exo/public-folders/enable-or-disable-mail-for-public-folder).

### <a name="mail-enable-sending-emails-to-the-queue-public-folder"></a><a name="mail-enable-sending-emails-to-the-queue-public-folder"></a>Activer la messagerie pour envoyer des e-mails au dossier public *File d’attente*

Activer la messagerie pour envoyer des e-mails au dossier public *File d’attente* à l’aide d’Outlook ou du shell de gestion Exchange.

Pour plus d’informations, voir [Autoriser les utilisateurs anonymes à envoyer des e-mails vers un dossier public à messagerie activée](/exchange/collaboration-exo/public-folders/enable-or-disable-mail-for-public-folder#allow-anonymous-users-to-send-email-to-a-mail-enabled-public-folder?preserve-view=true).

### <a name="create-mail-flow-rules"></a><a name="create-mail-flow-rules"></a>Créer des règles de flux de messagerie

Créez deux règles de flux de messagerie en fonction des informations de la table suivante :

|Objet  |Name |Appliquer cette règle si...             |Procédez comme suit...                          |
|---------|-----|----------------------------------|---------------------------------------------|
|Une règle pour les e-mails entrants |Consigner les e-mails envoyés à cette organisation|*L’expéditeur* est situé *En dehors de l’organisation*, et *le destinataire* est situé *Au sein de l’organisation*|Cci le compte de messagerie spécifié pour le dossier public *File d’attente*|
|Une règle pour les e-mails sortants | Consigner les e-mails envoyés à partir de cette organisation |*L’expéditeur* est situé *Au sein de l’organisation*, et *le destinataire* est situé *En dehors de l’organisation*|Cci le compte de messagerie spécifié pour le dossier public *File d’attente*|

Pour plus d’informations, voir [Gérer les règles de flux de messagerie dans Exchange Online](/exchange/security-and-compliance/mail-flow-rules/manage-mail-flow-rules?preserve-view=true) et [Actions des règles de flux de messagerie dans Exchange Online](/exchange/security-and-compliance/mail-flow-rules/mail-flow-rule-actions?preserve-view=true).

> [!NOTE]
> Si vous apportez des modifications dans le shell de gestion Exchange, les modifications deviennent visibles dans le centre d’administration Exchange après un certain délai. De plus, les modifications apportées dans Exchange seront disponibles dans [!INCLUDE[prod_short](prod_short.md)] après un délai. Le retard peut être de plusieurs heures.
