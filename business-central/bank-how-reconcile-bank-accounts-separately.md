---
title: Rapprochement des comptes bancaires
description: Découvrez comment rapprocher les transactions dans Business Central avec les transactions dans les relevés de votre banque.
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bholtorf
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.date: 10/04/2023
ms.custom: bap-template
---
# Rapprochement des comptes bancaires

Le rapprochement bancaire permet de s’assurer que ce qui se trouve dans vos livres correspond aux relevés que vous recevez de votre banque. Le rapprochement des comptes bancaires compare et fait correspondre les écritures des comptes bancaires que vous avez configurées dans [!INCLUDE[prod_short](includes/prod_short.md)] avec les transactions bancaires au niveau de votre banque. Le rapprochement peut ensuite reporter les soldes sur vos comptes bancaires dans [!INCLUDE[prod_short](includes/prod_short.md)] pour les mettre à la disposition des responsables financiers. Le rapprochement bancaire est également un moyen pratique de découvrir et de résoudre les paiements manquants et les erreurs de comptabilité.

Cet article décrit comment rapprocher les comptes bancaires à partir de la page **Rapprochement bancaire**.

Cependant, vous pouvez également rapprocher des comptes bancaires sur la page **Feuille rapprochement bancaire** lorsque vous traitez les paiements. Les écritures comptables compte bancaire ouvertes associées au client lettré ou à des écritures comptables fournisseur sont clôturées lorsque vous sélectionnez l’action **Valider les paiements et rapprocher les comptes bancaires**. Cela rapproche automatiquement le compte bancaire pour les paiements que vous validez avec le journal. Pour plus d’informations, reportez-vous à [Lettrage automatique des paiements et rapprochement des comptes bancaires](receivables-apply-payments-auto-reconcile-bank-accounts.md).

> [!NOTE]  
> Dans les versions nord-américaines, vous pouvez également effectuer cette tâche sur la page **Feuille rapprochement bancaire**, qui est mieux adaptée pour les chèques et les acomptes, mais ne vous permet pas d’importer des fichiers de relevé bancaire. Pour utiliser cette page à la place de la page **Rapprochement bancaire**, effacez le champ **Rapprochement bancaire avec correspondance auto.** sur la page **Paramètres comptabilité**. Pour plus d’informations, voir [Rapprocher des comptes bancaires](LocalFunctionality/UnitedStates/how-to-reconcile-bank-accounts.md) sous Fonctionnalité locale, États-Unis.

Les lignes de la page **Rapprochement bancaire** sont réparties sur deux volets. Le volet **Lignes relevé bancaire** indique le volet des transactions bancaires importées ou les écritures comptables comportant des arriérés de paiement. Le volet **Écritures comptables compte bancaire** affiche les écritures comptables dans le compte bancaire interne.

Le rapprochement des transactions dans les relevés de votre banque avec les écritures bancaires dans [!INCLUDE[prod_short](includes/prod_short.md)] est appelé *correspondance*. Il existe deux façons de faire correspondre les transactions avec les opérations bancaires :

* Automatiquement, à l’aide de l’action **Faire correspondre automatiquement**.
* Manuellement en sélectionnant des lignes dans les deux volets pour lier chaque ligne relevé bancaire à une ou plusieurs écritures comptables compte bancaire correspondantes, puis utiliser l’action **Faire correspondre manuellement**.

La case **Lettré** est cochée sur les lignes pour lesquelles les écritures correspondent. Pour plus d’informations, voir [Définir des règles pour le lettrage automatique des paiements](receivables-how-set-up-payment-application-rules.md). Si vous saisissez une date de fin de relevé sur le rapprochement bancaire après avoir rapproché ses lignes avec des écritures, [!INCLUDE [prod_short](includes/prod_short.md)] annulera les correspondances pour les lignes et les écritures postérieures à cette date.

> [!NOTE]
> Une fois que vous avez saisi une date dans le champ **Date du relevé**, la page **Rapprochement bancaire** filtre les écritures comptables bancaires pour n’afficher que les écritures jusqu’à cette date. Vous ne pouvez publier que des rapprochements bancaires avec des écritures bancaires au plus tard à la date de fin du relevé. Le filtre garantit que votre registre bancaire est équilibré avec votre relevé bancaire à la date de fin du relevé, la différence étant les paiements et les chèques en attente.

