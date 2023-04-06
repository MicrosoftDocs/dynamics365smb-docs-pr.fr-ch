---
title: Rapprocher les paiements à l’aide de l’application automatique
description: Décrit comment rapprocher les paiements avec la fonction de lettrage automatique pour lettrer les paiements ou les règlements dans leurs écritures ouvertes connexes.
author: brentholtorf
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 'payment process, direct payment posting, reconcile payment, expenses, cash receipts'
ms.search.form: '389, 1290, 1294, 1287'
ms.date: 06/22/2022
ms.author: bholtorf
---
# Rapprocher les paiements à l’aide de l’application automatique

La page **Journal de rapprochement bancaire** précise les paiements, entrants ou sortants, qui ont été enregistrés comme des transactions sur votre compte bancaire en ligne ou sur un service de paiement. Vous pouvez appliquer les paiements aux écritures comptables client, fournisseur et compte bancaire ouvertes associées. Complétez le journal en important un relevé bancaire en tant que flux ou fichier bancaire ou en saisissant manuellement les transactions que vous effectuez sur votre service de paiement.

> [!NOTE]
> La page offre une fonctionnalité de correspondance automatique qui lettre les paiements à leurs écritures ouvertes associées sur la base d’une correspondance entre les données d’une ligne de relevé bancaire (ligne feuille) et les données d’une ou de plusieurs écritures ouvertes. Notez que vous pouvez remplacer les applications automatiques suggérées, et vous pouvez choisir de ne pas utiliser du tout l’application automatique. Pour plus d’informations, voir l’étape 7.

Un journal de rapprochement bancaire est lié à un compte bancaire dans [!INCLUDE[prod_short](includes/prod_short.md)]. Le compte bancaire représente le compte bancaire en ligne où sont enregistrées les opérations de paiement. Toutes les écritures comptables compte bancaire ouvertes associées au client lettré ou à des écritures comptables fournisseur sont clôturées lorsque vous sélectionnez l’action **Valider les paiements et rapprocher les comptes bancaires**. Le compte bancaire est automatiquement rapproché pour les paiements que vous validez avec le journal.

Si vous utilisez le **Journal de rapprochement bancaire** pour enregistrer et appliquer les paiements des clients, vous pouvez configurer le journal pour utiliser une souche de numéros spécifique. Ensuite, vous pouvez spécifier la souche de numéros dans le champ **Souches de n° de rapprochement bancaire** sur un compte bancaire. L’utilisation d’une souche de numéros dédiée peut faciliter l’identification des entrées qui ont été publiées via le journal.

Comme pour les autres journaux, lorsque vous corrigez des écritures reportées, vous pouvez annuler des écritures qui ont été reportées via le journal de rapprochement bancaire à partir de la page **Comptabilité**. Par exemple, vous souhaiterez peut-être annuler des écritures pour des paiements que vous avez appliqués au mauvais client. Vous devez d’abord annuler le lettrage des écritures clients reportées. Ensuite, vous pouvez utiliser l’action **Contrepasser l’historique des transactions** dans la page **Contrepasser l’historique des transactions** pour annuler le journal ayant validé les paiements. Sinon, sur la page **Feuilles comptabilité validées**, vous pouvez utiliser l’action **Copier les lignes sélectionnées dans le journal** pour annuler des lignes spécifiques du journal de rapprochement bancaire validés. 

Lorsque vous utilisez l’application automatique, [!INCLUDE[prod_short](includes/prod_short.md)] reconnaît les écritures comptables bancaires déjà enregistrées, ce qui permet d’éviter les doubles écritures.

