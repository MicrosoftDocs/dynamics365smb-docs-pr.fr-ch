---
title: Procédure d'utilisation de la TVA sur les ventes et les achats | Microsoft Docs
description: Cette rubrique décrit comment effectuer des tâches telles que la correction de la TVA validée. Dans les pays/régions de l'UE, chaque transaction de vente et d'achat est soumise à des calculs de TVA. Elle décrit la procédure à suivre.
author: bholtorf
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: VAT, sales, purchases,
ms.date: 04/01/2020
ms.author: bholtorf
ms.openlocfilehash: b870e3370d6af99320593653f49f69936b179c22
ms.sourcegitcommit: 88e4b30eaf6fa32af0c1452ce2f85ff1111c75e2
ms.translationtype: HT
ms.contentlocale: fr-CH
ms.lasthandoff: 04/01/2020
ms.locfileid: "3182651"
---
# <a name="work-with-vat-on-sales-and-purchases"></a>Utiliser la TVA sur les ventes et les achats
Si votre pays ou région vous demande de calculer la TVA sur les transactions de vente et d'achat afin de pouvoir déclarer les montants à une administration fiscale, vous pouvez configurer [!INCLUDE[d365fin](includes/d365fin_md.md)] pour calculer automatiquement la TVA sur les documents vente et achat. Pour plus d'informations, voir [Configuration des méthodes de calcul et de validation de la taxe sur la valeur ajoutée](finance-setup-vat.md).

Il existe, cependant, certaines tâches associées à la TVA que vous pouvez effectuer manuellement. Par exemple, vous devrez peut-être corriger un montant validé si vous découvrez qu'un fournisseur utilise un mode d'arrondi différent.

## <a name="calculating-and-displaying-vat-amounts-in-sales-and-purchase-documents"></a>Calcul et affichage des montants de TVA dans des documents achat et vente  
Vous pouvez calculer et afficher des montants de TVA dans des documents achat et vente de façon différente, en fonction du type de client ou de fournisseur avec lequel vous traitez. Vous pouvez également remplacer le montant de TVA calculé pour qu'il corresponde au montant de TVA calculé par le fournisseur sur une transaction donnée.  

### <a name="unit-price-and-line-amount-includingexcluding-vat-on-sales-documents"></a>Prix unitaire et montant ligne incluant/excluant la TVA sur les documents vente  
Lorsque vous sélectionnez un numéro d'article dans le champ **N°** d'un document vente, [!INCLUDE[d365fin](includes/d365fin_md.md)] renseigne le champ **Prix unitaire**. Le prix unitaire provient de la fiche **Article** ou des prix article autorisés pour l'article et le client. [!INCLUDE[d365fin](includes/d365fin_md.md)] calcule le **Montant ligne** lorsque vous entrez une quantité pour la ligne.  

Si vous vendez au détail à des consommateurs, vous souhaitez peut-être que les documents vente incluent la TTC. Pour ce faire, activez la case à cocher **Prix TTC** du document.  

### <a name="including-or-excluding-vat-on-prices"></a>Inclusion ou exclusion de la TVA sur les prix
Si la case à cocher **Prix TTC** est activée sur un document vente, les champs **Prix unitaire** et **Montant ligne** incluent la TVA, ce que les noms de champ reflètent également. Par défaut, la TVA n'est pas incluse dans ces champs.  

Si le champ n'est pas sélectionné, l'application renseigne les champs **Prix unitaire** et **Montant ligne** en excluant la TVA, ce que reflètent les noms de champ.  

Vous pouvez configurer les paramètres par défaut de **Prix TTC** pour tous les documents vente relatifs à un client dans le champ **Prix TTC** sur la fiche **Client**. Vous pouvez également configurer des prix article pour inclure ou exclure la TVA. Normalement, les prix article contenus dans la fiche article sont les prix hors TVA. L'application utilise les informations du champ **Prix TTC** de la fiche **Article** pour déterminer le prix unitaire pour les documents vente.  

Le tableau suivant montre comment l'application calcule les montants de prix unitaire pour un document vente lorsque vous n'avez pas configuré de prix sur la page **Prix vente** :  

