---
title: '&lt;serviceTokenResolver&gt;'
ms.custom: 
ms.date: 03/30/2017
ms.prod: .net-framework
ms.reviewer: 
ms.suite: 
ms.technology: dotnet-clr
ms.tgt_pltfrm: 
ms.topic: article
ms.assetid: 6e9001e1-e064-4f47-84b2-46225c177746
caps.latest.revision: "8"
author: BrucePerlerMS
ms.author: bruceper
manager: mbaldwin
ms.workload: dotnet
ms.openlocfilehash: cd981c8e48f003060c74787fdd2f29557c07901d
ms.sourcegitcommit: 16186c34a957fdd52e5db7294f291f7530ac9d24
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 12/22/2017
---
# <a name="ltservicetokenresolvergt"></a>&lt;serviceTokenResolver&gt;
注册的服务令牌解析程序由标记处理程序集合中的处理程序。 服务的标记解析程序用于解析在传入令牌和消息上的加密令牌。  
  
 \<system.identityModel >  
\<identityConfiguration >  
\<securityTokenHandlers >  
\<securityTokenHandlerConfiguration >  
\<serviceTokenResolver >  
  
## <a name="syntax"></a>语法  
  
```xml  
<system.identityModel>  
  <identityConfiguration>  
    <securityTokenHandlers>  
      <securityTokenHandlerConfiguration>  
        <serviceTokenResolver type=xs:string>  
        </serviceTokenResolver>  
      </securityTokenHandlerConfiguration>  
    </securityTokenHandlers>  
  </identityConfiguration>  
</system.identityModel>  
```  
  
## <a name="attributes-and-elements"></a>特性和元素  
 下列各节描述了特性、子元素和父元素。  
  
### <a name="attributes"></a>特性  
  
|特性|描述|  
|---------------|-----------------|  
|类型|指定服务令牌解析程序的类型。 任一<xref:System.IdentityModel.Selectors.SecurityTokenResolver>类型或派生自类型<xref:System.IdentityModel.Selectors.SecurityTokenResolver>类。 有关如何指定详细信息`type`属性，请参阅 [自定义类型引用]。 必须的。|  
  
### <a name="child-elements"></a>子元素  
 无  
  
### <a name="parent-elements"></a>父元素  
  
|元素|描述|  
|-------------|-----------------|  
|[\<securityTokenHandlerConfiguration >](../../../../../docs/framework/configure-apps/file-schema/windows-identity-foundation/securitytokenhandlerconfiguration.md)|提供配置集合的安全令牌处理程序。|  
  
## <a name="remarks"></a>备注  
 服务的标记解析程序可以用于解析在传入令牌和消息上的加密令牌。 它用于检索应该用于解密传入令牌的密钥。 必须指定`type`属性。 指定的类型可以是<xref:System.IdentityModel.Selectors.SecurityTokenResolver>或派生自的自定义类型<xref:System.IdentityModel.Selectors.SecurityTokenResolver>类。  
  
 某些令牌处理程序，可以在配置中指定服务的标记解析程序设置。 对于单个令牌处理程序的设置会覆盖上的安全令牌的处理程序集合的指定。  
  
> [!NOTE]
>  指定`<serviceTokenResolver>`元素的子元素作为[ \<identityConfiguration >](../../../../../docs/framework/configure-apps/file-schema/windows-identity-foundation/identityconfiguration.md)元素已弃用，但仍支持向后兼容。 上的设置`<securityTokenHandlerConfiguration>`元素上会覆盖`<identityConfiguration>`元素。  
  
## <a name="example"></a>示例  
  
```xml  
<serviceTokenResolver type="MyNamespace.CustomTokenResolver, MyAssembly" />  
```
