---
layout: post
title: "想成为排列的数组"
permalink: /刷题模块/OJ/牛客/寒假训练营2025/第一场/div4_{贪心;计数;技巧}_牛客_想成为排列的数组.md/
date: 2025-01-22
author: "JNMC孙国庆"
---

#### [备用返回通道](../../README.md)

**题目链接**：[牛客网](https://ac.nowcoder.com/acm/contest/95323/G)
**时间限制**：C/C++/Rust/Pascal 1秒，其他语言2秒  
**空间限制**：C/C++/Rust/Pascal 256 M，其他语言512 M  
**64bit IO Format**：`%lld`
**题目描述**：
小红拿到了一个数组，她可以进行任意次以下操作：选择两个元素，使得其中一个加 1，另一个减 1。小红希望最终数组变成一个排列，请你帮助他确定这能否实现。如果可以实现的话，还需要求出最小操作次数。
长度为 $ n $ 的排列是由 $ 1 \sim n $ 这 $ n $ 个整数、按任意顺序组成的数组，其中每个整数恰好出现一次。例如，$\{2, 3, 1, 5, 4\}$ 是一个长度为 5 的排列，而 $\{1, 2, 2\}$ 和 $\{1, 3, 4\}$ 都不是排列，因为前者存在重复元素，后者包含了超出范围的数。
**输入描述**:
- 第一行输入一个整数 $ n $ ($ 1 \leq n \leq 10^5 $) 代表数组中的元素数量。
- 第二行输入 $ n $ 个整数 $ a_1, a_2, \ldots, a_n $ ($ -10^9 \leq a_i \leq 10^9 $) 代表数组元素。
**输出描述**:
如果无法生成排列，直接输出 `-1`；否则，输出一个整数，代表最小的操作次数。
**示例1**  
**输入**:
```
2
3 4
```
**输出**:
```
-1
```
**说明**:
在这个样例中，长度为 2 的排列有且仅有 $\{1, 2\}$ 和 $\{2, 1\}$ 两种，显然小红无论如何都无法将给定的数组变成这两种排列中的任意一种。
**示例2**  
**输入**:
```
4
0 3 4 3
```
**输出**:
```
1
```
**说明**:
在这个样例中，其中一种操作方式是同时将第一个元素加 1、第四个元素减 1，得到 $\{1, 3, 4, 2\}$，这是一个合法的排列。操作方案不唯一。

---
## 思路引导