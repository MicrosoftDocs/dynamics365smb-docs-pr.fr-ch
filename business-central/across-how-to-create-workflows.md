---
title: 'Procédure : créer des workflows | Microsoft Docs'
description: Vous pouvez créer des workflows qui connectent des tâches de processus entreprise exécutées par différents utilisateurs. Les tâches du système, telles que la validation automatique, peuvent être incluses comme étapes du workflow, précédées ou suivies des tâches de l'utilisateur. Demander et accorder une approbation pour créer des enregistrements sont des étapes classiques du workflow.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 01/24/2020
ms.author: sgroespe
ms.openlocfilehash: bb7c64727979b7e8f53898c03781a24bcf8f40c4
ms.sourcegitcommit: 877af26e3e4522ee234fbba606615e105ef3e90a
ms.translationtype: HT
ms.contentlocale: fr-CH
ms.lasthandoff: 01/28/2020
ms.locfileid: "2991847"
---
# <a name="create-workflows"></a>Créer des workflows
Vous pouvez créer des workflows qui connectent des tâches de processus entreprise exécutées par différents utilisateurs. Les tâches du système, telles que la validation automatique, peuvent être incluses comme étapes du workflow, précédées ou suivies des tâches de l'utilisateur. Demander et accorder une approbation pour créer des enregistrements sont des étapes classiques du flux de travail.  

Sur la page **Workflow**, créez un workflow en répertoriant les étapes concernées sur les lignes. Chaque étape comprend un événement de workflow modéré par des conditions d'événement, et une réponse de workflow avec des options de réponse. Définissez les étapes de workflow en renseignez les champs des lignes de workflow à partir de listes fixes de valeurs d'événement et de réponse qui sont les scénarios pris en charge par le code d'application.  

Lorsque vous créez des workflows, vous pouvez copier les étapes à partir de workflows existants ou de modèles de workflow. Les modèles de workflow représentent des workflows non modifiables qui existent dans la version générique de [!INCLUDE[d365fin](includes/d365fin_md.md)]. Le code des modèles de workflow ajoutés par Microsoft a le préfixe « MS- », comme dans « MS-PIW ». Pour plus d'informations, reportez-vous à la rubrique [Créer des flux de travail à partir de modèles de flux de travail](across-how-to-create-workflows-from-workflow-templates.md).  

Si votre scénario d'entreprise requiert des événements ou réponses de workflow qui ne sont pas pris en charge, un partenaire Microsoft doit les implémenter en personnalisant le code de l'application.  

> [!NOTE]  
>  Toutes les notifications relatives aux étapes du workflow sont envoyées à l'aide d'une file projets. Assurez-vous que la file projets dans votre installation est configurée pour traiter les notifications du flux de travail, et que la case à cocher **Démarrer automatiquement à partir de NAS** est activée. Pour plus d'informations, voir [Utiliser des files d'attente des travaux pour planifier des tâches](admin-job-queues-schedule-tasks.md).  

## <a name="to-create-a-workflow"></a>Pour créer un workflow  
1. Choisissez l'icône ![Ampoule qui ouvre la fonction Tell Me](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire"), entrez **Flux de travail**, puis sélectionnez le lien associé.  
2. Sélectionnez l'action **Nouveau**. La page **Flux de travail** s'ouvre.  
3. Dans le champ **Code**, entrez 20 caractères maximum pour identifier le workflow.  
4. Pour créer le flux de travail à partir d'un modèle de flux de travail, dans la page **Flux de travail**, choisissez l'action **Créer le flux de travail à partir du modèle**. Pour plus d'informations, reportez-vous à la rubrique [Créer des flux de travail à partir de modèles de flux de travail](across-how-to-create-workflows-from-workflow-templates.md).  
5. Dans le champ **Description**, décrivez le workflow.  
6. Dans le champ **Catégorie**, spécifiez la catégorie à laquelle le workflow appartient.  
7. Dans le champ **En cas d'événement**, spécifiez l'événement qui doit se produire pour démarrer l'étape du workflow.  

    Lorsque vous choisissez le champ, la page **Événements de flux de travail** s'ouvre pour vous permettre de choisir parmi tous les événements de flux de travail qui existent.  