|**Le prix inclut le champ TVA sur la fiche client.**|**Prix incluant le champ TVA dans l'en-tête vente**|**Action exécutée**|  
|-----------------------------------------------|----------------------------------------------------|--------------------------|  
|Désactivé|Désactivé|Le champ **Prix unitaire** de la fiche article est copié dans le champ **Prix unitaire HT** dans les lignes vente.|  
|Désactivé|Activé|L'application calcule le montant de TVA par unité et l'ajoute au **Prix unitaire** sur la fiche article. Ce prix unitaire total est entré dans le champ **Prix unitaire TTC** dans les lignes vente.|  
|Activé|Désactivé|L'application calcule le montant de la TVA inclus dans le **prix unitaire** sur la fiche article à l'aide du % TVA par rapport aux champs Gpe compta. marché TVA (prix) et Groupe compta. produit TVA. Le **prix unitaire** sur la fiche article, moins le montant de la TVA, est ensuite saisi dans le champ **Prix unitaire HT** dans les lignes de vente.|  
|Activé|Activé|Le champ **Prix unitaire** de la fiche article est copié dans le champ **Prix unitaire TTC** dans les lignes vente.|

## <a name="correcting-vat-amounts-manually-in-sales-and-purchase-documents"></a>Correction manuelle des montants de TVA dans des documents achat et vente  
Vous pouvez apporter des corrections à des écritures TVA validées. Cela permet de modifier les montants de TVA vente ou achat sans modifier la base de TVA. Vous pouvez avoir besoin d'apporter des modifications, par exemple, si vous recevez une facture d'un fournisseur qui n'a pas calculé correctement la TVA.  

Bien que vous ayez configuré une ou plusieurs combinaisons pour traiter la TVA à l'importation, vous devez configurer au moins un groupe de comptabilisation produit TVA. Par exemple, vous pouvez l'appeler **CORRECT** à des fins de correction, à moins que vous puissiez utiliser le même compte général dans le champ **Compte TVA achat** sur la ligne des paramètres de comptabilisation TVA. Pour plus d'informations, voir [Configuration des méthodes de calcul et de validation de la taxe sur la valeur ajoutée](finance-setup-vat.md).

Si un escompte a été calculé sur la base d'un montant facture TTC, vous remboursez la partie escompte du montant TVA lorsque l'escompte est accordé. Remarque : vous devez activer le champ **Ajustement des escomptes** à la fois dans les paramètres comptabilité (en général) et dans les paramètres comptabilisation TVA, pour des combinaisons particulières de groupes comptabilisation marché TVA et de groupes comptabilisation produit TVA.  

### <a name="to-set-the-system-up-for-manual-vat-entry-in-sales-documents"></a>Pour configurer le système pour la saisie manuelle de la TVA dans les documents de vente
La section suivante explique comment activer les modifications manuelles de la TVA sur les documents de vente. Les étapes sont similaires sur la page **Paramètres achats**.

1. Dans la page **Paramètres comptabilité**, spécifiez une **Différence TVA max. autorisée** entre le montant calculé par l'application et le montant calculé manuellement.  
2. Dans la page **Paramètres ventes**, activez le champ **Autoriser différence TVA**.  

### <a name="to-adjust-vat-for-a-sales-document"></a>Pour ajuster la TVA pour un document vente  
1. Ouvrez la commande vente appropriée.  
2. Sélectionnez l'action **Statistiques**.  
3. Dans l'organisateur **Facturation**, choisissez la valeur dans le champ **Nbre de lignes fiscales**.
4. Modifiez le champ **Montant TVA**.   

> [!NOTE]  
> Le montant de TVA total de la facture et l'identifiant TVA s'affichent dans les lignes. Vous pouvez ajuster les montants manuellement dans le champ **Montant TVA** des lignes correspondant à chaque identifiant TVA. Lorsque vous modifiez la valeur du champ **Montant TVA**, l'application vérifie que vous n'avez pas modifié la TVA d'une valeur supérieure à celle du montant spécifié comme différence maximale autorisée. Si le montant se situe en dehors de la plage **Différence TVA max. autorisée**, un avertissement s'affiche, indiquant la différence maximale autorisée. Vous ne pouvez pas poursuivre tant que le montant n'est pas ajusté conformément aux paramètres acceptables. Cliquez sur **OK** , puis entrez un autre **Montant TVA** s'inscrivant dans la plage autorisée. Si la différence TVA est inférieure ou égale à la différence maximale autorisée, la TVA est répartie de façon proportionnelle entre les lignes document ayant le même identifiant TVA.  

