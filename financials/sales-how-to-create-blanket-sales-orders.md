---
title: "Procédure : créer des commandes ouvertes vente | Microsoft Docs"
description: "Utilisez des commandes ouvertes quand un client a accepté d'acheter de grandes quantités à livrer en plusieurs expéditions de petite taille au cours d'une période déterminée."
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 09/08/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 2c13559bb3dc44cdb61697f5135c5b931e34d2a8
ms.openlocfilehash: 0b91925a7ec6adb40cdf99d5bcf3398b62c28b3f
ms.contentlocale: fr-ch
ms.lasthandoff: 09/22/2017

---
# <a name="how-to-work-with-blanket-sales-orders"></a>Procédure : utiliser des commandes ouvertes vente
Une commande ouverte vente représente le cadre d'un accord à long terme entre votre client et vous.

Une commande ouverte est généralement établie quand un client s'est engagé à acheter de grandes quantités à livrer en plusieurs expéditions de plus petite taille au cours d'une période déterminée. Souvent, les commandes ouvertes ne portent que sur un seul article avec des dates de livraison prédéterminées. La principale raison d'utiliser une commande ouverte plutôt qu'une commande vente est que les quantités entrées dans une commande ouverte n'affectent pas la disponibilité de l'article et peuvent donc être utilisées comme une feuille à des fins de surveillance, de précision et de planification.

Sur la commande ouverte, vous pouvez configurer chaque expédition comme une ligne commande distincte qui peut ensuite être convertie en commande vente au moment de l'expédition.

Vous pouvez utiliser une commande ouverte vente, par exemple, lorsqu'un client appelle pour passer une commande de 1 000 unités d'un article et souhaite des livraisons par lot de 250 unités chaque semaine du mois suivant.

> [!NOTE]
> Les commandes ouvertes achat fonctionnent de la même manière que les commandes ouvertes vente. Cette documentation ne couvre pas les commandes ouvertes achat.

## <a name="to-create-a-blanket-sales-order"></a>Pour créer une commande vente ouverte.  
1. Sélectionnez l'icône ![Page ou état pour la recherche](media/ui-search/search_small.png "Page ou état pour la recherche"), entrez **Commandes ouvertes vente**, puis sélectionnez le lien connexe.  
2. Sélectionnez l'action **Nouveau**.  
3. Renseignez les champs selon vos besoins. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
4.  Laissez vide le champ **Date commande**. Lors de la création de commandes vente séparées depuis la commande ouverte, la date commande de la commande vente est définie comme égale à la date du jour.
5. Dans le raccourci **Lignes**, créez des lignes distinctes pour chaque expédition. Par exemple, si le client souhaite 1 000 unités réparties de façon uniforme sur quatre semaines, entrez quatre lignes distinctes de 250 unités chacune.   

## <a name="to-create-a-sales-order-from-a-blanket-sales-order"></a>Pour créer une commande vente à partir d'une commande ouverte vente  

1.  Pour créer une commande pour l'une des lignes de l'ordre d'assemblage ouvert, effacez la quantité du champ **Qté à expédier** de toutes les lignes que vous ne voulez PAS expédier actuellement.  
2.  Lorsque vous êtes prêt à créer les commandes, sélectionnez **Créer commande**, puis **Oui**. Un message s'affiche, vous informant que la commande ouverte a été associée à un numéro de commande. Remarquez que la commande ouverte n'a pas été supprimée.  
3.  Cliquez sur le bouton **OK**.  
4.  Pour afficher les résultats des étapes précédentes, sélectionnez l'action **Ligne**, l'action **Lignes non validées**, puis l'action **Commandes**.  
5.  Dans la fenêtre **Lignes vente**Lignes vente, sélectionnez la commande vente appropriée, sélectionnez l'action **Ligne**, sélectionnez Ligne, puis sélectionnez l'action **Afficher document**.  

Ce qui suit s'applique aux commandes vente après leur création à partir de commandes vente ouvertes :  

- Une fois la commande ouverte convertie en commande vente, celle-ci contient toutes les lignes de la commande ouverte. Les lignes où la quantité figurant dans le champ **Qté à expédier** a été supprimée s'affichent mais avec les champs **Quantité** vides. Vous pouvez décider de laisser, de modifier ou de supprimer les lignes.  
- N'oubliez pas que la quantité de la ligne commande vente ne peut pas dépasser celle de la ligne commande ouverte associée. Sinon, la validation de la commande vente est impossible.  
- Lorsque la commande vente est validée comme expédiée et/ou facturée, les champs **Qté expédiée** et **Quantité facturée** sont mis à jour sur la commande ouverte concernée.  
- Le numéro de commande ouverte et un numéro de ligne sont enregistrés comme propriétés des lignes vente en cas de création à partir d'une commande ouverte.  
- Si les commandes vente ne sont pas créées directement depuis la commande ouverte mais ont trait à celle\-ci, il est possible de créer un lien entre une commande vente et une commande ouverte en entrant le numéro de commande ouverte associé dans le champ **N° commande ouverte** sur la ligne de commande vente.  
- Une fois la commande vente créée pour la quantité totale d'une ligne commande ouverte, aucune autre commande vente ne peut être créée pour la même ligne. Les utilisateurs ne peuvent plus entrer de quantité dans le champ **Qté à expédier**. Toutefois, si des quantités supplémentaires doivent être ajoutées à une commande ouverte, il est possible d'augmenter la valeur du champ **Quantité** et de créer des commandes supplémentaires.  
- La commande ouverte vente facturée reste dans le système jusqu'à ce qu'elle soit supprimée, soit en supprimant les commandes ouvertes individuelles, soit en exécutant le traitement par lots **Suppr. cdes vente ouv. fact.**.  
- Si un client est également enregistré comme contact dans le module Marketing et si vous avez spécifié un code modèle interaction pour les commandes vente ouvertes dans la fenêtre **Paramètres Marketing**, lorsque vous sélectionnez **Imprimer** pour imprimer la commande vente ouverte, une interaction est enregistrée automatiquement dans la table Écriture journal interaction.

