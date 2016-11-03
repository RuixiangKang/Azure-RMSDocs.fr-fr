---
title: "Comparaison d’Azure Information Protection avec AD RMS | Azure Information Protection"
description: "Si vous connaissez ou avez déjà déployé Active Directory Rights Management Services (AD RMS), vous vous demandez peut-être ce qui le différencie d’Azure Information Protection en termes de fonctionnement et de configuration requise."
author: cabailey
manager: mbaldwin
ms.date: 10/05/2016
ms.topic: article
ms.prod: 
ms.service: information-protection
ms.technology: techgroup-identity
ms.assetid: 8123bd62-1814-4d79-b306-e20c1a00e264
ms.reviewer: esaggese
ms.suite: ems
translationtype: Human Translation
ms.sourcegitcommit: 4591d5c45104108ccf151bb1d7a9382652e585a6
ms.openlocfilehash: 36adf768bdb5a0937af3563665bbe139c86ff250


---

# Comparaison d’Azure Information Protection avec AD RMS

>*S’applique à : services AD RMS (Active Directory Rights Management Services), Azure Information Protection, Office 365*

Si vous connaissez ou avez déjà déployé Active Directory Rights Management Services (AD RMS), vous vous demandez peut-être ce qui le différencie d’Azure Information Protection en termes de fonctionnement et de configuration requise en tant que solution de protection des informations.

Voici quelques-unes des principales différences pour Azure Information Protection :

- **Aucune infrastructure de serveur nécessaire** : Azure Information Protection n’a pas besoin de serveurs et de certificats PKI supplémentaires, contrairement à AD RMS, car Microsoft Azure s’occupe de cela pour vous. Ainsi, cette solution cloud est plus rapide à déployer et plus facile à gérer.

- **Authentification basée sur le cloud** : Azure Information Protection utilise Azure AD pour l’authentification, à la fois pour les utilisateurs internes et les utilisateurs d’autres organisations. Ainsi, vos utilisateurs mobiles peuvent être authentifiés même s’ils ne sont pas connectés à votre réseau interne et il est plus facile de partager du contenu protégé avec les utilisateurs d’autres organisations. De nombreuses organisations disposent déjà de comptes d’utilisateur dans Azure AD, car elles exécutent des services Azure ou Office 365. Si ce n’est pas le cas, RMS for individuals permet aux utilisateurs de créer un compte gratuit. Pour partager du contenu protégé AD RMS avec une autre organisation, vous devez configurer des approbations explicites avec chaque organisation.

- **Prise en charge intégrée des appareils mobiles** : aucune modification du déploiement n’est nécessaire pour qu’Azure RMS prenne en charge des appareils mobiles et des ordinateurs Mac. Pour prendre en charge ces appareils avec AD RMS, vous devez installer l’extension Appareils mobiles, configurer les services AD FS pour la fédération et créer des enregistrements supplémentaires pour votre service DNS public.

- **Modèles par défaut** : Azure Information Protection crée deux modèles par défaut dès que le service de protection est activé. Ainsi, il est très facile de protéger immédiatement les données importantes. Il n’existe aucun modèle par défaut pour AD RMS.

- **Modèles départementaux** : Azure Information Protection prend en charge les modèles départementaux comme paramètre de configuration pour les modèles supplémentaires que vous créez. Ce paramètre vous permet de spécifier quels utilisateurs voient le modèle dans leurs applications clientes (telles que les applications Office). Ainsi, ils peuvent facilement sélectionner la stratégie appropriée que vous définissez pour différents groupes d’utilisateurs. AD RMS ne prend pas en charge les modèles départementaux.

- **Suivi des documents, révocation et notification par e-mail** : Azure Information Protection prend en charge ces fonctionnalités avec l’application de partage RMS, ce qui n’est pas le cas d’AD RMS.

- **Classification et étiquetage** : Azure Information Protection prend en charge ces fonctionnalités avec la barre Azure Information Protection qui est intégrée aux applications Office, contrairement à AD RMS.


De plus, Azure Information Protection étant un service cloud, il peut offrir des correctifs et de nouvelles fonctionnalités plus rapidement qu’une solution de serveur locale. Aucune nouvelle fonctionnalité n’est planifiée pour AD RMS dans Windows Server 2016.

