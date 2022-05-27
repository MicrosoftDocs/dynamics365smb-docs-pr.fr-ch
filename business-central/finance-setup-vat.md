---
title: Configuration de la TVA
description: Assurez-vous de calculer, de valider et de déclarer correctement la TVA pour les ventes et les achats. Il est recommandé d’utiliser le guide de configuration assistée pour configurer la TVA.
author: brentholtorf
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: VAT, posting, tax, value-added tax
ms.search.form: 10, 1877, 470, 471, 472
ms.date: 04/12/2022
ms.author: bholtorf
ms.openlocfilehash: 98a190594dbd2b37f949bdc51e7f810dd739b769
ms.sourcegitcommit: 4853614c85beb347091c5c4c1ea8d974dec887fc
ms.translationtype: HT
ms.contentlocale: fr-CH
ms.lasthandoff: 05/11/2022
ms.locfileid: "8740326"
---
# <a name="set-up-calculations-and-posting-methods-for-value-added-tax"></a>Configurer des méthodes de calcul et de validation de la taxe sur la valeur ajoutée

Les clients et les entreprises payent la TVA lorsqu’ils achètent des biens ou des services. Le montant de la TVA à payer peut varier en fonction de plusieurs facteurs. Dans [!INCLUDE[prod_short](includes/prod_short.md)], vous configurez la TVA pour spécifier les taux à utiliser pour calculer les montants de taxe sur la base des paramètres suivants :

* À qui vous vendez  
* À qui vous achetez  
* Ce que vous vendez  
* Ce que vous achetez  

Vous pouvez configurer manuellement les calculs de la TVA, mais cette procédure peut être délicate et longue. Pour vous faciliter la tâche, nous avons fourni un guide de configuration assistée appelé **Paramètres TVA** pour vous aider. Il est recommandé d’utiliser le guide de configuration assistée pour configurer la TVA.

> [!NOTE]  
> Vous pouvez utiliser le guide uniquement si vous avez créé un profil Ma société, et si vous n’avez pas validé de transactions incluant la TVA. Sinon, il serait très facile d’utiliser différents taux de TVA par erreur et de générer des états de TVA erronés.  

Si vous souhaitez configurer vous-même les calculs de TVA, ou en savoir plus sur chaque étape, cet article contient des descriptions de chaque étape.  

[!INCLUDE [finance-vat](includes/finance-vat.md)]

## <a name="use-the-vat-setup-assisted-setup-guide-to-set-up-vat-recommended"></a>Utiliser le guide de configuration assistée Paramètres TVA pour configurer la TVA (recommandé)

Il est recommandé d’utiliser le guide de configuration assistée Paramètres TVA pour configurer la TVA dans [!INCLUDE[prod_short](includes/prod_short.md)].

Pour démarrer le guide de configuration assistée, procédez comme suit :

