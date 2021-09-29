# UML精粹

|  ![封面](./cover.jpg)   | 作者: [美] 马丁·福勒<br/>出版社: 电子工业出版社<br/>副标题: 标准对象建模语言简明指南<br/>原作名: UML Distilled: A Brief Guide to the Standard Object Modeling Language  |
| --- | :--- |


## 1. 简介
* ### 使用UML的方式
  * UML作为草稿
    > 作者几乎所有时候都把UML当作草稿
  * UML作为蓝图
    > 我相信这太难做好，而且会减慢开发速度。子系统接口级别的蓝图是合理的，但即使这样，你也应该预料到，当开发人员实现跨接口的交互时，可能要改变那些接口。逆向工程蓝图的价值依赖于工具。如果工具被用做动态的浏览器，会非常有帮助；如果工具生成一大堆文档，只会浪费更多的树木
  * UML作为编程语言
    > 把UML当做编程语言是一个美妙的主意，但我怀疑它很难被广泛接纳
* ### UML的13种官方图形类型
## 2. 开发过程
* 迭代和瀑布过程
* 预测性和自适应计划
  > 一个流派主张在需求过程本身上投入更多的精力;另一个流派主张需求剧烈变动是不可避免的。   
  > 你可以通过在早期冻结需求并且不允许变化来防止这个问题发生，但也有风险：交付的系统不再满足用户的需求。
* 为项目裁剪过程
* 为过程裁剪UML
## 3. 类图（基础）
 > 类图（class diagram）描述系统中的对象类型，以及存在于它们之间的各种静态关系。类图也展示类的性质和操作，以及应用于对象连接方式的约束。UML使用特性（feature）作为一个通用术语，覆盖了类的性质（property）和操作（operation）。
 * 性质（property）
   * 属性（attribute）
     * 语法：visibility name: tye multiplicity = default {property-string}
     * 例子：- name: String [1] = "Untitled" {readOnly}
   * 关联（association）
   * 属性和关联两者之间的关系
     > 性质虽然只是单个概念，但可以以两种十分不同的表示法出现：属性和关联。虽然在图中看起来十分不同，但实际上是同样的东西。    
     > 一般来说，我倾向于对小的东西使用属性，例如日期或布尔——一般来说，值类型。对于更重要的类，使用关联。
 * 操作（operation）
   * 语法：visibility name (parameter-list) : return-type {property-string}
 * 泛化（generalization）
   * 子类型化（或接口继承）
   * 子类化（或实现继承）
 * 注解符和注释
 * 依赖（dependency）
   > 如果改变一个元素——供应者（supplier）或目标——的定义会导致改变其他——客户（client）或源——类，两个元素之间就存在依赖（dependency）
 * 约束规则
## 4. 序列图
  > 当你要查看单个用例内若干对象的行为时，你应该使用序列图。序列图擅长于展示对象之间的协作；它们不太擅长于精确定义行为。
    * 风格
      * 中央控制（centralized control）[更简单]
      * 分布控制（distributed control）[创造了更多使用多态而不是使用条件逻辑的机会]
## 5. 类图：进阶概念
## 6. 对象图
  > 对象图（object diagram）是某时间点上的对象在系统中的快照。    
  > 对象图对于展示连接在一起的对象很有用。在许多情形下，虽然可以通过类图精确地定义结构，但该结构依然难以理解。此时，使用对象图会大有帮助。
## 7. 包图
  > 包图对大规模系统极其有用。通过包图可以获得系统主要元素之间的依赖关系。这些图形和常见的编程结构对应得很好。绘制包和依赖的图可以帮助你保持对应用依赖的控制
    * 包和依赖
	     * 应该没有环状依赖
	     * 依赖关系不是传递性的
	   * 包的分解
	     * 应用的分层结构：表现、领域、数据映射器和数据库
	     * 主题区域结构：租赁和资产
    * 实现包
	     * 接口和它的实现被分离到不同的包
## 8. 部署图
  > 部署图展示系统的物理布局，揭示哪个软件运行在哪个硬件上
## 9. 用例
  * 用例的内容
    > 用例是帮助理解系统功能需求的有价值的工具。在项目早期，应该粗略地描述每个用例，然后在开发该用例之前再去做更详细的版本。
  * 主成功场景（main success scenario）
  * 扩展（extension）
## 10. 状态机图
  > 转换（transition）表示从一个状态到另一个状态的转移。每个转换都有一个标签，标签有3个部分：trigger-signature[guard]/activity（触发器-签名[警戒条件]/活动）。所有部分都是可选的。trigger-signature通常是触发状态潜在改变的单个事件。guard，如果有的话，是对要执行的转换来说必须为真的布尔条件。activity是一些在转换期间要执行的行为。
## 11. 活动图
  > 活动图的长处在于这样一个事实：支持和鼓励并行行为。这使得活动图成为工作流和流程建模的一个很棒的工具
## 12. 通信图
  > 通信图（communication diagrams），交互图的一种，强调交互的各种参与者之间的数据链接。
## 13. 组合结构
  > 组合结构非常自然地适合展示组件及组件如何分解成部件，因此这个表示法大都在组件图中使用。
## 14. 组件图
  > 当你把系统分解成组件并要展示它们通过接口的相互关系时，或者把组件分解为更低级别的结构时，使用组件图。
