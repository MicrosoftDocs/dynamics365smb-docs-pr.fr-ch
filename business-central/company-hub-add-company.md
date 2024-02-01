---
title: Ajouter des entreprises à votre Hub Entreprise
description: "Découvrez comment ajouter des entreprises d’autres environnements Business\_Central à votre Hub Entreprise afin de pouvoir gérer le travail dans tous les environnements."
author: brentholtorf
ms.topic: conceptual
ms.search.keywords: 'accountant, accounting, company hub'
ms.search.form: '1151, 1155, 1166, 1165'
ms.date: 09/28/2023
ms.author: bholtorf
ms.service: dynamics-365-business-central
---
# <a name="add-companies-to-your-company-hub"></a>Ajouter des entreprises à votre Hub Entreprise

[!INCLUDE[azure-ad-to-microsoft-entra-id](~/../shared-content/shared/azure-ad-to-microsoft-entra-id.md)]

Avec le Hub Entreprise, vous pouvez accéder à votre travail à partir de plusieurs entreprises à partir de plusieurs environnements [!INCLUDE [prod_short](includes/prod_short.md)]. Vous pouvez ajouter manuellement des environnements et des entreprises si vos entreprises ne s’affichent pas automatiquement dans le Hub Entreprise.  

Sur la page de destination du Hub Entreprise, vous trouvez le menu **Configurer**, à partir duquel vous pouvez accéder à la page **Liens d’environnements**. Il suffit de sélectionner **Nouveau**, puis de renseigner les champs. [!INCLUDE [tooltip-inline-tip_md](includes/tooltip-inline-tip_md.md)]  

> [!NOTE]
> Vous pouvez connecter le Hub Entreprise à autant d’entreprises que vous le souhaitez. Cependant, vous ne pouvez connecter le Hub Entreprise qu’aux entreprises hébergées dans [!INCLUDE [prod_short](includes/prod_short.md)] en ligne.

## <a name="environment-links"></a>Liens d’environnements

Un lien d’environnement est une fiche sur laquelle vous spécifiez l’environnement [!INCLUDE [prod_short](includes/prod_short.md)] qui héberge une ou plusieurs entreprises dans lesquelles vous travaillez. Les données de la fiche de chaque environnement sont spécifiées par vous, et vous pouvez les modifier selon vos besoins. Toutefois, le champ **Liens d’environnement** est indispensable, car il vous permet d’accéder à la société dans [!INCLUDE [prod_short](includes/prod_short.md)]. Utilisez l’action **Tester la connexion** dans le ruban pour vérifier que vous avez saisi le bon lien. Le lien que vous devez saisir pointe vers l’environnement qui héberge la société que vous ajoutez et doit inclure l’ID Microsoft Entra ou le nom de domaine de l’organisation. Par exemple, s’il a spécifié un domaine tel que MyBusiness.com, le lien vers son instance [!INCLUDE [prod_short](includes/prod_short.md)] est ```https://businesscentral.dynamics.com/mybusiness.com?redirectedfromsignup=1```. Sinon, cela ressemblera à ceci : ```https://businesscentral.dynamics.com/1a23b456-789c-0123-45de-678910fg12h/production?redirectedfromsignup=1```  

Le lien est utilisé lorsque vous choisissez l’entreprise dans le Hub Entreprise.  

:::image type="content" source="media/company-hub-company-list-actions.png" alt-text="Actions pour une entreprise répertoriée dans le Hub Entreprise.":::

> [!TIP]
> Si vous travaillez dans la version d’essai gratuite de [!INCLUDE [prod_short](includes/prod_short.md)], il est facile d’ajouter les sociétés dans votre abonné. Vous pouvez trouver le lien d’environnement en copiant l’ID de Microsoft Entra à partir de la section **Dépannage** de la page Aide et support. Le nom de l’environnement est probablement la valeur par défaut, PRODUCTION. Ajoutez ces informations au champ **Lien d’environnement**, tel que ```https://businesscentral.dynamics.com/1a23b456-789c-0123-45de-678910fg12h/production?redirectedfromsignup=1```, puis choisissez **Tester la connexion**. La société d’évaluation sera ajoutée à la liste.
>
> Si vous êtes passé à la société d’essai de trente jours, Ma société, vous pouvez l’ajouter à la liste en choisissant l’action **Recharger/Recharger toutes les entreprises** dans la liste.

## <a name="load-companies"></a>Charger les entreprises

Lorsque vous avez ajouté vos environnements, vos entreprises s’affichent automatiquement. Cependant, si vous savez qu’une nouvelle société a été ajoutée à un environnement, vous pouvez choisir l’action **Recharger toutes les entreprises** pour actualiser la liste. Utilisez la même action pour actualiser les données de toutes vos entreprises.  

> [!TIP]
> Afin d’actualiser les données dans le Hub Entreprise, vous devez avoir accès aux données des entreprises dont les données proviennent.

## <a name="see-also"></a>Voir aussi

[Gérer le travail entre plusieurs entreprises dans le Hub Entreprise](company-hub.md)  
[Ressources pour l’Aide et le support](product-help-and-support.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
