---
title: 如何：确定探测请求的发现版本
ms.date: 03/30/2017
ms.assetid: b3c4e2e2-2957-4074-ae6a-776a5ca84278
ms.openlocfilehash: 6bd112be311eb9397ad89801be5358d67c7499fd
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 04/18/2019
ms.locfileid: "59332269"
---
# <a name="how-todetermine-the-discovery-version-of-a-probe-request"></a>如何：确定探测请求的发现版本
发现代理可能会公开使用不同发现版本的多个发现终结点。 当 UDP 多播探测请求到达代理时，代理应响应一条多播禁止消息。 为此，它必须知道请求的发现版本。  
  
### <a name="to-determine-the-discovery-version-of-a-probe-request"></a>确定探测请求的发现版本  
  
1. 在响应探测请求的方法（例如 <xref:System.ServiceModel.Discovery.DiscoveryProxy.OnBeginFind%2A>）中，使用静态 <xref:System.ServiceModel.OperationContext.Current%2A> 属性搜索  <xref:System.ServiceModel.Discovery.DiscoveryOperationContextExtension>，如下面的代码所示。  
  
    ```  
    DiscoveryOperationContextExtension doce = OperationContext.Current.Extensions.Find<DiscoveryOperationContextExtension>();  
    // Access the discovery version from the DiscoveryOperationContextExtension  
    doce.DiscoveryVersion;  
    ```  
  
## <a name="see-also"></a>请参阅

- <xref:System.ServiceModel.Discovery.Configuration.AnnouncementEndpointElement.DiscoveryVersion%2A>
- [实现发现代理](../../../../docs/framework/wcf/feature-details/implementing-a-discovery-proxy.md)
