---
title: "&lt;entries&gt; 的 &lt;add&gt;"
ms.custom: 
ms.date: 03/30/2017
ms.prod: .net-framework
ms.reviewer: 
ms.suite: 
ms.technology: dotnet-clr
ms.tgt_pltfrm: 
ms.topic: article
ms.assetid: 3af4805b-dc72-4f68-b168-da4fba8c6170
caps.latest.revision: "3"
author: dotnet-bot
ms.author: dotnetcontent
manager: wpickett
ms.workload: dotnet
ms.openlocfilehash: 1583ec3cab3ed43556dc066c1e4753ddf9845ef5
ms.sourcegitcommit: 16186c34a957fdd52e5db7294f291f7530ac9d24
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 12/22/2017
---
# <a name="ltaddgt-of-ltentriesgt"></a>&lt;entries&gt; 的 &lt;add&gt;
表示将筛选器映射到以前定义的客户端终结点的路由项。 与此筛选器匹配的消息将发送到此目标。  
  
 \<system.serviceModel >  
\<路由 >  
\<routingTables >  
\<表 >  
\<条目 >  
\<add>  
  
## <a name="syntax"></a>语法  
  
```xml
   <routing>      <filterTables>        <filterTable name="String">          <entries>            <add backupList="String"                 endpointName="String"                  filterName="String"                  priority="Integer" />          </entries>        </table>      </routingTables></routing>  
```  
  
```csharp  
```  
  
## <a name="attributes-and-elements"></a>特性和元素  
 下列各节描述了特性、子元素和父元素。  
  
### <a name="attributes"></a>特性  
  
|特性|描述|  
|---------------|-----------------|  
|backupList|一个字符串，指定对终结点备份列表的引用。|  
|endpoint（终结点）|一个字符串，指定对客户端终结点的引用，该终结点将接收与 `filterName` 特性所指定的筛选器匹配的消息。|  
|filterName|一个字符串，指定对筛选器元素的引用。|  
|priority|一个整数，指定此项的优先级。<br /><br /> 将根据优先级计算路由表中的项，0 表示优先级最低。 将同时计算某个特定优先级的所有项，如果未找到当前优先级的匹配项，将计算下一个优先级。<br /><br /> 此值为可选值。|  
  
### <a name="child-elements"></a>子元素  
 无。  
  
### <a name="parent-elements"></a>父元素  
  
|元素|描述|  
|-------------|-----------------|  
|[\<路由 >](../../../../../docs/framework/configure-apps/file-schema/wcf/routing.md)|一个包含路由映射项的配置节。|  
  
## <a name="see-also"></a>请参阅  
 <xref:System.ServiceModel.Routing.Configuration.RoutingSection?displayProperty=nameWithType>      
 <xref:System.ServiceModel.Routing.Configuration.FilterTableEntryElement?displayProperty=nameWithType> 
