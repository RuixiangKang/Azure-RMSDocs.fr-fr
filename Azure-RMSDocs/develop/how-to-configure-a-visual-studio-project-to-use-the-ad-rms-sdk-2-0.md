---
title: "Configurer Visual Studio| Azure RMS"
description: "Instructions sur la configuration d’un projet Visual Studio en vue d’utiliser RMS SDK 2.1."
keywords: 
author: bruceperlerms
ms.author: bruceper
manager: mbaldwin
ms.date: 02/23/2017
ms.topic: article
ms.prod: 
ms.service: information-protection
ms.technology: techgroup-identity
ms.assetid: 396A2C19-3A00-4E9A-9088-198A48B15289
audience: developer
ms.reviewer: shubhamp
ms.suite: ems
translationtype: Human Translation
ms.sourcegitcommit: 7068e0529409eb783f16bc207a17be27cd5d82a8
ms.openlocfilehash: fa884b43cef8183ec967cffb48a463ba8ba0f2fa


---

# <a name="configure-visual-studio"></a>Configurer Visual Studio

Cette rubrique contient des instructions sur la configuration d’un projet Visual Studio en vue d’utiliser Rights Management Services SDK 2.1.

## <a name="prerequisites"></a>Conditions préalables

-   [Installer le SDK](install-the-rms-sdk.md)

**Instructions**

### <a name="step-1-configure-a-visual-studio-project-to-use-rms-sdk-21"></a>Étape 1 : Configurer un projet Visual Studio pour utiliser RMS SDK 2.1

Ces instructions sont spécifiques à Microsoft Visual Studio 2010. Si vous utilisez une autre version de Microsoft Visual Studio, vos boîtes de dialogue de paramètres peuvent être légèrement différentes.

Ces instructions concernent la création d’une application 32 bits native.

1.  Ajoutez le répertoire Include de RMS SDK 2.1 à votre projet Visual Studio 2010.

    Sous **Propriétés de configuration**, sélectionnez **Répertoires VC++**, puis ajoutez le répertoire Include de RMS SDK 2.1 (**$(MSIPCSDKDIR)\\inc**) au champ **Répertoires Include**.

    ![Propriétés de configuration - Champ Répertoires Include](../media/include_directories.png)

2.  Ajoutez le répertoire des bibliothèques de RMS SDK 2.1 à votre projet Visual Studio 2010.

    Sous **Propriétés de configuration**, sélectionnez **Répertoires VC++**, puis ajoutez le répertoire des bibliothèques de RMS SDK 2.1 au champ **Répertoires de bibliothèques** de votre plateforme.

    -   Pour Win32, utilisez **$(MSIPCSDKDIR)\\lib**
    -   Pour x64, utilisez **$(MSIPCSDKDIR)\\lib\\x64**

    ![Propriétés de configuration - Champ Répertoires de bibliothèques](../media/library_directories.png)

3.  Ajoutez les fichiers de bibliothèque de RMS SDK 2.1 en tant que dépendances Visual Studio 2010.

    Sous **Éditeur de liens**, sélectionnez **Entrée**, puis ajoutez les fichiers de bibliothèque de RMS SDK 2.1 (**Msipc.lib** et **Msipc\_s.lib**) au champ **Dépendances supplémentaires**.

    ![Éditeur de liens - Fichiers de bibliothèque - Champ Dépendances](../media/additional_dependencies.png)

4.  Ajoutez la DLL de RMS SDK 2.1 en tant que DLL chargée en différé.

    Sous **Éditeur de liens**, sélectionnez **Entrée**, puis ajoutez le fichier DLL de RMS SDK 2.1 (**Msipc.dll**) au champ **Chargement différé des DLL**.

    ![Éditeur de liens - Champ Chargement différé des DLL](../media/delay_loaded.png)

5.  Créez des informations de version pour le fichier binaire créé.

    Sous **Explorateur de solutions**, sélectionnez **Fichiers de ressources**, puis ajoutez le nom du fichier binaire dans le champ **OriginalFileName**.

    ![Explorateur de solutions - Champ Fichiers de ressources](../media/original_file_name.png)

## <a name="related-topics"></a>Rubriques connexes

* [Installer le SDK](install-the-rms-sdk.md)

[!INCLUDE[Commenting house rules](../includes/houserules.md)]


<!--HONumber=Jan17_HO1-->