Pour plus d’informations et pour connaître les autres différences, consultez le tableau suivant qui présente une comparaison côte à côte des fonctionnalités et avantages d’Azure Information Protection et d’AD RMS. Si vous avez des questions spécifiques concernant la sécurité, consultez la section [Contrôles de chiffrement pour la signature et le chiffrement](compare-azure-rms-ad-rms.md#cryptographic-controls-for-signing-and-encryption) dans cet article.

> [!NOTE]
> Pour faciliter la comparaison, certaines informations présentées ici reprennent celles de la rubrique [Configuration requise pour Azure Information Protection](../get-started/requirements-azure-rms.md). Cette source propose des informations de prise en charge et de version plus précises sur [!INCLUDE[aad_rightsmanagement_1](../includes/aad_rightsmanagement_1_md.md)].

|Azure Information Protection|AD RMS|
|-----------------------------------------------------------------------------------------|--------------------------------------------------------|
|Prend en charge les fonctionnalités de Gestion des droits relatifs à l'information (IRM) dans les services Microsoft Online Services tels qu'Exchange Online et SharePoint Online, ou encore Office 365.<br /><br />Prend également en charge les produits serveur Microsoft locaux, tels qu’Exchange Server, SharePoint Server et les serveurs de fichiers qui exécutent Windows Server et l’infrastructure de classification des fichiers (ICF).|Prend en charge les produits serveur Microsoft locaux, tels qu’Exchange Server, SharePoint Server et les serveurs de fichiers qui exécutent Windows Server et l’infrastructure de classification des fichiers (ICF).|
|Permet une approbation implicite entre des organisations et les utilisateurs de ces organisations. Cela signifie que le contenu protégé peut être partagé entre les utilisateurs au sein d’une même organisation ou entre plusieurs organisations quand ils disposent de [!INCLUDE[o365_1](../includes/o365_1_md.md)] ou d’[!INCLUDE[aad_rightsmanagement_1](../includes/aad_rightsmanagement_1_md.md)], ou quand ils s’inscrivent pour obtenir un compte RMS for individuals.|Les approbations doivent être définies explicitement dans une relation de point à point entre deux organisations à l’aide de domaines d’utilisateurs approuvés ou d’approbations fédérées que vous créez en utilisant les services AD FS (Active Directory Federation Services).|
|Fournit deux modèles de stratégies de droits par défaut qui limitent l'accès du contenu à votre propre organisation : un modèle qui permet d'afficher en lecture seule le contenu protégé et un autre qui offre des autorisations d'écriture ou de modification pour le contenu protégé.<br /><br />Vous pouvez également créer vos propres modèles personnalisés, qui comprennent des modèles par département qui sont visibles uniquement pour un sous-ensemble d'utilisateurs. Pour plus d’informations, consultez [Configuration de modèles personnalisés pour le service Azure Rights Management](../deploy-use/configure-custom-templates.md).<br /><br />En outre, les utilisateurs peuvent définir leur propre jeu d'autorisations si les modèles ne suffisent pas.|Il n'existe aucun modèle de stratégie des droits par défaut ; vous devez les créer, puis les distribuer. Pour plus d'informations, consultez la page [Considérations relatives au modèle de stratégie AD RMS](http://go.microsoft.com/fwlink/?LinkId=154765).<br /><br />En outre, les utilisateurs peuvent définir leur propre jeu d'autorisations si les modèles ne suffisent pas.|
|La version minimale prise en charge de Microsoft Office est Office 2010, qui nécessite l’[application de partage RMS](../rms-client/sharing-app-windows.md).<br /><br />Microsoft Office pour Mac :<br /><br />- Microsoft Office pour Mac 2016 : pris en charge<br /><br />- Microsoft Office pour Mac 2011 : non pris en charge|La version minimale prise en charge de Microsoft Office est Office 2007.<br /><br />Microsoft Office pour Mac :<br /><br />- Microsoft Office pour Mac 2016 : pris en charge<br /><br />- Microsoft Office pour Mac 2011 : pris en charge|
|Prend en charge l’[application de partage RMS](../rms-client/sharing-app-windows.md) pour ordinateurs et appareils mobiles Windows et Mac.<br /><br />De plus, l'application de partage RMS prend en charge les fonctionnalités suivantes :<br /><br />- Partage avec des personnes dans une autre organisation.<br /><br />- Notification par courrier électronique permettant à l’expéditeur de savoir quand quelqu’un tente d’ouvrir une pièce jointe protégée.<br /><br />- Site de suivi des documents permettant notamment aux utilisateurs de révoquer des documents.|Prend en charge l’[application de partage RMS](../rms-client/sharing-app-windows.md) pour ordinateurs et appareils mobiles Windows et Mac. Toutefois, le partage n'inclut pas le partage avec des personnes extérieures à l'organisation, les notifications par courrier électronique et le site de suivi de document permettant aux utilisateurs de révoquer des documents.|
|Tous les types de fichiers peuvent bénéficier d’une [protection native ou générique](../rms-client/sharing-app-admin-guide-technical.md#levels-of-protection-native-and-generic) à l’aide de l’application de partage RMS.<br /><br />Pour les autres applications, consultez le tableau dans [Applications prenant en charge la protection des données Azure Rights Management](../get-started/requirements-applications.md).|Tous les types de fichiers peuvent bénéficier d’une [protection native ou générique](../rms-client/sharing-app-admin-guide-technical.md#levels-of-protection-native-and-generic) à l’aide de l’application de partage RMS.<br /><br />Pour les autres applications, consultez le tableau dans [Applications prenant en charge la protection des données Azure Rights Management](../get-started/requirements-applications.md).|
|La version minimale prise en charge du client Windows est Windows 7.|La version minimale prise en charge du client Windows est Windows Vista Service Pack 2.|
|Les appareils mobiles pris en charge sont les appareils Windows Phone, Android, iOS et Windows RT.<br /><br />L'assistance par e-mail via les services RMS d'Exchange ActiveSync est également prise en charge sur toutes les plateformes mobiles acceptant ce protocole.|La prise en charge des appareils mobiles inclut Windows Phone, Android, iOS et Windows RT et nécessite [Active Directory Rights Management Services Mobile Device Extension](http://technet.microsoft.com/library/dn673574.aspx).<br /><br />Une assistance par courrier électronique à l'aide d'Exchange ActiveSync IRM est prise en charge sur toutes les plateformes d'appareils mobiles qui acceptent ce protocole.|
|Prend en charge l’authentification multifacteur (MFA) pour les ordinateurs et les appareils mobiles.<br /><br />Pour plus d’informations, consultez [Multi-Factor Authentication (MFA) et Azure Information Protection](../get-started/requirements-azure-ad.md#multi-factor-authentication-mfa-and-azure-rms).|Prend en charge l'authentification par carte à puce si IIS est configuré pour demander des certificats.|
|Prend en charge le mode de chiffrement 2 sans configuration supplémentaire, lequel permet de renforcer la sécurité des longueurs de clé et des algorithmes de chiffrement.<br /><br />Pour plus d’informations, consultez la section [Contrôles de chiffrement pour la signature et le chiffrement](#cryptographic-controls-for-signing-and-encryption) de cet article, ainsi que la page [Modes de chiffrement d’AD RMS](http://go.microsoft.com/fwlink/?LinkId=266659).|Prend en charge le mode de chiffrement 1 par défaut et requiert une configuration supplémentaire pour prendre en charge le mode de chiffrement 2 pour une sécurité renforcée.<br /><br />Pour plus d’informations, consultez la section [Contrôles de chiffrement pour la signature et le chiffrement](#cryptographic-controls-for-signing-and-encryption) de cet article, ainsi que la page [Modes de chiffrement d’AD RMS](http://go.microsoft.com/fwlink/?LinkId=266659).|
|Prend en charge la migration à partir d'AD RMS et, si nécessaire, vers AD RMS :<br /><br />- [Migration d’AD RMS vers Azure Information Protection](../plan-design/migrate-from-ad-rms-to-azure-rms.md)<br /><br />- [Désaffectation et désactivation d’Azure Information Protection](../deploy-use/decommission-deactivate.md)|Prend en charge la migration depuis Azure Information Protection et vers Azure Information Protection :<br /><br />- [Désaffectation et désactivation d’Azure Rights Management](../deploy-use/decommission-deactivate.md)<br /><br />- [Migration d’AD RMS vers Azure Information Protection](../plan-design/migrate-from-ad-rms-to-azure-rms.md)|
|Requiert une licence Azure Information Protection pour protéger le contenu. Aucune licence Azure Information Protection n’est nécessaire pour utiliser du contenu protégé par Azure Information Protection (y compris si les utilisateurs appartiennent à une autre organisation).<br /><br />Pour plus d’informations, consultez la [liste des fonctionnalités](https://www.microsoft.com/en-us/cloud-platform/azure-information-protection-features) sur le site Azure Information Protection.|Nécessite une licence RMS pour protéger du contenu et utiliser du contenu protégé par AD RMS.<br /><br />Pour plus d'informations sur les licences pour AD RMS, voir [Licences d'administration (ML) et licences d'accès client (CAL)](https://www.microsoft.com/en-us/Licensing/product-licensing/client-access-license.aspx) , mais contacter votre partenaire Microsoft ou un représentant de Microsoft pour des informations spécifiques.|

## Contrôles de chiffrement pour la signature et le chiffrement
Azure Information Protection utilise toujours la norme RSA 2048 pour le chiffrement de toutes les clés publiques et la norme SHA 256 pour les opérations de signature. Par comparaison, AD RMS prend en charge les normes RSA 1024 et RSA 2048, ainsi que les normes SHA 1 ou SHA 256 pour les opérations de signature.

Azure Information Protection et AD RMS utilisent la norme AES 128 pour le chiffrement symétrique.

Azure Information Protection est conforme à la norme FIPS 140-2, que votre clé de locataire soit créée et gérée par Microsoft (par défaut) ou que vous gériez vous-même votre propre clé de locataire (option BYOK). Pour plus d’informations sur la gestion de votre clé de locataire, consultez [Planification et implémentation de la clé de locataire Azure Rights Management](../plan-design/plan-implement-tenant-key.md).

## Étapes suivantes
Si vous envisagez de migrer d’AD RMS vers Azure Information Protection, consultez [Migration d'AD RMS vers Azure Rights Management](../plan-design/migrate-from-ad-rms-to-azure-rms.md)





<!--HONumber=Oct16_HO1-->

