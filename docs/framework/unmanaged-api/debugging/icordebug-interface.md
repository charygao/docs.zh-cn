---
title: "ICorDebug 接口"
ms.custom: 
ms.date: 03/30/2017
ms.prod: .net-framework
ms.reviewer: 
ms.suite: 
ms.technology: dotnet-clr
ms.tgt_pltfrm: 
ms.topic: reference
api_name: ICorDebug
api_location: mscordbi.dll
api_type: COM
f1_keywords: ICorDebug
helpviewer_keywords: ICorDebug interface [.NET Framework debugging]
ms.assetid: 33f431d7-ab1a-494d-8af2-20ab15aba194
topic_type: apiref
caps.latest.revision: "20"
author: rpetrusha
ms.author: ronpet
manager: wpickett
ms.workload: dotnet
ms.openlocfilehash: 0ed0b3a8b42157f6a4fcbc6b4a05a416da736147
ms.sourcegitcommit: 16186c34a957fdd52e5db7294f291f7530ac9d24
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 12/22/2017
---
# <a name="icordebug-interface"></a>ICorDebug 接口
提供允许开发人员调试应用程序在公共语言运行时 (CLR) 环境中的方法。  
  
> [!NOTE]
>  在 Windows 95、 Windows 98 或 Windows ME，或在非 x86 平台 （例如 IA64 和 AMD64） 上不支持混合模式 （托管和本机代码） 调试。  
  
## <a name="methods"></a>方法  
  
|方法|描述|  
|------------|-----------------|  
|[CanLaunchOrAttach 方法](../../../../docs/framework/unmanaged-api/debugging/icordebug-canlaunchorattach-method.md)|确定是否可以在当前的计算机和运行时配置的上下文中启动新的进程或附加到给定的进程。|  
|[CreateProcess 方法](../../../../docs/framework/unmanaged-api/debugging/icordebug-createprocess-method.md)|将启动一个进程和调试器的控制之下其主线程。|  
|[DebugActiveProcess 方法](../../../../docs/framework/unmanaged-api/debugging/icordebug-debugactiveprocess-method.md)|将调试器附加到现有的进程。|  
|[EnumerateProcesses 方法](../../../../docs/framework/unmanaged-api/debugging/icordebug-enumerateprocesses-method.md)|获取正在调试的进程的枚举数。|  
|[GetProcess 方法](../../../../docs/framework/unmanaged-api/debugging/icordebug-getprocess-method.md)|返回"ICorDebugProcess"的对象与给定的进程 id。|  
|[Initialize 方法](../../../../docs/framework/unmanaged-api/debugging/icordebug-initialize-method.md)|初始化 `ICorDebug` 对象。|  
|[SetManagedHandler 方法](../../../../docs/framework/unmanaged-api/debugging/icordebug-setmanagedhandler-method.md)|指定托管事件的事件处理程序对象。|  
|[SetUnmanagedHandler 方法](../../../../docs/framework/unmanaged-api/debugging/icordebug-setunmanagedhandler-method.md)|指定非托管事件的事件处理程序对象。|  
|[Terminate 方法](../../../../docs/framework/unmanaged-api/debugging/icordebug-terminate-method.md)|终止`ICorDebug`对象。|  
  
## <a name="remarks"></a>备注  
 `ICorDebug`表示调试器进程的事件处理循环。 调试器必须等待[icordebugmanagedcallback:: Exitprocess](../../../../docs/framework/unmanaged-api/debugging/icordebugmanagedcallback-exitprocess-method.md)从在发布此接口之前正在调试的所有进程的回调。  
  
 `ICorDebug`对象是控制所有进一步托管调试的初始对象。 在.NET framework 1.0 和 1.1 版中，此对象是`CoClass`从 com。 创建对象 在.NET Framework 2.0 版中，此对象将不再`CoClass`对象。 它必须由创建[CreateDebuggingInterfaceFromVersion](../../../../docs/framework/unmanaged-api/hosting/createdebugginginterfacefromversion-function.md)函数，这是多区别版本。 此新的创建函数使客户端可以获取的特定实现`ICorDebug`，这也模拟了调试 API 的特定版本。  
  
> [!NOTE]
>  此接口不支持跨计算机或跨进程远程调用。  
  
## <a name="requirements"></a>惠?  
 **平台：**请参阅[系统要求](../../../../docs/framework/get-started/system-requirements.md)。  
  
 **标头：** CorDebug.idl、 CorDebug.h  
  
 **库：** CorGuids.lib  
  
 **.NET framework 版本：**[!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]  
  
## <a name="see-also"></a>请参阅  
 [调试接口](../../../../docs/framework/unmanaged-api/debugging/debugging-interfaces.md)
