---
title: Configurer des calendriers principaux
description: 'Vous pouvez affecter un calendrier de base à votre entreprise et à ses partenaires commerciaux, pour calculer les dates de livraison et de réception en fonction des jours ouvrés spécifiés.'
author: brentholtorf
ms.topic: conceptual
ms.devlang: al
ms.search.form: '7600, 7601, 7602, 5703'
ms.date: 06/11/2021
ms.author: bholtorf
ms.service: dynamics-365-business-central
---
# <a name="set-up-base-calendars"></a>Configurer des calendriers principaux

Vous pouvez affecter un calendrier principal à votre société et à ses partenaires commerciaux, tels que ses clients, ses fournisseurs, ou ses magasins. Les dates de livraison et de réception sur les lignes commande vente, commande achat, ordre de transfert, et ordre de fabrication sont calculées en fonction des jours ouvrés définis dans le calendrier. Lorsque vous paramétrez un nouveau calendrier principal, votre tâche consiste essentiellement à indiquer et à définir les jours chômés à appliquer.  

## <a name="to-set-up-a-base-calendar"></a>Pour configurer un calendrier principal

1.  Sélectionnez l’icône ![Ampoule qui ouvre la fonction Tell Me.](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire") entrez **Calendrier principal**, puis choisissez le lien associé.  
2.  Sélectionnez l’action **Nouveau**.  
3.  Complétez le champ **Code**.  
4. Choisissez l’action **Gérer modifications calendrier principal**.
5. Sur la page **Modifications calendrier principal**, utilisez le champ **Système abonnement** pour sélectionner une date ou un jour spécifique comme jour chômé récurrent. Vous pouvez choisir l’option **Abonnement annuel** ou **Abonnement hebdomadaire**.  

    Si vous sélectionnez **Abonnement annuel**, vous devez également entrer la date appropriée dans le champ **Date**.  

    Si vous sélectionnez **Abonnement hebdomadaire**, vous devez également sélectionner le jour de la semaine approprié dans le champ **Jour**. Si vous ne remplissez pas ce champ, vous devez compléter le champ **Date**. Le champ **Jour** est renseigné automatiquement.  

Lorsque vous créez une écriture, le champ **Jour chômé** est sélectionné. Vous pouvez choisir de décocher la case pour la définir comme un jour ouvré.  
 Lorsque vous affichez de nouveau la fiche calendrier principal, vous observerez que les écritures jour chômé que vous avez créées ont été mises à jour. Ces écritures s’affichent désormais en rouge et le champ **Jour chômé** est sélectionné.  

> [!NOTE]  
>  Lorsque vous paramétrez un nouveau calendrier principal, vous pouvez sélectionner des lignes dans un calendrier et les copier. Pour cela, utilisez la page **Modifications calendrier principal** correspondante.  

> [!IMPORTANT]  
>  Le calendrier principal défini pour le fournisseur ou le magasin affecte uniquement la manière dont les dates sont calculées et arrondies en jours ouvrés.
Spécifie une formule date pour le délai nécessaire au réapprovisionnement de l’article. Permet de calculer le champ **Date planifiée de réception**, si calcul en aval, et le champ **Date commande**, si calcul en amont. Voir [Calcul du délai](across-how-to-assign-base-calendars.md#lead-time-calculation).

## <a name="lead-time-calculation"></a>Calcul du délai

Le calendrier principal défini pour le fournisseur ou le magasin affecte uniquement la manière dont les dates sont calculées et arrondies en jours ouvrés. En conséquence, les deux champs date sur les lignes commande achat sont calculés comme suit sous différentes conditions.

|Direction de calcul|Calendrier fournisseur défini|Calendrier fournisseur non défini|
|---------------------|-----------------------|---------------------------|
|Aval|date réception prévue = date commande + délai fournisseur (par calendrier fournisseur et arrondie au jour ouvré suivant dans le calendrier fournisseur, puis dans le calendrier du magasin)|date réception prévue = date commande + délai fournisseur (par calendrier de magasin)|
|Amont|date commande = date réception prévue - délai fournisseur (par calendrier fournisseur et arrondie au jour ouvré précédent dans le calendrier fournisseur, puis dans le calendrier du magasin)|date commande = date réception prévue - délai fournisseur (par calendrier de magasin)|

> [!NOTE]
> Outre le calcul du délai qui affecte la date de réception prévue et la date de commande, comme illustré dans la table ci-dessus, le délai d’activité entrepôt et le délai de sécurité peuvent être ajoutés à des formules pour constituer la valeur du champ **Date réception prévue** comme suit : Date planifiée de réception + Délai de sécurité + Délai enlogement = Date réception prévue.

> [!Important]
> Si votre magasin utilise un calendrier sensiblement différent de celui de vos fournisseurs, il est important de créer des calendriers spécifiques pour ces fournisseurs, pour calculer les délais fournisseur optimaux. Pour plus d’informations sur le paramétrage des calendriers fournisseur, voir [Pour affecter un calendrier principal](across-how-to-assign-base-calendars.md#to-assign-a-base-calendar).

La valeur du champ **Délai de réappro.** est copiée à partir de la fiche article ou de la fiche point de stock, si le délai est défini pour l’article, ou sur la page **Catalogue fournisseur articles**, si le délai est défini pour le fournisseur.

## <a name="to-customize-a-calendar"></a>Pour personnaliser un calendrier
Lorsque vous personnalisez un calendrier principal pour votre société ou pour l’un de ses partenaires commerciaux, votre tâche consiste essentiellement à modifier le statut des jours ouvrés et chômés.

Par exemple, bien qu’un calendrier principal définisse en général tous les samedis comme des jours chômés, le calendrier personnalisé d’un magasin peut indiquer tous les samedis des mois de novembre et décembre, jusqu’aux vacances de Noël, comme des jours ouvrés.

La procédure suivante illustre l’exemple d’un magasin. Remarquez que, à ce stade, vous avez déjà affecté un calendrier principal au magasin.

1. Sélectionnez l’icône ![Ampoule qui ouvre la fonction Tell Me.](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire") entrez **Emplacements**, puis choisissez le lien associé.
2. Ouvrez le magasin que vous voulez mettre à jour, puis sélectionnez le champ **Calendrier personnalisé**. Notez qu’un calendrier doit être sélectionné dans le champ **Code calendrier principal**.
3. Sur la page **Écritures calendrier personnalisé** qui s’ouvre, choisissez l’action **Conserver modifications calendrier personnalisé**.
4. Dans la fenêtre **Modifications calendrier personnalisé**, ajoutez des lignes pour les écritures calendrier personnalisé.

    Lorsque vous entrez une ligne, la case à cocher **Jour chômé** est activé. Vous pouvez désactiver cette case à cocher pour passer au statut Jour ouvré.

    Le champ **Système abonnement** permet de définir une date ou un jour spécifique comme jour chômé récurrent. Vous pouvez choisir l’option **Récurrence annuelle** ou **Récurrence hebdomadaire**.

    Si vous sélectionnez **Abonnement annuel**, vous devez également entrer la date appropriée dans le champ **Date**. Si vous sélectionnez **Abonnement hebdomadaire**, vous devez également sélectionner le jour de la semaine approprié dans le champ **Jour**. Si vous ne remplissez pas ce champ, vous devez compléter le champ **Date**. Le champ **Jour** est renseigné automatiquement. Cette opération se révèle utile si vous souhaitez marquer une date comme un jour chômé ou ouvré.

5. Choisissez le bouton **OK**.

Sur la page **Écritures calendrier personnalisé**, vous constaterez que les écritures de date sont mises à jour conformément aux modifications apportées.

Sur la fiche Magasin, le champ **Calendrier personnalisé** affiche **Oui**, indiquant ainsi que le calendrier personnalisé a été configuré.

> [!Important]
> Si vous ne renseignez pas le champ **Code magasin** d’une ligne commande, le calendrier de votre société est utilisé.


Si vous ne renseignez pas le champ **Code transporteur** de la ligne commande, le calendrier de votre société est utilisé.

> [!NOTE]  
> Si vous modifiez un calendrier principal auquel sont associés des calendriers personnalisés ayant fait l’objet de modifications, tous les calendriers personnalisés existants sont automatiquement mis à jour.

## <a name="to-assign-a-base-calendar"></a>Pour affecter un calendrier principal
La procédure suivante planifie les dates de livraison sur les lignes commande vente pour un client comme exemple.

Les calendriers principaux sont affectés à votre propre société, à vos clients, fournisseurs, magasins et transporteurs comme suit :  

-   Sur les fiches **Informations société** et **Client**, le calendrier principal est affecté sur le raccourci **Expédition** .  
-   Sur la fiche **Fournisseur**, le calendrier principal est affecté sur le raccourci **Réception**.  
-   Sur la fiche **Magasin**, le calendrier principal est affecté sur le raccourci **Entrepôt**.  
-   Sur la page **Transporteurs** , le calendrier principal est affecté sur la page **Prestations transporteur**.  

1.  Sélectionnez l’icône ![Ampoule qui ouvre la fonction Tell Me.](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire") entrez **Clients**, puis choisissez le lien associé.  
2.  Ouvrez la fiche **Client** pour laquelle vous allez affecter un calendrier principal.  
3.  Sur le raccourci **Expédition**, dans le champ **Code calendrier principal**, sélectionnez le calendrier principal à affecter.  

> [!IMPORTANT]  
>  -   Si vous n’affectez aucun calendrier principal aux sociétés, toutes les dates sont calculées comme des jours ouvrés.  
> -   Si vous n’indiquez pas le magasin sur une ligne commande, toutes les dates sont calculées comme des jours ouvrés.  
> -   Le calendrier principal défini pour le fournisseur ou le magasin affecte uniquement la manière dont les dates sont calculées et arrondies en jours ouvrés.

> [!NOTE]  
>  Pour créer des écritures calendrier personnalisé, vous devez d’abord affecter un calendrier principal à la société.  

## <a name="see-also"></a>Voir aussi
[Achats](purchasing-manage-purchasing.md)  
[Production](production-manage-manufacturing.md)    
[Stock](inventory-manage-inventory.md)  
[Utiliser [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]
