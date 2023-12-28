---
title: Rapprocher les comptes bancaires à l’aide de l’assistant de rapprochement
description: Découvrez comment utiliser Copilot pour rapprocher les comptes bancaires dans Business Central.
author: jswymer
ms.author: jswymer
ms.reviewer: jswymer
ms.topic: how-to
ms.collection: get-started
ms.date: 10/25/2023
ms.custom: bap-template
---

# <a name="reconcile-bank-accounts-with-copilot-preview"></a>Rapprocher les comptes bancaires avec Copilot (version préliminaire)

[!INCLUDE[production-ready-preview-dynamics365](includes/production-ready-preview-dynamics365.md)]

Cet article explique comment utiliser l’assistance au rapprochement des comptes bancaires pour vous aider à rapprocher les transactions bancaires avec les écritures comptables dans Business Central.

## <a name="about-bank-account-reconciliation-assist"></a>À propos de l’assistant de rapprochement bancaire

L’assistant de rapprochement bancaire est un ensemble de fonctionnalités basées sur l’IA qui vous aident à rapprocher les comptes bancaires. L’assistant de rapprochement bancaire vous propose deux tâches distinctes via Copilot :

- Amélioration de la correspondance des transactions avec les écritures comptables

   Il se peut que vous connaissiez déjà l’action **Faire correspondre automatiquement** sur la page **Rapprochement bancaire** qui fait correspondre automatiquement la plupart des transactions bancaires avec les écritures comptables. Nous appelons cette opération *automatch*. Bien que la correspondance automatique fonctionne bien, les algorithmes utilisés peuvent parfois aboutir à de nombreuses transactions sans correspondance. Copilot utilise la technologie d’IA pour inspecter les transactions restantes et identifier davantage de correspondances, en fonction des dates, des montants et des descriptions. Par exemple, si plusieurs factures ont été payées en une seule fois par un client, Copilot rapproche la ligne de relevé bancaire unique avec les multiples écritures comptables des factures.
   
   Accédez à [Rapprocher les comptes bancaires avec Copilot](#reconcile-bank-accounts-with-copilot).

- Comptes généraux suggérés

  Pour les transactions bancaires résiduelles qui n’ont pu être mises en correspondance avec aucune écriture du grand livre, Copilot utilise la technologie d’IA pour comparer la description de la transaction avec les noms des comptes généraux, suggérant le compte général le plus probable pour effectuer la validation. Par exemple, Copilot pourrait suggérer que les transactions avec le descriptif « Fuel Stop24 » soient validées dans le compte « Transport ».
  
   Accédez à [Transférer les transactions bancaires sans correspondance vers les comptes généraux suggérés](#transfer-unmatched-bank-transactions-to-suggested-general-ledger-accounts).


   
## <a name="prerequisites"></a>Conditions préalables

- L’assistance au rapprochement des comptes bancaires est activée. Cette tâche est effectuée par un administrateur. [En savoir plus sur l’activation des fonctionnalités Copilot et IA](enable-ai.md).
- Les comptes bancaires dans Business Central que vous souhaitez rapprocher sont liés à un compte bancaire en ligne ou configurés avec un format d’importation de relevé bancaire. 
- Vous êtes familier avec le rapprochement des comptes bancaires dans Business Central, comme décrit dans [Rapprocher les comptes bancaires](bank-how-reconcile-bank-accounts-separately.md). 

<!--H2s. Required. A how-to article explains how to do a task. The bulk of each H2 should be a procedure.-->
## <a name="reconcile-bank-accounts-with-copilot"></a>Rapprocher les comptes bancaires avec Copilot

<!-- Similar to the **Match Automatically** capability on the **Bank Acc. Reconciliation** page, Bank account reconciliation assist can also automatically matches transactions in banks statements with bank entries. The difference is that **Match Automatically** uses a native rules-based algorithm, while Bank account reconciliation assist is based AI technology though Copilot. Bank account reconciliation assist is intended to supplement the **Match Automatically** capability. While **Match Automatically** is fairly successful at matching transactions, there are some instances where it can't&mdash;which is where Bank account reconciliation assist comes. By using the **Reconcile with Copilot** action on **Bank Acc. Reconciliation** page, you can find even more matches.-->

Copilot dans le rapprochement des comptes bancaires est destiné à être utilisé en complément de l’opération de rapprochement automatique. Pour cette raison, lorsque vous utilisez Copilot, l’opération de correspondance automatique s’exécute en premier pour effectuer les correspondances initiales. Ensuite, Copilot s’exécute pour tenter de faire correspondre les transactions que l’opération de correspondance automatique n’a pas gérées.   

Il existe deux approches pour rapprocher les comptes bancaires avec Copilot. Vous pouvez utiliser Copilot pour lancer un nouveau rapprochement sur un compte bancaire, directement depuis la liste **Rapprochement des comptes bancaires**, ou vous pouvez utiliser Copilot sur un rapprochement nouveau ou existant sur la carte **Rapprochement bancaire**.

# [À partir de la liste Rapprochement de comptes bancaires](#tab/fromlist) 

Avec cette approche, vous créez un rapprochement de compte bancaire à partir de zéro. Cette approche nécessite de sélectionner le compte bancaire et d’importer le fichier de relevé bancaire, si le compte bancaire n’est pas lié à un compte en ligne.

1. Sélectionnez l’icône ![Ampoule qui ouvre la fenêtre de recherche.](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire") entrez **Rapprochements bancaires**, puis sélectionnez le lien associé. 
1. Sélectionnez l’action **Rapprocher avec Copilot** pour ouvrir la fenêtre **Rapprocher avec Copilot**.
1. Définissez le champ **Effectuer un rapprochement pour ce compte bancaire** sur le compte bancaire que vous souhaitez rapprocher.

   ![Affiche la fenêtre de rapprochement avec copilote pour un rapprochement à partir de zéro](media/reconcile-bank-accounts-new-copilot.svg) 
 
1. Si le compte bancaire sélectionné n’est pas lié à un compte bancaire en ligne, vous devez importer le fichier de relevés bancaires. Pour importer le fichier, sélectionnez la valeur dans le champ **Utiliser les données de transaction à partir de** ou sélectionnez le bouton du trombone en regard du bouton **Générer**. Ensuite, utilisez **Sélectionner le fichier à importer** pour importer le fichier de relevé bancaire en le faisant glisser depuis votre appareil ou en parcourant votre appareil.
1. Pour effectuer un rapprochement avec Copilot, sélectionnez **Générer**.

   Copilot commence à générer des correspondances proposées. Une fois l’opération terminée, la fenêtre Rapprocher avec Copilot ouvre les résultats du processus de mise en correspondance.

1. Passez en revue les correspondances proposées comme décrit dans la section suivante.

# [À partir d’une carte de rapprochement bancaire](#tab/fromcard) 

Avec cette approche, vous utilisez Copilot soit sur un nouveau rapprochement de compte bancaire que vous créez manuellement, soit en modifiant un rapprochement existant. 


1. Sélectionnez l’icône ![Ampoule qui ouvre la fenêtre de recherche.](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire") entrez **Rapprochements bancaires**, puis sélectionnez le lien associé. 
1. Exécutez l’une des étapes suivantes :

   - Sélectionnez **Nouveau** pour démarrer un nouveau rapprochement. 
   - Sélectionnez et ouvrez un rapprochement existant dans la liste.
1. Dans la carte **Rapprochement bancaire**, sélectionnez **Rapprocher avec Copilot**

   ![Affiche le rapprochement avec l’action copilote sur la carte Rapprochement bancaire](media/bank-reconciliation-copilot-card.svg) 

   Copilot commence à générer des correspondances proposées. Une fois l’opération terminée, la fenêtre **Rapprocher avec Copilot** ouvre les résultats du processus de mise en correspondance. 

1. Passez en revue les correspondances proposées comme décrit dans la section suivante. 
---

### <a name="review-save-or-discard-proposed-matches"></a>Examiner, enregistrer ou supprimer les correspondances proposées

Après avoir exécuté Copilot, la fenêtre **Rapprocher avec Copilot** affiche les résultats détaillés, y compris les correspondances proposées. À ce stade, aucune correspondance proposée par Copilot n’a été enregistrée, cela vous donne donc la possibilité d’inspecter les propositions et de les enregistrer ou de les supprimer à votre guise.

![Affiche la fenêtre de rapprochement avec copilote avec les correspondances proposées](media/bank-reconciliation-copilot-window.png) 

La fenêtre Copilot est divisée en deux sections. La section supérieure fournit des détails généraux sur le résultat, comme décrit dans le tableau suivant.  La section inférieure **Proposition correspondante** répertorie les correspondances suggérées par Copilot.

|Champ|Désignation|
|-|-|
|Correspondance automatique|Spécifie le nombre de lignes dans le relevé bancaire mises en correspondance par l’opération de mise en correspondance automatique. Sélectionnez la valeur pour afficher la carte de rapprochement.  |
|Copilot mis en correspondance|Spécifie le nombre de lignes dans le relevé bancaire ayant des mises en correspondance proposées par Copilot. Vous pouvez afficher les détails des correspondances dans la section **Correspondances proposées**.|
|Solde final du relevé|Spécifie le solde final indiqué sur le relevé bancaire à rapprocher avec le compte bancaire|
|Valider si lettré intégralement|Activez ce commutateur si vous souhaitez valider automatiquement le rapprochement du compte bancaire lorsque toutes les lignes (100 %) correspondent et que vous avez sélectionné **Conserver**.|

#### <a name="save-or-discard-proposed-matches"></a>Enregistrer ou supprimer les correspondances proposées

Dans la section **Propositions correspondantes**, examinez les correspondances suggérées ligne par ligne, puis effectuez l’action appropriée :

- Pour ignorer une seule correspondance proposée, sélectionnez-la dans la liste, puis sélectionnez l’action **Supprimer la ligne**.

- Pour ignorer toutes les correspondances proposées et fermer la fenêtre Copilot, sélectionnez le bouton Supprimer (corbeille) ![Affiche l’icône de la corbeille pour supprimer toutes les propositions Copilot pour le rapprochement des comptes bancaires](media/copilot-delete-trash-can.png) en regard du bouton **Conserver** en bas de la fenêtre.

- Pour valider automatiquement le rapprochement complet lorsque vous l’enregistrez, activez le commutateur **Valider si entièrement appliqué**.  
- Pour enregistrer les correspondances actuellement affichées dans la fenêtre Copilot, sélectionnez **Conserver**.


## <a name="transfer-unmatched-bank-transactions-to-suggested-general-ledger-accounts"></a>Transférer les transactions bancaires sans correspondance vers les comptes généraux suggérés

Dans cette section, vous apprendrez à utiliser Copilot pour transférer des relevés de compte bancaire non rapprochés du grand livre du compte bancaire vers un compte du grand livre. Cette tâche ne peut être effectuée qu’à partir d’un rapprochement existant. 

1. Accédez à la liste des **Rapprochements de comptes bancaires** et ouvrez le rapprochement existant qui inclut les lignes non rapprochées.

   Commencez par ouvrir un rapprochement de compte bancaire existant. Cette étape vous offre une vue claire de toutes les lignes de relevé bancaire non rapprochées qui doivent être transférées vers le compte général.

2. Dans le volet **Lignes de relevé bancaire**, identifiez le volet des lignes de relevé bancaire sans correspondance et sélectionnez une ou plusieurs lignes que vous souhaitez rapprocher.

   Ces lignes sont les lignes de relevé sur lesquelles Copilot se concentre pour le transfert vers le compte général.

3. Sélectionnez **Transfert vers le compte général** pour démarrer le processus.

   ![Affiche le transfert vers le compte général avec l’action copilote sur la carte Rapprochement bancaire](media/bank-reconciliation-transfer-gl-copilot-card.svg) 

   Cette étape invite Copilot à commencer à générer des propositions pour le transfert.

4. Une fois que Copilot a fini de générer des propositions, la fenêtre **Propositions de transfert de compte général Copilot** s’ouvre.

   Cette fenêtre affiche les propositions dans la section **Proposition correspondante**. L’expérience est similaire au rapprochement avec Copilot.

   ![Affiche le transfert vers le compte général avec la page de correspondances proposées par copilote pour le rapprochement des comptes bancaires](media/bank-reconciliation-gl-transfer-proposed-matches.png) 

5. Examinez chaque proposition ligne par ligne pour garantir l’exactitude des transferts suggérés.

   - Si vous explorez la proposition en la sélectionnant dans la liste, vous êtes redirigé vers une liste de comptes. De là, vous pouvez choisir un autre compte. Ce type de correction manuelle n’est possible que lors de l’utilisation du flux **Transfert vers le compte général**, et non dans le flux de rapprochement. 
   - Si vous sélectionnez **Enregistrer...** en regard d’une proposition, vous pouvez ajouter le mappage à la page **Mappage de texte à compte** afin que la prochaine fois où ce texte s’affichera lors de la mise en correspondance, il sera mappé au compte proposé.

6. Supprimez ou enregistrez les propositions.

   - Si vous souhaitez ignorer une proposition spécifique, sélectionnez-la dans la liste, puis sélectionnez **Supprimer la ligne**. Pour ignorer toutes les propositions et quitter Copilot, sélectionnez le bouton Supprimer (corbeille) ![Affiche l’icône de la corbeille pour supprimer toutes les propositions Copilot pour le rapprochement des comptes bancaires](media/copilot-delete-trash-can.png) en regard du bouton **Conserver** en bas de la fenêtre.
   
   - Si les propositions répondent à vos exigences et que vous souhaitez les enregistrer, sélectionnez **Conserver**. 

      Cette étape confirme le transfert des propositions actuellement sélectionnées du grand livre du compte bancaire vers le compte général. Elle valide les nouveaux paiements sur les comptes généraux proposés et applique les lignes correspondantes aux écritures comptables du compte bancaire qui en résultent.

## <a name="next-steps"></a>Étapes suivantes

[Valider votre rapprochement bancaire](bank-how-reconcile-bank-accounts-separately.md#validate-your-bank-reconciliation)  

## <a name="see-also"></a>Voir aussi
[Résoudre les problèmes des fonctionnalités de Copilot et d’IA](ai-copilot-troubleshooting.md)  
[FAQ sur l’IA responsable pour l’assistance au rapprochement bancaire](faqs-bank-reconciliation.md)  
[Paramétrage des opérations bancaires](bank-setup-banking.md)  
[Rapprochement des comptes bancaires](bank-how-reconcile-bank-accounts-separately.md)  
[Lettrage automatique des paiements et rapprochement des comptes bancaires](receivables-apply-payments-auto-reconcile-bank-accounts.md) 