## <a name="calculating-vat-manually-using-journals"></a>Calcul manuel de la TVA à l'aide de feuilles  
Vous pouvez également ajuster les montants TVA dans les feuilles comptabilité, vente et achat. Par exemple, vous devrez peut-être le faire lorsque vous entrez une facture fournisseur dans votre feuille et qu'il y a une différence entre le montant de TVA calculé par [!INCLUDE[d365fin](includes/d365fin_md.md)] et le montant de TVA figurant sur la facture que vous avez reçue du fournisseur.  

### <a name="to-set-the-system-up-for-manual-vat-entry-in-a-general-journals"></a>Pour configurer le système pour la saisie manuelle de la TVA dans les feuilles comptabilité
Vous devez suivre les étapes suivantes avant de saisir manuellement la TVA dans une feuille comptabilité.  

1. Dans la page **Paramètres comptabilité**, spécifiez une **Différence TVA max. autorisée** entre le montant calculé par l'application et le montant calculé manuellement.  
2. Sur la page **Modèles feuille comptabilité**, activez la case à cocher **Autoriser différence TVA** pour la feuille appropriée.  

### <a name="to-set-the-system-up-for-manual-vat-entry-in-a-sales-and-purchase-journals"></a>Pour configurer le système pour la saisie manuelle de la TVA dans les feuilles vente et achat
Vous devez suivre les étapes suivantes avant de saisir manuellement la TVA dans une feuille vente et achat.

1. Sur la page **Paramètres achats**, activez la case à cocher **Autoriser différence TVA**.  
2. Répétez l'étape 1 pour la page **Paramètres ventes**.
3. Après avoir effectué la configuration décrite ci-avant, vous pouvez ajuster la valeur du champ **Montant TVA** de la ligne feuille comptabilité ou du champ **Montant TVA contrepartie** de la ligne feuille achat ou vente. [!INCLUDE[d365fin](includes/d365fin_md.md)] vérifie que la différence n'est pas supérieure à la valeur maximale spécifiée.  

    > [!NOTE]  
    > Si la différence est supérieure, un avertissement s'affiche, indiquant la différence maximale autorisée. Pour continuer, vous devez ajuster le montant. Sélectionnez **OK**, puis entrez un montant compris dans la plage autorisée. Si la différence de TVA est inférieure ou égale à la valeur maximale autorisée, [!INCLUDE[d365fin](includes/d365fin_md.md)] affiche la différence dans le champ **Différence TVA**.  

## <a name="posting-import-vat-with-purchase-invoices"></a>Validation de la TVA à l'importation dans les factures achat
Au lieu d'utiliser des feuilles comptabilité pour valider une facture TVA importation, vous pouvez utiliser une facture achat.  

### <a name="to-set-up-purchasing-for-posting-import-vat-invoices"></a>Pour paramétrer l'achat pour une validation des factures TVA à l'importation  
1. Paramétrer une fiche fournisseur pour l'administration d'importation qui vous envoie la facture TVA à l'importation. Les champs **Groupe compta. marché** et **Groupe compta. marché TVA** doivent être configurés de la même manière que le compte général pour la TVA à l'importation.  
2. Créez un **Groupe compta. produit** pour la TVA importation et paramétrez un **Gpe compta. produit TVA défaut** (TVA importation) pour le **Groupe compta. produit** lié.  
3. Choisissez l'icône ![Ampoule qui ouvre la fonction Tell Me](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire"), entrez **Plan comptable**, puis sélectionnez le lien associé.  
4. Sélectionnez le compte général de TVA à l'importation, puis sélectionnez l'action **Modifier**.  
5. Sur le raccourci **Validation**, sélectionnez la configuration **Groupe compta. produit** pour importer la TVA. [!INCLUDE[d365fin](includes/d365fin_md.md)] renseigne automatiquement le champ **Groupe compta. produit TVA**.  
6. Choisissez l'icône ![Ampoule qui ouvre la fonction Tell Me](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire"), entrez **Paramètres comptabilisation**, puis sélectionnez le lien associé.  
7. Créez une combinaison de **Groupe comptabilisation marché** pour l'administration fiscale et de **Groupe compta. produit** pour la TVA d'importation. Pour cette nouvelle combinaison, dans le champ **Compte achat**, sélectionnez le compte général de la TVA à l'importation.  