Vous pouvez importer des transactions bancaires sous forme de fichiers bancaires .csv ou d’un autre format fourni par votre banque. Si vous souhaitez importer des relevés bancaires en tant que flux bancaires, vous devez d’abord activer le service d’intégration bancaire dédié, puis associer le compte bancaire au compte bancaire en ligne associé. La feuille rapprochement bancaire détectera alors automatiquement les flux bancaire si vous sélectionnez l’action **Importer les transactions bancaires**. En outre, vous pouvez définir un compte bancaire de sorte à importer automatiquement de nouveaux flux de relevés bancaires toutes les heures. Les transactions pour les paiements qui ont déjà été validés comme lettrés et/ou rapprochés ne sont pas importées. Vous pouvez utiliser le service Envestnet Yodlee Bank Feeds pour obtenir ces transactions ; il est préinstallé dans certaines versions localisées de [!INCLUDE[d365fin](includes/d365fin_md.md)]. Pour plus d’informations, voir [Configurer le service Envestnet Yodlee Bank Feeds](bank-how-setup-bank-statement-service.md). Vous pouvez également contacter votre partenaire Microsoft pour obtenir de l’aide pour répondre aux exigences de votre entreprise ou de votre pays.

L’action **Mapper le texte avec le compte** vous permet de configurer des mappages entre le texte des paiements et des comptes de débit, de crédit et de contrepartie spécifiques afin que ces paiements soient validés dans les comptes spécifiés lorsque vous validez la feuille rapprochement bancaire. Cela s’avère utile, par exemple, pour les recettes ou dépenses récurrentes en liquide, notamment les achats fréquents de carburant pour les voitures ou les frais et intérêts bancaires, qui apparaissent régulièrement sur le relevé bancaire et n’ont pas besoin d’un document d’entreprise lié. (Voir l’étape 10 ci-dessous) Pour plus d’informations, reportez-vous à [Mapper du texte sur les paiements récurrents aux comptes pour un rapprochement automatique](receivables-how-map-text-recurring-payments-accounts-auto-reconcilliation.md).

Les lignes de journal peuvent ne pas avoir d’application suggérée, ce qui peut se produire pour diverses raisons. Par exemple, comme un document est manquant ou parce qu’un client a versé un montant trop élévé et qu’il y a un montant excédentaire après l’application du paiement sur une autre ligne feuille. Dans de tels cas, vous pouvez utiliser l’action **Transférer la différence vers un compte** pour créer et valider l’écriture comptable manquante, par exemple pour un remboursement, qui est nécessaire pour appliquer le paiement. (Voir l’étape 11) Pour plus d’informations, voir [Rapprocher les paiements qui ne peuvent pas être lettrés.](receivables-how-reconcile-payments-cannot-apply-auto.md).

Vous utilisez la fonction **Lettrer automatiquement**, soit automatiquement lorsque vous importez un fichier ou flux bancaire avec des transactions de paiement ou lorsque vous l’activez, pour lettrer des paiements à leurs écritures ouvertes associées sur la base d’une correspondance entre le texte d’une ligne relevé bancaire (ligne feuille) et le texte d’une ou plusieurs écritures ouvertes. Cette automatisation est basée sur des règles que vous définissez sur la page **Règles de lettrage de paiement**, où vous définissez également si une suggestion de lettrage doit être examinée. Pour plus d’informations, voir [Définir des règles pour le lettrage automatique des paiements](receivables-how-set-up-payment-application-rules.md).

Sur les lignes feuille dans lesquelles un paiement a été lettré automatiquement à une ou plusieurs écritures ouvertes, le champ **Fiabilité correspondance** présente une valeur **Faible**, **Moyenne** ou **Élevée** pour indiquer la qualité de la correspondance des données sur laquelle le lettrage de paiement suggéré est basée.

Certains lettrages de paiement nécessitent que vous les examiniez tel que défini par la règle de correspondance utilisée, comme les lignes avec une fiabilité de correspondance **Faible**. Les autres lignes nécessitent que vous les examiniez ainsi qu’une modification manuelle, car il y a une valeur dans le champ **Différence**. Pour examiner un ou plusieurs lettrages de paiement, choisissez le champ **Lignes à vérifier** ou **Lignes avec différence** en bas. La page **Révision lettrage paiement** s’ouvre et affiche toutes les informations pertinentes sur le client ou le fournisseur auquel le paiement est lettré, les détails de la correspondance et les actions pour traiter la ligne, telles que l’action **Accepter le lettrage**. (Voir les étapes 7 et 8)

