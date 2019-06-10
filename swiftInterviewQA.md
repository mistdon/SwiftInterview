Swift面试问答

在该教程中，你将完成一系列Swift相关的面试问题和答案。

- 💻
	Swift 5
	iOS 12
	Xcode10

Swift只有四岁，但是它已经成为iOS开发的默认语言。随着Swift版本升级到5.0, 它逐渐变成一门复杂、强有力的，面向对象的、函数导向的语言。每一次版本发布都带来更多的变革。

但你真的了解Swift吗？在本文中，你将发现一些有趣的Swift面试题。

你可以用这些问题去测试候选人的Swift知识，或者用来测试自己的水平。如果你不知道问题的答案，没关系，每个问题后都附带答案，方便你来对比。

下面的问题可以分为三个层级:

- **入门**: 适合Swift的新手，你讲看到一或两本相关的书籍, 并在自己的APP中使用。

- **中级**: 适合对Swift有强烈的兴趣，并且已经读过大量的Swift相关的书籍，并且有Swift的开发经验。

- **高级**：适合最有经验的开发人员 - 喜欢彻底探索语言和使用尖端技术的人们。

在每一个等级中，又分为两种类型的题目:

- **编程问题**: 适合邮件编码测试，可能包含书写代码.(注：在国内包含上机测试，白板测试)

- **口头测试**：适合面对面的交流，主要测试现场对答的能力

在开始之前，先打开一个palyground，以便在你对照答案之前可以在书写代码以验证。我们已经在Xcode10.2和Swift5的环境下，完成了所有问题的测试。

### 开始编程问题

**问题1:**

查看以下代码:

```swift
struct Tutorial{
    var difficulty: Int = 1
}
var tutorial1 = Tutorial()
var tutorial2 = tutorial1
tutorial2.difficulty = 2
```

`tutorial1.difficulty`和`tutorial2.difficulty`的值分别是什么？如果`Tutorial`是class，会有什么不同？为什么？
<details>
<summary>查看答案</summary>
tutorial1.difficulty是1, 而tutorial2.difficulty是2.

Swift中的结构题是值类型, 你是从值拷贝到值，而不是class的引用，以下代码创建了tutorial1的拷贝, 并且把它赋值给tutorial2:   

var tutorial2 = tutorial1
对tutorial2的改变不会影响到tutorial1。
如果Tutorial是类,tutorial1.difficulty和tutorial2.difficulty都是2. 类在Swift中是引用类型，当你尝试更改tutorial1的一个属性，你将会看到它映射到tutorial2. 反之亦然
</details>