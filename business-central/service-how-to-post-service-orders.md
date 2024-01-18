---
title: Procédure pour valider des commandes service
description: 'Après avoir créé une commande service, fourni toutes les informations et apporté les éventuelles modifications, vous pouvez valider cette commande.'
author: brentholtorf
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: null
ms.date: 12/13/2023
ms.author: bholtorf
---
# <a name="post-service-orders-and-credit-memos"></a>Validation des commandes et des avoirs service
Après avoir créé une commande service, fourni toutes les informations et apporté les éventuelles modifications, vous pouvez valider cette commande. Pour que vous puissiez valider une commande, celle-ci doit contenir au moins une ligne service et une ligne facture service avant. Si la commande contient plusieurs lignes service, toutes les lignes sont validées en même temps.  

Si vous avez un grand nombre de commandes service, vous pouvez gagner du temps en ayant recours à un traitement par lots pour les valider simultanément. Vous pouvez exécuter le traitement par lots à partir d’une commande service.

> [!Tip]
> Avant de valider un document service, il est recommandé d’utiliser l’action **Impression test** pour vérifier toutes les erreurs ou informations manquantes. S’il existe des erreurs, vous devez corriger le problème. Vous pouvez effectuer une nouvelle impression test pour vérifier le correctif, puis valider le document.

