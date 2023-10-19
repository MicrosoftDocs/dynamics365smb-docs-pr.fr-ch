---
title: Consolider les données de plusieurs sociétés
description: Cet article explique comment vous pouvez consolider les écritures comptables d’au moins deux sociétés séparées (filiales) dans une société consolidée.
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bnielse
ms.topic: conceptual
ms.date: 06/27/2023
ms.custom: bap-template
ms.search.keywords: 'consolidation, subsidiaries, consolidate'
ms.search.form: '1826, 1827'
---

# <a name="consolidating-financial-data-from-multiple-companies"></a>Consolidation des données financières de plusieurs sociétés

Certaines organisations utilisent [!INCLUDE [prod_short](includes/prod_short.md)] dans plusieurs centres de profit ou entités juridiques. D’autres utilisent [!INCLUDE [prod_short](includes/prod_short.md)] dans les filiales qui doivent rendre compte aux organisations mères. [!INCLUDE [prod_short](includes/prod_short.md)] fournit aux comptables des outils qui les aident à transférer les écritures comptables de deux ou plusieurs sociétés (filiales) dans une société consolidée.  

Chaque société impliquée dans une consolidation est appelée centre de profit. La société dans laquelle vous combinez les données est appelée société consolidée.  

Vous pouvez transférer les données financières des filiales vers la société consolidée, même si les filiales utilisent [!INCLUDE [prod_short](includes/prod_short.md)] dans différents environnements. Pour en savoir plus sur la façon de vous connecter à d’autres environnements, consultez [Configurer la consolidation de la société](finance-consolidated-company-reporting-setup.md#busunit).

Si les états financiers d’un centre de profit utilisent une devise différente de celle de la société consolidée, vous devez configurer les taux de change pour la consolidation. Pour en savoir plus sur les taux de change pour les consolidations, consultez [Configurer la consolidation de la société](finance-consolidated-company-reporting-setup.md#exchrates).  

Vous pouvez consolider :  

* des sociétés avec plusieurs plans comptables ;  
* des sociétés qui utilisent plusieurs exercices comptables et devises ;  
* la totalité ou un pourcentage des informations financières d’une société ;
* en utilisant plusieurs taux de change dans des comptes généraux individuels ;
* des sociétés dans d’autres programmes de gestion comptable et d’entreprise ;
* des sociétés dans des environnements [!INCLUDE [prod_short](includes/prod_short.md)] différents.

Vous configurez la société consolidée de la même manière que vous configurez d’autres sociétés. Le plan comptable est indépendant des plans comptables des centres de profit. Le plan comptable des centres de profit peut différer les uns des autres. Pour en savoir plus sur la configuration d’une consolidation, consultez [Configurer la consolidation de la société](finance-consolidated-company-reporting-setup.md).  

> [!TIP]
> La consolidation des données financières peut être particulièrement appropriée pour les processus intersociétés. Pour en savoir plus sur les fonctionnalités intersociétés, consultez [Gestion des transactions intersociétés](intercompany-manage.md).

## <a name="consolidate-data"></a>Consolider les données

Avant de procéder à une consolidation, il est recommandé de tester vos données avant de les transférer vers la société consolidée. [!INCLUDE[prod_short](includes/prod_short.md)] recherche des différences dans les informations des centres de profit et de la société consolidée. Par exemple, si les numéros de compte ou les codes axe sont différents. Corriger les erreurs trouvées avant d’exécuter l’état. Vous pouvez tester la base de données ou, si vous importez des données à partir d’un fichier XML, le fichier.

### <a name="test-the-data-before-you-consolidate"></a>Tester les données avant la consolidation

1. Ouvrez la société consolidée.  
2. Sélectionnez ![l’icône en forme d’Ampoule qui ouvre la fenêtre de recherche](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire"),  entrez **Centres de profit**, puis choisissez le lien associé.  
3. Testez le fichier et la base de données, comme suit :  

    * Pour tester un fichier, choisissez l’action **Tester fichier**, entrez le nom du fichier à tester, puis choisissez **Imprimer**.  
    * Pour tester la base de données, choisissez **Tester base de données**.  

### <a name="run-the-consolidation"></a>Exécuter la consolidation

Une fois les données testées, vous pouvez les transférer vers la société consolidée. Un guide de configuration assistée vous aide tout au long du processus.

> [!NOTE]
> Lorsque vous exécutez la consolidation, vous pouvez choisir les sociétés à inclure. Si votre société consolidée n’a pas accès à une ou plusieurs filiales, le guide vous y accorde l’accès.

1. Connectez-vous à la société consolidée.  
2. Sur la page **Centres de profit**, choisissez l’action **Consolider**.  
3. Renseignez les champs requis.  

## <a name="use-the-consolidated-trial-balance-report"></a>Utiliser l’état Balance consolidée

L’état **Balance consolidé** peut vous donner un aperçu de leur santé financière dans leur ensemble. L’état regroupe les écritures comptables de chacune de vos sociétés dans une nouvelle société que vous créez pour stocker les données consolidées. La société consolidée est un conteneur pour les données consolidées, et ne contient pas de données métier en temps réel. Les sociétés que vous incluez dans la société consolidée deviennent des **centres de profit** dans l’état. Avec quatre centres de profit maximum, vous pouvez utiliser l’état **Balance consolidée (4 stés)**.  

L’état affiche une ligne pour chaque compte et suit la structure du plan comptable. Un compte n’est pas affiché si tous les montants de la ligne sont égaux à 0. L’état affiche les informations suivantes pour chaque compte :

* Le numéro de compte et le nom du compte.
* Les totaux pour la société consolidée et pour chaque centre de profit. Les totaux peuvent s’afficher comme solde période ou écriture ouverte.
* Les éliminations effectuées dans la société consolidée. Elles sont toujours affichées pour une période correspondant à l’exercice comptable de la société consolidée.
* Le total de la société consolidée après les éliminations, affiché comme solde période ou écriture ouverte.

## <a name="eliminate-repeated-transactions"></a>Éliminer les transactions répétées

Après que vous avez consolidé toutes les sociétés, vous devez rechercher toutes les transactions enregistrées dans plusieurs sociétés, puis valider les écritures d’élimination pour les supprimer. Le traitement d’éliminations de consolidation est un processus manuel.  

Pour éliminer les transactions répétées :

1. Recherchez des transactions qui doivent être ajustées potentiellement et entrez les lignes feuille comptabilité pour les éliminer.
2. Exécutez le rapport **Éliminations consolidation compta.** pour évaluer l’effet des lignes feuille comptabilité avant la validation.
3. Validez les transactions d’ajustement.

L’état **Éliminations consolidation compta.** affiche une balance provisoire dans laquelle vous pouvez simuler les conséquences de l’élimination des écritures. L’état compare les écritures dans l’entreprise consolidée avec les éliminations inscrites au journal général.

Pour que vous puissiez inclure un centre de profit dans l’état, vous devez le configurer sur la page **Centres de profit**. Assurez-vous d’activer le bouton bascule **Consolider**.

Une ligne est créée pour chaque compte s’affiche, selon la structure du plan comptable. Un compte n’est pas affiché si tous les montants de la ligne sont égaux à 0. L’état affiche les informations suivantes pour chaque compte :

* Numéro de compte.
* Nom du compte.
* Si vous avez sélectionné un ou plusieurs codes centre de profit dans le champ **Code centre de profit** de la page de demande, un total excluant les éliminations et les centres de profit sélectionnés est affiché pour la société consolidée. Si le champ **Code centre de profit** n’est pas renseigné, un total excluant les éliminations est affiché pour la société consolidée.
* Si vous avez sélectionné un code centre de profit dans le champ **Code centre de profit** de la page de demande, un total est affiché pour les écritures importées à partir du centre de profit. Si le champ **Code centre de profit** n’est pas renseigné, un total est affiché pour les éliminations validées dans la société consolidée.
* Le total de la société consolidée, avec tous les centres de profit et toutes les éliminations validées.
* Les éliminations effectuées dans la société consolidée. C’est-à-dire les écritures du journal général sélectionnées sur la page de demande.
* Le texte de validation copié à partir de la feuille comptabilité.
* Le total de la société consolidée après les éliminations, si elles sont validées.

## <a name="export-and-import-consolidated-data-between-databases"></a>Exporter et importer des données consolidées entre des bases de données

Si les données d’un centre de profit se trouvent dans une autre base de données, vous pouvez effectuer un transfert manuel basé sur un fichier ou automatiser le processus à l’aide d’une API. Pour en savoir plus sur l’API, consultez [Utiliser notre API pour partager automatiquement des données entre les environnements](#use-our-api-to-automatically-share-data-across-environments).

Cette section décrit le processus manuel basé sur un fichier.

Vous exportez les données vers un fichier avant de les inclure dans la consolidation. Exportez chaque société séparément en utilisant le traitement par lots **Exporter fichier consolidation**.  

> [!TIP]
> Utilisez le même processus pour exporter les données consolidées que vous devez envoyer à Dynamics 365 Finance. Par exemple, si le centre de profit est une filiale et que la société mère utilise Dynamics 365 Finance.

Après l’exécution du traitement par lots, toutes les écritures des comptes généraux sont traitées. Pour chaque combinaison d’axe principal et date sélectionnés, la valeur des champs **Montant** des écritures est totalisée et exportée. La combinaison suivante des axes analytiques et de la date sélectionnés avec le même numéro de compte est traitée. Ensuite, les combinaisons du numéro de compte suivant sont traitées, et ainsi de suite.  

Les écritures exportées contiennent les champs suivants : **N° compte**, **Date comptabilisation** et **Montant**. Si des informations analytiques ont également été exportées, des codes axe et des sections analytiques sont également inclus.  

1. Pour chaque ligne exportée, si le total des champs **Montant** est un débit, le numéro de compte configuré dans le champ **Compte débit consolidation** du centre de profit est exporté vers la ligne. Si le total est un crédit, le numéro correspondant dans le champ **Compte crédit consolidation** est exporté vers la ligne.  
2. La date utilisée pour chaque ligne exportée est la date de fin de la période ou, si le transfert est opéré chaque jour, la date du calcul.  
3. La section analytique exportée pour la saisie est celle de la société consolidée configurée dans le champ **Code consolidation** pour cette section analytique. Si aucune section analytique de société consolidée n’a été entrée dans le champ **Code consolidé** à cette fin, la section analytique proprement dite est exportée vers la ligne.  
4. Les fichiers XML contiennent également les taux de change devise correspondant à la période de consolidation. Ces taux sont inclus dans une section distincte au début du fichier.  

## <a name="use-our-api-to-automatically-share-data-across-environments"></a>Utiliser notre API pour partager automatiquement des données entre les environnements

[!INCLUDE [prod_short](includes/prod_short.md)] fournit une API qui vous permet d’automatiser le processus de partage des données financières entre les centres de profit et la société consolidée. L’API est gratuite à utiliser et facile à configurer. Elle vous permet même de partager des données entre différents environnements [!INCLUDE [prod_short](includes/prod_short.md)]. Par exemple, vous devrez peut-être partager des données entre différents environnements lorsque les centres de profit ne se trouvent pas dans les mêmes zones géographiques Azure. Pour en savoir plus sur l’utilisation de l’API pour automatiser le processus de consolidation, consultez [Configurer la consolidation de la société](finance-consolidated-company-reporting-setup.md#busunit).

## <a name="see-also"></a>Voir aussi

[Configuration de la consolidation de la société](finance-consolidated-company-reporting-setup.md)  
[Gestion des transactions intersociétés](intercompany-manage.md)  
[Utiliser [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  
[Exportation de vos données métier vers Excel](about-export-data.md)

[!INCLUDE[footer-include](includes/footer-banner.md)]
