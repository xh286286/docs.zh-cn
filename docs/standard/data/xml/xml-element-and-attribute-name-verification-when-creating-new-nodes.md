---
title: 创建新节点时的 XML 元素和属性名验证
ms.date: 03/30/2017
ms.assetid: b489f647-a175-4659-ada4-170058bb41d0
ms.openlocfilehash: 0678f7daf5276a905ce890a5f6a0f64993fb08b0
ms.sourcegitcommit: 965a5af7918acb0a3fd3baf342e15d511ef75188
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/18/2020
ms.locfileid: "94828812"
---
# <a name="xml-element-and-attribute-name-verification-when-creating-new-nodes"></a>创建新节点时的 XML 元素和属性名验证
XML 文档对象模型 (DOM) 在创建新元素节点或属性节点时检查名称的有效性。 如果名称包含非法字符，则将引发异常。 若要确保名称有效且编码正确，需要使用 XmlConvert  类，在应用一级对名称进行编码和解码。 XmlWriter  包含执行附加操作的方法，以确保生成格式标准的 XML。  
  
## <a name="see-also"></a>请参阅

- [XML 文档对象模型 (DOM)](xml-document-object-model-dom.md)
