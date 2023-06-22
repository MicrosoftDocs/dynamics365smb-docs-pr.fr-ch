---
title: Consolider les données de plusieurs sociétés
description: Cet article explique comment vous pouvez consolider les écritures comptables d’au moins deux sociétés séparées (filiales) dans une société consolidée.
author: brentholtorf
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 'consolidation, subsidiaries, consolidate'
ms.search.form: '1826, 1827'
ms.date: 09/29/2022
ms.author: bholtorf
---

# <a name="consolidating-financial-data-from-multiple-companies" />Consolidation des données financières de plusieurs sociétés

Certaines organisations utilisent [!INCLUDE [prod_short](includes/prod_short.md)] dans plusieurs centres de profit ou entités juridiques. D’autres utilisent [!INCLUDE [prod_short](includes/prod_short.md)] dans les filiales qui doivent rendre compte aux organisations mères. Dans les deux cas, les comptables utilisent des outils intégrés pour aider à consolider les données financières.  

Vous pouvez consolider les écritures comptables d’au moins deux sociétés séparées (filiales) dans une société consolidée. Chaque société individuelle impliquée dans une consolidation est appelée centre de profit. La société résultant de la combinaison est appelée société consolidée.  

Vous pouvez importer des données dans la société consolidée à partir d’autres sociétés de le même abonné [!INCLUDE [prod_short](includes/prod_short.md)], des abonnés ou des fichiers.  

Si les états financiers d’un centre de profit sont dans une devise différente de celle utilisée dans la société consolidée, vous devez configurer les taux de change pour la consolidation.  

Vous pouvez consolider :  

* des sociétés avec plusieurs plans comptables ;  
* des sociétés qui utilisent plusieurs exercices comptables et devises ;  
* la totalité ou un pourcentage des informations financières d’une société ;
* en utilisant plusieurs taux de change dans des comptes généraux individuels.
* Entreprises dans d’autres programmes de gestion comptable et d’entreprise

Vous configurez la société consolidée de la même manière que vous configurez d’autres sociétés. Le plan comptable est indépendant des plans comptables des centres de profit. Le plan comptable des centres de profit peut différer les uns des autres. Vous configurez une liste de sociétés à consolider, vérifiez les données comptables avant leur consolidation, importez des fichiers ou des bases de données et générez des états de consolidation. Pour plus d’informations, voir [Configurer la consolidation de la société](finance-consolidated-company-reporting-setup.md).  

> [!TIP]
> La consolidation des données financières peut être particulièrement appropriée en association avec des processus intersociétés. Pour plus d’informations, voir [Gestion des transactions intersociétés](intercompany-manage.md).

## <a name="use-the-consolidated-trial-balance-report" />Utiliser l’état Balance consolidée

L’état **Balance consolidé** peut vous donner un aperçu de leur santé financière dans leur ensemble. L’état regroupe les écritures comptables de chacune de vos sociétés dans une nouvelle société que vous créez pour stocker les données consolidées. Cette société est généralement appelée *société consolidée*. La société consolidée est un conteneur pour les données consolidées, et ne contient pas de données métier en temps réel. Les sociétés que vous incluez dans la société consolidée deviennent des **centres de profit** dans l’état. Pour plus d’informations, voir [Configurer la consolidation de la société](finance-consolidated-company-reporting-setup.md). Avec quatre centres de profit maximum, vous pouvez utiliser l’état **Balance consolidée (4 stés)**.  

L’état affiche une ligne pour chaque compte et suit la structure du plan comptable. Un compte n’est pas affiché si tous les montants de la ligne sont égaux à 0. L’état affiche les informations suivantes pour chaque compte :

* Le numéro de compte et le nom du compte.
* Les totaux pour la société consolidée et pour chaque centre de profit. Les totaux peuvent s’afficher comme solde période ou écriture ouverte.
* Les éliminations effectuées dans la société consolidée. Elles sont toujours affichées pour une période correspondant à l’exercice comptable de la société consolidée.
* Le total de la société consolidée après les éliminations, affiché comme solde période ou écriture ouverte.

## <a name="consolidate-data" />Consolider les données

Le processus de transfert des chiffres des centres de profit vers la société consolidée est la *consolidation* à proprement parler. Avant de réaliser la consolidation, il peut être intéressant de rechercher les éventuelles différences entre les informations de base dans les centres de profit et dans la société consolidée. Il existe deux états que vous pouvez utiliser pour tester la base de données et le fichier.

### <a name="to-test-the-data-before-you-consolidate" />Pour tester les données avant la consolidation

Testez vos données avant de les transférer vers la société consolidée. [!INCLUDE[prod_short](includes/prod_short.md)] recherche des différences dans les informations des centres de profit et de la société consolidée. Par exemple, si les numéros de compte ou les codes axe sont différents. Vous devez corriger les erreurs avant d’exécuter l’état. Vous pouvez tester la base de données ou, si vous importez des données à partir d’un fichier XML, vous pouvez tester le fichier.  

