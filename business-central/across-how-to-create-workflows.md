---
title: Créer des flux de travail approbation pour connecter des tâches
description: Découvrez comment créer des flux de travail qui connectent des tâches exécutées par différentes personnes dans les processus entreprise.
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bholtorf
ms.topic: how-to
ms.date: 04/24/2023
ms.custom: bap-template
---
# <a name="create-workflows-to-connect-tasks-in-business-processes"></a><a name="create-workflows-to-connect-tasks-in-business-processes"></a>Créer des flux de travail pour connecter des tâches aux processus entreprise

Vous pouvez créer des flux de travail qui connectent des tâches aux processus entreprise exécutées par différents utilisateurs. Vous pouvez inclure des tâches système, telles que la validation automatique, comme étapes du flux de travail qui sont précédées ou suivies des tâches de l’utilisateur. Demander et accorder une approbation pour créer des enregistrements sont des étapes classiques du flux de travail.  

Sur la page **Flux de travail**, créez un flux de travail en répertoriant les étapes sur les lignes. Chaque étape comprend un déclencheur et une réponse :

* Un événement qui spécifie les conditions qui démarrent le flux de travail.
* Une réponse du flux de travail qui définit ce que fait le flux de travail.

[!INCLUDE[workflow](includes/workflow.md)]

Lorsque vous créez des flux de travail, vous pouvez copier les étapes à partir de flux de travail existants ou de modèles de flux de travail. Les modèles de flux de travail sont des flux de travail non modifiables fournis par [!INCLUDE[prod_short](includes/prod_short.md)]. Les identifiants des modèles de flux de travail ont le préfixe « MS- », comme dans « MS-PIW ». En savoir plus sur [Créer des flux de travail à partir de modèles de flux de travail](across-how-to-create-workflows-from-workflow-templates.md).  

> [!NOTE]  
> Toutes les notifications relatives aux étapes du flux de travail sont envoyées à l’aide d’une file projets. Veillez à ce que la file d’attente de tâches reflète les besoins de votre entreprise. Pour plus d’informations, voir [Utiliser des files d’attente des travaux pour planifier des tâches](admin-job-queues-schedule-tasks.md).  

:::image type="content" source="media/Workflows/workflow-example.png" alt-text="Illustration d’un exemple de flux de travail.":::

Un flux de travail est divisé en trois sections :

1. **En cas d'événement**  
   C’est là que le déclencheur est sélectionné.  
   Des exemples de déclencheur :
   * Un enregistrement de données de base est modifié
   * Une ligne feuille est créée
   * Un document entrant est créé ou lancé
   * L’approbation d’un document est exigée
2. **Condition**  
   Les **conditions** sont liées à l’événement et permettent de créer des filtres pour décider de la suite du flux de travail.
3. **Alors, réponse**  
   Les **réponses** spécifient les prochaines étapes du flux de travail.

Les options pour les événements et les réponses sont définies par le système. Pour ajouter de nouvelles options, vous devrez développer une extension.

## <a name="to-create-a-workflow"></a><a name="to-create-a-workflow"></a>Pour créer un flux de travail

