---
title: "CoUninitializeEE 函数"
ms.custom: 
ms.date: 03/30/2017
ms.prod: .net-framework
ms.reviewer: 
ms.suite: 
ms.technology: dotnet-clr
ms.tgt_pltfrm: 
ms.topic: reference
api_name: CoUninitializeEE
api_location: mscoree.dll
api_type: DLLExport
f1_keywords: CoUninitializeEE
helpviewer_keywords: CoUninitializeEE function [.NET Framework hosting]
ms.assetid: 5f5a311a-839a-465f-89d9-ff1c74da9736
topic_type: apiref
caps.latest.revision: "11"
author: rpetrusha
ms.author: ronpet
manager: wpickett
ms.workload: dotnet
ms.openlocfilehash: 4125a76ae50a293e35e326f775500c06120420d1
ms.sourcegitcommit: 16186c34a957fdd52e5db7294f291f7530ac9d24
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 12/22/2017
---
# <a name="couninitializeee-function"></a>CoUninitializeEE 函数
`CoUninitializeEE`已过时，不提供任何功能。  
  
## <a name="syntax"></a>语法  
  
```  
void CoUninitializeEE (  
    BOOL fFlags  
);  
```  
  
## <a name="remarks"></a>备注  
 公共语言运行时执行引擎无法从进程中卸载。 若要关闭的情况下执行引擎调用[CorExitProcess](../../../../docs/framework/unmanaged-api/hosting/corexitprocess-function.md)。  
  
## <a name="see-also"></a>请参阅  
 [CoInitializeEE 函数](../../../../docs/framework/unmanaged-api/hosting/coinitializeee-function.md)  
 [元数据全局静态函数](../../../../docs/framework/unmanaged-api/metadata/metadata-global-static-functions.md)
