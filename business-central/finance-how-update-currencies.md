---
title: Mettre à jour des taux de change devise
description: Suivez des montants dans différentes devises à l’aide de codes devise, et laissez Business Central ajuster les taux de devise étrangère des écritures validées avec un service externe.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.search.keywords: multiple currencies, adjust exchange rates, FX rates
ms.date: 07/23/2021
ms.author: edupont
ms.openlocfilehash: 44dd13f986098283d29e58d3e8c4ce0218b4a083
ms.sourcegitcommit: 41876b559872fe7adbfa5b59a6e1a71dc907fb15
ms.translationtype: HT
ms.contentlocale: fr-CH
ms.lasthandoff: 12/14/2021
ms.locfileid: "7921073"
---
# <a name="update-currency-exchange-rates"></a>Mettre à jour des taux de change devise

Étant donné que les sociétés opérent dans un nombre croissant de pays/régions, il devient essentiel qu’elles puissent échanger et générer des informations financières dans plusieurs devises. La devise société (DS) est définie dans la page **Paramètres comptabilité**, comme décrit dans l’article [ Configuration de Finance](finance-setup-finance.md). Une fois la devise société (DS) définie, elle sera représentée en tant que devise vide. Ainsi, lorsque le champ **Devise** est vide, cela signifie que la devise est DS.  

Ensuite, vous devez configurer des codes devise pour chaque devise que vous utilisez si vous achetez ou vendez dans des devises autres que votre devise société (DS). Des comptes bancaires peuvent également être créés à l’aide de devises. Il est possible d’enregistrer des transactions comptables dans différentes devises, cependant, la transaction comptable sera toujours validée dans la devise société (DS).

> [!Important]
> Ne créez pas le code devise société à la fois dans la page **Paramètres comptabilité** et dans la page **Devises**. Cela créera une confusion entre la devise vide et le code DS dans le tableau des devises, et des comptes bancaires, des clients ou des fournisseurs pourraient être créés accidentellement, certains avec la devise vide et d’autres avec le code DS.

Votre comptabilité est configurée pour utiliser votre devise société (DS), mais vous pouvez la configurer pour utiliser une autre devise avec un taux de change des devises. Si vous désignez une deuxième devise comme « devise report supplémentaire », [!INCLUDE[prod_short](includes/prod_short.md)] enregistre automatiquement les montants d’état en DS et dans cette devise report supplémentaire pour chaque écriture comptable, ainsi que pour d’autres écritures, telles que les écritures TVA. Pour plus d’informations, voir [Configurer une devise report supplémentaire](finance-how-setup-additional-currencies.md). La devise report supplémentaire est le plus souvent utilisée pour faciliter les états financiers pour les propriétaires qui résident dans des pays/régions utilisant des devises différentes de la devise société (DS).  

> [!IMPORTANT]
> Si vous souhaitez utiliser une devise de reporting supplémentaire pour le reporting financier, assurez-vous de bien comprendre les limites. Pour plus d’informations, voir [Configurer une devise report supplémentaire](finance-how-setup-additional-currencies.md).

## <a name="currencies"></a>Devises

> [!NOTE]  
> Dans [!INCLUDE[prod_short](includes/prod_short.md)], si vous recherchez des informations en temps réel sur les taux de devise étrangère (FX) ou les taux historiques, vous les trouverez sous la désignation de devise. En plus de cet article, consultez aussi [Configurer une devise report supplémentaire](finance-how-setup-additional-currencies.md).

Vous spécifiez les codes devise dans **Devises**, y compris les informations supplémentaires et les paramètres nécessaires pour chaque code devise.

> [!TIP]
> Créez les devises avec le code ISO international pour simplifier l’utilisation de la devise à l’avenir.

