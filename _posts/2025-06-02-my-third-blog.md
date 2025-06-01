---
layout: single
title: 我的第三篇博客
date: 2025-06-01
categories: [博客, 技术]
tags: [Jekyll, GitHub Pages]
mathjax: true
---
{% if page.mathjax %}
{% include mathjax.html %}
{% endif %}

# 大家好！这是我的第三篇博客文章。

## 欧拉公式

欧拉公式是数学中一个非常美丽的公式，它将五个最重要的数学常数联系在一起：

$$
e^{i\pi} + 1 = 0
$$

这个公式中的 $ e $ 是自然对数的底数，$ i $ 是虚数单位，$ \pi $ 是圆周率，$ 1 $ 和 $ 0 $ 是基本的整数。欧拉公式在数学、物理学和工程学中都有广泛的应用。

---

## 矩阵运算基础

矩阵是数学和编程中非常重要的概念，尤其在机器学习、图形学等领域。矩阵可以看作一个二维数组，例如一个 2×3 的矩阵如下：

$$
\begin{bmatrix}
a_{11} & a_{12} & a_{13} \\
a_{21} & a_{22} & a_{23}
\end{bmatrix}
$$

---

## 矩阵乘法

矩阵乘法是矩阵运算中的一种常见操作。假设我们有两个矩阵 $ A $ 和 $ B $：

- $ A $ 是一个 $ m \times n $ 矩阵（$ m $ 行 $ n $ 列）。
- $ B $ 是一个 $ n \times p $ 矩阵（$ n $ 行 $ p $ 列）。

它们的乘积 $ C = A \times B $ 是一个 $ m \times p $ 矩阵，其中 $ C $ 的元素 $ c_{ij} $ 计算公式为：

$$
c_{ij} = \sum_{k=1}^{n} a_{ik} b_{kj}
$$

---

### 示例

举个例子，假设 $ A $ 和 $ B $ 如下：

$$
A = 
\begin{bmatrix}
1 & 2 \\
3 & 4
\end{bmatrix}, \quad 
B = 
\begin{bmatrix}
5 & 6 \\
7 & 8
\end{bmatrix}
$$

计算 $ C = A \times B $：

$$
C = 
\begin{bmatrix}
1 \times 5 + 2 \times 7 & 1 \times 6 + 2 \times 8 \\
3 \times 5 + 4 \times 7 & 3 \times 6 + 4 \times 8
\end{bmatrix}
=
\begin{bmatrix}
19 & 22 \\
43 & 50
\end{bmatrix}
$$

---

## 用 Python 实现矩阵乘法

下面是一个简单的 Python 代码块，实现两个矩阵的乘法：

```python
def matrix_multiply(A, B):
    # 获取矩阵的维度
    m = len(A)        # A 的行数
    n = len(A[0])     # A 的列数，B 的行数
    p = len(B[0])     # B 的列数
    
    # 初始化结果矩阵 C，维度为 m x p
    C = [[0 for _ in range(p)] for _ in range(m)]
    
    # 计算矩阵乘法
    for i in range(m):
        for j in range(p):
            for k in range(n):
                C[i][j] += A[i][k] * B[k][j]
    
    return C

# 测试代码
A = [[1, 2], [3, 4]]
B = [[5, 6], [7, 8]]
C = matrix_multiply(A, B)

print("矩阵 A:")
for row in A:
    print(row)
print("矩阵 B:")
for row in B:
    print(row)
print("矩阵 C = A × B:")
for row in C:
    print(row)
```