Lorsque la valeur du champ **Solde final** du volet **Lignes relevé bancaire** est égale à la valeur du champ **Solde à simuler** du volet ainsi que le champ **Solde dernier relevé** du volet **Écritures comptables compte bancaire**, vous pouvez sélectionner l’action **Valider**. Toutes les écritures comptables de compte bancaire sans correspondance resteront sur la page, indiquant les différences que vous devez résoudre pour rapprocher le compte bancaire.

Toutes les lignes qui ne peuvent pas être mises en correspondance, indiquées par une valeur dans le champ **Différence**, resteront sur la page **Rapprochement bancaire** après validation. Elles représentent une certaine forme de différence que vous devez résoudre avant de pouvoir effectuer le rapprochement des comptes bancaires. Le tableau suivant décrit quelques situations commerciales typiques qui peuvent entraîner des différences.

| Différence | Motif | Résolution |
|------------|--------|------------|
| Une transaction dans votre compte bancaire dans [!INCLUDE[prod_short](includes/prod_short.md)] ne figure pas sur le relevé bancaire. | La transaction bancaire n’a pas été créée alors qu’une validation a été effectuée dans [!INCLUDE[prod_short](includes/prod_short.md)]. | Créez la transaction manquante (ou demandez à un débiteur de la faire). Réimportez ensuite le fichier de relevé de compte ou saisissez la transaction manuellement. |
| Une transaction sur le relevé bancaire n’existe pas en tant que ligne feuille ou document dans [!INCLUDE[prod_short](includes/prod_short.md)]. | Une transaction bancaire a été effectuée sans validation correspondante dans [!INCLUDE[prod_short](includes/prod_short.md)], par exemple la validation d’une ligne feuille pour une dépense. | Créez et validez l’écriture manquante. Pour apprendre un moyen rapide de lancer cette opération, consultez [Pour créer des écritures comptables manquantes avec lesquelles faire correspondre des transactions bancaires](bank-how-reconcile-bank-accounts-separately.md#to-create-missing-ledger-entries-to-match-bank-statement-lines). |
| Une transaction dans le compte bancaire interne correspond à une transaction bancaire, mais certaines informations sont trop différentes pour établir une correspondance. | Des informations, telles que le montant ou le nom du client, ont été saisies différemment dans la transaction bancaire et la validation interne. | Vérifiez les informations, puis faites les correspondre manuellement. Corrigez éventuellement la non-concordance des informations. |

Vous devez corriger les différences, par exemple en créant des écritures manquantes et en corrigeant les informations qui ne correspondent pas, ou en effectuant les transactions d’argent qui n’ont pas eu lieu, jusqu’à ce que le rapprochement du compte bancaire soit terminé et validé.

Vous pouvez renseigner le volet **Lignes relevé bancaire** de la page **Rapprochement bancaire** des manières suivantes :

* Automatiquement, à l’aide de la fonction **Importer le relevé bancaire** pour renseigner le volet **Lignes relevé bancaire** avec des transactions bancaires en fonction d’un flux ou d’un fichier importé fourni par la banque.
* Manuellement, en utilisant la fonction **Proposer lignes** pour renseigner le volet **Lignes relevé bancaire** en fonction des factures dans [!INCLUDE[prod_short](includes/prod_short.md)] qui comportent des arriérés de paiement.

## Pour ajouter des lignes rapprochement bancaire en important un relevé bancaire

Le volet **Lignes relevé bancaire** sera renseigné avec des transactions bancaires en fonction d’un flux ou d’un fichier importé fourni par la banque.

Pour importer des relevés bancaires en tant que flux bancaires, vous devez configurer le service Envestnet Yodlee Bank Feed. La configuration inclut la liaison de vos comptes bancaires dans [!INCLUDE[prod_short](includes/prod_short.md)] avec les comptes bancaires en ligne associés. Pour plus d’informations, voir [Configurer le service Envestnet Yodlee Bank Feeds](bank-how-setup-bank-statement-service.md).  

> [!TIP]
> Vous pouvez également importer des fichiers de relevés bancaires au format délimité par des virgules ou des points-virgules (.CSV). Utilisez la configuration assistée **Configurer un format de fichier de relevé bancaire** pour définir les formats d’importation des relevés bancaires et attacher le format à un compte bancaire. Vous pouvez ensuite utiliser ces formats lorsque vous importez des relevés bancaires dans la page **Rapprochement des comptes bancaires**.

1. Sélectionnez l’icône ![Ampoule qui ouvre la fonction Tell Me.](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire") entrez **Rapprochement bancaire**, puis sélectionnez le lien associé.
2. Sélectionnez l’action **Nouveau**.
3. Dans le champ **N° compte bancaire**, sélectionnez le compte bancaire approprié. Les écritures comptables compte bancaire qui existent pour le compte bancaire s’affichent le volet **Écritures comptables compte bancaire**.
4. Dans le champ **Date relevé**, saisissez la date du relevé de banque.
5. Dans le champ **Solde final du relevé**, saisissez le solde du relevé de banque.
6. Si vous avez un fichier de relevé bancaire, sélectionnez l’action **Importer le relevé bancaire**.
7. Localisez le fichier, puis sélectionnez le bouton **Ouvrir** pour importer les transactions bancaires dans le volet **Lignes relevé bancaire** sur la page **Rapprochement bancaire**.

## Pour renseigner les lignes rapprochement bancaire avec l’action Proposer lignes

Le volet **Lignes relevé bancaire** sera renseigné en fonction des factures dans [!INCLUDE[prod_short](includes/prod_short.md)] qui comportent des arriérés de paiement.  

1. Sur la page **Rapprochement bancaire**, sélectionnez l’action **Proposer lignes**.
2. Dans le champ **Date de début**, saisissez la date de validation la plus précoce des écritures comptables à rapprocher.
3. Dans le champ **Date de fin**, saisissez la date de validation la plus tardive des écritures comptables à rapprocher.

    > [!NOTE]
    > En règle générale, la date de fin correspond à la date spécifiée dans le champ **Date du relevé**. Cependant, si vous souhaitez rapprocher des transactions pour une partie seulement d’une période, vous pouvez saisir une date de fin différente.

4. Si vous ne souhaitez pas que les écritures comptables du compte bancaire incluent des écritures contrepassées ouvertes sans correspondance, activez le bouton à bascule **Exclure les écritures contrepassées**. Par défaut, la liste des écritures comptables des comptes bancaires inclura les écritures contrepassées jusqu’à la date du relevé.
5. Cliquez sur le bouton **OK**.

## Pour mettre en correspondance automatiquement des lignes de relevé bancaire avec des écritures comptables compte bancaire

La page **Rapprochement bancaire** propose une fonctionnalité de correspondance automatique basée sur une correspondance entre le texte d’une ligne relevé bancaire (volet gauche) et celui d’une ou de plusieurs écritures comptables compte bancaire (volet droit). Vous pouvez remplacer la correspondance automatique suggérée, et vous pouvez choisir de ne pas utiliser du tout la correspondance automatique. Pour plus d’informations, voir [Pour faire correspondre manuellement des lignes relevé bancaire avec des écritures comptables compte bancaire](bank-how-reconcile-bank-accounts-separately.md#to-match-bank-statement-lines-with-bank-account-ledger-entries-manually).

Vous pouvez rechercher la base des correspondances en utilisant l’action **Détails de correspondance**. Par exemple, les détails incluront les noms des champs qui contenaient des valeurs correspondantes.  

1. Sur la page **Rapprochement bancaire**, sélectionnez l’action **Faire correspondre automatiquement**. La page **Faire correspondre les écritures bancaires** s’ouvre.
2. Dans le champ **Tolérance date transaction (jours)**, spécifiez le nombre de jours avant et après la date comptabilisation de l’écriture comptable compte bancaire pendant lesquels l’action recherchera des dates transaction correspondantes dans le relevé bancaire.

    Si vous saisissez 0 ou laissez le champ vide, l’action **Faire correspondre automatiquement** recherchera uniquement les dates de transaction correspondantes sur la date comptabilisation de l’écriture comptable compte bancaire.
3. Cliquez sur le bouton **OK**.

    Les lignes sont codées par couleur pour faciliter la compréhension de ce qu’il faut en faire. Les lignes de relevé bancaire et les écritures comptables du compte bancaire qui correspondent au rapprochement bancaire actuel sont affichées en vert gras. Les écritures comptables de compte bancaire qui sont appariées sur d’autres rapprochements bancaires sont affichées en bleu italique.
4. Pour supprimer une correspondance, sélectionnez la ligne de relevé bancaire, et sélectionnez l’action **Supprimer correspondance**.

> [!TIP]
> Vous pouvez utiliser un mélange de correspondances manuelles et automatiques. Si vous avez mis en correspondance manuellement des écritures, la correspondance automatique n’écrasera pas vos sélections.

## Pour mettre en correspondance des lignes de relevé bancaire avec les écritures comptables compte bancaire manuellement

> [!TIP]
> Lors de la mise en correspondance manuelle des lignes et des écritures, les actions **Afficher tout**, **Afficher les écritures contrepassées**, **Masquer les écritures contrepassées** et **Afficher non-correspondances** peuvent faciliter l’obtention d’une vue d’ensemble. Par défaut, les écritures comptables du compte bancaire n’incluent pas les écritures contrepassées sans correspondance. Pour inclure ces entrées dans la liste et les faire correspondre manuellement, sélectionnez l’action **Afficher les écritures contrepassées**. Si vous choisissez de masquer les écritures contrepassées après avoir effectué une ou plusieurs correspondances, les écritures correspondantes sont toujours affichées.

> [!NOTE]
> Vous ne pouvez pas publier de rapprochement bancaire si vous effectuez une correspondance plusieurs à un et que les montants combinés contiennent des différences. Cela est vrai même si les différences combinées s’équilibrent à zéro.
>
> Voici un exemple de correspondance plusieurs-à-un qui présente des différences. La valeur de 200 pour l’écriture de relevé bancaire 1 est mise en correspondance avec deux écritures comptables bancaires qui ont une valeur totale de 180. La différence est de 20. La valeur de 350 pour l’écriture de relevé bancaire 2 est mise en correspondance avec deux autres écritures comptables bancaires qui ont une valeur totale de 370. La différence est de -20, ce qui équilibre la valeur de 20 pour le relevé bancaire 1.  
>
> Pour valider un rapprochement bancaire avec des différences sur les lignes, validez les différences, puis rapprochez-les des écritures validées.

1. Sur la page **Rapprochement bancaire**, sélectionnez une ligne non lettrée dans le volet **Lignes relevé bancaire**.
2. Dans le volet **Écritures comptables compte bancaire**, sélectionnez une ou plusieurs écritures comptables compte bancaire qui peuvent être mise en correspondance avec la ligne de relevé bancaire sélectionnée. Pour choisir plusieurs lignes, sélectionnez et maintenez la touche <kbd>CTRL</kbd> enfoncée, puis sélectionnez les lignes.

   > [!TIP]
   > Vous pouvez également faire correspondre manuellement plusieurs lignes de relevé bancaire avec une écriture comptable de compte bancaire. Par exemple, cela peut être utile si votre dépôt bancaire contient plusieurs modes de paiement, tels que des cartes de crédit de différents émetteurs, et que votre banque les répertorie sur des lignes distinctes.
3. Sélectionnez l’action **Faire correspondre manuellement**.

    La ligne de relevé bancaire sélectionnée et les écritures comptables compte bancaire sélectionnées deviennent vertes, et la case à cocher **Lettré** du volet de droite est activée.
4. Répétez les étapes 1 à 3 pour toutes les lignes de relevé bancaire qui ne sont pas mises en correspondance.

> [!TIP]
> Pour supprimer une correspondance, sélectionnez la ligne de relevé bancaire, et sélectionnez l’action **Supprimer correspondance**. Si vous avez rapproché plusieurs lignes de relevé bancaire avec une écriture comptable et que vous devez supprimer une ou plusieurs des lignes correspondantes, toutes les correspondances manuelles sont supprimées pour l’écriture comptable lorsque vous choisissez **Supprimer la correspondance**.

## Pour valider votre rapprochement bancaire

Pour revérifier le rapprochement de votre compte bancaire avant de le valider, utilisez l’action **Impression test** pour afficher un aperçu du rapprochement. L’état est disponible dans les contextes suivants :

* Lorsque vous préparez un rapprochement bancaire sur la page **Rapprochement bancaire**.
* Lorsque vous rapprochez des paiements sur la page **Feuilles rapprochement paiement**.

Les lignes qui ne peuvent pas être appariées restent sur la page **Rapprochement bancaire** après la validation. Ces lignes contiennent une valeur dans le champ **Différence**. La différence représente un écart que vous devez résoudre avant de pouvoir effectuer le rapprochement des comptes bancaires. Le tableau suivant décrit quelques situations commerciales typiques qui peuvent entraîner des différences.

| Différence | Motif | Résolution |
|------------|--------|------------|
| Une transaction dans votre compte bancaire dans [!INCLUDE[prod_short](includes/prod_short.md)] ne figure pas sur le relevé bancaire. | La transaction bancaire n’a pas été créée alors qu’une validation a été effectuée dans [!INCLUDE[prod_short](includes/prod_short.md)]. | Créez la transaction manquante (ou demandez à un débiteur de la faire). Réimportez ensuite le fichier de relevé de compte ou saisissez la transaction manuellement. |
| Une transaction sur le relevé bancaire n’existe pas en tant que ligne feuille ou document dans [!INCLUDE[prod_short](includes/prod_short.md)]. | Une transaction bancaire a été effectuée sans validation correspondante dans [!INCLUDE[prod_short](includes/prod_short.md)], par exemple la validation d’une ligne feuille pour une dépense. | Créez et validez l’écriture manquante. Pour apprendre un moyen rapide de lancer cette opération, consultez [Pour créer des écritures comptables manquantes avec lesquelles faire correspondre des transactions bancaires](bank-how-reconcile-bank-accounts-separately.md#to-create-missing-ledger-entries-to-match-bank-statement-lines). |
| Une transaction dans le compte bancaire interne correspond à une transaction bancaire, mais certaines informations sont trop différentes pour établir une correspondance. | Des informations, telles que le montant ou le nom du client, ont été saisies différemment dans la transaction bancaire et la validation interne. | Vérifiez les informations, puis faites les correspondre manuellement. Corrigez éventuellement la non-concordance des informations. |

Vous devez corriger les différences, par exemple en créant des écritures manquantes et en corrigeant les informations qui ne correspondent pas, ou en effectuant les transactions d’argent qui n’ont pas eu lieu, jusqu’à ce que le rapprochement du compte bancaire soit terminé et validé.

> [!NOTE]
> La page Rapprochement bancaire et le rapport de test supposent que vous n’effectuez le rapprochement que dans la période jusqu’à la date de fin du relevé. Si vous associez une ligne de relevé bancaire à une écriture comptable bancaire avant de saisir une date de fin de relevé, puis que vous saisissez une date de fin de relevé postérieure à la date de fin de l’écriture comptable bancaire, les données du rapport de test sont incorrectes.

Le tableau suivant décrit les champs du rapport de test qui peuvent vous aider à effectuer le rapprochement bancaire.

|Champ  |Désignation  |
|---------|---------|
|Date relevé| La date spécifiée dans le champ **Date du relevé** sur la page **Rapprochement bancaire**.|
|Solde dernier relevé|Le solde spécifié dans le champ **Solde dernier relevé** sur la page **Rapprochement bancaire**. Celui-ci est renseigné automatiquement à partir du rapprochement le plus récent pour le même compte bancaire. La valeur est zéro s’il s’agit de votre premier rapprochement de compte bancaire.|
|Solde final du relevé|Le solde spécifié dans le champ **Solde final du relevé** sur la page **Rapprochement bancaire**. |
|N° de compte général <*numéro*> Solde au <*date*> | Le solde du compte général à la date de fin du relevé. Il s’agit du solde non filtré à cette date. Si votre banque utilise votre devise locale, ce solde doit être le même que le solde de votre compte bancaire (affiché sur le côté droit de l’en-tête du rapport) lorsque vous avez rapproché toutes les lignes du relevé. Un **()** vide dans le nom de ce champ signifie que votre banque utilise la devise locale.<br><br>Une différence entre ce champ et les champs précédents pourrait indiquer que vous avez enregistré directement sur le compte général ou que vous utilisez le même compte général pour plusieurs banques, ce qui n’est pas recommandé. Les banques sont liées en comptabilité via le groupe comptabilisation du compte bancaire spécifié pour le compte.<br><br>Le rapport de test affiche un avertissement si vous avez des écritures directes, même si le solde de l’écriture est nul. Les écritures directes non soldées entraînent souvent des écarts cumulés pour les futurs rapprochements bancaires. Vous devez vérifier le solde comptable et les écritures comptables avant de reporter le rapprochement bancaire. Pour en savoir plus sur l’imputation directe, consultez [Éviter l’imputation directe](#avoid-direct-posting).|
|N° de compte général <*numéro*> Solde (<*DL*>) au <*date*>| Le solde du compte général à la date de fin du relevé en devise locale. Le solde est converti dans la devise du compte bancaire en utilisant le taux de change en vigueur à la date de fin du relevé. Il s’agit du solde non filtré à cette date. Vous comparez cela au champ **N° de compte G/L <* numéro *> solde au <* date*>* si votre banque utilise une devise étrangère. La valeur dans le champ du numéro de compte général <* numéro *> Solde au <* date*> pour la devise locale pourrait différer légèrement, car la conversion de devise peut entraîner de petites différences. Le solde de votre banque doit être très proche de ce solde.  |
|Solde compte bancaire au <*date*>| Le solde du compte bancaire à la date de fin du relevé.|
|Somme des différences    | La somme des différences pour les lignes de relevé. Pour accéder aux détails, activez le bouton **Imprimer les transactions restantes** lorsque vous saisissez des critères pour le rapport. Une différence est une ligne de relevé bancaire qui ne correspond pas complètement à une ou plusieurs écritures comptables bancaires. Vous ne pouvez pas valider un rapprochement de compte bancaire qui présente des différences. Vous pouvez valider un rapprochement bancaire contenant des écritures comptables bancaires qui ne correspondent pas aux lignes de relevé. Cette valeur est indiquée dans le champ **Transactions bancaires restantes** et dans une section distincte si vous activez le bouton à bascule Imprimer les transactions restantes.      |
|Solde relevé     | La valeur spécifiée dans le champ **Solde final du relevé** sur la page **Rapprochement bancaire**.  |
|Transactions bancaires restantes     | La somme des écritures comptables bancaires non appariées et autres que des chèques dont la date de validation est égale ou antérieure à la date de fin du relevé. Cela se produit lorsque vous enregistrez des transactions avant qu’elles ne soient enregistrées dans votre banque. Par exemple, à la fin d’une période. Lorsque vous créez le prochain rapprochement bancaire, vous pouvez rapprocher ces écritures.        |
|Chèques restants     | La somme des écritures comptables bancaires non appariées et autres que des chèques dont la date de validation est égale ou antérieure à la date de fin du relevé. Cela se produit lorsque vous enregistrez des transactions avant qu’elles ne soient enregistrées dans votre banque. Par exemple, cela peut se produire pour les chèques si un fournisseur n’encaisse pas un chèque au cours de la même période que vous l’avez enregistré. Lorsque vous créez le prochain rapprochement bancaire, vous pouvez rapprocher ces écritures.        |
|Solde compte bancaire     | Somme des valeurs du solde final du relevé bancaire, des transactions bancaires en cours et des chèques restants. Une fois que vous avez traité toutes les différences sur les entrées correspondantes, ce solde correspond à votre solde bancaire. Par exemple, vous avez comptabilisé toutes les écritures correspondantes ainsi que les écritures que vous n’avez pas pu faire correspondre pour ce relevé bancaire. Vous pouvez valider le rapprochement.        |

> [!TIP]
> Si vous lancez l’**Impression test** depuis la page **Feuille rapprochement bancaire**, [!INCLUDE [prod_short](includes/prod_short.md)] calcule la valeur dans le **Solde final du relevé** comme suit :
>
> * solde dernier relevé + somme de toutes les lignes de la feuille de rapprochement bancaire
>
> Vous pouvez utiliser la valeur pour comparaison avec votre relevé bancaire.

## Pour créer des écritures comptables manquantes avec lesquelles faire correspondre des lignes relevé bancaire

Les relevés bancaires comportent parfois des montants correspondant à la facturation d’intérêts ou de frais. Ces lignes relevé bancaire ne peuvent pas être mises en correspondance, car il n’existe aucune écriture comptable associée dans [!INCLUDE[prod_short](includes/prod_short.md)]. Vous devez ensuite valider une ligne feuille pour chaque transaction afin de créer une écriture comptable associée avec laquelle elle peut être mise en correspondance.

1. Sur la page **Rapprochement bancaire**, sélectionnez l’action **Transférer vers feuille comptabilité**.  
2. Sur la page **Trans. rappr. banc. -> f. cpta**, indiquez la feuille de comptabilité à utiliser, puis cliquez sur le bouton **OK**.

    La page **Feuille comptabilité** s’ouvre. Elle contient de nouvelles lignes feuille pour toutes les lignes de relevé bancaire dont les écritures comptables sont manquantes.
3. Renseignez la ligne feuille avec les informations, comme le compte de contrepartie. Pour en savoir plus, voir [Utiliser des feuilles comptabilité](ui-work-general-journals.md).  
4. Pour examiner le résultat de la validation avant de valider, choisissez l’option **Impression test**, puis choisissez une option pour accéder au rapport. L’état **Relevé bancaire** affiche les mêmes champs que dans l’en-tête de la page **Rapprochement bancaire**.
5. Sélectionnez l’action **Valider**.

    Une fois l’écriture validée, faites-lui correspondre la ligne de relevé bancaire.
6. Réactualisez ou rouvrez la page **Rapprochement bancaire**. La nouvelle écriture comptable s’affiche dans le volet **Écritures comptables compte bancaire**.
7. Faites correspondre la ligne relevé bancaire à l’écriture comptable compte bancaire, manuellement ou automatiquement.

## Trouver les transactions en suspens des périodes précédentes

Vous pouvez utiliser l’état Relevé bancaire pour rechercher les transactions en suspens des périodes précédentes. Les transactions en suspens ont été ouvertes avant la date du relevé et n’ont pas été fermées, ou ont été fermées après la publication du rapprochement bancaire.

Lorsque vous exécutez l’état Relevé bancaire à partir de la page Liste des relevés bancaires, vous pouvez activer le bouton à bascule **Écritures en suspens**, et l’état inclura une section qui répertorie les écritures en attente.

**Exemple** Nous avons des écritures comptables de compte bancaire A, B et C sur notre compte bancaire pour le mois d’août. Lorsque nous rapprochons notre compte bancaire pour le mois d’août, nous trouvons une ligne de relevé bancaire qui correspond à l’écriture A, mais aucune pour B et C. Nous publions donc le rapprochement avec l’écriture A rapprochée et les écritures B et C comme écritures en attente.

En septembre, nous recevons un paiement pour l’écriture B et décidons de rapprocher notre compte bancaire. Si nous exécutons l’état Relevé bancaire avant de publier le rapprochement, nous aurons une transaction rapprochée et une en attente.

Si nous imprimons l’état pour août, nous aurons des transactions en suspens pour nos écritures B et C, même si nous avons fermé l’écriture B en septembre.

## Annuler un rapprochement bancaire

Si vous découvrez une erreur dans un rapprochement bancaire validé, vous pouvez utiliser l’action **Annuler** sur la page **Liste des relevés bancaires** pour le corriger. Lorsque vous annulez un rapprochement bancaire validé, les écritures sont déplacées vers la page **Rapprochement bancaire** et sont marquées comme **Ouvertes**, ce qui signifie qu’elles ne sont pas rapprochées. Vous pouvez ensuite corriger le rapprochement bancaire et le valider à nouveau.

> [!NOTE]
> Dans la version des États-Unis, pour utiliser la fonction Annuler pour les rapprochements bancaires et les relevés bancaires validés, vous devez activer le bouton bascule **Rapprochement bancaire avec correspondance automatique** sur la page **Paramètres comptabilité**. La fonction Annuler n’est pas disponible pour les relevés bancaires publiés à partir des feuilles de calcul de rapprochement bancaire.

### Réutilisation du numéro de relevé bancaire

Le numéro de relevé bancaire utilisé pour le nouveau rapprochement bancaire est extrait du compte bancaire, tout comme le dernier relevé de solde. Vous pouvez modifier ces valeurs avant de commencer un nouveau rapprochement bancaire. Cependant, lorsque vous créez un nouveau rapprochement bancaire, [!INCLUDE[d365fin](includes/d365fin_md.md)] vérifie si le numéro de relevé est déjà attribué à un relevé bancaire validé. Si le numéro est utilisé, mais que vous souhaitez que le nouveau relevé bancaire l’utilise à la place, vous pouvez utiliser **Modifier n° relevé** sur la page **Rapprochement bancaire**.

### Exemples

Voici quelques exemples de la façon de corriger une erreur sur un rapprochement bancaire validé, avec ou sans l’utilisation du même numéro de relevé.

#### Exemple 1

Vous avez effectué des rapprochements bancaires pour janvier, février et mars. Le numéro de relevé bancaire était 100 pour mars. Plus tard, vous découvrez que mars n’a inclus que les entrées jusqu’au 30, ce qui signifie que les entrées pour le 31 sont manquantes. Vous devez donc refaire le rapprochement bancaire pour mars. Dans ce cas, nous allons ouvrir la page **Relevé bancaire**, choisissez le relevé de mars, puis choisissez **Annuler**. 

Le nouveau rapprochement bancaire porte le numéro de relevé 101. Pour réaffecter le nombre 100, choisissez **Modifier n° relevé** et entrez **100**. 

> [!TIP]
> N’oubliez pas de définir la date de fin de relevé appropriée (dans cet exemple, le 31 mars) et de modifier le champ **Solde dernier relevé**. 

#### Exemple 2

Vous avez effectué des rapprochements bancaires pour janvier, février, juin et juillet. Vous découvrez que février était incorrect. Supposons qu’il ait le numéro de déclaration 100. Comme dans l’exemple 1, vous utilisez les actions Annuler et Modifier n° relevé. pour changer le numéro de relevé comme dans l’exemple n° 1 ci-dessus et vous pouvez maintenant refaire le rapprochement bancaire de février.  

Après avoir validé le rapprochement bancaire corrigé pour février, sur la fiche de compte bancaire correspondante, le champ **Dernier n° relevé** affichera **100**, et le champ **Solde dernier relevé** affichera le solde de fin du relevé de février. 

Si le prochain rapprochement bancaire que vous effectuez est pour mars, [!INCLUDE[d365fin](includes/d365fin_md.md)] attribuera 101 comme numéro de relevé et lui donnera le bon **Solde dernier relevé**.

Si le prochain rapprochement bancaire que vous effectuez concerne le mois d’août, envisagez de modifier les valeurs dans les champs **N° dernier relevé** et **Solde dernier relevé** sur la fiche **Compte bancaire** avant de créer le prochain rapprochement bancaire, ou utilisez l’action **Modifier n° relevé** et modifiez également la valeur dans le champ **Solde dernier relevé** sur la page de rapprochement bancaire.

> [!NOTE]
> Le numéro de relevé est important lorsque vous effectuez des rapprochements bancaires avec des fichiers CAMT importés contenant des numéros de relevé ou lorsque vous effectuez un rapprochement sur la base de relevés bancaires imprimés. Si vous téléchargez simplement une série de transactions bancaires depuis votre banque en ligne, le numéro de relevé n’est généralement pas important.  
>
> Le dernier relevé de solde est conservé sur le compte bancaire pour minimiser les erreurs lors des rapprochements bancaires, mais il est également modifiable, vous permettant d’effectuer vos rapprochements bancaires dans l’ordre de votre choix. Cela signifie également que si vous annulez un relevé bancaire, le nouveau solde de clôture peut ne pas être le dernier relevé du solde sur le prochain relevé bancaire. Il n’y a aucune fonctionnalité qui vous permet de transférer un solde vers tous les relevés bancaires suivants, donc soyez conscient de cela lorsque vous utilisez Annuler.  

## Éviter l’imputation directe

N’utilisez pas de compte général qui permet la validation directe dans votre groupe comptabilisation de compte bancaire. La validation directe rompra le lien entre l’écriture comptable du compte bancaire et l’écriture comptable du compte général. Lorsque vous rapprochez votre compte bancaire, les écritures comptabilisées directement dans le compte général ne seront pas incluses et il sera difficile de mener à bien le rapprochement.

Cette erreur se produit souvent lors de la saisie d’un solde d’ouverture pour un compte bancaire. Il est important que vous ne comptabilisiez pas le solde d’ouverture directement dans la comptabilité. Les écritures dans le compte général qui sont comptabilisées directement dans le compte général causeront des problèmes. Par exemple, ces écritures peuvent vous empêcher de rapprocher votre compte bancaire. Pour les comptes bancaires en devise étrangère, les écritures peuvent entraîner l’accumulation de différences après la validation d’autres rapprochements bancaires, en raison des ajustements du taux de change. Souvent, vous comptabilisez le solde bancaire d’ouverture directement sur le compte bancaire, et le montant se retrouve ensuite dans le compte général. Sinon, contrepassez-le plus tard sur un compte général que vous utilisez pour équilibrer le solde d’ouverture des écritures comptables. Dans les deux cas, vous devez équilibrer toute écriture directe sur le compte général avant de commencer votre premier rapprochement bancaire, et surtout si le compte bancaire est en devise étrangère.

## Voir aussi

[Rapprochement de comptes bancaires](bank-manage-bank-accounts.md)  
[Lettrage automatique des paiements et rapprochement des comptes bancaires](receivables-apply-payments-auto-reconcile-bank-accounts.md)  
[Paramétrage des opérations bancaires](bank-setup-banking.md)  
[Définir des règles pour le lettrage automatique des paiements](receivables-how-set-up-payment-application-rules.md)  
[Utiliser [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
