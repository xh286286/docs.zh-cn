---
title: 类 - C# 编程指南
description: 了解类类型及其创建方式
ms.date: 08/21/2018
helpviewer_keywords:
- classes [C#]
- C# language, classes
ms.assetid: e8848524-7273-429f-8aba-c658d5eff5ad
ms.openlocfilehash: 8fa8d33ce9ece20a18c5c1542bc44cf569e9fa2e
ms.sourcegitcommit: 30a686fd4377fe6472aa04e215c0de711bc1c322
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/10/2020
ms.locfileid: "94440401"
---
# <a name="classes-c-programming-guide"></a>类（C# 编程指南）

## <a name="reference-types"></a>引用类型  

定义为 [类](../../language-reference/keywords/class.md)的一个类型是 *引用类型*。 在运行时，如果声明引用类型的变量，此变量就会一直包含值 [null](../../language-reference/keywords/null.md)，直到使用 [new](../../language-reference/operators/new-operator.md) 运算符显式创建类实例，或直到为此变量分配可能已在其他位置创建的兼容类型的对象，如下面的示例所示：

```csharp
//Declaring an object of type MyClass.
MyClass mc = new MyClass();

//Declaring another object of the same type, assigning it the value of the first object.
MyClass mc2 = mc;
```

创建对象时，在该托管堆上为该特定对象分足够的内存，并且该变量仅保存对所述对象位置的引用。 当分配托管堆上的类型和由 CLR 的自动内存管理功能对其进行回收（称为 *垃圾回收*）时，需要开销。 但是，垃圾回收已是高度优化，并且在大多数情况下，不会产生性能问题。 有关垃圾回收的详细信息，请参阅[自动内存管理和垃圾回收](../../../standard/garbage-collection/fundamentals.md)。  
  
## <a name="declaring-classes"></a>声明类

 使用后跟唯一标识符的 [class](../../language-reference/keywords/class.md) 关键字可以声明类，如下例所示：

 ```csharp
//[access modifier] - [class] - [identifier]
 public class Customer
 {
    // Fields, properties, methods and events go here...
 }
```

 `class` 关键字前面是访问级别。 因为此例中使用的是 [public](../../language-reference/keywords/public.md)，所以任何人都可以创建此类的实例。 类的名称遵循 `class` 关键字。 类名称必须是有效的 C# [标识符名称](../inside-a-program/identifier-names.md)。 定义的其余部分是类的主体，其中定义了行为和数据。 类上的字段、属性、方法和事件统称为 *类成员*。  
  
## <a name="creating-objects"></a>创建对象

虽然它们有时可以互换使用，但类和对象是不同的概念。 类定义对象类型，但不是对象本身。 对象是基于类的具体实体，有时称为类的实例。  
  
 可通过使用 [new](../../language-reference/operators/new-operator.md) 关键字，后跟对象要基于的类的名称，来创建对象，如：  

 ```csharp
 Customer object1 = new Customer();
 ```

 创建类的实例后，会将一个该对象的引用传递回程序员。 在上一示例中，`object1` 是对基于 `Customer` 的对象的引用。 该引用指向新对象，但不包含对象数据本身。 事实上，可以创建对象引用，而完全无需创建对象本身：  

```csharp
 Customer object2;
```

 不建议创建这样一个不引用对象的对象引用，因为尝试通过这类引用访问对象会在运行时失败。 但实际上可以使用这类引用来引用某个对象，方法是创建新对象，或者将其分配给现有对象，例如：  

 ```csharp
 Customer object3 = new Customer();
 Customer object4 = object3;
```
  
 此代码创建指向同一对象的两个对象引用。 因此，通过 `object3` 对对象做出的任何更改都会在后续使用 `object4` 时反映出来。 由于基于类的对象是通过引用来实现其引用的，因此类被称为引用类型。  
  
## <a name="class-inheritance"></a>类继承  

类完全支持继承，这是面向对象的编程的基本特点。 创建类时，可以继承自其他任何未定义为 [sealed](../../language-reference/keywords/sealed.md) 的类，而且其他类也可以继承自你的类并重写类虚方法。 此外，你可以实现一个或多个接口。

继承是通过使用 *派生* 来完成的，这意味着类是通过使用其数据和行为所派生自的 *基类* 来声明的。 基类通过在派生的类名称后面追加冒号和基类名称来指定，如：  

 ```csharp
 public class Manager : Employee
 {
     // Employee fields, properties, methods and events are inherited
     // New Manager fields, properties, methods and events go here...
 }
 ```

类声明基类时，会继承基类除构造函数外的所有成员。 有关详细信息，请参阅[继承](inheritance.md)。
  
与 C++ 不同，C# 中的类只能直接继承一个基类。 但是，因为基类本身可能继承自其他类，因此类可能间接继承多个基类。 此外，类可以支持实现一个或多个接口。 有关详细信息，请参阅[接口](../interfaces/index.md)。  
  
类可以声明为 [abstract](../../language-reference/keywords/abstract.md)（抽象）。 抽象类包含抽象方法，抽象方法包含签名定义但不包含实现。 抽象类不能实例化。 只能通过可实现抽象方法的派生类来使用该类。 与此相反，[sealed](../../language-reference/keywords/sealed.md)（密封）类不允许其他类继承。 有关详细信息，请参阅[抽象类、密封类和类成员](abstract-and-sealed-classes-and-class-members.md)。  
  
类定义可以在不同的源文件之间分割。 有关详细信息，请参阅[分部类和方法](partial-classes-and-methods.md)。  
  
## <a name="example"></a>示例

以下示例定义了一个公共类，该类包含一个[自动实现的属性](auto-implemented-properties.md)、一个方法和一个名为构造函数的特殊方法。 有关详细信息，请参阅[属性](properties.md)、[方法](methods.md)和[构造函数](constructors.md)主题。 然后使用 `new` 关键字实例化类的实例。  
  
[!code-csharp[Class Example](~/samples/snippets/csharp/programming-guide/classes-and-structs/class-example.cs)]
  
## <a name="c-language-specification"></a>C# 语言规范

[!INCLUDE[CSharplangspec](~/includes/csharplangspec-md.md)]  
  
## <a name="see-also"></a>请参阅

- [C# 编程指南](../index.md)
- [面向对象的编程](../../tutorials/intro-to-csharp/object-oriented-programming.md)
- [多态性](polymorphism.md)
- [标识符名称](../inside-a-program/identifier-names.md)
- [成员](members.md)
- [方法](methods.md)
- [构造函数](constructors.md)
- [终结器](destructors.md)
- [对象](objects.md)