Pour chaque ligne feuille de la page **Feuille rapprochement bancaire**, vous pouvez ouvrir la page **Lettrage paiement** pour visualiser toutes les écritures ouvertes candidates au paiement et pour afficher les informations détaillées pour chaque écriture sur la correspondance des données sur laquelle un lettrage de paiement est basé. Ici, vous pouvez appliquer les paiements manuellement ou réappliquer les paiements qui ont été automatiquement appliqués à une écriture incorrecte. (Voir l’étape 10) Pour plus d’informations, voir [Réviser ou lettrer les paiements après application automatique](receivables-how-review-apply-payments-auto-application.md).

> [!NOTE]  
> Vous pouvez lancer l’importation des transactions bancaires en même temps que vous ouvrez la page **Feuille rapprochement bancaire** pour une feuille existante. La procédure suivante décrit comment importer des transactions bancaires sur la page **Feuille rapprochement bancaire** après avoir créé une nouvelle feuille.

## Pour rapprocher les paiements à l’aide du lettrage automatique
1. Sélectionnez l’icône ![Ampoule qui ouvre la fenêtre de recherche.](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire") entrez **Feuilles rapprochement bancaire**, puis sélectionnez le lien associé.
2. Pour travailler dans une nouvelle feuille rapprochement bancaire, sélectionnez l’action **Nouvelle feuille**.
3. Sur la page **Liste comptes bancaires paiement**, sélectionnez le compte bancaire pour lequel vous voulez rapprocher des paiements, puis cliquez sur le bouton **OK**.
   La page **Feuille rapprochement bancaire** s’ouvre préparée pour le compte bancaire sélectionné.
4. Choisissez l’action **Importer les transactions bancaires**.
   Si le compte bancaire du journal sélectionné n’est pas configuré pour importer des opérations bancaires, [!INCLUDE[d365fin](includes/d365fin_md.md)] vous aide à y parvenir.
5. Sur la page **Sélectionner un fichier à importer**, sélectionnez le fichier contenant les transactions bancaires pour les paiements que vous souhaitez rapprocher, puis cliquez sur le bouton **Ouvrir**.  
6. Si le service Envestnet Yodlee Bank Feeds est activé, sur la page **Filtre de relevé bancaire** qui s’ouvre automatiquement, spécifiez l’intervalle de temps pour l’importation des relevés bancaires.

    La page **Feuille rapprochement bancaire** est renseignée avec les lignes pour les paiements représentant les transactions bancaires dans le relevé bancaire importé.

     Sur les lignes pour les paiements qui ont été automatiquement lettrés à leurs écritures ouvertes associées, le champ **Fiabilité correspondance** présente une valeur entre Faible et Élevée pour indiquer la qualité de la correspondance des données sur laquelle le lettrage du paiement suggéré est basé. En outre, les champs **Nom du compte**, **Type de compte** et **N° compte** sont renseignés à l’aide des informations sur le client ou le fournisseur auquel le paiement est lettré.

    Les lettrages automatiques, les qualités de correspondance et si les lignes doivent être révisées sont définis par des règles. Vous pouvez modifier les règles pour ajuster les résultats. Pour plus d’informations, voir [Définir des règles pour le lettrage automatique des paiements](receivables-how-set-up-payment-application-rules.md).

7. Pour examiner, accepter/supprimer ou modifier manuellement plusieurs lettrages de paiement qui ont une valeur dans le champ **Différence**, choisissez l’action **Lignes avec différence** en bas.

    La page **Révision lettrage paiement** s’ouvre et affiche le premier lettrage à examiner. Le prochain lettrage à examiner sera affiché sur la page au fur et à mesure que vous traitez le précédent. La révision inclut les informations pertinentes sur le client ou le fournisseur auquel le paiement est lettré, les détails de la correspondance et les actions pour traiter la ligne, telles que les actions **Accepter le lettrage** et **Lettrer manuellement**.

8. Pour examiner, accepter ou supprimer, ou modifier manuellement plusieurs applications de paiement que la règle a définies pour être examinées, choisissez l’action **Lignes à réviser**. 

9. Pour modifier un lettrage automatique, sélectionnez une feuille journal, puis sélectionnez l’action **Lettrer manuellement** pour relettrer ou lettrer le paiement manuellement sur la page **Lettrage paiement**. Pour plus d’informations, voir [Réviser ou lettrer les paiements après application automatique](receivables-how-review-apply-payments-auto-application.md).

10. Sélectionnez une ligne feuille non lettrée pour une réception ou une dépense récurrente en liquide, par exemple l’achat de carburant pour une voiture, puis sélectionnez **Mapper le texte avec le compte**. Pour plus d’informations, reportez-vous à [Mapper du texte sur les paiements récurrents aux comptes pour un rapprochement automatique](receivables-how-map-text-recurring-payments-accounts-auto-reconcilliation.md).

    Une fois terminé le mappage du texte de paiement avec les comptes, sélectionnez l’action **Lettrer manuellement**.

    Lorsqu’un mappage texte avec compte est configuré, le lettrage de paiement automatique qui en résulte contiendra **Élevée - Mappage de texte à compte** dans le champs **Fiabilité correspondance**.

11. Pour une ligne feuille qui n’a pas de lettrage suggéré car il n’existe aucune écriture comptable à laquelle elle peut être lettrée, choisissez l’action **Transférer la différence vers un compte** pour créer et valider l’écriture comptable manquante à laquelle lettrer le paiement. Pour plus d’informations, voir [Rapprocher les paiements qui ne peuvent pas être lettrés](receivables-how-reconcile-payments-cannot-apply-auto.md).

12. Lorsqu’il n’y a plus de lignes à exéminer et que le champ **Différence** est vide sur toutes les lignes, choisissez l’action **Valider**, puis choisissez l’une des options suivantes :

    - **Valider les paiements et rapprocher les comptes bancaires** - Pour valider les paiements comme lettrés et clôturer également les écritures comptables compte bancaire associées comme rapprochées.
    - **Valider les paiements uniquement** - Pour valider uniquement les paiements comme lettrés, mais laisser les écritures comptables compte bancaire ouvertes. Exige que vous rapprochiez le compte bancaire séparément, par exemple. Pour plus d’informations, voir [Rapprocher des comptes bancaires](bank-how-reconcile-bank-accounts-separately.md).
    - **Impression test** - Pour examiner le résultat de la validation avant de valider. L’état **Relevé bancaire** s’ouvre et affiche les mêmes champs qu’en bas de la page **Feuille rapprochement bancaire**.

Lorsque vous validez le journal de rapprochement bancaire, les écritures ouvertes appliquées sont fermées. Les comptes client, fournisseur ou général sont mis à jour. Pour les paiements sur les lignes feuille basées sur le mappage de texte à compte, les comptes généraux, client et fournisseur spécifiés sont mis à jour. Pour toutes les lignes feuille, des écritures comptables compte bancaire sont créées. Si vous sélectionnez l’action **Valider les paiements et rapprocher les comptes bancaires**, toutes les écritures comptables compte bancaire ouvertes associées au client lettré ou à des écritures comptables fournisseur sont clôturées. Cela signifie que le compte bancaire est automatiquement rapproché pour les paiements que vous validez avec le journal.

Vous pouvez comparer la valeur du champ **Solde sur compte bancaire après validation** avec la valeur du champ **Solde final du relevé** pour avoir un suivi lorsque le compte bancaire a fait l’objet d’un rapprochement en fonction des paiements que vous validez.

> [!NOTE]  
>   Si vous ne souhaitez pas rapprocher le compte bancaire à partir de la page **Feuille rapprochement bancaire**, vous devez utiliser la page **Rapprochement bancaire**. Pour plus d’informations, voir [Rapprocher des comptes bancaires](bank-how-reconcile-bank-accounts-separately.md).

## Voir la [formation Microsoft](/training/modules/use-journals-dynamics-365-business-central/) associée

## Voir aussi

[Gestion des comptes client](receivables-manage-receivables.md)  
[Ventes](sales-manage-sales.md)  
[Utiliser [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