1. Sélectionnez ![l’icône en forme d’Ampoule qui ouvre la fenêtre de recherche](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire"),  entrez **Flux de travail**, puis choisissez le lien associé.  
2. Sélectionnez l’action **Nouveau**. La page **Flux de travail** s’ouvre.  
3. Dans le champ **Code**, entrez 20 caractères maximum pour identifier le flux de travail.  
4. Pour créer le flux de travail à partir d’un modèle de flux de travail, dans la page **Flux de travail**, choisissez l’action **Créer le flux de travail à partir du modèle**. En savoir plus sur [Créer des flux de travail à partir de modèles de flux de travail](across-how-to-create-workflows-from-workflow-templates.md).  
5. Dans le champ **Description**, décrivez le flux de travail.  
6. Dans le champ **Catégorie**, spécifiez la catégorie à laquelle le flux de travail appartient.  
7. Dans le champ **En cas d’événement**, spécifiez l’événement qui doit se produire pour démarrer l’étape du flux de travail.  

   Lorsque vous choisissez le champ, la page **Événements du flux de travail** répertorie tous les événements disponibles du flux de travail.  
8. Dans le champ **Condition**, spécifiez une ou plusieurs conditions qui doivent être remplies pour que l’événement dans le champ **En cas d’événement** puisse se produire.  

   Lorsque vous choisissez le champ, la page **Conditions de l’événement** répertorie les champs de filtre qui peuvent être des conditions pour l’événement. Vous pouvez ajouter de nouveaux champs de filtre si vous le souhaitez.  

   Si l’événement du flux de travail est la modification d’un champ spécifique d’un enregistrement, utilisez la page **Conditions de l’événement** pour sélectionner le champ et le type de modification.  

   1. Pour spécifier une modification de champ pour l’événement, sur la page **Conditions d’événement**, dans le champ **Champ**, sélectionnez le champ qui est modifié.  
   2. Dans le champ **Opérateur**, sélectionnez **Diminué**, **Augmenté** ou **Modifié**.  
9. Dans le champ **Alors, réponse**, spécifiez la réponse qui suivra lorsque l’événement de flux de travail se produira.  

   Lorsque vous choisissez le champ, la page **Réponses du flux de travail** répertorie toutes les réponses du flux de travail et toutes les options de réponse disponibles.  
10. Dans le raccourci **Options pour la réponse sélectionnée**, spécifiez les options pour la réponse de flux de travail, en sélectionnant des valeurs dans les différents champs qui s’affichent, comme suit :  

    1. Pour spécifier des options pour une réponse de flux de travail impliquant l’envoi d’une notification, renseignez les champs comme indiqué dans le tableau suivant.  

    > [!NOTE]
    > Ces champs varient en fonction de la réponse que vous avez choisie.

       |Champ|Désignation|
       |-----|-----------|
       |**Notifier l'expéditeur**|Spécifiez si le demandeur de l’approbation doit être notifié au lieu du destinataire de la demande d’approbation. Si vous cochez la case, le champ **ID utilisateur du destinataire** est désactivé, car le demandeur de l’approbation, c’est-à-dire l’expéditeur, est notifié à la place. Le nom de la réponse du flux de travail est modifié en conséquence, en **Créer une notification pour &lt;Expéditeur&gt;**. Si la case n’est pas cochée, le nom de la réponse du flux de travail est **Créer une notification pour &lt;Utilisateur&gt;**.|
       |**Code utilisateur du destinataire**|Spécifiez l’utilisateur auquel la notification doit être envoyée. **Remarque** : cette option n’est disponible que pour les réponses de flux de travail avec un espace réservé pour un utilisateur spécifique. Pour les réponses de flux de travail sans espaces réservés pour les utilisateurs, le destinataire de la notification est généralement défini par les **Paramètres utilisateur approbation**.|
       |**Type écriture notification**|Spécifiez un déclencheur pour la notification du flux de travail. Le déclencheur peut être une modification d’enregistrement, une demande d’approbation ou une date d’échéance dépassée.|
       |**Page cible du lien**|Spécifiez la page que le lien dans la notification ouvre. La page doit avoir la même table source que l’enregistrement impliqué.|
       |**Lien personnalisé**|Spécifiez l’URL d’un lien qui est inclus dans la notification en complément du lien vers la page.|

    2. Pour spécifier des options pour une réponse de flux de travail impliquant la création d’une demande d’approbation, renseignez les champs comme indiqué dans le tableau suivant.  

       |Champ|Désignation|  
       |-----|-----------|  
       |**Formule échéance**|Spécifiez le nombre de jours dont dispose l’approbateur pour résoudre la demande. La période commence lorsque la demande est envoyée.|
       |**Déléguer après**|Spécifiez si et quand une demande d’approbation est automatiquement déléguée au remplaçant. Vous pouvez choisir de déléguer automatiquement un, deux ou cinq jours après la date de demande d’approbation.|
       |**Type approbateur**|Spécifiez l’approbateur, en fonction des paramètres des utilisateurs d’approbation et de flux de travail. Lorsque le champ est défini sur **Vendeur/Acheteur**, l’utilisateur spécifié dans le champ **Code vendeur/acheteur** sur la page **Paramètres utilisateur approbation** détermine l’approbateur. Les écritures de demande d’approbation sont ensuite créées en fonction de la valeur du champ **Type limite approbateur**. En savoir plus sur [Configurer des utilisateurs d’approbation](across-how-to-set-up-workflow-users.md).|
       |**Afficher le message de confirmation**|Spécifiez si un message de confirmation doit s’afficher après une demande d’approbation d’un utilisateur.|
       |**Type limite approbateur**|Spécifiez l’effet des limites pour les approbateurs. La limite d’approbation d’un approbateur doit être supérieure à la valeur de la demande. Les options possibles sont les suivantes : <ol><li>**Chaîne d’approbateurs** spécifie que les écritures demande d’approbation sont créées pour tous les approbateurs du demandeur jusqu’au et y compris le premier approbateur qualifié.</li><li>**Approbateur direct** spécifie qu’une écriture de demandes d’approbation n’est créée que pour l’approbateur immédiat du demandeur, quelle que soit la limite d’approbation de l’approbateur.</li><li>**Premier approbateur qualifié** spécifie qu’une écriture de demande d’approbation n’est créée que pour le premier approbateur du demandeur.</li><li>**Approbateur spécifique** indique que vous avertissez l’utilisateur choisi dans le champ **ID approbateur**.</li></ol>|

    3. Pour spécifier des options pour une réponse du flux de travail impliquant la création de lignes feuille, renseignez les champs comme indiqué dans le tableau suivant.  

       |Champ|Désignation|  
       |-----|-----------|  
       |**Nom du modèle feuille comptabilité**|Spécifiez le nom du modèle feuille comptabilité dans lequel les lignes feuille spécifiées sont créées.|  
       |**Nom feuille comptabilité**|Spécifiez le nom feuille comptabilité dans lequel les lignes feuille spécifiées sont créées.|  

11. Choisissez les boutons **Augmenter le retrait** et **Réduire le retrait** pour mettre en retrait le nom de l’événement dans le champ **Si** pour définir la position de l’étape dans le flux de travail.  

    1. Mettez en retrait l’événement sous le nom de l’étape précédente pour indiquer qu’il s’agit de l’étape suivante.  
    2. Indiquez que l’étape est l’une des étapes alternatives qui peuvent démarrer en fonction de sa condition en plaçant le nom de l’événement à la même indentation que les autres étapes. Classez ces étapes facultatives en fonction de leur priorité en plaçant l’étape la plus importante en premier.  

    > [!NOTE]  
    >  Vous ne pouvez modifier que le retrait d’une étape qui n’a pas d’étape suivante.  

12. Répétez les étapes 7 à 11 pour ajouter d’autres étapes de flux de travail, avant ou après l’étape que vous avez créée.  
13. Activez le bouton bascule **Activé** pour spécifier que le flux de travail démarre lorsque l’événement de la première étape de type **Point d’entrée** se produit. En savoir plus sur [Utiliser des flux de travail](across-use-workflows.md).  

> [!NOTE]  
> N’activez un flux de travail que lorsque vous êtes sûr qu’il est prêt.  

> [!TIP]  
> Pour explorer les relations entre les tables utilisées dans les flux de travail, choisissez l’icône ![Ampoule qui ouvre la fenêtre de recherche.](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire") puis entrez **Flux de travail - Relations de table**.  

## <a name="example-of-creating-a-new-workflow-using-existing-events"></a><a name="example-of-creating-a-new-workflow-using-existing-events"></a>Exemple de création d’un nouveau flux de travail à l’aide d’événements existants

L’exemple suivant crée un flux de travail pour approuver une modification du nom d’un fournisseur :

1. Sélectionnez ![l’icône en forme d’Ampoule qui ouvre la fenêtre de recherche](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire"), entrez **Flux de travail**, puis choisissez le lien associé.  
2. Sélectionnez l’action **Nouveau**. La page **Flux de travail** s’ouvre.
3. Dans la section Flux de travail, renseignez les champs requis comme indiqué dans le tableau suivant.

    |Champ  |Valeur  |
    |---------|---------|
    |**Code**|**VENDAPN-01**|
    |**Description**|**Approbation du changement de nom du fournisseur** |
    |**Catégorie**|**ACHATS**|

4. Pour créer la première étape du flux de travail, procédez comme suit.

    1. Dans le champ **En cas d’événement**, précisez *Un enregistrement fournisseur a été modifié*.  
    2. Dans le champ **Condition**, laissez la valeur définie sur **Toujours**. Dans le champ **Conditions d’événement**, choisissez le lien **Ajoutez une condition au cas où une valeur de champ serait modifiée**, puis sélectionnez le champ **Nom**. Le résultat de cette étape est que la condition se lit comme *Le nom a changé*.  
    3. Dans le champ **Alors, réponse**, choisissez le lien **Sélectionner la réponse**. Puis, sur la page **Réponses de flux de travail**, dans le champ **Sélectionner la réponse**, choisissez le champ **Rétablir la valeur de \<Field\> sur l’enregistrement et enregistrer la réponse de modification**. Puis, dans la section **Options pour la réponse sélectionnée**, spécifiez le champ **Nom**.  
    4. Choisissez le lien **Ajouter d’autres réponses**, puis ajoutez une entrée pour la réponse **Créer une demande d’approbation pour l’enregistrement à l’aide du type approbateur <%1> et <%2>**.  
    5. Dans la section **Options pour la réponse sélectionnée** pour la nouvelle réponse, modifiez le champ **Type d’approbateur** en **Groupe d’utilisateurs du flux de travail**. Ensuite, dans le champ **Groupe d’utilisateurs du flux de travail**, spécifiez le groupe d’utilisateurs. En savoir plus sur [Configurer des utilisateurs d’approbation](across-how-to-set-up-approval-users.md).  
    6. Ajoutez une troisième réponse, **Envoyer une demande d’approbation pour l’enregistrement et créer une notification**.  
    7. Ajoutez une quatrième réponse, **Afficher le message « %1 »**. Ensuite, dans la section **Options pour la réponse sélectionnée**, dans le champ **Message**, spécifiez **Une demande d’approbation a été envoyée**.  
    8. Cliquez sur le bouton **OK** pour revenir à l’étape du flux de travail.  

5. Sur la ligne suivante, ajoutez une nouvelle étape de flux de travail pour l’événement **Une demande d’approbation est approuvée**.

    1. Dans le champ **En cas d’événement**, précisez **Une demande d’approbation est approuvée**.  
    2. Choisissez le menu en ligne, puis choisissez **Augmenter le retrait**.  
    3. Dans le champ **Condition**, choisissez **Toujours**. Ensuite, dans le champ **Approbations en attente**, spécifiez **0**. La condition se lit comme **Approbations en attente : 0** pour indiquer que la demande ne nécessite pas d’autres approbateurs.  
    4. Dans le champ **Alors, réponse**, choisissez le lien **Sélectionner la réponse**. Puis, sur la page **Réponses de flux de travail**, dans le champ **Sélectionner la réponse**, choisissez la réponse **Envoyer une demande d’approbation pour l’enregistrement et créer une notification**.  
    5. Cliquez sur **OK**.  
6. Sur la ligne suivante, ajoutez une deuxième étape de flux de travail pour l’événement **Une demande d’approbation est approuvée**.  

    1. Dans le champ **En cas d’événement**, précisez **Une demande d’approbation est approuvée**.
    2. Dans le champ **Condition**, choisissez **Toujours**. Ensuite, dans le champ **Approbations en attente**, spécifiez **>0**. La condition se lit comme **Approbations en attente : >0** pour indiquer qu’il ne s’agit pas du dernier approbateur.  
    3. Dans le champ **Alors, réponse**, choisissez le lien **Sélectionner la réponse**. Puis, sur la page **Réponses de flux de travail**, dans le champ **Sélectionner la réponse**, choisissez la réponse **Envoyer une demande d’approbation pour l’enregistrement et créer une notification**.  
    4. Cliquez sur **OK**.  
7. Sur la ligne suivante, ajoutez une deuxième étape de flux de travail pour l’événement **Une demande d’approbation est déléguée**.  

    1. Dans le champ **En cas d’événement**, précisez **Une demande d’approbation est déléguée**.  
    2. Dans le champ **Condition**, laissez la valeur définie sur **Toujours**.  
    3. Dans le champ **Alors, réponse**, choisissez le lien **Sélectionner la réponse**. Puis, sur la page **Réponses de flux de travail**, dans le champ **Sélectionner la réponse**, choisissez la réponse **Envoyer une demande d’approbation pour l’enregistrement et créer une notification**.  
    4. Cliquez sur **OK**.  
8. Sur la ligne suivante, ajoutez une deuxième étape de flux de travail pour l’événement **Une demande d’approbation est rejetée**.  

    1. Dans le champ **En cas d’événement**, précisez **Une demande d’approbation est rejetée**.  
    2. Dans le champ **Condition**, laissez la valeur définie sur **Toujours**.  
    3. Dans le champ **Alors, réponse**, choisissez le lien **Sélectionner la réponse**. Ensuite, sur la page **Réponses de flux de travail**, dans le champ **Sélectionner la réponse**, choisissez la réponse **Ignorer les nouvelles valeurs**.  
    4. Choisissez le lien **Ajouter d’autres réponses**, puis ajoutez une entrée pour la réponse **Rejeter la demande d’approbation pour l’enregistrement et créer une notification**.
    5. Cliquez sur **OK**.  
9. Pour activer le flux de travail, activez le bouton à bascule **Activé**.  

L’illustration suivante donne un aperçu du résultat de cette procédure.  

:::image type="content" source="media/Workflows/workflow-example-2.png" alt-text="Illustration du flux de travail Approbation du nom du fournisseur.":::

Ensuite, testez le flux de travail en ouvrant une fiche fournisseur existante et en changeant son nom. Vérifiez qu’une demande d’approbation est envoyée après la modification du nom du fournisseur.

## <a name="see-related-microsoft-training"></a><a name="see-related-microsoft-training"></a>Voir la [formation Microsoft](/training/modules/create-workflows/) associée

## <a name="see-also"></a><a name="see-also"></a>Voir aussi

[Créer des flux de travail à partir de modèles de flux de travail](across-how-to-create-workflows-from-workflow-templates.md)  
[Configurer des utilisateurs d’approbation](across-how-to-set-up-approval-users.md)  
[Configuration de notifications de flux de travail approbation](across-setting-up-workflow-notifications.md)  
[Afficher des instances d’étape de flux de travail archivées](across-how-to-view-archived-workflow-step-instances.md)  
[Suppression des flux d’approbation](across-how-to-delete-workflows.md)  
[Procédure pas à pas : Configuration et utilisation d’un flux d’approbation d’achat](walkthrough-setting-up-and-using-a-purchase-approval-workflow.md)  
[Configurer les flux de travail approbation](across-set-up-workflows.md)  
[Utilisation des flux d’approbation](across-use-workflows.md)  
[Flux de travail](across-workflow.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
