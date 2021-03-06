---
title: "Télécharger et installer le client Azure Information Protection"
description: "Instructions destinées aux utilisateurs pour installer le client Azure Information Protection pour Windows, afin de pouvoir classifier et protéger des documents et des e-mails."
author: cabailey
ms.author: cabailey
manager: mbaldwin
ms.date: 02/24/2017
ms.topic: article
ms.prod: 
ms.service: information-protection
ms.technology: techgroup-identity
ms.assetid: 2bf09690-9dba-43b7-9e0a-0110915d4081
ms.reviewer: eymanor
ms.suite: ems
translationtype: Human Translation
ms.sourcegitcommit: 92ad7198aad17664062b8d007fa95524fe535443
ms.openlocfilehash: d4820070aff013b42ee49f4c7b81e78ffbc7a049
ms.lasthandoff: 02/24/2017


---

# <a name="download-and-install-the-azure-information-protection-client"></a>Télécharger et installer le client Azure Information Protection

Si votre administrateur n’installe pas le client Azure Information Protection pour vous, vous pouvez le faire vous-même. Vous devez être un administrateur local de votre PC pour installer ce client, de sorte qu’il puisse étiqueter et protéger vos documents et vos e-mails.

De plus :

- Le client Azure Information Protection requiert une version minimale de Microsoft .NET Framework 4.6.2. Si cette version est manquante, le programme d’installation tente de télécharger et d’installer ce composant requis. Lorsque ce composant requis est installé dans le cadre de l’installation du client, votre ordinateur doit être redémarré.

- Si vous disposez de Windows 7 SP1, le client Azure Information Protection exige la mise à jour spécifique [KB 2533623](https://support.microsoft.com/kb/2533623). Si votre PC a besoin de cette mise à jour, mais qu’elle n’est pas installée, l’installation s’effectue, mais un message s’affiche vous indiquant que vous devez installer cette mise à jour avant de pouvoir utiliser toutes les fonctionnalités du client Azure Information Protection. 

## <a name="to-download-and-install-the-azure-information-protection-client"></a>Pour télécharger et installer le client Azure Information Protection    

1.  Accédez à la page [Microsoft Azure Information Protection](https://go.microsoft.com/fwlink/?LinkId=303970) sur le site web de Microsoft.

    Cette page inclut des liens pour tous les appareils les plus couramment utilisés, afin que vous puissiez facilement télécharger une application visionneuse si elle est nécessaire pour ouvrir des fichiers protégés. Si vous n’êtes pas un administrateur local de votre PC, vous pouvez toujours installer l’application de visionneuse pour Windows. Cependant, ces instructions concernent l’installation du client complet qui vous permet d’étiqueter et de protéger les fichiers. 

2. Recherchez la section **Client Azure Information Protection** et cliquez sur l’icône Windows. Cliquez sur **Télécharger** et enregistrez le fichier **AzInfoProtection.exe**.     

3. Exécutez le fichier exécutable qui a été téléchargé. Si vous êtes invité à continuer, cliquez sur **Oui**.    

4. Dans la page **Installer le client Azure Information Protection** :     
    - Sélectionnez l’option d’installation d’une stratégie de démonstration si vous ne pouvez pas vous connecter au cloud mais souhaitez évaluer l’expérience avec le côté client d’Azure Information Protection à l’aide d’une stratégie locale à des fins de démonstration. Lorsque votre client se connecte à un service Azure Information Protection, cette stratégie de démonstration est remplacée par la stratégie Azure Information Protection de votre organisation.    

    - Cliquez sur **J’accepte** quand vous avez lu les termes du contrat de licence.    

5. Si vous êtes invité à continuer, cliquez sur **Oui** et attendez que l’installation se termine.    

6. Cliquez sur **Fermer**. Avant de commencer à utiliser le client Azure Information Protection :    

    - Si votre ordinateur exécute Office 2010, redémarrez votre ordinateur et passez à la section suivante pour la dernière étape.    
        
    - Pour les autres versions d’Office, redémarrez toutes les applications Office et toutes les instances de l’Explorateur de fichiers. L’installation est à présent terminée. Vous pouvez désormais utiliser le client pour étiqueter et protéger vos documents et vos e-mails.    

### <a name="installing-the-azure-information-protection-client-with-office-2010"></a>Installation du client Azure Information Protection avec Office 2010    
Une fois le client Azure Information Protection installé à l’aide des instructions précédentes :    

1. Ouvrez Microsoft Word. Lorsque vous exécutez une application Office 2010 pour la première fois après avoir installé le client Azure Information Protection, une boîte de dialogue **Microsoft Azure Information Protection** s’affiche. Cette boîte de dialogue vous indique que des informations d’identification administrateur sont requises pour terminer la connexion.

2. Dans la boîte de dialogue **Microsoft Azure Information Protection**, cliquez sur **OK**.

3. Si une boîte de dialogue **Contrôle d’accès utilisateur** s’affiche, cliquez sur **Oui**, afin que le client Azure Information Protection puisse mettre à jour le registre.   
L’installation est à présent terminée. Vous pouvez désormais utiliser Azure Information Protection pour étiqueter et protéger vos documents et vos e-mails.

## <a name="other-instructions"></a>Autres instructions    
Plus d’instructions pratiques dans le guide de l’utilisateur Azure Information Protection :

- [Que voulez-vous faire ?](client-user-guide.md#what-do-you-want-to-do)

## <a name="additional-information-for-administrators"></a>Informations supplémentaires pour les administrateurs    
Consultez [Procédure d’installation du client Azure Information Protection pour les utilisateurs](client-admin-guide.md#how-to-install-the-azure-information-protection-client-for-users) dans le guide de l’administrateur.
 

[!INCLUDE[Commenting house rules](../includes/houserules.md)]  

