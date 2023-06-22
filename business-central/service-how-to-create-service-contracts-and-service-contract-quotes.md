---
title: Comment utiliser des contrats de service et des devis contrat de service | Microsoft Docs
description: Vous pouvez créer un contrat de service manuellement ou à partir d’un devis contrat de service. Vous pouvez créer un contrat en fonction d’un devis contrat de service.
author: brentholtorf
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: null
ms.date: 04/01/2021
ms.author: bholtorf
---
# <a name="work-with-service-contracts-and-service-contract-quotes" />Utiliser des contrats de service et des devis contrat de service
Vous pouvez créer un contrat de service manuellement ou à partir d’un devis contrat de service. Vous pouvez utiliser un devis contrat de service en tant qu’étape préliminaire d’un contrat de service, dans laquelle votre société fait une offre au client et qui nécessite d’obtenir l’approbation du client pour pouvoir être convertie en contrat de service. Les procédures de création d’un contrat de service ou d’un devis contrat de service sont identiques.  

## <a name="to-create-a-service-contract-or-service-contract-quote" />Pour créer un contrat de service ou un devis contrat de service
1. Sélectionnez l’icône ![Ampoule qui ouvre la fonction Tell Me.](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire") entrez **Contrats de service** ou **Devis contrat de service**, puis sélectionnez le lien associé.  
2. Pour créer un contrat de service ou un devis contrat de service.  
3. Renseignez le champ **N°** . Une boîte de dialogue s’ouvre, vous demandant si vous souhaitez renseigner les données communes à partir d’un modèle contrat. Si vous souhaitez créer un tel contrat de service ou devis contrat de service, sélectionnez le bouton **Oui**. La page **Liste des modèles contrat de service** s’ouvre.  
4. Sélectionnez le modèle approprié, puis choisissez **OK** afin de l’utiliser pour créer le contrat de service ou le devis contrat de service.  
5. Dans le champ **N° client**, choisissez le client.  
6. Si vous ne souhaitez pas qu’une différence du montant annuel soit répartie automatiquement, choisissez la case à cocher **Autoriser montants non soldés**. Les valeurs des champs **Montant annuel** et **Montant annuel calculé** ne sont pas automatiquement égalisées. Si vous souhaitez que l’application répartisse automatiquement toutes les différences de montant annuel qui peuvent survenir suite à une modification du contrat de service, ne sélectionnez pas la case à cocher **Autoriser montants non soldés**.  
7. Ajoutez des lignes contrat au contrat de service ou devis contrat de service.  
8. Renseignez les autres champs si nécessaire.  

## <a name="to-convert-a-service-contract-quote-to-service-contract" />Pour convertir un devis contrat de service en contrat de service
Lorsqu’un client accepte un devis contrat de service, vous le convertissez en contrat de service. Vous pouvez en même temps créer une facture service pour la période de début du contrat si la date début de ce contrat est antérieure au début de la prochaine période de facturation.

Une fois les étapes suivantes effectuées, un contrat de service est créé avec le statut **Signé**. Si une facture service est créée pour la période de début du contrat, le montant facturé est calculé comme suit, selon que le montant est détaillé ou non.  

Pour les contrats détaillés, le montant facturé est calculé de la manière suivante :  

* montant facturé = somme du montant facturé de chaque ligne contrat.  
* Montant facturé de chaque ligne contrat = ((valeur devis / 12) x nombre de mois de la période de début) + ((valeur devis / nombre de jours de l’année) x nombre de jours restant dans la période de début).  
* Si la ligne contrat expire avant la fin de la période de début, la date d’expiration devient la date fin de la période de début de la ligne.  

Pour les contrats non détaillés, le montant facturé est calculé de la manière suivante :  

* montant facturé = (montant annuel / nombre de jours de l’année) x nombre de jours de la période de début.  
* Si le contrat expire avant la fin de la période de début, la date d’expiration devient la date fin de la période de début.    

1. Sélectionnez l’icône ![Ampoule qui ouvre la fonction Tell Me.](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire") entrez **Devis de contrats de service**, puis sélectionnez le lien associé.  
2. Ouvrez le devis contrat de service que vous voulez convertir en contrat de service.  
3. Sélectionnez l’action **Créer contrat**.  
4. Si la date de début du contrat est antérieure au début de la période de facturation suivante, on vous demandera si vous voulez créer une facture pour la période de démarrage du contrat. Choisissez **Oui**.  

 La facture service est validée sur le compte service du contrat, même si le contrat est prépayé.

## <a name="to-create-contract-service-credit-memos" />Pour créer des avoirs service contrat
Vous pouvez utiliser un avoir service contrat lorsqu’un client annule un contrat de service prépayé ou supprime un article de service d’un contrat prépayé. Vous pouvez également l’utiliser pour corriger une facture service erronée.  

1. Sélectionnez l’icône ![Ampoule qui ouvre la fonction Tell Me.](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire") entrez **Avoirs service**, puis sélectionnez le lien associé.  
2. Créez un avoir service.  
3. Renseignez le champ **N°** .  
4. Dans le champ **N° client**, entrez le numéro du client du contrat de service.  

     Le raccourci **Facturation** affiche des informations copiées à partir de la fiche **Client**. Si vous souhaitez valider l’avoir pour un autre client que celui indiqué sur le raccourci **Général**, entrez le numéro de ce client dans le champ **N° client facturé** .  

    > [!NOTE]  
    >  Vous pouvez comparer l’avoir avec le document validé initialement sur la page **Factures service enreg.**. Sélectionnez l’icône ![Ampoule qui ouvre la fonction Tell Me.](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire") entrez **Factures de service validées**, puis sélectionnez le lien associé.  

5. Renseignez les champs **Date comptabilisation** et **Date document**.  
6. Sur les lignes avoir, entrez les informations relatives aux articles retournés ou retirés, ou à la réduction qui est envoyée. Vous pouvez également utiliser le traitement par lots **Obtenir écr. contrat prépayé**.  

 Pour créer automatiquement un avoir lorsque les lignes du contrat sont retirées d’un contrat de service, sur la page **Contrat de Service**, sur le raccourci **Détails de la facture**, sélectionnez la case à cocher **Avoirs automatiques**.  

 Pour créer manuellement un avoir lorsque les lignes du contrat sont retirées d’un contrat de service, sur la page **Contrat de Service**, sélectionnez l’action **Avoir**.  

## <a name="updating-and-evaluating-contracts" />Mise à jour et évaluation des contrats
Vous devez parfois modifier les conditions d’un contrat après sa création. Dans la plupart des cas, vous devez ouvrir le contrat approprié sur la page **Contrat service** et le modifier de manière appropriée.  

Vous pouvez modifier le statut du contrat, initialement défini sur **Verrouillé**, ajouter et supprimer des lignes contrat et annuler un contrat. Pour connaître l’état de votre activité mesurée en termes de gains et pertes, vous pouvez effectuer une analyse commerciale rapide avec la fonctionnalité Trendscape contrat.

## <a name="to-add-a-contract-line-to-a-service-contract-or-contract-quote" />Pour ajouter une ligne contrat à un contrat de service ou à un devis contrat
Lorsqu’un client achète un nouvel article et souhaite l’inclure dans le contrat de service ou le devis contrat existant, vous pouvez enregistrer l’article en tant qu’article de service et l’ajouter ensuite en tant que nouvelle ligne contrat au contrat ou au devis contrat.  

1. Sélectionnez l’icône ![Ampoule qui ouvre la fonction Tell Me.](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire") entrez **Contrats de service**, puis sélectionnez le lien associé.  
2. Ouvrez le contrat de service ou devis de contrat de service auquel vous voulez ajouter une ligne.  
3. Choisissez l’action **Ouvrir contrat** pour ouvrir le contrat de service ou le devis contrat de service et le modifier.  
4. Accédez au raccourci **Détail facture** et activez le champ **Autoriser montants non soldés** si vous souhaitez modifier le montant annuel et répartir la différence du montant annuel manuellement dans les lignes de contrat. Sinon, désactivez le champ **Autoriser montants non soldés**. Une fois que vous avez modifié le montant annuel, cela répartit automatiquement la différence du montant annuel dans les lignes contrat.  
5. Sur le raccourci **Lignes**, ajoutez un article de service, un article ou une description de texte, sur chaque ligne contrat. Vous pouvez également ajouter des lignes devis contrat. Vous pouvez créer plusieurs contrats par article de service de façon à ce qu’il soit inclus dans différents contrats de service ou devis contrat simultanément.  
6. Vérifiez et corrigez les valeurs dans les champs **% remise ligne**, **Montant remise ligne**, **Délai de réponse**, **Période service** et d’autres champs, le cas échéant.

## <a name="to-remove-contract-lines" />Pour retirer des lignes contrat
Vous pouvez supprimer des lignes du contrat de service lorsque vous supprimez du contrat de service les articles de service correspondants. Généralement, vous supprimez une ligne contrat expirée ou qui correspond à l’article de service qui est tombé en panne.  

1. Sélectionnez l’icône ![Ampoule qui ouvre la fonction Tell Me.](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire") entrez **Contrats de service**, puis sélectionnez le lien associé.  
2. Ouvrez le contrat de service dont vous voulez supprimer des lignes.  
3. Choisissez l’action **Ouvrir contrat** pour ouvrir le contrat de service et le modifier.  
4. Choisissez la ligne contrat à supprimer. Renseignez le champ **Date expiration contrat** avec la date à compter de laquelle vous souhaitez supprimer la ligne. Par exemple, vous pourriez saisir la date à laquelle l’article de service est tombé en panne.  
5. Choisissez l’action **Supprimer lignes contrat**. La page **Supprimer lignes contrat** s’ouvre.  
6. Remplissez les filtres par défaut : **N° contrat**, **N° article de service** et **Type contrat**. Si nécessaire, vous pouvez appliquer des filtres supplémentaires ou modifier les filtres existants.  
7. Renseignez les champs du raccourci **Options**, puis sélectionnez l’action **Supprimer des lignes**.  

> [!NOTE]  
>  Si le contrat n’est pas détaillé, vous devez mettre à jour la valeur du champ **Montant annuel** du raccourci **Détail facture** de la page **Contrat de service** afin d’indiquer que l’article de service a disparu du contrat.  
>   
>  Si le contrat est détaillé et prépayé, et que vous avez validé des factures pour le contrat, vous pouvez créer un avoir pour ce contrat. Choisissez l’action **Créer avoir**. Cela n’est pas nécessaire si la case à cocher **Avoirs automatiques** sur le raccourci **Détails facture** est sélectionnée. Dans ce cas un avoir est créé automatiquement lorsque vous supprimez une ligne contrat.

## <a name="service-line-cost-and-value" />Coût et valeur Ligne service
Sur les lignes contrat de service, les montants des champs **Coût ligne** et **Valeur ligne** sont calculés comme indiqué dans les tableaux suivants.

| Options Coût ligne | Désignation|
|----------------------------------|---------------------------------------|  
|**Article de service** | Le coût est automatiquement récupéré à partir du champ **Valeur contrat par défaut** de la table **Article de service** et copié dans le champ **Coût ligne**. La formule suivante est utilisée pour calculer le coût ligne :<br /><br /> Coût unitaire vente x % valeur contrat / 100.|  
|**Article** | Le coût est automatiquement récupéré dans le champ **Coût unitaire** de la table **Article** et la valeur du champ **% valeur contrat** de la table **Paramètres Gestion des services**. La formule suivante est utilisée pour calculer le coût ligne :<br /><br /> Coût unitaire x % valeur contrat / 100.|  
|**Une description texte** | La valeur du champ **Coût ligne** est mise à zéro.|  

| Options Valeur ligne | Désignation|
|----------------------------------|---------------------------------------|  
|**Article de service** | Le prix est automatiquement récupéré à partir du champ **Valeur contrat par défaut** de la table **Article de service** et copié dans le champ **Valeur ligne**.|  
|**Article** | en fonction de la valeur du champ **Mode calcul valeur contrat** de la table **Paramètres Gestion des services**, le montant est récupéré soit du champ **Prix unitaire** ou **Coût unitaire** de la table **Article**. Après quoi, cette valeur est multipliée par la valeur du champ **% valeur contrat** dans la table **Paramètres Gestion des services** et divisée par 100. Ce montant est copié dans le champ **Valeur ligne**.<br /><br /> **NOTE :** si le champ **Mode calcul valeur contrat** est paramétré sur **Aucun**, l’application ne calcule pas la valeur du champ **Valeur ligne**.|  
|**Une description texte** | La valeur du champ **Valeur ligne** est mise à zéro.|  

## <a name="to-add-a-contract-discount-to-service-contract-quotes" />Pour ajouter une remise contrat pour des devis contrats de service
Vous pouvez ajouter des remises contrat sur des services pour les devis contrat et les contrats de service. Les remises peuvent être accordées sur les pièces de rechange d’un groupe article de service particulier, sur les heures ressource des ressources d’un groupe ressources particulier, et sur des coûts service particuliers.

1. Sélectionnez l’icône ![Ampoule qui ouvre la fonction Tell Me.](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire") entrez **Devis de contrats de service**, puis sélectionnez le lien associé.  
2. Choisissez le devis auquel ajouter des remises.  
3. Choisissez l’action **Remises service**. La page **Remise contrat/service** s’affiche.  
4. Pour créer une remise contrat, choisissez l’action **Nouveau**.  
5. Renseignez les champs de la ligne selon vos besoins. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)].  

> [!Tip]  
>  Pour ajouter des remises contrat directement à un contrat service, exécutez la procédure décrite sur la page **Liste des contrats de service**.  

## <a name="to-change-the-owner-of-a-service-contract" />Pour changer le propriétaire d’un contrat de service
Vous pouvez devoir changer le propriétaire d’un contrat de service. Si un article de service dans un contrat de service est enregistré dans plusieurs contrats non annulés et détenus par le même client, le propriétaire de tous les contrats de service qui comprennent cet article de service et de tous les articles de service inclus dans ces contrats est mis à jour automatiquement.  

> [!NOTE]  
>  Dans ce cas, seuls les contrats non annulés sont pris en compte. Le statut des devis contrat n’est pas pris en compte.  

> [!IMPORTANT]  
>  Les articles de service et les contrats peuvent être liés. La modification du propriétaire d’un contrat de service peut affecter ces relations.  
>   
>  Par exemple, supposons que l’article de service n° 8 est inclus dans les contrats SC00003 et SC00015. Le contrat SC00015 contient également l’article de service n° 15, qui est aussi inclus dans le contrat SC00080. Dans ce cas, le propriétaire des trois contrats et des articles de service est modifié.  

1. Sélectionnez l’icône ![Ampoule qui ouvre la fonction Tell Me.](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire") entrez **Contrats de service**, puis sélectionnez le lien associé. Ouvrez le contrat de service dont vous voulez modifier le propriétaire.  
2. Choisissez l’action **Ouvrir contrat** pour ouvrir le contrat et le modifier.  
3. Choisissez l’action **Modifier client**. La page **Modifier le client du contrat** s’ouvre.  
4. Dans les champs **N° contrat** et **N° article de service**, vous pouvez voir les numéros du contrat et de l’article de service du client sélectionné. Si le client possède plusieurs contrats contenant plusieurs articles de service, la valeur de ces champs est **Multiple**. Pour visualiser la liste des contrats ou des articles de service correspondants, sélectionnez ces valeurs de champ.  
5. Dans le champ **Nouveau n° client** , choisissez le nouveau client.  
6. Dans le champ **Nouveau code destinataire**, choisissez l’adresse.  
7. Cliquez sur le bouton **OK** pour modifier le client et/ou le code destinataire des contrats de service.  
8. Choisissez l’action **Verrouiller contrat** pour verrouiller le contrat et vous assurer que les changements sont appliqués dans les contrats.  

## <a name="to-update-a-service-contract-price" />Réviser un tarif de contrat de service
Vous pouvez mettre à jour les tarifs des contrats de service en indiquant un pourcentage révision tarif.  

1. Sélectionnez l’icône ![Ampoule qui ouvre la fonction Tell Me.](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire") entrez **Réviser tarifs contrat service**, puis sélectionnez le lien associé.
2. Choisissez le contrat de service.  
3. Dans le champ **Date révision**, saisissez une date. Le traitement par lots révise les tarifs de tous les contrats dont la prochaine date de mise à jour de tarif est antérieure ou égale à cette date.  
4. Saisissez le pourcentage à utiliser pour la révision des tarifs dans le champ **% révision tarif**.  
5. Dans le champ **Action**, sélectionnez **Réviser tarifs contrat**.  

## <a name="to-post-prepaid-contract-entries" />Pour valider des écritures contrat prépayé
Si vous utilisez des contrats de service prépayés, vous devez valider régulièrement les écritures contrat prépayé, de manière à transférer les paiements prépayés du compte contrat prépayé sur les comptes contrats ordinaires.  

Avant de pouvoir valider les écritures contrat prépayé, vous devez spécifier une souche de numéros dans le champ **N° doc. prépayé validation** de la page **Paramètres Gestion des services**.  

1. Sélectionnez l’icône ![Ampoule qui ouvre la fonction Tell Me.](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire") saisissez **Valider écr. contrat prépayé**, puis sélectionnez le lien associé.  
2. Dans le champ **Dernière date compta.**, entrez une date. Le traitement par lots valide les écritures comptables service dont la date comptabilisation est antérieure à cette date.  
4. Dans le champ **Date comptabilisation**, saisissez la date que vous souhaitez utiliser comme date comptabilisation sur les lignes feuille comptabilité.  
5. Dans le champ **Action**, choisissez **Valider transactions prépayées**.  
6. Choisissez **OK** pour valider les écritures.

## <a name="changing-the-service-contract-status" />Modifier le statut d’un contrat de service
Après signature du contrat de service, la valeur du champ **Changer statut** est automatiquement paramétrée sur **Verrouillé**. Si vous souhaitez modifier des informations dans le contrat de service ou dans le devis contrat de service, vous devez d’abord remplacer le statut **Verrouillé** du contrat ou du devis contrat par **Ouvert**. Notez que vous ne pouvez pas créer des factures service pour le contrat de service avec le statut modifié **Ouvert**. Après modification du contrat ou du devis contrat, vous devez réaffecter le statut **Verrouillé** afin de permettre de nouveau la création de factures service et d’écritures comptables pour le contrat de service, et d’enregistrer les modifications que vous y avez apportées.  

> [!NOTE]  
>  Le champ **Modifier statut** n’est pas lié au champ **Statut de lancement** de l’en\-tête commande service, qui régit la gestion des articles de service au niveau de l’entrepôt.  

## <a name="to-cancel-a-service-contract" />Pour annuler un contrat de service
Vous pouvez annuler un contrat de service lorsqu’il a expiré ou qu’il a été annulé par vous et/ou le client.  

> [!NOTE]  
>  Vous ne pouvez pas rouvrir un contrat après l’avoir annulé.  

1. Sélectionnez l’icône ![Ampoule qui ouvre la fonction Tell Me.](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire") entrez **Contrats de service**, puis sélectionnez le lien associé.  
2. Ouvrez le contrat de service à annuler.  
3. Choisissez l’action **Ouvrir contrat** pour ouvrir le contrat de service et le modifier.  
4. Dans le champ **Code motif annulation**, choisissez le code motif adéquat. Pour ajouter des codes motif, cliquez sur l’action **Avancé**.  

     Si le champ **Utiliser motif annulation contrat** est activé sur la page **Paramètres Gestion des services**, vous devez indiquer un code motif annulation lorsque vous annulez des contrats.  

5. Dans le champ **Statut**, choisissez **Annulé**.  
6. S’il existe des factures, des avoirs ou des écritures prépayées ouvertes non validées pour le contrat, un message de confirmation apparaît. Dans la zone de message, choisissez **Non** pour revenir au contrat et valider les documents, ou **Oui** pour poursuivre l’annulation du contrat.  

## <a name="filing-a-service-contract-or-contract-quote" />Remplir un contrat de service ou un devis contrat
Vous pouvez archiver à tout moment des contrats de service et des devis contrat pour enregistrer et archiver une copie du contrat ou du devis contrat. [!INCLUDE[prod_short](includes/prod_short.md)] archive automatiquement les contrats de service lorsque vous convertissez les devis contrat en contrats de service ou que vous annulez des contrats de service. Vous pouvez archiver un contrat ou un devis vous-même en choisissant l’action **Archiver contrat** sur les pages **Contrats de service** ou **Devis contrat de service**. Vous pouvez consulter vos contrats ou devis archivés en recherchant **Contrats archivés**.

## <a name="see-also" />Voir aussi
[Configurer des contrats de service](service-how-setup-service-contracts.md)  
[Gestion des services](service-service.md)  
[Convertir les contrats de service incluant des montants TVA](service-how-to-convert-service-contracts.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
