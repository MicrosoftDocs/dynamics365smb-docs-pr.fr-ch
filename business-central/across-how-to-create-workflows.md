---
title: Créer des flux de travail pour connecter des tâches
description: Vous pouvez créer des flux de travail qui relient les tâches de processus métier effectuées par différents utilisateurs et inclure des tâches système, telles que la validation automatique, en tant qu’étapes de flux de travail.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 06/30/2021
ms.author: edupont
ms.openlocfilehash: b4f6894c0d9c5a23445f70b2a50fcd677b17be66
ms.sourcegitcommit: a7cb0be8eae6ece95f5259d7de7a48b385c9cfeb
ms.translationtype: HT
ms.contentlocale: fr-CH
ms.lasthandoff: 07/08/2021
ms.locfileid: "6438422"
---
# <a name="create-workflows-to-connect-business-process-tasks"></a>Créer des flux de travail pour connecter des tâches de processus entreprise

Vous pouvez créer des workflows qui connectent des tâches de processus entreprise exécutées par différents utilisateurs. Les tâches du système, telles que la validation automatique, peuvent être incluses comme étapes du workflow, précédées ou suivies des tâches de l’utilisateur. Demander et accorder une approbation pour créer des enregistrements sont des étapes classiques du flux de travail.  

Sur la page **Workflow**, créez un workflow en répertoriant les étapes concernées sur les lignes. Chaque étape comprend un événement de workflow modéré par des conditions d’événement, et une réponse de workflow avec des options de réponse. Définissez les étapes de workflow en renseignez les champs des lignes de workflow à partir de listes fixes de valeurs d’événement et de réponse qui sont les scénarios pris en charge par le code d’application.  

Lorsque vous créez des workflows, vous pouvez copier les étapes à partir de workflows existants ou de modèles de workflow. Les modèles de workflow représentent des workflows non modifiables qui existent dans la version générique de [!INCLUDE[prod_short](includes/prod_short.md)]. Le code des modèles de workflow ajoutés par Microsoft a le préfixe « MS- », comme dans « MS-PIW ». Pour plus d’informations, reportez-vous à la rubrique [Créer des flux de travail à partir de modèles de flux de travail](across-how-to-create-workflows-from-workflow-templates.md).  

Si votre scénario d’entreprise requiert des événements ou réponses de workflow qui ne sont pas pris en charge, un partenaire Microsoft doit les implémenter en créant une extension qui met en place l’événement de flux de travail pertinent.  

> [!NOTE]  
> Toutes les notifications relatives aux étapes du workflow sont envoyées à l’aide d’une file projets. Veillez à ce que la file d’attente de tâches reflète les besoins de votre entreprise. Pour plus d’informations, voir [Utiliser des files d’attente des travaux pour planifier des tâches](admin-job-queues-schedule-tasks.md).  

:::image type="content" source="media/Workflows/workflow-example.png" alt-text="Illustration d’un exemple de flux de travail.":::

Le flux de travail est divisé en trois sections :

1) **En cas d’événement** C’est là que le déclencheur est sélectionné.
    Des exemples de déclencheur pourraient être :
    - Un enregistrement de données de base est modifié
    - Une ligne feuille est créée
    - Un document entrant est créé ou lancé
    - L’approbation d’un document est exigée

2) **Condition** Les **conditions** sont liées à l’événement ; s’ouvre pour créer des filtres lorsque l’événement est déclenché
3) **Alors, réponse** Les **Réponses** répondent à la prochaine étape du travail.

Pour les deux types d’événements, les événements sont définis par le système. De nouveaux événements doivent être ajoutés via le développement d’une extension.

## <a name="to-create-a-workflow"></a>Pour créer un workflow

