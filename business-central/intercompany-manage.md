---
title: Gestion des transactions intersociétés
description: 'Avec la fonctionnalité intersociétés, vous pouvez simplifier les processus et les transactions entre sociétés appartenant à la même organisation.'
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bhielse
ms.topic: conceptual
ms.date: 02/06/2023
ms.custom: bap-template
ms.search.keywords: 'IC, group, consolidation, affiliate, subsidiary'
ms.search.form: '605,'
---
# <a name="managing-intercompany-transactions"></a><a name="managing-intercompany-transactions"></a><a name="managing-intercompany-transactions"></a>Gestion des transactions intersociétés

Les entreprises ayant plus d’une entité juridique avec des fonctions comptables distinctes peuvent bénéficier de transactions intersociétés. Par exemple, il est utile pour les entreprises qui ont des filiales sur plusieurs marchés ou régions internationaux. Ou, une organisation peut comprendre plusieurs sociétés, mais pourrait ne pas disposer du nombre équivalent d’équipes comptables et administratives. Les transactions intersociétés vous permettent de simplifier et de rationaliser les processus et les transactions commerciaux entre les sociétés dans le cadre du partenariat intersociétés.

Lorsque vous avez spécifié les relations client et fournisseur pour les transactions intersociétés, les partenaires saisissent les informations une seule fois dans les documents de vente et d’achat. Un document correspondant est créé chez l’autre partenaire impliqué dans la transaction. Les fonctionnalités de mappage pour le plan comptable et les dimensions permettent de veiller à ce que les informations apparaissent aux bons endroits.  

La fonctionnalité Intersociétés offre quatre grands avantages :  

* Productivité accrue résultant du gain de temps et de la simplification des transactions  
* Possibilité d’erreur réduite grâce à une saisie unique d’informations et de mises à jour automatisées à l’échelle du système  
* Piste d’audit et visibilité complètes des activités commerciales et des historiques de transactions  
* Transactions efficaces, rentables avec des filiales ou des succursales  

## <a name="streamline-the-flow-of-business-activities"></a><a name="streamline-the-flow-of-business-activities"></a><a name="streamline-the-flow-of-business-activities"></a>Rationaliser le flux des activités commerciales

Les transactions intersociétés vous permettent de distribuer des documents vente et achat, ainsi que des écritures feuille comptabilité à l’ensemble de vos bureaux satellites, représentations commerciales ou succursales depuis le programme. La distribution des transactions permet de gagner du temps et d’augmenter l’efficacité dans toute l’organisation en réduisant la saisie de données. Il réduit le besoin d’envoyer, de recevoir, d’imprimer et d’archiver des documents de vente et d’achat.  

Vous contrôlez totalement tous les documents de transaction. Par exemple, vous pouvez rejeter un document qui vous a été envoyé et, de cette manière, utiliser les actions **Inverser des validations feuille** et **Annuler les réceptions/envois** incorrects. Ou bien, lorsque vous faites un achat à une société partenaire ou une filiale, vous pouvez mettre à jour la commande achat tant que la société vendeuse n’a pas expédié de biens.  

Lorsque vous entrez une transaction, vous n’avez pas besoin de spécifier les comptes à utiliser. Vous choisissez simplement le partenaire intersociétés. La fonctionnalité intersociétés crée des lignes feuilles comptabilité qui entraînent un équilibrage des lois des deux sociétés impliquées dans une transaction. Dans Clients et fournisseurs, vous affectez un code partenaire intersociétés à tout client ou fournisseur. À partir de ce moment, toutes les commandes et factures des transactions entre ces sociétés produisent des documents correspondants dans la société partenaire. Le résultat est des comptes correctement équilibrés.  

La fonctionnalité Intersociétés se concentre sur les documents de vente et d’achat et les lignes du journal général, et permet des transactions entre plusieurs bases de données [!INCLUDE [prod_short](includes/prod_short.md)]. Par exemple :

* Dans différents pays/régions
* Plusieurs devises
* Différents plans comptables
* Différents axes analytiques
* Différents numéros d’article  

Les transactions intersociétés utilisent plusieurs types d’écritures et de documents :  

* Écritures comptables
* Commandes achat et vente
* Factures achat et vente
* Avoirs
* Retours

Lorsque vous configurez les transactions intersociétés, vous créez une liste de partenaires intersociétés, un plan comptable intersociété et des axes analytiques intersociétés. Ensuite, vous pouvez créer des transactions dans les feuilles comptables intersociétés.

> [!NOTE]
> La feuille comptable en elle-même n’inclut pas les devises. Elle convertit tous les montants dans la devise locale au taux de change actuel.

Après avoir paramétré vos partenaires commerciaux comme clients et fournisseurs, et leur avoir affecté des codes partenaire intersociété, ils peuvent échanger des documents achat et vente intersociété, notamment des articles et des frais annexes. 

> [!NOTE]
> Les entreprises ne peuvent pas utiliser la fonctionnalité Intersociétés pour échanger tous les types de données. Les factures achat ne sont pas soumises aux partenaires commerciaux via des processus intersociétés. Mais les factures vente soumises via des processus intersociétés seront créées en tant que factures achat dans la société destinataire.

La consolidation des données financières peut être particulièrement appropriée pour les processus intersociétés. Pour plus d’informations, voir [Consolidation des données financières de plusieurs sociétés](finance-consolidated-company-reporting.md).

Le tableau suivant décrit une série de tâches et inclut des liens vers les articles qui les décrivent.

|À |Voir|
|---|---|
|Créez vos fournisseurs et vos clients intersociétés en tant que partenaires et configurez un plan comptable intersociétés.|[Configuration des fonctionnalités intersociétés](intercompany-how-setup.md)|
|Utilisez les documents ou les feuilles intersociétés pour valider les transactions effectuées avec vos partenaires intersociétés.|[Utiliser les documents et les feuilles intersociétés](intercompany-how-work-documents-journals.md)|
|Organisez et traitez les transactions entrantes et sortantes que vous échangez avec vos partenaires intersociétés.|[Gérer la boîte de réception et la boîte d’envoi intersociétés](intercompany-how-manage-intercompany-inbox.md)|
|Utilisez les transactions intersociétés pour répartir les coûts entre les sociétés partenaires.|[Allouer les coûts aux partenaires intersociétés](intercompany-allocate-costs.md)|

## <a name="see-also"></a><a name="see-also"></a><a name="see-also"></a>Voir aussi

[Finances](finance.md)  
[Configuration de Finance](finance-setup-finance.md)  
[Utiliser des feuilles comptabilité](ui-work-general-journals.md)  
[Utiliser [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)

## [!INCLUDE[prod_short](includes/free_trial_md.md)]


[!INCLUDE[footer-include](includes/footer-banner.md)]
