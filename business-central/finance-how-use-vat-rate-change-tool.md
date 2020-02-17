---
title: Utiliser l'outil de modification du taux de TVA | Microsoft Docs
description: Utiliser l'outil de modification du taux de TVA
author: andregu
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: VAT, posting, tax, value-added tax
ms.date: 01/06/2020
ms.author: andregu
ms.openlocfilehash: 0fe23bb6b1d4ce6fbf73a1978a66f6d47b8e78fe
ms.sourcegitcommit: 877af26e3e4522ee234fbba606615e105ef3e90a
ms.translationtype: HT
ms.contentlocale: fr-CH
ms.lasthandoff: 01/28/2020
ms.locfileid: "2992271"
---
# <a name="use-the-vat-rate-change-tool"></a>Utiliser l'outil de modification du taux de TVA

## <a name="understanding-the-vat-rate-conversion-process"></a>Familiarisation avec la conversion du taux de TVA  
L'outil de modification du taux de TVA effectue des conversions de taux de TVA pour les données principales, les feuilles et les commandes de différentes manières. Les données principales et les feuilles sélectionnées seront mises à jour par le groupe de comptabilisation du produit général ou le groupe de comptabilisation du produit TVA. Si une commande a été expédiée entièrement ou partiellement, les articles livrés conserveront le groupe de comptabilisation du produit général ou le groupe de comptabilisation du produit TVA actuel. Une nouvelle ligne de commande sera créée pour les articles non livrés et mis à jour pour uniformiser les groupes actuels et nouveaux de comptabilisation du produit général ou du produit TVA. En outre, les affectations de frais annexes, les réservations, ainsi que les informations sur la traçabilité seront mis à jour en conséquence.  

Quelques éléments ne sont pas convertis par l'outil :

* Commandes vente ou achat et factures pour lesquelles les expéditions ont été validées. Ces documents sont validés à l'aide du taux de TVA actuel.  
* Documents contenant des factures d'acompte validées. Par exemple, vous avez effectué ou reçu des acomptes sur les factures qui n'ont pas été réalisées avant d'utiliser l'outil de modification du taux de TVA. Dans ce cas, il existe une différence entre la TVA qui est due et la TVA qui a été payée dans les acomptes lorsque la facture est terminée. L'outil de modification du taux de TVA ignorera ces documents et vous devrez les mettre à jour manuellement.  
* Livraisons directes ou commandes spéciales.  
* Commandes vente ou achat avec l'intégration en entrepôt si elles sont livrées ou réceptionnées partiellement.  
* Contrats de service.  

### <a name="to-prepare-vat-rate-change-conversions"></a>Pour préparer les conversions de modification du taux de TVA  
Avant de configurer l'outil de modification du taux de TVA, vous devez vous préparer comme suit :

* Si des transactions utilisent plusieurs taux, vous devez les répartir par groupes soit en créant des comptes généraux pour chaque taux, soit en utilisant des filtres de données pour regrouper les transactions en fonction du taux.  
* Si vous créez des comptes généraux, vous devez créer des groupes de comptabilisation généraux.  
* Pour réduire le nombre de documents à convertir, validez autant de documents que possible et réduisez le nombre de documents non validés au maximum.  
* Sauvegardez les données.

### <a name="to-set-up-the-vat-rate-change-tool"></a>Pour configurer l'outil de modification du taux de TVA  
1. Choisissez l'icône ![Ampoule qui ouvre la fonction Tell Me](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire"), entrez **Paramètres modification taux TVA**, puis sélectionnez le lien associé.  
2. Sur les raccourcis **Données principales**, **Feuilles** et **Documents**, sélectionnez la valeur d'un groupe de comptabilisation dans la liste des options pour les champs requis. Pour chaque groupe, vous pouvez choisir de convertir les groupes comptabilisation produit TVA ou les groupes généraux comptabilisation produit, ou convertissez les deux valeurs si elles sont disponibles dans l'élément de données de base. Pour certaines zones, vous pouvez également définir un filtre pour convertir uniquement un sous-ensemble de valeurs, par exemple, les comptes généraux. 

### <a name="to-set-up-product-posting-group-conversion"></a>Pour paramétrer une conversion du groupe de comptabilisation du produit  
1. Choisissez l'icône ![Ampoule qui ouvre la fonction Tell Me](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire"), entrez **Paramètres modification taux TVA**, puis sélectionnez le lien associé.  
2. Dans la page **Paramètres modification taux TVA**, choisissez l'action **Conv. groupe compta. produit TVA** ou **Conv. groupe compta. produit général**.  
3. Dans le champ **Code début**, saisissez le groupe de comptabilisation actuel.  
4. Dans le champ **Code fin**, saisissez le nouveau groupe de comptabilisation.  

### <a name="to-perform-vat-rate-change-conversion"></a>Pour exécuter la conversion de modification du taux de TVA  
Vous utilisez l'outil de modification de la TVA pour gérer les variations du taux standard de TVA. Vous exécutez les conversions TVA et groupe comptabilisation TVA pour modifier les taux de TVA et garantir l'exactitude des états de TVA. En fonction de le paramétrage, les modifications suivantes sont apportées :  

* Les groupes de comptabilisation TVA et générale sont convertis.  
* Les modifications sont implémentées dans les comptes généraux, les clients, les fournisseurs, les documents ouverts, les lignes de feuille, etc.  

> [!IMPORTANT]  
>  Avant d'effectuer la conversion de modification du taux de TVA, vous pouvez tester la conversion. Pour ce faire, suivez la procédure ci-dessous, mais veillez à désactiver les cases à cocher **Effectuer la conversion** et **Outil de modification du taux de TVA terminé**. Lors de la conversion test, le champ **Converti** de la table **Écriture journal modification taux TVA** est supprimé et le champ **Date conversion** de la table **Écriture journal modification taux TVA** est vide. Une fois la conversion terminée, choisissez **Écritures journal modification pour taux de TVA** pour afficher les résultats de la conversion test. Vérifiez chaque écriture avant d'exécuter la conversion. Vérifiez en particulier les transactions qui utilisent un ancien taux de TVA.     

1. Choisissez l'icône d'![ampoule qui ouvre la fonction Tell Me](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire"), entrez **Modification taux TVA**, puis sélectionnez le lien **Paramètres modification taux TVA** link.  
2. Vérifiez que vous avez déjà configuré une conversion de groupe comptabilisation produit TVA ou une conversion de groupe comptabilisation produit général.  
3. Activez la case à cocher **Effectuer la conversion**.  

    > [!IMPORTANT]  
    >  Désactivez la case à cocher **Outil de modification du taux de TVA terminé**. La case est cochée automatiquement lorsque la conversion de modification du taux de TVA est terminée.  

4. Sélectionnez l'action **Convertir**.  
5. Une fois la conversion terminée, choisissez l'action **Écritures journal modification pour taux de TVA** pour afficher les résultats de la conversion.  

> [!IMPORTANT]  
>  Après la conversion, le champ **Converti** de la table **Écriture journal modification taux TVA** est activé et le champ **Date conversion** de la table **Écriture journal modification taux TVA** affiche la date de conversion.  
## <a name="see-also"></a>Voir aussi  
[Configuration de la TVA](finance-setup-vat.md)  
[Configuration de la TVA sur encaissement](finance-setup-unrealized-vat.md)      
[Déclarer la TVA à une autorité fiscale](finance-how-report-vat.md)  
[Utiliser la TVA sur les ventes et les achats](finance-work-with-vat.md)  
[Fonctionnalités locales dans Business Central](about-localization.md)
