---
title: 实现服务协定
ms.date: 03/30/2017
helpviewer_keywords:
- implementing service contracts [WCF]
ms.assetid: aefb6f56-47e3-4f24-ab0a-9bc07bf9885f
ms.openlocfilehash: 766e0c4d30a4fa0eed9ce154ca932f5371a43211
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 04/18/2019
ms.locfileid: "59196315"
---
# <a name="implementing-service-contracts"></a>实现服务协定
服务是一个类，会在一个或多个终结点公开客户端可用的功能。 若要创建服务时，编写实现 Windows Communication Foundation (WCF) 协定的类。 可以通过两种方法执行此操作。 可以将协定单独定义为接口，然后创建一个实现该接口的类。 或者，可以通过将 <xref:System.ServiceModel.ServiceContractAttribute> 属性放在该类本身，将 <xref:System.ServiceModel.OperationContractAttribute> 属性放在服务的客户端可用的方法上，来直接创建类和协定。  
  
## <a name="creating-a-service-class"></a>创建服务类  
 下面的示例是实现已单独定义的 `IMath` 协定的服务。  
  
```csharp  
// Define the IMath contract.  
[ServiceContract]  
public interface IMath  
{  
    [OperationContract]   
    double Add(double A, double B);  
  
    [OperationContract]  
    double Multiply (double A, double B);  
}  
  
// Implement the IMath contract in the MathService class.  
public class MathService : IMath  
{  
    public double Add (double A, double B) { return A + B; }  
    public double Multiply (double A, double B) { return A * B; }  
}  
```  
  
 或者，服务可以直接公开协定。 下面的示例是定义和实现 `MathService` 协定的服务类。  
  
```csharp  
// Define the MathService contract directly on the service class.  
[ServiceContract]  
class MathService  
{  
    [OperationContract]  
    public double Add(double A, double B) { return A + B; }  
    [OperationContract]  
    private double Multiply (double A, double B) { return A * B; }  
}  
```  
  
 请注意，上面的服务公开不同的协定，因为协定名称是不同的。 在第一个示例中，公开的协定命名为“`IMath`”，而在第二个示例中，协定命名为“`MathService`”。  
  
 您可以在服务和操作实现级别设置一些配置，如并发性和实例化。 有关详细信息，请参阅[设计和实现服务](../../../docs/framework/wcf/designing-and-implementing-services.md)。  
  
 在实现服务协定后，必须为该服务创建一个或多个终结点。 有关详细信息，请参阅[终结点创建概述](../../../docs/framework/wcf/endpoint-creation-overview.md)。 有关如何运行服务的详细信息，请参阅[托管服务](../../../docs/framework/wcf/hosting-services.md)。  
  
## <a name="see-also"></a>请参阅

- [设计和实现服务](../../../docs/framework/wcf/designing-and-implementing-services.md)
- [如何：使用协定类创建服务](../../../docs/framework/wcf/feature-details/how-to-create-a-wcf-contract-with-a-class.md)
- [如何：使用协定接口创建服务](../../../docs/framework/wcf/feature-details/how-to-create-a-service-with-a-contract-interface.md)
- [指定服务运行时行为](../../../docs/framework/wcf/specifying-service-run-time-behavior.md)