1. Sélectionnez l’icône ![Ampoule qui ouvre la fonction Tell Me.](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire") entrez **Flux de travail**, puis choisissez le lien associé.  
2. Sélectionnez l’action **Nouveau**. La page **Flux de travail** s’ouvre.  
3. Dans le champ **Code**, entrez 20 caractères maximum pour identifier le workflow.  
4. Pour créer le flux de travail à partir d’un modèle de flux de travail, dans la page **Flux de travail**, choisissez l’action **Créer le flux de travail à partir du modèle**. Pour plus d’informations, reportez-vous à la rubrique [Créer des flux de travail à partir de modèles de flux de travail](across-how-to-create-workflows-from-workflow-templates.md).  
5. Dans le champ **Description**, décrivez le workflow.  
6. Dans le champ **Catégorie**, spécifiez la catégorie à laquelle le workflow appartient.  
7. Dans le champ **En cas d’événement**, spécifiez l’événement qui doit se produire pour démarrer l’étape du workflow.  

    Lorsque vous choisissez le champ, la page **Événements de flux de travail** s’ouvre pour vous permettre de choisir parmi tous les événements de flux de travail qui existent.  
8. Dans le champ **Condition**, spécifiez une ou plusieurs conditions qui doivent être remplies pour que l’événement dans le champ **En cas d’événement** puisse se produire.  

    Lorsque vous sélectionnez le champ, la page **Conditions d’événement** s’ouvre pour vous permettre de choisir dans une liste de champs de filtre pouvant être utilisés comme conditions pour l’événement en question. Vous pouvez ajouter des champs de filtre à utiliser comme conditions d’événement. Définissez des filtres de condition d’événement comme vous définissez des filtres sur les pages de demande d’état.  

    Si l’événement de flux de travail est la modification d’un champ spécifique d’un enregistrement, la page **Conditions d’événement** s’ouvre avec des options pour sélectionner le champ et le type de modification.  

    1. Pour spécifier une modification de champ pour l’événement, sur la page **Conditions d’événement**, dans le champ **Champ**, sélectionnez le champ qui est modifié.  
    2. Dans le champ **Opérateur**, sélectionnez **Diminué**, **Augmenté** ou **Modifié**.  
9. Dans le champ **Alors, réponse**, spécifiez la réponse qui suivra lorsque l’événement de workflow se produira.  

     Lorsque vous choisissez le champ, la page **Réponses de flux de travail** s’ouvre pour vous permettre de choisir parmi toutes les réponses de flux de travail qui existent et de définir des options de réponse pour la réponse sélectionnée.  
10. Dans le raccourci **Options pour la réponse sélectionnée**, spécifiez les options pour la réponse de workflow, en sélectionnant des valeurs dans les différents champs qui s’affichent, comme suit :  

    1. Pour spécifier des options pour une réponse de workflow impliquant l’envoi d’une notification, renseignez les champs comme indiqué dans le tableau suivant.  

        |Champ|Description|  
        |-----|-----------|  
        |**Notifier l’expéditeur**|Indiquez si le demandeur de l’approbation est notifié au lieu du destinataire de la demande d’approbation. Si vous activez la case à cocher, le champ **ID utilisateur du destinataire** est désactivé, car le demandeur de l’approbation, c’est-à-dire l’expéditeur, est notifié à la place. Le nom de la réponse du flux de travail est modifié en conséquence, en **Créer une notification pour &lt;Expéditeur&gt;**. Si la case à cocher n’est pas activée, le nom de la réponse du flux de travail est **Créer une notification pour &lt;Utilisateur&gt;**.
        |**Code utilisateur du destinataire**|Spécifiez l’utilisateur auquel la notification doit être envoyée. **Remarque** : cette option n’est disponible que pour les réponses de workflow avec un espace réservé pour un utilisateur spécifique. Pour les réponses de workflow sans espaces réservés pour les utilisateurs, le destinataire de la notification est généralement défini par le paramètres utilisateur d’approbation.|  
        |**Type écriture notification**|Spécifie si la notification de flux de travail est déclenchée par une modification d’enregistrement, une demande d’approbation ou des données échues transmises.|
        |**Page cible du lien**|Spécifiez une autre page que le lien de la notification ouvre au lieu de la page par défaut. Notez que la page doit avoir la même table source que l’enregistrement impliqué.|
        |**Lien personnalisé**|Spécifiez l’URL d’un lien qui est ajouté à la notification en complément du lien vers une page.|  

    2. Pour spécifier des options pour une réponse de workflow impliquant la création d’une demande d’approbation, renseignez les champs comme indiqué dans le tableau suivant.  

        |Champ|Désignation|  
        |-----|-----------|  
        |**Formule échéance**|Spécifiez le nombre de jours suite auxquels la demande d’approbation doit être résolue, à compter de la date à laquelle elle a été envoyée.|
        |**Déléguer après**|Spécifiez si et quand une demande d’approbation est automatiquement déléguée au substitut approprié. Vous pouvez choisir de déléguer automatiquement un, deux ou cinq jours après la date de demande d’approbation.|
        |**Type approbateur**|Spécifiez l’approbateur, en fonction des paramètres des utilisateurs d’approbation et de workflow. Lorsque le champ est défini sur **Vendeur/Acheteur**, cela indique que l’utilisateur configuré dans le champ **Code vendeur/acheteur** de la page **Paramètres utilisateur approbation** détermine l’approbateur. Les écritures de demande d’approbation sont ensuite créées en fonction de la valeur du champ **Type limite approbateur**. Pour plus d’informations, voir [Configurer des utilisateurs d’approbation](across-how-to-set-up-workflow-users.md).|
        |**Afficher le message de confirmation**|Spécifiez si un message de confirmation apparaît aux utilisateurs après leur demande d’approbation.|
        |**Type limite approbateur**|Spécifiez les effets des limites d’approbation des approbateurs lorsque les écritures demande d’approbation sont créées pour eux. Un approbateur qualifié est un approbateur pour lequel la limite d’approbation est supérieure à la valeur de la demande. Les options suivantes existent : <ol><li>**Chaîne d’approbateurs** spécifie que les écritures demande d’approbation sont créées pour tous les approbateurs du demandeur jusqu’au et y compris le premier approbateur qualifié.</li><li>**Approbateur direct** spécifie qu’une écriture de demandes d’approbation n’est créée que pour l’approbateur immédiat du demandeur, quelle que soit la limite d’approbation de l’approbateur.</li><li>**Premier approbateur qualifié** spécifie qu’une écriture de demandes d’approbation n’est créée que pour le premier approbateur qualifié du demandeur.</li></ol>|
    3. Pour spécifier des options pour une réponse de workflow impliquant la création de lignes feuille, renseignez les champs comme indiqué dans le tableau suivant.  

        |Champ|Désignation|  
        |-----|-----------|  
        |**Nom du modèle feuille comptabilité**|Spécifiez le nom du modèle feuille comptabilité dans lequel les lignes feuille spécifiées sont créées.|  
        |**Nom feuille comptabilité**|Spécifiez le nom feuille comptabilité dans lequel les lignes feuille spécifiées sont créées.|  

11. Choisissez les boutons **Augmenter le retrait** et **Réduire le retrait** pour mettre en retrait le nom de l’événement dans le champ **Si** pour définir la position de l’étape dans le workflow.  

    1. Indiquez que l’étape est la suivante dans l’ordre du workflow en mettant en retrait le nom de l’événement sous le nom d’événement de l’étape précédente.  
    2. Indiquez que l’étape est l’une des étapes alternatives qui peuvent démarrer en fonction de sa condition en plaçant le nom de l’événement à la même indentation que les autres étapes. Classez ces étapes facultatives en fonction de leur priorité en plaçant l’étape la plus importante en premier.  

    > [!NOTE]  
    >  Vous ne pouvez modifier que le retrait d’une étape qui n’a pas d’étape suivante.  

12. Répétez les étapes 7 à 11 pour ajouter d’autres étapes de workflow, avant ou après l’étape que vous venez de créer.  
13. Activez la case à cocher **Activé** pour spécifier que le workflow démarre lorsque l’événement de la première étape de type **Point d’entrée** se produit. Pour plus d’informations, voir [Utilisation des workflows](across-use-workflows.md).  

> [!NOTE]  
> N’activez pas un workflow tant que vous n’êtes pas sûr qu’il est terminé et que les étapes de workflow concernées peuvent démarrer.  

> [!TIP]  
> Pour voir les relations entre les tables utilisées dans les flux de travail, sélectionnez l’icône ![Ampoule qui ouvre la fonction Tell Me.](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire") puis entrez **Flux de travail - Relations de table**.  

## <a name="example-of-creating-a-new-workflow-using-existing-events"></a>Exemple de création d’un nouveau flux de travail à l’aide d’événements existants

Dans l’exemple suivant, un nouveau flux de travail est créé pour approuver les modifications apportées au nom d’un fournisseur existant :

1. Sélectionnez l’icône ![Ampoule qui ouvre la fonction Tell Me.](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire") entrez **Flux de travail**, puis choisissez le lien associé.  
2. Sélectionnez l’action **Nouveau**. La page **Flux de travail** s’ouvre.
3. Dans la section Flux de travail, renseignez les champs requis comme indiqué dans le tableau suivant.

    |Champ  |Valeur  |
    |---------|---------|
    |**Code**|**VENDAPN-01**|
    |**Description**|**Approbation du changement de nom du fournisseur** |
    |**Catégorie**|**ACHATS**|

4. Pour créer la première étape du flux de travail, procédez comme suit.

    1. Dans le champ **En cas d’événement**, précisez *Un enregistrement fournisseur a été modifié*.  
    2. Dans le champ **Condition**, choisissez le mot **Toujours**, puis, sur la page **Conditions d’événement**, choisissez le lien **Ajouter une condition au cas où une valeur de champ serait modifiée**, puis sélectionnez le champ *Nom*.  

      Le résultat de cette étape est que la condition se lit comme *Le nom a changé*.  
    3. Dans le champ **Alors, réponse**, sélectionnez le lien **Sélectionner la réponse**, puis, dans la page **Réponses de flux de travail**, dans le champ **Sélectionner la réponse**, choisissez le champ *Rétablir la valeur de <Field> sur l’enregistrement et enregistrez la réponse de modification*, puis dans la section **Options pour la réponse sélectionnée**, précisez le champ *Nom*.  
    4. Choisissez le lien **Ajouter d’autres réponses**, puis ajoutez une entrée pour la réponse *Créer une demande d’approbation pour l’enregistrement à l’aide du type approbateur <%1> et <%2>.* .  
    5. Dans la section **Options pour la réponse sélectionnée** pour la nouvelle réponse, modifiez le champ **Type d’approbateur** sur *Groupe d’utilisateurs du flux de travail*, puis, dans le champ **Groupe d’utilisateurs du flux de travail**, spécifiez le groupe d’utilisateurs concerné.  

    Pour plus d’informations, voir [Configurer des utilisateurs d’approbation](across-how-to-set-up-approval-users.md).  
    6. Ajoutez une troisième réponse, *Envoyer une demande d’approbation pour l’enregistrement et créer une notification.*  
    7. Ajoutez une quatrième réponse, *Afficher le message « %1 »*, puis, dans la section **Options pour la réponse sélectionnée**, dans le champ Message, spécifiez **Une demande d’approbation a été envoyée**.  
    8. Cliquez sur le bouton OK pour revenir à l’étape du workflow.  

5. Sur la ligne suivante, ajoutez une nouvelle étape de workflow pour l’événement *Une demande d’approbation est approuvée.* .  

    1. Dans le champ **En cas d’événement**, précisez *Une demande d’approbation est approuvée*.  
    2. Choisissez le menu en ligne, puis choisissez **Augmenter le retrait**.  
    3. Dans le **Condition**, choisissez le mot **Toujours**, puis, dans le champ **Approbations en attente**, précisez *0*.  

      Le résultat de cette étape est que la condition se lit comme *Approbations en attente : 0* pour indiquer qu’il s’agit du dernier approbateur.  
    4. Dans le champ **Alors, réponse**, choisissez le lien **Sélectionner la réponse**, puis, sur la page **Réponses de flux de travail**, dans le champ **Sélectionner la réponse**, choisissez la réponse *Envoyer une demande d’approbation pour l’enregistrement et créer une notification*.  
    5. Cliquez sur le bouton OK.  
6. Sur la ligne suivante, ajoutez une deuxième étape de workflow pour l’événement *Une demande d’approbation est approuvée*.  

    1. Dans le champ **En cas d’événement**, précisez *Une demande d’approbation est approuvée*.
    2. Dans le **Condition**, choisissez le mot **Toujours**, puis, dans le champ **Approbations en attente**, précisez *>0*.  

      Le résultat de cette étape est que la condition se lit comme *Approbations en attente : >0* pour indiquer qu’il ne s’agit *pas* du dernier approbateur.  
    3. Dans le champ **Alors, réponse**, choisissez le lien **Sélectionner la réponse**, puis, sur la page **Réponses de flux de travail**, dans le champ **Sélectionner la réponse**, choisissez la réponse *Envoyer une demande d’approbation pour l’enregistrement et créer une notification*.  
    4. Cliquez sur le bouton OK.  
7. Sur la ligne suivante, ajoutez une deuxième étape de workflow pour l’événement *Une demande d’approbation est rejetée*.  

    1. Dans le champ **En cas d’événement**, précisez *Une demande d’approbation est rejetée*.  
    2. Dans le champ **Condition**, laissez la valeur définie sur *Toujours*.  
    3. Dans le champ **Alors, réponse**, choisissez le lien **Sélectionner la réponse**, puis, sur la page **Réponses de flux de travail**, dans le champ **Sélectionner la réponse**, choisissez la réponse *Ignorer les nouvelles valeurs*.  
    4. Choisissez le lien **Ajouter d’autres réponses**, puis ajoutez une entrée pour la réponse *Rejeter la demande d’approbation pour l’enregistrement et créer une notification*.
    5. Cliquez sur le bouton OK.  
8. Sur la ligne suivante, ajoutez une deuxième étape de workflow pour l’événement *Une demande d’approbation est rejetée*.  

    1. Dans le champ **En cas d’événement**, précisez *Une demande d’approbation est rejetée*.  
    2. Dans le champ **Condition**, laissez la valeur définie sur *Toujours*.  
    3. Dans le champ **Alors, réponse**, choisissez le lien **Sélectionner la réponse**, puis, sur la page **Réponses de flux de travail**, dans le champ **Sélectionner la réponse**, choisissez la réponse *Envoyer une demande d’approbation pour l’enregistrement et créer une notification*.  
    4. Cliquez sur le bouton OK.  
9. Pour activer le flux de travail, choisissez le champ **Activé**.  

Les illustrations suivantes donnent un aperçu du résultat de cette procédure.  

:::image type="content" source="media/Workflows/workflow-example-2.png" alt-text="Illustration du flux de travail Approbation du nom du fournisseur.":::

Ensuite, vous devez et tester le flux de travail en ouvrant un fournisseur existant et en changeant le nom. Vérifiez qu’une demande d’approbation est effectuée lors de la modification du nom du fournisseur.

## <a name="see-also"></a>Voir aussi

[Créer des flux de travail à partir de modèles de flux de travail](across-how-to-create-workflows-from-workflow-templates.md)  
[Configurer des utilisateurs d’approbation](across-how-to-set-up-approval-users.md)  
[Configuration de notifications de workflow](across-setting-up-workflow-notifications.md)  
[Afficher des instances d’étape de workflow archivées](across-how-to-view-archived-workflow-step-instances.md)  
[Supprimer des workflows](across-how-to-delete-workflows.md)  
[Procédure pas à pas : configuration et utilisation d’un flux d’approbation achat](walkthrough-setting-up-and-using-a-purchase-approval-workflow.md)  
[Paramétrage des workflows](across-set-up-workflows.md)  
[Utilisation des workflows](across-use-workflows.md)  
[Flux de travail](across-workflow.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
