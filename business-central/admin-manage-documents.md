---
title: Gérer le stockage en supprimant des documents ou en compressant des données
description: Apprenez à gérer l’accumulation de documents historiques (et à réduire la quantité de données stockées dans une base de données) en les supprimant ou en les compressant.
author: brentholtorf
ms.topic: conceptual
ms.search.form: '107, 9035, 9040'
ms.date: 09/14/2022
ms.author: bholtorf
ms.service: dynamics-365-business-central
---
# <a name="manage-storage-by-deleting-documents-or-compressing-data"></a>Gérer le stockage en supprimant des documents ou en compressant des données

Un rôle central, par exemple un administrateur d’application, doit régulièrement gérer les documents accumulés au fil du temps en les supprimant ou en les compressant.  

> [!TIP]
> Découvrez les autres moyens de réduire la quantité de données stockées dans une base de données en lisant [Réduction des données stockées dans les bases de données Business Central](/dynamics365/business-central/dev-itpro/administration/database-reduce-data) dans notre documentation pour développeurs et professionnels de l’informatique.

## <a name="delete-documents"></a>Supprimer des documents.

Dans certains cas, vous pouvez souhaiter supprimer des commandes achat facturées. Cependant, vous ne pouvez pas les supprimer tant que vous n’avez pas entièrement facturé et reçu les articles des commandes achat. [!INCLUDE[prod_short](includes/prod_short.md)] vous aide en vérifiant cela.

Les retours sont généralement supprimés après leur facturation. Lorsque vous validez une facture, elle est transférée vers la page **Avoir achat enregistré**. Si vous avez activé la case à cocher **Expédition retour sur avoir** sur la page **Paramètres achats**, la facture est transférée vers la page **Expédition retour enregistrée**. Vous pouvez supprimer les documents à l’aide du traitement par lots **Supprimer les retours achat facturés**. Avant de procéder à la suppression, le traitement par lots vérifie que les retours achat ont été entièrement livrés et facturés.  

Les commandes cadres achat ne sont pas supprimées automatiquement une fois que toutes les commandes achat associées ont été traitées et facturées. Au lieu de cela, vous pouvez les supprimer à l’aide du traitement par lots **Supprimer commandes cadres achat facturées**.  

Les commandes service facturées sont habituellement supprimées automatiquement après avoir été entièrement facturées. Lors de la validation d’une facture, une écriture correspondante est générée et peut être affichée sur la page **Factures service enreg.**.  

Le programme ne supprime pas les commandes service automatiquement cependant, si la quantité totale sur la commande a été validée à partir de la page **Facture service** plutôt qu’à partir de la commende de service elle-même. Vous devrez peut-être supprimer manuellement ces commandes facturées en exécutant le traitement par lots **Supprimer les commandes de service facturées**.  

## <a name="compress-data-with-date-compression"></a>Compresser les données avec la compression selon la date

Vous pouvez compresser les données dans [!INCLUDE [prod_short](includes/prod_short.md)] pour économiser de l’espace dans la base de données, ce qui dans [!INCLUDE [prod_short](includes/prod_short.md)] Online peut même vous faire économiser de l’argent. La compression, basée sur les dates et les fonctions, combine plusieurs anciennes écritures en une nouvelle écriture.

Vous pouvez compresser les écritures qui répondent à toutes les conditions suivantes :

* Elles proviennent d’exercices clos.
* Le champ **Ouvert** est défini sur **Non**.
* Elles ont au moins cinq ans. Si vous souhaitez compresser des données datant de moins de cinq ans, contactez votre partenaire Microsoft.

Par exemple, les écritures comptables fournisseur d’exercices précédents peuvent être compressées de façon à ce qu’il ne reste qu’une écriture créditrice et une écriture débitrice par compte et par mois. Le montant de la nouvelle écriture est la somme de toutes les écritures compressées. La date affectée est la date début de la période qui est compressée, par exemple le premier jour du mois (si les écritures sont compressées par mois). Après la compression, vous pouvez encore afficher le solde période de chaque compte de l’exercice précédent.

Le nombre d’écritures qui résultent d’un traitement par lots de compression dépend du nombre filtres que vous définissez, des champs qui sont combinés et de la durée de la période que vous choisissez. Il y a toujours au moins une écriture. Lorsque le traitement par lots est terminé, le résultat s’affiche dans la page **Historique des compressions**.

