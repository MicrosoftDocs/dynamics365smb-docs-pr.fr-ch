---
title: Configurer des devises
description: Vous devez configurer chaque devise si vous achetez ou vendez avec des devises autres que votre devise société (DS) ou si vous enregistrez des transactions comptables dans différentes devises.
author: brentholtorf
ms.topic: conceptual
ms.search.keywords: multiple currencies
ms.search.form: '5, 118'
ms.date: 03/15/2022
ms.author: bholtorf
ms.service: dynamics-365-business-central
---
# <a name="set-up-currencies"></a>Configurer des devises

[!INCLUDE [finance-currencies-def](includes/finance-currencies-def.md)]

Utilisez un service externe pour obtenir les derniers taux de change des devises dans la liste **Devises**. Pour plus d’informations, reportez vous à [Configurer un service de taux de change des devises](finance-how-update-currencies.md#set-up-a-currency-exchange-rate-service).  

[!INCLUDE [finance-currencies-lcy](includes/finance-currencies-lcy-note.md)]

## <a name="currencies"></a><a name="curr"></a>Devises

Le tableau suivant décrit les champs de la liste **Devises**.

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
|**Différence TVA max. autorisée**|Montant maximum autorisé pour les différences de TVA dans cette devise. Pour plus d’informations, consultez [Correction manuelle des montants de TVA dans des documents achat et vente](finance-work-with-vat.md#correcting-vat-amounts-manually-on-sales-and-purchase-documents). Par défaut, ce champ peut ne pas être visible. Il peut être récupéré en personnalisant la page.|
|**Type arrondi TVA**|Indique la méthode d’arrondi pour corriger manuellement les montants TVA dans les documents vente et achat. Par défaut, ce champ peut ne pas être visible. Il peut être récupéré en personnalisant la page.|

### <a name="available-currency-functions"></a>Fonctions de devise disponibles

Le tableau suivant décrit les actions clés sur la page **Devises**.  

|Menu|Action|Description|
|-------------|--------------|------------------------------|
|**Traitement**|**Proposer des comptes**|Utilisez des comptes des autres devises. Les comptes les plus fréquemment utilisés seront insérés.|
||**Modifier l’écart de règlement**|Modifiez l’écart de règlement maximum, le pourcentage d’écart de règlement ou les deux, et filtrez par devise. Pour plus d’informations, consultez [Écart de règlement et écart d’escompte](finance-payment-tolerance-and-payment-discount-tolerance.md).|
||**Taux de change**|Affichez les taux de change mis à jour pour les devises que vous utilisez.|
||**Ajuster taux de change**|Ajuster les écritures comptables, client, fournisseur et compte bancaire pour obtenir un solde mis à jour si le taux de change a évolué depuis la validation des écritures.|
||**Historique des transactions d’ajustement du taux de change**|Affichez les résultats de l’exécution du traitement par lots **Ajuster taux de change**. Une ligne est créée pour chaque devise et pour chaque combinaison de devise et de groupe comptabilisation comprise dans l’ajustement.|
|**Service de taux de change**|**Services de taux de change**|Affichez ou modifiez la configuration des services qui sont paramétrés pour extraire les taux de change de devise mis à jour lorsque vous sélectionnez l’action **Mettre à jour les taux de change**.|
||**Mettre à jour les taux de change**|Obtenez les récents taux de change des devises auprès d’un fournisseur de services.|
|**États**|**Solde devise étrangère**|Affichez les soldes de tous les clients et fournisseurs en devise étrangère et en devise société (DS). L’état affiche deux soldes en devise société. L’un correspond au solde en devise étrangère converti en devise société en utilisant le taux de change en vigueur au moment de la transaction. L’autre correspond au solde en devise converti en devise société en utilisant le taux de change à la date de travail.|

## <a name="lcy-and-other-currencies"></a>DS et autres devises

[!INCLUDE [finance-currencies-lcy-def](includes/finance-currencies-lcy-def.md)]

## <a name="rounding-currencies"></a>Arrondi des devises

Pour gérer les devises qui n’utilisent pas de décimales et pour éviter l’emploi de décimales inutiles dans les devises étrangères, vous pouvez utiliser deux fonctions d’arrondi différentes :

- arrondi montant unité ;  

- arrondi montant.  

Ces fonctions peuvent fonctionner indépendamment ou conjointement. En outre, les fonctions peuvent fonctionner avec l’arrondi facture.

Contrairement aux fonctions arrondi facture, les fonctions arrondi montant et arrondi montant unité affectent uniquement les comptes en devise étrangère et non les montants correspondants en devise locale. Elles n’entraînent pas de validation dans les comptes généraux. C’est pourquoi aucun compte général ne doit être spécifié dans les groupes comptabilisation ou dans d’autres emplacements.

### <a name="unit-amount-rounding"></a>Arrondi montant unité

La fonction arrondi montant unité contrôle la manière dont les prix de vente des articles et ressources en devises étrangères sont arrondis sur les lignes vente et achat. Vous devez spécifier les règles de chaque devise séparément dans le champ **Précis. arrondi montant unité** de la liste **Devises**.

La fonction arrondi montant unité est utilisée automatiquement à chaque fois que vous saisissez un article ou un numéro de ressource sur une ligne vente. Si la facture est pour un client avec un code devise, le prix des articles et des ressources est converti dans la devise du client. Le prix est arrondi en fonction de la précision d’arrondi montant unité de la devise.

### <a name="amount-rounding"></a>Arrondi montant

La fonction arrondi montant contrôle la manière dont les montants en devises étrangères sont arrondis sur les lignes feuille comptabilité, vente et achat. Vous devez spécifier les règles de chaque devise séparément dans le champ **Précis. arrondi montant** de la liste **Devises**.

Les montants en devises étrangères sont arrondis lorsque vous renseignez et validez les lignes feuille comptabilité, vente et achat.

## <a name="exchange-rates"></a>Taux de change

Vous pouvez enregistrer les taux de change de chaque devise étrangère et spécifier les dates à partir desquelles ces taux sont valables. Par exemple, vous pouvez saisir le taux de change pour chaque devise tous les jours, tous les mois ou tous les trimestres.

Vous pouvez conserver les taux de change historiques sur la page **Taux de change devise** à titre de référence. Lorsque vous avez besoin de mettre à jour les taux de change, vous pouvez utiliser le bouton **Mettre à jour les taux de change** pour obtenir les derniers taux de change de la part d’un fournisseur de service externe.

## <a name="general-ledger-accounts"></a>Comptes généraux

Vous ne pouvez pas associer de codes devise aux comptes généraux car les montants de ces derniers sont en devise locale. Si vous disposez d’un prêt bancaire en USD et placez des acomptes dans un compte bancaire en SEK, vous pouvez suivre ces comptes en configurant les comptes bancaires en USD et SEK. Avec les groupes comptabilisation, vous pouvez associer les comptes aux comptes généraux appropriés. Dans la comptabilité, la valeur des montants est indiquée en devise locale (DS).

Vous pouvez entrer un code devise sur une ligne feuille comptabilité et valider celle-ci dans un compte général. Le taux de change adéquat permet de convertir le montant en devise société (DS) avant sa validation dans le compte général.  

## <a name="example-of-a-receivable-currency-transaction"></a>Exemple de transaction en devise comptabilité

[!INCLUDE [finance-currencies-example](includes/finance-currencies-example.md)]

## <a name="see-also"></a>Voir aussi

[Mettre à jour des taux de change devise](finance-how-update-currencies.md)  
[Configurer une devise report supplémentaire](finance-how-setup-additional-currencies.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
