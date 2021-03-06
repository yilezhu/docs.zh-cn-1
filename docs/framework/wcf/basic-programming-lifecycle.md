---
title: 基本编程生命周期
ms.date: 03/30/2017
helpviewer_keywords:
- service creation [WCF]
ms.assetid: 7cf21bfe-23bd-46aa-8033-609f851dbf76
ms.openlocfilehash: 6d9ea3b877e7c735cf789039b2a6956037372888
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 04/18/2019
ms.locfileid: "59330553"
---
# <a name="basic-programming-lifecycle"></a>基本编程生命周期
Windows Communication Foundation (WCF) 使应用程序通报它们是在同一计算机上，在 Internet 上或在不同的应用程序平台上。 本主题概述了生成 WCF 应用程序所需的任务。 有关工作示例应用程序，请参阅[入门教程](../../../docs/framework/wcf/getting-started-tutorial.md)。  
  
## <a name="the-basic-tasks"></a>基本任务  
 要执行的基本任务依次为：  
  
1. 定义服务协定。 服务协定指定服务的签名、服务交换的数据和其他协定要求的数据。 有关详细信息，请参阅[Designing Service Contracts](../../../docs/framework/wcf/designing-service-contracts.md)。  
  
2. 实现协定。 若要实现服务协定，请创建实现协定的类并指定运行时应具有的自定义行为。 有关详细信息，请参阅[实现服务协定](../../../docs/framework/wcf/implementing-service-contracts.md)。  
  
3. 通过指定终结点和其他行为信息来配置服务。 有关详细信息，请参阅[配置服务](../../../docs/framework/wcf/configuring-services.md)。  
  
4. 承载服务。 有关详细信息，请参阅[托管服务](../../../docs/framework/wcf/hosting-services.md)。  
  
5. 生成客户端应用程序。 有关详细信息，请参阅[生成客户端](../../../docs/framework/wcf/building-clients.md)。  
  
 尽管本节中的主题遵循此顺序，但是一些方案并不会从头开始。 例如，如果想要为预先存在的服务生成客户端，则从步骤 5 开始。 或者，如果您是在生成其他人要使用的服务，则可以跳过步骤 5。  
  
 熟悉开发服务协定后，您还可以阅读[扩展性介绍](../../../docs/framework/wcf/introduction-to-extensibility.md)。 如果您创建服务出现问题，请[WCF 疑难解答快速入门](../../../docs/framework/wcf/wcf-troubleshooting-quickstart.md)若要查看其他人是否有相同或类似问题。  
  
## <a name="see-also"></a>请参阅

- [实现服务协定](../../../docs/framework/wcf/implementing-service-contracts.md)