## <a name="to-post-a-service-order"></a>Pour valider des commandes service :
1. Sélectionnez l’icône ![Ampoule qui ouvre la fonction Tell Me.](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire") entrez **Commandes service**, puis choisissez le lien associé.  
2. Ouvrez la commande service.  
3. Sur la page **Commande service**, choisissez l’une des actions suivantes.  

    |**Fonction**|**Résultat**|  
    |------------------|----------------|  
    |**Impression test** | Vérifie tous les éléments du document et présente les résultats dans un état. Si l’état indique des erreurs ou un manque d’informations, vous devez corriger le problème. Vous pouvez ensuite procéder à une nouvelle impression test.|  
    |**Valider** | Valide la commande sans imprimer de bon de livraison ou de facture.|  
    |**Valider et Imprimer** | Valide la commande et imprime un bon de livraison (si vous expédiez la commande sans la facturer) ou une facture (si vous facturez la commande).|  
    |**Valider par lot** | Valide plusieurs commandes service en une seule fois.|  

4. Lorsque vous validez la commande, vous devez choisir l’une des options suivantes indiquant la manière dont vous souhaitez valider la commande.  

    |**Option de validation**|**Résultat**|  
    |------------------------|----------------|  
    |**Livraison** | Valide l’expédition des articles.|  
    |**Facture** | Facture les articles déjà expédiés.|  
    |**Expédition et facturation** | Livre et facture les articles.|  
    |**Livrer et consommer** | Valide l’expédition et la consommation sur la commande. Il met à jour les quantités appropriées sur les lignes de service actuelles de la commande et sur le document expédition service validé précédemment.|  

Vous ne pouvez valider la consommation que si la ligne contient une quantité qui a été expédiée mais pas facturée ni consommée.  

Lors de la validation de la commande, les écritures et les documents validés correspondants sont créés. Les champs appropriés dans le document commande service sont mis à jour.  

## <a name="to-batch-post-service-orders"></a>Pour valider des commandes service à l’aide d’un traitement par lots
1. Sélectionnez l’icône ![Ampoule qui ouvre la fonction Tell Me.](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire") entrez **Commandes service**, puis choisissez le lien associé.  
2. Sélectionnez l’action **Valider par lot**.  
3.  Vous pouvez positionner un filtre pour sélectionner des numéros commande service ou un intervalle de numéros commande pour le traitement par lots à effectuer.  
4.  Cliquez sur **OK** pour démarrer le traitement par lots.  

## <a name="to-post-a-service-credit-memo"></a>Pour valider des avoirs service
Après avoir créé un avoir service et l’avoir renseigné, vous pouvez valider l’avoir. S’il y a des erreurs ou l’absence de certaines informations sur l’avoir crédit lors de la validation, le processus est interrompu par un message d’erreur.  

1. Sélectionnez l’icône ![Ampoule qui ouvre la fonction Tell Me.](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire") entrez **Avoirs service**, puis sélectionnez le lien associé.  
2. Créez un avoir service. Sélectionnez l’action **Nouveau**.  
3. Renseignez les champs suivants.  
4. Sélectionnez l’action **Valider**. Si vous souhaitez imprimer et valider l’avoir simultanément, choisissez plutôt l’action **Valider et imprimer**.  
5. Pour tester des avoirs avant de les valider, choisissez **Impression test**. Lorsque vous exécutez l’état, les dates de validation spécifiées dans le document sont vérifiées.  
6. Pour valider simultanément plusieurs avoirs service, exécutez le traitement par lots **TPL valider avoirs service**. Ceci peut être avantageux si vous avez beaucoup d’avoirs à valider.  

> [!NOTE]  
>  Il est important d'entrer toutes les informations nécessaires sur les avoirs avant de les valider par lots. Sinon, elles risquent de ne pas être validées. Lorsque le traitement par lots a terminé la validation, un message indique le nombre des avoirs service validés.  

## <a name="to-post-consumption-from-a-service-order"></a>Pour valider une consommation à partir d’une commande service
La procédure suivante décrit comment valider les articles, les heures et/ou coûts ressource utilisés pour une opération de service spécifique que vous n’allez pas facturer au client. Vous ne pouvez valider des articles, des heures et/ou des coûts consommés que pour une expédition validée pour laquelle il n’y a pas de facture ni de consommation validée.  

1. Sélectionnez l’icône ![Ampoule qui ouvre la fonction Tell Me.](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire") entrez **Commandes service**, puis choisissez le lien associé.  
2. Ouvrez la commande service dont vous voulez valider la consommation.  
3. Choisissez l’article de service. Choisissez l’action **Lignes service**.  
4. Recherchez les écritures requises et spécifiez les quantités pour lesquelles vous allez valider la consommation dans le champ **Qté à facturer**. La quantité ne peut pas être supérieure à la quantité déjà expédiée et la quantité restante, mais non facturée après la facturation partielle de cette expédition.  

    > [!NOTE]  
    >  Pour enregistrer la consommation relative à un projet, renseignez les champs **N° projet**, **N° tâche projet**, et **Type ligne projet** dans la ligne service.  

5. Choisissez les lignes à valider, puis sélectionnez l’action **Valider**. Sur la page qui s’ouvre, sélectionnez **Livrer et consommer**.  

Le service est validé comme étant consommé, entièrement ou partiellement, en fonction de la valeur renseignée dans le champ **Qté à consommer** et les écritures comptables correspondantes sont créées. En outre, les documents expédition service précédemment validés sont mis à jour, de façon chronologique, avec les quantités consommées. Les quantités appropriées sont mises à jour dans les lignes service de la commande.  

## <a name="to-post-shipments-from-service-orders"></a>Pour valider des expéditions à partir de commandes service
Après avoir spécifié les détails d’un service, vous pouvez ajuster et valider les quantités d’articles utilisées, le temps passé et les coûts exposés. Par conséquent, [!INCLUDE[prod_short](includes/prod_short.md)] apporte les modifications nécessaires afin de refléter le nouvel état du stock et le statut actuel du traitement de commande spécifique.  

La procédure suivante explique comment valider l’expédition des articles ligne service dans les magasins qui ne sont pas configuré pour appeler une gestion d’entrepôt.  

1. Sélectionnez l’icône ![en forme d’Ampoule qui ouvre la fenêtre de recherche](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire"), entrez **Commande service**, puis choisissez le lien associé. 2. Sur la page de la commande service sélectionnée, choisissez **Actions**, **Commande**, **Lignes service**.  
3. Sur la page **Lignes service**, recherchez les écritures requises, puis spécifiez la quantité à valider dans le champ **Qté à expédier**.  

   > [!NOTE]  
   >  La valeur de la quantité à expédier varie selon que vous voulez valider l'expédition entièrement ou partiellement. Si vous décidez d'expédier entièrement, la valeur renseignée dans le champ **Qté à expédier** doit être égale à celle renseignée dans le champ **Quantité**. Si vous validez une expédition partielle, vous devez spécifier la quantité que vous voulez expédier initialement. Si vous avez déjà expédié une partie du service en commande, prenez note de la valeur dans le champ **Qté expédiée**. La quantité maximale que vous pouvez entrer dans le champ **Qté à expédier** est le nombre d’unités qui n’ont pas encore été expédiées.  

4. Sélectionnez l’action **Valider**. Sur la page qui apparaît, sélectionnez le bouton **Expédier**.

[!INCLUDE[prod_short](includes/prod_short.md)] crée les écritures comptables appropriées (dans les écritures comptables garantie, les écritures comptables article, les écritures comptables service ou la comptabilité). Il génère également le document expédition service validé et met à jour les champs appropriés sur les lignes service de la commande service.  

Si le magasin est configuré pour exiger la gestion d’entrepôt, l’expédition et le déplacement d’articles de ligne service s’exécutent de la même manière que pour d’autres documents origine. La seule différence est que les articles de la ligne service peuvent être consommés en externe ou en interne et nécessitent donc deux fonctions de lancement différentes.  

Pour plus d’informations sur la manière d’expédier des articles ligne service dans les configurations d’entreposage avancées, accédez à Prélever des articles pour l’expédition entrepôt](warehouse-how-to-pick-items-for-warehouse-shipment.md).  

## <a name="to-undo-posted-consumption"></a>Pour annuler une consommation validée
Vous pouvez annuler la consommation sur les commandes service. Par exemple, parce qu’elle a été validée par erreur.  

1. Sélectionnez l’icône ![Ampoule qui ouvre la fonction Tell Me.](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire") entrez **Expéditions service validées**, puis sélectionnez le lien associé.  
2. Ouvrez l’expédition service validée pour laquelle la consommation erronée a été validée.  
3. Choisissez l’action **Lignes expédition service**.  
4. Sélectionnez les lignes contenant la consommation incorrecte, puis sélectionnez l’action **Annuler consommation**.  

 Une ligne expédition service d’équilibrage contenant des valeurs négatives est insérée dans les champs de quantité pour les lignes sélectionnées.  
  
> [!NOTE]  
>  Vous ne pouvez pas annuler la consommation service si :  

>    * La commande service a été clôturée.  
>    * Elle a été validée dans la zone Projets, ce qui signifie qu’aucune écriture comptable projet n’est liée à cette consommation.  

## <a name="to-post-service-lines"></a>Pour valider des lignes service
Si vous devez travailler sur une commande service pendant longtemps sans la valider, vous pouvez valider certaines des lignes service liées afin, par exemple de tenir votre stock à jour. Vous pouvez valider en spécifiant les quantités appropriées dans les lignes à valider. Vous pouvez décider de valider les lignes une à une en sélectionnant plusieurs lignes à la fois.  

La procédure suivante décrit la validation de l’expédition directement à partir d’une commande service dans des magasins sans configuration de gestion d’entrepôt. Si le magasin est configuré pour appeler une gestion d’entrepôt, la validation d’expédition a lieu dans un autre document entrepôt, en fonction de la configuration du magasin.

1. Sélectionnez l’icône ![Ampoule qui ouvre la fonction Tell Me.](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire") entrez **Commandes service**, puis choisissez le lien associé.  
2. Ouvrez la commande service, puis cliquez sur l’action **Lignes service**.  
4. Dans les lignes que vous allez valider, renseignez les champs **Qté à expédier**, **Qté à facturer** et/ou **Qté à consommer**, en fonction de la manière dont vous allez valider les lignes.  
5. Sélectionnez l’action **Valider**.

## <a name="see-also"></a>Voir aussi
[Validation dans la Gestion des services](service-service-posting.md)  
[Créer une commande service](service-how-to-create-service-orders.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