1. Ouvrez la société consolidée.  
2. Sélectionnez l’icône ![Ampoule qui ouvre la fonction Tell Me.](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire") entrez **Centres de profit**, puis choisissez le lien associé.  
3. Testez le fichier et la base de données, comme suit :  

    * Pour tester un fichier, choisissez l’action **Tester fichier**, entrez le nom du fichier à tester, puis choisissez **Imprimer**.  
    * Pour tester la base de données, choisissez **Tester base de données**.  

### <a name="run-the-consolidation" />Exécuter la consolidation

Une fois les données testées, vous pouvez les transférer vers la société consolidée.  

1. Connectez-vous à la société consolidée.  
2. Dans le **Tableau de bord Comptable**, choisissez l’action **Exécuter la consolidation**.  
3. Renseignez les champs requis.  
4. Dans la section Filtre, définissez un filtre pour le centre de profit ou le nom de l’entreprise concerné.  
5. Planifiez éventuellement l’état à exécuter à une heure spécifique.  

## <a name="eliminate-repeated-transactions" />Éliminer les transactions répétées

Après que vous avez consolidé toutes les sociétés, vous devez rechercher toutes les transactions enregistrées dans plusieurs sociétés, puis valider les écritures d’élimination pour les supprimer. Le traitement d’éliminations de consolidation est un processus manuel.  

Pour éliminer les transactions répétées :

1. Recherchez des transactions qui doivent être ajustées potentiellement et entrez les lignes feuille comptabilité pour les éliminer.
2. Exécutez le rapport **Éliminations consolidation compta.** pour évaluer l’effet des lignes feuille comptabilité avant la validation.
3. Validez les transactions d’ajustement.

L’état **Éliminations consolidation compta.** affiche une balance provisoire dans laquelle vous pouvez simuler les conséquences de l’élimination des écritures. L’état compare les écritures dans l’entreprise consolidée avec les éliminations inscrites au journal général.

Pour qu’un centre de profit puisse être inclus dans un état, il doit être défini sur la page **Centres de profit**. Le champ **Consolider** doit être sélectionné.

Une ligne est créée pour chaque compte s’affiche, selon la structure du plan comptable. Un compte n’est pas affiché si tous les montants de la ligne sont égaux à 0. Les informations suivantes sont données pour chaque compte :

* Numéro de compte.
* Nom du compte.
* Si vous avez sélectionné un ou plusieurs codes centre de profit dans le champ **Code centre de profit** de la page de demande, un total excluant les éliminations et les centres de profit sélectionnés est affiché pour la société consolidée. Si le champ **Code centre de profit** n’est pas renseigné, un total excluant les éliminations est affiché pour la société consolidée.
* Si vous avez sélectionné un code centre de profit dans le champ **Code centre de profit** de la page de demande, un total est affiché pour les écritures importées à partir du centre de profit. Si le champ **Code centre de profit** n’est pas renseigné, un total est affiché pour les éliminations validées dans la société consolidée.
* Le total de la société consolidée, avec tous les centres de profit et toutes les éliminations validées.
* Les éliminations effectuées dans la société consolidée. C’est-à-dire les écritures du journal général sélectionnées sur la page de demande.
* Le texte de validation copié à partir de la feuille comptabilité.
* Le total de la société consolidée après les éliminations, si elles sont validées.

## <a name="export-and-import-consolidated-data-between-databases" />Exporter et importer des données consolidées entre des bases de données

Si les données d’un centre de profit se trouvent dans une autre base de données, vous devez exporter les données dans un fichier avant de les inclure dans la consolidation. Chaque société doit être exportée séparément. À cette fin, utilisez le traitement par lots **Exporter fichier consolidation**.  

> [!TIP]
> Utilisez le même processus pour exporter les données consolidées qui doivent être soumises à Dynamics 365 Finance, par exemple si le centre de profit actuel est une filiale et que la société mère utilise Dynamics 365 Finance.

Après l’exécution du traitement par lots, toutes les écritures des comptes généraux sont traitées. Pour chaque combinaison d’axe principal et date sélectionnés, la valeur des champs **Montant** des écritures est totalisée et exportée. La combinaison suivante des axes analytiques et de la date sélectionnés avec le même numéro de compte est traitée. Ensuite, les combinaisons du numéro de compte suivant sont traitées, et ainsi de suite.  

Les écritures exportées contiennent les champs suivants : **N° compte**, **Date comptabilisation** et **Montant**. Si des informations analytiques ont également été exportées, des codes axe et des sections analytiques sont également inclus.  

1. Pour chaque ligne exportée, si le total des champs **Montant** est un débit, le numéro de compte configuré dans le champ **Compte débit consolidation** du centre de profit est exporté vers la ligne. Si le total est un crédit, le numéro correspondant dans le champ **Compte crédit consolidation** est exporté vers la ligne.  
2. La date utilisée pour chaque ligne exportée est la date de fin de la période ou, si le transfert est opéré chaque jour, la date du calcul.  
3. La section analytique exportée pour la saisie est celle de la société consolidée configurée dans le champ **Code consolidation** pour cette section analytique. Si aucune section analytique de société consolidée n’a été entrée dans le champ **Code consolidé** à cette fin, la section analytique proprement dite est exportée vers la ligne.  
4. Les fichiers XML contiennent également les taux de change devise correspondant à la période de consolidation. Ces taux sont inclus dans une section distincte au début du fichier.  

## <a name="see-also" />Voir aussi

[Configurer la consolidation de la société](finance-consolidated-company-reporting-setup.md)  
[Gestion des transactions intersociétés](intercompany-manage.md)  
[Utiliser [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  
[Exportation de vos données métier vers Excel](about-export-data.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]
