---
title: ISymUnmanagedScope::GetNamespaces 方法
ms.date: 03/30/2017
api_name:
- ISymUnmanagedScope.GetNamespaces
api_location:
- diasymreader.dll
api_type:
- COM
f1_keywords:
- ISymUnmanagedScope::GetNamespaces
helpviewer_keywords:
- GetNamespaces method, ISymUnmanagedScope interface [.NET Framework debugging]
- ISymUnmanagedScope::GetNamespaces method [.NET Framework debugging]
ms.assetid: c44b0440-04bd-460a-84fb-41afecf44503
topic_type:
- apiref
author: mairaw
ms.author: mairaw
ms.openlocfilehash: 3dc3c842bbb4b86b82d03848751673400bed193b
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 04/18/2019
ms.locfileid: "59213033"
---
# <a name="isymunmanagedscopegetnamespaces-method"></a>ISymUnmanagedScope::GetNamespaces 方法
获取此范围内所使用的命名空间。  
  
## <a name="syntax"></a>语法  
  
```  
HRESULT GetNamespaces(  
    [in]  ULONG32  cNameSpaces,  
    [out] ULONG32  *pcNameSpaces,  
    [out, size_is(cNameSpaces),  
        length_is(*pcNameSpaces)]  
        ISymUnmanagedNamespace* namespaces[]);  
```  
  
## <a name="parameters"></a>参数  
 `cNameSpaces`  
 [in] `namespaces` 数组的大小。  
  
 `pcNameSpaces`  
 [out]一个指向`ULONG32`接收包含命名空间所需的缓冲区的大小。  
  
 `namespaces`  
 [out]接收这些命名空间数组。  
  
## <a name="return-value"></a>返回值  
 如果方法成功，则为 S_OK否则为 E_FAIL 或某些其他错误代码。  
  
## <a name="requirements"></a>要求  
 **标头：** CorSym.idl CorSym.h  
  
## <a name="see-also"></a>请参阅

- [ISymUnmanagedScope 接口](../../../../docs/framework/unmanaged-api/diagnostics/isymunmanagedscope-interface.md)