Vous pouvez compresser les types de données suivants à l’aide de traitements par lots.

* Écritures financières : écritures comptables, écritures de taxe sur la valeur ajoutée (TVA), écritures comptables compte bancaire, écritures budgétaires comptables, écritures comptables clients et écritures comptables fournisseurs.
* Écritures entrepôt
* Écritures de ressource
* Écritures budget article
* Écritures comptables immobilisation, écritures comptables de maintenance immo., écritures comptables d’assurance immo.

Lorsque vous définissez des critères pour la compression, vous pouvez conserver le contenu de certains champs à l’aide des options sous **Conserver champs**. Les champs disponibles dépendent des données que vous compressez.

> [!NOTE]
> Avant de pouvoir exécuter la compression selon la date, vos vues d’analyse doivent être à jour. Pour plus d’informations, consultez la section [Mettre à jour une vue d’analyse](bi-how-analyze-data-dimension.md#update-an-analysis-view).

Après la compression, le contenu des champs suivants sera toujours conservé : **Date comptabilisation**, **N° fournisseur**, **Type de document**, **Code devise**, **Groupe comptabilisation**, **Montant**, **Montant ouvert**, **Montant initial DS**, **Montant ouvert DS**, **Montant DS**, **Achat DS**, **Remises facture DS**, **Escompte accordé DS** et **Escompte ouvert possible**.

## <a name="posting-compressed-entries"></a>Validation d’écritures compressées

Les écritures compressées sont publiées légèrement différemment de la publication standard. Cela permet de réduire le nombre de nouvelles écritures comptables créées par compression de date et est particulièrement important lorsque vous conservez des informations telles que les dimensions et les numéros de document. La compression de date crée de nouvelles entrées comme suit :

* Sur la page **Écritures comptables**, de nouvelles entrées sont créées pour les entrées compressées. Le champ **Description** contient l’information **Compression écritures** afin que les entrées compressées soient faciles à identifier. 
* Sur les pages comptables, telles que la page **Écritures comptables client**, une ou plusieurs entrées sont créées. 

Le processus de validation crée des écarts dans la série de numéros pour les entrées sur la page **Écritures comptables**. Ces numéros sont attribués aux écritures sur les pages comptables uniquement. La plage de numéros affectée aux entrées est disponible sur la page **Historique des transactions de comptabilité** dans les champs **N° séquence début** et **N° séquence fin**. 

> [!NOTE]
> Après avoir exécuté la compression des dates, tous les comptes du grand livre sont verrouillés. Cela signifie que vous ne pouvez pas, par exemple, contrepasser les écritures du fournisseur ou du grand livre bancaire pour les comptes affecté par la compression.

Le nombre d’écritures qui résultent d’un traitement par lots de compression dépend du nombre filtres que vous définissez, des champs qui sont combinés et de la durée de la période que vous choisissez. Il y aura toujours au moins une écriture.

> [!WARNING]
> La compression basée sur la date supprime des écritures ; vous devez donc toujours faire une sauvegarde de la base de données avant de lancer le traitement par lots.

### <a name="to-run-a-date-compression"></a>Pour exécuter la compression selon la date

1. Sélectionnez l’icône ![Rechercher une page ou un état](media/ui-search/search_small.png "Icône Rechercher une page ou un état"), entrez **Administration des données**, puis sélectionnez le lien associé.
2. Exécutez l’une des opérations suivantes :
    * Pour utiliser un guide de configuration assistée afin de configurer la compression selon la date pour un ou plusieurs types de données, choisissez **Guide d’administration des données**.
    * Pour configurer la compression pour un type de données individuel, choisissez **Compression des données**, **Compresser écritures**, puis choisissez les données à compresser.

   > [!NOTE]
   > Vous ne pouvez compresser que des données datant de plus de cinq ans. Si vous souhaitez compresser des données datant de moins de cinq ans, contactez votre partenaire Microsoft. Ils doivent utiliser le `OnSetMinimumNumberOfYearsToKeep` événement dans le codeunit "Date Compression" pour définir le seuil.


## <a name="see-also"></a>Voir aussi

[Administration](admin-setup-and-administration.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