### <a name="to-create-a-new-invoice-for-the-import-authority-vendor-once-you-have-completed-the-setup"></a>Pour créer une facture pour le fournisseur de l'administration d'importation, une fois le paramétrage terminé  
1. Choisissez l'icône ![Ampoule qui ouvre la fonction Tell Me](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire"), entrez **Factures achat**, puis sélectionnez le lien associé.  
2. Créez une facture achat.  
3. Dans le champ **N° fournisseur**, sélectionnez le fournisseur de l'administration d'importation, puis cliquez sur **OK**.  
4. Sur la ligne achat, dans le champ **Type**, sélectionnez **Compte général** et dans le champ **N°**, sélectionnez le compte général TVA importation.  
5. Dans le champ **Quantité**, tapez **1**.  
6. Dans le champ **Coût unitaire direct HT**, indiquez le montant de la TVA.  
7. Validez la facture.  

## <a name="processing-certificates-of-supply"></a>Traitement des certificats d'approvisionnement
Lorsque vous vendez des biens à un client dans un autre pays/une autre région de l'UE, vous devez envoyer au client un certificat d'approvisionnement que le client doit signer et vous renvoyer. Les procédures suivantes servent à traiter les certificats d'approvisionnement pour des expéditions vente, mais les mêmes étapes s'appliquent aux expéditions service des articles, ainsi qu'aux expéditions retour aux fournisseurs.  

### <a name="to-view-certificate-of-supply-details"></a>Pour afficher les détails d'un certificat d'approvisionnement  
1. Choisissez l'icône ![Ampoule qui ouvre la fonction Tell Me](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire"), entrez **Expéditions vente enregistrées**, puis sélectionnez le lien associé.  
2. Sélectionnez l'expédition vente appropriée à un client dans un autre pays/une autre région de l'UE.  
3. Sélectionnez **Détails certificat d'approvisionnement**.  
4. Par défaut, si la case à cocher **Certificat d'approvisionnement requis** est activée pour la configuration de groupe comptabilisation TVA pour le client, le champ **Statut** est défini sur **Requis**. Vous pouvez mettre à jour le champ pour indiquer si le client a retourné le certificat.  

    > [!Note]  
    >  Si la configuration de groupes comptabilisation TVA n'a pas la case **Certificat d'approvisionnement requis** cochée, alors un enregistrement est créé et le champ **Statut** est défini sur **Non applicable**. Vous pouvez mettre à jour le champ pour tenir compte des informations correctes de statut. Vous pouvez modifier manuellement le statut de **Non applicable** en **Requis**, et de **Requis** en **Non applicable** selon vos besoins.  

   Lorsque vous mettez à jour le champ **Statut** sur **Requis**, **Reçu** ou **Non reçu**, un certificat est créé.  

    > [!TIP]  
    >  Vous pouvez utiliser la page **Certificats d'approvisionnement** pour obtenir une vue du statut de toutes les expéditions validées pour lesquelles un certificat d'approvisionnement a été créé.  

5. Sélectionnez **Imprimer le certificat d'approvisionnement**.  

    > [!Note]  
    >  Vous pouvez afficher un aperçu ou imprimer le document. Lorsque vous choisissez **Imprimer le certificat d'approvisionnement** et que vous imprimez le document, la case à cocher **Imprimé** est automatiquement sélectionnée. En outre, s'il n'est pas déjà renseigné, le statut du certificat est mis à jour sur **Requis**. Si nécessaire, vous incluez le certificat imprimé à l'expédition.  

### <a name="to-print-a-certificate-of-supply"></a>Pour imprimer un certificat d'approvisionnement  
1. Choisissez l'icône ![Ampoule qui ouvre la fonction Tell Me](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire"), entrez **Expéditions vente enregistrées**, puis sélectionnez le lien associé.  
2. Sélectionnez l'expédition vente appropriée à un client dans un autre pays/une autre région de l'UE.  
3. Sélectionnez l'action **Imprimer le certificat d'approvisionnement**.  

    > [!NOTE]  
    >  Sinon, vous pouvez imprimer un certificat à partir de la page **Certificat d'approvisionnement**.  

4. Pour inclure des informations des lignes dans le document expédition sur le certificat d'approvisionnement, sélectionnez la case à cocher **Imprimer détails de ligne**.  
5. Activez la case à cocher **Créer des certificats d'approvisionnement s'ils n'ont pas encore été créés** pour que [!INCLUDE[d365fin](includes/d365fin_md.md)] crée des certificats pour les expéditions validées qui n'en ont pas au moment de l'exécution. Lorsque vous activez la case à cocher, de nouveaux certificats sont créés pour toutes les expéditions validées qui n'ont pas de certificats compris dans la plage sélectionnée.  
6. Par défaut, les paramètres de filtrage concernent le document d'expédition que vous avez sélectionné. Renseignez les informations de filtre pour sélectionner un certificat d'approvisionnement spécifique à imprimer.  
7. Dans la page **Certificat d'approvisionnement**, sélectionnez l'action **Imprimer** pour imprimer l'état ou l'action **Aperçu** pour l'afficher à l'écran.  

    > [!Note]  
    > Le champ **Statut Certificat d'approvisionnement** et le champ **Imprimé** sont mis à jour pour la livraison sur la page **Certificats d'approvisionnement**.  

