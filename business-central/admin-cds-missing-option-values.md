---
title: Gestion des valeurs option manquantes
description: Découvrez comment empêcher l’échec de la synchronisation complète en raison d’options différentes dans les champs mappés. Ce processus nécessite l’aide d’un développeur.
author: brentholtorf
ms.author: bholtorf
ms.custom: na
ms.reviewer: na
ms.topic: conceptual
ms.date: 03/23/2022
---

# Gestion des valeurs option manquantes
> [!NOTE]
> Dans la 1re vague de lancement 2022, vous pouvez créer vos propres mappages d’options. Pour plus d’informations, voir [Personnalisation des mappages d’options avec Microsoft Dataverse](/dynamics365/business-central/dev-itpro/administration/administration-custom-option-mapping). Les nouvelles fonctionnalités nécessitent que votre administrateur active la fonctionnalité **Mise à jour la fonctionnalité : Mapper aux jeux d’options dans Dataverse sans code** sur la page **Gestion des fonctionnalités**. Pour plus d’informations, voir [Activer les fonctionnalités à venir à l’avance](/dynamics365/business-central/dev-itpro/administration/feature-management).

Cette rubrique est destinée à un public technique. Les processus qu’elle décrit nécessitent l’aide d’un développeur.

[!INCLUDE[prod_short](includes/cds_long_md.md)] contient trois champs d’ensembles d’options qui contiennent des valeurs que vous pouvez mapper à des champs [!INCLUDE[prod_short](includes/prod_short.md)] de type Option pour la synchronisation automatique. Lors de la synchronisation, les options non mappées sont ignorées et les options manquantes sont ajoutées à la table [!INCLUDE[prod_short](includes/prod_short.md)] associée et à la table système **Mappage option Dataverse** pour une gestion manuelle ultérieure. Par exemple, en ajoutant les options manquantes dans l’un ou l’autre des produits, puis en mettant à jour le mappage.

La page **Mappage de table d’intégration** contient trois champs contenant une ou plusieurs valeurs option mappées. Après une synchronisation complète, la page **Mappage option Dataverse** contient les options non mappées dans les trois champs.

|         Enregistrement             | Valeur option | Légende valeur option |
|----------------------------|--------------|----------------------|
| Conditions de paiement : NET30       | 1            | 30 jours nets               |
| Conditions de paiement : 2%10NET30   | 2            | 2 % d’escompte sous 10 jours ; 30 jours nets        |
| Conditions de paiement : NET45       | 3            | 45 jours nets               |
| Conditions de paiement : NET60       | 4            | 60 jours nets               |
| Conditions de livraison : FOB       | 1            | FOB                  |
| Conditions de livraison : SANSFRAIS  | 2            | Sans frais            |
| Transporteur : TRANAÉRIEN   | 1            | Transport aérien             |
| Transporteur : DHL        | 2            | DHL                  |
| Transporteur : FEDEX      | 3            | FedEx                |
| Transporteur : UPS        | 4            | UPS                  |
| Transporteur : COURPOSTAL | 5            | Courrier postal          |
| Transporteur : PLEICHARGE   | 6            | Pleine charge            |
| Transporteur : APPELLERA   | 7            | Appellera            |

Le contenu de la page **Mappage option Dataverse** est basé sur des valeurs d’énumération dans la table **Compte CRM**. Dans [!INCLUDE[prod_short](includes/cds_long_md.md)], les champs suivants de la table Compte sont mappés aux champs des enregistrements client et fournisseur :

- **Adresse 1 : conditions de transport** du type de données Énumération, où les valeurs sont définies comme suit :

```
enum 5335 "CDS Shipment Method Code"
{
    Extensible = true;
    value(0; " ") { Caption = ' '; }
    value(1; "FOB") { Caption = 'FOB'; }
    value(2; "NoCharge") { Caption = 'No Charge'; }
}
```

- **Adresse 1 : conditions de livraison** du type de données Énumération, où les valeurs sont définies comme suit :

```
enum 5336 "CDS Shipping Agent Code"
{
    Extensible = true;
    value(0; " ") { Caption = ' '; }
    value(1; "Airborne") { Caption = 'Airborne'; }
    value(2; "DHL") { Caption = 'DHL'; }
    value(3; "FedEx") { Caption = 'FedEx'; }
    value(4; "UPS") { Caption = 'UPS'; }
    value(5; "PostalMail") { Caption = 'Postal Mail'; }
    value(6; "FullLoad") { Caption = 'Full Load'; }
    value(7; "WillCall") { Caption = 'Will Call'; }
}
```

- **Conditions de paiement** du type de données Énumération, où les valeurs sont définies comme suit :

```
enum 5334 "CDS Payment Terms Code"
{
    Extensible = true;
    value(0; " ") { Caption = ' '; }
    value(1; "Net30") { Caption = 'Net 30'; }
    value(2; "2%10Net30") { Caption = '2% 10; Net 30'; }
    value(3; "Net45") { Caption = 'Net 45'; }
    value(4; "Net60") { Caption = 'Net 60'; }
}
```

Toutes les énumérations [!INCLUDE[prod_short](includes/prod_short.md)] ci-dessus sont mappées à des ensembles d’options dans [!INCLUDE[prod_short](includes/cds_long_md.md)].

