---
title: "Comment créer une étiquette pour Azure Information Protection | Azure Rights Management"
description: 
author: cabailey
manager: mbaldwin
ms.date: 07/29/2016
ms.topic: article
ms.prod: azure
ms.service: rights-management
ms.technology: techgroup-identity
ms.assetid: 1b45faa5-0c9c-40d6-910a-f117e7b6e8a3
translationtype: Human Translation
ms.sourcegitcommit: 93444affe94b280db2c9e4e2960c6902e491dec6
ms.openlocfilehash: 26f22fb616f66332abf87501f782f1f8e8f0c013


---

# Comment créer une étiquette pour Azure Information Protection

>*S’applique à : Azure Information Protection (préversion)*

**[ Cette information est préliminaire et susceptible d'être modifiée. ]**

Même si Azure Information Protection est fourni avec des étiquettes par défaut que vous pouvez personnaliser, vous pouvez également créer vos propres étiquettes que les utilisateurs voient dans la barre Information Protection.

Vous pouvez ajouter une étiquette ou ajouter une sous-étiquette à une étiquette existante lorsque vous avez besoin d’un niveau supplémentaire de classification. Par exemple, l’étiquette **Secret**, qui se trouve dans la [stratégie par défaut](configure-policy-default.md), contient des sous-étiquettes.

Utilisez les instructions suivantes pour ajouter une étiquette à la stratégie Azure Information Protection.

1. Connectez-vous au [portail Azure](https://portal.azure.com).
 
2. Dans le menu hub, cliquez sur **Parcourir** et commencez à taper **Information** dans la zone Filtrer. Sélectionnez **Azure Information Protection**.

3. Dans le panneau **Azure Information Protection**, effectuez l’une des opérations suivantes :

    - Pour créer une étiquette, cliquez sur **Ajouter une nouvelle étiquette**.

    - Pour créer une sous-étiquette, cliquez avec le bouton droit ou sélectionnez le menu contextuel (**...**) de l’étiquette à laquelle vous souhaitez créer une sous-étiquette, puis cliquez sur **Ajouter une sous-étiquette**.

4. Dans le panneau **Étiquette** ou **Sous-étiquette**, sélectionnez les options que vous souhaitez pour cette nouvelle étiquette, puis cliquez sur **Enregistrer**.

    > [!NOTE]
    >Pour en savoir plus sur la configuration de la protection, consultez la rubrique [Comment configurer une étiquette pour appliquer la protection](configure-policy-protection.md).

5. Pour que les utilisateurs puissent voir ces modifications, cliquez dans le panneau **Azure Information Protection** sur **Publier**.

## Étapes suivantes

Pour plus d’informations sur la configuration de votre stratégie Azure Information Protection, utilisez les liens figurant dans la section [Configuration de la stratégie de votre organisation](configure-policy.md#configuring-your-organization-s-policy).  





<!--HONumber=Jul16_HO5-->