8. Dans le champ **Condition**, spécifiez une ou plusieurs conditions qui doivent être remplies pour que l'événement dans le champ **En cas d'événement** puisse se produire.  

    Lorsque vous sélectionnez le champ, la page **Conditions d'événement** s'ouvre pour vous permettre de choisir dans une liste de champs de filtre pouvant être utilisés comme conditions pour l'événement en question. Vous pouvez ajouter des champs de filtre à utiliser comme conditions d'événement. Définissez des filtres de condition d'événement comme vous définissez des filtres sur les pages de demande d'état.  

    Si l'événement de flux de travail est la modification d'un champ spécifique d'un enregistrement, la page **Conditions d'événement** s'ouvre avec des options pour sélectionner le champ et le type de modification.  

    1.  Pour spécifier une modification de champ pour l'événement, sur la page **Conditions d'événement**, dans le champ **Champ**, sélectionnez le champ qui est modifié.  
    2.  Dans le champ **Opérateur**, sélectionnez **Diminué**, **Augmenté** ou **Modifié**.  
9. Dans le champ **Alors, réponse**, spécifiez la réponse qui suivra lorsque l'événement de workflow se produira.  

     Lorsque vous choisissez le champ, la page **Réponses de flux de travail** s'ouvre pour vous permettre de choisir parmi toutes les réponses de flux de travail qui existent et de définir des options de réponse pour la réponse sélectionnée.  
