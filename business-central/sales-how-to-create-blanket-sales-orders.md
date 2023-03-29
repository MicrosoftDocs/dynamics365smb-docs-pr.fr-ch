---
title: Utiliser des Commandes cadres vente ou des commandes achat
description: Utilisez des commandes cadres quand un client a accepté d’acheter de grandes quantités à livrer en plusieurs expéditions de petite taille au cours d’une période déterminée. La même chose s’applique aux achats.
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.form: '507, 509, 6620, 6622, 6623, 9303, 9310'
ms.date: 04/01/2021
ms.author: edupont
---
# Utiliser des Commandes cadres vente ou des commandes cadres achat

Une commande cadre vente représente le cadre d’un accord à long terme entre votre client et vous. De même, vous utilisez des commandes cadre achat pour gérer les contrats à long terme entre vous et votre fournisseur.

Une commande cadre est généralement établie quand un client s’est engagé à acheter de grandes quantités à livrer en plusieurs expéditions de plus petite taille au cours d’une période déterminée. Souvent, les commandes cadres ne portent que sur un seul article avec des dates de livraison prédéterminées. La principale raison d’utiliser une commande cadre plutôt qu’une commande vente est que les quantités entrées dans une commande cadre n’affectent pas la disponibilité de l’article et peuvent donc être utilisées comme une feuille à des fins de surveillance, de précision et de planification.

Sur la commande cadre, vous pouvez configurer chaque expédition comme une ligne commande distincte qui peut ensuite être convertie en commande vente au moment de l’expédition.

Vous pouvez utiliser une commande cadre vente, par exemple, lorsqu’un client appelle pour passer une commande de 1 000 unités d’un article et souhaite des livraisons par lot de 250 unités chaque semaine du mois suivant.

> [!NOTE]
> Les commandes ouvertes achat fonctionnent de la même manière que les commandes ouvertes vente. Cette documentation couvre les commandes vente en cours uniquement.

## Pour créer une commande vente ouverte.