1. Sélectionnez l’icône en forme ![d’ampoule qui ouvre la fonction de recherche 1.](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire") entrez **Configuration assistée**.  
2. Choisissez **Configuration TVA** et finalisez la procédure.
3. Une fois la configuration assistée terminée, visitez la page **Paramètres comptabilisation TVA** et vérifiez si vous devez renseigner d’autres champs en fonction des exigences locales de votre version de [!INCLUDE [prod_short](includes/prod_short.md)]. Pour plus d’informations, voir [Fonctionnalité locale dans Business Central](about-localization.md).  

### <a name="check-the-vat-posting-setup"></a>Vérifier les paramètres comptabilisation TVA

Pour vous aider à démarrer rapidement, [!INCLUDE [prod_short](includes/prod_short.md)] affichera des notifications s’il vous manque des comptes du grand livre général (G/L) dans les groupes comptabilisation ou les paramètres comptabilisation, par exemple la page **Paramètres comptabilisation TVA**. Vous pouvez activer ou désactiver ce type de notification à l’aide de la notification *Compte général manquant dans le groupe comptabilisation ou la configuration* de la page **Mes notifications**. Il vous suffit d’accéder à la page **Mes paramètres**, puis de choisir *Modifier lorsque je reçois des notifications*. .  

Si vous choisissez une telle notification, [!INCLUDE [prod_short](includes/prod_short.md)] crée automatiquement ces paramètres comptabilisation en fonction des groupes comptabilisation du document ou de la feuille que vous utilisez actuellement.  

À ce stade, vous pouvez simplement remplir les comptes généraux manquants. Puis, plus tard, lorsque vous affinez davantage les paramètres, il est possible que vous réalisiez que cette configuration n’est pas correcte. [!INCLUDE [prod_short](includes/prod_short.md)] n’autorise pas la suppression des paramètres comptabilisation TVA ni des paramètres comptabilisation lorsqu’il existe des écritures créées à partir de telles configurations. À partir de la 1re vague de lancement 2022, vous pouvez utiliser le champ **Bloqué** sur la page **Paramètres comptabilisation TVA** pour empêcher les utilisateurs d’utiliser par erreur une configuration qui n’est plus pertinente pour les nouvelles validations.

## <a name="set-up-vat-registration-numbers-for-your-country-or-region"></a>Configurer les numéros d’identification intracommunautaire pour votre pays ou région

Pour garantir que les personnes entrent des numéros d’identification intracommunautaire valides, vous pouvez définir des formats pour les numéros d’identification intracommunautaire utilisés dans des pays ou des régions dans lesquels vous travaillez. [!INCLUDE[prod_short](includes/prod_short.md)] affichera un message d’erreur lorsque un employé fait une erreur ou utilise un format incorrect pour le pays ou la région.

Pour configurer des numéros d’identification intracommunautaire, procédez comme suit :

1. Sélectionnez l’icône en forme ![d’ampoule qui ouvre la fonction de recherche 2.](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire") entrez **Pays/Régions**.
2. Choisissez le pays ou la régions, puis cliquez sur **Formats n° identif. intracomm**.
3. Dans le champ **Formats**, définissez le format en saisissant un ou plusieurs des caractères suivants :  

* **#** Requiert un numéro à un seul chiffre.  
* **@** Requiert une lettre. Ce format n’est pas sensible à la casse.  
* **?** Tout caractère est autorisé.  

    > [!Tip]
    > Vous pouvez utiliser d’autres caractères tant qu’ils sont présents dans le format du pays ou de la région. Par exemple, si vous souhaitez inclure un point ou un trait d’union entre des séries de chiffres, vous pouvez définir le format sous la forme ##.####.### ou @@-###-###.  

## <a name="set-up-vat-business-posting-groups"></a>Configurer des groupes comptabilisation marché TVA

Les groupes comptabilisation marché TVA doivent représenter les marchés dans lesquels vous faites des affaires avec les clients et fournisseurs, et définissent comment calculer et valider la TVA dans chaque marché. Des exemples de groupes comptabilisation marché TVA sont **France** et **Union Européenne (UE)**.  

Utilisez des codes faciles à retenir et qui décrivent le groupe comptabilisation marché, tels que **UE**, **Non-UE** ou **France**. Le code doit être unique. Vous pouvez créer autant de codes que vous le souhaitez, mais vous ne pouvez pas avoir le même code deux fois dans une table.

Pour configurer un groupe comptabilisation marché TVA, procédez comme suit :

1. Sélectionnez l’icône en forme ![d’ampoule qui ouvre la fonction de recherche 3.](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire") entrez **Groupe compta. marché TVA**, puis choisissez le lien associé.  
2. Renseignez les champs selon vos besoins.

Paramétrez les groupes comptabilisation marché TVA par défaut en les liant à des groupes comptabilisation marché. [!INCLUDE[prod_short](includes/prod_short.md)] affecte automatiquement le groupe comptabilisation marché TVA lorsque vous affectez le groupe comptabilisation marché à un client, un fournisseur ou un compte général.

## <a name="set-up-vat-product-posting-groups"></a>Configurer des groupes comptabilisation produit TVA

Les groupes comptabilisation produit TVA représentent les articles et les ressources que vous achetez ou vendez et déterminent la manière de calculer et de valider la TVA en fonction du type d’article ou de ressource acheté ou vendu.  
Il est recommandé d’utiliser des codes faciles à retenir et qui décrivent le taux, par exemple **SANS TVA** ou **Zéro**, **TVA10** ou **Réduite** pour 10 % de TVA, et **TVA25** ou **Standard** pour 25 %.

Pour configurer un groupe comptabilisation marché TVA, procédez comme suit :

1. Sélectionnez l’icône en forme ![d’ampoule qui ouvre la fonction de recherche 4.](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire") entrez **Groupes compta. produit TVA**, puis choisissez le lien associé.  
2. Renseignez les champs selon vos besoins.

## <a name="combine-vat-posting-groups-in-vat-posting-setups"></a>Regrouper des groupes comptabilisation TVA dans les paramètres comptabilisation TVA

[!INCLUDE[prod_short](includes/prod_short.md)] calcule les montants de TVA sur les ventes et les achats en fonction des paramètres comptabilisation TVA, qui sont des combinaisons de groupes comptabilisation marché et produit TVA. Pour chaque combinaison, vous pouvez spécifier le pourcentage de TVA, le mode calcul TVA et les comptes généraux pour la validation de la TVA pour les achats, les ventes, ainsi que les taxes déductibles. Vous pouvez également indiquer si la TVA doit être recalculée lorsqu’un escompte est appliqué ou reçu.  

Définissez autant de combinaisons que nécessaire. Si vous voulez regrouper des combinaisons de paramètres comptabilisation TVA avec des attributs similaires, vous pouvez définir un **Identifiant TVA** pour chaque groupe et affecter l’identifiant aux membres du groupe.

Pour regrouper des paramètres comptabilisation TVA, procédez comme suit :

1. Sélectionnez l’icône en forme ![d’ampoule qui ouvre la fonction de recherche 5.](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire") entrez **Paramètres comptabilisation TVA**, puis choisissez le lien associé.
2. Renseignez les champs selon vos besoins. [!INCLUDE [tooltip-inline-tip_md](includes/tooltip-inline-tip_md.md)]

## <a name="assign-vat-posting-groups-by-default-to-multiple-entities"></a>Affecter des groupes comptabilisation TVA par défaut à plusieurs entités

Si vous souhaitez appliquer les mêmes groupes comptabilisation TVA à plusieurs entités, vous pouvez configurer [!INCLUDE[prod_short](includes/prod_short.md)] pour le faire par défaut. Plusieurs méthodes sont disponibles :

* Vous pouvez affecter des groupes comptabilisation marché aux groupes comptabilisation marché généraux ou aux modèles client ou fournisseur
* Vous pouvez affecter des groupes comptabilisation produit TVA aux groupes comptabilisation produit généraux  

Le groupe comptabilisation marché ou produit TVA est affecté lorsque vous choisissez un groupe comptabilisation marché ou produit pour un client, un fournisseur, un article ou une ressource.

## <a name="assign-vat-posting-groups-to-accounts-customers-vendors-items-and-resources"></a>Affecter des groupes comptabilisation TVA à des comptes, clients, fournisseurs, articles et ressources

Les sections suivantes décrivent comment affecter des groupes comptabilisation TVA à des entités individuelles.

### <a name="to-assign-vat-posting-groups-to-individual-general-ledger-accounts"></a>Pour affecter des groupes comptabilisation TVA à des comptes généraux individuels

1. Sélectionnez l’icône en forme ![d’ampoule qui ouvre la fonction de recherche 6.](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire") entrez **Plan comptable**, puis choisissez le lien associé.  
2. Ouvrez la fiche **Compte général** pour le compte.  
3. Sous le raccourci **Comptabilisation**, dans le champ **Type compta. TVA**, choisissez **Vente** ou **Achat**.  
4. Choisissez les groupes comptabilisation TVA à utiliser pour le compte vente ou achat.  

### <a name="to-assign-vat-business-posting-groups-to-customers-and-vendors"></a>Pour affecter des groupes comptabilisation marché TVA à des clients et des fournisseurs

1. Sélectionnez l’icône en forme ![d’ampoule qui ouvre la fonction de recherche 7.](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire") entrez **Client** ou **Fournisseur**, puis choisissez le lien associé.  
2. Sur la fiche **Client** ou **Fournisseur**, développez le raccourci **Facturation**.  
3. Choisissez le groupe comptabilisation marché TVA.  

### <a name="to-assign-vat-product-posting-groups-to-individual-items-and-resources"></a>Pour affecter des groupes comptabilisation produit TVA à des articles et des ressources individuels

1. Sélectionnez l’icône en forme ![d’ampoule qui ouvre la fonction de recherche 8.](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire"), entrez **Article** ou **Ressource**, puis choisissez le lien associé.  
2. Exécutez l’une des opérations suivantes :  

    * Sur la fiche **Article**, développez le raccourci **Prix et validation**, puis sélectionnez **Afficher plus** pour afficher le champ **Groupe compta. produit TVA**.  
    * Sur la fiche **Ressource**, développez le raccourci **Facturation**.  
3. Choisissez le groupe comptabilisation produit TVA.  

## <a name="set-up-clauses-to-explain-vat-exemption-or-non-standard-vat-rates"></a>Configurer des clauses pour expliquer l’exonération de TVA ou les taux de TVA non standard

Vous définissez une clause TVA afin de décrire le type de TVA qui est appliquée. Les informations peuvent être requises par une réglementation gouvernementale. Après avoir configuré une clause TVA et l’avoir associée à un paramètre validation TVA, la clause TVA est affichée sur les documents vente imprimés qui utilisent le groupe de paramètres validation TVA.

Si nécessaire, vous pouvez également spécifier comment convertir les clauses TVA dans d’autres langues. Ensuite, lorsque vous créez et imprimez un document vente qui contient un identifiant TVA, le document comprend la clause TVA traduite. Le code langue spécifié sur la fiche client détermine la langue.

Lorsque des taux de TVA non standard sont utilisés dans différents types de documents, tels que des factures ou des avoirs, les entreprises sont généralement tenues d’inclure un texte d’exonération (clause de TVA) indiquant les raisons pour lesquelles un taux de TVA réduit ou nul a été calculé. Vous pouvez définir différentes clauses de TVA à inclure dans les documents commerciaux en fonction du type de document, telles que facture ou avoir. Pour ce faire, accédez à la page **Clauses TVA par type doc.**.

Vous pouvez modifier ou supprimer une clause TVA, et les modifications que vous apportez seront visibles dans un état généré. Toutefois, [!INCLUDE[prod_short](includes/prod_short.md)] ne crée pas d’historique des modifications. Sur l’état, les désignations des clauses TVA sont imprimées et affichées pour toutes les lignes de l’état à côté du montant de la TVA et du montant de base de la TVA. Si aucune clause TVA n’a été définie pour les lignes du document vente, la totalité de la section est omise lors de l’impression de l’état.

### <a name="to-set-up-vat-clauses"></a>Pour configurer des clauses TVA

1. Sélectionnez l’icône en forme ![d’ampoule qui ouvre la fonction de recherche 9.](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire"), entrez **Clauses TVA**, puis choisissez le lien associé.  
2. Sur la page **Clauses TVA**, créez une ligne.  
3. Dans le champ **Code**, entrez un identificateur pour la clause. Vous utilisez ce code pour affecter la clause à des groupes comptabilisation TVA.  
4. Dans le champ **Description**, saisissez le texte d’exonération de TVA que vous souhaitez afficher sur les documents pouvant inclure la TVA. Dans le champ **Description 2**, entrez du texte supplémentaire, si nécessaire. Le texte sera affiché sur de nouvelles lignes.
5. Choisissez l’action **Description par type de document**.
6. Sur la page **Clauses TVA par type doc.**, remplissez les champs pour définir quel texte d’exonération de TVA afficher sur quel type de document.  
7. Facultatif : pour affecter immédiatement la clause TVA à un paramètre comptabilisation TVA, sélectionnez **Paramètres**, puis sélectionnez la clause. Si vous souhaitez attendre, vous pouvez affecter la clause ultérieurement dans la page **Paramètres comptabilisation TVA**.  
8. Facultatif : pour spécifier comment traduire la clause TVA, sélectionnez l’action **Traductions**.

### <a name="to-assign-a-vat-clause-to-a-vat-posting-setup"></a>Pour affecter une clause TVA à un paramètre comptabilisation TVA

1. Sélectionnez l’icône en forme ![d’ampoule qui ouvre la fonction de recherche 10.](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire"), entrez **Paramètres comptabilisation TVA**, puis choisissez le lien associé.  
2. Dans la colonne **Clause TVA**, choisissez la clause à utiliser pour chaque paramètre comptabilisation TVA auquel elle s’applique.  

### <a name="to-specify-translations-for-vat-clauses"></a>Pour spécifier des traductions pour les clauses TVA

1. Sélectionnez l’icône en forme ![d’ampoule qui ouvre la fonction de recherche 11.](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire"), entrez **Clauses TVA**, puis choisissez le lien associé.  
2. Sélectionnez l’option **Traductions**.  
3. Dans le champ **Code langue**, sélectionnez la langue de traduction.  
4. Dans les champs **Description** et **Description 2**, saisissez les traductions des descriptions. Ce texte s’affiche dans les documents état de TVA traduits.  

## <a name="create-a-vat-posting-setup-to-handle-import-vat"></a>Créer un paramètre comptabilisation TVA pour traiter la TVA à l’importation

Utilisez la fonction *TVA à l’importation* pour valider un document dont le montant est en TVA. Elle est utile lorsque vous recevez une facture des autorités fiscales pour la TVA sur les biens importés.  

Pour configurer des codes pour la TVA à l’importation, procédez comme suit :  

1. Sélectionnez l’icône en forme ![d’ampoule qui ouvre la fonction de recherche 12.](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire"), entrez **Groupes compta. produit TVA**, puis choisissez le lien associé.  
2. Sur la page Groupes compta. produit TVA, configurez un groupe comptabilisation produit TVA pour la TVA à l’importation.  
3. Sélectionnez l’icône en forme ![d’ampoule qui ouvre la fonction de recherche 13.](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire"), entrez **Paramètres comptabilisation TVA**, puis choisissez le lien associé.  
4. Sur la page Paramètres compta. TVA, créez une ligne ou utilisez l’un des groupes comptabilisation marché TVA existants en combinaison avec le nouveau groupe comptabilisation produit TVA créé pour la TVA à l’importation.  
5. Dans le champ **Mode calcul TVA**, sélectionnez **Exclusivement TVA**.  
6. Dans le champ **Compte TVA achat**, indiquez le compte général à utiliser pour valider la TVA à l’importation. Tous les autres comptes sont facultatifs.  

## <a name="use-reverse-charge-vat-for-trade-between-eu-countries-or-regions"></a>Utiliser une TVA déductible pour le commerce entre pays/régions de l’UE

Certaines sociétés doivent utiliser une TVA déductible dans leurs échanges avec d’autres sociétés. Par exemple, cette règle s’applique aux achats effectués dans des pays/régions de l’Union européenne et les ventes aux pays/régions de l’Union européenne.  

> [!NOTE]  
> Cette règle s’applique aux échanges avec des sociétés enregistrées comme assujetties à la TVA dans un autre pays/régions de l’UE. Si vous commercez directement avec des clients dans d’autres pays/régions de l’UE, nous vous recommandons de prendre contact avec votre administration fiscale afin d’obtenir des informations sur les règles applicables en matière de TVA.  

> [!TIP]  
> Vous pouvez vérifier qu’une société est enregistrée comme assujettie à la TVA dans un autre pays de l’UE en utilisant le service de validation des numéros d’identification de TVA de l’UE. Le service est disponible gratuitement dans [!INCLUDE[prod_short](includes/prod_short.md)]. Pour plus d’informations, consultez [Vérifier les numéros d’identification intracommunautaire](finance-how-validate-vat-registration-number.md).

### <a name="sales-to-eu-countries-or-regions"></a>Ventes dans des pays/régions de l’UE

La TVA n’est pas calculée sur les ventes à des sociétés assujetties à la TVA situées dans d’autres pays/régions de l’UE. Vous devez déclarer la valeur de ces ventes séparément dans votre déclaration de TVA.  

Pour calculer correctement la TVA sur les ventes effectuées dans des pays/régions de l’UE, vous devez procéder comme suit :  

* Configurez une ligne pour les ventes contenant les mêmes informations que pour les achats. Si vous avez déjà configuré des lignes sur la page Paramètres compta. TVA pour les achats effectués dans des pays/régions de l’UE, vous pouvez également utiliser ces lignes pour les ventes.  
* Affectez des groupes comptabilisation marché TVA dans le champ **Groupe compta. marché TVA** sur le raccourci **Facturation** de la fiche de chaque client de l’UE. Vous devez également saisir le numéro d’identification de la TVA client dans le champ **N° identif. intracomm.** sur le raccourci **International**.  

Lorsque vous validez une vente à un client situé dans un autre pays/une autre région de l’UE, le montant de TVA est calculé et une écriture TVA est créée à l’aide des informations sur la TVA déductible et la base TVA (montant utilisé pour calculer la TVA). Aucune écriture n’est validée dans les comptes TVA de la comptabilité.

## <a name="vat-rounding-for-documents"></a>Arrondi TVA pour les documents

Les montants figurant dans les documents qui n’ont pas encore été validés sont arrondis et affichés de façon à correspondre à l’arrondi final des montants réellement validés. La TVA est calculée pour un document terminé, ce qui signifie que la TVA calculée est basée sur la somme de toutes les lignes ayant le même identifiant TVA dans le document.  

## <a name="set-up-vat-reporting"></a>Configurer la déclaration TVA

Vous devez configurer des informations sur la façon dont les autorités fiscales de votre pays/région exigent que vous soumettiez des déclarations de TVA. Les étapes suivantes illustrent les informations les plus couramment utilisées. Cependant, votre pays/région peut nécessiter des étapes supplémentaires. Pour plus d’informations, consultez l’article correspondant dans la section *Fonctionnalité locale* du volet de gauche.

[!INCLUDE [vat-report-setup](includes/vat-report-setup.md)]

## <a name="see-also"></a>Voir aussi

[Paramétrer des modèles de déclaration de TVA et des noms de déclaration de TVA](finance-how-setup-vat-statement.md)  
[Configurer la TVA sur encaissement](finance-setup-unrealized-vat.md)  
[Déclarer la TVA à une autorité fiscale](finance-how-report-vat.md)  
[Utiliser la TVA sur les ventes et les achats](finance-work-with-vat.md)  
[Utiliser l’outil de modification du taux de TVA](finance-how-use-vat-rate-change-tool.md)  
[Vérifier les numéros d’identification intracommunautaire](finance-how-validate-vat-registration-number.md)  
[Fonctionnalités locales dans Business Central](about-localization.md)  
[Déclaration de TVA dans la version allemande](LocalFunctionality/Germany/vat-reporting.md)  
[TVA belge](LocalFunctionality/Belgium/belgian-vat.md)  
[TVA, Italie](LocalFunctionality/Italy/italian-vat.md)  
[Paramétrer les déclarations TVA et ICP électroniques dans la version néerlandaise](LocalFunctionality/Netherlands/how-to-set-up-electronic-vat-and-icp-declarations.md)  
[États de TVA dans la version espagnole](LocalFunctionality/Spain/vat-reports.md)  
[Configurer la validation de la taxe sur les biens et services dans la version australienne](LocalFunctionality/Australia/how-to-set-up-goods-and-service-tax-posting.md)  
[TVA dans la version tchèque](LocalFunctionality/Czech/finance-vat.md)  
[Déclaration de TVA dans la version norvégienne](LocalFunctionality/Norway/norwegian-vat-reporting.md)  
[Déclaration de la taxe sur les biens/services et de la taxe de vente harmonisée au Canada](LocalFunctionality/Canada/sales-tax-goods-services.md)  

## <a name="see-related-training-at-microsoft-learn"></a>Voir la formation associée sur [Microsoft Learn](/learn/paths/process-vat-dynamics-365-business-central/)


[!INCLUDE[footer-include](includes/footer-banner.md)]
