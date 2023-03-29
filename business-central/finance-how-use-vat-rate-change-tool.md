---
title: Gérer les changements de taux TVA
description: Apprenez à utiliser l’outil de changement de taux de TVA pour Dynamics 365 Business Central pour modifier les taux de TVA en fonction de la législation locale.
author: andregu
ms.topic: conceptual
ms.reviewer: edupont
ms.workload: na
ms.search.keywords: 'VAT, VAT rate, posting, tax, value-added tax'
ms.search.form: '550,'
ms.date: 06/16/2021
ms.author: andregu
---

# Gérer les changements de taux TVA

Les taux TVA peuvent changer en fonction de la législation locale. Tout changement de TVA a un impact sur vos données [!INCLUDE[prod_short](includes/prod_short.md)] si le taux TVA est abaissé, augmenté ou supprimé. La TVA est liée à de nombreuses entités dans [!INCLUDE[prod_short](includes/prod_short.md)], telles que les clients, les fournisseurs, les articles, les ressources, les frais annexes et les comptes généraux. Les modifications des taux TVA se produisent généralement à une date spécifique, à partir de laquelle vous devrez modifier la configuration de la TVA, les groupes comptabilisation, etc. pour vous assurer que les nouvelles commandes vente et les commandes achat sont créés avec le nouveau taux TVA.

## Modification des taux TVA

L’approche optimale pour gérer un changement de taux TVA consiste à valider et clôturer entièrement les commandes en cours et autres documents avant la date de changement de taux TVA, afin de s’assurer qu’ils ne sont pas affectés par le changement. Il s’agit de l’approche la plus propre qui vous permet de démarrer de nouvelles commandes et documents avec le nouveau taux TVA.

L’approche suivante est suggérée pour gérer un changement de taux TVA

1. Validez et clôturez entièrement les commandes en cours, les journaux et autres documents avant la date de changement. Vous pouvez attendre après la date de changement tant que vous n’ajoutez pas de nouvelles lignes et vous assurer que la date effective sera antérieure à la date de changement.  
2. Créez la nouvelle configuration de TVA.  
3. Activez le changement de TVA sur les entités (clients, fournisseurs, articles appropriés, etc.).  
4. À la date de changement de taux TVA, vous créez de nouveaux documents qui utiliseront le nouveau taux.  


> [!NOTE]  
> Nous mettons actuellement à jour l’outil de modification du taux TVA. Les fonctionnalités mentionnées ci-dessous peuvent ne pas correspondre aux fonctionnalités de votre environnement. La mise à jour aura lieu avant le 1er juillet 2020 et ne sera pas une mise à jour mensuelle régulière. Au lieu de cela, tous les environnements seront mis à jour automatiquement (correctif). Une fois cette mise à jour terminée, ce message n’apparaîtra plus.  

## L’outil de modification du taux TVA

L’outil de modification du taux TVA peut aider à la conversion des taux TVA sur les données de base, les journaux et les commandes, dans une certaine mesure. Cela est utile si vous souhaitez convertir plus facilement la TVA sur les données de base ou si vous avez des commandes que vous ne pouvez pas clôturer avant la date de changement et qui seront traitées sur une plus longue période, dépassant la date de changement du taux TVA. Il existe certaines restrictions et limitations dans l’outil de modification du taux TVA qui s’applique.

## Familiarisation avec la conversion du taux TVA et limitations

L’outil de modification du taux TVA effectue des conversions de taux TVA pour les données principales, les feuilles et les commandes de différentes manières. Les données principales et les feuilles sélectionnées seront mises à jour par le groupe de comptabilisation du produit général ou le groupe de comptabilisation du produit TVA. Si une commande a été expédiée entièrement ou partiellement, les articles livrés conserveront le groupe de comptabilisation du produit général ou le groupe de comptabilisation du produit TVA actuel. Une nouvelle ligne de commande sera créée pour les articles non livrés et mis à jour pour uniformiser les groupes actuels et nouveaux de comptabilisation du produit général ou du produit TVA. En outre, les affectations de frais annexes, les modèles de configuration pour les articles, les réservations, ainsi que les informations sur la traçabilité seront mis à jour en conséquence. 

Sur les lignes de commande, le prix unitaire sera mis à jour pour toutes les lignes de type Article et Ressource, si utilisation des prix avec TVA pour l’article. Pour les autres types ligne, il est possible de décider si le prix unitaire doit être mis à jour ou non.

Quelques éléments ne sont pas convertis par l’outil :

* Commandes vente ou achat et factures pour lesquelles les expéditions ont été validées. Ces documents sont validés à l’aide du taux de TVA actuel.  
* Documents contenant des factures d’acompte validées. Par exemple, vous avez effectué ou reçu des acomptes sur les factures qui n’ont pas été réalisées avant d’utiliser l’outil de modification du taux de TVA. Dans ce cas, il existe une différence entre la TVA qui est due et la TVA qui a été payée dans les acomptes lorsque la facture est terminée. L’outil de modification du taux de TVA ignorera ces documents et vous devrez les mettre à jour manuellement.  
* Commandes vente ou achat avec l’intégration en entrepôt si elles sont livrées ou réceptionnées partiellement.  
* Livraisons directes.
* Commandes spéciales. 
* Ordres d’assemblage.
* Contrats de service.  
* Avoirs.
* Retours.
* Prix sur les articles (données de base)
* Prix sur les prix de vente (données de base)
* Groupes comptabilisation marché sur les clients et fournisseurs.

