---
author: brentholtorf
ms.topic: include
ms.date: 03/15/2022
ms.author: bholtorf
ms.service: dynamics-365-business-central
---
Étant donné que les sociétés opérent dans un nombre croissant de pays/régions, il devient essentiel qu’elles puissent échanger et générer des informations financières dans plusieurs devises. La devise société (DS) est définie sur la page **Paramètres comptabilité** comme décrit dans l’article [Comprendre la comptabilité et le plan comptable](../finance-general-ledger.md). Une fois la devise société (DS) définie, elle sera représentée en tant que devise vide. Ainsi, lorsque le champ **Devise** est vide, cela signifie que la devise est DS.  

Ensuite, vous devez configurer des codes devise pour chaque devise que vous utilisez si vous achetez ou vendez dans des devises autres que votre devise société (DS). Des comptes bancaires peuvent également être créés à l’aide de devises. Il est possible d’enregistrer des transactions comptables dans différentes devises, cependant, la transaction comptable sera toujours validée dans la devise société (DS).

[!INCLUDE [finance-currencies-lcy](finance-currencies-lcy-note.md)]

Votre comptabilité est configurée pour utiliser votre devise société (DS), mais vous pouvez la configurer pour utiliser une autre devise avec un taux de change des devises. Si vous désignez une deuxième devise comme « devise report supplémentaire », [!INCLUDE[prod_short](prod_short.md)] enregistre automatiquement les montants d’état en DS et dans cette devise report supplémentaire pour chaque écriture comptable, ainsi que pour d’autres écritures, telles que les écritures TVA. Pour plus d’informations, voir [Configurer une devise report supplémentaire](../finance-how-setup-additional-currencies.md). La devise report supplémentaire est le plus souvent utilisée pour faciliter les états financiers pour les propriétaires qui résident dans des pays/régions utilisant des devises différentes de la devise société (DS).  

> [!IMPORTANT]
> Si vous souhaitez utiliser une devise de reporting supplémentaire pour le reporting financier, assurez-vous de bien comprendre les limites. Pour plus d’informations, voir [Configurer une devise report supplémentaire](../finance-how-setup-additional-currencies.md).

> [!NOTE]  
> Lorsque vous validez en comptabilité à l’aide d’un code devise, par exemple pour valider une dépense dans une feuille comptabilité à l’aide d’un code devise, la transaction est convertie en DS à l’aide du taux de change de la devise à la date comptabilisation. L’écriture comptable ne contiendra pas d’informations sur la devise utilisée, uniquement sa valeur en DS. Si vous voulez garder une trace de la devise d’origine, comme pour une facture, vous devez utiliser les documents de vente et d’achat ainsi que les comptes bancaires qui stockent les informations de code de devise pour les écritures.
