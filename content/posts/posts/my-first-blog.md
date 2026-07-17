---
title: "我的算法学习第一天：从零搭建技术博客"
date: 2026-07-18
categories: ["学习日记"]
tags: ["GitHub", "博客", "算法"]
---

## 🚀 今天做了什么

今天是我下定决心系统学习算法的第一天，我做了两件事：

### 1. 搭建了属于自己的技术博客
我用 GitHub Pages + Hugo 模板，0成本搭建了这个博客。以后这里会记录我学习算法的每一步。

### 2. 立下 Flag
**坚持写 30 篇算法学习笔记，每篇至少包含一道 LeetCode 题解。**

## 💻 今天学到的算法：二分查找

二分查找是最基础的算法之一，它的核心思想是**每次排除一半的搜索范围**。

### 关键点
- 必须是有序数组
- 注意边界条件（left <= right 还是 left < right）

### Python 代码实现
```python
def binary_search(nums, target):
    left, right = 0, len(nums) - 1
    while left <= right:
        mid = (left + right) // 2
        if nums[mid] == target:
            return mid
        elif nums[mid] < target:
            left = mid + 1
        else:
            right = mid - 1
    return -1