### Pour préparer les conversions de modification du taux de TVA

Avant de configurer l’outil de modification du taux de TVA, vous devez vous préparer comme suit :

* Si des transactions utilisent plusieurs taux, vous devez les répartir par groupes soit en créant des comptes généraux pour chaque taux, soit en utilisant des filtres de données pour regrouper les transactions en fonction du taux.  
* Si vous créez des comptes généraux, vous devez créer des groupes de comptabilisation généraux.  
* Pour réduire le nombre de documents à convertir, validez autant de documents que possible et réduisez le nombre de documents non validés au maximum.  
* Sauvegardez les données.

### Pour configurer l’outil de modification du taux de TVA

1. Sélectionnez l’icône ![Ampoule qui ouvre la fenêtre de recherche.](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire") entrez **Paramètres modification taux TVA**, puis choisissez le lien associé.  
2. Sur les raccourcis **Données principales**, **Feuilles** et **Documents**, sélectionnez la valeur d’un groupe de comptabilisation dans la liste des options pour les champs requis. Pour chaque groupe, vous pouvez choisir de convertir les groupes comptabilisation produit TVA ou les groupes généraux comptabilisation produit, ou convertissez les deux valeurs si elles sont disponibles dans l’élément de données de base. Pour certaines zones, vous pouvez également définir un filtre pour convertir uniquement un sous-ensemble de valeurs, par exemple, les comptes généraux. 
3. Sur le raccourci **Prix TTC**, choisissez les types ligne sur les commandes pour lesquelles vous souhaitez mettre à jour les prix unitaires. Les prix unitaires sur les lignes de type Article et Ressource seront toujours mis à jour.

### Pour paramétrer une conversion du groupe de comptabilisation du produit

1. Sélectionnez l’icône ![Ampoule qui ouvre la fenêtre de recherche.](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire") entrez **Paramètres modification taux TVA**, puis choisissez le lien associé.  
2. Dans la page **Paramètres modification taux TVA**, choisissez l’action **Conv. groupe compta. produit TVA** ou **Conv. groupe compta. produit général**.  
3. Dans le champ **Code début**, saisissez le groupe de comptabilisation actuel.  
4. Dans le champ **Code fin**, saisissez le nouveau groupe de comptabilisation.  

### Pour exécuter la conversion de modification du taux de TVA

Vous utilisez l’outil de modification de la TVA pour gérer les variations du taux standard de TVA. Vous exécutez les conversions TVA et groupe comptabilisation TVA pour modifier les taux de TVA et garantir l’exactitude des états de TVA. En fonction de le paramétrage, les modifications suivantes sont apportées :  

* Les groupes de comptabilisation TVA et générale sont convertis.  
* Les modifications sont implémentées dans les comptes généraux, les clients, les fournisseurs, les documents ouverts, les lignes de feuille, etc.  

> [!IMPORTANT]  
> Avant d’effectuer la conversion de modification du taux de TVA, vous pouvez tester la conversion. Pour ce faire, suivez la procédure ci-dessous, mais veillez à désactiver les cases à cocher **Effectuer la conversion** et **Outil de modification du taux de TVA terminé**. Lors de la conversion test, le champ **Converti** de la table **Écriture journal modification taux TVA** est supprimé et le champ **Date conversion** de la table **Écriture journal modification taux TVA** est vide. Une fois la conversion terminée, choisissez **Écritures journal modification pour taux de TVA** pour afficher les résultats de la conversion test. Vérifiez chaque écriture avant d’exécuter la conversion. Vérifiez en particulier les transactions qui utilisent un ancien taux de TVA.

1. Sélectionnez l’icône ![Ampoule qui ouvre la fenêtre de recherche.](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire") entrez **Modification taux TVA**, puis choisissez le lien associé **Paramètres modification taux TVA**.  
2. Vérifiez que vous avez déjà configuré une conversion de groupe comptabilisation produit TVA ou une conversion de groupe comptabilisation produit général.  
3. Activez la case à cocher **Effectuer la conversion**.  

    > [!IMPORTANT]  
    >  Désactivez la case à cocher **Outil de modification du taux de TVA terminé**. La case est cochée automatiquement lorsque la conversion de modification du taux de TVA est terminée.  

4. Sélectionnez l’action **Convertir**.  
5. Une fois la conversion terminée, choisissez l’action **Écritures journal modification pour taux de TVA** pour afficher les résultats de la conversion.  

> [!IMPORTANT]  
> Après la conversion, le champ **Converti** de la table **Écriture journal modification taux TVA** est activé et le champ **Date conversion** de la table **Écriture journal modification taux TVA** affiche la date de conversion.  

## Voir la [formation Microsoft](/training/modules/rate-change-dynamics-365-business-central/) associée

## Voir aussi

[Configuration de la TVA](finance-setup-vat.md)  
[Configuration de la TVA sur encaissement](finance-setup-unrealized-vat.md)  
[Déclarer la TVA à une autorité fiscale](finance-how-report-vat.md)  
[Utiliser la TVA sur les ventes et les achats](finance-work-with-vat.md)  
[Fonctionnalités locales dans Business Central](about-localization.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