1. Sélectionnez l’icône ![en forme d’Ampoule qui ouvre la fenêtre de recherche.](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire") entrez **Commandes cadres vente**, puis sélectionnez le lien associé.  
2. Sélectionnez l’action **Nouveau**.  
3. Renseignez les champs selon vos besoins. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
4. Laissez vide le champ **Date commande**. Lors de la création de commandes vente séparées depuis la commande cadre, la date commande de la commande vente est définie comme égale à la date du jour.
5. Dans le raccourci **Lignes**, créez des lignes distinctes pour chaque expédition. Par exemple, si le client souhaite 1 000 unités réparties de façon uniforme sur quatre semaines, entrez quatre lignes distinctes de 250 unités chacune.  

## Pour créer une commande vente à partir d’une commande cadre vente  

1. Pour créer une commande pour l’une des lignes de la commande vente en cours, effacez la quantité du champ **Qté à expédier** de toutes les lignes que vous ne voulez pas expédier actuellement.  
2. Lorsque vous êtes prêt à créer les commandes, sélectionnez **Créer commande**, puis **Oui**. Un message s’affiche, vous informant que la commande cadre a été associée à un numéro de commande. Remarquez que la commande cadre n’a pas été supprimée.  
3. Cliquez sur le bouton **OK**.  
4. Pour afficher les résultats des étapes précédentes, sélectionnez l’action **Ligne**, l’action **Lignes non validées**, puis l’action **Commandes**.  
5. Sur la page **Lignes vente**, sélectionnez la commande vente appropriée, l’action **Ligne**, puis l’action **Afficher document**.  

Ce qui suit s’applique aux commandes vente après leur création à partir de commandes vente ouvertes :  

- Une fois la commande cadre convertie en commande vente, celle-ci contient toutes les lignes de la commande cadre. Les lignes où la quantité figurant dans le champ **Qté à expédier** a été supprimée s’affichent mais avec les champs **Quantité** vides. Vous pouvez décider de laisser, de modifier ou de supprimer les lignes.  
- N’oubliez pas que la quantité de la ligne commande vente ne peut pas dépasser celle de la ligne commande cadre associée. Sinon, la validation de la commande vente est impossible.  
- Lorsque la commande vente est validée comme expédiée et/ou facturée, les champs **Qté expédiée** et **Quantité facturée** sont mis à jour sur la commande cadre concernée.  
- Le numéro de commande cadre et un numéro de ligne sont enregistrés comme propriétés des lignes vente en cas de création à partir d’une commande cadre.  
- Si les commandes vente ne sont pas créées directement depuis la commande cadre mais ont trait à celle\-ci, il est possible de créer un lien entre une commande vente et une commande cadre en entrant le numéro de commande cadre associé dans le champ **N° commande cadre** sur la ligne de commande vente.  
- Une fois la commande vente créée pour la quantité totale d’une ligne commande cadre, aucune autre commande vente ne peut être créée pour la même ligne. Les utilisateurs ne peuvent plus entrer de quantité dans le champ **Qté à expédier**. Toutefois, si des quantités supplémentaires doivent être ajoutées à une commande cadre, il est possible d’augmenter la valeur du champ **Quantité** et de créer des commandes supplémentaires.  
- La commande cadre vente facturée reste dans le système jusqu’à ce qu’elle soit supprimée, soit en supprimant les commandes cadres individuelles, soit en exécutant le traitement par lots **Suppr. cdes vente ouv. fact.**.  
- Si un client est également enregistré comme contact dans le module Marketing et si vous avez spécifié un code modèle interaction pour les commandes vente ouvertes sur la page **Paramètres Marketing**, lorsque vous sélectionnez **Imprimer** pour imprimer la commande vente ouverte, une interaction est enregistrée automatiquement dans la table Écriture journal interaction.

## Pour visualiser le statut d’une commande cadre vente

Vous pouvez visualiser le statut d’une commande cadre vente sur la page **Statistiques Commande vente en cours**. Ceci peut s’avérer utile lorsque vous commencez à facturer une commande créée à partir de la commande vente en cours.  

1.  Sélectionnez l’icône ![en forme d’Ampoule qui ouvre la fenêtre de recherche.](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire") entrez **Commandes cadres vente**, puis sélectionnez le lien associé.  
2.  Sélectionnez une commande vente en cours, puis sélectionnez l’action **Statistiques**.  
3.  Sur la page **Statistiques Commande vente en cours**, sur le raccourci **Général**, vous pouvez visualiser des informations récapitulatives concernant l’intégralité de la commande. Elles se basent sur la quantité totale des **champs Quantité** sur les lignes commande vente en cours.  

- Sur le raccourci **Facturation**, vous pouvez visualiser des informations récapitulatives concernant l’intégralité de la quantité dans les champs **Qté à facturer** des lignes de la commande vente en cours.  
- Sur le raccourci **Livraison**, vous pouvez visualiser des informations récapitulatives concernant l’intégralité de la quantité dans les champs **Qté à recevoir** des lignes de la commande vente en cours.  
- Sur le raccourci **Acompte**, vous pouvez visualiser des informations récapitulatives concernant les éventuels acomptes.  
- Sur le raccourci **Fournisseur**, vous pouvez visualiser certaines informations de base concernant le fournisseur.

## Pour afficher des lignes de commande vente ouverte non validées et validées

Le lien entre la commande cadre vente et la commande vente d’origine, et n’importe quel autre document vente, est conservé après validation en tant que liste des lignes facture validées et non validées de commande vente.  

1. Sélectionnez l’icône ![en forme d’Ampoule qui ouvre la fenêtre de recherche.](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire") entrez **Commandes cadres vente**, puis sélectionnez le lien associé.
2. Ouvrez la commande vente ouverte que vous souhaitez afficher.
3. Pour visualiser les écritures non validées, sélectionnez la ligne en question, sélectionnez l’action **Ligne**, puis l’action **Lignes non validées**. Choisissez l’une des options suivantes.  

|Option|Désignation|
|--|--|
|**Commandes**|Spécifie les commandes ouvertes associées à la ligne sélectionnée.|
|**Factures**|Spécifie les factures ouvertes associées à la ligne sélectionnée. Ouvrez les factures associées manuellement à une commande cadre en entrant le numéro de commande cadre dans la ligne facture vente.|
|**Retours**|Spécifie les commandes retour ouvertes associées à la ligne sélectionnée.|
|**Avoirs**|Spécifie les avoirs ouverts associés à la ligne sélectionnée.|

4. Pour visualiser les écritures validées, sélectionnez la ligne en question, sélectionnez l’action **Ligne**, puis l’action **Lignes validées**. Choisissez l’une des options suivantes.  

|Option|Désignation|
|---|----|
|**Livraisons**|Livraisons validées associées à la ligne sélectionnée.|
|**Factures**|Factures validées associées à la ligne sélectionnée.|
|**Réceptions retour**|Réceptions retour validées associés à la ligne sélectionnée.|
|**Avoirs**|Avoirs validés associés à la ligne sélectionnée.|

5. Sur la page **Lignes vente**, sélectionnez l’action **Afficher document** pour afficher l’écriture.

## Voir la [formation Microsoft](/training/modules/create-sales-documents-dynamics-365-business-central/) associée

## Voir aussi

[Ventes](sales-manage-sales.md)  
[Création d’ordres d’assemblage permanents](assembly-how-to-create-blanket-assembly-orders.md)  
[Définition des ventes](sales-setup-sales.md)  
[Utiliser [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]
