---
title: Extension QuickBooks Data Migration
description: "Décrit comment utiliser l’extension pour importer des clients, des fournisseurs, des articles, et des comptes de QuickBooks Desktop dans Business\_Central."
author: edupont04
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 'app, add-in, manifest, customize, import, implement'
ms.search.form: '1911, 1912, 1913, 1914, 1915, 1916, 1918, 1919'
ms.date: 06/24/2021
ms.author: edupont
---

# <a name="the-quickbooks-data-migration-extension"></a>Extension QuickBooks Data Migration

Cette extension facilite la migration des clients, des fournisseurs, des articles et des comptes de QuickBooks vers [!INCLUDE[prod_short](includes/prod_short.md)]. Si votre entreprise utilise QuickBooks aujourd’hui, vous pouvez exporter les informations appropriées puis ouvrir un guide de configuration assistée pour télécharger les données vers [!INCLUDE[prod_short](includes/prod_short.md)].  
Pour plus d’informations, voir [Importation des données métier à partir d’autres systèmes financiers](across-import-data-configuration-packages.md).

## <a name="data-from-quickbooks-desktop"></a>Données de QuickBooks Desktop

Vous pouvez importer les données suivantes de QuickBooks Online vers Business Central :

- Clients  
- Fournisseurs  
- Articles  
- Plan comptable  
- Commencer les transactions de solde en comptabilité  
- Quantités disponibles pour les articles de stock  
- Ouvrir des documents pour les clients et les fournisseurs, par exemple des factures, des avoirs et des paiements  

Nous effectuons une migration uniquement pour les montants complets dans les documents achat et vente. Nous ne mettons pas à jour les montants partiellement payés. Par exemple, si un client a payé 300 dollars sur un total de 500 dollars dans une facture vente, nous effectuons une migration des 500 complets. Si vous avez reçu des paiements partiels, vous devez les mettre à jour manuellement, avant ou après la migration de données. Nous vous recommandons de lettrer les transactions ouvertes avant d’exécuter une migration, pour faciliter juste des éléments ensuite.

> [!NOTE]
> Nous n’effectuons pas de migration des commandes achat ou des commandes vente.

## <a name="before-you-start"></a>Avant de commencer

Une grande partie du processus de migration consiste à spécifier les comptes vers lesquels migrer les transactions. Il est judicieux de planifier ce mappage avant d’exécuter la migration de données. Par exemple, les comptes où vous validez des transactions :

- La vente d’articles ou de services à un client  
- L’achat d’articles ou de service auprès d’un fournisseur  
- Ajustements des écritures comptables  

Business Central nécessite que les comptes généraux aient des numéros de compte. S’assurer que les numéros de compte sont affectés aux comptes dans QuickBooks.
Si les transactions de QuickBooks ont des montants de taxe, vous devez créer un compte taxes pour vos administrations fiscales dans Business Central avant de pouvoir valider des transactions.

Afin d’obtenir vos données de l’application QuickBooks Desktop vous devez télécharger l’outil d’exportation de données Microsoft.  Les instructions de l’outils sont dans l’Assistant Migration de données dans [!INCLUDE[prod_short](includes/prod_short.md)]. L’outil se connectera à votre application QuickBooks et exporter les données applicables à un fichier .zip.  

> [!NOTE]
> Actuellement, l’outil d’exportation de données fonctionne uniquement avec QuickBooks 2017 et 2018.

## <a name="finding-the-quickbooks-data-migration-extension"></a>Recherche de l’extension QuickBooks Data Migration

L’extension QuickBooks Data Migration est installée et prête à être utilisée comme partie intégrante du guide de configuration assistée Migration des données. Si vous êtes prêt à commencer maintenant et à exporter vos données depuis QuickBooks, choisissez l’![Ampoule qui ouvre la fenêtre de recherche.](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire") saisissez **Configuration assistée**, puis choisissez le lien associé. Choisissez **Migrer des données métier**, puis suivez les étapes du guide.  

## <a name="what-do-i-do-after-i-migrate-data"></a>Que faire après une migration des données ?

Après avoir effectué une migration des données, les transactions ont le statut Non validé, vous pouvez les consulter et faire des ajustements. Pour consulter les transactions, accédez à la page où vous les trouveriez normalement. Par exemple, pour examiner les factures vente non validées, accédez à la page Factures vente. Pour consulter des feuilles paiement, accédez à la page Feuilles paiement.
Il existe quelques éléments en particulier que vous devez effectuer : si les transactions dans QuickBooks avaient les montants de majoration ou de remise, vous devez ajouter manuellement les montants aux transactions associées dans Business Central avant de les valider.
Si vous utilisez la taxe sur la valeur ajoutée (TVA), vous devez ajouter un groupe comptabilisation marché et un groupe comptabilisation produit au paramétrage de la validation de manière à pouvoir valider les montants TVA.
Vérifiez les soldes de début des comptes du grand livre. QuickBooks ne stocke pas le solde actuel de tous les comptes, vous pouvez être amené à corriger les soldes d’ouverture.

## <a name="see-related-microsoft-training"></a>Voir la [formation Microsoft](/training/modules/migrate-data-dynamics-365-business-central/) associée

## <a name="see-also"></a>Voir aussi

[Importation des données métier à partir d’autres systèmes financiers](across-import-data-configuration-packages.md)  
[Personnalisation de [!INCLUDE[prod_short](includes/prod_short.md)] à l’aide des extensions](ui-extensions.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
