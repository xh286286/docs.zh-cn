---
title: 扩展性设计
ms.date: 10/22/2008
helpviewer_keywords:
- extending class libraries
- extensibility with class libraries in .NET Framework
- class library design guidelines [.NET Framework], extensibility
- class library extensibility [.NET Framework]
ms.assetid: 1cdb8740-871a-456c-9bd9-db96ca8d79b3
ms.openlocfilehash: 9e75ef433f3bd9af34e8dd40331a8267755e59fe
ms.sourcegitcommit: 965a5af7918acb0a3fd3baf342e15d511ef75188
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/18/2020
ms.locfileid: "94821380"
---
# <a name="designing-for-extensibility"></a>扩展性设计
设计框架的一个重要方面是确保已认真考虑框架的扩展性。 这需要您了解与各种扩展性机制相关的成本和好处。 本章可帮助您确定哪些可扩展性机制（子类、事件、虚拟成员、回调等）可以最大程度地满足您的框架的要求。  
  
 可以通过多种方式在框架中提供可扩展性。 它们的范围不太强大，但成本较低，且成本较高，但成本较高。 对于任何给定的扩展性要求，你应选择满足要求的成本最低的扩展性机制。 请记住，稍后可以添加更多的扩展性，但不会引入重大更改。  
  
## <a name="in-this-section"></a>本节内容  
 [未密封类](unsealed-classes.md)  
 [受保护成员](protected-members.md)  
 [事件和回调](events-and-callbacks.md)  
 [虚拟成员](virtual-members.md)  
 [抽象 (抽象类型和接口) ](abstractions-abstract-types-and-interfaces.md)  
 [用于实现抽象的基类](base-classes-for-implementing-abstractions.md)  
 [密封](sealing.md)  
 *部分©2005，2009 Microsoft Corporation。保留所有权利。*  
  
 *经许可重印皮尔逊教育，Inc. 的作者 [：从框架设计指导原则：用于可重复使用的 .Net 库的约定、惯例和模式; 第2版](https://www.informit.com/store/framework-design-guidelines-conventions-idioms-and-9780321545619) By Krzysztof Cwalina，Brad Abrams，通过 Addison-Wesley Professional 作为 Microsoft Windows 开发系列的一部分2008发布。*  
  
## <a name="see-also"></a>另请参阅

- [框架设计准则](index.md)
