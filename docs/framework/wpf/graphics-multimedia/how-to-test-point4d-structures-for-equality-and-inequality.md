---
title: "如何：测试 Point4D 结构是否相等和不相等"
ms.custom: 
ms.date: 03/30/2017
ms.prod: .net-framework
ms.reviewer: 
ms.suite: 
ms.technology: dotnet-wpf
ms.tgt_pltfrm: 
ms.topic: article
helpviewer_keywords:
- inequality [WPF], testing Point4D structures for
- equality [WPF], testing Point4D structures for
- testing [WPF], Point4D structures for equality
- Point4D structures [WPF], testing for inequality
- testing [WPF], Point4D structures for inequality
- Point4D structures [WPF], testing for equality
ms.assetid: e004a67e-db7f-4af8-a31f-e6b2a44ccf34
caps.latest.revision: "8"
author: dotnet-bot
ms.author: dotnetcontent
manager: wpickett
ms.workload: dotnet
ms.openlocfilehash: ac69ec232485ebd3097f2db3b31d3fd43d0ccc99
ms.sourcegitcommit: 16186c34a957fdd52e5db7294f291f7530ac9d24
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 12/22/2017
---
# <a name="how-to-test-point4d-structures-for-equality-and-inequality"></a>如何：测试 Point4D 结构是否相等和不相等
此示例演示如何测试<xref:System.Windows.Media.Media3D.Point4D>等式和不等式的结构。  
  
 下面的代码演示如何测试<xref:System.Windows.Media.Media3D.Point4D>结构的相等性和不相等使用<xref:System.Windows.Media.Media3D.Point4D>相等的方法。  <xref:System.Windows.Media.Media3D.Point4D>结构进行测试以使用重载的相等性的相等性 (`==`) 运算符，然后使用重载的不相等的不相等 (`!=`) 运算符，并最后<xref:System.Windows.Media.Media3D.Point3D>结构和<xref:System.Windows.Media.Media3D.Point4D>检查结构中的使用静态相等<xref:System.Windows.Media.Media3D.Point4D.Equals%2A>方法。  
  
## <a name="example"></a>示例  
 [!code-csharp[3DGallery_procedural_snip#Point4DEqualityExample_csharp](../../../../samples/snippets/csharp/VS_Snippets_Wpf/3DGallery_procedural_snip/CSharp/Misc3DOperationsExample.cs#point4dequalityexample_csharp)]  
  
## <a name="see-also"></a>请参阅  
 <xref:System.Windows.Media.Media3D.Point4D.op_Equality%2A>  
 <xref:System.Windows.Media.Media3D.Point4D.op_Inequality%2A>  
 <xref:System.Windows.Media.Media3D.Point4D.Equals%2A>
