---
title: “ICor调试异常调试事件”接口
ms.date: 03/30/2017
ms.assetid: f9ba60d8-b54d-417e-bb3e-fde4b41ca44c
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 2e2a147d46412eb4feb192070ff8420cab842a6c
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 04/18/2019
ms.locfileid: "59156450"
---
# <a name="icordebugexceptiondebugevent-interface"></a>“ICor调试异常调试事件”接口
扩展了[icor 调试调试事件](../../../../docs/framework/unmanaged-api/debugging/icordebugdebugevent-interface.md)接口以支持异常事件。  
  
## <a name="methods"></a>方法  
  
|方法|描述|  
|------------|-----------------|  
|[GetFlags 方法](../../../../docs/framework/unmanaged-api/debugging/icordebugexceptiondebugevent-getflags-method.md)|获取指示是否可拦截异常的标志。|  
|[GetNativeIP 方法](../../../../docs/framework/unmanaged-api/debugging/icordebugexceptiondebugevent-getnativeip-method.md)|获取此异常调试事件的本机接口指针。|  
|[GetStackPointer 方法](../../../../docs/framework/unmanaged-api/debugging/icordebugexceptiondebugevent-getstackpointer-method.md)|获取此异常调试事件的堆栈指针。|  
  
## <a name="remarks"></a>备注  
 `ICorDebugExceptionDebugEvent` 接口由以下事件类型实现：  
  
-   [MANAGED_EXCEPTION_FIRST_CHANCE](../../../../docs/framework/unmanaged-api/debugging/cordebugrecordformat-enumeration.md)  
  
-   [MANAGED_EXCEPTION_USER_FIRST_CHANCE](../../../../docs/framework/unmanaged-api/debugging/cordebugrecordformat-enumeration.md)  
  
-   [MANAGED_EXCEPTION_CATCH_HANDLER_FOUND](../../../../docs/framework/unmanaged-api/debugging/cordebugrecordformat-enumeration.md)  
  
-   [MANAGED_EXCEPTION_UNHANDLED](../../../../docs/framework/unmanaged-api/debugging/cordebugrecordformat-enumeration.md)  
  
> [!NOTE]
>  此接口仅适用于 .NET Native。 尝试调用 `QueryInterface` 来检索接口指针会为 .NET Native 外部的 ICorDebug 方案返回 `E_NOINTERFACE`。  
  
## <a name="requirements"></a>要求  
 **平台：** 请参阅[系统需求](../../../../docs/framework/get-started/system-requirements.md)。  
  
 **标头：** CorDebug.idl、 CorDebug.h  
  
 **库：** CorGuids.lib  
  
 **.NET Framework 版本：**[!INCLUDE[net_46_native](../../../../includes/net-46-native-md.md)]  
  
## <a name="see-also"></a>请参阅

- [调试接口](../../../../docs/framework/unmanaged-api/debugging/debugging-interfaces.md)
- [调试](../../../../docs/framework/unmanaged-api/debugging/index.md)
