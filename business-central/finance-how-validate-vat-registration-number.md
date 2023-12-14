---
title: Valider des numéros d’identification intracommunautaire
description: "Laissez Business\_Central valider les numéros d’identification intra-communautaire et d’autres informations sur la société pour vos contacts, clients et fournisseurs, sur la base du service de validation du numéro d’identification intra-communautaire de l’Union européenne."
author: andregu
ms.topic: conceptual
ms.reviewer: bholtorf
ms.search.keywords: 'VAT, posting, tax, value-added tax'
ms.search.form: '249, 575, 1279'
ms.date: 06/16/2021
ms.author: andregu
---

# Valider des numéros d’identification intracommunautaire

Il est important que les numéros d’identification intra-communautaire des clients, fournisseurs et contacts soient valides, si vous utilisez [!INCLUDE [prod_short](includes/prod_short.md)] dans un pays/une région où la TVA est utilisée. Par exemple, les sociétés modifient parfois leur statut d’assujettissement à la TVA, et dans certains pays/régions, les autorités fiscales peuvent vous demander de fournir des états, tels que l’état **Liste des ventes UE**, qui répertorient les numéros d’identification intra-communautaire à utiliser lorsque vous faites des affaires.

La Commission européenne fournit le service VIES de validation des numéros TVA sur son site Web, qui est public et gratuit. [!INCLUDE [prod_short](includes/prod_short.md)] vous permet de supprimer cette étape et d’utiliser le service VIES pour valider et suivre les numéros de TVA et d’autres informations de société pour les clients, fournisseurs et contacts. Le service de [!INCLUDE [prod_short](includes/prod_short.md)] s’appelle **Services validation N° id. intracomm. Union européenne**. Il est disponible sur la page **Connexions au service**, et vous pouvez commencer à l’utiliser immédiatement. La connexion au service est gratuite, et aucune inscription supplémentaire n’est obligatoire.

## Configurer le service pour vérifier automatiquement les numéros d’identification intra-communautaire

Pour activer **Services validation N° id. intracomm. Union européenne**, ouvrez l’entrée sur la page **Connexion au service**. Si le champ **Point de terminaison de service** n’est pas déjà rempli, utilisez l’action **Définir le point de terminaison par défaut**. Puis définissez le champ **Activé**.  

> [!IMPORTANT]
> Pour activer le service de validation, vous devez disposer des autorisations de l’administrateur.

Vous pouvez éventuellement configurer des modèles pour les types de données liées à la TVA que vous souhaitez que le service vérifie également. Pour plus d’informations, consultez la section [Modèles de validation](#validation-templates).

Lorsque vous utilisez la connexion à notre service, nous enregistrons un historique des numéros de TVA et des vérifications pour chaque client, fournisseur ou contact dans le **Journal identif. intracomm** pour faciliter le suivi. Le journal est spécifique à chaque client. Par exemple, le journal est utile pour prouver que vous avez vérifié que le numéro de TVA actuel est correct. Lorsque vous vérifiez un numéro de TVA, la colonne **Identificateur de demande** du journal indique que vous avez effectué des actions.

Vous pouvez afficher le journal d’identification TVA sur les fiches client, fournisseur ou contact, sous le raccourci **Facturation**, en cliquant sur le bouton de recherche dans le champ **N° identif. intracomm.**  

Voici quelques points à noter concernant le service VIES de validation de numéros de TVA :

* Le service utilise le protocole http, ce qui signifie que les données transférées via le service ne sont pas cryptées.  
* Vous pouvez rencontrer des temps d’arrêt pour ce service dont Microsoft n’est pas responsable. Le service fait partie d’un vaste réseau de l’UE de registres de TVA nationaux.

> [!IMPORTANT]
> Il vous incombe de vérifier la validité des données. Parfois, des données comportant des erreurs sont renvoyées par le service VIES de validation des numéros de TVA. Si la validation échoue, validez les numéros d’identification TVA sur le [site web](https://ec.europa.eu/taxation_customs/vies/), imprimez le résultat ou enregistrez-le dans un emplacement partagé, puis ajoutez le lien vers l’enregistrement de votre client, fournisseur ou contact. Pour plus d’informations, voir [Gérer les pièces jointes, les liens et les notes sur les fiches et les documents](ui-how-add-link-to-record.md).

## Modèles de validation

Vous pouvez utiliser le service VIES pour vérifier également d’autres informations société, telles que l’adresse, ainsi que le numéro d’identification intra-communautaire. Dans la page **Modèles Validation n° identif. intracomm.**, créez une entrée pour chaque pays/région pour lequel vous souhaitez obtenir une validation supplémentaire, puis spécifiez les informations que vous souhaitez faire valider automatiquement.  

Par exemple, ajoutez une entrée pour l’Espagne dans laquelle vous souhaitez obtenir la validation du nom, de la rue, de la ville et du code postal, puis une autre entrée pour l’Allemagne où vous souhaitez simplement valider le code postal, par exemple. Puis, dans la page **Paramètres services validation N° id. intracomm. Union européenne**, spécifiez le modèle par défaut.  

> [!NOTE]
> Assurez-vous toujours que le modèle par défaut répond à vos besoins. Vous pouvez modifier la valeur par défaut pour qu’elle corresponde à vos besoins, comme obtenir la validation de tous les champs ou d’aucun champ.

La prochaine fois que vous spécifiez un numéro d’identification intra-communautaire, le service valide le numéro et toutes les données supplémentaires déterminées par vos modèles de validation. Si les valeurs spécifiées sont différentes des valeurs renvoyées par le service, vous verrez les détails dans la page **Détails de validation** sur laquelle vous pouvez accepter ou réinitialiser les valeurs.  

## Voir aussi

[Configuration de la TVA](finance-setup-vat.md)  
[Configuration de la TVA sur encaissement](finance-setup-unrealized-vat.md)  
[Déclarer la TVA à une autorité fiscale](finance-how-report-vat.md)  
[Utiliser la TVA sur les ventes et les achats](finance-work-with-vat.md)  
[Fonctionnalités locales dans Business Central](about-localization.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