8. Envoyez le certificat d'approvisionnement imprimé au client pour signature.  

### <a name="to-update-the-status-of-a-certificate-of-supply-for-a-shipment"></a>Pour mettre à jour le statut d'un certificat d'approvisionnement pour une expédition  
1. Choisissez l'icône ![Ampoule qui ouvre la fonction Tell Me](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire"), entrez **Expéditions vente enregistrées**, puis sélectionnez le lien associé.  
2. Sélectionnez l'expédition vente appropriée à un client dans un autre pays/une autre région de l'UE.  
3. Dans le champ **Statut**, sélectionnez l'option appropriée.  

   Si le client a retourné le certificat d'approvisionnement signé, choisissez **Reçu**. Le champ **Date de réception** est mis à jour. Par défaut, la date de réception est configurée sur la date de travail actuelle.  

   Vous pouvez modifier la date pour tenir compte de la date à laquelle vous avez reçu le certificat d'approvisionnement signé du client. Vous pouvez également ajouter un lien vers le certificat signé à l'aide des liaisons standard de [!INCLUDE[d365fin](includes/d365fin_md.md)].  

   Si le client ne retourne pas le certificat d'approvisionnement signé, choisissez **Non reçu**. Vous devez envoyer au client une nouvelle facture qui inclut la TVA, parce que la facture initiale ne sera pas acceptée par l'administration fiscale.  

Pour afficher un groupe de certificats, vous commencez à partir de la page **Certificats d'approvisionnement**, puis mettez à jour les informations concernant le statut des certificats en attente à mesure que vous les recevez de la part de vos clients. Ceci peut être utile si vous souhaitez rechercher tous les certificats ayant un certain statut, par exemple, **Requis**, si vous souhaitez mettre à jour leur statut en **Non reçu**.  

### <a name="to-update-the-status-of-a-group-of-certificates-of-supply"></a>Pour mettre à jour le statut d'un groupe de certificats d'approvisionnement  
1. Choisissez l'icône ![Ampoule qui ouvre la fonction Tell Me](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire"), entrez **Certificats d'approvisionnement**, puis sélectionnez le lien associé.  
2. Filtrez le champ **Statut** sur la valeur que vous souhaitez afin de créer la liste des certificats que vous souhaitez gérer.  
3. Pour mettre les informations de statut à jour, sélectionnez **Modifier la liste**.  
4. Dans le champ **Statut**, sélectionnez l'option appropriée.  

   Si le client a retourné le certificat d'approvisionnement signé, choisissez **Reçu**. Le champ **Date de réception** est mis à jour. Par défaut, la date de réception est configurée sur la date de travail actuelle.  

   Vous pouvez modifier la date pour tenir compte de la date à laquelle vous avez reçu le certificat d'approvisionnement signé. Vous pouvez également ajouter un lien vers le certificat signé à l'aide des liaisons de document standard de [!INCLUDE[d365fin](includes/d365fin_md.md)].  

    > [!NOTE]  
    >  Vous ne pouvez pas créer un nouveau certificat d'approvisionnement sur la page **Certificat d'approvisionnement** lorsque vous y accédez à l'aide de cette procédure. Pour créer un certificat pour une expédition qui n'a pas été configurée pour en exiger, ouvrez l'expédition vente validée et utilisez l'une des deux procédures décrites ci-dessus :  
    >   
    > * Pour créer manuellement un certificat d'approvisionnement.  
    > * Pour imprimer un certificat d'approvisionnement.

## <a name="see-related-training-at-microsoft-learn"></a>Voir la formation associée sur [Microsoft Learn](/learn/paths/process-vat-dynamics-365-business-central/)

## <a name="see-also"></a>Voir aussi  
[Configuration des méthodes de calcul et de validation de la taxe sur la valeur ajoutée](finance-setup-vat.md)   
[Déclarer la TVA à une autorité fiscale](finance-how-report-vat.md)   
