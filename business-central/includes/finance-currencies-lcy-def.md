---
author: brentholtorf
ms.topic: include
ms.date: 03/04/2024
ms.author: bholtorf
ms.service: dynamics-365-business-central
---
Si votre entreprise opère dans plusieurs pays ou régions, il est probablement important que vous puissiez faire des affaires dans plusieurs devises. Vous définissez votre devise locale (DL) sur la page **Paramètres comptabilité**. Par la suite, votre devise locale sera représentée comme une devise vierge sur les documents et les transactions. Lorsque le champ **Devise** est vide, la devise est DL.

La vidéo suivante explique comment configurer votre devise locale.

> [!VIDEO https://www.microsoft.com/videoplayer/embed/RW1iM1n]

Ensuite, vous devez configurer des codes devise pour chaque devise que vous utilisez si vous achetez ou vendez dans des devises autres que votre devise société (DS). Des comptes bancaires peuvent également être créés à l’aide de devises. Il est possible d’enregistrer des transactions comptables dans différentes devises, cependant, la transaction comptable sera toujours validée dans la devise société (DS).

[!INCLUDE [finance-currencies-lcy](finance-currencies-lcy-note.md)]

Votre comptabilité est configurée pour utiliser votre devise société (DS), mais vous pouvez la configurer pour utiliser une autre devise avec un taux de change des devises. Si vous désignez une deuxième devise comme devise report supplémentaire, [!INCLUDE[prod_short](prod_short.md)] enregistre automatiquement les montants d’état en DL et dans cette devise report supplémentaire pour chaque écriture comptable, ainsi que pour d’autres écritures, telles que les écritures TVA. Pour plus d’informations, voir [Configurer une devise report supplémentaire](../finance-how-setup-additional-currencies.md). La devise report supplémentaire est le plus souvent utilisée pour faciliter les états financiers pour les propriétaires qui résident dans des pays/régions utilisant des devises différentes de la devise société (DS).  

> [!IMPORTANT]
> Si vous souhaitez utiliser une devise de reporting supplémentaire pour le reporting financier, assurez-vous de bien comprendre les limites. Pour plus d’informations, voir [Configurer une devise report supplémentaire](../finance-how-setup-additional-currencies.md).

> [!NOTE]  
> Lorsque vous validez dans le grand livre en utilisant une devise étrangère, [!INCLUDE [prod_short](prod_short.md)] convertit la transaction en DL en utilisant le taux de change de la devise à la date de comptabilisation. L’écriture comptable ne contiendra pas d’informations sur la devise utilisée, uniquement sa valeur en DL. Pour garder une trace de la devise d’origine, utiliser les documents de vente et d’achat et les comptes bancaires qui stockent les informations de devise pour les écritures.