|Champ|Description|  
|---------------------------------|---------------------------------------|  
|**Code**|Identifiant de la devise.|
|**Description**|Description libre de la devise.|
|**Code ISO**|Code international à trois lettres pour la devise défini dans la norme ISO 4217.|
|**Code numérique ISO**|Référence numérique internationale pour la devise définie dans la norme ISO 4217.|
|**Date du taux de change**|La dernière date de taux de change effectif.|
|**Devise U.M.E.**|Indique si la devise est une devise de l’U.M.E. (Union économique et monétaire), telle que EUR.|
|**Cpte gains constatés report**|Compte sur lequel le gain réel sera enregistré lorsque vous recevrez des paiements pour des créances ou enregistrerez le taux de change réel sur les paiements de dépenses. Pour consulter un exemple de transaction en devise comptable, voir l’exemple sous ce tableau. |
|**Cpte pertes constatées report**|Compte sur lequel la perte réelle sera enregistrée lorsque vous recevrez des paiements pour des créances ou enregistrerez le taux de change réel sur les paiements de dépenses. Pour consulter un exemple de transaction en devise comptable, voir l’exemple sous ce tableau. |
|**Cpte gains prévus**|Compte sur lequel le gain théorique sera comptabilisé lorsque vous effectuerez un ajustement de devise.|
|**Cpte pertes prévues**|Compte sur lequel la perte théorique sera comptabilisée lorsque vous effectuerez un ajustement de devise.|
|**Précision arrondi montant**|Certaines devises ont d’autres formats pour les montants facture que ceux définis dans la page **Paramètres comptabilité**. Si vous modifiez la précision arrondi montant pour une devise, tous les montants facture dans cette devise seront arrondis avec la précision mise à jour.|
|**Nombre décimales montant**|Certaines devises ont d’autres formats pour les montants facture que ceux définis dans la page **Paramètres comptabilité**. Si vous modifiez le nombre décimales montant pour une devise, tous les montants facture dans la devise seront arrondis avec les décimales mises à jour.|
|**Type arrondi facture**|Spécifie la méthode à utiliser si les montants doivent être arrondis. Les options sont **Au plus près**, **Vers le haut** et **Vers le bas**.|
|**Précision arrondi montant unité**|Certaines devises ont d’autres formats pour les montants unitaires que ceux définis dans la page **Paramètres comptabilité**. Si vous modifiez la précision arrondi montant unité pour une devise, tous les montants unitaires dans la devise seront arrondis avec la précision mise à jour.|
|**Nombre décimales montant unitaire**|Certaines devises ont d’autres formats pour les montants unitaires que ceux définis dans la page **Paramètres comptabilité**. Si vous modifiez le nombre décimales montant unitaire pour une devise, tous les montants unitaires dans la devise seront arrondis avec les décimales mises à jour.|
|**Précision arrondi lettrage**|Spécifie la taille de l’intervalle autorisé pour les différences d’arrondi lorsque vous lettrez différentes devises entre elles.|
|**Arrondi DS conversion. Compte débit**|Spécifie les informations de conversion qui doivent également contenir un compte débit si vous souhaitez insérer des lignes correction pour les différences d’arrondi dans les feuilles comptabilité en utilisant l’action **Insérer lignes arr. conv. DS**.|
|**Arrondi DS conversion. Compte crédit**|Spécifie les informations de conversion qui doivent également contenir un compte crédit si vous souhaitez insérer des lignes correction pour les différences d’arrondi dans les feuilles comptabilité en utilisant l’action **Insérer lignes arr. conv. DS**.|
|**Date dern. ajust. automatique**|Date du dernier ajustement de devise.|
|**Date dern. modification**|Date de la modifiction dans le paramétrage de la devise.|
|**% écart de règlement**|% d’écart de règlement maximum défini pour cette devise. Pour plus d’informations, consultez [Écart de règlement et écart d’escompte](finance-payment-tolerance-and-payment-discount-tolerance.md). |
|**Montant écart règlement max.**|Montant d’écart de règlement maximum défini pour cette devise. Pour plus d’informations, consultez [Écart de règlement et écart d’escompte](finance-payment-tolerance-and-payment-discount-tolerance.md). |
|**Facteur devise**|Indique la relation entre la devise et la devise société (DS) à l’aide du taux de change réel.|
|**Cpte gains constatés report**|Indique le compte général utilisé pour valider les gains de change sur ajustements de devise entre la devise société (DS) et la devise report supplémentaire. Les gains de change sont calculés lorsque le traitement par lots Ajuster taux de change est exécuté pour ajuster les comptes généraux. Par défaut, ce champ peut ne pas être visible. Il peut être récupéré en personnalisant la page.|
|**Cpte pertes constatées report**|Indique le compte général utilisé pour valider les pertes de change sur ajustements de devise entre la devise société (DS) et la devise report supplémentaire. Les gains de change sont calculés lorsque le traitement par lots Ajuster taux de change est exécuté pour ajuster les comptes généraux. Par défaut, ce champ peut ne pas être visible. Il peut être récupéré en personnalisant la page.|
|**Compte gains résiduels DR**|Indique le compte général utilisé pour valider les montants des gains résiduels (différences d’arrondi) lorsqu’une devise report supplémentaire est utilisée dans le module de comptabilité. Par défaut, ce champ peut ne pas être visible. Il peut être récupéré en personnalisant la page.|
|**Compte pertes résiduelles DR**|Indique le compte général utilisé pour valider les montants des pertes résiduelles (différences d’arrondi) lorsqu’une devise report supplémentaire est utilisée dans le module de comptabilité. Par défaut, ce champ peut ne pas être visible. Il peut être récupéré en personnalisant la page.|
|**Différence TVA max. autorisée**|Montant maximum autorisé pour les différences de TVA dans cette devise. Pour plus d’informations, consutez [Correction manuelle des montants de TVA dans des documents achat et vente](finance-work-with-vat.md#correcting-vat-amounts-manually-in-sales-and-purchase-documents). Par défaut, ce champ peut ne pas être visible. Il peut être récupéré en personnalisant la page.|
|**Type arrondi TVA**|Indique la méthode d’arrondi pour corriger manuellement les montants TVA dans les documents vente et achat. Par défaut, ce champ peut ne pas être visible. Il peut être récupéré en personnalisant la page.|

### <a name="example-of-a-receivable-currency-transaction"></a>Exemple de transaction en devise comptabilité

Lorsque vous recevez une facture d’une entreprise dans une devise étrangère, il est assez facile de calculer la valeur en devise locale (DS) de la facture en fonction du taux de change du jour. Cependant, la facture est souvent accompagnée de conditions de paiement afin que vous puissiez reporter le paiement à une date ultérieure, ce qui implique un taux de change potentiellement différent. Ce problème, combiné au fait que les taux de change bancaires diffèrent toujours des taux de change officiels, rend impossible l’anticipation du montant exact en devise locale (DS) requis pour couvrir la facture. Si la date d’échéance de la facture s’étend au mois suivant, vous devrez peut-être également réévaluer le montant en devise locale (DS) à la fin du mois. L’ajustement de la devise est nécessaire, car la nouvelle valeur DS requise pour couvrir le montant de la facture peut être différente et la dette de l’entreprise envers le fournisseur a potentiellement changé. Le nouveau montant DS peut être supérieur ou inférieur au montant précédent et représentera donc un gain ou une perte. Cependant, comme la facture n’a pas encore été payée, le gain ou la perte est considéré comme *non réalisé*. Ultérieurement, la facture est réglée et la banque est revenue au taux de change réel pour le paiement. Ce n’est que maintenant que le gain ou la perte *réalisé(e)* est calculé(e). Ce gain ou cette perte non réalisé(e) est ensuite contrepassé(e) et le gain ou la perte réalisé(e) est comptabilisé(e) à sa place.

Dans l’exemple suivant, une facture est reçue le 1er janvier avec le montant en devise 1 000. À ce moment là, le taux de change est 1,123.

|Date|Action|Montant devise|Taux document|Montant DS sur le document|Taux ajustement|Montant gains prévu|Taux règlement|Montant pertes constatées report|  
|-----|----------|------------|-----------|---------|-----------|-------------|---------|---------|
|1/1|**Facture**|1000|1,123|1123|||||
|1/31|**Ajustement**|1000||1125|1,125|2|||
|2/15|**Ajustement Contrepassation sur paiement**|1000||||-2|||
|2/15|**Paiement**|1000||1120|||1,120|-3|

À la fin du mois, un ajustement de devise est effectué lorsque le taux de change d’ajustement a été fixé à 1,125, ce qui déclenche un gain prévu de 2.

Au moment du paiement, le taux de change réel enregistré sur la transaction bancaire indique un taux de change de 1,120.

Ici, il y a une transaction prévu. Elle sera donc contrepassée avec le paiement.

Enfin, le paiement est enregistré et la perte réelle est validée sur le compte des pertes constatées.

## <a name="available-currency-functions"></a>Fonctions de devise disponibles

Le tableau suivant décrit les actions clés sur la page **Devises**. Certaines des actions sont expliquées dans les sections suivantes.  

|Menu|Action|Description|
|-------------|--------------|------------------------------|
|**Traitement**|**Proposer des comptes**|Utilisez des comptes des autres devises. Les comptes les plus fréquemment utilisés seront insérés.|
||Modifier l’écart de règlement|Modifiez l’écart de règlement maximum, le pourcentage d’écart de règlement ou les deux, et filtrez par devise. Pour plus d’informations, consultez [Écart de règlement et écart d’escompte](finance-payment-tolerance-and-payment-discount-tolerance.md).|
||**Taux change**|Affichez les taux de change mis à jour pour les devises que vous utilisez.|
||**Ajuster taux de change**|Ajuster les écritures comptables, client, fournisseur et compte bancaire pour obtenir un solde mis à jour si le taux de change a évolué depuis la validation des écritures.|
||**Historique des transactions d’ajust. taux de change**|Affichez les résultats de l’exécution du traitement par lots **Ajuster taux de change**. Une ligne est créée pour chaque devise et pour chaque combinaison de devise et de groupe comptabilisation comprise dans l’ajustement.|
|**Service de taux de change**|**Services de taux de change**|Affichez ou modifiez la configuration des services qui sont paramétrés pour extraire les taux de change de devise mis à jour lorsque vous sélectionnez l’action **Mettre à jour les taux de change**.|
||**Mettre à jour les taux de change**|Obtenez les récents taux de change des devises auprès d’un fournisseur de services.|
|**États**|**Solde devise étrangère**|Affichez les soldes de tous les clients et fournisseurs en devise étrangère et en devise société (DS). L’état affiche deux soldes en devise société. L’un correspond au solde en devise étrangère converti en devise société en utilisant le taux de change en vigueur au moment de la transaction. L’autre correspond au solde en devise converti en devise société en utilisant le taux de change à la date de travail.|

## <a name="exchange-rates"></a>Taux de change

Les taux de change permettent de calculer la valeur en devise société (DS) de chaque transaction en devise. La page **Taux d’échange** comprend les champs suivants :

|Champ|Description|  
|---------------------------------|---------------------------------------|  
|**Date début**|Date à laquelle le taux de change a été effectué|  
|**Code devise**|Code devise lié à ce taux de change|  
|**Code devise liée**|Si cette devise fait partie d’un calcul de devise triangulaire, le code devise associé peut être configuré ici|  
|**Montant taux de change**|Le montant du taux de change est le taux à utiliser pour le code devise sélectionné sur la ligne. Il s’agit normalement de 1 ou 100|  
|**Montant taux de change lié**|Le montant du taux de change lié concerne le taux à utiliser pour le code devise liée.|  
|**Montant taux de change ajust.**|Le montant du taux de change d’ajustement est le taux à utiliser pour le code devise sélectionné sur la ligne à utiliser pour le traitement par lots **Ajuster taux de change**.|  
|**Montant taux change lié ajust.**|Le montant du taux de change d’ajustement lié est le taux à utiliser pour le code devise sélectionné sur la ligne à utiliser pour le traitement par lots **Ajuster taux de change**.|  
|**Fixer montant taux de change**|Spécifie si le taux de change de la devise peut être modifié sur les factures et les lignes feuille.|  

En général, les valeurs des champs **Montant taux de change** et **Montant taux de change lié** sont utilisées comme taux de change par défaut sur tous les nouveaux documents client et fournisseur créés à l’avenir. Le taux de change est affecté au document en fonction de la date de travail actuelle.  

> [!Note]
> Le taux de change réel sera calculé à l’aide de cette formule :
>
> `Currency Amount = Amount / Exchange Rate Amount * Relational Exch. Rate Amount`

Le montant du taux de change d’ajustement ou le montant du taux de change d’ajustement lié sera utilisé pour mettre à jour toutes les transactions banque, client ou fournisseur.  

> [!Note]
> Le taux de change réel sera calculé à l’aide de cette formule :
>
> `Currency Amount = Amount / Adjustment Exch. Rate Amount * Relational Adjmt Exch. Rate Amt`

## <a name="adjusting-exchange-rates"></a>Ajustement des taux de change

Comme les taux de change ne cessent de fluctuer, il convient d’ajuster périodiquement les équivalents devise supplémentaires de votre système. À défaut d’effectuer ces ajustements, les montants convertis à partir de devises étrangères (ou supplémentaires) et publiés dans la comptabilité en DS risquent d’être erronés. En outre, les écritures quotidiennes validées avant la saisie d’un taux de change quotidien dans l’application doivent être mises à jour après la saisie des informations de taux de change quotidienne.

Le traitement par lots **Ajuster taux de change** permet d’ajuster manuellement les taux de change d’écritures client, fournisseur et compte bancaire validées. Il peut également mettre à jour d’autres montants en devise report dans des écritures comptables.  

> [!TIP]
> Vous pouvez utiliser un service pour mettre à jour automatiquement les taux de change dans le système. Pour plus d’informations, reportez vous à [Configurer un service de taux de change des devises](finance-how-update-currencies.md#to-set-up-a-currency-exchange-rate-service). Cependant, cela n’ajuste pas les taux de change sur les transactions déjà enregistrées. Pour mettre à jour les taux de change sur les écritures validées, utilisez la tâche de traitement par lots **Ajuster les taux de change**.

### <a name="effect-on-customers-and-vendors"></a>Effet sur les clients et fournisseurs

Pour les comptes client et fournisseur, le traitement par lots ajuste la devise en utilisant le taux de change valide à la date de comptabilisation spécifiée dans le traitement par lots. Le traitement par lots calcule les différences pour chaque solde en devise et valide les montants dans le compte général spécifié dans le champ **Compte gains prévus** ou **Compte pertes prévues** de la page **Devises**. Les écritures de contrepartie sont automatiquement validées sur le compte client/fournisseur en comptabilité.

Ce traitement par lots traite toutes les écritures comptables client et toutes les écritures comptables fournisseur ouvertes. En cas de différence du taux de change d’une écriture, le traitement par lots crée une écriture comptable détaillée client ou fournisseur reflétant le montant ajusté dans l’écriture comptable client ou fournisseur.

#### <a name="dimensions-on-customer-and-vendor-ledger-entries"></a>Axes analytiques sur des écritures comptables client et fournisseur

Les axes analytiques des écritures comptables client/fournisseur sont affectés aux écritures ajustement et les ajustements sont validés par combinaison de sections analytiques.

### <a name="effect-on-bank-accounts"></a>Effet sur les comptes bancaires

Pour les comptes bancaires, le traitement par lots ajuste la devise en utilisant le taux de change valide à la date de comptabilisation spécifiée dans le traitement par lots. Le traitement par lots calcule les différences pour chaque compte bancaire possédant un code devise et valide les montants dans le compte général spécifié dans le champ **Compte gains constatés** ou **Compte pertes constatées** de la page **Devises**. Les écritures de contrepartie sont automatiquement validées sur les comptes bancaires spécifiés dans les groupes comptabilisation banque. Le traitement par lots calcule une écriture par devise et par groupe comptabilisation.

#### <a name="dimensions-on-bank-account-entries"></a>Axes analytiques sur des écritures compte bancaire

Les axes analytiques par défaut du compte bancaire sont affectés aux écritures ajustement pour le compte général du compte bancaire et pour le compte gain/perte.

### <a name="effect-on-gl-accounts"></a>Effet sur les comptes généraux
Si vous validez en devise report, vous pouvez demander au traitement par lots de créer de nouvelles écritures comptables pour les ajustements de devise entre devise société et devise report. Le traitement par lots calcule les différences pour chaque écriture comptable et ajuste l’écriture comptable en fonction de la valeur du champ **Ajustement taux de change** de chaque compte général.

##### <a name="dimensions-on-gl-account-entries"></a>Axes analytiques sur des écritures compte général
Les axes analytiques par défaut des comptes dans lesquels ils sont validés sont affectés aux écritures ajustement.

> [!Important]
> Avant de pouvoir utiliser le traitement par lots, vous devez entrer le taux de change ajustement qui est utilisé pour ajuster les soldes en devises. Pour ce faire sur la page **Taux de change devise**.<br><br>  

> [!Video https://www.microsoft.com/videoplayer/embed/RE3Q24s?rel=0]

## <a name="to-set-up-a-currency-exchange-rate-service"></a>Configurer un service de taux de change des devises
Vous pouvez utiliser un service externe pour tenir vos taux de change des devises à jour, par exemple FloatRates. 

> [!NOTE]
> La plupart des services de taux de change fournissent des données compatibles avec le processus d’importation dans [!INCLUDE[prod_short](includes/prod_short.md)]. Cependant, les données sont parfois formatées différemment et vous devrez personnaliser votre processus d’importation. Pour cela, vous pouvez utiliser l’infrastructure d’échange de données en ajoutant votre propre codeunit. Vous aurez probablement besoin de l’aide d’un développeur. Pour plus d’informations, voir [Configurer les définitions d’échange de données](across-how-to-set-up-data-exchange-definitions.md).

1. Sélectionnez ![l’icône en forme d’ampoule qui ouvre la fonction Tell Me.](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire") entrez **Services de taux de change des devises**, puis choisissez le lien associé.
2. Sélectionnez l’action **Nouveau**.
3. Sur la page **Service de taux de change devise**, renseignez les champs selon vos besoins. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
4. Activez le bouton bascule **Activé** pour activer le service.

> [!NOTE]
> La vidéo suivante montre un exemple de connexion à un service de taux de change des devises, en prenant l’exemple de la Banque Centrale Européenne. Dans le segment qui décrit comment configurer les mappages de champs, le paramètre de la colonne **Source** pour **Nœud parent pour code devise** ne renverra que la première devise trouvée. Le paramètre doit être `/gesmes:Envelope/Code/Code/Code`.

<br><br>  
  
> [!Video https://www.microsoft.com/en-us/videoplayer/embed/RE4A1jy?rel=0]

## <a name="to-update-currency-exchange-rates-through-a-service"></a>Pour mettre à jour les taux de change des devises à partir d’un service
1. Sélectionnez l’icône ![Ampoule qui ouvre la fonction Tell Me.](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire") entrez **Devises**, puis choisissez le lien associé.
2. Choisissez l’option **Mettre à jour les taux de change**.

La valeur dans le champ **Taux de change** de la page **Devises** est mise à jour avec le dernier taux de change des devises.

## <a name="see-related-training-at-microsoft-learn"></a>Voir la formation associée sur [Microsoft Learn](/learn/paths/use-multiple-currencies-dynamics-365-business-central/)

## <a name="see-also"></a>Voir aussi
[Configurer une devise report supplémentaire](finance-how-setup-additional-currencies.md)  
[Clôture des exercices et des périodes](year-close-years-periods.md)  
[Utilisation de [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]
