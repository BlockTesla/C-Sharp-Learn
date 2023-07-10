# #我的学习笔记
## #计算机基础知识
### #关于.NET

通用类型系统（CTS）、虚拟执行系统（VES）和公共语言规范（CLS）是.NET框架的三个重要组成部分，它们分别有不同的作用和功能。

- 通用类型系统（CTS）是一种规范，它定义了.NET框架如何定义、使用和管理类型¹。它提供了一个面向对象的模型，支持在.NET框架上实现各种语言¹。它还定义了一组基本的数据类型，如布尔、字节、字符等¹。CTS中的两种主要类型是"""引用类型"""和"""值类"""型¹。引用类型的对象由对对象实际值的引用表示，而值类型的对象由其值表示¹。
- 虚拟执行系统（VES）是一个运行时环境，它负责执行.NET框架中的代码²。它将编译为中间语言（IL）的代码转换为特定平台的机器码，并提供内存管理、异常处理、安全检查等服务²。VES还支持跨语言调试和跨平台部署²。
- 公共语言规范（CLS）是一种规范，它定义了.NET框架中支持的语言之间的互操作性¹。它是CTS的子集，也就是说，CTS中的所有规则也适用于CLS，除非CLS规则更严格¹³。CLS通过定义一组开发人员可以确信在多种语言中都可用的功能来增强和确保语言的互用性³ 。如果一个组件只使用CLS中的规则生成，那么它就被认为是符合CLS的，也就是说，它可以被任何.NET框架支持的语言使用¹。

(1) 常规类型系统和公共语言规范 | Microsoft Learn. https://learn.microsoft.com/zh-cn/dotnet/standard/common-type-system.

(2) CTS、CLS、CLR分别作何解释？ - CSDN博客. https://blog.csdn.net/love_programmer/article/details/112002003.

(3) CTS，CLS，CLR解释 - 橙发 - 博客园. https://www.cnblogs.com/sandaman2019/p/11388033.html.


## ECMA-335 标准
### 公共语言基础结构 （CLI）

本标准定义了公共语言基础结构 （CLI），在该基础结构中，用多种高级语言编写的应用程序可以在不同的系统环境中执行，而无需重写这些应用程序以考虑这些环境的独特特征。本标准由以下部分组成：

- 分区 I：概念和体系结构 – 描述 CLI 的整体体系结构，并提供通用类型系统 （CTS）、虚拟执行系统 （VES） 和公共语言规范 （CLS） 的规范性描述。它还提供了元数据的信息性说明。
- 分区 II：元数据定义和语义 – 提供元数据的规范性描述：其物理布局（作为文件格式）、逻辑内容（作为一组表及其关系）及其语义（从假设的汇编程序 ilasm 中看到）。
- 分区 III：CIL 指令集 – 描述公共中间语言 （CIL） 指令集。

    { 类似于Java字节码 ，或者汇编 }

- 分区 IV：配置文件和库 – 提供 CLI 库的概述，以及它们分解到配置文件和库中的规范。配套文件 CLILibrary.xml 被视为此分区的一部分，但以 XML 格式分发，它提供了 CLI 库中每个类、值类型和接口的详细信息。
分区 V：调试交换格式 – 描述在 CLI 生产者和使用者之间交换调试信息的标准方法。
- 分区 VI：附件 – 包含一些用 CIL 汇编语言 （ILAsm） 编写的示例程序、有关汇编程序特定实现的信息、CIL 指令集的机器可读描述，可用于派生此汇编程序使用的部分语法以及操作 CIL 的其他工具，分区 IV 库设计中使用的一组指南， 和可移植性注意事项。