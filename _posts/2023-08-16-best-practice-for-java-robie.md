---
layout: post
title: Java进阶技巧
date: 2023-08-16
tags: java
---

## 集合操作

#### 💡 List 转换为 Array

```java

List<Integer> list = new ArrayList<>();
list.add(1);
list.add(2);
list.add(3);

//`list.stream()`：将 List 对象 `list` 转换为一个 Stream 对象，以便对其进行流式操作。
// `mapToInt(i -> i)`：在流中的每个元素上应用一个映射函数，将其转换为整数类型。在这里，使用 `mapToInt()` 方法将每个元素 `i` 转换为相同的整数值 `i`。
// `toArray()`：将流中的元素收集到一个数组中。由于 `mapToInt()` 方法将流中的元素转换为基本类型的整数，所以 `toArray()` 方法将返回一个 `int[]` 类型的数组。
int[] array = list.stream().mapToInt(i -> i).toArray();

```

[练习]
[2682. 找出转圈游戏输家](https://leetcode.cn/problems/find-the-losers-of-the-circular-game/)

---

#### 💡 创建 [m, n]的List

```java

// `IntStream.rangeClosed(m, n)`：创建一个 IntStream 对象，表示从 m 到 n（包括 m 和 n）的整数范围。`rangeClosed()` 方法会生成一个顺序递增的整数流，包含了指定范围内的所有值。
// `boxed()`：将 IntStream 转换为 Stream<Integer>。在这里，使用 `boxed()` 方法将 IntStream 中的每个原始 int 值包装成对应的包装类 Integer。
// `toList()`：将 Stream<Integer> 中的元素收集到一个 List<Integer> 对象中。`toList()` 方法是 Stream API 提供的一个收集器，它用于将 Stream 中的元素收集到一个 List 对象中。

List<Integer> consecutiveList = new ArrayList<>(
	IntStream.rangeClosed(m, n).boxed().toList()
);

```

[练习] 
[2682. 找出转圈游戏输家](https://leetcode.cn/problems/find-the-losers-of-the-circular-game/)