10. Dans le raccourci **Options pour la réponse sélectionnée**, spécifiez les options pour la réponse de workflow, en sélectionnant des valeurs dans les différents champs qui s'affichent, comme suit :  

    1.  Pour spécifier des options pour une réponse de workflow impliquant l'envoi d'une notification, renseignez les champs comme indiqué dans le tableau suivant.  

        |Champ|Description|  
        |----------------------------------|---------------------------------------|  
        |**Notifier l'expéditeur**|Indiquez si le demandeur de l'approbation est notifié au lieu du destinataire de la demande d'approbation. Si vous activez la case à cocher, le champ **ID utilisateur du destinataire** est désactivé, car le demandeur de l'approbation, c'est-à-dire l'expéditeur, est notifié à la place. Le nom de la réponse du flux de travail est modifié en conséquence, en **Créer une notification pour &lt;Expéditeur&gt;**. Si la case à cocher n'est pas activée, le nom de la réponse du flux de travail est **Créer une notification pour &lt;Utilisateur&gt;**.
        |**Code utilisateur du destinataire**|Spécifiez l'utilisateur auquel la notification doit être envoyée. Remarque : cette option n'est disponible que pour les réponses de workflow avec un espace réservé pour un utilisateur spécifique. Pour les réponses de workflow sans espaces réservés pour les utilisateurs, le destinataire de la notification est généralement défini par le paramètres utilisateur d'approbation.|  
        |**Type écriture notification**|Spécifie si la notification de flux de travail est déclenchée par une modification d'enregistrement, une demande d'approbation ou des données échues transmises.|
        |**Page cible du lien**|Spécifiez une autre page dans [!INCLUDE[d365fin](includes/d365fin_md.md)] que le lien de la notification ouvre au lieu de la page par défaut.<br /><br />Notez que la page doit avoir la même table source que l'enregistrement impliqué.|  
        |**Lien personnalisé**|Spécifiez l'URL d'un lien qui est ajouté à la notification en complément du lien vers une page dans [!INCLUDE[d365fin](includes/d365fin_md.md)].|  
    2.  Pour spécifier des options pour une réponse de workflow impliquant la création d'une demande d'approbation, renseignez les champs comme indiqué dans le tableau suivant.  

        |Champ|Désignation|  
        |----------------------------------|---------------------------------------|  
        |**Formule échéance**|Spécifiez le nombre de jours suite auxquels la demande d'approbation doit être résolue, à compter de la date à laquelle elle a été envoyée.|  
        |**Déléguer après**|Spécifiez si et quand une demande d'approbation est automatiquement déléguée au substitut approprié. Vous pouvez choisir de déléguer automatiquement un, deux ou cinq jours après la date de demande d'approbation.|  
        |**Type approbateur**|Spécifiez l'approbateur, en fonction des paramètres des utilisateurs d'approbation et de workflow.<br /><br /> Les options possibles sont les suivantes :<br /><br /> -   **Vendeur/Acheteur** indique que l'utilisateur configuré dans le champ **Code vendeur/acheteur** de la page **Paramètres utilisateur approbation** détermine l'approbateur. Les écritures de demande d'approbation sont ensuite créées en fonction de la valeur du champ **Type limite approbateur**.<br />     Pour plus d'informations, voir [Configurer des utilisateurs d'approbation](across-how-to-set-up-workflow-users.md).|  
        |**Afficher le message de confirmation**|Spécifiez si un message de confirmation apparaît aux utilisateurs après leur demande d'approbation.|  
        |**Type limite approbateur**|Spécifiez les effets des limites d'approbation des approbateurs lorsque les écritures demande d'approbation sont créées pour eux. Un approbateur qualifié est un approbateur pour lequel la limite d'approbation est supérieure à la valeur de la demande.<br /><br /> Les options possibles sont les suivantes :<br /><br /> 1.  **Chaîne d'approbateurs** spécifie que les écritures demande d'approbation sont créées pour tous les approbateurs du demandeur jusqu'au et y compris le premier approbateur qualifié.<br />2.  **Approbateur direct** spécifie qu'une écriture de demandes d'approbation n'est créée que pour l'approbateur immédiat du demandeur, quelle que soit la limite d'approbation de l'approbateur.<br />3.  **Premier approbateur qualifié** spécifie qu'une écriture de demandes d'approbation n'est créée que pour le premier approbateur qualifié du demandeur.<br />|  
    3.  Pour spécifier des options pour une réponse de workflow impliquant la création de lignes feuille, renseignez les champs comme indiqué dans le tableau suivant.  

        |Champ|Désignation|  
        |----------------------------------|---------------------------------------|  
        |**Nom du modèle feuille comptabilité**|Spécifiez le nom du modèle feuille comptabilité dans lequel les lignes feuille spécifiées sont créées.|  
        |**Nom feuille comptabilité**|Spécifiez le nom feuille comptabilité dans lequel les lignes feuille spécifiées sont créées.|  

11. Choisissez les boutons **Augmenter le retrait** et **Réduire le retrait** pour mettre en retrait le nom de l'événement dans le champ **Si** pour définir la position de l'étape dans le workflow.  
    1.  Indiquez que l'étape est la suivante dans l'ordre du workflow en mettant en retrait le nom de l'événement sous le nom d'événement de l'étape précédente.  
    2.  Indiquez que l'étape est l'une des étapes alternatives qui peuvent démarrer en fonction de sa condition en plaçant le nom de l'événement à la même indentation que les autres étapes. Classez ces étapes facultatives en fonction de leur priorité en plaçant l'étape la plus importante en premier.  

    > [!NOTE]  
    >  Vous ne pouvez modifier que le retrait d'une étape qui n'a pas d'étape suivante.  

12. Répétez les étapes 7 à 11 pour ajouter d'autres étapes de workflow, avant ou après l'étape que vous venez de créer.  
13. Activez la case à cocher **Activé** pour spécifier que le workflow démarre lorsque l'événement de la première étape de type **Point d'entrée** se produit. Pour plus d'informations, voir [Utilisation des workflows](across-use-workflows.md).  

> [!NOTE]  
>  N'activez pas un workflow tant que vous n'êtes pas sûr qu'il est terminé et que les étapes de workflow concernées peuvent démarrer.  

> [!TIP]  
>  Pour visualiser les relations entre les tables qui sont utilisées dans le flux de travail, choisissez l'icône ![Ampoule qui ouvre la fonction Tell Me](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire"), puis entrez **Flux de travail - Relations de table**.  

## <a name="see-also"></a>Voir aussi  
[Créer des flux de travail à partir de modèles de flux de travail](across-how-to-create-workflows-from-workflow-templates.md)   
[Configurer des utilisateurs d'approbation](across-how-to-set-up-approval-users.md)   
[Configuration de notifications de workflow](across-setting-up-workflow-notifications.md)   
[Afficher des instances d'étape de workflow archivées](across-how-to-view-archived-workflow-step-instances.md)   
[Supprimer des workflows](across-how-to-delete-workflows.md)   
[Procédure pas à pas : Configuration et utilisation d'un flux d'approbation achat](walkthrough-setting-up-and-using-a-purchase-approval-workflow.md)   
[Paramétrage des workflows](across-set-up-workflows.md)   
[Utilisation des workflows](across-use-workflows.md)   
[Flux de travail](across-workflow.md)      