## <a name="to-view-the-status-of-a-blanket-purchase-order"></a>Pour visualiser le statut d'une commande ouverte achat  
Vous pouvez visualiser le statut d'une commande ouverte vente dans la fenêtre **Statistiques Commande ouverte achat**. Ceci peut s'avérer utile lorsque vous commencez à facturer une commande créée à partir de la commande ouverte achat.  

1.  Sélectionnez l'icône ![Page ou état pour la recherche](media/ui-search/search_small.png "Page ou état pour la recherche"), entrez **Commandes ouvertes vente**, puis sélectionnez le lien connexe.  
2.  Sélectionnez une commande ouverte achat, puis sélectionnez l'action **Statistiques**.  
3.  Dans la fenêtre **Statistiques Commande ouverte achat**, sur le raccourci **Général**, vous pouvez visualiser des informations récapitulatives concernant l'intégralité de la commande. Elles se basent sur la quantité totale des **champs Quantité** sur les lignes commande ouverte achat.  

    - Sur le raccourci **Facturation**, vous pouvez visualiser des informations récapitulatives concernant l'intégralité de la quantité dans les champs **Qté à facturer** des lignes commande ouverte achat.  
    - Sur le raccourci **Expédition**, vous pouvez visualiser des informations récapitulatives concernant l'intégralité de la quantité dans les champs **Qté à recevoir** des lignes commande ouverte achat.  
    - Sur le raccourci **Acompte**, vous pouvez visualiser des informations récapitulatives concernant les éventuels acomptes.  
    - Sur le raccourci **Fournisseur**, vous pouvez visualiser certaines informations de base concernant le fournisseur.    

## <a name="to-view-unposted-and-posted-blanket-sales-order-lines"></a>Pour afficher des lignes de commande vente ouverte non validées et validées   
Le lien entre la commande ouverte vente et la commande vente d'origine, et n'importe quel autre document vente, est conservé après validation en tant que liste des lignes facture validées et non validées de commande vente.  

1. Sélectionnez l'icône ![Page ou état pour la recherche](media/ui-search/search_small.png "Page ou état pour la recherche"), entrez **Commandes ouvertes vente**, puis sélectionnez le lien connexe.
2. Ouvrez la commande vente ouverte que vous souhaitez afficher.
3. Pour visualiser les écritures non validées, sélectionnez la ligne en question, sélectionnez l'action **Ligne**, puis l'action **Lignes non validées**. Choisissez l'une des options suivantes.  

    <table>
    <tr>
    <th>Option</th>
    <th>Désignation</th>
    </tr>
    <tr>
    <td>**Commandes**</td>
    <td>Spécifie les commandes ouvertes associées à la ligne sélectionnée.</td>
    </tr>
    <tr>
    <td>**Factures**</td>
    <td>Spécifie les factures ouvertes associées à la ligne sélectionnée. Ouvrez les factures associées manuellement à une commande ouverte en entrant le numéro de commande ouverte dans la ligne facture vente.</td>
    </tr>
    <tr>
    <td>**Retours**</td>
    <td>Spécifie les commandes retour ouvertes associées à la ligne sélectionnée.</td>
    </tr>
    <tr>
    <td>**Avoirs**</td>
    <td>Spécifie les avoirs ouverts associés à la ligne sélectionnée.</td>
    </tr>
    </table>
4. Pour visualiser les écritures validées, sélectionnez la ligne en question, choisissez l'action **Ligne**, puis l'action **Lignes validées**. Choisissez l'une des options suivantes.  

    <table>
    <tr>
    <th>Option</th>
    <th>Désignation</th>
    </tr>
    <tr>
    <td>**Livraisons**</td>
    <td>Livraisons validées associées à la ligne sélectionnée.</td>
    </tr>
    <tr>
    <td>**Factures**</td>
    <td>Factures validées associées à la ligne sélectionnée.</td>
    </tr>
    <tr>
    <td>**Réceptions retour**</td>
    <td>Réceptions retour validées associés à la ligne sélectionnée.</td>
    </tr>
    <tr>
    <td>**Avoirs**</td>
    <td>Avoirs validés associés à la ligne sélectionnée.</td>
    </tr>
    </table>
5. Dans la fenêtre **Lignes vente**, sélectionnez l'action **Afficher document** pour afficher l'écriture.

## <a name="see-also"></a>Voir aussi
[Ventes](sales-manage-sales.md)  
[Définition des ventes](sales-setup-sales.md)  
[Utilisation de [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