### Extension des ensembles d’options dans [!INCLUDE[prod_short](includes/prod_short.md)]
1. Créez une extension AL.

2. Ajoutez une extension Énumération pour les options que vous souhaitez étendre. Veillez à utiliser la même valeur. 

```
enumextension 50100 "CDS Payment Terms Code Extension" extends "CDS Payment Terms Code"
{
    value(779800001; "Cash Payment") { Caption = 'Cash Payment'; }
    value(779800002; "Transfer") { Caption = 'Transfer'; }
}
```

> [!IMPORTANT]  
> Vous devez utiliser les mêmes valeurs ID option de [!INCLUDE[prod_short](includes/cds_long_md.md)] lorsque vous étendez l’énumération [!INCLUDE[prod_short](includes/prod_short.md)]. Sinon, la synchronisation échoue.

> [!IMPORTANT]  
> N’utilisez pas le caractère « , » dans les valeurs et les légendes enum. Ceci n’est actuellement pas pris en charge par l’exécution [!INCLUDE[prod_short](includes/prod_short.md)].

> [!NOTE]
> Les dix premiers caractères des nouveaux noms et légendes de valeur option doivent être uniques. Par exemple, deux options nommées « Transférer 20 jours ouvrables » et « Transférer 20 jours calendaires » provoquent une erreur, car leurs 10 premiers caractères (« Transférer ») sont identiques. Nommez-les, par exemple, « TRF20 JO » et « TRF20 JC ».

### Mettre à jour le mappage option [!INCLUDE[prod_short](includes/cds_long_md.md)]
Vous pouvez maintenant recréer le mappage entre les options [!INCLUDE[prod_short](includes/cds_long_md.md)] et les enregistrements [!INCLUDE[prod_short](includes/prod_short.md)].

Sur la page **Mappage de table d’intégration**, choisissez la ligne pour le mappage **Conditions de paiement**, puis l’action **Synchroniser les enregistrements modifiés**. La page **Mappage option Dataverse** est mise à jour avec les enregistrements supplémentaires ci-dessous.

|         Enregistrement                 | Valeur option   | Légende valeur option |
|--------------------------------|----------------|----------------------|
| Conditions de paiement : NET30           | 1              | 30 jours nets               |
| Conditions de paiement : 2%10NET30       | 2              | 2 % d’escompte sous 10 jours ; 30 jours nets        |
| Conditions de paiement : NET45           | 3              | 45 jours nets               |
| Conditions de paiement : NET60           | 4              | 60 jours nets               | 
| **Conditions de paiement : PMT EN ESP**  | **779800001**  | **Paiement en espèces**     |
| **Conditions de paiement : TRANSFERT**    | **779800002**  | **Transfert**         |

La table **Conditions de paiement** dans [!INCLUDE[prod_short](includes/prod_short.md)] aura alors de nouveaux enregistrements pour les options [!INCLUDE[prod_short](includes/cds_long_md.md)]. Dans la table suivante, les nouvelles options sont en gras. Les lignes en italique représentent toutes les options qui peuvent maintenant être synchronisées. Les lignes restantes représentent les options non utilisées et seront ignorées lors de la synchronisation. (Vous pouvez les supprimer ou étendre les options Dataverse avec les mêmes noms.)

| Code       | Calcul date échéance | Calcul date d’escompte | % remise | Calculer escompte sur avoirs | Description       |
|------------|----------------------|---------------------------|------------|-------------------------------|-------------------|
| 10 JOURS    | 10J                  |                           | 0.         | FAUX                         | 10 jours nets       |
| 14 JOURS    | 14D                  |                           | 0.         | FAUX                         | 14 jours nets       |
| 15 JOURS    | 15D                  |                           | 0.         | FAUX                         | 15 jours nets       |
| 1M(8J)     | 1M                   | 8J                        | 2.         | FAUX                         | 1 mois/2 % d’escompte sous 8 jours |
| 2 JOURS     | 2J                   |                           | 0.         | FAUX                         | 2 jours nets        |
| *2%10NET30* |                      |                           | 0.         | FAUX                         |                   |
| 21 JOURS    | 21J                  |                           | 0.         | FAUX                         | 21 jours nets       |
| 30 JOURS    | 30J                  |                           | 0.         | FAUX                         | 30 jours nets       |
| 60 JOURS    | 60J                  |                           | 0.         | FAUX                         | 60 jours nets       |
| 7 JOURS     | 7J                   |                           | 0.         | FAUX                         | 7 jours nets        |
| ***PMT EN ESP*** |                      |                           | 0.         | FAUX                         |                   |
| MC         | MC                   |                           | 0.         | FAUX                         | Mois en cours     |
| PR        | 0J                   |                           | 0.         | FAUX                         | Payable à réception  |
| *NET30*      |                      |                           | 0.         | FAUX                         |                   |
| *NET45*      |                      |                           | 0.         | FAUX                         |                   |
| *NET60*      |                      |                           | 0.         | FAUX                         |                   |
| ***TRANSFERT*** |                      |                           | 0.         | FAUX                         |                   |

## Voir aussi
[Mappage des tables et des champs à synchroniser](admin-how-to-modify-table-mappings-for-synchronization.md)

[!INCLUDE[footer-include](includes/footer-banner.md)]